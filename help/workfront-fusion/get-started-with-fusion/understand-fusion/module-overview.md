---
title: Présentation du module
description: 'Adobe Workfront Fusion distingue cinq types de modules : modules d’action, modules de recherche, modules de déclenchement, agrégateurs et itérateurs. Les agrégateurs et les itérateurs sont destinés à des scénarios avancés.'
author: Becky
feature: Workfront Fusion
exl-id: 4c8fe028-8425-426d-a006-f0c66871b3cd
source-git-commit: 190bfe5992fb21b789a7246c4ae732a5dc7672fa
workflow-type: tm+mt
source-wordcount: '878'
ht-degree: 22%

---

# Présentation du module

Adobe Workfront Fusion distingue cinq types de modules :

* Modules d’action
* Modules de recherche
* Modules déclencheurs
* Agrégateurs
* Itérateurs

Les agrégateurs et les itérateurs sont destinés à des scénarios avancés.

## Modules d’action

Les modules d’action sont le type de module le plus courant. Un module d’action type effectue une action et renvoie un lot unique, qui est ensuite transmis au module suivant pour traitement.

Contrairement aux modules de déclenchement, les modules d’action peuvent être placés au début, au milieu ou à la fin d’un scénario.

Les scénarios peuvent contenir un nombre illimité de modules d’action, bien qu’un grand nombre de modules (150+) puisse affecter les performances.

>[!BEGINSHADEBOX]

**Exemples :**

* **[!DNL Workfront]>[!UICONTROL Upload a file]** envoie un fichier à [!DNL Workfront] et retourne son identifiant.
* **[!UICONTROL Image]>[!UICONTROL Resize]** reçoit une image, la redimensionne à des dimensions spécifiées et la transmet à l’action suivante.

>[!ENDSHADEBOX]

Le type Action comporte quatre sous-types :

* Créer
* Lecture
* Mettre à jour
* Supprimer

Le sous-type Mise à jour comprend les trois opérations suivantes :

* **Effacer le contenu d’un champ**. Cette opération a lieu lorsque le contenu du champ est évalué sur le mot-clé `erase` (à ne pas confondre avec `empty`).

  ![Supprimer le mot-clé](assets/erase-content-of-field.png)

* **Ne pas modifier le contenu d’un champ**. Cette opération se produit lorsque le champ est vide ou que le contenu du champ est évalué sur vide (représenté par une valeur nulle dans JSON).

  ![Lot vide](assets/leave-content-field-unchanged.png)

* **Remplacer le contenu d’un champ**. Cette opération a lieu dans tous les autres cas que les deux décrits ci-dessus.

>[!NOTE]
>
>* Si vous ne voyez pas le mot-clé `erase` dans le panneau de mappage, le module n’est pas un module de mise à jour ou il n’a pas été mis à jour selon les dernières spécifications de l’application.
>* `Empty` ne modifie pas le contenu du champ. S’il est nécessaire d’effacer le champ, vous pouvez utiliser la formule suivante :
>
>   ![Si vide](assets/formula-ifempty-name-erase.png)
>
>* Le fait de laisser un champ inchangé lorsque son contenu est évalué comme vide n’est actuellement pas pris en charge.

## Modules de recherche

Les modules de recherche renvoient zéro, un ou plusieurs lots, qui sont ensuite transmis au module suivant pour traitement.

Vous pouvez placer des modules de recherche au début, au milieu ou à la fin d’un scénario.

Les scénarios peuvent contenir un nombre illimité de modules de recherche, bien qu’un grand nombre de modules (150+) puisse affecter les performances.

>[!BEGINSHADEBOX]

**Exemple :**

**[!DNL Workfront]>[!UICONTROL Read Related Records]** lit les enregistrements correspondant à la requête de recherche que vous spécifiez, dans un objet parent particulier.

>[!ENDSHADEBOX]

## Modules déclencheurs

Les Triggers génèrent des lots lorsqu’il y a eu une modification dans un service donné, comme la création ou la mise à jour d’un enregistrement.

Les déclencheurs renvoient zéro, un ou plusieurs lots, qui sont ensuite transmis au module suivant pour traitement.

Étant donné que les Triggers entraînent le début de l’exécution des scénarios, ils ne peuvent être placés qu’au début d’un scénario.

Chaque scénario ne peut contenir qu’un seul déclencheur.

[!DNL Workfront Fusion] utilise deux types de déclencheurs : les déclencheurs d’interrogation et les déclencheurs instantanés.

### Déclencheurs d’attente active

Les déclencheurs d’interrogation interrogent régulièrement un service donné même s’il n’y a eu aucune modification depuis l’exécution du scénario précédent. Nous vous recommandons de planifier l’exécution d’un scénario contenant un déclencheur d’attente active à intervalles réguliers. Si une modification correspond à la configuration du déclencheur, celui-ci renvoie des lots contenant des informations sur la modification. Si aucune modification ne correspond à la configuration, le déclencheur ne génère aucun lot.

Pour obtenir des instructions sur la planification d’un scénario, voir [Planification d’un scénario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

Les déclencheurs d’interrogation vous permettent de sélectionner le premier lot qu’ils doivent générer via un panneau qui s’affiche automatiquement après l’enregistrement d’un déclencheur ou la modification de ses paramètres. Cette sélection n’affecte que la première exécution du module. Une fois le module exécuté une fois, les exécutions suivantes surveillent uniquement les modifications qui se produisent après l’exécution la plus récente.

Pour plus d’informations, voir [Choisir l’emplacement de départ d’un module de déclenchement](/help/workfront-fusion/create-scenarios/add-modules/choose-where-trigger-module-starts.md).

>[!BEGINSHADEBOX]

**Exemples :**

* **[!DNL Workfront]>[!UICONTROL Watch records]** renvoie les enregistrements qui ont été ajoutés après la dernière exécution du scénario.

* **[!DNL Google Sheets]>[!UICONTROL Watch Rows]** renvoie les nouvelles lignes ajoutées après la dernière exécution du scénario.

>[!ENDSHADEBOX]

### Déclencheurs instantanés

Les déclencheurs instantanés permettent à un service d’informer [!DNL Workfront Fusion] d’une modification immédiatement après qu’elle se soit produite. Nous vous recommandons de planifier l’exécution immédiate d’un scénario contenant un déclencheur instantané.

Pour obtenir des instructions, voir [Planification d’un scénario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

Pour plus d’informations sur la manière dont les données entrantes sont traitées par un déclencheur instantané, voir [Déclencheurs instantanés (webhooks)](/help/workfront-fusion/references/modules/webhooks-reference.md).

>[!BEGINSHADEBOX]

**Exemples :**

* **[!DNL Workfront]>[!UICONTROL Watch Events]** renvoie des informations lorsqu’un certain type d’événement se produit dans Workfront, comme la création d’une tâche.
* **[!DNL Google Sheets]>[!UICONTROL Watch Changes]** renvoie des informations lorsqu’une cellule est mise à jour.

>[!ENDSHADEBOX]

## Agrégateurs

Un module Agrégateur accumule plusieurs lots en un seul lot.

Les agrégateurs ne renvoient qu’un seul lot, qui est ensuite transmis au module suivant pour un traitement ultérieur.

Vous ne pouvez placer des agrégateurs qu’au milieu d’un scénario.

Les scénarios peuvent contenir un nombre illimité d’agrégateurs, bien qu’un grand nombre de modules (150+) puisse affecter les performances.

>[!BEGINSHADEBOX]

**Exemples :**

* **[!UICONTROL Archive]>[!UICONTROL Create an archive]** compresse plusieurs fichiers dans une archive zip.
* **[!UICONTROL CSV]>[!UICONTROL Aggregate to CSV]** fusionne plusieurs chaînes d’un fichier CSV en une seule ligne.
* **[!UICONTROL Tools]>[!UICONTROL Text aggregator]** combine plusieurs chaînes en une seule.

>[!ENDSHADEBOX]

Pour plus d’informations, voir [Module d’agrégation](/help/workfront-fusion/references/modules/aggregator-module.md).

## Itérateurs

Un itérateur est un type de module qui divise les tableaux en lots distincts.

Les itérateurs renvoient un ou plusieurs lots, qui sont ensuite transmis au module suivant pour traitement.

Vous ne pouvez placer des itérateurs qu’au milieu d’un scénario.

Les scénarios peuvent contenir un nombre illimité d’itérateurs, bien qu’un grand nombre de modules (150+) puisse affecter les performances.

>[!BEGINSHADEBOX]

**Exemple :**

**[!UICONTROL Email]>[!UICONTROL Retrieve attachments]** divise un tableau de pièces jointes en lots distincts.

>[!ENDSHADEBOX]

Pour plus d’informations, consultez [Module Itérateur](/help/workfront-fusion/references/modules/iterator-module.md) et [Mapper un tableau](/help/workfront-fusion/create-scenarios/map-data/map-an-array.md).
