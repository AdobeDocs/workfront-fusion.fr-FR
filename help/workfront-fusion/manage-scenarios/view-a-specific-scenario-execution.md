---
title: Affichage de l’exécution d’un scénario spécifique
description: Vous pouvez afficher les détails d’une exécution de scénario spécifique, y compris le filtrage et la recherche d’événements de scénario.
author: Becky
feature: Workfront Fusion
exl-id: 34dd9836-9a1b-4ce2-b24e-ae769888a52a
source-git-commit: 42be02d6a59a5d7b8faccdcfe40e8b967153c6eb
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 10%

---

# Affichage de l’exécution d’un scénario spécifique

Vous pouvez afficher les détails d’une exécution de scénario spécifique, y compris le filtrage et la recherche d’événements de scénario.

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

## Afficher une exécution spécifique

Vous pouvez afficher une exécution à partir de l’historique des scénarios du scénario.


1. Cliquez sur l’onglet **[!UICONTROL Scénario]** dans le panneau de gauche, puis sur le scénario.

   Ou

   Si vous travaillez sur le scénario dans l’éditeur de scénarios, cliquez sur la flèche de gauche ![flèche de modification de sortie](assets/exit-editing-arrow.png) près du coin supérieur gauche de la fenêtre.

1. Cliquez sur **Historique** près du nom du scénario.
   ![onglet historique](assets/history-tab.png)


1. Recherchez l’exécution à afficher, puis cliquez sur **Détails** à l’extrémité droite de la ligne correspondant à cette exécution. Le lien [!UICONTROL Détails] n’est visible que si les détails de l’exécution sont disponibles.

   Le diagramme de scénario s’ouvre avec le panneau des détails de l’exécution ouvert à droite.

   Les modules qui ont généré la sortie pour cette exécution sont marqués avec des titres verts.

   Les modules qui n’ont pas été exécutés sont grisés.

1. Pour afficher la sortie d’un module, cliquez sur la bulle des détails de sortie près du module. Le nombre dans la bulle représente le nombre de lots générés par le module.

   ![Bulle de sortie près d&#39;un module](assets/output-bubble.png)

1. Pour afficher les lots qui ont passé par un filtre, cliquez sur le filtre. Le nombre près du filtre représente le nombre de lots qui ont passé par le filtre.
1. Pour rechercher un module ou un événement spécifique dans le panneau d’exécution, saisissez le terme de recherche dans la zone **Rechercher des événements d’exécution**. Les résultats s’affichent au fur et à mesure que vous tapez.
1. Pour limiter les résultats de recherche du panneau d’exécution par statut, tel que Succès ou Avertissement, cliquez sur le menu déroulant **Filtre de statut** et sélectionnez le statut.




>[!NOTE]
>
>Pour créer un lien vers un module spécifique, ajoutez des `?moduleId=<module-id>` à l’URL lors de l’affichage des pages suivantes :
>
>* Page de modification du scénario (l’URL se termine par `/edit`)
>* Exécution d’un scénario spécifique (l’URL se termine par `/logs/<log-id>`)
>
>`<module-id>` fait référence au nombre en regard du libellé du module lors de l’affichage du scénario.
>
>Cela peut s’avérer utile lors du débogage de scénarios ou de la copie de la configuration du module.
