---
title: Modules Bynder
description: Dans un scénario  [!DNL Adobe Workfront Fusion] , vous pouvez automatiser les workflows qui utilisent  [!DNL Bynder]et le connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: 0a45f8a7-12cc-41cc-9135-92f4779afac0
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '1779'
ht-degree: 85%

---

# Modules [!DNL Bynder]

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!DNL Bynder] et le connecter à plusieurs applications et services tiers.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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

Pour utiliser les modules [!DNL Bynder], vous devez disposer d’un compte [!DNL Bynder].

## Informations sur l’API Bundter

Le connecteur Bynder utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Version de l’API</td> 
   <td> v4 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.25.21</td> 
  </tr>
 </tbody> 
 </table>

## Connecter [!DNL Bynder] à Workfront Fusion  {#connect-bynder-to-workfront-fusion}

>[!NOTE]
>
>Bynder utilise le code d’autorisation / type d’octroi du jeton d’actualisation. Il s’agit du seul type d’octroi utilisé par le connecteur Fusion Bunder.

* [Créer une connexion à  [!DNL Bynder]  à partir de  [!DNL Workfront Fusion]](#create-a-connection-to-bynder-from-workfront-fusion)
* [Générer un [!UICONTROL identifiant client] et une [!UICONTROL clé secrète client] dans  [!DNL Bynder]  (Facultatif)](#generate-a-client-id-and-client-secret-in-bynder-optional)

### Créer une connexion à [!DNL Bynder] à partir de [!DNL Workfront Fusion]

Vous pouvez créer une connexion à votre compte [!DNL Bynder] directement à partir de [!DNL Workfront Fusion] depuis l’intérieur d’un module [!DNL Bynder].

1. Dans n’importe quel module [!DNL Bynder], cliquez sur **[!UICONTROL Ajouter]** à côté du champ [!UICONTROL Connexion].
1. Sélectionnez le domaine [!DNL Bynder] auquel vous souhaitez vous connecter.
1. (Facultatif) Cliquez sur **[!UICONTROL Paramètres avancés]**, puis saisissez votre [!UICONTROL Identifiant client] et [!UICONTROL clé secrète client].

   Pour plus d’informations sur la génération de l’identifiant client et de la clé secrète client, consultez dans cet article la section [Générer un identifiant client et une clé secrète client dans  [!DNL Bynder] (Facultatif)](#generate-a-client-id-and-client-secret-in-bynder-optional).

1. Dans la fenêtre de [!UICONTROL connexion], saisissez votre nom d’utilisateur ou d’utilisatrice (adresse e-mail) et votre mot de passe.
1. Cliquez sur **[!UICONTROL Continuer]** pour créer la connexion et revenir au module.

### Générer un [!UICONTROL Identifiant client] et une [!UICONTROL clé secrète client] dans [!DNL Bynder] (Facultatif)

Vous pouvez générer l’identifiant client et la clé secrète client à partir de votre compte [!DNL Bynder] si vous souhaitez créer une connexion à l’aide de ceux-ci. L’identifiant client et la clé secrète client sont générés lorsque vous créez une application dans [!DNL Bynder].

Pour obtenir des instructions sur la création d’une application dans [!DNL Bynder], consultez la section [Applications Oauth 2.0](https://developer-docs.bynder.com/api/authentication-oauth2-oauth-apps/) dans la documentation [!DNL Bynder].

>[!NOTE]
>
>* Lors de la création de l’application dans [!DNL Bynder], saisissez ce qui suit en tant que `redirect uri` :
>
>   * Cluster US : `https://app.workfrontfusion.com/oauth/cb/workfront-bynder`
>   * Groupement UE : `https://app-eu.workfrontfusion.com/oauth/cb/workfront-bynder`
>   * Cluster Azure : `https://app-az.workfrontfusion.com/oauth/cb/workfront-bynder`
>* Bynder utilise le code d’autorisation / type d’octroi du jeton d’actualisation. Il s’agit du seul type d’octroi utilisé par le connecteur Fusion Bunder.

## Modules [!DNL Bynder] et leurs champs

Lorsque vous configurez les modules [!DNL Bynder], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Bynder] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Actions](#actions)
* [Recherches](#searches)
* [Déclencheurs](#triggers)

### Actions

* [[!UICONTROL Ajouter une balise aux ressources]](#add-a-tag-to-assets)
* [[!UICONTROL Ajouter des ressources à une collection]](#add-assets-to-a-collection)
* [[!UICONTROL Appel API personnalisé]](#custom-api-call)
* [[!UICONTROL Télécharger des ressources]](#download-asset)
* [[!UICONTROL Lire les métadonnées des ressources]](#read-asset-metadata)
* [[!UICONTROL Supprimer une balise] des ressources](#remove-a-tag-from-assets)
* [[!UICONTROL Supprimer des ressources de la collection]](#remove-assets-from-collection)
* [[!UICONTROL Mettre à jour des métadonnées des ressources]](#update-asset-metadata)
* [[!UICONTROL Charger des ressources]](#upload-asset)

#### [!UICONTROL Ajouter une balise aux ressources]

Ce module d’action ajoute une balise à une ou plusieurs ressources

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Bynder] à [!DNL Workfront Fusion], voir <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Bynder] à [!DNL Workfront Fusion] </a>dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tag ID]</td> 
   <td> <p>Saisissez ou mappez l’ID de la balise à ajouter aux ressources.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset IDs]</td> 
   <td> <p>Pour chaque ressource à baliser, cliquez sur <strong>[!UICONTROL Add item]</strong>, puis saisissez ou mappez l’ID de la ressource.</p> </td> 
  </tr> 
 </tbody> 
 </table>

#### [!UICONTROL Ajouter des ressources à une collection]

Ce module d’action ajoute une ou plusieurs ressources à une collection.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Bynder] à [!DNL Workfront Fusion], consultez la section <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Bynder] à [!DNL Workfront Fusion] </a>dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collection ID]</td> 
   <td> <p>Saisissez ou mappez l’ID de la collection dans laquelle vous souhaitez ajouter des ressources.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset IDs]</td> 
   <td> <p>Pour chaque ressource à ajouter à la collection, cliquez sur <strong>[!UICONTROL Add item]</strong>, puis saisissez ou mappez l’ID de la ressource.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Appel API personnalisé]

Ce module d’action vous permet d’effectuer un appel personnalisé et authentifié à l’API [!DNL Bynder]. Cela vous permet de créer une automatisation du flux de données qui ne peut pas être réalisée par les autres modules [!DNL Bynder].

Lorsque vous configurez ce module, les champs suivants s’affichent.

Le module renvoie un code de statut, ainsi que les en-têtes et le corps de l’appel API.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Bynder] à [!DNL Workfront Fusion], consultez dans cet article la section <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Bynder] à [!DNL Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Saisir un chemin relatif à <code>https://{your-bynder-domain}/api/{api-version}/</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple : <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion ajoute les en-têtes d’autorisation pour vous.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Ajoutez la requête pour l’appel API sous la forme d’un objet JSON standard.</p> <p>Par exemple : <code>{"name":"something-urgent"}</code></p> </td> 
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

#### [!UICONTROL Télécharger des ressources]

Ce module d’action télécharge une seule ressource.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Bynder] à [!DNL Workfront Fusion], consultez la section <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Bynder] à [!DNL Workfront Fusion] </a>dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td>Saisissez ou mappez l’identifiant de la ressource que vous souhaitez télécharger.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset version]</td> 
   <td> <p>Saisissez ou mappez la version de la ressource que vous souhaitez télécharger. Pour télécharger la dernière version de la ressource, laissez le champ vide.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Lire les métadonnées de ressource]

Ce module d’action lit les métadonnées d’une ressource.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Bynder] à [!DNL Workfront Fusion], consultez la section <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Bynder] à [!DNL Workfront Fusion] </a>dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td>Saisissez ou mappez l’ID de la ressource dont vous souhaitez récupérer les métadonnées.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Sélectionnez les informations que vous souhaitez inclure dans le bundle de sortie pour ce module.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Supprimer une balise des ressources]

Ce module d’action supprime une balise d’une ou de plusieurs ressources

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Bynder] à [!DNL Workfront Fusion], voir <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Bynder] à [!DNL Workfront Fusion] </a>dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tag ID]</td> 
   <td> <p>Saisissez ou mappez l’ID de la balise à supprimer des ressources.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset IDs]</td> 
   <td> <p>Pour chaque ressource dont vous souhaitez supprimer une balise, cliquez sur <strong>[!UICONTROL Add item]</strong>, puis saisissez ou mappez l’ID de la ressource.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Supprimer des ressources de la collection]

Ce module d’action supprime une ou plusieurs ressources d’une collection.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Bynder] à [!DNL Workfront Fusion], consultez la section <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Bynder] à [!DNL Workfront Fusion] </a>dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collection ID]</td> 
   <td> <p>Saisissez ou mappez l’ID de la collection dans laquelle vous souhaitez supprimer des ressources.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset IDs]</td> 
   <td> <p>Pour chaque ressource à supprimer de la collection, cliquez sur <strong>[!UICONTROL Add item]</strong>, puis saisissez ou mappez l’ID de la ressource.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mettre à jour les métadonnées de ressource]

Ce module d’action met à jour les métadonnées d’une ressource existante.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Bynder] à [!DNL Workfront Fusion], consultez la section <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Bynder] à [!DNL Workfront Fusion] </a>dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td>Saisissez ou mappez l’ID de la ressource dont vous souhaitez mettre à jour les métadonnées.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>Sélectionnez les champs pour lesquels vous souhaitez saisir des informations, puis saisissez ou mappez les informations avec lesquelles vous souhaitez mettre à jour les métadonnées dans ces champs. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Metaproperties]</p> </td> 
   <td>Sélectionnez les options à mettre à jour, puis saisissez ou mappez les informations dans ces propriétés. Les propriétés des métadonnées sont des informations sur la ressource qui ne représentent pas de champs spécifiques dans la ressource.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Charger des ressources]

Ce module d’action charge une seule ressource.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Bynder] à [!DNL Workfront Fusion], consultez dans cet article la section <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Bynder] à [!DNL Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Save as]</td> 
   <td> <p>Sélectionnez le mode d’enregistrement du fichier que vous téléchargez.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL New asset]</strong> </p> <p>Sélectionnez les champs et les propriétés des métadonnées pour lesquels vous souhaitez saisir des informations, puis saisissez les informations dans ces champs.</p> <p>Saisissez ou mappez l’identifiant de la marque que vous souhaitez utiliser pour la ressource chargée.</p> </li> 
     <li> <p><strong>[!UICONTROL New asset version]</strong> </p> <p>Saisissez l’identifiant de la ressource pour laquelle vous chargez une nouvelle version.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Chargement de fichier asynchrone]</td> 
   <td>Activez cette option lors du chargement de fichiers volumineux. Cela empêche les fichiers volumineux de bloquer l’exécution du scénario.</td> 
  </tr> 
 </tbody> 
</table>

### Recherches

* [[!UICONTROL Répertorier les enregistrements]](#list-record)
* [[!UICONTROL Rechercher dans Assets]](#search-assets)

#### [!UICONTROL Répertorier les enregistrements]

Ce module de recherche récupère tous les éléments d’un type spécifique.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Bynder] à [!DNL Workfront Fusion], consultez dans cet article la section <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Bynder] à [!DNL Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement que vous souhaitez répertorier.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Read all collections]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL Read information about all tags]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL Read all assets of a collection]</strong> </p> <p>Saisissez ou mappez l’identifiant de la collection dont vous souhaitez répertorier les ressources.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Sélectionnez les champs que vous souhaitez inclure dans la sortie du module.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal de ressources que le module doit renvoyer au cours de chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Rechercher dans Assets]

Ce module de recherche permet de rechercher des ressources en fonction des critères que vous fournissez.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Bynder] à [!DNL Workfront Fusion], consultez dans cet article la section <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Bynder] à [!DNL Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search criteria]</td> 
   <td> <p>Saisissez les critères de recherche. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Field]</strong> </p> <p>Sélectionnez le champ que vous souhaitez utiliser dans votre recherche.</p> </li> 
     <li> <p><strong>[!UICONTROL Logical Operator]</strong> </p> <p>Sélectionnez l’opérateur que vous souhaitez utiliser dans votre recherche.</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Saisissez ou mappez la valeur à rechercher dans le champ sélectionné. Le type de valeur doit être identique au type de données du champ sélectionné. </p> <p>Pour plus d’informations sur les types de données, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">Types de données d’élément</a>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Result set]</td> 
   <td>Indiquez si vous souhaitez renvoyer la première ressource correspondante ou toutes les ressources correspondantes.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort by]</td> 
   <td> <p>Sélectionnez le champ en fonction duquel vous souhaitez effectuer un tri.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort Direction]</td> 
   <td> <p>Indiquez si vous souhaitez trier par ordre croissant ou décroissant.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Sélectionnez les champs que vous souhaitez inclure dans la sortie du module.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal de ressources que le module doit renvoyer au cours de chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Déclencheurs

#### [!UICONTROL Surveiller les ressources]

Lorsqu’une ressource est créée ou mise à jour, ce module de déclenchement lance un scénario.

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Bynder] à [!DNL Workfront Fusion], consultez dans cet article la section <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Bynder] à [!DNL Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">Type d’événement</td>
    <td>Choisissez si vous souhaitez démarrer le scénario lorsqu’une nouvelle ressource est créée ou lorsqu’une ressource existante est mise à jour.</td>
  </tr> 
  <tr>
     <td role="rowheader">[!UICONTROL Collections]</td>
   <td> <p>Sélectionnez la collection dont vous souhaitez surveiller les nouvelles ressources. Pour surveiller toutes les collections, laissez ce champ vide.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">Sorties</td>
    <td>Sélectionnez les champs que vous souhaitez inclure dans la sortie.</td>
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Limit]</td>

<td> <p>Saisissez le nombre maximum d’enregistrements que le module doit renvoyer au cours de chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>
