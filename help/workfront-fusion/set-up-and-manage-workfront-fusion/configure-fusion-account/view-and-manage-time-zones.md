---
title: Afficher et gérer les fuseaux horaires
description: Découvrez comment afficher et gérer les paramètres de fuseau horaire dans Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 9910d9b4-5a7a-4f4a-9e66-8600d3b6c785
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 39c34b17e766678e187837e07c90b67f365a4f1d
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 17%
---
# Afficher et gérer les fuseaux horaires

Adobe Workfront Fusion comprend des commandes pour les fuseaux horaires au niveau de l’organisation et au niveau de l’utilisateur.

* Fuseaux horaires de l’organisation : les scénarios utilisent les fuseaux horaires de l’organisation pour déterminer le moment où un événement planifié se produit.

* Fuseaux horaires de l’utilisateur : les fuseaux horaires de l’utilisateur déterminent l’heure affichée à un utilisateur.

>[!BEGINSHADEBOX]

Exemple :

Une organisation est basée à New York et l&#39;heure de l&#39;organisation est définie sur UTC-5 (Amérique/New York). Le scénario A appartient à cette organisation et doit s’exécuter à 9 h 00 tous les jours. Le scénario se déroule à 9 h dans le fuseau horaire de New York.

Un utilisateur de cette organisation vit à Los Angeles et a défini son fuseau horaire sur UTC-8 (Amérique/Los Angeles). Lorsque l’utilisateur consulte l’historique d’exécution du scénario A, il constate que le scénario s’est exécuté à 6 h 00. Même si le scénario s’est déroulé en fonction de l’heure à New York, l’utilisateur voit l’heure convertie dans son propre fuseau horaire.

>[!ENDSHADEBOX]



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
  <tr> 
   <td role="rowheader">Niveau d’accès</td> 
   <td> Vous devez être propriétaire ou administrateur d’une organisation pour modifier le fuseau horaire de cette organisation. </td>
   </tr>
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation Workfront](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Afficher et gérer le fuseau horaire de l’utilisateur

1. Dans Fusion, cliquez sur l’icône de votre profil Adobe en haut à droite de l’écran.
1. Dans le menu qui s’ouvre, sélectionnez **Profil Fusion**.
1. Sélectionnez l’onglet **Options de fuseau horaire**. Les onglets sont situés directement sous votre nom.
La liste Options de fuseau horaire s’affiche.
1. Dans la zone Web de la liste Options de fuseau horaire, recherchez votre nom.

   Le paramètre de fuseau horaire actuel de l’utilisateur s’affiche à droite de votre nom.
1. Pour modifier le fuseau horaire, cliquez sur Modifier ![Modifier le fuseau horaire](assets/edit-timezone-icon.png) en regard du fuseau horaire.
1. Dans la fenêtre Modifier les détails , dans le champ **Fuseau horaire**, sélectionnez le fuseau horaire que vous souhaitez définir.
1. Cliquer sur **Enregistrer**.


## Afficher et gérer le fuseau horaire de votre entreprise

>[!NOTE]
>
>Vous devez être propriétaire ou administrateur d’une organisation pour modifier le fuseau horaire de cette organisation.

1. Dans Fusion, cliquez sur l’icône de votre profil Adobe en haut à droite de l’écran.
1. Dans le menu qui s’ouvre, sélectionnez **Profil Fusion**.
1. Sélectionnez l’onglet **Options de fuseau horaire**. Les onglets sont situés directement sous votre nom.
La liste Options de fuseau horaire s’affiche.
1. Dans la zone Scénarios de la liste Options de fuseau horaire, localisez l’organisation pour laquelle vous souhaitez afficher ou gérer le fuseau horaire.

   Le paramètre de fuseau horaire actuel de l’organisation s’affiche à droite du nom de l’organisation.
1. Pour modifier le fuseau horaire, cliquez sur Modifier ![Modifier le fuseau horaire](assets/edit-timezone-icon.png) en regard du fuseau horaire.
1. Dans la fenêtre Modifier les détails , dans le champ **Fuseau horaire**, sélectionnez le fuseau horaire que vous souhaitez définir pour votre organisation.
1. Cliquer sur **Enregistrer**.


