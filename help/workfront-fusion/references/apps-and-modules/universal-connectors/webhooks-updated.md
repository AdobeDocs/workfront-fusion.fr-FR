---
title: Webhooks
description: Un webhook est un appel HTTP déclenché par un événement. Vous pouvez utiliser des webhooks pour activer les modules de déclenchement instantanés. Toute application connectée à Internet et autorisant des requêtes HTTP peut envoyer des webhooks à Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 8e415378-e9c1-4b49-874b-6d38aba0c303
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '1331'
ht-degree: 67%

---

# Webhooks



<!--This information moved to the webhooks article in the create scenarios folders in the new repo-->

Un webhook est un appel HTTP déclenché par un événement. Vous pouvez utiliser des webhooks pour activer les modules de déclenchement instantanés. Toute application connectée à Internet et autorisant des requêtes HTTP peut envoyer des webhooks à Adobe Workfront Fusion.

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

## Utiliser un webhook dans [!DNL Workfront Fusion]

>[!NOTE]
>
>Pour appeler un webhook tiers (un webhook sortant), vous pouvez utiliser un module HTTP. Pour plus d’informations, consultez la section [Modules HTTP](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors).

Pour utiliser un webhook pour connecter une application à [!DNL Workfront Fusion], procédez comme suit :

1. Ajoutez le module **[!UICONTROL Webhooks]** > **[!UICONTROL Custom Webhook]** de déclenchement instantané à votre scénario.

1. Cliquez sur **[!UICONTROL Add]** en regard du champ Webhook et saisissez un nom pour le nouveau webhook.
1. (Facultatif) Cliquez sur **[!UICONTROL Advanced Settings]**.
1. Dans le champ **[!UICONTROL IP restrictions]** , saisissez une liste séparée par des virgules des adresses IP à partir desquelles le module peut accepter des données.
1. Clic **[!UICONTROL Save]**

Une fois que vous avez créé un webhook, une URL unique s’affiche. Il s’agit de l’adresse à laquelle le webhook envoie des données. Workfront Fusion valide les données envoyées à cette adresse, puis les transmet pour traitement dans le scénario.

>[!NOTE]
>
>Une fois que vous avez créé un webhook, vous pouvez l’utiliser dans plusieurs scénarios à la fois.

### Configurer la structure de données du webhook {#configure-the-webhook-s-data-structure}

Pour reconnaître la structure des données de la payload entrante, [!DNL Workfront Fusion] analyse les exemples de données que vous envoyez à l’adresse affichée. Vous pouvez fournir les données d’exemples en effectuant une modification dans le service ou l’application qui fera que ce service ou cette application appellera le webhook. Vous pouvez par exemple supprimer un fichier.

Vous pouvez également envoyer les données d’exemple via le module [!UICONTROL HTTP] > [!UICONTROL Make a request] :

1. Créer un nouveau scénario avec le module **[!UICONTROL HTTP]** > **[!UICONTROL Make a request]**

1. Configurez le module avec les valeurs suivantes :

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"><p>[!UICONTROL URL] </p></td> 
      <td>Saisissez l’URL du webhook. Vous trouverez cette URL dans le module [!UICONTROL Webhooks] que vous avez utilisé pour configurer le webhook.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Method] </td> 
      <td><p>[!UICONTROL POST]</p></td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Body type]</td> 
      <td><p> [!UICONTROL Raw]</p></td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Content type]</td> 
      <td><p> JSON (application/json)</p></td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Request content]</td> 
      <td><p>JSON brut attendu dans le webhook</p></td> 
     </tr> 
    </tbody> 
   </table>

   ![Nouvelle configuration de scénario](/help/workfront-fusion/references/apps-and-modules/assets/new-scenario-set-up-like-this-350x446.png)

1. Ouvrez le scénario avec le module [!UICONTROL Webhooks] dans un onglet ou une fenêtre de navigateur distinct.
1. Dans le module Webhooks, cliquez sur **[!UICONTROL Redetermine data structure]**.

   Il n’est pas nécessaire de dissocier d’autres modules du module Webhooks.

1. Basculez vers le scénario avec le module [!UICONTROL HTTP] et exécutez-le.
1. Revenez au scénario avec le module Webhooks.

   Un message « [!UICONTROL Successfully determined] » signifie que le module a déterminé avec succès la structure de données.

   ![Déterminé avec succès](/help/workfront-fusion/references/apps-and-modules/assets/successfully-determined-350x175.png)

1. Cliquez sur **[!UICONTROL OK]** pour enregistrer la structure de données.

   Les éléments du webhook sont désormais disponibles dans le panneau de mappage pour une utilisation avec les modules suivants du scénario.

## La file d’attente webhook

Si un webhook reçoit des données et qu’aucun scénario actif n’attend ces données, les données sont stockées dans la file d’attente. Une fois le scénario activé, il traite tous les lots en attente dans la file d’attente de manière séquentielle.

>[!IMPORTANT]
>
>Les files d’attente de webhook sont partagées entre les scénarios qui utilisent le même webhook. Si l’un des scénarios est désactivé, toutes les données entrantes sont conservées dans la file d’attente.

## Formats de données entrantes pris en charge

[!DNL Workfront Fusion] prend en charge 3 formats de données entrants : [!UICONTROL Query String], [!UICONTROL Form Data] et [!UICONTROL JSON].

[!DNL Workfront Fusion] valide toutes les données entrantes par rapport à la structure de données sélectionnée. Ensuite, en fonction des paramètres du scénario, les données sont soit stockées dans la file d’attente pour traitement, soit traitées immédiatement.

Si une partie des données n’est pas validée, [!DNL Workfront Fusion] renvoie un code d’état HTTP 400 et spécifie, dans le corps de la réponse HTTP, la raison pour laquelle les données entrantes n’ont pas réussi les contrôles de validation. Si la validation des données entrantes réussit, Workfront Fusion renvoie un statut « [!UICONTROL 200 Accepted] ».

* [[!UICONTROL Query String]](#query-string)
* [[!UICONTROL Form Data]](#form-data)
* [[!UICONTROL JSON]](#json)

### [!UICONTROL Query String]

```
GET https://app.workfrontfusion.com/wh/<yourunique32characterslongstring>?name=<yourname>&job=automate
```

### [!UICONTROL Form Data]

```
POST https://app.workfrontfusion.com/wh/<yourunique32characterslongstring>

Content-Type: application/x-www-form-urlencoded

name=<yourname>&job=automate
```

#### Données de formulaire à plusieurs parties

```
POST https://app.workfrontfusion.com/wh/<yourunique32characterslongstring>


Content-Type: multipart/form-data; boundary=---generatedboundary

---generatedboundary

Content-Disposition: form-data; name="file"; filename="file.txt"


Content-Type: text/plain


Content of file.txt


---generatedboundary

Content-Disposition: form-data; name="name"

Workfront Fusion

---generatedboundary
```

Pour pouvoir recevoir des fichiers codés avec `multipart/form-data`, vous devez configurer une structure de données avec un champ de type `collection` contenant les champs imbriqués `name`, `mime` et `data`. Le champ `name` est de type `text` et contient le nom du fichier chargé. Le champ `mime` est de type `text` et contient un fichier au format MIME. Le champ `data` est de type `buffer` et contient des données binaires pour le fichier transféré.

Pour plus d’informations sur le format MIME, voir [Modules MIME](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/mime.md).

### [!UICONTROL JSON]

```
POST https://app.workfrontfusion.com/wh/<yourunique32characterslongstring>

Content-Type: application/json

{"name": "Workfront Fusion", "job": "automate"}
```

>[!TIP]
>
>Si vous souhaitez accéder au JSON d’origine, activez la transmission JSON lors de la configuration du webhook.
>
>1. Cliquez sur **[!UICONTROL Add]** pour ajouter un nouveau webhook.
>1. Cliquez sur **[!UICONTROL Show advanced settings]**.
>1. Cliquez sur **[!UICONTROL JSON pass-through]**.
>

## En-têtes de webhook

Pour accéder aux en-têtes du webhook, activez l’option Obtenir les en-têtes de requête lors de la configuration du webhook.

1. Cliquez sur **[!UICONTROL Add]** pour ajouter un nouveau webhook.
1. Cliquez sur **[!UICONTROL Show advanced settings]**.
1. Cliquez sur **[!UICONTROL Get request headers]**.

Vous pouvez extraire une valeur d’en-tête spécifique avec la combinaison des fonctions `map()` et `get()`.

>[!INFO]
>
>**Exemple :**
>
>L’exemple ci-dessous illustre une formule qui extrait la valeur de l’en-tête `authorization` du tableau `Headers[]`. La formule est utilisée dans un filtre qui compare la valeur extraite au texte donné pour ne transmettre que les webhooks en cas de correspondance.
>
>![Configurer un filtre](/help/workfront-fusion/references/apps-and-modules/assets/set-up-a-filter-350x169.png)
>
>Pour plus d’informations sur l’obtention d’un élément d’un tableau avec une clé donnée, consultez [Mappage d’un élément d’un tableau avec une clé donnée](/help/workfront-fusion/create-scenarios/map-data/map-an-array.md#map-an-arrays-element-with-a-given-key) dans l’article Mappage d’un tableau.

## Répondre aux webhooks

La réponse par défaut à un appel de webhook est le texte « Accepté ». La réponse est renvoyée à l’application qui a appelé le webhook lors de l’exécution du module webhook personnalisé.

* [Tester la réponse à un webhook](#test-the-response-to-a-webhook)
* [Exemple de réponse HTML](#html-response-example)
* [Exemple de redirection](#redirect-example)

### Tester la réponse à un webhook

1. Incluez le module **[!UICONTROL Custom Webhook]** dans votre scénario.
1. Ajoutez un nouveau webhook au module.
1. Copiez l’URL du webhook dans le presse-papiers.
1. Exécutez le scénario.

   L’icône en forme d’éclair dans le module [!UICONTROL Custom Webhook] se transforme en points qui tournent. Cela indique que le module attend désormais l’appel de webhook.

1. Ouvrez une nouvelle fenêtre de navigateur, collez l’URL copiée dans la barre d’adresse et appuyez sur **[!UICONTROL Enter]**.

   Le module [!UICONTROL Custom Webhook] est déclenché et le navigateur affiche une nouvelle page.

Si vous souhaitez personnaliser la réponse du webhook, utilisez le module de réponse webhook.

La configuration du module contient deux champs : [!UICONTROL Status] et [!UICONTROL Body].

* Le champ [!UICONTROL Status] contient des codes de statut de réponse HTTP tels que 2xx pour la réussite (par exemple, `200` pour OK), 3xx pour la redirection (par exemple, `307` pour la redirection temporaire), 4xx pour les erreurs client (par exemple, `400` pour une requête incorrecte), etc.

* Le champ [!UICONTROL Body] contient tout ce qui sera accepté par l’appel du webhook. Il peut s’agir de texte simple, de code HTML, de code XML, de code JSON, etc.

  >[!TIP]
  >
  >Nous vous recommandons de définir l’en-tête `Content-Type` du type MIME correspondant : `text/plain` pour du texte brut, `text/html` pour HTML, `application/json` pour JSON, `application/xml` pour XML, etc. Pour plus d’informations sur les types MIME, voir [Modules MIME](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/mime.md).

Le délai de temporisation pour l’envoi d’une réponse est de 40 secondes. Si la réponse n’est pas disponible au cours de cette période, Workfront Fusion renvoie un statut « 200 Accepté ».

### Exemple de réponse HTML

>[!INFO]
>
>**Exemple :**
>
>Configurez le module [!UICONTROL Webhook Response] comme suit :
>
><table style="table-layout:auto"> 
&gt; <col> 
&gt; <col> 
&gt; <tbody> 
&gt;  <tr> 
&gt;   <td role="rowheader">[!UICONTROL Status] </td> 
&gt;   <td> <p>Code de statut HTTP de succès 2xx (par exemple, 200)</p> </td> 
&gt;  </tr> 
&gt;  <tr> 
&gt;   <td role="rowheader">[!UICONTROL Body] </td> 
&gt;   <td> <p>Code HTML</p> </td> 
&gt;  </tr> 
&gt;  <tr> 
&gt;   <td role="rowheader"> <p>[!UICONTROL Custom headers]</p> </td> 
&gt;   <td> 
&gt;    <ul> 
&gt;     <li><strong>Clé</strong> : type de contenu</li> 
&gt;     <li><strong>Valeur</strong> : text/html</li> 
&gt;    </ul> </td> 
&gt;  </tr> 
&gt; </tbody> 
&gt;</table>
>
>![En-têtes personnalisés ](/help/workfront-fusion/references/apps-and-modules/assets/custom-headers-350x235.png)
>
>Cette opération génère une réponse HTML qui s’affiche dans un navigateur web :
>
>![Réponse HEML](/help/workfront-fusion/references/apps-and-modules/assets/html-response-350x70.png)

### Exemple de redirection

>[!INFO]
>
>**Exemple :** Configurez le module [!UICONTROL Webhook Response] comme suit :
>
><table style="table-layout:auto"> 
&gt; <col> 
&gt; <col> 
&gt; <tbody> 
&gt;  <tr> 
&gt;   <td role="rowheader">[!UICONTROL Status] </td> 
&gt;   <td> <p>Code d’état HTTP de redirection 3xx, par exemple 303</p> </td> 
&gt;  </tr> 
&gt;  <tr> 
&gt;   <td role="rowheader"> <p>[!UICONTROL Custom headers]</p> </td> 
&gt;   <td> 
&gt;    <ul> 
&gt;     <li><strong>[!UICONTROL Key]</strong>: Emplacement</li> 
&gt;     <li><strong>[!UICONTROL Value]</strong>: URL vers laquelle effectuer la redirection.</li> 
&gt;    </ul> </td> 
&gt;  </tr> 
&gt; </tbody> 
&gt;</table>
>
>![Réponse du Webhook](/help/workfront-fusion/references/apps-and-modules/assets/webhook-response-350x279.png)

## Désactivation de webhook

Les webhooks sont désactivés automatiquement si l’une des conditions suivantes s’applique :

* Le webhook n’a été connecté à aucun scénario depuis plus de 5 jours.
* Le webhook est utilisé uniquement dans les scénarios inactifs, qui sont inactifs depuis plus de 30 jours.

Les webhooks désactivés sont supprimés et désinscrits automatiquement s’ils ne sont connectés à aucun scénario et s’ils sont restés désactivés pendant plus de 30 jours.


## Dépannage

### Éléments manquants dans le panneau de mappage

Si certains éléments sont manquants dans le panneau de mappage dans la configuration des modules suivant le module [!UICONTROL Webhooks] > [!UICONTROL Custom Webhook] , cliquez sur le module **[!UICONTROL Webhooks]>[!UICONTROL Custom Webhook]** pour ouvrir sa configuration et cliquez sur **[!UICONTROL Re-determine data structure]** :

![Redéterminer la structure des données](/help/workfront-fusion/references/apps-and-modules/assets/redetermine-data-structure-btn-350x195.png)

Suivez ensuite les étapes décrites dans la section [Configuration de la structure de données du webhook](#configure-the-webhook-s-data-structure) dans cet article.
