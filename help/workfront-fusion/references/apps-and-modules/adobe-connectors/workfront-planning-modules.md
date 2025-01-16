---
title: Modules Adobe Workfront Planning
description: Avec les modules  [!DNL Adobe Workfront Planning] , vous pouvez démarrer un [!DNL Adobe Workfront Fusion] scénario basé sur des événements dans votre compte  [!DNL Adobe] Workfront Planning, créer, lire ou mettre à jour des contrats et d'autres enregistrements, rechercher des enregistrements à l'aide de critères que vous avez définis et charger des documents.
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
source-git-commit: cf2a4515ecd5e239e3370a6a0a3ffe70ecce3770
workflow-type: tm+mt
source-wordcount: '1100'
ht-degree: 70%

---

# Modules [!DNL Adobe Workfront Planning]

Avec les modules [!DNL Adobe Workfront Planning], vous pouvez déclencher un scénario lorsque des événements se produisent dans Workfront Planning. Vous pouvez également créer, lire, mettre à jour et supprimer des enregistrements, ou effectuer un appel API personnalisé vers votre compte [!DNL Adobe Workfront Planning].

## Conditions d’accès

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] formule*</td>
  <td> <p>[!UICONTROL Pro] ou une version ultérieure</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licence*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licence**</td> 
   <td>
   <p>Exigences de licence actuelles : aucune exigence de licence [!DNL Workfront Fusion] requise.</p>
   <p>Ou</p>
   <p>Ancienne exigence de licence : [!UICONTROL [!DNL Workfront Fusion] pour l’automatisation et l’intégration du travail] </p>
   </td>  
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Exigences actuelles du produit : si vous disposez du plan de [!DNL Adobe Workfront] [!UICONTROL Select] ou [!UICONTROL Prime], votre entreprise doit acheter du [!DNL Adobe Workfront Fusion] et [!DNL Adobe Workfront] utiliser les fonctionnalités décrites dans cet article. [!DNL Workfront Fusion] est inclus dans le plan de [!DNL Workfront] [!UICONTROL Ultimate].</p>
   <p>Ou</p>
   <p>Exigences liées aux produits hérités : votre entreprise doit acheter [!DNL Adobe Workfront Fusion] ainsi qu’[!DNL Adobe Workfront] pour utiliser la fonctionnalité décrite dans cet article.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Pour connaître la formule, le type de licence ou l’accès dont vous disposez, contactez votre équipe d’administration [!DNL Workfront].

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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

## Créer une connexion à [!DNL Adobe Workfront Planning]

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
          <td role="rowheader">[!UICONTROL Authentication URL]<p>(Facultatif)</p></td>
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
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Workfront Planning], voir <a href="#create-a-connection-to-adobe-workfront planning" class="MCXref xref" >Créer une connexion à [!DNL Adobe Workfront Planning]</a> dans cet article.</td>
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
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Workfront Planning], voir <a href="#create-a-connection-to-adobe-workfront planning" class="MCXref xref" >Créer une connexion à [!DNL Adobe Workfront Planning]</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type ID]</p>
      </td>
      <td>Saisissez ou mappez l’ID du champ à supprimer.</td> 
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
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Workfront Planning], voir <a href="#create-a-connection-to-adobe-workfront planning" class="MCXref xref" >Créer une connexion à [!DNL Adobe Workfront Planning]</a> dans cet article.</td>
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
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP dans [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
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
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre JSON, placez les guillemets à l’extérieur de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

<!--
### Searches

#### Search records

This action module retrieves a list of records based on criteria you specify.

-->

### Non catégorisé


#### Créer un enregistrement

Cette action crée un enregistrement unique dans Workfront Planning.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Workfront Planning], voir <a href="#create-a-connection-to-adobe-workfront planning" class="MCXref xref" >Créer une connexion à [!DNL Adobe Workfront Planning]</a> dans cet article.</td>
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
      <td>Ces champs sont basés sur le type d’enregistrement que vous avez sélectionné.</td> 
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
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Workfront Planning], voir <a href="#create-a-connection-to-adobe-workfront planning" class="MCXref xref" >Créer une connexion à [!DNL Adobe Workfront Planning]</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record ID]</p>
      </td>
      <td>Saisissez ou mappez l’ID de l’enregistrement que vous souhaitez supprimer.</td> 
      </tr>
  </tbody>
</table>

<!--

### Get all records

This action module retrieves all records from an [!DNL Adobe Workfront Planning] account.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>For instructions on creating a connection to [!DNL Adobe Workfront Planning], see <a href="#create-a-connection-to-adobe-workfront planning" class="MCXref xref" >Create a connection to [!DNL Adobe Workfront Planning]</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximum number of returned records]</p>
      </td>
      <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td> 
      </tr>
  </tbody>
</table>

-->

### Obtenir un enregistrement

Ce module d’action récupère un seul enregistrement d’[!DNL Adobe Workfront Planning] spécifié par son ID.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Workfront Planning], voir <a href="#create-a-connection-to-adobe-workfront planning" class="MCXref xref" >Créer une connexion à [!DNL Adobe Workfront Planning]</a> dans cet article.</td>
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
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Workfront Planning], voir <a href="#create-a-connection-to-adobe-workfront planning" class="MCXref xref" >Créer une connexion à [!DNL Adobe Workfront Planning]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Sélectionnez ou mappez l’espace de travail qui contient les enregistrements que vous souhaitez récupérer.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>Sélectionnez le type d’enregistrement que vous souhaitez récupérer.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximum number of returned records]</p>
      </td>
      <td>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</td> 
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
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Workfront Planning], voir <a href="#create-a-connection-to-adobe-workfront planning" class="MCXref xref" >Créer une connexion à [!DNL Adobe Workfront Planning]</a> dans cet article.</td>
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
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Workfront Planning], voir <a href="#create-a-connection-to-adobe-workfront planning" class="MCXref xref" >Créer une connexion à [!DNL Adobe Workfront Planning]</a> dans cet article.</td>
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
      <td>Ces champs sont basés sur le type d’enregistrement que vous avez sélectionné.</td> 
      </tr>
     <tr>
  </tbody>
</table>
