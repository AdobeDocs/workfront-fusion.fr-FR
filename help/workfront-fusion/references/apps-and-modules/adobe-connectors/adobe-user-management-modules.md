---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: apps-and-their-modules
title: Adobe des modules User Management
description: Dans un  [!DNL Adobe Workfront Fusion]  scénario, vous pouvez automatiser les workflows qui gèrent les utilisateurs dans votre compte Adobe.
author: Becky
feature: Workfront Fusion
exl-id: e8fe8ec4-4b00-4c9a-81a5-acb2039b153b
source-git-commit: 640fec2de63ad59ba89fae5373f85b8147d8dac0
workflow-type: tm+mt
source-wordcount: '2323'
ht-degree: 14%

---

# Adobe des modules User Management

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui gèrent les utilisateurs dans votre compte Adobe.

Si vous avez besoin d’instructions pour créer un scénario, consultez les articles sous [Créer un scénario : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] formule*</td>
  <td> <p>[!UICONTROL Pro] ou une version ultérieure</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licence*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licence**</td> 
   <td>
   <p>Exigences de licence actuelles : aucune exigence de licence [!DNL Workfront Fusion] requise.</p>
   <p>Ou</p>
   <p>Ancienne exigence de licence : [!UICONTROL [!DNL Workfront Fusion] pour l’automatisation et l’intégration du travail], [!UICONTROL [!DNL Workfront Fusion] pour l’automatisation du travail]</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Exigences actuelles relatives aux produits : si vous disposez du plan de [!DNL Adobe Workfront] [!UICONTROL Select] ou [!UICONTROL Prime], votre entreprise doit acheter des [!DNL Adobe Workfront Fusion] et [!DNL Adobe Workfront] utiliser les fonctionnalités décrites dans cet article. [!DNL Workfront Fusion] est inclus dans le plan de [!DNL Workfront] [!UICONTROL Ultimate].</p>
   <p>Ou</p>
   <p>Exigences liées aux produits hérités : votre entreprise doit acheter [!DNL Adobe Workfront Fusion] ainsi qu’[!DNL Adobe Workfront] pour utiliser la fonctionnalité décrite dans cet article.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Pour connaître la formule, le type de licence ou l’accès dont vous disposez, contactez votre équipe d’administration [!DNL Workfront].

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Création d’une connexion à Adobe User Management

Pour créer une connexion pour vos modules [!DNL Adobe User Management], procédez comme suit :

1. Cliquez sur **[!UICONTROL Add]** en regard de la zone Connexion .

1. Remplissez les champs suivants :

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Saisissez un nom pour cette connexion.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>Indiquez si vous vous connectez à un environnement de production ou hors production.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>Indiquez si vous vous connectez à un compte de service ou à un compte personnel.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Saisissez votre [!UICONTROL Client ID] de [!UICONTROL Adobe]. Pour plus d’informations, consultez la section [!UICONTROL Credentials] les détails du [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Saisissez votre [!UICONTROL Client Secret] de [!DNL Adobe]. Pour plus d’informations, consultez la section [!UICONTROL Credentials] les détails du [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL IMS Organization ID]</td>
        <td>Saisissez vos informations d’identification IMS [!DNL Adobe]. Identifiant unique d’une organisation. Il s’agit d’une chaîne de la forme A495E53@AdobeOrg où le préfixe devant le caractère @ est un nombre hexadécimal. Cette valeur figure dans le chemin d’URL de l’organisation dans l’Admin Console ou dans la console adobe.io pour votre intégration User Management.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Additional scopes]</td>
        <td>Pour chaque portée supplémentaire à ajouter, cliquez sur <b>Ajouter un élément</b> et saisissez la portée.</td>
        </tr>
      </tbody>
    </table>

1. Cliquez sur **[!UICONTROL Continue]** pour enregistrer la connexion et revenir au module .



## Adobe des modules User Management et de leurs champs

Lorsque vous configurez les modules de gestion des utilisateurs d’Adobe, Workfront Fusion affiche les champs répertoriés ci-dessous. D’autres champs de gestion des utilisateurs d’Adobe peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [Recherches](#searches)
* [Actions de l’utilisateur](#user-actions)
* [Actions du groupe d’utilisateurs](#user-group-actions)
* [Autre](#other)

### Recherches

* [Obtention des groupes d’utilisateurs et des profils de produits](#get-user-groups-and-product-profiles)
* [Obtenir des informations sur l’utilisateur](#get-user-information)
* [Obtention d’utilisateurs dans un groupe d’utilisateurs ou un profil de produits](#get-users-in-a-user-group-or-product-profile)
* [Obtenir les utilisateurs d’une organisation](#get-users-in-an-organization)

#### Obtention des groupes d’utilisateurs et des profils de produits

Ce module de recherche récupère une liste de tous les groupes d’utilisateurs et profils de produits de votre organisation, ainsi que des détails sur les groupes et les profils.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe User Management, voir <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Création d’une connexion à Adobe User Management</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nombre maximal de résultats renvoyés</td> 
   <td>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</td> 
  </tr> 
 </tbody> 
</table>

#### Obtenir des informations sur l’utilisateur

Ce module de recherche récupère les détails d’un utilisateur unique de l’organisation, identifié par son adresse e-mail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe User Management, voir <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Création d’une connexion à Adobe User Management</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adresse e-mail</td> 
   <td>Saisissez ou mappez l’adresse e-mail de l’utilisateur pour lequel vous souhaitez renvoyer des détails. Pour les utilisateurs Adobe ID, Enterprise et fédérés par e-mail, il doit s’agir de l’adresse e-mail complète, domaine compris. Dans tous les cas, le paramètre ne respecte pas la casse.</td> 
  </tr> 
 </tbody> 
</table>

#### Obtention d’utilisateurs dans un groupe d’utilisateurs ou un profil de produits

Ce module de recherche récupère une liste de tous les utilisateurs du groupe d’utilisateurs ou du profil de produit spécifié, ainsi que des détails sur les utilisateurs.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe User Management, voir <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Création d’une connexion à Adobe User Management</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom du groupe</td> 
   <td>Groupe d’utilisateurs, nom de profil de produit ou groupe d’administration. Pour un groupe d’administrateurs, le nom peut être l’un des groupes fixes <code>_org_admin</code>, <code>_deployment_admin</code> ou <code>_support_admin</code> ; ou un groupe d’administrateurs spécifique à un groupe. Ils sont identifiés par un préfixe sur le nom du groupe , tel que <code>_admin_groupName</code>, <code>_product_admin_productName</code> ou <code>_developer_groupName</code>. Si le groupe existe mais pas le groupe d’administrateurs, une liste vide est renvoyée.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Direct uniquement</td> 
   <td>Indiquez si le champ de groupes dans la structure d’utilisateur renvoyée contient uniquement les profils de produit dont cet utilisateur est un membre direct. Si la valeur est false, renvoie tous les groupes (groupes d’utilisateurs, profils de produits et groupes d’administrateurs) contenant l’utilisateur, qu’un droit pour un profil de produit particulier vienne directement (via l’affectation d’utilisateur) ou indirectement (via un groupe d’utilisateurs qui contient l’utilisateur affecté au profil de produit). Si la valeur est true, renvoie tous les groupes d’utilisateurs et groupes d’administrateurs contenant l’utilisateur, mais uniquement les profils de produit auxquels l’utilisateur a été explicitement attribué un droit. Un utilisateur peut être à la fois un membre direct et indirect d’un profil de produit.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Exclure les groupes</td> 
   <td>Indiquez si la réponse exclut le renvoi du tableau des groupes pour chaque utilisateur individuel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Statut</td> 
   <td>Cette option s’applique uniquement aux profils de produit. Sélectionnez Actif pour répertorier les utilisateurs qui ont été configurés pour le produit et qui disposent d’une licence active. Sélectionnez inactif pour répertorier les utilisateurs qui ont été ajoutés au profil de produit, mais qui ne disposent pas d’une licence active. Si rien n’est indiqué, le module renvoie tous les utilisateurs membres, quel que soit leur statut de droit.
</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nombre maximal de résultats renvoyés</td> 
   <td>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</td> 
  </tr> 
 </tbody> 
</table>

#### Obtenir les utilisateurs d’une organisation

Ce module de recherche renvoie tous les utilisateurs de l’organisation associés à la connexion.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe User Management, voir <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Création d’une connexion à Adobe User Management</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nombre maximal de résultats renvoyés</td> 
   <td>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</td> 
  </tr> 
 </tbody> 
</table>

### Actions de l’utilisateur

* [Ajout d’un utilisateur en tant que membre d’un groupe](#add-a-user-as-a-member-of-a-group)
* [Création d’un utilisateur](#create-a-user)
* [Supprimer un utilisateur des groupes](#remove-a-user-from-groups)
* [Mettre à jour un utilisateur](#update-a-user)

#### Ajout d’un utilisateur en tant que membre d’un groupe

Ce module d&#39;action ajoute un utilisateur en tant que membre du ou des groupes spécifiés. Ce module peut ajouter l’utilisateur à un maximum de quatre groupes.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe User Management, voir <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Création d’une connexion à Adobe User Management</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">l’utilisateur ou de l’utilisatrice</td> 
   <td>Saisissez ou mappez l’utilisateur que vous souhaitez ajouter aux groupes.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Domaine</td> 
   <td>Pour les Federated ID qui ne sont pas des adresses e-mail, saisissez le domaine auquel appartient l’utilisateur.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Groupes</td> 
   <td>Pour chaque groupe auquel vous souhaitez ajouter l’utilisateur, cliquez sur <b>Ajouter un élément</b> et saisissez ou mappez le groupe. Vous pouvez saisir jusqu’à quatre groupes, et devez en saisir au moins un.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Utilisation d’Adobe ID</td> 
   <td>Sélectionnez true pour vous assurer que l’ID utilisateur est interprété comme faisant référence à une Adobe ID existante même s’il existe une entreprise ou un Federated ID portant le même nom.</td> 
  </tr> 
 </tbody> 
</table>

#### Création d’un utilisateur

Ce module d’action crée un nouvel utilisateur dans l’organisation.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe User Management, voir <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Création d’une connexion à Adobe User Management</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type d’identifiant</td> 
   <td>Choisissez si vous souhaitez créer un utilisateur avec un Adobe ID, un Enterprise ID ou un Federated ID. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Si vous créez un utilisateur avec un Federated ID, sélectionnez le type de connexion.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">E-mail</td> 
   <td>Saisissez ou mappez l’adresse e-mail du nouvel utilisateur.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Domaine</td> 
   <td>Si vous créez un utilisateur avec un Federated ID et un identifiant basé sur un domaine, saisissez ou mappez le domaine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">l’utilisateur ou de l’utilisatrice</td> 
   <td>Si vous créez un utilisateur avec un Federated ID doté d'un nom de domaine, saisissez ou mappez l'utilisateur que le nouvel utilisateur représentera.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prénom</td> 
   <td>Saisissez ou mappez le prénom de l’utilisateur.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom</td> 
   <td>Saisissez ou mappez le nom de l’utilisateur.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Pays</td> 
   <td>Saisissez ou mappez le code pays ISO à deux caractères. Cette valeur ne peut pas être modifiée une fois l’utilisateur créé.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Option</td> 
   <td>Sélectionnez l’action à effectuer si l’utilisateur existe déjà dans l’organisation. Si aucune option n’est sélectionnée et que l’utilisateur existe déjà, le module renvoie une erreur.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Utilisation d’Adobe ID</td> 
   <td>Lorsque la valeur est true, l’ID utilisateur est interprété comme faisant référence à une Adobe ID existante même s’il existe une entreprise ou un Federated ID portant le même nom.</td> 
  </tr> 
 </tbody> 
</table>

#### Supprimer un utilisateur des groupes

Ce module d’action supprime l’appartenance d’un utilisateur des groupes spécifiés. Vous pouvez supprimer un utilisateur d’un maximum de quatre groupes à la fois.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe User Management, voir <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Création d’une connexion à Adobe User Management</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">l’utilisateur ou de l’utilisatrice</td> 
   <td>Saisissez ou mappez l’utilisateur que vous souhaitez supprimer des groupes.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Domaine</td> 
   <td>Pour les Federated ID qui ne sont pas des adresses e-mail, saisissez le domaine auquel appartient l’utilisateur.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Groupes</td> 
   <td>Pour chaque groupe dont vous souhaitez supprimer l’utilisateur, cliquez sur <b>Ajouter un élément</b> et saisissez ou mappez le groupe. Vous pouvez saisir jusqu’à quatre groupes, et devez en saisir au moins un.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Utilisation d’Adobe ID</td> 
   <td>Sélectionnez true pour vous assurer que l’ID utilisateur est interprété comme faisant référence à une Adobe ID existante même s’il existe une entreprise ou un Federated ID portant le même nom.</td> 
  </tr> 
 </tbody> 
</table>



#### Mettre à jour un utilisateur

Ce module d’action met à jour un utilisateur existant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe User Management, voir <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Création d’une connexion à Adobe User Management</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">l’utilisateur ou de l’utilisatrice</td> 
   <td>Saisissez ou mappez l’ID de l’utilisateur que vous souhaitez mettre à jour. Il s’agit de l’adresse e-mail de l’utilisateur, telle que <code>user@example.com</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Domaine</td> 
   <td>Si vous mettez à jour un utilisateur avec un Federated ID qui n’est pas une adresse e-mail, saisissez ou mappez le domaine auquel l’utilisateur appartient afin de l’identifier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">E-mail</td> 
   <td>Saisissez ou mappez la nouvelle adresse e-mail de l’utilisateur.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Prénom</td> 
   <td>Saisissez ou mappez le prénom de l’utilisateur.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom</td> 
   <td>Saisissez ou mappez le nom de l’utilisateur.</td> 
  </tr> 
 </tbody> 
</table>

### Actions du groupe d’utilisateurs

* [Ajouter des appartenances à un groupe d’utilisateurs](#add-memberships-for-a-user-group)
* [Création d’un groupe d’utilisateurs](#create-a-user-group)
* [Suppression d’un groupe d’utilisateurs](#delete-a-user-group)
* [Supprimer les appartenances à un groupe d’utilisateurs](#remove-memberships-for-a-user-group)
* [Mettre à jour un groupe d’utilisateurs](#update-a-user-group)

#### Ajouter des appartenances à un groupe d’utilisateurs

Ce module d’action ajoute des utilisateurs et des profils de produit à un groupe d’utilisateurs. Les utilisateurs ajoutés au groupe d’utilisateurs obtiennent le droit d’accès à tous les profils de produit du groupe d’utilisateurs. L’ajout d’un profil de produit donne des droits sur ce profil aux utilisateurs du groupe d’utilisateurs.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe User Management, voir <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Création d’une connexion à Adobe User Management</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom du groupe</td> 
   <td>Saisissez ou mappez le nom du groupe dont vous souhaitez supprimer les utilisateurs ou les profils.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Utilisateurs</td> 
   <td>Pour chaque utilisateur que vous souhaitez ajouter, cliquez sur <b>Ajouter un utilisateur</b> et saisissez son adresse e-mail.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Profils</td> 
   <td>Pour chaque profil que vous souhaitez ajouter au groupe, cliquez sur <b>Ajouter un utilisateur</b> et saisissez le nom du profil</td> 
  </tr> 
 </tbody> 
</table>

#### Création d’un groupe d’utilisateurs

Ce module d’action crée un groupe d’utilisateurs. Si un groupe portant le même nom existe déjà, le module peut le mettre à jour.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe User Management, voir <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Création d’une connexion à Adobe User Management</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom du groupe</td> 
   <td>Saisissez ou mappez un nom pour le nouveau groupe d’utilisateurs.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Description</td> 
   <td>Saisissez ou mappez une description pour le nouveau groupe d’utilisateurs.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Option</td> 
   <td>Sélectionnez l’action à effectuer si le groupe d’utilisateurs existe déjà dans l’organisation. Si aucune option n’est sélectionnée et que le groupe d’utilisateurs existe déjà, le module renvoie une erreur.</td> 
  </tr> 
 </tbody> 
</table>

#### Suppression d’un groupe d’utilisateurs

Ce module d’action supprime un groupe d’utilisateurs existant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe User Management, voir <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Création d’une connexion à Adobe User Management</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom du groupe</td> 
   <td>Saisissez ou mappez le nom du groupe que vous souhaitez supprimer.</td> 
  </tr> 
 </tbody> 
</table>

#### Supprimer les appartenances à un groupe d’utilisateurs

Ce module d’action supprime des utilisateurs ou des profils d’un groupe d’utilisateurs.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe User Management, voir <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Création d’une connexion à Adobe User Management</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom du groupe</td> 
   <td>Saisissez ou mappez le nom du groupe dont vous souhaitez supprimer les utilisateurs ou les profils.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Utilisateurs</td> 
   <td>Pour chaque utilisateur que vous souhaitez supprimer, cliquez sur <b>Ajouter un utilisateur</b> et saisissez son adresse e-mail.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Profils</td> 
   <td>Pour chaque profil à supprimer du groupe, cliquez sur <b>Ajouter un utilisateur</b> et saisissez le nom du profil</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Utilisation d’Adobe ID</td> 
   <td>Lorsque la valeur est true, l’ID utilisateur est interprété comme faisant référence à une Adobe ID existante même s’il existe une entreprise ou un Federated ID portant le même nom.</td> 
  </tr> 
 </tbody> 
</table>

#### Mettre à jour un groupe d’utilisateurs

Ce module d’action met à jour un groupe d’utilisateurs existant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe User Management, voir <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Création d’une connexion à Adobe User Management</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom de groupe d’origine</td> 
   <td>Saisissez ou mappez le nom actuel du groupe que vous souhaitez mettre à jour.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom du nouveau groupe</td> 
   <td>Saisissez ou mappez le nouveau nom que vous souhaitez donner au groupe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom de groupe d’origine</td> 
   <td>Saisissez ou mappez la description mise à jour du groupe.</td> 
  </tr> 
 </tbody>

### Autre

Ce module d’action effectue un appel personnalisé à l’API User Management d’Adobe.

#### Effectuer un appel API personnalisé.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe User Management, voir <a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >Création d’une connexion à Adobe User Management</a> dans cet article.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>URL</p>
      </td>
      <td>
        <p>Saisir un chemin relatif à <code>https://usermanagement.adobe.io/v2/usermanagement/</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Méthode</p>
      </td>
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">En-têtes</td>
      <td>
        <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p>
        <p>Par exemple, <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] ajoute automatiquement des en-têtes d’autorisation et des en-têtes x-api-key.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Chaîne de requête  </td>
      <td>
        <p>Saisissez la chaîne de requête.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Corps</td>
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lors de l’utilisation d’instructions conditionnelles telles que <code>if</code> dans votre fichier JSON, placez les guillemets en dehors de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>
