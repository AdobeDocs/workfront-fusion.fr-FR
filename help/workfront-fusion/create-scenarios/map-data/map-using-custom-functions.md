---
title: Mappage de données à l’aide de fonctions personnalisées
description: Lorsque vous mappez des éléments, vous pouvez utiliser des fonctions pour créer des formules simples ou complexes.
author: Becky
feature: Workfront Fusion
exl-id: dc4e697a-a65c-48bc-99de-8e26fbeb7ba7
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: c716296d771974ffdb59e916f9865c9efb2ad5a9
workflow-type: tm+mt
source-wordcount: '930'
ht-degree: 11%
---
# Mappage de données à l’aide de fonctions personnalisées

Vous pouvez créer des fonctions personnalisées dans la zone Fonctions de Fusion. Vous ajoutez ensuite ces fonctions à vos scénarios sous la forme d’un module Adobe App Builder .

Les fonctions personnalisées fonctionnent via Adobe App Builder. Votre entreprise doit donc disposer d’une licence Adobe App Builder pour les utiliser.

Les fonctions personnalisées, comme la plupart des éléments de scénario, sont détenues par les équipes.

Les fonctions sont de simples fonctions JavaScript. Pour inclure des variables ou des dépendances dans votre logique de fonction, utilisez des packages.

Pour plus d&#39;informations sur les packages, consultez [Utilisation de packages de fonctions personnalisées](/help/workfront-fusion/create-scenarios/map-data/use-custom-function-packages.md).

Workfront Fusion inclut également des fonctions intégrées qui vous permettent de créer des formules simples ou complexes. Ces fonctions couvrent un large éventail de cas d’utilisation, y compris les fonctions pour les tableaux, les chaînes, les nombres et les données des modules précédents.

Pour plus d&#39;informations et d&#39;instructions sur les fonctions intégrées, voir [Mapper un élément à l&#39;aide de fonctions intégrées](/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md).

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tout package de workflow Adobe Workfront et tout package d’automatisation et d’intégration Adobe Workfront</p><p>Workfront Ultimate</p><p>Packages Workfront Prime et Select, avec l’achat supplémentaire de Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licences Adobe Workfront</td> 
   <td> <p>Standard</p><p>Travail ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p><ul><li>Si votre organisation dispose d’un package Workfront Select ou Prime qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acquérir Adobe Workfront Fusion.</li><li>Vous devez disposer d’une licence Adobe App Builder pour utiliser des fonctions personnalisées.</ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Configuration d’une fonction personnalisée

Vous pouvez créer une fonction personnalisée dans la zone Fonctions qui peut être utilisée dans plusieurs scénarios ou configurer des fonctions personnalisées dans des scénarios individuels.

* [Créer une fonction personnalisée à utiliser dans plusieurs scénarios](#create-a-custom-function-to-use-in-multiple-scenarios)
* [Création d’une fonction personnalisée dans un scénario](#create-a-custom-function-within-a-scenario)

### Créer une fonction personnalisée à utiliser dans plusieurs scénarios

Les fonctions personnalisées qui peuvent être utilisées dans plusieurs scénarios sont configurées dans la zone Fonctions de Workfront Fusion. Une fois qu’une fonction est configurée, vous pouvez l’ajouter à un scénario à l’aide du connecteur Adobe App Builder.

* [Initialiser votre environnement d’exécution](#initialize-your-runtime-environment)
* [Connecter un projet App Builder existant](#connect-an-existing-app-builder-project)
* [Créez une fonction personnalisée dans la zone Fonctions](#create-a-custom-function-in-the-functions-area)

#### Initialiser votre environnement d’exécution

Avant de pouvoir créer des fonctions personnalisées, vous devez initialiser votre environnement d’exécution. Cela ne doit être effectué que si votre équipe ne dispose d’aucune fonction personnalisée.

>[!IMPORTANT]
>
>L’initialisation ne peut être effectuée que par un utilisateur ayant accès à Adobe App Builder, qu’il soit développeur ou administrateur système au sein de l’organisation IMS.
>
>Une fois l’initialisation terminée, tous les utilisateurs de l’équipe dans laquelle l’initialisation a été effectuée peuvent créer et utiliser des fonctions.

1. Cliquez sur l’onglet **Fonctions** ![Icône de fonctions](assets/functions-icon.png) dans le panneau de gauche.

   Si vous n’avez pas encore configuré votre environnement d’exécution, le message « Environnement d’exécution non configuré » s’affiche.
1. Cliquez sur **Initialiser l’exécution**.

   Au bout d’un certain temps, une liste de fonctions s’affiche, avec deux exemples de fonctions.

#### Connecter un projet App Builder existant

Lorsque Fusion crée le projet App Builder, il gère la configuration d’exécution pour vous. Si votre équipe dispose déjà d’un projet App Builder créé avant l’utilisation de Fusion, vous devez le connecter manuellement en créant une connexion App Builder qui utilise l’espace de noms et les informations d’identification d’exécution de ce projet. Vous n’avez pas besoin de recréer le projet.

>[!NOTE]
>
>Les informations d’identification que vous saisissez dans Fusion sont des informations d’identification d’exécution. Il ne s’agit pas de vos informations de connexion à Adobe. Gardez sécurisé le fichier de configuration que vous téléchargez et ne partagez pas sa valeur `auth`.

1. Dans Fusion, sélectionnez l’équipe qui a besoin de la connexion.
1. Cliquez sur l’onglet **Connexions** dans le panneau de gauche, puis sur **Créer une connexion**.
1. Sélectionnez **Adobe App Builder** comme type de connexion et saisissez un nom qui identifie le projet existant.
1. Dans le [Adobe Developer Console](https://developer.adobe.com/console), ouvrez le projet existant, puis sélectionnez l’espace de travail auquel vous souhaitez vous connecter.
1. Dans la présentation du projet, cliquez sur **Télécharger tout** pour télécharger le fichier JSON de configuration de l’espace de travail, puis ouvrez le fichier dans un éditeur de texte.
1. Dans la section `runtime` du fichier, recherchez la valeur `namespace`. Dans Fusion, saisissez-le dans le champ **Espace de noms**.
1. Dans la section `runtime`, recherchez la valeur `auth`. Il a le format `username:password`.

   * Dans Fusion, saisissez la partie située avant le signe des deux-points dans le champ **Nom d’utilisateur**.
   * Dans Fusion, saisissez la partie après le signe des deux-points dans le champ **Mot de passe**.

1. Cliquez sur **Continuer** pour enregistrer la connexion.
1. Revenez à l’onglet **Fonctions** dans Fusion et actualisez la page si nécessaire.

Pour plus d’informations sur les champs de connexion, voir [Modules Adobe App Builder](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-app-builder.md#create-a-connection-to-adobe-app-builder).

#### Créez une fonction personnalisée dans la zone Fonctions

Une fois votre environnement d’exécution configuré, vous pouvez commencer à créer des fonctions personnalisées.

>[!IMPORTANT]
>
>* Votre fonction personnalisée **doit** être une fonction JavaScript.
>* Votre fonction personnalisée **doit** renvoyer un objet.
>* Après avoir créé une fonction personnalisée, vous ne pouvez pas :
>
>   * Modifier son nom
>   * Afficher les valeurs de paramètre par défaut

1. Cliquez sur l’onglet **Fonctions** ![Icône de fonctions](assets/functions-icon.png) dans le panneau de gauche.
1. Cliquez sur **Ajouter une fonction**.
1. Saisissez le nom de la fonction personnalisée.

   Vous ne pourrez pas modifier ce nom ultérieurement.
1. Saisissez le code de la fonction.
1. Pour chaque valeur de paramètre par défaut que vous souhaitez ajouter, cliquez sur **Ajouter un paramètre** et saisissez le nom du paramètre et la valeur par défaut.

   Vous pouvez remplacer les paramètres par défaut lors de l’ajout de la fonction à un scénario.
1. Cliquer sur **Enregistrer**.

### Création d’une fonction personnalisée dans un scénario

Pour créer une fonction personnalisée dans un scénario, utilisez le module **Exécuter un bloc de code personnalisé** dans le connecteur Adobe App Builder.

Pour obtenir des instructions, voir [Module Adobe App Builder](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-app-builder.md).

## Ajouter une fonction personnalisée à un scénario

Pour ajouter une fonction personnalisée à un scénario, utilisez le connecteur Adobe App Builder.

Pour obtenir des instructions, voir [Module Adobe App Builder](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-app-builder.md).

