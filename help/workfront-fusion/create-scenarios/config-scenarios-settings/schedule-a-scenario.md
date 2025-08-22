---
content-type: reference
title: Planifier un scénario
description: Par défaut, un scénario s’exécute toutes les 15 minutes. Vous pouvez modifier ce paramètre en définissant le moment et la fréquence d’exécution d’un scénario activé. Vous pouvez planifier les scénarios Fusion pour qu’ils s’exécutent toutes les 5 minutes.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 9b74af0d-e7ff-4bf5-974e-0651d0d51f71
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 84%

---

# Planifier un scénario

Par défaut, un scénario s’exécute toutes les 15 minutes. Vous pouvez modifier ce paramètre en définissant le moment et la fréquence d’exécution d’un scénario activé. Vous pouvez planifier les scénarios Fusion pour qu’ils s’exécutent toutes les 5 minutes.

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
   <td> <p>Nouveau : Standard</p><p>Ou</p><p>Actuelle : [!UICONTROL Work] ou niveau supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licence Adobe Workfront Fusion **</td> 
   <td>
   <p>Actuel : aucune exigence de licence Workfront Fusion.</p>
   <p>Ou</p>
   <p>Héritée : n’importe laquelle. </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Nouveau :</p> <ul><li>Plan Workfront [!UICONTROL Select] ou [!UICONTROL Prime] : votre entreprise doit acheter Adobe Workfront Fusion.</li><li>Plan Workfront [!UICONTROL Ultimate] : Workfront Fusion est inclus.</li></ul>
   <p>Ou</p>
   <p>Actuel : votre entreprise doit acheter Adobe Workfront Fusion.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurations du niveau d’accès*</td> 
   <td> 
     <p>Vous devez être administrateur ou administratrice Workfront Fusion pour votre entreprise.</p>
     <p>Vous devez être un administrateur Workfront Fusion pour votre équipe.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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
