---
content-type: reference
title: 'Configuration et gestion des organisations et des équipes : index des articles'
description: Cette section contient des articles relatifs à la configuration et à la gestion des organisations et des équipes dans Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: aa570f28-7387-47c5-9968-e3554921b0f5
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 67%

---

# Supprimer des utilisateurs et utilisatrices via [!DNL Adobe Admin Console]

Vous pouvez supprimer une personne d’[!DNL Adobe Workfront Fusion] uniquement, en laissant l’accès à tout autre profil de produit [!DNL Adobe], ou vous pouvez la supprimer entièrement d’[!DNL Adobe Admin Console].

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] paquet</td> 
   <td> <p>Tous</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licence</td> 
   <td> <p>Nouveau : [!UICONTROL Standard]</p><p>Ou</p><p>En cours : [!UICONTROL Work] ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licence**</td> 
   <td>
   <p>Actuelle : aucune exigence de licence [!DNL Workfront Fusion] requise.</p>
   <p>Ou</p>
   <p>Héritée : n’importe laquelle. </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Nouveau :</p> <ul><li>[!UICONTROL Select] ou [!UICONTROL Prime] plan de [!DNL Workfront] : votre entreprise doit acheter des [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] plan : [!DNL Workfront Fusion] est inclus.</li></ul>
   <p>Ou</p>
   <p>Actuel : votre entreprise doit acheter [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurations du niveau d’accès*</td> 
   <td> 
     <p>Vous devez être un administrateur [!DNL Adobe Admin Console] pour votre organisation.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Supprimer un utilisateur de [!DNL Adobe Workfront Fusion] uniquement

Vous pouvez supprimer un utilisateur de Workfront Fusion tout en conservant ses autres autorisations de produit d’Adobe.

Pour obtenir des instructions, reportez-vous à « Supprimer des utilisateurs et des groupes d’utilisateurs d’un produit » dans l’article [Gestion des produits sur Admin Console](https://helpx.adobe.com/fr/enterprise/using/manage-products.html).

## Désactiver un utilisateur dans tous les produits du [!DNL Adobe Admin Console]

Pour supprimer un utilisateur, vous devez le désactiver à l’aide du [!DNL Adobe Admin Console].

Une personne est désactivée d’[!DNL Adobe Admin Console] lorsque l’une des conditions suivantes s’applique :

* La personne est déplacée d’un produit ou d’un profil de produit et n’est affectée à aucun autre produit ou profil de produit.
* La personne est supprimée d’un groupe lié à un profil de produit et n’est incluse dans aucun autre groupe lié à un profil de produit.
* La personne est supprimée d’un profil de produit et n’est affectée à aucun autre profil de produit.
* La personne est supprimée ou désactivée dans l’organisation qui inclut Workfront Fusion.

  Pour obtenir des instructions, consultez la section « Supprimer des utilisateurs et des utilisatrices » dans [Gérer les utilisateurs et les utilisatrices individuellement](https://helpx.adobe.com/fr/enterprise/using/manage-users-individually.html).

Dans [!DNL Workfront Fusion], la désactivation affecte l’utilisateur ou l’utilisatrice de l’une des manières suivantes :

* Si la personne se trouve dans une seule organisation, elle est désactivée.
* Si la personne se trouve dans plusieurs organisations, elle est supprimée de l’organisation dans laquelle elle a été modifiée dans [!DNL Adobe Admin Console].
* Tenez compte des points suivants lors de la suppression d’un utilisateur.

### Considérations relatives à la suppression d’un utilisateur ou d’une utilisatrice dans Workfront Fusion

Tenez compte des points suivants lors de la suppression d’un utilisateur.

* Lorsqu’un utilisateur est supprimé, ses connexions, clés et Webhooks sont supprimés.
* Tous les scénarios appartenant à l’utilisateur ou à l’utilisatrice sont transférés à la personne propriétaire de l’organisation. Les connexions dans ces scénarios doivent être mises à jour, car les connexions appartenant à l’utilisateur ou à l’utilisatrice ne sont plus valides.
* Si le profil utilisateur supprimé possède des applications ou des modèles publics, les applications ou les modèles publics sont transférés à la personne propriétaire de l’organisation. S’il n’existe pas de personne propriétaire de l’organisation, les applications ou les modèles publics sont transférés à une autre personne.
