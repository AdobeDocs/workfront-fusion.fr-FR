---
title: Modules Jira
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent le logiciel Jira et les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: b74a3618-c4a1-4965-a88d-1643bfab12db
source-git-commit: 017341e045a703f5d6e933a6df860f4fc8c0649d
workflow-type: tm+mt
source-wordcount: '2348'
ht-degree: 36%

---

# Modules Jira

>[!NOTE]
>
>Ces instructions s’appliquent à la nouvelle version du connecteur Jira, qui est simplement étiquetée Jira. Pour plus d’informations sur les connecteurs hérités de Jira Cloud et Jira Server, voir [Modules logiciels Jira](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-software-modules.md).

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent Jira et les connecter à plusieurs applications et services tiers.

Le connecteur Jira peut être utilisé pour Jira Cloud et le serveur de données Jira.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tout package de workflow Adobe Workfront et tout package d’automatisation et d’intégration Adobe Workfront</p><p>Workfront Ultimate</p><p>Packages Workfront Prime et Select, avec l’achat supplémentaire de Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licences Adobe Workfront</td> 
   <td> <p>Standard</p><p>Travail ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licence Adobe Workfront Fusion</td> 
   <td>
   <p>Basé sur les opérations : aucune exigence de licence Workfront Fusion</p>
   <p>Basé sur un connecteur (hérité) : Workfront Fusion pour l’automatisation et l’intégration du travail </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Si votre organisation dispose d’un package Workfront Select ou Prime qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acquérir Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences Adobe Workfront Fusion, consultez [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Conditions préalables

* Pour utiliser les modules Jira, vous devez disposer d’un compte Jira.
* Vous devez avoir accès au Developer Console Jira pour créer une application OAuth2 dans Jira.

## Connecter Jira à Workfront Fusion

La procédure de création d’une connexion à Jira diffère selon que vous créez une connexion de base ou une connexion OAuth2.

* [Créer une connexion OAuth2 à Jira](#create-an-oauth2-connection-to-jira)
* [Créer une connexion de base à Jira](#create-a-basic-connection-to-jira)

### Créer une connexion OAuth2 à Jira

Pour créer une connexion OAuth2 à Jira, vous devez créer une application dans Jira avant de pouvoir configurer la connexion dans Fusion.

* [Créer une application OAuth2 dans Jira](#create-an-oauth2-application-in-jira)
* [Configuration de la connexion OAutt2 dans Fusion](#configure-the-oauth2-connection-in-fusion)

#### Créer une application OAuth2 dans Jira

>[!IMPORTANT]
>
>Vous devez avoir accès au Developer Console Jira pour créer et configurer une application OAuth2 pour votre connexion Jira.

1. Accédez au [Jira Developer Console](https://developer.atlassian.com/console.myapps/).
1. Dans la zone Mes applications , cliquez sur **Créer**, puis sélectionnez **Intégration OAuth 2.0**.
1. Saisissez le nom de l’intégration, acceptez les conditions générales du développeur, puis cliquez sur **Créer**.

   L’application est créée et vous accédez à la zone de configuration de l’application.
1. Cliquez sur **Autorisations** dans le panneau de navigation de gauche.
1. Dans la zone Autorisations , recherchez la ligne **API Jira**.
1. Cliquez sur **Ajouter** sur la ligne API Jira, puis sur **Continuer** sur la même ligne.
1. Activez les portées suivantes :

   * Afficher les données de problème Jira (`read:jira-work`)
   * Affichage des profils utilisateur (`read:jira-user`)
   * Créer et gérer des événements (`write:jira-work`)

1. Dans le volet de navigation de gauche, cliquez sur **Autorisation**.
1. Cliquez sur **Ajouter** dans la ligne pour l’autorisation OAuth 2.0.
1. Dans le champ **URL de rappel**, saisissez l’une des URL suivantes, en fonction de votre centre de données Workfront Fusion :

   | Centre de données Fusion | URL de rappel |
   |---|---|
   | US | `https://app.workfrontfusion.com/oauth/cb/workfront-jira2` |
   | UE | `https://app-eu.workfrontfusion.com/oauth/cb/workfront-jira2` |
   | Azure | `https://app-az.workfrontfusion.com/oauth/cb/workfront-jira2` |

1. Dans le volet de navigation de gauche, cliquez sur **Paramètres**.
1. (Facultatif) Saisissez une description dans le champ Description, puis cliquez sur **Enregistrer les modifications** sous ce champ.
1. Copiez l’ID client et le secret client de la zone Paramètres vers un emplacement sécurisé, ou laissez cette page ouverte lorsque vous configurez la connexion dans Fusion.
1. Passez à [Configuration de la connexion OAutt2 dans Fusion](#configure-the-oauth2-connection-in-fusion)

#### Configuration de la connexion OAuth2 dans Fusion

1. Dans n’importe quel module Jira, cliquez sur **Ajouter** en regard du champ Connexion .
1. Configurez les champs suivants :

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>Type de connexion</p> </td> 
      <td> <p>Sélectionnez <b>OAuth 2</b>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Nom de la connexion</p> </td> 
      <td> <p>Saisissez un nom pour la nouvelle connexion.</p> </td> 
     </tr> 
     <tr>
      <td role="rowheader">URL du service</td>
      <td>Saisissez l’URL de votre instance Jira. Il s’agit de l’URL d’accès à Jira.</td>
     </tr>
     <tr>
      <td role="rowheader">Type de compte Jira</td>
       <td>Indiquez si vous vous connectez à Jira Cloud ou à Jira Data Center.</td>
     </tr>
     <tr> 
      <td role="rowheader">ID client</td> 
      <td> <p>Saisissez l’ID client de l’application Jira que vous avez créée dans <a href="#create-an-oauth2-application-in-jira" class="MCXref xref" data-mc-variable-override="">Créer une application OAuth2 dans Jira</a>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Clé secrète client</td> 
      <td> <p>Saisissez le secret client de l’application Jira que vous avez créée dans <a href="#create-an-oauth2-application-in-jira" class="MCXref xref" data-mc-variable-override="">Créer une application OAuth2 dans Jira</a>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Portées supplémentaires</td> 
      <td>Saisissez toutes les portées supplémentaires que vous souhaitez ajouter à cette connexion.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Version de l’API</td> 
      <td>Sélectionnez la version de l’API Jira à laquelle vous souhaitez que cette connexion se connecte.</td> 
     </tr> 
    </tbody> 
   </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour créer la connexion et retourner au module.

### Créer une connexion de base à Jira

La création d’une connexion de base à Jira diffère selon que vous créez une connexion à Jira Cloud ou à Jira Data Center.

* [Créer une connexion de base à Jira Cloud](#create-a-basic-connection-to-jira-cloud)
* [Créer une connexion de base au centre de données Jira](#create-a-basic-connection-to-jira-data-center)

#### Créer une connexion de base à Jira Cloud

>[!IMPORTANT]
>
> Pour créer une connexion de base à Jira Cloud, vous devez disposer d’un jeton API Jira.
>Pour obtenir des instructions sur l’acquisition d’un jeton API Jira, voir [Gérer les jetons API pour votre compte Atlassian](https://support.atlassian.com/atlassian-account/docs/manage-api-tokens-for-your-atlassian-account) dans la documentation d’Atlassian.


1. Dans n’importe quel module Jira, cliquez sur **Ajouter** en regard du champ Connexion .
1. Configurez les champs suivants :

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>Type de connexion</p> </td> 
      <td> <p>Choisissez si vous créez une connexion de base ou une connexion OAuth 2.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Nom de la connexion</p> </td> 
      <td> <p>Saisissez un nom pour la nouvelle connexion.</p> </td> 
     </tr> 
     <tr>
      <td role="rowheader">URL du service</td>
      <td>Saisissez l’URL de votre instance Jira. Il s’agit de l’URL d’accès à Jira.</td>
     </tr>
     <tr>
      <td role="rowheader">Type de compte Jira</td>
       <td>Indiquez si vous vous connectez à Jira Cloud ou à Jira Data Center.</td>
     </tr>
     <tr> 
      <td role="rowheader">E-mail</td> 
      <td>Saisissez votre adresse e-mail.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Jeton API</td> 
      <td>Saisissez votre jeton API.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Version de l’API</td> 
      <td>Sélectionnez la version de l’API Jira à laquelle vous souhaitez que cette connexion se connecte.</td> 
     </tr> 
    </tbody> 
   </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour créer la connexion et retourner au module.

#### Créer une connexion de base au centre de données Jira

>[!IMPORTANT]
>
> Pour créer une connexion de base au centre de données Jira, vous devez disposer d’un jeton d’accès personnel (PAT) Jira.
>Pour obtenir des instructions sur l’acquisition d’un jeton d’accès personnel Jira, voir [Gérer les jetons API pour votre compte Atlassian](https://confluence.atlassian.com/enterprise/using-personal-access-tokens-1026032365.html) dans la documentation d’Atlassian.
>Pour plus d’informations sur la création du PAT, voir [Configuration de votre PAT](#configure-your-pat) dans cet article.

1. Dans n’importe quel module Jira, cliquez sur **Ajouter** en regard du champ Connexion .
1. Configurez les champs suivants :

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>Type de connexion</p> </td> 
      <td> <p>Choisissez si vous créez une connexion de base ou une connexion OAuth 2.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Nom de la connexion</p> </td> 
      <td> <p>Saisissez un nom pour la nouvelle connexion.</p> </td> 
     </tr> 
     <tr>
      <td role="rowheader">URL du service</td>
      <td>Saisissez l’URL de votre instance Jira. Il s’agit de l’URL d’accès à Jira.</td>
     </tr>
     <tr>
      <td role="rowheader">Type de compte Jira</td>
       <td>Indiquez si vous vous connectez à Jira Cloud ou à Jira Data Center.</td>
     </tr>
     <tr> 
      <td role="rowheader">PAT (Personal access token)</td> 
      <td>Saisissez votre jeton d’accès personnel Jira.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Version de l’API</td> 
      <td>Sélectionnez la version de l’API Jira à laquelle vous souhaitez que cette connexion se connecte.</td> 
     </tr> 
    </tbody> 
   </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour créer la connexion et retourner au module.

##### Configurer votre chemin d’accès

Pour créer une connexion de base au centre de données Jira, vous devez disposer d’un jeton d’accès personnel (PAT) Jira.

Pour obtenir des instructions sur l’acquisition d’un jeton d’accès personnel Jira, voir [Gérer les jetons API pour votre compte Atlassian](https://confluence.atlassian.com/enterprise/using-personal-access-tokens-1026032365.html) dans la documentation d’Atlassian.

Vous aurez peut-être besoin des informations suivantes lors de la configuration de votre PAT

* URL de redirection

  | Centre de données Fusion | URL de redirection |
  |---|---|
  | US | `https://app.workfrontfusion.com/oauth/cb/workfront-jira` |
  | UE | `https://app-eu.workfrontfusion.com/oauth/cb/workfront-jira` |
  | Azure | `https://app-az.workfrontfusion.com/oauth/cb/workfront-jira` |

* Configurations de fichier

Pour utiliser un PAT, vous devez activer les éléments suivants dans le `jira/bin/WEB-INF/classes` Fichiers, dans le `jira-config.properties` de fichiers :

* `jira.rest.auth.allow.basic = true`
* `jira.rest.csrf.disabled = true`

Si ce fichier n’existe pas, vous devez le créer.

## Modules Jira et leurs champs

Lorsque vous configurez des modules Jira, Workfront Fusion affiche les champs répertoriés ci-dessous. Selon des facteurs tels que votre niveau d’accès dans l’application ou le service, d’autres champs Jira peuvent s’afficher en plus de ceux-ci. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, consultez [Mappage d’informations d’un module à l’autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Bouton (bascule) de mappage](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Déclencheurs](#triggers)
* [Actions](#actions)
* [Recherches](#searches)

### Déclencheurs

#### Rechercher des enregistrements

Ce module déclencheur lance un scénario lorsqu’un enregistrement est ajouté, mis à jour ou supprimé.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Webhook</td> 
   <td> <p>Sélectionnez le webhook que vous souhaitez utiliser pour surveiller les enregistrements ou créez un webhook. </p> <p>Pour créer un webhook :</p> 
    <ol> 
     <li>Cliquez sur <strong> Ajouter </strong></li> 
     <li>Saisissez un nom pour le webhook.</li> 
     <li> Sélectionnez la connexion que vous souhaitez utiliser pour votre webhook. <p>Pour plus d’informations sur la connexion de votre compte Jira à Workfront Fusion, voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Jira à Workfront Fusion</a> dans cet article.</p> </li> 
     <li> <p>Sélectionnez le type d’enregistrement que vous souhaitez que le logiciel surveille :</p> 
      <ul> 
       <li>Problème</li> 
       <li>Commentaire </li> 
       <li>Journal de travail </li> 
       <li>Projet </li> 
       <li>Sprint</li> 
       <li>Pièce jointe </li> 
      </ul> </li> 
     <li>Sélectionnez un ou plusieurs types d’événements qui déclencheront ce scénario.</li> 
     <li>Saisissez un filtre Jira Query Language pour ce module.<p>Pour plus d’informations sur JQL, consultez l’article <a href="https://www.atlassian.com/blog/jira-software/jql-the-most-flexible-way-to-search-jira-14#:~:text=JQLstandsforJiraQuery,projectmanagers%2Candbusinessusers.">JQL</a> sur le site d’aide d’Atlassian. </p></li>
     <li>Cliquez sur <b>Enregistrer</b> pour enregistrer le webhook. 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [Ajouter un problème au sprint](#add-issue-to-sprint)
* [Créer un enregistrement](#create-a-record)
* [Appel API personnalisé](#custom-api-call)
* [Supprimer un enregistrement](#delete-a-record)
* [Télécharger une pièce jointe](#download-an-attachment)
* [Lire un enregistrement](#read-a-record)
* [Mettre à jour un enregistrement](#update-a-record)

#### Ajouter un problème au sprint

Ce module d’action ajoute un ou plusieurs problèmes à un sprint.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Jira à Workfront Fusion, voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Jira à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de sprint</td> 
   <td>Saisissez ou mappez l’ID du sprint auquel vous souhaitez ajouter un problème.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID ou clés de l'événement</td> 
   <td>Pour chaque événement ou clé à ajouter au sprint, cliquez sur <b>Ajouter un élément</b> et saisissez l’ID d’événement ou la clé. Vous pouvez saisir jusqu’à 50 dans un seul module.</td> 
  </tr> 
 </tbody> 
</table>

#### Créer un enregistrement

Ce module d’action crée un nouvel enregistrement dans Jira.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Jira à Workfront Fusion, voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Jira à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type d’enregistrement</td> 
   <td> <p>Sélectionnez le type d’enregistrement que vous souhaitez que le module crée.</p> 
    <ul> 
     <li>Pièce jointe</li> 
     <li>Commentaire</li> 
     <li>Problème</li> 
     <li>Projet</li> 
     <li>Sprint </li> 
     <li>Journal de travail</li> 
     <li>l’utilisateur ou de l’utilisatrice</li> 
     <li>Panorama</li> 
     <li>Catégorie</li> 
     <li>Filtre</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Autres champs</td> 
   <td> Renseignez les autres champs. Les champs sont disponibles en fonction du type d’enregistrement sélectionné. </td> 
  </tr> 
 </tbody> 
</table>

#### Appel API personnalisé

Ce module d’action vous permet d’effectuer un appel authentifié personnalisé vers l’API Jira.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Jira à Workfront Fusion, voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Jira à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Saisir un chemin relatif à<code>&lt;Instance URL>/rest/api/2/ </code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Méthode</td> 
   td&gt; <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, consultez <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">En-têtes</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p> Workfront Fusion ajoute les en-têtes d’autorisation pour vous.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Chaîne de requête</td> 
   <td> <p>Ajoutez la requête pour l’appel API sous la forme d’un objet JSON standard.</p> <p>Par exemple : <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Corps</td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre JSON, placez les guillemets à l’extérieur de l’instruction conditionnelle.</p> 
     <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png">  </td> 
  </tr> 
 </tbody> 
</table>

#### Supprimer un enregistrement

Ce module d&#39;action supprime l&#39;enregistrement spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Jira à Workfront Fusion, voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Jira à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type d’enregistrement</td> 
   <td> <p>Sélectionnez le type d’enregistrement que vous souhaitez que le module supprime. </p> 
    <ul> 
     <li>Commentaire</li> 
     <li>Problème</li> 
     <li>Projet</li> 
     <li>Sprint </li> 
     <li>Journal de travail</li> 
     <li>Pièce jointe</li> 
     <li>Panorama</li> 
     <li>Catégorie</li> 
     <li>Filtre</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">(Type d’enregistrement)ID</td> 
   <td>Saisissez ou mappez l’identifiant ou la clé de l’enregistrement à supprimer.</td> 
  </tr> 
 </tbody> 
</table>

#### Télécharger une pièce jointe

Ce module d’action télécharge la pièce jointe spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Jira à Workfront Fusion, voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Jira à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID</td> 
   <td>Saisissez ou mappez l’ID de la pièce jointe que vous souhaitez télécharger.</td> 
  </tr> 
 </tbody> 
</table>

#### Lire un enregistrement

Ce module d’action lit les données de l’enregistrement spécifié dans Jira.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Jira à Workfront Fusion, voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Jira à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type d’enregistrement</td> 
   <td> <p>Sélectionnez le type d’enregistrement Jira que le module doit lire.</p> 
    <ul> 
     <li>Pièce jointe</li> 
     <li>Commentaire</li> 
     <li>Problème</li> 
     <li>Projet</li> 
     <li>Sprint </li> 
     <li>Journal de travail</li> 
     <li>l’utilisateur ou de l’utilisatrice</li> 
     <li>Panorama</li> 
     <li>Catégorie</li> 
     <li>Filtre</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sorties</td> 
   <td>Sélectionnez les sorties que vous souhaitez recevoir. Les options de sortie sont disponibles en fonction du type d’enregistrement sélectionné dans le champ « Type d’enregistrement ».</td> 
  </tr> 
  <tr> 
   <td role="rowheader">(Type d’enregistrement) ID</td> 
   <td> <p>Saisissez ou mappez l’ID Jira unique de l’enregistrement que le module doit lire.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Mettre à jour un enregistrement

Ce module d&#39;action met à jour un enregistrement existant, tel qu&#39;un événement ou un projet.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Jira à Workfront Fusion, voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Jira à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type d’enregistrement</td> 
   <td> <p>Sélectionnez le type d’enregistrement que vous souhaitez que le module mette à jour. Lorsque vous sélectionnez un type d’enregistrement, d’autres champs spécifiques à ce type d’enregistrement apparaissent dans le module.</p> 
    <ul> 
     <li>Commentaire</li> 
     <li>Problème</li> 
     <li>Projet</li> 
     <li>Sprint </li> 
     <li>Problème de transition</li> 
     <li>Catégorie </li> 
     <li>Filtre </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID ou clé</td> 
   <td>Saisissez ou mappez l’identifiant ou la clé de l’enregistrement que vous souhaitez mettre à jour.</td> 
  <tr> 
   <td role="rowheader">Autres champs</td> 
   <td> Renseignez les autres champs. Les champs sont disponibles en fonction du type d’enregistrement sélectionné. </td> 
  </tr> 
 </tbody> 
</table>

### Recherches

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

#### Rechercher des enregistrements

Ce module de recherche recherche les enregistrements d’un objet dans Jira qui correspondent à la requête que vous spécifiez.

Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Jira à Workfront Fusion, voir <a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connexion de Jira à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type d’enregistrement</td> 
   <td> <p>Sélectionnez le type d’enregistrement que vous souhaitez que le module recherche. Lorsque vous sélectionnez un type d’enregistrement, d’autres champs spécifiques à ce type d’enregistrement apparaissent dans le module.</p> 
    <ul> 
     <li>Problème</li> 
     <li>Projet</li> 
     <li>l’utilisateur ou de l’utilisatrice</li> 
     <li>Sprint</li> 
     <li>Panorama</li> 
     <li>Journal de travail</li> 
     <li>Commentaire</li> 
     <li>Problème de transition</li> 
     <li>Catégorie</li> 
    </ul> </td> 
  <tr> 
   <td role="rowheader"> <p>Nbre max. de résultats</p> </td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que vous souhaitez que le module récupère au cours de chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
   <tr> 
    <td role="rowheader">Offset</td> 
    <td> Saisissez ou mappez l’ID du premier élément pour lequel vous souhaitez récupérer des détails. Il s’agit d’une méthode de pagination des enregistrements. Si vous saisissez le 5000e élément comme décalage, le module renvoie les éléments 5000-9999.</td> 
   </tr>
  <tr> 
   <td role="rowheader">Autres champs</td> 
   <td> Renseignez les autres champs. Les champs sont disponibles en fonction du type d’enregistrement sélectionné. </td> 
  </tr> 
 </tbody> 
</table>
