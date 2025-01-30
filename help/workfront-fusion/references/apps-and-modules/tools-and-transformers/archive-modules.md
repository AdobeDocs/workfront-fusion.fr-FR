---
title: Modules Archive
description: Dans un scénario  [!DNL Adobe Workfront Fusion] , vous pouvez connecter une archive, comme un fichier compressé, à plusieurs applications et services tiers. Par exemple, vous pouvez configurer un scénario qui fait ce qui suit.
author: Becky
feature: Workfront Fusion
exl-id: 4b5ff3d5-601c-4119-ad70-3612ad5ba1ab
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 76%

---

# Modules [!UICONTROL Archive]

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez utiliser une archive, comme un fichier compressé, dans votre scénario, ce qui vous permet de l’utiliser dans vos automatismes ou vos intégrations.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

## Modules [!UICONTROL Archive] et leurs champs

Lorsque vous configurez les modules [!UICONTROL Archive], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!UICONTROL Archive] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [[!UICONTROL Extract an archive]](#extract-an-archive)
* [[!UICONTROL Create an archive]](#create-an-archive)
* [[!UICONTROL Inflate]](#inflate)
* [[!UICONTROL Deflate]](#deflate)

## [!UICONTROL Extract an archive]

Ce module d’action extrait d’une archive un fichier que vous avez identifié.

Le module renvoie l’ID du fichier et tous les champs associés, ainsi que les valeurs et les champs personnalisés auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p> Sélectionnez le fichier à extraire. Ce fichier peut être mappé à partir d’un module précédent (tel que le module [!DNL Workfront] &gt; [!UICONTROL Download a document]).</p>  </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Exemple :** récupérez le fichier ZIP du dossier [!DNL Dropbox] défini (par exemple, Archives), extrayez-le à l’aide du module [!UICONTROL Archive] et envoyez les fichiers extraits à l’adresse e-mail souhaitée en tant que pièces jointes avec le module [!UICONTROL Email] ou [!DNL Gmail].
>
>![Exemple de Dropbox ](/help/workfront-fusion/references/apps-and-modules/assets/example-dropbox-350x134.png)

## [!UICONTROL Create an archive]

Ce module d’agrégation ajoute les fichiers souhaités à une archive [!UICONTROL ZIP] ou [!UICONTROL TAR].

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module]</td> 
   <td> <p> Sélectionnez le module à partir duquel vous souhaitez récupérer les fichiers.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Type] </td> 
   <td> <p>Choisissez si vous souhaitez ajouter des fichiers à une archive [!UICONTROL ZIP] ou à une archive [!UICONTROL TAR].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Comment]</td> 
   <td>Saisissez un commentaire que vous souhaitez ajouter à l’archive.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Group by]</td> 
   <td> <p>Définissez une expression selon laquelle vous souhaitez regrouper la sortie agrégée. Cette expression peut contenir un ou plusieurs éléments mappés. Les données agrégées seront ensuite séparées en groupes à l’aide de la valeur de cette expression. Chaque groupe se présente sous la forme d’un lot distinct avec une clé (l’expression évaluée) et une valeur (le texte agrégé). Vous pouvez utiliser la clé comme filtre dans les modules suivants.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Stop processing after an empty aggregation]</td> 
   <td>Sélectionnez cette option pour arrêter le scénario lorsqu’il n’y a aucun résultat.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Archive name]</td> 
   <td> <p> Saisissez un nom pour l’archive créée. N’ajoutez pas d’extension.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Exemple :** surveiller les e-mails entrants à l’aide du module [!DNL Gmail] >[!UICONTROL Watch emails] . Si un e-mail est reçu, ses pièces jointes sont itérées en lots individuels, puis archivées dans le fichier [!DNL ZIP] et enregistrées dans le dossier Dropbox défini.
>
>![Exemple Gmail](/help/workfront-fusion/references/apps-and-modules/assets/example-gmail-350x102.png)

## [!UICONTROL Inflate]

Ce module transformateur décompresse les données binaires à l’aide d’un algorithme d’inflation.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data] </td> 
   <td> <p>Saisissez ou mappez les données que vous souhaitez décompresser à l’aide de la fonction de gonflage.</p> </td> 
  </tr> 
 </tbody> 
</table>

## [!UICONTROL Deflate]

Ce module de transformation compresse les données binaires à l’aide d’un algorithme de déflation.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data] </td> 
   <td> <p>Saisissez ou mappez les données que vous souhaitez compresser à l’aide de la fonction dégonfler.</p> </td> 
  </tr> 
 </tbody> 
</table>
