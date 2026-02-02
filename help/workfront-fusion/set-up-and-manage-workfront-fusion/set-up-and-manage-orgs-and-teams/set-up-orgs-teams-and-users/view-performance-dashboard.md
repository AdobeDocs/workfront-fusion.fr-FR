---
title: Afficher le tableau de bord des performances d’une organisation
description: Les administrateurs et administratrices de Fusion peuvent afficher un tableau de bord qui affiche les mesures d’exécution pour une organisation.
author: Becky
feature: Workfront Fusion
hide: true
hidefromtoc: true
source-git-commit: b4c9cd075cc2bb7aa3d5c568bb91fb8ce5c6f31e
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 9%

---

# Afficher le tableau de bord des performances d’une organisation

Le tableau de bord des performances de Fusion vous permet de voir rapidement quels scénarios sont les plus exécutés, où les retards se produisent et à quel point vos pools de salariés fonctionnent efficacement. Vous bénéficiez ainsi d’une visibilité en temps réel sur les volumes d’exécution, la profondeur de file d’attente, l’utilisation du pool et les performances au niveau du scénario.

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

## Composants du tableau de bord des performances

>[!NOTE]
>
>Les mesures sont affichées par pool de traitement. Pour afficher un autre pool de traitement, cliquez sur le champ Pool près du coin supérieur gauche du tableau de bord, puis sélectionnez le pool pour lequel vous souhaitez afficher les mesures.

<!--

>[!NOTE]
>
>Organizations can request provisioning for one additional worker pool (for a total of 2).

-->

Dans le tableau de bord des performances de Fusion , vous pouvez voir les mesures suivantes.

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

## Affichage du tableau de bord des performances de Fusion

1. Dans Fusion, cliquez sur Performances dans le volet de navigation de gauche.

   Le tableau de bord s’ouvre.

1. Pour afficher les données à un moment donné, passez la souris sur un tableau de bord et placez le curseur sur le moment voulu pour l’afficher.

   Une ligne s’affiche au-dessus de ce moment dans tous les graphiques, et une fenêtre affichant les données de ce moment s’affiche sur chaque graphique.
1. Pour afficher les données d’un scénario spécifique dans le graphique Exécutions par scénario ou Durée des exécutions, cliquez sur une barre de couleur du scénario pour lequel vous souhaitez afficher les données. Pour revenir à la vue affichant tous les scénarios, cliquez de nouveau sur le graphique.
1. Pour accéder à un scénario spécifique affiché dans le graphique Exécutions par scénario ou le graphique Durée des exécutions, faites un clic droit sur une barre de couleur du scénario et sélectionnez **Ouvrir le scénario dans un nouvel onglet**.
1. Pour développer un graphique, cliquez sur l’icône **Développer** ![icône Développer](assets/expand-icon.png) dans le coin supérieur droit de ce graphique.
1. Pour modifier la période du tableau de bord, sélectionnez le champ Période dans le coin supérieur droit du tableau de bord, puis sélectionnez une nouvelle période. La période disponible la plus longue est de 24 heures et la plus courte est de 15 minutes.
1. Pour actualiser les graphiques, cliquez sur l’icône Actualiser située en haut à droite du tableau de bord.
1. Pour afficher un autre pool de traitement, cliquez sur le champ Pool près du coin supérieur gauche du tableau de bord, puis sélectionnez le pool à afficher.



