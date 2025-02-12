---
title: Modules Adobe Workfront Planning
description: Avec les modules  [!DNL Adobe Workfront Planning] , vous pouvez démarrer un [!DNL Adobe Workfront Fusion] scénario basé sur des événements dans votre compte  [!DNL Adobe] Workfront Planning, créer, lire ou mettre à jour des contrats et d'autres enregistrements, rechercher des enregistrements à l'aide de critères que vous avez définis et charger des documents.
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
source-git-commit: 06ba97ec4245f9620f013711df9a77b76abb20be
workflow-type: tm+mt
source-wordcount: '1395'
ht-degree: 57%

---

# Modules [!DNL Adobe Workfront Planning]

Avec les modules [!DNL Adobe Workfront Planning], vous pouvez déclencher un scénario lorsque des événements se produisent dans Workfront Planning. Vous pouvez également créer, lire, mettre à jour et supprimer des enregistrements, ou effectuer un appel API personnalisé vers votre compte [!DNL Adobe Workfront Planning].

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
   <p>Actuel : aucune exigence de licence Workfront Fusion.</p>
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

## Créer une connexion à [!DNL Adobe Workfront Planning] {#create-a-connection-to-adobe-workfront-planning}

Vous pouvez créer une connexion à votre compte [!DNL Workfront Planning] directement depuis l’intérieur d’un module [!DNL Workfront Fusion].

1. Dans n’importe quel module de [!DNL Adobe Workfront Planning], cliquez sur **[!UICONTROL Add]** en regard de la zone Connexion .

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
          <td>Choisissez si vous souhaitez vous connecter à un compte de service ou à un compte personnel.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client ID]<p>(Facultatif)</p></td>
          <td>Saisissez votre [!UICONTROL Client ID] de [!DNL Adobe]. Pour plus d'informations, consultez la section [!UICONTROL Credentials details] de la [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]<p>(Facultatif)</p></td>
          <td>Saisissez votre [!UICONTROL Client Secret] de [!DNL Adobe]. Pour plus d'informations, consultez la section [!UICONTROL Credentials details] de la [!DNL Adobe Developer Console].
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Authentication URL]</td>
          <td>Saisissez l’URL que votre instance de Workfront utilisera pour authentifier cette connexion. <p>La valeur par défaut est <code>https://oauth.my.workfront.com/integrations/oauth2</code>.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Host prefix]</td>
          <td>Saisissez votre préfixe hôte.<p>La valeur par défaut est <code>origin-</code>.</p>
        </tr>
      </tbody>
    </table>

1. Cliquez sur **[!UICONTROL Continue]** pour enregistrer la connexion et revenir au module .

## Modules [!DNL Adobe Workfront Planning] et leurs champs

Lorsque vous configurez des modules Workfront, Workfront Fusion affiche les champs répertoriés ci-dessous. D’autres champs Workfront peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).


![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Déclencheurs](#triggers)
* [Actions](#actions)
* [Recherches](#searches)
* [Non catégorisé](#uncategorized)

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
      <td> <p>Vous pouvez définir des filtres pour ne surveiller que les enregistrements qui répondent aux critères sélectionnés.</p> <p>Pour chaque filtre, saisissez le champ que le filtre doit évaluer, l’opérateur et la valeur que le filtre doit autoriser. Vous pouvez utiliser plusieurs filtres en ajoutant des règles ET.</p> <p>Note : vous ne pouvez pas modifier les filtres dans les webhooks [!DNL Workfront] existants. Pour configurer différents filtres pour les abonnements aux événements [!DNL Workfront], supprimez le webhook actuel et créez-en un nouveau.</p> <p>Pour plus d’informations sur les filtres d’événement, consultez la section <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">Filtres d’abonnement aux événements dans les modules [!DNL Workfront] &gt; [!UICONTROL Watch Events]</a> de l’article Modules Workfront .</p> </td> 
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

#### Effectuer un appel API personnalisé.

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
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p>
        <p>Par exemple, <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] Ajoute automatiquement des en-têtes d’autorisation.</p>
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
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lors de l’utilisation d’instructions conditionnelles telles que <code>if</code> dans votre fichier JSON, placez les guillemets autour de l’instruction conditionnelle.</p> 
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
        <p>[!UICONTROL Condition for filters]</p>
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


### Non catégorisé


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
