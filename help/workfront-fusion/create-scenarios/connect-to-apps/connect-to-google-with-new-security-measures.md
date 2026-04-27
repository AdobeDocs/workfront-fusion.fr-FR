---
title: Connecter Adobe Workfront Fusion à Google Services avec des mesures de sécurité mises à jour
description: Google has introduced restrictions on how users can use their API. This article describes how to connect Adobe Workfront Fusion to Google, accounting for these update security measures.
author: Becky
feature: Workfront Fusion
exl-id: eac7ba26-664e-464c-b05c-8c2ebf407fb3
source-git-commit: bbd1ec27e52127c8814188612a1e8d5cfab0cd25
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 27%

---

# Connecter Adobe Workfront Fusion à Google Services avec des mesures de sécurité mises à jour

Google has introduced restrictions on how users can use their API. This article describes how to connect Adobe Workfront Fusion to Google, accounting for these update security measures.

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

## Google Services restrictions

Google introduced restrictions on how users can use their API as of June 1st, 2020. These security measures protect Google users from leakage or misuse of their personal data on Google.

These restrictions are related to the Gmail and Google Drive apps.

For more information about these restrictions, see &quot;Additional Requirements for Specific API Scopes&quot; in the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy#additional_requirements_for_specific_api_scopes)

To access restricted scopes, the connected service (Adobe Workfront Fusion or any other service that accesses the user&#39;s data via the API) must be verified, and must have a Letter of Assessment to prove that the service is secure and transparent about how they use the data. Workfront Fusion complies with all of Google&#39;s requirements for access to restricted scopes. However, most of the third-party connected services in Workfront Fusion don&#39;t have the Letter of Assessment, and therefore don&#39;t comply with Google terms. Because of that, Workfront Fusion is not permitted to send data to these services.

## Exceptions to Google Services restrictions

Il existe quelques exceptions qui permettent d’envoyer des données à un service tiers non approuvé qui ne possède pas de lettre d’évaluation sans enfreindre aucune des nouvelles restrictions. They differ based on Google Workspace with the Workfront Fusion OAuth client, Google Workspace with another OAuth client, or @gmail.com and @googlemail.com.

* [Google Workspace with Workfront Fusion OAuth client](#google-workspace-with-workfront-fusion-oauth-client)
* [Google Workspace with another OAuth client](#google-workspace-with-another-oauth-client)
* [@gmail.com and @googlemail.com](#gmailcom-and-googlemailcom)

### Google Workspace with Workfront Fusion OAuth client

Workfront Fusion uses the Domain-wide Installation exception. Domain-wide Installation is suited for Google Workspace users, and allows users to integrate unapproved services without any limitations. If you are a Google Workspace user, you don&#39;t have to perform any additional steps and can directly connect to unapproved services.

### Google Workspace with another OAuth client

Google Workspace users that prefer to use their own OAuth client instead of using the Workfront Fusion OAuth client can connect to Google Services through the Internal Use approach. Cette option est destinée aux utilisateurs et aux utilisatrices avancés. For instructions, see [Connect Adobe Workfront Fusion to Google Services using a custom OAuth client](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

### @gmail.com and @googlemail.com {#gmailcom-and-googlemailcom}

Users that access Google Services through @gmail.com or @googlemail.com can connect to Google Services through the Personal Use approach. Cette option est destinée aux utilisateurs et aux utilisatrices avancés. For instructions, see [Connect Adobe Workfront Fusion to Google Services using a custom OAuth client](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

## Questions fréquentes

* [What apps in Adobe Workfront Fusion are affected?](#what-apps-in-adobe-workfront-fusion-are-affected)
* [Do I have a Google Workspace account?](#do-i-have-a-g-suite-account)
* [What should I do if I&#39;m a @gmail.com or @googlemail.com user?](#what-should-i-do-if-im-gmailcom-or-googlemailcom-user)
* [What should I do if I&#39;m a Google Workspace user?](#what-should-i-do-if-im-a-g-suite-user)

### What apps in Adobe Workfront Fusion are affected? {#what-apps-in-adobe-workfront-fusion-are-affected}

Google Drive, Gmail, and Email (connected to Gmail account).

### Do I have a Google Workspace account? {#do-i-have-a-g-suite-account}

If your email address ends with @gmail.com or @googlemail.com, your account is not a Google Workspace account. If your Google account ends with a custom domain such as @my-company.com, then it is a Google Workspace account.

### What should I do if I&#39;m @gmail.com or @googlemail.com user? {#what-should-i-do-if-im-gmailcom-or-googlemailcom-user}

These new restrictions only apply if you are integrating Google Drive or Gmail. If you want to connect to Google Drive or Gmail, you can

* Switch to Google Workspace.

  ou

* créer un client OAuth personnalisé. Cette option est destinée aux utilisateurs et aux utilisatrices avancés.

  For instructions, see [Connect Adobe Workfront Fusion to Google Services using a custom OAuth client](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

If you want to integrate any other service than Google Drive or Gmail, these restrictions do not apply.

### What should I do if I&#39;m a Google Workspace user? {#what-should-i-do-if-im-a-g-suite-user}

Aucune action n’est requise.
