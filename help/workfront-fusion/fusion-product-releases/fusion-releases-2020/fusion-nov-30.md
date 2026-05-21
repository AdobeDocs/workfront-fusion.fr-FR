---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
keywords: Fusion
navigation-topic: fusion-release-activity
title: 'Activité Version de Workfront Fusion : semaine du mardi 30 novembre 2020'
description: Cette page décrit toutes les améliorations apportées à Adobe Workfront Fusion au cours de la semaine du mardi 30 novembre 2020.
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 76cc14b3-ffec-4d49-b471-f3eb9dd89658
TQID: https://experienceleague.adobe.com/1y9rppDRn9QYIcG5SJyNfVcyi7eHbGK-NcrF-hWjX-Y
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 207
ht-degree: 89%

---

# Activité Version de Workfront Fusion : semaine du mardi 30 novembre 2020

Cette page décrit toutes les améliorations apportées à Adobe Workfront Fusion au cours de la semaine du mardi 30 novembre 2020.

Pour obtenir la liste de toutes les modifications récentes, voir [Activité de publication d’Adobe Workfront Fusion](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

Pour obtenir la liste des correctifs récents dans Workfront Fusion, reportez-vous à la page [Mises à jour de maintenance Workfront](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html) et recherchez toutes les mises à jour intitulées Mise à jour de maintenance de Workfront Fusion.

## Limite de taux pour les webhooks Workfront Fusion 2.0.

Nous avons introduit un nouveau mécanisme de sécurisation des performances pour Workfront Fusion 2.0. Désormais, les webhooks sont limités à 100 requêtes par seconde. Lorsque cette limite est atteinte, Workfront Fusion 2.0 envoie un statut 429 (Too many requests).

Auparavant, les demandes webhook n’étaient pas limitées.


## Ajouter un formulaire personnalisé à un objet Workfront dans Workfront Fusion 2.0

Pour que vous puissiez ajouter des formulaires personnalisés à des objets dans Workfront Fusion 2.0, nous avons ajouté une action AssignCategories à Workfront > Divers. Module d’action.

Auparavant, il n’était pas possible d’utiliser un module Workfront Fusion 2.0 pour ajouter un formulaire personnalisé à un objet dans Workfront.
