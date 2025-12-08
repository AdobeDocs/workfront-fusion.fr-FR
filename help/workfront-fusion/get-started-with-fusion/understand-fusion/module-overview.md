---
title: Vue d’ensemble des modules
description: 'Adobe Workfront Fusion distingue cinq types de modules : modules d’action, modules de recherche, modules déclencheurs, agrégateurs et itérateurs. Les agrégateurs et les itérateurs sont destinés à des scénarios avancés.'
author: Becky
feature: Workfront Fusion
exl-id: 4c8fe028-8425-426d-a006-f0c66871b3cd
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: ht
source-wordcount: '917'
ht-degree: 100%

---

# Vue d’ensemble des modules

Adobe Workfront Fusion distingue cinq types de modules :

* Modules d’action
* Modules de recherche
* Modules déclencheurs
* Agrégateurs
* Itérateurs

Les agrégateurs et les itérateurs sont destinés à des scénarios avancés.

## Modules d’action

Les modules d’action sont le type de module le plus courant. Un module d’action type effectue une action et renvoie un lot unique, qui est ensuite transmis au module suivant pour traitement.

Contrairement aux modules déclencheurs, les modules d’action peuvent être placés au début, au milieu ou à la fin d’un scénario.

Les scénarios peuvent contenir un nombre illimité de modules d’action, bien qu’un grand nombre de modules (plus de 150) puisse affecter les performances.

>[!BEGINSHADEBOX]

**Exemples :**

* **Workfront > [!UICONTROL Charger un fichier]** envoie un fichier à Workfront et renvoie son identifiant.
* **[!UICONTROL Image] > [!UICONTROL Redimensionner]** reçoit une image, la redimensionne selon les dimensions spécifiées et la transmet à l’action suivante.

>[!ENDSHADEBOX]

Le type Action comporte quatre sous-types :

* Créer
* Lire
* Mettre à jour
* Supprimer

Le sous-type Mettre à jour permet les trois opérations suivantes :

* **Effacer le contenu d’un champ**. Cette opération se produit lorsque le contenu du champ est évalué par rapport au mot-clé `erase` (à ne pas confondre avec `empty`).

  ![Mot-clé Effacer](assets/erase-content-of-field.png)

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
>* Laisser un champ inchangé lorsque son contenu est évalué comme vide n’est actuellement pas pris en charge.

## Modules de recherche

Les modules de recherche peuvent renvoyer zéro, un ou plusieurs lots qui sont ensuite transmis au module suivant pour traitement.

Vous pouvez placer les modules de recherche au début, au milieu ou à la fin d’un scénario.

Les scénarios peuvent contenir un nombre illimité de modules de recherche, bien qu’un grand nombre de modules (plus de 150) puisse affecter les performances.

>[!BEGINSHADEBOX]

**Exemple :**

**Workfront > [!UICONTROL Lire les enregistrements associés]** lit les enregistrements qui correspondent à la requête que vous avez spécifiée, dans un objet parent particulier.

>[!ENDSHADEBOX]

## Modules déclencheurs

Les déclencheurs génèrent des lots lorsqu’il y a eu une modification dans un service donné, comme la création ou la mise à jour d’un enregistrement.

Les déclencheurs peuvent renvoyer zéro, un ou plusieurs lots qui sont ensuite transmis au module suivant pour traitement.

Étant donné que les déclencheurs entraînent le début de l’exécution des scénarios, ils ne peuvent être placés qu’au début d’un scénario.

Chaque scénario ne peut contenir qu’un seul déclencheur.

Workfront Fusion fait la distinction entre deux types de déclencheurs : les déclencheurs d’interrogation et les déclencheurs instantanés.

### Déclencheurs d’interrogation

Les déclencheurs d’interrogation interrogent régulièrement un service donné, même s’il n’y a pas eu de changement depuis l’exécution du dernier scénario. Nous vous recommandons de planifier l’exécution d’un scénario contenant un déclencheur d’interrogation à intervalles réguliers. Si une modification correspond à la configuration du déclencheur, celui-ci renvoie des lots contenant des informations sur la modification. Si aucune modification ne correspond à la configuration, le déclencheur ne renvoie aucun lot.

Pour obtenir des instructions sur la planification d’un scénario, consultez [Planification d’un scénario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

Les déclencheurs d’interrogation vous permettent de sélectionner le premier lot qu’ils doivent générer via un panneau qui s’affiche automatiquement après l’enregistrement d’un déclencheur ou la modification de ses paramètres. Cette sélection n’affecte que la première exécution du module. Une fois le module exécuté une fois, les exécutions suivantes surveillent uniquement les modifications qui se produisent après l’exécution la plus récente.

Pour plus d’informations, consultez [Sélection du point de départ d’un module de déclenchement](/help/workfront-fusion/create-scenarios/add-modules/choose-where-trigger-module-starts.md).

>[!BEGINSHADEBOX]

**Exemples :**

* **Workfront > [!UICONTROL Surveiller les enregistrements]** renvoie les fichiers qui ont été ajoutés depuis la dernière exécution du scénario.

* **[!DNL Google Sheets]> [!UICONTROL Surveiller les lignes]** renvoie les nouvelles lignes ajoutées depuis la dernière exécution du scénario.

>[!ENDSHADEBOX]

### Déclencheurs instantanés

Les déclencheurs instantanés permettent à un service d’informer Workfront Fusion d’une modification dès qu’elle se produit. Nous vous recommandons de planifier l’exécution immédiate d’un scénario contenant un déclencheur instantané.

Pour obtenir des instructions, consultez [Planification d’un scénario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

Pour plus d’informations sur la manière dont les données entrantes sont traitées par un déclencheur instantané, consultez [Déclencheurs instantanés (webhooks)](/help/workfront-fusion/references/modules/webhooks-reference.md).

>[!BEGINSHADEBOX]

**Exemples :**

* **Workfront > [!UICONTROL Surveiller les événements]** renvoie des informations lorsqu’un certain type d’événement se produit dans Workfront, comme la création d’une tâche.
* **[!DNL Google Sheets]> [!UICONTROL Surveiller les modifications]** renvoie des informations chaque fois qu’une cellule est mise à jour.

>[!ENDSHADEBOX]

## Agrégateurs

Un module agrégateur regroupe plusieurs lots en un seul lot.

Les agrégateurs ne renvoient qu’un seul lot, qui est ensuite transmis au module suivant pour traitement.

Vous ne pouvez placer des agrégateurs qu’au milieu d’un scénario.

Les scénarios peuvent contenir un nombre illimité d’agrégateurs, bien qu’un grand nombre de modules (plus de 150) puisse affecter les performances.

>[!BEGINSHADEBOX]

**Exemples :**

* **[!UICONTROL Archive] > [!UICONTROL Créer une archive]** compresse plusieurs fichiers dans une archive ZIP.
* **[!UICONTROL CSV] > [!UICONTROL Agréger en CSV]** fusionne plusieurs chaînes d’un fichier CSV en une seule ligne.
* **[!UICONTROL Outils] > [!UICONTROL Agrégateur de texte]** combine plusieurs chaînes en une seule.

>[!ENDSHADEBOX]

Pour plus d’informations, consultez [Module agrégateur](/help/workfront-fusion/references/modules/aggregator-module.md).

## Itérateurs

Un itérateur est un type de module qui divise les tableaux en plusieurs lots.

Les itérateurs renvoient un ou plusieurs lots, qui sont ensuite transmis au module suivant pour traitement.

Vous ne pouvez placer des itérateurs qu’au milieu d’un scénario.

Les scénarios peuvent contenir un nombre illimité d’itérateurs, bien qu’un grand nombre de modules (plus de 150) puisse affecter les performances.

>[!BEGINSHADEBOX]

**Exemple :**

**[!UICONTROL E-mail] > [!UICONTROL Récupérer les pièces jointes]** divise un tableau de pièces jointes en plusieurs lots.

>[!ENDSHADEBOX]

Pour plus d’informations, consultez [Module itérateur](/help/workfront-fusion/references/modules/iterator-module.md) et [Mappage d’un tableau](/help/workfront-fusion/create-scenarios/map-data/map-an-array.md).
