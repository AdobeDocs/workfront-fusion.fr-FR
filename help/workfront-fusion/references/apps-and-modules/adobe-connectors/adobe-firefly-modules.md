---
title: Modules Adobe Firefly
description: Dans un scénario  [!DNL Adobe Workfront Fusion] , vous pouvez automatiser les workflows qui utilisent  [!DNL Adobe Firefly] et le connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3b29ba3d-a769-4e97-b2c2-0b4eeed5b029
source-git-commit: a3494479614a4930427842fa68e6b586edca0833
workflow-type: tm+mt
source-wordcount: '2248'
ht-degree: 17%

---

# Modules [!DNL Adobe Firefly]

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!DNL Adobe Firefly] et le connecter à plusieurs applications et services tiers.

Si vous avez besoin d’instructions pour créer un scénario, consultez les articles sous [Créer un scénario : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

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

## Conditions préalables

Avant d’utiliser le connecteur [!DNL Adobe Firefly], vous devez vous assurer que les conditions préalables suivantes sont remplies :

* Vous devez disposer d’un compte [!DNL Adobe Firefly].

## Informations sur l’API Adobe Firefly

Le connecteur Adobe Firefly utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.4.24</td> 
  </tr>
 </tbody> 
 </table>

## Créer une connexion à [!DNL Adobe Firefly]

Pour créer une connexion pour vos modules [!DNL Adobe Firefly], procédez comme suit :

1. Cliquez sur **[!UICONTROL Add]** en regard de la zone Connexion .

1. Remplissez les champs suivants :

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Saisissez un nom pour cette connexion.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>Indiquez si vous vous connectez à un environnement de production ou hors production.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>Indiquez si vous vous connectez à un compte de service ou à un compte personnel.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Saisissez votre [!UICONTROL Client ID] de [!UICONTROL Adobe]. Pour plus d’informations, consultez la section Détails du [!UICONTROL Credentials] de la [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Saisissez votre [!UICONTROL Client Secret] de [!DNL Adobe]. Pour plus d’informations, consultez la section Détails du [!UICONTROL Credentials] de la [!DNL Adobe Developer Console].</td>
        </tr>
      </tbody>
    </table>

1. Cliquez sur **[!UICONTROL Continue]** pour enregistrer la connexion et revenir au module .

## Modules [!DNL Adobe Firefly] et leurs champs

Lorsque vous configurez les modules [!DNL Adobe Firefly], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Adobe Firefly] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Développement d’une image

Ce module d’action développe une image, éventuellement avec du contenu à partir d’une invite que vous fournissez.

Ce module fonctionne avec l’API Firefly V3 Async. La version précédente de ce module est obsolète et sera supprimée dans un proche avenir.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Campaign], voir <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Créer une connexion à [!DNL Adobe Firefly]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Saisissez ou mappez une invite pour le contenu avec lequel vous souhaitez développer l’image. Si aucune invite n’est fournie, l’image est développée avec le contenu correspondant à l’image d’origine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of variations]</td> 
   <td>Entrez un nombre compris entre 1 et 4. Le module génère ce nombre de variations d’image développées.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source]</td> 
   <td>Sélectionnez le mode de fourniture du fichier source :<ul><li><p><b>Fichier</b></p><p>Sélectionnez un fichier source dans un module précédent ou mappez le nom de fichier image de référence et le fichier image de référence du fichier source.</p></li><li><p><b>URL prédéfinie</b></p><p>Saisissez ou mappez l’URL de l’image source.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expanded image format]</td> 
   <td>Sélectionnez le format de fichier sous lequel l’image développée sera enregistrée.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expand by]</td> 
   <td>  <p>Choisissez si vous souhaitez développer l’image à l’aide de l’emplacement de l’image ou d’un masque.</p> 
   <ul>
   <li><b>Emplacement</b><p>Saisissez l’alignement horizontal et vertical, ainsi que l’incrustation de l’image placée sur les bords.</p></li>
   <li><b>Masque</b><p>Sélectionnez le fichier source du masque et indiquez si le masque doit être inversé.</p></li>
   </ul>
</td> 
</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>Sélectionnez la hauteur et la largeur souhaitées pour l’image développée.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]</td> 
   <td>Pour chaque image que le module va générer, cliquez sur <b>Ajouter un élément</b> et saisissez ou mappez un entier. Vous pouvez utiliser cette même adresse de contrôle dans un autre module Développer une image pour générer une image similaire avec différents styles. Le nombre d’adresses de contrôle que vous ajoutez doit être égal au champ Nombre de variations .</td> 
  </tr> 
 </tbody> 
</table>

### Développer une image (obsolète)

Ce module a été abandonné et sera supprimé prochainement. Utilisez plutôt le module Développer une image .

### Remplir une image

Ce module d’action remplit la zone masquée d’une image, éventuellement avec le contenu d’une invite que vous fournissez.

Ce module fonctionne avec l’API Firefly V3 Async. La version précédente de ce module est obsolète et sera supprimée dans un proche avenir.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Campaign], voir <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Créer une connexion à [!DNL Adobe Firefly]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Image > Source]</td> 
   <td>Sélectionnez la manière de fournir le fichier source d’image :<ul><li><p><b>Fichier</b></p><p>Sélectionnez un fichier source dans un module précédent ou mappez le nom de fichier image de référence et le fichier image de référence du fichier source.</p></li><li><p><b>URL prédéfinie</b></p><p>Saisissez ou mappez l’URL de l’image source.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mask > Source]</td> 
   <td>Sélectionnez la manière dont vous fournissez le fichier source du masque :<ul><li><p><b>Fichier</b></p><p>Sélectionnez un fichier source dans un module précédent ou mappez le nom de fichier image de référence et le fichier image de référence du fichier source.</p></li><li><p><b>URL prédéfinie</b></p><p>Saisissez ou mappez l’URL de l’image source.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Saisissez ou mappez une invite pour le contenu avec lequel vous souhaitez remplir l’image. Si aucune invite n’est fournie, l’image est remplie avec le contenu correspondant à l’image d’origine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of variations]</td> 
   <td>Entrez un nombre compris entre 1 et 4. Le module génère ce nombre de variations d’images remplies.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filled image format]</td> 
   <td>Sélectionnez le format de fichier sous lequel l’image remplie sera enregistrée.</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]</td> 
   <td>Pour chaque image que le module va générer, cliquez sur <b>Ajouter un élément</b> et saisissez ou mappez un entier. Vous pouvez utiliser cette même adresse de contrôle dans un autre module Développer une image pour générer une image similaire avec différents styles. Le nombre d’adresses de contrôle que vous ajoutez doit être égal au champ Nombre de variations .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>Sélectionnez la taille de l’image remplie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Locale]</td> 
   <td>Si des paramètres régionaux sont fournis, le module génère du contenu plus pertinent pour les paramètres régionaux spécifiés. <p>Les paramètres régionaux doivent être fournis dans le code de langue ISO 639-1 et la région ISO 3166-1.</p><p> Exemple : <code>en-US</code></p></td> 
  </tr> 
 </tbody> 
</table>

### Remplir une image (obsolète)

Ce module a été abandonné et sera supprimé prochainement. Utilisez plutôt le module Remplir une image .

## Générer une image

Ce module d’action génère une image et en fonction d’une invite que vous fournissez. Vous pouvez également fournir une image de référence facultative ; l’image générée correspondra au style de l’image de référence.

Ce module fonctionne avec l’API Firefly V3 Async. La version précédente de ce module est obsolète et sera supprimée dans un proche avenir.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Campaign], voir <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Créer une connexion à [!DNL Adobe Firefly]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Saisissez ou mappez une invite pour l’image que vous souhaitez générer. Plus de détails dans l’invite vous permettront de mieux contrôler ce qui apparaît dans l’image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of variations]</td> 
   <td>Entrez un nombre compris entre 1 et 4. Le module génère ce nombre de variations d’image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Generated image format]</td> 
   <td>Sélectionnez le format de fichier sous lequel l’image développée sera enregistrée. Si vous sélectionnez par défaut, le format du fichier est JPEG si aucune image de référence n’est fournie. Si une image de référence est fournie, le format de fichier de l’image générée est identique à celui de l’image de référence.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Structure > Image reference]</td> 
    <td>Sélectionnez la manière dont vous fournissez le fichier source pour la structure de la nouvelle image :<ul><li><p><b>Fichier</b></p><p>Sélectionnez un fichier source dans un module précédent ou mappez le nom de fichier image de référence et le fichier image de référence du fichier source.</p></li><li><p><b>URL prédéfinie</b></p><p>Saisissez ou mappez l’URL de l’image source.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Structure > Strength]</td> 
    <td>Saisissez un nombre compris entre 0 et 100 pour contrôler la manière dont Firefly suit strictement la structure de l’image source. Des valeurs plus élevées signifient que Firefly suit l’image plus strictement.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style > Image reference]</td> 
    <td>Sélectionnez la manière dont vous fournissez le fichier source pour le style de la nouvelle image :<ul><li><p><b>Fichier</b></p><p>Sélectionnez un fichier source dans un module précédent ou mappez le nom de fichier image de référence et le fichier image de référence du fichier source.</p></li><li><p><b>URL prédéfinie</b></p><p>Saisissez ou mappez l’URL de l’image source.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Structure > Strength]</td> 
    <td>Saisissez un nombre compris entre 0 et 100 pour contrôler le respect strict du style de l’image source par Firefly. Des valeurs plus élevées signifient que Firefly suit l’image plus strictement.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style > Presets]</td> 
   <td>Si vous souhaitez utiliser un style prédéfini, cliquez sur Ajouter un élément et saisissez ou mappez le style que vous souhaitez utiliser.<p>Pour obtenir une liste des styles prédéfinis, voir <a href="https://developer.adobe.com/firefly-services/docs/firefly-api/guides/concepts/style-presets//" >Styles de modèle d’image</a> dans la documentation destinée aux développeurs d’Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Negative prompt]</td> 
   <td>Saisissez ou mappez les mots à éviter dans le contenu généré. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content class]</td> 
   <td>Choisissez si vous souhaitez que l’image générée ressemble davantage à une photo ou à une illustration créée. <ul><li><b>Photo</b><p>Entrez des valeurs pour l'Ouverture, la Vitesse d'obturation (en secondes) et le champ de vision (en millimètres).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seed]</td> 
   <td>Pour chaque image que le module va générer, cliquez sur <b>Ajouter un élément</b> et saisissez ou mappez un entier. Vous pouvez utiliser cette même adresse de contrôle dans un autre module Développer une image pour générer une image similaire avec différents styles. Le nombre d’adresses de contrôle que vous ajoutez doit être égal au champ Nombre de variations .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>Sélectionnez la taille de l’image générée.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Visual intensity]</td> 
   <td>Saisissez ou mappez un entier qui représente l’intensité globale des caractéristiques visuelles existantes de la photo. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Locale]</td> 
   <td>Si des paramètres régionaux sont fournis, le module génère du contenu plus pertinent pour les paramètres régionaux spécifiés. <p>Les paramètres régionaux doivent être fournis dans le code de langue ISO 639-1 et la région ISO 3166-1.</p><p> Exemple : <code>en-US</code></p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tileable]</td> 
   <td>Activez cette option pour générer une image qui peut être répétée à l’infini dans toutes les directions.</td> 
  </tr> 
 </tbody> 
</table>

### Générer une image (obsolète)

Ce module a été abandonné et sera supprimé prochainement. Utilisez plutôt le module Generate an image .

### Générer un objet composite

Ce module d’action combine des images générées par Firefly pour créer un composite d’images.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Campaign], voir <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Créer une connexion à [!DNL Adobe Firefly]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Saisissez ou mappez une invite pour l’image que vous souhaitez générer. Plus de détails dans l’invite vous permettront de mieux contrôler ce qui apparaît dans l’image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of variations]</td> 
   <td>Entrez un nombre compris entre 1 et 4. Le module génère ce nombre de variations d’image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content classs]</td> 
   <td>Choisissez si vous souhaitez que l’image générée ressemble davantage à une photo ou à un tableau.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Image > Source]</td> 
    <td>Sélectionnez la manière dont vous fournissez le fichier source pour la structure de la nouvelle image :<ul><li><p><b>Fichier</b></p><p>Sélectionnez un fichier source dans un module précédent ou mappez le nom de fichier image de référence et le fichier image de référence du fichier source.</p></li><li><p><b>URL prédéfinie</b></p><p>Saisissez ou mappez l’URL de l’image source.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Generated image format]</td> 
   <td>Sélectionnez le format de fichier sous lequel l’image développée sera enregistrée. Si vous sélectionnez par défaut, le format du fichier est JPEG si aucune image de référence n’est fournie. Si une image de référence est fournie, le format de fichier de l’image générée est identique à celui de l’image de référence.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style > Image reference]</td> 
    <td>Sélectionnez la manière dont vous fournissez le fichier source pour le style de la nouvelle image :<ul><li><p><b>Fichier</b></p><p>Sélectionnez un fichier source dans un module précédent ou mappez le nom de fichier image de référence et le fichier image de référence du fichier source.</p></li><li><p><b>URL prédéfinie</b></p><p>Saisissez ou mappez l’URL de l’image source.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Structure > Strength]</td> 
    <td>Saisissez un nombre compris entre 0 et 100 pour contrôler le respect strict du style de l’image source par Firefly. Des valeurs plus élevées signifient que Firefly suit l’image plus strictement.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style > Presets]</td> 
   <td>Si vous souhaitez utiliser un style prédéfini, cliquez sur Ajouter un élément et saisissez ou mappez le style que vous souhaitez utiliser.<p>Pour obtenir une liste des styles prédéfinis, voir <a href="https://developer.adobe.com/firefly-services/docs/firefly-api/guides/concepts/style-presets//" >Styles de modèle d’image</a> dans la documentation destinée aux développeurs d’Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>Sélectionnez la taille à laquelle le composite généré doit être destiné. </td> 
  </tr> 
 </tbody> 
</table>

### Générer des images similaires

Ce module d’action génère des images similaires à l’image source que vous spécifiez.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Campaign], voir <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Créer une connexion à [!DNL Adobe Firefly]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of variations]</td> 
   <td>Entrez un nombre compris entre 1 et 4. Le module génère ce nombre de variations d’image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Generated image format]</td> 
   <td>Sélectionnez le format de fichier sous lequel l’image développée sera enregistrée. Si vous sélectionnez par défaut, le format du fichier est JPEG si aucune image de référence n’est fournie. Si une image de référence est fournie, le format de fichier de l’image générée est identique à celui de l’image de référence.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Image > Source]</td> 
    <td>Sélectionnez la manière dont vous fournissez le fichier source pour la structure de la nouvelle image :<ul><li><p><b>Fichier</b></p><p>Sélectionnez un fichier source dans un module précédent ou mappez le nom de fichier image de référence et le fichier image de référence du fichier source.</p></li><li><p><b>URL prédéfinie</b></p><p>Saisissez ou mappez l’URL de l’image source.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style > Image reference]</td> 
    <td>Sélectionnez la manière dont vous fournissez le fichier source pour le style de la nouvelle image :<ul><li><p><b>Fichier</b></p><p>Sélectionnez un fichier source dans un module précédent ou mappez le nom de fichier image de référence et le fichier image de référence du fichier source.</p></li><li><p><b>URL prédéfinie</b></p><p>Saisissez ou mappez l’URL de l’image source.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>Sélectionnez la taille à laquelle le composite généré doit être destiné. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]</td> 
   <td>Pour chaque image que le module va générer, cliquez sur <b>Ajouter un élément</b> et saisissez ou mappez un entier. Vous pouvez utiliser cette même adresse de contrôle dans un autre module Développer une image pour générer une image similaire avec différents styles. Le nombre d’adresses de contrôle que vous ajoutez doit être égal au champ Nombre de variations .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tileable]</td> 
   <td>Activez cette option pour générer une image qui peut être répétée à l’infini dans toutes les directions.</td> 
  </tr> 
 </tbody> 
</table>


### Effectuer un appel API personnalisé.

Ce module d’action effectue un appel personnalisé à l’API Firefly.

Pour connaître les API spécifiques disponibles, consultez [API Adobe Firefly](https://developer.adobe.com/firefly-services/docs/firefly-api/) dans la documentation d’Adobe Developer.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Firefly], voir <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Créer une connexion à [!DNL Adobe Firefly]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Saisir un chemin relatif à <code>https://firefly-api.adobe.io/</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p>
        <p>Par exemple, <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] Ajoute automatiquement des en-têtes d’autorisation.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lors de l’utilisation d’instructions conditionnelles telles que <code>if</code> dans votre fichier JSON, placez les guillemets en dehors de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

