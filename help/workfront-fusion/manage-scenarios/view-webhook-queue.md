---
title: file d'attente de k
description: De nombreux services proposent des webhooks pour envoyer des notifications instantanées chaque fois que le service est modifié. Les déclencheurs instantanés, également appelés webhooks, peuvent utiliser ces événements pour lancer des scénarios. Les événements sont placés dans la file d’attente du webhook lorsqu’ils sont en attente de traitement, par exemple lorsque le scénario est déjà en cours d’exécution. Vous pouvez afficher la file d’attente du webhook.
author: Becky
feature: Workfront Fusion
exl-id: 04aed0cb-e837-4c81-8eb1-113075d2ada8
TQID: 'https://experienceleague.adobe.com/FtTjoNtYNM9kuPDMaHa4883m13pLO2MRat5ohnjXuAM'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 1c28e4007e3e9d6503618482002e506f9393ee57
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 26%
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

![Bannière de file d&#39;attente](assets/queue-banner.png)

La page de file d’attente du webhook a la même disposition que les listes **[!UICONTROL Scénarios]** et **[!UICONTROL Webhooks]**.

>[!NOTE]
>
>La recherche et le tri s’appliquent uniquement aux événements actuellement chargés dans le tableau, et non à la file d’attente entière. Pour inclure d’autres événements, chargez d’abord les événements supplémentaires.

Pour afficher et gérer la file d’attente d’un webhook :

1. Cliquez sur **[!UICONTROL Webhooks]** dans le menu de gauche.
1. Recherchez le Webhook pour lequel vous souhaitez afficher la file d’attente.
1. Recherchez la colonne Nombre d’événements dans la file d’attente complète .

   ![File d’attente Webhook](assets/webhook-queue.png)

1. Cliquez sur le bouton **Opérations** pour afficher les détails des événements dans la file d’attente.

   La page de file d’attente du webhook s’ouvre. La page répertorie les événements de la file d’attente dans une table avec les colonnes suivantes : **[!UICONTROL ID]**, **[!UICONTROL Créé à]**, **[!UICONTROL Taille]** et **[!UICONTROL Détails]**.

1. (Facultatif) Pour filtrer les événements dans le tableau, saisissez du texte dans le champ **[!UICONTROL Rechercher]** au-dessus du tableau.
1. (Facultatif) Pour trier les événements, cliquez sur l’en-tête de colonne **[!UICONTROL ID]**, **[!UICONTROL Créé à]** ou **[!UICONTROL Taille]**.
1. (Facultatif) Pour modifier le nombre d’événements qui s’affichent sur chaque page, sélectionnez un nombre dans la liste déroulante **[!UICONTROL Afficher]** au bas de la page.
1. (Facultatif) Pour vous déplacer entre les pages d’événements, cliquez sur **[!UICONTROL Premier]**, **[!UICONTROL Précédent]**, **[!UICONTROL Suivant]** ou **[!UICONTROL Dernier]** au bas de la page.

   Ces boutons ne sont pas disponibles lorsque la file d’attente ne comporte qu’une seule page d’événements.

1. (Facultatif) Pour afficher la payload d’un événement, cliquez sur **[!UICONTROL Détails]** dans la ligne correspondant à l’événement.

   La boîte de dialogue des détails s’ouvre et affiche la payload de l’événement.

1. (Facultatif) Pour supprimer des événements :

   1. Sélectionnez les événements à supprimer en effectuant l’une des opérations suivantes :

      * Cochez la case en regard de chaque événement à sélectionner.
      * Cochez la case **[!UICONTROL Tout sélectionner]** pour sélectionner l’ensemble de la file d’attente, et pas seulement les événements actuellement chargés. Vous pouvez ensuite décocher toutes les cases des événements que vous souhaitez exclure de la sélection.

   1. Dans la barre située en bas de l&#39;écran, cliquez sur **Supprimer**.
