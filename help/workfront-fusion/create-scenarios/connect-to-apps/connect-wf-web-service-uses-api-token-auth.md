---
title: Connecter Adobe Workfront Fusion à un service web qui utilise l’autorisation par jeton API
description: Certains services ne permettent pas aux solutions d’intégration telles qu’Adobe Workfront Fusion de créer une application que vous pouvez facilement utiliser dans votre scénario.
author: Becky
feature: Workfront Fusion
exl-id: 4a8ac816-52de-41e8-96d7-1c8cde2ebe32
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '958'
ht-degree: 43%

---

# Connecter Adobe Workfront Fusion à un service web qui utilise l’autorisation par jeton API

Certains services ne permettent pas aux solutions d’intégration telles qu’Adobe Workfront Fusion de créer une application que vous pouvez facilement utiliser dans votre scénario.

La solution à ce problème consiste à connecter le service souhaité (application) à Workfront Fusion à l’aide du module HTTP > Effectuer une requête .

Cet article explique comment connecter presque n’importe quel service web à Workfront Fusion à l’aide d’une clé API/d’un jeton API.

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

## Se connecter à un service web qui utilise un jeton d’API

La procédure de connexion du service via un jeton d’API est similaire pour la plupart des services web.

1. Créez une application sur le site web du service web comme expliqué dans la section [Créer une application et obtenir le jeton d’API](#create-a-new-application-and-obtain-the-api-token) de cet article.
1. Obtenez la clé d’API ou le jeton d’API.
1. Ajoutez le module HTTP > Make a Request de Workfront Fusion à votre scénario.
1. Configurez le module en fonction de la documentation de l’API du service web et de l’exécution du scénario, comme expliqué dans la section [Configurer le module HTTP](#set-up-the-http-module) de cet article.

>[!NOTE]
>
>Cet exemple se connecte au service de notification push.

## Créer une application et obtenir le jeton d’API

>[!NOTE]
>
>Les services web peuvent créer et distribuer des clés d’API ou des jetons d’API de nombreuses manières. Pour obtenir des instructions sur l’obtention d’une clé et d’un jeton d’API pour le service web souhaité, rendez-vous sur le site web du service et recherchez « Clé d’API » ou « Jeton d’API ».
>
>Nous incluons des instructions pour l’obtention d’une clé d’API Pushover uniquement à titre d’exemple de ce que vous pourriez trouver.

1. Connectez-vous à votre compte Pushover.
1. Cliquez sur **Créer une application/un jeton d’API** au bas de la page.
1. Renseignez les informations de l’application et cliquez sur **Créer une application**.
1. Stockez le jeton d’API fourni dans un endroit sûr. Vous en aurez besoin pour le HTTP Workfront Fusion > Effectuer une requête pour vous connecter au service web souhaité (Pushover, dans ce cas).

## Configuration du module HTTP

Pour connecter un service web à votre scénario Workfront Fusion, vous devez utiliser HTTP > Créer un module de requête dans le scénario et configurer le module en fonction de la documentation de l’API du service web.

1. Ajoutez le module HTTP > Make a Request à votre scénario.
1. Pour envoyer un message push à l’aide de Workfront Fusion, configurez le module HTTP comme suit.

   >[!NOTE]
   >
   >Ces paramètres de module correspondent à la documentation de l’API du service web Pushover. Les paramètres peuvent être différents pour d’autres services web. Par exemple, le jeton API peut être inséré dans l’en-tête et non dans le champ Corps .

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> URL</td> 
      <td> <p><code>https://api.pushover.net/1/messages.json</code> </p> <p>Le champ URL contient le point d’entrée que vous trouverez dans la documentation de l’API du service web.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> Méthode</td> 
      <td> <p><code>POST</code> </p> <p>La méthode utilisée dépend du point d’entrée correspondant. Le point d’entrée de Pushover pour la publication de messages utilise la méthode POST.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> En-têtes</p> </td> 
      <td> <p>Certains services web peuvent utiliser des en-têtes pour spécifier l’authentification par jeton API ou d’autres paramètres. Ce n’est pas le cas dans notre exemple, car le point d’entrée de Pushover pour la publication de messages utilise Body (voir ci-dessous) pour tous les types de requêtes.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Chaîne de requête</p> </td> 
      <td> <p>Certains services web peuvent utiliser une chaîne de requête pour spécifier d’autres paramètres. Ce n’est pas le cas dans notre exemple, car le service web Pushover utilise Body (voir ci-dessous) pour tous les types de requête.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Type de corps</p> </td> 
      <td> <p><code>Raw</code> </p> <p>Ce paramètre vous permet de sélectionner le type de contenu JSON dans le champ Type de contenu ci-dessous.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Type de contenu</p> </td> 
      <td> <p><code>JSON (application/json)</code> </p> <p>JSON est le type de contenu requis par l’application Pushover. Cela peut différer des autres services web.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Demander le contenu</p> </td> 
      <td> <p>Saisissez le contenu de la demande de corps au format JSON. Vous pouvez utiliser le module JSON &gt; Créer JSON comme expliqué dans <a href="#map-the-json-body-using-the-json--create-json-module" class="MCXref xref">Mapper le corps JSON à l’aide du module JSON &gt; Créer JSON</a> dans cet article. Vous pouvez également saisir le contenu JSON manuellement, comme expliqué dans <a href="#enter-the-json-body-manually" class="MCXref xref">Saisir manuellement le corps du fichier JSON</a> dans cet article.</p> <p>Consultez la documentation de l’API du service web pour connaître les paramètres requis pour ce service web.</p> </td>

   </tr> 
    </tbody> 
   </table>

## Saisir le corps JSON manuellement

Spécifiez les paramètres et les valeurs au format JSON.

>[!BEGINSHADEBOX]

**Exemple :**

```
{"user":"12345c2ecu1hq42ypqzhswbyam34",
"token":"123459evz8aepwtxydndydgyumbfx",
"message":"Hello World!",
"title":"The Push Notification"}
```

>[!ENDSHADEBOX]

Cet exemple comprend les informations suivantes.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p> utilisateur</p> </td> 
   <td> <p>Votre USER_KEY. Vous pouvez le trouver dans votre tableau de bord de notification push.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> jeton </td> 
   <td> <p>Votre jeton API/clé API qui a été généré vous avez créé votre application push.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> message </td> 
   <td> <p>Contenu texte de la notification push envoyée à l’appareil ou aux appareils.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> title </td> 
   <td> <p>(Facultatif) Titre de votre message. Si aucune valeur n’est saisie, le nom de votre application est utilisé. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Mappez le corps JSON à l’aide du module JSON > Create JSON .

Le module Créer JSON facilite la spécification du JSON. Il vous donne également la possibilité de définir des valeurs de manière dynamique.

Pour plus d’informations sur les modules JSON, voir [Modules JSON](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/json-modules.md).

1. Saisissez ou mappez les valeurs à partir desquelles vous souhaitez créer JSON.

   ![Valeurs JSON](/help/workfront-fusion/create-scenarios/connect-to-apps/assets/json-values-350x288.png)

1. Connectez le module JSON > Créer un module JSON au module HTTP > Effectuer une requête .
1. Mappez la chaîne JSON du module Créer JSON au champ Contenu de la requête dans le HTTP > Effectuer une requête .

Lorsque vous exécutez le scénario, la notification push est envoyée à l’appareil qui a été enregistré dans votre compte Pushover.
