---
title: Contrôle de flux
description: Lorsque vous créez ou modifiez un scénario, vous pouvez configurer des paramètres pour contrôler la manière dont les données transitent dans celui-ci.
author: Becky
feature: Workfront Fusion
exl-id: b3aed366-c399-44fa-8967-54ecb8647d96
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 66%

---

# Contrôle de flux

Lorsque vous créez ou modifiez un scénario, vous pouvez configurer des paramètres pour contrôler la manière dont les données transitent dans celui-ci.

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tous</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licence Adobe Workfront</td> 
   <td> <p>Nouveau : Standard</p><p>Ou</p><p>En cours : Travail ou version ultérieure</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licence Adobe Workfront Fusion **</td> 
   <td>
   <p>Aucune exigence de licence Workfront Fusion</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Nouveau :</p> <ul><li>Sélectionnez ou le package Prime Workfront : votre entreprise doit acheter Adobe Workfront Fusion.</li><li>Package Ultimate Workfront : Workfront Fusion est inclus.</li></ul>
   <p>Ou</p>
   <p>Actuel : votre entreprise doit acheter Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Répéteur

Vous pouvez utiliser un module [!UICONTROL Répéteur] pour répéter une tâche un nombre de fois défini. Une module [!UICONTROL Répéteur] génère des lots l’un après l’autre.


<table>
    <tr>
        <td>[!UICONTROL Valeur initiale]</td>
        <td>Saisissez ou mappez la valeur que le module doit avoir dans la première itération. La valeur par défaut est 1.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Repeats]</td>
        <td>Saisissez ou mappez le nombre de répétitions du module. Ce nombre doit être supérieur ou égal à 0 et inférieur ou égal à 10 000.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Step]</td>
        <td>Il s’agit du nombre par lequel le module augmente la valeur. La valeur par défaut est 1.</td>
    </tr>
</table>

>[!BEGINSHADEBOX]

Par exemple, vous pouvez utiliser un module [!UICONTROL Répéteur] pour envoyer cinq e-mails avec les objets « Bonjour 1 », « Bonjour 2 », et ainsi de suite, en connectant le module **[!UICONTROL E-mail] > [!UICONTROL M’envoyer un e-mail]** au module [!UICONTROL Répéteur].

1. Cliquez sur l’icône [!UICONTROL Contrôle de flux] ![Icône Contrôle de flux](/help/workfront-fusion/references/apps-and-modules/assets/flow-control-icon.gif) en bas de l’écran, puis cliquez sur **[!UICONTROL Répéteur]** dans le menu qui s’affiche.
1. Cliquez sur le module [!UICONTROL Répéteur], puis sur **[!UICONTROL Se connecter automatiquement]** dans la zone qui s&#39;affiche.

   Le module Répéteur s’ouvre.

1. Dans le champ **[!UICONTROL Répétitions]**, saisissez le nombre de répétitions (lots sortis) que le module doit produire.

   Dans cet exemple, entrez 5.

   ![ Répéteur ](/help/workfront-fusion/references/apps-and-modules/assets/repeater-2-350x207.png)

   La valeur de l’élément augmente à chaque répétition selon la valeur spécifiée dans le champ **[!UICONTROL Étape]** que vous pouvez afficher en sélectionnant **[!UICONTROL Afficher les paramètres avancés]**. Ce nombre est 1 par défaut.

1. Cliquez sur **[!UICONTROL OK]** pour fermer la zone **[!UICONTROL Contrôle du flux]**.

1. Cliquez sur l’application ou le module de service connecté au module [!UICONTROL Répéteur].
1. Dans la zone qui s’affiche, saisissez les informations que vous souhaitez répéter.

   Dans notre exemple d’e-mail, vous devez saisir Bonjour dans le champ [!UICONTROL Objet], puis mapper `i` à partir du module répéteur.

   ![ Répéteur ](/help/workfront-fusion/references/apps-and-modules/assets/repeater-3-350x207.png)



>[!NOTE]
>
>Le nombre de répétitions n’est pas déterminé par la valeur de `i`, comme c’est le cas dans une boucle de programmation. Le module effectue autant de répétitions que le nombre indiqué dans le champ [!UICONTROL Répétitions]. La valeur `i` change à chaque itération du module [!DNL repeater] et peut être mappée à des modules ultérieurs. L’exemple ci-dessus mappe la valeur de `i` au message Bonjour, ce qui entraîne la création des messages « Bonjour 1 », « Bonjour 2 », et ainsi de suite.

>[!ENDSHADEBOX]

## [!UICONTROL Itérateur]

Un [!UICONTROL Itérateur] est un type spécial de module qui convertit un tableau en une série de lots. Chaque élément du tableau constitue un lot distinct dans la sortie du module [!UICONTROL Itérateur]. Pour plus d’informations, voir [Module Itérateur](/help/workfront-fusion/references/modules/iterator-module.md).

## Agrégateur de tableaux

Un agrégateur de tableaux est un type spécial de module qui permet de fusionner plusieurs lots en un seul lot. Pour plus d’informations, voir [Module d’agrégation](/help/workfront-fusion/references/modules/aggregator-module.md).

## [!UICONTROL Routeur]

Le module [!UICONTROL Routeur] vous permet de diviser votre flux en plusieurs itinéraires et de traiter les données de chaque itinéraire de manière différente. Dès qu’un module [!UICONTROL Routeur] reçoit un lot, il le transfère vers chaque itinéraire connecté dans l’ordre dans lequel les itinéraires ont été associés au module [!UICONTROL Routeur]. Pour plus d’informations, voir [Module routeur dans Adobe Workfront Fusion](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).

## Directives

Les directives de gestion des erreurs vous permettent de contrôler la manière dont votre scénario réagit aux erreurs.

Pour plus d’informations sur les directives de gestion des erreurs, voir [Directives de gestion des erreurs](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

