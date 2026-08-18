---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Configurer des outils et un compte d’extension d’interface utilisateur
description: Configurer des outils et un compte d’extension d’interface utilisateur
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 500
ht-degree: 0%

---


# Configurer des outils et un compte d’extension d’interface utilisateur

Avant de pouvoir créer une extension d’interface utilisateur pour Workfront Fusion, vous devez configurer vos outils et votre compte . Cela ne doit être fait qu&#39;une seule fois.

>[!NOTE]
>
>Cet article suppose que vous connaissez un peu les outils de développement logiciel.

<!--Access requirements-->

## Conditions préalables

Pour configurer vos outils d’extensibilité de l’interface utilisateur et votre compte , vous avez besoin des éléments suivants :

* **Un Adobe ID** ayant accès à une organisation Adobe. Il s’agit du compte que vous utilisez pour vous connecter à Fusion.
* **Accès des développeurs à App Builder.** L’administrateur de votre organisation devra peut-être vous accorder le rôle **Développeur** et vous ajouter à un **Profil de produit** qui inclut App Builder. Si, par la suite, des commandes échouent avec « vous n’êtes pas un développeur » ou si vous ne pouvez pas voir votre organisation, demandez à votre administrateur d’organisation Adobe de vous ajouter.
* **Administrateur système** <!--Adobe? Fusion?--> (éventuellement un autre membre de votre équipe) pour l’étape de publication finale. La création et le déploiement nécessitent uniquement le rôle Développeur, mais **l’envoi d’une extension pour approbation/publication nécessite le rôle Administrateur système**.

  Pour plus d&#39;informations sur les niveaux d&#39;accès Adobe, voir
  [Accès &#x200B;](https://developer.adobe.com/uix/docs/guides/get-access/) dans la documentation d’Adobe.

* **Ordinateur sur lequel vous pouvez installer un logiciel** et exécuter des commandes de terminal (macOS, Windows ou Linux).

## Installation de Node.js

L’outil Adobe s’exécute sur **Node.js**. Vous devez installer la version **LTS** (18 ou 20).

1. Accédez à <https://nodejs.org> et téléchargez le programme d’installation de **LTS**.
1. Exécutez le programme d’installation et acceptez les valeurs par défaut.
1. Confirmez que cela a fonctionné en ouvrant un terminal et en exécutant :

   ```sh
   node --version
   npm --version
   ```

   Vous devriez voir les numéros de version (par exemple `v20.17.0` et `10.x`).

1. (Conditionnel) Si `node` n’est pas trouvé, fermez et rouvrez votre terminal ou redémarrez votre ordinateur.

1. Passez à [Installation de l’interface de ligne de commande Adobe I/O (`aio`)](#install-the-adobe-io-cli-aio).

>[!TIP]
>
>* Si vous utilisez plusieurs versions de nœud, un gestionnaire de versions tel que `nvm` est pratique, mais facultatif.
>* L’interface de ligne de commande d’Adobe nécessite Node 18 ou une version ultérieure. Les toutes nouvelles versions non-LTS peuvent occasionnellement entraîner des problèmes. Nous vous recommandons donc d’utiliser LTS.

## Installation de l’interface de ligne de commande Adobe I/O (`aio`)

L’outil de ligne de commande que vous utilisez pour créer, créer et publier votre extension est appelé `aio`.

Pour l’installer globalement :

1. Utilisez la commande `npm` suivante sur votre ligne de commande.

   ```sh
   npm install -g @adobe/aio-cli
   ```

1. Vérifiez qu’il est installé à l’aide de la commande suivante :

   ```sh
   aio --version
   ```

   Vous devriez voir quelque chose comme `@adobe/aio-cli/11.x.x`.

1. Passez à [Connexion à Adobe](#sign-in-to-adobe).

>[!NOTE]
>
> Si une erreur d’autorisations s’affiche sur macOS/Linux, n’utilisez **&#x200B;**&#x200B;`sudo`. Au lieu de cela, corrigez les autorisations de dossier globales de npm ou utilisez un gestionnaire de versions de nœud qui s’installe dans votre répertoire personnel.

## Connexion à Adobe

1. Connectez l’interface de ligne de commande à votre compte Adobe avec la commande suivante :

   ```sh
   aio login
   ```

1. Dans la fenêtre du navigateur qui s’ouvre, connectez-vous avec votre Adobe ID et approuvez l’accès.

1. Une fois la connexion établie, fermez l’onglet du navigateur et revenez au terminal.

1. (Facultatif) Pour vous déconnecter ultérieurement (par exemple pour changer de compte), utilisez la commande : `aio logout`.
1. Continuez pour [Confirmer votre organisation active](#confirm-your-active-organization).

## Confirmer votre organisation active

Vérifiez l’organisation vers laquelle pointe l’interface de ligne de commande :

```sh
aio console org list      # see organizations you can use
aio console where         # see your currently selected org/project/workspace
```

Si vous appartenez à plusieurs organisations, sélectionnez celle qui convient :

```sh
aio console org select
```

Vous êtes maintenant prêt à créer le projet.
