---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Ajouter des utilisateurs et des utilisatrices à Adobe Workfront Fusion via Adobe Admin Console
description: Vous pouvez ajouter un utilisateur ou une utilisatrice à Adobe Admin Console et l’affecter à Adobe Workfront Fusion ou affecter un utilisateur ou une utilisatrice existant d’Adobe Admin Console à Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 7cb1c1a7-3c7a-459a-818f-d9cefcb9988b
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 43%

---

# Ajouter des utilisateurs et des utilisatrices à Adobe Workfront Fusion via Adobe Admin Console

Vous pouvez ajouter un utilisateur à la [!DNL Adobe Admin Console] et l’affecter à Adobe Workfront Fusion ou affecter un utilisateur existant de la [!DNL Adobe Admin Console] à Workfront Fusion.

Pour regarder une vidéo décrivant Workfront Fusion dans la [!DNL Adobe Admin Console], y compris comment ajouter des utilisateurs, voir [[!DNL Fusion] sur Adobe IMS](https://video.tv.adobe.com/v/3412464/){target=_blank}.



Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Formule Adobe Workfront*</td> 
   <td> <p>[!UICONTROL Pro] ou version supérieure</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licence Adobe Workfront*</td> 
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licence Adobe Workfront Fusion **</td> 
   <td>
   <p>Exigence de licence actuelle : aucune exigence de licence Workfront Fusion.</p>
   <p>Ou</p>
   <p>Exigence de licence héritée : [!UICONTROL Workfront Fusion for Work Automation and Integration] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Configuration requise actuelle du produit : si vous disposez du plan Adobe Workfront [!UICONTROL Select] ou [!UICONTROL Prime], votre entreprise doit acheter Adobe Workfront Fusion ainsi qu’Adobe Workfront pour utiliser les fonctionnalités décrites dans cet article. Workfront Fusion est inclus dans le plan Workfront [!UICONTROL Ultimate].</p>
   <p>Ou</p>
   <p>Exigences de produit héritées : votre entreprise doit acheter Adobe Workfront Fusion ainsi qu’Adobe Workfront pour utiliser les fonctionnalités décrites dans cet article.</p>
   </td> 
  </tr>
   <tr> 
   <td role="rowheader">[!DNL Adobe] droits d’administration</td> 
   <td>Vous devez être un ou une [!UICONTROL Product Configuration Administrator] de produits [!DNL Adobe] pour votre entreprise.</td> 
  </tr>
  </tbody> 
</table>

&#42;Pour connaître le forfait, le type de licence ou l’accès dont vous disposez, contactez votre administrateur ou administratrice Workfront.

&#42;&#42;Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).



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


## Conditions préalables

Avant d’utiliser le [!DNL Admin Console] pour Workfront, vous devriez recevoir un e-mail vous invitant à accéder à la console.

1. Si vous commencez sur [!DNL Adobe] et que vous avez reçu un e-mail vous indiquant que vous disposez désormais de droits d’administration du logiciel et des services [!DNL Adobe] pour votre entreprise, cliquez sur le bouton dans l’e-mail pour créer un compte [!DNL Adobe] et ouvrir [!DNL Admin Console].

   Ou

   Si vous disposez déjà d’un compte Adobe, accédez à la page [[!DNL Adobe Admin Console] &#x200B;](https://adminconsole.adobe.com).


## Ajout d’un nouvel utilisateur à [!DNL Adobe Admin Console] et Workfront Fusion

1. Dans la [[!DNL Adobe Admin Console] page](https://adminconsole.adobe.com/), sélectionnez l’onglet **[!UICONTROL Produits]** dans la barre de navigation supérieure, puis sélectionnez la mosaïque du produit **Workfront Fusion**.

   ![Fusion dans Admin Console](assets/fusion-product-admin-console.png)

1. Dans la liste qui s’affiche, sélectionnez l’entreprise à laquelle vous souhaitez ajouter un utilisateur ou une utilisatrice.

   ![Instance Fusion dans Admin Console](assets/fusion-instances-admin-console.png)

1. Dans la liste qui s’affiche, lorsque l’onglet **[!UICONTROL Profils de produit]** est sélectionné, cliquez sur le nom du lien Workfront Fusion [!UICONTROL Profil de produit].

   >[!IMPORTANT]
   >
   > N’apportez aucune modification au [!UICONTROL Profil de produit] en lui-même.

1. Avec l’onglet **[!UICONTROL Utilisateurs et utilisatrices]** sélectionné au-dessus de la liste, cliquez sur **[!UICONTROL Ajouter un utilisateur ou une utilisatrice]**.

1. Dans la zone **[!UICONTROL Ajouter des utilisateurs et des utilisatrices à ce profil de produit]**, saisissez l’adresse e-mail ou le nom d’un utilisateur ou d’une utilisatrice que vous souhaitez ajouter, puis sélectionnez-le dans la liste qui s’affiche.

1. Cliquer sur **[!UICONTROL Enregistrer]**.

   L’utilisateur est créé dans Workfront Fusion.

1. (Facultatif) Passez à [Modifier le niveau d’accès d’un utilisateur dans Workfront Fusion](#change-a-users-access-level-in-workfront-fusion)

## Modifier le niveau d’accès d’un utilisateur ou d’une utilisatrice dans Workfront Fusion

* [Modifier le rôle d’un utilisateur ou d’une utilisatrice sur Administrateur ou administratrice](#change-a-users-role-to-admin)
* [Remplacer le rôle d’un utilisateur par celui de membre, de comptable ou de développeur d’applications](#change-a-users-role-to-member-accountant-or-app-developer)

### Modifier le rôle d’un utilisateur ou d’une utilisatrice sur Administrateur ou administratrice

L’attribution d’un rôle d’administrateur ou d’administratrice à une personne doit être effectuée dans l’[!DNL Adobe Admin Console].

1. Sur la page Workfront Fusion [!UICONTROL Profil de produit] où vous avez ajouté l’utilisateur, sélectionnez l’onglet **[!UICONTROL Administrateurs]**.

1. Cliquez sur **[!UICONTROL Ajouter un administrateur ou une administratrice]**.

1. Dans la zone **[!UICONTROL Ajouter des administrateurs de profil de produit]**, saisissez l’adresse e-mail ou le nom de l’utilisateur que vous souhaitez devenir administrateur, puis sélectionnez l’utilisateur dans la liste qui s’affiche.

1. Cliquer sur **[!UICONTROL Enregistrer]**.

   L’utilisateur est désormais administrateur dans Workfront Fusion.

### Remplacer le rôle d’un utilisateur par celui de membre, de comptable ou de développeur d’applications

Les rôles de membre, de comptable et de développeur d’applications sont gérés dans Workfront Fusion.

Pour obtenir des instructions, voir [Affichage ou modification des rôles utilisateur](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/manage-users-and-teams/view-or-edit-user-roles.md).

## Affectation d’un utilisateur existant dans le [!DNL Adobe Admin Console] à Workfront Fusion

Vous pouvez ajouter un utilisateur existant à une équipe dans Fusion. Cela est géré dans Fusion.

Pour obtenir des instructions, voir [Ajouter un utilisateur à une équipe](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/add-a-user-to-a-team.md).
