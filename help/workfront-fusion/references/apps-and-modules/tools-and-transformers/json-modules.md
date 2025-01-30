---
title: Modules JSON
description: L’application JSON d’Adobe Workfront Fusion fournit des modules pour traiter les données au format JSON afin qu’Adobe Workfront Fusion puisse continuer à travailler avec le contenu des données ou créer un nouveau contenu JSON.
author: Becky
feature: Workfront Fusion
exl-id: f8b281c5-bb63-4412-98c5-d82f45f8eafc
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '1129'
ht-degree: 63%

---

# Modules [!UICONTROL JSON]

L’application [!DNL Adobe Workfront Fusion] [!UICONTROL JSON] fournit des modules pour traiter les données au format JSON afin que [!DNL Adobe Workfront Fusion] puissiez continuer à utiliser le contenu des données ou créer du contenu JSON.

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tous</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licence Adobe Workfront</td> 
   <td> <p>Nouveau : Standard</p><p>Ou</p><p>En cours : Travail ou version ultérieure</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licence Adobe Workfront Fusion **</td> 
   <td>
   <p>Actuel : aucune exigence de licence Workfront Fusion.</p>
   <p>Ou</p>
   <p>Hérité : Workfront Fusion pour l’automatisation et l’intégration du travail </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Nouveau :</p> <ul><li>Sélectionnez ou le package Prime Workfront : votre entreprise doit acheter Adobe Workfront Fusion.</li><li>Package Ultimate Workfront : Workfront Fusion est inclus.</li></ul>
   <p>Ou</p>
   <p>Actuel : votre entreprise doit acheter Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Remarques concernant l’analyse JSON

* [Structure des données](#data-structure)
* [Collection ou tableau](#collection-vs-array)

### Structures des données

La structure des données décrit la manière dont les données JSON sont organisées et permet de mapper des éléments JSON individuels avec d’autres modules de votre scénario. Si vous ne fournissez pas la structure des données, vous pouvez exécuter manuellement le module et [!DNL Workfront Fusion] construira la structure à partir du JSON fourni :

1. Ajoutez le module [!UICONTROL Parse JSON] à un scénario.
1. Dans le champ **[!UICONTROL JSON String]** , saisissez le fichier JSON à partir duquel vous souhaitez créer une structure de données.
1. Ne connectez pas encore d’autres modules au module [!UICONTROL Parse JSON]. Comme [!DNL Workfront Fusion] ne connaît pas encore la structure des données JSON, il n’est pas encore possible de mapper les données du module [!UICONTROL Parse JSON] à d’autres modules dans votre scénario.
1. Exécutez manuellement le scénario. Cela permet au module [!UICONTROL Parse JSON] d’identifier la structure JSON à partir du fichier JSON que vous avez fourni.
1. Vous pouvez maintenant connecter les modules suivants. Les éléments du module Analyse JSON sont maintenant disponibles pour le mappage.

Pour plus d’informations, voir [Structures de données dans [!UICONTROL Adobe Workfront Fusion]](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

### Collection ou tableau

Si le champ Chaîne de caractères JSON contient une collection `{ ... }`, la sortie est un paquet unique contenant les éléments de la collection.

>[!BEGINSHADEBOX]

**Exemple :**

```
{
    "name" : "Peter",

    "ID" : 1>}
```


![ Collection JSON ](/help/workfront-fusion/references/apps-and-modules/assets/json-collection.png)

>[!ENDSHADEBOX]

Si le champ Chaîne de caractères JSON contient un tableau `[ ... ]`, la sortie est une série de paquets. Chaque paquet contient un élément du tableau.

>[!BEGINSHADEBOX]

**Exemple :**

```
[
  {
    "name" : "Peter",
    "ID" : 1
  },

  {
    "name" : "Mike",
    "ID" : 2
  }
]
```

![ Tableau JSON ](/help/workfront-fusion/references/apps-and-modules/assets/json-array.png)

>[!ENDSHADEBOX]

## Modules [!UICONTROL JSON] et leurs champs

Lorsque vous configurez les modules [!DNL JSON], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces champs, d’autres champs JSON peuvent s’afficher, en fonction de facteurs tels que votre niveau d’accès à l’application ou au service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Convertir JSON en XML](#convert-json-to-xml)
* [Analyser la chaîne JSON](#parse-json)
* [Créer une chaîne JSON](#create-json)
* [Transformer la chaîne JSON](#transform-json)

### Agrégateurs

#### [!UICONTROL Aggregate to JSON]

Ce module agrégateur regroupe les résultats d’un module précédent en chaîne JSON.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source module] </td> 
   <td> <p>Sélectionnez le module qui produit les données que vous souhaitez agréger en chaîne JSON.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data structure]</td> 
   <td> <p>Sélectionnez la structure de données que vous souhaitez utiliser pour créer la chaîne JSON. La structure des données détermine les autres champs disponibles dans ce module. Pour plus d’informations, voir <a href="#data-structure" class="MCXref xref">Structure des données</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Indentation]</td> 
   <td> <p> Indiquez si vous souhaitez indenter la chaîne JSON en utilisant des tabulations, deux espaces ou quatre espaces.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group by]</td> 
   <td>Définissez une expression selon laquelle vous souhaitez regrouper la sortie agrégée. Cette expression peut contenir un ou plusieurs éléments mappés. Les données agrégées sont ensuite séparées en groupes à l’aide de la valeur de cette expression. Chaque groupe se présente sous la forme d’un lot distinct avec une clé (l’expression évaluée) et une valeur (le texte agrégé). Vous pouvez utiliser la clé comme filtre dans les modules suivants.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stop processing after an empty aggregation]</td> 
   <td>Activez cette option pour arrêter le scénario lorsqu’il n’y a aucun résultat.</td> 
  </tr> 
 </tbody> 
</table>

### Transformateurs

* [Convertir JSON en XML](#convert-json-to-xml)
* [Créer une chaîne JSON](#create-json)
* [Analyser la chaîne JSON](#parse-json)
* [Transformer la chaîne JSON](#transform-json)

#### [!UICONTROL Convert JSON to XML]

Ce module d’action convertit une chaîne JSON en XML.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL JSON string] </td> 
   <td> <p>Saisissez ou mappez le code JSON que vous souhaitez convertir en XML.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create JSON]

Ce module d’action crée du code JSON à partir d’une structure de données.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Structures des données</td> 
   <td> <p>Sélectionnez la structure de données que vous souhaitez utiliser pour créer la chaîne JSON. Pour plus d’informations, voir <a href="#data-structure" class="MCXref xref">Structure des données</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Mise en retrait</td> 
   <td> <p>Sélectionnez la mise en retrait à utiliser pour ce fichier JSON.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Parse JSON]

Ce module d’action analyse une chaîne JSON dans une structure de données, ce qui vous permet d’accéder aux données contenues dans la chaîne JSON.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data structure]</td> 
   <td> <p>Sélectionnez la structure de données que vous souhaitez utiliser pour créer la chaîne JSON. Pour plus d’informations, voir <a href="#data-structure" class="MCXref xref">Structure des données</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL JSON string] </td> 
   <td> <p>Saisissez ou mappez le code JSON que vous souhaitez analyser.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Transform JSON]

Ce module d’action transforme un objet en une chaîne JSON.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Mise en retrait</td> 
   <td> <p>Sélectionnez la mise en retrait à utiliser pour ce fichier JSON.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object]</td> 
   <td> <p>Saisissez ou mappez l’objet que vous souhaitez transformer en chaîne JSON.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Transformation des enregistrements de données en chaîne JSON

>[!BEGINSHADEBOX]

**Exemple :** l’exemple suivant montre comment transformer des enregistrements de données de [!DNL Google Sheets] au format JSON :

1. Placez le module [!DNL Google Sheets] > [!UICONTROL Select rows] dans votre scénario pour récupérer les données. Configurez le module pour récupérer les lignes de votre feuille de calcul [!DNL Google]. Définissez la variable &#x200B;**[!UICONTROL Maximum number of returned rows]** sur un petit nombre, mais plus grand qu’un à des fins de test (par exemple, trois). Exécutez le module [!DNL Google Sheets] en cliquant dessus avec le bouton droit et en choisissant « **[!UICONTROL Run this module only]** ». Vérifiez la sortie du module.

1. Connectez le module [!UICONTROL Array Aggregator] après le module [!DNL Google Sheets]. Dans la configuration du module, choisissez le module [!DNL Google Sheets] dans le champ **[!UICONTROL Source node]** . Laissez les autres champs tels quels pour le moment.

1. Connectez-vous [!UICONTROL JSON] > module [!UICONTROL Create JSON] après le module [!UICONTROL Array Aggregator]. La configuration du module nécessite une structure de données qui décrit le format JSON. Cliquez sur **[!UICONTROL Add]** pour ouvrir la configuration de la structure de données. La manière la plus simple de créer cette structure de données est de la générer automatiquement à partir d’un exemple JSON. Cliquez sur **[!UICONTROL Generator]** et collez votre exemple JSON dans le champ **[!UICONTROL Sample data]** :

   **Exemple :**

   ```
   {
   "books": [
   {
   "id": "ID",
   "title": "Title",
   "author": "Author"
   }
   ]
   }
   ```

1. Cliquez sur **[!UICONTROL Save]**. Le champ [!UICONTROL Specification] dans la structure de données contient désormais la structure générée.
1. Remplacez le nom de votre structure de données par un nom plus spécifique, puis cliquez sur **[!UICONTROL Save]**. Un champ correspondant à l’attribut de tableau racine apparaît comme champ mappable dans la configuration du module JSON.

1. Cliquez sur le bouton **[!UICONTROL Map]** en regard du champ et mappez l’élément de `Array[]` de la sortie de l’agrégateur de tableau vers celui-ci.

1. Cliquez sur **[!UICONTROL OK]** pour fermer la configuration du module de [!UICONTROL JSON].

1. Ouvrez la configuration du module [!UICONTROL Array Aggregator]. Remplacez **[!UICONTROL Target structure]** de [!UICONTROL Custom] par le champ du module [!UICONTROL JSON] correspondant à l’attribut du tableau racine. Mappez les éléments du module [!DNL Google Sheets] aux champs appropriés.

1. Cliquez sur **[!UICONTROL OK]** pour fermer la configuration du module de [!UICONTROL Array Aggregator].

1. Exécutez le scénario.

   Le module [!UICONTROL JSON] génère le format JSON correct.

1. Ouvrez la configuration du module [!DNL Google Sheets] et augmentez le nombre de [!UICONTROL Maximum number of returned rows] pour qu’il soit supérieur au nombre de lignes de votre feuille de calcul afin de traiter toutes les données.

>[!ENDSHADEBOX]

## Dépannage

### Impossible de mapper les données du module [!UICONTROL Parse JSON]

Assurez-vous que le contenu JSON est correctement mappé dans le module [!UICONTROL Parse JSON] et que la structure des données est correctement définie. Pour plus d’informations, voir [Transformer des enregistrements de données en JSON](#transforming-data-records-to-json) dans cet article.

### Le module échoue lors de l’utilisation d’instructions conditionnelles dans JSON.

Lorsque vous utilisez des instructions conditionnelles telles que `if` dans JSON, mettez les guillemets à l’extérieur de l’instruction conditionnelle.

>[!BEGINSHADEBOX]

**Exemple :**

![Citations dans JSON](/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png)

>[!ENDSHADEBOX]
