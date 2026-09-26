---
title: Variables mathématiques
description: Les variables mathématiques suivantes sont disponibles dans le panneau [!DNL Adobe Workfront Fusion mapping].
author: Becky
feature: Workfront Fusion
exl-id: b309f035-4d46-473b-b915-6938587b0bcf
TQID: 'https://experienceleague.adobe.com/7vPwofVyFGdTGAXXuqbP5mmpPgSEK0JqimFqWu-UlJU'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 01689332f97c15b317e686d11a27cb4dc7e2e8bd
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 83%
---
# Variables mathématiques

## Pi

Représente le symbole mathématique $\pi$.

## [!UICONTROL Aléatoire]

Renvoie un nombre pseudo-aléatoire à virgule flottante dans l’intervalle [`0`,`1`] (incluant `0`, mais pas `1`).

Utilisez la formule suivante pour générer un nombre entier pseudo-aléatoire dans l’intervalle [`min`,`max`] (incluant `min` et `max`) :

![Random](assets/math-variable-random-350x61.png)

```
floor(random * (1.max - 1.min + 1)) + 1.min
```
