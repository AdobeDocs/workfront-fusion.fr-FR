---
title: Modules SharePoint
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent Microsoft SharePoint Online et les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: 1a09aa86-5e0e-4347-b4cf-2b0a95e5b049
source-git-commit: 2493ce7ccca599e30b44b62558573ce2a55b03e0
workflow-type: tm+mt
source-wordcount: '4276'
ht-degree: 52%

---

# Modules Microsoft SharePoint Online

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent Microsoft SharePoint Online et les connecter à plusieurs applications et services tiers.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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

Pour utiliser les modules Microsoft SharePoint Online, vous devez disposer d’un compte Microsoft SharePoint Online.

## Informations sur l’API SharePoint

Le connecteur SharePoint utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td> https://graph.microsoft.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Version de l’API</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.14.2</td> 
  </tr>
 </tbody> 
 </table>

## Connexion de Microsoft SharePoint Online à Workfront Fusion {#connect-microsoft-sharepoint-online-to-workfront-fusion}

* [Connexion de Microsoft SharePoint Online à Workfront Fusion à l’aide d’un compte  [!DNL Microsoft] ](#connect-microsoft-sharepoint-online-to-workfront-fusion-using-a-microsoft-account)
* [Connexion de Microsoft SharePoint Online à Workfront Fusion à l’aide de paramètres avancés](#connect-microsoft-sharepoint-online-to-workfront-fusion-using-advanced-settings)
* [Connexion de Microsoft SharePoint Online à Workfront Fusion à l’aide de l’autorisation de certificat](#connect-microsoft-sharepoint-online-to-workfront-fusion-using-certificate-authorization)

### Connexion de Microsoft SharePoint Online à Workfront Fusion à l’aide d’un compte [!DNL Microsoft]

Vous pouvez utiliser votre compte [!DNL Microsoft] pour créer une connexion à Microsoft SharePoint Online. Pour obtenir des instructions sur la procédure de connexion de votre compte [!DNL Sharepoint] à Workfront Fusion, voir [Créer une connexion vers Adobe Workfront Fusion - Instructions de base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

### Connexion de Microsoft SharePoint Online à Workfront Fusion à l’aide de paramètres avancés

Pour inclure des informations d’identification dans la connexion, activez l’option Afficher les paramètres avancés . Pour ce type de connexion, vous avez besoin d’un identifiant client, d’un secret client et d’un identifiant client.

1. Dans un module SharePoint, cliquez sur **[!UICONTROL Ajouter]** à proximité du champ Connexion pour afficher la zone **[!UICONTROL Créer une connexion]**.
1. Cliquez sur **[!UICONTROL Afficher les paramètres avancés]**.
1. Remplissez les champs suivants :

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection type]</p> </td> 
      <td>Pour utiliser les informations d'identification du client, sélectionnez <b>Microsoft 365 Email</b>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>Saisissez un nom pour la connexion.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Client ID]</p> </td> 
      <td>Saisissez l’ID client de l’application SharePoint à laquelle vous vous connectez. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Client secret]</p> </td> 
      <td>Saisissez le secret client pour l’application SharePoint à laquelle vous vous connectez.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Tenant ID]</p> </td> 
      <td>Saisissez l’ID client de l’application SharePoint à laquelle vous vous connectez.</td> 
     </tr> 
    </tbody> 
   </table>

1. Cliquez sur **Continuer** pour enregistrer la connexion et revenir au module.

### Connexion de Microsoft SharePoint Online à Workfront Fusion à l’aide de l’autorisation de certificat

Vous pouvez utiliser l’autorisation de certificat pour vous connecter à SharePoint.

>[!IMPORTANT]
>
>Pour utiliser l’autorisation de certificat, vous devez d’abord créer une application dans Microsoft Entra et y télécharger le certificat.
>
>Pour obtenir des instructions, consultez [Comment configurer des autorités de certification pour l’authentification par certificat Microsoft Entra](https://learn.microsoft.com/en-us/entra/identity/authentication/how-to-configure-certificate-authorities) dans la documentation de Microsoft.

1. Dans un module SharePoint, cliquez sur **[!UICONTROL Ajouter]** à proximité du champ Connexion pour afficher la zone **[!UICONTROL Créer une connexion]**.
1. Cliquez sur **[!UICONTROL Afficher les paramètres avancés]**.
1. Remplissez les champs suivants :

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection type]</p> </td> 
      <td>Pour utiliser l’autorisation de certificat, sélectionnez <b>Microsoft SharePoint Online (authentification de certificat)</b>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>Saisissez un nom pour la connexion.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Client ID]</p> </td> 
      <td>Saisissez l’ID client de l’application SharePoint à laquelle vous vous connectez. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Thumbprint]</p> </td> 
      <td>Saisissez l’empreinte numérique de l’application SharePoint à laquelle vous vous connectez.</td> 
     </tr> 
      <tr>
        <td role="rowheader">[!UICONTROL Private key]</td>
        <td>
          <p>Saisissez le certificat ou la clé privée qui a été généré lors de la création de vos informations d’identification dans Microsoft. </p>
          <p>Pour extraire votre clé privée ou votre certificat privé, procédez comme suit :</p>
          <ol>
            <li>
              <p>Cliquez sur <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li>
            <p>Indiquez si vous extrayez un certificat ou une clé privée.</li>
            <li>
              <p>Sélectionnez le type de fichier que vous extrayez.</p>
            </li>
            <li>
              <p>Sélectionnez le fichier contenant la clé privée ou le certificat privé.</p>
            </li>
            <li>
              <p>Saisissez le mot de passe du fichier.</p>
            </li>
            <li>
              <p>Cliquez sur <b>[!UICONTROL Save]</b> pour extraire le fichier et revenir à la configuration de la connexion.</p>
            </li>
          </ol>
        </td>
      </tr>
    </tbody> 
   </table>

1. Cliquez sur **Continuer** pour enregistrer la connexion et revenir au module.

## Modules SharePoint Microsoft et leurs champs

Lorsque vous configurez les modules Microsoft SharePoint Online, Workfront Fusion affiche les champs répertoriés ci-dessous. D’autres champs Microsoft SharePoint Online peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, consultez [Mappage d’informations d’un module à l’autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Bouton (bascule) de mappage](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Élément Drive](#drive-item)
* [Élément](#item)
* [Liste](#list)
* [Page (Beta)](#page-beta)
* [Site](#site)
* [Autre](#other)

### Élément Drive

* [Créer un fichier](#create-a-file)
* [Créer un dossier](#create-a-folder)
* [Obtenir un fichier](#get-a-file)
* [Obtenir un dossier](#get-a-folder)
* [Mettre à jour un dossier ou un fichier](#update-a-folder-or-a-file)
* [Éléments du dossier de contrôle](#watch-folder-items)

#### Créer un fichier

Ce module renvoie la création d’un fichier dans SharePoint. Ce module est plus performant que le module Créer un fichier (hérité).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Sélectionnez le mode d’identification de l’emplacement du dossier dans lequel vous souhaitez récupérer les modifications.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL Drive ID]</strong> et <strong>[!UICONTROL Folder ID]</strong> de l’emplacement où vous souhaitez créer le fichier.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Sélectionnez l’emplacement où vous souhaitez créer le fichier. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file] </td>
      <td><p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p></td>
  </tr>  </tbody> 
</table>



#### Créer un fichier (hérité)

Ce module permet de créer un fichier dans SharePoint.

Pour de meilleures performances, il est recommandé d’utiliser le module [Créer un fichier](#create-a-file).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Sélectionnez le mode d’identification de l’emplacement du dossier dans lequel vous souhaitez récupérer les modifications.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL Drive ID]</strong> et <strong>[!UICONTROL Folder ID]</strong> de l’emplacement où vous souhaitez créer le fichier.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Sélectionnez l’emplacement où vous souhaitez créer le fichier. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
      <td><p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p></td>
  </tr>  </tbody> 
</table>

#### Créer un dossier

Ce module d’action crée un dossier dans SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Sélectionnez le mode d’identification de l’emplacement du dossier que vous souhaitez créer.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL Drive ID]</strong> et <strong>[!UICONTROL Folder ID]</strong> de l’emplacement où vous souhaitez créer le dossier.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Sélectionnez l’emplacement où vous souhaitez créer le dossier. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder name]</td> 
   <td>Saisissez ou mappez un nom pour le nouveau dossier.</td> 
  </tr>
  </tbody> 
</table>

#### Obtenir un fichier

Ce module d’action récupère le fichier SharePoint spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Sélectionnez le mode d’identification de l’emplacement du fichier que vous souhaitez obtenir.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong> et <strong>[!UICONTROL File ID]</strong> pour le fichier que vous souhaitez récupérer.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Sélectionnez l’emplacement du fichier. </p> </li> 
    </ul> </td> 
  </tr> 
</tbody> 
</table>

#### Obtenir un dossier

Ce module a récupéré des détails sur le dossier spécifié

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entrez Site, Lecteur et Fichier                ID]</td> 
   <td> <p>Sélectionnez le mode d’identification de l’emplacement du fichier que vous souhaitez obtenir.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong> et <strong>[!UICONTROL Folder path]</strong> pour le dossier que vous souhaitez récupérer.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Sélectionnez l’emplacement du dossier. </p> </li> 
    </ul> </td> 
  </tr> 
</tbody> 
</table>

#### Mettre à jour un dossier ou un fichier

Ce module d’action met à jour les métadonnées d’un dossier ou d’un fichier

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entrez Site, Lecteur et Fichier                ID]</td> 
   <td> <p>Sélectionnez le mode d’identification de l’emplacement du fichier que vous souhaitez obtenir.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong> et <strong>[!UICONTROL Folder ou item ID]</strong> pour le dossier ou le fichier que vous souhaitez récupérer.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Sélectionnez l’emplacement du dossier. </p> </li> 
    </ul> </td> 
  </tr> 
  </tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td>Pour chaque champ de métadonnées à mettre à jour, cliquez sur <b>Ajouter un élément</b> et saisissez le chemin d’accès et la valeur du champ.</td> 
  <tr>
</tbody> 
</table>

#### Éléments du dossier de contrôle

Ce module de déclenchement lance un scénario lorsqu’un élément est mis à jour dans un dossier que vous sélectionnez.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Sélectionnez le mode d’identification de l’emplacement du fichier que vous souhaitez obtenir.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez l’<strong>[!UICONTROL Site ID]</strong>, l’<strong>[!UICONTROL List ID]</strong>, et l’<strong>[!UICONTROL Folder ID]</strong> dans les champs qui s’affichent.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Sélectionnez l’emplacement du dossier que vous souhaitez surveiller. </p> </li> 
    </ul> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Saisissez le nombre maximal d’éléments que Workfront Fusion doit renvoyer au cours d’un cycle d’exécution de scénario.</td> 
  <tr>
  </tr>
</tbody> 
</table>

### Élément

* [[!UICONTROL Copier un élément]](#copy-an-item)
* [[!UICONTROL Créer un élément]](#create-an-item)
* [[!UICONTROL Supprimer un élément]](#delete-an-item)
* [[!UICONTROL Obtenir un élément]](#get-an-item)
* [Obtenir des détails](#get-details)
* [[!UICONTROL Éléments de liste]](#list-items)
* [[!UICONTROL Déplacer un élément]](#move-an-item)
* [[!UICONTROL Mettre à jour un élément]](#update-an-item)
* [[!UICONTROL Éléments de contrôle] (Planifié)](#watch-items-scheduled)


#### [!UICONTROL Copier un élément]

Ce module d’action copie un élément existant dans une liste SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Saisir des ID de site, de lecteur et de dossier</td> 
   <td> <p>Sélectionnez le mode d'identification du site et du lecteur contenant l'élément à copier.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL Drive ID]</strong> et <strong>[!UICONTROL Item ID]</strong> de l’élément à copier.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from list that you follow]</strong> </p> <p>Dans le champ Type d’élément, indiquez si vous déplacez un champ ou un dossier.  Sélectionnez le site qui contient l’élément à copier, puis sélectionnez la liste et choisissez l’élément. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination ID]</td> 
   <td> Saisissez ou mappez l’ID du dossier dans lequel vous souhaitez copier l’élément. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New name]</td> 
   <td>Saisissez ou mappez un nom pour la nouvelle copie de l’élément. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Créer un élément]

Ce module d’action crée un élément dans une liste SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Create an Item]</td> 
   <td> <p>Sélectionnez la manière dont vous souhaitez identifier le site et piloter l'emplacement où vous souhaitez créer un élément.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong> et <strong>[!UICONTROL List ID]</strong> où vous souhaitez créer l’élément.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le site qui contient la liste dans laquelle vous souhaitez créer un élément, puis sélectionnez la liste. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td>Pour chaque champ que vous souhaitez définir pour le nouvel élément, cliquez sur <b>Ajouter un élément</b> et saisissez la clé du champ (qui identifie le champ) et la valeur que vous souhaitez que le nouvel élément ait pour ce champ.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Supprimer un élément]

Ce module d’action supprime un élément existant dans une liste SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Update an Item]</td> 
   <td> <p>Sélectionnez le mode d’identification du site et de la liste contenant l’élément à supprimer.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong> et <strong>[!UICONTROL Item ID]</strong> de l’élément à supprimer.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le site qui contient l’élément à supprimer, puis la liste, et enfin l’élément. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obtenir un élément]

Ce module d’action renvoie les données d’un élément spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get an Item]</td> 
   <td> <p>Sélectionnez le mode d’identification du site et de la liste contenant l’élément que vous souhaitez obtenir.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong> et <strong>[!UICONTROL Item ID]</strong> de l’élément pour lequel vous souhaitez renvoyer des données.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le site qui contient la liste à partir de laquelle vous souhaitez récupérer un élément, sélectionnez la liste, puis sélectionnez l’élément. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Obtenir des détails

Ce module obtient les détails de l&#39;élément à partir de l&#39;URL spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL Web</td> 
   <td> Saisissez ou mappez l’URL de l’élément pour lequel vous souhaitez récupérer des détails. </td> 
  </tr> 
</tbody> 
</table>

#### [!UICONTROL Éléments de liste]

Ce module d’action récupère une liste de tous les éléments d’une liste spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List Items]</td> 
   <td> <p>Sélectionnez le mode d’identification de la liste à partir de laquelle vous souhaitez récupérer les éléments.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong> et <strong>[!UICONTROL List ID]</strong> pour la liste pour laquelle vous souhaitez répertorier des éléments.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le site qui contient la liste à partir de laquelle vous souhaitez récupérer les éléments, puis sélectionnez la liste. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal d’éléments que le module doit renvoyer au cours de chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Déplacer un élément]

Ce module d’action copie un élément existant dans une liste SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Saisir des ID de site, de lecteur et de dossier</td> 
   <td> <p>Sélectionnez le mode d’identification du site et de la liste contenant l’élément à déplacer.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong> et <strong>[!UICONTROL Item ID]</strong> pour l’élément que vous souhaitez déplacer.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from list that you follow]</strong> </p> <p>Dans le champ Type d’élément, indiquez si vous déplacez un champ ou un dossier. Sélectionnez le site qui contient l’élément à copier, puis sélectionnez la liste et choisissez l’élément. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination ID]</td> 
   <td> Saisissez ou mappez l’identifiant du dossier dans lequel vous souhaitez déplacer l’élément. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New name]</td> 
   <td>Saisissez ou mappez un nom pour l’élément déplacé. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mettre à jour un élément]

Ce module d’action met à jour un élément existant dans une liste SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Update an Item]</td> 
   <td> <p>Sélectionnez le mode d’identification du site et de la liste contenant l’élément que vous souhaitez mettre à jour.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL List ID]</strong> et <strong>[!UICONTROL Item ID]</strong> de l’élément que vous souhaitez mettre à jour.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le site qui contient l’élément que vous souhaitez mettre à jour, puis sélectionnez la liste et choisissez l’élément. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td>Pour chaque champ que vous souhaitez mettre à jour pour le nouvel élément, cliquez sur <b>Ajouter un élément</b> et saisissez la clé du champ (qui identifie le champ) et la nouvelle valeur que vous souhaitez donner à l’élément pour ce champ.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Éléments de contrôle] (Planifié)

Ce module de déclenchement lance un scénario lorsqu’un élément est créé ou modifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch Lists]</td> 
   <td>Choisissez si vous souhaitez surveiller les listes par heure de création (nouveaux éléments) ou par heure de modification (éléments mis à jour).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site and List ID]</td> 
   <td> <p>Sélectionnez le mode d’identification du site et de la liste à surveiller.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong> et <strong>[!UICONTROL List ID]</strong> que vous souhaitez regarder.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Sélectionnez le site que vous souhaitez surveiller, puis sélectionnez la liste. Ces listes déroulantes récupèrent uniquement les sites suivis.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal d’éléments que le module doit renvoyer au cours de chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Liste

* [[!UICONTROL Créer une liste]](#create-a-list)
* [[!UICONTROL Obtenir une liste]](#get-a-list)
* [[!UICONTROL Répertorier des listes]](#list-lists)
* [[!UICONTROL Surveiller des listes]](#watch-lists)

#### [!UICONTROL Créer une liste]

Ce module d’action crée une liste dans SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a Site ID]</td> 
   <td> <p>Sélectionnez la manière dont vous souhaitez identifier le site sur lequel vous souhaitez créer une liste.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez l’<strong>[!UICONTROL Site ID]</strong> où créer une liste.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le site sur lequel vous souhaitez créer une liste. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display Name]</td> 
   <td>Saisissez ou mappez un nom pour la nouvelle liste.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Saisissez ou mappez une description pour la nouvelle liste.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Add Columns]</td> 
   <td>Pour chaque colonne que vous souhaitez définir pour la nouvelle liste, cliquez sur <b>Ajouter un élément </b>, saisissez un <strong>[!UICONTROL Name]</strong> pour le champ, puis sélectionnez le <strong>[!UICONTROL Type]</strong> de valeur que vous souhaitez attribuer à la nouvelle colonne.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obtenir une liste]

Ce module d’action renvoie les données d’une liste spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get a List]</td> 
   <td> <p>Sélectionnez le mode d’identification du site et de la liste contenant l’élément que vous souhaitez obtenir.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong> et <strong>List ID</strong> que vous souhaitez renvoyer.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le site qui contient la liste que vous souhaitez récupérer, puis sélectionnez la liste. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Répertorier des listes]

Ce module d&#39;action récupère une liste de tous les éléments d&#39;un site spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List Lists]</td> 
   <td> <p>Sélectionnez le mode d’identification du site à partir duquel vous souhaitez récupérer les listes.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez le <strong>[!UICONTROL Site ID]</strong> qui contient les listes à renvoyer.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le site qui contient les listes que vous souhaitez récupérer. La liste déroulante récupère uniquement les sites que vous suivez.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal de listes que le module doit renvoyer pour chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Surveiller des listes]

Ce module de déclenchement lance un scénario lorsqu’une liste est créée ou modifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch Lists]</td> 
   <td>Choisissez si vous souhaitez surveiller les listes par heure de création (nouveaux éléments) ou par heure de modification (éléments mis à jour).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site ID]</td> 
   <td> <p>Sélectionnez la manière dont vous souhaitez identifier le site que vous souhaitez surveiller pour les listes.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong> où vous souhaitez regarder les listes.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Sélectionnez le site à surveiller. Le menu déroulant récupère uniquement les sites que vous suivez.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal de listes que le module doit renvoyer pour chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Page (Beta)

>[!NOTE]
>
>Les API en version `beta` dans [!DNL Microsoft Graph] sont susceptibles d’être modifiées. L’utilisation de ces API dans les applications de production n’est pas prise en charge.

* [Obtenir une page](#get-a-page)
* [Pages de liste](#list-pages)
* [Publier une page](#publish-a-page)
* [Pages Espion](#watch-pages)

#### [!UICONTROL Obtenir une page]

Ce module d’action renvoie les données d’une page spécifique.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get a Page]</td> 
   <td> <p>Sélectionnez le mode d’identification de la page que vous souhaitez récupérer.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong> et <strong>[!UICONTROL Page ID]</strong>.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le site qui contient la page que vous souhaitez récupérer, puis sélectionnez la page.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Pages de liste

Ce module récupère une liste de toutes les pages.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List Pages]</td> 
   <td> <p>Sélectionnez le mode d’identification des pages à répertorier.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez le <strong>[!UICONTROL Site ID]</strong> du site qui contient les pages à répertorier.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le site qui contient les pages à répertorier.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal de pages que le module doit renvoyer au cours de chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Publier une page

Ce module d’action publie la dernière version de la page sélectionnée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Publier une page]</td> 
   <td> <p>Sélectionnez le mode d’identification de la page à publier.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong> et <strong>[!UICONTROL Page ID]</strong>.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le site qui contient la page que vous souhaitez publier, puis sélectionnez la page.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Pages Espion

Ce module de déclenchement lance un scénario lorsqu’une page est modifiée sur le site spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site ID]</td> 
   <td> <p>Sélectionnez le mode d’identification des pages à répertorier.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez le <strong>[!UICONTROL Site ID]</strong> du site qui contient les pages que vous souhaitez regarder.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Sélectionnez le site qui contient les pages à regarder.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal de pages que le module doit renvoyer au cours de chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Site

* [[!UICONTROL Obtenir un site]](#get-a-site)
* [[!UICONTROL Rechercher des sites]](#search-sites)

#### [!UICONTROL Obtenir un site]

Ce module d’action renvoie les données d’un site spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get a Site]</td> 
   <td> <p>Sélectionnez le mode d’identification de la page que vous souhaitez récupérer.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez l’<strong>[!UICONTROL Site ID]</strong>.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le site que vous souhaitez récupérer.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Rechercher des sites]

Ce module d’action recherche des sites en fonction d’un paramètre que vous spécifiez.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Keyword of Display Name]</td> 
   <td> <p>Saisissez ou mappez le terme de recherche que vous souhaitez rechercher sur les sites.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal de sites que le module doit renvoyer pour chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Autre

* [Obtenir les modifications](#get-changes)
* [Effectuer un appel API](#make-an-api-call)
* [Surveiller les événements](#watch-events)

#### Obtenir les modifications

Ce module récupère les ajouts, les mises à jour et les suppressions effectués dans le dossier SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Sélectionnez le mode d'identification du site et du lecteur contenant l'élément à mettre à jour.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong>, <strong>[!UICONTROL Drive ID]</strong> et <strong>[!UICONTROL Folder ID]</strong> dans les champs qui s’affichent.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le site contenant l’élément à mettre à jour, puis le lecteur et le dossier. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Token]</td> 
   <td> Le jeton identifie à partir de quel point le module doit commencer à récupérer les modifications.  </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Effectuer un appel API]

Ce module vous permet d’effectuer un appel API personnalisé.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Microsoft SharePoint Online à Workfront Fusion, voir <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Microsoft SharePoint Online à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Saisissez un chemin relatif à <code>https://graph.microsoft.com</code>. Exemple :<code> /beta/sites</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, consultez <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard. Par exemple, <code>{"Content-type":"application/json"}</code>. Workfront Fusion ajoute les en-têtes d’autorisation pour vous.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Ajoutez la requête pour l’appel API sous la forme d’un objet JSON standard.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Sélectionnez le type de données à transmettre dans l’appel API.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre JSON, placez les guillemets à l’extérieur de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Surveiller les événements

Ce module de déclenchement instantané démarre un scénario lorsqu’un élément est ajouté, mis à jour ou supprimé dans SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
  <!--
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to Workfront Fusion, see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  -->
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Sélectionnez un webhook existant ou cliquez sur Ajouter et saisissez la connexion pour créer un webhook.</p> 
   </td> 
  </tr> 
 </tbody> 
</table>
