---
title: Modules Adobe Firefly
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent  [!DNL Adobe Firefly], et le connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3b29ba3d-a769-4e97-b2c2-0b4eeed5b029
TQID: https://experienceleague.adobe.com/1hI4NuUl2eEAgWyXRKLHQ3-6MM9-2tFyujGbRfHSBmU
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: b58ad82f-df6b-4b01-81a3-3a02ab9567a0
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 3886
ht-degree: 16%

---

# Modules [!DNL Adobe Firefly]

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent [!DNL Adobe Firefly] et le connecter à plusieurs applications et services tiers.

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

Avant d’utiliser le connecteur [!DNL Adobe Firefly], assurez-vous que les conditions préalables suivantes sont remplies :

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

1. Dans n’importe quel module, cliquez sur **[!UICONTROL Ajouter]** en regard de la zone Connexion .

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
        <td>Saisissez votre [!UICONTROL Adobe] [!UICONTROL Client ID]. Vous pouvez le consulter dans la section des détails [!UICONTROL Credentials] de la [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Saisissez votre [!UICONTROL Client Secret] [!DNL Adobe]. Vous pouvez le consulter dans la section des détails [!UICONTROL Credentials] de la [!DNL Adobe Developer Console].</td>
        </tr>
      </tbody>
    </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour enregistrer la connexion et revenir au module.

## Modules [!DNL Adobe Firefly] et leurs champs

Lorsque vous configurez les modules [!DNL Adobe Firefly], Workfront Fusion affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Adobe Firefly] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, consultez [Mappage d’informations d’un module à l’autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Bouton (bascule) de mappage](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Développement d’une image

Ce module d’action développe une image, éventuellement avec du contenu à partir d’une invite que vous fournissez.

Ce module fonctionne avec l’API Firefly V3 Async. La version précédente de ce module est obsolète et sera supprimée dans un proche avenir.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Firefly], voir <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Créer une connexion à [!DNL Adobe Firefly]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Saisissez ou mappez une invite pour le contenu avec lequel vous souhaitez développer l’image. Si aucune invite n’est fournie, l’image est développée avec le contenu correspondant à l’image d’origine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nombre de variations]</td> 
   <td>Entrez un nombre compris entre 1 et 4. Le module génère ce nombre de variations d’image développées.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source]</td> 
   <td>Sélectionnez le mode de fourniture du fichier source :<ul><li><p><b>Fichier</b></p><p>Sélectionnez un fichier source dans un module précédent ou mappez le nom de fichier image de référence et le fichier image de référence du fichier source.</p></li><li><p><b>URL prédéfinie</b></p><p>Saisissez ou mappez l’URL de l’image source.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Format d’image développé]</td> 
   <td>Sélectionnez le format de fichier sous lequel l’image développée sera enregistrée.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Développer par]</td> 
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
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Firefly], voir <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Créer une connexion à [!DNL Adobe Firefly]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Image &gt; Source]</td> 
   <td>Sélectionnez la manière de fournir le fichier source d’image :<ul><li><p><b>Fichier</b></p><p>Sélectionnez un fichier source dans un module précédent ou mappez le nom de fichier image de référence et le fichier image de référence du fichier source.</p></li><li><p><b>URL prédéfinie</b></p><p>Saisissez ou mappez l’URL de l’image source.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mask &gt; Source]</td> 
   <td>Sélectionnez la manière dont vous fournissez le fichier source du masque :<ul><li><p><b>Fichier</b></p><p>Sélectionnez un fichier source dans un module précédent ou mappez le nom de fichier image de référence et le fichier image de référence du fichier source.</p></li><li><p><b>URL prédéfinie</b></p><p>Saisissez ou mappez l’URL de l’image source.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Saisissez ou mappez une invite pour le contenu avec lequel vous souhaitez remplir l’image. Si aucune invite n’est fournie, l’image est remplie avec le contenu correspondant à l’image d’origine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nombre de variations]</td> 
   <td>Entrez un nombre compris entre 1 et 4. Le module génère ce nombre de variations d’images remplies.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Format d’image plein]</td> 
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

### Générer un composite adaptatif

Ce module d&#39;action compose de manière transparente une image du sujet en une image d&#39;arrière-plan à un emplacement masqué. Vous pouvez contrôler l&#39;intensité d&#39;application des ombres, la façon dont l&#39;éclairage et la couleur de l&#39;objet sont harmonisés avec l&#39;arrière-plan et si les détails d&#39;arrière-plan d&#39;origine sont conservés dans la zone masquée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Firefly], voir <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Créer une connexion à [!DNL Adobe Firefly]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Background &gt; Image &gt; Source]</td> 
   <td>Sélectionnez le mode d’affichage de l’image d’arrière-plan. L’image d’arrière-plan est la scène de destination où l’objet sera composé.<ul><li><p><b>Charger l’image</b></p><p>Chargez l’image d’arrière-plan ou mappez le fichier image d’un module précédent.</p></li><li><p><b>URL de l’image</b></p><p>Saisissez ou mappez l’URL de l’image d’arrière-plan.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Background &gt; Remplir le masque de zone &gt; Source]</td> 
   <td>Sélectionnez la manière dont vous fournissez le masque de zone de remplissage. Le masque de zone de remplissage indique la zone de l'arrière-plan où l'objet sera placé.<ul><li><p><b>Charger l’image</b></p><p>Chargez l’image du masque de zone de remplissage ou mappez le fichier image d’un module précédent.</p></li><li><p><b>URL de l’image</b></p><p>Saisissez ou mappez l’URL de l’image du masque de zone de remplissage.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object &gt; Image &gt; Source]</td> 
   <td>Sélectionnez la manière dont vous fournissez l’image de l’objet. L’image de l’objet est l’image source de l’objet à composer en arrière-plan.<ul><li><p><b>Charger l’image</b></p><p>Chargez l’image de l’objet ou mappez le fichier image d’un module précédent.</p></li><li><p><b>URL de l’image</b></p><p>Saisissez ou mappez l’URL de l’image de l’objet.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL , Objet &gt; Masque &gt; Source]</td> 
   <td>Sélectionnez la manière dont vous fournissez le masque d’objet. Le masque d’objet est le masque de segmentation de l’objet .<ul><li><p><b>Charger l’image</b></p><p>Chargez l’image du masque de saisie ou mappez le fichier image d’un module précédent.</p></li><li><p><b>URL de l’image</b></p><p>Saisissez ou mappez l’URL de l’image de masque d’objet.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nombre de variations]</td> 
   <td>Entrez un nombre compris entre 1 et 3. Le module génère ce nombre de variations composites.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]*</td> 
   <td>Cliquez sur <b>Ajouter un élément</b> pour ajouter une valeur de départ, puis saisissez ou mappez un entier. Utilisez une adresse de contrôle par variation. Le nombre de valeurs de départ doit correspondre à la valeur [!UICONTROL Number of Variations] si les deux sont fournis.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Harmonization]*</td> 
   <td>Saisissez un nombre compris entre 0 et 1 pour contrôler dans quelle mesure les couleurs et l'éclairage de l'objet sont ajustés en fonction de l'arrière-plan. <code>0.0</code> applique une harmonisation minimale et <code>1.0</code> une harmonisation maximale.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Shadow Intensité]*</td> 
   <td>Entrez un nombre compris entre 0 et 1 pour contrôler l'intensité de l'ombre dans le résultat composite. Des valeurs plus faibles réduisent l’ombre.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Preserve Background]*</td> 
   <td>Choisissez s’il faut conserver les détails d’arrière-plan d’origine dans la zone masquée pendant la composition. <ul><li><b>Oui</b><p>Les détails d’arrière-plan d’origine de la zone masquée sont conservés pendant la composition.</p></li><li><b>Non</b><p>Les détails d’arrière-plan d’origine de la zone masquée ne sont pas conservés pendant la composition.</p></li><li><b>Non défini</b><p>Utilisez le comportement par défaut pour cette option.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output &gt; Media Type]*</td> 
   <td>Sélectionnez le format de fichier sous lequel le composite généré sera enregistré.</td> 
  </tr> 
 </tbody> 
</table>

* Ces champs sont des champs avancés et ne s’affichent que si vous sélectionnez **[!UICONTROL Afficher les paramètres avancés]**.

### Générer une image

Ce module d’action génère une image et en fonction d’une invite que vous fournissez. Vous pouvez également fournir une image de référence facultative ; l’image générée correspondra au style de l’image de référence.

Ce module fonctionne avec l’API Firefly V3 Async. La version précédente de ce module est obsolète et sera supprimée dans un proche avenir.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Firefly], voir <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Créer une connexion à [!DNL Adobe Firefly]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Saisissez ou mappez une invite pour l’image que vous souhaitez générer. Plus de détails dans l’invite vous permettront de mieux contrôler ce qui apparaît dans l’image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model version]</td> 
   <td>Sélectionnez la version du modèle Firefly que vous souhaitez utiliser pour générer l’image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nombre de variations]</td> 
   <td>Entrez un nombre compris entre 1 et 4. Le module génère ce nombre de variations d’image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Generated image format]</td> 
   <td>Sélectionnez le format de fichier sous lequel l’image développée sera enregistrée. Si vous sélectionnez par défaut, le format du fichier est JPEG si aucune image de référence n’est fournie. Si une image de référence est fournie, le format de fichier de l’image générée est identique à celui de l’image de référence.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Structure &gt; Référence d’image]</td> 
    <td>Sélectionnez la manière dont vous fournissez le fichier source pour la structure de la nouvelle image :<ul><li><p><b>Fichier</b></p><p>Sélectionnez un fichier source dans un module précédent ou mappez le nom de fichier image de référence et le fichier image de référence du fichier source.</p></li><li><p><b>URL prédéfinie</b></p><p>Saisissez ou mappez l’URL de l’image source.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Structure &gt; Force]</td> 
    <td>Saisissez un nombre compris entre 0 et 100 pour contrôler la manière dont Firefly suit strictement la structure de l’image source. Des valeurs plus élevées signifient que Firefly suit l’image plus strictement.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style &gt; Référence d’image]</td> 
    <td>Sélectionnez la manière dont vous fournissez le fichier source pour le style de la nouvelle image :<ul><li><p><b>Fichier</b></p><p>Sélectionnez un fichier source dans un module précédent ou mappez le nom de fichier image de référence et le fichier image de référence du fichier source.</p></li><li><p><b>URL prédéfinie</b></p><p>Saisissez ou mappez l’URL de l’image source.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Structure &gt; Force]</td> 
    <td>Saisissez un nombre compris entre 0 et 100 pour contrôler le respect strict du style de l’image source par Firefly. Des valeurs plus élevées signifient que Firefly suit l’image plus strictement.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style &gt; Préréglages]</td> 
   <td>Si vous souhaitez utiliser un style prédéfini, cliquez sur Ajouter un élément et saisissez ou mappez le style que vous souhaitez utiliser.<p>Pour obtenir une liste des styles prédéfinis, voir <a href="https://developer.adobe.com/firefly-services/docs/firefly-api/guides/concepts/style-presets//" >Styles de modèle d’image</a> dans la documentation destinée aux développeurs d’Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Invite négative]</td> 
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
   <td role="rowheader">[!UICONTROL Intensité visuelle]</td> 
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
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Firefly], voir <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Créer une connexion à [!DNL Adobe Firefly]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Saisissez ou mappez une invite pour l’image que vous souhaitez générer. Plus de détails dans l’invite vous permettront de mieux contrôler ce qui apparaît dans l’image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nombre de variations]</td> 
   <td>Entrez un nombre compris entre 1 et 4. Le module génère ce nombre de variations d’image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content class]</td> 
   <td>Choisissez si vous souhaitez que l’image générée ressemble davantage à une photo ou à un tableau.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Image &gt; Source]</td> 
    <td>Sélectionnez la manière dont vous fournissez le fichier source pour la structure de la nouvelle image :<ul><li><p><b>Fichier</b></p><p>Sélectionnez un fichier source dans un module précédent ou mappez le nom de fichier image de référence et le fichier image de référence du fichier source.</p></li><li><p><b>URL prédéfinie</b></p><p>Saisissez ou mappez l’URL de l’image source.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Generated image format]</td> 
   <td>Sélectionnez le format de fichier sous lequel l’image développée sera enregistrée. Si vous sélectionnez par défaut, le format du fichier est JPEG si aucune image de référence n’est fournie. Si une image de référence est fournie, le format de fichier de l’image générée est identique à celui de l’image de référence.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style &gt; Référence d’image]</td> 
    <td>Sélectionnez la manière dont vous fournissez le fichier source pour le style de la nouvelle image :<ul><li><p><b>Fichier</b></p><p>Sélectionnez un fichier source dans un module précédent ou mappez le nom de fichier image de référence et le fichier image de référence du fichier source.</p></li><li><p><b>URL prédéfinie</b></p><p>Saisissez ou mappez l’URL de l’image source.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Structure &gt; Force]</td> 
    <td>Saisissez un nombre compris entre 0 et 100 pour contrôler le respect strict du style de l’image source par Firefly. Des valeurs plus élevées signifient que Firefly suit l’image plus strictement.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style &gt; Préréglages]</td> 
   <td>Si vous souhaitez utiliser un style prédéfini, cliquez sur Ajouter un élément et saisissez ou mappez le style que vous souhaitez utiliser.<p>Pour obtenir une liste des styles prédéfinis, voir <a href="https://developer.adobe.com/firefly-services/docs/firefly-api/guides/concepts/style-presets//" >Styles de modèle d’image</a> dans la documentation destinée aux développeurs d’Adobe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size]</td> 
   <td>Sélectionnez la taille à laquelle le composite généré doit être destiné. </td> 
  </tr> 
 </tbody> 
</table>

### Générer des images avec Image5

Ce module d’action génère une image à l’aide du modèle Image5 [!DNL Adobe Firefly]. Vous fournissez une invite de texte et, éventuellement, une image de référence pour guider la génération.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Firefly], voir <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Créer une connexion à [!DNL Adobe Firefly]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Saisissez ou mappez une description de l’image que vous souhaitez générer. L’invite doit comporter entre 1 et 1 500 caractères. Plus de détails dans l’invite vous permettent de contrôler davantage ce qui apparaît dans l’image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Format]</td> 
   <td>Sélectionnez la forme de l’image générée. Si une image de référence est fournie, sélectionnez <b>Auto</b>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resolution]</td> 
   <td>Sélectionnez la résolution de l’image générée. La génération de résolutions plus élevées prend plus de temps.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reference Image]</td> 
   <td>Vous pouvez éventuellement fournir une image de référence pour guider la génération. Cliquez sur <b>Ajouter un élément</b> et fournissez l’image. Lorsque vous utilisez une image de référence, définissez le format de  sur <b>Auto</b>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seed]*</td> 
   <td>Cliquez sur <b>Ajouter un élément</b> et saisissez ou mappez un entier pour reproduire un résultat de génération spécifique. Laissez le champ vide pour générer un résultat aléatoire.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt REASONING]*</td> 
   <td>Sélectionnez la stratégie de raisonnement rapide utilisée lors de la génération.<ul><li><p><b>Qualité - Génère la description de l’image</b></p><p>Génère une description de l’image dans la sortie du module.</p></li><li><p><b>Vitesse - Génération plus rapide, aucune description</b></p><p>Génère l’image plus rapidement, mais laisse la description de l’image vide.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Locale]*</td> 
   <td>Saisissez ou mappez une langue et un code de région pour adapter le contenu généré à un pays et une langue spécifiques. <p>Les paramètres régionaux doivent être fournis dans le code de langue ISO 639-1 et la région ISO 3166-1.</p><p>Exemple : <code>en-US</code></p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nombre de variations]*</td> 
   <td>Saisissez le nombre d’images à générer par demande. Actuellement, seul 1 est pris en charge. Pour générer plusieurs images, envoyez des requêtes distinctes.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]*</td> 
   <td>Sélectionnez le modèle de [!DNL Firefly] que vous souhaitez utiliser pour générer l’image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Saisissez ou mappez le nombre maximal de résultats avec lesquels vous souhaitez que le module fonctionne au cours d’un cycle d’exécution.</td> 
  </tr> 
 </tbody> 
</table>

*Ces champs sont avancés et ne s’affichent que si vous sélectionnez **[!UICONTROL Afficher les paramètres avancés]**.

### Générer un composite précis

Ce module d&#39;action place un sujet dans la région masquée d&#39;une image de fond et applique une harmonisation générative afin que le sujet se fond naturellement avec le fond.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Firefly], voir <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Créer une connexion à [!DNL Adobe Firefly]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Background &gt; Image &gt; Source]</td> 
   <td>Sélectionnez le mode d’affichage de l’image d’arrière-plan. L’image d’arrière-plan est la scène de destination où l’objet sera composé.<ul><li><p><b>Charger l’image</b></p><p>Chargez l’image d’arrière-plan ou mappez le fichier image d’un module précédent.</p></li><li><p><b>URL de l’image</b></p><p>Saisissez ou mappez l’URL de l’image d’arrière-plan.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Background &gt; Remplir le masque de zone &gt; Source]</td> 
   <td>Sélectionnez la manière dont vous fournissez le masque de zone de remplissage. Le masque de zone de remplissage indique la zone de l'arrière-plan où l'objet sera placé.<ul><li><p><b>Charger l’image</b></p><p>Chargez l’image du masque de zone de remplissage ou mappez le fichier image d’un module précédent.</p></li><li><p><b>URL de l’image</b></p><p>Saisissez ou mappez l’URL de l’image du masque de zone de remplissage.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object &gt; Image &gt; Source]</td> 
   <td>Sélectionnez la manière dont vous fournissez l’image de l’objet. L’image de l’objet est l’image source de l’objet à composer en arrière-plan.<ul><li><p><b>Charger l’image</b></p><p>Chargez l’image de l’objet ou mappez le fichier image d’un module précédent.</p></li><li><p><b>URL de l’image</b></p><p>Saisissez ou mappez l’URL de l’image de l’objet.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nombre de variations]</td> 
   <td>Entrez un nombre compris entre 1 et 3. Le module génère ce nombre de variations composites.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Seeds]*</td> 
   <td>Cliquez sur <b>Ajouter un élément</b> pour ajouter une valeur de départ, puis saisissez ou mappez un entier. Utilisez une adresse de contrôle par variation. Le nombre de valeurs de départ doit correspondre à la valeur [!UICONTROL Number of Variations] si les deux sont fournis.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blend]*</td> 
   <td>Entrez un nombre compris entre 0 et 1 pour contrôler le mélange entre l'apparence harmonisée et originale de l'objet. <code>0.0</code> applique une harmonisation complète et conserve <code>1.0</code> l’aspect de l’objet d’origine.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output &gt; Media Type]*</td> 
   <td>Sélectionnez le format de fichier sous lequel le composite généré sera enregistré.</td> 
  </tr> 
 </tbody> 
</table>

* Ces champs sont des champs avancés et ne s’affichent que si vous sélectionnez **[!UICONTROL Afficher les paramètres avancés]**.

### Générer des images similaires

Ce module d’action génère des images similaires à l’image source que vous spécifiez.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Firefly], voir <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Créer une connexion à [!DNL Adobe Firefly]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nombre de variations]</td> 
   <td>Entrez un nombre compris entre 1 et 4. Le module génère ce nombre de variations d’image.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model version]</td> 
   <td>Sélectionnez la version du modèle Firefly que vous souhaitez utiliser pour générer les images.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Generated image format]</td> 
   <td>Sélectionnez le format de fichier sous lequel l’image développée sera enregistrée. Si vous sélectionnez par défaut, le format du fichier est JPEG si aucune image de référence n’est fournie. Si une image de référence est fournie, le format de fichier de l’image générée est identique à celui de l’image de référence.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Image &gt; Source]</td> 
    <td>Sélectionnez la manière dont vous fournissez le fichier source pour la structure de la nouvelle image :<ul><li><p><b>Fichier</b></p><p>Sélectionnez un fichier source dans un module précédent ou mappez le nom de fichier image de référence et le fichier image de référence du fichier source.</p></li><li><p><b>URL prédéfinie</b></p><p>Saisissez ou mappez l’URL de l’image source.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style &gt; Référence d’image]</td> 
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


### Générer une vidéo

Ce module d’action génère une vidéo à partir d’une invite de texte. Vous pouvez également fournir une ou plusieurs images de référence pour guider la génération vidéo.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Firefly], voir <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Créer une connexion à [!DNL Adobe Firefly]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Prompt]</td> 
   <td>Saisissez ou mappez une description de la vidéo que vous souhaitez générer. Plus de détails dans l’invite vous permettent de mieux contrôler ce qui apparaît dans la vidéo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Image &gt; Conditions]</td> 
   <td>Fournissez éventuellement une ou plusieurs images de référence pour guider la génération vidéo. Cliquez sur <b>Ajouter un élément</b> pour chaque image de référence.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tailles]</td> 
   <td>Cliquez sur <b>Ajouter un élément</b> et saisissez ou mappez les dimensions de la vidéo générée.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bit Rate Factor]*</td> 
   <td>Entrez un nombre compris entre 0 et 63 pour spécifier le facteur de débit de la vidéo générée.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Video Settings &gt; Camera Motion]*</td> 
   <td>Sélectionnez le mouvement de caméra à utiliser dans la vidéo générée.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Video Settings &gt; Style d'invite]*</td> 
   <td>Sélectionnez le style d’invite à utiliser pour la vidéo générée.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Paramètres Vidéo &gt; Angle De Prise De Vue]*</td> 
   <td>Sélectionnez l’angle de prise de vue à utiliser dans la vidéo générée.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Video Settings &gt; Taille de la prise de vue]*</td> 
   <td>Sélectionnez la taille de prise de vue à utiliser dans la vidéo générée.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Saisissez ou mappez le nombre maximal de résultats avec lesquels vous souhaitez que le module fonctionne au cours d’un cycle d’exécution.</td> 
  </tr> 
 </tbody> 
</table>

* Ces champs sont des champs avancés et ne s’affichent que si vous sélectionnez **[!UICONTROL Afficher les paramètres avancés]**.

### Effectuer un appel API personnalisé

Ce module d’action effectue un appel personnalisé à l’API Firefly.

Pour connaître les API spécifiques disponibles, consultez [API &#x200B;](https://developer.adobe.com/firefly-services/docs/firefly-api/) dans la documentation d’Adobe Developer.

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
        <p>Saisissez un chemin d’accès relatif à <code>https://firefly-api.adobe.io/</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, consultez <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p>
        <p>Par exemple, <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion ajoute automatiquement des en-têtes d’autorisation.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre JSON, placez les guillemets à l’extérieur de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

