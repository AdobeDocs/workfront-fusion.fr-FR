---
title: Modules Datadog
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent Datadog et les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: c8c5f2e3-5af1-4957-bb6f-6c19c35102c5
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '954'
ht-degree: 62%

---

# Modules [!DNL Datadog]

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent [!DNL Datadog] et les connecter à plusieurs applications et services tiers.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tout package de workflow Adobe Workfront et tout package d’automatisation et d’intégration Adobe Workfront</p><p>Workfront Ultimate</p><p>les packages Workfront Prime et Select, avec un achat supplémentaire de Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licences Adobe Workfront</td> 
   <td> <p>Standard</p><p>Travail ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licence Adobe Workfront Fusion</td> 
   <td>
   <p>Basé sur les opérations : aucune exigence de licence Workfront Fusion</p>
   <p>Basé sur un connecteur (hérité) : Workfront Fusion pour l’automatisation et l’intégration du travail </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Si votre entreprise dispose d’un package Select ou Prime Workfront qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acheter Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Conditions préalables

Pour utiliser les modules [!DNL Datadog], vous devez disposer d’un compte [!DNL Datadog].

## Informations sur l’API Datadog

Le connecteur Datadog utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>1.0.11</td> 
  </tr>
 </tbody> 
 </table>

## Connecter [!DNL Datadog] à Workfront Fusion {#connect-datadog-to-workfront-fusion}

### Récupérer votre clé d’API et clé d’application {#retrieve-your-api-key-and-application-key}

Pour connecter votre compte [!DNL Datadog] à Workfront Fusion, vous devez récupérer une clé API et une clé d’application à partir de votre compte [!DNL Datadog].

1. Connectez-vous à votre compte [!DNL Datadog].
1. Dans le panneau de navigation de gauche, cliquez sur **[!UICONTROL Intégrations]**, puis sur **[!UICONTROL API]**.
1. Dans l’écran principal, cliquez sur **[!UICONTROL Clés d’API]**.
1. Pointez sur la barre violette pour faire apparaître la clé d’API.
1. Copiez la clé d’API dans un emplacement sécurisé.
1. Dans l’écran principal, cliquez sur **[!UICONTROL Clés d’application]**.
1. Pointez sur la barre violette pour faire apparaître la clé d’application.
1. Copiez la clé d’application dans un emplacement sécurisé.

### Création d’une connexion à [!DNL Datadog] dans Workfront Fusion

Vous pouvez créer une connexion à votre compte [!DNL Datadog] directement à partir d’un module [!UICONTROL Datadog].

1. Dans n’importe quel module [!UICONTROL Datadog], cliquez sur **[!UICONTROL Ajouter]** en regard du champ [!UICONTROL Connexion].
1. Remplissez les champs du module comme suit :

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection Name]</td> 
      <td> <p> Saisissez un nom pour la connexion.</p> </td> 
     </tr> 
        <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>Indiquez si cette connexion est destinée à un environnement de production ou hors production.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>Indiquez si vous vous connectez à un compte de service ou à un compte personnel.</td>
        </tr>
     <tr> 
      <td role="rowheader">[!UICONTROL Domain] </td> 
      <td> <p>Sélectionnez le domaine auquel vous souhaitez vous connecter (US ou UE).</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API Key Location] </td> 
      <td> <p>Indiquez si la clé API doit être incluse dans l’en-tête ou dans la chaîne de requête.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API Key]</td> 
      <td> <p> Saisissez votre clé d’API [!DNL Datadog]. </p> <p>Pour obtenir des instructions sur la récupération de la clé d’API, consultez <a href="#retrieve-your-api-key-and-application-key" class="MCXref xref">Récupérer votre clé d’API et votre clé d’application</a> dans cet article.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour créer la connexion et retourner au module.

## Modules [!DNL Datadog] et leurs champs

Lorsque vous configurez les modules [!DNL Datadog], Workfront Fusion affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Datadog] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Actions

* [[!UICONTROL Effectuer un appel API]](#make-an-api-call)
* [[!UICONTROL Publier les points de la série chronologique]](#post-timeseries-points)

#### [!UICONTROL Effectuer un appel API]

Ce module d’action vous permet d’effectuer un appel API personnalisé.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Datadog] à Workfront Fusion, voir <a href="#connect-datadog-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Datadog] à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Utiliser un domaine dédié]</td> 
   <td>Certains des points d’entrée de l’API Datadog qui s’attendent à un trafic entrant important s’exécutent sur leurs domaines dédiés. Cochez cette case pour utiliser le domaine dédié pour votre appel API.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Saisissez un chemin d’accès relatif à <code>https://api.datadoghq.com/api/</code>. Exemple :<code> /v1/org</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Méthodes de requête HTTP</a>.</p> </td> 
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
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre JSON, mettez les guillemets à l’extérieur de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple :** l’appel API suivant renvoie tous les tableaux de bord de votre compte [!DNL Datadog] :

URL : `/v1/dashboard`

Méthode : `GET`

![Exemple d’appel API Datadog](/help/workfront-fusion/references/apps-and-modules/assets/datadog-api-example.png)

Le résultat se trouve dans la sortie du module sous Offre spéciale > Corps > Tableaux de bord.

Dans notre exemple, 3 tableaux de bord ont été renvoyés :

![Réponse de l’API Datadog](/help/workfront-fusion/references/apps-and-modules/assets/datadog-api-response-example.png)

#### [!UICONTROL Publier les points de la série chronologique]

Le module vous permet d’afficher des données de séries chronologiques qui peuvent être représentées sur les tableaux de bord de [!DNL Datadog].

La limite pour les payloads compressées est de 3,2 mégaoctets (3 200 000), et de 62 mégaoctets (62 914 560) pour les payloads décompressées.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Datadog] à Workfront Fusion, voir <a href="#connect-datadog-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Datadog] à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td> Sélectionnez le type de mesure à utiliser. 
   <ul>
   <li>Jauge</li>
   <li>Taux</li>
   <li>Nombre</li>
   </ul>
   </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL Interval]</td> 
   <td> Si le type de mesure est un taux ou un comptage, définissez l’intervalle correspondant.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Points]</td> 
   <td><p>Ajoutez des points relatifs à une mesure.</p> <p>Il s’agit d’un tableau de points JSON. Chaque point a le format suivant : <code>[[POSIX_timestamp, numeric_value], ...] </code></p> <p>Note :  <p>L’horodatage doit être exprimé en secondes.</p> <p>L’horodatage doit être actuel. Le paramètre Actuel est défini sous forme de période n’allant pas au-delà de 10 minutes dans le futur ou d’une heure dans le passé.</p> <p> Le format de la valeur numérique doit être une valeur flottante.</p> </p> <p>Ce champ doit contenir au moins 1 élément.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Host]</td> 
   <td>Entrez le nom de l’hôte qui a produit la mesure. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td> Pour chaque balise à ajouter à la mesure, cliquez sur <b>Ajouter un élément</b> et saisissez la valeur de la balise.</td> 
  </tr> 
 </tbody> 
</table>
