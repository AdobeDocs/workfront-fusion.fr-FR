---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Création de l’interface utilisateur de l’extension personnalisée
description: Création de l’interface utilisateur de l’extension personnalisée
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 440
ht-degree: 0%

---


# Création de l’interface utilisateur de l’extension personnalisée

>[!NOTE]
>
>Cet article suppose que vous connaissez un peu les outils de développement logiciel.

Cette procédure décrit comment créer l’écran que les utilisateurs voient réellement et comment établir la **connexion (« poignée de main »)** avec Fusion.

Au cours de ce processus, il est important de rappeler que votre extension s’exécute dans deux cadres : le cadre masqué **enregistrement** et le cadre visible **IU**.

Pour plus d’informations sur les cadres associés aux extensions personnalisées, voir [Cadres inclus dans une extension d’interface utilisateur](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-01-overview.md#frames-included-in-a-ui-extension).

Pour obtenir des instructions sur la création du cadre d’enregistrement, voir [Créer un projet pour l’extensibilité de l’interface utilisateur](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md).

## Routage entre les deux trames

Les deux trames chargent la même `index.html` ; un petit routeur front-end décide du composant à afficher en fonction de l’URL.

1. Configurez les itinéraires dans `web-src/src/components/App.js`. L&#39;essentiel est :

   ```jsx
   import { HashRouter as Router, Routes, Route } from "react-router-dom";
   import ExtensionRegistration from "./ExtensionRegistration";
   import DashboardWidget from "./DashboardWidget";
   
   export default function App() {
     return (
       <Router>
         <Routes>
           {/* Background frame: registers the extension with Fusion */}
           <Route index element={<ExtensionRegistration />} />
           <Route path="index.html" element={<ExtensionRegistration />} />
   
           {/* Visible frame: the URL you returned from getWidget() */}
           <Route path="my-widget" element={<DashboardWidget />} />
         </Routes>
       </Router>
     );
   }
   ```

   Ces itinéraires sont mappés à la configuration précédente comme suit :

   * L’itinéraire par défaut (`index`) effectue le rendu de **`ExtensionRegistration`**, l’image masquée qui appelle `register(...)`.
   * L’itinéraire `my-widget` effectue le rendu de **`DashboardWidget`**, votre interface utilisateur visible. Cela correspond au `url: "/index.html#/my-widget"` que vous avez renvoyé à partir de `getWidget()` dans [la page précédente](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md).

   >[!NOTE]
   >
   > **Les itinéraires et l’URL du `getWidget` doivent être d’accord.** Si vous modifiez le nom de l’itinéraire, modifiez également le `url`, sinon Fusion chargera une page vierge.

1. Continuez pour [Terminer l’authentification à l’aide de `attach`](#complete-the-handshake-with-attach).

## Terminer l&#39;établissement de liaison avec `attach`

Il s’agit de la ligne la plus importante de votre interface utilisateur visible. Lorsque Fusion ouvre votre cadre d’interface utilisateur, il attend que ce cadre s’enregistre. Votre code s’enregistre en appelant `attach({ id })`.

**Si cet attribut est omis, Fusion expire** avec une erreur telle que *« en attente du message initial de l’iframe cible.«*

1. Ajoutez le code suivant à `web-src/src/components/DashboardWidget.js` :

   ```jsx
   import { useEffect, useState } from "react";
   import { attach } from "@adobe/uix-guest";
   import { extensionId } from "./Constants";
   
   export default function DashboardWidget() {
     const [connection, setConnection] = useState(null);
   
     useEffect(() => {
       // Tell Fusion this UI frame is ready. Required.
       attach({ id: extensionId })
         .then(setConnection)
         .catch((e) => console.error("attach failed", e));
     }, []);
   
     if (!connection) {
       return <p>Connecting to Fusion...</p>;
     }
   
     return <h2>Hello from my Fusion extension!</h2>;
   }
   ```

   Ce code effectue les opérations suivantes :

   * `attach({ id })` renvoie un **objet de connexion** une fois que Fusion répond. Nous vous recommandons d’enregistrer cet élément, car vous l’utiliserez à l’étape suivante pour lire le contexte que Fusion envoie.
   * Tant que la connexion n’est pas résolue, le raccourci « Connexion... » apparaît. Le message s’affiche.
   * Utilise le **même`extensionId`** que celui défini dans `Constants.js`.

   À ce stade, vous disposez d’une extension fonctionnelle : elle enregistre, joint et affiche un message. Tout ce qui suit concerne l’utilisation des données que Fusion vous donne.

1. Passez à [Lire le contexte Partages Fusion](#read-the-context-fusion-shares).

## Lire le contexte des partages Fusion

Une fois jointe, la connexion expose un **contexte partagé** avec des informations sur l’utilisateur, l’organisation et l’équipe actuels. Vous pouvez lire des valeurs individuelles avec `connection.sharedContext.get("<key>")` :

```jsx
const orgId = connection.sharedContext.get("imsOrgId");
const organization = connection.sharedContext.get("organization"); // full Fusion org
const user = connection.sharedContext.get("user");                 // full Fusion user
```

Cet exemple montre un exemple complet et réactif qui est également mis à jour lorsque l’utilisateur change d’organisation ou d’équipe :

```jsx
import { useEffect, useState } from "react";
import { attach } from "@adobe/uix-guest";
import { extensionId } from "./Constants";

const KEYS = ["imsOrgId", "imsUserId", "organization", "team", "user"];

function readContext(source) {
  // sharedContext behaves like a Map (.get); the change event gives a plain object.
  const get =
    typeof source.get === "function" ? (k) => source.get(k) : (k) => source[k];
  return Object.fromEntries(KEYS.map((k) => [k, get(k)]));
}

export default function DashboardWidget() {
  const [context, setContext] = useState(null);

  useEffect(() => {
    let cleanup = () => {};
    attach({ id: extensionId })
      .then((connection) => {
        // 1) initial values
        setContext(readContext(connection.sharedContext));

        // 2) react to org/team/user changes pushed by Fusion
        const onChange = (event) =>
          setContext(readContext(event?.detail?.context ?? connection.sharedContext));
        connection.addEventListener("contextchange", onChange);
        cleanup = () => connection.removeEventListener?.("contextchange", onChange);
      })
      .catch((e) => console.error("attach failed", e));
    return () => cleanup();
  }, []);

  if (!context) return <p>Connecting to Fusion...</p>;

  return (
    <div>
      <h2>{context.organization?.name ?? "No organization"}</h2>
      <p>Signed in as {context.user?.name} ({context.user?.email})</p>
      <p>IMS org: {context.imsOrgId}</p>
    </div>
  );
}
```

Souvenez-vous des points suivants :

* **Lire les valeurs initiales** à partir de `connection.sharedContext.get(key)` juste après `attach`.
* **Abonnez-vous à`contextchange`** pour rester synchronisé. Fusion déclenche cet événement chaque fois que l’organisation, l’équipe ou l’utilisateur actif change. Les nouvelles valeurs arrivent sur `event.detail.context`.

Pour obtenir la liste complète des clés et de ce qu’elles contiennent, reportez-vous à la [référence contextuelle de Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).

Pour poursuivre le processus de configuration de votre extension personnalisée, accédez à [Référence contextuelle de Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).
