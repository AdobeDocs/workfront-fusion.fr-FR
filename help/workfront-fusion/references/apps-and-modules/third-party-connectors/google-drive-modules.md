---
title: Modules Google Drive
description: Les modules  [!DNL Adobe Workfront Fusion Google Drive]  vous permettent de surveiller, de rechercher, de créer, de mettre à jour, de supprimer et de gérer vos fichiers, dossiers ou lecteurs partagés dans votre  [!DNL Google Drive].
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 788f4e1b-d774-45ad-a8be-b16922c1d5dc
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2096'
ht-degree: 58%

---

# Modules [!DNL Google Drive]

Les modules Adobe Workfront Fusion [!DNL Google Drive] vous permettent de surveiller, rechercher, créer, mettre à jour, supprimer et gérer vos fichiers, dossiers ou lecteurs partagés dans votre [!DNL Google Drive].

Dans un scénario Adobe Workfront Fusion, vous pouvez connecter votre compte [!DNL Google Drive] à plusieurs applications et services tiers.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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



## Connexion de [!DNL Google Drive] à Workfront Fusion

Si vous utilisez [!DNL @gmail.com] ou [!DNL @googlemail.com] utilisateur, vous devez créer un client OAuth sur le [!DNL Google Cloud Platform] pour obtenir vos [!UICONTROL ID client] et [!UICONTROL Secret client].

Pour obtenir des instructions détaillées sur la création du client OAuth (et l’obtention de l’[!UICONTROL ID client] et du [!UICONTROL Secret client]), voir [Connecter Adobe Workfront Fusion à [!DNL Google Services] à l’aide d’un client OAuth personnalisé](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Drive] à [!UICONTROL Workfront Fusion], voir [Créer une connexion à [!UICONTROL Adobe Workfront Fusion] : instructions de base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

## Modules [!DNL Google Drive] et leurs champs

Lorsque vous configurez les modules [!DNL Google Drive], Workfront Fusion affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Google Drive] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)



* [Déclencheurs](#triggers)
* [Actions](#actions)

### Déclencheurs

* [[!UICONTROL Surveiller tous les fichiers]](#watch-all-files)
* [[!UICONTROL Voir les commentaires]](#watch-comments)
* [[!UICONTROL Observer les fichiers dans le dossier]](#watch-files-in-folder)
* [[!UICONTROL Surveiller les fichiers partagés]](#watch-shared-files)

#### [!UICONTROL Surveiller tous les fichiers]

Ce module de déclenchement démarre un scénario lorsqu’un fichier de votre [!DNL Google Drive] est ajouté ou modifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Google Drive] à Workfront Fusion, voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
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
    <td >[!UICONTROL Convert [!DNL Google Documents] files to format]</td>
    <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Documents].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Spreadsheets] files to format]</td>
    <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Spreadsheets].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Slides] files to format]</td>
    <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Slides].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Drawings] files to format]</td>
    <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Drawings].</td>
  </tr>  
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td>Indiquez si vous souhaitez surveiller les nouveaux fichiers et toutes les modifications, ou uniquement les nouveaux fichiers.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of downloaded files]</td> 
   <td>Définissez le nombre maximal de résultats que Workfront Fusion téléchargera au cours d’un cycle (le nombre de répétitions par exécution de scénario).</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Surveiller les commentaires]

Ce module de déclenchement démarre un scénario lorsqu’un commentaire est ajouté ou modifié sur le fichier sélectionné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Google Drive] à Workfront Fusion, voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
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
   <td>Définissez le nombre maximal de commentaires que Workfront Fusion renverra au cours d’un cycle (le nombre de répétitions par exécution de scénario).</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Observer les fichiers dans le dossier]

Ce module de déclenchement démarre un scénario lorsqu’un fichier est ajouté ou modifié dans le dossier spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection] </td>
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Google Drive] à Workfront Fusion, voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
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
    <td >[!UICONTROL Convert [!DNL Google Documents] files to format]</td>
    <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Documents].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Spreadsheets] files to format]</td>
    <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Spreadsheets].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Slides] files to format]</td>
    <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Slides].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Drawings] files to format]</td>
    <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Drawings].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Watch]</td>
    <td>Indiquez si vous souhaitez surveiller les nouveaux fichiers et toutes les modifications, ou uniquement les nouveaux fichiers.</td>
  </tr> 
  <tr> 
    <td>[!UICONTROL Maximum number of downloaded files]</td>
    <td>Définissez le nombre maximal de résultats que Workfront Fusion téléchargera au cours d’un cycle (le nombre de répétitions par exécution de scénario).</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Surveiller les fichiers partagés]

Se déclenche lorsqu’un nouveau fichier est partagé avec vous ou qu’un fichier partagé existant est mis à jour.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Google Drive] à Workfront Fusion, voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
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
    <td >[!UICONTROL Convert [!DNL Google Documents] files to format]</td>
    <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Documents].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Spreadsheets] files to format]</td>
    <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Spreadsheets].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Slides] files to format]</td>
    <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Slides].</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Drawings] files to format]</td>
    <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Drawings].</td>
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td>Indiquez si vous souhaitez surveiller les nouveaux fichiers et toutes les modifications, ou uniquement les nouveaux fichiers.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of downloaded files]</td> 
   <td>Définissez le nombre maximal de résultats que Workfront Fusion téléchargera au cours d’un cycle (le nombre de répétitions par exécution de scénario).</td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [[!UICONTROL Copier un fichier]](#copy-a-file)
* [[!UICONTROL Créer un fFolder]](#create-a-folder)
* [[!UICONTROL Supprimer un fichier]](#delete-a-file)
* [[!UICONTROL Obtenir un fichier]](#get-a-file)
* [[!UICONTROL Obtenir un lien de partage]](#get-a-share-link)
* [[!UICONTROL Déplacer un fichier vers la corbeille]](#move-a-filefolder-to-trash)
* [[!UICONTROL Rechercher des fichiers ou des dossiers]](#search-for-filesfolders)
* [[!UICONTROL Mettre à jour un fichier]](#update-a-file)
* [[!UICONTROL Charger un fichier]](#upload-a-file)

#### [!UICONTROL Copier un fichier]

Ce module d’action copie un fichier au nouvel emplacement.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Google Drive] à Workfront Fusion, voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>Sélectionnez la destination vers laquelle vous souhaitez copier un fichier.</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Target folder]</td> 
   <td>Sélectionnez le dossier contenant le fichier à copier.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>Mappez l’identifiant du fichier que vous souhaitez copier.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL The name of the copy]</td> 
   <td>Saisissez un titre pour le nouveau fichier. Laissez ce champ vide si vous ne souhaitez pas modifier le nom du fichier d’origine.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Créer un dossier]

Ce module d’action crée un dossier à l’emplacement spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Google Drive] à Workfront Fusion, voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>Sélectionnez la destination vers laquelle vous souhaitez créer un dossier.</p> 
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
   <td>Sélectionnez cette option si vous souhaitez partager le dossier avec toute personne ayant le lien [!UICONTROL Share]. Dans le cas contraire, le lien de partage est réservé à la personne propriétaire.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Supprimer un fichier]

Ce module d’action supprime définitivement un fichier ou un dossier.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Google Drive] à Workfront Fusion, voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>Mappez l’ID du fichier que vous souhaitez supprimer.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obtenir un fichier]

Ce module d&#39;action récupère le fichier avec l&#39;identifiant spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Google Drive] à Workfront Fusion, voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Documents] files to format]</td> 
   <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Documents].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Spreadsheets] files to format]</td> 
   <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Spreadsheets].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Slides] files to format]</td> 
   <td>Sélectionnez le format de fichier dans lequel vous voulez convertir les [!DNL Google Slides].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Drawings] files to format]</td> 
   <td>Sélectionnez le format de fichier auquel vous souhaitez convertir les [!DNL Google Drawings].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>Mappez l’identifiant du fichier que vous souhaitez récupérer.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obtenir un lien de partage]

Ce module d&#39;action récupère le lien de partage d&#39;un fichier dans Google Drive.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Google Drive] à Workfront Fusion, voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>Indiquez l’ID du fichier dont vous souhaitez obtenir le lien de partage.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Déplacer un fichier vers la corbeille]

Ce module d’action déplace un fichier ou un dossier vers la corbeille.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Google Drive] à Workfront Fusion, voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>Mappez l’ID du fichier que vous souhaitez mettre à la corbeille.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Rechercher des fichiers ou des dossiers]

Ce module de recherche recherche des fichiers ou des dossiers en fonction de critères de recherche.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Google Drive] à Workfront Fusion, voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>Sélectionnez le lecteur de destination que vous souhaitez rechercher.</p> 
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
       <li> <p><strong>[!UICONTROL Search Options]</strong> </p> <p>Sélectionnez si vous voulez rechercher le terme exact ou si vous voulez rechercher les mots qui contiennent le terme de recherche.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Fulltext] search</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Query]</strong> </p> <p>Saisissez le terme de recherche que vous souhaitez rechercher dans votre [!DNL Google Drive].</p> </li> 
      </ul> </li> 
     <li> <p><strong>Saisir une requête personnalisée</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Query]</strong> </p> <p>Saisissez la requête personnalisée. Pour plus de détails, veuillez vous référer à la section [!UICONTROL Search for Files] de cet article.</p> </li> 
       <li> <p><strong>Ajouter le dossier sélectionné ci-dessus à la requête</strong> </p> <p>Recherche le dossier dans la collection des dossiers parent. Cette opération permet de trouver tous les fichiers et dossiers situés directement dans le dossier sélectionné au-dessus.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned results]</td> 
   <td>Définissez le nombre maximal de fichiers ou de dossiers que Workfront Fusion renverra au cours d’un cycle d’exécution.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Continue the execution of the route even if the module returns no results]</td> 
   <td>Activez cette option pour vous assurer que le scénario ne s’arrête pas si le module ne renvoie aucun résultat.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mettre à jour un fichier]

Ce module d’action met à jour les métadonnées ou le contenu d’un fichier.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Google Drive] à Workfront Fusion, voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>Sélectionnez la destination qui contient le fichier à mettre à jour.</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Move to a folder]</td> 
   <td>Si vous souhaitez déplacer le fichier vers un dossier spécifique, sélectionnez le dossier dans lequel vous souhaitez déplacer le fichier.</td> 
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
   <td>Si vous remplacez le contenu, sélectionnez un fichier source dans un module précédent ou mappez le nom et les données du fichier source.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convertir un fichier]</td> 
   <td>Activez cette option pour convertir le fichier au format de fichier Google correspondant.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Charger un fichier]

Charge un fichier sur votre [!DNL Google Drive].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Google Drive] à Workfront Fusion, voir <a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Google Drive] à [!UICONTROL Workfront Fusion]</a></p> </td> 
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
   <td>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</td> 
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

## Dépannage

### Impossible de charger ou de mettre à jour un fichier

Plusieurs raisons peuvent expliquer l’échec du chargement ou de la mise à jour d’un fichier :

* Le fichier chargé est trop volumineux et dépasse la taille maximale de fichier autorisée pour votre plan de [!DNL Google Drive], ou vous avez dépassé votre limite de stockage [!DNL Google Drive]. Vous pouvez soit mettre à niveau votre plan de stockage, soit supprimer les fichiers existants du service [!DNL Google Drive].
* Le dossier sélectionné dans lequel le fichier devait être chargé n’existe plus. Dans ce cas, le scénario s’arrête et vous devez sélectionner un autre dossier cible dans le module .

<!-- Not present February 2025

## Search for files

In the module List files in a folder you can use your own query which consists of these parts:

* **[!UICONTROL Field]** - Attribute of the file that is being searched, for example, the attribute `name` of the file.

* **[!UICONTROL Operator]** - Test that is performed on the data to provide a match, for example, `contains`.

* **[!UICONTROL Value]** - The content of the attribute that is tested, for example, the name of the file `My cool document`.

Combine clauses with the conjunctions `and` or `or`, and negate the query with `not`.

* [Fields](#fields)
* [Value types](#value-types)
* [Operators](#operators)
* [Examples](#examples)

### Fields 

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Field </th> 
   <th>Value Type </th> 
   <th>Operators</th> 
   <th> <p> Description</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>[!UICONTROL title]</code></td> 
   <td>string</td> 
   <td><code>contains</code><sup>1</sup>, <code>=</code>, <code>!=</code></td> 
   <td> <p> Name of the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL fullText]</code> </td> 
   <td>string </td> 
   <td><code>contains</code><sup>2, 3</sup> </td> 
   <td> <p> Full text of the file including name, description, content, and indexable text.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL mimeType]</code> </td> 
   <td> string</td> 
   <td><code>contains</code>, <code>=</code>, <code>!=</code></td> 
   <td> <p> MIME type of the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL modifiedDate]</code> </td> 
   <td> date<sup>4</sup></td> 
   <td><code> &lt;=</code>, <code>&lt;</code>, <code>=</code>, <code>!=</code>, <code>></code>, <code>>=</code></td> 
   <td> <p> Date of the last modification to the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL lastViewedByMeDate]</code> </td> 
   <td> date<sup>4</sup></td> 
   <td><code>&lt;=</code>, <code>&lt;</code>, <code>=</code>, <code>!=</code>, <code>></code>, <code>>=</code></td> 
   <td> <p> Date that the user last viewed a file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL trashed]</code></td> 
   <td>boolean </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p> Whether the file is in the trash or not.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL starred]</code></td> 
   <td>boolean </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p>Whether the file is starred or not.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL parents]</code></td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Whether the [!UICONTROL parents] collection contains the specified ID.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL owners]</code></td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Users who own the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL writers]</code></td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Users who have permission to modify the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL readers] </code> </td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Users who have permission to read the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL sharedWithMe]</code> </td> 
   <td>boolean </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p> Files that are in the user's "Shared with me" collection.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL properties] </code> </td> 
   <td>collection</td> 
   <td><code>has </code> </td> 
   <td> <p> Public custom file properties.</p> </td> 
  </tr> 
 </tbody> 
</table>

Consider the following about operators in these fields:

* The `contains` operator only performs prefix matching for a `title`.

   For example, the title "HelloWorld" matches for `title contains 'Hello'` but not for `title contains 'World'`.

* The `contains` operator only performs matching on entire string tokens for `fullText`.

   For example, if the full text of a doc contains the string "HelloWorld" only the query `fullText contains 'HelloWorld'` returns a result. Queries such as `fullText contains 'Hello'` would not return results in this scenario.

* The `contains` operator matches on an exact alphanumeric phrase if it is surrounded by double quotes.

   For example, if the `fullText` of a doc contains the string "Hello there world", then the query `fullText contains '"Hello there"'` returns a result, but the query `fullText contains '"Hello world"'` does not.

   Furthermore, because the search is alphanumeric, if the `fullText` of a doc contains the string "Hello_world", then the query `fullText contains '"Hello world"'` returns a result.

* Fields of `type` date are currently not comparable to each other, only to constant dates.

### Value types

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Value Type</th> 
   <th> <p> Notes</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>String </td> 
   <td> <p>Surround with single quotes '. Escape single quotes in queries with <code>\'</code>, e.g.,<code> 'Valentine\'s Day'</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>Boolean </td> 
   <td> <p><code>true </code>or <code>false</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>Date </td> 
   <td> <p>RFC 3339 format, default timezone is UTC, e.g., <code>2012-06-04T12:00:00-08:00</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Operators

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Operator </th> 
   <th> <p>Notes</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>contains</code></td> 
   <td> <p>The content of one string is present in the other.</p> </td> 
  </tr> 
  <tr> 
   <td><code>=</code> </td> 
   <td> <p> The content of a string or boolean is equal to the other.</p> </td> 
  </tr> 
  <tr> 
   <td><code>!=</code> </td> 
   <td> <p> The content of a string or boolean is not equal to the other.</p> </td> 
  </tr> 
  <tr> 
   <td><code>&lt;</code> </td> 
   <td> <p> A date is earlier than another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>&lt;=</code> </td> 
   <td> <p> A date is earlier than or equal to another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>></code> </td> 
   <td> <p> A date is later than another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>>=</code> </td> 
   <td> <p> A date is later than or equal to another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>in </code> </td> 
   <td> <p>An element is contained within a collection.</p> </td> 
  </tr> 
  <tr> 
   <td><code>and </code> </td> 
   <td> <p>Return files that match both clauses.</p> </td> 
  </tr> 
  <tr> 
   <td><code>or </code> </td> 
   <td> <p>Return files that match either clause.</p> </td> 
  </tr> 
  <tr> 
   <td><code>not </code> </td> 
   <td> <p>Negates a search clause.</p> </td> 
  </tr> 
  <tr> 
   <td><code>has </code> </td> 
   <td> <p>A collection contains an element matching the parameters.</p> </td> 
  </tr> 
 </tbody> 
</table>

For compound clauses, you can use parentheses to group clauses together. For example:
`modifiedDate > '2012-06-04T12:00:00' and (mimeType contains 'image/' or mimeType contains 'video/')` This search returns all files with an image or video MIME type that their last modification was after June 4, 2012. Because `and` and `or` operators are evaluated from left to right, without parentheses, the above example would return only images modified after June 4, 2012, but would return all videos, even those before June 4, 2012.

### Examples 

All examples on this page show the unencoded `<q>q</q>` parameter, where `title = 'hello'` is encoded as `title+%3d+%27hello%27`. Client libraries handle this encoding automatically.

* Search for files with the name "hello"
   <pre>title = 'hello'</pre>
* Search for folders using the folder-specific MIME type
   <pre>mimeType = 'application/vnd.google-apps.folder'</pre>
* Search for files that are not folders
   <pre>mimeType != 'application/vnd.google-apps.folder'</pre>
* Search for files with a name containing the words "hello" and "goodbye"
   <pre>title contains 'hello' and [!UICONTROL name] contains 'goodbye'</pre>
* Search for files with a name that does not contain the word "hello"
   <pre>not title contains 'hello'</pre>
* Search for files containing the word "hello" in the content
   <pre>fullText contains 'hello'</pre>
* Search for files not containing the word "hello" in the content
   <pre>not fullText contains 'hello'</pre>
* Search for files containing the exact phrase "hello world" in the content
   <pre>fullText contains '"hello world"'fullText contains '"hello_world"'</pre>
* Search for files with a query containing the "\" character (e.g., "\authors")
   <pre>fullText contains '\\authors'</pre>
* Search for files writeable by the user `test@example.org`
   <pre>'test@example.org' in [!DNL writers]</pre>
* Search for the ID `1234567` in the `parents` collection. This finds all files and folders located directly in the folder whose ID is `1234567`.
   <pre>'1234567' in [!UICONTROL parents]</pre>
* Search for the alias ID `appDataFolder` in the `parents` collection. This finds all files and folders located directly under the [Application Data folder](https://developers.google.com/drive/api/v2/appdata).
   <pre>'appDataFolder' in parents</pre>
* Search for files writeable by the users `test@example.org` and `test2@example.org`
   <pre>'test@example.org' in writers and 'test2@example.org' in writers</pre>
* Search for files containing the text "important" which are in the trash
   <pre>fullText contains 'important' and trashed = true</pre>
* Search for files modified after June 4th 2012
   <pre>modifiedDate > '2012-06-04T12:00:00' // default time zone is UTC</pre><pre>modifiedDate > '2012-06-04T12:00:00-08:00'</pre>
* Search for files shared with the authorized user with "hello" in the name
   <pre>sharedWithMe and title contains 'hello'</pre>
* Search for files with a [custom file property](https://developers.google.com/drive/api/v2/properties) named `additionalID` with the value `8e8aceg2af2ge72e78`.
   <pre>properties has { key='additionalID' and value='8e8aceg2af2ge72e78' and visibility='PRIVATE' }</pre>

Source of this guide is [[!DNL Google Drive] documentation](https://developers.google.com/drive/api/v2/search-shareddrives).

-->
