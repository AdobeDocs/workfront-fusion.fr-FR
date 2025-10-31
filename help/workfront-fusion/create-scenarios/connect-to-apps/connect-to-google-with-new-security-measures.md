---
title: Connecter Adobe Workfront Fusion à Google Services avec des mesures de sécurité mises à jour
description: Google a introduit des restrictions sur la manière dont les utilisateurs peuvent utiliser leur API. Cet article décrit comment connecter Adobe Workfront Fusion à Google, en tenant compte de ces mesures de sécurité de mise à jour.
author: Becky
feature: Workfront Fusion
exl-id: eac7ba26-664e-464c-b05c-8c2ebf407fb3
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 14%

---

# Connecter Adobe Workfront Fusion à Google Services avec des mesures de sécurité mises à jour

Google a introduit des restrictions sur la manière dont les utilisateurs peuvent utiliser leur API. Cet article décrit comment connecter Adobe Workfront Fusion à Google, en tenant compte de ces mesures de sécurité de mise à jour.

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

## Restrictions des services Google

Google a introduit des restrictions sur la manière dont les utilisateurs peuvent utiliser leur API à partir du 1er juin 2020. Ces mesures de sécurité protègent les utilisateurs de Google contre les fuites ou les utilisations abusives de leurs données personnelles sur Google.

Ces restrictions sont liées aux applications Gmail et Google Drive.

Pour plus d’informations sur ces restrictions, voir « Exigences supplémentaires pour les portées d’API spécifiques » dans la politique de données utilisateur des services d’API Google [&#128279;](https://developers.google.com/terms/api-services-user-data-policy#additional_requirements_for_specific_api_scopes)

Pour accéder aux portées restreintes, le service connecté (Adobe Workfront Fusion ou tout autre service qui accède aux données de l’utilisateur via l’API) doit être vérifié et doit disposer d’une lettre d’évaluation prouvant que le service est sécurisé et transparent sur la manière dont il utilise les données. Workfront Fusion se conforme à toutes les exigences de Google relatives à l’accès aux portées restreintes. Cependant, la plupart des services connectés tiers de Workfront Fusion ne disposent pas de la lettre d’évaluation et ne se conforment donc pas aux conditions générales de Google. Pour cette raison, Workfront Fusion n’est pas autorisé à envoyer des données à ces services.

## Exceptions aux restrictions des services Google

Il existe quelques exceptions qui permettent d’envoyer des données à un service tiers non approuvé qui ne possède pas de lettre d’évaluation sans enfreindre aucune des nouvelles restrictions. Elles diffèrent selon que Google Workspace est associé au client OAuth de Workfront Fusion, Google Workspace est associé à un autre client OAuth ou @gmail.com et @googlemail.com.

* [Google Workspace avec client OAuth Workfront Fusion](#google-workspace-with-workfront-fusion-oauth-client)
* [Google Workspace avec un autre client OAuth](#google-workspace-with-another-oauth-client)
* [@gmail.com et @googlemail.com](#gmailcom-and-googlemailcom)

### Google Workspace avec client OAuth Workfront Fusion

Workfront Fusion utilise l’exception d’installation à l’échelle du domaine. L’installation à l’échelle du domaine est adaptée aux utilisateurs de Google Workspace et permet d’intégrer des services non approuvés sans aucune limite. Si vous êtes un utilisateur de Google Workspace, vous n’avez aucune étape supplémentaire à effectuer et vous pouvez vous connecter directement à des services non approuvés.

### Google Workspace avec un autre client OAuth

Les utilisateurs de Google Workspace qui préfèrent utiliser leur propre client OAuth plutôt que le client OAuth de Workfront Fusion peuvent se connecter aux services Google par le biais de l’approche Utilisation interne. Cette option est destinée aux utilisateurs et aux utilisatrices avancés. Pour obtenir des instructions, voir [Connexion d’Adobe Workfront Fusion aux services Google à l’aide d’un client OAuth personnalisé](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

### @gmail.com et @googlemail.com {#gmailcom-and-googlemailcom}

Les utilisateurs qui accèdent aux services Google par @gmail.com ou @googlemail.com peuvent se connecter aux services Google par le biais de l’approche Utilisation personnelle. Cette option est destinée aux utilisateurs et aux utilisatrices avancés. Pour obtenir des instructions, voir [Connexion d’Adobe Workfront Fusion aux services Google à l’aide d’un client OAuth personnalisé](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

## Questions fréquentes

* [Quelles sont les applications affectées dans Adobe Workfront Fusion ?](#what-apps-in-adobe-workfront-fusion-are-affected)
* [Ai-je un compte Google Workspace ?](#do-i-have-a-g-suite-account)
* [Que dois-je faire si je suis un utilisateur de @gmail.com ou @googlemail.com ?](#what-should-i-do-if-im-gmailcom-or-googlemailcom-user)
* [Que dois-je faire si je suis un utilisateur de Google Workspace ?](#what-should-i-do-if-im-a-g-suite-user)

### Quelles sont les applications affectées dans Adobe Workfront Fusion ? {#what-apps-in-adobe-workfront-fusion-are-affected}

Google Drive, Gmail et Email (connecté au compte Gmail).

### Ai-je un compte Google Workspace ? {#do-i-have-a-g-suite-account}

Si votre adresse e-mail se termine par @gmail.com ou @googlemail.com, votre compte n’est pas un compte Google Workspace. Si votre compte Google se termine par un domaine personnalisé tel que @my-company.com, il s’agit alors d’un compte Google Workspace.

### Que dois-je faire si je suis un utilisateur @gmail.com ou @googlemail.com ? {#what-should-i-do-if-im-gmailcom-or-googlemailcom-user}

Ces nouvelles restrictions ne s’appliquent que si vous intégrez Google Drive ou Gmail. Si vous souhaitez vous connecter à Google Drive ou à Gmail, vous pouvez

* Basculer vers Google Workspace

  ou

* créer un client OAuth personnalisé. Cette option est destinée aux utilisateurs et aux utilisatrices avancés.

  Pour obtenir des instructions, voir [Connexion d’Adobe Workfront Fusion aux services Google à l’aide d’un client OAuth personnalisé](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

Si vous souhaitez intégrer un service autre que Google Drive ou Gmail, ces restrictions ne s’appliquent pas.

### Que dois-je faire si je suis un utilisateur de Google Workspace ? {#what-should-i-do-if-im-a-g-suite-user}

Aucune action n’est requise.
