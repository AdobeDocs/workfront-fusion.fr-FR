---
title: Modules Microsoft Dynamics 365
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent Microsoft Dynamics 365 et les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: 16ae173b-10ce-481d-8f6c-1df0e65f7c0e
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1866'
ht-degree: 74%

---

# [!DNL Microsoft Dynamics 365 modules]

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent [!DNL Microsoft Dynamics 365] et les connecter à plusieurs applications et services tiers.

>[!NOTE]
>
>Le connecteur [!DNL Microsoft Dynamics 365] ne prend pas en charge [!DNL Dynamics Finance and Operations].
>
>Pour plus d’informations sur le connecteur [!DNL Microsoft Dynamics 365 Finance and Operations], voir [[!DNL Microsoft Dynamics 365 Finance and Operations] modules](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/dynamics-finance-operations-modules.md).

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

Pour utiliser [!DNL Microsoft Dynamics] 365, vous devez avoir un compte [!DNL Microsoft Dynamics 365].

## Connecter Microsoft Dynamics 365 à Workfront Fusion

Vous pouvez créer une connexion à votre compte [!DNL Microsoft Dynamics 365] directement à partir d’un module [!DNL Microsoft Dynamics 365].

>[!NOTE]
>
>Certaines applications Microsoft utilisent la même connexion, qui est liée à des autorisations d’utilisateur ou d’utilisatrice. Ainsi, lors de la création d’une connexion, l’écran de consentement aux autorisations affiche les autorisations précédemment accordées à la connexion de cet utilisateur ou de cette utilisatrice, en plus des nouvelles autorisations nécessaires à l’application actuelle.
>
>Par exemple, si un utilisateur ou une utilisatrice dispose d’autorisations « Lire le tableau » accordées via le connecteur Excel, puis crée une connexion dans le connecteur Outlook pour lire les e-mails, l’écran de consentement aux autorisations affiche à la fois l’autorisation « Lire le tableau » déjà accordée et l’autorisation « Écrire des e-mails » nouvellement requise.

1. Dans n’importe quel module [!DNL Microsoft Dynamics 365], cliquez sur **[!UICONTROL Ajouter]** en regard du champ [!UICONTROL Connexion].


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
          <td>Saisissez votre [!UICONTROL Client ID] [!DNL Microsoft Dynamics].</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]<p>(Facultatif)</p></td>
          <td>Saisissez votre [!DNL Microsoft Dynamics] [!UICONTROL Client Secret].
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Authentication URL]</td>
          <td>Saisissez l’URL que votre instance de Workfront utilisera pour authentifier cette connexion. <p>La valeur par défaut est <code>https://oauth.my.workfront.com/integrations/oauth2</code>.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Resource]</td>
          <td>saisissez l’adresse de votre compte [!DNL Dynamics 365], sans <code>>https://</code>.</p>
        </tr>
      </tbody>
    </table>
1. Cliquez sur **[!UICONTROL Continuer]** pour créer la connexion et retourner au module.

>[!NOTE]
>
>Lors de l’enregistrement de Workfront Fusion sur votre portail [!DNL Microsoft Azure], utilisez l’URI de redirection suivant :
>
>* `https://app.workfrontfusion.com/oauth/cb/workfront-microsoft-dynamics2`


## Modules [!DNL Microsoft Dynamics 365] et leurs champs

Lorsque vous configurez les modules [!DNL Microsoft Dynamics 365], Workfront Fusion affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Microsoft Dynamics 365] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Déclencheurs](#triggers)
* [Actions](#actions)
* [Recherches](#searches)

### Déclencheurs

* [[!UICONTROL Surveiller des enregistrements (en temps réel)]](#watch-records-real-time)
* [[!UICONTROL Surveiller des enregistrements (prévus)]](#watch-records-scheduled)

#### [!UICONTROL Surveiller des enregistrements (en temps réel)]

Ce module de déclenchement instantané exécute un scénario lorsqu’un enregistrement (objet) que vous spécifiez est créé ou mis à jour dans [!DNL Dynamics 365].

Un webhook est nécessaire pour ce module.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Sélectionnez le webhook que vous souhaitez utiliser pour ce module. </p> <p>Pour ajouter un nouveau webhook :</p> 
    <ol> 
     <li value="1"> <p>Cliquez sur <strong>[!UICONTROL Add]</strong> à droite du champ Webhook.</p> </li> 
     <li value="2"> <p>Dans le champ Nom du <strong>[!UICONTROL Webhook]</strong>, saisissez un nom explicite pour le webhook.</p> </li> 
     <li value="3"> <p>Dans le champ <strong>[!UICONTROL Connection]</strong>, sélectionnez la connexion que vous souhaitez utiliser.</p> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Microsoft Dynamics 365] à Workfront Fusion, voir <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Microsoft Dynamics 365] à Workfront Fusion</a> dans cet article. </p> </li> 
     <li value="4"> <p>Cliquez sur <strong>[!UICONTROL Save]</strong> pour enregistrer votre webhook et revenir au module.</p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Surveiller des enregistrements (prévus)]

Ce module de déclenchement planifié exécute un scénario lorsqu’un enregistrement dans l’objet que vous spécifiez est créé ou mis à jour après la dernière exécution planifiée de ce scénario.

La sortie du module indique si l&#39;enregistrement trouvé est nouveau ou mis à jour. Si l’enregistrement a été ajouté et mis à jour au cours de la période, il est renvoyé en tant que nouvel enregistrement.

Cela se produit à un intervalle planifié régulier que vous spécifiez.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> «
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Microsoft Dynamics 365] à Workfront Fusion, voir <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Microsoft Dynamics 365] à Workfront Fusion</a> dans cet article. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Include]</td> 
   <td>Choisissez si vous souhaitez que le module regarde <strong>[!UICONTROL Nouveaux enregistrements uniquement]</strong>, <strong>[!UICONTROL Enregistrements mis à jour uniquement]</strong> ou <strong>[!UICONTROL Enregistrements nouveaux et mis à jour]</strong>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>Sélectionnez le type d’enregistrement [!UICONTROL Microsoft Dynamics 365] que vous souhaitez que le scénario surveille.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Sélectionnez les informations que vous souhaitez inclure dans le bundle de sortie pour ce module.
Les champs sont disponibles en fonction du type d’entité sélectionné.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Max Records]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [[!UICONTROL Créer un enregistrement]](#create-record)
* [[!UICONTROL Lancer un appel API]](#make-an-api-call)
* [[!UICONTROL Supprimer un enregistrement]](#delete-record)
* [[!UICONTROL Lire des enregistrements]](#read-records)
* [[!UICONTROL Mettre à jour des enregistrements]](#update-record)


#### [!UICONTROL Créer un enregistrement]

Ce module d’action crée une entité, telle qu’un rendez-vous ou une tâche.

Vous spécifiez des informations sur l’entité que vous souhaitez créer.

Le module renvoie l’ID de la nouvelle entité et des champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Microsoft Dynamics 365] à Workfront Fusion, voir <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Microsoft Dynamics 365] à Workfront Fusion</a> dans cet article. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>Sélectionnez le type d’entité que vous souhaitez que le module crée.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select Fields to Map]</td> 
   <td>Sélectionnez les champs pour lesquels vous souhaitez inclure des valeurs lors de la création de l’enregistrement. Les champs disponibles dépendent du type d’entité.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Property fields]</td> 
   <td> Il s’agit des champs que vous avez sélectionnés. Saisissez la valeur que vous souhaitez donner à l’enregistrement pour une propriété donnée. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Supprimer l’enregistrement]

Ce module d’action supprime une entité.

Vous spécifiez l’identifiant de l’entité.

Le module renvoie l’identifiant de l’entité et de tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Microsoft Dynamics 365] à Workfront Fusion, voir <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Microsoft Dynamics 365] à Workfront Fusion</a> dans cet article. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td> <p>Sélectionnez le type d’entité que vous souhaitez que le module supprime.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td> <p>Saisissez ou mappez l’identifiant [!DNL Microsoft Dynamics 365] unique de l’enregistrement que vous souhaitez que le module supprime.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Réaliser un appel API]

Ce module d’action permet d’effectuer un appel authentifié personnalisé vers l’API [!DNL Microsoft Dynamics 365]. De cette façon, vous pouvez créer une automatisation du flux de données qui ne peut pas être réalisée par les autres modules [!DNL Microsoft Dynamics 365].

Le module renvoie des informations sur le code d’état, les en-têtes et le corps. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Pour en savoir plus, consultez la documentation [!DNL Microsoft] sur l’utilisation de [!DNL Dynamics 365 Customer Engagement Web API].

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Microsoft Dynamics 365] à Workfront Fusion, voir <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Microsoft Dynamics 365] à Workfront Fusion</a> dans cet article. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Saisissez un chemin d’accès relatif à <code>&lt;Instance URL>/api/data/v9.1/</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> <p>Pour en savoir plus, voir</p> </td> 
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
 </tbody> 
</table>

#### [!UICONTROL Lire les enregistrements]

Ce module d’action lit les données d’une seule entité dans [!DNL Microsoft Dynamics 365].

Vous spécifiez l’identifiant de l’entité.

Le module renvoie l’identifiant de l’entité et tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Microsoft Dynamics 365] à Workfront Fusion, voir <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Microsoft Dynamics 365] à Workfront Fusion</a> dans cet article. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>Sélectionnez le type d’entité que vous souhaitez que le module lise.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Sélectionnez les informations que vous souhaitez inclure dans le bundle de sortie pour ce module.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Saisissez ou mappez l’identifiant [!DNL Microsoft Dynamics 365] unique de l’enregistrement que vous souhaitez que le module lise.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mettre à jour un enregistrement]

Ce module d’action met à jour une entité.

Vous spécifiez l’identifiant de l’entité.

Le module renvoie l’identifiant de l’enregistrement mis à jour et les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Microsoft Dynamics 365] à Workfront Fusion, voir <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Microsoft Dynamics 365] à Workfront Fusion</a> dans cet article. </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>Sélectionnez le type d’entité que le module doit mettre à jour.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select Fields to Map]</td> 
   <td>Sélectionnez les champs pour lesquels vous souhaitez inclure des valeurs lors de la création de l’enregistrement. Les champs disponibles dépendent du type d’entité.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Property fields]</td> 
   <td>Il s’agit des champs que vous avez sélectionnés. Saisissez la valeur que vous souhaitez donner à l’enregistrement pour une propriété donnée.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Saisissez ou mappez l’identifiant unique [!DNL Microsoft Dynamics] 365 de l’enregistrement que le module doit mettre à jour.</td> 
  </tr> 
 </tbody> 
</table>

### Recherches

#### [!UICONTROL Rechercher des enregistrements]

Ce module de recherche trouve des enregistrements dans un objet de [!DNL Microsoft Dynamics 365] qui correspondent à la requête que vous spécifiez. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Microsoft Dynamics 365] à Workfront Fusion, voir <a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Microsoft Dynamics 365] à Workfront Fusion</a> dans cet article. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>Sélectionnez le type d’entité que le module doit mettre à jour.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filters]</td> 
   <td> <p>Sélectionnez le filtre à utiliser pour cette recherche.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Standard Filters]</strong> </p> <p>Configurez le filtre en sélectionnant un champ et un opérateur, puis en saisissant ou en mappant la valeur à rechercher. Vous pouvez utiliser des règles AND ou OR pour votre filtre.</p> </li> 
     <li> <p><strong>[!UICONTROL Query Functions]</strong> </p> <p>Saisissez la fonction de requête de l’API web [!DNL Dynamics 365] que vous souhaitez utiliser pour la recherche. </p> <p>Pour plus d’informations sur les fonctions de requête, voir <a href="https://docs.microsoft.com/fr-fr/dynamics365/customer-engagement/web-api/queryfunctions?view=dynamics-ce-odata-9">Référence de fonction de requête d’API Web</a> dans la documentation [!DNL Microsoft].</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort]</td> 
   <td> <p>Indiquez l’ordre dans lequel les éléments sont renvoyés. Vous pouvez ajouter plusieurs types.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Field]</strong> </p> <p>Indiquez le champ de tri des résultats.</p> </li> 
     <li> <p><strong>[!UICONTROL Direction]</strong> </p> <p>Définissez la direction du tri (ascendant ou descendant).</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Max Records]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Sélectionnez les informations que vous souhaitez inclure dans le bundle de sortie pour ce module.</p> </td> 
  </tr> 
 </tbody> 
</table>
