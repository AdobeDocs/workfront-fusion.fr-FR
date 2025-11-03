---
title: Utiliser le protocole TLS mutuel dans les modules HTTP d’Adobe Workfront Fusion
description: Vous pouvez utiliser le protocole TLS mutuel dans vos modules HTTP d’Adobe Workfront Fusion, ce qui permet aux deux côtés de la transaction d’information de vérifier l’identité de l’autre.
author: Becky
feature: Workfront Fusion
exl-id: 1e0b4c3b-9a0b-491d-aaf2-0011d8386abe
source-git-commit: 54c368d335b30f55cab19595a5b4740dde6013a7
workflow-type: tm+mt
source-wordcount: '724'
ht-degree: 63%

---

# Utiliser le protocole TLS mutuel dans les modules HTTP d’Adobe Workfront Fusion

## Vue d’ensemble du protocole TLS mutuel

Lorsque vous envoyez des données sur Internet, il est important de vous assurer qu’elles arrivent ou qu’elles proviennent du bon emplacement et que seule la personne destinataire prévue peut les lire. Lorsque TLS est activé, le client (ordinateur demandant des informations) utilise des certificats pour vérifier l’identité du serveur (ordinateur fournissant des informations). Cela permet de sécuriser les connexions HTTP.

Le protocole TLS mutuel permet à cette confirmation d’identité de se dérouler dans les deux sens. Lorsque le serveur envoie son certificat pour vérifier son identité au client, il demande également le certificat du client. Cela permet de s’assurer que le serveur n’envoie pas d’informations à un site ou à une personne qui en ferait un mauvais usage.

>[!INFO]
>
>**Exemple :**
>
>* **TLS** : lorsqu’une personne saisit « MyGreatBank.com » dans un navigateur, elle veut s’assurer qu’elle se rend à My Great Bank, et non sur un site web qui risque d’abuser de ses informations bancaires ou de les vendre. Elle veut aussi s’assurer que les informations de son compte bancaire sont chiffrées.
>
>   Lorsque le navigateur (le client) se connecte à MyGreatBank.com (le serveur), TLS nécessite un certificat de MyGreatBank.com pour vérifier son identité. Le certificat est fourni par une autorité de certification, telle que [!DNL DigiCert] ou [!DNL Thawte]. Comme le navigateur fait confiance à l’autorité de certification, il autorise la connexion.
>
>* **TLS mutuel** : MySoftware.com est un client logiciel qui nécessite des informations de l’API MyGreatBank.com. MyGreatBank permet uniquement aux clients de confiance de se connecter à ses serveurs. Ainsi, en plus du protocole TLS standard qui vérifie l’identité de MyGreatBank.com, le processus d’autorité TLS/de certification vérifie également la demande de MySoftware.com.

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

## Fourniture de votre certificat public Workfront Fusion

Lorsque vous vous connectez à un service web avec une requête HTTP, le service web nécessite généralement un certificat public Workfront Fusion pour vérification. Cela permet au service web de comparer le certificat présenté dans la requête HTTP à celui du fichier, afin de s’assurer que le certificat se trouve sur la liste autorisée du service web.

Pour obtenir des instructions sur le téléchargement du certificat public Adobe Workfront Fusion vers un service web, consultez la documentation du service web.

>[!NOTE]
>
>Vous devrez peut-être fournir d’autres informations en plus du certificat. Pour plus d’informations sur les exigences d’un service web, consultez la documentation de l’API du service web.

Vous pouvez utiliser les liens suivants pour télécharger les certificats publics de Workfront Fusion. Pour localiser votre centre de données, consultez la section [Identifier votre centre de données](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md) dans l’article Configurer des adresses IP pour Fusion dans la place sur la liste autorisée de données de votre entreprise.

### Certificats pour 2025

>[!IMPORTANT]
>
>* Ces certificats publics Workfront Fusion expirent le **4 avril 2026** (États-Unis et UE) ou le **25 novembre 2025** (Azure). Une fois le vôtre arrivé à expiration, vous devrez charger un nouveau certificat vers le service web. Nous vous recommandons ce qui suit :
>
>   * Notez la date d’expiration et définissez un rappel pour penser à charger le certificat vers votre service web.
>   * Mettez cette page en signet pour trouver facilement les nouveaux certificats.
>
>* Il s’agit de certificats mTLS non génériques.

| Datacenter | Lien de téléchargement | Dates valides |
|---|---|---|
| Centre de données des États-Unis | [Télécharger le certificat américain Workfront Fusion 2025](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2025-certs/fusion-prod-us-mtls-certificate.pem) | Du 3 mars 2025 au 4 avril 2026 |
| Centre de données de l’UE | [Télécharger le certificat de l’UE Workfront Fusion 2025](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2025-certs/fusion-prod-eu-mtls-certificate.pem) | Du 3 mars 2025 au 4 avril 2026 |
| Cluster Azure | [Télécharger le certificat Workfront Fusion Azure 2025](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2025-certs/fusion-prod-az-mtls-certificate.pem) | Du 24 octobre 2024 au 25 novembre 2025 |

<!--

### Certificates for 2024

>[!IMPORTANT]
>
>* We recommend installing the certificates for 2025, available above.
>* These Workfront Fusion public certificates expire on **May 7, 2025**. After yours expires you will need to upload a new certificate to the web service. We recommend that you:
>
>   * Make note of the expiration date and set a reminder for yourself to upload the certificate to your web service.
>   * Bookmark this page to easily find the new certificates.
>
>* These are non-wildcard mTLS certificates.

| Datacenter | Download link | Dates valid |
|---|---|---|
| US Datacenter | [Download Workfront Fusion Certificate 2024](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-us-mtls-certificate.pem) | April 5, 2024 to May 7, 2025 |
| EU Datacenter | [Download Workfront Fusion EU Certificate 2024](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-eu-mtls-certificate.pem) | April 5, 2024 to May 7, 2025 |

-->

## Activation du TLS mutuel dans les modules HTTP Workfront Fusion

Tous les modules de requête Workfront Fusion [!UICONTROL HTTP] ont la possibilité d’activer le protocole TLS mutuel.

Pour activer le protocole TLS mutuel dans un module de requête [!UICONTROL HTTP], procédez comme suit :

1. Ajoutez un module de requête [!UICONTROL HTTP] à votre scénario.
1. Commencez à configurer le module.

   Pour obtenir des instructions sur la configuration d’un module de requête [!UICONTROL HTTP], consultez l’article approprié sous [Connecteurs universels](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors).

1. Activez **[!UICONTROL Afficher les paramètres avancés]** près du bas du module.
1. Activez **[!UICONTROL Utiliser TLS mutuel]**.
