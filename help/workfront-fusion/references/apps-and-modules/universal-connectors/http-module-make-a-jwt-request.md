---
title: HTTP > Créer un module de requête JWT
description: Le module Adobe Workfront Fusion HTTP > Créer une requête JWT envoie une requête HTTP(S) à une URL et l’autorise avec un jeton web JSON que Fusion signe automatiquement pour vous.
author: Becky
feature: Workfront Fusion
exl-id: 2f8c0b0d-085a-4b49-b350-4fd4cca1d0a7
TQID: 'https://experienceleague.adobe.com/fr'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 5e6403abee4e5767da9134529b9e88070bad5f44
workflow-type: tm+mt
source-wordcount: '1437'
ht-degree: 21%
---
# [!UICONTROL HTTP] > [!UICONTROL Effectuer une requête JWT] module

Le module Adobe Workfront Fusion [!UICONTROL HTTP] > [!UICONTROL Effectuer une requête JWT] envoie une requête HTTP(S) à une URL et l’autorise avec un jeton JSON Web Token (JWT) que le module signe pour vous à chaque appel. La réponse est ensuite traitée de la même manière que dans le module standard [!UICONTROL HTTP] > [!UICONTROL Effectuer une requête].

Ce module se comporte comme le module standard [!UICONTROL Effectuer une requête], avec une différence principale : il signe automatiquement un jeton JWT à partir des revendications que vous fournissez et l’ajoute à la requête, par défaut comme `Authorization: Bearer <token>`.

Utilisez ce module pour appeler toute API qui attend un JWT signé pour l’authentification, comme les services qui nécessitent un jeton porteur de courte durée signé avec un secret partagé (HMAC) ou une clé privée (RSA/ECDSA), sans créer le jeton lors d’une étape distincte.

Si l’API utilise OAuth 2.0, authentification de base, une clé API ou un certificat client, utilisez plutôt le module HTTP dédié correspondant.

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
   <p>Basé sur les opérations : disponible pour les organisations disposant de licences basées sur les opérations</p>
   <p>Basé sur un connecteur (hérité) : Workfront Fusion pour l’automatisation et l’intégration du travail </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Si votre organisation dispose d’un package Workfront Select ou Prime qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acquérir Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences Adobe Workfront Fusion, consultez [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Créer une connexion JWT

Le module nécessite une connexion JWT. La connexion stocke le matériel de signature afin que le secret ou la clé privée n’ait pas à apparaître dans le scénario.

### Créer une connexion JWT dans Fusion

1. Ajoutez le module [!UICONTROL HTTP] > [!UICONTROL Effectuer une requête JWT] à votre scénario.
1. Cliquez sur **[!UICONTROL Ajouter]** à côté du champ **[!UICONTROL Connexion]**.
1. Configurez les champs de connexion :

   <table style="table-layout:auto">
    <col>
    <col>
    <tbody>
     <tr>
      <td role="rowheader"><p>Nom de la connexion</p></td>
      <td><p>Saisissez un nom pour la connexion.</p></td>
     </tr>
     <tr>
      <td role="rowheader"><p>Algorithme</p></td>
      <td>
       <p>Sélectionnez l’algorithme de signature de la connexion.</p>
       <ul>
        <li><code>HS256</code></li>
        <li><code>HS384</code></li>
        <li><code>HS512</code></li>
        <li><code>RS256</code></li>
        <li><code>RS384</code></li>
        <li><code>RS512</code></li>
        <li><code>PS256</code></li>
        <li><code>PS384</code></li>
        <li><code>PS512</code></li>
        <li><code>ES256</code></li>
        <li><code>ES384</code></li>
        <li><code>ES512</code></li>
       </ul>
      </td>
     </tr>
     <tr>
      <td role="rowheader"><p>Secret</p></td>
      <td>
       <p>Saisissez la clé de signature.</p>
       <ul>
        <li>Pour les algorithmes <code>HS*</code>, utilisez la chaîne secrète partagée .</li>
        <li>Pour les algorithmes <code>RS*</code>, <code>PS*</code> et <code>ES*</code>, utilisez la clé privée codée en PEM.</li>
       </ul>
      </td>
     </tr>
    </tbody>
   </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour créer la connexion et revenir au module.

>[!IMPORTANT]
>
>Une connexion JWT se signe avec un seul algorithme. Si votre scénario nécessite plusieurs algorithmes de signature, créez une connexion distincte pour chaque algorithme. Cela correspond au comportement existant de l’application JWT autonome.

## [!UICONTROL HTTP] > [!UICONTROL Effectuer une requête JWT] le module et ses champs

Lorsque vous configurez le module [!UICONTROL HTTP] > [!UICONTROL Effectuer une requête JWT], Adobe Workfront Fusion affiche les champs répertoriés ci-dessous dans l’ordre dans lequel ils apparaissent dans l’interface utilisateur du module. Un titre en gras dans un module indique un champ obligatoire. Les champs marqués comme avancés sont masqués, sauf si vous sélectionnez **[!UICONTROL Afficher les paramètres avancés]**.

<table style="table-layout:auto">
 <col>
 <col>
 <tbody>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Connection]</p></td>
   <td><p>Sélectionnez une connexion JWT existante ou créez-en une.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL URL]</p></td>
   <td><p>URL cible de la requête.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Method]</p></td>
   <td><p>Méthode HTTP telle que GET, POST, PUT, PATCH ou DELETE.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Headers]</p></td>
   <td><p>En-têtes de requête personnalisés au format clé/valeur.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Query String]</p></td>
   <td><p>Paramètres de chaîne de requête au format clé/valeur.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Body type]</p></td>
   <td><p>Méthode d’encodage du corps de la requête. Les options incluent Raw, application/x-www-form-urlencoded et multipart/form-data.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Parse response]</p></td>
   <td><p>Lorsqu’elle est activée, Fusion analyse le corps de la réponse en fonction du type de contenu de la réponse.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL JWT Payload (revendications)]</p></td>
   <td><p>Paires clé/valeur incluses comme revendications dans la payload JWT. Les revendications réservées <code>exp</code>, <code>iat</code> et <code>nbf</code> doivent être un NumericDate — un nombre de secondes depuis l'époque Unix. Les valeurs de revendication conservent leur type JSON, de sorte que les nombres restent des nombres et les booléens restent des booléens.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Timeout] (avancé)</p></td>
   <td><p>Spécifiez le délai d’expiration de la requête en secondes (1 à 300). La valeur par défaut est de 40 secondes.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Retry Count] (avancé)</p></td>
   <td><p>Spécifiez le nombre de fois où la requête doit être réessayée si la requête échoue en raison d’une erreur réessayable.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Additional Retry Status Codes] (avancé)</p></td>
   <td><p>Spécifiez d’autres codes d’état HTTP qui doivent être traités comme pouvant être réessayés.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Share cookies with other HTTP modules] (advanced)</p></td>
   <td><p>Activez cette option pour partager les cookies du serveur avec tous les modules HTTP de votre scénario.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Self-signed certificate] (avancé)</p></td>
   <td><p>Téléchargez votre certificat si vous souhaitez utiliser TLS à l’aide de votre certificat autosigné.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Rejette les connexions qui utilisent des certificats non vérifiés (auto-signés)] (avancé)</p></td>
   <td><p>Activez cette option pour rejeter les connexions qui utilisent des certificats TLS non vérifiés.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Suivre la redirection] (avancé)</p></td>
   <td><p>Activez cette option pour suivre les redirections d’URL avec les réponses 3xx.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Désactive la sérialisation de plusieurs clés de chaîne de requête identiques à des tableaux] (avancé)</p></td>
   <td><p>Par défaut, Workfront Fusion gère plusieurs valeurs pour la même clé de paramètre de chaîne de requête d’URL que les tableaux. Par exemple, <code>www.test.com?foo=bar&amp;foo=baz</code> sera converti en <code>www.test.com?foo[0]=bar&amp;foo[1]=baz</code>. Activez cette option pour désactiver cette fonction.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Demander du contenu compressé] (avancé)</p></td>
   <td><p>Activez cette option pour demander une version compressée du site web. Ajoute un en-tête <code>[!UICONTROL Accept-Encoding]</code> pour demander un contenu compressé.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Use Mutual TLS] (avancé)</p></td>
   <td><p>Activez cette option pour utiliser le protocole TLS mutuel dans la requête HTTP.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Sign Options] (avancé)</p></td>
   <td><p>Pour chaque option de signe que vous souhaitez ajouter à la requête, cliquez sur <b>Ajouter un élément</b> et saisissez le nom et la valeur du paramètre.</p><p>Options supplémentaires transmises au signataire JWT, telles que <code>expiresIn</code>, <code>issuer</code>, <code>audience</code>, <code>subject</code> et <code>keyid</code>. Les valeurs de durée telles que <code>expiresIn</code> sont interprétées par la bibliothèque <code>jsonwebtoken</code>. Un nombre brut est traité comme une milliseconde. Par conséquent, utilisez une chaîne unitaire telle que <code>"1h"</code> ou <code>"3600s"</code> pour être explicite. L’algorithme est issu de la connexion et ne peut pas être remplacé ici.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Header Name] (avancé)</p></td>
   <td><p>Saisissez ou mappez le nom de l’en-tête de requête qui reçoit le jeton JWT signé. Par défaut : <code>Authorization</code>. Le nom de l’en-tête ne doit pas contenir de point (<code>.</code>), car les noms en pointillés sont rejetés et ne peuvent pas être masqués dans les journaux de requêtes.</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Token Type] (avancé)</p></td>
   <td><p>Saisissez ou mappez le schéma d’authentification placé avant le jeton, par exemple <code>Bearer</code>. Laissez ce champ vide pour envoyer le jeton brut sans préfixe.</p></td>
  </tr>
 </tbody>
</table>

## Création du jeton

1. Le module collecte les revendications dans le champ [!UICONTROL &#x200B; Payload (revendications)] du JWT .
1. Créances réservées telles que <code>exp</code><code>iat</code>, et <code>nbf</code> sont converties en valeurs NumericDate.
1. Le module applique les [!UICONTROL options de signature] et signe le jeton à l’aide de l’algorithme de la connexion.
1. Le jeton signé est placé dans l’en-tête de la requête défini par [!UICONTROL Nom de l’en-tête].
1. Si le paramètre [!UICONTROL Type de jeton] est défini, le module ajoute le préfixe avant le jeton. Par exemple, <code>Bearer eyJ...</code>.
1. La requête est envoyée et la réponse est traitée de la même manière que le module standard [!UICONTROL HTTP] > [!UICONTROL Effectuer une requête].

Le jeton signé est automatiquement masqué dans les journaux de débogage et d’erreur afin de ne jamais être exposé.

## Exemple

### Connexion

- Algorithme : `HS256`
- Secret : `my-shared-secret`

### Paramètres du module

- URL : `https://api.example.com/v1/orders`
- Méthode : `GET`
- Payload du JWT (revendications) :
  - `sub` = `service-account-42`
  - `iss` = `make-integration`
- Options de signature :
  - `expiresIn` = `1h`
- Nom de l’en-tête : `Authorization`
- Type de jeton : `Bearer`

### Résultat

Le module envoie la requête avec un en-tête similaire à :

```text
Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...
```

## FAQ / pièges

### Pourquoi mon jeton a-t-il expiré si rapidement ?

Vous avez probablement saisi un nombre nu pour des `expiresIn` telles que `3600`. La bibliothèque `jsonwebtoken` interprète les nombres simples en millisecondes. Utilisez plutôt une chaîne unitaire telle que `"1h"` ou `"3600s"`.

### Quand le jeton est-il créé ?

Le module signe un nouveau JWT chaque fois qu’il s’exécute, et non lorsque vous créez la connexion. La connexion stocke uniquement le matériel de signature et l’algorithme, de sorte que les revendications telles que `iat` et `exp` reflètent le moment de l’exécution de ce module.

Si la requête fait l’objet de nouvelles tentatives au cours de la même exécution de module, Fusion réutilise le même jeton signé pour ces nouvelles tentatives au lieu de signer un nouveau jeton pour chaque tentative. Pour cette raison, une valeur de `expiresIn` très courte peut expirer avant qu’une nouvelle tentative ne se produise et entraîner une nouvelle tentative d’envoi d’un jeton ayant déjà expiré. Pour éviter cela, utilisez une chaîne d’unité claire telle que `"1h"` ou `"3600s"` et évitez les durées de vie des jetons trop courtes.

### Puis-je modifier l’algorithme par demande ?

Non. L’algorithme est fixé par la connexion. Si vous avez besoin d’un autre algorithme, créez une autre connexion JWT.

### Puis-je envoyer le jeton dans un en-tête personnalisé ?

Oui. Définissez le champ [!UICONTROL &#x200B; Nom de l’en-tête &#x200B;] sur un nom personnalisé, mais il ne peut pas contenir de point (`.`).

### Puis-je envoyer le jeton brut sans `Bearer` ?

Oui. Laissez le champ [!UICONTROL Type de jeton] vide.

### Le jeton est-il visible dans les journaux ?

Non. Le jeton signé est automatiquement masqué dans les journaux de débogage et d’erreur.


>[!NOTE]
>
>Remarque technique : la signature utilise la bibliothèque `jsonwebtoken` et reflète le comportement de signature de l’application JWT autonome. De ce fait, les mêmes entrées produisent le même jeton que l’application JWT autonome.
