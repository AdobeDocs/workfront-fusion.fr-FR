---
title: Modules Allocadia
description: Dans un scénario  [!DNL Adobe Workfront Fusion] , vous pouvez automatiser les workflows qui utilisent Allocadia et les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: 9a6fccd6-6eee-42dc-a678-c1f34280d139
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1305'
ht-degree: 88%

---

# Modules [!DNL Allocadia]

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!DNL Allocadia] et le connecter à plusieurs applications et services tiers.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

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

## Conditions préalables

Pour utiliser les modules [!DNL Allocadia], vous devez disposer d’un compte [!DNL Allocadia].

## Informations sur l’API [!DNL Allocadia]

Le connecteur Allocadia utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Version de l’API</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.7.6</td> 
  </tr>
 </tbody> 
</table>

## Connecter [!DNL Allocadia] à [!DNL Workfront Fusion]

Vous pouvez créer une connexion à votre compte [!DNL Allocadia] directement à partir d’un module [!DNL Allocadia].

1. Dans n’importe quel module de [!DNL Allocadia], cliquez sur **[!UICONTROL Add]** en regard du champ [!UICONTROL Connection] .
1. Indiquez si vous souhaitez utiliser le serveur Amérique du Nord ou Europe.
1. Saisissez votre nom d’utilisateur ou d’utilisatrice et votre mot de passe.
1. Cliquez sur **[!UICONTROL Continue]** pour créer la connexion et revenir au module .

## Modules [!DNL Allocadia] et leurs champs

Lorsque vous configurez les modules [!DNL Allocadia], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Allocadia] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Déclencheurs](#triggers)
* [Actions](#actions)
* [Recherches](#searches)

### Déclencheurs

#### [!UICONTROL Watch Record]

Ce module déclencheur exécute un scénario lorsque des objets d’un type spécifique sont ajoutés, mis à jour ou les deux. Le module renvoie tous les champs standard associés à l’enregistrement ou aux enregistrements, ainsi que les champs et valeurs personnalisés auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> <table style="table-layout:auto"> <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Allocadia à [!DNL Workfront Fusion], consultez <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">[!UICONTROL Connect Allocadia] à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filtre</td> 
   <td> <p>Choisissez si vous souhaitez que le scénario regarde les nouveaux enregistrements uniquement, les [!UICONTROL Updated Records Only] ou les nouveaux enregistrements et les enregistrements mis à jour.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type d’entité</td> 
   <td>Sélectionnez le type d’enregistrement Allocadia que vous souhaitez que le module surveille.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sorties</td> 
   <td> <p>Sélectionnez les champs que vous souhaitez inclure dans la sortie du module. Les champs disponibles dépendent du type d’entité que vous avez sélectionné.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Limite</td> 
   <td> <p>Saisissez ou mappez le nombre maximal d’enregistrements que le module doit surveiller pour chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [Appel API personnalisé](#custom-api-call)
* [Lire l’enregistrement](#read-record)
* [Créer l’enregistrement](#create-record)
* [Supprimer l’enregistrement](#delete-record)
* [Mettre à jour l’enregistrement](#update-record)

#### [!UICONTROL Custom API Call]

Ce module d’action vous permet d’effectuer un appel personnalisé et authentifié à l’API [!DNL Allocadia]. Vous pouvez ainsi créer une automatisation du flux de données que les autres modules [!DNL Allocadia] ne peuvent pas réaliser.

L’action est basée sur le type d’entité (type d’objet Allocadia) que vous spécifiez.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Allocadia] à [!DNL Workfront Fusion], voir <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Allocadia] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Saisissez un chemin relatif à <code>https://api-na.allocadia.com/{version}</code> ou <code>https://api-eu.allocadia.com/{version}</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP dans [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] ajoute les en-têtes d’autorisation pour vous.</p> </td> 
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

#### [!UICONTROL Read Record]

Ce module d’action lit les données d’un seul enregistrement dans [!DNL Allocadia].

Vous indiquez l’ID de l’enregistrement.

Le module renvoie tous les champs standard associés à l’enregistrement, ainsi que tous les champs et valeurs personnalisés auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Allocadia] à [!DNL Workfront Fusion], voir <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Allocadia] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>Sélectionnez le type d’enregistrement [!DNL Allocadia] que vous souhaitez que le module lise.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Sélectionnez les champs que vous souhaitez inclure dans la sortie du module. Les champs disponibles dépendent du [!UICONTROL Entity Type] que vous avez sélectionné.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Saisissez ou mappez l’ID unique [!DNL Allocadia] de l’enregistrement que vous souhaitez que le module lise.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create Record]

Ce module d’action crée un enregistrement.

Le module renvoie l’ID de l’enregistrement et tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Allocadia] à [!DNL Workfront Fusion], voir <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Allocadia] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>Indiquez si vous souhaitez créer un enregistrement en fonction du choix de l’élément de ligne ou de la colonne.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Budgets]</td> 
   <td> <p>Sélectionnez le budget dans lequel vous souhaitez créer un enregistrement.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Column choices]</td> 
   <td>Sélectionnez la colonne à utiliser pour créer un enregistrement.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Label]</td> 
   <td>Saisissez ou mappez un libellé pour le nouvel enregistrement.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete Record]

Ce module d’action supprime un enregistrement particulier.

Vous indiquez l’ID de l’enregistrement.

Le module renvoie l’ID de l’enregistrement et tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Allocadia] à [!DNL Workfront Fusion], voir <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Allocadia] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td> <p>Sélectionnez le type d’entité à supprimer.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Line item]</strong> </p> <p>Saisissez l’ID de l’élément de ligne.</p> </li> 
     <li> <p><strong>[!UICONTROL Column Choice]</strong> </p> <p>Sélectionnez le budget dont vous souhaitez supprimer un enregistrement, puis saisissez l’ID de colonne et l’ID de choix.</p> </li> 
     <li> <p><strong>[!UICONTROL Forecast Tags]</strong> </p> <p>Sélectionnez le budget dont vous souhaitez supprimer un enregistrement, puis saisissez l’ID de balise.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update Record]

Ce module d’action met à jour un enregistrement, tel qu’un élément de ligne, un utilisateur ou une utilisatrice ou un choix de colonne.

Vous indiquez l’ID de l’enregistrement.

Le module renvoie l’ID de l’enregistrement et tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Allocadia] à [!DNL Workfront Fusion], voir <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Allocadia] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>Sélectionnez le type d’enregistrement [!DNL Allocadia] que le module doit mettre à jour. D’autres champs s’affichent en fonction du type d’entité sélectionné.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Budgets]</td> 
   <td> <p>Sélectionnez le budget dont vous souhaitez mettre à jour un enregistrement. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Recherches

#### [!UICONTROL Search Record]

Ce module de recherche recherche les enregistrements dans un objet dans [!DNL Allocadia] qui correspondent à la requête que vous avez spécifiée.

Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Vous indiquez le type d’enregistrement souhaité.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Allocadia] à [!DNL Workfront Fusion], voir <a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Allocadia] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>Sélectionnez le type d’enregistrement [!DNL Allocadia] que le module doit rechercher. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Budgets]</td> 
   <td> <p>Sélectionnez le budget à rechercher. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Result set]</td> 
   <td>Indiquez si vous souhaitez que le module renvoie tous les enregistrements correspondants ou uniquement le premier enregistrement correspondant.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximal count of records]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search criteria]</td> 
   <td>Sélectionnez le champ à rechercher, sélectionnez l’opération, puis saisissez ou mappez la valeur à rechercher. Vous pouvez ajouter des règles [!DNL AND] ou [!DNL OR] pour filtrer davantage votre recherche.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Sélectionnez les champs que vous souhaitez inclure dans la sortie du module. Les champs disponibles dépendent du type d’entité que vous avez sélectionné.</p> </td> 
  </tr> 
 </tbody> 
</table>
