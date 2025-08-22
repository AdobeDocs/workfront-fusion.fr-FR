---
title: Modules Google Docs
description: Les modules Adobe Workfront Fusion [!DNL Google Docs]  [!DNL Google Docs]  module vous permettent de surveiller, créer, modifier et récupérer des documents dans vos et  [!DNL Google Docs]  (pour  [!DNL Google Workspace]  utilisateurs).
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: cd44250d-c2cd-46b2-8773-15b30472a8d8
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '4087'
ht-degree: 80%

---

# Modules [!DNL Google Docs]

Les modules Adobe Workfront Fusion [!DNL Google Docs] vous permettent de surveiller, créer, modifier et récupérer des documents dans vos [!DNL Google Docs] et [!DNL Google Docs] (pour les utilisateurs [!DNL Google Workspace]).

Pour utiliser [!DNL Google Docs] avec Adobe Workfront Fusion, il est nécessaire d’avoir un compte [!DNL Google]. Si vous n’avez pas encore de compte [!DNL Google], vous pouvez en créer un sur la page d’aide des comptes [!DNL Google].

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

## Conditions préalables

Pour utiliser les modules [!DNL Google Docs], vous devez disposer d’un compte Google.

## Informations sur l’API Google Docs

Le connecteur Google Docs utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td> https://docs.googleapis.com/v1</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Version de l’API</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.4.13</td> 
  </tr>
 </tbody> 
 </table>

## Modules et champs [!DNL Google Docs]

Lorsque vous configurez les modules [!DNL Google Docs], [!UICONTROL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Google Docs] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Document

* [[!UICONTROL Créer un document]](#create-a-document)
* [[!UICONTROL Créer un document à partir d’un modèle]](#create-a-document-from-a-template)
* [[!UICONTROL Supprimer un document]](#delete-a-document)
* [[!UICONTROL Télécharger un document]](#download-a-document)
* [[!UICONTROL Obtenir le contenu d’un document]](#get-content-of-a-document)
* [[!UICONTROL Insérer un paragraphe dans un document]](#insert-a-paragraph-to-a-document)
* [[!UICONTROL Insérer une image dans un document]](#insert-an-image-to-a-document)
* [[!UICONTROL Répertorier des documents]](#list-documents)
* [[!UICONTROL Remplacer le texte d’un document]](#replace-text-in-a-document)
* [[!UICONTROL Remplacer une image par une nouvelle image]](#replace-an-image-with-a-new-image)
* [[!UICONTROL Surveiller des documents]](#watch-documents)

#### [!UICONTROL Créer un document]

Ce module d’action permet de créer un document dans le dossier sélectionné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Saisissez un nom pour le document.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content]</td> 
   <td> <p>Saisissez le contenu du document. Vous pouvez inclure HTML pour formater le document.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Sélectionnez le type de lecteur sur lequel vous souhaitez créer un document.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Dans le champ Emplacement du nouveau document , sélectionnez le dossier dans lequel vous souhaitez créer un document.</p> </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p>Dans le champ Emplacement du nouveau document , sélectionnez le dossier dans lequel vous souhaitez créer un document.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (disponible pour les utilisateurs et les utilisatrices de [!DNL Google Workspace] uniquement)</p> <p>Indiquez si vous souhaitez [!UICONTROL Use Domain Admin Access]. Si vous sélectionnez [!UICONTROL Yes], la requête est émise en tant qu’administrateur ou administratrice de domaine et tous les lecteurs partagés administrés par la personne effectuant la requête seront renvoyés.</p> <p>Sélectionnez le lecteur partagé sur lequel vous souhaitez créer un document.</p> <p>Note : si vous avez sélectionné dans ce champ l’option [!DNL Google Docs] et que vous n’êtes pas un utilisateur ou une utilisatrice de [!DNL Google Workspace], l’erreur <code>[400] Invalid Value</code> est renvoyée.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Insert a Header]</td> 
   <td> <p> Activez cette option pour insérer l’en-tête dans le document, puis saisissez ou mappez le texte de l’en-tête.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Insert a Footer] </td> 
   <td> <p>Activez cette option pour insérer le pied de page dans le document, puis saisissez ou mappez le texte de l’en-tête.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Créer un document à partir d’un modèle]

Ce module d’action crée une copie d’un modèle de document existant et remplace toutes les balises. Ce module permet également aux utilisateurs et aux utilisatrices de remplacer les images par de nouvelles images par URL.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Create a Document from a Template]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>Sélectionnez cette option pour mapper le modèle de document.</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> <br>Sélectionnez cette option pour choisir le modèle de document dans le menu déroulant.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Sélectionnez le type de lecteur sur lequel se trouve votre modèle. Cette option est disponible si vous avez sélectionné [!UICONTROL By Dropdown] dans le champ précédent.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p>  </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (disponible pour les utilisateurs et les utilisatrices de [!DNL Google Workspace] uniquement)</p> <p>Indiquez si vous souhaitez [!UICONTROL Use Domain Admin Access]. Si vous sélectionnez [!UICONTROL Yes], la requête est émise en tant qu’administrateur ou administratrice de domaine et tous les lecteurs partagés administrés par la personne effectuant la requête seront renvoyés.</p> <p>Sélectionnez le lecteur partagé où se trouve votre modèle.</p> <p>Note : si vous avez sélectionné l’option [!DNL Google Docs] dans ce champ et que vous n’êtes pas utilisateur ou utilisatrice de [!DNL Google Workspace], l’erreur <code>[400] Invalid Value</code> est renvoyée.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Document ID]</td> 
   <td> <p>Mappez l’identifiant du modèle si vous avez sélectionné En fonction du mappage ou sélectionnez le chemin d’accès au modèle et au modèle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Values]</p> </td> 
   <td> <p>Pour chaque balise pour laquelle vous souhaitez saisir une valeur, cliquez sur <b>Ajouter un élément</b>, saisissez la balise, puis saisissez la valeur qui sera saisie à la place de la balise dans le nouveau document.</p> 
    <ul> 
     <li><strong>[!UICONTROL Tags]</strong> <br>Saisissez les balises contenues dans le modèle de document. N’utilisez pas <code>&#123;&#123;&#125;&#125;</code>. Exemple : utilisez <code>name</code> au lieu de <code>&#123;&#123;name&#125;&#125;</code>.</li> 
     <li><strong>[!UICONTROL Replaced Value]</strong><br> Saisissez la valeur de la balise.</li> 
    </ul> <p>Par exemple, la variable <code> &#123;&#123;name&#125;&#125;</code> dans le document source s’affiche comme champ de nom, où la valeur peut être insérée, comme <code>John</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Images Replacement]</p> </td> 
   <td> <p>&gt;Pour chaque balise pour laquelle vous souhaitez saisir une valeur, cliquez sur <b>Ajouter un élément</b>, puis saisissez le lien vers l’[!UICONTROL Image Object ID] et l’[!UICONTROL Image URL] qui remplaceront l’image actuelle.</p> <p>Note : vous pouvez récupérer les ID d’image à l’aide du module [!UICONTROL Get a Document], où les ID sont contenus dans le tableau [!UICONTROL Inline Object Array].</p> <p>Nous vous recommandons d’ajouter du texte de remplacement aux images de votre document [!DNL Google]. </p> <p>Pour ajouter un texte de remplacement à l’image [!DNL Google Docs], procédez comme suit :</p> 
    <ol> 
     <li value="1">Faites un clic droit sur l’image.</li> 
     <li value="2">Sélectionnez l’option [!UICONTROL ALT text].</li> 
     <li value="3">Saisissez le [!UICONTROL ALT text] dans le champ [!UICONTROL Title] et cliquez sur [!UICONTROL OK].</li> 
    </ol> <p>Une fois le texte de remplacement ajouté à l’image, il est affiché entre parenthèses dans le nom du champ.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title] </td> 
   <td> <p>Saisissez le nom du nouveau document.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Sélectionnez le type de lecteur sur lequel se trouve votre modèle. Cette option est disponible si vous avez sélectionné [!UICONTROL By Dropdown] dans le champ précédent.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Sélectionnez le dossier dans lequel vous souhaitez créer le document.</p> </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p>Sélectionnez le dossier dans lequel vous souhaitez créer le document.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (disponible pour les utilisateurs et utilisatrices de [!DNL Google Workspace] uniquement)</p> <p>Indiquez si vous souhaitez [!UICONTROL Use Domain Admin Access]. Si vous sélectionnez [!UICONTROL Yes], la requête est émise en tant qu’administrateur ou administratrice de domaine et tous les lecteurs partagés administrés par la personne effectuant la requête seront renvoyés.</p> <p>Sélectionnez le lecteur partagé sur lequel vous souhaitez créer le document.</p> <p>Note : si vous avez sélectionné l’option [!DNL Google Docs] dans ce champ et que vous n’êtes pas utilisateur ou utilisatrice de [!DNL Google Workspace], l’erreur <code>[400] Invalid Value</code> est renvoyée.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Supprimer un document]

Ce module d’action supprime un document.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Sélectionnez le type de lecteur sur lequel se trouve le document que vous souhaitez supprimer.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Sélectionnez le dossier dans lequel se trouve le document à supprimer, puis sélectionnez ce dernier.</p> </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p>Sélectionnez le dossier dans lequel se trouve le document à supprimer, puis sélectionnez ce dernier.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (disponible pour les utilisateurs et les utilisatrices [!DNL Google Workspace] uniquement)</p> <p>Indiquez si vous souhaitez [!UICONTROL Use Domain Admin Access]. Si vous sélectionnez [!UICONTROL Yes], la requête est émise en tant qu’administrateur ou administratrice de domaine et tous les lecteurs partagés administrés par la personne effectuant la requête seront renvoyés.</p> <p>Sélectionnez le lecteur partagé sur lequel se trouve le document à supprimer, puis sélectionnez le document.</p> <p>Note : si vous avez sélectionné l’option [!DNL Google Docs] dans ce champ et que vous n’êtes pas un utilisateur ou une utilisatrice de [!DNL Google Workspace], l’erreur <code>[400] Invalid Value</code> est renvoyée.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Shared Drive]</td> 
   <td> <p>Sélectionnez le lecteur contenant le document à télécharger, puis sélectionnez un document. Cette option est disponible si vous avez sélectionné [!DNL My Drive] dans le champ [!UICONTROL Choose a Drive].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Document ID]</td> 
   <td> <p> Sélectionnez ou mappez le document à supprimer.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Télécharger un document]

Ce module d’action convertit et télécharge le document sélectionné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Sélectionnez le type de lecteur sur lequel se trouve le document à télécharger.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Dans le champ ID du document , sélectionnez le dossier dans lequel se trouve le document que vous souhaitez télécharger, puis sélectionnez le document.</p> </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p>Dans le champ ID du document , sélectionnez le dossier dans lequel se trouve le document que vous souhaitez télécharger, puis sélectionnez le document.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (disponible pour les utilisateurs et les utilisatrices de [!DNL Google Workspace] uniquement)</p> <p>Indiquez si vous souhaitez [!UICONTROL Use Domain Admin Access]. Si vous sélectionnez [!UICONTROL Yes], la requête est émise en tant qu’administrateur ou administratrice de domaine et tous les lecteurs partagés administrés par la personne effectuant la requête seront renvoyés.</p> <p>Sélectionnez le lecteur partagé sur lequel se trouve le document à télécharger, puis sélectionnez le document.</p> <p>Note : si vous avez sélectionné l’option [!DNL Google Docs] dans ce champ et que vous n’êtes pas utilisateur ou utilisatrice de [!DNL Google Workspace], l’erreur <code>[400] Invalid Value</code> est renvoyée.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Type] </p> </td> 
   <td> <p>Sélectionnez le format de fichier cible du document téléchargé.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obtenir le contenu d’un document]

Ce module d’action récupère un document spécifié.

Vous devrez peut-être augmenter vos autorisations.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get Content of a Document]</td> 
   <td> <p>Indiquez si vous souhaitez mapper l’ID du document ou sélectionner le document manuellement dans le menu déroulant.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Sélectionnez le type de lecteur contenant le document à récupérer.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Sélectionnez le dossier contenant le document à récupérer.</p> </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p>Sélectionnez le dossier contenant le document à récupérer.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (disponible pour les utilisateurs et utilisatrices de [!DNL Google Workspace] uniquement)</p> <p>Indiquez si vous souhaitez [!UICONTROL Use Domain Admin Access]. Si vous sélectionnez [!UICONTROL Yes], la requête est émise en tant qu’administrateur ou administratrice de domaine et tous les lecteurs partagés administrés par la personne effectuant la requête seront renvoyés.</p> <p>Sélectionnez le lecteur partagé qui contient le document à récupérer.</p> <p>Note : si vous avez sélectionné l’option [!DNL Google Docs] dans ce champ et que vous n’êtes pas un utilisateur ou une utilisatrice de [!DNL Google Workspace], l’erreur <code>[400] Invalid Value</code> est renvoyée.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Document ID]</td> 
   <td> <p>Saisissez ou sélectionnez le document à récupérer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Filter]</p> </td> 
   <td> <p>Sélectionnez l’objet que vous souhaitez renvoyer dans la sortie du module.</p> 
    <ul> 
     <li>[!UICONTROL Image] (par défaut)</li> 
     <li>[!UICONTROL Drawing]</li> 
     <li>[!UICONTROL Chart]</li> 
    </ul> <p>Note :  <p>Pour effectuer un mappage supplémentaire de ces objets, utilisez la valeur [!UICONTROL Inline Objects Array] dans la sortie de ce module (au lieu de [!UICONTROL inlineObjects]).</p> <p>Les objets [!UICONTROL Inline Objects Array] sont triés dans le même ordre que celui dans lequel ils apparaissent dans le document. Cela facilite le traitement.</p> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Insérer un paragraphe dans un document]

Ce module d’action ajoute ou insère un nouveau paragraphe dans un document existant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Select a Document]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>Sélectionnez cette option pour mapper le document.</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> <br> Sélectionnez cette option pour sélectionner le document dans le menu déroulant.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Sélectionnez le type de lecteur sur lequel se trouve le document auquel vous souhaitez ajouter un paragraphe. Cette option est disponible si vous avez sélectionné [!UICONTROL By Dropdown] dans le champ précédent.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Sélectionnez le dossier dans lequel se trouve le document auquel vous souhaitez ajouter un paragraphe.</p> </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p>Sélectionnez le dossier dans lequel se trouve le document auquel vous souhaitez ajouter un paragraphe.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (disponible pour les utilisateurs et les utilisatrices de [!DNL Google Workspace] uniquement)</p> <p>Indiquez si vous souhaitez [!UICONTROL Use Domain Admin Access]. Si vous sélectionnez [!UICONTROL Yes], la requête est émise en tant qu’administrateur ou administratrice de domaine et tous les lecteurs partagés administrés par la personne effectuant la requête seront renvoyés.</p> <p>Sélectionnez le lecteur partagé sur lequel se trouve le document auquel vous souhaitez ajouter un paragraphe, puis sélectionnez le document.</p> <p>Note : si vous avez sélectionné l’option [!DNL Google Docs] dans ce champ et que vous n’êtes pas un utilisateur ou une utilisatrice de [!DNL Google Workspace], l’erreur <code>[400] Invalid Value</code> est renvoyée.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Document ID]</td> 
   <td> <p>Mappez ou sélectionnez le document dans lequel vous souhaitez insérer du texte.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Insert a Paragraph]</p> </td> 
   <td> <p>Sélectionnez le mode d’insertion du nouveau texte dans le document.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL By specification of location]</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL By index]</strong> </p> 
        <ul> 
         <li> <p><strong>[!UICONTROL Index]</strong> </p> <p>Saisissez le numéro de l’index dans lequel vous souhaitez insérer votre texte. Vous pouvez utiliser le module [!UICONTROL Get a Document] pour récupérer le numéro d'index.</p> </li> 
         <li> <p><strong>[!UICONTROL Inserted text]</strong> </p> <p>Saisissez le texte à insérer dans le document.</p> </li> 
        </ul> </li> 
       <li> <p><strong>[!UICONTROL By segment ID]</strong> </p> <p>Sélectionnez l’en-tête et le pied de page dans lesquels vous souhaitez insérer du contenu et saisissez le texte à insérer dans les champs correspondants.</p> <p>Si l’en-tête ou le pied de page contient déjà du texte, le nouveau texte est ajouté avant le texte existant.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL By appending to the body of the document]</strong> </p> <p>Ajoute le texte saisi à la fin du contenu du corps du document.</p> <p>Le style du nouveau paragraphe sera copié à partir du paragraphe à l’index d’insertion actuel, listes et puces comprises.</p> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL By appending to the end of segment (Header and Footer)]</strong> </p> <p>Sélectionnez l’en-tête et le pied de page dans lesquels vous souhaitez insérer du contenu et saisissez le texte à insérer dans les champs correspondants.</p> <p>Si l’en-tête ou le pied de page contient déjà du texte, le nouveau texte est ajouté après le texte existant.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Appended Text]</td> 
   <td>Saisissez ou mappez le texte à ajouter au document.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Insérer une image dans un document]

Ce module d’action insère une image de l’URL vers le document.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Select a Document]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>Sélectionnez cette option pour mapper le modèle de document.</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> <br> Sélectionnez cette option pour sélectionner le document dans le menu déroulant.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Sélectionnez le type de lecteur sur lequel se trouve le document auquel vous souhaitez ajouter une image. Cette option est disponible si vous avez sélectionné [!UICONTROL By Dropdown] dans le champ précédent.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Sélectionnez le dossier dans lequel se trouve le document auquel vous souhaitez ajouter une image.</p> </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p>Sélectionnez le dossier dans lequel se trouve le document auquel vous souhaitez ajouter une image.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (disponible pour les utilisateurs et les utilisatrices de [!DNL Google Workspace] uniquement)</p> <p>Indiquez si vous souhaitez [!UICONTROL Use Domain Admin Access]. Si vous sélectionnez [!UICONTROL Yes], la requête est émise en tant qu’administrateur ou administratrice de domaine et tous les lecteurs partagés administrés par la personne effectuant la requête seront renvoyés.</p> <p>Sélectionnez le lecteur partagé sur lequel se trouve le document auquel vous souhaitez ajouter une image, puis sélectionnez le document.</p> <p>Note : si vous avez sélectionné l’option [!DNL Google Docs] dans ce champ et que vous n’êtes pas un utilisateur ou une utilisatrice de [!DNL Google Workspace], l’erreur <code>[400] Invalid Value</code> est renvoyée.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Document ID]</td> 
   <td> <p>Mappez ou sélectionnez le document dans lequel vous souhaitez insérer une image.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Insert an Image]</p> </td> 
   <td> <p>Sélectionnez le mode d’insertion de la nouvelle image dans le document.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL By specification of location]</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL By index]</strong> </p> 
        <ul> 
         <li> <p><strong>[!UICONTROL Index]</strong> </p> <p>Saisissez le numéro de l’index dans lequel vous souhaitez insérer votre image. Vous pouvez utiliser le module [!UICONTROL Get a Document] pour récupérer le [!UICONTROL Index number].</p>  </li> 
         <li> <p><strong>[!UICONTROL Image URL]</strong> </p> <p>Saisissez l’URL de l’image à insérer dans le document.</p> <p>La taille d’image maximale est de 50 Mo. Ne doit pas dépasser 25 mégapixels. Seuls les formats PNG, JPEG et GIF sont pris en charge.</p> </li> 
        </ul> </li> 
       <li> <p><strong>[!UICONTROL By segment ID]</strong> </p> <p>Sélectionnez l’en-tête et le pied de page auxquels vous souhaitez insérer l’image et saisissez l’URL de l’image dans les champs correspondants.</p> <p>La taille d’image maximale est de 50 Mo. L’image ne doit pas dépasser 25 mégapixels. Seuls les formats PNG, JPEG et GIF sont pris en charge.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL By appending to the body of the document]</strong> </p> <p>Ajoute une image spécifique à la fin du contenu du corps du document.</p> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL By appending to the end of segment (Header and Footer)]</strong> </p> <p>Sélectionnez l’en-tête et le pied de page auxquels vous souhaitez insérer une image et saisissez l’URL de l’image à insérer dans les champs correspondants.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Height Magnitude in Points/Width Magnitude in Points]</p> </td> 
   <td> <p>Définissez la hauteur ou la largeur de l’image insérée. Les proportions seront conservées.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Répertorier des documents]

Ce module d’action récupère une liste de documents du dossier sélectionné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Sélectionnez le type de lecteur dont vous souhaitez répertorier les documents.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Sélectionnez le dossier dont vous souhaitez répertorier les documents.</p> </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p>Sélectionnez le dossier dont vous souhaitez répertorier les documents.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (disponible pour les utilisateurs et utilisatrices de [!DNL Google Workspace] uniquement)</p> <p>Indiquez si vous souhaitez [!UICONTROL Use Domain Admin Access]. Si vous sélectionnez [!UICONTROL Yes], la requête est émise en tant qu’administrateur ou administratrice de domaine et tous les lecteurs partagés administrés par la personne effectuant la requête seront renvoyés.</p> <p>Sélectionnez le lecteur partagé dont vous souhaitez répertorier les documents.</p> <p>Note : si vous avez sélectionné l’option [!DNL Google Docs] dans ce champ et que vous n’êtes pas un utilisateur ou une utilisatrice de [!DNL Google Workspace], l’erreur <code>[400] Invalid Value</code> est renvoyée.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Définissez le nombre maximal de documents que Workfront Fusion renvoie dans un cycle d’exécution.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remplacer le texte d’un document]

Ce module d’action remplace le texte dans un document.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Select a Document]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>Sélectionnez cette option pour mapper le modèle de document.</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> <br> Sélectionnez cette option pour sélectionner le document dans le menu déroulant.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Sélectionnez le type de lecteur sur lequel se trouve le document auquel vous souhaitez ajouter du texte. Cette option est disponible si vous avez sélectionné [!UICONTROL By Dropdown] dans le champ précédent.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Sélectionnez le dossier dans lequel se trouve le document auquel vous souhaitez ajouter du texte, puis sélectionnez le document.</p> </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p>Sélectionnez le dossier dans lequel se trouve le document auquel vous souhaitez ajouter du texte, puis sélectionnez le document.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (disponible pour les utilisateurs et utilisatrices [!DNL Google Workspace] uniquement)</p> <p>Indiquez si vous souhaitez [!UICONTROL Use Domain Admin Access]. Si vous sélectionnez [!UICONTROL Yes], la requête est émise en tant qu’administrateur ou administratrice de domaine et tous les lecteurs partagés administrés par la personne effectuant la requête seront renvoyés.</p> <p>Sélectionnez le lecteur partagé sur lequel se trouve le document auquel vous souhaitez ajouter du texte, puis sélectionnez le document.</p> <p>Note : si vous avez sélectionné l’option [!DNL Google Docs] dans ce champ et que vous n’êtes pas utilisateur ou utilisatrice de [!DNL Google Workspace], l’erreur <code>[400] Invalid Value</code> est renvoyée.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Document ID]</td> 
   <td> <p>Mappez ou sélectionnez le document dans lequel vous souhaitez remplacer le texte.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Replace a Text]</p> </td> 
   <td> <p>Pour chaque texte à remplacer, cliquez sur <b>Ajouter un élément</b> et saisissez les informations suivantes :</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Old text to be replaced]</strong> </p> <p>Saisissez le texte à remplacer.</p> </li> 
     <li> <p><strong>[!UICONTROL New text to be inserted]</strong> </p> <p>Saisissez le nouveau texte.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
 </table>

#### [!UICONTROL Remplacer une image par une nouvelle image]

Ce module d’action remplace une image existante. Les proportions de l’image d’origine seront conservées.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Select a Document]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>Sélectionnez cette option pour mapper le modèle de document.</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> <br> Sélectionnez cette option pour sélectionner le document dans le menu déroulant.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Sélectionnez le type de lecteur sur lequel se trouve le document dont vous souhaitez remplacer une image. Cette option est disponible si vous avez sélectionné [!UICONTROL By Dropdown] dans le champ précédent.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Sélectionnez le dossier dans lequel se trouve le document dont vous souhaitez remplacer une image, puis sélectionnez le document.</p> </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p>Sélectionnez le dossier dans lequel se trouve le document dont vous souhaitez remplacer une image, puis sélectionnez le document.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (disponible pour les utilisateurs et utilisatrices [!DNL Google Workspace] uniquement)</p> <p>Indiquez si vous souhaitez [!UICONTROL Use Domain Admin Access]. Si vous sélectionnez [!UICONTROL Yes], la requête est émise en tant qu’administrateur ou administratrice de domaine et tous les lecteurs partagés administrés par la personne effectuant la requête seront renvoyés.</p> <p>Sélectionnez le lecteur partagé sur lequel se trouve le document dont vous souhaitez remplacer une image, puis sélectionnez le document.</p> <p>Remarque : si vous avez sélectionné l’option [!DNL Google Docs] dans ce champ et que vous n’êtes pas un utilisateur ou une utilisatrice [!DNL Google Workspace], l’erreur <code>[400] Invalid Value</code> est renvoyée.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Document ID]</td> 
   <td> <p>Mappez ou sélectionnez le document dans lequel vous souhaitez remplacer une image.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Images replace]</p> </td> 
   <td> Pour chaque image à remplacer, cliquez sur <b>Ajouter un élément</b> et saisissez l’identifiant de l’image existante, puis saisissez ou mappez l’URL de la nouvelle image qui remplacera l’image existante. <p>Les images sont répertoriées dans l’ordre dans lequel elles apparaissent dans le document. Par exemple : <code>Body: Image No. 1</code> est la première image du document.</p> </td> 
  </tr> 
 </tbody> 
</table>
</table>

#### [!UICONTROL Surveiller des documents]

Ce module de déclenchement renvoie les détails du document lorsqu’un nouveau document est créé ou modifié dans le dossier sélectionné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch Documents]</td> 
   <td> <p style="color: #000000;">Indiquez si vous souhaitez surveiller les documents créés ([!UICONTROL By Created Date]) ou modifiés ([!UICONTROL By Modified Date]).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Sélectionnez le type de lecteur à surveiller.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Sélectionnez le dossier à surveiller pour les documents créés ou modifiés.</p> </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p>Sélectionnez le dossier à surveiller pour les documents créés ou modifiés.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (disponible pour les utilisateurs et utilisatrices de [!DNL Google Workspace] uniquement)</p> <p>Indiquez si vous souhaitez [!UICONTROL Use Domain Admin Access]. Si vous sélectionnez [!UICONTROL Yes], la requête est émise en tant qu’administrateur ou administratrice de domaine et tous les lecteurs partagés administrés par la personne effectuant la requête seront renvoyés.</p> <p>Sélectionnez le lecteur partagé que vous souhaitez surveiller.</p> <p>Note : si vous avez sélectionné l’option [!DNL Google Shared Drive] dans ce champ et que vous n’êtes pas un utilisateur ou une utilisatrice de [!DNL Google Workspace], l’erreur <code>[400] Invalid Value</code> est renvoyée.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Définissez le nombre maximal de documents que Workfront Fusion renvoie dans un cycle d’exécution.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Autre

* [[!UICONTROL Rendre tous les liens d’un document cliquables]](#make-all-links-in-a-document-clickable)
* [[!UICONTROL Effectuer un appel API]](#make-an-api-call)

#### [!UICONTROL Rendre tous les liens d’un document cliquables]

Ce module d’action recherche tous les liens du document et les rend cliquables.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Make All Links in a Document]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>Sélectionnez cette option pour mapper le modèle de document.</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> <br> Sélectionnez cette option pour sélectionner le document dans le menu déroulant.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Drive]</td> 
   <td> <p>Sélectionnez le type de lecteur sur lequel se trouve le document dans lequel vous souhaitez que les liens soient cliquables. Cette option est disponible si vous avez sélectionné [!UICONTROL By Dropdown] dans le champ précédent.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL My Drive]</strong> </p> <p>Sélectionnez le dossier dans lequel se trouve le document dans lequel vous souhaitez rendre les liens cliquables.</p> </li> 
     <li> <p><strong>[!UICONTROL Shared With Me]</strong> </p> <p>Sélectionnez le dossier dans lequel se trouve le document dans lequel vous souhaitez rendre les liens cliquables.</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google] Shared Drive]</strong> (disponible pour les utilisateurs et les utilisatrices de [!DNL Google Workspace] uniquement)</p> <p>Indiquez si vous souhaitez [!UICONTROL Use Domain Admin Access]. Si vous sélectionnez [!UICONTROL Yes], la requête est émise en tant qu’administrateur ou administratrice de domaine et tous les lecteurs partagés administrés par la personne effectuant la requête seront renvoyés.</p> <p>Sélectionnez le lecteur partagé sur lequel se trouve le document dans lequel vous souhaitez que les liens puissent être cliquables, puis sélectionnez le document.</p> <p>Remarque : si vous avez sélectionné l’option [!DNL Google Docs] dans ce champ et que vous n’êtes pas un utilisateur ou une utilisatrice de [!DNL Google Workspace], l’erreur <code>[400] Invalid Value</code> est renvoyée.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Shared Drive]</td> 
   <td> <p>Sélectionnez le lecteur contenant le document dans lequel vous souhaitez mettre à jour les liens, puis sélectionnez un document. Cette option est disponible si vous avez sélectionné [!DNL My Drive] dans le champ [!UICONTROL Choose a Drive field].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Document ID]</td> 
   <td> <p> Sélectionnez ou mappez le document dans lequel vous souhaitez mettre à jour les liens.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Effectuer un appel API]

Ce module d’action vous permet d’effectuer un appel API personnalisé.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Saisissez un chemin relatif vers <code>https://docs.googleapis.com/</code>. Exemple : <code>/v1/documents/{presentationID}</code>. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Méthodes de requête HTTP</a>.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard. Par exemple, <code>{"Content-type":"application/json"}</code>. Workfront Fusion ajoute les en-têtes d’autorisation pour vous.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Saisissez la chaîne de requête.</p> </td> 
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

>[!BEGINSHADEBOX]

**Exemple :** l’appel API suivant récupère les détails du document spécifié dans Google Docs :

**URL :**

/v1/documents/1ujkf-GDgB0TQSYPrxbCSK4Uso54tHVMqHZEVZZxB6aY

**Méthode :**

[!UICONTROL GET]

![Exemple d’appel API](/help/workfront-fusion/references/apps-and-modules/assets/api-call-example.png)

Les détails du document récupéré se trouvent dans la sortie du module sous [!UICONTROL Lot] > [!UICONTROL Corps].

![Sortie d’appel API](/help/workfront-fusion/references/apps-and-modules/assets/api-output.png)

>[!ENDSHADEBOX]
