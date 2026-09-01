---
title: Création de scénarios à partir du stockage
description: Storage s’intègre au créateur de scénarios de Fusion. Vous pouvez donc créer des scénarios préconfigurés directement à partir de la page Storage pour télécharger ou télécharger des fichiers.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: aef1685cb25c0cdcb0dcdf9b0c73fb482d392e5f
workflow-type: tm+mt
source-wordcount: 272
ht-degree: 0%

---

# Création de scénarios à partir du stockage

Pour une présentation du stockage, voir [Présentation du stockage](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/storage-overview.md).

Le stockage s’intègre au créateur de scénarios de Fusion. Sur la page Stockage , les utilisateurs peuvent créer un scénario qui téléchargera le fichier sélectionné.

## Télécharger dans le scénario

1. Dans Workfront Fusion, cliquez sur **Stockage** dans le volet de navigation de gauche.
1. Accédez au référentiel contenant le fichier à télécharger dans un scénario.
1. Sélectionnez un fichier, puis cliquez sur **« Télécharger dans le scénario »** dans la barre d’actions.

Fusion crée ensuite un nouveau scénario nommé **« Télécharger le {fileName} »**. Ce scénario s’ouvre dans un onglet de navigateur distinct.

Le scénario est préconfiguré avec :

* Connexion active.
* Référentiel, dossier et fichier présélectionnés.
* Module permettant de générer une URL de téléchargement prédéfinie.
* Un module HTTP pour récupérer le fichier à partir de cette URL.
* Intervalle de planification par défaut de 15 minutes.

## Charger le fichier dans le scénario

1. Dans Workfront Fusion, cliquez sur **Stockage** dans le volet de navigation de gauche.
1. Accédez au référentiel et au dossier contenant le fichier à télécharger dans un scénario.
1. Lorsque vous naviguez à l’intérieur d’un dossier, cliquez sur le menu déroulant **Charger le fichier »**
1. Sélectionnez **« Charger le fichier dans le scénario »**.

Fusion crée ensuite un scénario nommé **Chargement vers {folderName} »**. Ce scénario s’ouvre dans un nouvel onglet du navigateur. Vous devez ajouter des modules pour fournir le fichier que vous souhaitez charger, tels que le module Workfront > Télécharger le document .

Le scénario est préconfiguré avec :

* Connexion active.
* Le référentiel et le dossier sont présélectionnés.
* Module permettant de générer une URL de chargement prédéfinie avec un nom de fichier d’espace réservé.
* Intervalle de planification par défaut de 15 minutes.

