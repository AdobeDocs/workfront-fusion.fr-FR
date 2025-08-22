---
title: Modules d’image
description: Les modules d’image Adobe Workfront Fusion vous permettent d’obtenir des informations sur une image spécifique (dimensions, type, etc.), de convertir une image dans un autre format de fichier et de modifier directement la taille de l’image.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: a7696c9d-002d-4bb4-ae10-1f69dc5e66fe
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '752'
ht-degree: 75%

---

# Modules d’image

Les modules Adobe Workfront Fusion [!UICONTROL Image] vous permettent d’obtenir des informations sur une image spécifique (dimensions, type, etc.), de convertir une image dans un autre format de fichier et de modifier directement la taille de l’image.

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

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Modules d’[!UICONTROL image] et leurs champs

Lorsque vous configurez ce module, les champs suivants s’affichent. Un titre en gras dans un module indique un champ obligatoire.

* [[!UICONTROL Convertir un format]](#convert-a-format)
* [[!UICONTROL Extraire les métadonnées]](#extract-metadata)
* [[!UICONTROL Redimensionner]](#resize)

### [!UICONTROL Convertir un format]

Ce module du transformateur modifie le format d’un fichier image. Ce module est compatible avec les formats suivants :

* PNG
* JPG
* GIF
* BMP

Le fichier source et la sortie doivent être dans l’un de ces formats. Par exemple, le module [!UICONTROL Image] > [!UICONTROL Convertir un format] peut transformer un fichier PNG en fichier BMP ou un fichier BMP en JPG.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output format]</td> 
   <td>Sélectionnez le format dans lequel vous souhaitez que le module convertisse le fichier source. </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Extraire les métadonnées]

Ce module du transformateur renvoie des informations de base sur un module.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Redimensionner]

Ce module du transformateur modifie la hauteur et la largeur d’une image en fonction des critères que vous spécifiez.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </td> 
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
  <tr> 
   <td role="rowheader">[!UICONTROL Change by percentage]</td> 
   <td>Si vous avez choisi de modifier l’image en pourcentage, saisissez ou mappez le pourcentage selon lequel vous souhaitez modifier l’image.</td> 
  </tr> 
 </tbody> 
</table>

## Dépannage

### Action terminée avec une erreur

une action peut se terminer par une erreur pour l’une des raisons suivantes :

* Les données reçues ne sont pas au format JPG/GIF/PNG/BMP.
* La limite largeur/hauteur maximale a été dépassée lors de la modification des dimensions de l’image. La taille de l’image ne doit pas dépasser 3 840 pixels de largeur et 2 160 pixels de hauteur.
* La taille maximale autorisée d’une image a été dépassée lors de la modification des dimensions ou du format de l’image.
