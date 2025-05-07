---
title: Modules Adobe I/O Events
description: Avec les modules Adobe I/O Events, vous pouvez démarrer un scénario Adobe Workfront Fusion en fonction des événements de vos applications Adobe.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: b2229f3e-a2a7-4b07-8ead-a37d193c2ec7
source-git-commit: 983ce043afbcc44ee8af2dfcd46738f170a2b257
workflow-type: tm+mt
source-wordcount: '969'
ht-degree: 35%

---

# Modules Adobe I/O Events

Avec les modules Adobe I/O Events, vous pouvez démarrer un scénario Adobe Workfront Fusion en fonction d’événements dans les comptes et services Adobe qui ne disposent pas d’un connecteur Workfront Fusion dédié.

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

Avant de pouvoir utiliser le connecteur Adobe I/O Events, vous devez vous assurer que les conditions préalables suivantes sont remplies :

* Vous devez disposer d’un compte Adobe actif.

## Informations sur l’API Adobe I/O Events

Le connecteur Adobe I/O Events utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td>https://api.adobe.io/events</td> 
  </tr>
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.6.7</td> 
  </tr>
 </tbody> 
 </table>

## Création d’une connexion à Adobe I/O Events

Pour créer une connexion pour vos modules Adobe I/O Events :

1. Cliquez sur Ajouter en regard de la zone Connexion .

1. Remplissez les champs suivants :

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">Nom de la connexion</td>
        <td>
          <p>Saisissez un nom pour cette connexion.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Environnement</td>
        <td>
          <p>Choisissez si vous souhaitez vous connecter à un environnement de production ou hors production.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Type</td>
        <td>
          <p>Choisissez si vous souhaitez vous connecter à un compte de service ou à un compte personnel.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Portées supplémentaires</td>
        <td>Pour ajouter des portées supplémentaires, cliquez sur <b>Ajouter un élément</b> et saisissez la portée.</td>
      </tr>
      <tr>
        <td role="rowheader">ID client</td>
        <td>Saisissez votre identifiant client Adobe. Vous trouverez cette information dans la section Informations d’identification du Adobe Developer Console</td>
      </tr>
      <tr>
        <td role="rowheader">Clé secrète client</td>
        <td>Saisissez votre clé secrète client Adobe. Vous trouverez cette information dans la section Informations d’identification du Adobe Developer Console</td>
      </tr>
      </tr>
        <tr>
        <td role="rowheader">ID d’organisation du client</td>
        <td>Saisissez votre ID d’organisation client. Elle se trouve dans l’URL d’identification du projet : <code>https://developer.adobe.com/console/projects/{consumer org ID}/ {project ID}/credentials/{credential ID}/details</code></td>
      </tr>
      <tr>
        <td role="rowheader">Identifiant d’identification</td>
        <td>Saisissez vos informations d’identification. Elle se trouve dans l’URL d’identification du projet : <code>https://developer.adobe.com/console/projects/{consumer org ID}/ {project ID}/credentials/{credential ID}/details</code></td>
      </tr>
      <tr>
        <td role="rowheader">Identifiant de l’organisation IMS</td>
        <td>Saisissez votre ID d’organisation Adobe. Vous trouverez cette information dans la section Informations d’identification du Adobe Developer Console</td>
      </tr>
        <tr>
        <td role="rowheader">ID de projet</td>
        <td>Saisissez votre ID de projet. Elle se trouve dans l’URL d’identification du projet : <code>https://developer.adobe.com/console/projects/{consumer org ID}/ {project ID}/credentials/{credential ID}/details</code></td>
      </tr>
      <tr>
        <td role="rowheader">WORKSPACE ID</td>
        <td>Pour afficher l’identifiant Workspace de votre projet, téléchargez les détails du projet depuis la page d’aperçu du projet dans Adobe Developer Console. </td>
      </tr>
    </tbody>
    </table>

1. Cliquez sur **Continuer** pour enregistrer la connexion et revenir au module.

## Modules Adobe I/O Events et leurs champs

Lorsque vous configurez les modules [!DNL Adobe I/O Events], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Adobe I/O Events] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Déclencheurs](#triggers)
* [Actions](#actions)
* [Recherches](#searches)

### Déclencheurs

<!--Becky start here-->

#### Créer un enregistrement d’événement

Ce module d’action utilise un webhook pour créer une description d’événement. Vous pouvez configurer un webhook ici. Si vous utilisez un webhook existant, les champs de ce module sont en lecture seule.

Pour créer un webhook :

1. Cliquez sur **Ajouter** en regard du champ Webhook.
1. Remplissez les champs suivants :

   <table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[!UICONTROL Webhook name]</td>
        <td>Saisissez le nom de ce webhook.</td>
       </tr>
       <tr>
         <td role="rowheader">[!UICONTROL Connection]</td>
        <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe I/O Events], voir <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >Créer une connexion à [!DNL Adobe I/O Events]</a> dans cet article.</td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Webhook description]
         </td>
         <td>
           Saisissez une description pour ce webhook.
        </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Fournisseur d’événements]
         </td>
         <td>
           Sélectionnez le produit ou le compte à partir duquel vous souhaitez créer des événements.
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Event type]
         </td>
         <td>
           Sélectionnez les événements que le webhook doit regarder. Le scénario se déclenche lorsque ces événements se produisent.
         </td>
       </tr>
     </tbody>
   </table>

1. Cliquez sur Enregistrer pour enregistrer le webhook et revenir au module .

### Actions

#### Récupérer tous les événements d’un journal

Ce module de recherche récupère tous les événements d’un enregistrement dans un journal.

<table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[!UICONTROL Connection]</td>
        <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe I/O Events], voir <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >Créer une connexion à [!DNL Adobe I/O Events]</a> dans cet article.</td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Registration ID]
         </td>
         <td>
           Sélectionnez l’enregistrement pour lequel vous souhaitez récupérer les événements.
        </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Maximum number of returned records]
         </td>
         <td>
              Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario. 
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Renvoyer les événements qui se produisent après]
         </td>
         <td>
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Seek]
         </td>
         <td>
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Latest]
         </td>
         <td>
         Activez cette option pour renvoyer l’événement le plus récent.
         </td>
       </tr>
     </tbody>
   </table>

#### Effectuer un appel API personnalisé.

Ce module d’action effectue un appel API personnalisé à l’API [!DNL Adobe I/O Events]

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
     <td role="rowheader">[!UICONTROL Connection]</td>
        <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe I/O Events], voir <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >Créer une connexion à [!DNL Adobe I/O Events]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Path]</p>
      </td>
      <td>
        <p>Saisir un chemin relatif à <code>https://api.adobe.io/events</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
      <td>
  <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p>  
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p>
        <p>Par exemple, <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion ajoute automatiquement des en-têtes d’autorisation et des en-têtes x-api-key.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Saisissez la chaîne de requête.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lors de l’utilisation d’instructions conditionnelles telles que <code>if</code> dans votre fichier JSON, placez les guillemets autour de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

### Recherches

#### Obtention des identifiants de fournisseur et d’événement

Ce module de recherche obtient les identifiants Adobe I/O Events pour le fournisseur et les événements spécifiés.

<table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[!UICONTROL Connection]</td>
        <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe I/O Events], voir <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >Créer une connexion à [!DNL Adobe I/O Events]</a> dans cet article.</td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Fournisseur d’événements]
         </td>
         <td>
           Sélectionnez le fournisseur pour lequel vous souhaitez récupérer l’identifiant.
        </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Event type]
         </td>
         <td>
              Sélectionnez les événements pour lesquels vous souhaitez fournir des identifiants. Les événements sont disponibles en fonction du fournisseur d’événement. 
         </td>
       </tr>
     </tbody>
   </table>

<!--

Watch Events

This trigger module starts a scenario when an event occurs in the chosen Adobe product or service.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">Webhook</td> 
   <td><p>Select the webhook that you want to use for this trigger, or add a new webhook. </p><p>To add a new webhook, <ol><li>Click <b>Add</b> next to the webhook field.</li><li>Enter the following: <ul><li>A name for the webhook</li><li>The connection that you want to use for this webhook</li><li>The source of the events you want to watch</li></ul></li><li>Click <b>Save</b> to save the webhook and return to the module. </td> 
   </tr> 
   </tbody> 
</table>

-->
