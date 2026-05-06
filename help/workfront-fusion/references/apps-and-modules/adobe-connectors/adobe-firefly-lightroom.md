---
title: Modules Adobe Firefly
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent Adobe Firefly Lightroom et les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3b29ba3d-a769-4e97-b2c2-0b4eeed5b029
source-git-commit: 965cb643039be36eb3608cd801439a6a055974e4
workflow-type: tm+mt
source-wordcount: '1430'
ht-degree: 17%

---

# Modules Adobe Firefly Lightroom

<!--add to tocs-->

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent Adobe Firefly Lightroom et les connecter à plusieurs applications et services tiers.

Si vous avez besoin d’instructions pour créer un scénario, consultez les articles sous [Créer un scénario : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tout package de workflow Adobe Workfront et tout package d’automatisation et d’intégration Adobe Workfront</p><p>Workfront Ultimate</p><p>Packages Workfront Prime et Select, avec l’achat supplémentaire de Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licences Adobe Workfront</td> 
   <td> <p>Standard</p><p>Travail ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licence Adobe Workfront Fusion</td> 
   <td>
   <p>Basé sur les opérations : aucune exigence de licence Workfront Fusion</p>
   <p>Basé sur un connecteur (hérité) : Workfront Fusion pour l’automatisation et l’intégration du travail </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Si votre organisation dispose d’un package Workfront Select ou Prime qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acquérir Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences Adobe Workfront Fusion, consultez [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Conditions préalables

Avant de pouvoir utiliser le connecteur Lightroom Adobe Firefly, vous devez vérifier que les conditions préalables suivantes sont remplies :

* Vous devez disposer d’un compte Adobe Firefly Lightroom actif.

## Création d’une connexion à Adobe Firefly Lightroom

Pour créer une connexion pour vos modules Adobe Firefly Lightroom :

1. Dans n’importe quel module, cliquez sur **[!UICONTROL Ajouter]** en regard de la zone Connexion .

1. Remplissez les champs suivants :

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">Nom de la connexion</td>
        <td>
          <p>Saisissez un nom pour cette connexion.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">Environnement</td>
        <td>Indiquez si vous vous connectez à un environnement de production ou hors production.</td>
        </tr>
        <tr>
        <td role="rowheader">Type</td>
        <td>Indiquez si vous vous connectez à un compte de service ou à un compte personnel.</td>
        </tr>
        <tr>
        <td role="rowheader">ID client</td>
        <td>Saisissez votre identifiant client Adobe. Vous trouverez cette information dans la section Informations d’identification du Adobe Developer Console.</td>
        </tr>
        <tr>
        <td role="rowheader">Clé secrète client</td>
        <td>Saisissez votre clé secrète client Adobe. Vous trouverez cette information dans la section Informations d’identification du Adobe Developer Console.</td>
        </tr>
      </tbody>
    </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour enregistrer la connexion et revenir au module.


## Modules Adobe Firefly Lightroom et leurs champs

Lorsque vous configurez les modules Adobe Firefly Lightroom, Workfront Fusion affiche les champs répertoriés ci-dessous. En fonction de facteurs tels que votre niveau d’accès dans l’application ou le service, d’autres champs Adobe Firefly Lightroom peuvent s’afficher. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, consultez [Mappage d’informations d’un module à l’autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Bouton (bascule) de mappage](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Ajout de XMP à l’image](#add-xmp-to-image)
* [Application des modifications Lightroom](#apply-lightroom-edits)
* [Application de paramètres prédéfinis de Lightroom](#apply-lightroom-presets)
* [Redressement automatique](#auto-straighten)
* [Correction automatique de la tonalité](#auto-tone)


### Ajout de XMP à l’image

Ce module applique à une image un paramètre prédéfini Lightroom basé sur XMP.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Firefly Lightroom, voir <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Créer une connexion à Adobe Firefly Lightroom</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL de l’image</td> 
   <td>Saisissez ou mappez une URL prédéfinie représentant l’image à laquelle vous souhaitez appliquer XMP.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type de stockage</td> 
   <td>Sélectionnez le type de stockage dans lequel l’image est stockée.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Contenu XMP</td> 
   <td>Saisissez ou mappez le texte du contenu XMP que vous souhaitez ajouter à l’image. Il doit s’agir d’une chaîne XML.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Orientation</td> 
    <td>Saisissez ou mappez l’orientation EXIF à appliquer à l’image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Stockage en sortie</td> 
    <td>Sélectionnez l’emplacement de stockage du fichier de sortie. <p>Le stockage interne Fusion ne stocke pas l’image en dehors du scénario, mais permet à d’autres modules du scénario d’accéder à l’image.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type de sortie</td> 
   <td>Sélectionnez le type de fichier pour le fichier de sortie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Remplacer</td> 
   <td>Sélectionnez oui si vous souhaitez permettre au module de remplacer la sortie s’il existe déjà. Cela s’applique uniquement au stockage dans le cloud d’Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Qualité</td> 
   <td>Saisissez ou mappez la qualité de l’image de sortie. 1 est la qualité la plus faible, et 12 est la qualité la plus élevée. Cela s’applique uniquement aux fichiers JPEG.</td> 
  </tr> 
 </tbody> 
</table>

### Application des modifications Lightroom

Ce module applique une ou plusieurs modifications Lightroom à une image. Les modifications incluent l’exposition, le contraste, la netteté et la saturation.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Firefly Lightroom, voir <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Créer une connexion à Adobe Firefly Lightroom</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL de l’image</td> 
   <td>Saisissez ou mappez une URL prédéfinie représentant l’image à laquelle vous souhaitez appliquer XMP.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type de stockage</td> 
   <td>Sélectionnez le type de stockage dans lequel l’image est stockée.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Modifier les options</td> 
   <td>Définissez les options de modification à appliquer à l’image.<p>Pour plus d’informations sur les options, voir <a href="https://developer.adobe.com/firefly-services/docs/lightroom/api/#operation/applyEdits">Appliquer les modifications Lightroom</a> dans la documentation de l’API Adobe Firefly Lightroom.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Stockage en sortie</td> 
    <td>Sélectionnez l’emplacement de stockage du fichier de sortie. <p>Le stockage interne Fusion ne stocke pas l’image en dehors du scénario, mais permet à d’autres modules du scénario d’accéder à l’image.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type de sortie</td> 
   <td>Sélectionnez le type de fichier pour le fichier de sortie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Remplacer</td> 
   <td>Sélectionnez oui si vous souhaitez permettre au module de remplacer la sortie s’il existe déjà. Cela s’applique uniquement au stockage dans le cloud d’Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Qualité</td> 
   <td>Saisissez ou mappez la qualité de l’image de sortie. 1 est la qualité la plus faible, et 12 est la qualité la plus élevée. Cela s’applique uniquement aux fichiers JPEG.</td> 
  </tr> 
 </tbody> 
</table>

### Application de paramètres prédéfinis de Lightroom

Ce module applique un ou plusieurs paramètres prédéfinis de Lightroom XMP à l’image donnée en utilisant les fichiers XMP de paramètres prédéfinis donnés.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Firefly Lightroom, voir <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Créer une connexion à Adobe Firefly Lightroom</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL de l’image</td> 
   <td>Saisissez ou mappez une URL prédéfinie représentant l’image à laquelle vous souhaitez appliquer XMP.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type de stockage</td> 
   <td>Sélectionnez le type de stockage dans lequel l’image est stockée.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Paramètres prédéfinis</td> 
   <td>Pour chaque paramètre prédéfini à appliquer, cliquez sur <b>Ajouter un élément</b>, saisissez l’URL prédéfinie du paramètre prédéfini et sélectionnez son type de stockage.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Stockage en sortie</td> 
    <td>Sélectionnez l’emplacement de stockage du fichier de sortie. <p>Le stockage interne Fusion ne stocke pas l’image en dehors du scénario, mais permet à d’autres modules du scénario d’accéder à l’image.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type de sortie</td> 
   <td>Sélectionnez le type de fichier pour le fichier de sortie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Remplacer</td> 
   <td>Sélectionnez oui si vous souhaitez permettre au module de remplacer la sortie s’il existe déjà. Cela s’applique uniquement au stockage dans le cloud d’Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Qualité</td> 
   <td>Saisissez ou mappez la qualité de l’image de sortie. 1 est la qualité la plus faible, et 12 est la qualité la plus élevée. Cela s’applique uniquement aux fichiers JPEG.</td> 
  </tr> 
 </tbody> 
</table>

### Redressement automatique

Ce module redresse automatiquement une image en appliquant la transformation verticale automatique.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Firefly Lightroom, voir <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Créer une connexion à Adobe Firefly Lightroom</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL de l’image</td> 
   <td>Saisissez ou mappez une URL prédéfinie représentant l’image à laquelle vous souhaitez appliquer XMP.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type de stockage</td> 
   <td>Sélectionnez le type de stockage dans lequel l’image est stockée.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Mode vertical</td> 
   <td>Sélectionnez le type de Mode vertical que vous souhaitez utiliser. Si vous ne définissez pas de valeur, un mode approprié sera automatiquement fourni.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Limiter le recadrage</td> 
   <td>Indiquez si l’image redressée doit être recadrée pour supprimer tous les bords vides.</td> 
  </tr> 
 <tr> 
   <td role="rowheader">Stockage de sortie</td> 
    <td>Sélectionnez l’emplacement de stockage du fichier de sortie. <p>Le stockage interne Fusion ne stocke pas l’image en dehors du scénario, mais permet à d’autres modules du scénario d’accéder à l’image.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type de sortie</td> 
   <td>Sélectionnez le type de fichier pour le fichier de sortie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Remplacer</td> 
   <td>Sélectionnez oui si vous souhaitez permettre au module de remplacer la sortie s’il existe déjà. Cela s’applique uniquement au stockage dans le cloud d’Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Qualité</td> 
   <td>Saisissez ou mappez la qualité de l’image de sortie. 1 est la qualité la plus faible, et 12 est la qualité la plus élevée. Cela s’applique uniquement aux fichiers JPEG.</td> 
  </tr> 
 </tbody> 
</table>


### Correction automatique de la tonalité

Ce module corrige automatiquement l’exposition, le contraste, la netteté et la saturation d’une image.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Firefly Lightroom, voir <a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >Créer une connexion à Adobe Firefly Lightroom</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL de l’image</td> 
   <td>Saisissez ou mappez une URL prédéfinie représentant l’image à laquelle vous souhaitez appliquer XMP.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type de stockage</td> 
   <td>Sélectionnez le type de stockage dans lequel l’image est stockée.</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">Stockage en sortie</td> 
    <td>Sélectionnez l’emplacement de stockage du fichier de sortie. <p>Le stockage interne Fusion ne stocke pas l’image en dehors du scénario, mais permet à d’autres modules du scénario d’accéder à l’image.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type de sortie</td> 
   <td>Sélectionnez le type de fichier pour le fichier de sortie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Remplacer</td> 
   <td>Sélectionnez oui si vous souhaitez permettre au module de remplacer la sortie s’il existe déjà. Cela s’applique uniquement au stockage dans le cloud d’Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Qualité</td> 
   <td>Saisissez ou mappez la qualité de l’image de sortie. 1 est la qualité la plus faible, et 12 est la qualité la plus élevée. Cela s’applique uniquement aux fichiers JPEG.</td> 
  </tr> 
 </tbody> 
</table>


