---
title: Outils de serveur MCP Adobe Workfront Fusion
description: Liste de référence des outils que le serveur MCP Adobe Workfront Fusion expose aux plateformes d’IA et à Coworker.
source-git-commit: 1bfcdb6abe42eca27d2f3ae5a1a1d2cfd3901d33
workflow-type: tm+mt
source-wordcount: '1546'
ht-degree: 7%
---

# Outils de serveur MCP Adobe Workfront Fusion


Cet article répertorie les outils que le serveur MCP Adobe Workfront Fusion expose à un agent d’IA connecté. L’agent appelle ces outils en votre nom lorsque vous lui demandez de rechercher, d’inspecter, de créer, d’exécuter, de mettre à jour ou de supprimer des éléments Fusion.

Les mêmes outils sont disponibles dans chaque surface prise en charge : connexions MCP personnalisées dans Claude, ChatGPT, Copilot ou votre propre agent ; et Coworker, à la fois autonomes et dans le rail de droite de Fusion. Pour la configuration, voir [Configuration du serveur MCP Adobe Workfront Fusion](configure-fusion-mcp-server.md).

L’agent agit dans Fusion à l’aide de votre Adobe ID, de votre rôle d’organisation Fusion et de vos rôles d’équipe. Un outil ne fonctionne que si vous disposez de l’autorisation correspondante dans Fusion. Adobe n’est pas responsable des modifications apportées par l’agent à vos données Fusion.

## Actions de lecture et d’écriture

Chaque outil est classé comme suit :

* **Lecture** : récupère des informations sans rien modifier, comme répertorier les scénarios ou obtenir une exécution.
* **Write** : crée, modifie, exécute ou supprime des données Fusion, telles que le clonage d’un scénario ou l’effacement d’une file d’attente webhook.

## Outils d’organisation

L’organisation active s’applique à tous les autres outils de la session en cours.

| Outil | Nom | Action | Description |
| --- | --- | --- | --- |
| Liste des organisations | `fusion_orgs_list` | Lire | Répertorie les organisations Fusion auxquelles vous pouvez accéder, avec leur identifiant, leur région (zone) et leur libellé. |
| Définir l’organisation active | `fusion_orgs_set` | Session | Active l’organisation pour la session en cours. Ne modifie aucune donnée Fusion. |
| Obtenir l’organisation actuelle | `fusion_organizations_get` | Lire | Renvoie l’organisation actuelle. |
| Liste des organisations | `fusion_organizations_list` | Lire | Répertorie toutes les organisations que vous pouvez afficher. |

## Équipes

| Outil | Nom | Action | Description |
| --- | --- | --- | --- |
| Liste des équipes | `fusion_teams_list` | Lire | Répertorie les équipes de l’organisation que vous pouvez afficher. |
| Obtenir l’équipe | `fusion_teams_get` | Lire | Renvoie une seule équipe dans une organisation. |
| Supprimer l&#39;équipe | `fusion_teams_delete` | Write | Supprime une équipe. Cela arrête également ses scénarios et supprime ses autorisations. Elle ne peut pas être annulée via l’API et nécessite une confirmation. |

## Utilisateurs et utilisatrices

| Outil | Nom | Action | Description |
| --- | --- | --- | --- |
| Obtention des régions Fusion | `fusion_users_get_regions` | Lire | Renvoie les régions et organisations Fusion auxquelles vous pouvez accéder. Utilisez-le pour rechercher des ID d’organisation valides. |
| Obtenir l’utilisateur actuel | `fusion_users_get_me` | Lire | Renvoie votre profil avec les rôles de votre organisation et de votre équipe. |
| Liste des utilisateurs | `fusion_users_list` | Lire | Répertorie les utilisateurs et utilisatrices de l’organisation. |
| Obtenir l’utilisateur | `fusion_users_get` | Lire | Renvoie un utilisateur unique dans une organisation. |

## Outils de scénario

### Scénarios

| Outil | Nom | Action | Description |
| --- | --- | --- | --- |
| Répertorier les scénarios | `fusion_scenarios_list` | Lire | Répertorie les scénarios dans l’organisation. |
| Obtenir le scénario | `fusion_scenarios_get` | Lire | Renvoie un scénario, y compris son plan directeur complet. |
| Obtenir le lien du scénario | `fusion_scenarios_get_link` | Lire | Renvoie le lien de l’interface utilisateur de Fusion pour ouvrir un scénario dans le navigateur. |
| Obtention des dépendances de scénario | `fusion_scenarios_getDependencies` | Lire | Renvoie les connexions, les clés, les entrepôts de données, les structures de données et les Webhooks aux références du plan directeur du scénario. |
| Rechercher les scénarios dépendants | `fusion_scenarios_dependents` | Lire | Recherche les scénarios qui font référence à un webhook, un magasin de données, une structure de données, une connexion, une clé ou un scénario donné. Utile pour l’analyse d’impact avant de modifier ou supprimer une ressource. |
| Validation du plan directeur | `fusion_scenarios_validate_blueprint` | Lire | Valide structurellement un plan directeur par rapport à une équipe (références de module, connexions, champs obligatoires) sans enregistrer quoi que ce soit. |
| Créer un scénario | `fusion_scenarios_create` | Write | Crée un scénario dans une équipe à partir d’un plan directeur, avec un nom, une description, un dossier, une planification et un traitement séquentiel facultatifs. |
| Cloner le scénario | `fusion_scenarios_clone` | Write | Clone un scénario dans la même équipe ou dans une autre. Lors du clonage entre les équipes, vous mappez chaque connexion, webhook, magasin de données, structure de données et clé à une ressource cible. Facultativement continue à partir du dernier enregistrement traité. |
| Mettre à jour le scénario | `fusion_scenarios_update` | Write | Modifie le nom, la description, le dossier, la planification ou le statut actif (activer/désactiver). Peut également restaurer un scénario supprimé. |
| Exécuter le scénario une fois | `fusion_scenarios_execute` | Write | Exécute un scénario une fois et attend (jusqu’à un délai d’expiration) le résultat, le statut renvoyé et tout message d’erreur. Non pris en charge pour les scénarios instantanés (déclenchés par webhook). |
| Supprimer le scénario | `fusion_scenarios_delete` | Write | Supprime un scénario. Les scénarios supprimés peuvent être restaurés avec **Mettre à jour le scénario**. |

Exemples d’invites :

* _Quels scénarios actifs de l’équipe marketing n’ont pas été modifiés depuis 6 mois ?_
* _Quelles connexions le scénario « Salesforce → Workfront sync » utilise-t-il ?_
* _Clonez la « prise de lead » dans l’équipe des ventes et remplacez la connexion de Salesforce des ventes._
* _Valider ce plan directeur avant de l’importer._
* _Exécutez le « rapport nocturne » une fois et dites-moi s’il réussit._

### Versions du scénario

| Outil | Nom | Action | Description |
| --- | --- | --- | --- |
| Liste des versions de scénario | `fusion_scenario_versions_list` | Lire | Répertorie les versions enregistrées d’un scénario. Filtrez par `version`, `createdAt`, `comment`. |
| Obtenir la version du scénario | `fusion_scenario_versions_get` | Lire | Renvoie le plan directeur et les métadonnées d’une version spécifique. |
| Créer une version de scénario | `fusion_scenario_versions_create` | Write | Publie un plan directeur en tant que nouvelle version de scénario, qui devient le plan directeur actif. Les versions antérieures sont conservées et la publication d’un plan directeur identique n’a aucun effet. |

Exemples d’invites :

* _Qu’est-ce qui a changé entre la version 12 et la version 14 de ce scénario ?_

### Dossiers

| Outil | Nom | Action | Description |
| --- | --- | --- | --- |
| Répertorier les dossiers | `fusion_folders_list` | Lire | Répertorie les dossiers de scénarios, avec le nombre de scénarios. |
| Créer un dossier | `fusion_folders_create` | Write | Crée un dossier dans une équipe. |
| Renommer le dossier | `fusion_folders_update` | Write | Renomme un dossier. |
| Supprimer le dossier | `fusion_folders_delete` | Write | Supprime un dossier. |

## Outils d&#39;exécution

| Outil | Nom | Action | Description |
| --- | --- | --- | --- |
| Liste des exécutions | `fusion_executions_list` | Lire | Répertorie les exécutions pour un scénario ou une exécution incomplète. Filtrez par `status` (par exemple, `status==3` pour les erreurs, `status==2` pour les avertissements), `timestamp`, `duration`, `bundles`, `operations`, `transfer`. Inclut éventuellement des exécutions de vérification. |
| Obtenir l’exécution | `fusion_executions_get` | Lire | Renvoie une seule exécution et des métadonnées sur son scénario ou une exécution incomplète. |

Exemples d’invites :

* _Afficher les exécutions ayant échoué de la « Synchronisation des factures » depuis hier et résumer les erreurs._
* _Quelle exécution de ce scénario a utilisé le plus d’opérations cette semaine ?_

## Outils d’exploitation (utilisation)

| Outil | Nom | Action | Description |
| --- | --- | --- | --- |
| Opérations d’obtention | `fusion_operations_get` | Lire | Renvoie une série temporelle d’opérations (par jour ou mois) pour une période allant jusqu’à 1 an. Filtrer par équipe, scénario ou package ; regrouper par module, package, scénario ou équipe. |
| Récapitulatif des opérations Get | `fusion_operations_summary_by_org` | Lire | Renvoie le nombre total d’opérations par scénario et équipe pour une période, plus le total global. |

Exemples d’invites :

* _Les 10 principaux scénarios par opération le mois dernier._
* _Combien d’opérations l’application Salesforce a-t-elle utilisées au T3 ?_

## Outils de connexion et clés

Ces outils renvoient uniquement des métadonnées. Ils ne renvoient pas d’informations d’identification, de jetons ou de valeurs secrètes.

| Outil | Nom | Action | Description |
| --- | --- | --- | --- |
| Rechercher des connexions | `fusion_connections_search` | Lire | Répertorie les connexions. Filtrez par `name`, `accountName`, `accountType`, `expire`, `teamId`, `scopesCount`, `editable`, `environmentType`, `authenticationType`. |
| Obtenir la connexion | `fusion_connections_get` | Lire | Renvoie les détails d’une seule connexion. |
| Supprimer la connexion | `fusion_connections_delete` | Write | Supprime une connexion. Échoue si un webhook en dépend toujours. Les scénarios qui l’utilisent sont désolidarisés et ne bloquent pas la suppression. |
| Clés de recherche | `fusion_keys_search` | Lire | Répertorie les clés. Filtrez par `name`, `typeName`, `teamId`. |
| Obtenir la clé | `fusion_keys_get` | Lire | Renvoie les détails d’une seule clé. |
| Supprimer la clé | `fusion_keys_delete` | Write | Supprime une clé. Les scénarios qui l’utilisent ne bloquent pas la suppression. |

Exemples d’invites :

* _Quelles connexions expirent au cours des 30 prochains jours et quels scénarios les utilisent ?_

## Outils Webhook

### Webhooks

| Outil | Nom | Action | Description |
| --- | --- | --- | --- |
| Répertorier les webhooks | `fusion_hooks_list` | Lire | Répertorie les Webhooks (hooks). Filtrez par `name`, `teamId`, `type`, `enabled`, `gone`, `typeName`, `scenarioId`, `priority`, `detached`, etc. |
| Obtenir webhook | `fusion_hooks_get` | Lire | Renvoie la configuration d’un webhook, la liaison du propriétaire et les références externes. |
| Obtenir les dépendances webhook | `fusion_hooks_dependencies` | Lire | Répertorie la connexion, la structure de données et la clé référencée par un webhook. Exécutez-le avant le clonage. |
| Cloner le webhook | `fusion_hooks_clone` | Write | Copie un webhook avec une nouvelle URL, éventuellement dans une autre équipe. Peut remplacer sa connexion, sa structure de données ou sa clé. |
| Supprimer le webhook | `fusion_hooks_delete` | Write | Supprime un webhook et ses événements placés en file d’attente. Seul le créateur du webhook peut le supprimer. |
| Rechercher des webhooks dépendants | `fusion_hooks_dependents` | Lire | Recherche les Webhooks qui font référence à une connexion donnée. |

### File d’attente du Webhook

| Outil | Nom | Action | Description |
| --- | --- | -------- | --- |
| Obtenir les statistiques sur la file d’attente | `fusion_queue_stats` | Lire | Renvoie le nombre d’événements en file d’attente, la limite de la file d’attente et si le webhook est activé. |
| File d’attente de la liste | `fusion_queue_list` | Lire | Répertorie les événements webhook reçus en attente de traitement. |
| Obtenir l’élément de file d’attente | `fusion_queue_get` | Lire | Retourne un seul événement en file d&#39;attente, incluant sa payload décodée. |
| Supprimer les éléments de la file d’attente | `fusion_hook_queue_delete` | Write | Supprime les événements webhook mis en file d’attente par ID (jusqu’à 50), ou tous ceux-ci avec des exclusions facultatives. Le nom de l&#39;outil connecté est `fusion_hook_queue_delete` et ne correspond pas à l&#39;ancien nom de `fusion_queue_delete`. |

Exemples d’invites :

* _Le webhook « Envois de formulaire » est-il en cours de sauvegarde ?_
* _Afficher la payload de l’événement en file d’attente le plus ancien._

## Stockage des données et outils de structure des données

| Outil | Nom | Action | Description |
| --- | --- | --- | --- |
| Répertorier les magasins de données | `fusion_datastores_list` | Lire | Répertorie les magasins de données avec le nombre d’enregistrements, la taille et la taille maximale. |
| Obtenir le magasin de données | `fusion_datastores_get` | Lire | Renvoie les métadonnées et l’utilisation d’un magasin de données, la structure de données liée et le paramètre de validation stricte. |
| Supprimer le magasin de données | `fusion_datastores_delete` | Write | Supprime un magasin de données et tous ses enregistrements. Échoue si un scénario l’utilise toujours. |
| Liste des enregistrements du magasin de données | `fusion_data_list` | Lire | Lit les enregistrements (clé + données JSON) d’un magasin de données, avec la pagination décalée. |
| Supprimer des enregistrements du magasin de données | `fusion_data_stores_data_delete` | Write | Supprime plusieurs enregistrements par clé, ou tous les enregistrements avec des exclusions facultatives. |
| Supprimer l’enregistrement du magasin de données | `fusion_data_stores_data_key_delete` | Write | Supprime un enregistrement par clé. Y parvient même si la clé n’existe pas. |
| Rechercher des magasins de données dépendants | `fusion_datastores_dependents` | Lire | Recherche les magasins de données qui utilisent une structure de données donnée. |
| Rechercher des structures de données | `fusion_data_structures_search` | Lire | Répertorie les structures de données. Filtrez par `name`, `strict`, `teamId`. |
| Obtenir la structure des données | `fusion_data_structures_get` | Lire | Renvoie une structure de données, y compris sa spécification de champ complète. |
| Supprimer la structure de données | `fusion_data_structures_delete` | Write | Supprime une structure de données. Échoue si un magasin de données l’utilise toujours. |

Exemples d’invites :

* _Quelles banques de données sont saturées à plus de 80 % ?_
* _Afficher les 20 premiers enregistrements dans le magasin de données « Carte client »._

## Outils du journal d’activité

| Outil | Nom | Action | Description |
| --- | --- | --- | --- |
| Liste des logs d’activité | `fusion_activity_logs_list` | Lire | Répertorie les événements d’audit de l’organisation (qui a fait quoi, à quelle entité, quand). Filtrez par `entity` (par exemple `scenario`, `connection`, `webhook`, `data store`, `user`), `action` (par exemple `created`, `deleted`, `updated`, `transferred ownership`), utilisateur, équipe et date et heure. |
| Exporter les journaux d’activité | `fusion_activity_logs_export` | Lire | Exporte les logs d’activité au format CSV ou XLSX, avec les mêmes filtres. |

Exemples d’invites :

* _Qui a supprimé les scénarios au cours des 7 derniers jours ?_
* _Exporter toutes les modifications de connexion de ce trimestre vers Excel._

## Commentaires

| Outil | Nom | Action | Description |
| --- | --- | --- | --- |
| Envoyer des commentaires | `fusion_feedback_submit` | Write | Envoie vos commentaires (bug, résultat incorrect, demande de fonctionnalité, éloge ou autre) à l’équipe Fusion. |

## Collègue

Tous les outils de cet article sont disponibles dans Coworker, à la fois en mode autonome et dans le rail de droite de Fusion, sous réserve des mêmes paramètres de lecture/écriture et de vos autorisations.

## Mise à jour des outils

Lorsqu’Adobe publie une nouvelle version du serveur MCP Fusion, les agents connectés récupèrent automatiquement l’ensemble d’outils mis à jour. Vous n&#39;avez pas besoin de vous reconnecter.


