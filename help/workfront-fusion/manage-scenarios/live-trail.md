---
title: Utilisation du Live Trail pour passer en revue l’exécution d’un scénario
description: Le journal en direct présente l’exécution d’un scénario, combinant des requêtes de module et une activité d’exécution dans une seule liste. Vous pouvez ouvrir les détails de la requête et de la réponse pour n’importe quelle opération.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
source-git-commit: 94449f8511d7480f1a4fc0ac6e8db9b067977abd
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 17%
---

# Utilisation du Live Trail pour passer en revue l’exécution d’un scénario

Le journal en direct présente l’exécution d’un scénario. Il combine les requêtes de module et l’activité d’exécution dans une seule liste chronologique. Vous pouvez ainsi suivre une exécution dans l’éditeur de scénarios et voir ce qui s’est passé sans quitter la zone de travail.

>[!NOTE]
>
>Cette fonctionnalité n’est disponible que dans la nouvelle expérience de l’éditeur de scénarios. Pour plus d’informations, voir [Expériences nouvelles et classiques](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences) dans l’éditeur de scénarios d’article.

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tout package de workflow Adobe Workfront et tout package d’automatisation et d’intégration Adobe Workfront</p><p>Workfront Ultimate</p><p>Packages Workfront Prime et Select, avec l’achat supplémentaire de Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licences Adobe Workfront</td> 
   <td> <p>Standard</p><p>Travail ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Si votre organisation dispose d’un package Workfront Select ou Prime qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acquérir Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation Workfront](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Ouvrir le journal en direct

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Sélectionnez le scénario que vous souhaitez examiner.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Lancez l’exécution du scénario, par exemple en cliquant sur **Exécuter une fois**.



Le Live Trail s’ouvre dans le panneau sur le côté droit de la zone de travail. Si vous fermez le panneau au cours d’une exécution, un petit onglet situé à droite de l’écran vous permet de l’ouvrir à nouveau sans perdre les événements qui ont été capturés.

## Événements de révision dans le Live Trail

Le journal en direct répertorie les requêtes de module et l’activité d’exécution dans l’ordre dans lequel elles se produisent. Vous pouvez :

* Effectuez une recherche dans la liste.
* Filtrer la liste par statut.
* Suivez l’événement le plus récent au fur et à mesure de l’exécution.
* Effacer la trace actuelle.

## Affichage des détails de la requête et de la réponse

1. Dans le Live Trail, cliquez sur la demande pour laquelle vous souhaitez afficher les détails.

   Le module qui a émis la requête est révélé sur la zone de travail, et les détails de la requête et de la réponse s’ouvrent dans le panneau.

1. Consultez les détails. La vue détaillée comprend :

   * Navigation entre les opérations du module
   * En-têtes et corps de requête
   * En-têtes et corps de réponse

1. (Facultatif) Copiez les détails pour les utiliser ailleurs en cliquant sur **Copier brut** ou **Copier cURL** :

   * Copiez un rapport brut de la requête et de la réponse.
   * Copiez une commande cURL pour la requête.

1. Pour revenir à la liste, cliquez sur la flèche vers l’arrière dans le coin supérieur gauche du panneau.

## Vérifiez que les détails de la requête et de la réponse sont disponibles

Les détails des requêtes et des réponses ne sont pas conservés pour chaque exécution planifiée ou déclenchée, car ils nécessitent un stockage important.

* L’option Exécuter une fois conserve toujours les détails de la requête et de la réponse.
* Pour les exécutions régulières d’un scénario, activez les journaux de débogage temporaires dans les paramètres du scénario avant les exécutions que vous souhaitez inspecter. Pour plus d’informations, voir [Journaux de débogage temporaires](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#temporary-debug-logs) dans l’article Configuration des paramètres de scénario.

Si vous ouvrez une exécution à partir de l’historique d’exécution et que le panneau requête et réponse ne contient aucune donnée, le panneau vous dirige vers le paramètre Journaux de débogage temporaires .
