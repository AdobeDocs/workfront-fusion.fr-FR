---
title: Fonctions mathématiques
description: Les fonctions mathématiques suivantes sont disponibles dans le panneau de mappage d’Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 3d08b09d-b395-4226-b7e3-d5650c428a59
source-git-commit: 24a6c1558fd6349c022df8a1847a7f39fafddd67
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 97%

---

# Fonctions mathématiques

## [!UICONTROL average ([array of values]) average(value1; [value2], ...)]

Renvoie la valeur moyenne des valeurs numériques d’un tableau spécifique ou la valeur moyenne des valeurs numériques saisies unitairement.

## [!UICONTROL ceil (number)]

Renvoie le plus petit entier supérieur ou égal à un nombre spécifié.

>[!BEGINSHADEBOX]

**Exemples :**

* `ceil(` `1.2` `)`

  Renvoie 2

* `ceil(` `4` `)`

  Renvoie 4

>[!ENDSHADEBOX]

## [!UICONTROL floor (number)]

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

## [!UICONTROL max ([array of values]), max(value1;value2; ...)]

Renvoie le plus grand nombre d’un tableau spécifié ou le plus grand nombre parmi les nombres renseignés individuellement.

## [!UICONTROL min ([array of values]), min(value1; value2; ...)]

Renvoie le plus petit nombre dans un tableau spécifié ou le plus petit nombre parmi les nombres saisis individuellement.

## [!UICONTROL round (number)]

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

## [!UICONTROL sum ([array of values]), sum(value1; value2; ...)]

Renvoie la somme des valeurs d’un tableau spécifié ou la somme des nombres saisis individuellement.

## [!UICONTROL parseNumber (number; decimal separator)]

Analyse une chaîne avec un nombre et renvoie le nombre. Par exemple, parseNumber(1 756,456;,)

## [!UICONTROL formatNumber (number; decimalPOINTS; [decimalSeparator]; [thousandsSeparator])]

Renvoie un nombre au format demandé. Par défaut, le point décimal est une virgule (,) et le séparateur des milliers est un point (.).

>[!BEGINSHADEBOX]

**Exemple :**

`formatNumber( 123456789 ; 3 ; , ; . )`

Renvoie 123.456.789,000

>[!ENDSHADEBOX]
