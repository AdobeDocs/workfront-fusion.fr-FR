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
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 58%

---

# Ajouter des utilisateurs et des utilisatrices à Adobe Workfront Fusion via Adobe Admin Console

Vous pouvez ajouter un utilisateur ou une utilisatrice à [!DNL Adobe Admin Console] et l’affecter à [!DNL Adobe Workfront Fusion] ou affecter un utilisateur ou une utilisatrice existant dans [!DNL Adobe Admin Console] à [!DNL Workfront Fusion].

Pour regarder une vidéo décrivant [!DNL Workfront Fusion] dans [!DNL Adobe Admin Console], y compris l’ajout d’utilisateurs ou d’utilisatrices, voir [[!DNL Fusion]  sur Adobe IMS](https://video.tv.adobe.com/v/3412464/){target=_blank}.



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
   <p>Ancienne exigence de licence : [!UICONTROL [!DNL Workfront Fusion] pour l’automatisation et l’intégration du travail] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Exigences actuelles relatives aux produits : si vous disposez du plan de [!DNL Adobe Workfront] [!UICONTROL Select] ou [!UICONTROL Prime], votre entreprise doit acheter des [!DNL Adobe Workfront Fusion] et [!DNL Adobe Workfront] utiliser les fonctionnalités décrites dans cet article. [!DNL Workfront Fusion] est inclus dans le plan de [!DNL Workfront] [!UICONTROL Ultimate].</p>
   <p>Ou</p>
   <p>Exigence du produit hérité : votre entreprise doit acheter [!DNL Adobe Workfront Fusion] et [!DNL Adobe Workfront] pour utiliser les fonctionnalités décrites dans cet article.</p>
   </td> 
  </tr>
   <tr> 
   <td role="rowheader">[!DNL Adobe] droits d’administration</td> 
   <td>Vous devez être un [!UICONTROL Product Configuration Administrator] de produits [!DNL Adobe] pour votre organisation.</td> 
  </tr>
  </tbody> 
</table>

&#42;Pour connaître la formule, le type de licence ou l’accès dont vous disposez, contactez votre administrateur ou votre administratrice [!DNL Workfront].

&#42;&#42;Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir [[!DNL Adobe Workfront Fusion] licences](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).



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
     <p>Vous devez être un administrateur ou une administratrice [!DNL Workfront Fusion] de votre organisation.</p>
     <p>Vous devez être un administrateur ou une administratrice [!DNL Workfront Fusion] de votre équipe.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++


## Conditions préalables

Avant d’utiliser [!DNL Admin Console] pour [!DNL Workfront], vous devriez recevoir un e-mail vous invitant à accéder à la console.

1. Si vous commencez sur [!DNL Adobe] et que vous avez reçu un e-mail vous indiquant que vous disposez désormais de droits d’administration du logiciel et des services [!DNL Adobe] pour votre entreprise, cliquez sur le bouton dans l’e-mail pour créer un compte [!DNL Adobe] et ouvrir [!DNL Admin Console].

   Ou

   Si vous disposez déjà d’un compte Adobe, accédez à la page [[!DNL Adobe Admin Console] ](https://adminconsole.adobe.com).


## Ajouter un nouvel utilisateur ou une nouvelle utilisatrice à [!DNL Adobe Admin Console] et [!DNL Workfront Fusion]

1. Dans la [[!DNL Adobe Admin Console] page](https://adminconsole.adobe.com/), sélectionnez l’onglet **[!UICONTROL Products]** dans la barre de navigation supérieure, puis sélectionnez la mosaïque du produit **[!DNL Workfront Fusion]**.

   ![Fusion dans Admin Console](assets/fusion-product-admin-console.png)

1. Dans la liste qui s’affiche, sélectionnez l’entreprise à laquelle vous souhaitez ajouter un utilisateur ou une utilisatrice.

   ![Instance Fusion dans Admin Console](assets/fusion-instances-admin-console.png)

1. Dans la liste qui s&#39;affiche, avec l&#39;onglet **[!UICONTROL Product Profiles]** sélectionné, cliquez sur le nom du lien [!DNL Workfront Fusion] [!UICONTROL Product Profile].

   >[!IMPORTANT]
   >
   > N’apportez aucune modification au [!UICONTROL Product Profile] lui-même.

1. Avec l’onglet **[!UICONTROL Users]** sélectionné au-dessus de la liste, cliquez sur **[!UICONTROL Add User]**.

1. Dans la zone de **[!UICONTROL Add users to this product profile]**, saisissez l’adresse e-mail ou le nom d’un utilisateur que vous souhaitez ajouter, puis sélectionnez l’utilisateur dans la liste qui s’affiche.

1. Cliquez sur **[!UICONTROL Save]**.

   La personne est créée dans [!DNL Workfront Fusion].

1. (Facultatif) Passez à la section [Modifier le niveau d’accès d’un utilisateur ou d’une utilisatrice dans  [!DNL Workfront Fusion]](#change-a-users-access-level-in-workfront-fusion).

## Modifier le niveau d’accès d’un utilisateur ou d’une utilisatrice dans Workfront Fusion

* [Modifier le rôle d’un utilisateur ou d’une utilisatrice sur Administrateur ou administratrice](#change-a-users-role-to-admin)
* [Remplacer le rôle d’un utilisateur par celui de membre, de comptable ou de développeur d’applications](#change-a-users-role-to-member-accountant-or-app-developer)

### Modifier le rôle d’un utilisateur ou d’une utilisatrice sur Administrateur ou administratrice

L’attribution d’un rôle d’administrateur ou d’administratrice à une personne doit être effectuée dans l’[!DNL Adobe Admin Console].

1. Sur la page de [!UICONTROL Product Profile] de [!DNL Workfront Fusion] où vous avez ajouté l’utilisateur, sélectionnez l’onglet **[!UICONTROL Admins]** .

1. Cliquez sur **[!UICONTROL Add Admin]**.

1. Dans la zone de **[!UICONTROL Add product profile administrators]**, saisissez l’adresse e-mail ou le nom de l’utilisateur ou de l’utilisatrice que vous souhaitez voir devenir administrateur, puis sélectionnez l’utilisateur ou l’utilisatrice dans la liste qui s’affiche.

1. Cliquez sur **[!UICONTROL Save]**.

   L’utilisateur est désormais administrateur dans [!DNL Workfront Fusion].

### Remplacer le rôle d’un utilisateur par celui de membre, de comptable ou de développeur d’applications

Les rôles de membre, de comptable et de développeur d’applications sont gérés dans Workfront Fusion.

Pour obtenir des instructions, voir [Affichage ou modification des rôles utilisateur](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/manage-users-and-teams/view-or-edit-user-roles.md).

## Attribuer une personne existante dans l’[!DNL Adobe Admin Console] à [!DNL Workfront Fusion]

Vous pouvez ajouter un utilisateur existant à une équipe dans Fusion. Cela est géré dans Fusion.

Pour obtenir des instructions, voir [Ajouter un utilisateur à une équipe](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/add-a-user-to-a-team.md).
