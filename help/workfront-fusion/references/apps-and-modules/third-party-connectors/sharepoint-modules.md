---
title: Modules SharePoint
description: Dans un scénario  [!DNL Adobe Workfront Fusion] , vous pouvez automatiser les workflows qui utilisent SharePoint et le connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: 1a09aa86-5e0e-4347-b4cf-2b0a95e5b049
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '2271'
ht-degree: 85%

---

# Modules [!DNL SharePoint]

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!DNL SharePoint] et le connecter à plusieurs applications et services tiers.

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

Pour utiliser les modules [!DNL SharePoint], vous devez disposer d’un compte [!DNL SharePoint].

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

## Connecter [!DNL SharePoint] à [!DNL Workfront Fusion] {#connect-sharepoint-to-workfront-fusion}

* [Connecter  [!DNL SharePoint]  à  [!DNL Workfront Fusion]  à l’aide d’un compte  [!DNL Microsoft] ](#connect-sharepoint-to-workfront-fusion-using-a-microsoft-account)
* [Connecter  [!DNL SharePoint]  à  [!DNL Workfront Fusion]  à l’aide des paramètres avancés](#connect-sharepoint-to-workfront-fusion-using-advanced-settings)

### Connecter [!DNL SharePoint] à [!DNL Workfront Fusion] à l’aide d’un compte [!DNL Microsoft]

Vous pouvez utiliser votre compte [!DNL Microsoft] pour créer une connexion à [!DNL SharePoint]. Pour obtenir des instructions sur la connexion de votre compte [!DNL Sharepoint] à [!DNL Workfront Fusion], voir [Créer une connexion à  [!DNL Adobe Workfront Fusion]  - Instructions de base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

### Connecter [!DNL SharePoint] à [!DNL Workfront Fusion] à l’aide des paramètres avancés

Pour connecter [!DNL SharePoint] à [!DNL Workfront Fusion] sans compte [!DNL Microsoft], vous avez besoin d’un ID client, d’un secret client et d’un ID de locataire.

1. Cliquez sur **[!UICONTROL Add]** en haut de la zone de **[!DNL SharePoint]** pour ouvrir la zone de **[!UICONTROL Create a connection]**.

1. (Facultatif) Modifiez le **[!UICONTROL Connection name]** par défaut.
1. Cliquez sur **[!UICONTROL Show advanced settings]**.
1. Saisissez les **[!UICONTROL Client ID]** et **[!UICONTROL Client Secret]** de [!DNL SharePoint].

1. Cliquez sur **[!UICONTROL Continue]**.
1. Dans la fenêtre de connexion qui s’affiche, saisissez vos informations d’identification pour vous connecter à l’application si vous ne l’avez pas déjà fait.
1. (Conditionnel) Si un bouton **[!UICONTROL Allow]** s’affiche, cliquez sur le bouton pour connecter l’application à [!DNL Workfront Fusion].

## Modules [!DNL SharePoint] et leurs champs

Lorsque vous configurez les modules [!DNL SharePoint], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL SharePoint] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Élément Drive](#drive-item)
* [Élément](#item)
* [Liste](#list)
* [Page (version bêta)](#page-beta)
* [Site](#site)
* [Autre](#other)

### Élément Drive

* [Créer un fichier](#create-a-file)
* [Créer un dossier](#create-a-folder)
* [Obtenir un fichier](#get-a-file)
* [Éléments du dossier de contrôle](#watch-folder-items)

#### Obtenir les modifications

Ce module renvoie les modifications apportées dans SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL SharePoint] à [!DNL Workfront Fusion], voir <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL SharePoint] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Sélectionnez le mode d’identification de l’emplacement du dossier dans lequel vous souhaitez récupérer les modifications.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong>, les <strong>[!UICONTROL List ID]</strong> et les <strong>[!UICONTROL Folder ID]</strong> dans les champs qui s’affichent.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Sélectionnez l’emplacement où vous souhaitez récupérer les modifications. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Token]</td> 
   <td> </td> 
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
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL SharePoint] à [!DNL Workfront Fusion], voir <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL SharePoint] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Sélectionnez le mode d’identification de l’emplacement du dossier que vous souhaitez créer.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong>, les <strong>[!UICONTROL List ID]</strong> et les <strong>[!UICONTROL Folder ID]</strong> dans les champs qui s’affichent.</p> </li> 
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
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL SharePoint] à [!DNL Workfront Fusion], voir <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL SharePoint] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Sélectionnez le mode d’identification de l’emplacement du fichier que vous souhaitez obtenir.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong>, les <strong>[!UICONTROL List ID]</strong> et les <strong>[!UICONTROL File ID]</strong> dans les champs qui s’affichent.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Sélectionnez l’emplacement du fichier. </p> </li> 
    </ul> </td> 
  </tr> 
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
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL SharePoint] à [!DNL Workfront Fusion], voir <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL SharePoint] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Sélectionnez le mode d’identification de l’emplacement du fichier que vous souhaitez obtenir.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong>, les <strong>[!UICONTROL List ID]</strong> et les <strong>[!UICONTROL folder ID]</strong> dans les champs qui s’affichent.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Sélectionnez l’emplacement du dossier que vous souhaitez surveiller. </p> </li> 
    </ul> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Entrer le nombre maximal d’éléments que [!DNL Workfront Fusion] doit renvoyer pendant un cycle d’exécution de scénario.</td> 
  <tr>
  </tr>
</tbody> 
</table>

### Élément

* [[!UICONTROL Copy an item]](#copy-an-item)
* [[!UICONTROL Create an item]](#create-an-item)
* [[!UICONTROL Delete an item]](#delete-an-item)
* [[!UICONTROL Get an Item]](#get-an-item)
* [[!UICONTROL List Items]](#list-items)
* [[!UICONTROL Move Item]](#move-an-item)
* [[!UICONTROL Update an item]](#update-an-item)
* [[!UICONTROL Watch Items] (Planifié)](#watch-items-scheduled)


#### [!UICONTROL Copy Item]

Ce module d’action copie un élément existant dans une liste SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL SharePoint] à [!DNL Workfront Fusion], voir <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL SharePoint] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Saisir des ID de site, de lecteur et de dossier</td> 
   <td> <p>Sélectionnez le mode d’identification du site et de la liste qui contiennent l’élément que vous souhaitez copier.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong>, les <strong>[!UICONTROL List ID]</strong> et les <strong>[!UICONTROL Item ID]</strong> dans les champs qui s’affichent.</p> </li> 
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

#### [!UICONTROL Create an item]

Ce module d’action crée un élément dans une liste SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL SharePoint] à [!DNL Workfront Fusion], voir <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL SharePoint] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Create an Item]</td> 
   <td> <p>Sélectionnez le mode d’identification du site et la liste dans laquelle vous souhaitez créer un élément.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong> et les <strong>[!UICONTROL List ID]</strong> dans les champs qui s’affichent.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le site qui contient la liste dans laquelle vous souhaitez créer un élément, puis sélectionnez la liste. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td>Pour chaque champ que vous souhaitez définir pour le nouvel élément, saisissez la clé du champ (identifie le champ) et la valeur du nouvel élément pour ce champ.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an item]

Ce module d’action supprime un élément existant dans une liste SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL SharePoint] à [!DNL Workfront Fusion], voir <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL SharePoint] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Update an Item]</td> 
   <td> <p>Sélectionnez le mode d’identification du site et de la liste contenant l’élément à supprimer.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong>, les <strong>[!UICONTROL List ID]</strong> et les <strong>[!UICONTROL Item ID]</strong> dans les champs qui s’affichent.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le site qui contient l’élément à supprimer, puis la liste, et enfin l’élément. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an Item]

Ce module d’action renvoie les données d’un élément spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL SharePoint] à [!DNL Workfront Fusion], voir <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL SharePoint] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get an Item]</td> 
   <td> <p>Sélectionnez le mode d’identification du site et de la liste contenant l’élément que vous souhaitez obtenir.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong>, les <strong>[!UICONTROL List ID]</strong> et les <strong>[!UICONTROL Item ID]</strong> dans les champs qui s’affichent.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le site qui contient la liste à partir de laquelle vous souhaitez récupérer un élément, sélectionnez la liste, puis sélectionnez l’élément. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Items]

Ce module d’action récupère une liste de tous les éléments d’une liste spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL SharePoint] à [!DNL Workfront Fusion], voir <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL SharePoint] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List Items]</td> 
   <td> <p>Sélectionnez le mode d’identification de la liste à partir de laquelle vous souhaitez récupérer les éléments.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong> et les <strong>[!UICONTROL List ID]</strong> dans les champs qui s’affichent.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le site qui contient la liste à partir de laquelle vous souhaitez récupérer les éléments, puis sélectionnez la liste. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal d’éléments que le module doit renvoyer au cours de chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move an Item]

Ce module d’action copie un élément existant dans une liste SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL SharePoint] à [!DNL Workfront Fusion], voir <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL SharePoint] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Saisir des ID de site, de lecteur et de dossier</td> 
   <td> <p>Sélectionnez le mode d’identification du site et de la liste contenant l’élément à déplacer.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong>, les <strong>[!UICONTROL List ID]</strong> et les <strong>[!UICONTROL Item ID]</strong> dans les champs qui s’affichent.</p> </li> 
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

#### [!UICONTROL Update an item]

Ce module d’action met à jour un élément existant dans une liste SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL SharePoint] à [!DNL Workfront Fusion], voir <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL SharePoint] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Update an Item]</td> 
   <td> <p>Sélectionnez le mode d’identification du site et de la liste contenant l’élément que vous souhaitez mettre à jour.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong>, les <strong>[!UICONTROL List ID]</strong> et les <strong>[!UICONTROL Item ID]</strong> dans les champs qui s’affichent.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le site qui contient l’élément que vous souhaitez mettre à jour, puis sélectionnez la liste et choisissez l’élément. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td>Pour chaque champ que vous souhaitez mettre à jour pour le nouvel élément, saisissez la clé du champ (identifie le champ) et la nouvelle valeur que vous souhaitez que l’élément ait pour ce champ.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Items] (Planifié)

Ce module de déclenchement lance un scénario lorsqu’un élément est créé ou modifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL SharePoint] à [!DNL Workfront Fusion], voir <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL SharePoint] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch Lists]</td> 
   <td>Choisissez si vous souhaitez surveiller les listes par heure de création (nouveaux éléments) ou par heure de modification (éléments mis à jour).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site and List ID]</td> 
   <td> <p>Sélectionnez le mode d’identification du site et de la liste à surveiller.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong> et les <strong>[!UICONTROL List ID]</strong> dans les champs qui s’affichent.</p> </li> 
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

* [[!UICONTROL Create a List]](#create-a-list)
* [[!UICONTROL Get a List]](#get-a-list)
* [[!UICONTROL List Lists]](#list-lists)
* [[!UICONTROL Watch Lists]](#watch-lists)

#### [!UICONTROL Create a List]

Ce module d’action crée une liste dans SharePoint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL SharePoint] à [!DNL Workfront Fusion], voir <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL SharePoint] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a Site ID]</td> 
   <td> <p>Sélectionnez le mode d’identification du site et de la liste dans lesquels vous souhaitez créer une liste.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez le <strong>[!UICONTROL Site ID]</strong> dans lequel vous souhaitez créer une liste.</p> </li> 
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
   <td>Pour chaque colonne que vous souhaitez définir pour la nouvelle liste, saisissez un <strong>[!UICONTROL Name]</strong> pour le champ, puis sélectionnez le <strong>[!UICONTROL Type]</strong> de valeur que vous souhaitez attribuer à la nouvelle colonne.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a List]

Ce module d’action renvoie les données d’une liste spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL SharePoint] à [!DNL Workfront Fusion], voir <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL SharePoint] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get a List]</td> 
   <td> <p>Sélectionnez le mode d’identification du site et de la liste contenant l’élément que vous souhaitez obtenir.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong> et <strong>ID de liste</strong> dans les champs qui s’affichent.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le site qui contient la liste que vous souhaitez récupérer, puis sélectionnez la liste. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Lists]

Ce module d’action récupère une liste de tous les éléments d’une liste spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL SharePoint] à [!DNL Workfront Fusion], voir <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL SharePoint] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List Lists]</td> 
   <td> <p>Sélectionnez le mode d’identification du site à partir duquel vous souhaitez récupérer les listes.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez le <strong>[!UICONTROL Site ID]</strong>.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le site qui contient les listes que vous souhaitez récupérer. La liste déroulante récupère uniquement les sites que vous suivez.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal de listes que le module doit renvoyer pour chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Lists]

Ce module de déclenchement lance un scénario lorsqu’une liste est créée ou modifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL SharePoint] à [!DNL Workfront Fusion], voir <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL SharePoint] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch Lists]</td> 
   <td>Choisissez si vous souhaitez surveiller les listes par heure de création (nouveaux éléments) ou par heure de modification (éléments mis à jour).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site and List ID]</td> 
   <td> <p>Sélectionnez le mode d’identification du site et de la liste à surveiller.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez le <strong>[!UICONTROL Site ID]</strong> où se trouve la liste que vous souhaitez observer.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>Sélectionnez le site à surveiller. Le menu déroulant récupère uniquement les sites que vous suivez.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal de listes que le module doit renvoyer pour chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Page (version bêta)

>[!NOTE]
>
>Les API en version `beta` dans [!DNL Microsoft Graph] sont susceptibles d’être modifiées. L’utilisation de ces API dans les applications de production n’est pas prise en charge.

#### [!UICONTROL Get a Page]

Ce module d’action renvoie les données d’une page spécifique.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL SharePoint] à [!DNL Workfront Fusion], voir <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL SharePoint] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get a Page]</td> 
   <td> <p>Sélectionnez le mode d’identification de la page que vous souhaitez récupérer.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Page ID]</strong> <strong>[!UICONTROL Site ID]</strong> et .</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le site qui contient la page que vous souhaitez récupérer, puis sélectionnez la page.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Site

* [[!UICONTROL Get a Site]](#get-a-site)
* [[!UICONTROL Search Sites]](#search-sites)

#### [!UICONTROL Get a Site]

Ce module d’action renvoie les données d’un site spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL SharePoint] à [!DNL Workfront Fusion], voir <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL SharePoint] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get a Site]</td> 
   <td> <p>Sélectionnez le mode d’identification de la page que vous souhaitez récupérer.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez le <strong>[!UICONTROL Site ID]</strong>.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le site que vous souhaitez récupérer.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search Sites]

Ce module d’action recherche des sites en fonction d’un paramètre que vous spécifiez.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL SharePoint] à [!DNL Workfront Fusion], voir <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL SharePoint] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
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
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL SharePoint] à [!DNL Workfront Fusion], voir <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL SharePoint] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>Sélectionnez le mode d’identification du site et de la liste contenant l’élément que vous souhaitez mettre à jour.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez les <strong>[!UICONTROL Site ID]</strong>, les <strong>[!UICONTROL Drive ID]</strong> et les <strong>[!UICONTROL Folder ID]</strong> dans les champs qui s’affichent.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le site contenant l’élément à mettre à jour, puis le lecteur et le dossier. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Token]</td> 
   <td> Le jeton identifie à partir de quel point le module doit commencer à récupérer les modifications.  </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Make an API Call]

Ce module vous permet d’effectuer un appel API personnalisé.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL SharePoint] à [!DNL Workfront Fusion], voir <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL SharePoint] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Saisissez un chemin relatif à <code>https://graph.microsoft.com</code>. Exemple :<code> /beta/sites</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP dans [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard. Par exemple : <code>{"Content-type":"application/json"}</code>. [!DNL Workfront Fusion] ajoute les en-têtes d’autorisation.</p> </td> 
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
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lors de l’utilisation d’instructions conditionnelles telles que <code>if</code> dans votre fichier JSON, placez les guillemets en dehors de l’instruction conditionnelle.</p> 
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
   <td> <p>For instructions about connecting your [!DNL SharePoint] account to [!DNL Workfront Fusion], see <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect [!DNL SharePoint] to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  -->
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Sélectionnez un webhook existant ou cliquez sur Ajouter pour créer un webhook.</p> 
   </td> 
  </tr> 
 </tbody> 
</table>
