---
title: Recherche et remplacement de variables, de sources et de connexions dans un scénario
description: Utilisez Rechercher et remplacer pour remplacer une variable mappée, remapper des références d’un module source à un autre ou copier une connexion à d’autres modules de votre scénario.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
source-git-commit: 94449f8511d7480f1a4fc0ac6e8db9b067977abd
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 15%
---

# Recherche et remplacement de variables, de sources et de connexions dans un scénario

>[!NOTE]
>
>Cette fonctionnalité n’est disponible que dans la nouvelle expérience de l’éditeur de scénarios. Pour plus d’informations, voir [Expériences nouvelles et classiques](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences) dans l’éditeur de scénarios d’article.

Rechercher et remplacer vous permet d’effectuer la même modification sur de nombreux modules à la fois. Vous pouvez :

* Remplacez une variable mappée sur l’ensemble du scénario ou dans un seul module.
* Remapper des références d’un module source à un autre.
* Copiez une connexion vers un ou tous les modules compatibles depuis la même application.

Avant d’apporter une modification, Rechercher et remplacer affiche un aperçu des modules qui seront affectés.

Dans l’expérience classique, vous pouvez utiliser la variable Swap, la source Remap et les outils de connexion Swap dans l’outil de développement pour effectuer ces tâches. Pour plus d’informations, voir [Déboguer un scénario](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md).

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
   <p>Si votre organisation dispose d’un package Workfront Select ou Prime qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acquérir Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation Workfront](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Ouvrir Rechercher et remplacer

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez apporter des modifications.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Cliquez sur l&#39;icône **Rechercher et remplacer** ![Rechercher et remplacer](assets/find-replace-icon.png) dans la zone Contrôles.

   Vous devrez peut-être cliquer sur l&#39;icône des trois points dans la zone Contrôles pour voir l&#39;icône Rechercher et remplacer.

Rechercher et remplacer s’ouvre dans le panneau sur le côté droit de la zone de travail.

## Remplacer une variable

Utilisez l’onglet **Variable** pour remplacer une variable mappée.

1. Ouvrez Rechercher et remplacer, puis cliquez sur l’onglet **Variable**.
1. Dans le champ Variable à rechercher , collez la variable à remplacer.
1. Dans le champ Remplacer par , collez dans la variable qui remplacera la variable précédente.
1. Dans le champ Module , choisissez le module auquel la modification s’appliquera, ou sélectionnez **Scénario entier** pour appliquer la modification à tous les modules concernés du scénario.
1. Cliquez sur **Remplacer**
1. Consultez l’aperçu des modules qui seront affectés. Pour accéder à un module sur la zone de travail, sélectionnez sa ligne dans l’aperçu.
1. Cliquez sur **Appliquer**.

## Remapper une source

Utilisez l&#39;onglet **&#x200B;**&#x200B;pour modifier le module auquel les mappages dans d&#39;autres modules font référence.

1. Ouvrez Rechercher et remplacer, puis cliquez sur l’onglet **&#x200B;**.
1. Dans le champ Module Source , sélectionnez le module source auquel les mappages font actuellement référence.
1. Dans les champs Module cible , sélectionnez le module auquel ils doivent faire référence à la place.
1. Dans le champ Module , choisissez le module auquel la modification s’appliquera, ou sélectionnez **Scénario entier** pour appliquer la modification à tous les modules concernés du scénario.
1. Cliquez sur **Remplacer**
1. Consultez l’aperçu des modules qui seront affectés. Pour accéder à un module sur la zone de travail, sélectionnez sa ligne dans l’aperçu.
1. Cliquez sur **Appliquer**.

## Copier une connexion vers d’autres modules

Utilisez l’onglet **Connexion** pour utiliser la même connexion dans plusieurs modules de la même application.

1. Ouvrez Rechercher et remplacer, puis cliquez sur l’onglet **Connexion**.
1. Dans le champ Connexion à partir de , sélectionnez un module qui possède actuellement la connexion que vous souhaitez utiliser pour d’autres modules.
1. Dans le champ Appliquer à, choisissez le module auquel la modification s’appliquera ou si vous souhaitez appliquer la modification à tous les modules compatibles du scénario.
1. Cliquez sur **Appliquer**.
