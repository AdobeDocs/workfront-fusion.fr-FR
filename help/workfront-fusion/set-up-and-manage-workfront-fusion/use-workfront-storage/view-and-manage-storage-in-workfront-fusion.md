---
title: Affichage et gestion du stockage dans Workfront Fusion
description: La zone de stockage répertorie les référentiels disponibles et vous permet de parcourir les dossiers et fichiers.
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: a2632cb3184cd555555136288e78ab1e05e4ea9d
workflow-type: tm+mt
source-wordcount: 330
ht-degree: 1%

---

# Affichage et gestion du stockage dans Workfront Fusion

La zone de stockage de Workfront Fusion vous permet d’afficher les référentiels de votre espace de stockage dans le cloud Adobe et d’interagir avec eux.

Pour une présentation du stockage, voir [Présentation du stockage](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/storage-overview.md).

>[!TIP]
>
>Le stockage doit être initialisé avant de pouvoir afficher les référentiels. Pour obtenir des instructions, voir [Initialiser le stockage](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/initialize-storage.md).

## Affichage des référentiels, des dossiers et des fichiers

1. Dans Workfront Fusion, cliquez sur **Stockage** dans le volet de navigation de gauche.
Une liste de référentiels s’ouvre.

   Si un seul référentiel est disponible, le référentiel s’ouvre directement.

1. Cliquez sur **Ouvrir** sur n’importe quel référentiel pour parcourir son contenu.

   L’ouverture d’un référentiel affiche des dossiers dans le référentiel.
1. Cliquez sur un dossier pour l’ouvrir et afficher ses fichiers.
1. Pour revenir à la structure de dossiers précédente, cliquez sur les chemins de navigation.


>[!NOTE]
>
>Un dossier vide affiche le message suivant : *« Ce dossier est vide »*

## Gestion de plusieurs connexions de stockage

Une équipe peut avoir plusieurs connexions de stockage Adobe.

1. Dans Workfront Fusion, cliquez sur **Stockage** dans le volet de navigation de gauche.
Lorsqu’il existe plusieurs connexions, des onglets s’affichent en haut de la page Stockage, étiquetés avec le nom de chaque connexion.
1. Pour passer aux référentiels d’une autre connexion, cliquez sur l’onglet correspondant.

Si une connexion devient non valide, par exemple si son jeton a expiré et n’a pas pu être actualisé, elle est automatiquement filtrée et n’apparaît pas sous la forme d’un onglet. L’actualisation planifiée du jeton de Fusion maintient les connexions valides automatiquement.

## Informations sur le fichier

Chaque fichier du tableau affiche :

| Colonne | Description |
| -------- | ------------- |
| **Nom** | Nom de fichier avec une icône de document. |
| **Type** | Badge d’extension de fichier, tel que PNG, PDF ou JPG. |
| **Taille** | Taille du fichier. Indique *« Traitement... »* si le fichier a été récemment chargé et que le serveur principal le traite toujours. |
| **Créé** | Date de création. |

Les fichiers affichent également un **badge de version** (par exemple, `v2`, `v3`) lorsqu’il existe plusieurs versions.

## Contrôles de table

* **Rechercher/filtrer** : filtrez les fichiers par nom à l’aide de la barre de recherche globale.
* **Tri** : cliquez sur les en-têtes de colonne pour trier.
* **Pagination** : sélectionnez 10, 25, 50 ou 100 éléments par page. La valeur par défaut est 25.
