---
title: Module Adobe App Builder
description: Le connecteur Adobe App Builder vous permet d’utiliser des fonctions personnalisées dans vos scénarios.
author: Becky
feature: Workfront Fusion
exl-id: 92661a0c-436b-4fbd-808a-a4fbe3cd2339
source-git-commit: 4392b9d13c49d3d64b2b694bf23cfc227ae36d02
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 26%

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

## Modules Adobe App Builder

### Exécution d’un bloc de code personnalisé

Ce module vous permet d’exécuter un bloc de code. Vous configurez le bloc de code lorsque vous configurez le module, qui est exécuté lorsque le module s’exécute lors de l’exécution d’un scénario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Sélectionnez la connexion contenant la fonction personnalisée que vous souhaitez exécuter. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Code block]</td> 
   <td>Saisissez le bloc de code que le module doit exécuter.<p>Pour formater le code afin de le lire plus facilement, cliquez sur l’icône <b>Formater le code</b>.</td> 
  </tr> 
   </tbody> 
</table>

### Exécution d’une fonction personnalisée

Ce module vous permet d’utiliser une fonction JavaScript personnalisée configurée précédemment et stockée dans la zone Fonctions .

Pour obtenir des instructions sur la configuration d’une fonction personnalisée, voir [Mapper des données à l’aide de fonctions personnalisées](/help/workfront-fusion/create-scenarios/map-data/map-using-custom-functions.md).

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
   <td role="rowheader">Paramètres  </td> 
   <td>Saisissez les valeurs des paramètres de la fonction. Les paramètres disponibles sont basés sur les paramètres configurés lors de la création de la fonction.<p>Si un paramètre possède une valeur par défaut, vous ne le verrez pas dans le champ, mais vous pouvez le remplacer en saisissant ou en mappant une valeur dans le champ.</p></td> 
  </tr> 
   </tbody> 
</table>
