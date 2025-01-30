---
title: XML
description: L’application XML vous permet d’analyser un texte au format XML via le module XML > Parse XML et de le convertir en lot afin de rendre les données disponibles pour d’autres modules. Vous pouvez également convertir un lot en texte XML via XML > Créer un module XML.
author: Becky
feature: Workfront Fusion
exl-id: ab323361-cd04-4dcc-ab02-0fb468334fdb
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '1302'
ht-degree: 63%

---

# XML

L’application [!UICONTROL XML] vous permet d’analyser un texte au format XML via le module [!UICONTROL XML] > [!UICONTROL Parse XML] et de le convertir en lot pour rendre les données disponibles dans d’autres modules. Vous pouvez également convertir un lot en texte au format XML via le module [!UICONTROL XML] > [!UICONTROL Create XML] .

## Conditions d’accès

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] formule*</td>
  <td> <p>[!UICONTROL Pro] ou une version ultérieure</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licence*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licence**</td> 
   <td>
   <p>Exigences de licence actuelles : aucune exigence de licence [!DNL Workfront Fusion] requise.</p>
   <p>Ou</p>
   <p>Ancienne exigence de licence : [!UICONTROL [!DNL Workfront Fusion] pour l’automatisation et l’intégration du travail] </p>
   </td>  
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Exigences actuelles du produit : si vous disposez du plan de [!DNL Adobe Workfront] [!UICONTROL Select] ou [!UICONTROL Prime], votre entreprise doit acheter du [!DNL Adobe Workfront Fusion] et [!DNL Adobe Workfront] utiliser les fonctionnalités décrites dans cet article. [!DNL Workfront Fusion] est inclus dans le plan de [!DNL Workfront] [!UICONTROL Ultimate].</p>
   <p>Ou</p>
   <p>Exigences liées aux produits hérités : votre entreprise doit acheter [!DNL Adobe Workfront Fusion] ainsi qu’[!DNL Adobe Workfront] pour utiliser la fonctionnalité décrite dans cet article.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Pour connaître la formule, le type de licence ou l’accès dont vous disposez, contactez votre équipe d’administration [!DNL Workfront].

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## [!UICONTROL Parse XML]

Le module [!UICONTROL XML] > [!UICONTROL Parse XML] analyse un texte au format XML et génère un lot unique contenant toutes les informations extraites du fichier XML.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Data structure]</p> </td> 
   <td> <p>La structure de données décrit la structure du XML pour rendre la sortie du module disponible dans le panneau de mappage pour les modules suivants.</p> <p>Si vous disposez d’un exemple du XML que vous souhaitez analyser, vous pouvez l’utiliser pour générer la structure de données :</p> 
    <ol> 
     <li value="1">Cliquez sur le bouton <strong>[!UICONTROL Add]</strong> .</li> 
     <li value="2">Cliquez sur le bouton <strong>[!UICONTROL Generator]</strong> .</li> 
     <li value="3">Copiez et collez l’exemple XML dans le champ <strong>[!UICONTROL Sample data]</strong> .</li> 
     <li value="4">Cliquez sur <strong>[!UICONTROL Save]</strong>.</li> 
     <li value="5">Vérifiez que la structure de données a bien été générée.</li> 
     <li value="6"> <p>Cliquez sur le bouton <strong>[!UICONTROL Save]</strong> pour enregistrer la structure de données.</p> <p>Vous pouvez ignorer les étapes 2 à 5 pour fournir une structure de données vide. Si la structure de données est vide, la sortie du module n’est pas disponible dans le panneau de mappage tant que le module n’a pas été exécuté au moins une fois.</p> </li> 
    </ol> <p>Pour plus d’informations, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md" class="MCXref xref">Structures de données dans [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Preserve numbers as text]</td> 
   <td>Activez cette option pour vous assurer que les nombres restent des valeurs de texte (chaîne). Sinon, les nombres sont convertis en valeurs numériques.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL XML]</p> </td> 
   <td> <p>Saisissez ou mappez le texte XML formaté que vous souhaitez analyser.</p> <p>Si vous utilisez une formule, assurez-vous que son type de valeur de résultat est (ou peut être automatiquement forcé à) le type de données [!UICONTROL Text]. </p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/if-you-use-a-formula-350x164.png" style="width: 350;height: 164;"> </p> <p>Si le type de valeur de résultat est [!UICONTROL Buffer] (données binaires), utilisez la fonction <code>toString()</code> pour le convertir en type de données Texte. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type de coercition dans [!DNL Adobe Workfront Fusion]</a> et <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">Types de données d’élément dans [!UICONTROL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Exemple :** pour télécharger un fichier XML à partir d’une URL et analyser son contenu, procédez comme suit :
>
>1. Créez un scénario.
>1. Insérer un [!UICONTROL HTTP] > [!UICONTROL Get a file] un module
>1. Ouvrez la configuration du module et procédez comme suit :
>
>   **URL** : URL du fichier XML (par exemple, `https://siftrss.com/f/rqLy05ayMBJ`)
>
>   ![Exemple d’URL de fichier XML](/help/workfront-fusion/references/apps-and-modules/assets/url-of-xml-file-350x184.png)
>
>1. Cliquez sur **[!UICONTROL OK]**&#x200B;pour enregistrer et fermer la configuration du module.
1. Ajoutez le module [!UICONTROL XML] > [!UICONTROL Parse XML], connectez-le après le module [!UICONTROL HTTP] > [!UICONTROL Get a file] et configurez-le comme suit :
>
<table style="table-layout:auto"> 
&gt;    <col> 
&gt;    <col> 
&gt;    <tbody> 
&gt;     <tr> 
&gt;      <td role="rowheader">[!UICONTROL Data structure]</td> 
&gt;      <td> 
&gt;       <ol> 
&gt;        <li value="1">Cliquez sur le bouton <strong>[!UICONTROL Add]</strong> .</li> 
&gt;        <li value="2">Cliquez sur le bouton <strong>[!UICONTROL Generator]</strong> .</li> 
&gt;        <li value="3">Dans votre navigateur web, ouvrez un nouvel onglet ou une nouvelle fenêtre.</li> 
&gt;        <li value="4">Insérez l’URL que vous avez utilisée à la troisième étape dans la barre d’adresse et récupérez le fichier XML.</li> 
&gt;        <li value="5">Sélectionnez tout le texte XML et copiez-le dans le presse-papiers.</li> 
&gt;        <li value="6">Fermez l’onglet ou la fenêtre et revenez à votre scénario.</li> 
&gt;        <li value="7">Collez le texte XML copié dans le champ Données d’exemple.</li> 
&gt;        <li value="8">Cliquez sur <strong>[!UICONTROL Save]</strong>.</li> 
&gt;        <li value="9">Vérifiez que la structure de données a bien été générée.</li> 
&gt;        <li value="10">Cliquez sur <strong>[!UICONTROL Save]</strong> pour enregistrer la structure de données.</li> 
&gt;       </ol> <p>Vous pouvez ignorer les étapes 2 à 9 pour fournir une structure de données vide. Si la structure de données est vide, la sortie du module n’est pas disponible dans le panneau de mappage tant que le module n’a pas été exécuté au moins une fois.</p> </td> 
&gt;     </tr> 
&gt;     <tr> 
&gt;      <td role="rowheader">[!UICONTROL XML]</td> 
&gt;      <td> <p>Mappez l’élément <code>Data </code> à partir de la sortie du module [!UICONTROL HTTP] &gt; [!UICONTROL Get a file] dans le champ . Utilisez la fonction <code>toString()</code> pour convertir sa valeur du type [!UICONTROL Buffer] (données binaires) en type de données [!UICONTROL Text].</p> <p>Vous pouvez copier et coller le code de la formule dans le champ : <code>&#123;&#123;toString(1.data)&#125;&#125;</code></p> <p>Pour plus d’informations sur les types de données buffer et texte, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">Types de données des éléments dans Adobe Workfront Fusion</a>.</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/paste-formula-code-350x99.png" style="width: 350;height: 99;"> </p> </td> 
&gt;     </tr> 
&gt;    </tbody> 
&gt;   </table>

## [!UICONTROL Parsing XML attributes]

Par défaut, le module [!UICONTROL XML] > [!UICONTROL Parse XML] place les attributs dans un `_attributes` de collection spécial en tant qu’enfant du nœud qui possède ces attributs. Si le noeud est un noeud de texte doté d’attributs, deux propriétés spéciales sont ajoutées : `_attributes` pour les attributs et `_value` pour le contenu textuel du noeud.

>[!INFO]
>
**Exemple :** cet XML :

```
<root attr="1">
<node attr="ABC">Hello, World</node>
</root>
```

est converti en ce lot :

![XML converti en lot](/help/workfront-fusion/references/apps-and-modules/assets/xml-converted-to-bundle.png)

## Créer du XML

Le module [!UICONTROL XML] > [!UICONTROL Create XML] convertit un lot en texte au format XML.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Data structure]</p> </td> 
   <td> <p>La structure des données décrit la structure du XML obtenu. Si vous disposez d’un exemple du XML que vous souhaitez créer, vous pouvez l’utiliser pour générer la structure des données :</p> 
    <ol> 
     <li value="1">Cliquez sur le bouton <strong>[!UICONTROL Add]</strong> .</li> 
     <li value="2">Cliquez sur le bouton <strong>[!UICONTROL Generator]</strong> .</li> 
     <li value="3">Copiez et collez l’exemple XML dans le champ Données d’exemple.</li> 
     <li value="4">Cliquez sur le bouton <strong>[!UICONTROL Save]</strong> .</li> 
     <li value="5">Vérifiez que la structure de données a bien été générée.</li> 
     <li value="6">Cliquez sur <strong>[!UICONTROL Save]</strong> pour enregistrer la structure de données.</li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Root element name]</td> 
   <td>Saisissez le nom de l’élément racine du XML. La valeur par défaut est <code>root</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Doctype SYSTEM ID]</td> 
   <td>Saisissez le nom du fichier à utiliser dans la déclaration <code> !DOCTYPE SYSTEM</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Doctype PUBLIC ID]</td> 
   <td>Saisissez le nom du fichier à utiliser dans la déclaration <code> !DOCTYPE PUBLIC</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Strip Xml Declaration]</td> 
   <td>Activer cette option pour supprimer la déclaration XML <code>&lt;?xml ... ?&gt;</code> et <code>&lt;!DOCTYPE ... &gt;</code> et ne conserver que l’élément racine XML et son contenu.</td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
**Exemple :**
>
Un cas d’utilisation type consiste à transformer des données d’une feuille de calcul [!DNL Google] au format XML.
>
1. Placez le module [!DNL Google Sheets] > [!UICONTROL Select rows] dans votre scénario pour récupérer les données. Configurez le module pour récupérer les lignes de votre feuille de calcul [!DNL Google]. Définissez la variable &#x200B;**[!UICONTROL Maximum number of returned rows]** sur un petit nombre, mais plus grand qu’un à des fins de test (par exemple, trois). Exécutez le module [!DNL Google Sheets] en cliquant dessus avec le bouton droit et en choisissant « **[!UICONTROL Run this module only]** ». Vérifiez la sortie du module.
1. Connectez le module [!UICONTROL Array Aggregator] après le module [!DNL Google Sheets]. Dans la configuration du module, choisissez le module [!DNL Google Sheets] dans le champ **[!UICONTROL Source node]** . Laissez les autres champs tels quels pour le moment.
1. Connectez le module [!UICONTROL XML] > [!UICONTROL Create XML] après le module [!UICONTROL Array Aggregator] .
>
La configuration du module nécessite une structure de données qui décrit la structure de la sortie XML. Cliquez sur le bouton **[!UICONTROL Add]** pour ouvrir la configuration de la structure de données. La méthode la plus simple pour créer cette structure de données consiste à la générer automatiquement à partir d’un exemple XML.
>
1. Cliquez sur le bouton **[!UICONTROL Generator]** et collez votre exemple XML dans le champ [!UICONTROL Sample data] :
>
![Exemple de champ de données](/help/workfront-fusion/references/apps-and-modules/assets/sample-data-field-350x146.png)
>
1. Cliquez sur **[!UICONTROL Save]**. Le champ des spécifications de la structure de données contient désormais la structure générée.
1. Remplacez le nom de votre structure de données par un nom plus spécifique, puis cliquez sur **[!UICONTROL Save]**. Un champ correspondant à l’attribut de tableau racine apparaît comme champ mappable dans la configuration du module JSON.
1. Cliquez sur le bouton **[!UICONTROL Map]** en regard du champ et mappez l’élément de `Array[]` de la sortie [!UICONTROL Array aggregator] à celui-ci :
1. Cliquez sur **[!UICONTROL OK]** pour fermer la configuration du module XML.
1. Ouvrez la configuration du module [!UICONTROL Array Aggregator]. Remplacez le **[!UICONTROL Target structure]** Personnalisé par le champ d’un module XML correspondant aux éléments XML element.Map parents du module [!DNL Google Sheets] par les champs appropriés.
1. Cliquez sur **[!UICONTROL OK]** pour fermer la configuration du module Array Aggregator.
1. Exécutez le scénario.
>
Le module XML génère le fichier XML correct.
>
1. Ouvrez la configuration du module [!DNL Google Sheets] et augmentez le nombre de [!UICONTROL Maximum number of returned rows] pour qu’il soit supérieur au nombre de lignes de votre feuille de calcul afin de traiter toutes les données.
>
Le fichier XML obtenu peut être enregistré dans [!DNL Dropbox], envoyé en tant que pièce jointe par e-mail, chargé via FTP sur un serveur, etc.

## Ajouter des attributs XML

Si vous souhaitez ajouter des attributs à un nœud complexe (un nœud qui contiendra d’autres nœuds), vous devez ajouter, pour le nœud complexe, une collection portant le nom `_attributes` dans votre structure de données personnalisées. Cette collection sera mappée aux attributs du nœud. Si vous souhaitez ajouter des attributs à un nœud de texte (par exemple : `<node attr="1">abc</node>`), vous devez ajouter une collection `_attributes` pour les attributs et une propriété de texte `_value` pour la valeur de ce nœud dans votre structure de données personnalisées.

```
{
   "name": "node",
   "type": "collection",
   "spec": [
      {
         "name": "_attributes",
         "type": "collection"
         "spec": [
            {
               "name": "attr1",
               "type": "text"
            }
         ]
      },
      {
         "name": "_value",
         "type": "text"
      }
   ]
}
```

## Dépannage : impossible de mapper les données du module [!UICONTROL Parse XML]

Assurez-vous que la structure des données est correctement définie. Vous pouvez également utiliser une structure de données vide et exécuter le module au moins une fois pour traiter une entrée XML.
