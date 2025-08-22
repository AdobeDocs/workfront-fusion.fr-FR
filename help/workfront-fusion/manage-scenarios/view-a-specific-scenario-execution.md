---
title: Affichage de l’exécution d’un scénario spécifique
description: Vous pouvez afficher les détails d’une exécution de scénario spécifique, y compris le filtrage et la recherche d’événements de scénario.
author: Becky
feature: Workfront Fusion
exl-id: 34dd9836-9a1b-4ce2-b24e-ae769888a52a
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 13%

---

# Affichage de l’exécution d’un scénario spécifique

Vous pouvez afficher les détails d’une exécution de scénario spécifique, y compris le filtrage et la recherche d’événements de scénario.

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tous</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licence Adobe Workfront</td> 
   <td> <p>Nouveau : Standard</p><p>Ou</p><p>En cours : Travail ou version ultérieure</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licence Adobe Workfront Fusion **</td> 
   <td>
   <p>Aucune exigence de licence Workfront Fusion</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Nouveau :</p> <ul><li>Sélectionnez ou le package Prime Workfront : votre entreprise doit acheter Adobe Workfront Fusion.</li><li>Package Ultimate Workfront : Workfront Fusion est inclus.</li></ul>
   <p>Ou</p>
   <p>Actuel : votre entreprise doit acheter Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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
