---
title: 'Activité Version de Workfront Fusion : semaine du 30 août 2021'
description: 'Activité Version de Workfront Fusion : semaine du 30 août 2021'
author: Luke
draft: Probably
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
exl-id: cac11147-5b3d-477b-869b-e255528c4bec
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 100%

---

# Activité Version de Workfront Fusion : semaine du 30 août 2021

Cette page décrit toutes les améliorations apportées à Adobe Workfront Fusion durant la semaine du 30 août 2021.

Pour obtenir la liste de toutes les modifications récentes, voir [Activité de publication d’Adobe Workfront Fusion](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

Pour obtenir la liste des correctifs récents dans Workfront Fusion, reportez-vous à la page [Mises à jour de maintenance Workfront](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html) et recherchez toutes les mises à jour intitulées Mise à jour de maintenance de Workfront Fusion.

## Filtrer les événements qui déclenchent le module Workfront > Surveiller les événements.

1. Configurer un filtre personnalisé pour les événements qui déclenchent le module Workfront > Surveiller les événements.

   Pour réduire le nombre d’exécutions de scénarios inutiles, nous avons mis à jour le module Workfront > Surveiller les enregistrements afin d’activer le filtrage des événements. Vous pouvez maintenant définir un filtre lors de la création d’un webhook. Cela permet au scénario de se déclencher uniquement lorsque l’événement remplit certains critères.

   Le filtre d’événement propose actuellement les opérations suivantes :

   * Égal à : déclenche un scénario uniquement si un événement correspond aux conditions du filtre. Par exemple, vous pouvez configurer un filtre qui déclenche un scénario uniquement si l’événement se produit dans un projet spécifique.
   * Non égal à : déclenche un scénario uniquement si un événement ne correspond pas aux conditions du filtre. Par exemple, vous pouvez créer un filtre qui déclenche un scénario uniquement si le problème qui se produit n’a pas le statut Fermé.

   Auparavant, le module Surveiller des enregistrements récupérait tous les enregistrements. Les utilisateurs et utilisatrices peuvent filtrer uniquement en configurant des filtres ultérieurement dans le scénario.

   Pour tirer parti du filtrage des événements, créez un webhook dans votre module Surveiller les événements. Il n’est actuellement pas possible de modifier les webhooks existants pour inclure cette fonctionnalité. Nous vous recommandons vivement de créer des webhooks à l’aide de filtres d’événement pour vos scénarios existants.

1. Filtrez les événements déclenchés par la connexion actuelle.

   Pour faciliter la configuration de vos webhooks pour le module Workfront > Surveiller les événements, nous avons inclus le filtre d’événement le plus courant. Désormais, le webhook dispose d’une option pour filtrer toute modification apportée par les modules à l’aide de la connexion spécifiée pour le module Surveiller les événements. En d’autres termes, avec ce filtre activé, les modifications effectuées par la personne Workfront associée à cette connexion ne peuvent pas déclencher le scénario.

   Auparavant, ce filtre n’était pas disponible. Par conséquent, les modifications apportées aux modules Workfront pouvaient déclencher des scénarios contenant ces modules plus facilement, ce qui pouvait entraîner le déclenchement de scénarios dans une boucle infinie.
