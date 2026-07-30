---
source-git-commit: 67301a4e3c16eaed28f92a1be7556c5574308429
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---
# Exemples de référence des notes de mise à jour de Fusion

Exemples de travail pour la compétence `fusion-release-notes`, en fonction des pages récentes réelles dans
`help/workfront-fusion/fusion-product-releases/fusion-releases-2026/`.

---

## Exemple 1 : une semaine simple et multi-fonctionnalités

Basé sur `fusion-2026-6-22.md`.

```markdown
---
title: Workfront Fusion release activity Week of June 22, 2026
description: Workfront Fusion release activity Week of June 22, 2026
author: Becky
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
---
# Workfront Fusion release activity: Week of June 22, 2026

This page describes all enhancements made in Adobe Workfront Fusion the week of June 22, 2026.

For a list of all recent changes, see [Adobe Workfront Fusion release activity](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

For a list of recent bug fixes in Workfront Fusion, see the [Workfront Maintenance Updates](https://experienceleague.adobe.com/en/docs/workfront-known-issues/releases/current-updates) page and check for any updates labeled Workfront Fusion Maintenance Update.

## Create custom JavaScript packages to use in scenarios

To provide better flexibility and control of your scenarios, we've added the ability to create a custom JavaScript packages that you can then use in scenarios. You can create custom packages in the Packages area of Fusion. You then add functions or variables from these packages to your scenarios in the form of an Adobe App Builder module.

Packages include functions, along with any variables or dependencies the functions rely on. You can also test functions in your package before using them in your scenarios

Because custom packages work through Adobe App Builder, your organization must have an Adobe App Builder license to use them.

For more information on using custom functions in Fusion, see [Use custom function packages](/help/workfront-fusion/create-scenarios/map-data/use-custom-function-packages.md).

## View changes between scenario versions

To make it easier to understand changes between scenario versions, we've added the ability to view and compare those changes. Now you can bring up a window that displays specific changes between two selected versions of the same scenario.

For more information, see [View and manage scenario versions](/help/workfront-fusion/manage-scenarios/restore-a-scenario-version.md).
```

---

## Exemple 2 : semaine avec une légende Action obligatoire/obsolescence

Basé sur `fusion-2026-3-9.md`.

```markdown
---
title: Workfront Fusion release activity Week of March 9, 2026
description: Workfront Fusion release activity Week of March 9, 2026
author: Becky
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
---
# Workfront Fusion release activity: Week of March 9, 2026

This page describes all enhancements made in Adobe Workfront Fusion the week of March 9, 2026.

For a list of all recent changes, see [Adobe Workfront Fusion release activity](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

For a list of recent bug fixes in Workfront Fusion, see the [Workfront Maintenance Updates](https://experienceleague.adobe.com/en/docs/workfront-known-issues/releases/current-updates) page and check for any updates labeled Workfront Fusion Maintenance Update.

## Log in to Fusion through Adobe IMS

>[!IMPORTANT]
>
>**Action Required: Migrate to IMS Login for Adobe Workfront Fusion by April 15.**
>
>To ensure that you will be able to log in after April 15, your Fusion administrator must migrate you to Adobe IMS. Please contact your Fusion administrator to be migrated.

As part of our ongoing security enhancements, Adobe is deprecating the legacy username and password login method for Adobe Workfront Fusion. Effective **April 15**, the legacy login flow **will no longer be supported**.

Going forward, access to Adobe Workfront Fusion will require authentication through the Adobe Identity Management System (IMS) login flow.

For instructions on provisioning access through the Adobe Admin Console, see [Add users to Adobe Workfront Fusion through the Adobe Admin Console](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/add-fusion-users-admin-console.md).

If you have questions or need assistance with the migration process, please contact your Adobe representative.

## New route labels

To make it easier to identify routes, we've added labels. Now, routes are labeled in the order they execute. Fallback and error handling routes are also labeled. Route labels also display any filters used for that route.

For more information on routes, see [Add a Router module and configure routes](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).
```

---

## Exemple 3 : lancement d’un nouveau connecteur

Basé sur `fusion-2026-7-27.md`.

```markdown
## Adobe Content Tagger connector and modules now available

You can now use Workfront Fusion to tag content in Adobe documents.

With the Adobe Content Tagger modules, you can:

* Tag colors in an image, returning the percentage covered by different pixel colors
* Tag keywords or key phrases that best describe the subject of a document
* Tag text in an image, indicating whether text is present and returning it if so

For more information, see [Adobe Content Tagger modules](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/content-tagging-modules.md).
```

Pour un lancement de connecteur de ce type, demandez toujours (selon l’étape 1 de la compétence) si l’utilisateur souhaite qu’une redirection soit configurée pour celui-ci.

---

## Modèle de mise à jour de la page Aperçu (`fusion-release-activity.md`)

Ajouter la semaine du 20 juillet 2026 à une section du mois de juillet 2026 existante :

```markdown
## Fusion releases in 2026

### July 2026

* [Workfront Fusion release activity: Week of July 20, 2026](/help/workfront-fusion/fusion-product-releases/fusion-releases-2026/fusion-2026-7-20.md)
* [Workfront Fusion release activity: Week of July 13 2026](/help/workfront-fusion/fusion-product-releases/fusion-releases-2026/fusion-2026-7-13.md)
```

Commencer une toute nouvelle année (exemple uniquement : faites-le lorsque la première version de {YYYY+1} est publiée) :

```markdown
## Fusion releases in 2027

### January 2027

* [Workfront Fusion release activity: Week of January 4, 2027](/help/workfront-fusion/fusion-product-releases/fusion-releases-2027/fusion-2027-1-4.md)

## Fusion releases in 2026

+++ **Click to open**

### December 2026
...
+++
```

---

## Modèle de mise à jour TOC.md

Ajout de la semaine du 20 juillet 2026 comme dernière entrée :

```markdown
* Fusion release activity {#fusion-release-activity}
    * [Adobe Workfront Fusion release activity](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md)
    * Fusion releases - 2026 {#fusion-releases-2026}
        * [Workfront Fusion release activity: Week of July 20, 2026](/help/workfront-fusion/fusion-product-releases/fusion-releases-2026/fusion-2026-7-20.md)
        * [Workfront Fusion release activity: Week of July 13 2026](/help/workfront-fusion/fusion-product-releases/fusion-releases-2026/fusion-2026-7-13.md)
        ...
```

---

## Redirige la référence du référentiel (pour l’étape 7)

Le référentiel de `redirects` frère (`Adobe-Enterprise-Docs/redirects`) contient des redirections 1:1 dans les fichiers CSV sous `redirects/`, une par environnement : `redirects-dev.csv`, `redirects-stage.csv`, `redirects-prod.csv`.

Règles de ligne (à partir du fichier README de ce référentiel) :

- `source` doit commencer par `/en` (les variations de langue sont créées automatiquement) et ne contenir aucun espace.
- `destination` peut s’agir d’un chemin relatif commençant par `/en` ou d’une URL complète commençant par `https` et ne doit contenir aucun espace.
- Pas de doublons `source`, et pas de doublons `source`/`destination`.
- Une redirection ne doit pas entraîner de boucle de redirection.

Après l’ajout d’une ligne, une requête de tirage doit toujours être générée dans le référentiel `redirects` et fusionnée avant de passer en ligne (~5 minutes après la fusion pour les redirections 1:1). Cette compétence n’ajoute la ligne qu’une fois que l’utilisateur l’a confirmée ; elle n’élève pas la requête de tirage.

---

## Incohérences connues dans les pages existantes (à titre de référence uniquement — ne les copiez pas dans de nouvelles pages)

1. **Titre d’année déplacé dans le fichier TOC.md** — les entrées de janvier et février 2026 se trouvent actuellement sous le titre `Fusion releases - 2025` au lieu de `Fusion releases - 2026`. Il s’agit d’un bogue préexistant, et non de la structure prévue.
2. **Virgule manquante avant l’année** — des pages comme `fusion-2026-7-13.md` utilisent « 13 juillet 2026 » au lieu de « 13 juillet 2026 » dans le titre/la description/H1. Insérez toujours la virgule dans les nouvelles pages.
3. **`hidefromtoc`vs `exl-id`/`TQID`** : les pages allant de `fusion-2026-4-27.md` en haut contiennent un `exl-id` (et parfois un `TQID`) ; les pages allant de `fusion-2026-5-4.md` en bas utilisent plutôt des `hidefromtoc: true`. Les nouvelles pages doivent suivre le modèle le plus récent (`hidefromtoc: true`, pas de `exl-id`/`TQID`), car ces identifiants sont attribués ultérieurement par le pipeline de publication.
4. Préfixe **`{hide-from-toc}`dans TOC.md** : utilisé pour supprimer l’accentuation des entrées plus anciennes dans le rendu de la navigation une fois qu’elles ne sont plus visibles récemment. Ne l’ajoutez pas à une toute nouvelle entrée.
