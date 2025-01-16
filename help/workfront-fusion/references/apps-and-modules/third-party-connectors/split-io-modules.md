---
title: Modules Split.io
description: Dans un scénario  [!DNL Adobe Workfront Fusion] , vous pouvez automatiser les workflows qui utilisent  [!DNL Split.io]et le connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: 7d738a96-5424-4c30-831f-82e1d4c6f9d2
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1493'
ht-degree: 87%

---

# Modules [!DNL Split.io]

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!DNL Split.io] et le connecter à plusieurs applications et services tiers.

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

Pour utiliser les modules [!DNL Split.io], vous devez disposer d’un compte [!DNL Split.io].

## Informations sur l’API Split.io

Le connecteur Split.io utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td> https://api.split.io/internal/api</td>
   </tr> 
  <tr> 
   <td role="rowheader">Version de l’API</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.34.1</td> 
  </tr>
 </tbody> 
 </table>

## Connecter [!DNL Split.io] à [!DNL Workfront Fusion] {#connect-split-io-to-workfront-fusion}

Vous pouvez créer une connexion à votre compte [!DNL Split.io] directement à partir d’un module [!DNL Split.io].

1. Dans n’importe quel module de [!DNL Split.io], cliquez sur **[!UICONTROL Add]** en regard du champ [!UICONTROL Connection] .
1. Saisissez un nom pour la connexion.
1. Saisissez votre clé d’API [!DNL Split.io].

   Pour plus d’informations sur les clés d’API [!DNL Split.io], voir [Clés d’API](https://help.split.io/hc/en-us/articles/360019916211-API-keys) dans la documentation [!DNL Split.io].

1. Cliquez sur **[!UICONTROL Continue]** pour créer la connexion et revenir au module .

## Modules [!DNL Split.io] et leurs champs

Lorsque vous configurez les modules [!DNL split.io], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL split.io] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Actions](#actions)
* [Recherches](#searches)

### Actions

* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Get Split]](#get-split)
* [[!UICONTROL Get Split Definition in Environment]](#get-split-definition-in-environment)
* [[!UICONTROL Create Split]](#create-split)
* [[!UICONTROL Delete Split]](#delete-split)
* [[!UICONTROL Create Split Definition in Environment]](#create-split-definition-in-environment)
* [[!UICONTROL Remove Split Definition from Environment]](#remove-split-definition-from-environment)
* [[!UICONTROL Partial Update Split Definition in Environment]](#partial-update-split-definition-in-environment)
* [[!UICONTROL Associate Tags]](#associate-tags)

#### [!UICONTROL Custom API Call]

Ce module d’action vous permet d’effectuer un appel personnalisé et authentifié à l’API [!DNL split.io]. Cela vous permet de créer une automatisation du flux de données qui ne peut pas être réalisée par les autres modules [!DNL split.io].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Split.io] à [!DNL Workfront Fusion], consultez dans cet article la section <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Split.io] à [!UICONTROL Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Saisir un chemin relatif à <code>https://api.split.io/internal/api/v2/</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Méthodes de requête HTTP dans [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion ajoute les en-têtes d’autorisation pour vous.</p> </td> 
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
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Saisissez ou mappez le nombre maximum d’enregistrements que vous souhaitez que le module utilise lors de chaque cycle d’exécution du scénario.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Split]

Ce module d’action récupère le partage.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Split.io] à [!DNL Workfront Fusion], consultez dans cet article la section <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Split.io] à [!UICONTROL Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Sélectionnez ou mappez l’espace de travail contenant le partage que vous souhaitez récupérer.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>Saisissez ou mappez le nom du partage que vous souhaitez récupérer.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Split Definition in Environment]

Ce module d’action récupère une définition de partage spécifique de l’environnement désigné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Split.io] à [!DNL Workfront Fusion], consultez dans cet article la section <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Split.io] à [!UICONTROL Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Sélectionnez ou mappez l’espace de travail qui contient la définition de partage que vous souhaitez récupérer.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Environment Name or ID]</td> 
   <td>Sélectionnez ou mappez l’environnement contenant la définition de partage que vous souhaitez récupérer.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>Saisissez ou mappez le nom du partage pour lequel vous souhaitez récupérer la définition de partage.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create Split]

Ce module d’action crée un partage dans votre organisation, à partir d’un type de trafic.

>[!NOTE]
>
>L’API ne configure le partage dans aucun environnement.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Split.io] à [!DNL Workfront Fusion], consultez dans cet article la section <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Split.io] à [!UICONTROL Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Sélectionnez ou mappez l’espace de travail dans lequel vous souhaitez créer le partage.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Traffic Type ID or Name]</td> 
   <td>Sélectionnez ou mappez le type de trafic que vous souhaitez utiliser pour créer le partage.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>Saisissez ou mappez un nom pour le partage que vous souhaitez créer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Description]</td> 
   <td>Saisissez ou mappez une description [!UICONTROL split] pour le fractionnement que vous souhaitez créer.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete Split]

Ce module d’action supprime un partage de votre organisation. Cette fonction déconfigure automatiquement la définition de partage de tous les environnements.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Split.io] à [!DNL Workfront Fusion], consultez dans cet article la section <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Split.io] à [!UICONTROL Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Sélectionnez ou mappez l’espace de travail dans lequel vous souhaitez supprimer le partage.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>Saisissez ou mappez le nom du partage que vous souhaitez supprimer.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create Split Definition in Environment]

Ce module d’action configure une définition de partage pour un environnement spécifique.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Split.io] à [!DNL Workfront Fusion], consultez dans cet article la section <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Split.io] à [!UICONTROL Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Sélectionnez ou mappez l’espace de travail dans lequel vous souhaitez créer une définition de partage.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Environment Name or ID]</td> 
   <td>Sélectionnez ou mappez l’environnement dans lequel vous souhaitez créer une définition de partage.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>Saisissez ou mappez le nom du partage pour lequel vous souhaitez créer une définition.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comments]</td> 
   <td>Saisissez ou mappez les commentaires à ajouter à la définition de partage.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Rules]</td> 
   <td> <p>Pour chaque règle de ciblage à ajouter à la définition, cliquez sur <b>[!UICONTROL Add item]</b>, puis saisissez ou mappez la règle.</p> <p>Pour plus d’informations sur les règles de ciblage, voir <a href="https://docs.split.io/reference#create-split-definition-in-environment">Créer une définition de partage dans un environnement</a> dans la documentation [!DNL Split.io].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Default rule]</td> 
   <td> <p>Saisissez ou mappez la règle que vous souhaitez que le partage utilise pour le trafic qui ne répond pas aux spécifications des autres règles.</p> <p>Pour plus d’informations sur les règles de ciblage, voir <a href="https://docs.split.io/reference#create-split-definition-in-environment">Créer une définition de partage dans un environnement</a> dans la documentation [!DNL Split.io].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Default treatment]</td> 
   <td> <p>Saisissez ou mappez le traitement que vous souhaitez que le partage utilise si le partage est terminé ou si la personne n’est pas incluse dans l’affectation du trafic.</p> <p>Pour plus d’informations sur les traitements, voir <a href="https://docs.split.io/reference#create-split-definition-in-environment">Créer une définition de partage dans un environnement</a> dans la documentation [!DNL Split.io].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Treatments]</td> 
   <td> <p>Pour chaque traitement à ajouter à la définition, cliquez sur <b>[!UICONTROL Add item]</b>, puis saisissez ou mappez le traitement.</p> <p>Pour plus d’informations sur les traitements, voir <a href="https://docs.split.io/reference#create-split-definition-in-environment">Créer une définition de partage dans un environnement</a> dans la documentation [!DNL Split.io].</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove Split Definition from Environment]

Ce module d’action déconfigure une définition de partage pour un environnement spécifique.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Split.io] à [!DNL Workfront Fusion], consultez dans cet article la section <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Split.io] à [!UICONTROL Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Sélectionnez ou mappez l’espace de travail dans lequel vous souhaitez supprimer une définition de partage.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Environment Name or ID]</td> 
   <td>Sélectionnez ou mappez l’environnement dans lequel vous souhaitez supprimer une définition de partage.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>Saisissez ou mappez le nom du partage pour lequel vous souhaitez supprimer une définition.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comments]</td> 
   <td>Saisissez ou mappez les commentaires à ajouter à la définition de partage.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Partial Update Split Definition in Environment]

Ce module d’action met à jour une définition de partage pour un environnement spécifique.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Split.io] à [!DNL Workfront Fusion], consultez dans cet article la section <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Split.io] à [!UICONTROL Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Sélectionnez ou mappez l’espace de travail dans lequel vous souhaitez mettre à jour une définition de partage.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Environment Name or ID]</td> 
   <td>Sélectionnez ou mappez l’environnement dans lequel vous souhaitez mettre à jour une définition de partage.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>Saisissez ou mappez le nom du partage pour lequel vous souhaitez mettre à jour une définition.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Update content]</td> 
   <td> <p>Pour chaque attribut de la division à mettre à jour, cliquez sur <b>[!UICONTROL Add item]</b> et saisissez ou mappez les modifications souhaitées.</p> <p>Pour plus d’informations, voir <a href="https://docs.split.io/reference#partial-update-split-definition-in-environment">Mise à jour partielle de la définition de partage dans l’environnement</a> dans la documentation [!DNL Split.io].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comments]</td> 
   <td>Saisissez ou mappez les commentaires à ajouter à la définition de partage.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Associate Tags]

Ce module d’action ajoute des balises à l’objet spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Split.io] à [!DNL Workfront Fusion], consultez dans cet article la section <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Split.io] à [!UICONTROL Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Sélectionnez ou mappez l’espace de travail dans lequel vous souhaitez ajouter une balise.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object Name]</td> 
   <td>Saisissez ou mappez le nom de l’objet auquel vous souhaitez ajouter des balises.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object Type]</td> 
   <td> <p>Saisissez ou mappez le type d’objet auquel vous souhaitez ajouter des balises.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td> <p>Pour chaque balise à ajouter, cliquez sur <b>[!UICONTROL Add item]</b> et saisissez ou mappez la balise.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Recherches

* [[!UICONTROL Get Workspaces]](#get-workspaces)
* [[!UICONTROL Get Environments]](#get-environments)
* [[!UICONTROL Get Splits]](#get-splits)
* [[!UICONTROL List Split Definitions in an Environment]](#list-split-definitions-in-an-environment)
* [[!UICONTROL Get Traffic Types]](#get-traffic-types)

#### [!UICONTROL Get Workspaces]

Ce module de recherche récupère les espaces de travail d’une organisation.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Split.io] à [!DNL Workfront Fusion], consultez dans cet article la section <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Split.io] à [!UICONTROL Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Saisissez ou mappez le nombre maximum d’espaces de travail que vous souhaitez que le module récupère au cours de chaque cycle d’exécution du scénario.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Environments]

Ce module de recherche récupère une liste d’environnements.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Split.io] à [!DNL Workfront Fusion], consultez dans cet article la section <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Split.io] à [!UICONTROL Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Sélectionnez ou mappez l’espace de travail contenant les environnements que vous souhaitez répertorier.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Splits]

Ce module de recherche récupère une liste de partages.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Split.io] à [!DNL Workfront Fusion], consultez dans cet article la section <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Split.io] à [!UICONTROL Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Sélectionnez ou mappez l’espace de travail contenant les partages que vous souhaitez répertorier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Saisissez ou mappez le nombre maximal de partages que le module doit récupérer au cours de chaque cycle d’exécution de scénario.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Split Definitions in an Environment]

Ce module de recherche récupère une liste de définitions de partage dans un environnement donné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Split.io] à [!DNL Workfront Fusion], consultez dans cet article la section <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Split.io] à [!UICONTROL Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Sélectionnez ou mappez l’espace de travail qui contient les définitions de partage que vous souhaitez répertorier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Environment Name or ID]</td> 
   <td>Sélectionnez ou mappez l’environnement qui contient les définitions de partage que vous souhaitez répertorier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Saisissez ou mappez le nombre maximal de définitions de partage que le module doit récupérer au cours de chaque cycle d’exécution de scénario.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Traffic Types]

Ce module de recherche récupère une liste des types de trafic.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Split.io] à [!DNL Workfront Fusion], consultez dans cet article la section <a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Split.io] à [!UICONTROL Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Sélectionnez ou mappez l’espace de travail qui contient les types de trafic que vous souhaitez répertorier.</td> 
  </tr> 
 </tbody> 
</table>
