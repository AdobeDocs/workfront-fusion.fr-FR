---
title: Modules Jira
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent le logiciel Jira et les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: b74a3618-c4a1-4965-a88d-1643bfab12db
source-git-commit: 9865101fe57c2668ecb5ad743b3d6963833feb4a
workflow-type: tm+mt
source-wordcount: '1608'
ht-degree: 33%

---

# Modules Jira

>[!NOTE]
>
>Ces instructions s’appliquent à la nouvelle version du connecteur Jira, qui est simplement étiquetée Jira. Pour plus d’informations sur les connecteurs hérités de Jira Cloud et Jira Server, voir [Modules logiciels Jira](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-software-modules.md).

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent Jira et les connecter à plusieurs applications et services tiers.

Le connecteur Jira peut être utilisé pour Jira Cloud et le serveur de données Jira.

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

Pour utiliser les modules Jira, vous devez disposer d’un compte Jira.

## Connecter Jira à Workfront Fusion

### Créer les informations d’identification nécessaires

Pour créer des connexions à Jira, vous aurez besoin des éléments suivants :

| Type de connexion | Type de compte | Informations d’identification nécessaires |
|---|---|---|
| OAuth 2 | Tous | ID client et secret client |
| De base | Jira Cloud | Jeton API Jira |
| De base | Centre de données Jira | Jeton d’accès personnel Jira (PAT) |

Pour obtenir des instructions sur la création de l’un de ces éléments, consultez la documentation Jira.

Lors de la création de ces informations d’identification, vous aurez besoin des informations suivantes :

* Pour OAuth 2 :

  | Centre de données Fusion | URL de redirection |
  |---|---|
  | US | `https://app.workfrontfusion.com/oauth/cb/workfront-jira2` |
  | UE | `https://app-eu.workfrontfusion.com/oauth/cb/workfront-jira2` |
  | Azure | `https://app-az.workfrontfusion.com/oauth/cb/workfront-jira2` |



* Pour les jetons d’accès personnel (PAT) :

  | Centre de données Fusion | URL de redirection |
  |---|---|
  | US | `https://app.workfrontfusion.com/oauth/cb/workfront-jira` |
  | UE | `https://app-eu.workfrontfusion.com/oauth/cb/workfront-jira` |
  | Azure | `https://app-az.workfrontfusion.com/oauth/cb/workfront-jira` |

  >[!IMPORTANT]
  >
  >Pour utiliser un PAT, vous devez activer les éléments suivants dans le `jira/bin/WEB-INF/classes` Fichiers, dans le `jira-config.properties` de fichiers :
  >
  >* `jira.rest.auth.allow.basic = true`
  >* `jira.rest.csrf.disabled = true`
  >
  >Si ce fichier n’existe pas, vous devez le créer.

### Création d’une connexion à Jira dans Workfront Fusion

Pour créer la connexion dans Workfront Fusion :

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
      <td role="rowheader">ID client</td> 
      <td> <p>Si vous créez une connexion OAuth 2, saisissez votre identifiant client Jira</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Clé secrète client</td> 
      <td> <p>Si vous créez une connexion OAuth 2, saisissez votre secret client Jira</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">E-mail</td> 
      <td>Si vous créez une connexion de base à Jira Cloud, saisissez votre adresse e-mail.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Jeton API</td> 
      <td>Si vous créez une connexion de base à Jira Cloud, saisissez votre jeton API.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Jeton d’accès personnel</td> 
      <td>Si vous créez une connexion de base au centre de données Jira, saisissez votre jeton d’accès personnel.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Version de l’API</td> 
      <td>Sélectionnez la version de l’API Jira à laquelle vous souhaitez que cette connexion se connecte.</td> 
     </tr> 
    </tbody> 
   </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour créer la connexion et retourner au module.


## Modules Jira et leurs champs

Lorsque vous configurez des modules Jira, Workfront Fusion affiche les champs répertoriés ci-dessous. Selon des facteurs tels que votre niveau d’accès dans l’application ou le service, d’autres champs Jira peuvent s’afficher en plus de ceux-ci. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

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
   <td> <p>Sélectionnez le webhook que vous souhaitez utiliser pour surveiller les enregistrements ou créez un webhook. </p> <p>Pour créer un webhook :</p> 
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
   td&gt; <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
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
   <td role="rowheader">Type d'enregistrement</td> 
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
