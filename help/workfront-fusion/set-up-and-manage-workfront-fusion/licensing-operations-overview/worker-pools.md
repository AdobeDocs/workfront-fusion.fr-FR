---
title: Pools de salariés
description: Un pool de travail est une quantité de ressources de traitement Workfront Fusion dédiées à une ou plusieurs organisations spécifiques. Toutes les opérations et tous les traitements Fusion s’effectuent dans le contexte du pool de programmes de travail affecté d’une organisation.
author: Becky
feature: Workfront Fusion
source-git-commit: bb94083eb9f58dc3ae9f94a59288da43317b567b
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# Pools de salariés

Un pool de travail est une quantité de ressources de traitement Workfront Fusion dédiées à une organisation spécifique. Toutes les opérations et tous les traitements Fusion s’effectuent dans le contexte du pool de programmes de travail affecté d’une organisation.

Les pools de salariés permettent à vos scénarios de fonctionner plus efficacement et éliminent les risques de rivaliser avec d&#39;autres organisations pour la capacité de traitement de Fusion.

## Présentation du pool de salariés

Un pool de travail permet de traiter les exécutions de scénario en parallèle. Chaque pool de travail est associé aux éléments suivants :

* Un certain nombre de travailleurs.
* Une file d’attente d’exécution.

Lorsqu’un scénario est exécuté, il est transmis dans la file d’attente d’exécution du pool de traitement. Les intervenants du pool extraient en permanence des tâches du pool d’exécution et les traitent en parallèle.

Si la profondeur de la file d’attente d’exécution augmente et que tous les programmes de travail existants sont utilisés, Workfront Fusion met automatiquement à l’échelle le pool en ajoutant d’autres programmes de travail. Cette évolutivité est dynamique et dépendante des événements, ce qui signifie que la capacité est exacte ou que les contrats sont basés sur une charge en temps réel sans que votre entreprise ou vous-même n’interveniez.

L’équipe de Workfront Fusion surveille en permanence l’utilisation et le comportement d’évolutivité des pools et peut examiner les seuils ou les modèles afin d’assurer des performances cohérentes au fur et à mesure de l’utilisation.
