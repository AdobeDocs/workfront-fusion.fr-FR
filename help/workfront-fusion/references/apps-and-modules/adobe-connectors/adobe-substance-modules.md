---
title: Modules Adobe Substance
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent  [!DNL Adobe Substance], et le connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
source-git-commit: 2e44c89d487100b3245b40f6927185a0ff12ef2f
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 31%

---

# Modules [!DNL Adobe Substance]

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent [!DNL Adobe Substance] et les connecter à plusieurs applications et services tiers.

Si vous avez besoin d’instructions pour créer un scénario, consultez les articles sous [Créer un scénario : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tout package de workflow Adobe Workfront et tout package d’automatisation et d’intégration Adobe Workfront.</p><p>Workfront Ultimate</p><p>Packages Workfront Prime et Select, avec un achat supplémentaire de Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licences Adobe Workfront</td> 
   <td> <p>Standard</p><p>Travail ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licence Adobe Workfront Fusion</td> 
   <td>
   <p>Basé sur les opérations : aucune exigence de licence Workfront Fusion.</p>
   <p>Basé sur le connecteur (hérité) : Workfront Fusion pour l’automatisation et l’intégration du travail </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Si votre entreprise dispose d’un package Workfront Select ou Prime qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acheter Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Conditions préalables

Avant d’utiliser le connecteur [!DNL Adobe Substance], vous devez vous assurer que les conditions préalables suivantes sont remplies :

* Vous devez disposer d’un compte [!DNL Adobe Substance].



## Modules [!DNL Adobe Substance] et leurs champs

Lorsque vous configurez les modules [!DNL Adobe Substance], Workfront Fusion affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Adobe Substance] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un astérisque en regard du nom du champ dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mapper des informations d’un module à l’autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Bouton bascule Mapper](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Composites](#composites)
* [Scènes](#scenes)
* [Espaces](#spaces)

### Composites

#### Générer un composite d’objet 3D

Ce module d’action génère du contenu pour un composite 3D qui inclut la ressource principale sélectionnée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Adobe Substance] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Autres champs</td> 
   <td>Configurez d’autres champs selon vos besoins. Pour plus d’informations sur les champs, consultez la <a href="https://s3d.adobe.io/docs#/operations/v1/composites/compose">documentation de l’API Substance Adobe</a>.</td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader">Camera name</td> 
   <td>Enter or map the name of an existing camera that has been previously defined in the source 3D file.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Content class</td> 
   <td>Select whether you want the composite to have the style of art or of a photo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Enable ground plane</td> 
   <td>Enable this to enable the auto-generated ground plane under the hero asset. This is useful if the 3D scene contains only a hero asset, without additional elements.</td> 
  </tr> -->
 </tbody> 
</table>

### Scènes

* [Convertir des fichiers 3D](#convert-3d-files)
* [Créer une scène 3D](#create-3d-scene)
* [Décrire une scène 3D](#describe-3d-scene)
* [Rendu d’objet 3D](#render-3d-object)
* [Rendu d’un objet 3D (version de base)](#render-3d-object-basic-version)

#### Convertir des fichiers 3D

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Adobe Substance] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Format</td> 
   <td>Sélectionnez le format vers lequel vous convertissez le fichier.</td> 
  </tr> 
<tr> 
   <td role="rowheader">Point d’entrée du modèle</td> 
   <td>La conversion prend généralement le premier fichier considéré comme un modèle 3D valide. Définissez ce point d’entrée pour lever toute ambiguïté lorsqu’il existe plusieurs options.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sources</td> 
   <td>Pour chaque fichier à convertir, cliquez sur <b> Ajouter un élément</b> puis saisissez les informations relatives au fichier.</td> 
  </tr> 
 </tbody> 
</table>

#### Créer une scène 3D

Ce module d’action crée une scène à l’aide des ressources que vous spécifiez.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Adobe Substance] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
   <td role="rowheader">Encodage</td> 
   <td>Sélectionnez le type de fichier de la scène.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom de base du fichier</td> 
   <td>Saisissez ou mappez un nom pour le fichier de sortie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Autres champs</td> 
   <td>Configurez d’autres champs selon vos besoins. Pour plus d’informations sur les champs, consultez la <a href="https://s3d.adobe.io/docs#/operations/v1/scenes/assemble">documentation de l’API Substance Adobe</a>.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Sources</td> 
   <td>Pour chaque fichier que vous souhaitez utiliser, cliquez sur <b> Ajouter un élément</b> puis saisissez les informations relatives au fichier.</td> 
  </tr> 
 </tbody> 
</table>

#### Décrire une scène 3D

Ce module d’action récupère des informations sur le contenu de scène 3D.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Adobe Substance] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
   <td role="rowheader">Fichier Scene</td> 
   <td>Saisissez ou mappez le chemin d’accès au fichier de scène à décrire.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Sources</td> 
   <td>Pour chaque fichier que vous souhaitez décrire, cliquez sur <b> Ajouter un élément</b> puis saisissez les informations relatives au fichier.</td> 
  </tr> 
 </tbody> 
</table>

#### Rendu d’objet 3D

Ce module d’action effectue le rendu d’une image d’une scène.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Adobe Substance] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
   <td role="rowheader">Autres champs</td> 
   <td>Configurez d’autres champs selon vos besoins. Pour plus d’informations sur les champs, consultez la <a href="https://s3d.adobe.io/docs#/operations/v1/scenes/render">documentation de l’API Substance Adobe</a>.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Sources</td> 
   <td>Pour chaque fichier que vous souhaitez utiliser, cliquez sur <b> Ajouter un élément</b> puis saisissez les informations relatives au fichier.</td> 
  </tr> 
 </tbody> 
</table>

#### Rendu d’un objet 3D (version de base)

Ce module d’action effectue le rendu d’une image d’une scène avec moins d’options que le module Rendu d’objet 3D.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Adobe Substance] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
   <td role="rowheader">Autres champs</td> 
   <td>Configurez d’autres champs selon vos besoins. Pour plus d’informations sur les champs, consultez la <a href="https://s3d.adobe.io/docs#/operations/v1/scenes/render-basic">documentation de l’API Substance Adobe</a>.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Sources</td> 
   <td>Pour chaque fichier que vous souhaitez utiliser, cliquez sur <b> Ajouter un élément</b> puis saisissez les informations relatives au fichier.</td> 
  </tr> 
 </tbody> 
</table>

### Espaces

#### Créer un emplacement

Ce module d’action vous permet de télécharger et de stocker temporairement des fichiers.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Adobe Substance] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
   <td role="rowheader">Nom du fichier</td> 
   <td>Saisissez ou mappez le nom du fichier en cours de chargement.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Données de fichier</td> 
   <td>Saisissez ou mappez les données binaires du fichier.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nom</td> 
   <td>Saisissez ou mappez un nom pour la valeur du formulaire multipartie.</td> 
  </tr> 
 </tbody> 
</table>
