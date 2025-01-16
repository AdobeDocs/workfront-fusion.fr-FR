---
title: Modules d’image
description: Les modules d’image Adobe Workfront Fusion vous permettent d’obtenir des informations sur une image spécifique (dimensions, type, etc.), de convertir une image dans un autre format de fichier et de modifier directement la taille de l’image.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: a7696c9d-002d-4bb4-ae10-1f69dc5e66fe
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 81%

---

# Modules d’image

[!DNL Adobe Workfront Fusion] modules [!UICONTROL Image] vous permettent d’obtenir des informations sur une image spécifique (dimensions, type, etc.), de convertir une image dans un autre format de fichier et de modifier directement la taille de l’image.

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
   <p>Ancienne exigence de licence : [!UICONTROL [!DNL Workfront Fusion] pour l’automatisation et l’intégration du travail], [!UICONTROL [!DNL Workfront Fusion] pour l’automatisation du travail]</p>
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

## Modules [!UICONTROL Image] et leurs champs

Lorsque vous configurez ce module, les champs suivants s’affichent. Un titre en gras dans un module indique un champ obligatoire.

* [[!UICONTROL Resize]](#resize)
* [[!UICONTROL Convert a format]](#convert-a-format)
* [[!UICONTROL Extract metadata]](#extract-metadata)

### [!UICONTROL Resize]

Ce module du transformateur modifie la hauteur et la largeur d’une image en fonction des critères que vous spécifiez.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez la source de l’image que vous souhaitez convertir. Vous pouvez sélectionner la sortie d’un module précédent ou mapper le fichier de données et le nom de fichier. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data]</td> 
   <td>Mappez le fichier que vous souhaitez convertir. Ce champ est disponible si vous avez sélectionné [!UICONTROL Map] dans le champ [!UICONTROL Source file] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td>Saisissez un nom pour le fichier converti. Ce champ est disponible si vous avez sélectionné [!UICONTROL Map] dans le champ [!UICONTROL Source file] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL I want to]</td> 
   <td>Indiquez si vous souhaitez conserver les proportions ou modifier les dimensions selon une hauteur et une largeur spécifiées.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL According to]</td> 
   <td> <p>Sélectionnez la manière dont vous souhaitez que le module détermine la nouvelle taille de l’image. Ce champ s’affiche si vous avez choisi de conserver les proportions dans le champ Je veux. D’autres champs s’affichent en fonction de la sélection effectuée dans ce champ.</p> 
    <ul> 
     <li> <p>[!UICONTROL Maximum width]</p> <p>Réduit une image à une largeur que vous spécifiez. La hauteur est calculée automatiquement.</p> </li> 
     <li> <p>[!UICONTROL Maximum height]</p> <p>Réduit une image à une hauteur que vous spécifiez. La largeur est calculée automatiquement.</p> </li> 
     <li> <p>[!UICONTROL Maximum height or width]</p> <p>Réduit une image de sorte que sa hauteur et sa largeur ne dépassent pas les valeurs que vous spécifiez. Comme cette option conserve les proportions, l’une des dimensions peut être plus petite que celle spécifiée. Par exemple, si la hauteur et la largeur sont toutes deux définies sur 40, une image de 400x300 sera réduite à 40x30.</p> </li> 
     <li> <p>[!UICONTROL Minimum width]</p> <p>Agrandit une image à une largeur que vous spécifiez. La hauteur est calculée automatiquement.</p> </li> 
     <li> <p>[!UICONTROL Minimum height]</p> <p>Agrandit une image à une hauteur que vous spécifiez. La largeur est calculée automatiquement.</p> </li> 
     <li> <p>[!UICONTROL Minimum height or width]</p> <p>Agrandit une image de sorte que sa hauteur et sa largeur ne soient pas inférieures aux valeurs que vous spécifiez. Comme cette option conserve les proportions, l’une des dimensions peut être plus grande que celle spécifiée. Par exemple, si la hauteur et la largeur sont toutes deux définies sur 300, une image de 40x30 sera agrandie à 400x300.</p> </li> 
     <li> <p>[!UICONTROL Percent]</p> <p>Modifie la taille de l’image d’un pourcentage en fonction de la valeur que vous spécifiez. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Width]</td> 
   <td>Saisissez ou mappez la largeur souhaitée de l’image redimensionnée en pixels.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Height]</td> 
   <td>Saisissez ou mappez la hauteur souhaitée de l’image redimensionnée en pixels.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Convert a format]

Ce module du transformateur modifie le format d’un fichier image. Ce module est compatible avec les formats suivants :

* PNG
* JPG
* GIF
* BMP

Le fichier source et la sortie doivent être dans l’un de ces formats. Par exemple, le module [!UICONTROL Image] >[!UICONTROL Convert a format] peut transformer un fichier PNG en fichier BMP, ou un fichier BMP en mot de passe JPG.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez la source de l’image que vous souhaitez convertir. Vous pouvez sélectionner la sortie d’un module précédent ou mapper le fichier de données et le nom de fichier. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data]</td> 
   <td>Mappez le fichier que vous souhaitez convertir. Ce champ est disponible si vous avez sélectionné [!UICONTROL Map] dans le champ [!UICONTROL Source file] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td>Saisissez un nom pour le fichier converti. Ce champ est disponible si vous avez sélectionné [!UICONTROL Map] dans le champ [!UICONTROL Source file] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output format]</td> 
   <td>Sélectionnez le format dans lequel vous souhaitez que le module convertisse le fichier source. </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Extract metadata]

Ce module du transformateur renvoie des informations de base sur un module.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez la source de l’image que vous souhaitez convertir. Vous pouvez sélectionner la sortie d’un module précédent ou mapper le fichier de données et le nom de fichier. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data]</td> 
   <td>Mappez le fichier que vous souhaitez convertir. Ce champ est disponible si vous avez sélectionné Mapper dans le champ [!UICONTROL Source file] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td>Saisissez un nom pour le fichier converti. Ce champ est disponible si vous avez sélectionné Mapper dans le champ [!UICONTROL Source file] .</td> 
  </tr> 
 </tbody> 
</table>

## Problèmes possibles

### Action terminée avec une erreur

Il existe trois cas dans lesquels une action peut se terminer par une erreur :

* Les données reçues n’étaient pas au format JPG/GIF/PNG/BMP.
* La limite de largeur/hauteur maximale a été dépassée lors de la modification des dimensions de l’image. La taille de l’image ne doit pas dépasser 3 840 pixels de largeur et 2 160 pixels de hauteur.
* La taille maximale autorisée d’une image a été dépassée lors de la modification des dimensions ou du format de l’image.
