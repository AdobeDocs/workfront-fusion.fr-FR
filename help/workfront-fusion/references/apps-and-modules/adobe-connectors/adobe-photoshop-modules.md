---
title: Modules Adobe Photoshop
description: Avec les modules Adobe Photoshop, vous pouvez lancer un scénario Adobe Workfront Fusion en fonction des événements de votre compte Adobe Photoshop, créer, lire ou mettre à jour des contrats et d’autres enregistrements, rechercher des enregistrements à l’aide des critères que vous avez définis et charger des documents.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 0e41d1af-af69-4f9b-a5b3-479562254084
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '5392'
ht-degree: 12%

---

# Modules [!DNL Adobe Photoshop]

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent [!DNL Adobe Photoshop] et les connecter à plusieurs applications et services tiers.


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
   <p>Actuel : aucune exigence de licence Workfront Fusion</p>
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

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Conditions préalables

Avant d’utiliser le connecteur [!DNL Adobe Photoshop], vous devez vous assurer que les conditions préalables suivantes sont remplies :

* Vous devez disposer d’un compte [!DNL Adobe Photoshop].
* Vous devez posséder une licence Firefly Services.
* Vous devez disposer d’un identifiant client et d’un secret client. Vous pouvez les acquérir à partir du Adobe Developer Console.

## Informations sur l’API Adobe Photoshop

Le connecteur Adobe Photoshop utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td>https://image.adobe.io/pie/psdService</td> 
  </tr>
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.12.31</td> 
  </tr>
 </tbody> 
 </table>

## Créer une connexion à [!DNL Adobe Photoshop]

Pour créer une connexion pour vos modules [!DNL Adobe Photoshop], procédez comme suit :

1. Dans n’importe quel module, cliquez sur **[!UICONTROL Ajouter]** en regard de la zone Connexion .

1. Remplissez les champs suivants :

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>
          <p>Choisissez si vous souhaitez utiliser une connexion JWT ou une connexion serveur à serveur.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Saisissez un nom pour cette connexion.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Saisissez votre [!UICONTROL Adobe] [!UICONTROL Client ID]. Vous pouvez le trouver dans la section des détails des [!UICONTROL Credentials] du [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Saisissez votre [!UICONTROL Client Secret] [!DNL Adobe]. Vous pouvez le trouver dans la section des détails des [!UICONTROL Credentials] du [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Technical account ID]</td>
        <td>Si vous utilisez une connexion JWT, saisissez votre [!UICONTROL Identifiant de compte technique] [!DNL Adobe]. Vous pouvez le trouver dans la section des détails des [!UICONTROL Credentials] du [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Organization ID]</td>
        <td>Si vous utilisez une connexion JWT, saisissez votre [!UICONTROL Organization ID] [!DNL Adobe]. Vous pouvez le trouver dans la section des détails des [!UICONTROL Credentials] du [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Private key]</td>
        <td>
          <p>Si vous utilisez une connexion JWT, saisissez la clé privée qui a été générée lors de la création de vos informations d’identification dans le [!DNL Adobe Developer Console]. </p>
          <p>Pour extraire votre clé privée ou votre certificat privé, procédez comme suit :</p>
          <ol>
            <li value="1">
              <p>Cliquez sur <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li value="2">
              <p>Sélectionnez le type de fichier que vous extrayez.</p>
            </li>
            <li value="3">
              <p>Sélectionnez le fichier contenant la clé privée ou le certificat privé.</p>
            </li>
            <li value="4">
              <p>Saisissez le mot de passe du fichier.</p>
            </li>
            <li value="5">
              <p>Cliquez sur <b>Enregistrer</b> pour extraire le fichier et revenir à la configuration de la connexion.</p>
            </li>
          </ol>
        </td>
        </tr>
      </tbody>
    </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour enregistrer la connexion et revenir au module.

## Modules [!DNL Adobe Photoshop] et leurs champs

Lorsque vous configurez les modules [!DNL Adobe Photoshop], Workfront Fusion affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Adobe Photoshop] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Application des modifications PSD](#apply-psd-edits)
* [Correction automatique des couleurs d’une image](#auto-color-correct-an-image)
* [Convertir le format d’image](#convert-image-format)
* [Création d’un masque](#create-a-mask)
* [Création d’un nouveau PSD](#create-a-new-psd)
* [Modifier des calques de texte](#edit-text-layers)
* [Modifier les calques de texte (hérités)](#edit-text-layers-legacy)
* [Exécuter une action JSON](#execute-an-action-json)
* [Flou relatif à la profondeur d’exécution](#execute-depth-blur)
* [Exécution d’actions Photoshop](#execute-photoshop-actions)
* [Exécuter le recadrage de produit](#execute-product-crop)
* [Obtenir les informations sur le calque](#get-layer-info)
* [Effectuer un appel API personnalisé.](#make-a-custom-api-call)
* [Supprimer l’arrière-plan](#remove-background)
* [Remplacement d’un objet dynamique](#replace-a-smart-object)
* [Remplacement d’un objet dynamique (hérité)](#replace-a-smart-object-legacy)
* [Redimensionnement d’une image](#resize-an-image)
* [Filigrane d’une image](#watermark-an-image)

### Application des modifications PSD

Ce module d’action applique diverses modifications au niveau du document et des calques.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Photoshop], voir <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Créer une connexion à [!DNL Adobe Photoshop]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel le fichier que vous souhaitez modifier est stocké.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Input) File location]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès du fichier que vous souhaitez modifier. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options &gt; Document &gt; Taille de l’image) Hauteur]</p>
      </td>
      <td> Saisissez ou mappez la hauteur de l’image en pixels. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options &gt; Document &gt; Taille de l’image) Largeur]</p>
      </td>
      <td> Saisissez ou mappez la largeur de l’image en pixels. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options &gt; Document &gt; Taille de la zone de travail) Haut]</p>
      </td>
   <td> Saisissez ou mappez, en pixels, la coordonnée y du coin supérieur gauche du document. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options &gt; Document &gt; Taille de la zone de travail) Bas]</p>
      </td>
   <td> Saisissez ou mappez, en pixels, la coordonnée y du coin inférieur droit du document. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options &gt; Document &gt; Taille de la zone de travail) à gauche]</p>
      </td>
   <td> Saisissez ou mappez, en pixels, la coordonnée x du coin supérieur gauche du document. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options &gt; Document &gt; Taille de la zone de travail) Droite]</p>
      </td>
   <td> Saisissez ou mappez, en pixels, la coordonnée x du coin inférieur droit du document. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options &gt; Document) Trim]</p>
      </td>
   <td> Sélectionnez Pixels transparents pour baser le rognage sur les pixels transparents de l’image. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Default font]</p>
      </td>
   <td> Saisissez le nom postscript complet de la police à utiliser comme valeur par défaut globale pour le document. Cette police sera utilisée pour tout calque de texte qui comporte une police manquante et pour lequel aucune autre police n’a été spécifiquement fournie. Si cette police est manquante, l’option spécifiée dans Gérer les polices manquantes prend effet. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Fonts]</p>
      </td>
   <td> Pour chaque police dont le document a besoin, cliquez sur Ajouter un élément et saisissez l’emplacement de stockage et de fichier de la police. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Gérer les polices manquantes]</p>
      </td>
   <td> Sélectionnez l’action à effectuer s’il manque une ou plusieurs polices dans le document. <ul><li><code>fail</code>: la tâche ne réussira pas et le statut sera défini sur échec, avec les détails de l’erreur fournis dans la section détails du statut.</li><li><code>useDefault</code>: le traitement réussit et toutes les polices manquantes sont remplacées par ArialMT.</li></ul></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Calques]</p>
      </td>
   <td> Pour chaque calque à ajouter, cliquez sur Ajouter un élément et renseignez les détails du calque. <p>Pour plus d’informations sur les options de calque, voir <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_applyPsdEdits/">Appliquer les modifications PSD</a> dans la documentation d’Adobe Photoshop.  </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Pour chaque fichier modifié que vous souhaitez créer, cliquez sur Ajouter un élément et saisissez le stockage, l’emplacement et le type répertoriés dans ce tableau.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel vous souhaitez stocker le nouveau fichier.</p><p>La sélection du stockage interne Fusion rend le fichier disponible pour les modules ultérieurs, mais ne rend pas le fichier disponible en dehors du scénario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès de l’emplacement de stockage du nouveau fichier. Cela n’est nécessaire que si vous n’avez pas choisi le stockage interne Fusion pour le stockage de sortie.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td>Sélectionnez le type de fichier vers lequel vous souhaitez convertir le fichier. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Indiquez si le fichier nouvellement modifié remplacera un fichier de sortie existant. Cela s’applique uniquement aux fichiers dans l’espace de stockage Adobe.</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Trim to Canvas]</p>
      </td>
   <td>Indiquez si les rendus doivent être de taille Zone de travail. True ajuste les rendus à la taille de la zone de travail, tandis que False les rend à la taille du calque.</td> 
    </tr>
    </tbody>
</table>

### Correction automatique des couleurs d’une image

Ce module d’action corrige automatiquement la couleur de l’image spécifiée.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Photoshop], voir <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Créer une connexion à [!DNL Adobe Photoshop]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel le fichier dont vous souhaitez corriger les couleurs est stocké.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Input) File location]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès du fichier dont vous souhaitez corriger la couleur. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel vous souhaitez stocker le nouveau fichier.</p><p>La sélection du stockage interne Fusion rend le fichier disponible pour les modules ultérieurs, mais ne rend pas le fichier disponible en dehors du scénario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès de l’emplacement de stockage du nouveau fichier. Cela n’est nécessaire que si vous n’avez pas choisi le stockage interne Fusion pour le stockage de sortie.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td>Sélectionnez le type de fichier vers lequel vous souhaitez convertir le fichier. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Indiquez si le fichier nouvellement modifié remplacera un fichier de sortie existant. Cela s’applique uniquement aux fichiers dans l’espace de stockage Adobe.</p>
      </td>
    </tr>
    </tbody>
</table>

### Convertir le format d’image

Ce module d’action convertit un fichier en JPEG, PNG, PSD ou TIFF.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Photoshop], voir <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Créer une connexion à [!DNL Adobe Photoshop]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel est stocké le fichier que vous souhaitez supprimer de l’arrière-plan.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Input) File location]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès au fichier duquel vous souhaitez supprimer l’arrière-plan. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Pour chaque fichier converti que vous souhaitez créer, cliquez sur Ajouter un élément et saisissez le stockage, l’emplacement et le type répertoriés dans ce tableau.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel vous souhaitez stocker le nouveau fichier.</p><p>La sélection du stockage interne Fusion rend le fichier disponible pour les modules ultérieurs, mais ne rend pas le fichier disponible en dehors du scénario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès de l’emplacement de stockage du nouveau fichier. Cela n’est nécessaire que si vous n’avez pas choisi le stockage interne Fusion pour le stockage de sortie. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td>Sélectionnez le type de fichier vers lequel vous souhaitez convertir le fichier. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Indiquez si le fichier nouvellement modifié remplacera un fichier de sortie existant. Cela s’applique uniquement aux fichiers dans l’espace de stockage Adobe.</p>
      </td>
    </tr>
    </tbody>
</table>

### Création d’un masque

Ce module d’action renvoie un fichier PNG avec un masque appliqué autour du sujet.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Photoshop], voir <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Créer une connexion à [!DNL Adobe Photoshop]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers à partir duquel est stocké le fichier à partir duquel vous souhaitez créer un masque.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Input) File location]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès au fichier à partir duquel vous souhaitez créer un masque. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel vous souhaitez stocker le fichier de masque.</p><p>La sélection du stockage interne Fusion rend le fichier disponible pour les modules ultérieurs, mais ne rend pas le fichier disponible en dehors du scénario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès où le fichier de masque sera stocké. Cela n’est nécessaire que si vous n’avez pas choisi le stockage interne Fusion pour le stockage de sortie.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Overwrite]</td>
      <td>
        <p>Indiquez si le fichier nouvellement modifié remplacera un fichier de sortie existant. Cela s’applique uniquement aux fichiers dans l’espace de stockage Adobe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Color space]</p>
      </td>
   <td>Choisissez si l’image de sortie utilise la couleur RGB ou RGBA. </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Mask format]</p>
      </td>
   <td>Indiquez si le masque doit être souple (en drapeau) ou binaire. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Optimize]</p>
      </td>
   <td>Sélectionnez Performances pour optimiser la vitesse ou Lot pour permettre le temps d’attente. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Post process]</p>
      </td>
   <td>Choisissez d’activer ou non le post-traitement.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Version]</p>
      </td>
   <td>La valeur par défaut est 4.0</td> 
    </tr> 
    </tbody>
</table>

### Création d’un nouveau PSD

Ce module d’action crée un nouveau PSD avec des calques facultatifs et génère des rendus ou des enregistrements en tant que PSD.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Photoshop], voir <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Créer une connexion à [!DNL Adobe Photoshop]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options &gt; Document &gt; Taille de l’image) Hauteur]</p>
      </td>
      <td> Saisissez ou mappez la hauteur de l’image en pixels. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options &gt; Document &gt; Taille de l’image) Largeur]</p>
      </td>
      <td> Saisissez ou mappez la largeur de l’image en pixels. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options &gt; Document) Résolution]</p>
      </td>
   <td> Saisissez ou mappez, en pixels par pouce, la résolution de l’image. Ce doit être entre 72 et 300. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options &gt; Document) Mode]</p>
      </td>
   <td> Sélectionnez le mode de l’image. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options &gt; Document) Fill]</p>
      </td>
   <td> Choisissez si vous souhaitez que le remplissage du calque d’arrière-plan soit transparent, blanc ou la couleur d’arrière-plan de l’image. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options &gt; Document) Depth]</p>
      </td>
   <td> Sélectionnez la profondeur de l’image. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Calques]</p>
      </td>
   <td> Pour chaque calque à ajouter, cliquez sur Ajouter un élément et renseignez les détails du calque. <p>Pour plus d’informations sur les options de calque, voir <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_createPsd/">Créer un PSD</a> dans la documentation d’Adobe Photoshop.  </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Global font]</p>
      </td>
   <td> Saisissez le nom postscript complet de la police à utiliser comme valeur par défaut globale pour le document. Cette police sera utilisée pour tout calque de texte qui comporte une police manquante et pour lequel aucune autre police n’a été spécifiquement fournie. Si cette police est manquante, l’option spécifiée dans Gérer les polices manquantes prend effet. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Fonts]</p>
      </td>
   <td> Pour chaque police dont le document a besoin, cliquez sur Ajouter un élément et saisissez l’emplacement de stockage et de fichier de la police. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Gérer les polices manquantes]</p>
      </td>
   <td> Sélectionnez l’action à effectuer s’il manque une ou plusieurs polices dans le document. <ul><li><code>fail</code>: la tâche ne réussira pas et le statut sera défini sur échec, avec les détails de l’erreur fournis dans la section détails du statut.</li><li><code>useDefault</code>: le traitement réussit et toutes les polices manquantes sont remplacées par ArialMT.</li></ul></td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Pour chaque fichier que vous souhaitez créer, cliquez sur Ajouter un élément et saisissez le stockage, l’emplacement et le type répertoriés dans ce tableau.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel vous souhaitez stocker le nouveau fichier.</p><p>La sélection du stockage interne Fusion rend le fichier disponible pour les modules ultérieurs, mais ne rend pas le fichier disponible en dehors du scénario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès de l’emplacement de stockage du nouveau fichier. Cela n’est nécessaire que si vous n’avez pas choisi le stockage interne Fusion pour le stockage de sortie.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td>Sélectionnez le type de fichier vers lequel vous souhaitez convertir le fichier. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Autres champs]</td>
      <td>
        <p><p>Pour plus d’informations sur les options de sortie, voir <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_createPsd/">Créer un PSD</a> dans la documentation d’Adobe Photoshop.  </p>
      </td>
    </tr>
    </tbody>
</table>

### Modifier des calques de texte

Ce module d’action modifie les calques de texte d’un fichier Photoshop. Vous pouvez saisir des détails de modification distincts pour plusieurs calques dans le même fichier.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Photoshop], voir <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Créer une connexion à [!DNL Adobe Photoshop]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Input file storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel le fichier que vous souhaitez modifier est stocké.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Input file URL]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès du fichier que vous souhaitez modifier. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gérer les polices manquantes]</td>
      <td>
        <p>Sélectionnez l’action à effectuer s’il manque une ou plusieurs polices dans le document. Si la police n’est pas fournie, le module utilise la police par défaut.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Default font]  </td>
      <td>
        <p>Saisissez le nom postscript complet de la police à utiliser comme valeur par défaut globale pour le document. Cette police sera utilisée pour tout calque de texte qui comporte une police manquante et pour lequel aucune autre police n’a été spécifiquement fournie. Si cette police est manquante, l’option spécifiée dans Gérer les polices manquantes prend effet.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Fonts]</p>
      </td>
   <td> Saisissez l’emplacement de stockage et de fichier de la police. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Layers]</td>
   <td> <p>Pour chaque calque de texte à modifier, cliquez sur <b>Ajouter un élément</b> et saisissez les options de calque.<p>Pour plus d’informations sur les options de calque, voir <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_editText/">Modifier le texte</a> dans la documentation d’Adobe Photoshop.</p>  </td>     </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel vous souhaitez stocker le fichier modifié.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès de l’emplacement de stockage du fichier modifié. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td> Sélectionnez le type de fichier pour le fichier modifié. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Indiquez si le fichier nouvellement modifié remplacera un fichier de sortie existant.</p>
      </td>
    </tr>
  </tbody>
</table>

### Modifier les calques de texte (hérités)

Ce module d’action modifie un calque de texte sur un fichier Photoshop.

Pour modifier plusieurs calques, utilisez le module [Modifier les calques de texte](#edit-text-layers).

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Photoshop], voir <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Créer une connexion à [!DNL Adobe Photoshop]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Input file storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel le fichier que vous souhaitez modifier est stocké.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Input file URL]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès du fichier que vous souhaitez modifier. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gérer les polices manquantes]</td>
      <td>
        <p>Sélectionnez l’action à effectuer s’il manque une ou plusieurs polices dans le document. Si la police n’est pas fournie, le module utilise la police par défaut.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Default font]  </td>
      <td>
        <p>Saisissez le nom postscript complet de la police à utiliser comme valeur par défaut globale pour le document. Cette police sera utilisée pour tout calque de texte qui comporte une police manquante et pour lequel aucune autre police n’a été spécifiquement fournie. Si cette police est manquante, l’option spécifiée dans Gérer les polices manquantes prend effet.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Options) Fonts]</p>
      </td>
   <td> Saisissez l’emplacement de stockage et de fichier de la police. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Layers]</td>
   <td> <p>Pour plus d’informations sur les options de calque, voir <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_editText/">Modifier le calque de texte</a> dans la documentation d’Adobe Photoshop.</p>  </td>     </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Stockage du fichier de sortie]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel vous souhaitez stocker le fichier modifié.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel vous souhaitez stocker le fichier modifié.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès de l’emplacement de stockage du fichier modifié. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td> Sélectionnez le type de fichier pour le fichier modifié. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Indiquez si le fichier nouvellement modifié remplacera un fichier de sortie existant.</p>
      </td>
    </tr>
  </tbody>
</table>


### Exécuter une action JSON

Ce module d’action exécute des actions Photoshop à l’aide de commandes JSON.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Photoshop], voir <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Créer une connexion à [!DNL Adobe Photoshop]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel le fichier que vous souhaitez modifier est stocké.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Input) File location]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès du fichier que vous souhaitez modifier. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL , action JSON]</td>
      <td>
        <p>Saisissez la commande JSON correspondant à l’action à effectuer.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Polices / Motifs / Brosses / Images supplémentaires]</td>
      <td>
        <p>Pour chaque police, modèle, pinceau ou image supplémentaire à utiliser dans cette action, cliquez sur Ajouter un élément et saisissez l’espace de stockage et l’emplacement du fichier de l’élément.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Font / Pattern / Brush file URL]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès au fichier que vous souhaitez utiliser. </td> 
    </tr>
    <tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Pour chaque fichier à créer, cliquez sur Ajouter un élément et saisissez les options de stockage, d'emplacement, de type et de remplacement répertoriées dans ce tableau.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Sorties) Storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel vous souhaitez stocker le fichier modifié.</p><p>La sélection du stockage interne Fusion rend le fichier disponible pour les modules ultérieurs, mais ne rend pas le fichier disponible en dehors du scénario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Sorties) URL du fichier]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès de l’emplacement de stockage du fichier modifié.  Cela n’est nécessaire que si vous n’avez pas choisi le stockage interne Fusion pour le stockage de sortie.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Sorties) Type]</p>
      </td>
   <td> Sélectionnez le type de fichier pour le fichier modifié. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Sorties) Remplacer]</td>
      <td>
        <p>Indiquez si le fichier nouvellement modifié remplacera un fichier de sortie existant.</p>
      </td>
    </tr>
      </tbody>
</table>

### Flou relatif à la profondeur d’exécution

Ce module d’action exécute l’action Flou de profondeur sur le fichier sélectionné.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Photoshop], voir <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Créer une connexion à [!DNL Adobe Photoshop]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Input file storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel le fichier que vous souhaitez modifier est stocké.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Input file URL]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès du fichier que vous souhaitez modifier. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Sorties) Storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel vous souhaitez stocker le fichier modifié.</p><p>La sélection du stockage interne Fusion rend le fichier disponible pour les modules ultérieurs, mais ne rend pas le fichier disponible en dehors du scénario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Sorties) URL du fichier]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès de l’emplacement de stockage du fichier modifié.  Cela n’est nécessaire que si vous n’avez pas choisi le stockage interne Fusion pour le stockage de sortie.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Sorties) Type]</p>
      </td>
   <td> Sélectionnez le type de fichier pour le fichier modifié. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Sorties) Remplacer]</td>
      <td>
        <p>Indiquez si le fichier nouvellement modifié remplacera un fichier de sortie existant.</p>
      </td>
    </tr>
   <tr>
      <td role="rowheader">[!UICONTROL Other fields]</td>
      <td>
        <p>Pour plus d’informations sur les autres options de flou de profondeur, voir <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_depthBlur/">Execute Depth Blur</a> dans la documentation de l’API Adobe Photoshop.</p>
      </td>
    </tr>
  </tbody>
</table>

### Exécution d’actions Photoshop

Ce module d’action exécute une action Photoshop sur l’image sélectionnée.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Photoshop], voir <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Créer une connexion à [!DNL Adobe Photoshop]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Input file storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel le fichier que vous souhaitez modifier est stocké.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Input file URL]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès du fichier que vous souhaitez modifier. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Actions file storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel le fichier d’actions est stocké.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Actions file URL]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès du fichier d’actions. </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Nom de l’action]</p>
      </td>
   <td> Si vous souhaitez uniquement exécuter une action spécifique, vous pouvez spécifier l’action à lire à partir du jeu d’actions. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Font / Pattern / Brush storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel le fichier que vous souhaitez utiliser est stocké.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Font / Pattern / Brush file URL]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès au fichier que vous souhaitez utiliser. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Sorties) Storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel vous souhaitez stocker le fichier modifié.</p><p>La sélection du stockage interne Fusion rend le fichier disponible pour les modules ultérieurs, mais ne rend pas le fichier disponible en dehors du scénario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Sorties) URL du fichier]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès de l’emplacement de stockage du fichier modifié.  Cela n’est nécessaire que si vous n’avez pas choisi le stockage interne Fusion pour le stockage de sortie.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Sorties) Type]</p>
      </td>
   <td> Sélectionnez le type de fichier pour le fichier modifié. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Sorties) Remplacer]</td>
      <td>
        <p>Indiquez si le fichier nouvellement modifié remplacera un fichier de sortie existant.</p>
      </td>
    </tr>
   <tr>
      <td role="rowheader">[!UICONTROL Other fields]</td>
      <td>
        <p>Pour plus d’informations sur les autres options de flou de profondeur, voir <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_depthBlur/">Execute Depth Blur</a> dans la documentation de l’API Adobe Photoshop.</p>
      </td>
    </tr>
  </tbody>
</table>

### Exécuter le recadrage de produit

Ce module d’action exécute le recadrage de produit sur l’image sélectionnée.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Photoshop], voir <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Créer une connexion à [!DNL Adobe Photoshop]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Input file storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel le fichier à recadrer est stocké.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Input file URL]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès du fichier que vous souhaitez recadrer. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Unit]</p>
      </td>
   <td> Choisissez si vous souhaitez décrire l’ajustement de la hauteur et de la largeur en pixels ou en pourcentage. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Width]</p>
      </td>
   <td> Saisissez ou mappez la quantité de remplissage de largeur que vous souhaitez ajouter. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Height]</p>
      </td>
   <td> Saisissez ou mappez la quantité de remplissage en hauteur à ajouter. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Sorties) Storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel vous souhaitez stocker le fichier modifié.</p><p>La sélection du stockage interne Fusion rend le fichier disponible pour les modules ultérieurs, mais ne rend pas le fichier disponible en dehors du scénario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Sorties) URL du fichier]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès de l’emplacement de stockage du fichier modifié.  Cela n’est nécessaire que si vous n’avez pas choisi le stockage interne Fusion pour le stockage de sortie.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Sorties) Type]</p>
      </td>
   <td> Sélectionnez le type de fichier pour le fichier modifié. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Sorties) Remplacer]</td>
      <td>
        <p>Indiquez si le fichier nouvellement modifié remplacera un fichier de sortie existant.</p>
      </td>
    </tr>
   <tr>
      <td role="rowheader">[!UICONTROL Other fields]</td>
      <td>
        <p>Pour plus d’informations sur les autres options de flou de profondeur, voir <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_depthBlur/">Execute Depth Blur</a> dans la documentation de l’API Adobe Photoshop.</p>
      </td>
    </tr>
  </tbody>
</table>

### Obtenir les informations sur le calque

Ce module d’action récupère les informations de calque du fichier PSD spécifié.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Photoshop], voir <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Créer une connexion à [!DNL Adobe Photoshop]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Input file storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel est stocké le fichier à partir duquel vous souhaitez récupérer les informations de calque.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Input file URL]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès au fichier à partir duquel vous souhaitez récupérer les informations de calque. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Thumbnails]</p>
      </td>
   <td> Sélectionnez le type de fichier dont vous souhaitez afficher les miniatures. Les miniatures sont de petits aperçus pour tout calque rendu.</td> 
    </tr>
  </tbody>
</table>

### Effectuer un appel API personnalisé.

Ce module d’action effectue un appel personnalisé à l’API Photoshop.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Photoshop], voir <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Créer une connexion à [!DNL Adobe Photoshop]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Saisissez un chemin relatif à <code>https://image.adobe.io/pie/psdService</code>. Exemple : <code>/photoshopActions</code></p>
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
        <p>Workfront Fusion ajoute automatiquement des en-têtes d’autorisation.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Saisissez la chaîne de requête.</p>
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

### Supprimer l’arrière-plan

Ce module d’action identifie l’objet principal de votre image et supprime l’arrière-plan.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Photoshop], voir <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Créer une connexion à [!DNL Adobe Photoshop]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel est stocké le fichier que vous souhaitez supprimer de l’arrière-plan.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Input) File location]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès au fichier duquel vous souhaitez supprimer l’arrière-plan. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel vous souhaitez stocker le nouveau fichier.</p><p>La sélection du stockage interne Fusion rend le fichier disponible pour les modules ultérieurs, mais ne rend pas le fichier disponible en dehors du scénario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès de l’emplacement de stockage du nouveau fichier.  Cela n’est nécessaire que si vous n’avez pas choisi le stockage interne Fusion pour le stockage de sortie.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Overwrite]</td>
      <td>
        <p>Indiquez si le fichier nouvellement modifié remplacera un fichier de sortie existant. Cela s’applique uniquement aux fichiers dans l’espace de stockage Adobe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Color space]</p>
      </td>
   <td>Choisissez si l’image de sortie utilise la couleur RGB ou RGBA. </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Mask format]</p>
      </td>
   <td>Indiquez si les bords de l’image doivent être lisses (contours progressifs) ou binaires. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Optimize]</p>
      </td>
   <td>Sélectionnez Performances pour optimiser la vitesse ou Lot pour permettre le temps d’attente. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Post process]</p>
      </td>
   <td>Choisissez d’activer ou non le post-traitement.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Version]</p>
      </td>
   <td>La valeur par défaut est 4.0</td> 
    </tr> 
    </tbody>
</table>

### Remplacement d’un objet dynamique

Ce module d’action remplace un objet dynamique dans un calque PSD et génère de nouveaux rendus.

Ce module utilise l’API d’objet intelligent version 2.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Photoshop], voir <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Créer une connexion à [!DNL Adobe Photoshop]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel l’objet dynamique est stocké.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Input) File location]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès de l’objet dynamique. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Layers]</p>
      </td>
   <td>Pour chaque calque que vous souhaitez ajouter à l’objet dynamique, cliquez sur Ajouter un élément et saisissez le nom ou l’ID de l’objet, le service de fichiers dans lequel l’objet dynamique est stocké et l’URL ou le chemin d’accès du calque.<p>Pour obtenir une description des paramètres avancés de cette zone, voir <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_replaceSmartObject/">Remplacer un objet dynamique</a> dans la documentation de l’API Photoshop </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Redimensionner l'image pendant le déplacement]</p>
      </td>
   <td> Choisissez si vous souhaitez redimensionner l’image.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Pour chaque nouveau rendu que vous souhaitez que le module produise, cliquez sur Ajouter un élément et renseignez les champs suivants. Vous pouvez avoir un maximum de 25 fichiers de sortie.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel vous souhaitez stocker le nouveau fichier.</p><p>La sélection du stockage interne Fusion rend le fichier disponible pour les modules ultérieurs, mais ne rend pas le fichier disponible en dehors du scénario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès de l’emplacement de stockage du nouveau fichier.  Cela n’est nécessaire que si vous n’avez pas choisi le stockage interne Fusion pour le stockage de sortie.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Sorties) Type]</p>
      </td>
   <td> Sélectionnez le type de fichier pour le fichier modifié. </td> 
    </tr>
     </tbody>
</table>

### Remplacement d’un objet intelligent (hérité)

Ce module d’action remplace un objet dynamique dans un calque PSD et génère de nouveaux rendus.

Ce module utilise l’ancienne version des objets dynamiques.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Photoshop], voir <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Créer une connexion à [!DNL Adobe Photoshop]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Input) Storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel l’objet dynamique est stocké.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Input) File location]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès de l’objet dynamique. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Layers]</p>
      </td>
   <td>Pour chaque calque que vous souhaitez ajouter à l’objet dynamique, cliquez sur Ajouter un élément et saisissez le nom ou l’ID de l’objet, le service de fichiers dans lequel l’objet dynamique est stocké et l’URL ou le chemin d’accès du calque.<p>Pour obtenir une description des paramètres avancés de cette zone, voir <a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_replaceSmartObject/">Remplacer un objet dynamique</a> dans la documentation de l’API Photoshop </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Pour chaque nouveau rendu que vous souhaitez que le module produise, cliquez sur Ajouter un élément et renseignez les champs suivants. Vous pouvez avoir un maximum de 25 fichiers de sortie.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel vous souhaitez stocker le nouveau fichier.</p><p>La sélection du stockage interne Fusion rend le fichier disponible pour les modules ultérieurs, mais ne rend pas le fichier disponible en dehors du scénario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès de l’emplacement de stockage du nouveau fichier.  Cela n’est nécessaire que si vous n’avez pas choisi le stockage interne Fusion pour le stockage de sortie.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Sortie) Largeur]</p>
      </td>
   <td> Largeur, en pixels, du fichier de sortie. Le module conserve les proportions d’origine. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Indiquez si le fichier nouvellement modifié remplacera un fichier de sortie existant. Cela s’applique uniquement aux fichiers dans l’espace de stockage Adobe.</p>
      </td>
    </tbody>
</table>

### Redimensionnement d’une image

Cette action redimensionne une image en utilisant les mêmes proportions.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Photoshop], voir <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Créer une connexion à [!DNL Adobe Photoshop]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel le fichier à redimensionner est stocké.</p><p>La sélection du stockage interne Fusion rend le fichier disponible pour les modules ultérieurs, mais ne rend pas le fichier disponible en dehors du scénario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Emplacement du fichier]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès du fichier à redimensionner.  Cela n’est nécessaire que si vous n’avez pas choisi le stockage interne Fusion pour le stockage de sortie.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Outputs]</td>
      <td>
        <p>Pour chaque fichier converti que vous souhaitez créer, cliquez sur Ajouter un élément et saisissez les options de stockage, d’emplacement et autres, comme indiqué dans ce tableau.</p>
      </td>
    </tr>
    <tr>
    <tr>
      <td role="rowheader">[!UICONTROL Storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel vous souhaitez stocker le nouveau fichier.</p><p>La sélection du stockage interne Fusion rend le fichier disponible pour les modules ultérieurs, mais ne rend pas le fichier disponible en dehors du scénario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Emplacement du fichier]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès de l’emplacement de stockage du nouveau fichier.  Cela n’est nécessaire que si vous n’avez pas choisi le stockage interne Fusion pour le stockage de sortie.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Width]</p>
      </td>
   <td> Largeur, en pixels, du fichier de sortie. Le module conserve les proportions d’origine. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Largeur max.]</p>
      </td>
   <td>Lorsque la largeur est égale à 0, la propriété Max avec peut être fournie pour obtenir la taille. La largeur maximale est prioritaire et est inférieure à la largeur du document.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Overwrite]</td>
      <td>
        <p>Indiquez si le fichier nouvellement modifié remplacera un fichier de sortie existant. Cela s’applique uniquement aux fichiers dans l’espace de stockage Adobe.</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[!UICONTROL Rogner sur la zone de travail]</p>
      </td>
   <td>Sélectionnez Oui pour ajuster les rendus à la taille de la zone de travail ou Non pour définir la taille du calque des rendus.</td> 
    </tr>
    </tbody>
</table>

### Filigrane d’une image

Ce module d’action ajoute un filigrane à l’image sélectionnée.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Photoshop], voir <a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >Créer une connexion à [!DNL Adobe Photoshop]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Base &gt; Entrée) Stockage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel est stocké le fichier auquel vous souhaitez ajouter un filigrane.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Base &gt; Entrée) Emplacement du fichier]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès du fichier auquel vous souhaitez ajouter un filigrane. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Filigrane &gt; Entrée) Stockage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel est stocké le filigrane que vous souhaitez ajouter.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Filigrane &gt; Entrée) Stockage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel est stocké le filigrane que vous souhaitez ajouter.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Filigrane &gt; Limites) Hauteur]</p>
      </td>
   <td>Saisissez ou mappez la hauteur souhaitée du filigrane en pixels.</td> 
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Filigrane &gt; Limites) Largeur]</p>
      </td>
   <td> Saisissez ou mappez la largeur souhaitée du filigrane en pixels. </td> 
    </tr>  
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Filigrane &gt; Limites) À Gauche]</p>
      </td>
   <td> Saisissez ou mappez la distance en pixels entre le côté gauche de l’image et le filigrane.</td> 
    </tr>  
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Filigrane &gt; Limites) Haut]</p>
      </td>
   <td> Saisissez ou mappez la distance en pixels entre le haut de l’image et le filigrane.</td> 
    </tr>  
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Storage]</td>
      <td>
        <p>Sélectionnez le service de fichiers dans lequel vous souhaitez stocker le fichier en filigrane.</p><p>La sélection du stockage interne Fusion rend le fichier disponible pour les modules ultérieurs, mais ne rend pas le fichier disponible en dehors du scénario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) File location]</p>
      </td>
   <td> Saisissez ou mappez l’URL ou le chemin d’accès de l’emplacement de stockage du fichier en filigrane. Cela n’est nécessaire que si vous n’avez pas choisi le stockage interne Fusion pour le stockage de sortie.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Output) Type]</p>
      </td>
   <td>Sélectionnez le type de fichier vers lequel vous souhaitez convertir le fichier. </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL (Sortie) Largeur]</p>
      </td>
   <td> Largeur, en pixels, du fichier de sortie. Le module conserve les proportions d’origine. </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL (Output) Overwrite]</td>
      <td>
        <p>Indiquez si le fichier nouvellement modifié remplacera un fichier de sortie existant. Cela s’applique uniquement aux fichiers dans l’espace de stockage Adobe.</p>
      </td>
    </tbody>
</table>
