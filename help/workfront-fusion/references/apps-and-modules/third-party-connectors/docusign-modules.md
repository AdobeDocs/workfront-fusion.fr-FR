---
title: Modules DocuSign
description: Les modules  [!DNL Adobe Workfront Fusion DocuSign]  vous permettent de surveiller et de récupérer le statut des enveloppes, de rechercher et de récupérer des enveloppes, ou de télécharger et d’envoyer un document pour vous connecter à votre compte  [!DNL DocuSign] .
author: Becky
draft: Probably
feature: Workfront Fusion, Digital Content and Documents
exl-id: 94a823a6-3c70-42a1-b6cf-298591dbca15
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '1631'
ht-degree: 85%

---

# Modules DocuSign

Les modules [!DNL Adobe Workfront Fusion] [!DNL DocuSign] vous permettent de surveiller et de récupérer le statut des enveloppes, de rechercher et de récupérer des enveloppes, ou de télécharger et d’envoyer un document pour vous connecte à votre compte [!DNL DocuSign].

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

Pour utiliser les modules [!DNL DocuSign], vous devez disposer d’un compte [!DNL DocuSign].

## Informations sur l’API DocuSign

Le connecteur DocuSign utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>1.18.11</td> 
  </tr>
 </tbody> 
 </table>

## Connecter [!DNL DocuSign] à [!DNL Workfront Fusion] {#connect-docusign-to-workfront-fusion}

Pour créer une connexion pour vos modules [!DNL DocuSign], procédez comme suit :

1. Cliquez sur **[!UICONTROL Add]** en regard de la zone de [!UICONTROL Connection] lorsque vous commencez à configurer le premier module de [!DNL DocuSign].
1. Saisissez les informations suivantes :

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>Saisir un nom pour la nouvelle connexion [!DNL DocuSign]</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Account type]</td> 
      <td>Indiquez si le compte auquel vous souhaitez vous connecter est un compte de production ou de démonstration.</td> 
     </tr> 
    </tbody> 
   </table>

1. Poursuivez comme décrit dans la section [Créer une connexion à  [!DNL Adobe Workfront Fusion]  - Instructions de base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md#connect).

## Modules [!DNL DocuSign] et leurs champs

Lorsque vous configurez les modules [!DNL DocuSign], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL DocuSign] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Déclencheurs](#triggers)
* [Actions](#actions)

### Déclencheurs

#### [!UICONTROL Watch envelopes]

Ce module de déclenchement lance un scénario lorsqu’une enveloppe est envoyée, diffusée, signée, terminée ou refusée.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL DocuSign] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Sélectionnez le compte qui contient les enregistrements à surveiller.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event type]</td> 
   <td> <p> Sélectionnez le type d’événement à surveiller.</p> 
    <ul> 
     <li>[!UICONTROL Document completed]</li> 
     <li>[!UICONTROL Document declined]</li> 
     <li>[!UICONTROL Document sent]</li> 
     <li>[!UICONTROL Document signed]</li> 
     <li>[!UICONTROL New document in Inbox]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Output fields]</p> </td> 
   <td> <p>Sélectionnez les champs que vous souhaitez inclure dans la sortie du module.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Saisissez ou mappez le nombre maximum d’enregistrements que vous souhaitez que le module utilise lors de chaque cycle d’exécution du scénario.</td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Download a document]](#download-a-document)
* [[!UICONTROL Read an envelope]](#read-an-envelope)
* [[!UICONTROL Upload a file to an envelope]](#upload-a-file-to-an-envelope)
* [[!UICONTROL Create a new envelope]](#create-a-new-envelope)
* [[!UICONTROL Add Recipient to Envelope]](#add-recipient-to-envelope)
* [[!UICONTROL Add custom field]](#add-custom-field)
* [[!UICONTROL Modify custom field]](#modify-custom-field)
* [[!UICONTROL Send envelope]](#send-envelope)

#### [!UICONTROL Custom API Call]

Ce module d’action vous permet d’effectuer un appel API personnalisé.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL DocuSign] à [!DNL Workfront Fusion], voir <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Connecter [!DNL DocuSign] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Account]</td> 
   <td>Saisissez ou mappez le compte que vous souhaitez utiliser pour accéder à l’API [!DNL DocuSign].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL URL]</td> 
   <td> <p>Saisissez l’adresse sur le serveur web avec lequel le module doit interagir.</p> <p>Vous pouvez saisir une URL relative, ce qui signifie que vous n’avez pas besoin d’inclure le protocole (comme <code>http://</code>) au début. Cela indique au serveur web que l’interaction se produit sur le serveur.</p> <p>Par exemple : <code>[!DNL /api/conversations].create</code></p>  </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Method]</td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard. Cela détermine le type de contenu de la requête.</p> <p>Par exemple,<code> {"Content-type":"application/json"}</code></p> <p>Note : si vous obtenez des erreurs et qu’il est difficile de déterminer leur origine, envisagez de modifier les en-têtes en fonction de la documentation [!DNL Workfront]. Si votre appel API personnalisé renvoie une erreur de requête HTTP 422, essayez d’utiliser un en-tête « Content-Type:text/plain ».</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query String]</td> 
   <td> <p>Ajoutez la requête pour l’appel API sous la forme d’un objet JSON standard.</p> <p>Par exemple : <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Body]</td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre JSON, placez les guillemets à l’extérieur de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td>Saisissez ou mappez le nombre maximal de résultats à utiliser au cours d’un cycle d’exécution.</td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Exemple :** répertorier les enveloppes
>
>L’appel API suivant renvoie des enveloppes à partir de la date spécifiée dans votre compte [!DNL DocuSign] :
>
>**URL** : `/v2.1/accounts/{accountId}/envelopes/`
>
>**Méthode** : `GET`
>
>**Chaîne de requête** :
>
>* **Clé** : `from_date`
>
>* **Valeur** : `YYYY-MM-DD`
>
>Indique le moment où la requête commence à vérifier les modifications de statut des enveloppes du compte.
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/example-docusign-setup-350x770.png)
>
>Le résultat se trouve dans la sortie du module sous Lot > Corps > Enveloppes.
>
>Dans notre exemple, six enveloppes ont été renvoyées :
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/docusign-example-output-350x677.png)

#### [!UICONTROL Download a document]

Ce module d’action télécharge un seul document.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL DocuSign] à [!DNL Workfront Fusion], voir <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Connecter [!DNL DocuSign] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Sélectionnez le compte contenant le document que vous souhaitez télécharger.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Saisissez ou mappez l’ID de l’enveloppe que vous souhaitez télécharger.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Document ID]</p> </td> 
   <td> <p>Saisissez ou mappez l’ID du document que vous souhaitez télécharger.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Certificate]</td> 
   <td>Sélectionnez <strong>[!UICONTROL Yes]</strong> si vous souhaitez inclure le certificat de signature d’enveloppe dans le téléchargement.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Documents by User ID]</td> 
   <td>Sélectionnez <strong>[!UICONTROL Yes]</strong> si vous souhaitez permettre aux destinataires de récupérer des documents par ID d’utilisateur. Par exemple, si une personne est incluse dans deux ordres de transmission différents avec des visibilités différentes, l’utilisation de cette option renvoie tous les documents des deux transmissions.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Encrypt]</td> 
   <td>Sélectionnez <strong>[!UICONTROL Yes]</strong> si vous souhaitez que les octets du PDF renvoyés dans la réponse soient chiffrés pour tous les gestionnaires de clés configurés sur votre compte [!DNL DocuSign].</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Language]</td> 
   <td>Sélectionnez la langue.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show Changes]</td> 
   <td>Lorsque ce paramètre est défini sur <strong>[!UICONTROL Yes]</strong>, les champs modifiés pour le PDF renvoyé sont surlignés en jaune et les signatures ou initiales facultatives sont entourées en rouge.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watermark]</td> 
   <td> <p>Sélectionnez <strong>[!UICONTROL No]</strong> pour supprimer le filigrane des documents du PDF.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read an envelope]

Ce module d’action lit des informations sur une enveloppe dans [!DNL DocuSign] en utilisant l’ID d’enveloppe.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL DocuSign] à [!DNL Workfront Fusion], voir <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Connecter [!DNL DocuSign] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Sélectionnez le compte contenant le document à partir duquel vous souhaitez lire les informations.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Saisissez ou mappez l’ID du document à partir duquel vous souhaitez lire les informations.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Sélectionnez les propriétés à afficher dans la sortie du module. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file to an envelope]

Ce module charge un fichier spécifié dans une enveloppe existante dans DocuSign.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL DocuSign] à [!DNL Workfront Fusion], voir <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Connecter [!DNL DocuSign] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Sélectionnez le compte contenant l’enveloppe dans laquelle vous souhaitez charger un fichier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Saisissez ou mappez l’ID de l’enveloppe dans laquelle vous souhaitez charger un fichier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Sélectionnez un fichier source à partir d’un module précédent ou saisissez le nom et les données du fichier source.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a new envelope]

Ce module d’action crée une enveloppe à partir d’un modèle. Il renvoie l’ID et le statut de la nouvelle enveloppe.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td>

<td> <p>Pour plus d’informations sur la connexion de votre compte DocuSign à Workfront Fusion, consultez les articles sous <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Account] </td>
   <td> <p>Sélectionnez le compte contenant l’enveloppe dans laquelle vous souhaitez charger un fichier.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Template]</td>
   <td> <p> Sélectionnez le modèle à partir duquel vous souhaitez créer l’enveloppe. Les modèles sont disponibles en fonction des [!UICONTROL Account] que vous avez sélectionnés.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL After creation]
   </td> 
   <td> <p>Indiquez si vous souhaitez enregistrer l’enveloppe en tant que brouillon ou l’envoyer pour signature.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Template recipients]</td>
    <td>Sélectionner la personne destinataire de cette enveloppe</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add Recipient to Envelope]

Ce module d’action ajoute une ou plusieurs personnes destinataires à une enveloppe existante. Si l’enveloppe a déjà été envoyée, la personne destinataire reçoit un e-mail. Ce module n’est pas valide pour les enveloppes déjà terminées.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Connection] </td>
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte DocuSign à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL Account] </td>
   <td> <p>Sélectionnez le compte contenant l’enveloppe à laquelle vous souhaitez ajouter des personnes destinataires.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Envelope ID]</td>
    <td>Sélectionnez ou mappez l’ID de l’enveloppe à laquelle vous souhaitez ajouter la personne destinataire.</td>
  </tr> 
  <tr data-mc-conditions="">
    <td role="rowheader">[!UICONTROL Recipient type]</td>
   <td> <p> Sélectionnez le type de personne destinataire à ajouter à l’enveloppe.</p> 
    <ul> 
     <li> <p>[!UICONTROL Agent]</p> </li> 
     <li> <p>[!UICONTROL Carbon copy]</p> </li> 
     <li> <p>[!UICONTROL Certified delivery]</p> </li> 
     <li> <p>[!UICONTROL In-person signer]</p> </li> 
     <li> <p>[!UICONTROL Intermediary]</p> </li> 
     <li> <p>[!UICONTROL Signer]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Email]</td>
   <td> <p>Saisissez ou mappez l’adresse e-mail de la personne destinataire à ajouter à l’enveloppe.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Name]</td>
   <td>Saisissez ou mappez le nom de la personne destinataire à ajouter à l’enveloppe.</td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Routing order]</td>
   <td> <p>Saisissez ou mappez le numéro de routage de la personne destinataire. Le numéro de routage détermine l’ordre dans lequel les personnes destinataires reçoivent et signent vos documents.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Email body]</td>
   <td>Saisissez ou mappez le corps (contenu) de l’e-mail à envoyer à la personne destinataire.</td> 
  </tr> 
  <tr>
    <td role="rowheader">[!UICONTROL Email subject]</td>
   <td>Saisissez ou mappez l’objet de l’e-mail à envoyer à la personne destinataire.</td> 
  </tr> 
    <td role="rowheader">[!UICONTROL Private message]</td>
   <td> <li> <p>Seule la personne destinataire sélectionnée voit le message privé, ainsi que le message général. Le message privé est limité à 1 000 caractères.</p> </li> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Authentication]</td> 
   <td> <p>Sélectionnez la méthode d’authentification à utiliser pour confirmer l’identité de la personne destinataire.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL None]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL Access code]</strong> </p> <p>Saisissez ou mappez le code d’accès.</p> </li> 
     <li> <p><strong>[!UICONTROL Phone]</strong> </p> <p>Saisissez ou mappez le numéro de téléphone.</p> </li> 
     <li> <p><strong>[!UICONTROL SMS]</strong> </p> <p>Saisissez ou mappez le numéro de téléphone.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add custom field]

Ce module d’action ajoute un champ personnalisé au document.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL DocuSign] à [!DNL Workfront Fusion], voir <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Connecter [!DNL DocuSign] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Sélectionnez le compte contenant le document auquel vous souhaitez ajouter un champ personnalisé.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Saisissez ou mappez l’ID de l’enveloppe qui contient le document auquel vous souhaitez ajouter un champ personnalisé.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field name]</td> 
   <td>Saisissez ou mappez un nom pour le nouveau champ à ajouter.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Required]</td> 
   <td>Activez cette option si vous souhaitez que le champ ajouté soit un champ obligatoire.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show field]</td> 
   <td>Activez cette option si vous souhaitez que le champ soit visible.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Value]</td> 
   <td>Saisissez ou mappez la valeur (contenu) du champ ajouté. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Modify custom field]

Ce module d’action modifie un champ personnalisé à l’aide du nom du champ.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL DocuSign] à [!DNL Workfront Fusion], voir <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Connecter [!DNL DocuSign] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Sélectionnez le compte contenant le document dont vous souhaitez modifier un champ personnalisé.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Saisissez ou mappez l’ID de l’enveloppe qui contient le document dont vous souhaitez modifier un champ personnalisé.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field ID]</td> 
   <td>Saisissez ou mappez l’ID du champ à modifier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field name]</td> 
   <td>Saisissez ou mappez le nom du champ à modifier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Required]</td> 
   <td>Activez cette option si vous souhaitez que le champ modifié soit un champ obligatoire.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show field]</td> 
   <td>Activez cette option si vous souhaitez que le champ soit visible.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Value]</td> 
   <td>Saisissez ou mappez la valeur (contenu) du champ modifié. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Send envelope]

Ce module d’action envoie un brouillon d’enveloppe à ses personnes destinataires.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL DocuSign] à [!DNL Workfront Fusion], voir <a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">Connecter [!DNL DocuSign] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>Sélectionnez le compte contenant le brouillon d’enveloppe à envoyer à ses personnes destinataires.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> Saisissez ou mappez l’ID du brouillon d’enveloppe à envoyer à ses personnes destinataires.</p> </td> 
  </tr> 
 </tbody> 
</table>
