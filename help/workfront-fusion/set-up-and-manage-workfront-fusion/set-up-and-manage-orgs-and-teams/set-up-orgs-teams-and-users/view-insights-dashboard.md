---
title: Affichage du tableau de bord des informations pour une organisation
description: Les administrateurs et administratrices de Fusion peuvent afficher un tableau de bord qui affiche les mesures d’exécution pour une organisation.
author: Becky
feature: Workfront Fusion
exl-id: 8f80f86a-69e5-48a1-9812-87322a4959a6
TQID: https://experienceleague.adobe.com/tBZCbpImQxY42gOE8e04aQwCJC8EKgrDTIAt6Sw1KaU
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 557ec6de4ccf0753005fed3e4772d2eb9317537d
workflow-type: tm+mt
source-wordcount: 848
ht-degree: 6%

---

# Affichage du tableau de bord des informations pour une organisation

Le tableau de bord Fusion Insights vous permet de voir rapidement quels scénarios sont les plus exécutés, où les retards se produisent et avec quelle efficacité vos pools de salariés fonctionnent. Vous bénéficiez ainsi d’une visibilité en temps réel sur les volumes d’exécution, la profondeur de file d’attente, l’utilisation du pool et les performances au niveau du scénario.

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Workflow Adobe Workfront Automatisation et intégration d’Ultimate et d’Adobe Workfront Ultimate</p><p>Workfront Ultimate</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licences Adobe Workfront</td> 
   <td> <p>Standard</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurations des niveaux d’accès</td> 
   <td> 
     <p>Vous devez être administrateur ou administratrice Workfront Fusion pour votre entreprise.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation Workfront](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Composants du tableau de bord Insights

>[!NOTE]
>
>Les mesures sont affichées par pool de traitement. Pour afficher un autre pool de traitement, cliquez sur le champ Pool près du coin supérieur gauche du tableau de bord, puis sélectionnez le pool pour lequel vous souhaitez afficher les mesures.

<!--

>[!NOTE]
>
>Organizations can request provisioning for one additional worker pool (for a total of 2).

-->

Dans le tableau de bord Fusion Insights, vous pouvez voir les mesures suivantes.

* **Exécutions en attente de traitement**
Ce graphique montre le nombre d’exécutions en attente de traitement (également appelées liste d’attente d’exécution) à un moment donné.

  Un nombre élevé d’exécutions en attente de traitement peut affecter les performances de votre instance Fusion. Vous recevrez une notification si votre liste d’attente d’exécution atteint 5 000 exécutions. Nous vous recommandons d’identifier les scénarios responsables et de les modifier ou de les désactiver. Si le retard d’exécution élevé persiste, l’équipe de Fusion protège les performances de votre instance Fusion en désactivant les scénarios responsables.
* **Utilisation du pool**
Ce graphique montre l&#39;utilisation du pool de collaborateurs au fil du temps. Si ce graphique montre régulièrement l&#39;utilisation du pool de travail, vous pouvez affecter certains scénarios à un autre pool.

  Si un pool est proche de 100 % d’utilisation, les autres ressources qui utilisent le même pool peuvent être retardées ou interrompues. Si cela se produit, nous vous recommandons de réaffecter un scénario à forte utilisation à un autre pool de traitement ou de modifier les scénarios existants pour qu’ils consomment moins de ressources.
* **Exécutions par scénario**
Ce graphique affiche les exécutions par scénario. Différentes couleurs représentent différents scénarios. Lorsque vous pointez sur le graphique, une fenêtre s’affiche, indiquant la couleur du scénario.

  Vous pouvez utiliser ce graphique pour identifier les scénarios susceptibles de provoquer une liste d&#39;attente d&#39;exécution ou une utilisation élevée du pool de travail.
* **Durée des exécutions**
Ce graphique affiche les exécutions par scénario. Différentes couleurs représentent différents scénarios. Lorsque vous pointez sur le graphique, une fenêtre s’affiche, indiquant la couleur du scénario.

  Vous pouvez utiliser ce graphique pour identifier les scénarios qui prennent plus de temps que d’habitude, y compris ceux affectés par des problèmes liés à une application ou un service connecté.
* **Journal d’exécution**
Ce tableau répertorie chaque exécution de scénario d’échec ou d’avertissement dans votre organisation. Vous pouvez ainsi rechercher et résoudre les problèmes d’exécution sans quitter le tableau de bord.

## Affichage du tableau de bord Fusion Insights

1. Dans Fusion, cliquez sur **Insights** dans le volet de navigation de gauche.

   Le tableau de bord s’ouvre.

1. Pour afficher les données à un moment donné, passez la souris sur un tableau de bord et placez le curseur sur le moment voulu pour l’afficher.

   Une ligne s’affiche au-dessus de ce moment dans tous les graphiques, et une fenêtre affichant les données de ce moment s’affiche sur chaque graphique.
1. Pour afficher les données d’un scénario spécifique dans le graphique Exécutions par scénario ou Durée des exécutions, cliquez sur une barre de couleur du scénario pour lequel vous souhaitez afficher les données. Pour revenir à la vue affichant tous les scénarios, cliquez de nouveau sur le graphique.
1. Pour accéder à un scénario spécifique affiché dans le graphique Exécutions par scénario ou le graphique Durée des exécutions, faites un clic droit sur une barre de couleur du scénario et sélectionnez **Ouvrir le scénario dans un nouvel onglet**.
1. Pour développer un graphique, cliquez sur l’icône **Développer** ![icône Développer](assets/expand-icon.png) dans le coin supérieur droit de ce graphique.
1. Pour modifier la période du tableau de bord, sélectionnez le champ Période dans le coin supérieur droit du tableau de bord, puis sélectionnez une nouvelle période. La période disponible la plus longue est de 24 heures et la plus courte est de 15 minutes.
1. Pour actualiser les graphiques, cliquez sur l’icône Actualiser située en haut à droite du tableau de bord.
1. Pour afficher un autre pool de traitement, cliquez sur le champ Pool près du coin supérieur gauche du tableau de bord, puis sélectionnez le pool à afficher.

## Filtrer et trier les exécutions dans le journal d’exécution

Utilisez le Journal d’exécution pour rechercher les exécutions de scénario ayant échoué ou renvoyé un avertissement dans l’ensemble de votre organisation, et réactivez tous les scénarios qui ont été automatiquement désactivés après des échecs répétés.

1. Dans le journal d’exécution, filtrez les exécutions selon l’une des méthodes suivantes :

   * [!UICONTROL Équipe]
   * [!UICONTROL Scénario]
   * [!UICONTROL Type d’exécution]
   * [!UICONTROL Période &#x200B;]
   * [!UICONTROL État de désactivation]
   * [!UICONTROL &#x200B; Message d’erreur &#x200B;]

   Pour la plupart des filtres, vous pouvez choisir de ne faire correspondre que les valeurs sélectionnées ou tout le reste, à l’exception de celles-ci.

1. Cliquez sur une exécution pour afficher plus de détails sur son erreur.
1. Pour réactiver un ou plusieurs scénarios qui ont été automatiquement désactivés après des échecs répétés, sélectionnez les exécutions, puis cliquez sur **Activer**.

   <!-- BECKY CHECK ME: confirm this button's exact label against the live UI. The Slack feature request calls it "Activate," but a related community post describes the same action as "Reactivate." -->

   Avant de réactiver un scénario, recherchez la cause de ses échecs, tels que des informations d’identification expirées ou un problème de connecteur, afin que le scénario n’échoue pas immédiatement à nouveau.
