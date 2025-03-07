---
title: Modules Microsoft OneDrive
description: Dans un scénario  [!DNL Adobe Workfront Fusion] , vous pouvez automatiser les workflows qui utilisent OneDrive et les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: d21eafad-9c67-4f42-b718-0aa4223846e6
source-git-commit: 632128bdcb6f8b8361f5a28e4a5fb527eb274d54
workflow-type: tm+mt
source-wordcount: '4087'
ht-degree: 96%

---

# Modules [!DNL Microsoft OneDrive]

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!DNL OneDrive] et le connecter à plusieurs applications et services tiers.

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

Pour utiliser les modules [!DNL OneDrive], vous devez disposer d’un compte [!DNL Microsoft OneDrive].



## Informations sur l’API OneDrive

Le connecteur OneDrive utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td> https://graph.microsoft.com/v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Version de l’API</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v2.0.10</td> 
  </tr>
 </tbody> 
 </table>


## Connexion du service [!DNL OneDrive] à [!DNL Workfront Fusion].

Pour obtenir des instructions sur la connexion de votre compte [!DNL OneDrive] à [!UICONTROL Workfront Fusion], voir [Créer une connexion à [!UICONTROL Adobe Workfront Fusion] : instructions de base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Certaines applications Microsoft utilisent la même connexion, qui est liée à des autorisations d’utilisateur ou d’utilisatrice. Ainsi, lors de la création d’une connexion, l’écran de consentement aux autorisations affiche les autorisations précédemment accordées à la connexion de cet utilisateur ou de cette utilisatrice, en plus des nouvelles autorisations nécessaires à l’application actuelle.
>
>Par exemple, si un utilisateur ou une utilisatrice dispose d’autorisations « Lire le tableau » accordées via le connecteur Excel, puis crée une connexion dans le connecteur Outlook pour lire les e-mails, l’écran de consentement aux autorisations affiche à la fois l’autorisation « Lire le tableau » déjà accordée et l’autorisation « Écrire des e-mails » nouvellement requise.

## Modules [!DNL Microsoft OneDrive] et leurs champs

Lorsque vous configurez les modules [!DNL OneDrive], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL OneDrive] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Fichier ou dossier](#filefolder)
* [Autre](#other)

### Fichier ou dossier

* [[!UICONTROL Copier un fichier]](#copy-a-file)
* [[!UICONTROL Créer un dossier]](#create-a-folder)
* [[!UICONTROL Supprimer un fichier/dossier]](#delete-a-filefolder)
* [[!UICONTROL Télécharger un fichier]](#download-a-file)
* [[!UICONTROL Obtenir un fichier]](#get-a-file)
* [[!UICONTROL Obtenir un lien de partage]](#get-a-share-link)
* [[!UICONTROL Déplacer un fichier ou un dossier]](#move-a-filefolder)
* [[!UICONTROL Rechercher des fichiers ou des dossiers]](#search-filesfolders)
* [[!UICONTROL Charger un fichier]](#upload-a-file)
* [[!UICONTROL Surveiller des fichiers ou des dossiers]](#watch-filesfolders)

#### [!UICONTROL Copier un dossier]

Ce module d’action copie un fichier dans un nouvel emplacement de dossier.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour savoir comment connecter votre compte [!DNL OneDrive] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (File ID &amp; File Path)]</td> 
   <td>Indiquez si vous souhaitez identifier le fichier par ID de fichier ou par chemin d’accès au fichier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a File ID] / [!UICONTROL File Path]</td> 
   <td> <p>Sélectionnez le mode de saisie de l’ID de fichier ou du chemin d’accès au fichier :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>Sélectionnez cette option si vous souhaitez saisir directement l’ID ou le chemin d’accès du fichier, ou si vous souhaitez le mapper à partir d’un module précédent.</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>Sélectionnez cette option si vous souhaitez effectuer une sélection dans une liste de fichiers ou de chemins d’accès disponibles. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] location]</td> 
   <td> <p>Sélectionnez l’emplacement contenant le fichier à copier :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Indiquez si le module doit pouvoir saisir un identifiant de lecteur.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Saisissez l’identifiant du lecteur contenant le fichier ou le dossier à copier.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Sélectionnez le site SharePoint qui contient le fichier à déplacer. Les sites disponibles sont des sites suivis par la personne connectée.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>Sélectionnez le groupe dont le lecteur contient le fichier que vous souhaitez copier.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>Sélectionnez ou mappez le lecteur contenant le fichier à copier. Ce champ n’est pas disponible si vous avez sélectionné [!UICONTROL No] dans le champ [!UICONTROL Enable to Enter a Drive ID].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p role="rowheader">[!UICONTROL File] / [!UICONTROL File ID] / [!UICONTROL File Path]</p> </td> 
   <td> <p>Si vous avez sélectionné [!UICONTROL Enter Manually], saisissez ou mappez l’identifiant ou le chemin d’accès du fichier à copier.</p> <p>Si vous avez sélectionné Sélectionner dans la liste, sélectionnez le fichier à copier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a New Folder Location]</td> 
   <td> <p>Sélectionnez le mode de saisie de l’emplacement dans lequel vous souhaitez copier le fichier :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>Sélectionnez cette option si vous souhaitez saisir directement l’ID ou le chemin d’accès du fichier, ou si vous souhaitez le mapper à partir d’un module précédent.</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>Sélectionnez cette option si vous souhaitez choisir parmi une liste de dossiers disponibles. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New OneDrive location]</td> 
   <td> <p>Sélectionnez l’emplacement où vous souhaitez copier le filtre. Cette option est disponible si vous avez choisi de sélectionner l’emplacement du nouveau dossier dans une liste.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Indiquez si le module doit pouvoir saisir un identifiant de lecteur.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Saisissez l’identifiant du lecteur sur lequel vous souhaitez copier le fichier.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Sélectionnez le site [!DNL SharePoint] où vous souhaitez copier le fichier. Les sites disponibles sont des sites suivis par la personne connectée.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>Sélectionnez le groupe dont vous souhaitez copier le fichier sur le lecteur.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>Sélectionnez ou mappez le lecteur contenant le dossier dans lequel vous souhaitez copier le fichier. Ce champ n’est pas disponible si vous avez sélectionné [!UICONTROL No] dans le champ [!UICONTROL Enable to Enter a Drive ID].</p> <p>Si vous laissez ce champ vide, le fichier ou le dossier ne peut être copié que dans le même [!UICONTROL OneDrive].</p> <p>Vous pouvez copier des fichiers et des dossiers de [!UICONTROL My Drive] vers un [!UICONTROL Site's Drive] ou un [!UICONTROL Group's Drive]. </p> <p>Vous ne pouvez copier les fichiers d’un [!UICONTROL Site's Drive] que sur le même lecteur du même site.</p> <p>Vous pouvez copier les fichiers d’un [!UICONTROL Group's Drive] uniquement sur le même lecteur du même groupe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Saisissez ou mappez le dossier dans lequel vous souhaitez déplacer la copie ou le dossier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New Copied File Name]</td> 
   <td> <p>Saisissez ou mappez un nom pour la nouvelle copie du fichier. Vous pouvez laisser ce champ vide si vous ne souhaitez pas modifier le nom du fichier d’origine.</p> <p>Le nom doit inclure l’extension de fichier. Exemple : <code>file.txt</code></p> </td> 
  </tr> 
 </tbody> 
</table>

<!-- Start audit here-->

#### [!UICONTROL Créer un dossier]

Ce module d’action crée un dossier dans le lecteur spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour savoir comment connecter votre compte [!DNL OneDrive] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] location]</td> 
   <td> <p>Sélectionnez l’emplacement où vous souhaitez créer un dossier :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Indiquez si le module doit pouvoir saisir un identifiant de lecteur.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Sélectionnez le lecteur sur lequel vous souhaitez créer un dossier.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Sélectionnez la site [!DNL SharePoint] où vous souhaitez créer un dossier. Les sites disponibles sont des sites suivis par la personne connectée.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>Sélectionnez le groupe propriétaire du lecteur dans lequel vous souhaitez créer un dossier.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>Sélectionnez le lecteur sur lequel vous souhaitez créer un dossier. Ce champ n’est pas disponible si vous avez sélectionné [!UICONTROL No] dans le champ [!UICONTROL Enable to Enter a Drive ID].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Si vous souhaitez que le nouveau dossier soit un sous-dossier, accédez au dossier dans lequel vous souhaitez qu’il soit un sous-dossier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New Folder Name]</td> 
   <td> <p>Saisissez ou mappez un nom pour le nouveau dossier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL If the Folder with the Same Name Exists]</td> 
   <td>Sélectionnez la procédure applicable si un fichier portant le même nom existe déjà.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Supprimer un fichier/dossier]

Ce module d’action supprime le fichier sélectionné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour savoir comment connecter votre compte [!DNL OneDrive] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (File/Folder ID &amp; Path)]</td> 
   <td>Indiquez si vous souhaitez identifier le fichier par ID de fichier ou par chemin d’accès au fichier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a File/Folder ID /Enter a File/Folder Path]</td> 
   <td> <p>Sélectionnez le mode de saisie de l’ID de fichier ou du chemin d’accès au fichier :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>Sélectionnez cette option si vous souhaitez saisir directement l’ID ou le chemin d’accès du fichier, ou si vous souhaitez le mapper à partir d’un module précédent.</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>Sélectionnez cette option si vous souhaitez effectuer une sélection dans une liste de fichiers ou de chemins d’accès disponibles. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] location]</td> 
   <td> <p>Sélectionnez l’emplacement devant faire l’objet de la recherche :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Indiquez si le module doit pouvoir saisir un identifiant de lecteur.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Saisissez l’identifiant du lecteur qui contient le fichier ou le dossier que vous souhaitez supprimer.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Sélectionnez le site [!DNL SharePoint] qui contient le fichier ou le dossier que vous souhaitez supprimer. Les sites disponibles sont des sites suivis par la personne connectée.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>Sélectionnez le groupe dont le lecteur contient le fichier ou le dossier que vous souhaitez supprimer.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>Sélectionnez ou mappez le lecteur qui contient le fichier ou le dossier que vous souhaitez supprimer. Ce champ n’est pas disponible si vous avez sélectionné [!UICONTROL No] dans le champ [!UICONTROL Enable to Enter a Drive ID].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sélectionner [!UICONTROL File/Folder]</td> 
   <td>Indiquez si vous souhaitez supprimer un fichier ou un dossier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File] / [!UICONTROL File ID] / [!UICONTROL File Path]</td>
   <td> <p>Si vous avez sélectionné [!UICONTROL Enter Manually], saisissez ou mappez l’identifiant ou le chemin d’accès du fichier que vous souhaitez supprimer.</p> <p>Si vous avez sélectionné [!UICONTROL Select] dans la liste, sélectionnez le fichier que vous souhaitez supprimer.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Télécharger un fichier]

Ce module d’action télécharge le fichier spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour savoir comment connecter votre compte [!DNL OneDrive] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (File ID &amp; File Path)]</td> 
   <td>Indiquez si vous souhaitez identifier le fichier par ID de fichier ou par chemin d’accès au fichier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Saisissez un ID de fichier ou un chemin d’accès au fichier.</td> 
   <td> <p>Sélectionnez le mode de saisie de l’ID de fichier ou du chemin d’accès au fichier :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>Sélectionnez cette option si vous souhaitez saisir directement l’ID ou le chemin d’accès du fichier, ou si vous souhaitez le mapper à partir d’un module précédent.</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>Sélectionnez cette option si vous souhaitez effectuer une sélection dans une liste de fichiers ou de chemins d’accès disponibles. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] location]</td> 
   <td> <p>Sélectionnez l’emplacement contenant le fichier à télécharger :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Indiquez si le module doit pouvoir saisir un identifiant de lecteur.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Saisissez l’ID du lecteur contenant le fichier que vous souhaitez télécharger.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Sélectionnez le site SharePoint contenant le fichier que vous souhaitez télécharger. Les sites disponibles sont des sites suivis par la personne connectée.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>Sélectionnez le groupe dont le lecteur contient le fichier que vous souhaitez télécharger.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>Sélectionnez ou mappez le lecteur contenant le fichier que vous souhaitez télécharger. Ce champ n’est pas disponible si vous avez sélectionné [!UICONTROL No] dans le champ [!UICONTROL Enable to Enter a Drive ID].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File] / [!UICONTROL File ID] / [!UICONTROL File Path]</td>
   <td> <p>Si vous avez sélectionné [!UICONTROL Enter Manually], saisissez ou mappez l’ID ou le chemin d’accès au fichier à télécharger.</p> <p>Si vous avez sélectionné [!UICONTROL Select from the list], sélectionnez le fichier à télécharger.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Convert to PDF]</td> 
   <td> <p>Activez cette option pour convertir le fichier en PDF. Vous pouvez effectuer une conversion à partir des types de fichiers suivants :</p> 
    <table style="table-layout:auto"> 
     <col> 
     <col> 
     <col> 
     <tbody> 
      <tr> 
       <td> 
        <ul> 
         <li> <p> <p>CSV</p> </p> </li> 
         <li> <p> <p>DOC</p> </p> </li> 
         <li> <p> <p>DOCX</p> </p> </li> 
         <li> <p> <p>ODP</p> </p> </li> 
         <li> <p> <p>ODS</p> </p> </li> 
         <li> <p> <p>ODT</p> </p> </li> 
        </ul> </td> 
       <td> 
        <ul> 
         <li> <p> <p>POT</p> </p> </li> 
         <li> <p> <p>POTM</p> </p> </li> 
         <li> <p> <p>POTX</p> </p> </li> 
         <li> <p> <p>PPS</p> </p> </li> 
         <li> <p> <p>PPSX</p> </p> </li> 
         <li> <p> <p>PPSXM</p> </p> </li> 
        </ul> </td> 
       <td> 
        <ul> 
         <li> <p>PPT</p> </li> 
         <li> <p>PPTM</p> </li> 
         <li> <p>PPTX</p> </li> 
         <li> <p>RTF</p> </li> 
         <li> <p>XLS</p> </li> 
         <li> <p>XLSX</p> </li> 
        </ul> </td> 
      </tr> 
     </tbody> 
    </table> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obtenir un fichier]

Ce module d’action récupère les métadonnées d’un fichier spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour savoir comment connecter votre compte [!DNL OneDrive] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (File ID &amp; File Path)]</td> 
   <td>Indiquez si vous souhaitez identifier le fichier par ID de fichier ou par chemin d’accès au fichier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a File ID] / [!UICONTROL File Path]</td> 
   <td> <p>Sélectionnez le mode de saisie de l’ID de fichier ou du chemin d’accès au fichier :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>Sélectionnez cette option si vous souhaitez saisir directement l’ID ou le chemin d’accès du fichier, ou si vous souhaitez le mapper à partir d’un module précédent.</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>Sélectionnez cette option si vous souhaitez effectuer une sélection dans une liste de fichiers ou de chemins d’accès disponibles. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] location]</td> 
   <td> <p>Sélectionnez l’emplacement devant faire l’objet de la recherche :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Indiquez si le module doit pouvoir saisir un identifiant de lecteur.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Saisissez l’ID du lecteur contenant le fichier que vous souhaitez obtenir.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Sélectionnez le site SharePoint qui contient le fichier que vous souhaitez obtenir. Les sites disponibles sont des sites suivis par la personne connectée.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>Sélectionnez le groupe dont le lecteur contient le fichier que vous souhaitez obtenir.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>Sélectionnez ou mappez le lecteur contenant le fichier que vous souhaitez obtenir. Ce champ n’est pas disponible si vous avez sélectionné [!UICONTROL No] dans le champ [!UICONTROL Enable to Enter a Drive ID].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File] / [!UICONTROL File ID] / [!UICONTROL File Path]</td> 
   <td> <p>Si vous avez sélectionné [!UICONTROL Enter Manually], saisissez ou mappez l’ID ou le chemin d’accès au fichier que vous souhaitez obtenir.</p> <p>Si vous avez sélectionné [!UICONTROL Select from the list], sélectionnez le fichier que vous souhaitez obtenir.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obtenir un lien de partage]

Ce module d’action renvoie un lien de partage pour le fichier spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour savoir comment connecter votre compte [!DNL OneDrive] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (File ID &amp; File Path)]</td> 
   <td>Indiquez si vous souhaitez identifier le fichier par ID de fichier ou par chemin d’accès au fichier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a File ID] / [!UICONTROL File Path]</td> 
   <td> <p>Sélectionnez le mode de saisie de l’ID de fichier ou du chemin d’accès au fichier :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>Sélectionnez cette option si vous souhaitez saisir directement l’ID ou le chemin d’accès du fichier, ou si vous souhaitez le mapper à partir d’un module précédent.</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>Sélectionnez cette option si vous souhaitez effectuer une sélection dans une liste de fichiers ou de chemins d’accès disponibles. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] location]</td> 
   <td> <p>Sélectionnez l’emplacement pour lequel vous souhaitez récupérer un lien de partage :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Indiquez si le module doit pouvoir saisir un identifiant de lecteur.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Saisissez l’identifiant du lecteur contenant le fichier pour lequel vous souhaitez récupérer un lien de partage.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Sélectionnez le site SharePoint contenant le fichier pour lequel vous souhaitez récupérer un lien de partage. Les sites disponibles sont des sites suivis par la personne connectée.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>Sélectionnez le groupe dont le lecteur contient le fichier pour lequel vous souhaitez récupérer un lien de partage.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>Sélectionnez ou mappez le lecteur contenant le fichier pour lequel vous souhaitez récupérer un lien de partage. Ce champ n’est pas disponible si vous avez sélectionné [!UICONTROL No] dans le champ [!UICONTROL Enable to Enter a Drive ID].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File] / [!UICONTROL File ID] / [!UICONTROL File Path]</td> 
   <td> <p>Si vous avez sélectionné [!UICONTROL Enter Manually], saisissez ou mappez l’identifiant ou le chemin du fichier pour lequel vous souhaitez récupérer un lien de partage.</p> <p>Si vous avez sélectionné [!UICONTROL Select] dans la liste, sélectionnez le fichier pour lequel vous souhaitez récupérer un lien de partage.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Permission Type]</td> 
   <td> <p>Indiquez si vous souhaitez que les personnes disposant du lien puissent lire et écrire dans le fichier, ou le lire uniquement.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scope]</td> 
   <td>Indiquez si vous souhaitez que le fichier soit disponible pour toute personne disposant du lien ou uniquement pour les personnes membres de votre organisation disposant du lien.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Déplacer un fichier/dossier]

Ce module d’action déplace un fichier ou un dossier vers un nouvel emplacement de dossier.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour savoir comment connecter votre compte [!DNL OneDrive] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (File ID &amp; File Path)]</td> 
   <td>Indiquez si vous souhaitez identifier le fichier par ID de fichier ou par chemin d’accès au fichier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a File ID / File Path]</td> 
   <td> <p>Sélectionnez le mode de saisie de l’ID de fichier ou du chemin d’accès au fichier :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>Sélectionnez cette option si vous souhaitez saisir directement l’ID ou le chemin d’accès du fichier, ou si vous souhaitez le mapper à partir d’un module précédent.</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>Sélectionnez cette option si vous souhaitez effectuer une sélection dans une liste de fichiers ou de chemins d’accès disponibles. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] location]</td> 
   <td> <p>Sélectionnez l’emplacement contenant le fichier ou le dossier à déplacer :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Indiquez si le module doit pouvoir saisir un identifiant de lecteur.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Saisissez l’identifiant du lecteur contenant le fichier ou le dossier à déplacer.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Sélectionnez le site [!DNL SharePoint] contenant le fichier ou le dossier à déplacer. Les sites disponibles sont des sites suivis par la personne connectée.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>Sélectionnez le groupe dont le lecteur contient le fichier ou le dossier que vous souhaitez déplacer.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>Sélectionnez ou mappez le lecteur contenant le fichier ou le dossier à déplacer. Ce champ n’est pas disponible si vous avez sélectionné [!UICONTROL No] dans le champ [!UICONTROL Enable to Enter a Drive ID].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sélectionner [!UICONTROL File/Folder]</td> 
   <td>Indiquez si vous souhaitez déplacer un fichier ou un dossier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p role="rowheader">[!UICONTROL File] / [!UICONTROL File ID] / [!UICONTROL File Path]</p> <p role="rowheader">[!UICONTROL Folder] / [!UICONTROL Folder ID] / [!UICONTROL Folder Path]</p> </td> 
   <td> <p>Si vous avez sélectionné [!UICONTROL Enter Manually], saisissez ou mappez l’identifiant ou le chemin d’accès du fichier ou du dossier que vous souhaitez déplacer.</p> <p>Si vous avez sélectionné [!UICONTROL Select] dans la liste, sélectionnez le fichier ou le dossier à déplacer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a New Folder Location]</td> 
   <td> <p>Sélectionnez le mode de saisie de l’emplacement vers lequel vous souhaitez déplacer le fichier ou le dossier :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>Sélectionnez cette option si vous souhaitez saisir directement l’ID ou le chemin d’accès du fichier, ou si vous souhaitez le mapper à partir d’un module précédent.</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>Sélectionnez cette option si vous souhaitez effectuer une sélection dans une liste de fichiers ou de chemins d’accès disponibles. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] location]</td> 
   <td> <p>Sélectionnez l’emplacement où déplacer le fichier ou le dossier :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Indiquez si le module doit pouvoir saisir un identifiant de lecteur.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Saisissez l’identifiant du lecteur sur lequel vous souhaitez déplacer le fichier ou le dossier.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Sélectionnez le site [!DNL SharePoint] où vous souhaitez déplacer le fichier ou le dossier. Les sites disponibles sont des sites suivis par la personne connectée.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>Sélectionnez le groupe contenant le lecteur sur lequel vous souhaitez déplacer le fichier ou le dossier.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>Sélectionnez ou mappez le lecteur contenant le dossier vers lequel vous souhaitez déplacer le fichier ou le dossier. Ce champ n’est pas disponible si vous avez sélectionné [!UICONTROL No] dans le champ [!UICONTROL Enable to Enter a Drive ID].</p> <p>Si vous laissez ce champ vide, le fichier ou le dossier ne peut être déplacé que dans le même [!DNL OneDrive].</p> <p>Vous pouvez déplacer des fichiers et des dossiers de [!UICONTROL My Drive] vers un [!UICONTROL Site's Drive] ou un [!UICONTROL Group's Drive]. </p> <p>Vous ne pouvez déplacer des fichiers d’un [!UICONTROL Site's Drive] que vers le même lecteur du même site.</p> <p>Vous ne pouvez déplacer des fichiers d’un [!UICONTROL Group's Drive] que vers le même lecteur du même groupe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Saisissez ou mappez le dossier dans lequel vous souhaitez déplacer le fichier ou le dossier.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Rechercher dans des fichiers/dossiers]

Ce module de recherche renvoie les fichiers et les dossiers en fonction de critères que vous avez définis.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour savoir comment connecter votre compte [!DNL OneDrive] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] location]</td> 
   <td> <p>Sélectionnez l’emplacement devant faire l’objet de la recherche :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Indiquez si le module doit pouvoir saisir un identifiant de lecteur.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Saisissez l’identifiant du lecteur que le module doit rechercher.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> <p>Accédez au dossier dans lequel vous souhaitez que le module effectue la recherche. Vous pouvez également saisir une requête pour filtrer les résultats renvoyés.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Shared With Me]</b> </p> <p>Le module recherche les fichiers qui ont été partagés avec la personne propriétaire du lecteur.</p> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Sélectionnez le site [!DNL SharePoint] sur lequel vous souhaitez que le module effectue une recherche. Les sites disponibles sont des sites suivis par la personne connectée.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>Sélectionnez le groupe dont le lecteur doit faire l’objet d’une recherche par le module.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose an Item Type]</td> 
   <td> <p>Indiquez si vous souhaitez effectuer la recherche sur des fichiers, des dossiers ou les deux.</p> <p>Remarque : vous ne pouvez pas rechercher de dossiers dans un lecteur [!UICONTROL Shared With Me].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Charger un fichier]

Ce module d’action charge un fichier dans le dossier spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour savoir comment connecter votre compte [!DNL OneDrive] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Saisir (ID et chemin d’accès de l’emplacement du dossier)</td> 
   <td>Indiquez si vous souhaitez identifier le dossier cible par ID ou par chemin d’accès.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] location]</td> 
   <td> <p>Sélectionnez l’emplacement où vous souhaitez charger un fichier :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Indiquez si le module doit pouvoir saisir un identifiant de lecteur.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Sélectionnez le lecteur contenant le fichier que vous souhaitez obtenir.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Sélectionnez le Site [!DNL SharePoint] contenant le dossier dans lequel vous souhaitez charger un fichier. Les sites disponibles sont des sites suivis par la personne connectée.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>Sélectionnez le groupe dont le lecteur contient le dossier dans lequel vous souhaitez charger un fichier.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>Sélectionnez le lecteur contenant le dossier dans lequel vous souhaitez charger un fichier. Ce champ n’est pas disponible si vous avez sélectionné [!UICONTROL No] dans le champ [!UICONTROL Enable to Enter a Drive ID].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL If the File with the Same Name Exists]</td> 
   <td>Sélectionnez la procédure applicable si un fichier portant le même nom existe déjà.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Ajoutez une description au fichier chargé.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Surveiller des fichiers ou des dossiers]

Ce module de déclenchement démarre un scénario lorsqu’un fichier ou un dossier est créé ou mis à jour.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour savoir comment connecter votre compte [!DNL OneDrive] à [!DNL Workfront Fusion], voir la section <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch Files/Folders]</td> 
   <td> <p>Sélectionnez le mode de contrôle des fichiers ou des dossiers :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL By Created Time]</b> </p> <p>Contrôlez de nouveaux fichiers ou dossiers.</p> </li> 
     <li> <p><b>[!UICONTROL By Updated Time]</b> </p> <p>Contrôlez les fichiers ou dossiers existants mis à jour.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] location]</td> 
   <td> <p>Sélectionnez l’emplacement à contrôler :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>Indiquez si le module doit pouvoir saisir un identifiant de lecteur.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>Saisissez l’identifiant du lecteur que le module doit contrôler.</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> <p>Accédez au dossier que le module doit contrôler. Vous pouvez également saisir une requête pour filtrer les résultats renvoyés.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Shared With Me]</b> </p> <p>Le module surveille les fichiers qui ont été partagés avec la ou le propriétaire du lecteur.</p> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>Sélectionnez le site SharePoint que le module doit contrôler. Les sites disponibles sont des sites suivis par la personne connectée.</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>Sélectionnez le groupe dont le lecteur doit être contrôlé par le module.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose an Item Type]</td> 
   <td> <p>Indiquez si vous souhaitez contrôler les fichiers, les dossiers ou les deux.</p> <p>Remarque : vous ne pouvez pas contrôler des dossiers dans un lecteur [!UICONTROL Shared With Me].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>



### Autre

#### [!UICONTROL Effectuer un appel API]

Ce module effectue un appel API personnalisé.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour les instructions concernant la connexion de votre compte [!DNL OneDrive] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Saisissez un chemin relatif à <code>https://graph.microsoft.com</code>. Exemple :<code> /v1.0/me/drive/root/children</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion ajoute les en-têtes d’autorisation pour vous.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Ajoutez la requête pour l’appel API sous la forme d’un objet JSON standard.</p> <p>Par exemple : <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre JSON, mettez les guillemets à l’extérieur de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>



## En cas d’impossibilité à charger ou à mettre à jour un fichier

Plusieurs problèmes peuvent se produire lors de l’échec du chargement ou de la mise à jour d’un fichier :

* Le fichier chargé est trop volumineux et dépasse la taille maximale autorisée par votre formule [!DNL OneDrive] ou vous avez utilisé l’ensemble du quota de stockage de votre compte [!DNL OneDrive]. Pour obtenir plus d’espace de stockage, supprimez les fichiers existants de [!DNL OneDrive] ou mettez à niveau votre compte [!DNL OneDrive].
* OneDrive ne permet pas de charger deux fichiers portant le même nom dans un dossier. Si le dossier cible contient un fichier portant le même nom que le fichier en cours de chargement, l’exécution du scénario débouche sur une erreur. La solution consiste à simplement renommer le fichier en cours de chargement. Si vous souhaitez mettre à jour un fichier, utilisez l’action [!UICONTROL Mettre à jour un fichier].
* Le dossier précédemment sélectionné, vers lequel le fichier est chargé, n’existe plus. Le scénario s’arrête et vous devez sélectionner à nouveau le dossier cible.
