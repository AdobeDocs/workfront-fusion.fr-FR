---
title: Modules Adobe Workfront Planning
description: Avec les modules  [!DNL Adobe Workfront Planning] , vous pouvez lancer un scénario Adobe Workfront Fusion en fonction des événements de votre compte de planification  [!DNL Adobe] Workfront, créer, lire ou mettre à jour des contrats et d’autres enregistrements, rechercher des enregistrements à l’aide des critères que vous avez définis et charger des documents.
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
TQID: https://experienceleague.adobe.com/QHOFWDOT-18-c0b3wLXsRV5cjGVxlcyLhvZdkev3GFg
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: f0e185778e01b71a91837531a082e88485e97ca2
workflow-type: tm+mt
source-wordcount: 6075
ht-degree: 44%

---


# Modules Adobe Workfront Planning

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

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

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
   <td><pre><code>https://&#123;&#123;connection.host&#125;&#125;/maestro/api/&#123;&#123;common.maestroApiVersion&#125;&#125;/</code></pre></td> 
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
          <p>Sélectionnez la connexion <b>Authentification </b>.</p>
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

## Modules [!DNL Adobe Workfront Planning] version 2 et leurs champs

>[!IMPORTANT]
>
>Les modules de cette section appartiennent au connecteur Workfront Planning V2.Pour les modules du connecteur Workfront Planning V1, consultez les modules [[!DNL Adobe Workfront Planning] Version 1 et leurs champs](#adobe-workfront-planning-version-1-modules-and-their-fields).

Lorsque vous configurez les modules de planification Workfront, Workfront Fusion affiche les champs répertoriés ci-dessous. Des champs Workfront supplémentaires peuvent s’afficher, selon votre niveau d’accès dans l’application ou le service, par exemple. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, consultez [Mappage d’informations d’un module à l’autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

* [Espaces de travail](#workspaces-v2)
* [Types d’enregistrements](#record-types-v2)
* [Enregistrements](#records-v2)
* [Champs](#fields-v2)
* [Vues](#views-v2)
* [Autorisations](#permissions-v2)
* [Autre](#other-v2)

### Espaces de travail (V2)

* [Créer un espace de travail](#create-a-workspace-v2)
* [Supprimer un espace de travail](#delete-a-workspace-v2)
* [Obtenir tous les espaces de travail](#get-all-workspaces-v2)
* [Obtenir un espace de travail](#get-a-workspace-v2)
* [Mise à jour d’un espace de travail](#update-a-workspace-v2)

#### Créer un espace de travail (V2)

Ce module d&#39;action crée un espace de travail dans Planning.

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
        <p>[!UICONTROL Workspace name]</p>
      </td>
      <td>Saisissez ou mappez un nom pour le nouvel espace de travail.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Description</p>
      </td>
      <td>Saisissez ou mappez une description pour le nouvel espace de travail/td&gt; 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Couleur</p>
      </td>
      <td>Sélectionnez la couleur que vous souhaitez utiliser pour représenter le nouveau type d’enregistrement</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Icône</p>
      </td>
      <td>Mappez l’icône que vous souhaitez utiliser pour ce type d’enregistrement.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Propriétaire</p>
      </td>
      <td>Saisissez ou mappez l’ID utilisateur Adobe IMS de l’utilisateur que vous souhaitez propriétaire de l’espace de travail.</td> 
    </tr>
  </tbody>
</table>

#### Suppression d’un espace de travail (V2)

Ce module d’action supprime un seul espace de travail, spécifié par l’ID.

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
        <p>[!UICONTROL Workspace ID]</p>
      </td>
      <td>Saisissez ou mappez l’identifiant de l’espace de travail à supprimer.</td> 
    </tr>
  </tbody>
</table>

#### Obtenir tous les espaces de travail (V2)

Ce module récupère une liste de tous les espaces de travail.

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
        <p>[!UICONTROL Maximum number of returned workspaces]</p>
      </td>
      <td>Saisissez ou mappez le nombre maximal d’espaces de travail que le module renverra au cours d’un cycle d’exécution.</td> 
    </tr>
  </tbody>
</table>

#### Obtenir un espace de travail (V2)

Ce module récupère un espace de travail par son identifiant.

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
        <p>[!UICONTROL Workspace ID]</p>
      </td>
      <td>Saisissez ou mappez l’identifiant de l’espace de travail que vous souhaitez récupérer.</td> 
    </tr>
  </tbody>
</table>

#### Mise à jour d’un espace de travail (V2)

Ce module d&#39;action met à jour un nouvel espace de travail dans Planning.

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
      <td>Sélectionnez l’espace de travail à mettre à jour.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace name]</p>
      </td>
      <td>Saisissez ou mappez un nom pour le nouvel espace de travail.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Description</p>
      </td>
      <td>Saisissez ou mappez une description pour le nouvel espace de travail/td&gt; 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Couleur</p>
      </td>
      <td>Sélectionnez la couleur que vous souhaitez utiliser pour représenter le nouveau type d’enregistrement</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Icône</p>
      </td>
      <td>Mappez l’icône que vous souhaitez utiliser pour ce type d’enregistrement.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Propriétaire</p>
      </td>
      <td>Saisissez ou mappez l’ID utilisateur Adobe IMS de l’utilisateur que vous souhaitez propriétaire de l’espace de travail.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Sections de type d’enregistrement</p>
      </td>
      <td>Pour chaque section de type d’enregistrement que vous souhaitez ajouter à cet espace de travail, cliquez sur <b>Ajouter un élément</b> et saisissez le nom de la section, les ID de type d’enregistrement et si vous souhaitez remplacer les ID de type d’enregistrement existants.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Sections de type d’enregistrement &gt; Remplacer</p>
      </td>
      <td>Choisissez de remplacer les sections existantes par celles du module. Si ce n'est pas le cas, les sections du module sont ajoutées à la liste existante des sections.</td> 
    </tr>
  </tbody>
</table>


### Types d’enregistrement (V2)

* [Création d’un type d’enregistrement](#create-a-record-type-v2)
* [Supprimer un type d’enregistrement](#delete-a-record-type-v2)
* [Obtention des types d’enregistrements globaux](#get-global-record-types-v2)
* [Obtenir un type d’enregistrement](#get-a-record-type-v2)
* [Obtenir des types d’enregistrement](#get-record-types-v2)
* [Mise à jour d’un type d’enregistrement](#update-a-record-type-v2)

#### Création d’un type d’enregistrement (V2)

Ce module d&#39;action crée un nouveau type d&#39;enregistrement dans l&#39;espace de travail sélectionné.

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
      <td>Sélectionnez l’espace de travail dans lequel vous souhaitez créer un type d’enregistrement.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Nom d’affichage</p>
      </td>
      <td>Saisissez ou mappez un nom pour le nouveau type d’enregistrement.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Description</p>
      </td>
      <td>Saisissez ou mappez une description pour le nouveau type d’enregistrement.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Icône</p>
      </td>
      <td>Mappez l’icône que vous souhaitez utiliser pour ce type d’enregistrement.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Couleur</p>
      </td>
      <td>Sélectionnez la couleur que vous souhaitez utiliser pour représenter le nouveau type d’enregistrement</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Type d’enregistrement Source</p>
      </td>
      <td>Si vous utilisez un autre type d’enregistrement à copier comme point de départ, sélectionnez ce type d’enregistrement.</td> 
    </tr>
  </tbody>
</table>

#### Suppression d’un type d’enregistrement (V2)

Ce module d’action supprime un seul type d’enregistrement, spécifié par l’ID.

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

#### Obtention des types d’enregistrements globaux (V2)

Ce module récupère une liste des types d’enregistrements dans un compte Adobe Workfront Planning.

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
      <td>Sélectionnez un espace de travail. Le module renvoie les types d’enregistrements globaux qui peuvent être ajoutés à cet espace de travail.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Nombre maximal de types d'enregistrements renvoyés]</p>
      </td>
      <td>Saisissez ou mappez le nombre maximal de types d’enregistrements que le module renverra au cours d’un cycle d’exécution.</td> 
    </tr>
  </tbody>
</table>

#### Obtenir un type d’enregistrement (V2)

Ce module récupère un type d’enregistrement par son identifiant.

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
      <td>Saisissez ou mappez l’identifiant du type d’enregistrement à récupérer.</td> 
    </tr>
  </tbody>
</table>

#### Obtenir les types d’enregistrements (V2)

Ce module récupère une liste des types d’enregistrements disponibles dans un espace de travail donné.

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
      <td>Sélectionnez l’espace de travail pour lequel vous souhaitez récupérer les types d’enregistrements.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Nombre maximal de types d'enregistrements renvoyés]</p>
      </td>
      <td>Saisissez ou mappez le nombre maximal de types d’enregistrements que le module renverra au cours d’un cycle d’exécution.</td> 
    </tr>
  </tbody>
</table>

#### Mise à jour d’un type d’enregistrement (V2)

Ce module met à jour un type d’enregistrement.

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
      <td>Sélectionnez l’espace de travail dans lequel vous souhaitez mettre à jour un type d’enregistrement.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Type d’enregistrement]</p>
      </td>
      <td>Sélectionnez l’espace de travail dans lequel vous souhaitez mettre à jour un type d’enregistrement.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Nom d’affichage</p>
      </td>
      <td>Saisissez ou mappez un nom pour le type d’enregistrement.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Description</p>
      </td>
      <td>Saisissez ou mappez une description pour le type d’enregistrement.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>ID de champ de Principal</p>
      </td>
      <td>Saisissez ou mappez l’identifiant du champ utilisé comme titre du type d’enregistrement.</td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>Icône</p>
      </td>
      <td>Mappez l’icône que vous souhaitez utiliser pour ce type d’enregistrement.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Couleur</p>
      </td>
      <td>Sélectionnez la couleur que vous souhaitez utiliser pour représenter le nouveau type d’enregistrement</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Liable avec les identifiants Workspace</p>
      </td>
      <td>Pour chaque espace de travail vers lequel vous souhaitez que ce type d’enregistrement puisse créer un lien, cliquez sur <b>Ajouter un élément</b> et saisissez l’identifiant de l’espace de travail.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Liable avec les Workspace ID &gt; Remplacer</p>
      </td>
      <td>Choisissez de remplacer les espaces de travail existants par ceux du module . Si non, les espaces de travail du module sont ajoutés à la liste existante des espaces de travail.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Autorisé à créer un type d’enregistrement dynamique</p>
      </td>
      <td>Pour chaque objet autorisé à créer des types d’enregistrements dynamiques à partir de ce type d’enregistrement, cliquez sur <b>Ajouter un élément</b> et saisissez le type et l’ID de l’objet.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Autorisé à créer un type d’enregistrement dynamique &gt; Remplacer</p>
      </td>
      <td>Choisissez s'il faut remplacer les sujets existants par ceux du module. Si non, les sujets du module sont ajoutés à la liste existante des sujets.</td> 
    </tr>
  </tbody>
</table>



### Enregistrements (V2)

* [Créer un enregistrement](#create-a-record-v2)
* [Supprimer un enregistrement](#delete-a-record-v2)
* [Obtenir un enregistrement](#get-a-record-v2)
* [Obtenir des enregistrements par type d’enregistrement](#get-records-by-record-type-v2)
* [Déplacer des enregistrements](#move-records-v2)
* [Rechercher des enregistrements](#search-records-v2)
* [Mettre à jour un enregistrement](#update-a-record-v2)

#### Création d’un enregistrement (V2)

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
        <p>[!UICONTROL Workspace]</p>
      </td>
      <td>Sélectionnez l’espace de travail dans lequel vous souhaitez créer un enregistrement.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type]</p>
      </td>
      <td>Sélectionnez le type d’enregistrement que vous souhaitez créer.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Autres champs</p>
      </td>
      <td>Saisissez les valeurs que vous souhaitez attribuer au nouvel enregistrement. Ces champs sont basés sur le type d’enregistrement que vous avez sélectionné et sont propres à votre organisation Workfront Planning.</td> 
    </tr>
  </tbody>
</table>

#### Suppression d’un enregistrement (V2)

Ce module d&#39;action supprime un seul enregistrement, spécifié par l&#39;ID.

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
      <td>Saisissez ou mappez l’identifiant de l’enregistrement à supprimer.</td> 
    </tr>
  </tbody>
</table>

#### Obtenir un enregistrement (V2)

Ce module d&#39;action récupère un enregistrement, spécifié par son identifiant.

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
        <p>[!UICONTROL Workspace ID]</p>
      </td>
      <td>Saisissez ou mappez l’identifiant de l’enregistrement que vous souhaitez récupérer.</td> 
    </tr>
  </tbody>
</table>

#### Obtention des enregistrements par type d’enregistrement (V2)

Ce module récupère une liste de tous les enregistrements du type d’enregistrement donné.

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
      <td>Sélectionnez l’espace de travail qui contient les enregistrements à récupérer.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Type d’enregistrement]</p>
      </td>
      <td>Sélectionnez le type d'enregistrement à renvoyer.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximum number of returned records]</p>
      </td>
      <td>Saisissez ou mappez le nombre maximal d'enregistrements que le module renverra au cours d'un cycle d'exécution.</td> 
    </tr>
  </tbody>
</table>

#### Déplacer des enregistrements (V2)

Ce module réorganise un ou plusieurs enregistrements dans un type d&#39;enregistrement en spécifiant où les placer.

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
      <td>Sélectionnez l’espace de travail qui contient les enregistrements à déplacer.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Type d’enregistrement]</p>
      </td>
      <td>Sélectionnez le type d’enregistrement à déplacer.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Espace de travail]</p>
      </td>
      <td>Sélectionnez l’espace de travail qui contient les enregistrements à déplacer.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Espace de travail]</p>
      </td>
      <td>Sélectionnez l’espace de travail qui contient les enregistrements à déplacer.</td> 
    </tr>
  </tbody>
</table>

#### Rechercher des enregistrements (V2)

Retourner les enregistrements selon les critères que vous spécifiez

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
      <td>Sélectionnez l’espace de travail qui contient les enregistrements à récupérer.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Type d’enregistrement]</p>
      </td>
      <td>Sélectionnez le type d’enregistrement qui contient les enregistrements à récupérer.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Other fields]</p>
      </td>
      <td>Pour chaque champ sur lequel vous souhaitez appliquer un filtre, saisissez l’opérateur et la valeur de ce champ. Ces champs sont basés sur le type d’enregistrement que vous avez sélectionné et sont propres à votre organisation Workfront Planning.</td> 
    </tr>
  </tbody>
</table>

#### Mise à jour d’un enregistrement (V2)

Ce module met à jour l’enregistrement spécifié.



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
      <td>Sélectionnez l’espace de travail contenant l’enregistrement à mettre à jour.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record type ID]</p>
      </td>
      <td>Sélectionnez le type d’enregistrement à mettre à jour.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Record ID]</p>
      </td>
      <td>Saisissez ou mappez l’ID de l’enregistrement que vous souhaitez mettre à jour.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Other fields]</p>
      </td>
      <td>Saisissez des valeurs pour d’autres champs. Les champs disponibles dépendent de l’enregistrement sélectionné.</td> 
    </tr>
  </tbody>
</table>


### Champs (V2)

* [Création d’un champ](#create-a-field-v2)
* [Suppression d’un champ](#delete-a-field-v2)
* [Obtenir un champ](#get-a-field-v2)
* [Obtenir les champs par type d’enregistrement](#get-fields-by-record-type-v2)
* [Mettre à jour un champ](#update-a-field-v2)

#### Créer un champ (V2)

Ce module d’action crée un champ sur le type d’enregistrement spécifié.

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
      <td>Sélectionnez l’espace de travail dans lequel vous souhaitez créer un champ.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Type d’enregistrement]</p>
      </td>
      <td>Sélectionnez le type d’enregistrement pour lequel vous souhaitez créer un champ.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Nom d’affichage</p>
      </td>
      <td>Saisissez ou mappez un nom pour le nouveau champ.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Description</p>
      </td>
      <td>Saisissez ou mappez une description pour le nouveau champ.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Type de champ</p>
      </td>
      <td>Sélectionnez le type de données du champ.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Autres champs</p>
      </td>
      <td>D’autres champs spécifiques au type de champ sélectionné peuvent être disponibles. Renseignez les valeurs de ces champs.</td> 
    </tr>
  </tbody>
</table>

#### Suppression d’un champ (V2)

Ce module d’action supprime un seul champ, spécifié par l’ID.

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
        <p>[!UICONTROL Field ID]</p>
      </td>
      <td>Saisissez ou mappez l’ID du champ à supprimer.</td> 
    </tr>
  </tbody>
</table>

#### Obtenir un champ (V2)

Ce module récupère un champ par son identifiant.

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
        <p>[!UICONTROL Field ID]</p>
      </td>
      <td>Saisissez ou mappez l’identifiant du champ que vous souhaitez récupérer.</td> 
    </tr>
  </tbody>
</table>

#### Obtenir les champs par type d’enregistrement (V2)

Ce module récupère une liste de champs pour un type d’enregistrement spécifique.

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
      <td>Sélectionnez l’espace de travail qui contient les champs que vous souhaitez renvoyer.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Type d’enregistrement]</p>
      </td>
      <td>Sélectionnez le type d’enregistrement pour lequel vous souhaitez renvoyer des champs.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Nombre maximal de champs renvoyés]</p>
      </td>
      <td>Saisissez ou mappez le nombre maximal de champs que le module renverra au cours d’un cycle d’exécution.</td> 
    </tr>
  </tbody>
</table>

#### Mise à jour d’un champ (V2)

Ce module met partiellement à jour un champ par son identifiant.

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
        <p>[!UICONTROL Type de ressource]</p>
      </td>
      <td>Sélectionnez le type de ressource qui contient le champ à mettre à jour.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Field ID]</p>
      </td>
      <td>Sélectionnez le champ à mettre à jour.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Nom d'affichage]</p>
      </td>
      <td>Saisissez ou mappez un nom pour le champ.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Description]</p>
      </td>
      <td>Saisissez ou mappez une description pour le champ.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Autres paramètres]</p>
      </td>
      <td>Saisissez des valeurs pour d’autres paramètres de champ. Les paramètres disponibles dépendent du champ sélectionné.</td> 
    </tr>
  </tbody>
</table>


### Vues (V2)

* [Création d’une vue](#create-a-view-v2)
* [Suppression d’une vue](#delete-a-view-v2)
* [Obtenir une vue](#get-a-view-v2)
* [Obtention des vues par type d’enregistrement](#get-views-by-record-type-v2)
* [Mise à jour d’une vue](#update-a-view-v2)

#### Création d’une vue (V2)

Ce module d’action crée une vue pour le type d’enregistrement sélectionné.

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
      <td>Sélectionnez l’espace de travail dans lequel vous souhaitez créer une vue.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Type d’enregistrement]</p>
      </td>
      <td>Sélectionnez le type d’enregistrement pour lequel vous souhaitez créer une vue.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Nom de la vue</p>
      </td>
      <td>Saisissez ou mappez un nom pour la nouvelle vue.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Type d’affichage</p>
      </td>
      <td>Indiquez si la nouvelle vue est de type Tableau, Chronologie ou Calendrier.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Champ de date de début</p>
      </td>
      <td>S'il s'agit d'une vue de calendrier ou de chronologie, sélectionnez le champ que la vue utilisera pour placer l'enregistrement sur la chronologie.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Champ de date de fin.</p>
      </td>
      <td>S'il s'agit d'une vue de calendrier ou de chronologie, sélectionnez le champ que la vue utilisera pour déterminer la date de fin sur la chronologie.</td> 
    </tr>
  </tbody>
</table>

#### Suppression d’une vue (V2)

Ce module d’action supprime une vue unique, spécifiée par l’ID.

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
        <p>[!UICONTROL View ID]</p>
      </td>
      <td>Saisissez ou mappez l'ID de la vue à supprimer.</td> 
    </tr>
  </tbody>
</table>

#### Obtenir une vue (V2)

Ce module récupère une vue par son identifiant.

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
        <p>[!UICONTROL View ID]</p>
      </td>
      <td>Saisissez ou mappez l'identifiant de la vue que vous souhaitez récupérer.</td> 
    </tr>
  </tbody>
</table>

#### Obtention des vues par type d’enregistrement (V2)

Ce module récupère une liste de vues pour le type d’enregistrement spécifique.

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
      <td>Sélectionnez l’espace de travail contenant les vues à récupérer.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Type d’enregistrement]</p>
      </td>
      <td>Sélectionnez le type d’enregistrement qui contient les vues à récupérer.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Nombre maximal de vues renvoyées]</p>
      </td>
      <td>Saisissez ou mappez le nombre maximal de vues que le module renverra au cours d’un cycle d’exécution.</td> 
    </tr>
  </tbody>
</table>

#### Mise à jour d’une vue (V2)

Ce module d&#39;action met à jour la vue spécifiée.

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
      <td>Sélectionnez l’espace de travail dans lequel vous souhaitez mettre à jour une vue.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Type d’enregistrement]</p>
      </td>
      <td>Sélectionnez le type d’enregistrement pour lequel vous souhaitez mettre à jour une vue.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>ID de vue</p>
      </td>
      <td>Sélectionnez la vue à mettre à jour.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Nom de la vue</p>
      </td>
      <td>Saisissez ou mappez un nom pour la nouvelle vue.</td> 
    </tr>
  </tbody>
</table>

### Autorisations (V2)

* [Ignorer les demandes d’accès](#dismiss-access-requests-v2)
* [Obtenir tous les membres et leurs rôles pour une ressource](#get-all-members-and-their-roles-for-a-resource-v2)
* [Obtenir les autorisations en vigueur de l’utilisateur actuel sur une ressource](#get-the-current-users-effective-permissions-on-a-resource-v2)
* [Liste des demandes d’accès en attente pour une ressource](#list-pending-access-requests-for-a-resource-v2)
* [Demande d’accès à une ressource](#request-access-to-a-resource-v2)

#### Ignorer les demandes d’accès (V2)

Ce module d&#39;action rejette une ou plusieurs demandes d&#39;accès, spécifiées par l&#39;ID.



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
        <p>[!UICONTROL Type de ressource]</p>
      </td>
      <td>Saisissez ou mappez l’identifiant du Workspace à supprimer.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Resource ID]</p>
      </td>
      <td>Saisissez ou mappez l’identifiant de la ressource pour laquelle vous souhaitez ignorer les demandes d’accès.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL ID de requête]</p>
      </td>
      <td>Pour chaque demande d’accès à ignorer, cliquez sur <b>Ajouter un élément</b> et saisissez l’ID de la demande.</td> 
    </tr>
  </tbody>
</table>

#### Récupérer tous les membres et leurs rôles pour une ressource (V2)

Ce module répertorie tous les utilisateurs, groupes et équipes qui ont une relation de partage explicite sur la ressource. Les informations d’identification utilisées dans la connexion pour ce module doivent disposer de l’autorisation Gérer sur la ressource.

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
        <p>[!UICONTROL Type de ressource]</p>
      </td>
      <td>Sélectionnez le type de ressource pour lequel vous souhaitez récupérer des informations.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Resource ID]</p>
      </td>
      <td>Saisissez ou mappez l’identifiant de la ressource pour laquelle vous souhaitez récupérer des informations.</td> 
    </tr>
  </tbody>
</table>

#### Obtenir les autorisations effectives de l’utilisateur actuel sur une ressource (V2)

Ce module renvoie les autorisations d’affichage, de modification, de suppression et d’ajout de l’utilisateur actuel pour une ressource donnée.

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
        <p>[!UICONTROL Type de ressource]</p>
      </td>
      <td>Sélectionnez le type de ressource pour lequel vous souhaitez récupérer des autorisations.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Resource ID]</p>
      </td>
      <td>Saisissez ou mappez l’identifiant de la ressource pour laquelle vous souhaitez récupérer les autorisations.</td> 
    </tr>
  </tbody>
</table>

#### Liste des demandes d’accès en attente pour une ressource (V2)

Ce module renvoie toutes les demandes d’accès en attente pour la ressource donnée.

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
        <p>[!UICONTROL Type de ressource]</p>
      </td>
      <td>Sélectionnez le type de ressource pour lequel vous souhaitez récupérer des informations.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Resource ID]</p>
      </td>
      <td>Saisissez ou mappez l’identifiant de la ressource pour laquelle vous souhaitez récupérer des informations.</td> 
    </tr>
  </tbody>
</table>

#### Demande d’accès à une ressource (V2)

Ce module crée ou met à jour une demande d&#39;accès pour l&#39;utilisateur actuel sur la ressource donnée.

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
        <p>[!UICONTROL Type de ressource]</p>
      </td>
      <td>Sélectionnez le type de ressource pour lequel vous souhaitez créer ou mettre à jour une demande d’accès.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Resource ID]</p>
      </td>
      <td>Saisissez ou mappez l’identifiant de la ressource pour laquelle vous souhaitez créer ou mettre à jour une demande d’accès.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Message]</p>
      </td>
      <td>Saisissez ou mappez le texte d’un message que vous souhaitez inclure dans la demande d’accès.</td> 
    </tr>
  </tbody>
</table>



### Autres (V2)

* [Obtention de l’ID d’authentification à partir de l’ID Workfront](#get-auth-id-from-workfront-id-v2)
* [Effectuer un appel API personnalisé](#make-a-custom-api-call-v2)
* [Surveiller les événements](#watch-events-v2)

#### Obtention de l’ID d’authentification à partir de l’ID Workfront (V2)

Ce module prend un ID utilisateur Workfront et renvoie l&#39;ID d&#39;autorisation correspondant utilisé par Planning.

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
        <p>[!UICONTROL Workfront User ID]</p>
      </td>
      <td>Saisissez ou mappez l’ID Workfront de l’utilisateur pour lequel vous souhaitez récupérer un ID d’autorisation.</td> 
    </tr>
  </tbody>
</table>

#### Effectuer un appel API personnalisé (V2)&lt;table

Ce module effectue un appel personnalisé à l’API Workfront Planning.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre application Workfront à Workfront Fusion, consultez <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connecter Workfront à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>Saisissez un chemin relatif vers <code> https://&lt;WORKFRONT_DOMAIN>/maestro/api/.</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL API Version]</td> 
   <td>Sélectionnez la version de l’API Workfront que vous souhaitez que le module utilise.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, consultez <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP dans Adobe Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard. Cela détermine le type de contenu de la requête.</p> <p>Par exemple,<code> {"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
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

#### Événements Espion (V2)

Ce module de déclenchement démarre un scénario lorsqu’un enregistrement, un type d’enregistrement ou un espace de travail est créé, mis à jour ou supprimé dans Workfront Planning.

>[!IMPORTANT]
>
>Vous pouvez modifier ce module ultérieurement. Le webhook sera modifié.
>
>Tenez compte des points suivants lors de la mise à jour d’un webhook :
>
>* Le webhook modifié est traité par les abonnements aux événements de Workfront comme un nouvel abonnement. L’historique des abonnements aux événements n’est pas conservé pour la configuration webhook précédente, car il est considéré comme un abonnement aux événements distinct.
>* Le passage de l’ancien au nouvel abonnement à un événement peut ne pas être parfaitement synchronisé. Il est donc possible de recevoir un événement deux fois (si le nouvel abonnement commence à s&#39;exécuter avant l&#39;arrêt de l&#39;ancien) ou de manquer un événement (si l&#39;ancien abonnement s&#39;arrête avant que le nouveau ne commence à s&#39;exécuter).
>
>Pour plus d’informations sur la modification des Webhooks, voir [Modifier les Webhooks](/help/workfront-fusion/manage-scenarios/edit-webhooks.md).

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
      <td role="rowheader">[!UICONTROL Objects to watch]</td>
      <td>Choisissez si vous souhaitez consulter les nouveaux enregistrements, les enregistrements mis à jour, les enregistrements nouveaux et mis à jour ou les enregistrements supprimés.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Type de configuration]</td>
      <td>Choisissez si vous souhaitez une configuration simple ou une configuration avancée. <p>Pour plus d’informations sur la configuration avancée, consultez <a href="#example-of-advanced-logic-in-the-watch-events-module" class="MCXref xref" >Exemple de logique avancée dans le module Événements de contrôle</a> dans cet article.</td>
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

Pour un exemple d’utilisation de la logique avancée sur ce module, voir [Exemple de logique avancée dans le module Événements de montre](#example-of-advanced-logic-in-the-watch-events-module).






## Modules [!DNL Adobe Workfront Planning] version 1 et leurs champs

>[!IMPORTANT]
>
>Les modules de cette section appartiennent au connecteur Workfront Planning V1.Pour les modules du connecteur Workfront Planning V2, consultez les modules [[!DNL Adobe Workfront Planning] Version 2 et leurs champs](#adobe-workfront-planning-version-2-modules-and-their-fields).

Lorsque vous configurez les modules de planification Workfront, Workfront Fusion affiche les champs répertoriés ci-dessous. Des champs Workfront supplémentaires peuvent s’afficher, selon votre niveau d’accès dans l’application ou le service, par exemple. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, consultez [Mappage d’informations d’un module à l’autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).


![Bouton (bascule) de mappage](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Déclencheurs](#triggers)
* [Actions](#actions)
* [Recherches](#searches)
* [Non classée](#uncategorized)

### Déclencheurs

#### Surveiller les événements

Ce module de déclenchement démarre un scénario lorsqu’un enregistrement, un type d’enregistrement ou un espace de travail est créé, mis à jour ou supprimé dans Workfront Planning.

>[!IMPORTANT]
>
>Vous pouvez modifier ce module ultérieurement. Le webhook sera modifié.
>
>Tenez compte des points suivants lors de la mise à jour d’un webhook :
>
>* Le webhook modifié est traité par les abonnements aux événements de Workfront comme un nouvel abonnement. L’historique des abonnements aux événements n’est pas conservé pour la configuration webhook précédente, car il est considéré comme un abonnement aux événements distinct.
>* Le passage de l’ancien au nouvel abonnement à un événement peut ne pas être parfaitement synchronisé. Il est donc possible de recevoir un événement deux fois (si le nouvel abonnement commence à s&#39;exécuter avant l&#39;arrêt de l&#39;ancien) ou de manquer un événement (si l&#39;ancien abonnement s&#39;arrête avant que le nouveau ne commence à s&#39;exécuter).
>
>Pour plus d’informations sur la modification des Webhooks, voir [Modifier les Webhooks](/help/workfront-fusion/manage-scenarios/edit-webhooks.md).

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

Pour un exemple d’utilisation de la logique avancée sur ce module, voir [Exemple de logique avancée dans le module Événements de montre](#example-of-advanced-logic-in-the-watch-events-module).

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

Ce module effectue un appel API personnalisé à l’API [!DNL Adobe Workfront Planning].

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
      <td>Pour chaque champ à utiliser dans votre recherche, recherchez ce champ, sélectionnez l’opérateur, puis saisissez ou mappez la valeur à rechercher. Les champs sont disponibles en fonction du type d’enregistrement sélectionné.</td> 
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
    <!--
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximum number of returned records]</p>
      </td>
      <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td>
    </tr>
    -->
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

## Exemple de logique avancée dans le module watch Events

Il s’agit d’un exemple du format pris par une logique avancée lors de l’utilisation du module Workfront Planning > Événements Espion .

```
[
  {
    "fieldName": "recordTypeId",
    "fieldValue": "Rt68c886502d4b5554ee80896b",
    "comparison": "eq",
    "state": "newState"
  },
  {
    "fieldName": "data",
    "fieldValue": {
      "F68c886502d4b5554ee808975": "planning"
    },
    "comparison": "eq",
    "state": "newState"
  },
  {
    "fieldName": "data",
    "fieldValue": {
      "F68c886502d4b5554ee808975": "active"
    },
    "comparison": "eq",
    "state": "newState"
  }
]
```

Tenez compte des points suivants lors de l’utilisation d’une logique avancée dans le module Événement de contrôle :

* La première entrée de `"fieldvalue":` est l’identifiant de type d’enregistrement Planning extrait de l’URL. Dans cet exemple, l&#39;ID de type d&#39;enregistrement Planning est `Rt68c886502d4b5554ee80896b`.
* Les données Planning sont renvoyées dans un tableau appelé `data `, qui apparaît dans cet exemple sous la forme `"fieldName": "data"`.
* Les fieldNames Planning sont renvoyés sous la forme d&#39;identifiants commençant par `F`.
* Comme cet exemple évalue un connecteur de filtre `OR`, il comporte deux entrées pour le même champ (`F68c886502d4b5554eec808975`).  Les deux options de liste déroulante en fonction desquelles le module effectue un filtrage sont `"planning"` et `"active"`.

