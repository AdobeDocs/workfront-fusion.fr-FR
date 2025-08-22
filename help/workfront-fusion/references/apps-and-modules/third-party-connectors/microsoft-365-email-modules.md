---
title: Messagerie e-mail Microsoft Office 365
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent la messagerie Microsoft Office 365 et les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: 5d4072ba-c598-4347-a42f-c59c7add0a1b
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2915'
ht-degree: 47%

---

# Modules [!DNL Microsoft Office 365 Email]

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent [!UICONTROL Microsoft Office 365 Email] et les connecter à plusieurs applications et services tiers.

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

Pour utiliser les modules [!DNL Microsoft Office 365 Email], vous devez disposer d’un compte [!DNL Microsoft Office 365 Email].

## Informations sur l’API de messagerie Microsoft Office 365

Le connecteur de messagerie Microsoft Office 365 utilise les éléments suivants :

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
   <td>v2.6.5</td> 
  </tr>
 </tbody> 
 </table>

## Connexion du service [!DNL Office 365 Email] à Workfront Fusion

Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365 Email] à [!UICONTROL Workfront Fusion], voir [Créer une connexion à [!UICONTROL Adobe Workfront Fusion] : instructions de base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Certaines applications Microsoft utilisent la même connexion, qui est liée à des autorisations d’utilisateur ou d’utilisatrice. Ainsi, lors de la création d’une connexion, l’écran de consentement aux autorisations affiche les autorisations précédemment accordées à la connexion de cet utilisateur ou de cette utilisatrice, en plus des nouvelles autorisations nécessaires à l’application actuelle.
>
>Par exemple, si un utilisateur ou une utilisatrice dispose d’autorisations « Lire le tableau » accordées via le connecteur Excel, puis crée une connexion dans le connecteur Outlook pour lire les e-mails, l’écran de consentement aux autorisations affiche à la fois l’autorisation « Lire le tableau » déjà accordée et l’autorisation « Écrire des e-mails » nouvellement requise.

## Modules [!DNL Microsoft Office 365 Email] et leurs champs

Lorsque vous configurez les modules [!DNL Microsoft Office 365 Email], Workfront Fusion affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Microsoft Office 365 Email] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Message](#message)
* [Brouillon de message](#draft-message)
* [Pièce jointe](#attachment)
* [Autre](#other)

### Message

* [[!UICONTROL Création et envoi d’un message (hérité)]](#create-and-send-a-message)
* [[!UICONTROL Supprimer un message]](#delete-a-message)
* [[!UICONTROL Recevoir un message]](#get-a-message)
* [[!UICONTROL Déplacer un message]](#move-a-message)
* [[!UICONTROL Rechercher des messages]](#search-messages)
* [[!UICONTROL Surveiller les messages]](#watch-messages)



#### [!UICONTROL Création et envoi d’un message (hérité)]

Ce module d’action crée et envoie un e-mail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>Saisissez ou mappez l’objet du message.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td> <p>Saisissez ou mappez le texte du corps de l’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>Sélectionnez l’importance de l’e-mail</p> 
    <ul> 
     <li>[!UICONTROL Low]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL High]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL To Recipients]</p> </td> 
   <td> <p>Pour chaque destinataire auquel vous souhaitez envoyer l’e-mail, cliquez sur <b>Ajouter un élément</b> et saisissez les informations suivantes :</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Saisissez l’adresse e-mail du contact.</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Saisissez le nom du contact.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Recipients]</p> </td> 
   <td> <p><p>Pour chaque destinataire auquel vous souhaitez envoyer une copie de l’e-mail, cliquez sur <b>Ajouter un élément</b> et saisissez les informations suivantes :</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Saisissez l’adresse e-mail du contact.</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Saisissez le nom du contact.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Bcc Recipients]</p> </td> 
   <td> <p>Pour chaque destinataire auquel vous souhaitez envoyer une copie de l’e-mail, sans permettre à d’autres destinataires de voir son nom ou son adresse e-mail, cliquez sur <b>Ajouter un élément</b> et saisissez les informations suivantes :</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Saisissez l’adresse e-mail du contact.</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Saisissez le nom du contact.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>Pour chaque pièce jointe que vous souhaitez ajouter à l’e-mail, cliquez sur <b>Ajouter un élément</b> et saisissez les informations suivantes :</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Source file]</strong> </p> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Internet Message Headers]</td> 
   <td> <p>Pour chaque en-tête que vous souhaitez ajouter à l’e-mail, cliquez sur <b>Ajouter un élément</b> et saisissez les informations suivantes :</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Saisir le nom de l’en-tête</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Saisissez une valeur pour l’en-tête.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Supprimer un message]

Ce module d’action supprime un e-mail existant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adresse e-mail de l’expéditeur]</td> 
   <td> <p> Pour utiliser une adresse e-mail partagée, saisissez l’adresse ici. L’utilisateur dont les informations d’identification sont utilisées dans la connexion utilisée pour ce module doit avoir accès au dossier partagé.<p>Laissez ce champ vide pour utiliser l’adresse e-mail du propriétaire de la connexion.</p></p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Message ID]</td> 
   <td> <p> Sélectionnez ou mappez l’ID du message que vous souhaitez supprimer.</p> </td> 
  </tr> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Recevoir un message]

Ce module d’action récupère les métadonnées d’un message spécifique

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adresse e-mail de l’expéditeur]</td> 
   <td> <p> Pour utiliser une adresse e-mail partagée, saisissez l’adresse ici. L’utilisateur dont les informations d’identification sont utilisées dans la connexion utilisée pour ce module doit avoir accès au dossier partagé.<p>Laissez ce champ vide pour utiliser l’adresse e-mail du propriétaire de la connexion.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID]</td> 
   <td> <p> Sélectionnez ou mappez l’ID du message pour lequel vous souhaitez récupérer les métadonnées.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get MIME contents]</td> 
   <td>Activez cette option pour récupérer des données sur le contenu MIME du message. Le contenu [!UICONTROL MIME] peut comprendre des images, des fichiers audio et vidéo ou d’autres types de fichiers.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Déplacer un message]

Ce module d&#39;action déplace un e-mail vers un dossier sélectionné dans la boîte aux lettres.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID]</td> 
   <td> <p> Sélectionnez ou mappez l’ID du message que vous souhaitez déplacer vers un autre dossier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mail Folder] </td> 
   <td> <p>Sélectionnez ou mappez l’ID du dossier dans lequel vous souhaitez déplacer le message.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Rechercher des messages]

Ce module de recherche recherche les messages en fonction de critères spécifiques.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Adresse e-mail de l’expéditeur]</td> 
   <td> <p> Pour utiliser une adresse e-mail partagée, saisissez l’adresse ici. L’utilisateur dont les informations d’identification sont utilisées dans la connexion utilisée pour ce module doit avoir accès au dossier partagé.<p>Laissez ce champ vide pour utiliser l’adresse e-mail du propriétaire de la connexion.</p></p> </td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL Mail Folder]</td> 
   <td> <p>Sélectionnez le dossier qui contient les messages dans lesquels effectuer la recherche.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search]</td> 
   <td>Saisissez votre requête de recherche. Pour plus d’informations sur la manière d’écrire une requête de recherche, voir l’article de support [!DNL Microsoft] <a href="https://support.microsoft.com/en-us/office/search-mail-and-people-in-outlook-com-88108edf-028e-4306-b87e-7400bbb40aa7?ui=en-us&amp;rs=en-us&amp;ad=us">Rechercher des courriers et des personnes dans [!DNL Outlook.com]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
   <td> <p>Sélectionnez la façon dont vous souhaitez classer les résultats :</p> 
    <ul> 
     <li>[!UICONTROL Subject (Ascending or descending)]</li> 
     <li>[!UICONTROL Created Date Time (Ascending or descending)]</li> 
     <li>[!UICONTROL Last Modified Date Time (Ascending or descending)]</li> 
     <li>[!UICONTROL Received Date Time (Ascending or descending)]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez le nombre maximal de messages que Workfront Fusion doit renvoyer au cours d’un cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Surveiller les messages]

Ce module de déclenchement lance un scénario lorsqu’un nouvel e-mail est envoyé ou reçu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Watch Messages]</p> </td> 
   <td> <p>Sélectionnez les messages que vous souhaitez surveiller :</p> 
    <ul> 
     <li>[!UICONTROL Only Unread]</li> 
     <li>[!UICONTROL Only read]</li> 
     <li>[!UICONTROL All]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mail Folder]</td> 
   <td> <p>Sélectionnez le dossier qui contient les messages que vous voulez surveiller.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search]</td> 
   <td>Saisissez votre requête de recherche. Le module renvoie les messages qui correspondent à cette requête. Pour plus d’informations sur la manière d’écrire une requête de recherche, voir l’article de support [!DNL Microsoft] <a href="https://support.microsoft.com/en-us/office/search-mail-and-people-in-outlook-com-88108edf-028e-4306-b87e-7400bbb40aa7?ui=en-us&amp;rs=en-us&amp;ad=us">Rechercher des courriers et des personnes dans [!DNL Outlook.com]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Saisissez le nombre maximal de messages que Workfront Fusion doit renvoyer au cours d’un cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Brouillon de message

* [Créer un brouillon de message](#create-a-draft-message)
* [Envoyer un brouillon de message](#send-a-draft-message)
* [Mettre à jour un message](#update-a-message)

#### [!UICONTROL Créer un brouillon de message]

Ce module d’action crée un e-mail en tant que brouillon.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>Saisissez l’objet du message.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body Content Type]</td> 
   <td>Choisissez le format du corps du message : HTML ou texte.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td> <p>Saisissez ou mappez le texte du corps de l’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>Sélectionnez l’importance de l’e-mail</p> 
    <ul> 
     <li>[!UICONTROL Low]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL High]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL To Recipients]</p> </td> 
   <td> <p>Pour chaque destinataire auquel vous souhaitez envoyer l’e-mail, cliquez sur <b>Ajouter un élément</b> et saisissez les informations suivantes :</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Saisissez l’adresse e-mail du contact.</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Saisissez le nom du contact.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Recipients]</p> </td> 
   <td> <p><p>Pour chaque destinataire auquel vous souhaitez envoyer une copie de l’e-mail, cliquez sur <b>Ajouter un élément</b> et saisissez les informations suivantes :</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Saisissez l’adresse e-mail du contact.</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Saisissez le nom du contact.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Bcc Recipients]</p> </td> 
   <td> <p>Pour chaque destinataire auquel vous souhaitez envoyer une copie de l’e-mail, sans permettre à d’autres destinataires de voir son nom ou son adresse e-mail, cliquez sur <b>Ajouter un élément</b> et saisissez les informations suivantes :</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Saisissez l’adresse e-mail du contact.</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Saisissez le nom du contact.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>Pour chaque pièce jointe que vous souhaitez ajouter à l’e-mail, cliquez sur <b>Ajouter un élément</b> et saisissez les informations suivantes :</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Source file]</strong> </p> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adresse e-mail de l’expéditeur]</td> 
   <td> <p> Pour utiliser une adresse e-mail partagée, saisissez l’adresse ici. L’utilisateur dont les informations d’identification sont utilisées dans la connexion utilisée pour ce module doit avoir accès au dossier partagé.<p>Laissez ce champ vide pour utiliser l’adresse e-mail du propriétaire de la connexion.</p></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Envoyer un brouillon de message]

Ce module d’action envoie un e-mail qui est actuellement dans le brouillon.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adresse e-mail de l’expéditeur]</td> 
   <td> <p> Pour utiliser une adresse e-mail partagée, saisissez l’adresse ici. L’utilisateur dont les informations d’identification sont utilisées dans la connexion utilisée pour ce module doit avoir accès au dossier partagé.<p>Laissez ce champ vide pour utiliser l’adresse e-mail du propriétaire de la connexion.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Draft Message ID]</td> 
   <td> <p> Sélectionnez ou mappez l’ID de message du brouillon que vous souhaitez envoyer.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mettre à jour un message]

Ce module d&#39;action met à jour un message existant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adresse e-mail de l’expéditeur]</td> 
   <td> <p> Pour utiliser une adresse e-mail partagée, saisissez l’adresse ici. L’utilisateur dont les informations d’identification sont utilisées dans la connexion utilisée pour ce module doit avoir accès au dossier partagé.<p>Laissez ce champ vide pour utiliser l’adresse e-mail du propriétaire de la connexion.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a message ID]</td> 
   <td> <p>Sélectionnez la manière dont vous souhaitez identifier le message à mettre à jour :</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter Manually]</strong> </p> <p>Saisissez ou mappez l’ID du message.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le dossier qui contient le message que vous souhaitez mettre à jour, puis sélectionnez le message.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>Saisissez l’objet du message.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td> <p>Saisissez le texte du corps du message.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>Sélectionnez l’importance de l’e-mail</p> 
    <ul> 
     <li>[!UICONTROL Low]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL High]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL To Recipients]</p> </td> 
   <td> <p>Pour chaque destinataire auquel vous souhaitez envoyer l’e-mail, cliquez sur <b>Ajouter un élément</b> et saisissez les informations suivantes :</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Saisissez l’adresse e-mail du contact.</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Saisissez le nom du contact.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Recipients]</p> </td> 
   <td> <p><p>Pour chaque destinataire auquel vous souhaitez envoyer une copie de l’e-mail, cliquez sur <b>Ajouter un élément</b> et saisissez les informations suivantes :</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Saisissez l’adresse e-mail du contact.</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Saisissez le nom du contact.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Bcc Recipients]</p> </td> 
   <td> <p>Pour chaque destinataire auquel vous souhaitez envoyer une copie de l’e-mail, sans permettre à d’autres destinataires de voir son nom ou son adresse e-mail, cliquez sur <b>Ajouter un élément</b> et saisissez les informations suivantes :</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Saisissez l’adresse e-mail du contact.</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Saisissez le nom du contact.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>Pour chaque pièce jointe que vous souhaitez ajouter à l’e-mail, cliquez sur <b>Ajouter un élément</b> et saisissez les informations suivantes :</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Source file]</strong> </p> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mark it as Read]</td> 
   <td>Activez cette option pour marquer le message mis à jour comme lu.</td> 
  </tr> 
 </tbody> 
</table>

### Pièce jointe

* [[!UICONTROL Télécharger une pièce jointe]](#download-an-attachment)
* [[!UICONTROL Répertorier les pièces jointes]](#list-attachments)

#### [!UICONTROL Télécharger une pièce jointe]

Ce module télécharge la pièce jointe spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adresse e-mail de l’expéditeur]</td> 
   <td> <p> Pour utiliser une adresse e-mail partagée, saisissez l’adresse ici. L’utilisateur dont les informations d’identification sont utilisées dans la connexion utilisée pour ce module doit avoir accès au dossier partagé.<p>Laissez ce champ vide pour utiliser l’adresse e-mail du propriétaire de la connexion.</p></p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Message ID]</td> 
   <td> <p> Sélectionnez ou mappez l’ID du message qui contient la pièce jointe que vous souhaitez télécharger.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Attachment ID]</td> 
   <td> <p>Saisissez ou mappez l’identifiant de la pièce jointe que vous souhaitez télécharger. Vous pouvez localiser cette idée à l’aide du module Pièces jointes de la liste .</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Répertorier les pièces jointes]

Ce module permet de récupérer une liste de pièces jointes appartenant au message spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adresse e-mail de l’expéditeur]</td> 
   <td> <p> Pour utiliser une adresse e-mail partagée, saisissez l’adresse ici. L’utilisateur dont les informations d’identification sont utilisées dans la connexion utilisée pour ce module doit avoir accès au dossier partagé.<p>Laissez ce champ vide pour utiliser l’adresse e-mail du propriétaire de la connexion.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID]</td> 
   <td> <p> Sélectionnez ou mappez l’ID du message dont vous souhaitez récupérer les pièces jointes.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum de pièces jointes que vous souhaitez que le module renvoie au cours de chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Autre

* [[!UICONTROL Ajouter une pièce jointe]](#add-an-attachment)
* [Créer et envoyer un message](#create-and-send-a-message)
* [[!UICONTROL Effectuer un appel API]](#make-an-api-call)

#### [!UICONTROL Ajouter une pièce jointe]

Ce module permet d’ajouter une pièce jointe volumineuse à un message.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adresse e-mail de l’expéditeur]</td> 
   <td> <p> Pour utiliser une adresse e-mail partagée, saisissez l’adresse ici. L’utilisateur dont les informations d’identification sont utilisées dans la connexion utilisée pour ce module doit avoir accès au dossier partagé.<p>Laissez ce champ vide pour utiliser l’adresse e-mail du propriétaire de la connexion.</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID]</td> 
   <td> <p> Sélectionnez ou mappez l’ID du message auquel vous souhaitez ajouter une pièce jointe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Créer et envoyer un message]

Ce module d’action crée et envoie un e-mail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>Saisissez ou mappez l’objet du message.</p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td> <p>Saisissez ou mappez le texte du corps de l’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>Sélectionnez l’importance de l’e-mail</p> 
    <ul> 
     <li>[!UICONTROL Low]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL High]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL To Recipients]</p> </td> 
   <td> <p>Pour chaque destinataire auquel vous souhaitez envoyer l’e-mail, cliquez sur <b>Ajouter un élément</b> et saisissez les informations suivantes :</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Saisissez l’adresse e-mail du contact.</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Saisissez le nom du contact.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Recipients]</p> </td> 
   <td> <p><p>Pour chaque destinataire auquel vous souhaitez envoyer une copie de l’e-mail, cliquez sur <b>Ajouter un élément</b> et saisissez les informations suivantes :</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Saisissez l’adresse e-mail du contact.</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Saisissez le nom du contact.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Bcc Recipients]</p> </td> 
   <td> <p>Pour chaque destinataire auquel vous souhaitez envoyer une copie de l’e-mail, sans permettre à d’autres destinataires de voir son nom ou son adresse e-mail, cliquez sur <b>Ajouter un élément</b> et saisissez les informations suivantes :</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Saisissez l’adresse e-mail du contact.</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Saisissez le nom du contact.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>Pour chaque pièce jointe que vous souhaitez ajouter à l’e-mail, cliquez sur <b>Ajouter un élément</b> et saisissez les informations suivantes :</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Source file]</strong> </p> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Internet Message Headers]</td> 
   <td> <p>Ajouter les en-têtes du message.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Saisir le nom de l’en-tête</p> </li> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>Saisissez une valeur pour l’en-tête.</p> </li> 
    </ul> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Adresse e-mail de l’expéditeur]</td> 
   <td> <p> Pour utiliser une adresse e-mail partagée, saisissez l’adresse ici. L’utilisateur dont les informations d’identification sont utilisées dans la connexion utilisée pour ce module doit avoir accès au dossier partagé.<p>Laissez ce champ vide pour utiliser l’adresse e-mail du propriétaire de la connexion.</p></p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</td> 
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
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Saisissez un chemin relatif à <code>https://graph.microsoft.com</code>. Exemple :<code> /v1.0/me/messages</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   td&gt; <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lors de l’utilisation d’instructions conditionnelles telles que <code>if</code> dans votre fichier JSON, placez les guillemets en dehors de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>
