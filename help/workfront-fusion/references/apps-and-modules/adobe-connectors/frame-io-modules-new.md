---
title: Modules Frame.io (Beta)
description: Compte  [!DNL Adobe Workfront Fusion Frame].io modules enable you to monitor, create, update, retrieve, or delete assets and comments in your [!DNL Frame.io] .
author: Becky
feature: Workfront Fusion
exl-id: 16d32ebd-1807-495e-8aaf-27346056ec71
source-git-commit: bf3e35a287c3beb2310a7b8d2c21c65aebfb9076
workflow-type: tm+mt
source-wordcount: '2168'
ht-degree: 46%

---

# Modules [!DNL Frame.io] Beta (V4)

>[!IMPORTANT]
>
>Cet article décrit la nouvelle version (bêta) du connecteur Frame.io. Ce connecteur est utilisé pour se connecter à Frame.io version 4.
>
>Pour obtenir des instructions sur la version héritée du connecteur Frame.io, voir [Connecteur hérité Frame.io](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md).

Les modules [!DNL Adobe Workfront Fusion] [!DNL Frame.io] vous permettent de surveiller, créer, mettre à jour, récupérer ou supprimer des ressources et des commentaires dans votre compte [!DNL Frame.io].

Workfront propose deux connecteurs Frame.io, en fonction de la version de Frame.io à laquelle vous vous connectez.

| Connecteur | Version Frame.io |
|---|---|
| Frame.io (Beta) | V4 |
| Frame.io (hérité) | V3 |

Pour obtenir des instructions sur la version héritée du connecteur Frame.io, voir [Connecteur hérité Frame.io](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md).


Pour obtenir une vidéo d’introduction au connecteur Frame.io, consultez ce qui suit :

* [Frame.io](https://video.tv.adobe.com/v/3427032/){target=_blank}

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
   <p>Actuel : aucune exigence de licence Workfront Fusion</p>
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

## Conditions préalables

Pour utiliser des modules [!DNL Frame.io], vous devez disposer d’un compte [!DNL Frame.io].

## Informations sur l’API Frame.io

Le connecteur Frame.io utilise les éléments suivants :

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

Le processus de connexion diffère selon que vous utilisez le connecteur Frame.io hérité ou le connecteur Frame.io Beta.

1. Dans un module Beta Frame.io, cliquez sur **[!UICONTROL Ajouter]** en regard de la zone Connexion.

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
            <p>Choisissez si vous souhaitez créer une connexion d’authentification des utilisateurs IMS ou une connexion de serveur IMS à serveur.</p>
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
          <td>Saisissez votre [!UICONTROL Client ID] [!DNL Adobe]. Vous pouvez le trouver dans la section [!UICONTROL Credentials details] d’[!DNL Adobe Developer Console].<p>Pour obtenir des instructions sur la localisation des informations d’identification, voir <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication#credentials" class="MCXref xref" >Informations d’identification</a> dans la documentation Adobe Developer.</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]</td>
          <td>Saisissez votre [!UICONTROL Client Secret] [!DNL Adobe]. Vous pouvez le trouver dans la section [!UICONTROL Credentials details] d’[!DNL Adobe Developer Console].<p>Pour obtenir des instructions sur la localisation des informations d’identification, voir <a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication#credentials" class="MCXref xref" >Informations d’identification</a> dans la documentation Adobe Developer.</p>
        </tr>
       </tbody>
    </table>
1. Cliquez sur **[!UICONTROL Continuer]** pour enregistrer la connexion et revenir au module.

## Modules [!DNL Frame.io] et leurs champs

Lorsque vous configurez les modules [!DNL Frame.io], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Frame.io] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Ressources](#assets)
* [Commentaires](#comments)
* [Dossiers](#folders)
* [Projets](#projects)
* [Partages](#shares)
* [Espaces de travail](#workspaces)
* [Autre](#other)

### Ressources

* [[!UICONTROL Créer une ressource]](#create-an-asset)
* [[!UICONTROL Supprimer une ressource]](#delete-an-asset)
* [[!UICONTROL Obtenir une ressource]](#get-an-asset)
* [[!UICONTROL Liste des ressources]](#list-assets)
* [[!UICONTROL Mettre à jour une ressource]](#update-an-asset)

#### [!UICONTROL Créer une ressource] <!--different for v4-->

Ce module d’action crée une ressource.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de compte] </td> 
   <td> <p>Sélectionnez le compte ou mappez l’identifiant du compte contenant le projet pour lequel vous souhaitez créer une ressource.</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Sélectionnez l’espace de travail ou mappez l’identifiant de l’espace de travail contenant le projet pour lequel vous souhaitez créer une ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Sélectionnez le projet ou mappez l’ID du projet pour lequel vous souhaitez créer une ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Path] </td> 
   <td> <p>Sélectionnez le chemin d’accès où vous souhaitez créer une ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File Name] </td> 
   <td> <p>Saisissez le nom du fichier que vous souhaitez utiliser pour cette ressource.</p> </td> 
  </tr>
    <tr> 
    <td role="rowheader">Taille du fichier </td> 
    <td> <p>Saisissez ou mappez la taille du fichier en octets.</p> </td> 
   </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL Source URL] </td> 
   <td> <p>Si vous créez un fichier, saisissez l’URL du fichier que vous souhaitez charger.</p> </td> 
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
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de compte] </td> 
   <td> <p>Sélectionnez le compte ou mappez l’identifiant du compte contenant la ressource à supprimer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
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
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de compte] </td> 
   <td> <p>Sélectionnez le compte ou mappez l’identifiant du compte contenant la ressource à récupérer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Sélectionnez ou mappez la ressource à récupérer.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Liste des ressources]

Ce module de recherche récupère toutes les ressources dans le dossier du projet spécifié.

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de compte] </td> 
   <td> <p>Sélectionnez le compte ou mappez l’identifiant du compte qui contient les ressources à répertorier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nombre maximal de ressources renvoyées] </td> 
   <td> <p>Saisissez ou mappez le nombre maximal de ressources que le module doit renvoyer au cours de chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Commentaires

* [[!UICONTROL Créer un commentaire]](#create-a-comment)
* [[!UICONTROL Supprimer un commentaire]](#delete-a-comment)
* [[!UICONTROL Obtenir un commentaire]](#get-a-comment)
* [[!UICONTROL Répertorier des commentaires]](#list-comments)
* [[!UICONTROL Mettre à jour un commentaire]](#update-a-comment)

#### [!UICONTROL Créer un commentaire]

Ce module d’action ajoute un nouveau commentaire ou une nouvelle réponse à la ressource.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de compte] </td> 
   <td> <p>Sélectionnez le compte ou mappez l’identifiant du compte contenant la ressource à laquelle vous souhaitez ajouter un commentaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Sélectionnez le compte ou mappez l’identifiant de l’espace de travail contenant la ressource à laquelle vous souhaitez ajouter un commentaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Sélectionnez le projet ou mappez l’ID du projet qui contient la ressource à laquelle vous souhaitez ajouter un commentaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Path] </td> 
   <td> <p>Sélectionnez le chemin d’accès à la ressource à laquelle vous souhaitez ajouter un commentaire.</p> </td> 
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
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de compte] </td> 
   <td> <p>Sélectionnez le compte ou mappez l’identifiant du compte contenant les commentaires à supprimer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
   <td> <p>Saisissez ou mappez l’identifiant du commentaire que vous souhaitez supprimer.</p> </td> 
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
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de compte] </td> 
   <td> <p>Sélectionnez le compte ou mappez l’identifiant du compte contenant les commentaires dont vous souhaitez récupérer les détails.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
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
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de compte] </td> 
   <td> <p>Sélectionnez ou mappez le compte contenant la ressource à partir de laquelle vous souhaitez récupérer des commentaires.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Sélectionnez ou mappez l’espace de travail contenant la ressource à partir de laquelle vous souhaitez récupérer les commentaires.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Sélectionnez le projet qui contient la ressource à partir de laquelle vous souhaitez récupérer des commentaires.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Path] </td> 
   <td> <p>Sélectionnez le chemin d’accès menant à la ressource à partir de laquelle vous souhaitez répertorier les commentaires.</p> </td> 
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
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de compte] </td> 
   <td> <p>Sélectionnez ou mappez le compte contenant le projet contenant la ressource sur laquelle vous souhaitez mettre à jour un commentaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment ID] </td> 
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

### Dossiers

#### Créer un dossier

Ce module d’action crée un dossier dans Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de compte] </td> 
   <td> <p>Sélectionnez ou mappez le compte sur lequel vous souhaitez créer un dossier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Sélectionnez ou mappez l’espace de travail dans lequel vous souhaitez créer un dossier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID] </td> 
   <td> <p>Sélectionnez l’emplacement où vous souhaitez créer un dossier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Path] </td> 
   <td> <p>Sélectionnez le chemin d’accès où vous souhaitez créer un dossier.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nom </td> 
   <td> <p>Saisissez ou mappez un nom pour le nouveau dossier.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Projets

* [Créer un projet](#create-a-project)
* [Répertorier les projets](#list-projects)

#### Créer un projet

Ce module d’action crée un projet dans Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de compte] </td> 
   <td> <p>Sélectionnez ou mappez le compte sur lequel vous souhaitez créer un projet.</p> </td> 
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

#### [!UICONTROL Répertorier des projets]

Ce module de recherche récupère tous les projets pour l’équipe spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de compte] </td> 
   <td> <p>Sélectionnez ou mappez le compte contenant la ressource à partir de laquelle vous souhaitez récupérer les projets.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>Sélectionnez ou mappez l’espace de travail contenant la ressource à partir de laquelle vous souhaitez récupérer les projets.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Nombre maximal de projets renvoyés] </td> 
   <td> <p>Saisir ou mapper le nombre maximal de projets
   vous souhaitez que le module réapparaisse lors de chaque cycle d’exécution du scénario.</p> </td> 
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
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de compte] </td> 
   <td> <p>Sélectionnez ou mappez le compte contenant le lien de partage auquel vous souhaitez ajouter une ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Share link ID] </td> 
   <td> <p>Sélectionnez ou mappez le lien de partage auquel vous souhaitez ajouter une ressource.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Asset ID] </td> 
   <td> <p>Saisissez ou mappez l’identifiant de la ressource que vous souhaitez ajouter au lien de partage.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Créer un lien de partage

Ce module d&#39;action crée un lien de partage dans Frame.io.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de compte] </td> 
   <td> <p>Sélectionnez ou mappez le compte sur lequel vous souhaitez créer un lien de partage.</p> </td> 
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
   <td> <p>Pour chaque ressource à ajouter au lien de partage, cliquez sur <b>Ajouter un élément</b> et saisissez l’identifiant de la ressource.</p> </td> 
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

Ce module d’action crée un espace de travail dans Frame.io

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de compte] </td> 
   <td> <p>Sélectionnez ou mappez le compte sur lequel vous souhaitez créer un espace de travail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Saisissez ou mappez un nouveau nom pour l’espace de travail.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Liste des espaces de travail

Ce module répertorie tous les espaces de travail d’un compte.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de compte] </td> 
   <td> <p>Sélectionnez ou mappez le compte contenant la ressource à partir de laquelle vous souhaitez récupérer les espaces de travail.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Nombre maximal d’espaces de travail renvoyés] </td> 
   <td> <p>Saisir ou mapper le nombre maximal d’espaces de travail
   vous souhaitez que le module réapparaisse lors de chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Autre

#### [!UICONTROL Effectuer un appel API personnalisé]

Ce module vous permet d’effectuer un appel API personnalisé.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Frame.io], voir <a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">Connecter [!DNL Frame.io] à [!DNL Adobe Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Saisissez un chemin relatif à <code>https://api.frame.io</code>. Exemple : <code> /v4/me</code></p> <p>Note : pour obtenir la liste des points d’entrée disponibles, voir la référence de l’API [!DNL Frame.io].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Ajoute automatiquement des en-têtes d’autorisation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Chaîne de requête] </td> 
   <td> <p>Saisissez la chaîne de requête. Pour chaque paramètre à inclure dans la chaîne de requête, cliquez sur <b>[!UICONTROL Add item]</b> et saisissez le nom du champ et la valeur souhaitée.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lors de l’utilisation d’instructions conditionnelles telles que <code>if</code> dans votre fichier JSON, placez les guillemets en dehors de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
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
