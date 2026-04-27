---
content-type: reference
title: 'Set up and managing organizations and teams: article index'
description: This section contains articles related to setting up and managing organizations and teams in Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: aa570f28-7387-47c5-9968-e3554921b0f5
source-git-commit: 6762806f17a0fc55531b647a84901b8ca572a997
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 67%

---

# Supprimer des utilisateurs et utilisatrices via [!DNL Adobe Admin Console]

You can remove a user from Adobe Workfront Fusion only, leaving access to any other [!DNL Adobe] product profiles, or you can remove the user from the [!DNL Adobe Admin Console] entirely.

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
     <p>You must be an Adobe Admin Console administrator for your organization.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation Workfront](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Remove a user from Adobe Workfront Fusion only

You can remove a user from Workfront Fusion while leaving their other Adobe product permissions intact.

For instructions, see &quot;Remove users and user groups from a product&quot; in the article [Manage products on Admin Console](https://helpx.adobe.com/fr/enterprise/using/manage-products.html).

## Deactivate a user in all products in the [!DNL Adobe Admin Console]

To delete a user, you must deactivate the user through the [!DNL Adobe Admin Console].

Une personne est désactivée d’[!DNL Adobe Admin Console] lorsque l’une des conditions suivantes s’applique :

* La personne est déplacée d’un produit ou d’un profil de produit et n’est affectée à aucun autre produit ou profil de produit.
* La personne est supprimée d’un groupe lié à un profil de produit et n’est incluse dans aucun autre groupe lié à un profil de produit.
* La personne est supprimée d’un profil de produit et n’est affectée à aucun autre profil de produit.
* La personne est supprimée ou désactivée dans l’organisation qui inclut Workfront Fusion.

  Pour obtenir des instructions, consultez la section « Supprimer des utilisateurs et des utilisatrices » dans [Gérer les utilisateurs et les utilisatrices individuellement](https://helpx.adobe.com/fr/enterprise/using/manage-users-individually.html).

In Workfront Fusion, the deactivation affects the user in one of the following ways:

* Si la personne se trouve dans une seule organisation, elle est désactivée.
* Si la personne se trouve dans plusieurs organisations, elle est supprimée de l’organisation dans laquelle elle a été modifiée dans [!DNL Adobe Admin Console].

### Considérations relatives à la suppression d’un utilisateur ou d’une utilisatrice dans Workfront Fusion

Consider the following when deleting a user.

* When a user is deleted, the user&#39;s connections, keys, and webhooks are removed.
* Tous les scénarios appartenant à l’utilisateur ou à l’utilisatrice sont transférés à la personne propriétaire de l’organisation. Les connexions dans ces scénarios doivent être mises à jour, car les connexions appartenant à l’utilisateur ou à l’utilisatrice ne sont plus valides.
* Si le profil utilisateur supprimé possède des applications ou des modèles publics, les applications ou les modèles publics sont transférés à la personne propriétaire de l’organisation. S’il n’existe pas de personne propriétaire de l’organisation, les applications ou les modèles publics sont transférés à une autre personne.
