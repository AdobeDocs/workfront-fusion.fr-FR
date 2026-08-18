---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Créer un projet pour l’extensibilité de l’interface utilisateur
description: Créer un projet pour l’extensibilité de l’interface utilisateur
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 1360
ht-degree: 0%

---

# Créer un projet pour l’extensibilité de l’interface utilisateur

>[!NOTE]
>
>Cet article suppose que vous connaissez un peu les outils de développement logiciel.

Pour créer une extension d’interface utilisateur personnalisée, vous devez créer un projet App Builder correspondant.

Cette page décrit comment générer un projet App Builder générique avec la ligne de commande `aio`. « Générique » signifie que le projet ne démarre **pas** à partir d’un modèle spécifique au produit. Démarrer avec une application générique simplifie le projet et lui permet de se connecter à Workfront Fusion.

Il peut être utile de vous familiariser avec les concepts et la terminologie suivants concernant la création d’un projet à utiliser avec l’extensibilité d’Adobe Fusion AI.

* **** (<https://developer.adobe.com/console>) est le tableau de bord web où réside votre projet.

* **Terminologie** :

  | Terme | Signification |
  | ------ | --------------- |
  | **Organisation** | L’organisation Adobe de votre entreprise. La même organisation que celle utilisée dans Fusion. |
  | **Projet** | Conteneur pour une application/extension. Vous allez créer un projet pour votre extension. |
  | **Espace de travail** | Une copie de la configuration du projet pour une étape de travail. Chaque projet dispose d’un espace de travail **Production** et vous utilisez généralement également un espace de travail **Évaluation** pour les tests. Pensez aux espaces de travail comme aux « environnements ». |
  | **Informations d’identification/services** | Autorisations que votre application peut utiliser. Les valeurs par défaut créées pour vous suffisent pour démarrer. |

* Il existe deux manières de créer un projet :

  * **Automatique (recommandé) :** l’`aio app init` de commande crée le projet et les espaces de travail pour vous lors de la génération du code. Cet article décrit ce processus.
  * **Manuel :** vous commencez par créer le projet vous-même dans le Developer Console, puis vous `aio` pointez dessus. Nous vous recommandons de ne le faire que si votre organisation nécessite que les projets soient créés de manière centralisée.

* Lorsque vous décidez de l’espace de travail à utiliser, développez et déployez-le d’abord sur **Stage**. Fusion charge une version d’évaluation uniquement lorsque l’utilisateur active les tests d’évaluation dans son profil Fusion (menu d’avatar de l’utilisateur > Paramètres de produit > Profil Fusion > Préférences > Extensions d’évaluation) ; dans le cas contraire, seules les extensions de production publiées s’affichent. Vous pouvez également prévisualiser localement avec `aio app run`, puis convertir en **Production** ultérieurement.

  Pour plus d’informations sur la promotion en production, voir [Publication de votre extension](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md).


## Exécuter `aio app init`

1. Ouvrez un terminal.
1. Dans le terminal, déplacez-vous vers le dossier dans lequel vous conservez les projets.
1. Exécuter :

   ```sh
   aio app init my-fusion-extension --standalone-app
   ```

   * `my-fusion-extension` est le nom du dossier/de l’application. Vous pouvez sélectionner ce nom, mais en utilisant des lettres minuscules, des tirets et sans espaces.
   * `--standalone-app` indique à l’interface de ligne de commande de créer un **squelette d’application simple** au lieu de vous demander de choisir un modèle de produit. Il s’agit de la clé pour éviter le modèle AEM (ou tout autre modèle).

1. Lorsque vous y êtes invité, **sélectionnez votre organisation** (si vous en appartenez à plusieurs).
1. Lorsque vous y êtes invité, sélectionnez **Créer un projet** et acceptez le nom suggéré, ou sélectionnez un projet vide existant.

   La commande configure automatiquement les espaces de travail **Évaluation** et **Production**.

   La commande génère également des fichiers dans le dossier `my-fusion-extension` et exécute `npm install`.

1. Passez à [Confirmer la création du projet](#confirm-project-creation).

>[!NOTE]
>
> **Si vous préférez le menu interactif :** exécutez `aio app init my-fusion-extension` > (sans `--standalone-app`). Lorsqu’il **demande « Quels modèles voulez-vous rechercher ? »** ou affiche une liste de contrôle de modèles, ne sélectionnez pas un modèle de produit comme AEM. Choisissez l’option pour créer une **application autonome** / **« Tous les points d’extension → aucun »**.

## Vérifier la création du projet

1. Dans le terminal, accédez au dossier créé :

   ```sh
   cd my-fusion-extension
   ```

   Vous devriez voir une structure similaire à celle-ci (certains fichiers sont omis) :

   ```
   my-fusion-extension/
   |--- app.config.yaml   // main configuration (you will edit this)
   |---  package.json   //dependencies and scripts
   |---  src/    // your source code
   |---  web-src/  or  src/.../web-src/  // front-end files (HTML/JS)
   ```

   Les deux fichiers qui vous intéressent le plus sont les suivants :

   * **`app.config.yaml`** : configuration centrale. Plus loin dans le processus, vous ajouterez une section `extensions:` ici qui connecte votre application à un point d’extension Fusion.
   * **`package.json`** : répertorie les bibliothèques utilisées par votre application. Vous ajouterez ici la bibliothèque invitée Extensibilité de l’interface utilisateur d’Adobe.

1. Passez à [Ajouter les bibliothèques requises](#add-required-libraries).

>[!TIP]
>
> Ne vous inquiétez pas si la disposition générée diffère légèrement entre les versions de l’interface de ligne de commande. Cette procédure vous indique exactement quels fichiers créer et quoi y placer, afin que vous puissiez correspondre à la structure attendue quel que soit le point de départ.

## Ajout des bibliothèques requises

Votre extension a besoin de deux bibliothèques :

* **`@adobe/uix-guest`** : permet à votre application de communiquer avec Fusion (l’hôte).
* **`@adobe/react-spectrum`** : composants de l’interface utilisateur React d’Adobe, afin que votre écran corresponde à l’aspect d’Adobe. (Facultatif, mais recommandé ; vous pouvez utiliser HTML brut à la place.)

Pour installer ces bibliothèques :

1. Dans le terminal, exécutez :

   ```sh
   npm install @adobe/uix-guest @adobe/react-spectrum
   ```

1. (Conditionnel) Si le projet généré n’inclut pas déjà React, installez-le également :

   ```sh
   npm install react react-dom react-router-dom
   ```

1. Continuez pour [Confirmer les versions du projet](#confirm-the-project-builds).

## Confirmer les versions de projet

Avant de modifier quoi que ce soit, assurez-vous que le projet vide est généré

1. Dans le terminal, exécutez :

   ```sh
   aio app build
   ```

   Si cette opération s’effectue sans erreur, vos outils et votre projet sont correctement configurés. Vous êtes prêt à connecter le projet à Fusion.

   >[!TIP]
   >
   > **Si la création échoue** la cause la plus courante est une version de Node.js non prise en charge. Exécutez `node --version` et assurez-vous qu’il s’agit de 18 ou 20.
   >
   >* Pour plus d’informations sur l’installation de Node.js, voir [Configuration de vos outils](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md).
   >* Pour plus d’informations sur les autres erreurs possibles, voir [Dépannage](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md).

1. Passez à [Configurer le projet pour Fusion](#configure-the-project-for-fusion).

## Configuration du projet pour Fusion

L’étape suivante de la configuration de votre extension personnalisée consiste à connecter votre projet générique à Workfront Fusion.

Tu pourras :

1. [Créer un dossier pour votre extension](#create-a-folder-for-your-extension)
1. Parlez à App Builder d’un **point d’extension** Fusion (en `app.config.yaml`).
1. Décrivez les éléments de votre extension (en `ext.config.yaml`).
1. **Inscrivez** votre widget afin que Fusion connaisse son titre et l’emplacement de son interface utilisateur.

Nous utilisons `fusion/nav-organization/1` partout. Pour cibler la section Équipe à la place, permutez en `fusion/nav-team/1` partout. Pour prendre en charge les deux, répétez le motif pour chacun d’eux.

## Créer un dossier pour votre extension

1. Créez vos fichiers de sorte que le projet ressemble à ceci :

   ```
   my-fusion-extension/
   |-- app.config.yaml
   |-- src/
          |-- fusion-nav-organization-1/          // one folder per extension point
             |-- ext.config.yaml
             |-- web-src/
                |-- src/
                   |-- components/
                      |-- App.js
                      |-- ExtensionRegistration.js
                      |-- DashboardWidget.js
                      |-- Constants.js
   ```

   Nous vous recommandons de nommer le dossier après le point d’extension (`fusion-nav-organization-1`). Le nom exact dépend de vous, mais il doit correspondre à ce que vous référencez dans `app.config.yaml`.

1. Continuez sur [Déclarez le point d’extension en `app.config.yaml`](#declare-the-extension-point-in-appconfigyaml).

## Déclarez le point d’extension en `app.config.yaml`

1. Ouvrez `app.config.yaml` et mettez à jour son contenu vers :

   ```yaml
   extensions:
     fusion/nav-organization/1:
       $include: src/fusion-nav-organization-1/ext.config.yaml
   ```

   Ces contenus décrivent les éléments suivants :

   * `extensions:` : cette application implémente un ou plusieurs points d’extension.
   * `fusion/nav-organization/1` : emplacement Fusion auquel vous vous connectez. **Le nom doit correspondre exactement** y compris la version `1`.
   * `$include:` : pointe vers un second fichier de configuration (créé à l’étape suivante) qui décrit le contenu de cette extension. Le fait de le conserver dans un fichier distinct permet de garder `app.config.yaml` propre et vous permet d’ajouter d’autres points d’extension ultérieurement.

   >[!NOTE]
   >
   >Si vous ciblez les deux extensions, répertoriez les deux, chacune disposant de son propre dossier :
   >
   > ```yaml
   > extensions:
   >     fusion/nav-organization/1:
   >         $include: src/fusion-nav-organization-1/ext.config.yaml
   >     fusion/nav-team/1:
   >         $include: src/fusion-nav-team-1/ext.config.yaml
   > ```

   1. Passez à [Décrire l’extension dans `ext.config.yaml`](#describe-the-extension-in-extconfigyaml)

## Décrire l’extension en `ext.config.yaml`

1. Créez des `src/fusion-nav-organization-1/ext.config.yaml` avec :

   ```yaml
   operations:
      view:
       - type: web
         impl: index.html
   web: web-src
   hooks:
     pre-app-build: node node_modules/@adobe/uix-guest/scripts/generate-metadata.js
      pre-app-run: node node_modules/@adobe/uix-guest/scripts/generate-metadata.js
   ```

   Ces contenus décrivent les éléments suivants :

   * **`operations.view`** : déclare que votre extension fournit une **vue** (interface utilisateur visible), diffusée à partir de `index.html`. C’est ce qui permet à votre extension d’afficher un écran plutôt que de s’exécuter uniquement en arrière-plan.
   * **`web: web-src`** : le dossier qui contient vos fichiers front-end. App Builder crée tout ici et l’héberge sur le réseau de diffusion de contenu (CDN) d’Adobe.
   * **`hooks`** : petites commandes qui s’exécutent automatiquement au moment de la création/de l’exécution. Le script `generate-metadata.js` est fourni avec `@adobe/uix-guest` et génère un fichier `app-metadata.json` dont votre code d’enregistrement a besoin (voir Étape 4). Vous n&#39;écrivez pas ce script ; vous le référencez simplement.

   >[!NOTE]
   >
   > Si vous avez également besoin d’une logique côté serveur, vous pouvez également ajouter des `actions` sans serveur (petites fonctions d’arrière-plan). Les actions sont facultatives et ne sont pas requises pour générer une interface utilisateur. Nous les laissons donc de côté pour que ce guide reste ciblé. Si vous les ajoutez ultérieurement, déclarez un dossier `actions:` ici et un `runtimeManifest:` dans `app.config.yaml`. La raison la plus courante d’en ajouter une est d’appeler les API Workfront/Fusion sans accéder à la configuration CORS du navigateur.
   > Pour plus d’informations sur l’appel des API, voir [Appeler des API Workfront et Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md).
1. Passez à [Définir un ID d’extension stable](#set-a-stable-extension-id).

## Définir un ID d’extension stable

Votre extension nécessite un identifiant unique que les deux trames partagent.

Pour plus d’informations sur les cadres associés aux extensions personnalisées, voir [Cadres inclus dans une extension d’interface utilisateur](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-01-overview.md#frames-included-in-a-ui-extension).

1. Créer un `src/fusion-nav-organization-1/web-src/src/components/Constants.js` :

   ```js
   module.exports = {
     extensionId: 'my-fusion-extension'
   };
   ```

   Utilisez la même valeur partout où votre code fait référence à l’ID d’extension.
1. Continuez sur [Enregistrer votre widget](#register-your-widget).


## Enregistrer votre widget

« Enregistrement » est la manière dont le cadre d’arrière-plan masqué indique à Fusion ce que votre extension offre. Vous déclarez une méthode `dashboard.getWidget()` qui renvoie le titre de votre widget et l’URL de son interface utilisateur visible.

1. Créez des `src/fusion-nav-organization-1/web-src/src/components/ExtensionRegistration.js`.
La partie importante est l&#39;appel `register(...)` :

   ```js
   import { register } from "@adobe/uix-guest";
   import metadata from "../../../../app-metadata.json";
   import { extensionId } from "./Constants";
   
   async function init() {
     await register({
       id: extensionId,
       metadata,
       methods: {
         dashboard: {
           getWidget() {
             return {
               id: extensionId,
               title: "My Fusion tool",        // shown on the Fusion nav button
               description: "What this tool does",
               url: "/index.html#/my-widget",  // route to your visible UI
               hideWidgetHeader: false          // false = Fusion shows the title
             };
           }
         }
       }
      });
   }
   
   init().catch(console.error);
   ```

   Points clés :

   * **`title`** est le libellé que Fusion attribue au bouton de navigation. Si `hideWidgetHeader` est `false`, Fusion affiche également le titre sous la forme d’un en-tête au-dessus de votre interface utilisateur.
   * **`url`** est l’itinéraire vers votre interface utilisateur *visible* dans cette même application. Ici, il s’agit d’une route de hachage (`#/my-widget`) gérée par votre routeur front-end (configurée sur la page suivante). Elle doit être résolue sur le composant qui effectue le rendu de votre écran.
   * **`metadata`** provient de `app-metadata.json`, que le hook `generate-metadata` crée pour vous au moment de la création. Importez-le comme indiqué.
   * Le nom de la méthode `dashboard.getWidget` correspond au contrat convenu que Fusion appelle pour découvrir votre widget. Conservez l’espace de noms `dashboard` et le nom du `getWidget`.

Le serveur principal de votre extension est maintenant terminé. Étape suivante dans la création de l’interface utilisateur de l’extension.

Pour obtenir des instructions sur la création de l’interface utilisateur, voir [Créer l’interface utilisateur d’extension personnalisée](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md).
