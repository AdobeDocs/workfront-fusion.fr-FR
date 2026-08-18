---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Présentation de la démonstration d’une extension personnalisée
description: Présentation de la démonstration d’une extension personnalisée
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 964
ht-degree: 0%

---


# Présentation de la démonstration de la création d’une extension personnalisée dans Fusion

>[!NOTE]
>
>Cet article suppose que vous connaissez un peu les outils de développement logiciel.

Cette démonstration explique comment créer une extension personnalisée, la déployer et l’exécuter dans Fusion.

Comprend :

* Génère un modèle automatique d’application App Builder à partir du modèle Experience Cloud Shell générique.
* Reciblez l’application vers un point d’extension Fusion.
* Déployez l’application dans l’espace de travail d’évaluation.
* Activez les tests d’évaluation dans Fusion et affichez l’application en cours d’exécution.

Commencer à partir du modèle plutôt qu’un `--standalone-app` vide signifie que le Bootstrap de la SPA est généré pour vous : `index.js`, `exc-runtime.js`, `App.js` avec le routage et la `ErrorBoundary`, et un exemple de `ExtensionRegistration`. Les étapes en direct de la démonstration consistent à recibler la configuration et à modifier deux fichiers, ce qui est exactement la manière dont le vrai `fusion-uix-guest` a été créé.

>[!NOTE]
>
> **Time :** la démonstration en direct prend environ 10 minutes après la configuration de vos outils. Vous devez effectuer la configuration unique (Node 18/20, `aio` CLI, `aio login`) **avant** la démonstration. Pour obtenir des instructions, voir [Configurer des outils et un compte d’extension d’interface utilisateur](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md).


## Avant de commencer

Cela ne doit être effectué qu’une seule fois, et peut être effectué hors caméra avant votre démonstration.

```sh
node --version          # must be 18 or 20
aio --version           # @adobe/aio-cli installed
aio login               # signs you into your Adobe org
aio console org select  # pick the org you'll demo in (same org as Fusion)
```

Deux choses doivent être vraies dans l’organisation de démonstration :

* Le point d’extension `fusion/nav-organization/1` est intégré à l’organisation. S’il n’est pas intégré, le déploiement échoue avec l’erreur 1060. Pour plus d’informations, voir [Dépannage des extensions personnalisées](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md).
* La fonction des extensions personnalisées est activée sur l’hôte Fusion. (Cette fonctionnalité est activée par défaut). Étant donné que vous allez effectuer une démonstration d’une version d’évaluation plutôt que d’une version publiée, vous allez également activer le commutateur **Extensions d’évaluation** dans votre profil Fusion. (Ce commutateur est illustré à l’étape 7.) Fusion n’affiche que les extensions publiées jusqu’à ce que vous le fassiez.

## Étape 1 : générer l’application à partir du modèle générique

```sh
aio app init my-fusion-extension --template @adobe/generator-app-excshell
cd my-fusion-extension
```

* Sélectionnez **Créer un projet** lorsque vous y êtes invité, puis acceptez le nom suggéré.
* `@adobe/generator-app-excshell` est le modèle d’extension d’interface utilisateur générique **Experience Cloud Shell** et n’est pas spécifique au produit. Il met en œuvre une SPA complète et fonctionnelle sous `src/dx-excshell-1/`.

>[!NOTE]
>
>Si vous préférez le menu, exécutez `aio app init my-fusion-extension`, choisissez **Ajouter des extensions ou une application autonome** > **Modèles**, puis sélectionnez **« Extension UIX App Builder pour Experience Cloud Shell »**.

Vous obtiendrez un ensemble de fichiers, y compris les suivants :

```
my-fusion-extension/
|-- app.config.yaml
|-- src/dx-excshell-1/
    |-- ext.config.yaml
    |-- web-src/src/
        |-- index.js          // SPA bootstrap (exc-app Runtime + React render)
        |-- exc-runtime.js    // Experience Cloud Shell runtime glue
        |-- components/
            |-- App.js                    // Router + ErrorBoundary (generated)
            |-- ExtensionRegistration.js  // sample registration (generated)
```

## Étape 2 : ajouter la bibliothèque invitée Fusion

Le modèle comprend déjà React, React Spectrum et exc-app. Ajoutez la bibliothèque qui communique avec l’hôte Fusion :

```sh
npm install @adobe/uix-guest
```

## Étape 3 : reciblage de la configuration sur Fusion

Ouvrez **`app.config.yaml`** et modifiez **uniquement la clé du point d’extension** du point d’interface d’Experience Cloud vers celui de Fusion (laissez le chemin d’accès au `$include` en l’état) :

```yaml
extensions:
  fusion/nav-organization/1:                 # was: dx/excshell/1
    $include: src/dx-excshell-1/ext.config.yaml
```

Vous n’avez rien à modifier d’autre dans la configuration. Le nom de dossier `dx-excshell-1` est interne et n’a aucune incidence sur Fusion. Vous pouvez donc le laisser. Renommer signifie également mettre à jour les chemins d’accès aux actions. Ignorez cette étape pour la démonstration.

>[!NOTE]
>
>Si vous ciblez la section **Équipe**, utilisez plutôt `fusion/nav-team/1`. Pour expédier **à la fois** organisation et équipe en production, utilisez **deux projets distincts**. Un lot de point d’extension par nom de registre évite une collision entre applications partagées.

## Étape 4 : Modifier les fichiers d’enregistrement et de widget

Tous les chemins sont sous `src/dx-excshell-1/web-src/src/components/`.

### **`ExtensionRegistration.js`**

Le fichier généré enregistre un exemple d’Experience Cloud Shell. Remplacez son `methods` par le contrat Fusion **`dashboard.getWidget`** afin que Fusion connaisse votre titre et l’emplacement de l’interface utilisateur :

```js
import { Text } from "@adobe/react-spectrum";
import { register } from "@adobe/uix-guest";
import metadata from "../../../../app-metadata.json";
import { extensionId } from "./Constants";

function ExtensionRegistration() {
  const init = async () => {
    await register({
      id: extensionId,
      metadata,
      methods: {
        dashboard: {
          getWidget() {
            return {
              id: extensionId,
              title: "My Fusion tool",          // label on the Fusion nav button
              description: "Hello from App Builder",
              url: "/index.html#/widget",       // route to the visible UI (4b)
              widgetSize: { defaultWidth: 6, defaultHeight: 6 },
              hideWidgetHeader: false,
            };
          },
        },
      },
    });
  };
  init().catch(console.error);

  return <Text>Registering with Fusion...</Text>;
}

export default ExtensionRegistration;
```

Si `Constants.js` n’existe pas à côté, créez-le :

```js
module.exports = { extensionId: "my-fusion-extension" };
```

### `DashboardWidget.js`

Créez ce fichier. Il termine l’établissement de la liaison et affiche le contexte Fusion actif :

```js
import { useEffect, useState } from "react";
import { Flex, Heading, Text, View } from "@adobe/react-spectrum";
import { attach } from "@adobe/uix-guest";
import { extensionId } from "./Constants";

const KEYS = ["imsOrgId", "imsUserId", "organization", "team", "user"];

export default function DashboardWidget() {
  const [ctx, setCtx] = useState(null);

  useEffect(() => {
    attach({ id: extensionId })
      .then((guest) => {
        const read = () =>
          KEYS.reduce((acc, k) => ({ ...acc, [k]: guest.sharedContext.get(k) }), {});
        setCtx(read());
        guest.addEventListener("contextchange", () => setCtx(read()));
      })
      .catch((e) => console.error("attach failed", e));
  }, []);

  return (
    <View padding="size-300">
      <Heading level={2}>Hello from App Builder</Heading>
      {!ctx ? (
        <Text>Connecting to Fusion...</Text>
      ) : (
        <Flex direction="column" gap="size-100" marginTop="size-200">
          <Text>User: {ctx.user?.name ?? ctx.imsUserId}</Text>
          <Text>Organization: {ctx.organization?.name} (id {ctx.organization?.id})</Text>
          <Text>Team: {ctx.team?.name ?? "-"}</Text>
        </Flex>
      )}
    </View>
  );
}
```

### `App.js`

Le routeur généré envoie déjà `index` / `index.html` à `ExtensionRegistration`. Ajoutez un itinéraire pour le widget et importez-le :

```js
import DashboardWidget from "./DashboardWidget";
// ...inside <Routes>, alongside the existing ExtensionRegistration routes:
<Route exact path="widget" element={<DashboardWidget />} />
```

> Le chemin d’accès (`widget`) doit correspondre au hachage dans `getWidget().url` (`/index.html#/widget`). Conservez le `index.js`/la `exc-runtime.js` généré(e) et le reste du `App.js` exactement comme prévu, car il s’agit du bootstrap que vous souhaitez que le modèle fournisse.

## Étape 5 : création

```sh
aio app build
```

Cette opération compile le front-end et exécute le hook de métadonnées qui génère des `app-metadata.json`. Corrigez les erreurs avant de continuer.

## Étape 6 : déploiement dans l’environnement intermédiaire

```sh
aio console workspace select     # choose Stage
aio app deploy
```

`deploy` héberge votre interface utilisateur sur le réseau CDN d’Adobe et enregistre le point d’entrée d’extension dans l’espace de travail d’évaluation, ce qui permet à Fusion de le découvrir. L’interface de ligne de commande imprime l’URL du point d’entrée, tel que `https://<project>-stage.adobeio-static.net`.

## Étape 7 : activer le test d’évaluation et afficher l’extension dans Fusion

1. Ouvrez Fusion sur Experience Cloud, connecté à la même organisation que celle vers laquelle vous avez déployé.
1. Ouvrez le menu d’avatar de l’utilisateur et accédez à **Paramètres du produit** > **Profil Fusion** > **Préférences**.
1. Activez le bouton **Extensions d’évaluation** et confirmez le rechargement.

   Fusion charge désormais les extensions à partir de l’espace de travail d’évaluation et les marque **(évaluation)**.
1. Accédez à la zone **Organisation** du volet de navigation de gauche.

   Le bouton **Mon outil Fusion (phase)** s’affiche.
1. Cliquez sur le bouton **Mon outil Fusion (phase)**.
Votre interface utilisateur se charge dans le panneau principal et affiche l’utilisateur, l’organisation et l’équipe actifs.
1. **Changer l’organisation ou l’équipe active** dans Fusion.

   Le panneau se met à jour et affiche le contexte en direct (`contextchange`).

>[!TIP]
>
>Si le bouton n’apparaît pas, rechargez-le une fois, car la découverte est mise en cache par session. Consultez ensuite la section [Dépannage des extensions personnalisées](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md).


## Itération pendant la démonstration

Apportez une modification, puis recréez et redéployez.  Les utilisateurs verront l’extension mise à jour la prochaine fois qu’ils l’ouvriront.

```sh
aio app build && aio app deploy
```

## Passage en production après la démonstration

Il suffit de faire une démonstration de l’environnement d’évaluation. Pour publier cette version à l’échelle de l’organisation, basculez vers l’espace de travail de production, déployez et envoyez la demande d’approbation. La demande doit être envoyée avec un rôle Administrateur système. Pour le processus complet, voir [Version en production](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md#release-on-production).

## Démonstration de la piste de discussion (facultatif)

Vous pouvez faire les points suivants pendant votre démonstration en direct :

* **« J’ai commencé à partir du modèle Experience Cloud Shell générique. »** Cela remodèle l’ensemble du shell SPA. Je n’ai donc reciblé que le point d’extension et modifié deux fichiers.
* **« Fusion est l&#39;hôte, mon application est l&#39;invité.«** Ils s’exécutent dans des cadres distincts et parlent de SDK d’extensibilité de l’interface utilisateur d’Adobe, sans mise en réseau personnalisée.
* **« Inscription ou affichage** » Le cadre masqué *enregistre* ce que je propose (`dashboard.getWidget`) et le cadre visible *s’attache* et lit le contexte.
* **« Le test d’évaluation est un commutateur par utilisateur. »** Par défaut, Fusion affiche uniquement les extensions publiées. J’ai cliqué sur Extensions d’évaluation dans mon profil Fusion pour charger ma version d’évaluation, sans version de production.
* **« Live context.«** Le changement d’organisation ou d’équipe renvoie le contexte et l’invité effectue un nouveau rendu.
