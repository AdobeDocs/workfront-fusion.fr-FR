---
title: Fonctions générales
description: Les fonctions générales suivantes sont disponibles dans le panneau de mappage dAdobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 6d4b8801-aa7e-47d4-80b3-aceac10c073f
TQID: 'https://experienceleague.adobe.com/1IX25ZtrWVizi5gZJfFw-acnW5eIuXpGgcXgXW0T-Hw'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 8ea986eb6573bb49accfad312bb0796faa2642ab
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 25%
---
# Fonctions générales

## Variables

Vous pouvez utiliser ces variables générales pour identifier les détails d’une exécution :

* `executionId` : identifiant de l’exécution de ce scénario
* `scenarioId` : ID du scénario en cours d’exécution
* `scenarioName` : nom du scénario en cours d’exécution
* `scenarioUrl` : lien vers le scénario actuel dans l’interface utilisateur de Fusion.
* `executionUrl` : lien vers l’exécution actuelle du scénario dans l’interface utilisateur de Fusion.
* `scenarioApiUrl` : URL de l’API Fusion pour le scénario actuel.
* `executionApiUrl` : URL de l’API Fusion pour les détails de l’exécution en cours.
* `teamId` : identifiant de l’équipe Fusion propriétaire du scénario actuel.
* `organizationId` : ID de l’organisation Fusion associé à l’exécution en cours. Il ne s’agit pas d’un identifiant d’organisation Adobe IMS.
* `triggerTimestamp` : heure de déclenchement de cette exécution
* `operationsConsumed` : nombre d’opérations utilisées à ce stade du scénario.

Les noms de variables sont sensibles à la casse. Par exemple, utilisez `scenarioUrl`, pas `scenarioURL`.

Vous pouvez utiliser ces variables dans des champs mappés sans créer d’URL ni d’ID d’équipe et d’organisation de codage en dur. Par exemple, vous pouvez inclure les éléments suivants dans un champ de texte mappé d’une notification :

<pre><code>
Scenario: &#123;&#123;scenarioName&#125;&#125;
Open scenario: &#123;&#123;scenarioUrl&#125;&#125;
Open execution: &#123;&#123;executionUrl&#125;&#125;
Team: &#123;&#123;teamId&#125;&#125;
Organization: &#123;&#123;organizationId&#125;&#125;
</code></pre>

Gardez les points suivants à l’esprit lorsque vous utilisez ces variables :

* Les valeurs sont résolues lors de l’exécution du scénario. Le panneau de mappage répertorie les variables, mais il ne prévisualise pas leurs valeurs.
* `scenarioUrl` et `executionUrl` le lien vers le scénario et vers l’exécution dans l’interface utilisateur de Fusion. `scenarioApiUrl` et `executionApiUrl` sont des URL de point d’entrée de l’API, et non des liens vers des pages Fusion.
* Les variables d’URL d’API renvoient uniquement du texte. Ils n’effectuent pas de requête et ne fournissent pas d’informations d’authentification. L’authentification et les autorisations normales de l’API s’appliquent toujours.
* Les liens n’accordent pas d’accès supplémentaire. Les autorisations normales de Fusion s’appliquent.
* `executionUrl` n’est pas généré pour les exécutions qui ne sont pas enregistrées dans l’historique d’exécution, telles que les exécutions de sandbox ou les exécutions pour lesquelles la synchronisation de l’historique est désactivée. Un lien généré ne garantit pas que les détails d’exécution sont disponibles au moment où vous l’utilisez.
* `scenarioUrl` ne peut pas être généré pour un modèle ou un scénario non enregistré.
* Si une URL ne peut pas être générée, la variable n’a pas de valeur.

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

### [!UICONTROL isBlank(value)]

Renvoie `true` si la valeur est `null` ou une chaîne vide, sinon renvoie `false`. Contrairement à `ifEmpty`, cette fonction ne traite pas les `0` numériques ou les chaînes contenant uniquement des espaces comme vides.

>[!BEGINSHADEBOX]

**Exemple :**

* `isBlank("")     `

  Renvoie vrai
* `isBlank(null)   `

  Renvoie vrai
* `isBlank("Hello")`

  Renvoie false
* `isBlank(0)      `

  Renvoie false
* `isBlank(" ")    `

  Renvoie false

>[!ENDSHADEBOX]


### [!UICONTROL in(value; value1; value2; ...)]

Renvoie `true` si la valeur est égale à l’une des valeurs fournies (égalité stricte, aucune coercition de type).

>[!BEGINSHADEBOX]

**Exemple :**

* `in("B"; "A"; "B"; "C")`

  Renvoie vrai
* `in("D"; "A"; "B"; "C")`

  Renvoie false
* `in(2; 1; 2; 3)        `

  Renvoie vrai
* `in("2"; 1; 2; 3)      `

  Renvoie false

>[!ENDSHADEBOX]

### [!UICONTROL ifin(value; value1; value2; ...; trueExpression; falseExpression)]

Renvoie `trueExpression` si la valeur correspond à l’une des valeurs de correspondance fournies, sinon renvoie `falseExpression`. Requiert au moins 3 arguments (valeur, une valeur de correspondance et trueExpression + falseExpression).

>[!BEGINSHADEBOX]

**Exemple :**

* `ifin("B"; "A"; "B"; "yes"; "no")`

  Renvoie oui
* `ifin("D"; "A"; "B"; "yes"; "no")`

  Renvoie no
* `ifin("X"; "X"; "found"; "not found")`

  Renvoie trouvée

>[!ENDSHADEBOX]

### [!UICONTROL case(indexNumber; value1; value2; ...)]

Renvoie la valeur à la position spécifiée par le numéro d&#39;index (basé sur 1). Renvoie `null` si l’index est hors limites ou est égal à 0.

>[!BEGINSHADEBOX]

**Exemple :**

* `case(1; "Sun"; "Mon"; "Tue")`

  Renvoie Sun
* `case(2; "Sun"; "Mon"; "Tue")`

  Renvoie Lun
* `case(3; "Sun"; "Mon"; "Tue")`

  Renvoie True
* `case(5; "a"; "b")           `

  Renvoie null

>[!NOTE]
>
>Nous vous recommandons d’utiliser cette option pour obtenir le nom du jour à partir d’une date :
>`case(dayOfWeek(date); "Sun"; "Mon"; "Tue"; "Wed"; "Thu"; "Fri"; "Sat")`

>[!ENDSHADEBOX]

