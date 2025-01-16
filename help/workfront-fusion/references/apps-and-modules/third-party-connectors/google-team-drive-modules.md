---
title: Modules Google Team Drive
description: Les modules  [!DNL Adobe Workfront Fusion Google Team Drive]  vous permettent de contrôler, télécharger, mettre à jour, copier, supprimer ou récupérer des fichiers et de créer des dossiers dans votre  [!DNL Google Shared]  Drive.
author: Becky
feature: Workfront Fusion
exl-id: 95dd9d23-1df9-40da-8fd0-646cc697bfc8
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1059'
ht-degree: 74%

---

# Modules [!DNL Google Team Drive]

Les modules [!DNL Adobe Workfront Fusion] [!DNL Google Team Drive] vous permettent de contrôler, télécharger, mettre à jour, copier, supprimer ou récupérer des fichiers et de créer des dossiers sur votre [!DNL Google Shared Drive].

Afin d’utiliser [!DNL Google Team Drive] avec [!DNL Adobe Workfront Fusion], il est nécessaire d’avoir un compte [!DNL Google Workspace]. Si vous n’en avez pas, vous pouvez créer un compte [!DNL Google Workspace] sur le [[!DNL Google Workspace] site d’inscription](https://workspace.google.com/business/signup/welcome).

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!DNL Google Team Drive] et le connecter à plusieurs applications et services tiers.

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

Pour utiliser les modules [!DNL Google Team Drive], vous devez disposer d’un [!DNL Google Team Drive].

## Modules [!DNL Google Team Drive] et leurs champs

Lorsque vous configurez les modules [!DNL Google Team Drive], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Google Team Drive] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Les champs de dialogue du module qui sont affichés en **gras** (dans le scénario [!DNL Workfront Fusion], **et non** dans cet article de documentation) sont obligatoires.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Déclencheurs

#### [!UICONTROL Watch Files]

Renvoie les détails du fichier lorsqu’un nouveau fichier est ajouté et/ou modifié dans le dossier spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Team Drive] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Team Drive]</td> 
   <td> <p> Sélectionnez le lecteur partagé que vous souhaitez surveiller.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Sélectionnez le dossier dans le lecteur partagé.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL What files to watch]</td> 
   <td> <p> Sélectionnez le type de fichiers à surveiller.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Documents] fichiers à formater] </td> 
   <td> <p>Sélectionnez le format dans lequel vous souhaitez que les fichiers [!DNL Google Documents] visionnés soient convertis.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Sheets] fichiers à formater] </td> 
   <td> <p>Sélectionnez le format dans lequel vous souhaitez que les fichiers [!DNL Google Sheets] visionnés soient convertis.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Slides] fichiers à formater] </td> 
   <td> <p>Sélectionnez le format dans lequel vous souhaitez que les fichiers [!DNL Google Slides] visionnés soient convertis.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Drawings] fichiers à formater] </td> 
   <td> <p>Sélectionnez le format dans lequel vous souhaitez que les fichiers [!DNL Google Drawings] visionnés soient convertis.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td> <p> Indiquez si vous souhaitez surveiller les fichiers nouveaux et modifiés dans le dossier ou uniquement les nouveaux fichiers.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of downloaded files]</td> 
   <td> <p> Définissez le nombre maximum de fichiers que [!DNL Workfront Fusion] renverra au cours d’un cycle d’exécution.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [[!UICONTROL Upload a File]](#upload-a-file)
* [[!UICONTROL Update a File]](#update-a-file)
* [[!UICONTROL Copy a File]](#copy-a-file)
* [[!UICONTROL Delete a File]](#delete-a-file)
* [[!UICONTROL Move a File to Trash]](#move-a-file-to-trash)
* [[!UICONTROL Get a File]](#get-a-file)
* [[!UICONTROL Get a File List]](#get-a-file-list)
* [[!UICONTROL Create a Folder]](#create-a-folder)

#### [!UICONTROL Upload a File]

Charge un fichier vers le lecteur partagé spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Team Drive] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Team Drive] </td> 
   <td> <p>Sélectionnez le lecteur partagé vers lequel vous souhaitez charger un fichier.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Sélectionnez le dossier dans le lecteur partagé.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Source File]</p> </td> 
   <td> <p>Indiquez le fichier que vous souhaitez charger sur le lecteur partagé.</p> <p>Mappez le fichier que vous souhaitez charger à partir du module précédent (par exemple [!UICONTROL HTTP] &gt;[!UICONTROL Get a File] ou [!UICONTROL Dropbox] &gt;[!UICONTROL Get a file)], ou saisissez manuellement le nom et les données du fichier.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Title]</td> 
   <td> <p> Saisissez le titre du fichier qui sera affiché dans le dossier partagé.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert a File]</td> 
   <td> <p> Activez cette option pour convertir le fichier au format Google correspondant dans votre dossier partagé.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a File]

Permet de modifier le nom et/ou le contenu du fichier.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Team Drive] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Team Drive]</td> 
   <td> <p> Sélectionnez le lecteur partagé qui contient le fichier à mettre à jour.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Sélectionnez le dossier dans le lecteur partagé.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td> <p> Saisissez (mappez) l’identifiant du fichier que vous souhaitez mettre à jour.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Source File]</p> </td> 
   <td>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Title] </td> 
   <td> <p>Saisissez le nouveau titre du fichier mis à jour.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert a File]</td> 
   <td> <p> Activez cette option pour convertir le fichier au format [!DNL Google] correspondant dans votre dossier partagé.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Copy a File]

Copie un fichier spécifié vers le dossier sélectionné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Team Drive] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Team Drive]</td> 
   <td> <p> Sélectionnez le lecteur partagé qui contient le fichier à copier.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Sélectionnez le dossier cible vers lequel vous souhaitez copier le fichier.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td> <p> Saisissez (mappez) l’ID du fichier que vous souhaitez copier.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL The name of the copy file]</p> </td> 
   <td> <p>Saisissez le nouveau nom du fichier si vous souhaitez qu’il soit modifié dans l’emplacement cible.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a File]

Supprime un fichier spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Team Drive] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td> <p> Saisissez ou mappez l’ID du fichier que vous souhaitez supprimer.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a File to Trash]

Déplace le fichier spécifié vers la corbeille.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Team Drive] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td> <p> Saisissez ou mappez l’ID du fichier que vous souhaitez déplacer vers la corbeille.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a File]

Récupère les détails du fichier spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Team Drive] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Documents] fichiers à formater] </td> 
   <td> <p>Sélectionnez le format dans lequel vous souhaitez que les fichiers [!DNL Google Documents] soient convertis.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Sheets] fichiers à formater] </td> 
   <td> <p>Sélectionnez le format dans lequel vous souhaitez que les fichiers [!DNL Google Sheets] soient convertis.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Slides] fichiers à formater] </td> 
   <td> <p>Sélectionnez le format dans lequel vous souhaitez que les fichiers [!DNL Google Slides] soient convertis.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Drawings] fichiers à formater] </td> 
   <td> <p>Sélectionnez le format dans lequel vous souhaitez que les fichiers [!DNL Google Drawings] soient convertis.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td> <p> Saisissez ou mappez l’ID du fichier que vous souhaitez récupérer.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a File List]

Récupère les détails des fichiers et/ou des dossiers en fonction du terme de recherche.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Team Drive] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Team Drive]</td> 
   <td> <p> Sélectionnez le lecteur partagé à partir duquel vous souhaitez répertorier les fichiers.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Sélectionnez le dossier dans lequel vous souhaitez répertorier les fichiers.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>Sélectionnez le type de recherche que vous souhaitez effectuer - voir ci-dessous.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Query]</p> </td> 
   <td> 
    <ul> 
     <li style="font-weight: bold;"> <p>[!UICONTROL Search within file names]</p> <p style="font-weight: normal;">Saisissez le nom du fichier (y compris son extension) lorsque l’option [!UICONTROL Search for exact term Search] est sélectionnée ou saisissez la partie du nom lorsque l’option [!UICONTROL Search for names containing the searched term] est sélectionnée.</p> </li> 
     <li> <p style="font-weight: bold;">[!UICONTROL Fulltext search]</p> <p>Saisissez le terme de recherche pour effectuer une recherche parmi les noms, les descriptions et le contenu des fichiers.</p> </li> 
     <li> <p style="font-weight: bold;">[!UICONTROL Custom search query]</p> <p>Saisissez le terme de recherche de requête [!DNL Google]. Pour plus de détails, veuillez consulter la <a href="https://developers.google.com/drive/api/v2/ref-search-terms">documentation de recherche de requête</a> de [!DNL Google]. Exemple : <code>fullText contains '"Hello world"'</code></p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Retrieve]</td> 
   <td>Sélectionnez si vous souhaitez récupérer des fichiers, des dossiers ou les deux.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned results]</td> 
   <td> <p> Définissez le nombre maximum de fichiers ou de dossiers que [!DNL Workfront Fusion] renverra au cours d’un cycle d’exécution.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Folder]

Crée un nouveau dossier.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Team Drive] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Team Drive]</td> 
   <td> <p> Sélectionnez le lecteur partagé sur lequel vous souhaitez créer un dossier.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Sélectionnez le dossier dans lequel vous souhaitez créer un dossier.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL The name of the new folder]</td> 
   <td> <p> Saisissez le nom du nouveau dossier.</p> </td> 
  </tr> 
 </tbody> 
</table>
