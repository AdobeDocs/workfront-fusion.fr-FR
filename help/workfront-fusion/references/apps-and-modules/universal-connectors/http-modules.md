---
title: HTTP > Autres modules
description: L’application HTTP Adobe Workfront Fusion fournit divers modules de communication basés sur le protocole HTTP (Hypertext Transfer Protocol). HTTP est la base de la communication des données pour le World Wide Web. Vous pouvez utiliser les modules pour télécharger des pages et des fichiers web, appeler des webhooks et des points de terminaison d’API, etc.
author: Becky
feature: Workfront Fusion
exl-id: 7db97e6e-262d-4be2-823b-423f56a7d886
source-git-commit: 54c368d335b30f55cab19595a5b4740dde6013a7
workflow-type: tm+mt
source-wordcount: '624'
ht-degree: 59%

---

# HTTP > Autres modules

L’application Adobe Workfront Fusion [!UICONTROL HTTP] fournit divers modules de communication basés sur le protocole HTTP (Hypertext Transfer Protocol). HTTP est la base de la communication des données pour le World Wide Web. Vous pouvez utiliser les modules pour télécharger des pages et des fichiers web, appeler des webhooks et des points de terminaison d’API, etc.

Le bon choix du module dépend du mécanisme d’authentification/d’autorisation de la ressource à laquelle vous souhaitez accéder. Vous trouverez ci-dessous des exemples de modules :

* **Effectuer une requête** : principalement destiné aux ressources n’utilisant aucun type d’authentification ou d’autorisation
* **Effectuer une requête d’authentification de base** : pour les ressources utilisant [!DNL HTTP] authentification de base (BA)
* **Effectuer une requête OAuth 2.0** : pour les ressources utilisant le protocole d’autorisation OAuth 2.0
* **Effectuer une demande d’authentification de certificat client** : pour les ressources utilisant un protocole d’autorisation qui nécessite un certificat côté client
* **Effectuer une demande d’autorisation de clé API** : pour les ressources utilisant des clés API pour l’autorisation

>[!NOTE]
>
>Si vous vous connectez à un produit Adobe qui n’a pas encore de connecteur dédié, il est recommandé d’utiliser le module Adobe Authenticator.
>
>Pour plus d’informations, voir [Module Adobe Authenticator](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md).

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

## Modules de requête

Consultez les articles suivants pour obtenir des instructions spécifiques aux modules de requête :

* [Module [!UICONTROL HTTP] > [!UICONTROL Effectuer une requête]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Effectuer une demande d’autorisation de base] module](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-basic-auth-request.md)
* [Module [!UICONTROL HTTP] > [!UICONTROL Effectuer une requête OAuth 2.0]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-oauth-2-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Effectuer une demande d’autorisation de certificat client] module](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-client-cert-auth-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Effectuer une demande d’autorisation de clé API]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-api-key-auth-request.md)

## Autres modules d’action

* [[!UICONTROL Obtenir un fichier]](#get-a-file)
* [[!UICONTROL Résoudre une URL cible]](#resolve-a-target-url)

### [!UICONTROL Obtenir un fichier]

Ce module d’action télécharge un fichier à partir de l’URL spécifiée. Une fois le fichier téléchargé, vous pouvez continuer à traiter le fichier (mapper les données du fichier) à l’aide d’autres modules dans le scénario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Evaluate all states as errors (except for 2xx and 3xx )] </td> 
   <td> <p>Utilisez cette option pour configurer la gestion des erreurs.</p> <p>Pour plus d’informations, voir <a href="/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md" class="MCXref xref">Gestion des erreurs dans Adobe Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>Saisissez ou mappez l’URL du fichier à télécharger. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Share cookies with other HTTP modules] </td> 
   <td> <p>Activez cette option si vous souhaitez que les cookies de ce site soient disponibles pour d’autres modules. </p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Résoudre une URL cible]

Ce module d’action résout une chaîne de redirections HTTP et renvoie une URL cible.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>Saisissez ou mappez l’URL à résoudre, par exemple une URL [!DNL bit.ly].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method] </td> 
   <td> <p>Indiquez si vous souhaitez utiliser la méthode [!UICONTROL HEAD] ou la méthode [!UICONTROL GET].</p> </td> 
  </tr> 
 </tbody> 
</table>

## Modules itérateurs

### [!UICONTROL Récupérer des en-têtes]

Ce module renvoie chaque en-tête (nom et valeur) du module HTTP spécifié dans un lot distinct.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
   <td> <p> Sélectionnez le module à partir duquel vous souhaitez récupérer les en-têtes.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Générer des jetons web JSON (JWT)

Il est possible de générer un jeton JWT à l’aide de fonctions intégrées :

En-tête :

![En-tête JWT](/help/workfront-fusion/references/apps-and-modules/assets/jwt-header-350x19.png)

Code à copier-coller :

```
{{replace(replace(replace(base64("{""alg"":""HS256"",""typ"":""JWT""}"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```

Payload :

![Payload JWT](/help/workfront-fusion/references/apps-and-modules/assets/jwt-payload-350x17.png)

Code à copier-coller :

```
{{replace(replace(replace(base64("{""iss"":""key"",""exp"":" + (timestamp + 60) + "}"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```

Jeton :

![ Jeton JWT ](/help/workfront-fusion/references/apps-and-modules/assets/jwt-token-350x15.png)

Code à copier-coller :

```
{{1.value}}.{{2.value}}.{{replace(replace(replace(sha256(1.value + "." + 2.value; "base64"; "secret"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```
