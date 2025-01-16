---
title: Variables mathématiques
description: Les variables mathématiques suivantes sont disponibles dans le panneau  [!DNL Adobe Workfront Fusion mapping] .
author: Becky
feature: Workfront Fusion
exl-id: b309f035-4d46-473b-b915-6938587b0bcf
source-git-commit: 24a6c1558fd6349c022df8a1847a7f39fafddd67
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 91%

---

# Variables mathématiques

## Pi

Représente le symbole mathématique $\pi$.

## [!UICONTROL random]

Renvoie un nombre pseudo-aléatoire à virgule flottante dans l’intervalle [`0`,`1`] (incluant `0`, mais pas `1`).

Utilisez la formule suivante pour générer un nombre entier pseudo-aléatoire dans l’intervalle [`min`,`max`] (incluant `min` et `max`) :

![](assets/math-variable-random-350x61.png)

```
floor(random * (1.max - 1.min + 1)) + 1.min
```
