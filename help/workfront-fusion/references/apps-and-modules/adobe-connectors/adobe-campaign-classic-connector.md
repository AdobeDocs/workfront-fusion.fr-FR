---
title: Modules Adobe Campaign v7/v8
description: Avec les modules  [!DNL Adobe Campaign]   [!DNL Adobe Campaign] , vous pouvez lancer un scénario Adobe Workfront Fusion en fonction des événements de votre compte, créer, lire ou mettre à jour des contrats et d’autres enregistrements, rechercher des enregistrements à l’aide des critères que vous avez définis et charger des documents.
author: Becky
feature: Workfront Fusion
exl-id: 9fdff26c-c7c0-4eb8-a36f-4aeaf432b333
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1326'
ht-degree: 82%

---

# Modules [!DNL Adobe Campaign]

Avec les modules [!DNL Adobe Campaign], vous pouvez démarrer un scénario Adobe Workfront Fusion en fonction des événements de votre compte [!DNL Adobe Campaign v7/v8], créer, lire ou mettre à jour des enregistrements, rechercher des enregistrements à l’aide des critères que vous avez définis et effectuer des appels d’API personnalisés.

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

Vous devez ajouter les adresses IP Fusion à [!DNL Adobe Campaign].

* Pour plus d’informations sur l’ajout d’adresses IP à votre liste autorisée Campaign, voir [Ajouter des adresses IP à la liste autorisée](https://experienceleague.adobe.com/fr/docs/control-panel/using/sftp-management/ip-range-allow-listing#adding-ip-addresses-allow-list) dans la documentation Adobe Campaign.
* Pour obtenir la liste des adresses IP à ajouter à la place sur la liste autorisée de données, voir [Configurer des adresses IP pour Fusion dans la place sur la liste autorisée de données de votre organisation](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md).

## Informations sur l’API Adobe Campaign

Le connecteur Adobe Campaign utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.7.22</td> 
  </tr>
 </tbody> 
 </table>

## Connexion de [!DNL Adobe Campaign] à Adobe Workfront Fusion

>[!IMPORTANT]
>
>Il est vivement recommandé de créer une connexion serveur à serveur. Adobe Campaign a mis à jour son API pour n’accepter que les connexions de serveur à serveur. Si vous vous connectez à la version 8 ou ultérieure de Campaign, vous **devez** créez une connexion serveur à serveur.
>
>Pour plus d’informations sur les nouvelles exigences de connexion de Campaign, voir [Migration des opérateurs techniques Campaign vers Adobe Developer Console](https://experienceleague.adobe.com/fr/docs/campaign/technotes-ac/tn-new/ims-migration) dans la documentation de Campaign.

1. Dans n’importe quel module [!DNL Adobe Campaign], cliquez sur **[!UICONTROL Ajouter]** en regard du champ [!UICONTROL Connexion].
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
            <p>Indiquez si vous créez une connexion de base ou une connexion serveur à serveur.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Connection name]</td>
          <td>
            <p>Saisissez un nom pour cette connexion.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Base URL]</td>
          <td>Saisissez l’URL de base que vous utilisez pour vous connecter à votre instance [!DNL Adobe Campaign].</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Username]</td>
          <td>Si vous créez une connexion de base, saisissez votre nom d’utilisateur ou d’utilisatrice Adobe Campaign.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Password]</td>
          <td>Si vous créez une connexion de base, saisissez votre mot de passe Adobe Campaign.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client ID]</td>
          <td>Si vous créez une connexion serveur à serveur, saisissez votre [!UICONTROL Client ID] [!DNL Adobe]. Vous pouvez le trouver dans la section [!UICONTROL Credentials details] d’[!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]</td>
          <td>Si vous créez une connexion serveur à serveur, saisissez votre [!UICONTROL Client Secret] [!DNL Adobe]. Vous pouvez le trouver dans la section [!UICONTROL Credentials details] de l’[!DNL Adobe Developer Console].
        </tr>
     </tbody>
    </table>
1. Cliquez sur **[!UICONTROL Continuer]** pour créer la connexion et retourner au module.

## Modules [!DNL Adobe Campaign] et leurs champs

Lorsque vous configurez les modules [!DNL Adobe Campaign], Workfront Fusion affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Adobe Campaign] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

<!--* [Triggers](#triggers)-->
* [Actions](#actions)
* [Recherches](#searches)

<!--### Triggers

#### [!UICONTROL Watch records]

This scheduled trigger module starts a scenario when a record changes.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Campaign], see <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Create a connection to [!DNL Adobe Campaign]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Select whether you want to watch for new records, updated records, or both.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Select the resource that you want to watch for.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields to include in output]</td> 
   <td>Select the fields that you want to include in the module's output.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom fields to include in output]</td> 
   <td>For each custom field that you want to include in output, click <b>[!UICONTROL Add]</b> and enter the name of the custom field.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned results]</td> 
   <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td> 
  </tr> 
 </tbody> 
</table>-->


### Actions

* [[!UICONTROL Créer un enregistrement]](#create-a-record)
* [[!UICONTROL Supprimer un enregistrement]](#delete-record)
* [[!UICONTROL Effectuer un appel d’API personnalisé]](#make-a-custom-api-call)
* [[!UICONTROL Exécuter une action]](#perform-an-action)
* [[!UICONTROL Lire un enregistrement]](#read-a-record)
* [[!UICONTROL S’abonner ou se désabonner]](#subscribe-or-unsubscribe)
* [[!UICONTROL Mettre à jour un enregistrement]](#update-record)

#### [!UICONTROL Créer un enregistrement]

Ce module d’action crée un enregistrement dans [!DNL Adobe Campaign].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Campaign], voir <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Créer une connexion à [!DNL Adobe Campaign]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Sélectionnez le type d’enregistrement [!DNL Adobe Campaign] à créer.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields] </td> 
   <td>Sélectionnez les champs pour lesquels vous souhaitez définir des valeurs lors de la création de l’enregistrement, puis renseignez les valeurs de ces champs. Les champs varient en fonction du type d’enregistrement sélectionné.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom fields]</td> 
   <td> Pour chaque champ personnalisé à ajouter au nouvel enregistrement, cliquez sur <b>[!UICONTROL Add item]</b> et saisissez ou mappez le nom et la valeur du champ. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Supprimer l’enregistrement]

Ce module d’action supprime un seul enregistrement d’[!DNL Adobe Campaign].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Campaign], voir <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Créer une connexion à [!DNL Adobe Campaign]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Sélectionnez le type de ressource à supprimer.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Saisissez ou mappez l’ID de la ressource que vous souhaitez supprimer.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Effectuer un appel API personnalisé]

Ce module effectue un appel API personnalisé à l’API [!DNL Adobe Campaign].

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Campaign], voir <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Créer une connexion à [!DNL Adobe Campaign]</a> dans cet article.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Action]</td>
      <td><p>Sélectionnez l’action que vous souhaitez que l’appel API effectue.</p>
      <p>[!UICONTROL Execute query]</p>
      <p>[!UICONTROL Write]</p>
      <p>[!UICONTROL Get entity if more recent]</p>
      <p>[!UICONTROL Select all]</p>
      <p>[!UICONTROL Push event]</p>
    </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p>
        <p>Par exemple, <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion ajoute automatiquement l’en-tête du jeton [!UICONTROL x-security].</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL XML Body]</td>
   <td> <p>Ajoutez le contenu du corps de l’appel API au format XML, sans l’élément de session. </td>     </tr>
  </tbody>
</table>


#### [!UICONTROL Exécuter une action]

Ce module d’action exécute une action sélectionnée sur un objet dans l’API [!DNL Adobe Campaign].

Pour plus d’informations sur des actions et des champs spécifiques, voir Documentation de l’API [[!DNL Adobe Campaign] &#x200B;](https://experienceleague.adobe.com/developer/campaign-api/api/p-14.html?lang=fr).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Campaign], voir <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Créer une connexion à [!DNL Adobe Campaign]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td><p>Sélectionnez l’action à effectuer sur l’objet.</p>
   <ul>
   <li><p><b>[!DNL List]</b></p><p> Pour les champs disponibles, voir <a href="#search" class="MCXref xref" >[!UICONTROL Search]</a> dans cet article. </p></li>
     <li><p><b>[!UICONTROL Get]</b></p><p> Pour les champs disponibles, voir <a href="#search" class="MCXref xref" >[!UICONTROL Search]</a> dans cet article. </p></li> 
   <li><p><b>[!UICONTROL Create]</b></p><p> Pour les champs disponibles, voir <a href="#create-a-record" class="MCXref xref" >[!UICONTROL Create a record]</a> dans cet article. </p></li>
   <li><p><b>[!UICONTROL Update]</b></p><p> Pour les champs disponibles, voir <a href="#update-record" class="MCXref xref" >[!UICONTROL Update a record]</a> dans cet article. </p></li>
   <li><p><b>[!UICONTROL Delete]</b></p><p> Pour les champs disponibles, voir <a href="#delete-record" class="MCXref xref" >[!UICONTROL Delete a record]</a> dans cet article. </p></li>
   </ul>
   </td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Lire un enregistrement]

Ce module d’action lit un enregistrement à partir d’[!DNL Adobe Campaign].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Campaign], voir <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Créer une connexion à [!DNL Adobe Campaign]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Sélectionnez le type d’enregistrement [!DNL Adobe Campaign] que vous souhaitez lire.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL ID] </td> 
   <td>Saisissez ou mapper l’ID de l’enregistrement que vous souhaitez lire.</td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Fields to include in output] </td> 
   <td>Sélectionnez les champs que vous souhaitez inclure dans la sortie du module.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom fields to include in output]</td> 
   <td>Pour chaque champ personnalisé à inclure dans la sortie, cliquez sur <b>[!UICONTROL Add]</b> et saisissez le nom du champ personnalisé.</td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Abonner ou désabonner]

Ce module d’action abonne une personne à un service d’information ou la désabonne.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Campaign], voir <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Créer une connexion à [!DNL Adobe Campaign]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscribe or unsubscribe]</td> 
   <td>Indiquez si vous souhaitez vous abonner au service d’information ou vous en désabonner.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Service name]</td> 
   <td>Sélectionnez le service auquel vous souhaitez vous abonner ou dont vous souhaitez vous désabonner.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Recipient email address] </td> 
   <td>Saisissez ou mappez l’adresse e-mail de la personne que vous souhaitez abonner au service d’information ou que vous souhaitez désabonner de ce service.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mettre à jour l’enregistrement]

Ce module d’action met à jour un seul enregistrement dans [!DNL Adobe Campaign].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Campaign], voir <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Créer une connexion à [!DNL Adobe Campaign]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Sélectionnez le type d’enregistrement [!DNL Adobe Campaign] à créer.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL ID] </td> 
   <td>Saisissez ou mappez l’ID de l’enregistrement que vous souhaitez mettre à jour.</td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL Fields] </td> 
   <td>Sélectionnez les champs pour lesquels vous souhaitez mettre à jour les valeurs, puis renseignez les valeurs de ces champs. Les champs varient en fonction du type d’enregistrement sélectionné.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom fields]</td> 
   <td> Pour chaque champ personnalisé à mettre à jour, cliquez sur <b>[!UICONTROL Add item]</b> et saisissez ou mappez le nom et la valeur du champ. </td> 
  </tr> 
 </tbody> 
</table>

### Recherches

#### [!UICONTROL Rechercher]

Ce module de recherche renvoie des enregistrements en fonction des critères spécifiés.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Campaign], voir <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Créer une connexion à [!DNL Adobe Campaign]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Sélectionnez le type d’enregistrement [!DNL Adobe Campaign] à créer.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search criteria]</td> 
   <td>Saisissez les champs et les valeurs que la recherche doit utiliser. Les champs dépendent de la ressource sélectionnée.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</td> 
  </tr> 
 </tbody> 
</table>
