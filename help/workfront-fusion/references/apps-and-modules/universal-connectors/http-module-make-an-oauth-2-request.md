---
title: Module HTTP > Effectuer une requête OAuth 2.0
description: Pour effectuer une requête HTTP(S)  [!DNL Adobe Workfront Fusion]  auprès de serveurs nécessitant une autorisation OAuth 2.0, vous devez d’abord créer une connexion OAuth. [!DNL Adobe Workfront Fusion]  s’assure que tous les appels effectués avec cette connexion comportent les en-têtes d’autorisation appropriés et actualise automatiquement les jetons associés lorsque cela est nécessaire.
author: Becky
feature: Workfront Fusion
exl-id: a302a1d4-fddf-4a71-adda-6b87ff7dba4b
source-git-commit: 3ba5d67806e0d495bd4a91589d06cfb9adb25c0c
workflow-type: tm+mt
source-wordcount: '1918'
ht-degree: 83%

---

# [!UICONTROL HTTP] > module [!UICONTROL Make an OAuth 2.0 request]

>[!NOTE]
>
>[!DNL Adobe Workfront Fusion] nécessite une licence [!DNL Adobe Workfront Fusion] en plus d’une licence [!DNL Adobe Workfront].

Pour effectuer une requête HTTP(S) [!DNL Adobe Workfront Fusion] auprès de serveurs nécessitant une autorisation OAuth 2.0, vous devez d’abord créer une connexion OAuth. [!DNL Adobe Workfront Fusion] s’assure que tous les appels effectués avec cette connexion comportent les en-têtes d’autorisation appropriés et actualise automatiquement les jetons associés lorsque cela est nécessaire.

[!DNL Workfront Fusion] prend en charge les flux d’authentification OAuth 2.0 suivants :

* Flux du code d’autorisation
* Flux implicite

D’autres flux, tels que le flux d’informations d’identification du mot de passe de la personne propriétaire de la ressource et le flux d’informations d’identification du client, ne sont pas automatiquement pris en charge par ce module.

Pour plus d’informations sur l’authentification OAuth 2.0, voir [Le framework d’autorisation OAuth 2.0](https://tools.ietf.org/html/rfc6749).

>[!NOTE]
>
>Si vous vous connectez à un produit Adobe qui n’a pas encore de connecteur dédié, il est recommandé d’utiliser le module Adobe Authenticator.
>
>Pour plus d’informations, voir [Module Adobe Authenticator](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md).

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

Pour connaître la formule, le type de licence ou l’accès dont vous disposez, contactez vote administrateur ou administratrice [!DNL Workfront].

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licenses [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)

## Création d’une connexion pour une requête [!DNL OAuth]

* [Instructions générales pour créer une connexion dans le module HTTP > Effectuer une requête OAuth 2.0](#general-instructions-for-creating-a-connection-in-the-http--make-an-oauth-20-request-module)
* [Instructions pour la création d’une connexion à Google dans le module de requête HTTP >[!UICONTROL Make] OAuth 2.0](#instructions-for-creating-a-connection-to-google-in-the-http-make-an-oauth-20-request-module)
* [Instructions pour se connecter à l’API Microsoft Graph via le module HTTP > Effectuer une requête OAuth 2.0](#instructions-for-connecting-to-microsoft-graph-api-via-the-http--make-an-oauth-20-request-module)

### Instructions générales pour créer une connexion dans le module [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request]

1. Créez un client OAuth dans le service [!DNL target] avec lequel vous voulez que [!DNL Adobe Workfront Fusion] communique. Cette option se trouve probablement dans la section [!UICONTROL Developer] du service donné.

   1. Lors de la création d’un client, saisissez l’URL appropriée dans le champ `[!UICONTROL Redirect URL]` ou `[!UICONTROL Callback URL]` :

      | Amériques/Asie-Pacifique | `https://app.workfrontfusion.com/oauth/cb/oauth2` |
      |---|---|
      | EMEA | `https://app-eu.workfrontfusion.com/oauth/cb/oauth2` |

   1. Après la création du client, le service en question affiche deux clés : `[!UICONTROL Client ID]` et `[!UICONTROL Client Secret]`. Certains services les appellent `[!UICONTROL App Key]` et `[!UICONTROL App Secret]`. Sauvegardez la clé et le secret dans un endroit sûr, afin de pouvoir les fournir lors de la création de la connexion dans Workfront Fusion.

1. Trouvez l’`[!UICONTROL Authorize URI]` et le `[!UICONTROL Token URI]` dans la documentation de l’API du service en question. Il s’agit d’adresses URL par lesquelles [!DNL Workfront Fusion] communique avec le service [!DNL target]. Les adresses servent à l’autorisation OAuth.

   >[!NOTE]
   >
   >Si le service utilise le flux implicite, vous n’avez besoin que de `[!UICONTROL Authorize URI]`.

   >[!INFO]
   >
   >**Exemple :** adresses Yahoo :
   >
   >* Authorize URI :
   >
   >`https://api.login.yahoo.com/oauth2/request_auth`
   >
   >* Token URI :
   >
   >`https://api.login.yahoo.com/oauth2/get_token`

1. (Le cas échéant) Si le service cible utilise des portées (droits d’accès), vérifiez comment le service sépare les portées individuelles et assurez-vous de définir le séparateur dans les paramètres avancés en conséquence. Si le séparateur n’est pas défini correctement, [!DNL Workfront Fusion] ne parvient pas à créer la connexion et vous recevez une erreur de portée non valide.
1. Après avoir effectué les étapes ci-dessus, vous pouvez commencer à créer la connexion OAuth dans [!DNL Workfront Fusion]. Ajoutez le module de traitement des demandes et des réponses HTTP(S) OAuth 2.0 à votre scénario.
1. Dans le champ Connexion du module, cliquez sur **[!UICONTROL Add]**.

1. Renseignez les champs suivants pour créer une connexion :

   <table style="table-layout:auto">  
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection name] </td> 
      <td> <p>Saisissez le nom de la connexion.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Flow type]</p> </td> 
      <td> <p>Sélectionnez le flux d’obtention des jetons.</p> 
       <ul> 
        <li><strong>[!UICONTROL Authorization Code]</strong>: renseignez les <code>[!UICONTROL Authorize URI]</code> et les <code>[!UICONTROL Token URI]</code> dans la documentation de l’API du service.</li> 
        <li><strong>[!UICONTROL Implicit]</strong>: saisissez le <code>[!UICONTROL Authorize URI]</code> dans la documentation de l’API du service.</li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Scope] </td> 
      <td> <p>Ajouter des portées individuelles. Vous trouverez ces informations dans la documentation destinée aux développeurs et développeuses (API) du service concerné.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Scope separator] </td> 
      <td> <p>Sélectionnez le séparateur des portées saisies ci-dessus. Vous trouverez ces informations dans la documentation destinée aux développeurs et développeuses (API) du service concerné.</p> <p>Attention : si le séparateur n’est pas défini correctement, [!DNL Workfront Fusion] ne parvient pas à créer la connexion et vous recevez une erreur de portée non valide.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client ID] </td> 
      <td> <p>Saisissez l’identifiant client. Vous obtenez l’identifiant client lorsque vous créez un client OAuth dans le service auquel vous souhaitez vous connecter.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client Secret]</td> 
      <td> <p> Saisissez le secret client. Vous obtenez le secret client lorsque vous créez un client OAuth dans le service auquel vous souhaitez vous connecter.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Authorize parameters]</p> </td> 
      <td> <p>Ajoutez les paramètres que vous souhaitez inclure dans l’appel d’autorisation. Les paramètres standard suivants sont toujours inclus automatiquement et ne doivent pas être ajoutés.</p> <p>Paramètres standard :</p> 
       <ul> 
        <li> <p><strong>[!UICONTROL response_type]</strong> </p> <p> <code>code </code>pour [!UICONTROL Authorization Code flow] et <code>token </code>pour [!UICONTROL Implicit flow]</p> </li> 
        <li> <p><strong>[!UICONTROL redirect_uri]</strong> </p> 
         <table style="table-layout:auto">  
          <col> 
          <col> 
          <tbody> 
           <tr> 
            <td role="rowheader">Amériques/Asie-Pacifique</td> 
            <td>https://app.workfrontfusion.com/oauth/cb/oauth2</td> 
           </tr> 
           <tr> 
            <td role="rowheader">EMEA </td> 
            <td>https://app-eu.workfrontfusion.com/oauth/cb/oauth2</td> 
           </tr> 
          </tbody> 
         </table> </li> 
        <li> <p><strong>[!UICONTROL client_id]</strong> </p> <p> L’identifiant client que vous avez reçu lors de la création du compte</p> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Access token parameters]</p> </td> 
      <td> <p>Ajoutez les paramètres que vous souhaitez inclure dans l’appel de jeton. Les paramètres standard suivants sont toujours inclus automatiquement et ne doivent pas être ajoutés.</p> <p>Paramètres standard :</p> 
       <ul> 
        <li><strong>[!UICONTROL grant_type]</strong>: <code>authorization_code</code></li> 
        <li> <p><strong>[!UICONTROL redirect_uri]:</strong> </p> 
         <table style="table-layout:auto">  
          <col> 
          <col> 
          <tbody> 
           <tr> 
            <td role="rowheader">Amériques/Asie-Pacifique</td> 
            <td>https://app.workfrontfusion.com/oauth/cb/oauth2</td> 
           </tr> 
           <tr> 
            <td role="rowheader">EMEA </td> 
            <td>https://app-eu.workfrontfusion.com/oauth/cb/oauth2</td> 
           </tr> 
          </tbody> 
         </table> </li> 
        <li><strong>[!UICONTROL client_id]</strong>: l’identifiant client que vous avez reçu lors de la création du compte est automatiquement inclus dans le corps de la requête</li> 
        <li><strong>client_secret</strong> : le secret du client ou de la cliente que vous avez reçu lors de la création du compte est automatiquement inclus dans le corps de la demande.</li> 
        <li><strong>code</strong> : le code renvoyé par la demande d’autorisation</li> 
       </ul> <p>Note :  <p>La norme OAuth 2.0 prend en charge au moins deux méthodes d’authentification du client ou de la cliente au cours de cette étape (<code>[!UICONTROL client_secret_basic]</code> et <code>[!UICONTROL client_secret_post]</code>). [!DNL Workfront Fusion] envoie automatiquement l’ID et le secret du client ou de la cliente spécifiés via la méthode <code>[!UICONTROL client_secret_post]</code>. Par conséquent, ces paramètres sont automatiquement inclus dans le corps de la demande de jeton. </p> <p>Pour plus d’informations sur l’authentification OAuth 2.0, voir <a href="https://tools.ietf.org/html/rfc6749">Framework d’autorisation OAuth 2.0</a>.</p> </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Refresh token parameters]</p> </td> 
      <td> <p>Ajoutez les paramètres que vous souhaitez inclure dans l’appel de jeton. Les paramètres standard suivants sont toujours inclus automatiquement et ne doivent pas être ajoutés.</p> <p>Paramètres standard :</p> 
       <ul> 
        <li> <p><strong>[!UICONTROL grant_type]</strong>: <code>refresh_token</code></p> </li> 
        <li> <p><strong>[!UICONTROL refresh_token]</strong>: jeton d’actualisation le plus récent obtenu par le service auquel vous vous connectez</p> </li> 
        <li> <p><strong>[!UICONTROL client_id]</strong>: l’identifiant client que vous avez reçu lors de la création du compte est automatiquement inclus dans le corps de la requête</p> </li> 
        <li> <p><strong>[!UICONTROL client_secret]</strong>: le secret client reçu lors de la création du compte est automatiquement inclus dans le corps de la requête</p> </li> 
       </ul> <p>Note :  <p>La norme OAuth 2.0 prend en charge au moins deux méthodes d’authentification du client ou de la cliente au cours de cette étape (<code>[!UICONTROL client_secret_basic]</code> et <code>[!UICONTROL client_secret_post]</code>). [!DNL Workfront Fusion] envoie automatiquement l’ID et le secret du client ou de la cliente spécifiés via la méthode <code>[!UICONTROL client_secret_post]</code>. Par conséquent, ces paramètres sont automatiquement inclus dans le corps de la demande de jeton. </p> <p>Pour plus d’informations sur l’authentification OAuth 2.0, voir <a href="https://tools.ietf.org/html/rfc6749">Framework d’autorisation OAuth 2.0</a>.</p> </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Custom Headers]</p> </td> 
      <td> <p>Spécifiez les clés et valeurs supplémentaires à inclure dans l’en-tête des étapes [!UICONTROL Token] et R[!UICONTROL efresh Token].</p> <p>Note :  <p>La norme OAuth 2.0 prend en charge au moins deux méthodes d’authentification du client ou de la cliente au cours de cette étape (<code>[!UICONTROL client_secret_basic]</code> et <code>[!UICONTROL client_secret_post]</code>). [!DNL Workfront Fusion] ne prend pas automatiquement en charge la méthode <code>[!UICONTROL client_secret_basic]</code>. Si le service auquel vous vous connectez prévoit que l’ID et le secret du client ou de la cliente soient combinés en une seule chaîne, puis encodés en base64 dans l’en-tête d’autorisation, vous devez ajouter cet en-tête et la valeur de la clé ici.</p> <p> Pour plus d’informations sur l’authentification OAuth 2.0, voir <a href="https://tools.ietf.org/html/rfc6749">Framework d’autorisation OAuth 2.0</a>.</p> </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Token placement]</p> </td> 
      <td> <p>Choisissez d’envoyer le jeton dans le [!UICONTROL header], le [!UICONTROL query string] ou les deux lors de la connexion à l’URL spécifiée.</p> <p>Les jetons sont le plus souvent envoyés dans l’en-tête de la demande.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Header token name] </td> 
      <td> <p>Saisissez le nom du jeton d’autorisation dans l’en-tête. Par défaut : <code>[!UICONTROL Bearer]</code>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Query string parameter name] </td> 
      <td> <p>Saisissez le nom du jeton d’autorisation dans la chaîne de requête. Par défaut : <code>[!UICONTROL access_token]</code>.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Cliquez sur **[!UICONTROL Continue]** pour enregistrer les paramètres de connexion.
1. Passez à [Configuration du module de requête OAuth 2.0](#oauth-20-request-module-setup).

### Instructions pour créer une connexion à [!DNL Google] dans le [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request module]

L’exemple suivant montre comment utiliser le module de requête [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0] pour vous connecter à [!DNL Google].

1. Assurez-vous d’avoir créé un projet, configuré les paramètres OAuth et généré vos informations d’identification comme décrit dans [Connecter  [!DNL Adobe Workfront Fusion]  à  [!DNL Google Services]  à l’aide d’un client OAuth personnalisé](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).
1. Ouvrez le module [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request] .
1. Cliquez sur **[!UICONTROL Add]** en regard de la zone de connexion.
1. Saisissez les valeurs suivantes :

   <table style="table-layout:auto">  
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection name] </td> 
      <td> <p>Saisissez le nom de la connexion.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Flow type]</p> </td> 
      <td> <p>[!UICONTROL Authorization Code]</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Authorize URI]</td> 
      <td><code>https://accounts.google.com/o/oauth2/v2/auth</code> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Token URI]</td> 
      <td><code>https://www.googleapis.com/oauth2/v4/token</code> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Scope] </td> 
      <td> <p>Ajouter des portées individuelles. Pour plus d’informations sur les portées, consultez <a href="https://developers.google.com/identity/protocols/oauth2/scopes?hl=fr">Portées OAuth 2.O pour les API [!DNL Google]</a> dans la documentation [!DNL Google].</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Scope separator] </td> 
      <td> <p>[!UICONTROL SPACE]</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client ID] </td> 
      <td> <p>Saisissez votre ID client [!DNL Google]. </p> <p>Pour créer un ID client, consultez <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md#create2" class="MCXref xref">Créer des informations d’identification OAuth</a> dans <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md" class="MCXref xref">[!DNL Connect Adobe Workfront Fusion] pour [!DNL Google Services] avec un client OAuth personnalisé</a>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client Secret]</td> 
      <td> <p>Saisissez votre secret client [!DNL Google]. </p> <p>Pour créer un secret client, consultez <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md#create2" class="MCXref xref">Créer des informations d’identification OAuth</a> dans <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md" class="MCXref xref">[!DNL Connect Adobe Workfront Fusion] pour les services [!DNL Google] avec un client OAuth personnalisé</a>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Authorize parameters]</p> </td> 
      <td> <p>Ajoutez la paire clé-valeur <code>[!UICONTROL access_type]</code> - <code>[!UICONTROL offline] </code>.</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/google-authentication-http.png"> </p> <p>Note : si vous rencontrez des problèmes d’authentification, par exemple lors de l’actualisation des jetons, essayez d’ajouter la paire clé-valeur <code>[!UICONTROL prompt] </code>- <code>[!UICONTROL consent] </code>.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Cliquez sur **[!UICONTROL Continue]** pour enregistrer les paramètres de connexion.
1. Passez à [Configuration du module de requête OAuth 2.0](#oauth-20-request-module-setup).

<!--### Instructions for connecting to [!DNL Microsoft Graph API] via the [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request] module 

For instructions regarding [!DNL Microsoft Graph API], see [Call the [!DNL MS Graph REST API] via the [!DNL Adobe Workfront Fusion] [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request] module](/help/workfront-fusion/create-scenarios/connect-to-apps/call-the-ms-graph-rest-api.md).-->

## Configuration du module de requête OAuth 2.0

Lorsque vous avez établi une connexion [!DNL Oauth 2].0 comme décrit dans [Créer une connexion pour une requête  [!DNL OAuth] ](#creating-a-connection-for-an-oauth-request), continuez à configurer le module comme vous le souhaitez. Tous les jetons d’autorisation sont automatiquement inclus dans cette requête et dans toute autre requête utilisant la même connexion.

Lorsque vous configurez le module [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request] , [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mapper des informations d’un module à l’autre dans  [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

<!--
<img src="" style="width: 350;height: 74;">
-->

<table style="table-layout:auto">  
 <col> 
 <col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la configuration d’une connexion, consultez <a href="#creating-a-connection-for-an-oauth-request" class="MCXref xref">Créer une connexion pour une requête OAuth</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Evaluate all states as errors (except for 2xx and 3xx]) </td> 
   <td> <p>Utilisez cette option pour configurer la gestion des erreurs.</p> <p>Pour plus d’informations, voir <a href="/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md" class="MCXref xref">Gestion des erreurs dans [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>Saisissez l’URL à laquelle vous souhaitez envoyer une requête, par exemple un point d’entrée API, un site web, etc.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Méthodes de requête HTTP dans [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers] </td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard. Par exemple, <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Saisissez les paires clé-valeur de requête souhaitées.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Body type]</p> </td> 
   <td> <p>Le corps du message HTTP est constitué des octets de données transmis dans un message de transaction HTTP, immédiatement après les en-têtes, le cas échéant.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p>Le type de corps Raw convient généralement à la plupart des requêtes HTTP, même dans les cas où la documentation de développement ne spécifie pas les données à envoyer.</p> <p>Spécifiez un formulaire d’analyse des données dans le champ [!UICONTROL Content type] .</p> <p>Peu importe le type de contenu sélectionné, les données peuvent être saisies dans n’importe quel format requis ou indiqué par la documentation de développement.</p> </li> 
     <li> <p><strong>[!UICONTROL Application/x-www-form-urlencoded]</strong> </p> <p>Ce type de corps est destiné aux données POST qui utilisent <code>[!UICONTROL application/x-www-form-urlencoded]</code>.</p> <p>Pour <code>[!UICONTROL application/x-www-form-urlencoded]</code>, le corps du message HTTP envoyé au serveur est essentiellement une unique chaîne de requête. Les clés et les valeurs sont encodées dans des paires clé-valeur séparées par <code>&amp;</code> et avec <code>=</code> entre la clé et la valeur. </p> <p>Pour les données binaires, <code>use [!UICONTROL multipart/form-data]</code> est utilisé à la place.</p> 
      <div class="example" data-mc-autonum="<b>Example: </b>">
       <span class="autonumber"><span><b>Exemple : </b></span></span> 
       <p>Exemple du format de requête HTTP obtenu :</p> 
       <p><code>field1=value1&amp;field2=value2</code> </p> 
      </div> </li> 
     <li> <p><strong>[!UICONTROL Multipart/form-data]</strong> </p> <p>Le [!UICONTROL Multipart/form-data] est une requête HTTP multipartie utilisée pour envoyer des fichiers et des données. Elle est fréquemment utilisée pour charger des fichiers sur le serveur.</p> <p>Ajouter des champs à envoyer dans la requête. Chaque champ doit contenir une paire clé-valeur.</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Text]</strong> </p> <p>Saisissez la clé et la valeur à envoyer dans le corps de la requête.</p> </li> 
       <li> <p><strong>[!UICONTROL File]</strong> </p> <p>Saisissez la clé et indiquez le fichier source à envoyer dans le corps de la requête.</p> <p>Mappez le fichier que vous souhaitez charger à partir du module précédent (par exemple [!UICONTROL HTTP] &gt;[!UICONTROL Get a File] ou [!UICONTROL Google Drive] &gt;[!UICONTROL Download a File)], ou saisissez manuellement le nom et les données du fichier.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Parse response]</p> </td> 
   <td> <p>Activez cette option pour analyser automatiquement les réponses et convertir les réponses JSON et XML, de sorte que vous n’ayez pas besoin d’utiliser les modules [!UICONTROL JSON] &gt; [!UICONTROL Parse JSON] ou [!UICONTROL XML] &gt; [!UICONTROL Parse XML].</p> <p>Avant de pouvoir utiliser du contenu JSON ou XML analysé, exécutez le module une fois manuellement afin qu’il puisse reconnaître le contenu de la réponse et vous permettre de le mapper dans les modules suivants.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timeout] </td> 
   <td> <p>Saisissez le délai d’expiration de la demande en secondes (1-300). La valeur par défaut est de 40 secondes.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Share cookies with other HTTP modules]</td> 
   <td> <p> Activez cette option pour partager les cookies du serveur avec tous les modules HTTP de votre scénario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Self-signed certificate]</td> 
   <td> <p> Chargez votre certificat si vous souhaitez utiliser TLS à l’aide de votre certificat auto-signé.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reject connections that are using unverified (self-signed) certificates] </td> 
   <td> <p>Activez cette option pour rejeter les connexions qui utilisent des certificats TLS non vérifiés.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Follow redirect]</td> 
   <td> <p> Activez cette option pour suivre les redirections d’URL avec les réponses 3xx.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Follow all redirects] </td> 
   <td> <p>Activez cette option pour suivre les redirections d’URL avec tous les codes de réponse.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Disable serialization of multiple same query string keys as arrays]</p> </td> 
   <td> <p>Par défaut, [!DNL Workfront Fusion] traite les valeurs multiples de la même clé de paramètre de chaîne de requête URL comme des tableaux. Par exemple, <code>www.test.com?foo=bar&amp;foo=baz</code> sera converti en <code>www.test.com?foo[0]=bar&amp;foo[1]=baz</code>. Activez cette option pour désactiver cette fonction. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Request compressed content]</td> 
   <td> <p> Activez cette option pour demander une version compressée du site web.</p> <p>Cette option ajoute un en-tête <code>[!UICONTROL Accept-Encoding]</code> pour demander du contenu compressé.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Use Mutual TLS]</td> 
   <td> <p>Activez cette option pour utiliser le protocole TLS mutuel dans la requête HTTP.</p> <p>Pour plus d’informations sur le protocole TLS mutuel, voir <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/use-mtls-in-http-modules.md" class="MCXref xref">Utiliser le protocole TLS mutuel dans les modules HTTP dans [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>
