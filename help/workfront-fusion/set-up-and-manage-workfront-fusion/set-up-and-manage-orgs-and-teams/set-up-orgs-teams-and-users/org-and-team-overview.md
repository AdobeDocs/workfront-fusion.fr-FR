---
title: Présentation des organisations et des équipes Fusion
description: Les fonctionnalités Organisation et Équipes Adobe Workfront Fusion permettent aux entreprises de contrôler l’accès aux scénarios et aux autres fonctionnalités dans Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 44e6de2a-b2d3-410d-abc3-10facd258495
TQID: 'https://experienceleague.adobe.com/rWg9TitUlX092UIFTY1LUZsR7UlmWwE5dItl6wnlBMA'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: f9cdbcf936fc6b022f6513f47b9b377424731419
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 39%
---
# Présentation des organisations et des équipes Adobe Workfront Fusion

Les fonctionnalités Organisation et Équipes Adobe Workfront Fusion permettent aux entreprises de contrôler l’accès aux scénarios et aux autres fonctionnalités dans Fusion.

Une organisation est la plus grande entité d’Adobe Workfront Fusion. Par exemple, votre organisation Fusion peut représenter le compte Fusion pour l’ensemble de votre société.

Les équipes sont des groupes plus petits au sein de l’organisation et partagent des ressources Fusion telles que des scénarios, des connexions et des modèles.

Pour obtenir des instructions sur la création d&#39;une équipe, voir [Créer une équipe](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/create-a-team.md).

## Organisations

Les utilisateurs de Workfront Fusion appartiennent à une organisation.

Les utilisateurs doivent être ajoutés à une organisation avant d’être ajoutés à une équipe.

### Ressources de l’organisation

Les ressources suivantes affectent l’ensemble de l’organisation de Fusion et sont donc détenues et gérées au niveau de l’organisation :

* **Pools de salariés :** : un pool de salariés est une quantité de ressources de traitement Workfront Fusion dédiées à une organisation spécifique.

  Pour plus d&#39;informations, voir [Pools de salariés](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/worker-pools.md).

* **Opérations** : une opération dans Adobe Workfront Fusion est une tâche effectuée par un module.

  Pour plus d’informations, consultez [Opérations](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/operations-in-workfront-fusion.md).

### Rôles d’organisation

Un utilisateur ou une utilisatrice possède l’un des rôles suivants dans une organisation :

* **[!UICONTROL Personne propriétaire]** : la personne propriétaire dispose de toutes les autorisations disponibles dans l’organisation.
* **[!UICONTROL Administrateur]** : les administrateurs peuvent gérer les utilisateurs sur le Adobe Admin Console si l’organisation est activée pour Adobe Identity Management System (IMS) ou peuvent inviter de nouveaux utilisateurs pour les organisations qui ne sont pas sur IMS. Il peut également approuver des modèles.
* **[!UICONTROL Membre]** : les membres peuvent utiliser Workfront Fusion, mais ne peuvent pas apporter de modifications organisationnelles.
* **[!UICONTROL Comptable]** : les comptables peuvent afficher les informations de licence dans le tableau de bord de l&#39;organisation, mais ne peuvent effectuer aucune action.
* **[!UICONTROL Développeur ou développeuse d’applications]** : les fonctionnalités de ce rôle ne sont actuellement pas disponibles. Elle seront disponibles ultérieurement. Il est déconseillé d’affecter des utilisateurs et des utilisatrices à ce rôle pour l’instant.

Pour plus d’informations sur les actions spécifiques dont disposent les utilisateurs et les utilisatrices pour chaque rôle d’organisation, voir [Rôles d’organisation et d’équipe](/help/workfront-fusion/references/licenses-and-roles/organization-roles.md).

## Équipes

Les équipes sont des groupes d’utilisateurs et d’utilisatrices qui partagent un accès à des ressources spécifiques. Ces ressources peuvent inclure les éléments suivants :

* Scénarios
* Connexions
* Webhooks
* Clés
* Entrepôts de données
* Structures de données
* Paramètres de notification par e-mail

>[!NOTE]
>
>Comme les équipes partagent des ressources, il est parfois utile qu’une équipe ne compte qu’un seul membre. Par exemple, les utilisateurs en formation peuvent créer des connexions avec leurs comptes Workfront individuels. Tous les membres de l’équipe peuvent également se connecter au compte Workfront individuel. Dans ce cas, nous recommandons que l’utilisateur soit le seul membre d’une équipe de formation.

Les organisations peuvent disposer d’autant d’équipes que nécessaire et les utilisateurs et les utilisatrices peuvent appartenir à une ou plusieurs équipes.

Les utilisateurs et les utilisatrices peuvent sélectionner leur équipe dans la liste déroulante du panneau de navigation de gauche. Les utilisateurs et les utilisatrices ne voient que les équipes dont ils font partie. Sélectionner une équipe permet à un utilisateur ou à une utilisatrice d’accéder aux ressources de cette équipe.

### Rôles d’équipe

Un utilisateur ou une utilisatrice possède l’un des rôles suivants dans chacune de ses équipes :

* **[!UICONTROL Administrateur d&#39;équipe]** : les administrateurs peuvent ajouter, supprimer ou modifier le rôle d&#39;un membre de l&#39;équipe. Ils peuvent également effectuer toute action disponible pour les autres rôles d&#39;équipe.
* **[!UICONTROL Personne membre de l’équipe]** : le rôle de personne membre de l’équipe permet aux utilisateurs et aux utilisatrices de créer et d’exécuter des scénarios.
* **[!UICONTROL Surveillance de l’équipe]** : le rôle de [!UICONTROL surveillance] permet aux utilisateurs et aux utilisatrices d’accéder aux informations d’exécution pour les scénarios, mais ils ne peuvent pas concevoir de scénarios ou modifier leur statut « actif ».
* **[!UICONTROL Opérateur ou opératrice d’équipe]** : le rôle d’[!UICONTROL opérateur ou opératrice] permet aux utilisateurs et aux utilisatrices d’afficher les données d’exécution et de modifier le statut « actif » des scénarios.
* **[!UICONTROL Personne membre de l’équipe limitée]** : les fonctionnalités de ce rôle ne sont actuellement pas disponibles. Elles seront disponibles ultérieurement. Il est déconseillé d’affecter des utilisateurs et des utilisatrices à ce rôle pour l’instant.

Pour plus d’informations sur les actions spécifiques dont les utilisateurs et les utilisatrices disposent dans chaque rôle d’équipe, voir [Rôles d’organisation et d’équipe](/help/workfront-fusion/references/licenses-and-roles/organization-roles.md).

### Rôles d&#39;équipe personnalisés

<!-- BECKY CHECK ME: The source material (the Slack announcement) says flexible permissions are live in QA and for internal customers, with a limited pilot with paid customers next, then general availability. Confirm availability at the 2026-11-12 release before publishing, and whether this section should say that the feature is available only to some organizations. -->

Outre les rôles d&#39;équipe prédéfinis, chaque équipe comporte un onglet **[!UICONTROL Rôles]** dans lequel vous pouvez créer vos propres rôles. Vous pouvez créer, mettre à jour et supprimer des rôles, et choisir exactement les autorisations incluses par chaque rôle. Vous n’êtes plus limité à un ensemble fixe de rôles.

Pour obtenir des instructions, voir [Afficher et gérer les rôles d&#39;équipe](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/manage-users-and-teams/view-and-manage-team-roles.md).

Avec les rôles personnalisés, vous pouvez :

* Donnez à chaque personne uniquement l’accès dont elle a besoin dans le cadre de son travail, ce qui réduit le risque de modifications accidentelles des scénarios critiques.
* Configurez l’accès pour qu’il corresponde au fonctionnement de votre organisation, au lieu d’adapter vos équipes aux rôles prédéfinis.
* Gérez l’accès vous-même, sans contacter l’assistance.

Toute personne disposant de l&#39;autorisation **[!UICONTROL Gérer les membres]** d&#39;une équipe peut créer, mettre à jour, supprimer et affecter des utilisateurs à des rôles dans cette équipe. Dans les rôles prédéfinis, cette autorisation est incluse dans les rôles Administrateur d’équipe et Propriétaire de l’organisation .

* Les propriétaires d’organisation peuvent créer et gérer des rôles dans toutes les équipes.
* Les administrateurs de l’organisation ne peuvent gérer les rôles que dans les équipes dont ils sont membres et pour lesquelles ils disposent de l’autorisation **[!UICONTROL Gérer les membres]**.
* Les administrateurs d’équipe peuvent gérer les rôles au sein de leurs équipes.

<!-- BECKY CHECK ME: The source does not describe the steps in the Roles tab, the list of permissions that you can choose from, or whether you can edit or delete the predefined roles. Add the steps and permissions list once confirmed. Also confirm that Team Admins can manage roles (the source says the Manage members permission was previously given to Team Admin and Org Owner roles, and that team and org admins can create roles only in the teams where they are admins). -->
