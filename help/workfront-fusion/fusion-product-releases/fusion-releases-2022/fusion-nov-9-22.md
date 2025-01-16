---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: 'Activité Version de Workfront Fusion : semaine du 7 novembre 2022'
description: Cette page décrit toutes les améliorations apportées à Adobe Workfront Fusion durant la semaine du 7 novembre 2022.
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
exl-id: 9d58abd0-1fe7-43c8-a1ea-2fadea738590
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 100%

---

# Activité Version de Workfront Fusion : semaine du 7 novembre 2022

**Optimisation de la file d’attente de webhooks**

La file d’attente des webhooks de Fusion a été optimisée avec cette version. Le service qui accepte les webhooks est désormais distinct de la file d’attente et des autres processus. Cette modification permet à Fusion de traiter les files d’attente des webhooks à un rythme plus rapide et plus cohérent.

Au cours de la mise en œuvre de cette modification, nous avons pu mieux comprendre le temps de traitement des enregistrements attendu pour les événements webhook en file d’attente. La page de la visionneuse de webhook de Fusion ne devrait pas dépasser 1 minute d’ancienneté.

Pour afficher les événements webhook actuellement en file d’attente, accédez à Webhooks, dans le volet de navigation de gauche. Les icônes de camion comportant un nombre dans le numérateur indiquent les événements dans la file d’attente pour ce webhook. Cliquez sur l’icône de camion pour afficher les événements placés dans la file d’attente.


**Les webhooks inutilisés seront désormais désactivés ou supprimés.**

Nous avons apporté quelques modifications à la façon dont Workfront Fusion gère les webhooks inutilisés. Désormais, les webhooks sont désactivés automatiquement si l’une des conditions suivantes s’applique :

* Le webhook n’est connecté à aucun scénario depuis plus de 5 jours.
* Le webhook est utilisé uniquement dans les scénarios inactifs, qui sont inactifs depuis plus de 30 jours.

Les webhooks désactivés sont supprimés et désinscrits automatiquement s’ils ne sont connectés à aucun scénario et s’ils sont restés désactivés pendant plus de 30 jours.
