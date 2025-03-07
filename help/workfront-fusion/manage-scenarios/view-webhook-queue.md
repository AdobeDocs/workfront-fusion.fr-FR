---
title: file d'attente de k
description: De nombreux services proposent des webhooks pour envoyer des notifications instantanées chaque fois que le service est modifié. Les déclencheurs instantanés, également appelés webhooks, peuvent utiliser ces événements pour lancer des scénarios. Les événements sont placés dans la file d’attente du webhook lorsqu’ils sont en attente de traitement, par exemple lorsque le scénario est déjà en cours d’exécution. Vous pouvez afficher la file d’attente du webhook.
author: Becky
feature: Workfront Fusion
exl-id: 04aed0cb-e837-4c81-8eb1-113075d2ada8
source-git-commit: 3d06958b6f706f4f974230853fb6553232656fd3
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 32%

---

# Afficher la file d’attente d’un webhook

De nombreux services proposent des webhooks pour envoyer des notifications instantanées chaque fois que le service est modifié. Les déclencheurs instantanés, également appelés webhooks, peuvent utiliser ces événements pour lancer des scénarios. Les événements sont placés dans la file d’attente du webhook lorsqu’ils sont en attente de traitement, par exemple lorsque le scénario est déjà en cours d’exécution. Vous pouvez afficher la file d’attente du webhook.

Les données webhook entrantes sont toujours stockées dans la file d’attente, quelle que soit la manière dont vous avez défini l’option Les données sont confidentielles dans le panneau des paramètres du scénario. Une fois les données traitées dans un scénario, elles sont définitivement supprimées de la file d’attente.

Pour plus d’informations sur les webhooks, voir [Déclencheurs instantanés (webhooks)](/help/workfront-fusion/references/modules/webhooks-reference.md).

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
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir [[!DNL Adobe Workfront Fusion] Licences](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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
