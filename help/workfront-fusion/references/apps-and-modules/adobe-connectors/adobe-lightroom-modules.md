---
title: Modules Adobe Lightroom
description: Avec les modules Adobe Lightroom, vous pouvez démarrer un scénario Adobe Workfront Fusion en fonction des événements de votre compte Adobe Lightroom.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3f29ab35-7a90-4afb-a283-4faaacec5b15
source-git-commit: 5d1424fe88efb56e565077bf36211795c9bc96ed
workflow-type: tm+mt
source-wordcount: '2563'
ht-degree: 21%

---

# Modules [!DNL Adobe Lightroom]

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!DNL Adobe Lightroom] et le connecter à plusieurs applications et services tiers.

Si vous avez besoin d’instructions pour créer un scénario, consultez les articles sous [Créer un scénario : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

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

Avant d’utiliser le connecteur [!DNL Adobe Lightroom], vous devez vous assurer que les conditions préalables suivantes sont remplies :

* Vous devez disposer d’un compte [!DNL Adobe Lightroom].
* Une application web OAuth doit être configurée dans Adobe Admin Console. Pour plus d’informations, consultez [Configuration d’une application OAuth dans Adobe Admin Console](#configure-an-oauth-application-in-the-adobe-admin-console) dans cet article.

## Informations sur l’API Adobe Lightroom

Le connecteur Adobe Lightroom utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td>https://lr.adobe.io</td> 
  </tr>
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.17.128</td> 
  </tr>
 </tbody> 
 </table>



## Création d’une connexion à Adobe Lightroom

Pour vous connecter à Adobe Lightroom, vous devez d’abord configurer une application OAuth dans Adobe Admin Console. Une fois cette application configurée, vous pouvez créer des connexions à partir de Workfront Fusion.

### Configuration d’une application OAuth dans Adobe Admin Console

1. Commencez la configuration d’une application web OAuth dans Adobe Admin Console.

   Pour obtenir des instructions, consultez [Guide de mise en œuvre de l’authentification de l’utilisateur](https://developer.adobe.com/developer-console/docs/guides/authentication/UserAuthentication/implementation) dans la documentation Adobe destinée aux développeurs.
1. Lors de la configuration de l’application web OAuth, saisissez les valeurs suivantes :

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Scopes]</td>
        <td>
          <ul>
            <li>AdobeID</li>
            <li>lr_partner_rendition_apis</li>
            <li>openid</li>
            <li>offline_access</li>
            <li>lr_partner_apis</li>
          </ul>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL REDIRECT URI]</td>
        <td><code>https://app.workfrontfusion.com/oauth/cb/adobe-lightroom5</code></td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Redirect URI pattern]</td>
        <td><code>https://app\.workfrontfusion\.com/oauth/cb/adobe-lightroom5</code></td>
        </tr>
      </tbody>
    </table>

### Créer une connexion à Adobe Lightroom à partir de Workfront Fusion

Pour créer une connexion pour vos modules [!DNL Adobe Lightroom], procédez comme suit :

1. Dans n’importe quel module Adobe Lightroom, cliquez sur **[!UICONTROL Ajouter]** en regard de la zone Connexion .

1. Remplissez les champs suivants :

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Saisissez un nom pour cette connexion.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>Indiquez si vous vous connectez à un environnement de production ou hors production.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>Indiquez si vous vous connectez à un compte de service ou à un compte personnel.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Saisissez votre [!UICONTROL Adobe] [!UICONTROL Client ID]. Vous pouvez le trouver dans la section des détails des [!UICONTROL Credentials] du [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Saisissez votre [!UICONTROL Client Secret] [!DNL Adobe]. Vous pouvez le trouver dans la section des détails des [!UICONTROL Credentials] du [!DNL Adobe Developer Console]</td>
        </tr>
      </tbody>
    </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour enregistrer la connexion et revenir au module.


## Modules Adobe Lightroom et leurs champs

Lorsque vous configurez les modules [!DNL Adobe Lightroom], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Adobe Lightroom] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Autre](#other)
* [Ressources](#assets)
* [Albums](#albums)

### Autre

* [Contrôle de l’intégrité](#health-check)
* [Récupération des métadonnées du catalogue d’utilisateurs](#retrieve-user-catalog-metadata)

#### Contrôle de l’intégrité

Ce module d’action récupère un identifiant de version du serveur Lightroom, ce qui prouve si le service Lightroom est en cours d’exécution.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Lightroom], voir <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Créer une connexion à [!DNL Adobe Lightroom]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Credentials]</td>
      <td>
        <p>Si vous souhaitez fournir des informations d’identification spécifiques pour vous assurer qu’un serveur spécifique est en cours d’exécution, cliquez sur <b>Ajouter un élément</b> et saisissez les informations d’identification.</p><p>Les en-têtes d’autorisation sont ajoutés automatiquement.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Récupération des métadonnées du catalogue d’utilisateurs

Ce module d’action récupère les métadonnées d’un catalogue dans Adobe Lightroom. Un catalogue contient des ressources, des albums ou d’autres ressources.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Lightroom], voir <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Créer une connexion à [!DNL Adobe Lightroom]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Credentials]</td>
      <td>
        <p>Si vous souhaitez fournir des informations d’identification spécifiques pour vous assurer que vous pouvez accéder au compte utilisateur approprié, cliquez sur Ajouter un élément et saisissez les informations d’identification.</p><p>Les en-têtes d’autorisation sont ajoutés automatiquement.</p>
      </td>
    </tr>
  </tbody>
</table>

### Ressources

* [Créer un fichier d’origine de ressource](#create-an-asset-original-file)
* [Création d’une ressource](#create-an-asset)
* [Créer un fichier de paramètres de développement XMP externe de ressource](#create-an-asset-external-xmp-develop-setting-file)
* [Générer des rendus pour un fichier d’origine](#generate-renditions-for-an-original-file)
* [Obtenir une ressource de catalogue](#get-a-catalog-asset)
* [Obtention du dernier paramètre de développement XMP externe de ressource](#get-the-latest-asset-external-xmp-develop-setting-file)
* [Obtenir le dernier rendu de ressource](#get-the-latest-asset-rendition)
* [Récupération de ressources](#retrieve-assets)

#### Créer un fichier d’origine de ressource

Ce module d’action crée et charge un fichier original pour une ressource.

<!--BECKY START HERE-->

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Lightroom], voir <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Créer une connexion à [!DNL Adobe Lightroom]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant du catalogue contenant la ressource.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant de la ressource pour laquelle vous souhaitez créer et téléchargez un fichier.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Longueur du contenu en octets]</td>
      <td>
        <p>Saisissez ou mappez la longueur du contenu en octets.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Plage d’octets]</td>
      <td>
        <p>Saisissez ou mappez la plage d’octets de la requête, y compris le premier et le dernier octets et la longueur de l’entité, comme défini dans le document RFC 2616. Ces informations ne doivent être incluses que lorsque les données sont trop volumineuses pour être téléchargées dans un seul appel.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Content type]</td>
      <td>
        <p>Sélectionnez le type de contenu du nouveau fichier.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Création d’une ressource

Ce module d’action crée une ressource avec les métadonnées initiales et les informations d’importation.


<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Lightroom], voir <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Créer une connexion à [!DNL Adobe Lightroom]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant du catalogue dans lequel la ressource sera créée.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant de la nouvelle ressource.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Type de ressource]</td>
      <td>
        <p>Indiquez si la ressource est une image ou une vidéo.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Datetime user created]</td>
      <td>
        <p>Saisissez ou mappez une date au format <code>YYYY-MM-DDT00:00:00-00:00</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Datetime user updated]</td>
      <td>
        <p>Saisissez ou mappez une date au format <code>YYYY-MM-DDT00:00:00-00:00</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Date capturée]</td>
      <td>
        <p>Saisissez ou mappez une date au format <code>YYYY-MM-DDT00:00:00-00:00</code>.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Créer un fichier de paramètres de développement XMP externe de ressource

Ce module d’action prend en charge deux workflows. Le premier workflow consiste à charger le fichier de paramètres de développement XMP externe pour la ressource. Le deuxième workflow consiste à créer un fichier de paramètres de développement XMP externe en copiant à partir du fichier de paramètres de développement xmp externe d’une autre ressource.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Lightroom], voir <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Créer une connexion à [!DNL Adobe Lightroom]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Longueur du contenu en octets]</td>
      <td>
        <p>Saisissez ou mappez la longueur du contenu en octets.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Charger un nouveau fichier ou copier le fichier XMP/develop]</td>
      <td>
        <p>Indiquez si vous téléchargez un nouveau fichier ou si vous copiez un fichier à partir d’une ressource existante.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant du catalogue contenant la ressource.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant de la ressource vers laquelle vous souhaitez charger ou copier un fichier.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Lien vers XMP/fichier de développement]</td>
      <td>
        <p>Saisissez ou mappez un lien vers le fichier que vous souhaitez télécharger ou copier.</p><p>Ce fichier doit être au format JSON en cas de copie de fichier ou XML en cas de chargement de fichier.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Générer des rendus pour un fichier d’origine

Ce module d’action génère de manière asynchrone des rendus pour un fichier original.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Lightroom], voir <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Créer une connexion à [!DNL Adobe Lightroom]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Type(s) de rendu (séparés par des points-virgules)]</td>
      <td>
        <p>Saisissez le type de rendu pour le rendu que vous souhaitez créer. Si vous saisissez plusieurs types, séparez-les par un point-virgule (;). <p>Types possibles :</p><ul><li><code>fullsize</code></li><li><code>2560</code></li></ul></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Longueur du contenu en octets]</td>
      <td>
        <p>Saisissez ou mappez la longueur du contenu en octets.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant du catalogue contenant la ressource.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant de la ressource pour laquelle vous souhaitez créer un rendu d’un fichier.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Obtenir une ressource de catalogue

Ce module d’action récupère des informations sur une seule ressource d’un catalogue. Le catalogue doit appartenir à l’utilisateur dont les informations d’identification sont représentées dans la connexion utilisée dans ce module.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Lightroom], voir <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Créer une connexion à [!DNL Adobe Lightroom]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant du catalogue contenant la ressource.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant de la ressource pour laquelle vous souhaitez récupérer des informations.</p>
      </td>
    </tr>
  </tbody>
</table>


#### Obtenir le dernier fichier de paramètres de développement XMP externe de ressource

Ce module d’action récupère le fichier de paramètres XMP externes de ressource le plus récent.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Lightroom], voir <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Créer une connexion à [!DNL Adobe Lightroom]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant du catalogue contenant la ressource.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant de la ressource associée au fichier de paramètres de développement XMP.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Obtenir le dernier rendu de ressource

Ce module d’action récupère le dernier rendu de ressource du type spécifié.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Lightroom], voir <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Créer une connexion à [!DNL Adobe Lightroom]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant du catalogue contenant la ressource.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant de la ressource associée au fichier de paramètres de développement XMP.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Type de rendu]</td>
      <td>
        <p>Sélectionnez le type de rendu à récupérer.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Récupération de ressources

Ce module d’action récupère les ressources détenues par l’utilisateur dont les informations d’identification sont représentées dans la connexion utilisée dans ce module.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Lightroom], voir <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Créer une connexion à [!DNL Adobe Lightroom]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant du catalogue contenant la ressource.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Date et heure de début]</td>
      <td>
        <p>Saisissez ou mappez une date et heure. Le module renvoie les enregistrements qui ont été mis à jour après cet horodatage.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Renvoyer les ressources capturées avant]</td>
      <td>
        <p>Saisissez une date au format <code>YYYY-MM-DDT00:00:00</code>. Le module renvoie les résultats capturés avant cette date.</p><p> Ce champ ne peut pas être utilisé avec le champ <code>Return assets captured after</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Nombre maximal de ressources renvoyées]</td>
      <td>
        <p>Saisissez le nombre maximum d’enregistrements que le module doit renvoyer au cours de chaque cycle d’exécution de scénario.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL SHA256 Valeur de hachage du fichier original]</td>
      <td>
        <p></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Masquer les ressources qui se trouvent dans les piles ? »]</td>
      <td>
        <p></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset subtype values]</td>
      <td>
        <p></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset IDs]</td>
      <td>
        <p>Saisissez ou mappez jusqu’à 100 identifiants de ressource, séparés par des virgules.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Types de ressources à exclure]</td>
      <td>
        <p>Sélectionnez cette option pour exclure les ressources complètes ou incomplètes. Pour inclure toutes les ressources, laissez ce champ vide.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Group values]</td>
      <td>
        <p></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Name values]</td>
      <td>
        <p></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Favori status]</td>
      <td>
        <p></p>
      </td>
    </tr>
    </tr>
  </tbody>
</table>

### Albums

* [Ajout de ressources à un album](#add-assets-to-an-album)
* [Création d’un album](#create-an-album)
* [Supprimer un album](#delete-an-album)
* [Obtenir un album](#get-an-album)
* [Liste des actifs d’un album](#list-assets-of-an-album)
* [Récupérer les albums](#retrieve-albums)
* [Mettre à jour un album](#update-album)

#### Ajout de ressources à un album

Ce module d’action ajoute une ou plusieurs ressources à l’album spécifié. Vous pouvez ajouter jusqu’à 50 ressources en un cycle d’exécution.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Lightroom], voir <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Créer une connexion à [!DNL Adobe Lightroom]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant du catalogue contenant l’album auquel vous souhaitez ajouter des ressources.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant de l’album auquel vous souhaitez ajouter des ressources.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Assets]</td>
      <td>
        <p>Pour chaque élément que vous souhaitez ajouter à l’album, cliquez sur <b>Ajouter un élément</b> et saisissez les champs suivants.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Asset ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant de la ressource que vous souhaitez ajouter à l’album</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Cette ressource est-elle une couverture d'album ?]</td>
      <td>
        <p>Indiquez si vous souhaitez que cette ressource s’affiche sous la forme de l’image représentant l’album.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Order]</td>
      <td>
        <p></p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Metadata]</td>
      <td>
        <p>Saisissez ou mappez toutes les métadonnées que vous souhaitez inclure à la ressource. Il doit s’agir d’une seule chaîne de texte d’une longueur maximale de 1 à 24 caractères.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL ID distant]</td>
      <td>
        <p>Saisissez l’identifiant de la ressource.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Création d’un album

Ce module d’action permet de créer un album dans Lightroom.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Lightroom], voir <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Créer une connexion à [!DNL Adobe Lightroom]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant du catalogue dans lequel vous souhaitez créer un album.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
      <td>
        <p>Saisissez ou mappez un identifiant pour le nouvel album.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Subtype]</td>
      <td>
        <p>Sélectionnez le sous-type de l’album.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL API key]</td>
      <td>
        <p>Saisissez la clé API du service qui crée l’album.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Datetime user created]</td>
      <td>
        <p>Saisissez ou mappez une date au format <code>YYYY-MM-DDT00:00:00-00:00Z</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Datetime user updated]</td>
      <td>
        <p>Saisissez ou mappez une date au format <code>YYYY-MM-DDT00:00:00-00:00Z</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album name]</td>
      <td>
        <p>Saisissez ou mappez un nom pour le nouvel album.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Cover ID]</td>
      <td>
        <p>Saisissez ou mappez l’ID d’une ressource à utiliser comme couverture de cet album.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL ID distant]</td>
      <td>
        <p>Saisissez l’identifiant de la ressource.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Created date]</td>
      <td>
        <p>Saisissez ou mappez une date au format <code>YYYY-MM-DDT00:00:00-00:00Z</code>.</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL Updated date]</td>
      <td>
        <p>Saisissez ou mappez une date au format <code>YYYY-MM-DDT00:00:00-00:00Z</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL L'album est-il supprimé ?]</td>
      <td>
        <p>Activez cette option si le contenu affilié de manière externe a été supprimé.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL de l’emplacement pour modifier le contenu affilié]</td>
      <td>
        <p>S'il existe une URL où les utilisateurs peuvent modifier le contenu de cet album, saisissez-la ici.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL de l'emplacement pour afficher le contenu affilié]</td>
      <td>
        <p>S'il existe une URL où les utilisateurs peuvent voir le contenu de cet album, saisissez-la ici.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Supprimer un album

Ce module d’action supprime un album.

L’album supprimé doit avoir été créé par la même application cliente qui le supprime actuellement et il doit être de sous-type `project` ou `project_set`.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Lightroom], voir <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Créer une connexion à [!DNL Adobe Lightroom]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant du catalogue contenant l’album que vous souhaitez supprimer.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant de l’album que vous souhaitez supprimer.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Supprimer les albums enfants ?]</td>
      <td>
        <p>Choisissez si vous souhaitez supprimer les albums enfants de l'album supprimé.</p>
      </td>
    </tr>
  </tbody>
</table>

### Obtenir un album

Ce module d&#39;action récupère l&#39;album spécifié

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Lightroom], voir <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Créer une connexion à [!DNL Adobe Lightroom]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant du catalogue contenant l’album que vous souhaitez récupérer.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant de l’album que vous souhaitez récupérer.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Liste des actifs d’un album

Ce module d’action récupère une liste des ressources de l’album spécifié.



#### Récupérer les albums

Ce module d&#39;action récupère une liste d&#39;albums dans le catalogue spécifié.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Lightroom], voir <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Créer une connexion à [!DNL Adobe Lightroom]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant du catalogue contenant les albums à récupérer.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Subtypes]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant de l’album que vous souhaitez récupérer.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Nom de l'album qui précède les résultats actuels]</td>
      <td>
        <p>Si vous paginez vos résultats, saisissez ou mappez le nom du dernier album sur la page précédente.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Nombre maximal d'albums renvoyés]</td>
      <td>
        <p>Définissez le nombre maximal de ressources que [!DNL Workfront Fusion] renverrez au cours d’un cycle d’exécution. La valeur par défaut de ce champ est 100. Ce module peut renvoyer plus d'albums que cette limite si plusieurs albums à la limite ont la même valeur de <code>name_after</code>.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Mettre à jour l&#39;album

Ce module d&#39;action met à jour l&#39;album spécifié.

L’album mis à jour doit avoir été créé par la même application cliente que celle qui le met maintenant à jour, et il doit être de sous-type `project` ou `project_set`.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Lightroom], voir <a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >Créer une connexion à [!DNL Adobe Lightroom]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Catalog ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant du catalogue contenant l’album que vous souhaitez mettre à jour.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Album ID]</td>
      <td>
        <p>Saisissez ou mappez l’identifiant de l’album que vous souhaitez mettre à jour.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Autres champs</td>
      <td>
      <td>Pour la description des autres champs de ce module, voir <a href="#create-an-album" class="MCXref xref" >Créer un album</a> dans cet article.</td>
      </td>
    </tr>
  </tbody>
</table>
