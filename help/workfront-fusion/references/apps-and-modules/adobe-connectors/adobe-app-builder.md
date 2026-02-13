---
title: Module Adobe App Builder
description: Le connecteur Adobe App Builder vous permet d’utiliser des fonctions personnalisées dans vos scénarios.
author: Becky
feature: Workfront Fusion
source-git-commit: 8250d4fdad8ed7ffe63cd003f6e0cb325cbbfa8d
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 31%

---

# Module Adobe App Builder

Vous pouvez créer des fonctions personnalisées dans la zone Fonctions de Fusion. Vous ajoutez ensuite ces fonctions à vos scénarios sous la forme d’un module Adobe App Builder .

Les fonctions personnalisées fonctionnent via Adobe App Builder. Votre entreprise doit donc disposer d’une licence Adobe App Builder pour les utiliser.

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

## Module Adobe App Builder

Le seul module Adobe App Builder actuellement disponible est Exécuter une action , qui vous permet d’utiliser une fonction JavaScript personnalisée configurée précédemment.

Pour obtenir des instructions sur la configuration d’une fonction personnalisée, voir [Mapper des données à l’aide de fonctions personnalisées](/help/workfront-fusion/create-scenarios/map-data/map-using-custom-functions.md).

### Exécuter une action

Ce module exécute une fonction personnalisée configurée précédemment.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Sélectionnez la connexion contenant la fonction personnalisée que vous souhaitez exécuter. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td>Sélectionnez la fonction personnalisée que vous souhaitez exécuter.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Paramètres [!UICONTROL] </td> 
   <td>Saisissez les valeurs des paramètres de la fonction. Les paramètres disponibles sont basés sur les paramètres configurés lors de la création de la fonction.<p>Si un paramètre possède une valeur par défaut, vous ne le verrez pas dans le champ, mais vous pouvez le remplacer en saisissant ou en mappant une valeur dans le champ.</p></td> 
  </tr> 
   </tbody> 
</table>


