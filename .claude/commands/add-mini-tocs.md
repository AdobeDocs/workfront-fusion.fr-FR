---
name: add-mini-tocs
description: ""
source-git-commit: 4ec81401b5a76edd620b9779414ee578966b4315
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---


# Ajouter des mini tables des matières

Analyse un fichier Markdown et insère une mini table des matières sous chaque en-tête qualifié qui comporte des sous-en-têtes directs.

## Workflow

1. Lire le fichier cible.
2. Identifiez chaque en-tête à `##` niveau ou plus profond qui a au moins un en-tête enfant direct (un niveau `#` plus profond).
3. Pour chaque en-tête parent de ce type, créez une liste à puces de liens vers ses enfants directs uniquement.
4. Insérez la liste juste avant le premier en-tête enfant, après tout texte d’introduction qui suit l’en-tête parent.
5. Si une mini table des matières existe déjà à cet emplacement, comparez-la aux en-têtes enfants actuels de cette section. Si la liste est obsolète (entrées manquantes, entrées supplémentaires ou liens incorrects), remplacez-la par la liste mise à jour. S’il correspond déjà, ignorez-le.
6. Écrivez le fichier mis à jour.

## Portée

- **Jamais** créez une mini table des matières sous le titre de l’article `#`. Les mini tables des matières ne sont ajoutées que sous les en-têtes `##` et plus en profondeur.
- Un en-tête de `##` obtient une liste de ses enfants directs `###`.
- Un en-tête de `###` obtient une liste de ses enfants directs `####`.
- Et ainsi de suite pour les niveaux plus profonds.

## Format du lien

Chaque entrée de la liste utilise le format suivant :

```
* [Heading text](#anchor)
```

### Ancrer les règles de génération

Convertissez le texte d’en-tête en ancre comme suit :

1. Tout le texte en minuscules.
2. Supprimez tous les caractères qui ne sont pas des lettres, des chiffres, des espaces ou des tirets.
3. Remplacez les espaces par des tirets.
4. Supprimez toute mise en forme de code encadrée de backtick (conservez le texte à l’intérieur).

Exemple : `### Create or edit a function` → `#create-or-edit-a-function`

## Règles d’imbrication

- Lien **enfants directs** (un niveau plus profond que le parent) uniquement dans chaque liste.
- N’incluez pas les petits-enfants ou les en-têtes plus profonds dans la même liste.
- Si ces en-têtes enfants ont eux-mêmes des enfants, leur propre mini table des matières distincte est insérée en dessous.

**Exemple de structure :**

```
## Manage a package          ← parent: gets a list of ### headings
### Functions                ← child of ##, parent of ####: gets a list of #### headings
#### Create a function       ← child of ###
#### Delete a function       ← child of ###
### Variables                ← child of ##
### History                  ← child of ##
```

Résultats dans :

Sous `## Manage a package` :

```
* [Functions](#functions)
* [Variables](#variables)
* [History](#history)
```

Sous `### Functions` :

```
* [Create a function](#create-a-function)
* [Delete a function](#delete-a-function)
```

## Emplacement

Insérez la mini liste des tables des matières juste avant le premier en-tête enfant. S’il existe un texte d’introduction entre l’en-tête parent et le premier en-tête enfant, la liste suit ce texte, directement au-dessus du premier en-tête enfant. Incluez toujours une ligne vide avant et après la liste de table des matières miniature.

## Éléments à ignorer

- `#` en-têtes (titre de l’article) : n’ajoutez jamais de mini table des matières ici.
- En-têtes parents avec un seul enfant direct : ignorer — une liste à un seul élément n’ajoute aucune valeur de navigation.
- Sections sans en-têtes enfants : ignorer.
