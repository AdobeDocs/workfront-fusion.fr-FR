---
title: Modules Finances et opérations de Microsoft Dynamics 365
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent Microsoft Dynamics 365 Finance and Operations et les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: 96f8d4f1-f97b-4da8-8d82-83cccb54ec68
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1021'
ht-degree: 24%

---

# [!DNL Microsoft Dynamics 365 Finance and Operations modules]

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent [!DNL Microsoft Dynamics 365] et les connecter à plusieurs applications et services tiers.

>[!NOTE]
>
>Le connecteur [!DNL Microsoft Dynamics 365 Finance and Operations] ne prend pas en charge [!DNL Dynamics 365].
>
>Pour les modules Microsoft Dynamics 365, voir [[!DNL Microsoft Dynamics 365 modules]](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-dynamics-365-modules.md).



Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

## Créer une connexion

Pour créer une connexion pour vos modules Finances et opérations Microsoft Dynamics 365 :

1. Dans un module Finances et opérations de Microsoft Dynamics 365, cliquez sur **[!UICONTROL Ajouter]** en regard de la zone Connexion.

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
          <p>Indiquez si vous créez une connexion Dynamics Finance and Operations standard ou une connexion à l’aide d’un code d’autorisation.</p>
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
        <td>Saisissez votre ID client Dynamics Finance and Operations .</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Saisissez votre clé secrète client Dynamics Finance and Operations . </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Tenant ID]</td>
        <td>Saisissez votre ID client Dynamics Finance and Operations.</td>
        </tr>
        <tr>
        <td role="rowheader">Ressource</td>
        <td>Saisissez l’URL de votre compte Dynamics Finance and Operations (sans https://)</td>
        </tr>
      </tbody>
    </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour enregistrer la connexion et revenir au module.



## Modules Finances et opérations de Microsoft Dynamics 365 et leurs champs

>[!IMPORTANT]
>
>Les entités de données disponibles via l’API Dynamics 365 F&amp;O peuvent varier par instance. Si vous ne savez pas quelles entités sont disponibles via l’API, il est utile de parcourir les entités de votre instance à l’aide du point d’entrée « data ». Le point d&#39;entrée « data » dans Dynamics 365 Finance and Operations est l&#39;URL racine pour accéder aux services OData. Ce point d’entrée vous permet d’interagir avec diverses entités de données exposées par le système à l’aide des protocoles OData standard.
>
>Vous pouvez récupérer ces entités à l’aide du module d’appel API personnalisé.
>
><!--For more information -->



### Créer un élément d’entité

Ce module d&#39;action crée un nouvel élément d&#39;entité dans Microsoft Dynamics 365 Finance and Operations.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>Pour plus d’informations sur la connexion de Microsoft Dynamics 365 Finance and Operations à Workfront Fusion, voir <a href="#create-a-connection" class="MCXref xref">Création d’une connexion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>Saisissez ou mappez le type d'entité Dynamics Finance and Operations que vous souhaitez créer.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Body]</td>
     <td> <p>Saisissez ou mappez un corps JSON contenant les données que vous souhaitez inclure dans le nouvel élément d’entité.</p> </td> 
  </tr> 
 </tbody> 
</table>



### Supprimer l’élément d’entité

Ce module d&#39;action supprime un élément d&#39;entité de Dynamics Finance and Operations. L’élément est identifié par ses champs de clé de Principal.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>Pour plus d’informations sur la connexion de Microsoft Dynamics 365 Finance and Operations à Workfront Fusion, voir <a href="#create-a-connection" class="MCXref xref">Création d’une connexion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>Saisissez ou mappez le type d'entité Dynamics Finance and Operations que vous souhaitez supprimer.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Champs de clé de Principal]</td>
     <td> Les champs de clé de Principal identifient l’élément. Pour chaque champ de clé primaire que vous souhaitez fournir, cliquez sur <b>Ajouter un élément</b> et saisissez ou mappez la clé et la valeur uniques qui identifient cet élément. </td> 
  </tr> 
 </tbody> 
</table>

### Effectuer un appel API personnalisé.

Ce module d&#39;action effectue un appel personnalisé à l&#39;API Dynamics Finance and Operations.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
    <td> <p>Pour plus d’informations sur la connexion de Microsoft Dynamics 365 Finance and Operations à Workfront Fusion, voir <a href="#create-a-connection" class="MCXref xref">Création d’une connexion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>Saisissez un chemin d’accès relatif à votre URL Dynamics Finance and Operations.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard. Cela détermine le type de contenu de la requête.</p> <p>Par exemple,<code> {"Content-type":"application/json"}</code></p> <p>Remarque : si vous obtenez des erreurs et qu’il est difficile de déterminer leur origine, pensez à modifier les en-têtes en vous basant sur la documentation de Workfront. Si votre appel API personnalisé renvoie une erreur de requête HTTP 422, essayez d’utiliser un en-tête <code>"Content-Type":"text/plain"</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Chaîne de requête]</td> 
   <td> <p>Ajoutez la requête pour l’appel API sous la forme d’un objet JSON standard.</p> <p>Par exemple : <code>{"name":"something-urgent"}</code></p> <p>Conseil : nous vous recommandons d’envoyer des informations via le corps JSON plutôt que sous forme de paramètres de requête.</p> </td> 
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



### Élément d’entité de lecture

Ce module d&#39;action renvoie les données d&#39;un élément d&#39;entité. L’élément est identifié par ses champs de clé de Principal.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>Pour plus d’informations sur la connexion de Microsoft Dynamics 365 Finance and Operations à Workfront Fusion, voir <a href="#create-a-connection" class="MCXref xref">Création d’une connexion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>Saisissez ou mappez le type d'entité Dynamics Finance and Operations que vous souhaitez lire.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Champs de clé de Principal]</td>
     <td> Les champs de clé de Principal identifient l’élément. Pour chaque champ de clé primaire que vous souhaitez fournir, cliquez sur <b>Ajouter un élément</b> et saisissez ou mappez la clé et la valeur uniques qui identifient cet élément. </td> 
  </tr> 
 </tbody> 
</table>

### Mettre à jour l’élément d’entité

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>Pour plus d’informations sur la connexion de Microsoft Dynamics 365 Finance and Operations à Workfront Fusion, voir <a href="#create-a-connection" class="MCXref xref">Création d’une connexion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>Saisissez ou mappez le type d'entité Dynamics Finance and Operations à mettre à jour.</td> 
  </tr>  
  <tr> 
    <td>[!UICONTROL Champs de clé de Principal]</td>
     <td> Les champs de clé de Principal identifient l’élément. Pour chaque champ de clé primaire que vous souhaitez fournir, cliquez sur <b>Ajouter un élément</b> et saisissez ou mappez la clé et la valeur uniques qui identifient cet élément. </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Body]</td>
     <td> <p>Saisissez ou mappez un corps JSON contenant les données que vous souhaitez inclure dans le nouvel élément d’entité.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Recherche

Ce module de recherche renvoie les résultats en fonction des critères que vous spécifiez.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre application Workfront à Workfront Fusion, voir <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connexion de Workfront à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Entity]</td> 
   <td>Saisissez ou mappez le type d'entité Dynamics Finance and Operations que vous souhaitez rechercher.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria]</td> 
   <td> <p>Renseignez le champ avec lequel vous souhaitez effectuer une recherche, l’opérateur que vous souhaitez utiliser dans votre requête et la valeur que vous recherchez dans le champ.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Sort by]</td> 
   <td> <p>Saisissez ou mappez le champ selon lequel vous souhaitez trier les résultats.</p> </td> 
  </tr> 
 </tbody> 
</table>


<!--

### List All

This module lists all records for a given entity.  The item is identified by its Primary key fields.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>For instructions about connecting Microsoft Dynamics 365 Finance and Operations to Workfront Fusion, see <a href="#create-a-connection" class="MCXref xref">Create a connection</a> in this article.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Record Type]</td>
     <td>Choose the Dynamics Finance and Operations entity type that you want the module to list.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Outputs]</td>
     <td> <p>Select the information you want included in the output bundle for this module.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Watch Record

This trigger module starts a scenario when a record of the given type is created or updated.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
    <td> <p>For instructions about connecting Microsoft Dynamics 365 Finance and Operations to Workfront Fusion, see <a href="#create-a-connection" class="MCXref xref">Create a connection</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to watch.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Enter the field that you want to search by, the operator you want to use in your query, and the value that you are searching for in the field.</p> <p>Note: Do not use <code>username </code>in your search criteria. Including <code>username </code>in an API query to Workfront logs the user into Workfront, and the search will not be successful.</p> <p>Note: <code>In</code> and <code>NotIn</code>work with arrays. The inputs should be in array format.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Select the information you want included in the output bundle for this module.</p> </td> 
  </tr> 
 </tbody> 
</table>

-->
