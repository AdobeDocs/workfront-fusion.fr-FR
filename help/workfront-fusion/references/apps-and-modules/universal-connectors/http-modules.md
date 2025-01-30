---
title: HTTP > Autres modules
description: L’application HTTP  [!DNL Adobe Workfront Fusion]  fournit divers modules de communication basés sur le protocole HTTP (Hypertext Transfer Protocol). HTTP est la base de la communication des données pour le World Wide Web. Vous pouvez utiliser les modules pour télécharger des pages et des fichiers web, appeler des webhooks et des points de terminaison d’API, etc.
author: Becky
feature: Workfront Fusion
exl-id: 7db97e6e-262d-4be2-823b-423f56a7d886
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 91%

---

# HTTP > Autres modules

>[!NOTE]
>
>[!UICONTROL Adobe Workfront Fusion] nécessite une licence [!UICONTROL Adobe Workfront Fusion] en plus d’une licence [!UICONTROL Adobe Workfront].

L’application [!DNL Adobe Workfront Fusion] [!UICONTROL HTTP] fournit divers modules de communication basés sur le protocole HTTP (Hypertext Transfer Protocol). HTTP est la base de la communication des données pour le World Wide Web. Vous pouvez utiliser les modules pour télécharger des pages et des fichiers web, appeler des webhooks et des points de terminaison d’API, etc.

Le bon choix du module dépend du mécanisme d’authentification/d’autorisation de la ressource à laquelle vous souhaitez accéder. Vous trouverez ci-dessous des exemples de modules :

* Effectuer une requête : module universel destiné principalement aux ressources qui n’utilisent aucun type d’authentification/autorisation.
* Effectuer une requête d’authentification de base : pour les ressources qui utilisent l’authentification de base (BA) [!DNL HTTP].
* Effectuer une requête OAuth 2.0 : pour les ressources utilisant le protocole d’autorisation OAuth 2.0.
* Effectuer une demande d’authentification de certificat client : pour les ressources utilisant le protocole d’autorisation qui nécessite un certificat côté client.
* Effectuer une demande d’autorisation de clé API : pour les ressources utilisant des clés API pour l’autorisation.

>[!NOTE]
>
>Si vous vous connectez à un produit Adobe qui n’a pas encore de connecteur dédié, il est recommandé d’utiliser le module Adobe Authenticator.
>
>Pour plus d’informations, voir [Module Adobe Authenticator](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md).

## Modules de requête

Consultez les articles suivants pour obtenir des instructions spécifiques aux modules de requête :

* [[!UICONTROL HTTP] > module [!UICONTROL Make a request]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-request.md)
* [[!UICONTROL HTTP] > module [!UICONTROL Make a Basic Authorization request]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-basic-auth-request.md)
* [[!UICONTROL HTTP] > module [!UICONTROL Make an OAuth 2.0 request]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-oauth-2-request.md)
* [[!UICONTROL HTTP] > module [!UICONTROL Make a Client Certificate Authorization request]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-client-cert-auth-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Make an API Key Authorization request]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-api-key-auth-request.md)

## Autres modules d’action

* [[!UICONTROL Get a File]](#get-a-file)
* [[!UICONTROL Resolve a target URL]](#resolve-a-target-url)

### [!UICONTROL Get a File]

Ce module d’action télécharge un fichier à partir de l’URL spécifiée. Une fois le fichier téléchargé, vous pouvez continuer à traiter le fichier (mapper les données du fichier) à l’aide d’autres modules dans le scénario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>Saisissez ou mappez l’URL du fichier à télécharger. </p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Resolve a target URL]

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
   <td> <p>Choisissez si vous souhaitez utiliser la méthode [!UICONTROL HEAD] ou la méthode [!UICONTROL GET].</p> </td> 
  </tr> 
 </tbody> 
</table>

## Modules itérateurs

### [!UICONTROL Retrieve headers]

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
