---
title: Modules audio et vidéo Adobe Firefly
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent l’audio et la vidéo Adobe Firefly, ainsi que les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
source-git-commit: f54338aa35b8453ac991c9e16974f2b61fd30168
workflow-type: tm+mt
source-wordcount: '1618'
ht-degree: 15%

---

# Modules audio et vidéo Adobe Firefly

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent l’audio et la vidéo Adobe Firefly, ainsi que les connecter à plusieurs applications et services tiers.

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

Avant de pouvoir utiliser le connecteur audio et vidéo Adobe Firefly, vous devez vous assurer que les conditions préalables suivantes sont remplies :

* Vous devez disposer d’un compte audio et vidéo Adobe Firefly actif.

## Création d’une connexion à Adobe Firefly Audio and Video

Pour créer une connexion pour vos modules audio et vidéo Adobe Firefly :

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


## Modules audio et vidéo Adobe Firefly et leurs champs

Lorsque vous configurez les modules audio et vidéo Adobe Firefly, Workfront Fusion affiche les champs répertoriés ci-dessous. En plus de ces éléments, des champs audio et vidéo Adobe Firefly supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, consultez [Mappage d’informations d’un module à l’autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Bouton (bascule) de mappage](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Actions

* [Décrire le modèle](#describe-template)
* [Dub audio ou vidéo](#dub-audio-or-video)
* [Générer une vidéo d’avatar à partir de texte ou d’audio](#generate-avatar-video-from-text-or-audio)
* [Générer un discours à partir du texte](#generate-speech-from-text)
* [Recadrer la vidéo](#reframe-video)
* [Modèle de rendu](#render-template)
* [Transcrire le média](#transcribe-media)

#### Décrire le modèle

Ce module d’action analyse un fichier MOGRT (modèle vidéo) et renvoie un manifeste de contrôles modifiables, de polices, d’images, d’audio, de vidéo et d’autres valeurs prises en charge.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Firefly, voir <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Création d’une connexion à Adobe Firefly</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Saisissez ou mappez l’URL prédéfinie qui pointe vers le fichier du modèle d’entrée.</td> 
  </tr>
 </tbody> 
</table>

#### Dub audio ou vidéo

Ce module d’action génère des doublons audio ou vidéo. Elle peut également inclure la synchronisation des lèvres dans la vidéo générée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Firefly, voir <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Création d’une connexion à Adobe Firefly</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type de doublon</td> 
   <td>Choisissez si vous souhaitez générer un dub audio ou vidéo.</td> 
  </tr>
  <tr> 
   <td role="rowheader">URL prédéfinie</td> 
   <td>Saisissez ou mappez l’URL prédéfinie que le module utilisera pour la saisie.<p>Les domaines suivants pour le stockage multimédia sont acceptés par Firefly Audio and Video</p>
   <ul>
   <li>adobe.io</li>
   <li>frame.io</li>
   <li>amazonaws.com</li>
   <li>windows.net</li>
   <li>dropboxusercontent.com</li>
   <li>drive.google.com</li>
   <li>cloudfront.net</li>
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Type de média</td> 
   <td>Sélectionnez le type de média du fichier d’entrée</td> 
  </tr>
  <tr> 
   <td role="rowheader">Synchronisation labiale</td> 
   <td>Choisissez de générer une synchronisation de lèvres composites de haute qualité pour la sortie vidéo.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Codes de paramètres régionaux cibles</td> 
   <td>Pour chaque code de paramètre régional à ajouter, cliquez sur <b>Ajouter un élément</b> et sélectionnez le code de paramètre régional.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Transcriptions</td> 
   <td>Pour chaque transcription que vous souhaitez ajouter, cliquez sur <b>Ajouter un élément</b> et saisissez ou mappez les URL prédéfinies pour la transcription.</td> 
  </tr>
 </tbody> 
</table>

#### Générer une vidéo d’avatar à partir de texte ou d’audio

Ce module d’action génère une vidéo d’avatar à partir d’une transcription ou d’un fichier audio que vous fournissez.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Firefly, voir <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Création d’une connexion à Adobe Firefly</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Saisissez ou mappez l’URL prédéfinie que le module utilisera pour la saisie.   </td> 
  </tr>
  <tr> 
  <tr> 
   <td role="rowheader">Code du paramètre régional</td> 
   <td>Sélectionnez le code de paramètre régional qui représente la langue que vous souhaitez utiliser dans le résultat.</td> 
  </tr>
   <td role="rowheader">Type de média (Source)</td> 
   <td>Sélectionnez le type de média du fichier d’entrée</td> 
  </tr>
  <tr> 
   <td role="rowheader">Avatar</td> 
   <td>Sélectionnez l’avatar que vous souhaitez utiliser pour la vidéo générée.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Type de média</td> 
   <td>Sélectionnez le type de média de sortie pour la vidéo générée.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Largeur</td> 
   <td>Saisissez ou mappez la largeur de la vidéo générée.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Hauteur</td> 
   <td>Saisissez ou mappez la hauteur de la vidéo générée.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Contexte</td> 
   <td>Sélectionnez le type d’arrière-plan à utiliser pour la vidéo générée :
   <ul>
   <li><b>Vidéo</b> : saisissez ou mappez l’URL de la vidéo d’arrière-plan.</li> 
   <li><b>Image</b> : saisissez ou mappez l’URL de l’image d’arrière-plan.</li>
   <li><b>Couleur</b> : saisissez ou mappez la valeur hexadécimale de la couleur que vous souhaitez utiliser pour l’arrière-plan de la vidéo.</li> 
   </ul>
   </td>
  </tr>
 </tbody> 
</table>

#### Générer un discours à partir du texte

Ce module d’action génère la parole à partir d’une transcription. Vous pouvez fournir une transcription en texte brut ou une URL présignée. La réponse inclut un identifiant de tâche et une URL de statut pour le suivi de la tâche.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Firefly, voir <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Création d’une connexion à Adobe Firefly</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Script</td> 
   <td>Sélectionnez le type de script que vous souhaitez fournir.
   <ul>
   <li><b>Texte</b> : saisissez le texte source ou mappez-le au champ de texte.</li>
   <li><b>Fichier texte</b> : saisissez ou mappez l’URL du fichier texte dans le champ URL.</li>
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Code du paramètre régional</td> 
   <td>Sélectionnez le code de paramètre régional qui représente la langue que vous souhaitez utiliser dans le résultat.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Type de média</td> 
   <td>Cela devrait être <code>text/plain</code>.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Voix</td> 
   <td>Sélectionnez la voix que vous souhaitez utiliser. Les voix disponibles sont issues du catalogue des voix d’Adobe Firefly.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Sortie</td> 
   <td>Cela devrait être <code>audio/wav</code>.</td> 
  </tr>
 </tbody> 
</table>

#### Recadrer la vidéo

Ce module recadre les médias que vous fournissez. Le média est fourni via une URL présignée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Firefly, voir <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Création d’une connexion à Adobe Firefly</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL prédéfinie</td> 
   <td>Saisissez ou mappez l’URL prédéfinie que le module utilisera pour la saisie.<p>Les domaines suivants pour le stockage multimédia sont acceptés par Firefly Audio and Video</p>
   <ul>
   <li>adobe.io</li>
   <li>frame.io</li>
   <li>amazonaws.com</li>
   <li>windows.net</li>
   <li>dropboxusercontent.com</li>
   <li>drive.google.com</li>
   <li>cloudfront.net</li>
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Détection de modification de scène</td> 
   <td>Choisissez s'il faut appliquer la détection d'édition de scène avant de recadrer. </td> 
  </tr>
  <tr> 
   <td role="rowheader">Point focal</td> 
   <td>Pour chaque point focal à ajouter, cliquez sur <b>Ajouter un élément</b> et saisissez ou l’identifiant de mot-clé du point focal.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Chevauchements</td> 
   <td>Pour chaque recouvrement à ajouter, cliquez sur <b>Ajouter un élément</b> et saisissez les informations relatives au recouvrement.
   <ul>
   <li><b></b> : saisissez ou mappez l’URL qui pointe vers le média source.</li> 
   <li><b>Heure de début</b> : saisissez l’heure de début ou mappez-la.</li>
   <li><b>Durée</b> : saisissez ou mappez la durée du recouvrement.</li> 
   <li><b>Largeur</b> : saisissez ou mappez la largeur de la superposition mise à l’échelle.</li> 
   <li><b>Hauteur</b> : saisissez ou mappez la hauteur de la superposition mise à l’échelle.</li> 
   <li><b>Point d’ancrage</b> : sélectionnez le point d’ancrage du recouvrement.</li> 
   <li><b>Décalage X</b> : saisissez ou mappez le décalage horizontal du recouvrement.</li> 
   <li><b>Décalage Y</b> : saisissez ou mappez le décalage vertical pour le recouvrement.</li> 
   <li><b>Répéter</b> : saisissez la <code>loop</code> pour qu’un GIF soit mis en boucle.</li> 
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Format du média</td> 
   <td>Sélectionnez le format de la vidéo recadrée.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Format Sidecar</td> 
   <td>Sélectionnez le format des métadonnées supplémentaires.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Rendus</td> 
   <td>Pour ajouter des rendus supplémentaires, cliquez sur <b>Ajouter un élément</b> et saisissez les informations de rendu.<!--add additional info--></td> 
  </tr>
 </tbody> 
</table>

#### Modèle de rendu

Ce module effectue le rendu d’une ou plusieurs variations vidéo en appliquant des remplacements et des paramètres d’exportation prédéfinis.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Firefly, voir <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Création d’une connexion à Adobe Firefly</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL du fichier de modèle d’entrée</td> 
   <td>Saisissez ou mappez l’URL prédéfinie qui représente le modèle que vous souhaitez rendre.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Polices</td> 
   <td>Pour chaque police que vous souhaitez ajouter, cliquez sur <b>Ajouter un élément</b> et saisissez le nom postscript de la police et l’URL du fichier de police.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Lorsqu’une police est manquante</td> 
   <td>Indiquez si vous souhaitez faire échouer le rendu ou utiliser la police par défaut si une police est manquante.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Ressources multimédias</td> 
   <td>Pour chaque ressource multimédia à ajouter, cliquez sur <b>Ajouter un élément</b> et saisissez ou mappez l’URL prédéfinie qui représente la ressource.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Exporter les paramètres prédéfinis</td> 
   <td>Pour chaque paramètre d’exportation prédéfini que vous souhaitez ajouter, cliquez sur <b>Ajouter un élément</b> sélectionnez le paramètre vidéo prédéfini, puis saisissez ou mappez l’URL prédéfinie qui représente le paramètre prédéfini.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Variations</td> 
   <td>Pour chaque variation à ajouter, cliquez sur <b>Ajouter un élément</b> et saisissez les détails de la variation. Vous devez saisir des détails pour au moins une variation.<!--add data here--></td> 
  </tr>
  <tr> 
   <td role="rowheader">Définitions de sortie</td> 
   <td>Définissez des sorties en cliquant sur <b>Ajouter un élément</b> et en sélectionnant les variations et paramètres prédéfinis ajoutés que vous souhaitez utiliser, puis en ajoutant un nom de fichier. Les variations et les paramètres prédéfinis sont indexés sur 0 (le premier élément de la liste des variations est 0, le suivant est 1, etc.).</td> 
  </tr>
 </tbody> 
</table>

#### Transcrire le média

Ce module transcrit l&#39;audio ou la vidéo.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Firefly, voir <a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >Création d’une connexion à Adobe Firefly</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type de transcription</td> 
   <td>Choisissez si vous souhaitez transcrire des données audio ou vidéo.   </td> 
  </tr>
  <tr> 
   <td role="rowheader">URL prédéfinie</td> 
   <td>Saisissez ou mappez l’URL prédéfinie que le module utilisera pour la saisie.   </td> 
  </tr>
  <tr> 
  </tr>
   <td role="rowheader">Type de média </td> 
   <td>Sélectionnez le type de média du fichier d’entrée</td> 
  </tr>
  <tr> 
   <td role="rowheader">Codes de paramètres régionaux cibles</td> 
   <td>Pour chaque code de paramètre régional à ajouter, cliquez sur <b>Ajouter un élément</b> et sélectionnez le code de paramètre régional qui représente la langue à utiliser dans le résultat.</td> 
  <tr> 
   <td role="rowheader">Format de la légende</td> 
   <td>Saisissez <code>SRT</code> pour inclure des sous-titres ou laissez le champ vide si vous ne souhaitez pas de sous-titres.</td> 
  </tr>
 </tbody> 
</table>



