---
title: Services Adobe PDF
description: Services Adobe PDF
author: Becky
draft: Probably
feature: Workfront Fusion, Digital Content and Documents
exl-id: e6fbbc20-4315-4668-9e11-af7cfa82ae66
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '4125'
ht-degree: 92%

---

# [!DNL Adobe PDF Services]

Avec les [!DNL Adobe PDF Services] [!DNL Adobe Workfront Fusion], vous pouvez extraire des données d’un fichier PDF ou générer un nouveau fichier PDF à partir des données que vous fournissez. Vous pouvez également convertir divers types de fichiers en PDF ou des PDF en d’autres types de fichiers. Les services PDF vous permettent également de combiner, de compresser ou de lire les métadonnées d’un fichier PDF, ainsi que de contrôler la protection par mot de passe du fichier.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

Pour plus d’informations sur l’API utilisée pour les services PDF, voir [API de génération de document Adobe](https://www.adobe.io/apis/documentcloud/dcsdk/doc-generation.html).

## Remarques de sécurité lors de l’utilisation des [!DNL Adobe PDF Services]

Les [!DNL Adobe PDF Services] peuvent lire, convertir ou modifier vos fichiers, mais ni [!DNL Adobe] ni [!DNL Workfront Fusion] ne stocke vos fichiers ou données. Cela signifie que :

* Vous conservez le contrôle de vos fichiers, y compris de leur sécurité.
* Vous n’avez pas besoin d’avoir un compte de stockage ou de stockage dans le cloud [!UICONTROL Adobe] pour utiliser les PDF Services.

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

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Conditions préalables

Pour créer une connexion de serveur à serveur OAuth, vous devez ajouter l’API Adobe PDF Services à votre console Adobe Developers. Lors de l’ajout de l’API, sélectionnez l’option Serveur à serveur OAuth.

Pour obtenir des instructions, voir [Ajouter une API au projet à l’aide d’OAuth](https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/) dans la documentation Adobe Developer.

## Informations sur l’API Adobe PDF Services

Le connecteur Adobe PDF Services utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td>https://pdf-services-stage.adobe.io</td> 
  </tr>
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v2.1.4</td> 
  </tr>
 </tbody> 
 </table>

## Créer une connexion à [!DNL Adobe PDF Services]

Pour créer une connexion pour vos modules [!DNL Adobe PDF Services], procédez comme suit :

1. Dans un module [!DNL Adobe PDF Services], cliquez sur **[!UICONTROL Ajouter]** en regard de la zone Connexion.

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
            <p>Indiquez si vous souhaitez créer une connexion serveur à serveur ou une connexion JWT.</p>
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
          <td>Saisissez votre [!UICONTROL Client ID] [!DNL Adobe]. Vous pouvez le trouver dans la section [!UICONTROL Credentials details] de l’[!DNL Adobe Developer Console].<p>Pour obtenir des instructions sur la localisation des informations d’identification, voir <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" >Informations d’identification</a> dans la documentation Adobe Developer.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]</td>
          <td>Saisissez votre [!UICONTROL Client Secret] [!DNL Adobe]. Vous pouvez le trouver dans la section [!UICONTROL Credentials details] de la [!DNL Adobe Developer Console].<p>Pour obtenir des instructions sur la localisation des informations d’identification, consultez <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" >Informations d’identification</a> dans la documentation Adobe Developer.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Technical account ID] (JWT uniquement)</td>
          <td>Saisissez votre [!UICONTROL Technical account ID] [!DNL Adobe]. Vous pouvez le trouver dans la section [!UICONTROL Credentials details] de l’[!DNL Adobe Developer Console].<p>Pour obtenir des instructions sur la localisation des informations d’identification, consultez <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" >Informations d’identification</a> dans la documentation Adobe Developer.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Organization ID] (JWT uniquement)</td>
          <td>Saisissez votre [!UICONTROL Organization ID] [!DNL Adobe]. Vous pouvez le trouver dans la section [!UICONTROL Credentials details] de l’[!DNL Adobe Developer Console].<p>Pour obtenir des instructions sur la localisation des informations d’identification, consultez <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/#credentials" class="MCXref xref" >Informations d’identification</a> dans la documentation Adobe Developer.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Meta scopes] (JWT uniquement)</td>
          <td>
            Saisissez les métascopes nécessaires à la connexion.
          </td>
        </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Private key]</td>
        <td>
          <p>Si vous avez sélectionné une connexion JWT, saisissez la clé privée générée lors de la création de vos informations d’identification dans l’[!DNL Adobe Developer Console]. </p>
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
              <p>Cliquez sur <b>[!UICONTROL Save]</b> pour extraire le fichier et revenir à la configuration de la connexion.</p>
            </li>
          </ol>
        </td>
      </tr>
       </tbody>
    </table>
1. Cliquez sur **[!UICONTROL Continuer]** pour enregistrer la connexion et revenir au module.


## Modules et champs [!DNL Adobe PDF Services]

Lorsque vous configurez [!DNL PDF Services], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de cela, des champs supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [[!UICONTROL Combiner des fichiers PDF]](#combine-pdf-files)
* [[!UICONTROL Compresser des fichiers PDF]](#compress-pdf-files)
* [[!UICONTROL Convertir le document en fichier PDF]](#convert-document-to-pdf-file)
* [[!UICONTROL Convertir le HTML en fichier PDF]](#convert-html-to-pdf-file)
* [[!UICONTROL Convertir l’image en fichier PDF]](#convert-image-to-pdf-file)
* [[!UICONTROL Convertir le PDF en document]](#convert-pdf-to-document)
* [[!UICONTROL Convertir le PDF en image]](#convert-pdf-to-image)
* [[!UICONTROL Extraire le texte/tableau]](#extract-text--table)
* [[!UICONTROL Générer un document]](#generate-document)
* [[!UICONTROL Linéariser un fichier PDF]](#linearize-a-pdf-file)
* [Effectuer un appel API personnalisé.](#make-a-custom-api-call)
* [[!UICONTROL OCR pour le fichier PDF]](#ocr-for-pdf-file)
* [[!UICONTROL Manipulation de page]](#page-manipulation)
* [[!UICONTROL Balisage automatique de l’accessibilité des PDF]](#pdf-accessibility-auto-tag)
* [[!UICONTROL Propriétés du fichier PDF]](#pdf-file-properties)
* [[!UICONTROL Protéger le fichier PDF]](#protect-pdf-file)
* [[!UICONTROL Supprimer la protection d’un fichier PDF]](#remove-protection-of-a-pdf-file)
* [Partager un fichier PDF](#split-a-pdf-file)

### [!UICONTROL Combiner des fichiers PDF]

Ce module d’action prend plusieurs fichiers PDF et les combine en un seul fichier PDF. Par exemple, ce module pourrait combiner tous les documents d’un projet [!UICONTROL Workfront] en un seul PDF à la fin du projet.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Sélectionnez la connexion à utiliser pour ce module.</p> Pour savoir comment créer une connexion avec [!DNL Adobe PDF Services], voir <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Créer une connexion avec [!DNL Adobe PDF Services]</a> dans cet article. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Documents]</td> 
   <td> <p>Vous pouvez utiliser un module d’agrégation pour rassembler les documents à combiner dans un PDF, ou vous pouvez ajouter les documents manuellement. </p> <p>Il est recommandé d’utiliser un module [!UICONTROL Array Aggregator] pour agréger les sorties d’un module précédent. En utilisant un agrégateur, vous n’avez pas besoin de connaître les noms, les emplacements ou les numéros des fichiers à combiner. L’utilisation d’un agrégateur est donc beaucoup plus souple et évolutive que la saisie manuelle des documents à combiner.</p> <p>Pour utiliser le module de fichiers [!UICONTROL Combine PDF] avec un agrégateur, vous devez activer le mappage dans le champ [!UICONTROL Documents]. </p> <p>Dans cet exemple, le module [!UICONTROL Read Related Records] identifie les documents associés à un projet et le module [!UICONTROL Download Documents] télécharge chacun d’entre eux. Tous les PDF sont regroupés dans un tableau, qui est transmis au module de fichiers [!UICONTROL Combine PDF].</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/combine-example-350x104.png" style="width: 350;height: 104;"> </p> <p>Vous pouvez également saisir les documents manuellement.</p> <p>Pour chaque document à inclure dans le PDF combiné :</p> 
    <ol> 
     <li value="1"> <p>Cliquez sur [!UICONTROL Add a Document].</p> </li> 
     <li value="2"> <p>Dans le champ [!UICONTROL Source file], sélectionnez le module qui produit le document que vous souhaitez inclure, ou mappez le nom et les données du fichier source. </p> </li> 
     <li value="3"> <p>(Facultatif) Si vous souhaitez inclure uniquement certaines pages du fichier source, cliquez sur <strong>[!UICONTROL Add item]</strong> dans le champ [!UICONTROL Pages], saisissez la première et la dernière page de la plage de pages à inclure, puis cliquez sur <strong>[!UICONTROL Add]</strong>. Vous pouvez inclure plusieurs plages de pages dans un même document.</p> </li> 
     <li value="4"> <p>Cliquez sur <strong>[!UICONTROL Add]</strong>. </p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Compresser des fichiers PDF]

Ce module d’action prend un fichier PDF et le compresse. Cela peut être utile pour économiser de la bande passante ou de la mémoire.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Sélectionnez la connexion à utiliser pour ce module.</p> Pour savoir comment créer une connexion avec [!DNL Adobe PDF Services], voir <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Créer une connexion avec [!DNL Adobe PDF Services]</a> dans cet article. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> <p>Le fichier source doit être au format PDF. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Compression level]</td> 
   <td>Sélectionnez le niveau de compression que vous souhaitez utiliser.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Convertir un document en fichier PDF]

Cet outil permet de convertir un document en fichier PDF. Le fichier source doit être dans l’un des formats de document suivants :

* DOC
* XLS
* PPT
* TXT
* RTF

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Sélectionnez la connexion à utiliser pour ce module.</p> Pour savoir comment créer une connexion avec [!DNL Adobe PDF Services], voir <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Créer une connexion avec [!DNL Adobe PDF Services]</a> dans cet article. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> <p>Le fichier source doit être dans l’un des formats suivants :</p> 
    <ul> 
     <li> <p>DOC</p> </li> 
     <li> <p>XLS</p> </li> 
     <li> <p>PPT</p> </li> 
     <li> <p>TXT</p> </li> 
     <li> <p>RTF</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Language]</td> 
   <td> <p>Sélectionnez la langue par défaut du document source. Cela permet au module de sélectionner une police appropriée, si aucune police n’est incluse dans le fichier source.</p> <p>Sélectionnez l’une des langues suivantes :</p> 
    <ul> 
     <li> <p>en-US (par défaut) : anglais (États-Unis d’Amérique)</p> </li> 
     <li> <p>ca-ES : catalan (Espagne)</p> </li> 
     <li> <p>cs-CZ : tchèque (République tchèque)</p> </li> 
     <li> <p>da-DK : danois (Danemark)</p> </li> 
     <li> <p>de-DE : allemand (Allemagne)</p> </li> 
     <li> <p>en-AE : anglais (Émirats arabes unis)</p> </li> 
     <li> <p>en-GB : anglais (Royaume-Uni)</p> </li> 
     <li> <p>en-IL : anglais (Israël)</p> </li> 
     <li> <p>en-US : anglais (États-Unis d’Amérique)</p> </li> 
     <li> <p>es-ES : espagnol (Espagne)</p> </li> 
     <li> <p>es-MX : espagnol (Mexique)</p> </li> 
     <li> <p>eu-ES : basque (Espagne)</p> </li> 
     <li> <p>fi-FI : finnois (Finlande)</p> </li> 
     <li> <p>fr-CA : français (Canada)</p> </li> 
     <li> <p>fr-FR : français (France)</p> </li> 
     <li> <p>fr-MA : français (Maroc)</p> </li> 
     <li> <p>hr-HR : croate (Croatie)</p> </li> 
     <li> <p>hu-HU : hongrois (Hongrie)</p> </li> 
     <li> <p>it-IT : italien (Italie)</p> </li> 
     <li> <p>ja-JP : japonais (Japon)</p> </li> 
     <li> <p>kr-KR : coréen (Corée du Sud)</p> </li> 
     <li> <p>nb-NO : bokmål (Norvège)</p> </li> 
     <li> <p>nl-NL : néerlandais (Pays-Bas)</p> </li> 
     <li> <p>pl-PL : polonais (Pologne)</p> </li> 
     <li> <p>pt-BR : portugais (Brésil)</p> </li> 
     <li> <p>pt-PT : portugais (Portugal)</p> </li> 
     <li> <p>ro-RO : roumain (Roumanie)</p> </li> 
     <li> <p>ru-RU : russe (Russie)</p> </li> 
     <li> <p>sk-SK : slovaque (Slovaquie)</p> </li> 
     <li> <p>sl-SI : slovène (Slovénie)</p> </li> 
     <li> <p>sv-SE : suédois (Suède)</p> </li> 
     <li> <p>tr-TR : turc (Turquie)</p> </li> 
     <li> <p>uk-UA : ukrainien (Ukraine)</p> </li> 
     <li> <p>zh-CN : chinois (Chine continentale)</p> </li> 
     <li> <p>zh-TW : chinois (Taïwan)</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Convertir un fichier HTML en PDF]

Cet outil permet de convertir un fichier HTML en fichier PDF.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Sélectionnez la connexion à utiliser pour ce module.</p> Pour savoir comment créer une connexion avec [!DNL Adobe PDF Services], voir <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Créer une connexion avec [!DNL Adobe PDF Services]</a> dans cet article. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> <p>Important : le fichier source doit être au format HTML ou ZIP. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL JSON]</td> 
   <td> <p>Si votre HTML fait référence à des variables JavaScript, vous pouvez inclure ces variables ici. </p> <p>Pour chaque variable, cliquez sur <strong>[!UICONTROL Add item]</strong> et indiquez la clé et la valeur de la variable.</p> <p>Note :   
     <ul> 
      <li> <p>Lors de la création d’un PDF à partir d’un fichier ZIP, le collatéral source doit inclure un élément de script tel que : <code> &lt;script src='./json.js' type='text/javascript'&gt;&lt;/script&gt;</code>. </p> </li> 
      <li> <p>Lors de la création d’un PDF à partir d’une URL, le contenu de cet objet JSON est injecté dans la VM du navigateur avant le rendu de la page. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Include header and footer]</td> 
   <td> <p>Activez cette option pour créer des en-têtes et des pieds de page pour le document PDF.</p> 
    <ul> 
     <li> <p>L’en-tête comprend une date et le titre du document.</p> </li> 
     <li> <p>Le pied de page comprend le nom du fichier et un numéro de page.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Page width]</td> 
   <td>Saisissez la largeur du papier, en pouces. Le module utilise ces informations pour formater les pages du fichier PDF créé.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Page height]</td> 
   <td>Saisissez la hauteur du papier, en pouces. Le module utilise ces informations pour formater les pages du fichier PDF créé.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Convertir une image en fichier PDF]

Cet outil permet de convertir une image en fichier PDF.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Sélectionnez la connexion à utiliser pour ce module.</p> Pour savoir comment créer une connexion avec [!DNL Adobe PDF Services], voir <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Créer une connexion avec [!DNL Adobe PDF Services]</a> dans cet article. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom du fichier source et le fichier image.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Convertir le PDF en document]

Cet outil permet de convertir un fichier PDF en document. Vous pouvez sélectionner l’un des formats suivants pour le fichier de sortie.

* DOC
* DOCX
* PPTX
* XLSX
* RTF

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Sélectionnez la connexion à utiliser pour ce module.</p> Pour savoir comment créer une connexion avec [!DNL Adobe PDF Services], voir <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Créer une connexion avec [!DNL Adobe PDF Services]</a> dans cet article. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> <p>Le fichier source doit être au format PDF. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Files Format]</td> 
   <td> <p>Sélectionnez le format de sortie des fichiers :</p> 
    <ul> 
     <li> <p>DOC</p> </li> 
     <li> <p>DOCX</p> </li> 
     <li> <p>PPTX</p> </li> 
     <li> <p>XLSX</p> </li> 
     <li> <p>RTF</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Language]</td> 
   <td> <p>Sélectionnez la langue par défaut du document source. Cela permet au module de sélectionner une police appropriée, si aucune police n’est incluse dans le fichier source.</p> <p>Sélectionnez l’une des langues suivantes :</p> 
    <ul> 
     <li> <p>en-US (par défaut) : anglais (États-Unis d’Amérique)</p> </li> 
     <li> <p>ca-ES : catalan (Espagne)</p> </li> 
     <li> <p>cs-CZ : tchèque (République tchèque)</p> </li> 
     <li> <p>da-DK : danois (Danemark)</p> </li> 
     <li> <p>de-DE : allemand (Allemagne)</p> </li> 
     <li> <p>en-AE : anglais (Émirats arabes unis)</p> </li> 
     <li> <p>en-GB : anglais (Royaume-Uni)</p> </li> 
     <li> <p>en-IL : anglais (Israël)</p> </li> 
     <li> <p>en-US : anglais (États-Unis d’Amérique)</p> </li> 
     <li> <p>es-ES : espagnol (Espagne)</p> </li> 
     <li> <p>es-MX : espagnol (Mexique)</p> </li> 
     <li> <p>eu-ES : basque (Espagne)</p> </li> 
     <li> <p>fi-FI : finnois (Finlande)</p> </li> 
     <li> <p>fr-CA : français (Canada)</p> </li> 
     <li> <p>fr-FR : français (France)</p> </li> 
     <li> <p>fr-MA : français (Maroc)</p> </li> 
     <li> <p>hr-HR : croate (Croatie)</p> </li> 
     <li> <p>hu-HU : hongrois (Hongrie)</p> </li> 
     <li> <p>it-IT : italien (Italie)</p> </li> 
     <li> <p>ja-JP : japonais (Japon)</p> </li> 
     <li> <p>kr-KR : coréen (Corée du Sud)</p> </li> 
     <li> <p>nb-NO : bokmål (Norvège)</p> </li> 
     <li> <p>nl-NL : néerlandais (Pays-Bas)</p> </li> 
     <li> <p>pl-PL : polonais (Pologne)</p> </li> 
     <li> <p>pt-BR : portugais (Brésil)</p> </li> 
     <li> <p>pt-PT : portugais (Portugal)</p> </li> 
     <li> <p>ro-RO : roumain (Roumanie)</p> </li> 
     <li> <p>ru-RU : russe (Russie)</p> </li> 
     <li> <p>sk-SK : slovaque (Slovaquie)</p> </li> 
     <li> <p>sl-SI : slovène (Slovénie)</p> </li> 
     <li> <p>sv-SE : suédois (Suède)</p> </li> 
     <li> <p>tr-TR : turc (Turquie)</p> </li> 
     <li> <p>uk-UA : ukrainien (Ukraine)</p> </li> 
     <li> <p>zh-CN : chinois (Chine continentale)</p> </li> 
     <li> <p>zh-TW : chinois (Taïwan)</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Convertir le PDF en image]

Cet outil convertit un PDF en image au format PNG ou JPEG, qui est ensuite générée sous forme de liste ou regroupée dans un fichier ZIP.

Si la sortie est au format ZIP, le PDF est converti en une image par page et chaque image se termine par le numéro de page. Les fichiers images sont ensuite regroupés dans un fichier ZIP.

Par exemple, un fichier appelé « TestFile » comportant 8 pages produira 8 images, nommées « TestFile_1 » à « TestFile_8 ». La sortie du module est un fichier ZIP contenant les 8 images.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Sélectionnez la connexion à utiliser pour ce module.</p> Pour savoir comment créer une connexion avec [!DNL Adobe PDF Services], voir <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Créer une connexion avec [!DNL Adobe PDF Services]</a> dans cet article. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> <p>Le fichier source doit être au format PDF. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Files Format]</td> 
   <td> <p>Sélectionnez le format de sortie des fichiers :</p> 
    <ul> 
     <li>PNG</li> 
     <li>JPEG</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type de sortie]</td> 
   <td> <p>Choisissez si vous souhaitez que les fichiers soient générés sous la forme d’une liste de fichiers ou d’un fichier ZIP.</td> 
  </tr> 
  <tr> 
 </tbody> 
</table>

### [!UICONTROL Extraire un texte/tableau]

Ce module d’action vous permet d’extraire des données d’un fichier PDF. Le module produit des éléments de texte individuels, tels qu’un paragraphe ou le texte d’une seule cellule d’un tableau.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Sélectionnez la connexion à utiliser pour ce module.</p> Pour savoir comment créer une connexion avec [!DNL Adobe PDF Services], voir <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Créer une connexion avec [!DNL Adobe PDF Services]</a> dans cet article. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Elements that should be extracted as JSON]</td> 
   <td> 
    <ul> 
     <li> <p>[!UICONTROL Text]</p> </li> 
     <li> <p>[!UICONTROL Tables]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Extract Bounding boxes?]</td> 
   <td>Activez cette option pour extraire des données sur le cadre de sélection du texte.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Include styling information for output?]</td> 
   <td>Activez cette option pour ajouter des informations de style au fichier JSON de sortie.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Générer un document]

Le module [!UICONTROL Générer un document] est un moyen puissant de créer un PDF contenant les données que vous sélectionnez. Vous pouvez le mettre en forme à l’aide d’un modèle [!DNL Microsoft Word] ou en fournissant des données au format JSON.

Pour plus d’informations sur la fonctionnalité [!UICONTROL [!DNL Adobe PDF Services] Générer un document], consultez [Vue d’ensemble de la génération de document](https://www.adobe.io/apis/documentcloud/dcsdk/docs.html) dans la documentation [!DNL Adobe Document Services].

* [Utiliser le module [!UICONTROL Générer un document] avec un modèle  [!DNL Microsoft Word] ](#use-the-generate-document-module-with-a-microsoft-word-template)
* [Utiliser le module [!UICONTROL Générer un document] avec JSON](#use-the-generate-document-module-with-json)

#### Utiliser le module [!UICONTROL Générer un document] avec un modèle [!DNL Microsoft Word]


>[!NOTE]
>
>Pour en savoir plus sur les modèles Microsoft Word, consultez [Modules de modèles Microsoft Word](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-word-templates-modules.md).
>
>Vous n’avez pas besoin d’utiliser les modules de modèle Microsoft Word pour utiliser un modèle Microsoft Word avec le module de génération de document des services PDF.


Pour utiliser le module [!UICONTROL Générer un document] avec un modèle [!UICONTROL Microsoft Word], vous devez d’abord créer le modèle. Pour obtenir des instructions, recherchez « Créer un modèle » dans la documentation [!DNL Microsoft Office].

Renseignez les champs du module [!UICONTROL Générer un document] comme suit :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Sélectionnez la connexion à utiliser pour ce module.</p> Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe PDF Services], consultez <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Créer une connexion à [!DNL Adobe PDF Services]</a> dans cet article. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source File]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> <p>Ce fichier source est le modèle de [!DNL Microsoft Word] utilisé par le module pour générer le nouveau PDF.</p> <p>Nous vous recommandons de créer un projet dans [!DNL Workfront] pour les modèles [!DNL Microsoft Word] que vous utilisez dans [!DNL Workfront Fusion]. Vous pouvez ensuite utiliser le module [!DNL Workfront] &gt; [!UICONTROL Download document] pour extraire le modèle approprié dans votre scénario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format]</td> 
   <td> <p>Sélectionnez le format du document généré.</p> 
    <ul> 
     <li> <p>PDF</p> </li> 
     <li> <p>DOCX</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data for merge]</td> 
   <td> <p>Pour chaque balise de valeur de votre modèle que vous souhaitez remplacer par du texte, renseignez les éléments suivants :</p> 
    <ul> 
     <li> <p>[!UICONTROL Key]</p> <p>Saissez une clé. Dans le modèle, la clé correspond au texte affiché dans la balise de valeur. Par exemple, si vous souhaitez placer du texte dans la balise de valeur <code>&#123;&#123;name&#125;&#125;</code>, saisissez <code>name </code> dans le champ de clé.</p> </li> 
     <li> <p>Type de valeur</p> <p>Indiquez si les données du champ de valeur sont une valeur, un objet ou un tableau d’objets.</p> </li> 
     <li> <p>[!UICONTROL Value]</p> <p>Saisissez ou mappez le texte que vous souhaitez afficher dans le document généré à la place de la balise de valeur.</p> </li> 
    </ul> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/generate-with-template-350x241.png" style="width: 350;height: 241;"> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Utiliser le module [!UICONTROL Générer un document] avec JSON

Pour utiliser le module [!UICONTROL Générer un document] avec JSON, renseignez les champs comme suit :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Sélectionnez la connexion à utiliser pour ce module.</p> Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe PDF Services], consultez <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Créer une connexion à [!DNL Adobe PDF Services]</a> dans cet article. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source File]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Format]</td> 
   <td> <p>Sélectionnez le format du document généré.</p> 
    <ul> 
     <li> <p>PDF</p> </li> 
     <li> <p>DOCX</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data for merge]</td> 
   <td> <p>Pour utiliser JSON dans ce module, vous devez activer le mappage sur ce champ.</p> <p>Saisissez ou mappez le JSON à partir duquel le document est généré. </p> <p>Vous pouvez saisir le JSON directement dans ce champ, ou mapper la sortie JSON d’un module JSON.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Linéariser un fichier PDF]

Cet outil linéarise un document PDF pour créer un document PDF optimisé pour le web. Un document PDF linéarisé peut être consulté page par page sans avoir à télécharger l’intégralité du document.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Sélectionnez la connexion à utiliser pour ce module.</p> Pour savoir comment créer une connexion avec [!DNL Adobe PDF Services], voir <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Créer une connexion avec [!DNL Adobe PDF Services]</a> dans cet article. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Effectuer un appel API personnalisé

Ce module d’action envoie une requête HTTP personnalisée à l’API Services PDF.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Sélectionnez la connexion à utiliser pour ce module.</p> Pour plus d’informations sur l’établissement d’une connexion à [!DNL Adobe PDF Services], voir <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Créer la connexion à [!DNL Adobe PDF Services]</a> dans cet article. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> Saisissez un chemin relatif ou une URL. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion ajoute automatiquement les en-têtes d’autorisation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Ajoutez la requête pour l’appel API sous la forme d’un objet JSON standard.</p> <p>Par exemple : <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>Pour chaque champ à ajouter à l’appel API, cliquez sur <b>Ajouter un élément</b> et saisissez la clé et la valeur facultative du champ.</p> <p>Note :  <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre JSON, placez les guillemets à l’extérieur de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>


### [!UICONTROL OCR pour les fichiers PDF]

Cet outil effectue une reconnaissance optique de caractères (OCR) sur un fichier et produit un PDF.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Sélectionnez la connexion à utiliser pour ce module.</p> Pour savoir comment créer une connexion avec [!DNL Adobe PDF Services], voir <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Créer une connexion avec [!DNL Adobe PDF Services]</a> dans cet article. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Language]</td> 
   <td>Sélectionnez la langue de ce document.<p>Pour connaître les options linguistiques, voir <a href="#convert-document-to-pdf-file" class="MCXref xref" >Convertir le document en fichier PDF</a> dans cet article. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL OCR type]</td> 
   <td> 
    <ul> 
     <li> <p>Le type [!UICONTROL Modified original image] garantit que le texte est consultable et sélectionnable, mais modifie l’image originale au cours du processus de nettoyage (par exemple, la désaligne) avant de placer un calque de texte invisible par-dessus. Ce type supprime les artefacts indésirables et peut, dans certains cas, rendre le document plus lisible. </p> </li> 
     <li> <p>Le type [!UICONTROL Unchanged original image] superpose également un calque de texte consultable à l’image originale, mais dans ce cas, l’image originale est inchangée. Ce type permet d’obtenir une fidélité maximale à l’image originale.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Manipulation des pages]

Ce module vous permet de faire pivoter ou de supprimer sélectivement des pages dans un document PDF. Par exemple, vous pouvez passer de l’affichage en mode portrait à l’affichage en mode paysage ou supprimer certaines pages du document PDF.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Sélectionnez la connexion à utiliser pour ce module.</p> Pour savoir comment créer une connexion avec [!DNL Adobe PDF Services], voir <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Créer une connexion avec [!DNL Adobe PDF Services]</a> dans cet article. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td> <p>Sélectionnez l’action que vous souhaitez effectuer sur le fichier.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Delete]</b> </p> <p>Sélectionnez cette option pour supprimer des pages du document.</p><p>Pour chaque plage de pages à supprimer, cliquez sur <strong>[!UICONTROL Add]</strong> et saisissez la première et la dernière page de la plage de pages. </p> <p>Note :   
     <ul> 
      <li> <p>Vous pouvez utiliser des nombres négatifs pour compter à partir de la fin du document. La dernière page d’un document est -1, l’avant-dernière page est -2, et ainsi de suite.</p> </li> 
      <li> <p>Pour supprimer une seule page, définissez le même numéro de page pour le début et la fin de la plage.</p></ul> </li> 
     <li> <p><b>[!UICONTROL Rotate]</b> </p> <p>Sélectionnez cette option pour faire pivoter les pages, puis entrez l’angle, en degrés dans le sens des aiguilles d’une montre, selon lequel vous souhaitez faire pivoter les pages du document par rapport à leur orientation initiale.</p> <p>Pour passer du mode portrait au mode paysage ou inversement, faites pivoter la page de 90 ou 270 degrés.</p> <p>Si une page est à l’envers, faites-la pivoter de 180 degrés.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pages]</td> 
   <td> <p>Pour chaque plage de pages à supprimer, cliquez sur <strong>[!UICONTROL Add]</strong> et saisissez la première et la dernière page de la plage de pages. </p> <p>Note :   
     <ul> 
      <li> <p>Vous pouvez utiliser des nombres négatifs pour compter à partir de la fin du document. La dernière page d’un document est -1, l’avant-dernière page est -2, et ainsi de suite.</p> </li> 
      <li> <p>Pour supprimer une seule page, définissez le même numéro de page pour le début et la fin de la plage.</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que vous souhaitez que le module utilise lors de chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Balises automatiques pour l’accessibilité des PDF]

Ce module d’action crée un PDF qui est balisé pour les cas d’utilisation de l’accessibilité. Il crée également un rapport Microsoft Excel facultatif qui répertorie les problèmes et propose des solutions.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Sélectionnez la connexion à utiliser pour ce module.</p> Pour savoir comment créer une connexion avec [!DNL Adobe PDF Services], voir <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Créer une connexion avec [!DNL Adobe PDF Services]</a> dans cet article. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Shift Headings]</td> 
   <td> <p>Activez cette option pour décaler les titres du document.</p> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Generate Report]</td> 
   <td> <p>Activez cette option pour générer un rapport qui répertorie les problèmes d’accessibilité dans le PDF ainsi que leur emplacement, et qui donne des suggestions sur la manière de résoudre ces problèmes.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Propriétés d’un fichier PDF]

Cet outil permet d’extraire des informations de base sur le document, telles que :

* Nombre de pages
* La version PDF
* Si le fichier est chiffré
* Si le fichier est linéarisé
* Si le fichier contient des fichiers intégrés

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Sélectionnez la connexion à utiliser pour ce module.</p> Pour savoir comment créer une connexion avec [!DNL Adobe PDF Services], voir <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Créer une connexion avec [!DNL Adobe PDF Services]</a> dans cet article. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Protection d’un fichier PDF]

Cet outil sécurise un document PDF à l’aide d’un mot de passe utilisateur ou propriétaire. Il définit également des restrictions sur certaines fonctions telles que l’impression, la modification et la copie dans le document PDF. Vous sélectionnez le type de contenu à chifrer et l’algorithme de chiffrement.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Sélectionnez la connexion à utiliser pour ce module.</p> Pour savoir comment créer une connexion avec [!DNL Adobe PDF Services], voir <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Créer une connexion avec [!DNL Adobe PDF Services]</a> dans cet article. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> <p>Le fichier source doit être au format PDF. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Password Protection Type]</td> 
   <td> <p>Activez cette option pour utiliser des mots de passe afin de chiffrer le document PDF d’entrée. Si vous activez cette option, vous devez spécifier et saisir une valeur pour l’un des éléments suivants, ou les deux : </p> 
    <ul> 
     <li> <p>[!UICONTROL User Password]</p> </li> 
     <li> <p>[!UICONTROL Owner Password] </p> </li> 
    </ul> <p>Chaque mot de passe peut comporter jusqu’à 128 caractères.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Encryption Algorithm]</td> 
   <td> <p>Sélectionnez l’algorithme de chiffrement. </p> 
    <ul> 
     <li> <p>[!UICONTROL AES-128 encryption]</p> <p>Le mot de passe ne prend en charge que les caractères LATIN-I. </p> </li> 
     <li> <p>[!UICONTROL AES-256 encryption]</p> <p>Le mot de passe prend en charge le jeu de caractères Unicode.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content to Encrypt]</td> 
   <td> <p>Sélectionnez le type de contenu à chiffrer.</p> 
    <ul> 
     <li> <p>[!UICONTROL All content]</p> </li> 
     <li> <p>[!UICONTROL All content except metadata]</p> </li> 
     <li> <p>[!UICONTROL Only embedded data] </p> </li> 
    </ul> <p>La sélection de l’option « [!UICONTROL Only embedded data] » rend inefficaces toutes les autorisations d’accès fournies.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Permissions]</td> 
   <td> <p>Sélectionnez les autorisations que vous souhaitez inclure pour permettre l’impression, la modification ou la copie de contenu.</p> <p>Les paramètres d'autorisations ne sont utilisés que si le mot de passe du propriétaire [!UICONTROL Owner Password] est défini dans le champ [!UICONTROL Password Protection Type].</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Supprimer la protection d’un fichier PDF]

Cet outil supprime la sécurité (protection par mot de passe) d’un document PDF.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Sélectionnez la connexion à utiliser pour ce module.</p> Pour savoir comment créer une connexion avec [!DNL Adobe PDF Services], voir <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Créer une connexion avec [!DNL Adobe PDF Services]</a> dans cet article. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> <p>Le fichier source doit être au format PDF.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Password]</td> 
   <td>Saisissez le mot de passe qui protège actuellement le fichier.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Partager un fichier PDF]

Ce module d’action permet de partager un document PDF en plusieurs documents plus petits. Vous indiquez si vous souhaitez le partager en fonction du nombre de fichiers, de pages par fichier ou de plages de pages.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Sélectionnez la connexion à utiliser pour ce module.</p> Pour savoir comment créer une connexion avec [!DNL Adobe PDF Services], voir <a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >Créer une connexion avec [!DNL Adobe PDF Services]</a> dans cet article. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> <p>Le fichier source doit être au format PDF.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split option]</td> 
   <td>Sélectionnez la manière dont vous souhaitez partager le fichier. 
   <ul>
   <li><p><b>Plages de pages</b></p><p>Pour chaque plage de pages que vous souhaitez partager en un document distinct, cliquez sur <b>Ajouter</b> et saisissez la page sur laquelle vous souhaitez commencer et la page sur laquelle vous souhaitez terminer.</p></li>
   <li><p><b>Nombre de pages</b></p><p>Saisissez le nombre de pages que vous souhaitez inclure dans les nouveaux documents.</p></li>
   <li><p><b>Compte de fichier</b></p><p>Saisissez le nombre de fichiers de taille égale en lesquels vous souhaitez partager le document.</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

