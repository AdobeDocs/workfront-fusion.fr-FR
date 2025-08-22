---
title: Choisir l’emplacement de démarrage d’un module déclencheur
description: Certains modules déclencheur vous permettent de sélectionner le premier lot à partir duquel vous souhaitez que la récupération des lots démarre.
author: Becky
feature: Workfront Fusion
exl-id: 83628fa5-82e2-4f67-bfed-70a4c3c19f7f
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 50%

---

# Choisir l’emplacement de démarrage d’un module déclencheur

Certains modules déclencheur vous permettent de sélectionner le premier lot à partir duquel vous souhaitez que la récupération des lots démarre.

Vous pouvez également indiquer si vous souhaitez récupérer tous les lots ou uniquement les lots à partir d’une date spécifique.

Pour plus d’informations sur les modules de déclenchement, consultez la section [Modules de déclenchement](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) dans l’article Présentation des modules.

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
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Choisir l’emplacement de démarrage d’un module déclencheur

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez choisir l’emplacement de départ du déclencheur.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Configurez et enregistrez un module de déclenchement.

   Ou

   Cliquez avec le bouton droit de la souris sur l’icône du module de déclenchement, puis sélectionnez **Choisir par où commencer**.

   ![Choisir par où commencer](assets/choose-where-to-start.png)

1. Sélectionnez une option dans la zone **[!UICONTROL Choisir l’emplacement de démarrage]** qui s’affiche.

   Les options affichées dépendent des possibilités d’un service donné. Elles peuvent inclure les éléments suivants :

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody>
    <tr>
    <td>[!UICONTROL From now on] (par défaut)</td>
    <td>Récupère tous les lots ajoutés ou mis à jour (en fonction des paramètres) une fois cette option sélectionnée</td>
    </tr>
     <tr>
    <td>[!UICONTROL Since specific date]</td>
    <td>Récupère tous les lots ajoutés ou mis à jour (en fonction des paramètres) après une date et une heure spécifiées</td>
      </tr>
      <tr>
    <td>[!UICONTROL All]</td>
    <td>Récupère tous les lots disponibles</td>
     </tr>
      <tr>
    <td>[!UICONTROL Choisir manuellement]</td>
    <td>Permet de sélectionner le premier lot à partir duquel la récupération des lots doit démarrer.</td>
     </tr>
     </tbody>
   </table>
