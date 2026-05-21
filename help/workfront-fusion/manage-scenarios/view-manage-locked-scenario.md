---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: scenarios
title: Gérer des scénarios verrouillés
description: Gestion des scénarios verrouillés dans Adobe Workfront Fusion
author: Becky
feature: Workfront Fusion
exl-id: b5e92bdc-cc1d-4b22-8c5f-42cc279d5590
TQID: https://experienceleague.adobe.com/1eVGWr4SwutYzNmCKB62CCWbQ6ExdXtpjC5BORh-kxo
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 327
ht-degree: 77%

---

# Gérer des scénarios verrouillés

Dans certains cas, un scénario peut être temporairement verrouillé dans Workfront Fusion. Les scénarios verrouillés seront automatiquement déverrouillés dans les 2 à 4 heures. Vous pouvez déverrouiller les scénarios manuellement, mais cela n’est généralement pas recommandé.

Les scénarios peuvent être verrouillés pour plusieurs raisons :

* Workfront Fusion ne prend pas en charge le traitement parallèle de scénarios planifiés. Ces scénarios sont verrouillés au début de l’exécution du scénario et déverrouillés à la fin. Si l’exécution est interrompue, le scénario peut ne pas se déverrouiller. Cela peut se produire lorsqu’un utilisateur ou une utilisatrice force manuellement l’arrêt du scénario ou en cas de problème du système.

* L’équipe d’ingénieurs de Workfront Fusion peut verrouiller un scénario en raison de problèmes de performances ou autres.

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
   <p>Si votre organisation dispose d’un package Workfront Select ou Prime qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acquérir Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Déverrouiller un scénario verrouillé

Les scénarios verrouillés seront déverrouillés 2 à 4 heures après leur verrouillage. Vous pouvez déverrouiller un scénario manuellement avant qu’il ne soit automatiquement déverrouillé.

>[!WARNING]
>
>Le déverrouillage manuel d’un scénario peut entraîner des erreurs d’exécution du scénario. Nous vous recommandons de déverrouiller manuellement les scénarios uniquement lorsqu’un scénario est verrouillé en raison du démarrage et de l’arrêt des exécutions dans le cadre de la conception du scénario. Dans d’autres cas, nous vous recommandons d’attendre que le scénario soit déverrouillé automatiquement.


Pour déverrouiller manuellement un scénario verrouillé :

1. Accédez à la page Détails du scénario du scénario verrouillé.
1. Cliquez sur **[!UICONTROL Options]** dans le coin supérieur droit de l’écran.
1. Sélectionnez **[!UICONTROL Déverrouiller l’exécution]**.
1. Cliquez sur **[!UICONTROL Déverrouiller]**.
   ![Déverrouiller le scénario](assets/unlock-scenario.png)
