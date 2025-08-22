---
title: Modules Salesforce
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent Salesforce et le connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: 3c7c03a7-67ea-4673-90b0-7d0506d9fa10
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2984'
ht-degree: 78%

---

# Modules [!DNL Salesforce]

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent [!DNL Salesforce] et le connecter à plusieurs applications et services tiers.

Pour obtenir une vidéo d’introduction au connecteur Salesforce, voir :

* [Salesforce](https://video.tv.adobe.com/v/3427027/){target=_blank}

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

>[!NOTE]
>
>* Toutes les éditions de [!DNL Salesforce] ne disposent pas d’un accès à l’API. Pour plus d’informations, voir les informations sur les éditions [!DNL Salesforce] avec un accès à l’API sur le site de la communauté [!DNL Salesforce].
>* Pour plus d’informations sur les erreurs spécifiques renvoyées par l’API [!DNL Salesforce], voir la documentation sur l’API [!DNL Salesforce]. Vous pouvez également vérifier le statut de l’API [!DNL Salesforce] pour toutes les pannes de service possibles.
>

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

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Conditions préalables

Pour utiliser les modules [!DNL Salesforce], vous devez disposer d’un compte [!DNL Salesforce].

## Informations sur l’API Salesforce

Le connecteur Salesforce utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td> {{connection.instanceUrl}}</td>
  </tr> 
  <tr> 
   <td role="rowheader">Version de l’API</td> 
   <td> v62.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.15.14</td> 
  </tr>
 </tbody> 
 </table>

## À propos de la recherche d’objets [!DNL Salesforce]

Lors de la recherche d’objets, vous pouvez saisir des termes de recherche individuels ou créer une requête plus complexe à l’aide de caractères génériques et d’opérateurs :

* Utilisez le caractère joker astérisque (\*) pour remplacer zéro ou plusieurs caractères. Par exemple, une recherche de Ca\* renvoie des éléments qui commencent par Ca.
* Utilisez un caractère joker point d’interrogation (?) pour remplacer un seul caractère. Par exemple, une recherche de Jo?n renvoie des éléments avec le terme John ou Joan mais pas Jon.
* Utilisez l’opérateur guillemets (&quot; &quot;) pour trouver une correspondance exacte. Par exemple : &quot;réunion de lundi&quot;

Pour plus d’informations sur les possibilités de recherche, voir la documentation [!DNL Salesforce] destinée à l’équipe de développement sur SOQL et SOSL.

## Créer une connexion à [!DNL Salesforce]

Pour créer une connexion pour vos modules [!DNL Salesforce], procédez comme suit :

1. Dans un module [!DNL Salesforce], cliquez sur **[!UICONTROL Ajouter]** en regard de la zone Connexion.

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
          <p>Saisissez un nom pour la nouvelle connexion.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>
          <p>Indiquez si vous vous connectez à un environnement de production ou hors production.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>
          <p>Indiquez si vous vous connectez à un compte de service ou à un compte personnel.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Saisissez votre identifiant client Salesforce.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Saisissez votre secret client Salesforce. </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Sandbox]</td>
        <td>Activez cette option s’il s’agit d’un environnement Sandbox.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL API Version]</td>
        <td>Saisissez la version de l’API Salesforce que vous souhaitez utiliser. La version par défaut est 62.0.</td>
      </tr>
    </tbody>
    </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour enregistrer la connexion et revenir au module.


## Modules [!DNL Salesforce] et leurs champs

* [Déclencheurs](#triggers)
* [Actions](#actions)
* [Recherches](#searches)

### Déclencheurs

* [[!UICONTROL Surveiller un champ]](#watch-a-field)
* [[!UICONTROL Surveiller des enregistrements]](#watch-for-records)
* [[!UICONTROL Surveiller des messages sortants]](#watch-outbound-messages)

#### [!UICONTROL Surveiller un champ]

Ce module de déclenchement lance un scénario lorsqu’un champ est mis à jour dans [!DNL Salesforce].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Salesforce] à Workfront Fusion, voir <a href="#create-a-connection-to-salesforce">Création d’une connexion à Salesforce</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type] </td> 
   <td> <p>Sélectionnez le type d’enregistrement qui contient le champ que le module doit surveiller. Vous devez choisir un type d’enregistrement pour lequel [!UICONTROL Field History] est activé dans la configuration de [!DNL Salesforce]. Pour plus d’informations, consultez la section <a href="https://help.salesforce.com/s/articleView?id=xcloud.tracking_field_history.htm&type=5">Suivi de l’historique des champs</a> dans la documentation [!DNL Salesforce]. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Field]</td> 
   <td> <p>Sélectionnez les champs que le module doit surveiller pour détecter les modifications. Les champs disponibles dépendent du type d’enregistrement sélectionné.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal de champs que le module doit renvoyer pour chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Surveiller des enregistrements]

Ce module de déclenchement exécute un scénario lorsqu’un enregistrement d’un objet est créé ou mis à jour. Le module renvoie tous les champs standard associés à l’enregistrement ou aux enregistrements, ainsi que les champs et valeurs personnalisés auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Salesforce] à Workfront Fusion, voir <a href="#create-a-connection-to-salesforce">Création d’une connexion à Salesforce</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Type] </td> 
   <td> <p>Sélectionnez le type d’enregistrement [!DNL Salesforce] que le module doit surveiller.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Fields]</td> 
   <td>Sélectionnez les champs que le module doit surveiller. Les champs disponibles dépendent du type d’enregistrement.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal count of records].</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td> <p>Déterminez si vous souhaitez que le scénario ne surveille que les nouveaux enregistrements du type que vous avez sélectionné ou les nouveaux enregistrements du type que vous avez sélectionné, ainsi que toutes les autres modifications apportées aux enregistrements de ce type.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Surveiller des messages sortants]

Ce module de déclenchement exécute un scénario lorsqu’une personne envoie un message. Le module renvoie tous les champs standard associés à l’enregistrement ou aux enregistrements, ainsi que les champs et valeurs personnalisés auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Ce module nécessite une configuration supplémentaire. Un flux doit être configuré pour les messages sortants.

* Pour obtenir des instructions sur les flux dans Salesforce, voir [Automatiser les tâches avec des flux](https://help.salesforce.com/s/articleView?id=platform.flow.htm) dans la documentation de Salesforce.
* Pour plus d’informations sur la configuration d’un message sortant dans Salesforce, voir [ Envoyer un message sortant à partir de votre flux déclenché par enregistrement ](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_builder_outbound_message.htm) dans la documentation de Salesforce

<!--

1. Go to the [!DNL Salesforce] setup page.

   To access the setup page, locate and click the button labeled "[!UICONTROL Setup]" in the upper-right hand corner of the [!DNL Salesforce] account. From the [!DNL Salesforce] setup page, locate the "[!UICONTROL Quick Find / Search]" bar on the left hand side. Search for "[!UICONTROL Workflow Rules]." 

1. Click **[!UICONTROL Workflow Rules]**. 
1. On the the [!UICONTROL Workflow Rules] page that appears, click **[!UICONTROL New Rule]** and select the object type the rule will apply to (such as "[!UICONTROL Opportunity]" if you are monitoring updates to Opportunity records).
1. Click **[!UICONTROL Next]**.
1. Set a rule name, evaluation criteria, and rule criteria, then click **[!UICONTROL Save]** and **[!UICONTROL Next]**.

1. Click **[!UICONTROL Done]**.
1. From the newly created Workflow rule, click **[!UICONTROL Edit]**..
1. From the **[!UICONTROL Add Workflow Action]** drop-down list, select **[!UICONTROL New Outbound Message]**.

1. Specify name, description, Endpoint URL, and fields you want to include in the new outbound message, then click **[!UICONTROL Save]**.

   The **[!UICONTROL Endpoint URL]** field contains the URL provided on the [!DNL Salesforce] [!UICONTROL Outbound Message] in Workfront Fusion.

1. Configure a scenario beginning with the [!UICONTROL Outbound Message] event. 

1. Click the **</>** icon in the bottom right and copy the provided URL.
1. Return to the **[!UICONTROL Workflow Rules]** page, locate the newly created rule, then click **[!UICONTROL Activate]**.

-->

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Webhook]</td> 
   <td> <p>Sélectionnez le webhook que vous souhaitez utiliser pour surveiller les messages sortants. Pour ajouter un webhook, cliquez sur <strong>[!UICONTROL Add]</strong> et saisissez le nom et la connexion du webhook.</p> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Salesforce] à Workfront Fusion, consultez <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à [!UICONTROL Adobe Workfront Fusion] - Instructions de base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type] </td> 
   <td> <p>Sélectionnez le type d’enregistrement [!DNL Salesforce] que le module doit surveiller pour les messages sortants.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Fields]</td> 
   <td> <p>Sélectionnez les champs que le module doit surveiller pour les messages sortants. Les champs disponibles dépendent du type d’enregistrement.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [[!UICONTROL Créer un enregistrement]](#create-a-record)
* [[!UICONTROL Appel API personnalisé]](#custom-api-call)
* [[!UICONTROL Supprimer un enregistrement]](#delete-a-record)
* [[!UICONTROL Télécharger la pièce jointe/le document]](#download-attachmentdocument)
* [[!UICONTROL Lire un enregistrement]](#read-a-record)
* [[!UICONTROL Charger la pièce jointe/le document]](#upload-attachmentdocument)
* [Charger fichier](#upload-file)

#### [!UICONTROL Créer un enregistrement]

Ce module d’action crée un nouvel enregistrement dans un objet.

Le module vous permet de sélectionner les champs de l’objet disponibles dans le module. Cela réduit le nombre de champs à parcourir lors de la configuration du module.

Le module renvoie l’identifiant de l’enregistrement et de tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Salesforce] à Workfront Fusion, voir <a href="#create-a-connection-to-salesforce">Création d’une connexion à Salesforce</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Record Type] </p> </td> 
   <td> <p>Sélectionnez le type d’enregistrement [!DNL Salesforce] que vous souhaitez que le module crée. Les champs deviennent disponibles en fonction du type d’enregistrement sélectionné dans le champ [!UICONTROL Record Type]. Ces champs reposent sur l’API [!DNL Salesforce].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Select fields to map]</td> 
   <td> <p>Sélectionnez les champs que vous souhaitez que le module configure lors de la création du nouvel enregistrement. Les champs obligatoires figurent en tête de liste. </p> <p>Les champs sélectionnés s’ouvrent sous ce champ. Vous pouvez maintenant saisir des valeurs dans ces champs.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Appel API personnalisé]

Ce module d’action vous permet d’effectuer un appel personnalisé et authentifié à l’API [!DNL Salesforce]. De cette façon, vous pouvez créer une automatisation du flux de données qui ne peut pas être réalisée par les autres modules [!DNL Salesforce].

Le module renvoie les éléments suivants :

* **[!UICONTROL Code d’état]** (nombre) : indique la réussite ou l’échec de votre requête HTTP. Ce sont des codes standard que vous pouvez consulter sur Internet.
* **[!UICONTROL En-têtes]** (objet) : contexte plus détaillé pour le code de réponse/d’état qui ne se rapporte pas au corps de sortie. Tous les en-têtes qui apparaissent dans un en-tête de réponse ne sont pas des en-têtes de réponse. Certains peuvent donc ne pas vous être utiles.

  Les en-têtes de réponse dépendent de la requête HTTP que vous avez choisie lors de la configuration du module.

* **[!UICONTROL Corps]** (objet) : selon la requête HTTP que vous avez choisie lors de la configuration du module, vous pouvez recevoir des données en retour. Ces données, telles que les données d’une requête [!UICONTROL GET], sont contenues dans cet objet.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Salesforce] à Workfront Fusion, voir <a href="#create-a-connection-to-salesforce">Création d’une connexion à Salesforce</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Saisissez un chemin relatif à <code> &lt;Instance URL&gt;/services/data/v62.0/</code>.</p> <p>Pour obtenir la liste des points d’entrée disponibles, reportez-vous à la section <a href="https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/intro_what_is_rest_api.htm">Guide pour l’équipe de développement de l’API REST Salesforce</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard. Par exemple, <code>{"Content-type":"application/json"}</code>. Workfront Fusion ajoute les en-têtes d’autorisation pour vous.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Ajoutez la requête pour l’appel API sous la forme d’un objet JSON standard. Par exemple : <code>{"name":"something-urgent"}</code></p> </td> 
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

>[!BEGINSHADEBOX]

**Exemple :** l’appel API suivant renvoie la liste des utilisateurs et utilisatrices de votre compte [!DNL Salesforce] :

* **URL** : `query`

* **Méthode** : [!UICONTROL GET]

* **Chaîne de requête** :

* **Clé** : `q`

* **Valeur** :`SELECT Id, Name, CreatedDate, LastModifiedDate FROM User LIMIT 10`

Les correspondances de la recherche se trouvent dans la sortie du module sous **[!UICONTROL Bundle] > [!UICONTROL Corps] > [!UICONTROL Enregistrements]**.

Dans notre exemple, 6 utilisateurs ou utilisatrices ont été renvoyés :

![Correspond à la recherche](/help/workfront-fusion/references/apps-and-modules/assets/matches-of-the-search-350x573.png)

>[!ENDSHADEBOX]

#### [!UICONTROL Supprimer un enregistrement]

Ce module d’action supprime un enregistrement existant dans un objet.

Vous indiquez l’ID de l’enregistrement.

Le module renvoie l’ID de l’enregistrement et tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Salesforce] à Workfront Fusion, voir <a href="#create-a-connection-to-salesforce">Création d’une connexion à Salesforce</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type] </td> 
   <td> <p>Sélectionnez le type d’enregistrement [!DNL Salesforce] que le module doit supprimer.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>Saisissez ou mappez l’identifiant [!DNL Salesforce] unique de l’enregistrement que vous souhaitez que le module supprime.</p> <p>Pour obtenir l’identifiant, ouvrez l’objet [!DNL Salesforce] dans votre navigateur et copiez le texte à la fin de l’URL après la dernière barre oblique (/). Par exemple : <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Télécharger la pièce jointe/le document]

Ce module d’action permet de télécharger un document ou une pièce jointe à partir d’un enregistrement.

Indiquez l’ID de l’enregistrement et le type de téléchargement souhaité.

Le module renvoie l’ID de la pièce jointe ou du document et tous les champs associés, ainsi que tous les champs et valeurs personnalisés auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr>
    <td>[!UICONTROL Connection]</td>
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Salesforce] à Workfront Fusion, voir <a href="#create-a-connection-to-salesforce">Création d’une connexion à Salesforce</a> dans cet article.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Type of Download]</td>
    <td> <p>Indiquez le type de fichier que vous souhaitez télécharger à partir de Salesforce.</p> 
     <ul> 
      <li>[!UICONTROL Attachment]</li> 
      <li>[!UICONTROL Document]</li> 
      <li>[!UICONTROL ContentDocument] (Il s’agit d’un document qui a été chargé dans une bibliothèque de [!DNL Saleforce CRM Content] ou [!DNL Salesforce Files]).</li> 
     </ul> </td>
  </tr> 
  <tr>
    <td> <p>[!UICONTROL ID] / </p> <p>[!UICONTROL Attachment ID] / </p> <p>[!UICONTROL ContentDocument ID]</p> </td>
    <td> <p>Saisissez ou mappez l’ID [!DNL Salesforce] unique de l’enregistrement que le module doit télécharger.</p> <p>Pour obtenir l’ID, ouvrez l’objet [!DNL Salesforce] dans votre navigateur et copiez le texte à la fin de l’URL après la dernière barre oblique (/). Par exemple : <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Lire un enregistrement]

Ce module d’action lit les données d’un seul objet dans [!DNL Salesforce].

Vous indiquez l’ID de l’enregistrement.

Le module renvoie l’identifiant de l’enregistrement et de tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr>
    <td>[!UICONTROL Connection]</td>
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Salesforce] à Workfront Fusion, voir <a href="#create-a-connection-to-salesforce">Création d’une connexion à Salesforce</a> dans cet article.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Record Type]</td>
    <td>Sélectionnez le type d’enregistrement [!DNL Salesforce] que le module doit lire.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Record Fields]</td>
    <td>Sélectionnez les champs que le module doit lire. Vous devez sélectionner au moins un champ. Les champs disponibles dépendent du type d’enregistrement.</td>
  </tr> 
  <tr>
    <td>[!UICONTROL ID]</td>
    <td> <p>Saisissez ou mappez l’identifiant [!DNL Salesforce] unique de l’enregistrement que vous souhaitez que le module lise.</p> <p>Pour obtenir l’identifiant, ouvrez l’objet [!DNL Salesforce] dans votre navigateur et copiez le texte à la fin de l’URL après la dernière barre oblique (/). Par exemple : <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td>
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Mettre à jour un enregistrement]

Ce module d’action modifie un enregistrement dans un objet.

Le module vous permet de sélectionner les champs de l’objet disponibles dans le module. Cela réduit le nombre de champs à parcourir lors de la configuration du module.

Le module renvoie l’ID de l’enregistrement et tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Salesforce] à Workfront Fusion, voir <a href="#create-a-connection-to-salesforce">Création d’une connexion à Salesforce</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td>Saisissez ou mappez l’ID de l’enregistrement que vous souhaitez mettre à jour.</td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Record Type] </p> </td> 
   <td> <p>Sélectionnez le type d’enregistrement [!DNL Salesforce] que vous souhaitez que le module mette à jour. Les champs sont disponibles en fonction du type d’enregistrement sélectionné dans le champ Type d’enregistrement. Ces champs sont basés sur l’API [!DNL Salesforce].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Select fields to map]</td> 
   <td> <p>Sélectionnez les champs que vous souhaitez que le module configure lors de la création du nouvel enregistrement. Les champs obligatoires figurent en tête de liste. </p> <p>Les champs sélectionnés s’ouvrent sous ce champ. Vous pouvez maintenant saisir des valeurs dans ces champs.</p> </td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Charger la pièce jointe/le document]

Ce module d’action charge un fichier et le joint à un enregistrement spécifié, ou charge un document.

Le module renvoie l’ID de la pièce jointe ou du document et tous les champs associés, ainsi que tous les champs et valeurs personnalisés auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Salesforce] à Workfront Fusion, voir <a href="#create-a-connection-to-salesforce">Création d’une connexion à Salesforce</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Type of Upload]</td> 
   <td>Sélectionnez si vous souhaitez que le module charge une pièce jointe ou un document.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td>Saisissez ou mappez l’ID de l’objet pour lequel vous souhaitez charger une pièce jointe.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder]</td> 
   <td>Sélectionnez le dossier dans lequel vous souhaitez charger un document. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source File]</td> 
   <td>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</td> 
  </tr> 
 </tbody> 
</table>

#### Charger fichier

Ce module d’action charge un seul fichier dans Salesforce.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la connexion de votre compte [!DNL Salesforce] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à[!DNL &#x200B; Adobe Workfront Fusion] - Instructions de base</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Liaison de documents]</td> 
   <td>Indiquez s’il faut appliquer un lien vers le document de contenu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL linkedEntityId]</td> 
   <td>Si vous utilisez la liaison de documents, saisissez ou mappez l'identifiant de l'objet lié.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ShareType]</td> 
   <td>Si vous utilisez la liaison de documents, sélectionnez les autorisations pour le fichier.<ul><li><b>Autorisation Observateur</b><p>L’utilisateur peut afficher le fichier.</p></li><li><b>Autorisation Collaborateur</b><p>L’utilisateur peut afficher et modifier le fichier.</p></li><li><b>Autorisations déduites</b><p>Les autorisations sont basées sur les autorisations de l’utilisateur sur l’enregistrement associé, comme une bibliothèque.</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td>Si vous utilisez la liaison de documents, saisissez ou mappez la visibilité du document.<ul><li><b>AllUsers</b><p>Disponible pour tous les utilisateurs disposant d’autorisations</p></li><li><b>InternalUsers</b><p>Disponible pour les utilisateurs internes disposant d’autorisations.</p></li><li><b>SharedUsers</b><p>Disponible pour les utilisateurs et utilisatrices qui peuvent voir le flux sur lequel le fichier est publié.</p></li></ul></td> 
  </tr> 
 </tbody> 
</table>

### Recherches

* [Recherche](#search)
* [Rechercher avec requête](#search-with-query)

#### [!UICONTROL Rechercher]

Ce module d’action permet de récupérer tous les enregistrements répondant à un critère donné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la connexion de votre compte [!DNL Salesforce] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à[!DNL &#x200B; Adobe Workfront Fusion] - Instructions de base</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td> <p>Sélectionnez le type d’objet que vous souhaitez rechercher.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search criteria]</td> 
   <td>Sélectionnez le champ dans lequel vous souhaitez effectuer une recherche, l’opérateur que vous souhaitez utiliser dans votre requête et la valeur que vous recherchez dans le champ. Vous pouvez relier des requêtes en utilisant AND ou OR.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Sélectionnez les champs que vous souhaitez inclure dans la sortie du module. Les champs sont disponibles en fonction du type d’enregistrement.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Result set]</td> 
   <td>Indiquez si vous souhaitez que le module renvoie tous les enregistrements correspondants ou uniquement le premier enregistrement correspondant.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximal]</td> 
   <td>Saisissez ou mappez le nombre maximum d’enregistrements que vous souhaitez que le module récupère au cours de chaque cycle d’exécution du scénario.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Recherche avec requête]

Ce module de recherche permet de rechercher les enregistrements d’un objet dans [!DNL Salesforce] qui correspondent à la requête de recherche que vous avez spécifiée. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Salesforce] à Workfront Fusion, voir <a href="#create-a-connection-to-salesforce">Création d’une connexion à Salesforce</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search Type]</td> 
   <td> <p>Sélectionnez le type de recherche que vous souhaitez que le module effectue :</p> 
    <ul> 
     <li> <p>[!UICONTROL Simple]</p> </li> 
     <li> <p>[!UICONTROL Using SOSL (Salesforce Object Search Language)]</p> </li> 
     <li> <p>[!UICONTROL Using SOQL (Salesforce Object Query Language)]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Type] </p> </td> 
   <td> <p>Si vous avez sélectionné le type Recherche simple, choisissez le type d’enregistrement [!DNL Salesforce] que vous souhaitez que le module recherche.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query] / [!UICONTROL SOSL Query] / [!UICONTROL SOQL Query]</td> 
   <td> <p>Saisissez la requête par laquelle vous souhaitez effectuer la recherche.</p> <p>Pour plus d’informations sur SOSL, consultez la section <a href="https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_sosl.htm">Salesforce Object Search Language (SOSL)</a> dans la documentation [!DNL Salesforce].</p> <p>Pour plus d’informations sur SOQL, consultez la section <a href="https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_soql.htm">Salesforce Object Query Language (SOQL)</a> dans la documentation [!DNL Salesforce].</p> <p>Note : la valeur du paramètre <code>RETURNING </code> influence la sortie du module. Si vous utilisez <code>LIMIT</code>, [!DNL Fusion] ignorera les paramètres du champ [!UICONTROL Maximal count of records]. Si vous ne définissez aucune limite, Fusion insérera la valeur [!UICONTROL LIMIT = Maximal count of records].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal count of records].</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>
