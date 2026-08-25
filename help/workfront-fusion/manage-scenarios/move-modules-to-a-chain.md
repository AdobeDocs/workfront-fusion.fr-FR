---
title: Déplacer des modules vers une chaîne
description: Vous pouvez sélectionner un groupe de modules dans un scénario et les déplacer dans un nouveau scénario chaîné, sans recréer manuellement les mappages ou les structures de données.
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: f1a80f64edc410ae76bfbba1280df7232e2d09c5
workflow-type: tm+mt
source-wordcount: 513
ht-degree: 17%

---

# Déplacer des modules vers une chaîne

>[!IMPORTANT]
>
>Cette fonctionnalité est disponible dans Beta et n’est pas recommandée pour les workflows de production critiques. En tant que fonctionnalité Beta, le comportement peut changer et les cas Edge peuvent ne pas être entièrement gérés.

Vous pouvez sélectionner un groupe de modules dans un scénario et les déplacer dans un nouveau scénario chaîné, sans recréer manuellement les mappages ou les structures de données. Cela permet de modulariser facilement des scénarios volumineux.

Lorsque vous déplacez un groupe de modules dans une chaîne, Workfront Fusion :

* Déplace les modules sélectionnés vers un nouveau scénario.
* Ouvre le nouveau scénario dans une fenêtre de navigateur distincte.
* Remplace les modules sélectionnés dans le scénario d’origine par un module Chaîne > Appeler un scénario enfant .
* Crée automatiquement les structures de données d’entrée et de sortie requises pour le nouveau scénario enfant.
* Préserve le comportement existant du scénario, de sorte que ce dernier continue de s’exécuter de la même manière qu’avant le déplacement des modules.
* Met automatiquement à jour les mappages :
  * Les modules déplacés dans le scénario enfant reçoivent des données par le biais de l’option Chaîne > Recevoir des données à partir des entrées du module parent.
  * Les sorties du scénario enfant sont automatiquement exposées au scénario parent.
  * Les mappages existants dans le plan directeur sont ajustés pour correspondre à la nouvelle structure.

Pour plus d&#39;informations sur la planification des scénarios chaînés, voir [Enchaîner plusieurs scénarios](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md).

Pour obtenir des instructions sur la configuration des modules Chain, voir [Modules Chain](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md).

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
   <p>Si votre organisation dispose d’un package Workfront Select ou Prime qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acquérir Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Conditions préalables

Les modules que vous souhaitez déplacer dans une chaîne doivent déjà exister dans un scénario et vous devez sélectionner plusieurs modules.

## Limites

Vous ne pouvez pas déplacer une sélection de modules dans une chaîne dans les cas suivants :

* Les modules sélectionnés ne font pas partie d’un seul flux ininterrompu. Par exemple, vous ne pouvez pas sélectionner en même temps des modules provenant de deux itinéraires différents et non connectés.
* La sélection comprend un module webhook.
* La sélection inclut un autre module de chaîne.
* La sélection inclut un module Routeur, et vous n&#39;avez pas sélectionné toutes les routes de ce routeur.
* Un module sélectionné a un itinéraire de gestionnaire d’erreurs, et vous n’avez pas également sélectionné cet itinéraire.

## Déplacement de modules dans une chaîne

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Sélectionnez le scénario contenant les modules à déplacer.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Sélectionnez les modules à déplacer dans une chaîne en maintenant la touche [!UICONTROL Maj] enfoncée et en cliquant sur les modules à déplacer.
1. Cliquez avec le bouton droit sur l’un des modules sélectionnés.
1. Sélectionnez **[!UICONTROL Déplacer vers la chaîne]**.
