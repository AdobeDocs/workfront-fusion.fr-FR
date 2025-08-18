---
title: Analyseur de texte
description: Vous pouvez utiliser l’outil d’analyse de texte pour analyser le texte en vue de l’utiliser dans d’autres modules de scénario  [!DNL Adobe Workfront Fusion] . L’analyseur de texte ne nécessite pas de connexion.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 885d714e-fc09-41a2-89dc-ebe29a355e43
source-git-commit: 679a4f5c91625dfecf32e10904700bf75ea7a7cf
workflow-type: tm+mt
source-wordcount: '1311'
ht-degree: 85%

---

# [!UICONTROL Analyseur de texte]

Vous pouvez utiliser l’[!UICONTROL outil d’analyse de texte] pour analyser le texte en vue de l’utiliser dans d’autres modules de scénario [!DNL Adobe Workfront Fusion]. L’[!UICONTROL analyseur de texte] ne nécessite pas de connexion.

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
   <p>Aucune exigence de licence Workfront Fusion</p>
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

## Informations sur l’API de l’analyseur de texte

Le connecteur de l’analyseur de texte utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v2</td> 
  </tr>
 </tbody> 
 </table>

## Modules de l’[!UICONTROL analyseur de texte] et leurs champs

Lorsque vous configurez les modules de l’[!UICONTROL analyseur de texte], [!DNL Adobe Workfront Fusion] affiche les champs répertoriés ci-dessous. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Transformateurs

* [[!UICONTROL Obtenir des éléments à partir de HTML]](#get-elements-from-html)
* [[!UICONTROL Obtenir des éléments à partir de texte]](#get-elements-from-text)
* [[!UICONTROL HTML vers texte]](#html-to-text)
* [[!UICONTROL Motif correspondant]](#match-pattern)
* [[!UICONTROL Remplacer]](#replace)

#### [!UICONTROL Obtenir des éléments à partir de HTML]

Récupère les éléments souhaités à partir du code HTML.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Continue the execution of the route even if the module finds no matches]</td> 
   <td> <p>Activez cette option pour vous assurer que le module n’arrête pas le scénario s’il ne renvoie aucun résultat.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Element type]</td> 
   <td> <p> Sélectionnez le type d’élément que vous souhaitez récupérer dans le code HTML. </p> 
    <ul> 
     <li>[!UICONTROL Image]</li> 
     <li>[!UICONTROL Link]</li> 
     <li>[!UICONTROL iFrame element(s)]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL HTML] </td> 
   <td> <p>Saisissez ou mappez le code HTML à partir duquel vous souhaitez récupérer les types d’éléments spécifiés.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obtenir des éléments à partir de texte]

Analyse les éléments du texte en fonction du modèle donné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Input text]</td> 
   <td> <p>Saisissez ou mappez le texte à analyser.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Pattern]</td> 
   <td> <p>Sélectionnez le motif qui reflète les éléments que vous souhaitez analyser à partir du texte.</p> <p>Pour saisir une expression régulière personnalisée, sélectionnez Personnalisée dans la liste, puis saisissez l’expression personnalisée dans le champ Expression régulière personnalisée .</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Ignore Duplicate Occurrences]</td> 
   <td> <p>Cochez cette case pour ignorer les occurrences en double d’un élément de texte.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL HTML en texte]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL HTML] </td> 
   <td> <p>Saisissez le code HTML à convertir en texte brut.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Line break] </td> 
   <td> <p>Sélectionnez le type de nouvelle ligne (saut de ligne).</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Uppercase headings]</p> </td> 
   <td> <p>Activez cette option pour convertir le texte inclus dans les balises d’en-tête (telles que &lt;h2&gt; &lt;/h2&gt;) en texte en majuscules.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Motif correspondant]

Le module [!UICONTROL Motif correspondant] vous permet de rechercher et d’extraire des éléments de chaîne de caractères correspondant à un motif de recherche d’un texte donné. Ce module utilise des expressions régulières (également appelées regex ou regexp).

Une expression régulière est une séquence de caractères dans laquelle chaque caractère est soit un métacaractère, ayant une signification spéciale, soit un caractère régulier ayant une signification littérale. Ces caractères et métacaractères identifient un motif qui peut être utilisé pour rechercher du texte. Par exemple, si vous souhaitez rechercher des noms, vous pouvez configurer une expression régulière pour rechercher un motif constitué de deux mots consécutifs commençant par des majuscules. Les expressions régulières sont un puissant outil de recherche et de manipulation de texte.

Le présent article ne vise pas à aborder la question des expressions régulières. Nous vous recommandons les ressources suivantes :

* Pour obtenir la liste complète des métacaractères, voir [Expressions régulières](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions) dans la documentation web MDN.
* Pour un tutoriel sur la création d’expressions régulières, nous vous recommandons [RegexOne](https://regexone.com/).
* Pour expérimenter des expressions régulières, nous vous recommandons le site web [Regular Expressions 101](https://regex101.com/). Sélectionnez le ECMAScript (JavaScript) FLAVOR dans le panneau de gauche.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Pattern] </td> 
   <td> <p>Saisissez le motif d’expression régulière. </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Exemple : </b></span></span> <code>[+-]?(\d+(\.\d+)?|\.\d+)([eE][+-]?\d+)?</code> extrait tous les chiffres du texte fourni.</p> <p>Note :  <p>Le motif doit contenir au moins un groupe de capture entre parenthèses <code>()</code>. Si le motif ne contient aucun groupe de capture, le lot de sortie est vide.</p> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Global match]</td> 
   <td> <p>Activez cette option pour récupérer toutes les correspondances dans le texte. Chaque correspondance est générée dans un lot distinct. Si cette option est désactivée, le module récupère uniquement la première entrée.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Case sensitive]</td> 
   <td> <p> Activez cette option pour que ce module traite le texte comme étant sensible à la casse.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Multiline] </td> 
   <td> <p>Activez cette option pour vous assurer que les métacaractères de début et de fin (<code>^</code> et <code>$</code>) correspondent au début ou à la fin de chaque ligne, et pas seulement au début ou à la fin de l’ensemble de la chaîne de caractères d’entrée.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Singleline]</td> 
   <td>Activez cette option pour vous assurer que le point (.) correspond aux caractères de nouvelle ligne (<code>\n</code>).</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Continue the execution of the route even if the module returns no results]</td> 
   <td> <p>Activez cette option pour vous assurer que le module n’arrête pas le scénario s’il ne renvoie aucun résultat.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Text] </td> 
   <td> <p>Saisissez ou mappez le texte que vous souhaitez faire correspondre au motif.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remplacer]

Recherche une valeur ou une expression régulière dans le texte saisi et remplace le résultat par la nouvelle valeur.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Pattern] </td> 
   <td> <p>Saisissez le terme de recherche. Vous pouvez également utiliser une expression régulière. Pour plus d’informations sur l’expression régulière, voir le module <a href="#match-pattern" class="MCXref xref">[!UICONTROL Match Pattern]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL New value]</td> 
   <td> <p> Saisissez la valeur qui doit remplacer le terme de recherche.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Global match]</td> 
   <td> <p>Activez cette option pour récupérer toutes les correspondances dans le texte. Chaque correspondance est générée dans un lot distinct. Si cette option est désactivée, le module récupère uniquement la première entrée.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Case sensitive]</td> 
   <td> <p> Activez cette option pour que ce module traite le texte comme étant sensible à la casse.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Multiline] </td> 
   <td> <p>Activez cette option pour vous assurer que les métacaractères de début et de fin (<code>^</code> et <code>$</code>) correspondent au début ou à la fin de chaque ligne, et pas seulement au début ou à la fin de l’ensemble de la chaîne de caractères d’entrée.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Singleline]</td> 
   <td>Activez cette option pour vous assurer que le point (.) correspond aux caractères de nouvelle ligne (<code>\n</code>).</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Text] </td> 
   <td> <p>Saisissez le texte à rechercher.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Récupération de données

La récupération de données, parfois appelée web scraping, extraction des données ou web harvesting, est le processus de collecte de données à partir de sites web et de stockage de ces données dans votre base de données ou feuille de calcul locale. Si vous souhaitez récupérer les données d’un site web et que vous ne connaissez pas les expressions régulières, vous pouvez utiliser un outil de récupération de données.

Si l’outil de récupération de données fournit une API REST, vous pouvez vous y connecter via nos [[!UICONTROL modules HTTP]](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors) et [Webhooks](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md) universels.

## Dépannage de l’analyseur de texte

Utilisez ces informations si l’analyseur de texte échoue à produire une sortie.

>[!BEGINSHADEBOX]

Exemple :

Le module doit analyser le type de fichier d’un document de fichier « filename.docx », et l’extension du nom de fichier varie de DOCX à PDF et à CSV.

L’expression à utiliser dans ce cas est [!DNL \..+].

Cette expression régulière génère normalement une correspondance complète.

Cependant, l’implémentation de cette expression dans votre analyseur de texte n’entraîne pas de correspondance :

![Aucune correspondance](/help/workfront-fusion/references/apps-and-modules/assets/text-parser-you-dont-get-a-match-350x365.png)

Cela est dû au fait que la valeur « i » indique uniquement le nombre de correspondances par correspondance. Dans ce cas, nous avons deux correspondances, il y a donc après la valeur « i » une valeur numérique 1 et 2. Le cas d’utilisation à appliquer ici est que, si vous devez faire correspondre ou transférer des données via un filtre vers la seconde valeur correspondante, vous pouvez spécifier la valeur à l’aide de sa représentation numérique.

![Correspondance](/help/workfront-fusion/references/apps-and-modules/assets/text-parser-matches-350x355.png)

Pour obtenir les valeurs de correspondance dont vous avez besoin pour ajouter des intervalles à la partie que vous souhaitez analyser (par exemple, pour extraire uniquement « docx » de « filename.docx »), selon l’expression régulière que nous utilisons pour ce scénario, vous devez appliquer les intervalles sur \.(.+)

Cela capture « docx », le place dans un groupe et ignore « . » .

![Obtenir les correspondances](/help/workfront-fusion/references/apps-and-modules/assets/text-parser-get-matches-350x592.png)

Dans la sortie affichée dans l’image ci-dessous, le groupe de capture correspondra à n’importe quel caractère (sauf pour les terminaisons de ligne).

![Output](/help/workfront-fusion/references/apps-and-modules/assets/text-parser-output-350x389.png)

Une autre solution qui intègre également l’expression régulière consiste à utiliser la fonction Remplacer.

`{{replace("abcdefghijklmno pqr stuvw xyz.docx"; "/.\./"; ".")}}`

Remplacez alors `abcdefghijklmno pqr stuvw xyz.docx` avec votre variable de nom de fichier.

>[!ENDSHADEBOX]
