---
source-git-commit: 4d32e8aab5b3b8a12dbc23e61f517fc4fd6dc9e5
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---
# Modèles de référence des notes de mise à jour

Modèles détaillés pour chaque type de page de note de mise à jour. Ils sont basés sur les modèles de la section
`help/quicksilver/product-announcements/product-releases/release-note-templates/` et
mise en forme réelle utilisée dans les dernières versions trimestrielles.

&#x200B;---

## Modèle de page de la zone de produit

```markdown
---
title: {Written Quarter} {Year} {Area} enhancements
description: {Written Quarter} {Year} {Area} enhancements
author: {Author}
feature: Product Announcements
recommendations: noDisplay, noCatalog
exl-id: {existing UUID}
---
# {Written Quarter} {Year} {Area} enhancements

This page describes {Area} enhancements made with the {Written Quarter} {Year} release to the Preview environment. These enhancements will be made available in the Production environment as noted.

For a list of all changes available at this point in the {Written Quarter} {Year} release cycle, see [{Written Quarter} {Year} release overview](/help/quicksilver/product-announcements/product-releases/{YY}-q{N}-release-activity/{YY}-q{N}-release-overview.md).

## Feature Title Here

>[!NOTE]
>
>Preview: {Month Day, Year}
>Production fast release: {Month Day, Year}
>Production for everyone: {Month Day, Year}

Feature description paragraph.

For more information, see [Help article title](/help/quicksilver/path/to/article.md).
```

### Règles pour les pages de la zone de produit

- Utiliser Markdown (et non HTML) pour le contenu du corps
- Chaque fonctionnalité reçoit un en-tête H2
- La légende `>[!NOTE]` doit être précédée d&#39;une ligne vide
- Le format `>[!NOTE]` est exactement :

  ```
  >[!NOTE]
  >
  >Preview: {date}
  >Production fast release: {date}
  >Production for everyone: {date}
  ```

- Si une fonction a été temporairement supprimée, ajoutez une ligne après la date :

  ```
  >
  >This feature has been temporarily removed from the Production environment on {date}.
  ```

- Les liens d’aide utilisent des chemins absolus commençant par `/help/quicksilver/`

&#x200B;---

## Modèle de page d’aperçu

```markdown
---
title: {Written Quarter} {Year} release overview
description: This page provides information about functionality that is included in the {Written Quarter} {Year} release. These enhancements are planned to become available in the Production environment throughout the quarter.
author: {Author}
feature: Product Announcements
recommendations: noDisplay, noCatalog
exl-id: {existing UUID}
---
# {Written Quarter} {Year} release overview

This page provides information about functionality that is included in the {Written Quarter} {Year} release scheduled for {Release Month} {Year}.

The enhancements on this page are available in the Preview environment. This page will be updated with additional enhancements as the {Written Quarter} {Year} release nears its planned Production release.

>[!IMPORTANT]
>
>
>Monthly and quarterly releases are planned to be available on the Thursday of the second full week of the month, unless otherwise specified.
>
>|Monthly release|Quarterly release|
>|----|----|
>|<ul><li>{VV}.{M} ({Month Day, Year})</li><li>{VV}.{M} ({Month Day, Year})</li><li>{VV}.{M} ({Month Day, Year})</li></ul>|<ul><li>{VV}.{M} ({Month Day, Year})</li></ul>|
>
>Note that for the final release of each quarter ({VV}.{M} this quarter), users on the fast release schedule will receive the release one day early ({Month Day, Year}).
>
>For more information on the fast release process, see [Enable or disable the fast release process](/help/quicksilver/administration-and-setup/set-up-workfront/configure-system-defaults/enable-fast-release-process.md).

## Adobe Workfront enhancements

* [Administrator enhancements](#administrator-enhancements)
* [Document enhancements](#document-enhancements)
* [Project enhancements](#project-enhancements)
* [Reporting enhancements](#reporting-enhancements)
* [Requesting enhancements](#requesting-enhancements)
* [Other enhancements](#other-enhancements)
```

### Tableau des fonctionnalités de présentation

Chaque section de zone produit H3 contient un tableau HTML. Utilisez cette structure exacte :

```html
### {Area} enhancements

<table>
            <col style="width: 50%;" />
            <col style="width: 25%;" />
            <tbody>
              <tr>
        <td><strong>Feature</strong>
        </td>
        <td><strong>Preview</strong></td>
        <td><strong>Fast release</strong></td>
        <td><strong>Quarterly</strong></td>
        </tr>
    <tr>
        <td>
            <a href="/help/quicksilver/product-announcements/product-releases/{YY}-q{N}-release-activity/{YY}-q{N}-{area}.md" class="MCXref xref" xrefformat="{para}">Feature Title</a><p>Short description of the feature.</p>
        </td>
        <td><p>{Month Day, Year}</p></td>
        <td><p>{Month Day, Year}</p></td>
        <td><p>{Month Day, Year}</p></td>
    </tr>
            </tbody>
        </table>
```

#### Règles de table

- Cellule caractéristique : balise `<a>` avec `class="MCXref xref" xrefformat="{para}"` suivie d’`<p>` description
- Le `href` renvoie vers la page de la zone produit (et non vers une ancre spécifique).
- Cellules de date : enveloppées dans des balises `<p>`
- Pour les éléments hors planification, ajoutez `<p>[!BADGE Off schedule]{type=Neutral}</p>` après le lien
- Une `<p></p>` vide après que le lien est acceptable lorsqu’aucun badge n’est nécessaire
- Veiller à ce que la mise en retrait d’HTML reste cohérente avec les fichiers existants

### Présentation des dernières sections

Après toutes les tables de zone de produit :

```markdown
## Release notes for other areas

### Workfront Fusion enhancements

New features in Workfront Fusion are available in Production at a cadence outside of the standard release schedule. For more information about the latest features, see [Adobe Workfront Fusion release activity](https://experienceleague.adobe.com/fr/docs/workfront-fusion/using/fusion-release-activity/fusion-release-activity).

### Workfront Planning enhancements

New features in Workfront Planning are available in Production. For more information about the latest features, see [{Written Quarter} {Year} release activity for Adobe Workfront Planning](/help/quicksilver/product-announcements/product-releases/planning-release-activity/planning-release-activity-{YY}-q{N}.md).

There are no updates for the following at this point in the release:

* Scenario Planner
* Proof
* Goals

## Desktop proofing viewer updates

{Version info if available, otherwise omit section}

## Announcements

{Announcement content}

### API version {NN}

{API version info}

### Workfront Maintenance Updates

For information about the maintenance updates made during the {Written Quarter} {Year} release, see [Workfront Maintenance Updates](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html?lang=fr).

### Training updates

Explore the latest updates made to learning programs, learning paths, videos, and guides for each Adobe Workfront product release. For more information, see the "What's New" section of the [Workfront Tutorials page](https://experienceleague.adobe.com/docs/workfront-learn/tutorials-workfront/home.html?lang=fr).
```

&#x200B;---

## Modèle de page d’apparence

```markdown
---
title: Look-and-feel updates during the {Written Quarter} {Year} release time frame
description: Look-and-feel updates during the {Written Quarter} {Year} release time frame
author: {Author}
feature: Product Announcements
recommendations: noDisplay, noCatalog
exl-id: {existing UUID}
---

# Look-and-feel updates during the {Written Quarter} {Year} release time frame

This page describes minor updates to the look and feel of various areas of the Adobe Workfront application that were made within the {Written Quarter} {Year} release timeframe. These enhancements will be made available in the Production environment a minimum of 2 weeks after releasing to Preview.

For a list of all changes available with the {Written Quarter} {Year} release, see [{Written Quarter} {Year} Release overview](/help/quicksilver/product-announcements/product-releases/{YY}-q{N}-release-activity/{YY}-q{N}-release-overview.md).

## Feature Title

>[!NOTE]
>
>Preview release: {Month Day, Year}; Planned Production release: {Month Day, Year}

Description of the look-and-feel change.
```

&#x200B;---

## Formats de légende de date

### Pages de la zone de produit (multiligne)

```markdown
>[!NOTE]
>
>Preview: March 5, 2026
>Production fast release: April 15, 2026
>Production for everyone: April 16, 2026
```

### Pages d’apparence (une seule ligne)

```markdown
>[!NOTE]
>
>Preview release: March 5, 2026; Planned Production release: March 19, 2026
```

### Pages hebdomadaires (une seule ligne)

```markdown
>[!NOTE]
>
>Preview release: February 9, 2023; Planned Production release: February 23, 2023
```

&#x200B;---

## Incohérences connues à surveiller

1. **Mauvais lien d’aperçu pour le trimestre** — Les pages de la zone produit renvoient parfois à l’aperçu du trimestre précédent (par exemple, `26-q1` au lieu de `26-q2`).
2. **Les dates de prévisualisation n’indiquent pas la bonne année** — Les tableaux de présentation affichent parfois l’année précédente dans la colonne de prévisualisation (par exemple, « 2025 » au lieu de « 2026 »)
3. **Balises de fermeture `</tr>` manquantes** — Certaines lignes du tableau HTML ne comportent pas de balises de fermeture appropriées
4. **`content-type: release-notes`** : présent dans les fichiers plus anciens, omis dans les nouvelles pages de la zone produit 26-q2. Suivez le modèle du trimestre en cours.
5. **Frappe dans le modèle** — Le modèle d&#39;apparence a `relesae` au lieu de `release` ; utilisez toujours l&#39;orthographe correcte
6. **Lien `<p></p>` après la fonctionnalité manquant** — Certaines lignes du tableau d’aperçu omettent la balise `<p>` vide après la balise `<a>`
