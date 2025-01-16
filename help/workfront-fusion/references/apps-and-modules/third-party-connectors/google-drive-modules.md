---
title: Modules Google Drive
description: Les modules  [!DNL Adobe Workfront Fusion Google Drive]  vous permettent de surveiller, de rechercher, de créer, de mettre à jour, de supprimer et de gérer vos fichiers, dossiers ou lecteurs partagés dans votre  [!DNL Google Drive].
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 788f4e1b-d774-45ad-a8be-b16922c1d5dc
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '2489'
ht-degree: 81%

---

# Modules [!DNL Google Drive]

Les modules [!DNL Adobe Workfront Fusion] [!DNL Google Drive] vous permettent de surveiller, de rechercher, de créer, de mettre à jour, de supprimer et de gérer vos fichiers, dossiers ou lecteurs partagés dans votre [!DNL Google Drive].

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez connecter votre compte [!DNL Google Drive] à plusieurs applications et services tiers.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <p>Ancienne exigence de licence : [!UICONTROL [!DNL Workfront Fusion] pour l’automatisation et l’intégration du travail] </p>
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

## Informations sur l’API Google Drive

Le connecteur du lecteur Google utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td> https://www.googleapis.com/drive/v3</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Version de l’API</td> 
   <td> v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v4.1.22</td> 
  </tr>
 </tbody> 
 </table>



## Connecter [!DNL Google Drive] à [!DNL Workfront Fusion]

Si vous êtes [!DNL @gmail.com] ou [!DNL @googlemail.com] utilisateur, vous devez créer un client OAuth sur [le [!DNL Google Cloud Platform]](https://console.developers.google.com/projectselector2/apis/dashboard?supportedpurview=project) afin d’obtenir des [!UICONTROL Client ID] et des [!UICONTROL Client Secret].

Pour obtenir des instructions détaillées sur la création du client OAuth (et l’obtention de [!UICONTROL Client ID] et de [!UICONTROL Client Secret]), voir [Connexion [!DNL Adobe Workfront Fusion] à [!DNL Google Services] à l’aide d’un client OAuth personnalisé](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

Pour savoir comment connecter votre compte [!DNL Google Drive] à [!UICONTROL Workfront Fusion], voir [Créer une connexion à [!UICONTROL Adobe Workfront Fusion] - Instructions de base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

## Modules [!DNL Google Drive] et leurs champs

Lorsque vous configurez les modules [!DNL Google Drive], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Google Drive] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)



* [Déclencheurs](#triggers)
* [Actions](#actions)

### Déclencheurs

* [[!UICONTROL Watch Files In Folder]](#watch-files-in-folder)
* [[!UICONTROL Watch All Files]](#watch-all-files)
* [[!UICONTROL Watch shared files]](#watch-shared-files)
* [[!UICONTROL Watch Comments]](#watch-comments)

#### [!UICONTROL Watch Files In Folder]

Récupère les détails du fichier lorsqu’un fichier est ajouté ou modifié dans le dossier spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection] </td>
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Drive] à [!DNL Workfront Fusion], voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Select the folder to be watched]</td>
    <td >Sélectionnez le dossier sur votre lecteur dans lequel vous souhaitez surveiller les fichiers.</td>
  </tr> 
  <tr> 
    <td>[!UICONTROL What files to watch]</td>
   <td> <p>Sélectionnez le type de fichiers que vous souhaitez surveiller.</p> 
    <ul> 
     <li>[!UICONTROL All]</li> 
     <li>[!DNL Google Documents]</li> 
     <li>[!DNL Google Spreadsheets]</li> 
     <li>[!DNL Google Slides]</li> 
     <li>[!DNL Google Drawings]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td >[!UICONTROL Convert [!DNL Google Documents] fichiers à formater]</td>
    <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Documents].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Spreadsheets] fichiers à formater]</td>
    <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Spreadsheets].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Slides] fichiers à formater]</td>
    <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Slides].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Drawings] fichiers à formater]</td>
    <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Drawings].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Watch]</td>
    <td>Indiquez si vous souhaitez surveiller les nouveaux fichiers et toutes les modifications, ou uniquement les nouveaux fichiers.</td>
  </tr> 
  <tr> 
    <td>[!UICONTROL Maximum number of downloaded files]</td>
    <td>Définissez le nombre maximum de résultats que [!DNL Workfront Fusion] téléchargera au cours d’un cycle (le nombre de répétitions par excécution de scénario).</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch All Files]

Récupère les détails d’un fichier lorsqu’un fichier de votre [!DNL Google Drive] est ajouté ou modifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Drive] à [!DNL Workfront Fusion], voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL What files to watch]</td> 
   <td> <p>Sélectionnez le type de fichiers que vous souhaitez surveiller.</p> 
    <ul> 
     <li>[!UICONTROL All]</li> 
     <li>[!DNL Google Documents]</li> 
     <li>[!DNL Google Spreadsheets]</li> 
     <li>[!DNL Google Slides]</li> 
     <li>[!DNL Google Drawings]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td >[!UICONTROL Convert [!DNL Google Documents] fichiers à formater]</td>
    <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Documents].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Spreadsheets] fichiers à formater]</td>
    <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Spreadsheets].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Slides] fichiers à formater]</td>
    <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Slides].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Drawings] fichiers à formater]</td>
    <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Drawings].</td>
  </tr>  
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td>Indiquez si vous souhaitez surveiller les nouveaux fichiers et toutes les modifications, ou uniquement les nouveaux fichiers.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of downloaded files]</td> 
   <td>Définissez le nombre maximum de résultats que [!DNL Workfront Fusion] téléchargera au cours d’un cycle (le nombre de répétitions par excécution de scénario).</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch shared files]

Se déclenche lorsqu’un nouveau fichier est partagé avec vous ou qu’un fichier partagé existant est mis à jour.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Drive] à [!DNL Workfront Fusion], voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Select the folder to be watched]</td> 
   <td>Sélectionnez le dossier partagé dans lequel vous souhaitez surveiller les fichiers.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL What files to watch]</td> 
   <td> <p>Sélectionnez le type de fichiers que vous souhaitez surveiller.</p> 
    <ul> 
     <li>[!UICONTROL All]</li> 
     <li>[!DNL Google Documents]</li> 
     <li>[!DNL Google Spreadsheets]</li> 
     <li>[!DNL Google Slides]</li> 
     <li>[!DNL Google Drawings]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td >[!UICONTROL Convert [!DNL Google Documents] fichiers à formater]</td>
    <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Documents].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Spreadsheets] fichiers à formater]</td>
    <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Spreadsheets].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Slides] fichiers à formater]</td>
    <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Slides].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Drawings] fichiers à formater]</td>
    <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Drawings].</td>
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td>Indiquez si vous souhaitez surveiller les nouveaux fichiers et toutes les modifications, ou uniquement les nouveaux fichiers.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of downloaded files]</td> 
   <td>Définissez le nombre maximum de résultats que [!DNL Workfront Fusion] téléchargera au cours d’un cycle (le nombre de répétitions par excécution de scénario).</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Comments]

Se déclenche lorsqu’un commentaire est ajouté ou modifié dans le fichier sélectionné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Drive] à [!DNL Workfront Fusion], voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File]</td> 
   <td>Sélectionnez le fichier dont vous souhaitez surveiller les commentaires.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td>Sélectionnez si vous souhaitez surveiller toutes les modifications ou les nouveaux commentaires uniquement.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned comments]</td> 
   <td>Définissez le nombre maximal de commentaires que [!DNL Workfront Fusion] renverra au cours d’un cycle (nombre de répétitions par exécution de scénario).</td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [[!UICONTROL Upload a File]](#upload-a-file)
* [[!UICONTROL Update a File]](#update-a-file)
* [[!UICONTROL Copy a File]](#copy-a-file)
* [[!UICONTROL Delete a File]](#delete-a-file)
* [[!UICONTROL Move a File/Folder to Trash]](#move-a-filefolder-to-trash)
* [[!UICONTROL Get a file]](#get-a-file)
* [[!UICONTROL Search for Files/Folders]](#search-for-filesfolders)
* [[!UICONTROL Create a Folder]](#create-a-folder)
* [[!UICONTROL Get a share link]](#get-a-share-link)

#### [!UICONTROL Upload a File]

Charge un fichier sur votre [!DNL Google Drive].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Drive] à [!DNL Workfront Fusion], voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Destination]</td> 
   <td> <p>Sélectionnez la destination où vous souhaitez charger un fichier.</p> 
    <ul> 
     <li>[!DNL My Drive]</li> 
     <li>[!DNL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Target folder]</td> 
   <td>Sélectionnez le dossier vers lequel vous souhaitez charger un fichier. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td>Choisissez si vous voulez utiliser un fichier transmis par un module précédent ou si vous voulez mapper le fichier manuellement.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File name]</td> 
   <td>Sélectionnez le nom du fichier. Cette option est disponible si vous sélectionnez « [!UICONTROL Map] » dans le champ [!UICONTROL source file].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Data]</td> 
   <td>Sélectionnez le fichier de données que vous souhaitez charger. Cette option est disponible si vous sélectionnez « [!UICONTROL Map] » dans le champ [!UICONTROL source file].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Title]</td> 
   <td>Saisissez un titre pour le nouveau fichier.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert a file]</td> 
   <td>L’activation de cette option permet au module de convertir les fichiers au format [!DNL Google] correspondant.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a File]

Met à jour les métadonnées ou le contenu d’un fichier.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Drive] à [!DNL Workfront Fusion], voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>Sélectionnez la destination où vous souhaitez charger un fichier.</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Move to a folder]</td> 
   <td>Si vous souhaitez déplacer le fichier vers un autre dossier, sélectionnez le dossier dans lequel vous souhaitez déplacer le fichier.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>Mappez l’ID du fichier que vous souhaitez mettre à jour.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Title]</td> 
   <td>Saisissez un titre pour le fichier mis à jour.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Change a file content]</td> 
   <td>Indiquez si vous souhaitez remplacer le contenu du fichier.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td>Choisissez si vous voulez utiliser un fichier transmis par un module précédent ou si vous voulez mapper le fichier manuellement. Ce champ est disponible si vous avez choisi de modifier le contenu du fichier dans le champ précédent.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File name]</td> 
   <td>Sélectionnez le nom du fichier. Cette option est disponible si vous sélectionnez « [!UICONTROL Map] » dans le champ [!UICONTROL source file].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Data]</td> 
   <td>Sélectionnez le fichier de données que vous souhaitez charger. Cette option est disponible si vous sélectionnez « [!UICONTROL Map] » dans le champ [!UICONTROL source file].</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Copy a File]

Copie un fichier au nouvel emplacement.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Drive] à [!DNL Workfront Fusion], voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>Sélectionnez la destination où vous souhaitez charger un fichier.</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Target folder]</td> 
   <td>Sélectionnez le dossier dans lequel se trouve le fichier à copier.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>Mappez l’ID du fichier que vous souhaitez mettre à jour.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL The name of the copy]</td> 
   <td>Saisissez un titre pour le nouveau fichier. Laissez ce champ vide si vous ne souhaitez pas modifier le nom du fichier d’origine.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a File]

Supprime définitivement un fichier ou un dossier.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Drive] à [!DNL Workfront Fusion], voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>Mappez l’ID du fichier que vous souhaitez supprimer.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a File/Folder to Trash]

Déplace un fichier ou un dossier vers la corbeille.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Drive] à [!DNL Workfront Fusion], voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>Mappez l’ID du fichier que vous souhaitez mettre à la corbeille.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a file]

Récupère le fichier dont l&#39;ID est spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Drive] à [!DNL Workfront Fusion], voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Documents] fichiers à formater]</td> 
   <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Documents].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Spreadsheets] fichiers à formater]</td> 
   <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Spreadsheets].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Slides] fichiers à formater]</td> 
   <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Slides].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Drawings] fichiers à formater]</td> 
   <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Drawings].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>Mappez l’identifiant du fichier que vous souhaitez récupérer.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search for Files/Folders]

Recherche des fichiers ou des dossiers sur la base de critères de recherche.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Drive] à [!DNL Workfront Fusion], voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>Sélectionnez la destination à rechercher.</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL List a folder]</td> 
   <td>Accédez au dossier dans lequel vous souhaitez rechercher les fichiers ou les dossiers.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Retrieve]</td> 
   <td> <p> Indiquez si vous souhaitez effectuer la recherche sur des fichiers, des dossiers ou les deux.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Search]</p> </td> 
   <td> <p>Sélectionnez le type de recherche que vous souhaitez effectuer.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Search within file/folder names]</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Query]</strong> </p> <p>Saisissez une partie du nom du fichier ou le nom du fichier complet (y compris le suffixe) que vous souhaitez rechercher.</p> </li> 
       <li> <p><strong>[!UICONTROL Search Options]</strong> </p> <p>Sélectionnez si vous voulez rechercher le terme exact ou si vous voulez rechercher les mots qui contiennent le terme recherché.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Fulltext] la recherche</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Query]</strong> </p> <p>Saisissez le terme de recherche que vous souhaitez rechercher dans votre [!DNL Google Drive].</p> </li> 
      </ul> </li> 
     <li> <p><strong>Saisir une requête personnalisée</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Query]</strong> </p> <p>Saisissez la requête personnalisée. Pour plus d’informations, reportez-vous à la section [!UICONTROL Search for Files] de cet article.</p> </li> 
       <li> <p><strong>Ajouter le dossier sélectionné ci-dessus à la requête</strong> </p> <p>Recherche le dossier dans la collection des dossiers parent. Cette opération permet de trouver tous les fichiers et dossiers situés directement dans le dossier sélectionné au-dessus.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned results]</td> 
   <td>Définissez le nombre maximum de fichiers ou de dossiers que [!DNL Workfront Fusion] renverra au cours d’un cycle d’exécution.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Continue the execution of the route even if the module returns no results]</td> 
   <td>Activez cette option pour vous assurer que le scénario ne s’arrête pas si le module ne renvoie aucun résultat.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Folder]

Crée un dossier à l’emplacement spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Drive] à [!DNL Workfront Fusion], voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>Sélectionnez la destination où vous souhaitez charger un fichier.</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL New folder location]</td> 
   <td>Naviguez jusqu’à l’emplacement où vous souhaitez créer un dossier.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL The name of the new folder]</td> 
   <td>Saisissez un nom pour le dossier que vous créez.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Share folder]</td> 
   <td>Sélectionnez cette option si vous souhaitez partager le dossier avec toute personne disposant du lien [!UICONTROL Share]. Dans le cas contraire, le lien de partage est réservé à la personne propriétaire.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a share link]

Récupère le lien de partage d’un fichier dans Google Drive.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Drive] à [!DNL Workfront Fusion], voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>Indiquez l’ID du fichier dont vous souhaitez obtenir le lien de partage.</td> 
  </tr> 
 </tbody> 
</table>

## Dépannage

### Impossible de charger ou de mettre à jour un fichier

Il existe plusieurs situations dans lesquelles le chargement ou la mise à jour d’un fichier échoue :

* Le fichier chargé est trop volumineux et dépasse la taille maximale autorisée pour votre plan [!DNL Google Drive] ou vous avez dépassé votre limite de stockage [!DNL Google Drive]. Vous pouvez soit mettre à niveau votre plan de stockage, soit supprimer les fichiers existants du service [!DNL Google Drive].
* Le dossier sélectionné dans lequel le fichier devait être chargé n’existe plus. Le scénario s’arrête et il est alors nécessaire de sélectionner à nouveau un dossier cible.

## Rechercher des fichiers

Dans le module Répertorier des fichiers dans un dossier, vous pouvez utiliser votre propre requête, qui se compose des éléments suivants :

* **[!UICONTROL Field]** - Attribut du fichier recherché, par exemple, l’attribut `name` du fichier.

* **[!UICONTROL Operator]** - Test effectué sur les données pour fournir une correspondance, par exemple, `contains`.

* **[!UICONTROL Value]** - Le contenu de l’attribut testé, par exemple le nom du fichier `My cool document`.

Combinez les clauses avec les conjonctions `and` ou `or`, et annulez la requête avec `not`.

* [Champs](#fields)
* [Types de valeurs](#value-types)
* [Opérateurs](#operators)
* [Exemples](#examples)

### Champs

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>champ </th> 
   <th>Type de valeur </th> 
   <th>Opérateurs</th> 
   <th> <p> Description</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>[!UICONTROL title]</code></td> 
   <td>chaîne</td> 
   <td><code>contains</code><sup>1</sup>, <code>=</code>, <code>!=</code></td> 
   <td> <p> Nom du fichier.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL fullText]</code> </td> 
   <td>chaîne </td> 
   <td><code>contains</code><sup>2, 3</sup> </td> 
   <td> <p> Texte complet du fichier comprenant le nom, la description, le contenu et le texte indexable.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL mimeType]</code> </td> 
   <td> chaîne</td> 
   <td><code>contains</code>, <code>=</code>, <code>!=</code></td> 
   <td> <p> Type MIME du fichier.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL modifiedDate]</code> </td> 
   <td> date<sup>4</sup></td> 
   <td><code> &lt;=</code>, <code>&lt;</code>, <code>=</code>, <code>!=</code>, <code>></code>, <code>>=</code></td> 
   <td> <p> Date de la dernière modification du fichier.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL lastViewedByMeDate]</code> </td> 
   <td> date<sup>4</sup></td> 
   <td><code>&lt;=</code>, <code>&lt;</code>, <code>=</code>, <code>!=</code>, <code>></code>, <code>>=</code></td> 
   <td> <p> Date à laquelle l’utilisateur ou l’utilisatrice a consulté un fichier pour la dernière fois.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL trashed]</code></td> 
   <td>booléen </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p> Que le fichier soit dans la corbeille ou non.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL starred]</code></td> 
   <td>booléen </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p>Que le fichier soit marqué d’une étoile ou non.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL parents]</code></td> 
   <td>Collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Indique si la collection de [!UICONTROL parents] contient l’ID spécifié.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL owners]</code></td> 
   <td>Collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Utilisateurs et utilisatrices propriétaires du fichier.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL writers]</code></td> 
   <td>Collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Utilisateurs et utilisatrices autorisés à modifier le fichier.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL readers] </code> </td> 
   <td>Collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Utilisateurs et utilisatrices autorisés à lire le fichier.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL sharedWithMe]</code> </td> 
   <td>booléen </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p> Fichiers qui se trouvent dans la collection « Partagés avec moi » de l’utilisateur ou de l’utilisatrice.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL properties] </code> </td> 
   <td>Collection</td> 
   <td><code>has </code> </td> 
   <td> <p> Propriétés des fichiers publics personnalisés.</p> </td> 
  </tr> 
 </tbody> 
</table>

Tenez compte de ce qui suit à propos des opérateurs dans ces champs :

* L’opérateur `contains` ne recherche la correspondance de préfixes que pour un `title`.

  Par exemple, le titre « HelloWorld » correspond à `title contains 'Hello'` mais pas à `title contains 'World'`.

* L’opérateur `contains` ne recherche la correspondance que sur des jetons de chaînes de caractères entières pour le `fullText`.

  Par exemple, si le texte intégral d’un document contient la chaîne « HelloWorld », seule la requête `fullText contains 'HelloWorld'` renvoie un résultat. Des requêtes telles que `fullText contains 'Hello'` ne reverraient pas de résultat dans ce scénario.

* L’opérateur `contains` recherche la correspondance d’une expression alphanumérique exacte si elle est entourée de guillemets.

  Par exemple, si le `fullText` d’un document contient la chaîne « Hello there world », la requête `fullText contains '"Hello there"'` renvoie un résultat, mais pas la requête `fullText contains '"Hello world"'`.

  De plus, la recherche étant alphanumérique, si le `fullText` d’un document contient la chaîne « Hello_world », la requête `fullText contains '"Hello world"'` renvoie un résultat.

* Les champs de date `type` ne sont actuellement pas comparables entre eux, mais seulement avec des dates constantes.

### Types de valeurs

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Type de valeur</th> 
   <th> <p> Notes</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Chaîne </td> 
   <td> <p>Entourer de guillemets simples '. Ignore les guillemets simples dans les requêtes avec <code>\'</code>, par exemple, <code> 'Valentine\'s Day'</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>Booléen </td> 
   <td> <p><code>true </code>ou <code>false</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>Date </td> 
   <td> <p>Format RFC 3339, le fuseau horaire par défaut est UTC, par exemple <code>2012-06-04T12:00:00-08:00</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Opérateurs

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Opérateur </th> 
   <th> <p>Notes</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>contains</code></td> 
   <td> <p>Le contenu d’une chaîne est présent dans l’autre.</p> </td> 
  </tr> 
  <tr> 
   <td><code>=</code> </td> 
   <td> <p> Le contenu d’une chaîne ou d’un booléen est égal à l’autre.</p> </td> 
  </tr> 
  <tr> 
   <td><code>!=</code> </td> 
   <td> <p> Le contenu d’une chaîne ou d’un booléen n’est pas égal à l’autre.</p> </td> 
  </tr> 
  <tr> 
   <td><code>&lt;</code> </td> 
   <td> <p> Une date est antérieure à une autre.</p> </td> 
  </tr> 
  <tr> 
   <td><code>&lt;=</code> </td> 
   <td> <p> Une date est antérieure ou égale à une autre.</p> </td> 
  </tr> 
  <tr> 
   <td><code>></code> </td> 
   <td> <p> Une date est postérieure à une autre.</p> </td> 
  </tr> 
  <tr> 
   <td><code>>=</code> </td> 
   <td> <p> Une date est postérieure ou égale à une autre.</p> </td> 
  </tr> 
  <tr> 
   <td><code>in </code> </td> 
   <td> <p>Un élément est contenu dans une collection.</p> </td> 
  </tr> 
  <tr> 
   <td><code>and </code> </td> 
   <td> <p>Retourne les fichiers qui correspondent aux deux clauses.</p> </td> 
  </tr> 
  <tr> 
   <td><code>or </code> </td> 
   <td> <p>Retourne les fichiers qui correspondent à l’une ou l’autre clause.</p> </td> 
  </tr> 
  <tr> 
   <td><code>not </code> </td> 
   <td> <p>Annule une clause de recherche.</p> </td> 
  </tr> 
  <tr> 
   <td><code>has </code> </td> 
   <td> <p>Une collection contient un élément correspondant aux paramètres.</p> </td> 
  </tr> 
 </tbody> 
</table>

Pour les clauses composées, vous pouvez utiliser des parenthèses pour les regrouper. Par exemple :
`modifiedDate > '2012-06-04T12:00:00' and (mimeType contains 'image/' or mimeType contains 'video/')` Cette recherche renvoie tous les fichiers de type MIME image ou vidéo dont la dernière modification est postérieure au 4 juin 2012. Les opérateurs `and` et `or` étant évalués de gauche à droite, sans parenthèses, l’exemple ci-dessus ne renverrait que les images modifiées après le 4 juin 2012, mais il renverrait toutes les vidéos, même celles antérieures au 4 juin 2012.

### Exemples

Tous les exemples de cette page montrent le paramètre `<q>q</q>` non codé, où `title = 'hello'` est codé comme `title+%3d+%27hello%27`. Les bibliothèques clientes gèrent cet encodage automatiquement.

* Recherche des fichiers portant le nom « hello »
  <pre>title = 'hello'</pre>
* Recherche de dossiers à l’aide du type MIME spécifique au dossier
  <pre>mimeType = 'application/vnd.google-apps.folder'</pre>
* Recherche des fichiers qui ne sont pas des dossiers
  <pre>mimeType != 'application/vnd.google-apps.folder'</pre>
* Recherche des fichiers dont le nom contient les mots « hello » et « goodbye »
  <pre>le titre contient « hello » et [!UICONTROL name] contient « goodbye »</pre>
* Recherche des fichiers dont le nom ne contient pas le mot « hello »
  <pre>not title contains 'hello'</pre>
* Recherche des fichiers contenant le mot « hello » dans leur contenu
  <pre>fullText contains 'hello'</pre>
* Recherche des fichiers ne contenant pas le mot « hello » dans leur contenu
  <pre>not fullText contains 'hello'</pre>
* Recherche des fichiers contenant l’expression exacte « hello world » dans leur contenu
  <pre>fullText contains '"hello world"'fullText contains '"hello_world"'</pre>
* Recherche des fichiers avec une requête contenant le caractère « \ » (par exemple, &quot;\authors&quot;)
  <pre>fullText contains '\\authors'</pre>
* Recherche des fichiers pouvant être écrits par l’utilisateur `test@example.org`
  <pre>'test@example.org' in [!DNL writers]</pre>
* Recherche de l’ID `1234567` dans la collection `parents`. Cette opération permet de trouver tous les fichiers et dossiers situés directement dans le dossier dont l’ID est `1234567`.
  <pre>'1234567' dans [!UICONTROL parents]</pre>
* Recherche de l’ID d’alias `appDataFolder` dans la collection `parents`. Cette opération permet de trouver tous les fichiers et dossiers situés directement sous le [dossier Données d’application](https://developers.google.com/drive/api/v2/appdata).
  <pre>'appDataFolder' in parents</pre>
* Rechercher des fichiers pouvant être écrits par les utilisateurs `test@example.org` et `test2@example.org`
  <pre>'test@example.org' in writers and 'test2@example.org' in writers</pre>
* Recherche des fichiers contenant le texte « important » qui se trouvent dans la corbeille
  <pre>fullText contains 'important' and trashed = true</pre>
* Recherche des fichiers modifiés après le 4 juin 2012
  <pre>modifiedDate &gt; '2012-06-04T12:00:00' // default time zone is UTC</pre><pre>modifiedDate &gt; '2012-06-04T12:00:00-08:00'</pre>
* Recherche des fichiers partagés avec la personne autorisée dont le nom contient « hello »
  <pre>sharedWithMe and title contains 'hello'</pre>
* Recherche des fichiers avec une [propriété de fichier personnalisé](https://developers.google.com/drive/api/v2/properties) nommée `additionalID` avec la valeur `8e8aceg2af2ge72e78`
  <pre>Les propriétés comportent { key='additionalID' and value='8e8aceg2af2ge72e78' and visibility='PRIVATE' }.</pre>

La source de ce guide est la [[!DNL Google Drive] documentation](https://developers.google.com/drive/api/v2/search-shareddrives).
