---
title: Modules e-mail
description: Dans un scénario Adobe Workfront Fusion, vous pouvez connecter votre compte de messagerie à plusieurs applications et services tiers. Vous pouvez ainsi télécharger des e-mails via IMAP, envoyer des e-mails via SMTP, créer de nouveaux brouillons, déplacer et copier des e-mails d'un dossier vers un autre, marquer les e-mails comme lus ou non lus et supprimer des e-mails.
author: Becky
feature: Workfront Fusion
exl-id: 28a04bad-d3ef-4f3a-be93-8b04761a75e4
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '2491'
ht-degree: 61%

---

# Modules e-mail

Dans un scénario Adobe Workfront Fusion, vous pouvez connecter votre compte de messagerie à plusieurs applications et services tiers. Vous pouvez ainsi télécharger des e-mails via IMAP, envoyer des e-mails via SMTP, créer de nouveaux brouillons, déplacer et copier des e-mails d&#39;un dossier vers un autre, marquer les e-mails comme lus ou non lus et supprimer des e-mails.

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tout package de workflow Adobe Workfront et tout package d’automatisation et d’intégration Adobe Workfront</p><p>Workfront Ultimate</p><p>les packages Workfront Prime et Select, avec un achat supplémentaire de Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licences Adobe Workfront</td> 
   <td> <p>Standard</p><p>Travail ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licence Adobe Workfront Fusion</td> 
   <td>
   <p>Basé sur les opérations : aucune exigence de licence Workfront Fusion</p>
   <p>Basé sur un connecteur (hérité) : Workfront Fusion pour l’automatisation et l’intégration du travail </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Si votre entreprise dispose d’un package Select ou Prime Workfront qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acheter Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Connecter votre e-mail à Workfront Fusion {#connect-your-email-to-workfront-fusion}

* [Se connecter à Google](#connect-to-google)
* [Se connecter à d’autres services de messagerie (IMAP)](#connect-to-other-email-services-smap)

### Se connecter à [!DNL Google]

Utilisez cette option pour créer des scénarios avec des modules de messagerie qui nécessitent une connexion à votre compte [!DNL Google]. Il s’agit d’un compte avec des portées restreintes.

Vous pouvez créer une connexion à votre compte [!DNL Google] directement depuis un module d’e-mail.

1. Dans n’importe quel module d’e-mail, cliquez sur **[!UICONTROL Ajouter]** en regard du champ [!UICONTROL Connexion].
1. Sélectionnez **[!DNL Google]** comme type de connexion.
1. Saisissez un nom pour la connexion.
1. (Facultatif) Saisissez votre ID client [!UICONTROL [!DNL Google]] et votre [!UICONTROL Secret client].
1. Cliquez sur **[!UICONTROL Continuer]** pour créer la connexion et revenir au module.

### Se connecter à d’autres services de messagerie (IMAP)

La connexion IMAP vous permet d&#39;accéder à votre boîte aux lettres à distance et de lire ou manipuler des messages dans votre boîte aux lettres. La connexion IMAP est utilisée par la plupart des modules de messagerie.

1. Dans n’importe quel module d’e-mail, cliquez sur **[!UICONTROL Ajouter]** en regard du champ [!UICONTROL Connexion].
1. Sélectionnez **[!UICONTROL Autres (SMTP)]** comme type de connexion.
1. Saisissez un **[!UICONTROL nom]** pour la connexion.
1. Sélectionnez votre **[!UICONTROL fournisseur de messagerie]** dans la liste. Si votre fournisseur de messagerie ne figure pas dans la liste, sélectionnez Autre.
1. Saisissez le **[!UICONTROL Nom d’utilisateur]** et votre **[!UICONTROL Mot de passe]** pour le compte de messagerie.
1. (Le cas échéant) Si votre fournisseur ne figure pas sur la liste, saisissez votre **[!UICONTROL Serveur SMTP]** et le **[!UICONTROL Port]**, puis indiquez si vous souhaitez **[!UICONTROL Utiliser une connexion sécurisée (TLS)]**. Pour trouver ces informations, consultez la section [!UICONTROL Aide] de votre messagerie. Si vous ne disposez pas de ces informations, contactez votre fournisseur de services de messagerie.
1. Pour utiliser un certificat auto-signé, activez l’option **Rejeter les certificats non autorisés** et chargez votre certificat auto-signé. Pour obtenir des instructions, voir [Charger un certificat auto-signé](#upload-a-self-signed-certificate)
1. Cliquez sur **[!UICONTROL Continuer]** pour créer la connexion et retourner au module.

#### Charger un certificat auto-signé

Pour ajouter un certificat auto-signé :

1. Cliquez sur **Extraire**.
1. Sélectionnez le type de fichier que vous extrayez.
1. Sélectionnez le fichier contenant le certificat ou .
1. Saisissez le mot de passe du fichier.
1. Cliquez sur **Enregistrer** pour extraire le fichier et revenir à la configuration du module.

## Modules [!UICONTROL E-mail] et leurs champs

Lorsque vous configurez les modules [!UICONTROL E-mail], Workfront Fusion affiche les champs répertoriés ci-dessous. En plus de cela, des champs supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Certains champs de l’e-mail peuvent déjà contenir des données si vous les avez utilisées dans un autre module dans le scénario. Consultez la documentation d’aide à propos des e-mails si vous avez besoin d’informations à leur sujet.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>L’identifiant unique d’e-mail appelé « [!UICONTROL Identifiant e-mail (UID)] » est l’identifiant de l’e-mail. L’identifiant e-mail est spécifique à chacun des dossiers de l’e-mail.

* [Déclencheurs](#triggers)
* [Actions](#actions)
* [Itérateurs](#iterators)

### Déclencheurs

#### [!UICONTROL Surveiller des e-mails]

Ce module de déclenchement lance un scénario lorsqu’un nouvel e-mail est reçu pour traitement en fonction de critères spécifiés.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur la procédure de connexion de votre compte de messagerie à [!UICONTROL Workfront Fusion], voir <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connecter votre e-mail à [!UICONTROL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] </td> 
   <td> <p>Sélectionnez le dossier qui contient les e-mails que vous souhaitez surveiller.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Criteria]</p> </td> 
   <td> <p>Sélectionnez les critères de surveillance des e-mails :</p> 
    <ul> 
     <li>[!UICONTROL All Emails]</li> 
     <li>[!UICONTROL Only Read Emails]</li> 
     <li>[!UICONTROL Only Unread Emails]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sender Email Address] </td> 
   <td> <p>Saisissez l’adresse e-mail de l’expéditeur ou de l’expéditrice dont vous souhaitez surveiller les e-mails.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Saisissez l’objet de l’e-mail que vous souhaitez surveiller.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Phrase] </td> 
   <td> <p>Saisissez des mots-clés pour n’observer que les e-mails les contenant.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mark message(s) as read when fetched]</td> 
   <td> <p>Activez cette option pour marquer l’e-mail non lu comme lu après en avoir récupéré les détails.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of results]</td> 
   <td> <p> Saisissez ou mappez le nombre maximal d’e-mails que Workfront Fusion doit renvoyer au cours d’un cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [[!UICONTROL Copier un e-mail]](#copy-an-email)
* [[!UICONTROL Créer un brouillon]](#create-a-draft)
* [[!UICONTROL Supprimer un e-mail]](#delete-an-email)
* [[!UICONTROL Obtenir des e-mails]](#get-emails)
* [[!UICONTROL Marquer un e-mail comme lu]](#mark-an-email-as-read)
* [[!UICONTROL Marquer un e-mail comme non lu]](#mark-an-email-as-unread)
* [[!UICONTROL Déplacer un e-mail]](#move-an-email)
* [[!UICONTROL Envoyer un e-mail]](#send-an-email)

#### [!UICONTROL Copier un e-mail]

Ce module d’action copie un e-mail ou un brouillon dans un dossier sélectionné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur la procédure de connexion de votre compte de messagerie à [!UICONTROL Workfront Fusion], voir <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connecter votre e-mail à [!UICONTROL Workfront Fusion]</a> dans cet article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Folder]</td> 
   <td>Sélectionnez le dossier dans lequel vous souhaitez copier l’e-mail. Exemple : dossier Principal.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination Folder]</td> 
   <td> <p> Sélectionnez le dossier dans lequel vous souhaitez copier l’e-mail. Exemple : dossier Travail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Saisissez l’UID de l’e-mail que vous souhaitez copier dans le dossier de destination.</p> <p>Vous pouvez obtenir l’UID de l’e-mail à l’aide du module [!UICONTROL Email] &gt; [!UICONTROL Watch Email] ou du module [!UICONTROL Search Email].</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Créer un brouillon]

Ce module d’action crée et ajoute un nouveau brouillon à un dossier sélectionné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur la procédure de connexion de votre compte de messagerie à [!UICONTROL Workfront Fusion], voir <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connecter votre e-mail à [!UICONTROL Workfront Fusion]</a> dans cet article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Sélectionnez le dossier dans lequel vous souhaitez créer le brouillon de l’e-mail.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL To] </td> 
   <td> <p>Saisissez ou mappez l’adresse e-mail à laquelle vous souhaitez envoyer l’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Saisissez ou mappez l’objet de l’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content] </td> 
   <td> <p>Saisissez ou mappez le contenu de l’e-mail au format HTML à l’aide des balises HTML ou en texte brut.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>Pour chaque pièce jointe à ajouter, cliquez sur <b>Ajouter un élément</b> et saisissez les informations suivantes :</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File name]</strong> </p> <p>Saisissez le nom du fichier, y compris son extension. </p> </li> 
     <li> <p><strong>[!UICONTROL Data]</strong> </p> <p>Saisissez le chemin d’accès au dossier dans lequel vous souhaitez charger la pièce jointe.</p> </li> 
     <li> <p><strong>[!UICONTROL Content-ID]</strong> </p> <p>Saisissez l’identifiant du contenu pour insérer la pièce jointe (image) dans le contenu.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy Recipient] </td> 
   <td> <p>Pour chaque adresse e-mail à laquelle vous souhaitez envoyer une copie de cet e-mail, cliquez sur <b>Ajouter un élément</b> et saisissez l’adresse e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blind Copy Recipient]</td> 
   <td> <p> Pour chaque adresse e-mail à laquelle vous souhaitez envoyer une copie de cet e-mail sans que l’adresse e-mail n’apparaisse dans l’e-mail, cliquez sur <b>Ajouter un élément</b> et saisissez l’adresse e-mail.</p> </td> 
  </tr> 
  <!--<tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL From] </td> 
   <td> <p>Enter or map the email address (and name, if needed) that appears in the [!UICONTROL From] field in the email. </p> <p>Important: Use the correct syntax: <code>name@email.com</code> or <code>"Name" name@email.com</code>.</p> <p>Note:  Normally, Workfront Fusion uses the email address that you entered when creating the connection as the sender address. If you enter any other email address, an error may occur when sending a message because your account may not have permission to send emails from a different address than your own. E.g. <code>test@mail.com</code> or "<code>John Bush" test@email.com</code>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Sender]</p> </td> 
   <td> <p>Enter or map the email address that appears in the [!UICONTROL Sender] field in the email.</p> <p>Tip:  If you are unsure whether to use this field or the From field, we recommend choosing the From field.</p> <p>Important: Use the correct syntax: <code>name@email.com</code> or <code>"Name" name@email.com</code></p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Reply-To]</td> 
   <td> <p> If you want replies to this email sent to a different address than the "[!UICONTROL from]" address, enter the email address where you want replies to this email sent.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL In-Reply-To]</td> 
   <td> <p> If you are replying to a specific email, enter or map the ID of the email you are replying to.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL References] </td> 
   <td> <p>Enter the message IDs of all the replies in the thread.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Priority]</p> </td> 
   <td> <p>Select the priority of the email:</p> 
    <ul> 
     <li>[!UICONTROL High]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL Low]</li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Headers]</p> </td> 
   <td> <p>Add the headers:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Key]</strong> </p> <p>Add the key. For example, Sender, Date, To, and so on.</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Enter the value for the key.</p> </li> 
    </ul> </td> 
  </tr> -->
 </tbody> 
</table>

#### [!UICONTROL Supprimer un e-mail]

Ce module d’action supprime un e-mail ou un brouillon du dossier sélectionné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur la procédure de connexion de votre compte de messagerie à [!UICONTROL Workfront Fusion], voir <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connecter votre e-mail à [!UICONTROL Workfront Fusion]</a> dans cet article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Sélectionnez le dossier contenant l’e-mail à supprimer.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Saisissez l’UID de l’e-mail que vous souhaitez supprimer.</p> <p>Vous pouvez obtenir l’UID de l’e-mail à l’aide du module E-mail &gt; Observer l’e-mail ou du module [!UICONTROL Search Email].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expunge]</td> 
   <td> <p>Activez cette option pour supprimer définitivement tous les messages marqués comme [!UICONTROL Deleted] dans la boîte aux lettres actuellement ouverte.</p> <p>Remarque : dans [!DNL Gmail], ce comportement est piloté par le paramètre dans la section [!UICONTROL Settings] &gt;[!UICONTROL Forwarding POP/IMAP in IMAP access].</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obtenir des e-mails]

Ce module renvoie les e-mails qui correspondent aux critères spécifiés.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur la procédure de connexion de votre compte de messagerie à [!UICONTROL Workfront Fusion], voir <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connecter votre e-mail à [!UICONTROL Workfront Fusion]</a> dans cet article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] </td> 
   <td> <p>Sélectionnez le dossier contenant les e-mails que vous souhaitez récupérer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mark message(s) as read when fetched] </td> 
   <td> <p>Activez cette option si vous souhaitez marquer l’e-mail non lu comme lu après en avoir récupéré les détails.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Criteria]</p> </td> 
   <td> <p>Sélectionnez les critères des e-mails que vous souhaitez récupérer :</p> 
    <ul> 
     <li>[!UICONTROL All Emails]</li> 
     <li>[!UICONTROL Only Read Emails]</li> 
     <li>[!UICONTROL Only Unread Emails]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sender Email Address] </td> 
   <td> <p>Saisissez ou mappez l’adresse e-mail de l’expéditeur ou de l’expéditrice dont vous souhaitez récupérer les e-mails.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Recipient Email]</td> 
   <td> <p> Saisissez ou mappez l’adresse e-mail de la personne destinataire dont vous souhaitez récupérer les e-mails.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From date] </td> 
   <td> <p>Saisissez ou mappez une date pour récupérer les e-mails traités à la date spécifiée ou après celle-ci.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Before date]</td> 
   <td> <p> Saisissez ou mappez une date pour récupérer les e-mails traités à la date spécifiée ou avant celle-ci.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Saisissez ou mappez l’objet de l’e-mail que vous souhaitez récupérer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Phrase] </td> 
   <td> <p>Saisissez ou mappez des mots-clés pour récupérer uniquement les e-mails contenant ces mots-clés.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email ID (UID)]</td> 
   <td> <p> Saisissez l’identifiant d’e-mail (UID) de l’adresse e-mail dont vous souhaitez récupérer les détails.</p> <p>Vous pouvez obtenir l’UID de l’e-mail à l’aide du module [!UICONTROL Watch Email] ou du module [!UICONTROL Search Email] de Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of results]</td> 
   <td> <p> Le nombre maximal d’e-mails que Workfront Fusion doit renvoyer au cours d’un cycle d’exécution de scénario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Continue the execution of the route even if the module returns no results]</td> 
   <td> <p> Sélectionnez cette option si vous souhaitez continuer à exécuter le module même si aucun résultat n’est renvoyé.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Marquer un e-mail comme lu]

Ce module d&#39;action marque un email ou un brouillon dans un dossier sélectionné comme lu, en définissant l&#39;indicateur [!UICONTROL Read].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur la procédure de connexion de votre compte de messagerie à [!UICONTROL Workfront Fusion], voir <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connecter votre e-mail à [!UICONTROL Workfront Fusion]</a> dans cet article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Sélectionnez le dossier contenant l’e-mail que vous souhaitez marquer comme lu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Saisissez l’UID de l’e-mail que vous souhaitez marquer comme lu.</p> <p>Vous pouvez obtenir l’UID de l’e-mail à l’aide du module E-mail &gt; Observer l’e-mail ou du module [!UICONTROL Search Email].</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Marquer un e-mail comme non lu]

Marque un e-mail ou un brouillon dans un dossier sélectionné comme non lu en activant l’indicateur Non lu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur la procédure de connexion de votre compte de messagerie à [!UICONTROL Workfront Fusion], voir <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connecter votre e-mail à [!UICONTROL Workfront Fusion]</a> dans cet article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Sélectionnez le dossier contenant l’e-mail que vous souhaitez marquer comme non lu. Exemple : dossier Principal.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Saisissez l’UID de l’e-mail que vous souhaitez marquer comme non lu.</p> <p>Vous pouvez obtenir l’UID de l’e-mail à l’aide du module E-mail &gt; Observer l’e-mail ou du module [!UICONTROL Search Email].</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Déplacer un e-mail]

Déplace un e-mail ou un brouillon sélectionné vers un dossier sélectionné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur la procédure de connexion de votre compte de messagerie à [!UICONTROL Workfront Fusion], voir <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connecter votre e-mail à [!UICONTROL Workfront Fusion]</a> dans cet article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Folder]</td> 
   <td>Sélectionnez le dossier contenant l’e-mail à déplacer. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination Folder]</td> 
   <td> <p> Sélectionnez le dossier auquel vous souhaitez ajouter l’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Saisissez l’UID de l’e-mail que vous souhaitez déplacer vers le dossier de destination.</p> <p>Vous pouvez obtenir l’UID de l’e-mail à l’aide du module E-mail &gt; Observer l’e-mail ou du module [!UICONTROL Search Email].</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Envoyer un e-mail]

Envoie un nouvel e-mail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte de messagerie à Workfront Fusion, voir <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">Connexion de votre adresse e-mail à [!UICONTROL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Save Message after Sending]</td> 
   <td>Une fois l’e-mail envoyé, il est enregistré dans votre messagerie. Activez cette option si vous souhaitez enregistrer les e-mails envoyés à l’aide de Workfront Fusion dans le dossier <i>[!UICONTROL Sent mail]</i> ou dans un autre dossier de votre boîte aux lettres. Certains services de messagerie, tels que [!DNL Gmail], enregistrent automatiquement les messages envoyés.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL To] </td> 
   <td> <p>Ajoutez les adresses e-mail auxquelles vous souhaitez envoyer l’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Saisissez ou mappez l’objet de l’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Content Type]</p> </td> 
   <td> <p>Sélectionnez le type de [!UICONTROL content] de l’e-mail :</p> 
    <ul> 
     <li>HTML</li> 
     <li>[!UICONTROL Plaintext]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content] </td> 
   <td> <p>Saisissez ou mappez le contenu de l’e-mail au format HTML à l’aide de balises HTML, ou en texte brut, selon ce que vous avez choisi dans le champ [!UICONTROL Content Type].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>Pour chaque pièce jointe à ajouter, cliquez sur <b>Ajouter un élément</b> et saisissez les informations suivantes :</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File name]</strong> </p> <p>Saisissez le nom du fichier, y compris son extension. </p> </li> 
     <li> <p><strong>[!UICONTROL Data]</strong> </p> <p>Saisissez le chemin d’accès au dossier dans lequel vous souhaitez charger la pièce jointe.</p> </li> 
     <li> <p><strong>[!UICONTROL Content-ID]</strong> </p> <p>Saisissez l’identifiant du contenu pour insérer la pièce jointe (image) dans le contenu.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy Recipient] </td> 
   <td> <p>Pour chaque adresse e-mail à laquelle vous souhaitez envoyer une copie de cet e-mail, cliquez sur <b>Ajouter un élément</b> et saisissez l’adresse e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blind Copy Recipient]</td> 
   <td> <p> Pour chaque adresse e-mail à laquelle vous souhaitez envoyer une copie de cet e-mail sans que l’adresse e-mail n’apparaisse dans l’e-mail, cliquez sur <b>Ajouter un élément</b> et saisissez l’adresse e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Sender]</p> </td> 
   <td> <p>Saisissez ou mappez l’adresse e-mail qui apparaît dans le champ [!UICONTROL Sender] dans l’e-mail.</p> <p>Conseil : si vous ne savez pas si vous allez choisir d’utiliser ce champ ou le champ « De », nous vous conseillons de choisir le champ « De ».</p> <p>Important : utilisez la syntaxe correcte : <code>name@email.com</code> ou <code>"Name" name@email.com</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reply-To]</td> 
   <td> <p> Si vous souhaitez que les réponses à cet e-mail soient envoyées à une adresse différente de celle de l’adresse du champ « De », saisissez l’adresse e-mail vers laquelle vous souhaitez que les réponses à cet e-mail soient envoyées.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL In-Reply-To]</td> 
   <td> <p> Si vous répondez à un e-mail spécifique, saisissez ou mappez l’identifiant de l’e-mail auquel vous répondez.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL References] </td> 
   <td> <p>Saisissez les identifiants des messages de toutes les réponses du fil de discussion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Priority]</p> </td> 
   <td> <p>Sélectionnez la priorité de l’e-mail :</p> 
    <ul> 
     <li>[!UICONTROL High]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL Low]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Headers]</p> </td> 
   <td> <p>Ajoutez les en-têtes :</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Key]</strong> </p> <p>Ajoutez la clé. Par exemple, [!UICONTROL Sender], [!UICONTROL Date], [!UICONTROL To], etc.</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Saisissez la valeur de la clé.</p> </li> 
    </ul> </td> 
  </tr> 
<tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL From] </td> 
   <td> <p>Saisissez ou mappez l’adresse e-mail (et le nom, le cas échéant) qui apparaît dans le champ [!UICONTROL From] dans l’e-mail. </p> <p>Important : utilisez la syntaxe correcte : <code>name@email.com</code> ou <code>"Name" name@email.com</code>.</p> <p>Remarque : en règle générale, Workfront Fusion utilise l’adresse e-mail que vous avez saisie lors de la création de la connexion comme adresse d’expéditeur. Si vous saisissez une autre adresse e-mail, une erreur peut se produire lors de l’envoi d’un message, car votre compte peut ne pas être autorisé à envoyer des e-mails depuis une autre adresse que la vôtre. Par exemple : <code>test@mail.com</code> ou <code>John Bush" test@email.com</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Itérateurs

#### [!UICONTROL Itérer les pièces jointes]

Itère une par une les pièces jointes reçues.

Le module itérateur d’e-mail vous permet de gérer les pièces jointes des e-mails séparément. Vous pouvez, par exemple, le configurer pour qu’il surveille les e-mails afin qu’il itère les e-mails comportant des pièces jointes et qu’il reçoive des alertes.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source module]</td> 
   <td> <p>Sélectionnez le module qui génère l’e-mail avec les pièces jointes que vous souhaitez itérer.</p> </td> 
  </tr> 
 </tbody> 
</table>

Pour plus d’informations sur les itérateurs, voir [Module Itérateur](/help/workfront-fusion/references/modules/iterator-module.md).
