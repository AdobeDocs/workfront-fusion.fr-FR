---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: 'Activité Version de Workfront Fusion : semaine du 3 mai 2021'
description: Cette page décrit toutes les améliorations apportées à Adobe Workfront Fusion durant la semaine du 3 mai 2021.
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
exl-id: 8858fc79-5eda-4938-9bb5-c05be38f02bc
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 100%

---

# Activité Version de Workfront Fusion : semaine du 3 mai 2021

Cette page décrit toutes les améliorations apportées à Adobe Workfront Fusion durant la semaine du 3 mai 2021.

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
