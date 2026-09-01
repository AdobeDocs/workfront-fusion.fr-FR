---
title: Vue d’ensemble de l’espace de stockage
description: Le stockage est une page de Workfront Fusion qui permet aux équipes d’accéder directement à leurs référentiels Adobe Enterprise Storage Management (ESM). Les utilisateurs peuvent ainsi parcourir les dossiers, charger et télécharger des fichiers, afficher l’historique des versions et créer des scénarios d’automatisation.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: d5568479d43bd5518adae5b66b132b4075e7f356
workflow-type: tm+mt
source-wordcount: 279
ht-degree: 2%

---

# Vue d’ensemble de l’espace de stockage

<!--Add to navigation articles once this goes to production-->

La zone de stockage de Workfront Fusion permet aux équipes d’accéder directement à leurs référentiels de gestion du stockage d’entreprise (ESM) Adobe. Les utilisateurs peuvent parcourir les dossiers, charger et télécharger des fichiers, afficher l’historique des versions et créer des scénarios d’automatisation, le tout sans quitter Fusion.

Le stockage appartient aux équipes et nécessite l’intégration de l’organisation au système Adobe Identity Management (IMS) avec un accès au stockage Adobe.

Les fichiers de Fusion Storage sont mis en miroir dans les fichiers Adobe (adobe.com/files). De ce fait, tous les fichiers accessibles dans les fichiers Adobe sont accessibles dans Fusion Storage.

Pour obtenir des instructions sur l&#39;utilisation du stockage, voir :

* [Initialiser le stockage](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/initialize-storage.md)
* [Affichage et gestion du stockage dans Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/view-and-manage-storage-in-workfront-fusion.md)
* [Charger les fichiers vers le stockage](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/upload-files-to-storage.md)
* [Télécharger des fichiers depuis le stockage](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/download-files-from-storage.md)
* [Supprimer des fichiers du stockage](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/delete-files-from-storage.md)
* [Affichage de l’historique des versions de fichiers dans le stockage](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/view-storage-file-version-history.md)
* [Création de scénarios à partir du stockage](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/create-scenarios-from-storage.md)

## Conditions préalables de stockage

Pour utiliser la zone de stockage Workfront Fusion, les informations suivantes doivent être vraies :

* L’organisation a intégré **Adobe Identity Management System (IMS)**
* L’organisation dispose de **Stockage**
* L’utilisateur est connecté à l’**organisation Adobe IMS appropriée** (celle correspondant à l’organisation Fusion sélectionnée).
* Le compte de l’utilisateur a **accès au stockage Adobe**

## Glossaire

Lors de l’utilisation de

| Terme | Définition |
| ------ | ----------- |
| **référentiel** | Conteneur de stockage de niveau supérieur dans Adobe ESM, généralement mappé à un projet ou un espace de travail |
| **Connexion** | Lien sécurisé entre Fusion et le stockage Adobe, créé automatiquement lors de l’initialisation. Utilise l’authentification Adobe IMS avec actualisation automatique du jeton |
| **ESM** | Gestion du stockage d’entreprise, service de stockage de fichiers dans le cloud Adobe |
| **IMS** | Système Adobe Identity Management, plateforme d&#39;authentification et d&#39;identité Adobe |

<!--

## UI Reference — Key Screens

### 1. Initialization Screen

* Cloud icon with **"Adobe Storage"** heading
* Description text explaining the feature
* **"Initialize Storage"** button (primary action)
* Error variants for access restriction, org mismatch, access denied, no storage found

### 2. Repository List

* Table with **Name** and **Region** columns
* **"Open"** action button per row

### 3. File Browser

* Breadcrumb navigation bar
* **"Upload File"** dropdown button (with "Upload File" and "Upload File in Scenario" options)
* File/folder table with **Name**, **Type**, **Size**, **Created** columns
* Floating action bar on file selection with: **Download**, **Download in Scenario**, **Versions**, **Delete**
* Upload/download progress banners (top-right corner)

### 4. Version History Panel

* Right-side slide-out panel
* Version list with date, version badge, and download button per entry
* **"current"** label on the latest version

-->
