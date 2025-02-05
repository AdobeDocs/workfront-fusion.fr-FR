---
title: Contrôle de flux
description: Lorsque vous créez ou modifiez un scénario, vous pouvez configurer des paramètres pour contrôler la manière dont les données transitent dans celui-ci.
author: Becky
feature: Workfront Fusion
exl-id: b3aed366-c399-44fa-8967-54ecb8647d96
source-git-commit: 5a95b2c191d4e6d8750dc57a47923f416612b4a9
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 38%

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
   <p>Aucune exigence de licence Workfront Fusion.</p>
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

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], consultez [[!DNL Adobe Workfront Fusion] licences](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Répéteur

Vous pouvez utiliser un module [!UICONTROL Repeater] pour répéter une tâche un certain nombre de fois. Un module [!UICONTROL Repeater] génère des lots, l’un après l’autre.


<table>
    <tr>
        <td>[!UICONTROL Initial value]</td>
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

Par exemple, vous pouvez utiliser un module [!UICONTROL Repeater] pour envoyer cinq e-mails avec les sujets « Hello 1 », « Hello 2 », etc., en connectant le module **[!UICONTROL Email]>[!UICONTROL Send me an email]** au module [!UICONTROL Repeater].

1. Cliquez sur l’icône [!UICONTROL Flow Control] ![Icône Contrôle de flux](/help/workfront-fusion/references/apps-and-modules/assets/flow-control-icon.gif) en bas de l’écran, puis sur **[!UICONTROL Repeater]** dans le menu qui s’affiche.
1. Cliquez sur le module [!UICONTROL Repeater], puis sur **[!UICONTROL Connect automatically]** dans la zone qui s&#39;affiche.

   Le module Répéteur s’ouvre.

1. Dans le champ **[!UICONTROL Repeats]** , saisissez le nombre de répétitions (lots sortis) que le module doit produire.

   Dans cet exemple, entrez 5.

   ![ Répéteur ](/help/workfront-fusion/references/apps-and-modules/assets/repeater-2-350x207.png)

   La valeur de l&#39;article augmente à chaque répétition de cette valeur spécifiée dans le champ **[!UICONTROL Step]**, que vous pouvez afficher en sélectionnant **[!UICONTROL Show advanced settings]**. Ce nombre est 1 par défaut.

1. Cliquez sur **[!UICONTROL OK]** pour fermer la boîte de **[!UICONTROL Flow Control]**.

1. Cliquez sur le module d’application ou de service connecté au module de [!UICONTROL Repeater].
1. Dans la zone qui s’affiche, saisissez les informations que vous souhaitez répéter.

   Dans notre exemple d’e-mail, vous devez saisir Hello dans la zone de [!UICONTROL Subject], puis mapper les `i` du module de répétition.

   ![ Répéteur ](/help/workfront-fusion/references/apps-and-modules/assets/repeater-3-350x207.png)



>[!NOTE]
>
>Le nombre de répétitions n’est pas déterminé par la valeur de `i`, comme c’est le cas dans une boucle de programmation. Le module répétera le nombre de fois indiqué dans le champ [!UICONTROL Repeats]. La valeur `i` change à chaque itération du module [!DNL repeater] et peut être mappée à des modules ultérieurs. L’exemple ci-dessus mappe la valeur de `i` au message Bonjour, ce qui entraîne la création des messages « Bonjour 1 », « Bonjour 2 », et ainsi de suite.

>[!ENDSHADEBOX]

## [!UICONTROL Iterator]

Un [!UICONTROL Iterator] est un type spécial de module qui convertit un tableau en une série de lots. Chaque élément de tableau sera un lot distinct dans la sortie du module [!UICONTROL Iterator]. Pour plus d’informations, voir [Module Itérateur](/help/workfront-fusion/references/modules/iterator-module.md).

## Agrégateur de tableaux

Un agrégateur de tableaux est un type spécial de module qui permet de fusionner plusieurs lots en un seul lot. Pour plus d’informations, voir [Module d’agrégation](/help/workfront-fusion/references/modules/aggregator-module.md).

## [!UICONTROL Router]

Le module [!UICONTROL Router] vous permet de diviser votre flux en plusieurs itinéraires et de traiter différemment les données au sein de chaque itinéraire. Une fois qu&#39;un module [!UICONTROL Router] reçoit un lot, il le transmet à chaque route connectée dans l&#39;ordre dans lequel les routes ont été rattachées au module [!UICONTROL Router]. Pour plus d’informations, voir [Module Routeur dans  [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).

## Directives

Les directives de gestion des erreurs vous permettent de contrôler la manière dont votre scénario réagit aux erreurs.

Pour plus d’informations sur les directives de gestion des erreurs, voir [Directives de gestion des erreurs](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

