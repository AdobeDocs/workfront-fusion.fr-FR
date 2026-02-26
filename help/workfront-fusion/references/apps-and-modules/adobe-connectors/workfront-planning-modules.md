---
title: Modules Adobe Workfront Planning
description: Avec les modules  [!DNL Adobe Workfront Planning] , vous pouvez lancer un scénario Adobe Workfront Fusion en fonction des événements de votre compte de planification  [!DNL Adobe] Workfront, créer, lire ou mettre à jour des contrats et d’autres enregistrements, rechercher des enregistrements à l’aide des critères que vous avez définis et charger des documents.
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
source-git-commit: a58a6c25751eb10365508c06ab1571ce7652d0c8
workflow-type: tm+mt
source-wordcount: '1992'
ht-degree: 69%

---

# Modules [!DNL Adobe Workfront Planning]

Avec les modules [!DNL Adobe Workfront Planning], vous pouvez déclencher un scénario lorsque des événements se produisent dans Workfront Planning. Vous pouvez également créer, lire, mettre à jour et supprimer des enregistrements, ou effectuer un appel API personnalisé vers votre compte [!DNL Adobe Workfront Planning].

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
   <td role="rowheader">Produit</td> 
   <td>
   <p>Si votre organisation dispose d’un package Workfront Select ou Prime qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acquérir Adobe Workfront Fusion.</li></ul>
   </td>
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation Workfront](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Conditions préalables

Pour accéder à Workfront Planning, vous devez disposer des éléments suivants :

* Un nouveau package et une nouvelle licence Workfront. Workfront Planning n’est pas disponible pour les packages ou licences Workfront hérités.
* Un package Workfront Planning.
* L’instance de Workfront de votre organisation doit être intégrée à l’expérience unifiée Adobe.

## Informations sur l’API Adobe Workfront Planning

Le connecteur Adobe Workfront Planning utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td>https://{{connection.host}}/maestro/api/{{common.maestroApiVersion}}/</td> 
  </tr>
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.13.7</td> 
  </tr>
 </tbody> 
 </table>

## Connexion de Workfront Planning à Workfront Fusion

Le connecteur Workfront Planning utilise OAuth 2.0 pour se connecter à Workfront Planning.

Vous pouvez créer une connexion à votre compte Workfront Planning directement depuis un module Workfront Planning Fusion.

* [Se connecter à Workfront Planning à l’aide de l’ID client et du secret client](#connect-to-workfront-planning-using-client-id-and-client-secret)
* [Connexion à Workfront Planning à l’aide d’une connexion serveur à serveur](#connect-to-workfront--planning-using-a-server-to-server-connection)

### Se connecter à Workfront Planning à l’aide de l’ID client et du secret client

1. Dans un module Adobe Workfront Planning, cliquez sur **Ajouter** en regard du champ Connexion .
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
          <p>Sélectionnez <b>Connexion d’authentification Adobe Workfront</b>.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Saisissez un nom pour la nouvelle connexion.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Saisissez votre ID client Workfront. Vous le trouverez dans la zone Applications OAuth2 de la zone Configuration dans Workfront. Ouvrez l’application spécifique à laquelle vous vous connectez pour afficher l’ID client.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Saisissez votre secret client Workfront. Vous le trouverez dans la zone Applications OAuth2 de la zone Configuration dans Workfront. Si vous ne disposez pas d’un secret client pour votre application OAuth2 dans Workfront, vous pouvez en générer un autre. Pour obtenir des instructions, consultez la documentation de Workfront.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Authentication URL]</td>
        <td>Vous pouvez conserver la valeur par défaut ou saisir l’URL de votre instance Workfront, suivie de <code>/integrations/oauth2</code>. <p>Exemple : <code>https://mydomain.my.workfront.com/integrations/oauth2</code></p></td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Host prefix]</td>
        <td>Dans la plupart des cas, cette valeur doit être <code>origin</code>.
      </tr>
    </tbody>
    </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour enregistrer la connexion et revenir au module.

   Si vous n’êtes pas connecté à Workfront Planning, vous êtes redirigé vers un écran de connexion. Une fois la connexion effectuée, vous pouvez autoriser la connexion.

>[!NOTE]
>
>* Les connexions OAuth 2.0 à l’API Workfront ne dépendent plus des clés API.
>* Pour créer une connexion à un environnement Sandbox Workfront, vous devez créer une application OAuth2 dans cet environnement, puis utiliser l’ID client et le secret client générés par cette application dans la connexion.

### Connexion à Workfront Planning à l’aide d’une connexion serveur à serveur

1. Dans un module Adobe Workfront Planning, cliquez sur **Ajouter** en regard du champ Connexion .
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
          <p>Sélectionnez <b>Connexion Adobe Workfront de serveur à serveur</b>.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Saisissez un nom pour la nouvelle connexion.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Instance name]</td>
        <td>
          <p>Saisissez le nom de votre instance, également appelée domaine.</p><p>Exemple : si votre URL est <code>https://example.my.workfront.com</code>, saisissez <code>example</code>.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Instance lane]</td>
        <td>
          <p>Indiquez le type d’environnement auquel cette connexion doit se connecter.</p><p>Exemple : si votre URL est <code>https://example.my.workfront.com</code>, saisissez <code>my</code>.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Saisissez votre ID client Workfront. Vous le trouverez dans la zone Applications OAuth2 de la zone Configuration dans Workfront. Ouvrez l’application spécifique à laquelle vous vous connectez pour afficher l’ID client.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Saisissez votre secret client Workfront. Vous le trouverez dans la zone Applications OAuth2 de la zone Configuration dans Workfront. Si vous ne disposez pas d’un secret client pour votre application OAuth2 dans Workfront, vous pouvez en générer un autre. Pour obtenir des instructions, consultez la documentation de Workfront.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Scopes]</td>
        <td>Saisissez toutes les étendues applicables à cette connexion.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Host prefix]</td>
        <td>Dans la plupart des cas, cette valeur doit être <code>origin</code>.
      </tr>
    </tbody>
    </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour enregistrer la connexion et revenir au module.

   Si vous n’êtes pas connecté à Workfront Planning, vous êtes redirigé vers un écran de connexion. Une fois la connexion effectuée, vous pouvez autoriser la connexion.

>[!NOTE]
>
>* Les connexions OAuth 2.0 à l’API Workfront ne dépendent plus des clés API.
>* Pour créer une connexion à un environnement Sandbox Workfront, vous devez créer une application OAuth2 dans cet environnement, puis utiliser l’ID client et le secret client générés par cette application dans la connexion.


## Modules [!DNL Adobe Workfront Planning] et leurs champs

Lorsque vous configurez les modules Workfront, Workfront Fusion affiche les champs répertoriés ci-dessous. Des champs Workfront supplémentaires peuvent s’afficher, selon votre niveau d’accès dans l’application ou le service, par exemple. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, consultez [Mappage d’informations d’un module à l’autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).


![Bouton (bascule) de mappage](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Déclencheurs](#triggers)
* [Actions](#actions)
* [Recherches](#searches)
* [Non classée](#uncategorized)

### Déclencheurs

#### Surveiller les événements

Ce module de déclenchement démarre un scénario lorsqu’un enregistrement, un type d’enregistrement ou un espace de travail est créé, mis à jour ou supprimé dans Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Webhook]</td>
      <td>Sélectionnez le webhook à utiliser ou cliquez sur Ajouter pour en créer un nouveau.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Workfront Planning], voir <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Créer une connexion à [!DNL Adobe Workfront Planning]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Object type]</td>
      <td>Indiquez si vous souhaitez surveiller des enregistrements, des types d’enregistrement ou des espaces de travail.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL State]</td>
      <td>Indiquez si vous souhaitez surveiller l’ancien ou le nouvel état.<ul><li><p><b>[!UICONTROL New state]</b></p><p>Déclenchez un scénario lorsque l’enregistrement <b>prend</b> une valeur donnée.</p></li><li><p><b>[!UICONTROL Old state]</b></p><p>Déclenchez un scénario lorsque l’enregistrement <b>quitte</b> une valeur donnée.</p></li></ul></td> 
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Si vous observez des enregistrements, sélectionnez le Workspace que vous souhaitez observer pour les enregistrements.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>Si vous observez des enregistrements, sélectionnez le type d’enregistrement à observer.</td>
    </tr>
    </tr>
     <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL Events filters]</p> </td> 
      <td> <p>Vous pouvez définir des filtres pour ne surveiller que les enregistrements qui répondent aux critères sélectionnés.</p> <p>Pour chaque filtre, saisissez le champ que le filtre doit évaluer, l’opérateur et la valeur que le filtre doit autoriser. Vous pouvez utiliser plusieurs filtres en ajoutant des règles ET.</p> <p>Remarque : vous ne pouvez pas modifier les filtres dans les Webhooks Workfront existants. Pour configurer différents filtres pour les abonnements aux événements Workfront, supprimez le webhook actuel et créez-en un nouveau.</p> <p>Pour plus d’informations sur les filtres d’événement, consultez la section <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref"> Filtres d’abonnement aux événements dans les modules Workfront &gt; [!UICONTROL Watch Events]</a> dans l’article Modules Workfront .</p> </td> 
     </tr> 
    <tr>
      <td role="rowheader">[!UICONTROL Objects to watch]</td>
      <td>Indiquez si vous souhaitez surveiller les enregistrements. nouveaux, mis à jour, nouveaux et mis à jour ou supprimés.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Exclude updates made by this connection]</p>
      </td>
      <td>Activez cette option pour empêcher le déclenchement du scénario lorsqu’une modification est effectuée par la connexion utilisée par ce module. Cela empêche qu’une autre instance du scénario soit déclenchée si ce scénario exécute une action de déclenchement.</td> 
      </tr>
  </tbody>
</table>

### Actions

* [Supprimer un type d’enregistrement](#delete-a-record-type)
* [Effectuer un appel d’IA personnalisé](#make-a-custom-api-call)

#### Supprimer un type d’enregistrement

Ce module d&#39;action supprime un seul type d&#39;enregistrement dans Workfront Planning par son identifiant.

>[!WARNING]
>
>La suppression d’un type d’enregistrement dans Workfront Planning entraîne la suppression de tous les enregistrements de la table des types d’enregistrement.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Workfront Planning], voir <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Créer une connexion à [!DNL Adobe Workfront Planning]</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type ID]</p>
      </td>
      <td>Saisissez ou mappez l’identifiant du type d’enregistrement à supprimer.</td> 
      </tr>
  </tbody>
</table>

#### Effectuer un appel API personnalisé

Ce module lance un appel API personnalisé à l’API [!DNL Adobe Workfront Planning].

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Workfront Planning], voir <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Créer une connexion à [!DNL Adobe Workfront Planning]</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>Saisir un chemin relatif à <code>https://(YOUR_WORKFRONT_DOMAIN)/maestro/api/</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, consultez <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p>
        <p>Par exemple, <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion ajoute automatiquement des en-têtes d’autorisation.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Pour chaque paire clé/valeur à ajouter à la chaîne de requête, cliquez sur <b>Ajouter un élément</b> et saisissez la clé et la valeur.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre JSON, placez les guillemets à l’extérieur de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>


### Recherches

#### Rechercher des enregistrements

Ce module d’action récupère une liste d’enregistrements en fonction des critères que vous spécifiez.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Workfront Planning], voir <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Créer une connexion à [!DNL Adobe Workfront Planning]</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>Saisissez ou mappez le Workspace contenant les enregistrements que vous souhaitez rechercher.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type]</p>
      </td>
      <td>Sélectionnez le type d’enregistrement à rechercher.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record Fields]</p>
      </td>
      <td>Pour chaque champ à utiliser dans votre recherche, localisez ce champ, sélectionnez l’opérateur et saisissez ou mappez la valeur à rechercher. Les champs sont disponibles en fonction du type d’enregistrement sélectionné.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Condition pour les filtres]</p>
      </td>
      <td>Sélectionnez la condition de vos filtres :<ul><li><b>ET</b><p>Le module renvoie les enregistrements qui respectent <b>toutes</b> les valeurs de champ que vous avez sélectionnées.</p></li><li><b>OU</b><p>Le module renvoie les enregistrements qui correspondent à l’<b>une </b> valeurs de champ que vous avez sélectionnées.</p></li></ul></td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Limit]</p>
      </td>
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
      </tr>
  </tbody>
</table>


### Non classée


#### Créer un enregistrement

Cette action crée un enregistrement unique dans Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Workfront Planning], voir <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Créer une connexion à [!DNL Adobe Workfront Planning]</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type ID]</p>
      </td>
      <td>Saisissez ou mappez le type d’enregistrement que vous souhaitez créer. Les types d’enregistrements disponibles dépendent de votre compte Workfront Planning.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Autres champs</p>
      </td>
      <td>Saisissez les valeurs que vous souhaitez attribuer au nouvel enregistrement. Ces champs sont basés sur le type d’enregistrement que vous avez sélectionné.</td> 
      </tr>
     <tr>
  </tbody>
</table>

### Supprimer un enregistrement

Ce module d&#39;action supprime l&#39;enregistrement spécifié dans Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Workfront Planning], voir <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Créer une connexion à [!DNL Adobe Workfront Planning]</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record ID]</p>
      </td>
      <td>Saisissez ou mappez l’ID de l’enregistrement que vous souhaitez supprimer.</td> 
      </tr>
  </tbody>
</table>

### Obtenir un enregistrement

Ce module d’action récupère un seul enregistrement d’[!DNL Adobe Workfront Planning] spécifié par son ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Workfront Planning], voir <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Créer une connexion à [!DNL Adobe Workfront Planning]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record ID]</td>
      <td>Saisissez ou mappez l’ID de l’enregistrement que vous souhaitez récupérer.</td>
    </tr>
  </tbody>
</table>

### Obtenir des enregistrements par type d’enregistrement

Ce module d’action récupère tous les enregistrements du type spécifié.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Workfront Planning], voir <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Créer une connexion à [!DNL Adobe Workfront Planning]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Sélectionnez ou mappez l’espace de travail qui contient les enregistrements que vous souhaitez récupérer.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>Sélectionnez le type d’enregistrement que vous souhaitez récupérer.</td>
    </tr>
     <!--<tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximum number of returned records]</p>
      </td>
      <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td> -->
  </tbody>
</table>

### Obtenir des types d’enregistrement

Ce module d’action récupère une liste de types d’enregistrement dans un compte [!DNL Adobe Workfront Planning].

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Workfront Planning], voir <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Créer une connexion à [!DNL Adobe Workfront Planning]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Sélectionnez ou mappez l’espace de travail contenant les types d’enregistrements à récupérer.</td>
    </tr>
  </tbody>
</table>

### Mettre à jour l’enregistrement

Cette action met à jour un seul enregistrement dans Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Workfront Planning], voir <a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >Créer une connexion à [!DNL Adobe Workfront Planning]</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record ID]</p>
      </td>
      <td>Saisissez ou mappez le type d’enregistrement que vous souhaitez mettre à jour. Les types d’enregistrements disponibles dépendent de votre compte Workfront Planning.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Autres champs</p>
      </td>
      <td>Saisissez les nouvelles valeurs que vous souhaitez attribuer à l'enregistrement. Ces champs sont basés sur le type d’enregistrement que vous avez sélectionné.</td> 
      </tr>
     <tr>
  </tbody>
</table>


## Utiliser JSONata pour la répartition lisible des `record-types`

L’expression JSONata suivante crée une sortie lisible par l’utilisateur de la requête Planning qui vous donne la répartition des types d’enregistrements. Le nom du type d’enregistrement, les noms des champs et les noms des options de champ (le cas échéant) sont ainsi lisibles par un nom et le reste de la structure reste intact.

```
(
    $s0 := ({"data":$ ~> | fields | {"options":(options){name:$}} |});
    $s1 := ({"data":$s0.data ~> | **.fields | {"options_name":(options.*){displayName:$}} | });
    $s2 := $s1 ~> | data | {"fields":(fields){displayName:$}} |; 
    $s2.data{displayName:$}
)
```

Pour plus d’informations sur l’utilisation des modules JSONata, voir [Modules JSONata](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/jsonata-module.md).

