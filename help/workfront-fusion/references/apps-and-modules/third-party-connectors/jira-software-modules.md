---
title: Modules de Jira Software
description: Dans un scénario  [!DNL Adobe Workfront Fusion] , vous pouvez automatiser les workflows qui utilisent  [!DNL Jira]  Software et le connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: 92cac080-d8f6-4770-a6a6-8934538c978b
source-git-commit: 4e45e691ed453cec5af1fa7b52204031af83f869
workflow-type: tm+mt
source-wordcount: '1881'
ht-degree: 73%

---

# Modules [!DNL Jira Software]

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!DNL Jira Software] et le connecter à plusieurs applications et services tiers.

Ces instructions s’appliquent aux modules Jira Cloud et Jira Server.

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

Pour utiliser les modules [!DNL Jira], vous devez disposer d’un compte [!DNL Jira].

## Informations sur l’API Jira

Le connecteur Jira utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"></td> 
   <td> Jira Cloud</td> 
   <td> Serveur Jira</td> 
  </tr> 
  <tr> 
   <td role="rowheader">apiVersion</td> 
   <td> 2</td> 
   <td> 2</td> 
  </tr> 
  <tr> 
   <td role="rowheader">apiVersionAgile</td> 
   <td> 1,0 </td> 
   <td> 1,0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>1,7,29</td> 
   <td>1,0,19</td> 
  </tr>
 </tbody> 
 </table>

## Connecter [!DNL Jira Software] à [!DNL Workfront Fusion]

La méthode de connexion dépend de si vous utilisez [!DNL Jira Cloud] ou [!DNL Jira Server].

* [Connecter  [!DNL Jira Cloud]  à Workfront Fusion](#connect-jira-cloud-to-workfront-fusion)
* [Connecter  [!DNL Jira Server]  à  [!DNL Workfront Fusion]](#connect-jira-server-to-workfront-fusion)

### Connecter [!DNL Jira Cloud] à [!DNL Workfront Fusion]

Connecter [!DNL Jira Cloud] à [!DNL Workfront Fusion]

Pour [!DNL Jira Software] connecter à [!DNL Workfront Fusion], vous devez créer un jeton API et l’insérer avec votre URL de service et votre nom d’utilisateur dans le champ [!UICONTROL Create a connection] de [!DNL Workfront Fusion].

#### Créer un jeton d’API dans [!DNL Jira]

1. Créez un jeton API dans Jira.

   Pour obtenir des instructions, nous vous recommandons de rechercher « Créer un jeton API » dans la documentation Jira.
1. Après avoir créé le jeton, copiez-le vers un emplacement sécurisé.

   >[!IMPORTANT]
   >
   >Vous ne pouvez plus visualiser le jeton après avoir fermé cette boîte de dialogue.
1. Conservez le jeton généré en lieu sûr.
1. Continuez avec [Configurer le jeton d’API  [!DNL Jira]  dans  [!DNL Workfront Fusion]](#configure-the-jira-api-token-in-workfront-fusion).

#### Configurer le jeton d’API [!DNL Jira] dans [!DNL Workfront Fusion]

1. Dans n’importe quel module de [!DNL Jira Cloud] de [!DNL Workfront Fusion], cliquez sur **[!UICONTROL Add]** en regard du champ [!UICONTROL connection] .
1. Indiquez les informations suivantes :

   * **Environnement**
   * **Type**
   * **[!UICONTROL Service URL]:** Il s’agit de l’URL de base que vous utilisez pour accéder à votre compte Jira. Exemple : `yourorganization.atlassian.net`
   * **[!UICONTROL Username]**
   * **[!UICONTROL API token]:** il s’agit du jeton API que vous avez créé dans la section [Créer un jeton API dans [!DNL Jira]](#create-an-api-token-in-jira) de cet article.

1. Cliquez sur [!UICONTROL Continue] pour créer la connexion et revenir au module .

### Connecter [!DNL Jira Server] à [!DNL Workfront Fusion]

Pour autoriser une connexion entre [!DNL Workfront Fusion] et [!DNL Jira Server], vous avez besoin de votre clé de consommateur ou consommatrice, de votre clé privée et de l’URL du service. Vous devrez peut-être contacter votre administrateur [!DNL Jira] pour cette information.

* [Générer des clés publiques et privées pour votre connexion  [!DNL Jira] ](#generate-public-and-private-keys-for-your-jira-connection)
* [Configurer l’application cliente en tant que consommatrice dans  [!DNL Jira]](#configure-the-client-app-as-a-consumer-in-jira)
* [Créer une connexion au serveur  [!DNL Jira]  ou au centre de données Jira dans  [!DNL Workfront Fusion]](#create-a-connection-to-jira-server-or-jira-data-center-in-workfront-fusion)

#### Générer des clés publiques et privées pour votre connexion [!DNL Jira]

Pour obtenir une clé privée pour votre connexion [!DNL Workfront Fusion Jira], vous devez générer des clés publiques et privées.

1. Dans votre terminal, exécutez les commandes `openssl` suivantes.

   * `openssl genrsa -out jira_privatekey.pem 1024`

     Cette commande génère une clé privée de 1 024 bits.

   * `openssl req -newkey rsa:1024 -x509 -key jira_privatekey.pem -out jira_publickey.cer -days 365`

     Cette commande crée un certificat X509.

   * `openssl pkcs8 -topk8 -nocrypt -in jira_privatekey.pem -out jira_privatekey.pcks8`

     Cette commande extrait la clé privée (format PKCS8) dans le fichier `jira_privatekey.pcks8`.

   * `openssl x509 -pubkey -noout -in jira_publickey.cer  > jira_publickey.pem`

     Cette commande permet d’extraire la clé publique du certificat dans le fichier `jira_publickey.pem`.

     >[!NOTE]
     >
     >Si vous utilisez Windows, vous devrez peut-être enregistrer manuellement la clé publique dans le fichier `jira_publickey.pem` :
     >
     >1. Dans votre terminal, exécutez la commande suivante :
     >   
     >   `openssl x509 -pubkey -noout -in jira_publickey.cer`
     >   
     >1. Copiez la sortie du terminal, y compris `-------BEGIN PUBLIC KEY--------` et `-------END PUBLIC KEY--------`.
     >   
     >1. Collez la sortie du terminal dans un fichier nommé `jira_publickey.pem`.


1. Continuez à [configurer l’application cliente en tant que consommatrice dans  [!DNL Jira]](#configure-the-client-app-as-a-consumer-in-jira).

#### Configurez l’application cliente en tant que consommatrice dans [!DNL Jira].

1. Connectez-vous à votre instance [!DNL Jira].
1. Dans le panneau de navigation de gauche, cliquez sur **[!UICONTROL [!DNL Jira] Settings]** ![](/help/workfront-fusion/references/apps-and-modules/assets/jira-settings-icon.png) > **[!UICONTROL Applications]** > **[!UICONTROL Application links]**.
1. Dans le champ **[!UICONTROL Enter the URL of the application you want to link]** , saisissez

   ```
   https://app.workfrontfusion.com/oauth/cb/workfront-jiraserver-oauth1
   ```

1. Cliquez sur **[!UICONTROL Create new link]**. Ignorez le message d’erreur « Aucune réponse n’a été reçue de l’URL que vous avez saisie ».
1. Dans la fenêtre **[!UICONTROL Link applications]** , saisissez les valeurs dans les champs **[!UICONTROL Consumer key]** et **[!UICONTROL Shared secret]** .

   Vous pouvez choisir les valeurs de ces champs.

1. Copiez les valeurs des champs **[!UICONTROL Consumer key]** et **[!UICONTROL Shared secret]** vers un emplacement sécurisé.

   Vous aurez besoin de ces valeurs plus tard dans le processus de configuration.

1. Remplissez les champs de l’URL comme suit :

   | champ | Description |
   |---|---|
   | [!UICONTROL Request Token URL] | `<Jira base url>/plugins/servlet/oauth/request-token` |
   | [!UICONTROL Authorization URL] | `<Jira base url>/plugins/servlet/oauth/authorize` |
   | [!UICONTROL Access Token URL] | `<Jira base url>/plugins/servlet/oauth/access-token` |

1. Cochez la case **[!UICONTROL Create incoming link]** .
1. Cliquez sur **[!UICONTROL Continue]**.
1. Dans la fenêtre **[!UICONTROL Link applications]**, renseignez les champs suivants :

   <table style="table-layout:auto"> 
    <col data-mc-conditions=""> 
    <col data-mc-conditions=""> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Consumer Key]</p> </td> 
      <td> Collez la clé de consommateur que vous avez copiée dans un endroit sûr.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Consumer name]</td> 
      <td>Saisissez le nom de votre choix. Ce nom est destiné à vous servir de référence.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Public key]</td> 
      <td>Collez la clé publique de votre fichier <code>[!DNL jira_publickey.pem]</code>.</td> 
     </tr> 
    </tbody> 
   </table>

1. Cliquez sur **[!UICONTROL Continue]**.
1. Continuez vers [Créer une connexion à  [!DNL Jira Server]  ou  [!DNL Jira Data Center]  dans  [!DNL Workfront Fusion]](#create-a-connection-to-jira-server-or-jira-data-center-in-workfront-fusion).

#### Créer une connexion à [!DNL Jira Server] ou [!DNL Jira Data Center] dans [!DNL Workfront Fusion]

>[!NOTE]
>
>Utilisez l’application [!DNL Jira Server] pour vous connecter à [!DNL Jira Server] ou [!DNL Jira Data Center].

1. Dans n’importe quel module de [!DNL Jira Server] de [!DNL Workfront Fusion], cliquez sur **[!UICONTROL Add]** en regard du champ [!UICONTROL connection] .
1. Dans le panneau [!UICONTROL Create a connection], renseignez les champs suivants :

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td> <p>Saisir le nom de la connexion</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Environment]</p> </td> 
      <td> <p>Choisissez si vous utilisez un environnement de production ou hors production.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Type]</p> </td> 
      <td> <p>Choisissez si vous utilisez un compte de service ou un compte personnel.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Consumer Key]</td> 
      <td>Collez la clé de consommateur que vous avez copiée dans un endroit sûr dans <a href="#configure-the-client-app-as-a-consumer-in-jira" class="MCXref xref">Configurer l’application client en tant que consommatrice dans [!DNL Jira]</a>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!DNL Private Key]</td> 
      <td>Collez la clé privée du fichier <code>[!DNL jira_privatekey.pcks8]</code> que vous avez créé dans <a href="#generate-public-and-private-keys-for-your-jira-connection" class="MCXref xref">Générer des clés publiques et privées pour votre connexion [!DNL Jira]</a>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!DNL Service URL]</td> 
      <td>Saisissez l’URL de votre instance [!DNL Jira]. Exemple : <code>yourorganization.atlassian.net</code></td> 
     </tr> 
    </tbody> 
   </table>

1. Cliquez sur **[!UICONTROL Continue]** pour créer la connexion et revenir au module .

## Modules [!DNL Jira Software] et leurs champs

Lorsque vous configurez les modules [!DNL Jira Software], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Jira Software] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Déclencheurs](#triggers)
* [Actions](#actions)
* [Recherches](#searches)

### Déclencheurs

#### [!UICONTROL Watch for records]

Ce module déclencheur lance un scénario lorsqu’un enregistrement est ajouté, mis à jour ou supprimé.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Sélectionnez le webhook que vous souhaitez utiliser pour surveiller les enregistrements. </p> <p>Pour ajouter un nouveau webhook :</p> 
    <ol> 
     <li value="1">Cliquez sur <strong>[!UICONTROL Add]</strong></li> 
     <li value="2">Saisissez un nom pour le webhook.</li> 
     <li value="3"> <p>Sélectionnez la connexion que vous souhaitez utiliser pour votre webhook. </p> <p>Pour savoir comment connecter votre compte [!DNL Jira Software] à [!DNL Workfront Fusion], consultez l’article <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL Jira Software] à [!DNL Workfront Fusion]</a>.</p> </li> 
     <li value="4"> <p>Sélectionnez le type d’enregistrement que vous souhaitez que le logiciel surveille :</p> 
      <ul> 
       <li>[!UICONTROL Comment] </li> 
       <li>[!UICONTROL Issue]</li> 
       <li>[!UICONTROL Project] </li> 
       <li>[!UICONTROL Sprint]</li> 
      </ul> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [[!UICONTROL Add issue to sprint]](#add-issue-to-sprint)
* [[!UICONTROL Create a Record]](#create-a-record)
* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Delete a record]](#delete-a-record)
* [[!UICONTROL Download an attachment]](#download-an-attachment)
* [[!UICONTROL Read a record]](#read-a-record)
* [[!UICONTROL Update a record]](#update-a-record)

#### [!UICONTROL Add issue to sprint]

Ce module d’action ajoute un ou plusieurs problèmes à un sprint.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Jira Software] à [!DNL Workfront Fusion], voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL Jira Software] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sprint ID]</td> 
   <td>Saisissez ou mappez l’ID du sprint auquel vous souhaitez ajouter un problème.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Issue ID or Keys]</td> 
   <td>Pour chaque événement ou clé que vous souhaitez voir l’expérience, cliquez sur <b>[!UICONTROL Add item]</b> et saisissez l’ID d’événement ou la clé. Vous pouvez saisir jusqu’à 50 dans un seul module.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Record]

Ce module d’action crée un nouvel enregistrement dans Jira.

Le module renvoie tous les champs standard associés à l’enregistrement, ainsi que tous les champs et valeurs personnalisés auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Jira Software] à [!DNL Workfront Fusion], voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL Jira Software] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Sélectionnez le type d'enregistrement que vous souhaitez créer par le module, puis renseignez les autres champs spécifiques à ce type d'enregistrement qui apparaîtront dans le module.</p> 
    <ul> 
     <li>[!UICONTROL Attachment]</li> 
     <li>[!UICONTROL Comment]</li> 
     <li>[!UICONTROL Issue]</li> 
     <li>[!UICONTROL Project]</li> 
     <li>[!UICONTROL Sprint] </li> 
     <li>[!UICONTROL Worklog]</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Custom API Call]

Ce module d’action vous permet d’effectuer un appel personnalisé et authentifié à l’API [!DNL Jira Software]. Utilisez ce module pour créer une automatisation du flux de données qui ne peut pas être effectuée par les autres modules [!DNL Jira Software].

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Jira Software] à [!DNL Workfront Fusion], voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL Jira Software] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Saisir un chemin relatif à<code>&lt;Instance URL>/rest/api/2/ </code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP dans [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] ajoute les en-têtes d’autorisation pour vous.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Ajoutez la requête pour l’appel API sous la forme d’un objet JSON standard.</p> <p>Par exemple : <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre JSON, placez les guillemets à l’extérieur de l’instruction conditionnelle.</p> 
     <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png">  </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a record]

Ce module d&#39;action supprime l&#39;enregistrement spécifié.

Vous indiquez l’ID de l’enregistrement.

Le module renvoie l’ID de l’enregistrement et tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Jira Software] à [!DNL Workfront Fusion], voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL Jira Software] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement que vous souhaitez que le module supprime. </p> 
    <ul> 
     <li>[!UICONTROL Attachment]</li> 
     <li>[!UICONTROL Comment]</li> 
     <li>[!UICONTROL Issue]</li> 
     <li>[!UICONTROL Project]</li> 
     <li>[!UICONTROL Sprint] </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID or Key]</td> 
   <td>Saisissez ou mappez l’ID ou la clé de l’enregistrement que vous souhaitez supprimer.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download an attachment]

Ce module d’action télécharge une pièce jointe particulière.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Jira Software] à [!DNL Workfront Fusion], voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL Jira Software] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Saisissez ou mappez l’ID de la pièce jointe que vous souhaitez télécharger.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a record]

Ce module d’action lit les données d’un seul enregistrement dans [!DNL Jira Software].

Vous indiquez l’ID de l’enregistrement.

Le module renvoie tous les champs standard associés à l’enregistrement, ainsi que tous les champs et valeurs personnalisés auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Jira Software] à [!DNL Workfront Fusion], voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL Jira Software] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement [!DNL Jira] que vous souhaitez que le module lise.</p> 
    <ul> 
     <li>[!UICONTROL Attachment]</li> 
     <li>[!UICONTROL Issue]</li> 
     <li>[!UICONTROL Project]</li> 
     <li>[!UICONTROL Sprint] </li> 
     <li>[!UICONTROL User]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Sélectionnez les sorties que vous souhaitez recevoir. Les options de sortie sont disponibles en fonction du type d’enregistrement sélectionné dans le champ « [!UICONTROL Record Type] ».</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td> <p>Saisissez ou mappez l’ID unique [!DNL Jira Software] de l’enregistrement que vous souhaitez que le module lise.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a record]

Ce module d’action met à jour un enregistrement existant, tel qu’une question ou un projet.

Vous indiquez l’ID de l’enregistrement.

Le module renvoie l’ID de l’enregistrement et tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Jira Software] à [!DNL Workfront Fusion], voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL Jira Software] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement que vous souhaitez que le module mette à jour. Lorsque vous sélectionnez un type d’enregistrement, d’autres champs spécifiques à ce type d’enregistrement apparaissent dans le module.</p> 
    <ul> 
     <li>[!UICONTROL Comment]</li> 
     <li>[!UICONTROL Issue]</li> 
     <li>[!UICONTROL Project]</li> 
     <li>[!UICONTROL Sprint] </li> 
     <li>[!UICONTROL Transition issue]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID or Key]</td> 
   <td>Saisissez ou mappez l'identifiant ou la clé de l'enregistrement à mettre à jour, puis renseignez les autres champs spécifiques à ce type d'enregistrement qui apparaîtront dans le module.</td> 
  </tr> 
 </tbody> 
</table>

### Recherches

* [[!UICONTROL List records]](#list-records)
* [[!UICONTROL Search for records]](#search-for-records)

#### [!UICONTROL List records]

Ce module de recherche permet de retrouver tous les éléments d’un type spécifique qui correspondent à votre requête de recherche.

Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Jira Software] à [!DNL Workfront Fusion], voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL Jira Software] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement que vous souhaitez voir figurer dans le module. Lorsque vous sélectionnez un type d’enregistrement, d’autres champs spécifiques à ce type d’enregistrement apparaissent dans le module.</p> 
    <ul> 
     <li>[!UICONTROL Comment]</li> 
     <li>[!UICONTROL Issue]</li> 
     <li>[!UICONTROL Project]</li> 
     <li>[!UICONTROL Sprint issue]</li> 
     <li>[!UICONTROL Worklog]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Max Results]</p> </td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que vous souhaitez que le module récupère au cours de chaque cycle d’exécution du scénario.</p> </td> 
  </tr> <!--
   <tr> 
    <td role="rowheader">Offset</td> 
    <td> Enter or map the ID of the first item you want to retrieve details for. This is a way to paginate the records. If you enter the 5000th item as the offset, the module would return items 5000-9999.</td> 
   </tr>
  --> 
 </tbody> 
</table>

#### [!UICONTROL Search for records]

Ce module de recherche recherche les enregistrements dans un objet dans [!DNL Jira Software] qui correspondent à la requête que vous avez spécifiée.

Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Jira Software] à [!DNL Workfront Fusion], voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connecter [!DNL Jira Software] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement que vous souhaitez que le module recherche. Lorsque vous sélectionnez un type d’enregistrement, d’autres champs spécifiques à ce type d’enregistrement apparaissent dans le module.</p> 
    <ul> 
     <li>[!UICONTROL Issues]</li> 
     <li> <p>[!UICONTROL Issues by JQL (Jira Query Lanuguage)] </p> <p>Pour plus d’informations sur JQL, consultez l’article <a href="https://www.atlassian.com/blog/jira-software/jql-the-most-flexible-way-to-search-jira-14#:~:text=JQLstandsforJiraQuery,projectmanagers%2Candbusinessusers.">JQL</a> sur le site d’aide d’Atlassian. </p> </li> 
     <li>[!UICONTROL Project]</li> 
     <li>[!UICONTROL Project by issue]</li> 
     <li>[!UICONTROL User]</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
