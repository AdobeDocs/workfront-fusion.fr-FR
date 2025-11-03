---
title: Modules de Jira Software
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent  [!DNL Jira]  logiciel, ainsi que les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: 92cac080-d8f6-4770-a6a6-8934538c978b
source-git-commit: d4bdc4005a3b7b22d64adc8ca1d20bcf534ddfd1
workflow-type: tm+mt
source-wordcount: '2466'
ht-degree: 65%

---

# Modules [!DNL Jira Software]

>[!NOTE]
>
>Ces instructions s’appliquent aux anciens connecteurs Jira Cloud et Jira Server. Pour plus d’informations sur la nouvelle version du connecteur Jira, qui est simplement étiquetée Jira, voir [Modules Jira](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-modules-new.md).

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent [!DNL Jira Software] et les connecter à plusieurs applications et services tiers.

Ces instructions s’appliquent aux modules Jira Cloud et Jira Server.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <td> 1.0 </td> 
   <td> 1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>1,7,29</td> 
   <td>1,0,19</td> 
  </tr>
 </tbody> 
 </table>

## Connecter [!DNL Jira Software] à Workfront Fusion

La méthode de connexion dépend de si vous utilisez [!DNL Jira Cloud] ou [!DNL Jira Server].

* [Connecter  [!DNL Jira Cloud]  à Workfront Fusion](#connect-jira-cloud-to-workfront-fusion)
* [Connecter  [!DNL Jira Server]  à Workfront Fusion](#connect-jira-server-to-workfront-fusion)

### Connecter [!DNL Jira Cloud] à Workfront Fusion

Connecter [!DNL Jira Cloud] à Workfront Fusion

Pour [!DNL Jira Software] connecter à Workfront Fusion, vous devez créer un jeton API et l’insérer avec votre URL de service et votre nom d’utilisateur dans le champ [!UICONTROL Créer une connexion] de Workfront Fusion.

#### Créer un jeton d’API dans [!DNL Jira]

1. Créez un jeton API dans Jira.

   Pour obtenir des instructions, nous vous recommandons de rechercher « Créer un jeton API » dans la documentation Jira.
1. Après avoir créé le jeton, copiez-le vers un emplacement sécurisé.

   >[!IMPORTANT]
   >
   >Vous ne pouvez plus visualiser le jeton après avoir fermé cette boîte de dialogue.
1. Conservez le jeton généré en lieu sûr.
1. Continuez avec [Configurer le jeton  [!DNL Jira] ’API dans Workfront Fusion](#configure-the-jira-api-token-in-workfront-fusion).

#### Configuration du jeton API [!DNL Jira] dans Workfront Fusion

1. Dans n’importe quel module de [!DNL Jira Cloud] de Workfront Fusion, cliquez sur **[!UICONTROL Ajouter]** en regard du champ [!UICONTROL connexion].
1. Indiquez les informations suivantes :

   * **Environnement**
   * **Type**
   * **[!UICONTROL URL du service] :** il s’agit de l’URL de base que vous utilisez pour accéder à votre compte Jira. Exemple : `yourorganization.atlassian.net`
   * **[!UICONTROL Le nom d’utilisateur ou d’utilisatrice]**
   * **[!UICONTROL Le jeton d’API] :** il s’agit du jeton d’API que vous avez créé dans la section [Créer un jeton d’API dans [!DNL Jira]](#create-an-api-token-in-jira) de cet article.

1. Cliquez sur [!UICONTROL Continuer] pour créer la connexion et revenir au module.

### Connecter [!DNL Jira Server] à Workfront Fusion

Pour autoriser une connexion entre Workfront Fusion et [!DNL Jira Server], vous avez besoin de votre clé de client, de votre clé privée et de l’URL du service. Vous devrez peut-être contacter votre administrateur [!DNL Jira] pour cette information.

* [Générer des clés publiques et privées pour votre connexion  [!DNL Jira] &#x200B;](#generate-public-and-private-keys-for-your-jira-connection)
* [Configurer l’application cliente en tant que consommatrice dans  [!DNL Jira]](#configure-the-client-app-as-a-consumer-in-jira)
* [Création d’une connexion  [!DNL Jira] serveur ou au centre de données Jira dans Workfront Fusion](#create-a-connection-to-jira-server-or-jira-data-center-in-workfront-fusion)

#### Générer des clés publiques et privées pour votre connexion [!DNL Jira]

Pour acquérir une clé privée pour votre connexion [!DNL Workfront Fusion Jira], vous devez générer des clés publiques et privées. Cette opération s’effectue via le terminal de votre ordinateur. Vous pouvez localiser votre terminal en recherchant terminal dans le menu de démarrage ou la barre de recherche de votre ordinateur (et non dans la barre de recherche de votre navigateur).

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
1. Dans le panneau de navigation de gauche, cliquez sur **[!UICONTROL [!DNL Jira]les paramètres]** ![icône des paramètres Jira](/help/workfront-fusion/references/apps-and-modules/assets/jira-settings-icon.png) > **[!UICONTROL Applications]**> **[!UICONTROL Liens d’application]**.
1. Dans le champ **[!UICONTROL Entrer l’URL de l’application que vous voulez lier]**, entrez :

   ```
   https://app.workfrontfusion.com/oauth/cb/workfront-jiraserver-oauth1
   ```

1. Cliquez sur **[!UICONTROL Créer un lien]**. Ignorez le message d’erreur « Aucune réponse n’a été reçue de l’URL que vous avez saisie ».
1. Dans la fenêtre **[!UICONTROL Lier les applications]**, entrez des valeurs dans les champs **[!UICONTROL Clé de consommateur ou consommatrice]** et **[!UICONTROL Secret partagé]**.

   Vous pouvez choisir les valeurs de ces champs.

1. Copiez les valeurs des champs **[!UICONTROL Clé de consommateur ou consommatrice]** et **[!UICONTROL Secret partagé]** dans un endroit sûr.

   Vous aurez besoin de ces valeurs plus tard dans le processus de configuration.

1. Remplissez les champs de l’URL comme suit :

   | champ | Description |
   |---|---|
   | [!UICONTROL URL du jeton de demande] | `<Jira base url>/plugins/servlet/oauth/request-token` |
   | [!UICONTROL URL d’autorisation] | `<Jira base url>/plugins/servlet/oauth/authorize` |
   | [!UICONTROL URL du jeton d’accès] | `<Jira base url>/plugins/servlet/oauth/access-token` |

1. Cochez la case **[!UICONTROL Créer un lien entrant]**.
1. Cliquez sur **[!UICONTROL Continuer]**.
1. Dans la fenêtre **[!UICONTROL Lier les applications]**, remplissez les champs suivants :

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

1. Cliquez sur **[!UICONTROL Continuer]**.
1. Passez à [Créer une connexion à ou [!DNL Jira Server] dans Workfront Fusion [!DNL Jira Data Center]  &#x200B;](#create-a-connection-to-jira-server-or-jira-data-center-in-workfront-fusion)

#### Créer une connexion à [!DNL Jira Server] ou [!DNL Jira Data Center] dans Workfront Fusion

>[!NOTE]
>
>Utilisez l’application [!DNL Jira Server] pour vous connecter à [!DNL Jira Server] ou [!DNL Jira Data Center].

1. Dans n’importe quel module de [!DNL Jira Server] de Workfront Fusion, cliquez sur **[!UICONTROL Ajouter]** en regard du champ [!UICONTROL connexion].
1. Dans le panneau [!UICONTROL Créer une connexion], remplissez les champs suivants :

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td> <p>Saisissez un nom pour la connexion.</p> </td> 
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

1. Cliquez sur **[!UICONTROL Continuer]** pour créer la connexion et retourner au module.

## Modules [!DNL Jira Software] et leurs champs

Lorsque vous configurez les modules [!DNL Jira Software], Workfront Fusion affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Jira Software] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Déclencheurs](#triggers)
* [Actions](#actions)
* [Recherches](#searches)

### Déclencheurs

#### [!UICONTROL Surveiller des enregistrements]

Ce module déclencheur lance un scénario lorsqu’un enregistrement est ajouté, mis à jour ou supprimé.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Sélectionnez le webhook que vous souhaitez utiliser pour surveiller les enregistrements. </p> <p>Pour ajouter un nouveau webhook :</p> 
    <ol> 
     <li value="1">Cliquez sur <strong>[!UICONTROL Add]</strong>.</li> 
     <li value="2">Saisissez un nom pour le webhook.</li> 
     <li value="3"> <p>Sélectionnez la connexion que vous souhaitez utiliser pour votre webhook. </p> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Jira Software] à Workfront Fusion, voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de [!DNL Jira Software] à Workfront Fusion</a> dans cet article.</p> </li> 
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

* [[!UICONTROL Ajouter un problème au sprint]](#add-issue-to-sprint)
* [[!UICONTROL Créer un enregistrement]](#create-a-record)
* [[!UICONTROL Appel API personnalisé]](#custom-api-call)
* [[!UICONTROL Supprimer un enregistrement]](#delete-a-record)
* [[!UICONTROL Télécharger une pièce jointe]](#download-an-attachment)
* [[!UICONTROL Lire un enregistrement]](#read-a-record)
* [[!UICONTROL Mettre à jour un enregistrement]](#update-a-record)

#### [!UICONTROL Ajouter un problème au sprint]

Ce module d’action ajoute un ou plusieurs problèmes à un sprint.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Jira Software] à Workfront Fusion, voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de [!DNL Jira Software] à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sprint ID]</td> 
   <td>Saisissez ou mappez l’ID du sprint auquel vous souhaitez ajouter un problème.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Issue ID or Keys]</td> 
   <td>Pour chaque événement ou clé que vous souhaitez voir l’expérience, cliquez sur <b>[!UICONTROL Add item]</b> et saisissez l’identifiant ou la clé de l’événement. Vous pouvez saisir jusqu’à 50 dans un seul module.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Créer un enregistrement]

Ce module d’action crée un nouvel enregistrement dans Jira.

Le module renvoie tous les champs standard associés à l’enregistrement, ainsi que tous les champs et valeurs personnalisés auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Jira Software] à Workfront Fusion, voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de [!DNL Jira Software] à Workfront Fusion</a> dans cet article.</p> </td> 
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

#### [!UICONTROL Appel API personnalisé]

Ce module d’action vous permet d’effectuer un appel personnalisé et authentifié à l’API [!DNL Jira Software]. Utilisez ce module pour créer une automatisation du flux de données qui ne peut pas être effectuée par les autres modules [!DNL Jira Software].

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Jira Software] à Workfront Fusion, voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de [!DNL Jira Software] à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Saisir un chemin relatif à<code>&lt;Instance URL>/rest/api/2/ </code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion ajoute les en-têtes d’autorisation pour vous.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Ajoutez la requête pour l’appel API sous la forme d’un objet JSON standard.</p> <p>Par exemple : <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lors de l’utilisation d’instructions conditionnelles telles que <code>if</code> dans votre fichier JSON, placez les guillemets en dehors de l’instruction conditionnelle.</p> 
     <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png">  </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Supprimer un enregistrement]

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
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Jira Software] à Workfront Fusion, voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de [!DNL Jira Software] à Workfront Fusion</a> dans cet article.</p> </td> 
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

#### [!UICONTROL Télécharger une pièce jointe]

Ce module d’action télécharge une pièce jointe particulière.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Jira Software] à Workfront Fusion, voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de [!DNL Jira Software] à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Saisissez ou mappez l’ID de la pièce jointe que vous souhaitez télécharger.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Lire un enregistrement]

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
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Jira Software] à Workfront Fusion, voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de [!DNL Jira Software] à Workfront Fusion</a> dans cet article.</p> </td> 
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
   <td>Sélectionnez les sorties que vous souhaitez recevoir. Les options de sortie sont disponibles en fonction du type d’enregistrement sélectionné dans le champ [!UICONTROL Record Type].</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td> <p>Saisissez ou mappez l’identifiant unique [!DNL Jira Software] de l’enregistrement que vous souhaitez que le module lise.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Lire un enregistrement]

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
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Jira Software] à Workfront Fusion, voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de [!DNL Jira Software] à Workfront Fusion</a> dans cet article.</p> </td> 
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

* [[!UICONTROL Liste des enregistrements]](#list-records)
* [[!UICONTROL Rechercher des enregistrements]](#search-for-records)

>[!IMPORTANT]
>
>Le module de recherche utilisé par le connecteur Jira hérité peut entraîner l’erreur suivante :
>
>`[410] The requested API has been removed. Please migrate to the /rest/api/3/search/jql API. A full migration guideline is available at https://developer.atlassian.com/changelog/#CHANGE-2046`
>
>Cela est dû à une obsolescence du côté de Jira.
>
>Si vous rencontrez cette erreur, vous pouvez remplacer le module de recherche du connecteur Jira hérité par celui du nouveau connecteur. Notez que le nouveau connecteur permet de sélectionner la version d’API utilisée. Veillez à sélectionner V3 lors de la création de la connexion.
>
> ![Option de version de l’API dans le nouveau connecteur Jira](/help/workfront-fusion/references/apps-and-modules/assets/jira-version-option.png)
>
>Notez que :
>
>* Seul le module de recherche est affecté. Actuellement, les autres points d’entrée de l’API Jira utilisés par le connecteur Fusion ne sont pas affectés par cette obsolescence.
>
>* Le déploiement géographique peut entraîner des incohérences. Atlassian déploie cette modification à l’échelle régionale, ce qui signifie que certaines instances Jira Cloud peuvent toujours prendre temporairement en charge les points d’entrée plus anciens. Cela peut entraîner un comportement incohérent entre les environnements.

#### [!UICONTROL Liste des enregistrements]

Ce module de recherche permet de retrouver tous les éléments d’un type spécifique qui correspondent à votre requête de recherche.

Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Jira Software] à Workfront Fusion, voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de [!DNL Jira Software] à Workfront Fusion</a> dans cet article.</p> </td> 
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

#### [!UICONTROL Rechercher des enregistrements]

Ce module de recherche recherche les enregistrements d’un objet dans [!DNL Jira Software] qui correspondent à la requête de recherche que vous avez spécifiée.

Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Jira Software] à Workfront Fusion, voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de [!DNL Jira Software] à Workfront Fusion</a> dans cet article.</p> </td> 
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
