---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Publier votre extension personnalisée
description: Publier votre extension personnalisée
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: 925a8ee910434c474d527c2914897d7c42e4a3d1
workflow-type: tm+mt
source-wordcount: 1236
ht-degree: 1%

---

# Publier votre extension personnalisée

>[!NOTE]
>
>Cet article suppose que vous connaissez un peu les outils de développement logiciel.

Votre extension s’exécute dans Fusion uniquement après avoir été **créée**, **déployée** vers Adobe et **approuvée** pour votre organisation. Les procédures de cette page expliquent comment publier votre extension et vérifier le résultat.

Ces informations sont adaptées de la documentation officielle d’Adobe et s’appliquent spécifiquement à Workfront Fusion. Pour obtenir des informations générales sur Adobe, consultez [flux de développement des extensions de l’interface utilisateur](https://developer.adobe.com/uix/docs/guides/development-flow/) et [gestion des extensions de l’interface utilisateur](https://developer.adobe.com/uix/docs/guides/publication/) dans la documentation d’Adobe.

## Espaces de travail

Chaque projet App Builder comporte un espace de travail **d’évaluation** et **de production**. Considérez-les comme des environnements :

* **Phase** est destiné au développement et aux tests. Vous effectuez un déploiement ici pendant l’itération. Aucune approbation n’est requise et le résultat est visible uniquement par le biais du commutateur de test d’évaluation décrit ci-dessous (ou l’aperçu local).
* **Production** est destiné à être diffusé à tout le monde. Après le déploiement en production, vous envoyez une **demande d’approbation**, puis une fois celle-ci approuvée, l’extension est enregistrée dans le registre de l’application Adobe et présentée à l’ensemble de l’organisation.

>[!NOTE]
>
> **Rôles :** la création et le déploiement nécessitent le rôle **Développeur** ; l’envoi de la demande d’approbation pour publication nécessite un rôle **Administrateur système**.
>Pour plus d’informations, voir :
>
> * [Configurer des outils et un compte d’extension d’interface utilisateur](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md)
> * [Accès &#x200B;](https://developer.adobe.com/uix/docs/guides/get-access/) dans la documentation d’Adobe.

Par défaut, Fusion affiche uniquement les extensions **publiées**. Il s’agit d’extensions que vous avez déployées dans l’espace de travail **de production**, puis envoyées pour **approbation**. Il s’agit de la valeur par défaut sécurisée, de sorte qu’un déploiement en cours ne semble jamais accidentellement à l’ensemble de votre organisation.

Un déploiement dans l’espace de travail **Stage** n’est pas publié, il n’apparaît donc pas seul dans Fusion. Vous pouvez essayer une extension de deux manières avant de la publier :

* **Prévisualisez-le localement** avec `aio app run` (voir [Aperçu local des extensions de l’interface utilisateur](https://developer.adobe.com/uix/docs/guides/preview-extension-locally/) dans la documentation d’Adobe). Rien n’est déployé et vous seul le voyez.
* **Chargez-le à partir de l’environnement d’évaluation dans Fusion** en activant un commutateur de test par utilisateur dans votre profil Fusion. Cette procédure est décrite dans [Test d’une version d’évaluation dans Fusion](#test-a-stage-build-in-fusion) dans cet article.

## Test d’une version d’évaluation dans Fusion

Utilisez ce flux pour afficher un déploiement d’étape dans Fusion avant de le publier.

### Étape 1 : sélection de l’espace de travail d’évaluation

```sh
aio console where                  # shows current org / project / workspace
aio console workspace select       # choose Stage
```

### Étape 2 : création

```sh
aio app build
```

Cette opération compile votre front-end et exécute le hook de métadonnées (qui génère des `app-metadata.json`). Corrigez les erreurs signalées avant de continuer.

### Étape 3 : Déployer

```sh
aio app deploy
```

`deploy` fait deux choses :

* **Héberge votre interface utilisateur** sur le réseau de diffusion de contenu d’Adobe, à une URL de type `https://<project>-stage.adobeio-static.net`. L’interface de ligne de commande imprime cette **URL de point d’entrée d’extension** une fois l’opération terminée. Il s’agit de l’URL que Fusion charge dans son iframe.
* **Enregistre les points d’entrée de votre extension** pour le point d’extension (`fusion/nav-organization/1`) dans l’espace de travail d’évaluation.

>[!TIP]
>
> **Si le déploiement échoue avec « Le point d’extension &#39;fusion/nav-organization/1&#39; n’existe pas » (erreur 1060) :** le point d’extension Fusion n’est pas encore activé pour votre organisation. Il s’agit d’une étape d’intégration, pas d’une erreur dans votre code.
>Pour plus d’informations, consultez la section [Le point d’extension n’existe pas](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md#error-1060-extension-point-does-not-exist) dans l’article de dépannage.

### Étape 4 : activer le test d’évaluation dans votre profil Fusion

Fusion charge les extensions d’environnement intermédiaire uniquement lorsque vous souscrivez, par utilisateur :

1. Connectez-vous à Fusion avec un compte de la **même organisation** dans laquelle vous avez déployé .
1. Ouvrez le menu d’avatar de l’utilisateur dans le coin supérieur et accédez à **Paramètres du produit** > **Profil Fusion** > **Préférences**.
1. Activez le commutateur **Extensions d’évaluation**.

   Fusion vous invite à recharger le fichier.
1. Confirmez le rechargement.

Après le rechargement, Fusion charge les extensions à partir de l’espace de travail d’évaluation au lieu de l’ensemble publié et les libellent chacune **(étape)** dans la navigation afin que vous puissiez les différencier.

Ce commutateur est un paramètre de test personnel stocké dans votre navigateur, et non un paramètre d’organisation. Désactivez-la (et rechargez-la) pour revenir aux extensions publiées. Étant donné qu’il est stocké localement, il ne vous suit pas sur un autre navigateur ou ordinateur.

### Étape 5 : vérification dans Fusion

1. Ouvrez la section correspondant à votre point d’extension :
   * `fusion/nav-organization/1` → la zone **Organisation** du volet de navigation de gauche.
   * `fusion/nav-team/1` → la zone **Équipe** (commencez par sélectionner une équipe).

   Un bouton avec le titre que vous avez défini dans `getWidget()` s’affiche, marqué **(Phase)**.
1. Cliquez sur le bouton qui s’est affiché.

Votre interface utilisateur charge et reçoit le [contexte de fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).

Si le bouton ne s’affiche pas ou si le panneau affiche une erreur, voir [Dépannage](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md).

## Version de production

Lorsque votre extension fonctionne sur l’environnement d’évaluation et que vous êtes prêt pour tous les utilisateurs :

### Étape 1 : passer à l’espace de travail de production

```sh
aio console workspace select       # choose Production
```

Lorsque l’interface de ligne de commande vous invite à consulter le fichier `.env`, sélectionnez **Fusionner** afin de conserver vos variables d’environnement.

### Étape 2 : création et déploiement en production

```sh
aio app build
aio app deploy
```

### Étape 3 : Soumettre la demande de validation

La publication est une **demande d’approbation envoyée à partir de l’espace de travail de production** :

1. Ouvrez le [&#128279;](https://developer.adobe.com/console), sélectionnez votre **Organisation**, ouvrez votre **Projet** et passez à l’espace de travail **Production**.
1. Envoyez votre application pour **approbation/publication** (le rôle **Administrateur système** est requis).
1. Après approbation, votre extension est ajoutée au registre des applications **&#x200B;**&#x200B;et devient disponible dans [Adobe Experience Cloud](https://experience.adobe.com?lang=fr), y compris Fusion, pour votre organisation.

Pour obtenir des instructions détaillées, voir [Gestion des extensions d’interface utilisateur](https://developer.adobe.com/uix/docs/guides/publication/) dans la documentation d’Adobe Developer.

## Statut et mises à jour

Certains comportements valent la peine d’être connus, afin que vous puissiez dire « vous y travaillez toujours » en dehors de « quelque chose ne va pas » :

* **Déployé en production est différent de visible.** `aio app deploy` en exploitation télécharge votre application, mais ne fait pas apparaître l’extension. Il s’affiche uniquement une fois la demande d’approbation soumise et approuvée. Si vous avez déployé en production et que vous ne le voyez toujours pas dans Fusion, la raison habituelle est qu’il n’est pas encore approuvé.
* **Les mises à jour à code seul n’ont pas besoin d’une nouvelle approbation.** Si votre extension est déjà publiée et que vous modifiez uniquement son code (l’interface utilisateur ou les actions d’exécution), redéployez vers la même URL avec :

  ```sh
  aio app deploy --force-deploy
  ```

  Les utilisateurs obtiendront la nouvelle version la prochaine fois qu’ils ouvriront l’extension. Ils n&#39;ont rien à installer. Il vous suffit de soumettre une nouvelle demande d’approbation lorsque vous modifiez l’**enregistrement** lui-même, par exemple en ajoutant un nouveau point d’extension ou en modifiant ce que `getWidget()` annonce.
* **Une extension révoquée ou retirée disparaît.** Si une extension est révoquée par vous ou retirée, elle cesse d’apparaître dans Fusion sans message d’erreur. Si une extension qui fonctionnait auparavant disparaît pour tout le monde, vérifiez si elle a été révoquée avant de rechercher un problème de code.

## Supprimer (révoquer) une extension

La suppression d’une extension publiée est effectuée en **révoquant** dans Adobe Exchange :

1. Se connecter à **&#x200B;**.
1. Accédez à **Gérer** > **Applications App Builder**.
1. Sélectionnez **Révoquer** en regard de l’extension à supprimer, puis confirmez.

Après la révocation, l’extension affiche un statut *révoqué* dans Extension Manager et n’apparaît plus dans Fusion. Pour le supprimer complètement, supprimez le projet dans le Developer Console. Un projet ne peut pas être supprimé tant que son extension n’est pas révoquée.

Pour un déploiement test d’évaluation uniquement, vous pouvez supprimer le déploiement avec :

```sh
aio app undeploy
```

## Ressources supplémentaires

Les ressources suivantes sont disponibles dans la documentation d’Adobe :

* [Flux de développement de l’extension d’interface utilisateur](https://developer.adobe.com/uix/docs/guides/development-flow/)
* [Gestion des extensions d’interface utilisateur (publier/approuver/révoquer)](https://developer.adobe.com/uix/docs/guides/publication/)
* [Création d’un projet dans Developer Console](https://developer.adobe.com/uix/docs/guides/creating-project-in-dev-console/)
* [Accès (rôles)](https://developer.adobe.com/uix/docs/guides/get-access/)
* [Aperçu local des extensions de l’interface utilisateur](https://developer.adobe.com/uix/docs/guides/preview-extension-locally/)
