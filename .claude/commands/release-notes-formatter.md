---
name: release-notes-formatter
description: Formatez et validez les notes de mise à jour de Workfront pour garantir la cohérence, la structure correcte et des liens appropriés. À utiliser uniquement pour les fichiers de notes de mise à jour dans les répertoires de versions de produits ou lorsque l’utilisateur mentionne des notes de mise à jour, des versions de produit ou des versions trimestrielles. Ne s’applique pas aux articles de procédure ni à la documentation générale.
source-git-commit: 4d32e8aab5b3b8a12dbc23e61f517fc4fd6dc9e5
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 2%

---


# Formateur de notes de mise à jour

Formater et valider les notes de mise à jour d’Adobe Workfront dans le répertoire `help/quicksilver/product-announcements/product-releases/`.

## Types de page

Identifiez le type de page à partir du chemin d’accès au fichier et du contenu :

| Type de page | Modèle de fichier | Modèle |
|-----------|-------------|----------|
| **Vue d’ensemble** | `{YY}-q{N}-release-overview.md` | Voir .#overview-page-template |
| **Zone du produit** | `{YY}-q{N}-{area}.md` | Voir .#product-area-page-template |
| **Planification** | `planning-release-activity-{YY}-q{N}.md` | Similaire à la zone de produit |
| **Apparence** | `look-and-feel-updates-{YY}-q{N}.md` | Voir .#look-and-feel-page-template |

## Workflow de formatage

### Étape 1 : valider FrontMATTER

Champs obligatoires pour toutes les pages de notes de mise à jour :

```yaml
---
title: <descriptive title>
description: <matches or summarizes the title>
author: <author name>
feature: Product Announcements
recommendations: noDisplay, noCatalog
exl-id: <existing UUID — never generate or change>
---
```

Règles :
- `feature` doit être exactement `Product Announcements`
- `recommendations` doit être exactement `noDisplay, noCatalog`
- N’inventez jamais une `exl-id`, incluez-la uniquement si elle existe déjà
- Ne pas ajouter de `draft: Probably` sur les pages réelles (modèles uniquement)

### Étape 2 : valider la structure par type de page

#### Pages de la zone de produit

1. **H1** : `{Written Quarter} {Area} enhancements`
   - Exemple : `# Second Quarter 2026 Administrator enhancements`
   - Le trimestre doit être écrit : « Premier trimestre », « Deuxième trimestre », « Troisième trimestre », « Quatrième trimestre »

2. **Paragraphe d’introduction** : décrit la zone et les liens vers la présentation.
   - Doit être lié au fichier de vue d’ensemble **trimestre correct**
   - Bogue courant : liaison au trimestre précédent (par exemple, `26-q1` au lieu de `26-q2`)

3. **H2 par fonctionnalité** : titre de la fonctionnalité comme en-tête
   - **Fonctionnalités les plus récentes en premier** — la note de mise à jour la plus récente doit apparaître comme le premier H2 après le paragraphe d&#39;introduction
   - Les anciennes fonctionnalités suivent dans l’ordre chronologique inverse

4. **Bloc de légende de date** après chaque point H2 :

```markdown
>[!NOTE]
>
>Preview: {Month Day, Year}
>Production fast release: {Month Day, Year}
>Production for everyone: {Month Day, Year}
```

5. **Corps** : description des fonctionnalités, puis lien vers la documentation d’aide.

#### Pages de présentation

1. **H1** : `{Written Quarter} release overview`

2. **Paragraphe d’introduction** avec le mois de publication prévu

3. **`>[!IMPORTANT]`bloc** avec le tableau de calendrier des versions

4. `Adobe Workfront enhancements`**** H2 avec liste à puces des liens d’ancrage :

```markdown
* [Administrator enhancements](#administrator-enhancements)
* [Document enhancements](#document-enhancements)
```

5. **H3 par zone de produit** avec le tableau des fonctionnalités HTML (voir .claude/commands/_release-notes-formatter-reference.md#overview-feature-table)
   - Dans chaque tableau, **les fonctionnalités les plus récentes en premier** — la ligne la plus récente apparaît en haut du tableau (après la ligne d’en-tête)

6. **Sections de fin** (H2) : notes de mise à jour pour d’autres zones, mises à jour des visionneuses de vérification pour bureau, annonces, version de l’API, mises à jour de maintenance, mises à jour de formation

### Étape 3 : valider les liens

- **Lien d’aperçu dans les pages de la zone produit** : doit pointer vers le même trimestre
   - Correct : `26-q2-release-activity/26-q2-release-overview.md`
   - Erreur : `26-q1-release-activity/26-q1-release-overview.md`
- **Liens d’ancrage dans la vue d’ensemble** : doivent correspondre aux identifiants H3 (minuscules, tirets).
- **Liens des fonctionnalités dans les tableaux de présentation** : vous devez utiliser `class="MCXref xref" xrefformat="{para}"`
- **Liens vers les documents d’aide** : doit commencer par `/help/quicksilver/`

### Étape 4 : valider les dates

- Format : `{Month} {Day}, {Year}` (par exemple, « 12 mars 2026 »)
- Utiliser des `TBD` pour les dates inconnues
- Les dates du bloc de `>[!NOTE]` de la page de la zone produit doivent correspondre à la ligne correspondante du tableau d’aperçu
- Les dates de prévisualisation doivent précéder les dates de production.

### Étape 5 : correctifs courants

Appliquez ces correctifs lors du formatage :

| Problème | Corriger |
|-------|-----|
| Mauvais trimestre du lien d’aperçu | Mettre à jour pour correspondre au propre trimestre du fichier |
| Bloc de date de `>[!NOTE]` manquant | Ajouter un bloc après l’en-tête de fonctionnalité H2 |
| Format de date incohérent | Normaliser pour `Month Day, Year` |
| Ligne vide manquante avant `>[!NOTE]` | Ajouter une ligne vide |
| Espaces supplémentaires dans les lignes de légende | Rogner l’espace de fin |
| HTML dans les pages de zone de produit | Conserver en tant que markdown (HTML est réservé aux tableaux de présentation uniquement) |
| `exl-id` manquant | Ne le faites pas — n&#39;en générez pas |

### Étape 6 : mettre à jour la table des matières

Chaque fois que vous créez une **nouvelle** page de notes de mise à jour (présentation ou zone produit), ajoutez-la à `help/quicksilver/TOC.md` dans la même modification. Une page qui ne figure pas dans la table des matières n’apparaît pas dans la navigation publiée, même si des liens dans le tableau d’aperçu pointent vers elle.

Où l’ajouter :

- La table des matières comporte une section par trimestre sous un en-tête tel que `* 2026 Q3 Release {#release-26-q3}`. Si l’en-tête du trimestre n’existe pas encore (première page d’un nouveau trimestre), ajoutez-le au-dessus du trimestre précédent afin que le dernier trimestre se trouve en haut.
- Sous cet en-tête de trimestre, répertoriez les pages dans cet ordre :
   1. **Présentation** en premier (`Third Quarter 2026 release overview`).
   2. **Pages de zone de produit** classées par ordre alphabétique par nom de zone (administrateur, documents, opérations d’entreprise, projets, compte rendu des performances, demande).
   3. **Autres améliorations** la dernière (toujours après les zones de produit alphabétiques).

Chaque entrée de la table des matières est un lien Markdown utilisant le titre de la page et le chemin d’accès absolu au référentiel :

```markdown
      * [Third Quarter 2026 Documents enhancements](/help/quicksilver/product-announcements/product-releases/26-q3-release-activity/26-q3-documents.md)
```

Associez la mise en retrait (six espaces) aux entrées environnantes. Utilisez la page H1 mot à mot comme texte du lien, par exemple `Documents enhancements`, `Requesting enhancements` (pas `Requests`), de sorte que les libellés de la table des matières correspondent aux trimestres précédents.

Erreurs courantes à éviter :

- Création d’une page de zone produit sans l’ajouter à la table des matières.
- Création d’un lien vers la présentation d’un autre trimestre à partir de la nouvelle page produit (étape 3).
- Insérer les pages d&#39;un nouveau trimestre sous l&#39;en-tête du trimestre précédent.

## Conventions de dénomination des fichiers

| Type | Motif | Exemple |
|------|---------|---------|
| Vue d’ensemble | `{YY}-q{N}-release-overview.md` | `26-q2-release-overview.md` |
| Zone du produit | `{YY}-q{N}-{area-slug}.md` | `26-q2-admin-and-setup.md` |
| Répertoire | `{YY}-q{N}-release-activity/` | `26-q2-release-activity/` |

Limaces de zone standard : `admin-and-setup`, `documents`, `projects`, `reports`, `requests`, `other`

## Mappage du trimestre

| Trimestre | Formulaire Écrit | Mois |
|---------|-------------|--------|
| T1 | Premier Trimestre | Jan-Mar |
| T2 | Deuxième Trimestre | Avr-Juin |
| T3 | Troisième trimestre | Juillet-Septembre |
| T4 | Quatrième trimestre | Oct-Déc |

La mise à jour trimestrielle de la production arrive généralement le jeudi de la deuxième semaine complète du dernier mois du trimestre.

## Liste de contrôle de validation

Lors de l’examen d’un fichier de notes de mise à jour, vérifiez les points suivants :

- [ ] FrontMATTER contient tous les champs obligatoires avec des valeurs correctes
- [ ] H1 correspond au format du type de page
- [ ] lien Aperçu pointe vers le trimestre correct
- [ ] Chaque fonctionnalité comporte un bloc de date `>[!NOTE]` (pages de zone de produit)
- [ ] format de date est cohérent (`Month Day, Year`)
- [ ] lignes du tableau des fonctionnalités de l’aperçu correspondent au contenu de la page de la zone produit
- [ ] Aucun lien interne rompu
- [ ] liens d’ancrage dans la vue d’ensemble correspondent aux ID de section H3
- [ Les fonctionnalités ] sont classées en commençant par la plus récente (pages de zone de produit et tableaux de présentation)
- [ ] Les nouvelles pages de notes de mise à jour sont répertoriées dans `help/quicksilver/TOC.md` sous le trimestre approprié, avec la présentation en premier et les zones de produits dans l’ordre alphabétique (Autre dernière)

## Ressources supplémentaires

- Pour obtenir des modèles et des exemples HTML complets, voir .claude/commands/_release-notes-formatter-reference.md
