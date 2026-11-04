---
title: Expliquer une erreur de scénario à l’aide de l’IA
description: Lorsque l’exécution d’un scénario échoue, vous pouvez cliquer sur Expliquer en regard de l’erreur pour obtenir une description courte et en langage clair de l’erreur et de la manière de la corriger.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: e2420c8a25fd9e38c4b0300b00560fe1837a5e43
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 15%
---
# Expliquer une erreur de scénario à l’aide de l’IA

Lorsque l’exécution d’un scénario échoue, l’IA peut vous donner une description courte et en langage clair de l’erreur et de la manière de la corriger. L’explication s’affiche en regard de l’erreur d’origine, vous pouvez donc lire les deux ensemble.

Vous pouvez expliquer les erreurs dans les domaines suivants de Workfront Fusion :

* Détails de l’erreur de module dans le concepteur de scénarios
* Détails d’exécution dans l’historique d’exécution d’un scénario
* Le tableau [!UICONTROL Journaux d’exécutions en échec] sur la page Insights

>[!NOTE]
>
>Le bouton **[!UICONTROL Expliquer]** n’est disponible que dans le nouveau concepteur de scénario. Il n’est pas disponible dans l’ancien concepteur de scénarios.

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

## Expliquez une erreur dans les détails de sortie du module

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez expliquer une erreur.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Exécutez le scénario comme prévu ou en cliquant sur **Exécuter une fois**.
1. Lorsqu’un module échoue, ouvrez les détails de l’erreur du module.
1. Cliquez sur **[!UICONTROL Expliquer]**.

   Le bouton se trouve sous l’erreur.

   ![Expliquer l’erreur dans la sortie du module](assets/explain-in-module-output.png)

L’explication s’affiche sous l’erreur.

>[!NOTE]
>
> * Tandis que l’IA génère l’explication, un état de chargement s’affiche.
> * Si la génération de l’explication échoue, cliquez sur **[!UICONTROL Réessayer]**.
> * Si votre organisation atteint sa limite d’utilisation de l’IA, un message de limite d’utilisation s’affiche au lieu d’une explication.

## Expliquer une erreur dans l’historique d’exécution d’un scénario

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche, puis cliquez sur le scénario.
1. Cliquez sur **[!UICONTROL Historique]** près du nom du scénario.
1. Cliquez sur l’exécution ayant échoué que vous souhaitez afficher.

   Chaque erreur dans les détails de l’exécution est associée à un bouton **[!UICONTROL Expliquer]**.

1. Cliquez sur **[!UICONTROL Expliquer]** sous l’erreur que vous souhaitez expliquer.

   Si plusieurs modules ont échoué lors de l’exécution, vous pouvez expliquer chaque erreur seule.

   ![Expliquer dans l’historique d’exécution](assets/explain-in-execution-details.png)

Pour plus d’informations sur l’affichage d’une exécution, voir [Afficher l’historique d’exécution d’un scénario](/help/workfront-fusion/manage-scenarios/view-scenario-execution-history.md) et [Afficher l’exécution d’un scénario spécifique](/help/workfront-fusion/manage-scenarios/view-a-specific-scenario-execution.md).

>[!NOTE]
>
> * Tandis que l’IA génère l’explication, un état de chargement s’affiche.
> * Si la génération de l’explication échoue, cliquez sur **[!UICONTROL Réessayer]**.
> * Si votre organisation atteint sa limite d’utilisation de l’IA, un message de limite d’utilisation s’affiche au lieu d’une explication.

## Expliquer une erreur sur la page Insights

1. Dans Fusion, cliquez sur **[!UICONTROL Insights]** dans le volet de navigation de gauche.
1. Dans le tableau [!UICONTROL Échec des exécutions], passez la souris sur la ligne en échec que vous souhaitez afficher.

   Un bouton **[!UICONTROL Expliquer]** s’affiche.

1. Cliquez sur **[!UICONTROL Expliquer]**.

   ![Expliquer dans la page Insights](assets/explain-failed-execution-log.png)

   Une fenêtre contextuelle s’ouvre, qui affiche l’erreur et l’explication de l’IA.

Pour plus d’informations sur la page Insights, voir [Afficher le tableau de bord Insights pour une organisation](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/view-insights-dashboard.md).

>[!NOTE]
>
> * Tandis que l’IA génère l’explication, un état de chargement s’affiche.
> * Si la génération de l’explication échoue, cliquez sur **[!UICONTROL Réessayer]**.
> * Si votre organisation atteint sa limite d’utilisation de l’IA, un message de limite d’utilisation s’affiche au lieu d’une explication.
