---
title: Mappage de données à l’aide de fonctions personnalisées
description: Lorsque vous mappez des éléments, vous pouvez utiliser des fonctions pour créer des formules simples ou complexes.
author: Becky
feature: Workfront Fusion
source-git-commit: 109ea8a6b3c37918110dc930a19ac85ef3e6d764
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 20%

---

# Mappage de données à l’aide de fonctions personnalisées

Vous pouvez créer des fonctions personnalisées dans la zone Fonctions de Fusion. Vous ajoutez ensuite ces fonctions à vos scénarios sous la forme d’un module Adobe App Builder .

Les fonctions personnalisées fonctionnent via Adobe App Builder. Votre entreprise doit donc disposer d’une licence Adobe App Builder pour les utiliser.

Les fonctions personnalisées, comme la plupart des éléments de scénario, sont détenues par les équipes.

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

Les fonctions personnalisées sont configurées dans la zone Fonctions de Workfront Fusion. Une fois qu’une fonction est configurée, vous pouvez l’ajouter à un scénario à l’aide du connecteur Adobe App Builder.

### Initialiser votre environnement d’exécution

Avant de pouvoir créer des fonctions personnalisées, vous devez initialiser votre environnement d’exécution. Cela ne doit être effectué que si votre équipe ne dispose d’aucune fonction personnalisée.

>[!IMPORTANT]
>
>L’initialisation ne peut être effectuée que par un utilisateur ayant accès à Adobe App Builder, qu’il soit développeur ou administrateur système au sein de l’organisation IMS.
>
>Une fois l’initialisation terminée, tous les utilisateurs de l’équipe dans laquelle l’initialisation a été effectuée peuvent créer et utiliser des fonctions.

1. Cliquez sur l’onglet **Fonctions** ![Icône Fonctions](assets/functions-icon.png) dans le panneau de gauche.

   Si vous n’avez pas encore configuré votre environnement d’exécution, le message « Environnement d’exécution non configuré » s’affiche.
1. Cliquez sur **Initialiser l’exécution**.

   Au bout d’un certain temps, une liste de fonctions s’affiche, avec deux exemples de fonctions.

### Création d’une fonction personnalisée

Une fois votre environnement d’exécution configuré, vous pouvez commencer à créer des fonctions personnalisées.

>[!IMPORTANT]
>
>* Votre fonction personnalisée **doit** doit être une fonction JavaScript.
>* Votre fonction personnalisée **obligatoire** renvoie un objet .
>* Après avoir créé une fonction personnalisée, vous ne pouvez pas :
>
>   * Modifier son nom
>   * Afficher les valeurs de paramètre par défaut

1. Cliquez sur l’onglet **Fonctions** ![Icône Fonctions](assets/functions-icon.png) dans le panneau de gauche.
1. Cliquez sur **Ajouter une fonction**.
1. Saisissez le nom de la fonction personnalisée.

   Vous ne pourrez pas modifier ce nom ultérieurement.
1. Saisissez le code de la fonction.
1. Pour chaque valeur de paramètre par défaut à ajouter, cliquez sur **Ajouter un paramètre** et saisissez le nom du paramètre et sa valeur par défaut.

   Vous pouvez remplacer les paramètres par défaut lors de l’ajout de la fonction à un scénario.
1. Cliquer sur **Enregistrer**.

## Ajouter une fonction personnalisée à un scénario

Pour ajouter une fonction personnalisée à un scénario, utilisez le connecteur Adobe App Builder.

Pour obtenir des instructions, consultez [Module Adobe App Builder](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-app-builder.md).

