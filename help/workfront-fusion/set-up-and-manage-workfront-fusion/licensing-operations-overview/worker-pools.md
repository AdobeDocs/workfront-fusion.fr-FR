---
title: Pools de salariés
description: Un pool de travail est une quantité de ressources de traitement Workfront Fusion dédiées à une ou plusieurs organisations spécifiques. Toutes les opérations et tous les traitements Fusion s’effectuent dans le contexte du pool de programmes de travail affecté d’une organisation.
author: Becky
feature: Workfront Fusion
exl-id: 8bf508a8-d1f9-455f-af89-62f688289137
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: b800142d824927e5765eed50a831731e6b5d9925
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 19%
---
# Pools de salariés

Un pool de travail est une quantité de ressources de traitement Workfront Fusion dédiées à une organisation spécifique. Toutes les opérations et tous les traitements Fusion s’effectuent dans le contexte du pool de programmes de travail affecté d’une organisation.

Les pools de salariés permettent à vos scénarios de fonctionner plus efficacement et éliminent les risques de rivaliser avec d&#39;autres organisations pour la capacité de traitement de Fusion.

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

## Présentation du pool de salariés

Un pool de travail permet de traiter les exécutions de scénario en parallèle. Chaque pool de travail est associé aux éléments suivants :

* Un certain nombre de travailleurs.
* Une file d’attente d’exécution.

Lorsqu’un scénario est exécuté, il est transmis dans la file d’attente d’exécution du pool de traitement. Les intervenants du pool extraient en permanence des tâches du pool d’exécution et les traitent en parallèle.

Si la profondeur de la file d’attente d’exécution augmente et que tous les programmes de travail existants sont utilisés, Workfront Fusion met automatiquement à l’échelle le pool en ajoutant d’autres programmes de travail. Cette évolutivité est dynamique et dépendante des événements, ce qui signifie que la capacité est exacte ou que les contrats sont basés sur une charge en temps réel sans que votre entreprise ou vous-même n’interveniez.

L’équipe de Workfront Fusion surveille en permanence l’utilisation et le comportement d’évolutivité des pools et peut examiner les seuils ou les modèles afin d’assurer des performances cohérentes au fur et à mesure de l’utilisation.

## Renommer un pool de travail

Les propriétaires et les administrateurs de l’organisation peuvent renommer les pools de collaborateurs affectés à leur organisation. Par défaut, chaque pool affiche un nom généré par le système. Vous pouvez donner à un pool un nom personnalisé, tel que `Marketing EU` ou `High-volume integrations`, et le modifier si nécessaire.

Le changement de nom d’un pool modifie uniquement son libellé. Les scénarios, les exécutions et la capacité du pool ne sont pas affectés. Le nouveau nom s’affiche là où le pool est visible, par exemple lorsque vous attribuez des scénarios à un pool.

>[!NOTE]
>
>L’onglet **[!UICONTROL Pools de programmes de travail]** s’affiche uniquement lorsque plusieurs pools de programmes de travail sont affectés à votre organisation. Si votre organisation dispose d’un seul pool de travail ou utilise le pool partagé, l’onglet n’apparaît pas.

Pour renommer un pool de traitement :

1. Dans le volet de navigation de gauche, cliquez sur **Présentation de l’organisation**
1. Cliquez sur l&#39;onglet **[!UICONTROL Pools de salariés]**, en haut de la page.

   L’onglet répertorie chaque pool et indique le nombre de scénarios qui lui sont affectés.

1. Cliquez sur **[!UICONTROL Renommer]** en regard du pool à renommer.
1. Dans le panneau qui s’ouvre, saisissez le nouveau nom.
1. Cliquer sur **Enregistrer**.
