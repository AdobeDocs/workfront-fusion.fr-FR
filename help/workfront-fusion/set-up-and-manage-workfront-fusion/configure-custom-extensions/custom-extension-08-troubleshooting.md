---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Résolution des problèmes liés aux extensions personnalisées
description: Résolution des problèmes liés aux extensions personnalisées
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 1136
ht-degree: 0%

---


# Résolution des problèmes liés aux extensions personnalisées

>[!NOTE]
>
>Cet article suppose que vous connaissez un peu les outils de développement logiciel.

Cet article présente quelques solutions aux problèmes que vous êtes le plus susceptible de rencontrer lors de la création d’extensions personnalisées, globalement dans l’ordre dans lequel ils se produisent pendant le développement.

## Liste de contrôle rapide

Si quelque chose ne fonctionne pas, vérifiez d’abord les éléments suivants :

* Node.js est la version 18 ou 20 (`node --version`).
* Vous êtes connecté (`aio login`) et vous vous trouvez dans l’organisation/le projet/l’espace de travail approprié (`aio console where`).
* Le nom du point d’extension correspond exactement, y compris la version : `fusion/nav-organization/1`.
* Le `url` dans `getWidget()` correspond à un itinéraire dans votre application.
* Vos appels d’interface utilisateur visibles `attach({ id })`.
* Vous recherchez le bon ensemble d’extensions dans Fusion :
  * Pour afficher une version d’évaluation, déployez sur l’environnement d’évaluation et activez le bouton des extensions d’évaluation dans votre profil Fusion (Paramètres de produit > Profil Fusion > Préférences).
  * Pour afficher une extension publiée, déployez-la en production et faites-la approuver.

## Erreur 1060 : « Le point d’extension n’existe pas »

**Message complet :** `CoreConsoleAPISDK ... 1060: Extension point 'fusion/nav-organization/1' does not exist` lors de l’`aio app deploy`.

**Signification :** le point d’extension Fusion n’est pas encore activé (« intégré ») pour votre organisation Adobe. Adobe vérifie, au moment du déploiement, que le point d’extension existe dans le catalogue de votre organisation. Ce n’est **pas** un problème avec votre code ou votre YAML.

**Correctif :** demandez à l’équipe Fusion d’intégrer le ou les points d’extension (`fusion/nav-organization/1` et/ou `fusion/nav-team/1`) pour votre organisation IMS. Lorsque vous demandez une intégration, incluez les éléments suivants :

* votre **identifiant de l’organisation IMS** (`XXXX@AdobeOrg`),
* le(s) **point(s) d’extension** dont vous avez besoin,
* vos noms de projet et espace de travail ****.

Une fois l’intégration confirmée, exécutez à nouveau `aio app deploy`.


## « En attente du message initial de l’iframe cible » : le panneau tourne à tout jamais

**Signification :** Fusion a ouvert votre interface utilisateur visible, mais n’a pas terminé l’établissement de la liaison. Par conséquent, le délai de Fusion a expiré.

**Causes fréquentes :**

* `attach` se trouve uniquement dans le composant d’enregistrement, et non dans le widget visible.
* Le `url` dans `getWidget()` pointe vers un itinéraire qui effectue le rendu du composant **enregistrement** (ou une page vierge) au lieu de votre widget.
* Le `id` transmis à `attach` diffère du `id` utilisé dans `register`. Ils doivent être identiques, donc gardez les deux en `Constants.js`.

**Correctif :** assurez-vous que votre composant **visible** appelle `attach({ id })` :

```jsx
useEffect(() => {
  attach({ id: extensionId }).catch(console.error);
}, []);
```

Pour plus d’informations, voir [Création de l’interface utilisateur de l’extension personnalisée](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md).



## Le bouton de navigation n’apparaît pas dans Fusion

Si le bouton de navigation de votre extension personnalisée n’apparaît pas dans Fusion, vérifiez ces éléments dans l’ordre :

1. **Cherchez-vous le bon jeu d’extensions ?** Par défaut, Fusion affiche uniquement les extensions publiées, qui ont été déployées en production et approuvées. Si vous testez une version d’évaluation, activez le commutateur Extensions d’évaluation dans votre profil Fusion (Paramètres de produit > Profil Fusion > Préférences) et rechargez. Les éléments de l’étape sont étiquetés **(étape)**.
Pour plus d’informations, voir [Publication de votre extension personnalisée](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md).
1. **A-t-il été révoqué ou retiré ?** Une extension révoquée ou retirée cesse d’apparaître dans Fusion sans erreur. Si un bouton qui fonctionnait auparavant disparaissait, vérifiez qu’il est toujours actif dans Adobe Exchange avant de rechercher un problème de code.
1. **Est-il déployé dans l’espace de travail approprié ?** Déployez sur l’espace de travail que vous êtes en train de charger, l’espace de travail d’évaluation lorsque vous utilisez le commutateur de test d’évaluation.
1. **Est-il déployé dans la bonne organisation ?** Connectez-vous à Fusion avec un compte de la **même** organisation IMS que celle sur laquelle vous avez déployé .
1. **Est-ce dans la bonne section ?** `fusion/nav-organization/1` affiche sous **Organisation** ; `fusion/nav-team/1` affiche sous **Équipe** (vous devez d’abord sélectionner une équipe).
1. **Existe-t-il une faute de frappe du nom du point d’extension ?** Il doit lire exactement `fusion/nav-organization/1` dans les deux `app.config.yaml` et le chemin d’inclusion `ext.config.yaml` du dossier .


## Le bouton apparaît, mais le panneau est vide

Si le bouton apparaît mais que le panneau est vide, vérifiez les éléments suivants :

* **Non-correspondance d’itinéraire :** la `url` de `getWidget()` (telle que `/index.html#/my-widget`) doit correspondre à une `<Route>` dans `App.js`. Une discordance charge une page sans composant.
* **Erreur JavaScript :** ouvrez l’onglet Outils de développement (F12) > **Console** de votre navigateur et recherchez les erreurs provenant de l’iframe. Corrigez l’erreur signalée et effectuez un redéploiement.
* **En-tête manquant/dupliqué :** `hideWidgetHeader` dans `getWidget()` contrôle si Fusion affiche le titre au-dessus de votre interface utilisateur. Définissez-le sur `true` si vous effectuez le rendu de votre propre en-tête.

## L’iframe est bloqué (politique de sécurité du contenu / « refus de créer un iframe »)

Fusion autorise uniquement les extensions hébergées sur le réseau CDN App Builder d’Adobe (`*.adobeio-static.net`), où `aio app deploy` place vos fichiers par défaut. Si vous hébergez votre interface utilisateur ailleurs, par exemple dans un domaine personnalisé, Fusion refuse de la charger. Effectuez le déploiement via App Builder comme indiqué ou demandez à l’équipe Fusion si votre domaine peut être placé sur la liste autorisée.

## Le contexte est vide ou obsolète

* **Vide juste après le chargement :** lisez le contexte **après** la résolution du `attach`, pas avant. D’ici là, afficher un état « Connexion... ».
* **Pas de mise à jour lorsque l’utilisateur change d’organisation ou d’équipe** Abonnez-vous à l’événement `contextchange` et lisez à nouveau vos clés dans le gestionnaire. Pour plus d’informations, consultez la section [Lire le contexte des partages Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md#read-the-context-fusion-shares) dans l’article Créer l’interface utilisateur de l’extension personnalisée.
* **Les dates ne semblent pas correctes :** les champs de date arrivent sous la forme de chaînes ISO **strings**, et non d’objets `Date`. Enveloppez-les dans du `new Date(...)`. Voir [ Dates](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md#dates) dans l’article Référence contextuelle de Fusion.

## L’appel d’une API échoue avec une erreur CORS.

**Symptôme :** la console du navigateur affiche *« Aucun en-tête « Access-Control-Allow-Origin »* (ou la requête est bloquée) lorsque votre interface utilisateur appelle directement une API Workfront/Fusion.

**Correctif :** n’appelez pas ces API depuis le navigateur. Acheminez l’appel via votre propre **action d’exécution** App Builder (côté serveur, pas de CORS) et demandez à l’invité d’appeler l’action avec une URL relative de même origine. Pour plus d’informations, voir [Appeler les API Workfront et Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md).


## L’action de proxy renvoie 401 même avec un jeton valide

**Signification :** avec `require-adobe-auth: true`, la passerelle Adobe valide l’appel avant l’exécution de votre action et peut rejeter ou supprimer des en-têtes personnalisés dont vous avez besoin en amont, en les faisant apparaître sous forme de `401`.

**Correction :** définissez des `require-adobe-auth: false` sur l’action **et** appliquez l’autorisation vous-même. Demander un porteur de `Authorization` dans l&#39;action, la transférer en amont, et garder une cible stricte. Voir [required-adobe-auth : true ou false](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md#require-adobe-auth-true-vs-false).

## Fusion `GET /api/v3/hooks` renvoie 400

**Signification :** point d’entrée des points d’entrée des points d’entrée est **de portée équipe**, il s’`teamId` donc d’un paramètre de requête obligatoire.

**Correctif :** l’appel `/api/v3/hooks?teamId=<team.id>`. Les points d’extension ne sont disponibles que pour l’équipe active. Pour couvrir une organisation, bouclez ses équipes et fusionnez. Les scénarios, en revanche, acceptent les `organizationId`. Voir [Spécificités de l’API Fusion v3](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md#fusion-v3-api-specifics).


## Erreurs `aio`

* **`aio: command not found`:** l’interface de ligne de commande n’est pas installée ou ne se trouve pas sur votre CHEMIN. Relancez `npm install -g @adobe/aio-cli`, puis ouvrez un nouveau terminal.
* **La création/le déploiement échoue sur une toute nouvelle version de nœud :** utilisez le nœud **18 ou 20 LTS**. Les nouvelles versions non-LTS rompent parfois la chaîne d’outils.
* **« Vous n’êtes pas un développeur » / ne peut pas voir votre organisation :** l’administrateur de l’organisation Adobe doit vous accorder le rôle **Développeur** et l’accès à App Builder. Pour plus d’informations, voir [Configurer des outils et un compte d’extension d’interface utilisateur](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md).
* **401 / jeton non valide lors du déploiement ou de la découverte :** votre session a expiré ou vous mélangez des environnements. Exécutez `aio logout` puis `aio login`, confirmez le `aio console where` et déployez-le dans l’espace de travail que vous êtes en train de charger.

## Collecte d’informations à des fins d’assistance

Collectez ces informations pour établir un diagnostic beaucoup plus rapidement :

* La commande exacte que vous avez exécutée et la sortie d’erreur **full**.
* Votre **ID d’organisation IMS**, **projet** et **espace de travail**.
* Le **point d’extension** vous ciblez.
* Si `aio app deploy` a réussi et si l’extension est **publiée** (ou, pour un test d’évaluation, si les extensions d’évaluation sont activées).
* Erreurs éventuelles dans le navigateur **Console** (F12) lors de l’ouverture du panneau dans Fusion.
