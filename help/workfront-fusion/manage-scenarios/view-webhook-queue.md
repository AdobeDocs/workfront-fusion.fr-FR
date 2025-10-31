---
title: file d'attente de k
description: De nombreux services proposent des webhooks pour envoyer des notifications instantanées chaque fois que le service est modifié. Les déclencheurs instantanés, également appelés webhooks, peuvent utiliser ces événements pour lancer des scénarios. Les événements sont placés dans la file d’attente du webhook lorsqu’ils sont en attente de traitement, par exemple lorsque le scénario est déjà en cours d’exécution. Vous pouvez afficher la file d’attente du webhook.
author: Becky
feature: Workfront Fusion
exl-id: 04aed0cb-e837-4c81-8eb1-113075d2ada8
source-git-commit: 42be02d6a59a5d7b8faccdcfe40e8b967153c6eb
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 23%

---

# Afficher la file d’attente d’un webhook

De nombreux services proposent des webhooks pour envoyer des notifications instantanées chaque fois que le service est modifié. Les déclencheurs instantanés, également appelés webhooks, peuvent utiliser ces événements pour lancer des scénarios. Les événements sont placés dans la file d’attente du webhook lorsqu’ils sont en attente de traitement, par exemple lorsque le scénario est déjà en cours d’exécution. Vous pouvez afficher la file d’attente du webhook.

Les données webhook entrantes sont toujours stockées dans la file d’attente, quelle que soit la manière dont vous avez défini l’option Les données sont confidentielles dans le panneau des paramètres du scénario. Une fois les données traitées dans un scénario, elles sont définitivement supprimées de la file d’attente.

Pour plus d’informations sur les webhooks, voir [Déclencheurs instantanés (webhooks)](/help/workfront-fusion/references/modules/webhooks-reference.md).

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
