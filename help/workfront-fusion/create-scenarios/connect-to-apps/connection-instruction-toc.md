---
title: Création de connexions
description: Une connexion doit respecter les exigences définies par l’API de l’application ou du service web auquel elle se connecte. Pour cette raison, les instructions de configuration d’une connexion varient en fonction de l’application ou du service web. Cet article peut vous aider à identifier et à localiser les instructions pour connecter  [!DNL Adobe Workfront Fusion]  à l’application ou au service web de votre choix.
author: Becky
feature: Workfront Fusion
exl-id: 281403a6-6f88-4976-8a10-1d0848ef9b35
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 60%

---

# Création de connexions

Une connexion doit respecter les exigences définies par l’API de l’application ou du service web auquel elle se connecte. Pour cette raison, les instructions de configuration d’une connexion varient en fonction de l’application ou du service web. Cet article peut vous aider à identifier et à localiser les instructions pour connecter [!DNL Adobe Workfront Fusion] à l’application ou au service web de votre choix.

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
   <p>Actuel : aucune exigence de licence Workfront Fusion</p>
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

## Se connecter à une application ou à un service web qui ne nécessite pas de configuration.

Dans la plupart des cas, vous pouvez utiliser le module pour créer une connexion avec peu ou pas d’informations supplémentaires. [!DNL Workfront Fusion] gère automatiquement l’authentification.

Pour obtenir des instructions sur la création d’une connexion sans considérations particulières, voir [Création d’une connexion - Instructions de base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md).

## Connexion à une application ou à un service Adobe

Pour vous connecter à un service ou à une application Adobe, vous aurez peut-être besoin d’informations provenant de Adobe Admin Console, telles que votre ID d’organisation ou votre ID de compte technique.

Vous pouvez également utiliser le module Adobe Authenticator pour vous connecter à n’importe quelle API Adobe à l’aide d’une seule connexion. Cela vous permet de vous connecter plus facilement à des produits Adobe qui n’ont pas encore de connecteur Fusion dédié.

Pour obtenir des instructions spécifiques, consultez [l’article relatif au connecteur](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#connectors-for-adobe-products).

## Se connecter à une application ou service web [!DNL Microsoft]

La plupart des applications [!DNL Microsoft] dans [!DNL Workfront Fusion] vous permettent de créer une connexion sans informations supplémentaires.

Les circonstances suivantes nécessitent des étapes supplémentaires lors de la création d’une connexion :

* Utilisation des modules Microsoft Dynamics 365.

  Pour obtenir des instructions, voir [Modules Microsoft Dynamics 365](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-dynamics-365-modules.md).

* Connexion à l’API Microsoft Graph à l’aide d’un module HTTP

  Pour obtenir des instructions, voir [Appeler l’API REST MS Graph](/help/workfront-fusion/create-scenarios/connect-to-apps/call-the-ms-graph-rest-api.md).

## Se connecter à une application ou un service web [!DNL Google]

Le processus pour se connecter à des applications [!DNL Google] peut varier en fonction du type compte [!DNL Google] que vous utilisez. En outre, les mesures de sécurité [!DNL Google] peuvent nécessiter une configuration supplémentaire lorsque vous vous connectez à [!DNL Workfront Fusion].

Pour plus d’informations, voir ce qui suit :

* [Connecter Adobe Workfront Fusion à Google Services à l’aide d’un client OAuth personnalisé](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md)
* [Connecter Adobe Workfront Fusion à Google Services avec des mesures de sécurité mises à jour](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-google-with-new-security-measures.md)

## Autres applications nécessitant une configuration supplémentaire

Certains services et applications ne respectent pas la configuration de base pour les connexions [!DNL Workfront Fusion]. Vous trouverez des instructions pour la connexion de ces applications dans l’article correspondant à cette application.

Pour obtenir des instructions spécifiques, consultez [l’article relatif au connecteur](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#connectors-for-third-party-applications).
