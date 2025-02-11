---
title: Appeler l’API REST MS Graph
description: Appeler l’API REST MS Graph via le HTTP Adobe Workfront Fusion et effectuer une requête OAuth 2.0
author: Becky
feature: Workfront Fusion
exl-id: f411c807-955d-44fe-98b1-3ebba3fe0861
source-git-commit: a7ee3e751b75523c4da62cea71e59a63f98b95e0
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 21%

---

# Appeler l’API REST MS Graph

De nombreux services web Microsoft sont accessibles via l’API Microsoft Graph. Vous pouvez créer une connexion à l’API Microsoft Graph à l’aide du module de requête HTTP > Créer une requête OAuth 2.0 de Workfront Fusion .

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront 
   <td> <p>Tous</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licence Adobe Workfront</td> 
   <td> <p>Nouveau : Standard</p><p>Ou</p><p>Actuellement : Travail ou licence supérieure</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licence Adobe Workfront Fusion **</td> 
   <td>
   <p>Actuel : aucune exigence de licence Workfront Fusion.</p>
   <p>Ou</p>
   <p>Héritée : n’importe laquelle. </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Nouveau :</p> <ul><li>Sélectionnez ou Prime Workfront Plan : votre entreprise doit acheter Adobe Workfront Fusion.</li><li>Plan Ultimate Workfront : Workfront Fusion est inclus.</li></ul>
   <p>Ou</p>
   <p>Actuel : votre entreprise doit acheter Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Enregistrement de Workfront Fusion dans le portail d’enregistrement d’applications Microsoft

Pour créer une connexion à l’API REST Microsoft Graph, vous devez d’abord enregistrer Adobe Workfront Fusion.

1. Commencez l’enregistrement d’une nouvelle application comme décrit dans la section [Enregistrement d’une application avec la plateforme d’identités Microsoft](https://learn.microsoft.com/en-us/graph/auth-register-app-v2) dans la documentation de Microsoft.

   Dans le cadre de l’enregistrement, Microsoft nécessite les informations suivantes :

   <table style="table-layout:auto">
      <tr>
        <td>Nom de l’application</td>
        <td>Saisissez un nom pour l’application, par exemple « Mon application Workfront Fusion ».</td>
      </tr>
      <tr>
        <td>URL de redirection</td>
        <td><code>https://app.workfrontfusion.com/oauth/cb/oauth2</code></td>
      </tr>
    </table>

1. Une fois l’enregistrement de l’application terminé, notez l’ID de l’application.

   >[!IMPORTANT]
   >
   >Vous aurez besoin de l’ID d’application pour configurer votre connexion dans Workfront Fusion.

1. Générez un secret client. Prenez note de cette clé secrète.

   Pour obtenir des instructions, consultez [Enregistrement d’une application auprès de la plateforme d’identités Microsoft](https://learn.microsoft.com/en-us/graph/auth-register-app-v2) dans la documentation de Microsoft.

   >[!IMPORTANT]
   >
   >Vous aurez besoin du secret client pour configurer votre connexion dans Workfront Fusion.

1. Configurez les autorisations de votre application.

   Pour plus d’informations sur l’emplacement et la configuration de ces champs, consultez la section « Configurer des autorisations pour le graphique Microsoft » dans [Obtenir l’accès sans utilisateur](https://docs.microsoft.com/en-us/graph/auth-v2-service) dans la documentation de Microsoft.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">De quel type d’autorisations votre application a-t-elle besoin ?</td> 
      <td>Sélectionnez <code>Delegated permissions</code>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Sélectionner des autorisations</td> 
      <td> <p>Sélectionnez les autorisations suivantes :</p> 
       <ul> 
        <li> <p><code>offline_access</code> </p> </li> 
        <li> <p><code>openid</code> </p> </li> 
        <li> <p>Toutes les autres autorisations requises par vos intégrations (par exemple : <code>User.Read</code>).</p> </li> 
       </ul> <p><b>Important</b> : vous aurez besoin des autorisations sélectionnées pour configurer votre connexion dans Workfront Fusion.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Passez à [Configurer la connexion de l’API MS Graph dans Workfront Fusion](#configure-your-ms-graph-api-connection-in-workfront-fusion).

## Configurer la connexion de l’API MS Graph dans Workfront Fusion

Après avoir enregistré Workfront Fusion, comme indiqué dans la section [Enregistrer Workfront Fusion sur le portail d’enregistrement d’applications Microsoft](#register-workfront-fusion-in-the-microsoft-application-registration-portal), vous pouvez configurer votre connexion dans le module HTTP > Créer une requête Oauth 2.0.

1. Ajoutez un module HTTP > Créer un appel OAuth 2.0 à votre scénario.
1. Cliquez sur **Ajouter** en regard du champ de connexion.
1. Configurez les champs de connexion comme suit :

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">Nom de la connexion</td> 
      <td>Saisissez un nom pour la connexion.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p role="rowheader">Environnement</p> </td> 
      <td>Choisissez si vous vous connectez à un compte de production ou hors production. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p role="rowheader">Type</p> </td> 
      <td>Indiquez si vous vous connectez à un compte de service ou à un compte personnel. </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p role="rowheader">Type de flux</p> </td> 
      <td>Sélectionnez <code>Authorization Code</code>. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Autoriser URI</td> 
      <td>Saisissez <code>https://login.microsoftonline.com/common/oauth2/v2.0/authorize</code>. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">URI du jeton</td> 
      <td>Saisissez <code>https://login.microsoftonline.com/common/oauth2/v2.0/token</code>. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Étendue</td> 
      <td> <p>Saisissez les autorisations que vous avez sélectionnées lors de l’enregistrement, comme expliqué dans la section <a href="#register-workfront-fusion-in-the-microsoft-application-registration-portal" class="MCXref xref">Enregistrement de Workfront Fusion sur le portail d’enregistrement d’applications Microsoft</a>.</p> <p>Pour chaque portée, cliquez sur <b>Ajouter</b> et saisissez l’autorisation.</p> <p>Exemple : <code>offline_access</code>.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Séparateur d’étendue</td> 
      <td>Sélectionnez <code>SPACE</code>. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">ID client</td> 
      <td>Saisissez l’ID d’application à l’étape 2 dans <a href="#register-workfront-fusion-in-the-microsoft-application-registration-portal" class="MCXref xref">Enregistrer Workfront Fusion sur le portail d’enregistrement d’applications Microsoft</a>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Clé secrète client</td> 
      <td>Saisissez le secret client que vous avez généré à l’étape 3 dans <a href="#register-workfront-fusion-in-the-microsoft-application-registration-portal" class="MCXref xref">Enregistrement de Workfront Fusion sur le portail d’enregistrement d’applications Microsoft</a>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Autoriser les paramètres</td> 
      <td> <p>Ajoutez les paramètres Autoriser suivants. Pour chaque paramètre que vous ajoutez, cliquez sur <b>Ajouter un élément</b> et saisissez les informations suivantes : </p> 
       <ul> 
        <li> <p>Clé :<code> response_mode</code> Valeur : <code>query</code></p> </li> 
        <li> <p>Clé : <code>prompt </code>Valeur : <code>consent</code></p> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Paramètres du jeton d’accès</td> 
      <td>Vous n’avez rien à saisir dans ce champ.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Paramètres du jeton d’actualisation</td> 
      <td> 
       <ol> 
        <li value="1"> <p>Cliquez sur <b> Ajouter un élément </b>.</p> </li> 
        <li value="2"> <p>Dans le champ <b>Clé</b>, saisissez <code>scope</code>.</p> </li> 
        <li value="3"> <p>Dans le champ <b>Valeur</b>, saisissez toutes les portées que vous avez saisies dans le champ de portée, séparées par des espaces.</p> <p>Exemple : <code>offline_access openid User.Read</code></p> </li> 
       </ol> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">En-têtes personnalisés</td> 
      <td>Vous n’avez rien à saisir dans ce champ.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Placement du jeton</td> 
      <td><code>In the header</code> </td> 
     </tr> 
    </tbody> 
   </table>

1. Cliquez sur **Continuer**.
1. Dans la fenêtre qui s’affiche, cliquez sur **Accepter** pour terminer la connexion et revenir au module.
