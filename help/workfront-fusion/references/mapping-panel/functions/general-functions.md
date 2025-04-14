---
title: Fonctions générales
description: Les fonctions générales suivantes sont disponibles dans le panneau de mappage dAdobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 6d4b8801-aa7e-47d4-80b3-aceac10c073f
source-git-commit: 295004ab7536b85124bc366d6832c08365338d08
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 52%

---

# Fonctions générales

## Variables

Vous pouvez utiliser deux variables générales pour identifier des détails sur une exécution :

* `executionID` : identifiant de l’exécution de ce scénario
* `triggerTimestamp` : heure de déclenchement de cette exécution

## [!UICONTROL get (object or array; path)]

Renvoie le chemin d’accès à la valeur d’un objet ou d’un tableau. Pour accéder aux objets imbriqués, utilisez la notation par points. Le premier élément d’un tableau est l’index 1.

>[!BEGINSHADEBOX]

**Exemples :**

* `get( array ; 1 + 1 )`
* `get( array ; 5.raw_name )`
* `get( object ; raw_name )`
* `get( object ; raw_name.sub_raw_name )`

>[!ENDSHADEBOX]

## [!UICONTROL if (expression; value1; value2)]

Renvoie la `value1` si l’expression est considérée comme true ; sinon elle renvoie la `value2`.

Pour créer une instruction if qui renvoie une valeur uniquement si plusieurs expressions sont évaluées sur true, utilisez le mot-clé `and`.

Pour combiner des instructions `if`, utilisez les opérateurs `and` et `or` .

![opérateur and](assets/and-in-if-statement.png)

>[!BEGINSHADEBOX]

**Exemples :**

* `if( 1 = 1 ; A ; B )`

  Renvoie A

* `if( 1 = 2 ; A ; B )`

  Renvoie B

* `if( 1 = 2 and 1 = 2 ; A ; B )`

  Renvoie B

>[!ENDSHADEBOX]

## [!UICONTROL ifempty (value1; value2)]

Renvoie la `value1` si cette valeur n’est pas vide ; sinon elle renvoie la `value2`.

>[!BEGINSHADEBOX]

**Exemples :**

* `ifempty(` `A` `;` `B` )

  Renvoie A

* `ifempty(` `unknown` `;` `B` )

  Renvoie B

* `ifempty(` `""` `;` `B` )

  Renvoie B

>[!ENDSHADEBOX]

## [!UICONTROL switch (expression; value1; result1; [value2; result2; ...]; [else])]

Évalue une valeur (appelée expression) par rapport à une liste de valeurs ; renvoie le résultat correspondant à la première valeur correspondante. Pour inclure une valeur `else`, ajoutez-la après l’expression ou la valeur finale.

>[!BEGINSHADEBOX]

**Exemples :**

* `switch( B ; A ; 1 ; B ; 2 ; C ; 3 )`

  Renvoie 2

* `switch( C ; A ; 1 ; B ; 2 ; C ; 3 )`

  Renvoie 3

* `switch( X ; A ; 1 ; B ; 2 ; C ; 3 ; 4 )`

  Renvoie 4

  Dans cette fonction, 4 est la valeur à renvoyer si aucune expression ne s’applique (la valeur `else`).

>[!ENDSHADEBOX]

## [!UICONTROL omit(object; key1; [key2; ...])]

Omet les clés données de l’objet et renvoie le reste.

>[!BEGINSHADEBOX]

**Exemple :**

`omit(` User `;` password `)`

Renvoie une collection des informations de l’utilisateur ou de l’utilisatrice, à l’exclusion du mot de passe.

>[!ENDSHADEBOX]

## [!UICONTROL pick(object; key1; [key2; ...])]

Sélectionne uniquement les clés données de l’objet.

>[!BEGINSHADEBOX]

**Exemple :**

`pick(` User `;` password `;` email `)`

Renvoie une collection contenant uniquement le mot de passe et l’adresse e-mail de l’utilisateur ou de l’utilisatrice.

>[!ENDSHADEBOX]

## mergeCollections(collection1 ; collection2)

Fusionne deux collections en combinant leurs paires clé-valeur. Si les deux collections contiennent la même clé, la valeur de la deuxième collection remplace celle de la première collection.
