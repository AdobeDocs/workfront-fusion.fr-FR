---
title: Fonctions de tableau
description: Les fonctions de tableau suivantes sont disponibles dans le panneau de mappage d’Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 16c3915c-add1-4aab-a0e1-75fc590c42a6
source-git-commit: 2c732659f3f3e81e13b7b12a5df5bde19c0e0928
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 95%

---

# Fonctions de tableau

## [!UICONTROL join (array; separator)]

Concatène tous les éléments d’un tableau en une chaîne, en utilisant le séparateur spécifié entre chaque élément.

## [!UICONTROL length (array)]

Renvoie le nombre d’éléments d’un tableau.

## [!UICONTROL keys (object)]

Renvoie un tableau des propriétés d’un objet ou d’un tableau donné.

## [!UICONTROL slice (array; start; [end])]

Renvoie un nouveau tableau contenant uniquement les éléments sélectionnés.

## [!UICONTROL merge (array1; array2; ...)]

Fusionne un ou plusieurs tableaux en un seul.

## [!UICONTROL contains (array; value)]

Vérifie si un tableau contient la valeur.

## [!UICONTROL remove (array; value1; value2; ...)]

Supprime les valeurs spécifiées dans les paramètres d’un tableau. Cette fonction est efficace uniquement pour les tableaux primitifs de textes ou de nombres.

## [!UICONTROL add (array; value1; value2; ...)]

Ajoute les valeurs spécifiées dans les paramètres à un tableau et renvoie ce tableau.

## [!UICONTROL map (complex array; key;[key for filtering];[possible values for filtering])]

Renvoie un tableau primitif contenant les valeurs d’un tableau complexe. Cette fonction permet de filtrer les valeurs. Utilisez des noms de variables bruts pour les clés.

>[!BEGINSHADEBOX]

**Exemples :**

* `map(Emails[];email)`

  Renvoie un tableau primitif contenant les e-mails.

* `map(Emails[];email;label;work;home)`

  Renvoie un tableau primitif contenant les e-mails dont le libellé est « travail » ou « perso ».

>[!ENDSHADEBOX]

Pour plus d’informations, voir [Mapper un tableau ou un élément de tableau](/help/workfront-fusion/create-scenarios/map-data/map-an-array.md).

## shuffle

## [!UICONTROL sort (array; [order]; [key])]

Trie les valeurs d’un tableau. Les valeurs valides du paramètre `order` sont les suivantes :

* `asc`

  (par défaut) - ordre croissant : 1, 2, 3, ... pour le type Nombre. A, B, C, a, b, c, ... pour le type Texte.

* `desc`

  ordre décroissant : ..., 3, 2, 1 pour le type Nombre. ..., c, b, a, C, B, A pour le type Texte.

* `asc ci`

  ordre croissant insensible à la casse : A, a, B, b, C, c, ... pour le type Texte.

* `desc ci`

  ordre décroissant insensible à la casse : ..., C, c, B, b, A, a pour le type Texte.

Utilisez le paramètre `key` pour accéder aux propriétés des objets complexes.

Utilisez des noms de variables bruts pour les clés.

Pour accéder aux propriétés imbriquées, utilisez la notation avec point.

Le premier élément d’un tableau est l’index 1.

>[!BEGINSHADEBOX]

**Exemples :**

* `sort(Contacts[];name)`

  Trie un tableau de contacts en fonction de la propriété « name » dans l’ordre croissant par défaut.

* `sort(Contacts[];desc;name)`

  Trie un tableau de contacts en fonction de la propriété « name » dans l’ordre décroissant.

* `sort(Contacts[];asc ci;name)`

  Trie un tableau de contacts en fonction de la propriété « name » dans l’ordre croissant insensible à la casse.

* `sort(Emails[];sender.name)`

  Trie un tableau d’e-mails en fonction de la propriété « sender.name ».

>[!ENDSHADEBOX]

## [!UICONTROL reverse (array)]

Le premier élément du tableau devient le dernier élément, le deuxième devient l’avant-dernier, et ainsi de suite.

## [!UICONTROL flatten (array)]

Crée un nouveau tableau dans lequel sont concaténés tous les éléments des sous-tableaux, de manière récursive, jusqu’à la profondeur spécifiée.

## [!UICONTROL distinct (array; [key])]

Supprime les doublons dans un tableau. Utilisez l’argument « [!UICONTROL key] » pour accéder aux propriétés dans des objets complexes. Pour accéder aux propriétés imbriquées, utilisez la notation avec point. Le premier élément d’un tableau est l’index 1.

>[!BEGINSHADEBOX]

**Exemple :** `distinct(Contacts[];name)`

Supprime les doublons dans un tableau de contacts en comparant la propriété « nom ».

>[!ENDSHADEBOX]

## toCollection

## toArray

Cette fonction convertit une collection en un tableau de paires clé-valeur.

>[!BEGINSHADEBOX]

**Exemples :**

Prenons l’exemple de la collection suivante :

`{ key1: "value1", key2: "value2:}`

La fonction

`toArray({ key1: "value1", key2: "value2:})`

Renvoie le tableau de paires clé-valeur

`[{ key1: "value1"}, { key2: "value2"}]`

>[!ENDSHADEBOX]

## [!UICONTROL arrayDifference [array1, array2, mode]]

Renvoie la différence entre deux tableaux.

Saisissez l’une des valeurs suivantes pour le paramètre `mode`.

* `classic` : renvoie un nouveau tableau contenant tous les éléments de `array1` qui n’existent pas dans `array2`.

* `symmetric` : renvoie un tableau d’éléments qui ne sont pas communs aux deux tableaux.

  En d’autres termes, la fonction renvoie un tableau contenant tous les éléments de `array1` qui n’existent pas dans `array2`, et tous les éléments de `array2` qui n’existent pas dans `array1`.

>[!BEGINSHADEBOX]

**Exemples :**

Les tableaux suivants :

```
myArray = [1,2,3,4,5]
```

```
yourArray = [3,4,5,6,7]
```

* `arrayDifference [myArray, yourArray, classic]`

  Retourne `[1,2]`

* `arrayDifference [yourArray, myArray, classic]`

  Renvoie `[6,7]`

* `arrayDifference [myArray, yourArray, symmetric]`

  Renvoie `[1,2,6,7]`

>[!ENDSHADEBOX]

## deDuplicate

## Mots-clés

## emptyarray
