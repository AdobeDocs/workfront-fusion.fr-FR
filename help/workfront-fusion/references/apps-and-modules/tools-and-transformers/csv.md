---
title: CSV
description: Les modules CSV d’Adobe Workfront Fusion vous permettent de créer des fichiers CSV et d’analyser du texte CSV à partir d’une valeur textuelle reçue ou d’un fichier.
author: Becky
feature: Workfront Fusion
exl-id: bc6d5ddc-93c3-437b-8537-5bece1351c1d
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 48%

---

# CSV

Les modules Adobe Workfront Fusion [!UICONTROL CSV] vous permettent de créer des fichiers CSV et d’analyser le texte CSV à partir d’une valeur de texte reçue ou d’un fichier.

Comme il s&#39;agit d&#39;un transformateur, ces modules ne nécessitent pas de connexion.

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tout package de workflow Adobe Workfront et tout package d’automatisation et d’intégration Adobe Workfront</p><p>Workfront Ultimate</p><p>les packages Workfront Prime et Select, avec un achat supplémentaire de Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licences Adobe Workfront</td> 
   <td> <p>Standard</p><p>Travail ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Si votre entreprise dispose d’un package Select ou Prime Workfront qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acheter Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++



## [!UICONTROL Créer un CSV]

L’agrégateur [!UICONTROL Créer CSV] vous permet de créer un texte CSV à partir de valeurs de texte reçues.

Pour plus d’informations sur les agrégateurs, voir [Module Agrégateur](/help/workfront-fusion/references/modules/aggregator-module.md).

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Source Module]</td>
        <td>Sélectionnez le module qui génère les champs que vous souhaitez utiliser pour créer le fichier CSV.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Aggregated Fields]</td>
        <td>Sélectionnez les champs que vous souhaitez agréger dans la liste des champs disponibles.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Include headers in the first row]</td>
        <td>Sélectionnez cette option pour inclure les en-têtes dans le résultat.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Group by]</td>
        <td>Saisissez le filtre pour grouper les résultats. Par exemple, saisissez une date.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Stop processing after an empty aggregation]</td>
        <td>Sélectionnez cette option pour arrêter le scénario lorsqu’il n’y a aucun résultat.</td>
    </tr>
</table>

## [!UICONTROL Créer un CSV (avancé)]

L’agrégateur [!UICONTROL Créer un CSV (avancé)] vous permet de créer un texte CSV à partir de valeurs de texte reçues. Il utilise une structure de données qui définit les colonnes CSV dans le fichier CSV résultant. Une fois définies, les colonnes apparaissent comme des champs dans la configuration du module CSV et peuvent être mappées à d’autres modules du scénario.

Pour plus d’informations sur les agrégateurs, voir [Module Agrégateur](/help/workfront-fusion/references/modules/aggregator-module.md).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
        <td>Sélectionnez le module qui génère les champs que vous souhaitez utiliser pour créer le fichier CSV.</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data Structure]</td> 
   <td> <p>Sélectionnez la structure de données pour agréger les champs comme vous le souhaitez. Après avoir défini la structure des données, vous pouvez mapper les éléments aux champs correspondants.</p> <p>Pour plus d’informations, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md" class="MCXref xref">Structures de données</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Include headers in the first row] </td> 
   <td>Sélectionnez cette option pour inclure les en-têtes dans le résultat. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group by] </td> 
   <td>Saisissez le filtre pour grouper les résultats. Par exemple, saisissez une date. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stop processing after an empty aggregation] </td> 
   <td>Sélectionnez cette option pour arrêter le scénario lorsqu’il n’y a aucun résultat. </td> 
  </tr> 
 </tbody> 
</table>


>[!BEGINSHADEBOX]

**Exemple** :

Cet exemple montre comment exporter des contacts Google dans un fichier CSV avec deux colonnes appelées « Nom complet » et « E-mail ». Le lot de sortie du module [!UICONTROL Contacts Google] > [!UICONTROL Obtenir les contacts d&#39;un groupe] présente la structure suivante. Les adresses e-mail sont stockées dans le <code>[!UICONTROL  E-mails []]</code> item, qui est un tableau de collections, chaque collection contenant deux éléments : <code>Label</code> et <code>E-mail</code>.
![Transformation](/help/workfront-fusion/references/apps-and-modules/assets/transforming-350x546.png)

Le module [!DNL Create CSV] simple propose une liste de cases à cocher correspondant aux éléments de niveau supérieur d’un lot. Si vous tentez de sélectionner <code>Nom complet</code> et <code>E-mails</code> , le module [!UICONTROL Créer CSV] génère la sortie suivante, qui peut ne pas être celle que vous souhaitez :

```
"emails","fullName"
"[object Object]","Shon Winer"
"[object Object]","Lizeth Fulmore"
"[object Object]","Hilario Gullatt"
"[object Object]","Abby Eisenbarth"
```

Parce que l’élément <code>Nom complet</code> est de type Texte simple, il est exporté comme prévu. L’élément <code>E-mails</code>, qui est d’un tableau de collections de type complexe, est exporté en tant qu’[objet Object], qui correspond à la manière dont les collections et les tableaux sont transformés en texte par défaut.

Pour plus d’informations, voir [Types de données d’élément](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md).


Pour exporter le contenu de l’e-mail <code> </code>élément de la première collection des <code>Emails[]</code> Au lieu de cela, vous devez utiliser le module [!UICONTROL Créer CSV (avancé)]. Ce module vous permet de définir des colonnes individuelles de votre fichier CSV et de mapper des éléments à celles-ci, y compris les colonnes imbriquées.

1. Insérez le module [!UICONTROL Créer un fichier CSV (avancé)] dans un scénario.
1. Cliquez sur le bouton <strong>[!UICONTROL Ajouter]</strong> en regard du champ [!UICONTROL Structure de données] pour créer une structure de données.
1. Saisissez le nom de la structure de données et cliquez sur <strong>[!UICONTROL Ajouter un élément]</strong> pour ajouter les différentes colonnes. Pour exporter deux colonnes : « Nom complet » et « E-mail », la structure de données résultante ressemblerait à ceci :

   ![Sortie des contacts Google](/help/workfront-fusion/references/apps-and-modules/assets/google-contacts-350x524.png)

1. Une fois la structure des données définie, les champs correspondant à chaque colonne individuelle apparaissent dans la configuration du module [!UICONTROL Créer CSV (avancé)] afin que vous puissiez mapper les éléments. Prenez le premier élément de la <code>[!UICONTROL E-mails[]]</code> tableau et mapper son élément <code>E-mail </code>dans le champ/la colonne E-mail :

   ![Créer un module CSV avancé](/help/workfront-fusion/references/apps-and-modules/assets/create-csv-advanced-350x308.png)

1. Exécutez le scénario. Parce que l’élément <code>E-mails[1] : E-mail</code> Associé à la colonne « E-mail » est de type Texte simple, il s’exporte correctement.

```
"Full Name","Email"
"Shon Winer","Shon@Winer.com"
"Lizeth Fulmore","Lizeth@Fulmore.com"
"Hilario Gullatt","Hilario@Gullatt.com"
"Abby Eisenbarth","Abby@Eisenbarth.com"
```

>[!ENDSHADEBOX]

## [!UICONTROL Analyse CSV]

Le transformateur [!UICONTROL Analyse CSV] vous permet d’analyser un texte CSV à partir d’une valeur textuelle reçue ou d’un fichier.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of columns]</td> 
   <td>Indiquez le nombre de colonnes dans le fichier CSV.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL CSV contains headers]</td> 
   <td> <p>Sélectionnez cette option si la première ligne du texte CSV contient des en-têtes.</p> <p>Note : le module n’utilise pas ces en-têtes pour étiqueter les colonnes dans le résultat. En revanche, ce champ garantit que les en-têtes ne sont pas inclus dans les données de sortie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL delimiterType]</td> 
   <td> <p>Sélectionnez le délimiteur pour le fichier CSV. Le délimiteur est le caractère de texte qui indique la limite entre des valeurs ou des champs distincts.</p> 
    <ul> 
     <li>[!UICONTROL Comma]</li> 
     <li>[!UICONTROL Tab]</li> 
     <li> <p>[!UICONTROL Other]</p> <p>Si vous sélectionnez [!UICONTROL Other], saisissez le caractère de délimitation que le fichier CSV utilise pour séparer les valeurs. Vous devez saisir exactement un caractère.<br></p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Preserve quotes inside unquoted field]</td> 
   <td>Activez cette option pour conserver les quillemets.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL CSV]</td> 
   <td>Saisissez ou mappez le fichier CSV que vous souhaitez analyser.<p>Note : <p>Si vos données sont sous forme binaire (typiquement à partir d’un fichier), vous devez utiliser la fonction toString() pour convertir les données binaires en [!UICONTROL String] :</p><p><img src="/help/workfront-fusion/references/apps-and-modules/assets/parse-csv-350x123.png"></p></p></td> 
  </tr> 
 </tbody> 
</table>
