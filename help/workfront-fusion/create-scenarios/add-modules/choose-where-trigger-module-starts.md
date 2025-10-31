---
title: Choisir l’emplacement de démarrage d’un module déclencheur
description: Certains modules déclencheur vous permettent de sélectionner le premier lot à partir duquel vous souhaitez que la récupération des lots démarre.
author: Becky
feature: Workfront Fusion
exl-id: 83628fa5-82e2-4f67-bfed-70a4c3c19f7f
source-git-commit: c83070a7c2d1d048000a4eace4aaede73c7ec49d
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 45%

---

# Choisir l’emplacement de démarrage d’un module déclencheur

Certains modules déclencheur vous permettent de sélectionner le premier lot à partir duquel vous souhaitez que la récupération des lots démarre.

Vous pouvez également indiquer si vous souhaitez récupérer tous les lots ou uniquement les lots à partir d’une date spécifique.

Pour plus d’informations sur les modules de déclenchement, consultez la section [Modules de déclenchement](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) dans l’article Présentation des modules.

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

+++## Choisissez où commence un module de déclenchement

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
