---
title: Modules Gmail
description: Dans un scénario  [!DNL Adobe Workfront Fusion] , vous pouvez automatiser les workflows qui utilisent Gmail et les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: 62269eca-c3cf-42fe-a866-fb66d2363b8d
source-git-commit: 0581601a254a9492f4166d78eb0f11868d390f24
workflow-type: tm+mt
source-wordcount: '1527'
ht-degree: 82%

---

# Modules [!DNL Gmail]

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!DNL Gmail] et le connecter à plusieurs applications et services tiers.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

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

Pour utiliser les modules [!DNL Gmail], vous devez disposer d’un compte [!DNL Gmail].

## Connecter [!DNL Gmail] à [!DNL Workfront Fusion] {#connect-gmail-to-workfront-fusion}

* [Connexion [!DNL Gmail] à [!DNL Workfront Fusion] à l’aide de  [!DNL Google Workspace]](#connect-gmail-to-workfront-fusion-usingg-suite)
* [Connecter  [!DNL Gmail]  à  [!DNL Workfront Fusion]  via  [!DNL gmail.com]  ou  [!DNL googlemail].com](#connect-gmail-to-workfront-fusion-using-gmailcom-or-googlemailcom)

### Connecter [!DNL Gmail] à [!DNL Workfront Fusion] via [!DNL  Google Workspace] {#connect-gmail-to-workfront-fusion-using-g-suite}

Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Workspace] à [!UICONTROL Workfront Fusion], voir [Créer une connexion - Instructions de base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md).

### Connecter [!DNL Gmail] à [!DNL Workfront Fusion] via [!DNL gmail.com] ou [!DNL googlemail].com {#connect-gmail-to-workfront-fusion-using-gmail-com-or-googlemail-com}

Si vous êtes [!DNL @gmail.com] ou [!DNL @googlemail.com] utilisateur, vous devez créer un client OAuth sur [le [!DNL Google Cloud Platform]](https://console.developers.google.com/projectselector2/apis/dashboard?supportedpurview=project) afin d’obtenir un [!UICONTROL Client ID] et un [!UICONTROL Client Secret].

Pour obtenir des instructions détaillées sur la création du client OAuth et l’obtention d’un [!UICONTROL Client ID] et d’une [!UICONTROL Client Secret], voir [Connexion d’Adobe Workfront Fusion aux services Google à l’aide d’un client OAuth personnalisé](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

## Modules [!DNL Gmail] et leurs champs

Lorsque vous configurez les modules [!DNL Gmail], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Gmail] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Déclencheurs](#triggers)
* [Actions](#actions)
* [Itérateurs](#iterators)

### Déclencheurs

#### [!UICONTROL Watch emails]

Ce module déclencheur exécute un scénario lorsqu’un nouvel e-mail est reçu pour être traité.

Le module renvoie tous les champs standard associés à l’enregistrement ou aux enregistrements, ainsi que les champs et valeurs personnalisés auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Gmail] à [!DNL Workfront Fusion], voir <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Gmail] à [!UICONTROL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Sélectionnez le dossier d’e-mail que vous souhaitez consulter.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Filter type] </td> 
   <td> <p>Sélectionnez le type de filtre que vous souhaitez utiliser pour consulter les e-mails.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Simple filter]</strong> </p> <p>Renseignez les champs [!UICONTROL Criteria], [!UICONTROL Sender Email Address], [!UICONTROL Subject] et [!UICONTROL Search Phrase]</p> </li> 
     <li> <p> <strong>[!UICONTROL Gmail filter]</strong> </p> <p>Dans le champ [!UICONTROL Query] , saisissez la requête à utiliser pour filtrer les e-mails.</p> <p>Pour plus d’informations sur les filtres [!DNL Gmail], voir <a href="https://support.google.com/mail/answer/7190">Opérateurs de recherche</a> dans la documentation de [!DNL Gmail].</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Criteria]</td> 
   <td>Choisissez si vous souhaitez regarder des e-mails [!UICONTROL all email], [!UICONTROL only read emails] ou [!UICONTROL only unread].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sender email address]</td> 
   <td> <p> Saisissez une adresse e-mail pour ne consulter que les e-mails envoyés à partir de cette adresse.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject]</td> 
   <td>Saisissez une chaîne de texte pour n’afficher que les e-mails dont l’objet contient cette chaîne de texte.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search phrase]</td> 
   <td>Saisissez une chaîne de texte pour ne consulter que les e-mails qui contiennent cette chaîne de texte n’importe où dans l’e-mail.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mark email message(s) as read when fetched]</td> 
   <td> <p> Activez cette option pour marquer les e-mails récupérés comme lus.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of results]</td> 
   <td> <p> Définissez le nombre maximal de résultats avec lesquels [!DNL Workfront Fusion] fonctionnera pendant un cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [[!UICONTROL Send an email]](#send-an-email)
* [[!UICONTROL Create a draft]](#create-a-draft)
* [[!UICONTROL Mark an email as read]](#mark-an-email-as-read)
* [[!UICONTROL Mark an email as unread]](#mark-an-email-as-unread)
* [[!UICONTROL Move an email]](#move-an-email)
* [[!UICONTROL Copy an email]](#copy-an-email)
* [[!UICONTROL Delete an email]](#delete-an-email)
* [[!UICONTROL Modify email labels]](#modify-email-labels)

#### [!UICONTROL Send an email]

Ce module d’action envoie un nouvel e-mail.

Vous spécifiez la personne destinataire de l’e-mail.

Le module renvoie l’identifiant de l’e-mail et de tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Gmail] à [!DNL Workfront Fusion], voir <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Gmail] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL From]</td> 
   <td> <p>Saisissez ou mappez une adresse e-mail de l’expéditeur ou de l’expéditrice.</p> <p>Remarque : si vous saisissez une adresse e-mail incorrecte, une erreur peut se produire lors de l’envoi d’un message, car votre compte peut ne pas être autorisé à envoyer des e-mails à partir d’une adresse différente de la vôtre.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL To] </td> 
   <td> <p>Cliquez sur <strong>[!UICONTROL Add]</strong>, puis saisissez ou mappez l’adresse e-mail de chaque destinataire.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject] </td> 
   <td> <p>Saisissez ou mappez l’objet de l’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Content] </td> 
   <td> <p>Saisissez ou mappez le contenu de l’e-mail (corps du message). Les balises HTML sont autorisées.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attachments] </td> 
   <td> <p>Cliquez sur <strong>[!UICONTROL Add]</strong> pour ajouter une pièce jointe. Vous pouvez mapper un fichier à partir des modules précédents.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Copy recipients]</td> 
   <td> <p> Cliquez sur <strong>[!UICONTROL Add]</strong>, puis saisissez ou mappez l’adresse e-mail de chaque destinataire de la copie.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Blind copy recipients]</td> 
   <td> <p> Cliquez sur <strong>[!UICONTROL Add]</strong>, puis saisissez ou mappez l’adresse e-mail de chaque destinataire de copie invisible.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a draft]

Ce module d’action crée un brouillon d’e-mail et l’ajoute à un dossier que vous spécifiez.

Vous spécifiez le dossier dans lequel vous souhaitez créer un brouillon.

Le module renvoie l’identifiant du brouillon d’e-mail et les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Gmail] à [!DNL Workfront Fusion], voir <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Gmail] à [!UICONTROL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Sélectionnez le dossier [!DNL Gmail] dans lequel vous souhaitez créer un brouillon.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL To] </td> 
   <td> <p>Cliquez sur <strong>[!UICONTROL Add]</strong>, puis saisissez ou mappez l’adresse e-mail de chaque destinataire.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject] </td> 
   <td> <p>Saisissez ou mappez l’objet de l’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Content] </td> 
   <td> <p>Saisissez ou mappez le contenu de l’e-mail (corps du message). Les balises HTML sont autorisées.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attachments] </td> 
   <td> <p>Cliquez sur <strong>[!UICONTROL Add]</strong> pour ajouter une pièce jointe. Vous pouvez mapper un fichier à partir des modules précédents.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Copy recipients]</td> 
   <td> <p> Cliquez sur <strong>[!UICONTROL Add]</strong>, puis saisissez ou mappez l’adresse e-mail de chaque destinataire de la copie.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Blind copy recipients]</td> 
   <td> <p> Cliquez sur <strong>[!UICONTROL Add]</strong>, puis saisissez ou mappez l’adresse e-mail de chaque destinataire de copie invisible.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mark an email as read]

Ce module d’action marque un e-mail comme lu.

Vous indiquez l’identifiant de l’e-mail et de son dossier.

Le module renvoie l’identifiant de l’e-mail et des champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Gmail] à [!DNL Workfront Fusion], voir <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Gmail] à [!UICONTROL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Sélectionnez le dossier [!DNL Gmail] qui contient l’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)]</td> 
   <td> <p> Saisissez ou mappez l’identifiant d’e-mail.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mark an email as unread]

Ce module d’action marque un e-mail ou un brouillon d’e-mail comme non lu.

Vous indiquez l’identifiant de l’e-mail et de son dossier.

Le module renvoie l’identifiant de l’e-mail et des champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Gmail] à [!DNL Workfront Fusion], voir <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Gmail] à [!UICONTROL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Sélectionnez le dossier [!DNL Gmail] qui contient l’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)] </td> 
   <td> <p>Saisissez ou mappez l’identifiant de l’e-mail que vous souhaitez marquer comme non lu.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move an email]

Ce module d’action déplace un e-mail ou un brouillon d’e-mail vers un dossier que vous spécifiez.

Vous indiquez le dossier, le dossier de destination et l’identifiant de l’e-mail.

Le module renvoie l’identifiant de l’e-mail et des champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Gmail] à [!DNL Workfront Fusion], voir <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Gmail] à [!UICONTROL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Sélectionnez le dossier source [!DNL Gmail] qui contient l’e-mail que vous souhaitez déplacer.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination folder]</td> 
   <td> <p> Sélectionnez le dossier cible [!DNL Gmail] vers lequel vous souhaitez déplacer l’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)]</td> 
   <td> <p> Saisissez ou mappez l’identifiant de l’e-mail que vous souhaitez déplacer.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Copy an email]

Ce module d’action copie un e-mail ou un brouillon d’e-mail dans un dossier que vous spécifiez.

Vous indiquez le dossier, le dossier de destination et l’identifiant de l’e-mail.

Le module renvoie l’identifiant de l’e-mail et de tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Gmail] à [!DNL Workfront Fusion], voir <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Gmail] à [!UICONTROL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Sélectionnez le dossier source [!DNL Gmail] qui contient l’e-mail que vous souhaitez copier.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination folder]</td> 
   <td> <p>Sélectionnez le dossier cible [!DNL Gmail] dans lequel vous souhaitez copier l’e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)]</td> 
   <td> <p>Saisissez ou mappez l’identifiant de l’e-mail que vous souhaitez copier.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an email]

Ce module d’action supprime un e-mail ou un brouillon d’e-mail d’un dossier que vous spécifiez.

Le module renvoie l’identifiant de l’e-mail et des champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Gmail] à [!DNL Workfront Fusion], voir <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Gmail] à [!UICONTROL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL [!DNL Gmail] Message ID]</p> </td> 
   <td> <p>Saisissez ou mappez l’identifiant de l’e-mail que vous souhaitez supprimer.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Permanently] </td> 
   <td> <p>Activez cette option pour autoriser le module à supprimer définitivement l’e-mail, plutôt que de le déplacer vers le dossier de la corbeille.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Modify email labels]

Ce module d&#39;action modifie le libellé d’un e-mail que vous spécifiez.

Le module renvoie l’identifiant de l’e-mail et des champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Gmail] à [!DNL Workfront Fusion], voir <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Gmail] à [!UICONTROL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Gmail] Message ID]</td> 
   <td> <p> Saisissez ou mappez l’identifiant de l’e-mail que vous souhaitez supprimer.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Labels to add]</p> </td> 
   <td> <p>Sélectionnez ou mappez le libellé à ajouter à l’e-mail sélectionné.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Labels to remove]</td> 
   <td> <p> Sélectionnez ou mappez le libellé à supprimer de l’e-mail sélectionné.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Les champs [!UICONTROL Label to add] et [!UICONTROL Label to remove] ne chargent que les libellés créés par l’utilisateur.

### Itérateurs

#### [!UICONTROL Iterate attachments]

Vous pouvez itérer les pièces jointes d’e-mail. Chaque pièce jointe est un lot distinct dans la sortie du module. Pour plus d’informations, voir [Module Itérateur](/help/workfront-fusion/references/modules/iterator-module.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module] </td> 
   <td> <p>Sélectionnez le module à partir duquel vous souhaitez itérer les pièces jointes. </p> </td> 
  </tr> 
 </tbody> 
</table>
