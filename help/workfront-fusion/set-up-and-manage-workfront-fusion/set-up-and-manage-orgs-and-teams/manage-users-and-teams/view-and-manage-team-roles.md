---
title: Afficher et gérer les rôles d'équipe
description: Chaque équipe comporte un onglet Rôles dans lequel vous pouvez afficher les rôles de l’équipe, créer vos propres rôles, choisir les autorisations incluses par chaque rôle et mettre à jour ou supprimer des rôles.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: a3a6922afd713cd002cdf472c7ef62c1855b80d9
workflow-type: tm+mt
source-wordcount: '1032'
ht-degree: 11%
---
# Afficher et gérer les rôles d&#39;équipe

Vous pouvez afficher les rôles disponibles dans une équipe, créer vos propres rôles et choisir les autorisations incluses par chaque rôle. Vous pouvez également mettre à jour et supprimer des rôles.

Les rôles personnalisés offrent les avantages suivants :

* Chaque membre de l’équipe dispose uniquement de l’accès dont a besoin sa tâche, ce qui réduit le risque de modifications accidentelles des scénarios critiques.
* Les rôles personnalisés peuvent mieux correspondre au fonctionnement de votre organisation, au lieu d’adapter vos équipes aux rôles prédéfinis.
* Vous pouvez gérer l’accès vous-même, sans contacter l’assistance.

Pour obtenir un aperçu des organisations, des équipes et des rôles d&#39;équipe prédéfinis, consultez [Présentation de l&#39;organisation et de l&#39;équipe](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/org-and-team-overview.md). Pour les autorisations incluses dans les rôles prédéfinis, voir [Rôles d&#39;organisation et d&#39;équipe](/help/workfront-fusion/references/licenses-and-roles/organization-roles.md).

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
   <p>Si votre organisation dispose d’un package Workfront Select ou Prime qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acquérir Adobe Workfront Fusion.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurations des niveaux d’accès</td> 
   <td> 
     <p>Vous devez disposer de l'autorisation <b>[!UICONTROL Gérer les membres]</b> dans l'équipe. Dans les rôles prédéfinis, cette autorisation est incluse dans les rôles Administrateur d’équipe et Propriétaire de l’organisation .</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation Workfront](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Qui peut gérer les rôles d&#39;équipe

Toute personne disposant de l&#39;autorisation **[!UICONTROL Gérer les membres]** d&#39;une équipe peut créer, mettre à jour, supprimer et affecter des utilisateurs à des rôles dans cette équipe.

* Les propriétaires d’organisation peuvent créer et gérer des rôles dans toutes les équipes.
* Les administrateurs de l’organisation ne peuvent gérer les rôles que dans les équipes dont ils sont membres et pour lesquelles ils disposent de l’autorisation **[!UICONTROL Gérer les membres]**.
* Les administrateurs d’équipe peuvent gérer les rôles au sein de leurs équipes.

## Créer ou modifier un rôle

1. Dans Fusion, dans le volet de navigation de gauche, cliquez sur **Présentation de l’équipe**.
1. (Conditionnel) Si vous n&#39;êtes pas sur la page pour l&#39;équipe dont vous souhaitez afficher les rôles, cliquez sur la liste déroulante **Équipe** près du haut de la page et sélectionnez l&#39;équipe appropriée.
1. Ouvrez l’onglet **[!UICONTROL Rôles]**.

   Cet onglet répertorie les rôles disponibles dans l&#39;équipe, y compris les rôles prédéfinis. Pour chaque rôle, la liste affiche le nom du rôle et un résumé de ses autorisations, telles que « Aucune autorisation », « Membre » ou « 19 autorisations personnalisées ».

1. Pour créer un rôle, cliquez sur **[!UICONTROL Créer un rôle]**.

   Ou

   Pour modifier un rôle, cliquez sur **[!UICONTROL Modifier]** dans la ligne du rôle que vous souhaitez modifier.

   <!-- BECKY CHECK ME: The Edit button is available for the predefined roles as well as custom roles. Confirm the title of the edit page, whether you can rename the predefined roles, and what happens to users who already have the role. -->

1. Saisissez un nom pour le rôle dans le champ **[!UICONTROL Nom du rôle]**.
1. Dans la liste déroulante **[!UICONTROL Modèle de rôle]**, sélectionnez le modèle à partir duquel vous souhaitez commencer.

   Le modèle définit les autorisations initiales pour le rôle. Le modèle par défaut est **[!UICONTROL Visionneuse]**.

1. Dans la zone **[!UICONTROL Autorisations étendues]**, sélectionnez les autorisations que vous souhaitez que le rôle inclue.

   Les autorisations sont regroupées par zone, par exemple **[!UICONTROL Automatisations]**, **[!UICONTROL Connexions]** et **[!UICONTROL Équipe]**. Pour chaque zone, vous pouvez effectuer l’une des opérations suivantes :

   * Pour définir toutes les autorisations d&#39;une zone en même temps, cliquez sur **[!UICONTROL Pas d&#39;accès]**, **[!UICONTROL Affichage uniquement]** ou **[!UICONTROL Accès complet]** en regard du nom de la zone.
   * Pour choisir des autorisations spécifiques, cochez ou décochez la case correspondant à chaque autorisation.

   Pour obtenir la liste des autorisations, voir [Autorisations que vous pouvez inclure dans un rôle](#permissions-that-you-can-include-in-a-role) dans cet article.

   <!-- BECKY CHECK ME: Confirm the options in the Role template dropdown and what each one selects. Confirm exactly what No access, View only, and Full access select in each area (in the screenshot, View only selects the view permissions). Confirm whether there is a Description field, and whether there are areas below Team on the page (the screenshots end at Team). -->

1. Cliquer sur **[!UICONTROL Enregistrer]**. Pour fermer la page sans enregistrer, cliquez sur **[!UICONTROL Annuler]**.
1. (Facultatif) Pour supprimer un rôle, cliquez sur **[!UICONTROL Supprimer]** dans la ligne du rôle de l’onglet **[!UICONTROL Rôles]**.

   <!-- BECKY CHECK ME: Confirm why the Delete button is unavailable (dimmed) for some roles, such as Team Operator, Team Member, and Team Admin in the screenshot, whether there is a confirmation prompt, and what happens to users who have the role. Update this step and add a note, if needed. -->

Un rôle que vous créez est disponible dans l’équipe. Vous pouvez l’affecter aux membres de l’équipe.

### Autorisations que vous pouvez inclure dans un rôle

<table style="table-layout:auto">
 <col>
 <col>
 <thead>
  <tr>
   <th>Zone</th>
   <th>Autorisations</th>
  </tr>
 </thead>
 <tbody>
 <tr>
   <td role="rowheader">[!UICONTROL Automations]</td>
   <td>Afficher la liste, Afficher les détails, Afficher l’historique d’exécution, Gérer les notifications, Réinitialiser les statistiques, Exécuter une fois, Modifier le planning, Activer, Désactiver, Créer, Modifier, Publier, Supprimer</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Incomplete executions]</td>
   <td>Afficher, Gérer</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Webhooks]</td>
   <td>Afficher, Afficher la file d’attente, Créer, Modifier, Gérer la file d’attente, Modifier la priorité, Supprimer</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Connexions]</td>
   <td>Afficher, Créer, Modifier, Supprimer</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Keys]</td>
   <td>Afficher, Créer, Modifier, Supprimer</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Data stores]</td>
   <td>Afficher la liste, Parcourir les enregistrements, Créer, Modifier, Supprimer</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Structures de données]</td>
   <td>Afficher, Créer, Modifier, Supprimer</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Templates]</td>
   <td>Afficher la liste, Afficher les détails, Créer, Modifier, Supprimer</td>
  </tr>
 <tr>
   <td role="rowheader">[!UICONTROL Team]</td>
   <td>Afficher l'équipe, Modifier les paramètres d'équipe, Gérer les membres, Supprimer l'équipe</td>
  </tr>
 </tbody>
</table>

<!-- BECKY CHECK ME: Confirm that this list is complete, and add a description of what each permission allows, if needed. The list is taken from the Create role page, which may have more areas below Team. -->

## Cloner des rôles à une autre équipe

Vous pouvez copier les rôles d&#39;une équipe vers une autre équipe, de sorte que vous n&#39;ayez pas à recréer les mêmes rôles dans chaque équipe.

1. Ouvrez l’onglet **[!UICONTROL Rôles]** de l’équipe, comme décrit dans [Créer ou modifier un rôle](#create-or-edit-a-role) dans cet article.
1. Cliquez sur **[!UICONTROL Cloner à l&#39;équipe]**.

   La page **[!UICONTROL Cloner des rôles à une autre équipe]** s&#39;ouvre.

1. Dans la liste déroulante **[!UICONTROL Équipe cible]**, sélectionnez l’équipe vers laquelle vous souhaitez cloner les rôles.

   Un tableau s&#39;affiche et répertorie les rôles dans l&#39;équipe actuelle.

1. Pour chaque rôle du tableau, vérifiez et définissez les éléments suivants :

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Source role]</td> 
      <td> <p>Le rôle dans l'équipe actuelle, avec un résumé de ses autorisations.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Action]</td> 
      <td> <p>Que faire de ce rôle ? Par exemple, <b>[!UICONTROL Copier dans le rôle existant]</b> copie les autorisations du rôle source dans un rôle qui existe déjà dans l’équipe cible.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Target]</td> 
      <td> <p>Rôle dans l’équipe cible dans lequel le rôle source est copié.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Changes]</td> 
      <td> <p>Si le rôle cible diffère du rôle source. Par exemple, <b>[!UICONTROL Déjà synchronisé]</b> signifie que le rôle cible dispose déjà des mêmes autorisations que le rôle source.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Users]</td> 
      <td> <p>Informations sur les utilisateurs qui disposent du rôle. Par exemple, <b>[!UICONTROL Aucun utilisateur correspondant]</b> signifie qu’il n’y a aucun utilisateur à inclure.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Status]</td> 
      <td> <p>Résultat pour le rôle après le clonage.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Cliquez Sur **[!UICONTROL Cloner]**. Pour fermer la page sans clonage, cliquez sur **[!UICONTROL Annuler]**.

<!-- BECKY CHECK ME: The screenshot shows the Clone roles to another team page after a target team is selected. Confirm the options in the Action dropdown (for example, whether you can create a new role in the target team), the options in the Target dropdown, what the checkbox in the Users column does (for example, whether it also assigns the role to matching users in the target team) and what "matching users" means, what the Changes column shows when the roles differ, and what the Status column shows before and after you clone. -->

<!-- BECKY CHECK ME: Confirm whether the Target team dropdown lists all teams or only the teams that you can manage, and whether the Clone to team button is visible to everyone who can manage roles. -->

## Attribution d’un rôle à un utilisateur

Vous attribuez un rôle personnalisé de la même manière que vous attribuez un rôle prédéfini. Pour obtenir des instructions, voir [Ajouter un utilisateur à une équipe](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/add-a-user-to-a-team.md) et [Afficher ou modifier les rôles utilisateur](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/manage-users-and-teams/view-or-edit-user-roles.md#view-or-edit-user-roles-for-a-team).

<!-- BECKY CHECK ME: Confirm that custom roles appear in the role dropdowns in both of these procedures. -->

## Considérations

* Cascade d’autorisations d’organisation. Pour permettre à quelqu&#39;un d&#39;effectuer une action dans toutes les équipes, attribuez un rôle d&#39;organisation au lieu de créer un rôle d&#39;équipe. Pour plus d&#39;informations, voir [Rôles d&#39;organisation et d&#39;équipe](/help/workfront-fusion/references/licenses-and-roles/organization-roles.md).
* Les rôles que vous créez appartiennent à une équipe.

<!-- BECKY CHECK ME: The Slack thread says that defining a role that is available in all teams was out of scope for the initial release. Confirm that a role belongs to a single team, and that you clone it to use it in another team. -->
