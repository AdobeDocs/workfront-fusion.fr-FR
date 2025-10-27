---
title: Modules Adobe Workfront
description: Vous pouvez utiliser le connecteur Adobe Workfront Fusion Adobe Workfront pour automatiser vos processus dans Workfront. Si vous disposez d’une licence Workfront Fusion pour l’automatisation et l’intégration du travail, vous pouvez également l’utiliser pour vous connecter à des applications et services tiers.
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: 93c27cf6-38b0-466c-87bb-926c4817eae7
source-git-commit: d2c873ffec406ae343fbcc72246688dec0bd1eab
workflow-type: tm+mt
source-wordcount: '7373'
ht-degree: 55%

---

# Modules Adobe Workfront

>[!IMPORTANT]
>
>Cet article contient des instructions pour la nouvelle version du connecteur Workfront, publiée le 22 octobre 2025. Ce nouveau connecteur reflète les modifications apportées à l’API Workfront.
>
>Le nouveau connecteur s’appelle « Workfront » et le connecteur précédemment disponible s’appelle « Workfront (hérité) ».
>
>Nous vous recommandons de :
>
>* Utilisation du nouveau connecteur lors de la création ou de la mise à jour d’un scénario.
>* Mise à niveau des modules existants vers le nouveau connecteur.
>
>Pour obtenir des instructions sur la mise à niveau de modules existants, voir [Mettre à niveau un module Workfront vers une nouvelle version](/help/workfront-fusion/manage-scenarios/update-module-to-new-version.md) dans l’article Mettre à niveau un module vers une nouvelle version.
>
>Pour plus d’informations sur les raisons pour lesquelles un nouveau connecteur est parfois nécessaire, consultez [Présentation des API dans Fusion](/help/workfront-fusion/get-started-with-fusion/understand-fusion/api-overview.md).

Vous pouvez utiliser le connecteur Adobe Workfront Fusion Adobe Workfront pour automatiser vos processus dans Workfront. Vous pouvez également connecter Workfront à d’autres applications et services.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <p>Héritée : n’importe laquelle. </p>
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

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).


>[!NOTE]
>
>* Si votre entreprise utilise l’ancien package de licence (basé sur les connecteurs), elle doit disposer d’une licence Workfront Fusion for Work Automation and Integration pour se connecter à des applications et services tiers. Le connecteur Workfront n’est pas comptabilisé par rapport au nombre d’applications actives disponibles pour votre organisation. Tous les scénarios, même s’ils utilisent uniquement l’application Workfront, sont comptés par rapport au nombre total de scénarios de votre organisation.

+++

## Connexion de Workfront à Workfront Fusion

Le connecteur Workfront utilise OAuth 2.0 pour se connecter à Workfront.

Vous pouvez créer une connexion à votre compte Workfront directement depuis un module Workfront Fusion.

* [Connexion à Workfront à l’aide de l’ID client et du secret client](#connect-to-workfront-using-client-id-and-client-secret)
* [Connexion à Workfront à l’aide d’une connexion serveur à serveur](#connect-to-workfront-using-a-server-to-server-connection)

### Connexion à Workfront à l’aide de l’ID client et du secret client

1. Dans un module Adobe Workfront, cliquez sur **Ajouter** en regard du champ Connexion.
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
          <p>Sélectionnez <b>Connexion d’authentification Adobe Workfront</b>.</p>
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
        <td>Saisissez votre identifiant client Workfront. Vous pouvez le trouver dans la zone Applications OAuth2 de la configuration de Workfront. Ouvrez l’application spécifique à laquelle vous vous connectez pour afficher l’ID client.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Saisissez votre secret client Workfront. Vous pouvez le trouver dans la zone Applications OAuth2 de la configuration de Workfront. Si vous ne disposez pas d’un secret client pour votre application OAuth2 dans Workfront, vous pouvez en générer un autre. Pour plus d’informations, consultez la documentation de Workfront.</td>
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

   Si vous n’êtes pas connecté à Workfront, vous êtes redirigé vers un écran de connexion. Après vous être connecté, vous pouvez autoriser la connexion.

>[!NOTE]
>
>* Les connexions OAuth 2.0 à l’API Workfront ne dépendent plus des clés API.
>* Pour créer une connexion à un environnement Workfront Sandbox, vous devez créer une application OAuth2 dans cet environnement, puis utiliser l’ID client et le secret client générés par cette application dans votre connexion.

### Connexion à Workfront à l’aide d’une connexion serveur à serveur

1. Dans un module Adobe Workfront, cliquez sur **Ajouter** en regard du champ Connexion.
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
          <p>Sélectionnez <b>Connexion serveur à serveur Adobe Workfront</b>.</p>
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
          <p>Saisissez le nom de votre instance, également appelée votre domaine.</p><p>Exemple : si votre URL est <code>https://example.my.workfront.com</code>, saisissez <code>example</code>.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Instance lane]</td>
        <td>
          <p>Saisissez le type d’environnement auquel cette connexion se connectera.</p><p>Exemple : si votre URL est <code>https://example.my.workfront.com</code>, saisissez <code>my</code>.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Saisissez votre identifiant client Workfront. Vous pouvez le trouver dans la zone Applications OAuth2 de la configuration de Workfront. Ouvrez l’application spécifique à laquelle vous vous connectez pour afficher l’ID client.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Saisissez votre secret client Workfront. Vous pouvez le trouver dans la zone Applications OAuth2 de la configuration de Workfront. Si vous ne disposez pas d’un secret client pour votre application OAuth2 dans Workfront, vous pouvez en générer un autre. Pour plus d’informations, consultez la documentation de Workfront.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Scopes]</td>
        <td>Saisissez toutes les portées applicables pour cette connexion.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Host prefix]</td>
        <td>Dans la plupart des cas, cette valeur doit être <code>origin</code>.
      </tr>
    </tbody>
    </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour enregistrer la connexion et revenir au module.

   Si vous n’êtes pas connecté à Workfront, vous êtes redirigé vers un écran de connexion. Après vous être connecté, vous pouvez autoriser la connexion.

>[!NOTE]
>
>* Les connexions OAuth 2.0 à l’API Workfront ne dépendent plus des clés API.
>* Pour créer une connexion à un environnement Workfront Sandbox, vous devez créer une application OAuth2 dans cet environnement, puis utiliser l’ID client et le secret client générés par cette application dans votre connexion.

## Modules Workfront et leurs champs

Lorsque vous configurez des modules Workfront, Workfront Fusion affiche les champs répertoriés ci-dessous. D’autres champs Workfront peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).


![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>* Si vous ne voyez pas les champs les plus à jour dans un module Workfront, cela peut être dû à des problèmes de mise en cache. Patientez une heure et réessayez.
>* Les codes d’état HTTP 429 d’Adobe Workfront ne doivent pas provoquer de désactivations, mais déclencher une courte pause dans l’exécution du scénario.

* [Déclencheurs](#triggers)
* [Actions](#actions)
* [Recherches](#searches)

### Déclencheurs

<!--
* [Watch Events](#watch-events) 
* [Watch Record](#watch-record) 
* [Watch Field](#watch-field)
-->

+++ **[!UICONTROL Surveiller les événements]**

Ce module déclencheur exécute un scénario en temps réel lorsque des objets d’un type spécifique sont ajoutés, mis à jour ou supprimés dans Workfront.

Le module renvoie tous les champs standard associés à l’enregistrement, ainsi que tous les champs et valeurs personnalisés auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

1. Cliquez sur **[!UICONTROL Ajouter]** à droite de la zone **Webhook**.

1. Configurez le webhook dans la zone **[!UICONTROL Ajouter un hook]** qui s’affiche.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Webhook name]</td> 
      <td>Saisissez un nom pour le webhook.</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Connection]</td> 
      <td> <p>Pour plus d’informations sur la connexion de votre application Workfront à Workfront Fusion, voir <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connexion de Workfront à Workfront Fusion</a> dans cet article.</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Record Type]</td> 
      <td>Sélectionnez le type d’enregistrement Workfront que vous souhaitez que le module regarde.</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL State]</td> 
      <td>Indiquez si vous souhaitez surveiller l’ancien ou le nouvel état.<ul><li><p><b>[!UICONTROL New state]</b></p><p>Déclenchez un scénario lorsque l’enregistrement <b>prend</b> une valeur donnée.</p><p>Par exemple, si l’état est défini sur [!UICONTROL New State] et que le filtre est défini sur [!UICONTROL Status] [!UICONTROL Equals] [!UICONTROL In Progress], le webhook déclenche un scénario lorsque le [!UICONTROL Status] passe à [!UICONTROL In Progress], quel que soit le statut antérieur. </p></li><li><p><b>[!UICONTROL Old state]</b></p><p>Déclenchez un scénario lorsque l’enregistrement <b>quitte</b> une valeur donnée.</p><p>Par exemple, si l’état est défini sur [!UICONTROL Old State] et que le filtre est défini sur [!UICONTROL Status] [!UICONTROL Equals] [!UICONTROL In Progress], le webhook déclenche un scénario lorsqu’un [!UICONTROL Status], qui est actuellement [!UICONTROL In Progress] passe à un autre statut. </p></li></ul></td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL Events filters]</p> </td> 
      <td> <p>Vous pouvez définir des filtres pour ne surveiller que les enregistrements qui répondent aux critères sélectionnés.</p> <p>Pour chaque filtre, saisissez le champ que le filtre doit évaluer, l’opérateur et la valeur que le filtre doit autoriser. Vous pouvez utiliser plusieurs filtres en ajoutant des règles ET.</p> <p><b>REMARQUE </b> : vous ne pouvez pas modifier les filtres dans les Webhooks Workfront existants. Pour configurer différents filtres pour les abonnements aux événements Workfront, supprimez le webhook actif et créez-en un.</p> <p>Pour plus d’informations sur les filtres d’événement, consultez la section <a href="#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref"> Filtres d’abonnement aux événements dans les modules Workfront &gt; [!UICONTROL Watch Events]</a> dans cet article.</p> </td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td>Exclure les événements créés par cette connexion</td> 
      <td>Activez cette option pour exclure les événements créés ou mis à jour à l’aide du même connecteur que celui utilisé par ce module de déclenchement. Cela peut empêcher qu’un scénario se déclenche lui-même et se répète en une boucle sans fin.<p><b>REMARQUE </b> : le type d'enregistrement Affectation n'inclut pas cette option.</p></td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Record Origin]</td> 
      <td>
       <p>Choisissez si vous souhaitez que le scénario regarde [!UICONTROL Nouveaux enregistrements uniquement], [!UICONTROL Enregistrements mis à jour uniquement], [!UICONTROL Enregistrements nouveaux et mis à jour] ou [!DNL Deleted Records Only].</p>
       <p><b>REMARQUE </b> : si vous choisissez [!UICONTROL Enregistrements nouveaux et mis à jour], la création du webhook crée 2 abonnements aux événements (pour la même adresse webhook).</p>
       </td> 
     </tr> 
    </tbody> 
   </table>



   <!--Markdown 0032 placeholder-->

Une fois le webhook créé, vous pouvez afficher l’adresse du point d’entrée auquel les événements sont envoyés.

Pour plus d’informations, consultez la section [Exemples de payloads d’événement](https://experienceleague.adobe.com/fr/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-api#examples-of-event-payloads) dans l’article API d’abonnement aux événements dans la documentation de Workfront.

Consultez une liste des types d’objets Workfront pour lesquels vous pouvez utiliser ce module dans [Types d’objets Workfront disponibles pour chaque module Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Champ de contrôle]**

Ce module de déclenchement exécute un scénario lorsqu’un champ que vous spécifiez est mis à jour. Le module renvoie l’ancienne et la nouvelle valeur du champ spécifié. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre application Workfront à Workfront Fusion, voir <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connexion de Workfront à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement Workfront que vous souhaitez que le module regarde.</p> <p>Par exemple, sélectionnez [!UICONTROL Task] si vous souhaitez commencer à exécuter le scénario chaque fois qu’un champ d’enregistrement est mis à jour dans une tâche.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Field]</td> 
   <td>Sélectionnez le champ que le module doit surveiller pour les mises à jour. Ces champs reflètent les champs que votre administrateur Workfront a configurés pour le suivi.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Outputs]</td> 
   <td>Sélectionnez les champs d’objet à inclure dans le lot de sortie pour ce module.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

Consultez une liste des types d’objets Workfront pour lesquels vous pouvez utiliser ce module dans [Types d’objets Workfront disponibles pour chaque module Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Enregistrement de contrôle]**

Ce module déclencheur exécute un scénario lorsque des objets d’un type spécifique sont ajoutés, mis à jour ou les deux. Le module renvoie tous les champs standard associés à l’enregistrement ou aux enregistrements, ainsi que les champs et valeurs personnalisés auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Dans la sortie, le module indique si chaque enregistrement est nouveau ou mis à jour.

Les enregistrements qui ont été ajoutés et mis à jour depuis la dernière exécution du scénario sont renvoyés en tant que nouveaux enregistrements.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre application Workfront à Workfront Fusion, voir <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connexion de Workfront à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Choisissez si vous souhaitez que le scénario regarde [!UICONTROL Nouveaux enregistrements uniquement], [!UICONTROL Enregistrements mis à jour uniquement] ou [!UICONTROL Enregistrements nouveaux et mis à jour].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement Workfront que vous souhaitez que le module regarde.</p> <p>Par exemple, si vous souhaitez lancer le scénario chaque fois qu’un nouveau projet est créé, sélectionnez [!UICONTROL Project].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Sélectionnez les champs à inclure dans le lot de sortie pour ce module.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reference]</td> 
   <td> <p>Sélectionnez les champs de référence à inclure dans le lot de sortie pour ce module.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Sélectionnez les champs de collection à inclure dans le lot de sortie pour ce module.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Optional Filter]</td> 
   <td> <p>(Avancé) Saisissez une chaîne de code API pour définir des paramètres ou du code supplémentaires qui affineront vos critères. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

Consultez une liste des types d’objets Workfront pour lesquels vous pouvez utiliser ce module dans [Types d’objets Workfront disponibles pour chaque module Workfront](#workfront-object-types-available-for-each-workfront-module).

+++


### Actions

<!--
* [Convert object](#convert-object) 
* [Create a record (attaching custom forms)](#create-a-record-attaching-custom-forms) 
* [Create a record](#create-a-record) 
* [Custom API Call](#custom-api-call) 
* [Delete Record](#delete-record) 
* [Download Document](#download-document) 
* [Misc Action](#misc-action) 
* [Read a Record](#read-a-record) 
* [Update Record](#update-record) 
* [Upload Document](#upload-document)
-->

+++ **[!UICONTROL Convertir un objet]**

Ce module d’action effectue l’une des conversions suivantes :

* Convertir un problème en projet
* Convertir un problème en tâche
* Convertir une tâche en projet

>[!NOTE]
>
>Depuis juillet 2024, les formulaires personnalisés peuvent être inclus lors de la conversion d’un objet.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre application Workfront à Workfront Fusion, voir <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connexion de Workfront à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Object type]</td> 
   <td> <p>Sélectionnez le type d’objet à convertir. Il s’agit du type dont dispose l’objet avant la conversion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Convert to]</td> 
   <td>Sélectionnez l’objet dans lequel vous souhaitez le convertir. Il s’agit du type de l’objet après la conversion.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL &lt;Object&gt; ID]</td> 
   <td> <p>Saisissez l’ID de l’objet. </p> <p>Remarque : lorsque vous saisissez l’identifiant d’un objet, vous pouvez commencer à saisir son nom, puis le sélectionner dans la liste. Le module saisit ensuite l’ID approprié dans le champ.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Template ID]</td> 
   <td> <p>Si vous effectuez une conversion vers un projet, sélectionnez l’ID de modèle à utiliser pour le projet.</p> <p>Remarque : lorsque vous saisissez l’identifiant d’un objet, vous pouvez commencer à saisir son nom, puis le sélectionner dans la liste. Le module saisit ensuite l’ID approprié dans le champ.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Custom forms]</td> 
   <td>Sélectionnez les formulaires personnalisés à ajouter à l’objet nouvellement converti, puis saisissez les valeurs des champs du formulaire personnalisé.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Options]</td> 
   <td> <p>Activez les options souhaitées lors de la conversion de l’objet. Des options sont disponibles selon l’objet que vous convertissez ou à partir duquel vous effectuez cette conversion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Copy native fields]</td> 
   <td> <p>Activez cette option pour copier les champs natifs de l’objet d’origine vers le nouvel objet.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Copy custom forms]</td> 
   <td> <p>Activez cette option pour copier les champs natifs de l’objet d’origine vers le nouvel objet.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Créer un enregistrement]** 

Ce module d’action crée un objet, tel qu’un projet, une tâche ou un événement dans Workfront, et vous permet d’ajouter un formulaire personnalisé au nouvel objet. Le module vous permet de sélectionner les champs de l’objet disponibles dans le module.

Vous indiquez l’ID de l’enregistrement.

Le module renvoie l’ID de l’enregistrement et tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Veillez à indiquer le nombre minimum de champs de saisie. Par exemple, si vous souhaitez créer un problème, vous devez fournir un identifiant de projet parent valide dans le champ d’identifiant de projet pour indiquer l’emplacement du problème dans Workfront. Vous pouvez utiliser le panneau de mappage pour mapper ces informations à partir d’un autre module dans votre scénario, ou vous pouvez les saisir manuellement en saisissant le nom, puis en le sélectionnant dans la liste.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre application Workfront à Workfront Fusion, voir <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connexion de Workfront à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement Workfront que vous souhaitez que le module crée.</p> <p>Par exemple, si vous souhaitez créer un projet, sélectionnez [!UICONTROL Project] dans la liste déroulante.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Select fields to map]</td> 
   <td> <p>Sélectionnez les champs qui doivent être disponibles pour la saisie de données. Vous pouvez ainsi utiliser ces champs sans avoir à faire défiler ceux dont vous n’avez pas besoin. Vous pouvez ensuite saisir ou mapper des données dans ces champs.</p> <p>Pour les champs des formulaires personnalisés, utilisez le champ <b>[!UICONTROL Attach Custom Form]</b>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Attach Custom Form]</td> 
   <td>Sélectionnez les formulaires personnalisés que vous souhaitez ajouter au nouvel objet, sélectionnez les champs pour lesquels vous souhaitez saisir des valeurs, puis saisissez ou mappez des valeurs pour ces champs.</td> 
  </tr> 
 </tbody> 
</table>

Consultez une liste des types d’objets Workfront pour lesquels vous pouvez utiliser ce module dans [Types d’objets Workfront disponibles pour chaque module Workfront](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* Lorsque vous saisissez l’ID d’un objet, vous pouvez commencer à saisir son nom, puis le sélectionner dans la liste. Le module saisit ensuite l’ID approprié dans le champ.
>* Lors de la saisie du texte d’un champ personnalisé ou d’un objet [!UICONTROL Note] (commentaire ou réponse), vous pouvez utiliser des balises HTML dans le champ [!UICONTROL Texte de la note] pour créer du texte enrichi, comme du texte en gras ou en italique.
>



>[!NOTE]
>
>Les utilisateurs sont créés avec le statut Désactivé et Approbation en attente . Si votre organisation a été migrée vers Adobe Admin Console et que le badge Approbation en attente n’est pas supprimé dans les minutes qui suivent, vous pouvez approuver l’utilisateur.
>
>* **Résoudre le problème des utilisateurs individuels**
>
>      Vous pouvez valider des utilisateurs et utilisatrices individuels dans la liste Utilisateurs et utilisatrices.
>
>      1. Sélectionnez la ou les personnes dans la liste Utilisateurs et utilisatrices.
>      1. Cliquez sur le menu à trois points dans l’en-tête de la liste.
>      1. Sélectionnez **Approuver**.
>      1. Après quelques minutes, actualisez la page.
>
>* **Résoudre les utilisateurs ajoutés dans un grand lot**
>
>   Pour valider les utilisateurs et utilisatrices ajoutés dans un lot volumineux, vous pouvez ajouter ce lot de personnes directement dans Adobe Admin Console.
>
>   Pour obtenir des instructions, voir la section [Gérer plusieurs utilisateurs et utilisatrices | Chargement CSV en masse](https://helpx.adobe.com/fr/enterprise/using/bulk-upload-users.html?lang=fr) dans la documentation Adobe.

+++

<!--

+++ **[!UICONTROL Create Record (Legacy)]**

>[!IMPORTANT]
>
>This module has been replaced with the Create a record module. We recommend using that module in new scenarios.
>Existing scenarios that use this module will continue to function as expected. This module will be removed from the module selector in May 2025.

This action module creates an object, such as a project, task, or issue in Workfront. The module allows you to select which of the object's fields are available in the module.

You specify the ID of the record.

The module returns the ID of the  record and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

Make sure you provide the minimum number of input fields. For example, if you want to create an issue, you need to provide a valid parent project ID in the Project ID field to indicate where the issue should live in Workfront. You can use the mapping panel to map this information from another module in your scenario, or you can enter it manually by typing in the name and then selecting it from the list.

This module does not attach custom forms when creating the object. To attach custom forms while creating an object, use the [!UICONTROL Create a record (attaching custom forms)] module.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to create.</p> <p>For example, if you want to create a Project, select [!UICONTROL Project] from the dropdown list.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Select fields to map]</td> 
   <td>Select the fields that you want available for data input. This allows you to use these fields without having to scroll through the ones you don't need.</td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* When entering the ID of an object, you can begin typing the name of the object, then select it from the list. The module then enters the appropriate ID into the field.
>* When entering the text for a custom field or a [!UICONTROL Note] object (Comment or reply), you can use HTML tags in the [!UICONTROL Note Text] field to create rich text, such as bold or italic text.

+++

-->

+++ **[!UICONTROL Appel API personnalisé]**

Ce module d’action vous permet d’effectuer un appel authentifié personnalisé vers l’API Workfront. De cette façon, vous pouvez automatiser les flux de données, ce que ne peuvent pas faire les autres modules de Workfront.

Le module renvoie les informations suivantes :

* **[!UICONTROL Code d’état]** (nombre) : indique la réussite ou l’échec de votre requête HTTP. Ce sont des codes standard que vous pouvez consulter sur Internet.
* **[!UICONTROL En-têtes]** (objet) : contexte plus détaillé pour le code de réponse/d’état qui ne se rapporte pas au corps de sortie. Tous les en-têtes qui apparaissent dans un en-tête de réponse ne sont pas des en-têtes de réponse. Certains peuvent donc ne pas vous être utiles.

  Les en-têtes de réponse dépendent de la requête HTTP que vous avez choisie lors de la configuration du module.

* **[!UICONTROL Corps]** (objet) : selon la requête HTTP que vous avez choisie lors de la configuration du module, vous pouvez recevoir des données en retour. Ces données, telles que les données d’une requête GET, sont contenues dans cet objet.

Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre application Workfront à Workfront Fusion, voir <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connexion de Workfront à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>Saisissez un chemin relatif vers <code> https://&lt;WORKFRONT_DOMAIN&gt;/attask/api/&lt;API_VERSION&gt;/</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL API Version]</td> 
   <td>Sélectionnez la version de l’API Workfront que le module doit utiliser.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP dans Adobe Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard. Cela détermine le type de contenu de la requête.</p> <p>Par exemple,<code> {"Content-type":"application/json"}</code></p> <p>Remarque : si vous obtenez des erreurs et qu’il est difficile de déterminer leur origine, pensez à modifier les en-têtes en vous basant sur la documentation de Workfront. Si votre appel API personnalisé renvoie une erreur de requête HTTP 422, essayez d’utiliser un en-tête <code>"Content-Type":"text/plain"</code>.</p> </td> 
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

Consultez une liste des types d’objets Workfront pour lesquels vous pouvez utiliser ce module dans [Types d’objets Workfront disponibles pour chaque module Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

+++ **[!UICONTROL Supprimer l’enregistrement]**

Ce module d’action supprime un objet, tel qu’un projet, une tâche ou un problème dans Workfront.

Vous indiquez l’ID de l’enregistrement.

Le module renvoie l’ID de l’enregistrement et tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre application Workfront à Workfront Fusion, voir <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connexion de Workfront à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Force delete]</td> 
   <td>Activez cette option pour vous assurer que l’enregistrement est supprimé, même si l’interface utilisateur de Workfront demande confirmation de la suppression.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Async delete]</td> 
   <td>Activez cette option pour permettre au module d’effectuer une suppression asynchrone.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>ID</td> 
   <td> <p>Saisissez l’ID Workfront unique de l’enregistrement que le module doit supprimer.</p> <p>Pour obtenir l’identifiant, ouvrez l’objet Workfront dans votre navigateur et copiez le texte à la fin de l’URL après « ID= ». Par exemple : https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td>Sélectionnez le type d’enregistrement Workfront que vous souhaitez que le module supprime.</td> 
  </tr> 
 </tbody> 
</table>

Consultez une liste des types d’objets Workfront pour lesquels vous pouvez utiliser ce module dans [Types d’objets Workfront disponibles pour chaque module Workfront](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>Nous vous recommandons de configurer le scénario suivant pour éviter que les enregistrements ne soient supprimés en raison d’opérations asynchrones.
>
>1. Supprimez l’enregistrement de manière synchrone.
>1. Ajoutez la gestion des erreurs au module Supprimer l’enregistrement pour ignorer l’erreur provoquée par le délai d’expiration de 40 secondes.


+++

+++ **[!UICONTROL Télécharger un document]**

Ce module d’action permet de télécharger un document à partir de Workfront.

Vous indiquez l’ID de l’enregistrement.

Le module renvoie le contenu, le nom, l’extension et la taille de fichier du document. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre application Workfront à Workfront Fusion, voir <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connexion de Workfront à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Document ID]</td> 
   <td> <p>Mappez ou saisissez manuellement l’ID Workfront unique du document que le module doit télécharger.</p> <p>Pour obtenir l’identifiant, ouvrez l’objet Workfront dans votre navigateur et copiez le texte à la fin de l’URL après « ID= ». Par exemple : https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

Consultez une liste des types d’objets Workfront pour lesquels vous pouvez utiliser ce module dans [Types d’objets Workfront disponibles pour chaque module Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

### **Obtenir une URL de fichier prédéfinie**

Ce module d’action reçoit des URL de fichier prédéfinies qui peuvent être utilisées ultérieurement par d’autres API.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre application Workfront à Workfront Fusion, voir <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connexion de Workfront à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Document ID]</td> 
   <td> <p>Mappez ou saisissez manuellement l’ID Workfront unique du document pour lequel vous souhaitez obtenir une URL prédéfinie.</p> <p>Pour obtenir l’identifiant, ouvrez l’objet Workfront dans votre navigateur et copiez le texte à la fin de l’URL après « ID= ». Par exemple : https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Time to URL expiration]</td> 
   <td> <p>Saisissez ou mappez le nombre de minutes pendant lesquelles cette URL existera avant son expiration. La valeur par défaut est de 1 minute.</p><p>Pour modifier cette valeur, ce paramètre doit être activé par l’équipe Workfront Fusion. Si elle n’est pas activée, la valeur reste égale à 1 minute, quel que soit le nombre que vous avez saisi.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++ **[!UICONTROL Actions diverses]**

Ce module d’action vous permet d’effectuer des actions sur l’API.

>[!NOTE]
>
>Depuis juillet 2024, l’action `convertToProject` inclut les `copyCategories` de terrain. Lorsque la valeur est définie sur `TRUE`, tous les formulaires personnalisés sont inclus dans le projet dans lequel le problème est converti.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre application Workfront à Workfront Fusion, voir <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connexion de Workfront à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement Workfront avec lequel vous souhaitez que le module interagisse.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Action]</td> 
   <td> <p>Sélectionnez l’action que le module doit exécuter.</p> <p>Vous devrez peut-être remplir des champs supplémentaires, en fonction du [!UICONTROL Record Type] et de l’[!UICONTROL Action] que vous choisissez. Certaines combinaisons de ces deux paramètres peuvent ne nécessiter qu’un ID d’enregistrement, tandis que d’autres (telles que Projet pour le <strong>[!UICONTROL Record Type]</strong> et le [!UICONTROL Attach Template] pour l’<strong>[!UICONTROL Action]</strong>) requièrent des informations supplémentaires (comme un ID d’objet et un ID de modèle).</p><p>Pour connaître les options disponibles pour certaines actions, reportez-vous à la section <a href="#misc-action-options" class="MCXref xref">Options d’action diverses</a> de cet article.</p> <p>Pour plus d’informations sur les champs individuels, consultez la section <a href="http://developer.workfront.com/">Documentation destinée à l’équipe de développement de Workfront</a>. <p><strong>Note</strong> : le site de documentation destinée à l’équipe de développement contient uniquement des informations jusqu’à la version 14 de l’API. Il inclut néanmoins des informations précieuses pour les appels API. </p> 
    <ol> 
     <li value="1"> <p>Sélectionnez le type d’enregistrement dans le volet de navigation de gauche de la page de documentation destinée aux développeurs de Workfront. Les types suivants possèdent leurs propres pages :</p> 
      <ul> 
       <li> <p>[!UICONTROL Projects]</p> </li> 
       <li> <p>[!UICONTROL Tasks]</p> </li> 
       <li> <p>[!UICONTROL Issues]</p> </li> 
       <li> <p>[!UICONTROL Users]</p> </li> 
       <li> <p>[!UICONTROL Documents]</p> </li> 
      </ul> <p>Pour tous les autres types d’enregistrement, sélectionnez <b>[!UICONTROL Other objects and endpoints]</b> et recherchez le type d’enregistrement sur les pages triées par ordre alphabétique.</p> </li> 
     <li value="2"> <p>Sur la page du type d’enregistrement approprié, recherchez l’action (Ctrl+F ou Cmd+F).</p> </li> 
     <li value="3"> <p>Affichez les descriptions des champs disponibles sous l’action sélectionnée.</p> </li> 
    </ol> <p>Note :  <p>Lors de la création d’une épreuve par le biais du module Workfront [!UICONTROL Misc Action] , il est recommandé de créer une épreuve sans option avancée, puis de la mettre à jour à l’aide de l’API SOAP [!DNL Workfront Proof].</p><p>Pour plus d'informations sur la création d'un BAT avec l'API Workfront (que ce module utilise), voir <a href="https://experienceleague.adobe.com/fr/docs/workfront/using/adobe-workfront-api/tips-troubleshooting-apis/api-create-proof-options-json" class="MCXref xref">Ajouter des options de relecture avancée lors de la création d'un BAT via l'API Adobe Workfront</a></p> </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td>Saisissez ou mappez l’ID Workfront unique de l’enregistrement avec lequel vous souhaitez que le module interagisse.<p>Pour obtenir l’identifiant, ouvrez l’objet Workfront dans votre navigateur et copiez le texte à la fin de l’URL après « ID= ». Par exemple : https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p></td> 
  </tr> 
 </tbody> 
</table>

Consultez une liste des types d’objets Workfront pour lesquels vous pouvez utiliser ce module dans [Types d’objets Workfront disponibles pour chaque module Workfront](#workfront-object-types-available-for-each-workfront-module).

#### Options d’action diverses

##### Tâche

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>Action</th> 
   <th>Options</th> 
  </tr> 
  <tr> 
   <td>Copier</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearConstraints</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>Efface les données financières</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>Efface les notifications de rappel</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>Déplacer</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearDocuments</li>
   <li>clearConstraints</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>Efface les données financières</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>Efface les notifications de rappel</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

##### Problème

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>Action</th> 
   <th>Options</th> 
  </tr> 
  <tr> 
   <td>Copier</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearPermissions</li>
   <li>clearProgress</li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>Convertir en une tâche</td> 
   <td>
   <ul>
   <li>preserveIssue<p>Conserver l'événement d'origine et lier sa résolution à cette tâche</p></li>
   <li>preservePrimaryContact<p>Autoriser le créateur de l'événement à accéder à cette tâche</p></li>
   <li>preserveCompletionDate<p>Conserver la date d'achèvement prévue pour l'événement</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>Convertir en projet</td> 
   <td>
   <ul>
   <li>preserveIssue<p>Conserver l'événement d'origine et lier sa résolution à cette tâche</p></li>
   <li>preservePrimaryContact<p>Autoriser le créateur de l'événement à accéder à cette tâche</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



##### Projet

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>Action</th> 
   <th>Options</th> 
  </tr> 
  <tr> 
   <td>Copier</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>Efface les données financières</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>Efface les notifications de rappel</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>Joindre un modèle / Enregistrer comme modèle</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearBillingRates</li>
   <li>clearConstraints</li>
   <li>clearDeliverables<p>Efface les objectifs</p></li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>Efface les données financières</p></li>
   <li>clearHourTypes</li>
   <li>clearIssueSetup<p>Efface les propriétés de file d'attente et la configuration des événements</p></li>
   <li>clearPredecessors</li>
   <li>clearRisks</li>
   <li>clearSharingOptions</li>
   <li>clearTimedNotifications<p>Efface les notifications de rappel</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



+++

+++ **[!UICONTROL Lire un enregistrement]**

Ce module d’action récupère les données d’un seul enregistrement.

Vous indiquez l’ID de l’enregistrement. Vous pouvez également spécifier les enregistrements associés que le module doit lire.

Par exemple, si l’enregistrement que le module est en train de lire est un projet, vous pouvez spécifier que vous souhaitez que les tâches du projet soient lues.

Le module renvoie un tableau de données des champs de sortie que vous avez spécifiés.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>Pour plus d’informations sur la connexion de votre application Workfront à Workfront Fusion, voir <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connexion de Workfront à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Record Type]</td>

<td>Choisissez le type d’objet Workfront que le module doit lire.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Outputs]</td>

<td> <p>Sélectionnez les informations que vous souhaitez inclure dans le bundle de sortie pour ce module.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Output Custom Form]</td>
     <td> <p>Sélectionnez les formulaires personnalisés à inclure dans le lot de sortie pour ce module, puis sélectionnez les champs spécifiques à partir des formulaires personnalisés à inclure dans la sortie.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL References]</td>
   <td>Sélectionnez les champs de référence que vous souhaitez inclure dans la sortie.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Collections]</td>
   <td>Sélectionnez les champs de référence que vous souhaitez inclure dans la sortie.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL ID]</td>
   <td> <p>Saisissez l’ID Workfront unique de l’enregistrement que le module doit lire.</p> <p>Pour obtenir l’identifiant, ouvrez l’objet Workfront dans votre navigateur et copiez le texte à la fin de l’URL après « ID= ». Par exemple : https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

Consultez une liste des types d’objets Workfront pour lesquels vous pouvez utiliser ce module dans [Types d’objets Workfront disponibles pour chaque module Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

<!--

+++ **[!UICONTROL Read a Record (Legacy)]**

>[!IMPORTANT]
>
>This module has been replaced with the Read a record module. We recommend using that module in new scenarios.
>Existing scenarios that use this module will continue to function as expected. This module will be removed from the module selector in May 2025.

This action module retrieves data from a single record.

You specify the ID of the record. You can also specify which related records you want the module to read.

For example, if the record that the module is reading is a project, you can specify that you want the project's tasks read.

The module returns an array of data from the output fields you specified.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Record Type]</td>
  
   <td>Choose the Workfront object type that you want the module to read.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Outputs]</td>
  
   <td> <p>Select the information you want included in the output bundle for this module.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL References]</td>
   <td>Select any reference fields that you want to include in the output.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Collections]</td>
   <td>Select any reference fields that you want to include in the output.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL ID]</td>
   <td> <p>Enter the unique Workfront ID of the record that you want the module to read.</p> <p>To get the ID, open the Workfront object in your browser and copy the text at the end of the URL after "ID=." For example: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

+++

-->

+++ **Mettre à jour la version de la payload des événements**

Workfront a récemment publié une nouvelle version de son service d’abonnement aux événements. La nouvelle version ne constitue pas une modification de l’API Workfront, mais plutôt une modification de la fonctionnalité d’abonnement aux événements. Ce module d&#39;action met à jour la version de la payload de l&#39;événement utilisée pour ce scénario.

Pour plus d’informations sur la nouvelle version de l’abonnement aux événements, consultez [Contrôle de version des abonnements aux événements](https://experienceleague.adobe.com/fr/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-versioning) dans la documentation de Workfront

Pour obtenir des ressources sur la conservation de vos scénarios Workfront Fusion pendant la mise à niveau de l’abonnement à l’événement, y compris un enregistrement de webinaire, consultez [&#x200B; Conservation de vos scénarios Fusion pendant la mise à niveau de la version V2 des abonnements aux événements](https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/event-follow-up-preserving-your-fusion-scenarios-during-the/td-p/754182?profile.language=fr).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre application Workfront à Workfront Fusion, voir <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connexion de Workfront à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Version]</td> 
   <td> Sélectionnez la version de l'abonnement à l'événement que vous souhaitez utiliser pour cette payload. </td> 
  </tr> 
 </tbody> 
</table>


+++

+++ **Mettre à jour un enregistrement**


Ce module d’action met à jour un objet, tel qu’un projet, une tâche ou un problème. Le module vous permet de sélectionner les champs de l’objet disponibles dans le module.

Vous indiquez l’ID de l’enregistrement.

Le module renvoie l’ID de l’objet et de tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre application Workfront à Workfront Fusion, voir <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connexion de Workfront à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>Saisissez l’ID Workfront unique de l’enregistrement que le module doit mettre à jour.</p> <p>Pour obtenir l’identifiant, ouvrez l’objet Workfront dans votre navigateur et copiez le texte à la fin de l’URL après « ID= ». Par exemple : https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Record Type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement Workfront que le module doit mettre à jour.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Select fields to map]</td> 
   <td>Sélectionnez les champs qui doivent être disponibles pour la saisie de données. Vous pouvez ainsi utiliser ces champs sans avoir à faire défiler ceux dont vous n’avez pas besoin. Vous pouvez ensuite saisir ou mapper des données dans ces champs.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Attach Custom Form]</td> 
   <td>Sélectionnez les formulaires personnalisés pour lesquels vous souhaitez fournir des valeurs de champ dans le nouvel enregistrement. Après avoir sélectionné le formulaire, saisissez les données des champs de ce formulaire.<p> Pour fournir les valeurs de champ d’un formulaire que vous joignez dans ce module, incluez l’ID de formulaire personnalisé dans la section Champs à mapper .</td> 
  </tr> 
 </tbody> 
</table>

Consultez une liste des types d’objets Workfront pour lesquels vous pouvez utiliser ce module dans [Types d’objets Workfront disponibles pour chaque module Workfront](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
> Lors de la saisie du texte d’un champ personnalisé ou d’un objet [!UICONTROL Note] (commentaire ou réponse), vous pouvez utiliser des balises HTML dans le champ [!UICONTROL Texte de la note] pour créer du texte enrichi, comme du texte en gras ou en italique.


+++

<!--

+++ **[!UICONTROL Update Record (Legacy)]**

>[!IMPORTANT]
>
>This module has been replaced with the Update a record module. We recommend using that module in new scenarios.
>Existing scenarios that use this module will continue to function as expected. This module will be removed from the module selector in May 2025.

This action module updates an object, such as a project, task, or issue. The module allows you to select which of the object's fields are available in the module.

You specify the ID of the record.

The module returns the ID of the  object and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>Enter the unique Workfront ID of the record that you want the module to update.</p> <p>To get the ID, open the Workfront object in your browser and copy the text at the end of the URL after "ID=." For example: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to update.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Select fields to map]</td> 
   <td>Select the fields that you want available for data input. This allows you to use these fields without having to scroll through the ones you don't need. You can then enter or map data into these fields.</td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* When entering the ID of an object, you can begin typing the name of the object, then select it from the list. The module then enters the appropriate ID into the field.
>* When entering the text for a custom field or a [!UICONTROL Note] object (Comment or reply), you can use HTML tags in the [!UICONTROL Note Text] field to create rich text, such as bold or italic text.

+++

-->

+++ **[!UICONTROL Charger le document]**

Ce module d&#39;action charge un document dans un objet Workfront, tel qu&#39;un projet, une tâche ou un événement. Ce module charge le document par blocs, ce qui rend le processus de chargement plus fluide pour Workfront.

Ce module peut gérer des fichiers plus volumineux que le module hérité et fait partie d’un déploiement échelonné vers les organisations qui disposent d’un package Ultimate Workfront.

Indiquez l’emplacement du document, le fichier à charger et éventuellement un nouveau nom pour le fichier.

Le module renvoie l’ID du document et des champs associés, ainsi que les valeurs et les champs personnalisés auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre application Workfront à Workfront Fusion, voir <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connexion de Workfront à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Related Record ID]</td> 
   <td>Saisissez l’ID Workfront unique de l’enregistrement dans lequel vous souhaitez charger le document.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Related Record Type]</td> 
   <td>Sélectionnez le type d’enregistrement Workfront sur lequel vous souhaitez que le module charge le document.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder ID]</td> 
   <td>Selon le type d’enregistrement associé, vous devrez peut-être saisir ou mapper un ID de dossier.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </td> 
  </tr> 
 </tbody> 
</table>

Consultez une liste des types d’objets Workfront pour lesquels vous pouvez utiliser ce module dans [Types d’objets Workfront disponibles pour chaque module Workfront](#workfront-object-types-available-for-each-workfront-module).

+++

<!--

+++ **[!UICONTROL Upload Document (Legacy)]**

This action module uploads a document to a Workfront object, such as a project, task, or issue. It uploads the entire document at once. 

You specify the location for the document, the file you want to upload, and an optional new name for the file.

The module returns the ID of the document and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Related Record ID]</td> 
   <td>Enter the unique Workfront ID of the record to which you want to upload the document.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Related Record Type]</td> 
   <td>Select the type of Workfront record where you want the module to upload the document.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder ID]</td> 
   <td>Depending on the type of related record, you may need to enter or map a folder ID.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).


+++
-->

### Recherches

<!--
* [Read Related Records](#read-related-records) 
* [Search](#search)
-->

+++ **[!UICONTROL Lire les enregistrements associés]**

Ce module de recherche lit les enregistrements correspondant à la requête de recherche que vous spécifiez, dans un objet parent particulier.

Vous spécifiez les champs à inclure dans la sortie. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre application Workfront à Workfront Fusion, voir <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connexion de Workfront à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement parent (objet Workfront) dont vous souhaitez lire les enregistrements associés.</p> <p>Consultez dans cet article une liste des types d’objets Workfront pour lesquels vous pouvez utiliser ce module dans <a href="#object-types-available-for-each-workfront-search-module" class="MCXref xref">Types d’objets Workfront disponibles pour chaque module Workfront</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Parent Record ID]</td> 
   <td> <p>Saisissez ou mappez l’identifiant de l’enregistrement parent dont vous souhaitez lire les enregistrements associés.</p> <p>Pour obtenir l’identifiant, ouvrez l’objet Workfront dans votre navigateur et copiez le texte à la fin de l’URL après « ID= ». Par exemple : https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Collections]</td> 
   <td>Sélectionnez ou mappez le type d’enregistrement enfant que le module doit lire.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>Sélectionnez les informations que vous souhaitez inclure dans le bundle de sortie pour ce module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Rechercher]**

Ce module de recherche recherche les enregistrements dans un objet de Workfront qui correspondent à la requête que vous spécifiez.

Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre application Workfront à Workfront Fusion, voir <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connexion de Workfront à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement Workfront que vous souhaitez que le module recherche.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Custom forms list]</td> 
   <td> <p>Sélectionnez au moins un formulaire personnalisé. Les champs de ces formulaires personnalisés seront disponibles pour la requête.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Result Set]</td> 
   <td>Sélectionnez une option pour indiquer si vous souhaitez que le module obtienne le premier résultat correspondant à vos critères de recherche ou tous les résultats correspondants.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria fields]</td> 
   <td> <p>Sélectionnez les champs que vous souhaitez utiliser pour vos critères de recherche. Ces champs seront ensuite disponibles dans la liste déroulante Critères de recherche.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria]</td> 
   <td> <p>Renseignez le champ avec lequel vous souhaitez effectuer une recherche, l’opérateur que vous souhaitez utiliser dans votre requête et la valeur que vous recherchez dans le champ.</p> <p>Note : n’utilisez pas <code>username </code> dans vos critères de recherche. L’inclusion de la mention <code>username </code> dans une requête d’API vers Workfront connecte l’utilisateur à Workfront et la recherche échoue.</p> <p>Note : <code>In</code> et <code>NotIn</code> fonctionnent avec des tableaux. Les entrées doivent être au format de tableau.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>Sélectionnez les champs que vous souhaitez inclure dans la sortie de ce module.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL References]</td> 
   <td>Sélectionnez les champs de référence à inclure dans la recherche.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Collections]</td> 
   <td>Sélectionnez les collections à ajouter à la recherche.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Recherche (hérité)]**

>[!IMPORTANT]
>
>Ce module a été remplacé par le module Rechercher des enregistrements. Nous vous recommandons d’utiliser ce module dans de nouveaux scénarios.
>&#x200B;>Les scénarios existants qui utilisent ce module continueront à fonctionner comme prévu. Ce module sera supprimé du sélecteur de modules en mai 2025.

Ce module de recherche recherche les enregistrements dans un objet de Workfront qui correspondent à la requête que vous spécifiez.

Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre application Workfront à Workfront Fusion, voir <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connexion de Workfront à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement Workfront que vous souhaitez que le module recherche.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Result Set]</td> 
   <td>Sélectionnez une option pour indiquer si vous souhaitez que le module obtienne le premier résultat correspondant à vos critères de recherche ou tous les résultats correspondants.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria fields]</td> 
   <td> <p>Sélectionnez les champs que vous souhaitez utiliser pour vos critères de recherche. Ces champs seront ensuite disponibles dans la liste déroulante Critères de recherche.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria]</td> 
   <td> <p>Renseignez le champ avec lequel vous souhaitez effectuer une recherche, l’opérateur que vous souhaitez utiliser dans votre requête et la valeur que vous recherchez dans le champ.</p> <p>Note : n’utilisez pas <code>username </code> dans vos critères de recherche. L’inclusion de la mention <code>username </code> dans une requête d’API vers Workfront connecte l’utilisateur à Workfront et la recherche échoue.</p> <p>Note : <code>In</code> et <code>NotIn</code> fonctionnent avec des tableaux. Les entrées doivent être au format de tableau.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>Sélectionnez les champs que vous souhaitez inclure dans la sortie de ce module.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL References]</td> 
   <td>Sélectionnez les champs de référence à inclure dans la recherche.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Collections]</td> 
   <td>Sélectionnez les collections à ajouter à la recherche.</td> 
  </tr> 
 </tbody> 
</table>

+++

<!--not visible Jan 6, 2025

+++ **[!UICONTROL Search (Legacy)]**

This search module looks for records in an object in Workfront that match the search query you specify.

You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to search for.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Result Set]</td> 
   <td>Select an option to specify whether you want the module to get the first result that matches your search criteria or all the results that match it.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal]</td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria]</td> 
   <td> <p>Enter the field that you want to search by, the operator you want to use in your query, and the value that you are searching for in the field.</p> <p>Note: Do not use <code>username </code>in your search criteria. Including <code>username </code>in an API query to Workfront logs the user into Workfront, and the search will not be successful.</p> <p>Note: <code>In</code> and <code>NotIn</code>work with arrays. The inputs should be in array format.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>Select the fields that you want to include in the output for this module.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL References]</td> 
   <td>Select any reference fields that you want to include in the search.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Collections]</td> 
   <td>Select any collections that you want to add to the search.</td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

+++-->

## Types d’objets Workfront disponibles pour chaque module Workfront

<!-- [Object types available for each Workfront trigger module](#object-types-available-for-each-workfront-trigger-module) 
* [Object types available for each Workfront action module](#object-types-available-for-each-workfront-action-module) 
* [Object types available for each Workfront search module](#object-types-available-for-each-workfront-search-module)-->

+++**Types d’objet disponibles pour chaque module de déclenchement Workfront**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col>         
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL Watch Record]</th> 
   <th>[!UICONTROL Watch Field]</th> 
   <th>[!UICONTROL Watch Events]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Processus d’approbation</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Affectation</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Niveau de référence</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Enregistrement de facturation </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Taux de facturation</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Entreprise</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Tableau de bord</td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Document</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Dossier de documents</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Demande de document</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Version du document</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Frais</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Type de frais</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Groupe</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Heure</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Type d’heure</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Problème</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Itération</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Fonction</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Entrée au journal</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Jalon</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Chemin jalonné</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Note</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Balise de note</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Portfolio</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Programme</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Projet</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Utilisateur du projet</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Approbation d'épreuve</td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Temps réservé* </td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Rapport</td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Risque</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Type de risque</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Personne approbatrice d’étape</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tâche</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Equipe</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Modèle</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Tâche de modèle</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Feuille de temps</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>l’utilisateur ou de l’utilisatrice</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Mettre à jour</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Types d’objet disponibles pour chaque module d’action Workfront**

>[!NOTE]
>
>Le module [!UICONTROL Télécharger le document] n&#39;est pas inclus dans ce tableau, car les types d&#39;objets Workfront ne font pas partie de sa configuration.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL Create a record]</th> 
   <th>[!UICONTROL Update a record]</th> 
   <th>[!UICONTROL Delete a record]</th> 
   <th>[!UICONTROL Upload Document]</th> 
   <th>[!UICONTROL Read a record]</th> 
   <th>[!UICONTROL Custom API Call]</th> 
   <th>[!UICONTROL Misc Action]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Processus d’approbation</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Affectation</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Niveau de référence</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
   <tr> 
   <td>Enregistrement de facturation</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Taux de facturation</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Entreprise</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Document</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Dossier de documents</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Version du document</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Taux de change</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Frais</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Type de frais</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Document externe</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Groupe</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Heure</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Type d’heure</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Problème</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Itération</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Fonction</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Entrée au journal</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Jalon</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Chemin jalonné</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Note</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Balise de note</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Portfolio</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Programme</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Projet</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Utilisateur du projet</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Temps réservé* </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Risque</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Type de risque</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Personne approbatrice d’étape</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tâche</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Equipe</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Modèle</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tâche de modèle</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Feuille de temps</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>l’utilisateur ou de l’utilisatrice</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Mettre à jour</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Types d’objet disponibles pour chaque module de recherche Workfront**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL Search]</th> 
   <th>[!UICONTROL Read Related Records]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Processus d’approbation</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Affectation</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Enregistrement de facturation</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Taux de facturation</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Entreprise</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Document</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Dossier de documents</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Version du document</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Frais</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Type de frais</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Groupe</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Heure</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Type d’heure</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Problème</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Itération</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Fonction</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Entrée au journal</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Jalon</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Chemin jalonné</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Note</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Balise de note</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Portfolio</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Programme</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Projet</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Utilisateur du projet</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Temps réservé* </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Risque</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Type de risque</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Personne approbatrice d’étape</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tâche</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Equipe</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Modèle</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Tâche de modèle</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Feuille de temps</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>l’utilisateur ou de l’utilisatrice</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Délégation d'utilisateur</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

Nous vous recommandons de vérifier deux fois pour vous assurer que cela fonctionne comme prévu.

+++

## Filtres d’abonnement aux événements dans les modules Workfront > [!UICONTROL Événements Espion]

>[!NOTE]
>
>* Il est vivement recommandé d’utiliser des filtres d’abonnement aux événements dans vos modules [!UICONTROL Surveiller les événements].
>
>* Workfront a récemment publié une nouvelle version de son service d’abonnement aux événements. La nouvelle version ne constitue pas une modification de l’API Workfront, mais plutôt une modification de la fonctionnalité d’abonnement aux événements. Ce module d&#39;action met à jour la version de la payload de l&#39;événement utilisée pour ce scénario.
>
>   Pour plus d’informations sur la nouvelle version de l’abonnement aux événements, consultez [Contrôle de version des abonnements aux événements](https://experienceleague.adobe.com/fr/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-versioning) dans la documentation de Workfront
>
>   Pour obtenir des ressources sur la conservation de vos scénarios Workfront Fusion pendant la mise à niveau de l’abonnement à l’événement, y compris un enregistrement de webinaire, voir [ Conservation de vos scénarios Fusion pendant la mise à niveau de la version V2 des abonnements aux événements (https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/event-follow-up-preserving-your-fusion-scenarios-during-the/td-p/754182?profile.language=fr)].

Le module Workfront [!UICONTROL Événements Espion] déclenche des scénarios basés sur un webhook qui crée un abonnement aux événements dans l’API Workfront. L’abonnement à un événement est un ensemble de données qui détermine les événements envoyés au webhook. Par exemple, si vous configurez un module [!UICONTROL Surveiller les événements] qui recherche les problèmes, alors l’abonnement à l’événement envoie uniquement les événements liés aux problèmes.

En utilisant des filtres d’abonnement aux événements, les utilisateurs et utilisatrices de Fusion peuvent créer des abonnements aux événements qui conviennent mieux à leurs cas d’utilisation. Par exemple, vous pouvez configurer un abonnement à un événement dans l’API Workfront pour envoyer au webhook uniquement les problèmes liés à un projet spécifique, en veillant à ce que le module [!UICONTROL Événements Espion] ne se déclenche que pour les problèmes de ce projet. La possibilité de créer des déclencheurs plus étroits améliore la conception des scénarios en réduisant le nombre de déclencheurs non pertinents.

Cela diffère de la configuration d’un filtre dans le scénario Workfront Fusion. Sans filtre d’abonnement à un événement, votre webhook reçoit tous les événements liés au type d’objet sélectionné. La plupart de ces événements seraient hors de propos dans le scénario et doivent être filtrés avant que le scénario puisse continuer.

Les opérateurs suivants sont disponibles dans le filtre Workfront > Surveiller les événements :

* Est égal à
* Non égal à
* Supérieur à
* Inférieur à
* Est supérieur ou égal à
* Est inférieur ou égal à
* Contient
* Existe
   * Cet opérateur ne nécessite pas de valeur et le champ de valeur est absent.
* N’existe pas
   * Cet opérateur ne nécessite pas de valeur et le champ de valeur est absent.
* Modifié
   * Cet opérateur ne nécessite pas de valeur et le champ de valeur est absent.
   * Cet opérateur ignore le champ État.
   * Lorsque vous utilisez `Changed`, sélectionnez **Événements mis à jour uniquement** dans le champ **Origine de l’enregistrement**.

>[!IMPORTANT]
>
>Vous ne pouvez pas modifier les filtres dans les Webhooks Workfront existants. Pour configurer différents filtres pour les abonnements aux événements Workfront, supprimez le webhook actif et créez-en un.

>[!INFO]
>
>**Exemple :** supposons un scénario de traitement de nouveaux problèmes affectés à une utilisatrice spécifique, Ana.
>
>### Filtrer les événements à l’aide d’un filtre d’abonnement aux événements (recommandé)
>
>En utilisant le filtre d’événement, vous pouvez configurer le webhook pour qu’il déclenche le scénario lorsqu’un problème est affecté à Ana lors de la création du problème. L’ID d’utilisatrice d’Ana est b378489d8f7cd3cee0539260720a84b7.
>
>![Filtre d’événement](/help/workfront-fusion/references/apps-and-modules/assets/event-filter-watch-events-350x277.png)
>
>Si 100 problèmes sont créés en une journée, mais que seuls deux d’entre eux sont affectés à Ana, le scénario s’exécutera deux fois.
>
>### Filtrer les événements au sein du scénario (non recommandé)
>
>Pour filtrer les événements afin que seuls les problèmes affectés à Ana soient traités, vous pouvez créer un filtre après le module [!UICONTROL Événements de contrôle].
>
>![Sans filtre d’événement](/help/workfront-fusion/references/apps-and-modules/assets/watch-events-non-event-filter-350x206.png)
>
>Si 100 problèmes sont créés en une journée, mais que seuls deux d’entre eux sont affectés à Ana, le scénario s’exécutera 100 fois. Le filtre arrêtera 98 exécutions, mais le module déclencheur continuera à consommer des données et à effectuer des opérations dans toutes les exécutions.

Pour plus d’informations sur les abonnements aux événements Workfront, voir [FAQ - Abonnements aux événements](https://experienceleague.adobe.com/fr/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-faq).

Pour plus d’informations sur les webhooks, voir [Déclencheurs instantanés (webhooks) dans Adobe Workfront Fusion](/help/workfront-fusion/references/modules/webhooks-reference.md)

Pour plus d’informations sur les filtres dans les scénarios, voir [Ajouter un filtre à un scénario](/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md).
