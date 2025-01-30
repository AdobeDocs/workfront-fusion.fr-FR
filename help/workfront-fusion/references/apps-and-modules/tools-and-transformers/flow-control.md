---
title: Contrôle de flux
description: Lorsque vous créez ou modifiez un scénario, vous pouvez configurer des paramètres pour contrôler la manière dont les données transitent dans celui-ci.
author: Becky
feature: Workfront Fusion
exl-id: b3aed366-c399-44fa-8967-54ecb8647d96
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 50%

---

# Contrôle de flux

Lorsque vous créez ou modifiez un scénario, vous pouvez configurer des paramètres pour contrôler la manière dont les données transitent dans celui-ci.

## Conditions d’accès

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] formule*</td>
  <td> <p>[!UICONTROL Pro] ou une version ultérieure</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licence*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licence**</td> 
   <td>
   <p>Exigences de licence actuelles : aucune exigence de licence [!DNL Workfront Fusion] requise.</p>
   <p>Ou</p>
   <p>Ancienne exigence de licence : [!UICONTROL [!DNL Workfront Fusion] pour l’automatisation et l’intégration du travail], [!UICONTROL [!DNL Workfront Fusion] pour l’automatisation du travail]</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Exigences actuelles du produit : si vous disposez du plan de [!DNL Adobe Workfront] [!UICONTROL Select] ou [!UICONTROL Prime], votre entreprise doit acheter du [!DNL Adobe Workfront Fusion] et [!DNL Adobe Workfront] utiliser les fonctionnalités décrites dans cet article. [!DNL Workfront Fusion] est inclus dans le plan de [!DNL Workfront] [!UICONTROL Ultimate].</p>
   <p>Ou</p>
   <p>Exigences liées aux produits hérités : votre entreprise doit acheter [!DNL Adobe Workfront Fusion] ainsi qu’[!DNL Adobe Workfront] pour utiliser la fonctionnalité décrite dans cet article.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Pour connaître la formule, le type de licence ou l’accès dont vous disposez, contactez votre équipe d’administration [!DNL Workfront].

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], consultez [[!DNL Adobe Workfront Fusion] licences](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Répéteur

Vous pouvez utiliser un module [!UICONTROL Repeater] pour répéter une tâche un certain nombre de fois. Un module [!UICONTROL Repeater] génère des lots, l’un après l’autre.

Par exemple, vous pouvez utiliser un module [!UICONTROL Repeater] pour envoyer cinq e-mails avec les sujets « Hello 1 », « Hello 2 », etc., en connectant le module **[!UICONTROL Email]>[!UICONTROL Send me an email]** au module [!UICONTROL Repeater].

Pour utiliser un module [!UICONTROL Repeater] :

1. Cliquez sur l’icône [!UICONTROL Flow Control] ![Icône Contrôle de flux](/help/workfront-fusion/references/apps-and-modules/assets/flow-control-icon.gif) en bas de l’écran, puis sur **[!UICONTROL Repeater]** dans le menu qui s’affiche.
1. Cliquez sur le lot [!UICONTROL Repeater], puis sur **[!UICONTROL Connect automatically]** dans la zone qui s’affiche.
1. Dans la zone [!UICONTROL Flow Control] qui s’affiche, saisissez le nombre de répétitions (lots sortis) souhaité dans la zone **[!UICONTROL Repeats]**.

   Dans notre exemple d’e-mail, vous devez saisir 5.

   ![ Répéteur ](/help/workfront-fusion/references/apps-and-modules/assets/repeater-2-350x207.png)

   La valeur de l&#39;article augmente à chaque répétition de cette valeur spécifiée dans le champ **[!UICONTROL Step]**, que vous pouvez afficher en sélectionnant **[!UICONTROL Show advanced settings]**. Ce nombre est 1 par défaut.

1. Cliquez sur **[!UICONTROL OK]** pour fermer la boîte de **[!UICONTROL Flow Control]**.

1. Cliquez sur le module d’application ou de service connecté au module de [!UICONTROL Repeater].
1. Dans la zone qui s’affiche, saisissez les informations que vous souhaitez répéter.

   Dans notre exemple d’e-mail, vous devez saisir Hello dans la zone de [!UICONTROL Subject], puis mapper les `i` du module de répétition.

   ![ Répéteur ](/help/workfront-fusion/references/apps-and-modules/assets/repeater-3-350x207.png)

| Élément | Description |
|---|---|
| [!UICONTROL Initial value] | Saisissez ou mappez le nombre que le module doit définir comme `i` dans la première itération. La valeur par défaut est 1. |
| [!UICONTROL Repeats] | Saisissez ou mappez le nombre de répétitions du module. Ce nombre doit être supérieur ou égal à 0 et inférieur ou égal à 10 000. |
| [!UICONTROL Step] | Il s’agit du nombre selon lequel le module augmente la valeur de `i`. La valeur par défaut est 1. |

{style="table-layout:auto"}

>[!NOTE]
>
>Le nombre de répétitions n’est pas déterminé par la valeur de `i`, comme c’est le cas dans une boucle de programmation. Le module répétera le nombre de fois indiqué dans le champ [!UICONTROL Repeats]. La valeur `i` change à chaque itération du module [!DNL repeater] et peut être mappée à des modules ultérieurs. L’exemple ci-dessus mappe la valeur de `i` au message Bonjour, ce qui entraîne la création des messages « Bonjour 1 », « Bonjour 2 », et ainsi de suite.

## [!UICONTROL Iterator]

Un [!UICONTROL Iterator] est un type spécial de module qui convertit un tableau en une série de lots. Chaque élément de tableau sera un lot distinct dans la sortie du module [!UICONTROL Iterator]. Pour plus d’informations, voir [Module Itérateur](/help/workfront-fusion/references/modules/iterator-module.md).

## Agrégateur de tableaux

Un agrégateur de tableaux est un type spécial de module qui permet de fusionner plusieurs lots en un seul lot. Pour plus d’informations, voir [Module d’agrégation](/help/workfront-fusion/references/modules/aggregator-module.md).

## [!UICONTROL Router]

Le module [!UICONTROL Router] vous permet de diviser votre flux en plusieurs itinéraires et de traiter différemment les données au sein de chaque itinéraire. Une fois qu&#39;un module [!UICONTROL Router] reçoit un lot, il le transmet à chaque route connectée dans l&#39;ordre dans lequel les routes ont été rattachées au module [!UICONTROL Router]. Pour plus d’informations, voir [Module Routeur dans  [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).

<!--
<div>
<h2>Directives</h2>
<p>The error handling directives allow you to control how your scenario reacts to errors. For more information, see <a href="/help/workfront-fusion/create-scenarios/config-error-handling/advanced-error-handling.md" class="MCXref xref">Advanced error handling in Adobe Workfront Fusion</a> and <a href="/help/workfront-fusion/references/errors/directives-for-error-handling.md" class="MCXref xref">Directives for error handling in Adobe Workfront Fusion</a>.</p>
</div>
-->
