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
source-git-commit: f7c1d5b1de74cc0c59e3a00938bed14b489500db
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 42%

---

# Ajouter des utilisateurs et des utilisatrices à Adobe Workfront Fusion via Adobe Admin Console

Vous pouvez ajouter un utilisateur à la [!DNL Adobe Admin Console] et l’affecter à Adobe Workfront Fusion ou affecter un utilisateur existant de la [!DNL Adobe Admin Console] à Workfront Fusion.

Pour regarder une vidéo décrivant Workfront Fusion dans la [!DNL Adobe Admin Console], y compris comment ajouter des utilisateurs, voir [[!DNL Fusion] sur Adobe IMS](https://video.tv.adobe.com/v/3412464/){target=_blank}.

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
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurations des niveaux d’accès</td> 
   <td> 
     <p>Vous devez être administrateur ou administratrice Workfront Fusion pour votre entreprise.</p>
     <p>Vous devez être un administrateur Workfront Fusion pour votre équipe.</p>
   </td> 
  </tr> 
  </tr>
   <tr> 
   <td role="rowheader">Configurations des niveaux d’accès</td> 
   <td>Vous devez être administrateur de la configuration de produit pour les produits Adobe de votre entreprise.</td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

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
