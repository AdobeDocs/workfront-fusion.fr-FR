---
title: Microsoft OneDrive pour les modules Business
description: Dans un scénario  [!DNL Adobe Workfront Fusion] , vous pouvez automatiser les workflows qui utilisent  [!DNL Microsoft OneDrive for Business]et le connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: 657bea46-064e-4333-8e86-81678bb1c3bd
source-git-commit: e1e15985db9683525250d1f9f9276224b2baf0e6
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 73%

---

# Modules [!DNL Microsoft OneDrive for Business]

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!DNL Microsoft OneDrive for Business] et le connecter à plusieurs applications et services tiers.

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

Pour utiliser [!DNL Microsoft OneDrive for Business] avec [!DNL Adobe Workfront Fusion], vous devez disposer d’un compte [!DNL Microsoft].

## Connexion du service [!DNL Microsoft OneDrive for Business] à [!DNL Workfront Fusion].

Pour savoir comment connecter votre compte [!DNL Microsoft OneDrive for Business] à [!UICONTROL Workfront Fusion], voir [Créer une connexion à [!UICONTROL Adobe Workfront Fusion] - Instructions de base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Certaines applications Microsoft utilisent la même connexion, qui est liée à des autorisations d’utilisateur ou d’utilisatrice. Ainsi, lors de la création d’une connexion, l’écran de consentement aux autorisations affiche les autorisations précédemment accordées à la connexion de cet utilisateur ou de cette utilisatrice, en plus des nouvelles autorisations nécessaires à l’application actuelle.
>
>Par exemple, si un utilisateur ou une utilisatrice dispose d’autorisations « Lire le tableau » accordées via le connecteur Excel, puis crée une connexion dans le connecteur Outlook pour lire les e-mails, l’écran de consentement aux autorisations affiche à la fois l’autorisation « Lire le tableau » déjà accordée et l’autorisation « Écrire des e-mails » nouvellement requise.

## Modules [!DNL Microsoft OneDrive for Business] et leurs champs

Lorsque vous configurez les modules [!DNL Microsoft OneDrive for Business], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Microsoft OneDrive for Business] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Déclencheurs](#triggers)
* [Actions](#actions)

### Déclencheurs

* [[!UICONTROL Watch files]](#watch-files)
* [[!UICONTROL Watch folders]](#watch-folders)

#### [!UICONTROL Watch files]

Ce module déclencheur s’active lorsqu’un nouveau fichier est ajouté ou mis à jour dans un dossier surveillé.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Drive ID]</p> </td> 
   <td> <p>Sélectionnez le lecteur que vous souhaitez surveiller.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p> Sélectionnez le dossier que vous souhaitez surveiller. Dans un scénario, vous ne pouvez surveiller qu’un seul dossier.</p> <p>Conseil : pour surveiller plusieurs dossiers, créez un scénario indépendant pour chacun d’eux.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL I want to watch]</p> </td> 
   <td> <p>Indiquez si vous souhaitez regarder les nouveaux fichiers et toutes les modifications, ou les nouveaux fichiers uniquement.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned rows]</td> 
   <td> <p> Définissez le nombre maximal de résultats que le module doit renvoyer au cours d’un cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch folders]

Ce module de déclenchement s’active lorsqu’un nouveau dossier est ajouté au dossier surveillé.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Drive ID]</p> </td> 
   <td> <p>Sélectionnez le lecteur que vous souhaitez surveiller.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p> Sélectionnez le dossier que vous souhaitez surveiller. Dans un scénario, vous ne pouvez surveiller qu’un seul dossier.</p> <p>Conseil : pour effectuer le suivi de plusieurs dossiers, créez un scénario indépendant pour chacun d’eux.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL I want to watch]</p> </td> 
   <td> <p>Indiquez si vous souhaitez surveiller les nouveaux dossiers et toutes les modifications, ou les nouveaux dossiers uniquement.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned rows]</td> 
   <td> <p> Définissez le nombre maximal de résultats que le module doit renvoyer au cours d’un cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [[!UICONTROL Create a folder]](#create-a-folder)
* [[!UICONTROL Delete a file]](#delete-a-file)
* [[!UICONTROL Delete a folder]](#delete-a-folder)
* [[!UICONTROL Get a file]](#get-a-file)
* [[!UICONTROL Get a sharing link]](#get-a-sharing-link)
* [[!UICONTROL Upload a file]](#upload-a-file)

#### [!UICONTROL Create a folder]

Crée un dossier à l’intérieur du dossier parent spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td><strong>[!UICONTROL Connection]</strong> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td><strong>[!UICONTROL Drive ID]</strong> </td> 
   <td> <p>Sélectionnez le lecteur sur lequel vous souhaitez créer un dossier.</p> </td> 
  </tr> 
  <tr> 
   <td><strong>[!UICONTROL Folder]</strong> </td> 
   <td> <p>Sélectionnez le dossier dans lequel vous souhaitez créer un dossier.</p> </td> 
  </tr> 
  <tr> 
   <td><strong>[!UICONTROL Folder name]</strong> </td> 
   <td>Saisissez ou mappez un nom pour le nouveau dossier.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a file]

Ce module d’action déplace le fichier spécifié vers la corbeille.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Drive ID]</td> 
   <td> <p>Sélectionnez le lecteur sur lequel vous souhaitez supprimer un fichier.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td> <p>Saisissez l’ID du fichier que vous souhaitez supprimer. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a folder]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Drive ID]</td> 
   <td> <p>Sélectionnez le lecteur sur lequel vous souhaitez supprimer un fichier.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder ID]</td> 
   <td> <p>Saisissez ou mappez l’ID du dossier à supprimer. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a file]

Ce module d’action récupère le fichier avec l’ID donné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Drive ID]</td> 
   <td> <p>Sélectionnez le lecteur à partir duquel vous souhaitez récupérer un fichier.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td> <p>Saisissez l’ID du fichier que vous souhaitez récupérer. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a sharing link]

Ce module récupère un lien que vous pouvez partager pour accorder l’accès au fichier spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Drive ID]</td> 
   <td> <p>Sélectionnez le lecteur vers lequel vous souhaitez charger un fichier.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Enter]</td> 
   <td> <p>Indiquez si vous souhaitez choisir un fichier à l’aide de l’ID du fichier ou du chemin d’accès au fichier. Saisissez l’ID du fichier ou le chemin d’accès dans le champ qui s’affiche.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permission type]</p> </td> 
   <td> <p>Sélectionnez si vous souhaitez que les personnes qui reçoivent le lien disposent d’autorisations de lecture et d’écriture ou de lecture seule.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Scope]</td> 
   <td> <p> Indiquez si vous souhaitez que le fichier soit accessible à toute personne disposant du lien ou accessible uniquement aux personnes membres de votre organisation.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file]

Ce module d’action charge un fichier binaire ou un fichier de texte dans un dossier spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Drive ID]</td> 
   <td> <p>Sélectionnez le lecteur vers lequel vous souhaitez charger un fichier.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Sélectionnez le dossier dans le lecteur.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Source File]</p> </td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL If the file with the same name exists]</td> 
   <td> <p> Sélectionnez ce que vous souhaitez faire si un fichier portant le même nom que le fichier que vous essayez de charger existe déjà.</p> 
    <ul> 
     <li>[!UICONTROL Replace the existing file]</li> 
     <li>[!UICONTROL Rename the new file]</li> 
     <li>[!UICONTROL End with an error]</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
