---
title: Configuration d’un webhook pour un service web sans connecteur
description: Si un service web ne dispose pas actuellement d’un connecteur dédié dans Workfront Fusion, mais qu’il prend en charge l’envoi de Webhooks, vous pouvez ajouter le service à un scénario à l’aide du module Webhook personnalisé comme déclencheur instantané.
author: Becky
feature: Workfront Fusion
exl-id: 51ef13fb-2978-4927-8d5f-7d83995f11e0
source-git-commit: c83070a7c2d1d048000a4eace4aaede73c7ec49d
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 15%

---

# Configuration d’un webhook pour un service web sans connecteur

Si un service web ne dispose pas actuellement d’un connecteur dédié dans Workfront Fusion, mais qu’il prend en charge l’envoi de Webhooks, vous pouvez ajouter le service à un scénario à l’aide du module Webhook personnalisé comme déclencheur instantané. Ce processus est appelé réception d’un webhook, et il nécessite une configuration du côté de l’application à laquelle vous vous connectez.

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tout package de workflow Adobe Workfront et tout package d’automatisation et d’intégration Adobe Workfront</p><p>Workfront Ultimate</p><p>les packages Workfront Prime et Select, avec un achat supplémentaire de Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licences Adobe Workfront</td> 
   <td> <p>Standard</p><p>Travail ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Si votre entreprise dispose d’un package Select ou Prime Workfront qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acheter Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Recevoir un webhook

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez ajouter un webhook.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Ajoutez le module **Webhooks > Custom webhook** pour commencer votre scénario.
1. Cliquez sur **Ajouter** en regard du champ Webhook.
1. Saisissez un **nom du Webhook** dans la zone qui s’affiche
1. (Facultatif) configurez le webhook.

   Pour obtenir des instructions, voir [ Webhooks ](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md).

1. Cliquer sur **Enregistrer**.

1. Cliquez sur **Copier l’adresse dans le presse-papiers**, puis cliquez sur **OK**.

1. Connectez-vous au service web et procédez comme suit :

   1. Dans la zone Paramètres du service web, créez un webhook.

      Les instructions spécifiques dépendent de l’application. Nous vous recommandons de rechercher « Créer un webhook » dans la documentation de l’application.
   1. Collez l’adresse que vous avez copiée dans le presse-papiers à l’étape 3.
   1. Sélectionnez l’événement qui déclenchera le webhook.

1. Exécutez le scénario.

   Lorsque le ou les événements se produisent, le module webhook personnalisé se déclenche et le scénario s’exécute.
