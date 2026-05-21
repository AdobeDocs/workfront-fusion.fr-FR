---
title: file d'attente de k
description: De nombreux services proposent des webhooks pour envoyer des notifications instantanées chaque fois que le service est modifié. Les déclencheurs instantanés, également appelés webhooks, peuvent utiliser ces événements pour lancer des scénarios. Les événements sont placés dans la file d’attente du webhook lorsqu’ils sont en attente de traitement, par exemple lorsque le scénario est déjà en cours d’exécution. Vous pouvez afficher la file d’attente du webhook.
author: Becky
feature: Workfront Fusion
exl-id: 04aed0cb-e837-4c81-8eb1-113075d2ada8
TQID: https://experienceleague.adobe.com/FtTjoNtYNM9kuPDMaHa4883m13pLO2MRat5ohnjXuAM
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 331
ht-degree: 47%

---

# Afficher la file d’attente d’un webhook

De nombreux services proposent des webhooks pour envoyer des notifications instantanées chaque fois que le service est modifié. Les déclencheurs instantanés, également appelés webhooks, peuvent utiliser ces événements pour lancer des scénarios. Les événements sont placés dans la file d’attente du webhook lorsqu’ils sont en attente de traitement, par exemple lorsque le scénario est déjà en cours d’exécution. Vous pouvez afficher la file d’attente du webhook.

Les données webhook entrantes sont toujours stockées dans la file d’attente, quelle que soit la manière dont vous avez défini l’option Les données sont confidentielles dans le panneau des paramètres du scénario. Une fois les données traitées dans un scénario, elles sont définitivement supprimées de la file d’attente.

Pour plus d’informations sur les webhooks, consultez la section [Déclencheurs instantanés (webhooks)](/help/workfront-fusion/references/modules/webhooks-reference.md).

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

## Afficher la file d’attente d’un webhook

Tous les messages des webhooks entrants sont stockés dans la file d’attente du webhook.

Si un scénario comporte actuellement une file d’attente, une bannière s’affiche dans ce scénario :

![Bannière de file d’attente](assets/queue-banner.png)

Pour afficher la file d’attente d’un webhook :

1. Cliquez sur **[!UICONTROL Webhooks]** dans le menu de gauche.
1. Recherchez le Webhook pour lequel vous souhaitez afficher la file d’attente.
1. Recherchez le nombre d’événements dans le bouton Événements reçus .

   ![File d’attente Webhook](assets/webhook-queue.png)

1. Cliquez sur le bouton pour afficher les détails des événements dans la file d’attente.
