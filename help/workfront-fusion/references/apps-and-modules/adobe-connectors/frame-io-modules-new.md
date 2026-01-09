---
title: Modules Frame.io
description: Compte  [!DNL Adobe Workfront Fusion Frame].io modules enable you to monitor, create, update, retrieve, or delete assets and comments in your [!DNL Frame.io] .
author: Becky
feature: Workfront Fusion
exl-id: 16d32ebd-1807-495e-8aaf-27346056ec71
source-git-commit: 3cb613c11500dfc94774783ee0b38e6f1768de20
workflow-type: tm+mt
source-wordcount: '4539'
ht-degree: 86%

---

# Modules [!DNL Frame.io] V4

>[!IMPORTANT]
>
>Cet article décrit la nouvelle version du connecteur Frame.io. Ce connecteur est utilisé pour se connecter à la version 4 de Frame.io.
>
>Pour obtenir des instructions sur la version héritée du connecteur Frame.io, consultez [Connecteur hérité Frame.io](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md).

Les modules [!DNL Frame.io] d’Adobe Workfront Fusion vous permettent de surveiller, de créer, de mettre à jour, de récupérer ou de supprimer des ressources et des commentaires dans votre compte [!DNL Frame.io].

Workfront propose deux connecteurs Frame.io, en fonction de la version de Frame.io à laquelle vous vous connectez.

| Connecteur | Version Frame.io |
|---|---|
| Frame.io | V4 |
| Frame.io (hérité) | V3 |

Pour obtenir des instructions sur la version héritée du connecteur Frame.io, consultez [Connecteur hérité Frame.io](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md).


Pour obtenir une vidéo d’introduction au connecteur Frame.io, consultez ce qui suit :

* [Frame.io](https://video.tv.adobe.com/v/3427032/){target=_blank}

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

## Conditions préalables

Pour utiliser des modules [!DNL Frame.io], vous devez disposer d’un compte [!DNL Frame.io].

## Informations sur l’API Frame.io

Le connecteur Frame.io utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td> https://api.frame.io/v4</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Version de l’API</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.0.76</td> 
  </tr>
 </tbody> 
 </table>

## Connecter [!DNL Frame.io] à [!UICONTROL Adobe Workfront Fusion]

Vous pouvez vous connecter automatiquement à l’aide des informations d’identification d’utilisateur ou d’utilisatrice, créer manuellement une connexion d’informations d’identification d’utilisateur ou d’utilisatrice ou créer une connexion de serveur à serveur.

* [Se connecter automatiquement avec les informations d’identification d’utilisateur ou d’utilisatrice](#connect-automatically-with-user-credentials#)
* [Créer manuellement une connexion aux informations d’identification d’un utilisateur ou d’une utilisatrice](#create-a-user-credentials-connection-manually)
* [Créer une connexion de serveur à serveur](#create-a-server-to-server-connection)

### Se connecter automatiquement avec les informations d’identification d’utilisateur ou d’utilisatrice

Cette méthode crée automatiquement une connexion si vous êtes connecté à Frame.io, ou vous dirige vers la page de connexion Frame.io afin que vous puissiez vous connecter.

1. Dans un module Frame.io, cliquez sur **[!UICONTROL Ajouter]** en regard de la zone Connexion.
1. Saisissez un nom pour la connexion.
1. Cliquez sur **Continuer**.
1. Si un message vous invite à vous connecter à votre compte Frame.io, faites-le.
1. Si vous faites partie de plusieurs organisations Frame.io, sélectionnez celle que vous souhaitez utiliser pour cette connexion.

La connexion est établie.

### Créer manuellement une connexion aux informations d’identification d’un utilisateur ou d’une utilisatrice

Vous pouvez créer une connexion d’informations d’identification d’utilisateur ou d’utilisatrice en vous connectant à Frame.io ou en fournissant un ID client ou un secret client.

Pour créer une connexion serveur à serveur, vous devez d’abord configurer une application dans l’Adobe Developer Console.

* [Créer des informations d’identification d’utilisateur ou d’utilisatrice dans l’Adobe Developer Console](#create-user-credentials-in-the-adobe-developer-console)
* [Configurer une connexion d’authentification d’utilisateur ou d’utilisatrice](#configure-a-user-authentication-connection)

#### Créer des informations d’identification d’utilisateur ou d’utilisatrice dans l’Adobe Developer Console

Si vous ne disposez pas déjà d’informations d’identification de serveur à serveur sur un projet Adobe Developer Console, vous pouvez les créer.

1. Ouvrez l’[Adobe Developer Console](https://developer.adobe.com/).
1. Sélectionnez un projet existant dans l’Adobe Developer Console à utiliser pour cette connexion

   Ou

   Créez un projet dans l’Adobe Developer Console. Pour obtenir des instructions, consultez [Créer un projet vide](https://developer.adobe.com/developer-console/docs/guides/projects/projects-empty).

1. Sur la page de vue d’ensemble du projet ou sur la page Commencer de votre nouveau projet, cliquez sur **Ajouter une API**.
1. Sur la page qui s’ouvre, recherchez l’**API Frame.io** et cliquez dessus.
1. Sur la page Sélectionner le type d’authentification, choisissez **Authentification de l’utilisateur ou de l’utilisatrice** et cliquez sur **Suivant**.
1. Sur la page Ajouter des informations d’identification d’authentification d’utilisateur ou d’utilisatrice, sélectionnez **Application web OAuth** et cliquez sur **Suivant**.
1. Sur la page Configurer les informations d’identification de l’application web OAuth, saisissez ce qui suit :   <table style="table-layout:auto">
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Default redirect URI]</td>
          <td>
            <p><code>https://oauth.app.workfrontfusion.com/oauth/cb/frame-io2</code></p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Redirect URI pattern]</td>
          <td>
            <p><code>https://oauth\.app\.workfrontfusion\.com/oauth/cb/frame-io2</code></p>
          </td>
        </tr>
       </tbody>
    </table>
1. Cliquez sur **Suivant**.
1. Cliquez sur **Enregistrer l’API configurée**.
1. Sur la page produit, cliquez sur la carte correspondant aux informations d’identification que vous venez de créer.

   Vous trouverez ici votre ID client et votre secret client.

>[!NOTE]
>
> Nous vous recommandons de laisser cette fenêtre ouverte lorsque vous commencez à configurer votre connexion dans Adobe Workfront Fusion. Vous pouvez copier l’ID client ainsi que récupérer et copier le secret client de cette page pour le coller dans les champs de connexion.


#### Configuration d’une connexion d’authentification utilisateur

1. Dans un module Frame.io, cliquez sur **[!UICONTROL Ajouter]** en regard de la zone Connexion.
1. Dans la zone Créer une connexion, cliquez sur **Afficher les paramètres avancés**.

1. Remplissez les champs suivants :

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Connection type]</td>
          <td>
            <p>Sélectionnez <b>Authentification de l’utilisateur ou de l’utilisatrice IMS</b>.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Connection name]</td>
          <td>
            <p>Saisissez un nom pour cette connexion.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client ID]</td>
          <td>Saisissez votre [!UICONTROL Client ID] [!DNL Adobe]. Vous pouvez le trouver dans la section [!UICONTROL Credentials details] d’[!DNL Adobe Developer Console].<p>Pour obtenir des instructions sur la création d’informations d’identification, consultez <a href="#create-user-credentials-in-the-adobe-developer-console" class="MCXref xref">Créer des informations d’identification d’utilisateur ou d’utilisatrice dans l’Adobe Developer Console</a> dans cet article.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]</td>
          <td>Saisissez votre [!UICONTROL Client Secret] [!DNL Adobe]. Vous pouvez le trouver dans la section [!UICONTROL Credentials details] d’[!DNL Adobe Developer Console].<p>Pour obtenir des instructions sur la création d’informations d’identification, consultez <a href="#create-user-credentials-in-the-adobe-developer-console" class="MCXref xref">Créer des informations d’identification d’utilisateur ou d’utilisatrice dans l’Adobe Developer Console</a> dans cet article.</p>
        </tr>
       </tbody>
    </table>
1. Si un message vous invite à vous connecter à votre compte Frame.io, faites-le.
1. Si vous faites partie de plusieurs organisations Frame.io, sélectionnez celle que vous souhaitez utiliser pour cette connexion.

La connexion est établie.


### Créer une connexion de serveur à serveur

Pour créer une connexion serveur à serveur, vous devez d’abord configurer une application dans l’Adobe Developer Console.

* [Créer des informations d’identification serveur à serveur dans l’Adobe Developer Console](#create-server-to-server-credentials-in-the-adobe-developer-console)
* [Configurer une connexion de serveur à serveur](#configure-a-server-to-server-connection)

#### Créer des informations d’identification serveur à serveur dans l’Adobe Developer Console

Si vous ne disposez pas déjà d’informations d’identification de serveur à serveur sur un projet Adobe Developer Console, vous pouvez les créer.

1. Ouvrez l’[Adobe Developer Console](https://developer.adobe.com/).
1. Sélectionnez un projet existant dans l’Adobe Developer Console à utiliser pour cette connexion

   Ou

   Créez un projet dans l’Adobe Developer Console. Pour obtenir des instructions, consultez [Créer un projet vide](https://developer.adobe.com/developer-console/docs/guides/projects/projects-empty).

1. Sur la page de vue d’ensemble du projet ou sur la page Commencer de votre nouveau projet, cliquez sur **Ajouter une API**.
1. Sur la page qui s’ouvre, recherchez l’**API Frame.io** et cliquez dessus.
1. Sur la page Sélectionner le type d’authentification, sélectionnez **Authentification de serveur à serveur** et cliquez sur **Suivant**.
1. Saisissez un nom pour les informations d’identification. Vous pouvez ainsi identifier les informations d’identification ultérieurement dans la zone Informations d’identification de l’API de l’Adobe Admin Console.
1. Cliquez sur **Suivant**.
1. Sur la page Sélectionner les profils de produit, sélectionnez le profil de produit qui inclut le compte Frame.io auquel vous souhaitez vous connecter.
1. Cliquez sur **Enregistrer l’API configurée**.
1. Sur la page produit, cliquez sur la carte correspondant aux informations d’identification que vous venez de créer.

   Vous trouverez ici votre ID client et votre secret client.

>[!NOTE]
>
> Nous vous recommandons de laisser cette fenêtre ouverte lorsque vous commencez à configurer votre connexion dans Adobe Workfront Fusion. Vous pouvez copier l’ID client ainsi que récupérer et copier le secret client de cette page pour le coller dans les champs de connexion.


#### Configuration d’une connexion de serveur à serveur

1. Dans un module Frame.io, cliquez sur **[!UICONTROL Ajouter]** en regard de la zone Connexion.

1. Remplissez les champs suivants :

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Connection type]</td>
          <td>
            <p>Sélectionnez <b>IMS de serveur à serveur</b>.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Connection name]</td>
          <td>
            <p>Saisissez un nom pour cette connexion.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client ID]</td>
          <td>Saisissez votre [!UICONTROL Client ID] [!DNL Adobe]. Vous pouvez le trouver dans la section [!UICONTROL Credentials details] d’[!DNL Adobe Developer Console].<p>Pour obtenir des instructions sur la création d’informations d’identification, consultez <a href="#create-server-to-server-credentials-in-the-adobe-developer-console" class="MCXref xref">Créer des informations d’identification de serveur à serveur dans l’Adobe Developer Console</a> dans cet article.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]</td>
          <td>Saisissez votre [!UICONTROL Client Secret] [!DNL Adobe]. Vous pouvez le trouver dans la section [!UICONTROL Credentials details] d’[!DNL Adobe Developer Console].<p>Pour obtenir des instructions sur la création d’informations d’identification, consultez <a href="#create-server-to-server-credentials-in-the-adobe-developer-console" class="MCXref xref">Créer des informations d’identification de serveur à serveur dans l’Adobe Developer Console</a> dans cet article.</p>
        </tr>
       </tbody>
    </table>
1. Cliquez sur **[!UICONTROL Continuer]** pour enregistrer la connexion et revenir au module.




## Modules [!DNL Frame.io] et leurs champs

Lorsque vous configurez les modules [!DNL Frame.io], Workfront Fusion affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Frame.io] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, consultez [Mappage d’informations d’un module à l’autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Bouton (bascule) de mappage](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Ressources](#assets)
* [Commentaires](#comments)
* [Dossiers](#folders)
* [Projets](#projects)
* [Partages](#shares)
* [Espaces de travail](#workspaces)
* [Métadonnées](#metadata)
* [Autre](#other)

### Ressources

* [[!UICONTROL Créer une ressource]](#create-an-asset)
* [[!UICONTROL Supprimer une ressource]](#delete-an-asset)
* [[!UICONTROL Obtenir une ressource]](#get-an-asset)
* [[!UICONTROL Répertorier des ressources]](#list-assets)
* [Surveiller une ressource supprimée](#watch-asset-deleted)
* [Surveiller une nouvelle ressource](#watch-new-asset)

#### [!UICONTROL Créer une ressource] <!--different for v4-->

Ce module d’action crée une ressource. Vous pouvez charger un fichier local ou fournir l’URL d’un fichier distant à partir duquel créer la ressource.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez le compte ou mappez l’ID du compte qui contient le projet pour lequel vous souhaitez créer une ressource.</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Sélectionnez l’espace de travail ou mappez l’ID de l’espace de travail qui contient le projet pour lequel vous souhaitez créer une ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID du projet] </td> 
   <td> <p>Sélectionnez le projet ou mappez l’ID du projet pour lequel vous souhaitez créer une ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Path] </td> 
   <td> <p>Sélectionnez le chemin où vous souhaitez créer une ressource.</p> </td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader">[!UICONTROL File Name] </td> 
   <td> <p>Enter the name of the file that you want to use for this asset.</p> </td> 
  </tr> -->
    <tr> 
    <td role="rowheader">Type de chargement </td> 
    <td> <p>Choisissez si vous créez une ressource à partir d’un fichier local ou d’une vie distante.</p> </td> 
   </tr>
    <tr> 
    <td role="rowheader">Taille de fichier </td> 
    <td> <p>Si vous téléchargez un fichier local, saisissez ou mappez la taille du fichier en octets.</p> </td> 
   </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL Source URL] </td> 
   <td> <p>Si vous créez la ressource à partir d’un fichier distant, saisissez l’URL du fichier à charger.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom du fichier source.</p> </td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader">[!UICONTROL Media type] </td> 
   <td> <p>Select the media type for this asset.</p> </td> 
  </tr> -->
  </tbody> 
</table>

#### [!UICONTROL Création d’une ressource (héritée)] <!--different for v4-->

Ce module d’action crée une ressource.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez le compte ou mappez l’ID du compte qui contient le projet pour lequel vous souhaitez créer une ressource.</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Sélectionnez l’espace de travail ou mappez l’ID de l’espace de travail qui contient le projet pour lequel vous souhaitez créer une ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID du projet] </td> 
   <td> <p>Sélectionnez le projet ou mappez l’ID du projet pour lequel vous souhaitez créer une ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Path] </td> 
   <td> <p>Sélectionnez le chemin où vous souhaitez créer une ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File Name] </td> 
   <td> <p>Saisissez le nom du fichier que vous souhaitez utiliser pour cette ressource.</p> </td> 
  </tr>
    <tr> 
    <td role="rowheader">Taille de fichier </td> 
    <td> <p>Saisissez ou mappez la taille du fichier en octets.</p> </td> 
   </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL Source URL] </td> 
   <td> <p>Si vous créez un fichier, saisissez l’URL du fichier à charger.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Media type] </td> 
   <td> <p>Sélectionnez le type de média de cette ressource.</p> </td> 
  </tr> 
  </tbody> 
</table>

#### [!UICONTROL Supprimer une ressource]

Ce module d’action supprime une ressource spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez le compte ou mappez l’ID du compte qui contient la ressource que vous souhaitez supprimer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de la ressource] </td> 
   <td> <p>Sélectionnez ou mappez la ressource à supprimer.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obtenir une ressource]

Ce module d’action récupère les détails d’une ressource.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez le compte ou mappez l’ID du compte qui contient la ressource que vous souhaitez récupérer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Sélectionnez ou mappez la ressource à récupérer.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Répertorier des ressources]

Ce module de recherche récupère toutes les ressources dans le dossier du projet spécifié.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez le compte ou mappez l’identifiant du compte qui contient les ressources que vous souhaitez répertorier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned assets] </td> 
   <td> <p>Saisissez ou mappez le nombre maximal de ressources que le module doit renvoyer au cours de chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Surveiller une ressource supprimée

Ce module de déclenchement démarre un scénario lorsqu’une ressource est supprimée.

Sélectionnez le webhook à utiliser pour ce module ou cliquez sur Ajouter en regard du champ Webhook et saisissez les informations suivantes :

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name] </td> 
   <td> <p>Saisissez un nom pour le nouveau webhook.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez le compte ou mappez l’identifiant du compte que vous souhaitez surveiller pour obtenir les ressources supprimées.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Surveiller une nouvelle ressource

Ce module de déclenchement démarre un scénario lorsqu’une nouvelle ressource est créée.

Sélectionnez le webhook à utiliser pour ce module ou cliquez sur Ajouter en regard du champ Webhook et saisissez les informations suivantes :

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name] </td> 
   <td> <p>Saisissez un nom pour le nouveau webhook.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez le compte ou mappez l’identifiant du compte que vous souhaitez surveiller pour obtenir les nouvelles ressources.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Commentaires

* [[!UICONTROL Créer un commentaire]](#create-a-comment)
* [[!UICONTROL Supprimer un commentaire]](#delete-a-comment)
* [[!UICONTROL Obtenir un commentaire]](#get-a-comment)
* [[!UICONTROL Répertorier des commentaires]](#list-comments)
* [[!UICONTROL Mettre à jour un commentaire]](#update-a-comment)
* [Surveiller le commentaire mis à jour](#watch-comment-updated)
* [Surveiller le nouveau commentaire](#watch-new-comment)

#### [!UICONTROL Créer un commentaire]

Ce module d’action ajoute un nouveau commentaire ou une nouvelle réponse à la ressource.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez le compte ou mappez l’ID du compte contenant la ressource à laquelle vous souhaitez ajouter un commentaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Sélectionnez le compte ou mappez l’ID de l’espace de travail contenant la ressource à laquelle vous souhaitez ajouter un commentaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID du projet] </td> 
   <td> <p>Sélectionnez le projet ou mappez l’ID du projet qui contient la ressource à laquelle vous souhaitez ajouter un commentaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Path] </td> 
   <td> <p>Sélectionnez le chemin de la ressource à laquelle vous souhaitez ajouter un commentaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p> Saisissez le contenu textuel du commentaire ou de la réponse.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp] </td> 
   <td> <p>Saisissez le numéro de l’image dans la vidéo à laquelle le commentaire doit être lié.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Page] </td> 
   <td> <p>Si la ressource est un PDF, saisissez ou mappez la page à laquelle le commentaire doit être joint.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Supprimer un commentaire]

Ce module d’action supprime un commentaire existant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez le compte ou mappez l’ID du compte qui contient le commentaire à supprimer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>Saisissez ou mappez l’ID du commentaire à supprimer.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obtenir un commentaire]

Ce module d’action récupère les détails du commentaire spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez le compte ou mappez l’ID du compte qui contient le commentaire dont vous devez récupérer les détails.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID du commentaire] </td> 
   <td> <p>Sélectionnez le commentaire dont vous souhaitez récupérer les détails.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Répertorier des commentaires]

Ce module de recherche récupère tous les commentaires de la ressource spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Saisissez ou mappez le compte contenant la ressource à partir de laquelle récupérer les commentaires.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Sélectionnez ou mappez l’espace de travail qui contient la ressource à partir de laquelle récupérer les commentaires.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Sélectionnez le projet contenant la ressource à partir de laquelle récupérer les commentaires.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Path] </td> 
   <td> <p>Sélectionnez le chemin conduisant à la ressource à partir de laquelle répertorier les commentaires.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned comments] </td> 
   <td> <p>Saisissez ou mappez le nombre maximum de commentaires que vous souhaitez que le module renvoie lors de chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mettre à jour un commentaire]

Ce module d’action modifie un commentaire existant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez ou mappez le compte contenant le projet qui contient la ressource sur laquelle vous souhaitez mettre à jour un commentaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID du commentaire] </td> 
   <td> <p>Sélectionnez le commentaire à mettre à jour.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p> Saisissez le contenu textuel du commentaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp] </td> 
   <td> <p>Saisissez le numéro de l’image dans la vidéo à laquelle le commentaire est lié.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Page] </td> 
   <td> <p>Si la ressource est un PDF, saisissez ou mappez la page à laquelle le commentaire est joint.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Surveiller le commentaire mis à jour

Ce module déclencheur lance un scénario lorsqu’un commentaire est mis à jour.

Sélectionnez le webhook à utiliser pour ce module ou cliquez sur Ajouter en regard du champ Webhook et saisissez les informations suivantes :

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name] </td> 
   <td> <p>Saisissez un nom pour le nouveau webhook.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez le compte ou mappez l’ID du compte que vous souhaitez surveiller pour obtenir des commentaires mis à jour.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Surveiller le nouveau commentaire

Ce module déclencheur lance un scénario lorsqu’un commentaire est créé.

Sélectionnez le webhook à utiliser pour ce module ou cliquez sur Ajouter en regard du champ Webhook et saisissez les informations suivantes :

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name] </td> 
   <td> <p>Saisissez un nom pour le nouveau webhook.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez le compte ou mappez l’ID du compte que vous souhaitez observer pour obtenir de nouveaux commentaires.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Dossiers

#### Créer un dossier

Ce module d’action crée un dossier dans Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez ou mappez le compte dans lequel vous souhaitez créer un dossier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Sélectionnez ou mappez l’espace de travail dans lequel vous souhaitez créer un dossier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Sélectionnez le projet dans lequel vous souhaitez créer un dossier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Path] </td> 
   <td> <p>Sélectionnez le chemin où vous souhaitez créer un dossier.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nom </td> 
   <td> <p>Saisissez ou mappez un nom pour le nouveau dossier.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Projets

* [Créer un projet](#create-a-project)
* [Inviter des utilisateurs et utilisatrices à rejoindre le projet Frame.io](#invite-users-to-frameio-project)
* [Répertorier les projets](#list-projects)

#### Créer un projet

Ce module d’action crée un projet dans Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez ou mappez le compte dans lequel vous souhaitez créer un projet.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Sélectionnez ou mappez l’espace de travail dans lequel vous souhaitez créer un projet.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nom </td> 
   <td> <p>Saisissez ou mappez un nom pour le nouveau projet.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Inviter des utilisateurs et utilisatrices à rejoindre le projet Frame.io

Ce module d’action invite les utilisateurs et utilisatrices à rejoindre le projet Frame.io spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez ou mappez le compte contenant le projet auquel vous souhaitez inviter un utilisateur ou une utilisatrice.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Sélectionnez ou mappez l’espace de travail contenant le projet auquel vous souhaitez inviter un utilisateur ou une utilisatrice.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID de projet </td> 
   <td> <p>Sélectionnez ou mappez le projet auquel vous souhaitez inviter un utilisateur ou une utilisatrice.</p> </td> 
  </tr> 
  </tr> 
   <tr> 
   <td role="rowheader">Identifiant d’utilisateur ou d’utilisatrice </td> 
   <td> <p>Sélectionnez ou mappez l’utilisateur ou l’utilisatrice que vous souhaitez inviter au projet.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Répertorier des projets]

Ce module de recherche récupère tous les projets pour l’équipe spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Saisissez ou mappez le compte contenant la ressource à partir de laquelle vous souhaitez récupérer les projets.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Sélectionnez ou mappez l’espace de travail qui contient la ressource à partir de laquelle vous souhaitez récupérer les projets.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned projects] </td> 
   <td> <p>Saisissez ou mappez le nombre maximal de projets que le module doit renvoyer pour chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Partages

* [Ajouter une ressource à un lien de partage](#add-an-asset-to-a-share-link)
* [Créer un lien de partage](#create-a-share-link)

#### Ajouter une ressource à un lien de partage

Ce module d’action ajoute une ressource à un lien de partage dans Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez ou mappez le compte contenant le lien de partage auquel vous souhaitez ajouter une ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Share link ID] </td> 
   <td> <p>Sélectionnez ou mappez le lien de partage auquel vous souhaitez ajouter une ressource.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Saisissez ou mappez l’ID de la ressource à ajouter au lien de partage.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Créer un lien de partage

Ce module d’action crée un lien de partage dans Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez ou mappez le compte dans lequel vous souhaitez créer un lien de partage.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Sélectionnez ou mappez l’espace de travail dans lequel vous souhaitez créer un lien de partage.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Sélectionnez ou mappez le projet dans lequel vous souhaitez créer un lien de partage.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Accès </td> 
   <td> <p>Indiquez si ce lien a un accès public ou restreint.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Ressources </td> 
   <td> <p>Pour chaque ressource à ajouter au lien de partage, cliquez sur <b>Ajouter un élément</b> et saisissez l’ID de la ressource.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Description </td> 
   <td> <p>Saisissez ou mappez une description pour le lien de partage.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nom </td> 
   <td> <p>Saisissez ou mappez la date d’expiration du lien de partage.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nom </td> 
   <td> <p>Saisissez ou mappez un nom pour le nouveau lien de partage.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nom </td> 
   <td> <p>Saisissez ou mappez une phrase secrète pour le lien de partage.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Espaces de travail

#### Créer un espace de travail

Ce module d’action crée un nouvel espace de travail dans Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez ou mappez le compte dans lequel vous souhaitez créer un espace de travail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Saisissez ou mappez un nouveau nom pour l’espace de travail.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Répertorier les espaces de travail

Ce module répertorie tous les espaces de travail d’un compte.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Saisissez ou mappez le compte contenant la ressource à partir de laquelle vous souhaitez récupérer les espaces de travail.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned workspaces] </td> 
   <td> <p>Saisissez ou mappez le nombre maximal d’espaces de travail que le module doit renvoyer pour chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Métadonnées

* [Création d’un champ de niveau compte](#create-an-account-level-field)
* [Suppression d’un champ de niveau compte](#delete-an-account-level-field)
* [Obtenir les métadonnées](#get-metadata)
* [Répertorier les champs au niveau du compte](#list-account-level-fields)
* [Mise à jour d’une définition de champ au niveau du compte](#update-an-account-level-field-definition)
* [Mise à jour des métadonnées sur plusieurs fichiers](#update-metadata-across-multiple-files)

#### Création d’un champ de niveau compte

Ce module d’action crée et configure un champ de métadonnées au niveau du compte.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez ou mappez le compte sur lequel vous souhaitez créer les métadonnées.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Type de champ </td> 
   <td> <p>Sélectionnez le type de champ de métadonnées que vous souhaitez créer, puis configurez les options de ce champ.</p> </td> 
  </tr> 
  </tr> 
   <tr> 
   <td role="rowheader">Nom </td> 
   <td> <p>Saisissez ou mappez un nom pour le nouveau champ.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Suppression d’un champ de niveau compte

Ce module d’action supprime un seul champ de métadonnées au niveau du compte.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez ou mappez le compte contenant le champ de métadonnées à supprimer.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID de définition de champ </td> 
   <td> <p>Saisissez ou mappez l’identifiant du champ que vous souhaitez supprimer. Vous pouvez trouver des identifiants de champ avec le module Champs de niveau compte de liste .</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Obtenir les métadonnées

Ce module d&#39;action récupère les métadonnées d&#39;un fichier dans Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez ou mappez le compte contenant le fichier pour lequel vous souhaitez récupérer les métadonnées.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Identifiant du fichier </td> 
   <td> <p>Saisissez ou mappez l’identifiant du fichier pour lequel vous souhaitez récupérer les métadonnées.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Afficher la valeur nulle </td> 
   <td> <p>Activez cette option pour inclure les champs avec une valeur nulle dans la sortie.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Répertorier les champs au niveau du compte

Ce module récupère une liste des champs de métadonnées de niveau compte pour le compte spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez ou mappez le compte à partir duquel vous souhaitez répertorier les champs.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned agreements]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal de champs que le module doit renvoyer pour chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Mise à jour d’une définition de champ au niveau du compte

Ce module met à jour la définition d’un champ de métadonnées existant unique.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez ou mappez le compte sur lequel vous souhaitez créer les métadonnées.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID de définition de champ </td> 
   <td> <p>Saisissez ou mappez l’identifiant du champ que vous souhaitez mettre à jour. Vous pouvez trouver des identifiants de champ avec le module Champs de niveau compte de liste .</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Type de champ </td> 
   <td> <p>Si vous souhaitez modifier le type de champ, sélectionnez le type de champ de métadonnées que vous souhaitez créer, puis configurez les options de ce champ.</p> </td> 
  </tr> 
  </tr> 
   <tr> 
   <td role="rowheader">Nom </td> 
   <td> <p>Saisissez ou mappez un nouveau nom pour le champ.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Mise à jour des métadonnées sur plusieurs fichiers

Ce module met à jour les champs de métadonnées d’un ou de plusieurs fichiers avec les valeurs que vous spécifiez.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez ou mappez le compte contenant les fichiers pour lesquels vous souhaitez mettre à jour les métadonnées.</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Sélectionnez l’espace de travail ou mappez l’ID de l’espace de travail qui contient le projet pour lequel vous souhaitez créer une ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID du projet] </td> 
   <td> <p>Sélectionnez le projet ou mappez l’ID du projet pour lequel vous souhaitez créer une ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File IDs] </td> 
   <td> <p>Pour chaque fichier pour lequel vous souhaitez mettre à jour les métadonnées, cliquez sur <b>Ajouter un élément</b> et saisissez ou mappez l’identifiant du fichier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Values] </td> 
   <td> <p>Pour chaque champ pour lequel vous souhaitez mettre à jour les métadonnées, cliquez sur <b>Ajouter un élément</b> et saisissez ou mappez l’identifiant de la définition de champ et la valeur que vous souhaitez placer dans ce champ. Tous les fichiers spécifiés dans le champ ID de fichier sont mis à jour avec cette valeur de champ.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Autre

* [Effectuer un appel API personnalisé](#make-a-custom-api-call)
* [Surveiller les événements](#watch-events)
* [Surveiller la mise à jour de la valeur des métadonnées](#watch-metadata-value-updated)


#### [!UICONTROL Effectuer un appel API personnalisé]

Ce module vous permet d’effectuer un appel API personnalisé.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Saisissez un chemin relatif à <code>https://api.frame.io</code>. Exemple : <code> /v4/me</code></p> <p>Note : pour obtenir la liste des points d’entrée disponibles, voir la référence de l’API [!DNL Frame.io].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, consultez <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion ajoute automatiquement des en-têtes d’autorisation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query string] </td> 
   <td> <p>Saisissez la chaîne de requête. Pour chaque paramètre à inclure dans la chaîne de requête, cliquez sur <b>[!UICONTROL Add item]</b> et saisissez le nom du champ et la valeur souhaitée.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre JSON, placez les guillemets à l’extérieur de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Surveiller les événements

Ce module de déclenchement instantané démarre un scénario lorsque l’événement sélectionné se produit dans Frame.io.

Vous pouvez utiliser un webhook existant ou en créer un nouveau.

Pour créer un webhook :

1. Cliquez sur **Ajouter** à côté du champ Webhook.
1. Renseignez les informations suivantes :

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
     <td role="rowheader">Nom du Webhook </td> 
      <td> <p>Saisissez un nom pour le nouveau webhook.</p> </td> 
     </tr> 
     <tr> 
       <td role="rowheader">[!UICONTROL Connection] </td> 
       <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
     </tr> 
     <tr> 
     <td role="rowheader">[!UICONTROL Account ID] </td> 
      <td> <p>Sélectionnez ou mappez le compte contenant l’espace de travail dans lequel vous souhaitez regarder les événements.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Workspace ID]</td> 
      <td> <p>Saisissez l’identifiant de l’espace de travail dans lequel vous souhaitez regarder les événements.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Events]</td> 
      <td> <p>Sélectionnez les événements qui doivent déclencher ce module</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Cliquez sur **Enregistrer** pour enregistrer le webhook et revenir au module .
1. Cliquez sur **OK** dans le module Événements Espion pour enregistrer la configuration.


#### Surveiller la mise à jour de la valeur des métadonnées

Ce module déclencheur lance un scénario lorsqu’un commentaire est mis à jour.

Sélectionnez le webhook à utiliser pour ce module ou cliquez sur Ajouter en regard du champ Webhook et saisissez les informations suivantes :

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name] </td> 
   <td> <p>Saisissez un nom pour le nouveau webhook.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], consultez la section <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à Adobe Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account ID] </td> 
   <td> <p>Sélectionnez le compte ou mappez l’ID du compte dont vous souhaitez surveiller les mises à jours des valeurs de métadonnées.</p> </td> 
  </tr> 
 </tbody> 
</table>


<!-- 
**Example:** The following API call returns all teams and its details in your [!DNL Frame.io] account:

URL: `/v2/teams`

Method: `GET`

![API call example](/help/workfront-fusion/references/apps-and-modules/assets/api-call-example.png)

The result can be found in the module's Output under Bundle > Body.

In our example, the details of 1 team were returned:

![API call output](/help/workfront-fusion/references/apps-and-modules/assets/api-call-output.png)

-->
