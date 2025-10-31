---
title: Connecter Adobe Workfront Fusion à Google Services à l’aide d’un client OAuth personnalisé
description: Vous pouvez utiliser Adobe Workfront Fusion pour vous connecter aux services Google à l’aide d’un client OAuth personnalisé. Cette procédure nécessite un compte Google existant.
author: Becky
feature: Workfront Fusion
exl-id: 2f0bc289-4ecf-4a31-9d7b-641bbca6fc95
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '976'
ht-degree: 30%

---

# Connecter Adobe Workfront Fusion à Google Services à l’aide d’un client OAuth personnalisé

Vous pouvez utiliser Adobe Workfront Fusion pour vous connecter aux services Google à l’aide d’un client OAuth personnalisé. Cette procédure nécessite un compte Google existant.

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

Vous avez besoin d’un compte Google existant pour établir cette connexion.

## Connecter Fusion aux services Google à l’aide d’un client OAuth personnalisé

Pour établir cette connexion, vous devez créer et configurer un projet sur la plateforme Google Cloud, puis configurer la connexion dans Fusion en fonction de ce projet.

>[!NOTE]
>
>Cette procédure est destinée à :
>
>* un usage personnel (utilisateurs ou utilisatrices `@gmail.com` et `@googlemail.com`) ;
>* Utilisation interne (utilisateurs de Google Workspace qui préfèrent utiliser un client OAuth personnalisé)

* [Création d’un projet sur Google Cloud Platform](#create-a-project-on-google-cloud-platform)
* [Configurer les paramètres de consentement OAuth](#configure-oauth-consent-settings)
* [Créer des informations d’identification OAuth](#create-oauth-credentials)
* [Connexion à Google dans Workfront Fusion](#connect-to-google-in-workfront-fusion)

### Création d’un projet sur Google Cloud Platform

Pour créer un projet sur Google Cloud Platform, procédez comme suit :

1. Commencez à créer un projet sur Google Cloud Platform.

   Pour obtenir des instructions détaillées, consultez [Création d’un projet Google Cloud](https://developers.google.com/workspace/guides/create-project) dans la documentation de Google.
1. Lors de l’activation des API , vous devez activer l’API Google Drive ainsi que l’API de toutes les applications Google que vous souhaitez utiliser (telles que l’API Google Sheets).
1. Terminez la création du projet.
1. Passez à la section [Configurer les paramètres de consentement OAuth](#configure-oauth-consent-settings) dans cet article.

### Configurer les paramètres de consentement OAuth

1. Commencer à configurer OAuth pour votre projet

   Pour obtenir des instructions détaillées, consultez [Configuration de l’écran de consentement OAuth et choix des portées](https://developers.google.com/workspace/guides/configure-oauth-consent) dans la documentation de Google.
1. Sélectionnez **Externe**, puis cliquez sur **Créer**.

   >[!NOTE]
   >
   >Cette option ne vous sera pas facturée. Pour plus d’informations, voir Informations de Google sur les exceptions aux exigences de vérification.

1. Remplissez les champs obligatoires comme suit :

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>Nom de l’application</p> </td> 
      <td> <p>Saisissez le nom de l’application qui demande un consentement.</p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Exemple : </b></span></span>Adobe Workfront Fusion </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">E-mail d’assistance aux utilisateurs</td> 
      <td>Saisissez une adresse e-mail pour que les utilisateurs et utilisatrices puissent vous contacter en cas de questions sur le consentement au moment de se connecter à cette application.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Adresses e-mail</td> 
      <td>Saisissez une ou plusieurs adresses e-mail que Google peut utiliser pour vous informer de toute modification apportée à votre projet.</td> 
     </tr> 
    </tbody> 
   </table>

1. Sous Domaines autorisés, cliquez sur **Ajouter un domaine**, puis saisissez `workfrontfusion.com`.
1. Ajoutez les portées suivantes :

   <table style="table-layout:auto">
    <col> 
    <col> 
    <thead> 
     <tr> 
      <th>Service/API</th> 
      <th>Portées requises</th> 
     </tr> 
    </thead> 
    <tbody> 
     <tr> 
      <td> <p>Gmail</p> </td> 
      <td> <p>https://mail.google.com/</p> <p>https://www.googleapis.com/auth/gmail.labels</p> <p>https://www.googleapis.com/auth/gmail.send</p> <p>https://www.googleapis.com/auth/gmail.readonly</p> <p>https://www.googleapis.com/auth/gmail.compose</p> <p>https://www.googleapis.com/auth/gmail.insert</p> <p>https://www.googleapis.com/auth/gmail.modify</p> <p>https://www.googleapis.com/auth/gmail.metadata</p> </td> 
     </tr> 
     <tr> 
      <td> <p>Google Drive</p> </td> 
      <td> <p>https://www.googleapis.com/auth/drive</p> <p>https://www.googleapis.com/auth/drive.readonly</p> </td> 
     </tr> 
    </tbody> 
   </table>

   Il se peut que vous deviez développer la liste ou passer à la page suivante de la liste pour les voir toutes.

1. (Facultatif) Ajoutez des utilisateurs et utilisatrices de test au projet.
1. Vérifiez l’exactitude de vos informations, puis cliquez sur **Retour au tableau de bord**.

   >[!NOTE]
   >
   >Vous n’avez pas besoin d’envoyer votre écran de consentement et votre demande pour vérification par Google.

1. Passez à [Créer des informations d’identification OAuth](#create-oauth-credentials).

### Créer des informations d’identification OAuth

1. Commencez à créer les informations d’identification d’identifiant client OAuth.

   Pour obtenir des instructions, voir [Création d’informations d’identification d’accès](https://developers.google.com/workspace/guides/create-credentials) dans la documentation de Google.

   >[!NOTE]
   >
   >S’il ne s’agit pas de la première API ou service (Gmail ou Google Drive) que vous avez activé, il n’est pas nécessaire de créer de nouvelles informations d’identification.

1. Remplissez les champs obligatoires comme suit :

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">Type d’application</td> 
      <td> <p> Application web</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Nom</td> 
      <td>Workfront Fusion </td> 
     </tr> 
    </tbody> 
   </table>

1. Sous URI de redirection autorisés, saisissez **l’une** des informations suivantes :

   * Pour Gmail ou Google Drive : `https://app.workfrontfusion.com/oauth/cb/google-restricted`

   * Pour les autres applications Google : `https://app.workfrontfusion.com/oauth/cb/google`

1. Cliquez sur **Créer**.

   L’identifiant client et le secret client s’affichent.

1. Copiez l’ID client et le secret client à un emplacement sécurisé. Vous les utiliserez pour établir une connexion dans Workfront Fusion.
1. Passez à [Connexion à Google dans Workfront Fusion](#connect-to-google-in-workfront-fusion).

### Connexion à Google dans Workfront Fusion

Le processus de création d’une connexion à Google diffère selon que vous utilisez un module d’un service Google (tel que Google Sheets ou Google Docs) ou que vous vous connectez à Google via le module HTTP > Créer une requête OAuth2.0 .

* [Connexion à Google dans un service Google](#connect-to-google-in-a-google-service)
* [Connexion à Google dans le module HTTP > Créer une requête OAuth2.0](#connect-to-google-in-the-http--make-an-oauth20-request-module)

#### Connexion à Google dans un service Google

1. Dans Workfront Fusion, recherchez le module Google pour lequel vous devez créer une connexion.
1. Cliquez sur **Créer une connexion**, puis cliquez sur **Afficher les paramètres avancés**.
1. Renseignez les champs Nom de la connexion, Environnement et Type selon vos besoins.
1. Saisissez l’ID client et le secret client que vous avez récupérés dans [Créer des informations d’identification OAuth](#create-oauth-credentials) dans les champs respectifs, puis cliquez sur **Continuer**.

1. Connectez-vous avec votre compte Google.

   La fenêtre **Cette application n’est pas vérifiée** s’affiche. Notez que l’« application » mentionnée dans le titre de la fenêtre est le client OAuth que vous avez créé ci-dessus.

1. Cliquez sur **Avancé**, puis sur **Accéder à Workfront Fusion (non sécurisé)** pour autoriser l’accès à l’aide de votre client OAuth personnalisé.

1. Cliquez sur **Autoriser** pour accorder l’autorisation Workfront Fusion.
1. Dans la fenêtre qui s’affiche, cliquez à nouveau sur **Autoriser** pour confirmer vos choix.

   La connexion au service Google souhaité à l’aide d’un client OAuth personnalisé est établie.

#### Connexion à Google dans le module HTTP > Créer une requête OAuth2.0 {#connect-to-google-in-the-http--make-an-oauth20-request-module}

Pour obtenir des instructions sur la connexion à Google dans le module HTTP > Créer une requête OAuth 2.0 , voir [Instructions pour créer une connexion à Google dans le module HTTP > Créer un module de requête OAuth 2.0](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-oauth-2-request.md#instructions-for-creating-a-connection-to-google-in-the-http-make-an-oauth-20-request-module) dans l’article HTTP > Créer un module de requête OAuth 2.0 .

## Message d’erreur possible : [403 Accès non configuré]

Si le message d’erreur `403 Access Not Configured` s’affiche, vous devez activer l’API correspondante dans votre plateforme cloud Google. Pour activer l’API, suivez les étapes de la section [Création d’un projet sur Google Cloud Platform](#create-a-project-on-google-cloud-platform) de cet article.
