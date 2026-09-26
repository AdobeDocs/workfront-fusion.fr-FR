---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: 'Activité Version de Workfront Fusion : semaine du 3 mai 2021'
description: Cette page décrit toutes les améliorations apportées à Adobe Workfront Fusion au cours de la semaine du mardi 3 mai 2021.
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 8858fc79-5eda-4938-9bb5-c05be38f02bc
TQID: 'https://experienceleague.adobe.com/GZ5W-9Q1Y9M-cCVN1CupZVs8GuQPy4Dusifz-5sxJm8'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
    internal-label: Integrations
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
  - id: d968a1bc-9a90-4926-a531-bcf272c32aad
    internal-label: Administration
subfeature_v2:
  - id: a29813d3-f0cc-4b60-9396-13b558370803
    internal-label: Product announcements
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
source-git-commit: 01689332f97c15b317e686d11a27cb4dc7e2e8bd
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 100%
---
# Activité Version de Workfront Fusion : semaine du 3 mai 2021

Cette page décrit toutes les améliorations apportées à Adobe Workfront Fusion au cours de la semaine du mardi 3 mai 2021.

Pour obtenir la liste de toutes les modifications récentes, voir [Activité de publication d’Adobe Workfront Fusion](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

Pour obtenir la liste des correctifs récents dans Workfront Fusion, reportez-vous à la page [Mises à jour de maintenance Workfront](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html?lang=fr) et recherchez toutes les mises à jour intitulées Mise à jour de maintenance de Workfront Fusion.

## Le connecteur Salesforce peut désormais effectuer des recherches à l’aide de SOQL.

Le module Salesforce > Recherche d’enregistrements a désormais la possibilité d’effectuer une recherche à l’aide de SOQL (Salesforce Object Query Language). Vous pouvez également effectuer des recherches à l’aide des options disponibles précédemment (recherches SOSL et simples).

## Le nouveau type de connexion dans le connecteur Azure DevOps nécessite moins de portées.

Pour améliorer la sécurité, nous avons ajouté un nouveau type de connecteur au connecteur Azure DevOps Workfront Fusion. Désormais, lorsque vous créez une connexion dans un module Azure DevOps, vous pouvez choisir entre deux types de connexions :

* Azure DevOps

  Ce nouveau type de connexion limite les portées à celles spécifiquement nécessaires à Workfront Fusion.

* Azure DevOps (demander toutes les portées)

  Il s’agit du type de connexion hérité, qui demande toutes les portées disponibles lors d’une connexion à Azure DevOps.

Nous vous recommandons d’utiliser le type de connexion Azure DevOps dans tous vos nouveaux scénarios qui utilisent Azure DevOps. Nous vous recommandons également de modifier les modules Azure DevOps dans vos scénarios existants afin d’utiliser le nouveau type de connexion. Le type de connexion Azure DevOps (Demander toutes les portées) hérité sera bientôt obsolète.
