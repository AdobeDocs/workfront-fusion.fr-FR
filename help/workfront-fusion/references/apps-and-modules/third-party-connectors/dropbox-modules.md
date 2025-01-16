---
title: Modules Dropbox
description: Dans un scénario  [!DNL Adobe Workfront Fusion] , vous pouvez automatiser les workflows qui utilisent Dropbox et le connecter à plusieurs applications et services tiers. Cela vous permet d’automatiser des activités telles que la surveillance, la recherche, la récupération, la mise en liste, la création et la modification de fichiers et de dossiers dans votre Dropbox.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 29ce5940-4d71-4719-ab5e-f03c44b28c8c
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '2869'
ht-degree: 88%

---

# Modules [!DNL Dropbox]

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!UICONTROL Dropbox] ou [!DNL Dropbox Business], et les connecter à plusieurs applications et services tiers. Vous pouvez ainsi automatiser des activités telles que la surveillance, la recherche, la récupération, la mise en liste, la création et la modification de fichiers et de dossiers dans votre [!UICONTROL Dropbox].

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

## Conditions préalables

* Pour utiliser des modules [!DNL Dropbox], vous devez disposer d’un compte [!DNL Dropbox].

>[!IMPORTANT]
>
>Dropbox doit approuver les demandes comptant plus de 50 utilisateurs et utilisatrices.
>
>Pour plus d’informations, recherchez « Production approval » dans le guide de développement de Dropbox.

## Informations sur l’API Dropbox

Le connecteur de Dropbox utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td> https://api.dropboxapi.com/2    </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Version de l’API</td> 
   <td> 2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td><ul><li><p>Dropbox</p><p>v5.3.9</p></li><li><p>Dropbox Business</p><p>v1.0.12</p></li></ul></td> 
  </tr>
 </tbody> 
 </table>


## Créer une connexion à [!DNL Dropbox]

Pour créer une connexion pour vos modules [!DNL Dropbox], procédez comme suit :

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
        <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>Indiquez si cette connexion est destinée à un environnement de production ou hors production.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>Indiquez si vous vous connectez à un compte de service ou à un compte personnel.</td>
        </tr>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Saisissez votre [!UICONTROL Client ID] de [!UICONTROL Dropbox]. </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Saisissez votre [!UICONTROL Client Secret] de [!DNL Dropbox]. </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Account Type]</td>
        <td>Choisissez si vous vous connectez à un compte personnel Dropbox ou à un compte professionnel (Dropbox Business).</td>
        </tr>
      </tbody>
    </table>

1. Cliquez sur **[!UICONTROL Continue]** pour enregistrer la connexion et revenir au module .## Modules [!DNL Dropbox] et leurs champs

## Modules [!DNL Dropbox] et leurs champs

Lorsque vous configurez les modules [!DNL Dropbox], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Dropbox] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Modules déclencheurs](#trigger-modules)
* [Modules pour l’obtention de fichiers et de dossiers  [!DNL Dropbox] ](#modules-for-getting-dropbox-files-and-folders)
* [Modules pour la création et la modification de fichiers et de données  [!DNL Dropbox] ](#modules-for-creating-and-editing-dropbox-files-and-folders)
* [Autres modules](#other-modules)

### Modules déclencheurs

#### [!UICONTROL Watch Files]

Ce module de type Déclencheur renvoie les détails du fichier lorsque le fichier d’un dossier spécifié est modifié.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Dropbox] à [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-dropbox" class="MCXref xref">Créer une connexion à [!DNL Dropbox]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Sélectionnez le dossier où vous souhaitez surveiller les modifications.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch also subfolders]</td> 
   <td> <p> Activez cette option pour surveiller également les fichiers modifiés dans les sous-dossiers du dossier sélectionné.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit] </td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Modules pour l’obtention de fichiers et de dossiers [!DNL Dropbox]

* [[!UICONTROL Search Files/Folders]](#search-filesfolders)
* [[!UICONTROL Download a File]](#download-a-file)
* [[!UICONTROL Get a Folder Metadata]](#get-a-folder-metadata)
* [[!UICONTROL List All Files/Subfolders in a Folder]](#list-all-filessubfolders-in-a-folder)
* [[!UICONTROL List File Revisions]](#list-file-revisions)

#### [!UICONTROL Search Files/Folders]

Ce module de recherche recherche les enregistrements dans un objet dans [!DNL Dropbox] qui correspondent à la requête que vous avez spécifiée.

Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Dropbox] à [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-dropbox" class="MCXref xref">Créer une connexion à [!DNL Dropbox]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>Saisissez le terme de recherche.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Sélectionnez le dossier où vous souhaitez rechercher. Ce module recherche l’intégralité de [!DNL Dropbox] si vous ne sélectionnez pas de dossier.</p> </td> 
  </tr> 
  <tr> 
   <td>Statut du fichier</td> 
   <td> <p> Sélectionnez le statut du fichier pour limiter la recherche au statut du fichier sélectionné.</p> </td> 
  </tr> 
  <tr> 
   <td>Catégories de fichiers</td> 
   <td> <p> Sélectionnez les catégories de fichiers pour limiter la recherche aux catégories sélectionnées.</p> </td> 
  </tr> 
  <tr> 
   <td>Extensions de fichiers</td> 
   <td> <p> Sélectionnez les extensions de fichiers à rechercher.</p> </td> 
  </tr> 
  <tr> 
   <td>Limite </td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download a File]

Ce module d’action télécharge un fichier à partir d’un dossier.

Vous spécifiez le fichier et son emplacement.

Le module renvoie l’ID du fichier et tous les champs associés, ainsi que les valeurs et les champs personnalisés auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

>[!NOTE]
>
>Ce module est utile pour fournir des fichiers aux modules suivants.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Dropbox] à [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-dropbox" class="MCXref xref">Créer une connexion à [!DNL Dropbox]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>Sélection des fichiers</td> 
   <td> <p> Choisissez si vous souhaitez mapper le chemin du fichier ou sélectionnez le fichier manuellement.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Chemin du fichier / Fichier</p> </td> 
   <td> <p style="font-weight: bold;">Chemin du fichier</p> <p>Saisissez ou mappez le chemin cible sur le fichier.</p> <p style="font-weight: bold;">Fichier</p> <p>Sélectionnez le fichier dans le menu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Folder Metadata]

Ce module d’action récupère les détails d’un dossier partagé.

Vous spécifiez l’ID du dossier.

Le module renvoie l’ID du dossier et de tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Dropbox] à [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-dropbox" class="MCXref xref">Créer une connexion à [!DNL Dropbox]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>Identifiant de dossier partagé</td> 
   <td> <p> Saisissez ou mappez l’ID du dossier dont vous souhaitez récupérer les détails.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List All Files/Subfolders in a Folder]

Ce module d’action répertorie les fichiers ou les dossiers d’un dossier spécifique.

Vous spécifiez l’ID du dossier.

Le module renvoie les ID des fichiers ou dossiers et tous les champs associés, ainsi que les valeurs et les champs personnalisés auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre application [!DNL Dropbox] à [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-dropbox" class="MCXref xref">Créer une connexion à [!DNL Dropbox]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>Liste </td> 
   <td> <p>Indiquez si vous souhaitez récupérer des fichiers ou des dossiers.</p> </td> 
  </tr> 
  <tr> 
   <td>Afficher uniquement les fichiers téléchargeables</td> 
   <td> <p> Activez cette option pour ne renvoyer que les fichiers téléchargeables. Certains types de fichiers, tels que les documents Google, ne sont pas téléchargeables.</p> </td> 
  </tr> 
  <tr> 
   <td>Dossier </td> 
   <td> <p>Saisissez ou mappez le dossier à partir duquel vous souhaitez récupérer des fichiers ou des dossiers.</p> </td> 
  </tr> 
  <tr> 
   <td>Limite </td> 
   <td> <p>Saisissez ou mappez le nombre maximal d’enregistrements que le module doit lister pour chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List File Revisions]

Ce module d’action récupère toutes les révisions de fichier (un historique de version) d’un fichier particulier.\
Vous spécifiez l’identifiant du fichier.

Le module renvoie tous les champs standard associés à l’enregistrement, ainsi que tous les champs et valeurs personnalisés auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Dropbox] à [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-dropbox" class="MCXref xref">Créer une connexion à [!DNL Dropbox]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>Sélection des fichiers</td> 
   <td> <p> Choisissez si vous souhaitez mapper le chemin du fichier ou sélectionnez le fichier manuellement.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Chemin du fichier / Fichier</p> </td> 
   <td> <p style="font-weight: bold;">Chemin du fichier</p> <p>Saisissez ou mappez le chemin cible sur le fichier.</p> <p style="font-weight: bold;">Fichier</p> <p>Sélectionnez le fichier dans le menu.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Limite</p> </td> 
   <td> <p>Saisissez ou mappez le nombre maximal d’enregistrements que le module doit lister pour chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Modules pour la création et la modification de fichiers et de dossiers [!DNL Dropbox]

* [[!UICONTROL Upload] un fichier](#upload-a-file)
* [[!UICONTROL Create a Folder]](#create-a-folder)
* [[!UICONTROL Create/Overwrite a Text File]](#createoverwrite-a-text-file)
* [[!UICONTROL Create/Update a Share Link]](#createupdate-a-share-link)
* [[!UICONTROL Restore a File]](#restore-a-file)
* [[!UICONTROL Move a File/Folder]](#move-a-filefolder)
* [[!UICONTROL Rename a File/Folder]](#rename-a-filefolder)
* [[!UICONTROL Delete a File/Folder]](#delete-a-filefolder)

#### [!UICONTROL Upload a File]

Ce module d’action charge un fichier dans un dossier.

Vous spécifiez des informations telles que l’emplacement du document, le fichier à charger et éventuellement un nouveau nom pour le fichier.

Le module renvoie l’ID du fichier et tous les champs associés, ainsi que les valeurs et les champs personnalisés auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Dropbox] à [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-dropbox" class="MCXref xref">Créer une connexion à [!DNL Dropbox]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder]</td> 
   <td> <p> Sélectionnez le dossier de votre [!DNL Dropbox] dans lequel vous souhaitez charger le fichier.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Source File]</p> </td> 
   <td> <p>Saisissez ou mappez le fichier que vous souhaitez ajouter au dossier [!DNL Dropbox] sélectionné ci-dessus.</p> <p style="font-weight: bold;">[!UICONTROL File name]</p> <p>Saisissez ou mappez le nom du fichier, y compris son extension.</p> <p style="font-weight: bold;">[!UICONTROL File data]</p> <p>Saisissez ou mappez les données du fichier (provenant du module précédent, par exemple [!UICONTROL Google Drive] &gt; [!UICONTROL Get a File)].</p> <p>Remarque : la taille maximale du fichier chargé est de 150 Mo.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Overwrite an existing file]</td> 
   <td> <p> Activez cette option pour remplacer le fichier existant par le nouveau fichier. Si cette option est désactivée, le fichier chargé est renommé.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Folder]

Ce module d’action crée un dossier.

Vous spécifiez le chemin et un nom pour le dossier.

Le module renvoie l’ID du dossier et tous les champs associés, ainsi que les valeurs et les champs personnalisés auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Dropbox] à [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-dropbox" class="MCXref xref">Créer une connexion à [!DNL Dropbox]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder Name] </td> 
   <td> <p>Saisissez le nom du nouveau dossier.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Folder]</p> </td> 
   <td> <p>Saisissez ou mappez le chemin où vous souhaitez créer un dossier.</p> <p>Note :   <p>Si vous utilisez un compte [!DNL Dropbox Business] (avec espaces d’équipe), vous devez supprimer la barre oblique <code>/</code>, ou ne cliquez pas sur <strong>[!UICONTROL Click here] pour choisir un dossier</strong> pour créer un dossier d’équipe à la racine.</p> <p>Si la barre oblique n’est pas supprimée, une erreur <code>[409] path/malformed_path/..</code> est renvoyée.</p> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Auto rename]</td> 
   <td> <p> Activez cette option pour renommer le nouveau dossier si un dossier portant le même nom existe déjà à l’emplacement cible.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create/Overwrite a Text File]

Ce module d’action crée un fichier DOC ou remplace le contenu d’un fichier existant.

Vous spécifiez le fichier source et le dossier.

Le module renvoie l’ID du dossier et tous les champs associés, ainsi que les valeurs et les champs personnalisés auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Dropbox] à [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-dropbox" class="MCXref xref">Créer une connexion à [!DNL Dropbox]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Select to]</td> 
   <td> <p> Indiquez si vous souhaitez créer ou remplacer un fichier DOC.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Sélectionnez l’emplacement cible où vous souhaitez créer un fichier.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Source File]</p> </td> 
   <td> <p>Saisissez ou mappez le fichier que vous souhaitez ajouter au dossier [!DNL Dropbox].</p> <p style="font-weight: bold;">Nom du fichier</p> <p>Saisissez le nom du nouveau fichier DOC (sans extension).</p> <p style="font-weight: bold;">Contenu du fichier</p> <p>Saisissez le contenu textuel du fichier DOC.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create/Update a Share Link]

Ce module d’action crée un lien public vers un fichier.

Vous spécifiez le fichier et des informations sur le lien.

Le module renvoie l’ID du lien et tous les champs associés, ainsi que les valeurs et les champs personnalisés auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Dropbox] à [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-dropbox" class="MCXref xref">Créer une connexion à [!DNL Dropbox]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Way of selecting files]</td> 
   <td> <p> Indiquez si vous souhaitez mapper ou saisir le chemin du fichier, ou sélectionnez le fichier manuellement.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL File Path / File]</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL File Path]</p> <p>Saisissez ou mappez le chemin cible sur le fichier.</p> <p style="font-weight: bold;">[!UICONTROL File]</p> <p>Sélectionnez le fichier dans le menu.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Requested Visibility]</p> </td> 
   <td> <p>Indiquez si le lien est public, pour l’équipe ou restreint par un mot de passe.</p> <p>Remarque : les options [!UICONTROL Team only] et [!UICONTROL Access with password] ne sont disponibles que pour les utilisateurs disposant d’une version [!DNL Dropbox Pro] ou supérieure.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Link's Expiration Date]</td> 
   <td> <p> Saisissez la date et l’heure d’expiration du lien, il ne sera alors plus accessible. Si ce champ n’est pas renseigné, le lien n’expire pas. Pour consulter une liste des formats de date et d’heure pris en charge, voir la section <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Coercition de type dans [!DNL Adobe Workfront Fusion]</a>.</p> <p>Remarque : les options [!UICONTROL Team only] et [!UICONTROL Access with password] ne sont disponibles que pour les utilisateurs disposant de versions [!UICONTROL Dropbox Pro] ou supérieures.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Link's Access Level]</p> </td> 
   <td> <p>Définissez l’autorisation de la personne destinataire du lien.</p> <p><strong>[!UICONTROL Viewer]</strong> Les utilisateurs et utilisatrices qui utilisent le lien peuvent afficher le contenu et le commenter.</p> <p><strong>[!UICONTROL Editor]</strong> Les utilisateurs et utilisatrices qui utilisent le lien peuvent modifier, afficher et commenter le contenu.</p> <p><strong>[!UICONTROL Max]</strong> Les utilisateurs et utilisatrices qui utilisent le lien reçoivent le niveau d’accès maximal auquel vous pouvez définir le lien.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Restore a File]

Ce module d’action restaure une version précédente d’un fichier.

Vous spécifiez le fichier et le numéro de la révision que vous souhaitez.

Le module renvoie l’identifiant de la version et de tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Dropbox] à [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-dropbox" class="MCXref xref">Créer une connexion à [!DNL Dropbox]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Way of selecting files]</td> 
   <td> <p> Indiquez si vous souhaitez mapper ou saisir le chemin du fichier, ou sélectionnez le fichier manuellement.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL File Path] / [!UICONTROL File]</p> </td> 
   <td> <p><strong>[!UICONTROL File Path]</strong> </p> <p>Saisissez ou mappez le chemin cible sur le fichier.</p> <p><strong>[!UICONTROL File]</strong> </p> <p>Sélectionnez le fichier dans le menu.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Revision]</p> </td> 
   <td> <p>Saisissez ou mappez le numéro de révision de la révision que vous souhaitez restaurer.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a File/Folder]

Ce module d’action déplace un fichier ou un dossier vers un autre emplacement.

Vous spécifiez le fichier ou le dossier, ainsi que la méthode et l’emplacement de son déplacement.

Le module renvoie l’ID du fichier ou du dossier et tous les champs associés, ainsi que les valeurs et les champs personnalisés auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Dropbox] à [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-dropbox" class="MCXref xref">Créer une connexion à [!DNL Dropbox]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Way of selecting files] </td> 
   <td> <p>Indiquez si vous souhaitez mapper ou saisir le chemin du fichier, ou sélectionnez le fichier manuellement.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL File/Folder Path] / [!UICONTROL File/Folder]</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL File/Folder Path]</p> <p>Saisissez ou mappez le chemin cible vers le fichier ou le dossier.</p> <p style="font-weight: bold;">[!UICONTROL File/Folder]</p> <p>Sélectionnez le fichier ou le dossier dans le menu.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL To Folder]</p> </td> 
   <td> <p>Saisissez ou mappez l’emplacement cible du fichier ou du dossier.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL New Name]</p> </td> 
   <td> <p>Saisissez le nouveau nom du fichier ou du dossier dans le nouvel emplacement.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Auto Rename]</p> </td> 
   <td> <p>Activez cette option pour vous assurer que si un fichier ou un dossier portant le même nom existe déjà, le module renomme le nouveau fichier ou dossier en ajoutant ([!UICONTROL NUMBER]) après le nom du fichier ou du dossier. Sinon, le fichier ou le dossier de l’emplacement cible est remplacé.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Allow ownership transfer]</p> </td> 
   <td> <p>Activez cette option pour permettre les déplacements par la personne propriétaire, même si cela entraîne un transfert de propriété pour le contenu déplacé.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Rename a File/Folder]

Ce module d’action renomme un fichier ou un dossier.

Indiquez le fichier ou le dossier et le nouveau nom.

Le module renvoie l’ID du fichier ou du dossier et tous les champs associés, ainsi que les valeurs et les champs personnalisés auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Dropbox] à [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-dropbox" class="MCXref xref">Créer une connexion à [!DNL Dropbox]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>Sélection des fichiers</td> 
   <td> <p> Indiquez si vous souhaitez mapper ou saisir le chemin du fichier, ou sélectionnez le fichier manuellement.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Chemin d’accès au fichier/dossier/Fichier/Dossier</p> </td> 
   <td> <p style="font-weight: bold;">Chemin d’accès au fichier/dossier</p> <p>Saisissez ou mappez le chemin cible vers le fichier ou le dossier.</p> <p style="font-weight: bold;">Fichier ou dossier</p> <p>Sélectionnez le fichier ou le dossier dans le menu.</p> </td> 
  </tr> 
  <tr> 
   <td>Renommer </td> 
   <td> <p>Saisissez le [!UICONTROL target name] du fichier, y compris son extension.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a File/Folder]

Ce module d’action supprime un fichier ou un dossier.

Vous spécifiez le fichier ou le dossier.

Le module renvoie l’ID de l’enregistrement et tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Dropbox] à [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-dropbox" class="MCXref xref">Créer une connexion à [!DNL Dropbox]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Way of selecting files]</td> 
   <td> <p> Indiquez si vous souhaitez mapper ou saisir le chemin du fichier, ou sélectionnez le fichier manuellement.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL File Path] / [!UICONTROL File]</p> </td> 
   <td> <p style="font-weight: bold;">[!UICONTROL File Path]</p> <p>Saisissez ou mappez le chemin cible sur le fichier.</p> <p style="font-weight: bold;">[!UICONTROL File]</p> <p>Sélectionnez le fichier dans le menu.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Autres modules

#### [!UICONTROL Make an API Call]

Ce module d’action vous permet d’effectuer un appel personnalisé et authentifié à l’API [!DNL Dropbox]. Cela vous permet de créer une automatisation du flux de données qui ne peut pas être réalisée par les autres modules [!DNL Dropbox].

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Dropbox] à [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-dropbox" class="MCXref xref">Créer une connexion à [!DNL Dropbox]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Saisissez un chemin relatif à <code>https://api.dropboxapi.com</code>. Par exemple, <code>/2/files/list_folder</code></p> <p>Pour obtenir la liste des points d’entrée disponibles, voir la <a href="https://www.dropbox.com/developers/documentation/http/documentation">Documentation de l’API Dropbox v2</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP dans [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Headers] </td> 
   <td> <p>Saisissez les en-têtes de requête de votre choix. [!DNL Workfront Fusion] ajoute automatiquement des en-têtes d’autorisation.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query String]</td> 
   <td> <p> Saisissez la chaîne de requête.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Body] </td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :   <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre JSON, mettez les guillemets à l’extérieur de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Exemple :** l’appel API suivant renvoie le 10 premiers fichiers du dossier [!DNL /Text files] de votre compte [!DNL Dropbox] :
>
>URL : `/2/files/list_folder`
>
>Corps :
> 
>`{`
>
>`"path": "/Text files",`
>
>`"limit": 10,`
>
>`"recursive": false,`
>
>`"include_deleted": false`
>
>`}`
>
>Les correspondances de la recherche se trouvent dans la sortie du module sous [!UICONTROL Bundle] > [!UICONTROL Body] > entrées.
>
>Dans notre exemple, 10 tickets ont été renvoyés :

## Problèmes courants

* [Impossible de charger ou de mettre à jour un fichier](#unable-to-upload-or-update-a-file)
* [L’image référencée via un lien partagé n’est pas rendue.](#image-referenced-via-a-shared-link-does-not-render)

### Impossible de charger ou de mettre à jour un fichier

Il existe plusieurs situations dans lesquelles le chargement ou la mise à jour d’un fichier échoue :

* Le fichier chargé est trop volumineux et dépasse la taille de fichier maximale autorisée pour votre plan [!DNL Dropbox] ou vous avez utilisé la totalité des quotas de stockage de votre compte [!DNL Dropbox]. Vous devez supprimer des fichiers existants de votre compte [!DNL Dropbox] ou mettre à niveau votre plan.
* Le dossier précédemment sélectionné, dans lequel le fichier est chargé, n’existe plus. Le scénario s’arrête et vous devez sélectionner à nouveau le dossier cible.

### L’image référencée via un lien partagé n’est pas rendue.

L’URL renvoyée par l’[!UICONTROL Dropbox] >[!UICONTROL Create a shared link] n’est pas liée directement à une image, mais à une page [!DNL Dropbox]. Pour forcer le téléchargement de l’image, remplacez le `?dl=0` de fin par `?dl=1`. Pour forcer le rendu de l’image (par exemple, dans un navigateur web ou dans Facebook Messenger), ajoutez `&raw=1` à l’URL.

Si vous devez obtenir le lien direct ou brut de votre image pour votre site web ou pour d’autres modules [!DNL Workfront Fusion], vous devez modifier l’URL partagée initiale de la manière suivante :

URL d’origine :

`https://www.dropbox.com/s/ia8qtvs20f3a5ux/Screen%20Shot%202018-10-15%20at%204.21.11%20PM.png?dl=0`

1. Remplacez `www` par `dl`.
1. Supprimez `?dl=0`.

URL finale :

`https://dl.dropbox.com/s/ia8qtvs20f3a5ux/Screen%20Shot%202018-10-15%20at%204.21.11%20PM.png`

Pour modifier automatiquement l’URL, vous pouvez utiliser la fonction `replace()` deux fois :

* Remplacer www par dl

  ![](/help/workfront-fusion/references/apps-and-modules/assets/www-to-dl-350x32.png)

* Et pour supprimer ?dl=0

  ![](/help/workfront-fusion/references/apps-and-modules/assets/remove-dl0-350x33.png)

Pour le faire en une seule étape, combinez les fonctions suivantes :

![](/help/workfront-fusion/references/apps-and-modules/assets/replace-both-350x47.png)

Vous pouvez également la copier et la coller dans le champ. Remplacez `1.url` par l’URL.

```
{{replace(replace(1.url; "?dl=0"; ""); "www"; "dl")}}
```
