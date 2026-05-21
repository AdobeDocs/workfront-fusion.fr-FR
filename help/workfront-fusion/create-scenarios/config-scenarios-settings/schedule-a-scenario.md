---
content-type: reference
title: Planifier un scénario
description: Par défaut, un scénario s’exécute toutes les 15 minutes. Vous pouvez modifier ce paramètre en définissant le moment et la fréquence d’exécution d’un scénario activé. Vous pouvez planifier les scénarios Fusion pour qu’ils s’exécutent toutes les 5 minutes.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 9b74af0d-e7ff-4bf5-974e-0651d0d51f71
TQID: https://experienceleague.adobe.com/jWWR3vbD-ShhjTws5p3Gx24C2YfL-qYKHXyssnR-dFM
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 575
ht-degree: 97%

---

# Planifier un scénario

Par défaut, un scénario s’exécute toutes les 15 minutes. Vous pouvez modifier ce paramètre en définissant le moment et la fréquence d’exécution d’un scénario activé. Vous pouvez planifier les scénarios Fusion pour qu’ils s’exécutent toutes les 5 minutes.

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

## Planifier un scénario

1. Cliquez sur l’onglet **Scénario** dans le panneau de gauche.
1. Sélectionnez le scénario que vous souhaitez planifier.
1. Dans le coin supérieur droit de la page Détails du scénario, cliquez sur **[!UICONTROL Options]** > **[!UICONTROL Planification]**

   Ou

   Cliquez sur l’icône **[!UICONTROL Planification]** (horloge) sur le module de déclenchement du scénario.

1. Renseignez les champs suivants :

   <table style="table-layout:auto">   
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Run scenario]</td> 
      <td> <p>Sélectionnez la fréquence, puis l’intervalle d’exécution du scénario.</p> 
       <ul> 
        <li> <p><strong>[!UICONTROL At regular intervals]</strong> </p> <p>Saisissez le nombre de minutes entre les exécutions. La valeur par défaut est de 15 minutes.</p> </li> 
        <li> <p><strong>[!UICONTROL Once]</strong> </p> <p>Saisissez la date et l’heure d’exécution du scénario. Utilisez le format <code>MM/DD/YYYY h:mm A</code>. Exemple : <code>06/25/2019 11:00 PM</code>.</p> </li> 
        <li> <p><strong>[!UICONTROL Every day]</strong> </p> <p>Saisissez l’heure à laquelle vous souhaitez que le scénario s’exécute. Utilisez le format <code>h:mm A</code>. Exemple : <code>11:00 PM</code>.</p> </li> 
        <li> <p><strong>[!UICONTROL Days of the week]</strong> </p> <p>Jours : sélectionnez les jours de la semaine pendant lesquels le scénario doit s’exécuter. Vous pouvez sélectionner un ou plusieurs jours.</p> <p>Heure : saisissez l’heure à laquelle le scénario doit s’exécuter les jours sélectionnés. Utilisez le format <code>h:mm A</code>. Exemple : <code>11:00 PM</code></p> </li> 
        <li> <p><strong>[!UICONTROL Days of the month]</strong> </p> <p>Jours : sélectionnez les jours du mois pendant lesquels le scénario doit s’exécuter. Vous pouvez sélectionner un ou plusieurs jours.</p> <p>Heure : saisissez l’heure à laquelle le scénario doit s’exécuter les jours sélectionnés. Utilisez le format <code>h:mm A</code>. Exemple : <code>11:00 PM</code></p> </li> 
        <li> <p><strong>[!UICONTROL Specified dates]</strong> </p> <p>Mois : sélectionnez les mois pendant lesquels le scénario doit s’exécuter. Vous pouvez sélectionner un ou plusieurs mois.</p> <p>Jours : sélectionnez les jours du mois pendant lesquels le scénario doit s’exécuter. Vous pouvez sélectionner un ou plusieurs jours.</p> <p>Heure : saisissez l’heure à laquelle le scénario doit s’exécuter les jours sélectionnés. Utilisez le format <code>h:mm A</code>. Exemple : <code>11:00 PM</code></p> </li> 
       </ul> <p>Remarque : pour qu’un scénario s’exécute à une date, celle-ci doit exister. Par exemple, un scénario planifié uniquement pour le 31 du mois ne s’exécutera pas en février, avril, juin, septembre ou novembre, car ces mois n’ont pas de 31e jour.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Advanced scheduling]</td> 
      <td>Vous pouvez définir des intervalles de temps spécifiques pendant lesquels votre scénario doit s’exécuter. Vous pouvez spécifier des intervalles en heures de la journée, en jours de semaine ou en mois. Pour chaque intervalle, cliquez sur <strong>[!UICONTROL Add]</strong> et renseignez les champs comme décrit dans le champ [!UICONTROL Run scenario].</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Start]</td> 
      <td>Saisissez la date et l’heure après lesquelles vous souhaitez que le scénario s’exécute. Utilisez le format <code>MM/DD/YYYY h:mm A</code>. Exemple : <code>06/25/2019 11:00 PM</code></td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL End]</td> 
      <td>Saisissez la date et l’heure auxquelles vous souhaitez que le scénario s’exécute. Utilisez le format <code>MM/DD/YYYY h:mm A</code>. Exemple : <code>06/25/2019 11:00 PM</code></td> 
     </tr> 
    </tbody> 
   </table>

1. Cliquez sur **[!UICONTROL OK]** pour enregistrer les paramètres de planning et revenir au scénario.
