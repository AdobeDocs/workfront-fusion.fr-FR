---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: scenarios
title: Gérer des scénarios verrouillés
description: Gérer des scénarios verrouillés dans  [!DNL Adobe Workfront Fusion]
author: Becky
feature: Workfront Fusion
exl-id: b5e92bdc-cc1d-4b22-8c5f-42cc279d5590
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 72%

---

# Gérer des scénarios verrouillés

Dans certains cas, un scénario peut être temporairement verrouillé dans [!DNL Workfront Fusion]. Les scénarios verrouillés seront automatiquement déverrouillés dans les 2 à 4 heures. Vous pouvez déverrouiller les scénarios manuellement, mais cela n’est généralement pas recommandé.

Les scénarios peuvent être verrouillés pour plusieurs raisons :

* Workfront Fusion ne prend pas en charge le traitement parallèle de scénarios planifiés. Ces scénarios sont verrouillés au début de l’exécution du scénario et déverrouillés à la fin. Si l’exécution est interrompue, le scénario peut ne pas se déverrouiller. Cela peut se produire lorsqu’un utilisateur ou une utilisatrice force manuellement l’arrêt du scénario ou en cas de problème du système.

* L’équipe d’ingénieurs de Workfront Fusion peut verrouiller un scénario en raison de problèmes de performances ou autres.

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] paquet</td> 
   <td> <p>Tous</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licence</td> 
   <td> <p>Nouveau : [!UICONTROL Standard]</p><p>Ou</p><p>En cours : [!UICONTROL Work] ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licence**</td> 
   <td>
   <p>Actuelle : aucune exigence de licence [!DNL Workfront Fusion] requise.</p>
   <p>Ou</p>
   <p>Héritée : n’importe laquelle. </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Nouveau :</p> <ul><li>[!UICONTROL Select] ou [!UICONTROL Prime] plan de [!DNL Workfront] : votre entreprise doit acheter des [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] plan : [!DNL Workfront Fusion] est inclus.</li></ul>
   <p>Ou</p>
   <p>Actuel : votre entreprise doit acheter [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurations du niveau d’accès*</td> 
   <td> 
     <p>Vous devez être un administrateur ou une administratrice [!DNL Workfront Fusion] de votre organisation.</p>
     <p>Vous devez être un administrateur ou une administratrice [!DNL Workfront Fusion] de votre équipe.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++


## Déverrouiller un scénario verrouillé

Les scénarios verrouillés seront déverrouillés 2 à 4 heures après leur verrouillage. Vous pouvez déverrouiller un scénario manuellement avant qu’il ne soit automatiquement déverrouillé.

>[!WARNING]
>
>Le déverrouillage manuel d’un scénario peut entraîner des erreurs d’exécution du scénario. Nous vous recommandons de déverrouiller manuellement les scénarios uniquement lorsqu’un scénario est verrouillé en raison du démarrage et de l’arrêt des exécutions dans le cadre de la conception du scénario. Dans d’autres cas, nous vous recommandons d’attendre que le scénario soit déverrouillé automatiquement.


Pour déverrouiller manuellement un scénario verrouillé :

1. Accédez à la page Détails du scénario du scénario verrouillé.
1. Cliquez sur **[!UICONTROL Options]** dans le coin supérieur droit de l’écran.
1. Sélectionnez **[!UICONTROL Unlock execution]**.
1. Cliquez sur **[!UICONTROL Unlock]**.
   ![](assets/unlock-scenario.png)
