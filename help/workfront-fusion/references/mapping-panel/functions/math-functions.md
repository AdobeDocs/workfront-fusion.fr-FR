---
title: Fonctions mathématiques
description: Les fonctions mathématiques suivantes sont disponibles dans le panneau de mappage d’Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 3d08b09d-b395-4226-b7e3-d5650c428a59
source-git-commit: e11e581c092ebba343a0f2d6943ecbe4d0fe4c87
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 62%

---

# Fonctions mathématiques

## [!UICONTROL average ([tableau de valeurs]) average(value1; [value2], ...)]

Renvoie la valeur moyenne des valeurs numériques d’un tableau spécifique ou la valeur moyenne des valeurs numériques saisies unitairement.

## [!UICONTROL ceil (nombre)]

Renvoie le plus petit entier supérieur ou égal à un nombre spécifié.

>[!BEGINSHADEBOX]

**Exemples :**

* `ceil(` `1.2` `)`

  Renvoie 2

* `ceil(` `4` `)`

  Renvoie 4

>[!ENDSHADEBOX]

## [!UICONTROL floor (nombre)]

Renvoie le plus grand entier inférieur ou égal à un nombre spécifié.

>[!BEGINSHADEBOX]

**Exemples :**

* `floor(` `1.2` `)`

  Renvoie 1

* `floor(` `1.9` `)`

  Renvoie 1

* `floor(` `4` `)`

  Renvoie 4

>[!ENDSHADEBOX]

## [!UICONTROL max ([tableau de valeurs]), max(valeur1;valeur2; ...)]

Renvoie le plus grand nombre d’un tableau spécifié ou le plus grand nombre parmi les nombres renseignés individuellement.

## [!UICONTROL min ([tableau de valeurs]), min(valeur1; valeur2; ...)]

Renvoie le plus petit nombre dans un tableau spécifié ou le plus petit nombre parmi les nombres saisis individuellement.

## [!UICONTROL round (nombre)]

Arrondit le nombre au nombre entier immédiatement inférieur.

>[!BEGINSHADEBOX]

**Exemples :**

* `round(` `1.2` `)`

  Renvoie 1

* `round(` `1.5` `)`

  Renvoie 2

* `round(` `1.7` `)`

  Renvoie 2

* `round(` `2` `)`

  Renvoie 2

>[!ENDSHADEBOX]

## [!UICONTROL sum ([tableau de valeurs]), sum(valeur1; valeur2; ...)]

Renvoie la somme des valeurs d’un tableau spécifié ou la somme des nombres saisis individuellement.

## [!UICONTROL parseNumber (nombre ; séparateur décimal)]

Analyse une chaîne avec un nombre et renvoie le nombre. Par exemple, parseNumber(1 756,456;,)

## [!UICONTROL formatNumber (nombre ; decimalPOINTS; [decimalSeparator]; [thousandsSeparator])]

Renvoie un nombre au format demandé. Par défaut, le point décimal est une virgule (,) et le séparateur des milliers est un point (.).

>[!BEGINSHADEBOX]

**Exemple :**

`formatNumber( 123456789 ; 3 ; , ; . )`

Renvoie 123.456.789,000

>[!ENDSHADEBOX]

### [!UICONTROL abs(number)]

[!BADGE Nouveau !]{type=Informative}

Renvoie la valeur absolue d’un nombre.

>[!BEGINSHADEBOX]

**Exemple :**

* `abs(-3.14)`

  Renvoie 3,14.
* `abs(3.14)`

  Renvoie 3,14.


### [!UICONTROL div(number1; number2; ...)]

[!BADGE Nouveau !]{type=Informative}

Divise tous les nombres dans l’ordre indiqué.

>[!BEGINSHADEBOX]

**Exemple :**

* `div(10; 2)`

  Renvoie 5
* `div(100; 5; 4)`

  Renvoie 5


### [!UICONTROL ln(number)]

[!BADGE Nouveau !]{type=Informative}

Renvoie le logarithme naturel du nombre.


>[!BEGINSHADEBOX]

**Exemple :**

* `ln(1)`

  Renvoie 0
* `ln(2.718281828)`

  Renvoie 1


### [!UICONTROL log(number1 ; number2)]

[!BADGE Nouveau !]{type=Informative}

Renvoie le logarithme de `number2` au `number1` de base.

>[!BEGINSHADEBOX]

**Exemple :**

* `log(10; 100)`

  Renvoie 2
* `log(2; 8)`

  Renvoie 3


### [!UICONTROL number(string)]

[!BADGE Nouveau !]{type=Informative}

Convertit une chaîne en nombre.

>[!BEGINSHADEBOX]

**Exemple :**

* `number("3.14")`

  Renvoie 3,14.
* `number("42")`

  Renvoie 42


### [!UICONTROL power(number; power)]

[!BADGE Nouveau !]{type=Informative}

Renvoie un nombre élevé à la puissance spécifiée.

>[!BEGINSHADEBOX]

**Exemple :**

* `power(2; 3)`

  Renvoie 8
* `power(4; 0.5)`

  Renvoie 2


### [!UICONTROL prod(number1 ; number2 ; ...)]

[!BADGE Nouveau !]{type=Informative}

Multiplie tous les nombres fournis ensemble.

>[!BEGINSHADEBOX]

**Exemple :**

* `prod(2; 3; 4)`

  Renvoie 24
* `prod(5; 5)`

  Renvoie 25


### [!UICONTROL sortAscNum(number1 ; number2 ; ...)]

[!BADGE Nouveau !]{type=Informative}

Renvoie les nombres fournis triés par ordre croissant.

>[!BEGINSHADEBOX]

**Exemple :**

* `sortAscNum(3; 1; 2)`

  Renvoie \[1, 2, 3]
* `sortAscNum(5; 3; 4)`

  Renvoie \[3, 4, 5]


### [!UICONTROL sortDescNum(number1 ; number2 ; ...)]

[!BADGE Nouveau !]{type=Informative}

Renvoie les nombres fournis triés par ordre décroissant.

>[!BEGINSHADEBOX]

**Exemple :**

* `sortDescNum(3; 1; 2)`

  Renvoie \[3, 2, 1]
* `sortDescNum(5; 3; 4)`

  Renvoie \[5, 4, 3]


### [!UICONTROL sqrt(number)]

[!BADGE Nouveau !]{type=Informative}

Renvoie la racine carrée d’un nombre.

>[!BEGINSHADEBOX]

**Exemple :**

* `sqrt(9)`

  Renvoie 3
* `sqrt(4)`

  Renvoie 2


### [!UICONTROL sub(number1 ; number2 ; ...)]

[!BADGE Nouveau !]{type=Informative}

Soustrait tous les nombres dans l&#39;ordre fourni.

>[!BEGINSHADEBOX]

**Exemple :**

* `sub(10; 3; 2)`

  Renvoie 5
* `sub(20; 5)`

  Renvoie 15
