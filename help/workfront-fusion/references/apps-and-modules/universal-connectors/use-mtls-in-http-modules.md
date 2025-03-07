---
title: Utiliser le protocole TLS mutuel dans les modules HTTP d’Adobe Workfront Fusion
description: Vous pouvez utiliser le protocole TLS mutuel dans vos modules HTTP d’Adobe Workfront Fusion, ce qui permet aux deux côtés de la transaction d’information de vérifier l’identité de l’autre.
author: Becky
feature: Workfront Fusion
exl-id: 1e0b4c3b-9a0b-491d-aaf2-0011d8386abe
source-git-commit: 1fa1ef68267d971a2769400a031b333de2f684ce
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 87%

---

# Utiliser le protocole TLS mutuel dans les modules HTTP dans [!DNL Adobe Workfront Fusion]

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

## Fournir votre certificat public [!DNL Workfront Fusion]

Lorsque vous vous connectez à un service web avec une requête HTTP, le service web requiert généralement un certificat public [!DNL Workfront Fusion] pour vérification. Cela permet au service web de comparer le certificat présenté dans la requête HTTP à celui du fichier, afin de s’assurer que le certificat se trouve sur la liste autorisée du service web.

Pour obtenir des instructions sur le chargement du certificat public [!DNL Adobe Workfront Fusion] à un service web, consultez la documentation du service web.

>[!NOTE]
>
>Vous devrez peut-être fournir d’autres informations en plus du certificat. Pour plus d’informations sur les exigences d’un service web, consultez la documentation de l’API du service web.

Vous pouvez utiliser les liens suivants pour télécharger les certificats publics Workfront Fusion :

### Certificats du mercredi 23 avril 2024 au jeudi 7 mai 2025

>[!IMPORTANT]
>
>* Ces certificats publics  expirent le 7 mai 2025. [!DNL Workfront Fusion] Une fois le vôtre arrivé à expiration, vous devrez charger un nouveau certificat vers le service web. Nous vous recommandons ce qui suit :
>
>   * Notez la date d’expiration et définissez un rappel pour penser à charger le certificat vers votre service web.
>   * Mettez cette page en signet pour trouver facilement les nouveaux certificats.
>
>* Il s’agit de certificats mTLS non génériques.

* [Télécharger le Certificat  [!DNL Workfront Fusion]  2023](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-us-mtls-certificate.pem)
* [Télécharger le Certificat UE  [!DNL Workfront Fusion]  2023](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-eu-mtls-certificate.pem)

  À utiliser dans l’UE


## Activer le protocole TLS mutuel dans les modules HTTP d’[!DNL Workfront Fusion]

Tous les modules de requête [!UICONTROL HTTP] d’[!DNL Workfront Fusion] ont la possibilité d’activer le protocole TLS mutuel.

Pour activer le protocole TLS mutuel dans un module de requête [!UICONTROL HTTP], procédez comme suit :

1. Ajoutez un module de requête [!UICONTROL HTTP] à votre scénario.
1. Commencez à configurer le module.

   Pour obtenir des instructions sur la configuration d’un module de requête [!UICONTROL HTTP], consultez l’article approprié sous [Connecteurs universels](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors).

1. Activez **[!UICONTROL Afficher les paramètres avancés]** près du bas du module.
1. Activez **[!UICONTROL Utiliser TLS mutuel]**.
