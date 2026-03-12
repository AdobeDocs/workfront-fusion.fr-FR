---
title: Gestion des utilisateurs d’Adobe Workfront Fusion dans votre entreprise
description: Gestion des utilisateurs d’Adobe Workfront Fusion dans votre entreprise
author: Becky
feature: Workfront Fusion
exl-id: 32c221fa-856b-4921-9fa6-5e60f2aa08cd
source-git-commit: 88d7a92a4b117d10ab114e32ab5e61f03bc5a846
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 35%

---

# Afficher ou modifier des rôles d’utilisateur ou d’utilisatrice

Les administrateurs d’Adobe Workfront Fusion peuvent gérer les rôles utilisateur dans Workfront Fusion.


>[!NOTE]
>
>Si votre organisation est en train de passer au Adobe Admin Console, vous ne pouvez pas gérer les utilisateurs dans Workfront (ajout ou suppression d’utilisateurs). Vous pouvez effectuer ces actions dans le Adobe Admin Console une fois la migration terminée.

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
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurations des niveaux d’accès</td> 
   <td> 
     <p>Vous devez être administrateur ou administratrice Workfront Fusion pour votre entreprise.</p>
     <p>Vous devez être un administrateur Workfront Fusion pour votre équipe.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation Workfront](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Afficher ou modifier les rôles utilisateur d’une organisation

Les administrateurs d’Adobe Workfront Fusion peuvent afficher et mettre à jour les rôles utilisateur d’une organisation.

1. Connecté en tant qu’administrateur Workfront Fusion, sélectionnez **[!UICONTROL Tous les utilisateurs]** dans le volet de navigation de gauche.
1. Cliquez sur **[!UICONTROL Détails]** dans la ligne de l’utilisateur ou de l’utilisatrice que vous souhaitez afficher.
1. (Facultatif) Pour mettre à jour le rôle de l’utilisateur dans une organisation, cliquez sur la liste déroulante de la colonne **[!DNL Role]** de la ligne de l’organisation dans laquelle vous souhaitez modifier le rôle de l’utilisateur, puis sélectionnez le nouveau rôle.

<!--

### Considerations when adding or changing organization Owners

Your organization can have more than one Owner. 

When assigning a user to or from an Owner role, consider the following. 

* Only an Owner can assign the Owner role, or assign another role to a current Owner.
* Only Admins can be upgraded to Owner.
* If there is only one Owner, that Owner role cannot be changed or removed.
* If there is only one Owner, that Owner cannot be deleted if there are other users in the organization.
* When an Admin is assigned an Owner role, they automatically become Admin in all teams within the org.
* When an Owner is assigned to another role, that user automatically becomes a Team Member in all teams.
* When a new team is created, all Owners are automatically assigned as Team Admins.

-->

## Afficher ou modifier les rôles utilisateur d&#39;une équipe

Les administrateurs Adobe Workfront Fusion et les administrateurs d’équipe peuvent afficher et mettre à jour les rôles utilisateur.

1. Connecté en tant qu’administrateur Workfront Fusion, sélectionnez **[!UICONTROL Tous les utilisateurs]** dans le volet de navigation de gauche.
1. Cliquez sur **[!UICONTROL Détails]** dans la ligne de l’utilisateur ou de l’utilisatrice que vous souhaitez afficher.
1. Cliquez sur l’icône Équipes dans la colonne **[!DNL Role]** de la ligne de l’organisation contenant l’équipe dans laquelle vous souhaitez afficher ou modifier le rôle de l’utilisateur.
1. (Facultatif) Pour mettre à jour le rôle de l’utilisateur dans une équipe, cliquez sur la liste déroulante de la colonne **[!DNL Role]** dans la ligne de l’équipe où vous souhaitez modifier le rôle de l’utilisateur, puis sélectionnez le nouveau rôle.
