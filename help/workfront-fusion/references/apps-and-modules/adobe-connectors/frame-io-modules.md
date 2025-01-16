---
title: Modules Frame.io
description: Compte  [!DNL Adobe Workfront Fusion Frame].io modules enable you to monitor, create, update, retrieve, or delete assets and comments in your [!DNL Frame.io] .
author: Becky
feature: Workfront Fusion
exl-id: 121b145c-d04d-44b9-b673-ea2928e2346d
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1969'
ht-degree: 88%

---

# Modules [!DNL Frame.io]

Les modules [!DNL Adobe Workfront Fusion] [!DNL Frame.io] vous permettent de surveiller, créer, mettre à jour, récupérer ou supprimer des ressources et des commentaires dans votre compte [!DNL Frame.io].

Pour obtenir une vidéo d’introduction au connecteur Frame.io, consultez ce qui suit :

* [Frame.io](https://video.tv.adobe.com/v/3427032/){target=_blank}

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

Pour utiliser des modules [!DNL Frame.io], vous devez disposer d’un compte [!DNL Frame.io].

## Informations sur l’API Frame.io

Le connecteur Frame.io utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td> https://api.frame.io/v2</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Version de l’API</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.0.76</td> 
  </tr>
 </tbody> 
 </table>

## Connecter [!DNL Frame.io] à [!UICONTROL Adobe Workfront Fusion]

Vous pouvez vous connecter à [!DNL Frame.io] à l’aide d’un jeton API ou d’OAuth 2.0.

[Se connecter à  [!DNL Frame.io]  à l’aide d’un jeton API](#connect-to-frameio-using-an-api-token)

[Se connecter à  [!DNL Frame.io]  à l’aide d’OAuth 2.0 PKCE](#connect-to-frameio-using-oauth-20-pkce)

### Se connecter à [!DNL Frame.io] à l’aide d’un jeton API

Pour connecter votre compte [!DNL Frame.io] à [!DNL Workfront Fusion] à l’aide d’un jeton API, vous devez créer le jeton API dans votre compte [!DNL Frame.io] et l’insérer dans la boîte de dialogue de [!UICONTROL Create a connection] de [!DNL Frame.io] [!DNL Workfront Fusion].

1. Connectez-vous à votre compte [!DNL Frame.io].
1. Accédez à la page **[!UICONTROL Tokens]** dans le développeur [!DNL Frame.io].
1. Cliquez sur **[!UICONTROL New]**.
1. Saisissez le nom du jeton, sélectionnez les portées à utiliser, puis cliquez sur **[!UICONTROL Create]**.
1. Copiez le jeton fourni.
1. Accédez à [!DNL Workfront Fusion] et ouvrez la boîte de dialogue **[!UICONTROL Create a connection]** du module [!DNL Frame.io] .
1. Dans le champ **[!UICONTROL Connection type]** , sélectionnez **[!DNL Frame.io]**.
1. Saisissez le jeton que vous avez copié à l’étape 5 dans le champ **[!UICONTROL Your [!DNL Frame.io] API Key]** et cliquez sur **[!UICONTROL Continue]** pour établir la connexion.

La connexion a été établie. Vous pouvez poursuivre la configuration du module.

### Se connecter à [!DNL Frame.io] à l’aide d’OAuth 2.0 PKCE

Vous pouvez créer une connexion à [!DNL Frame.io] à l’aide d’OAuth 2.0 PKCE avec un identifiant client facultatif. Si vous souhaitez inclure un identifiant client dans votre connexion, vous devez créer une application OAuth 2.0 dans votre compte [!DNL Frame.io].

* [Se connecter à  [!DNL Frame.io]  à l’aide d’OAuth 2.0 PKCE (sans identifiant client)](#connect-to-frameio-using-using-oauth-20-pkce-without-client-id)
* [Se connecter à  [!DNL Frame.io]  à l’aide d’OAuth 2.0 PKCE (avec un identifiant client)](#connect-to-frameio-using-using-oauth-20-pkce-with-client-id)

#### Se connecter à [!DNL Frame.io] à l’aide d’OAuth 2.0 PKCE (sans identifiant client)

1. Accédez à [!DNL Workfront Fusion] et ouvrez la boîte de dialogue **[!UICONTROL Create a connection]** du module [!DNL Frame.io] .
1. Dans le champ **[!UICONTROL Connection type]** , sélectionnez **[!UICONTROL [!DNL Frame.io] OAuth 2.0 PKCE]**.
1. Saisissez le nom de la nouvelle connexion dans le champ **[!UICONTROL Connection name]** .
1. Cliquez sur **[!UICONTROL Continue]** pour établir la connexion.

La connexion a été établie. Vous pouvez poursuivre la configuration du module.

#### Se connecter à [!DNL Frame.io] en utilisant OAuth 2.0 PKCE (avec un identifiant client)

1. Créez une application OAuth 2.0 dans [!DNL Frame.io]. Pour obtenir des instructions détaillées, consultez la documentation [!DNL Frame.io] sur [!UICONTROL OAuth 2.0 Code Authorization Flow].

   >[!IMPORTANT]
   >
   >Lorsque vous créez l’application OAuth 2.0 dans [!DNL Frame.io], procédez comme suit :
   >
   >* Saisissez l’URI de redirection suivant :
   >   
   >  Amériques/APAC `https://app.workfrontfusion.com/oauth/cb/frame-io5`
   >
   >  EMEA `https://app-eu.workfrontfusion.com/oauth/cb/frame-io5`
   >
   >* Activez l’option PCKE.


1. Copiez la valeur `client_id` fournie.
1. Accédez à [!DNL Workfront Fusion] et ouvrez la boîte de dialogue **[!UICONTROL Create a connection]** du module [!DNL Frame.io] .
1. Dans le champ **[!UICONTROL Connection type]** , sélectionnez **[!UICONTROL [!DNL Frame.io] OAuth 2.0 PKCE]**.
1. Saisissez le nom de la nouvelle connexion dans le champ **[!UICONTROL Connection name]** .
1. Cliquez sur **[!UICONTROL Show advanced settings]**.
1. Saisissez le `client_id` que vous avez copié à l’étape 2 dans le champ **[!UICONTROL Client ID]** .
1. Cliquez sur **[!UICONTROL Continue]** pour établir la connexion.

La connexion a été établie. Vous pouvez poursuivre la configuration du module.

## Modules [!DNL Frame.io] et leurs champs

Lorsque vous configurez les modules [!DNL Frame.io], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Frame.io] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Ressources](#assets)
* [Commentaires](#comments)
* [Projets](#projects)
* [Autre](#other)

### Ressources

* [[!UICONTROL Create an Asset]](#create-an-asset)
* [[!UICONTROL Delete an Asset]](#delete-an-asset)
* [[!UICONTROL Get an Asset]](#get-an-asset)
* [[!UICONTROL List Assets]](#list-assets)
* [[!UICONTROL Update an Asset]](#update-an-asset)
* [[!UICONTROL Watch Asset Deleted]](#watch-asset-deleted)
* [[!UICONTROL Watch Asset Label Updated]](#watch-asset-label-updated)
* [[!UICONTROL Watch New Asset]](#watch-new-asset)

#### [!UICONTROL Create an Asset]

Ce module d’action crée une ressource.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Sélectionnez ou mappez l’équipe propriétaire du projet pour lequel vous souhaitez créer une ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Sélectionnez le projet ou mappez l’ID du projet pour lequel vous souhaitez créer une ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Sélectionnez le dossier ou mappez l’ID du dossier dans lequel vous souhaitez créer une ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type] </td> 
   <td> <p>Indiquez si vous souhaitez créer un dossier ou un fichier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Saisissez le nom du nouveau fichier ou dossier.</p> </td> 
  </tr> <!--
   <tr> 
    <td role="rowheader">File Type </td> 
    <td> <p>Select the type of file you want to upload.</p> </td> 
   </tr>
  --> <!--
   <tr> 
    <td role="rowheader">File Size </td> 
    <td> <p>The file size in bytes.</p> </td> 
   </tr>
  --> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source URL] </td> 
   <td> <p>Saisissez l’URL du fichier à charger.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description] </td> 
   <td> <p>Saisissez une brève description de la ressource.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an Asset]

Ce module d’action supprime une ressource spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Sélectionnez ou mappez l’équipe propriétaire du projet qui contient la ressource à supprimer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p> Sélectionnez le projet qui contient la ressource à supprimer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Sélectionnez le dossier contenant la ressource à supprimer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Sélectionnez ou mappez la ressource à supprimer.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an Asset]

Ce module d’action récupère les détails d’une ressource.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Sélectionnez ou mappez l’équipe propriétaire du projet qui contient la ressource dont vous souhaitez récupérer les détails.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p> Sélectionnez le projet qui contient la ressource dont vous souhaitez récupérer les détails.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Sélectionnez le dossier contenant la ressource dont vous souhaitez récupérer les détails.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Sélectionnez la ressource ou mappez l’ID de la ressource dont vous souhaitez récupérer les détails.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Assets]

Ce module de recherche récupère toutes les ressources dans le dossier du projet spécifié.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Sélectionnez ou mappez l’équipe propriétaire du projet contenant le dossier dont vous souhaitez récupérer les ressources.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p> Sélectionnez le projet contenant le dossier dont vous souhaitez récupérer les ressources.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Sélectionnez le dossier dont vous souhaitez répertorier les ressources.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Définissez le nombre maximal de ressources que [!DNL Workfront Fusion] renverra pendant un cycle d’exécution.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### `[!UICONTROL Update an Asset]`

Ce module d’action vous permet de mettre à jour le nom, la description ou les champs personnalisés d’une ressource existante.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Sélectionnez ou mappez l’équipe propriétaire du projet dont vous souhaitez mettre à jour une ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Sélectionnez le projet ou mappez l’ID du projet pour lequel vous souhaitez mettre à jour une ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Sélectionnez le dossier ou mappez l’ID du dossier dans lequel vous souhaitez mettre à jour une ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Saisissez le nom du fichier mis à jour.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description] </td> 
   <td> <p>Saisissez une brève description de la ressource mise à jour.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Asset Deleted]

Ce module de déclenchement démarre un scénario lorsqu’une ressource est supprimée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name]</td> 
   <td> <p> Saisissez le nom du webhook, par exemple Ressource supprimée.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Sélectionnez l’équipe pour laquelle ce webhook est créé.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Asset Label Updated]

Ce module de déclenchement démarre un scénario lorsque le statut d’une ressource est défini, modifié ou supprimé.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name]</td> 
   <td> <p> Saisissez le nom du webhook, par exemple Statut de la ressource mis à jour.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Sélectionnez l’équipe pour laquelle ce webhook est créé.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch New Asset]

Ce module de déclenchement démarre un scénario lorsqu’une nouvelle ressource est créée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name]</td> 
   <td> <p> Saisissez le nom du webhook, par exemple Ressource créée.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Sélectionnez l’équipe pour laquelle ce webhook est créé.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Commentaires

* [[!UICONTROL Create a Comment]](#create-a-comment)
* [[!UICONTROL Delete a Comment]](#delete-a-comment)
* [[!UICONTROL Get a Comment]](#get-a-comment)
* [[!UICONTROL List Comments]](#list-comments)
* [[!UICONTROL Update a Comment]](#update-a-comment)
* [[!UICONTROL Watch Comment Updated]](#watch-comment-updated)
* [[!UICONTROL Watch New Comment]](#watch-new-comment)

#### [!UICONTROL Create a Comment]

Ce module d’action ajoute un nouveau commentaire ou une nouvelle réponse à la ressource.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type] </td> 
   <td> <p>Indiquez si vous souhaitez créer un commentaire ou répondre à un commentaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Sélectionnez ou mappez l’équipe propriétaire du projet contenant la ressource à laquelle vous souhaitez ajouter un commentaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Sélectionnez le projet ou mappez l’ID du projet qui contient la ressource à laquelle vous souhaitez ajouter un commentaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Sélectionnez le dossier ou mappez l’ID du dossier contenant la ressource à laquelle vous souhaitez ajouter un commentaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Sélectionnez ou mappez la ressource à laquelle vous souhaitez ajouter un commentaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>Sélectionnez ou mappez le commentaire auquel vous souhaitez ajouter une réponse.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p> Saisissez le contenu textuel du commentaire ou de la réponse.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp] </td> 
   <td> <p>Saisissez le numéro de l’image dans la vidéo à laquelle le commentaire doit être lié.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Comment]

Ce module d’action supprime un commentaire existant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID]</td> 
   <td> <p> Sélectionnez ou mappez l’équipe propriétaire du projet qui contient la ressource dont vous souhaitez supprimer un commentaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p> Sélectionnez le projet ou mappez l’ID du projet qui contient la ressource dont vous souhaitez supprimer un commentaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td> <p> Sélectionnez le dossier contenant la ressource dont vous souhaitez supprimer un commentaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Sélectionnez la ressource contenant le commentaire à supprimer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>Sélectionnez le commentaire à supprimer.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Comment]

Ce module d’action récupère les détails du commentaire spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Sélectionnez ou mappez l’équipe propriétaire du projet qui contient le dossier dont vous souhaitez récupérer les ressources.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Sélectionnez le projet contenant le dossier dont vous souhaitez récupérer les ressources.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Sélectionnez le dossier dont vous souhaitez répertorier les ressources.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Sélectionnez la ressource contenant le commentaire que vous souhaitez récupérer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>Sélectionnez le commentaire dont vous souhaitez récupérer les détails.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Comments]

Ce module de recherche récupère tous les commentaires de la ressource spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Sélectionnez ou mappez l’équipe propriétaire du projet qui contient le dossier dont vous souhaitez récupérer les commentaires.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Sélectionnez le projet contenant le dossier dont vous souhaitez récupérer les commentaires.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Sélectionnez le dossier contenant la ressource dont vous souhaitez répertorier les commentaires.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Sélectionnez la ressource pour laquelle vous souhaitez répertorier les commentaires.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Définissez le nombre maximal de commentaires que [!DNL Workfront Fusion] renverra pendant un cycle d’exécution.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a Comment]

Ce module d’action modifie un commentaire existant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Sélectionnez ou mappez l’équipe propriétaire du projet qui contient la ressource dont vous souhaitez mettre à jour un commentaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Sélectionnez le projet qui contient la ressource dont vous souhaitez mettre à jour un commentaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td> <p>Sélectionnez le dossier contenant la ressource dont vous souhaitez mettre à jour un commentaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Sélectionnez la ressource dont vous souhaitez mettre à jour un commentaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>Sélectionnez le commentaire à mettre à jour.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p> Saisissez le contenu textuel du commentaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp] </td> 
   <td> <p>Saisissez le numéro de l’image dans la vidéo à laquelle le commentaire est lié.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Comment Updated]

Ce module déclencheur lance un scénario lorsqu’un commentaire est modifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name] </td> 
   <td> <p>Saisissez le nom du webhook, par exemple Commentaire modifié.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Sélectionnez l’équipe pour laquelle ce webhook est créé.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch New Comment]

Ce module déclencheur lance un scénario lors de la création d’un commentaire ou d’une réponse.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name] </td> 
   <td> <p>Saisissez le nom du webhook, par exemple : Nouveau commentaire.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Sélectionnez l’équipe pour laquelle ce webhook est créé.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Projets

#### [!UICONTROL List Projects]

Ce module de recherche récupère tous les projets pour l’équipe spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Team ID] </td> 
   <td> <p>Sélectionnez ou mappez l’équipe dont vous souhaitez récupérer les projets.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Définissez le nombre maximal de projets que [!DNL Workfront Fusion] renverra pendant un cycle d’exécution.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Autre

#### [!UICONTROL Make an API Call]

Ce module vous permet d’effectuer un appel API personnalisé.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frame-io-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Saisissez un chemin relatif à <code>https://api.frame.io</code>. Exemple : <code> /v2/teams</code></p> <p>Note : pour obtenir la liste des points d’entrée disponibles, voir la référence de l’API [!DNL Frame.io].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Méthodes de requête HTTP dans [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Ajoute automatiquement des en-têtes d’autorisation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String] </td> 
   <td> <p>Saisissez la chaîne de requête. Pour chaque paramètre que vous souhaitez inclure dans la chaîne de requête, cliquez sur <b>[!UICONTROL Add item]</b> et saisissez le nom du champ et la valeur souhaitée.</p> </td> 
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

**Exemple :** l’appel API suivant renvoie toutes les équipes et les détails de cet appel dans votre compte [!DNL Frame.io] :

URL : `/v2/teams`

Méthode : `GET`

![](/help/workfront-fusion/references/apps-and-modules/assets/api-call-example.png)

Le résultat se trouve dans la sortie du module sous Lot > Corps.

Dans notre exemple, les détails d’une équipe ont été renvoyés :

![](/help/workfront-fusion/references/apps-and-modules/assets/api-call-output.png)
