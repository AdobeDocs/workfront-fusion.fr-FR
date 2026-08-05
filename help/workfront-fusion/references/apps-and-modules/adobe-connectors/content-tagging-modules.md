---
title: Modules Adobe Content Tagger
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent Adobe Content Tagger et les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
source-git-commit: 801e8cb1a4c807aaa4275382c2d6211cf3cd6d1f
workflow-type: tm+mt
source-wordcount: '1098'
ht-degree: 21%

---

# Modules Adobe Content Tagger

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent Adobe Content Tagger et les connecter à plusieurs applications et services tiers.

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
   <p>Basé sur les opérations : disponible pour les organisations disposant de licences basées sur les opérations</p>
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

## Créer une connexion à Adobe Content Tagger

Pour créer une connexion pour vos modules Adobe Content Tagger :

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


## Modules Adobe Content Tagger et leurs champs

Lorsque vous configurez les modules Adobe Content Tagger, Workfront Fusion affiche les champs répertoriés ci-dessous. D’autres champs Adobe Content Tagger peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, consultez [Mappage d’informations d’un module à l’autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Bouton (bascule) de mappage](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Actions

* [Couleurs des balises](#tag-colors)
* [Mots-clés de balise](#tag-keywords)
* [Balisage de texte dans une image](#tag-text-in-an-image)

#### Couleurs des balises

Ce module renvoie le pourcentage d’une image couverte par différentes couleurs de pixels, triées en 40 catégories de couleurs.


<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Content Tagger, voir <a href="#create-a-connection-to-adobe-content-tagger" class="MCXref xref" >Créer une connexion à Adobe Content Tagger</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom du fichier image</td> 
   <td>Saisissez ou mappez le nom de fichier de l’image pour laquelle vous souhaitez baliser les couleurs.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Données d’image</td> 
   <td>Saisissez ou mappez les données de fichier de l’image dont vous souhaitez baliser les couleurs.</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">Format de l’image</td> 
    <td>Sélectionnez le type d’image de l’image dont vous souhaitez baliser les couleurs.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nombre de couleurs</td> 
    <td>Saisissez ou mappez le nombre de couleurs à renvoyer. Pour renvoyer tous les résultats, saisissez 0.</p></td> 
  </tr> 
 <tr> 
   <td role="rowheader">Couverture minimale</td> 
   <td>Saisissez ou mappez la couverture minimale pour laquelle vous souhaitez baliser les couleurs. Seules les couleurs couvrant au moins cette quantité de l’image seront renvoyées. Une valeur de 1 représente 100 % de l’image, et une valeur de .5 représente 50 % de l’image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Redimensionnez l’image avant l’extraction.</td> 
   <td>Sélectionnez Oui pour redimensionner l’image sur 320x320 avant d’extraire les couleurs. Sélectionnez Non pour extraire des couleurs de l’image en taille réelle.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Activer le masque de premier plan/arrière-plan</td> 
   <td>Sélectionnez Oui si vous souhaitez afficher les couleurs séparément pour l’image globale, le premier plan et l’arrière-plan.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Récupérer des tons</td> 
   <td>Sélectionnez Oui si vous souhaitez récupérer des données sur les tons chauds, neutres et froids en plus des couleurs.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nombre maximal de couleurs renvoyées</td> 
   <td>Saisissez ou mappez le nombre maximal de couleurs que le module avec un retour pour un cycle d’exécution.</td> 
  </tr> 
 </tbody> 
</table>



#### Mots-clés de balise

Ce module extrait les mots-clés ou expressions clés qui décrivent le mieux l’objet du document.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Content Tagger, voir <a href="#create-a-connection-to-adobe-content-tagger" class="MCXref xref" >Créer une connexion à Adobe Content Tagger</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom de fichier du document</td> 
   <td>Saisissez ou mappez le nom de fichier du document à partir duquel vous souhaitez extraire les mots-clés.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Données d’image</td> 
   <td>Saisissez ou mappez les données de fichier du document à partir duquel vous souhaitez extraire les mots-clés.</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">Format de l’image</td> 
    <td>Sélectionnez le format du document à partir duquel vous souhaitez extraire les mots-clés.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de l’application</td> 
   <td>Saisissez ou mappez l'ID application pour le document.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nombre d'expressions clés</td> 
   <td>Saisissez ou mappez le nombre d’expressions clés que le module doit renvoyer. Pour renvoyer tous les résultats, saisissez 0.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Pertinence minimale</td> 
   <td>Saisissez ou mappez le seuil de score au-dessous duquel les résultats ne seront pas renvoyés.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Longueur minimale de l’expression de la clé (mots)</td> 
   <td>Saisissez ou mappez le nombre minimum de mots requis dans les expressions clés.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Longueur maximale de l’expression de la clé (mots)</td> 
   <td>Saisissez ou mappez le nombre maximal de mots requis dans les expressions clés.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Profondeur d'unité sémantique</td> 
   <td>Sélectionnez la profondeur à laquelle vous souhaitez que les réponses hiérarchiques aillent.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Types d’entités</td> 
   <td>Pour chaque type d'entité auquel vous souhaitez limiter les expressions clés, cliquez sur <b>Ajouter un élément</b> et saisissez les informations relatives au type d'entité.</td> 
  </tr> 
 </tbody> 
</table>

#### Balisage de texte dans une image

Ce module indique si du texte est présent dans une image et renvoie le texte s’il est présent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Content Tagger, voir <a href="#create-a-connection-to-adobe-content-tagger" class="MCXref xref" >Créer une connexion à Adobe Content Tagger</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom du fichier image</td> 
   <td>Saisissez ou mappez le nom de fichier du document à partir duquel vous souhaitez extraire du texte.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Données d’image</td> 
   <td>Saisissez ou mappez les données de fichier du document à partir duquel vous souhaitez extraire du texte.</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">Format de l’image</td> 
    <td>Sélectionnez le format du document à partir duquel vous souhaitez extraire du texte.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filtrer avec dictionnaire</td> 
   <td>Choisissez de ne renvoyer que les mots figurant dans le dictionnaire d'anglais.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Probabilité minimale</td> 
   <td>Entrez ou mappez la probabilité minimale, où le module ne renverra que les mots reconnus avec au moins cette probabilité. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Pertinence minimale</td> 
   <td>Saisissez le pourcentage minimal de l’image que le texte renvoyé doit couvrir. La pertinence est calculée comme la fraction de la zone du cadre englobant du texte extrait par rapport à l’image complète. 0,01 se traduirait par un texte occupant au moins 1 % de l’image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nombre maximal de résultats renvoyés</td> 
   <td>Saisissez ou mappez le nombre maximal de résultats que le module renverra pour un cycle d’exécution.</td> 
  </tr> 
 </tbody> 
</table>
