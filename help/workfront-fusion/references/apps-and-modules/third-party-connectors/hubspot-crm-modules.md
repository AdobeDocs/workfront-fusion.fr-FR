---
title: Modules CRM HubSpot
description: Les modules CRM HubSpot  [!DNL Adobe Workfront Fusion]  vous permettent de surveiller les événements, les enregistrements, les contacts, les engagements et les envois de fichiers et de formulaires, ainsi que de les créer, récupérer, mettre à jour et supprimer dans votre compte  [!DNL HubSpot CRM] .
author: Becky
feature: Workfront Fusion
exl-id: b8a1bbcd-337e-4c92-a1a6-d6d4bab1f440
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '5655'
ht-degree: 33%

---

# Modules [!DNL HubSpot CRM]

Les modules [!DNL Adobe Workfront Fusion] [!DNL HubSpot CRM] vous permettent de surveiller les événements, les enregistrements, les contacts, les engagements, les envois de fichiers et de formulaires, ainsi que de les créer, récupérer, mettre à jour et supprimer dans votre compte [!DNL HubSpot CRM].

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

Pour utiliser les modules [!DNL HubSpot CRM], vous devez disposer d’un compte [!DNL HubSpot CRM].

## Informations sur l’API HubSpot CRM

Le connecteur CRM HubSpot utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td>https://api.hubapi.com</td> 
  </tr>
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v2.0.14</td> 
  </tr>
 </tbody> 
 </table>

## Connecter [!DNL Adobe Workfront Fusion] à [!DNL HubSpot CRM]

Pour suivre la procédure de connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], consultez la section [Créer une connexion à  [!DNL Adobe Workfront Fusion]  - Instructions de base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md).

>[!NOTE]
>
>Lors de la configuration d&#39;une connexion, sélectionnez le type de connexion **HubSpot CRM**. Le type HubSpot CRM (obsolète) prend en charge les connexions existantes, mais nous vous recommandons de ne pas l’utiliser pour créer de nouvelles connexions.

## Modules [!DNL HubSpot CRM] et leurs champs

Lorsque vous configurez les modules [!DNL Hubspot CRM], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Hubspot CRM] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Objets CRM](#crm-objects)
* [Enregistrements (transactions, contacts et entreprises)](#records-deals-contacts-and-companies)
* [Contacts](#contacts)
* [Transactions](#deals)
* [Entreprises](#companies)
* [Engagements](#engagements)
* [Événements et notifications](#events-and-notifications)
* [Fichiers](#files)
* [Tâches](#tasks)
* [Utilisateurs](#users)
* [Tickets](#tickets)
* [Formulaires](#forms)
* [Réseaux Sociaux (Diffusion)](#social-media-broadcast)
* [Publications du blog](#blog-posts)
  <!--* [Workflows]-->
* [Abonnements](#subscriptions)
  <!--* [Associations](#associations)-->
* [Autre](#other)

+++**Objets CRM**

### Objets CRM

* [Rechercher des objets CRM](#search-for-crm-objects)
* [Objets Watch CRM](#watch-crm-objects)

#### [!UICONTROL Search for CRM Objects]

Ce module de recherche recherche des objets CRM à partir de propriétés personnalisées ou de requêtes. Pour rechercher des produits ou des éléments de ligne, utilisez une connexion spéciale avec une portée personnalisée requise.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Saisissez ou mappez le nombre maximal d’éléments que le module renverra dans un cycle d’exécution.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object Type to Search]</td> 
   <td>Sélectionnez le type d’objet CRM Hubspot que vous souhaitez rechercher.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output properties]</td> 
   <td>Sélectionnez les propriétés à afficher dans la sortie du module. Les champs disponibles dépendent de l’objet que vous avez sélectionné.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by] </td> 
   <td> <p>Sélectionner le mode de filtrage de la recherche</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Query]</strong> </p> <p>Entrer ou mapper la requête</p> </li> 
     <li> <p><strong>[!UICONTROL Properties]</strong> </p> <p>Saisissez les groupes ou filtres de votre recherche.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort by]</td> 
   <td> <p>Cliquez si vous souhaitez trier les résultats. Si vous choisissez de trier les résultats, les champs suivants s’affichent. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Property name]</strong> </p> <p>Sélectionnez la propriété par laquelle vous souhaitez trier les résultats</p> </li> 
     <li> <p><strong>[!UICONTROL Direction]</strong> </p> <p>Choisissez si vous souhaitez trier les résultats dans une direction ascendante ou descendante.</p> </li> 
    </ul> </td> 
  </tr> 
   <tr> 
    <td role="rowheader">Décalage de début</td> 
    <td>Saisissez ou mappez l’ID du premier élément pour lequel vous souhaitez récupérer des détails. Ce module renvoie uniquement jusqu’à 5 000 résultats à la fois. La définition d'un décalage de début vous permet de récupérer des éléments autres que les 5 000 premiers. Si le décalage de début est de 5 000, le module renvoie les éléments 5 000 à 9 9999.</td> 
   </tr>
 </tbody> 
</table>

#### Objets Watch CRM

Ce module de déclenchement démarre un scénario lorsqu’un objet CRM est créé ou mis à jour.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Saisissez ou mappez le nombre maximal d’éléments que le module renverra dans un cycle d’exécution.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object type to search]</td> 
   <td> <p>Sélectionnez le type d’objet que vous souhaitez rechercher.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Properties]</td> 
   <td>Sélectionnez les propriétés que vous souhaitez inclure dans la sortie de ce module.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Created/Updated]</td> 
   <td>Indiquez si vous souhaitez observer les objets créés (nouveaux) ou mis à jour (modifiés).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by]</td> 
   <td>Vous pouvez ajouter un filtre pour vous assurer que le scénario ne démarre que lorsque certaines conditions sont remplies.<ul><li><b>Requête</b><p>Saisissez la requête en fonction de laquelle vous souhaitez effectuer le filtrage.</li><li><b>Propriétés</b><p>Pour chaque propriété que vous souhaitez utiliser pour filtrer les résultats, cliquez sur <b>Ajouter un élément</b> et saisissez le nom, l’opérateur et la valeur de la propriété.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Enregistrements (affaires, contacts et sociétés)**

### Enregistrements (transactions, contacts et entreprises)

* [Créer un enregistrement](#create-a-record)
* [[!UICONTROL Create a Record (Legacy)]](#create-a-record-legacy)
* [[!UICONTROL Delete a Record]](#delete-a-record)
* [[!UICONTROL Get a Record]](#get-a-record)
* [[!UICONTROL Get a Record Property]](#get-a-record-property)
* [Lister les enregistrements](#list-records)
* [[!UICONTROL Update a Record]](#update-a-record)
* [[!UICONTROL Watch Records]](#watch-records)

#### Créer un enregistrement

Ce module d’action crée un contact, une entreprise ou une affaire.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement que vous souhaitez créer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Property groups]</td> 
   <td>Pour chaque propriété que vous souhaitez ajouter lors de la création de l’enregistrement, sélectionnez le groupe dans lequel se trouve la propriété. Le groupe de propriétés s’ouvre, puis vous pouvez renseigner la valeur des propriétés. Les groupes de propriétés et les propriétés disponibles dépendent du type d’enregistrement que vous souhaitez créer.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Record (Legacy)]

Ce module d’action crée un contact, une entreprise ou une transaction.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement que vous souhaitez créer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Properties]</td> 
   <td>Renseignez les propriétés à définir pour l’enregistrement. Les champs disponibles dépendent du type d’enregistrement à créer.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Record]

Ce module d’action supprime un contact, une société ou une transaction.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Sélectionnez le type d’enregistrement à supprimer.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Saisissez l’identifiant du contact, de l’entreprise ou de la transaction à supprimer. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Record]

Ce module d’action récupère les détails d’un contact, d’une entreprise ou d’une transaction.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement.</p> 
    <ul> 
     <li>[!UICONTROL Contact]</li> 
     <li>[!UICONTROL Company] </li> 
     <li>[!UICONTROL Deal]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search Type]</td> 
   <td>Si vous recevez un contact, indiquez si vous souhaitez l’identifier par identifiant ou par adresse e-mail.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Saisissez l’identifiant du contact, de l’entreprise ou de la transaction à récupérer. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>Saisissez l’adresse e-mail du contact dont vous souhaitez récupérer les informations. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Record Property]

Ce module d’action récupère les métadonnées d’une propriété d’enregistrement spécifique par son nom (interne).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Sélectionnez le type d’enregistrement dont vous souhaitez récupérer les métadonnées.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Property Name]</td> 
   <td>Sélectionnez la propriété dont vous souhaitez récupérer les métadonnées.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Option ID]</td> 
   <td> <p> Certaines propriétés disposent d’un ensemble d’options disponibles qu’un utilisateur ou une utilisatrice peut sélectionner comme valeur de propriété. Saisissez l’identifiant de l’option qui représente la valeur de propriété que vous souhaitez récupérer.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Lister les enregistrements

Ce module de recherche renvoie une liste de contacts, d’entreprises ou d’offres. La production est limitée à 5 000 contacts, 12 500 entreprises ou 12 500 contrats.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td> <p>Sélectionnez le type d'enregistrement à renvoyer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Properties]</td> 
   <td>Sélectionnez les propriétés que vous souhaitez inclure dans la sortie de ce module.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr>

</tbody> 
</table>

#### [!UICONTROL Update a Record]

Ce module d’action met à jour un contact, une entreprise ou une transaction.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Sélectionnez le type d’enregistrement que vous souhaitez mettre à jour.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search Type]</td> 
   <td> <p>Si vous recevez un contact, sélectionnez le mode d’identification de l’enregistrement :</p> 
    <ul> 
     <li> <p>[!UICONTROL ID]</p> </li> 
     <li> <p>[!UICONTROL Email]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Saisissez l’identifiant du contact, de l’entreprise ou de la transaction que vous souhaitez mettre à jour. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>Saisissez l’adresse e-mail du contact dont vous souhaitez mettre à jour les informations. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Properties]</td> 
   <td>Renseignez les propriétés à définir pour l’enregistrement. Les champs disponibles dépendent du type d’enregistrement à créer.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Records]

Ce module déclencheur lance un scénario lorsqu’un contact, une entreprise ou une transaction a fait l’objet d’une modification ou d’une création au cours des 30 derniers jours. La sortie est limitée à 10 000 enregistrements.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>Sélectionnez le type d’enregistrement comportant la propriété que vous souhaiter surveiller.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search]</td> 
   <td>Indiquez si vous souhaitez surveiller les enregistrements récemment modifiés ou récemment créés.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Properties]</td> 
   <td>Sélectionnez les propriétés à inclure dans la sortie du module.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Contacts**

### Contacts

* [[!UICONTROL Add Contacts to a List]](#add-contacts-to-a-list)
* [Créer/mettre à jour un contact](#createupdate-a-contact)
* [[!UICONTROL Create/Update a Contact (Legacy)]](#createupdate-a-contact-legacy)
* [[!UICONTROL Create/Update a Group of Contacts]](#createupdate-a-group-of-contacts)
* [[!UICONTROL List Contacts]](#list-contacts)
* [[!UICONTROL List Contacts of a Company]](#list-contacts-of-a-company)
* [[!UICONTROL Merge contacts]](#merge-contacts)
* [[!UICONTROL Remove a Contact from a List]](#remove-a-contact-from-a-list)
* [[!UICONTROL Search for Contacts]](#search-for-contacts)
* [Observer les contacts ajoutés à une liste](#watch-contacts-added-to-a-list)

#### [!UICONTROL Add Contacts to a List]

Ce module ajoute à une liste de contacts les enregistrements de contacts déjà créés dans le système.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID] </td> 
   <td>Sélectionnez l’ID de la liste à laquelle vous souhaitez ajouter le contact. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL IDs/Emails] </td> 
   <td> <p>Sélectionnez le mode d’identification des contacts que vous souhaitez ajouter à la liste :</p> 
    <ul> 
     <li> <p>[!UICONTROL IDs]</p> <p>Ajoutez les ID des contacts que vous souhaitez ajouter à la liste.</p> </li> 
     <li> <p>[!UICONTROL Emails]</p> <p>Ajoutez les adresses e-mail des contacts que vous souhaitez ajouter à la liste.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Créer/mettre à jour un contact

Ce module d&#39;action crée un contact s&#39;il n&#39;existe pas dans un portail. Si le contact existe sur le portail, ce module le met à jour avec les valeurs fournies.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Property groups]</td> 
   <td>Pour chaque propriété que vous souhaitez ajouter lors de la création du contact, sélectionnez le groupe dans lequel se trouve la propriété. Le groupe de propriétés s’ouvre, puis vous pouvez renseigner les valeurs des propriétés.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create/Update a Contact (Legacy)]

Crée un contact s’il n’existe pas encore dans un portail ou le met à jour avec les dernières valeurs de propriété s’il existe dans un portail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Properties]</td> 
   <td>Renseignez les propriétés que vous souhaitez définir ou mettre à jour pour le contact. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create/Update a Group of Contacts]

Crée un groupe de contacts ou les met à jour s’ils existent déjà. Les performances sont meilleures lorsque la taille du lot est limitée à 100 contacts ou moins. Les modifications effectuées via ce point d’entrée sont traitées de manière asynchrone. Plusieurs minutes peuvent donc être nécessaires pour que les modifications soient appliquées aux enregistrements de contacts.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Batch of Contacts to Create/Update] </td> 
   <td> <p>Ajoutez le lot de contacts.</p> <p>Cliquez sur <strong>[!UICONTROL Add item]</strong> pour ajouter un nouveau contact. Dans la fenêtre qui s’affiche, saisissez ou mappez les informations suivantes :</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Search Type]</strong> </p> <p>Sélectionnez le mode d’identification du contact :</p> 
      <ul> 
       <li> <p>[!UICONTROL ID]</p> <p>Saisissez l’ID du contact que vous souhaitez créer ou mettre à jour. </p> </li> 
       <li> <p>[!UICONTROL Email]</p> <p>Saisissez l’adresse e-mail du contact que vous souhaitez créer ou mettre à jour. </p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Properties]</strong> </p> <p>Renseignez les propriétés que vous souhaitez définir ou mettre à jour pour le contact.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Contacts]

Renvoie tous les contacts qui ont été créés dans le portail. La sortie est limitée à 5 000 contacts. Pour répertorier les contacts précédents ou suivants, vous pouvez utiliser le paramètre [!UICONTROL advanced] pour décaler la liste.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Nombre maximum de contacts que [!DNL Workfront Fusion] doit renvoyer pendant un cycle d’exécution de scénario. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output properties]</td> 
   <td>Sélectionnez les propriétés à afficher dans la sortie du module. </td> 
  </tr> 
   <tr> 
    <td role="rowheader">ID de contact [décalage de début] </td> 
    <td>Saisissez ou mappez l’identifiant de l’utilisateur que vous souhaitez pour commencer la liste. Par exemple, définir l’ID de contact comme ID du 101e contact permettra au module de répertorier les contacts 101-5100 plutôt que 1-5000. </td> 
   </tr>
 </tbody> 
</table>

#### [!UICONTROL List Contacts of a Company]

Récupère une liste de contacts de l’entreprise. La sortie est limitée à 5 000 contacts. Pour répertorier les contacts précédents ou suivants, vous pouvez utiliser le paramètre [!UICONTROL advanced] pour décaler la liste.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Saisissez l’ID de l’entreprise dont vous souhaitez répertorier les contacts. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Nombre maximum de contacts que [!DNL Workfront Fusion] doit renvoyer pendant un cycle d’exécution de scénario. </td> 
  </tr> 
   <tr> 
    <td role="rowheader">ID de contact [décalage de début] </td> 
    <td>Saisissez ou mappez l’identifiant de l’utilisateur que vous souhaitez pour commencer la liste. Par exemple, définir l’ID de contact comme ID du 101e contact permettra au module de répertorier les contacts 101-5100 plutôt que 1-5000. </td> 
   </tr>
 </tbody> 
</table>

#### [!UICONTROL Merge contacts]

Ce module d&#39;action fusionne les contacts

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID 1] </td> 
   <td>Saisissez l’ID de l’un des contacts que vous souhaitez fusionner. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID 2] </td> 
   <td>Saisissez l’ID de l’autre contact que vous souhaitez fusionner.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove a Contact from a List]

Supprime un contact d’une liste de contacts.

>[!NOTE]
>
>Vous ne pouvez pas supprimer manuellement des contacts d’une liste dynamique.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID] </td> 
   <td>Sélectionnez l’ID de la liste à partir de laquelle vous souhaitez supprimer le contact. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contact ID] </td> 
   <td>Saisissez l’ID du contact que vous souhaitez supprimer de la liste. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search for Contacts]

Récupère une liste de contacts à l’aide de la requête.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td>Saisissez la requête.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td>Entrez ou mappez le nombre maximum de contacts que [!DNL Workfront Fusion] doit renvoyer pendant un cycle d’exécution de scénario. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch contacts added to a list]

Ce module de déclenchement lance un scénario lorsqu’un nouveau contact est ajouté à une liste. Cette option est disponible uniquement pour les utilisateurs et utilisatrices disposant d’un compte Marketing payant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td>Saisissez ou mappez l’ID de la liste contenant les contacts que vous souhaitez surveiller.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Properties]</td> 
   <td>Sélectionnez les propriétés à inclure dans la sortie du module.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Offres**

### Transactions

* [[!UICONTROL Get a Deal's CRM Pipeline]](#get-a-deals-crm-pipeline)
* [[!UICONTROL List Deal/Ticket Pipelines]](#list-dealticket-pipelines)

#### [!UICONTROL Get a Deal's CRM Pipeline]

Renvoie le pipeline de la transaction.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pipeline ID] </td> 
   <td>Saisissez ou mappez l’ID du pipeline dont vous souhaitez récupérer les détails. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stage ID] </td> 
   <td>Saisissez ou mappez l’ID de l’étape dont vous souhaitez récupérer les détails. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Deal/Ticket Pipelines]

Renvoie tous les pipelines de transactions et de tickets pour un portail donné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object Type] </td> 
   <td>Indiquez si vous souhaitez répertorier les transactions ou les tickets.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Entreprises**

### Entreprises

#### [!UICONTROL Search for Companies by domain]

Récupère une liste d’entreprises à partir d’une correspondance exacte avec la propriété de domaine.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Domain] </td> 
   <td>Entrez le domaine des entreprises que vous souhaitez rechercher, par exemple <code>[!DNL hubspot].com</code>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Nombre maximum d’entreprises que [!DNL Workfront Fusion] doit renvoyer pendant un cycle d’exécution de scénario. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output properties]</td> 
   <td>Sélectionnez les propriétés à afficher dans la sortie du module. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Engagements**

### Engagements

* [Associer un engagement à un objet CRM](#associate-an-engagement-with-a-crm-object)
* [Créer un engagement](#create-an-engagement)
* [Supprimer un engagement](#delete-an-engagement)
* [Contrats Watch](#watch-engagements)

#### Associer un engagement à un objet CRM

Ce module d’action associe un engagement à un contact, une entreprise ou une affaire.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Sélectionnez le type d’enregistrement CRM auquel vous souhaitez associer un engagement. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Engagement ID]</td> 
  <td>Saisissez ou mappez l'ID de l'engagement que vous souhaitez associer à l'objet.</td> 
   </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record ID]</td> 
  <td>Saisissez ou mappez l'ID de l'enregistrement auquel vous souhaitez associer l'engagement.</td> 
   </tr> 
 </tbody> 
</table>

#### Créer un engagement

Ce module d’action crée un engagement (une note, une tâche ou une activité, par exemple) avec un objet CRM dans HubSpot. Les engagements sont toute interaction avec un contact qui doit être consignée dans le CRM.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Is Active?]</td> 
   <td>Activez cette option si le nouvel engagement sera actif lors de sa création. Un engagement doit être actif pour apparaître dans le journal.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
  <td>Sélectionnez le type d’engagement à créer.
  <ul>
  <li><b>E-mail</b><p></p>Passez à <a href="#email-metadata" class="MCXref xref" >Métadonnées d’e-mail</a>.</p></li>
  <li><b>Appel</b><p>Passez à <a href="#call-metadata" class="MCXref xref" >Métadonnées d’appel</a>.</p></li>
  <li><b>Réunion</b><p>Passez à <a href="#meeting-fields" class="MCXref xref" >Champs de réunion</a>.</p></li>
  <li><b>Tâche</b><p>Passez à <a href="#task-fields" class="MCXref xref" >Champs de la tâche</a>.</p></li>
  <li><b>Note</b><p>Dans le champ Corps , saisissez le texte de la note.</p></li>
  </ul>
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">Date et heure</td> 
   <td>Saisissez ou mappez un horodatage pour l’engagement.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de propriétaire</td> 
   <td>Saisissez ou mappez l'ID de propriétaire de la personne à laquelle l'engagement sera affecté.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">UID</td> 
   <td>Saisissez ou mappez un identifiant pour l'engagement, qui peut être utilisé sur tous les types d'objet.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID du portail</td> 
   <td>Saisissez ou mappez l’identifiant du portail. Cela s’avère utile si votre organisation dispose de plusieurs portails.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Contacts associés</td> 
   <td>Pour chaque contact auquel vous souhaitez associer cet engagement, cliquez sur <b>Ajouter un élément</b> et saisissez l’ID de contact.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sociétés associées</td> 
   <td>Pour chaque société à laquelle vous souhaitez associer cet engagement, cliquez sur <b>Ajouter un élément</b> et saisissez l’ID d’entreprise.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Offres associées</td> 
   <td>Pour chaque affaire à laquelle vous souhaitez associer cet engagement, cliquez sur <b>Ajouter un article</b> et saisissez l’ID d’affaire.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tickets associés</td> 
   <td>Pour chaque ticket auquel vous souhaitez associer cet engagement, cliquez sur <b>Ajouter un élément</b> et saisissez l’ID de ticket.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Pièces jointes</td> 
   <td>Pour chaque pièce jointe à laquelle vous souhaitez associer cet engagement, cliquez sur <b>Ajouter un élément</b> et saisissez l'ID de fichier du fichier à joindre.</td> 
  </tr> 
 </tbody> 
</table>

##### Métadonnées e-mail

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL From > Email]</p> </td> 
   <td> <p>Saisissez ou mappez l’adresse e-mail à partir de laquelle l’e-mail sera envoyé.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL First Name]</td> 
   <td>Saisissez ou mappez le prénom de la personne à partir de laquelle l’e-mail sera envoyé.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Last Name]</td> 
  <td>Saisissez ou mappez le nom de la personne à partir de laquelle l’e-mail sera envoyé.
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">À</td> 
   <td>Pour chaque adresse e-mail à laquelle vous souhaitez envoyer l’e-mail, cliquez sur <b>Ajouter un élément</b> et saisissez ou mappez l’adresse e-mail.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Cc</td> 
   <td>Pour chaque adresse e-mail à laquelle vous souhaitez copier l’e-mail, cliquez sur <b>Ajouter un élément</b> et saisissez ou mappez l’adresse e-mail.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Cci</td> 
   <td>Pour chaque adresse e-mail à laquelle vous souhaitez envoyer l’e-mail en Cci, cliquez sur <b>Ajouter un élément</b> et saisissez ou mappez l’adresse e-mail.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Objet</td> 
   <td>Saisir ou mapper le texte de l’objet de l’e-mail</td> 
  </tr> 
  <tr> 
   <td role="rowheader">HTML</td> 
   <td>Pour envoyer un e-mail au format HTML, saisissez ou mappez le corps de l’e-mail, y compris les balises d’HTML.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Texte</td> 
   <td>Pour envoyer un e-mail au format texte uniquement, saisissez ou mappez le texte du corps de l’e-mail.</td> 
  </tr> 
 </tbody> 
</table>

##### Métadonnées de l’appel

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL To Number]</p> </td> 
   <td> <p>Saisissez ou mappez le numéro de téléphone auquel l’appel sera effectué.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From Number]</td> 
   <td>Saisissez ou mappez le numéro de téléphone à partir duquel l’appel sera effectué.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status]</td> 
  <td>Sélectionnez le statut de l’appel.
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">Corps</td> 
   <td>Saisissez ou mappez les détails ou les notes de l’appel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID externe</td> 
   <td>Ce champ représente l’identifiant interne d’un appel effectué dans HubSpot. Cela ne nécessite aucune action.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Durée</td> 
   <td>Saisir ou mapper la durée de l’appel en millisecondes</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de compte externe</td> 
   <td>Ce champ représente l’identifiant de compte interne d’un appel effectué dans HubSpot. Cela ne nécessite aucune action.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL d’enregistrement</td> 
   <td>Saisissez ou mappez l’URL du fichier d’enregistrement.</td> 
  </tr> 
 </tbody> 
</table>

##### Champs de réunion

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Title]</p> </td> 
   <td> <p>Saisissez ou mappez le titre ou l'objet de la réunion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Saisissez ou mappez le texte de la description ou des détails de la réunion.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Time]</td> 
  <td>Saisissez ou mappez l’heure de début de la réunion sous la forme d’un horodatage UNIX.
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">Heure de fin</td> 
   <td>Saisissez ou mappez l’heure de fin de la réunion sous forme d’horodatage UNIX.</td> 
  </tr> 
 </tbody> 
</table>

##### Champs de tâche

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Subject]</p> </td> 
   <td> <p>Saisissez ou mappez le titre ou l’objet de la tâche.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Saisissez ou mappez le texte de la description ou des détails de la tâche.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Statut</td> 
   <td>Sélectionnez le statut de la tâche.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL For Object Type]</td> 
  <td>Saisissez <code>CONTACT</code> ou <code>COMPANY</code>.
  </td> 
   </tr> 
 </tbody> 
</table>

#### Supprimer un engagement

Ce module d’action supprime un engagement par son identifiant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Saisissez ou mappez l'ID de l'engagement à supprimer.</td> 
  </tr> 
 </tbody> 
</table>

#### Contrats Watch

Ce module de déclenchement lance un scénario lorsqu’un nouvel engagement est créé dans un portail. Ce module renvoie uniquement les enregistrements créés au cours des 30 derniers jours ou les 10 000 enregistrements les plus récemment créés.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Nombre maximum d’entreprises que [!DNL Workfront Fusion] doit renvoyer pendant un cycle d’exécution de scénario. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Since]</td> 
   <td>Saisissez ou mappez la date la plus proche pour laquelle vous souhaitez observer les événements. Utilisez le format <code>MM/DD/YYYY h:mm</code>.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Événements et notifications**

### Événements et notifications

* [Créer/mettre à jour un événement de chronologie](#create--update-a-timeline-event)
* [Liste des types d’événements de chronologie](#list-timeline-event-types)
* [Événements du calendrier de surveillance](#watch-calendar-events)
* [Notifications Watch](#watch-notifications)

#### Créer/mettre à jour un événement de chronologie

Ce module d’action crée ou met à jour un événement de chronologie. Ce module ne peut être utilisé qu’avec une connexion de développeur qui comprend votre identifiant utilisateur, votre clé API HubSpot, votre identifiant client et votre secret client.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application ID]</td> 
   <td>Saisissez ou mappez l’identifiant de l’application à laquelle cet événement appartient.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td>Saisissez ou mappez un ID pour cet événement. Les identifiants d’événement ne sont pas générés par le système.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event Type ID]</td> 
   <td>Saisissez ou mappez l’identifiant du type d’événement de cet événement.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>Saisissez ou mappez l’adresse e-mail du contact pour lequel vous créez l’événement.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object ID]</td> 
   <td>Saisissez ou mappez l’ID du contact pour lequel vous créez l’événement.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp]</td> 
   <td>Saisissez ou mappez la date et l’heure de cet événement.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom data]</td> 
   <td>Pour chaque élément de données personnalisées que vous souhaitez ajouter à cet événement, cliquez sur <b>Ajouter un élément</b> et saisissez le nom et la valeur de l’élément.</td> 
  </tr> 
 </tbody> 
</table>

#### Liste des types d’événements de chronologie

Ce module de recherche renvoie une liste de tous les événements de chronologie pour une application spécifique. Ce module ne peut être utilisé qu’avec une connexion de développeur qui comprend votre identifiant utilisateur, votre clé API HubSpot, votre identifiant client et votre secret client.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application ID]</td> 
   <td>Saisissez ou mappez l’ID de l’application à laquelle ces événements appartiennent. </td> 
  </tr> 
 </tbody> 
</table>

#### Événements du calendrier de surveillance

Ce module de déclenchement démarre un scénario lorsqu’un nouvel événement est ajouté à un calendrier. Il comprend jusqu’à 500 tâches dans l’intervalle entre les dates de début et de fin. Ce module ne peut être utilisé qu’avec une connexion de développeur qui comprend votre identifiant utilisateur, votre clé API HubSpot, votre identifiant client et votre secret client.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Events Type]</td> 
   <td>Indiquez si vous souhaitez regarder les événements sociaux, les événements de contenu ou tous les événements.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal de fichiers que le module doit renvoyer au cours de chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Date]</td> 
   <td>Saisissez ou mappez la date de début.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End Date]</td> 
   <td>Saisissez ou mappez la date de fin.</td> 
  </tr> 
 </tbody> 
</table>

#### Notifications Watch

Ce module de déclenchement lance un scénario lorsqu’une nouvelle notification de modifications est envoyée.  Il comprend jusqu’à 500 tâches dans l’intervalle entre les dates de début et de fin. Ce module ne peut être utilisé qu’avec une connexion de développeur qui comprend votre identifiant utilisateur, votre clé API HubSpot, votre identifiant client et votre secret client. HubSpot ne peut contenir qu’une seule URL webhook par application de développement.

Pour créer un webhook pour ce module, cliquez sur **Ajouter** en regard du champ webhook et renseignez les champs suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application ID]</td> 
   <td>Saisissez l’ID de l’application à utiliser pour ce webhook. Vous trouverez l’identifiant sur votre portail de développement HubSpot.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscriptions]</td> 
   <td> <p>Pour chaque type de notification que vous souhaitez observer, cliquez sur <b>Ajouter un élément</b> et sélectionnez le type d’abonnement.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Force to Remove Old Subscriptions]</td> 
   <td>Activez cette option pour désolidariser ou supprimer les anciens abonnements attachés à ce webhook.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Fichiers**

### Fichiers

* [[!UICONTROL Create a Folder]](#create-a-folder)
* [Supprimer un fichier](#delete-a-file)
* [[!UICONTROL Delete a Folder]](#delete-a-folder)
* [Fichiers de liste](#list-files)
* [[!UICONTROL Move a File]](#move-a-file)
* [Charger un fichier](#upload-a-file)
* [Fichiers de contrôle](#watch-files)

#### [!UICONTROL Create a Folder]

Ce module crée un dossier.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder Name] </td> 
   <td>Saisissez ou mappez un nom pour le nouveau dossier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent Folder ID] </td> 
   <td>Sélectionnez l’ID du dossier parent du dossier que vous créez. </td> 
  </tr> 
 </tbody> 
</table>

#### Supprimer un fichier

Ce module d’action supprime définitivement un fichier et toutes les données et miniatures associées du gestionnaire de fichiers.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Saisissez ou mappez l’identifiant du fichier que vous souhaitez supprimer.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Folder]

Marque un dossier comme supprimé.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Saisissez ou mappez l’identifiant du dossier que vous souhaitez supprimer.</td> 
  </tr> 
 </tbody> 
</table>

#### Fichiers de liste

Ce module de recherche renvoie une liste des fichiers stockés dans le gestionnaire de fichiers.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal de fichiers que le module doit renvoyer au cours de chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>Saisissez ou mappez l’identifiant du dossier contenant les fichiers à répertorier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Pour inclure uniquement les fichiers dont le nom de fichier contient des caractères spécifiques, saisissez ou mappez les caractères à inclure dans le nom de fichier.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a File]

Déplace un fichier vers un autre dossier.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID] </td> 
   <td>Saisissez ou mappez l’ID du fichier à déplacer. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td>Sélectionnez l’ID du dossier dans lequel vous souhaitez déplacer le fichier. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Saisissez un nom pour le fichier déplacé.</td> 
  </tr> 
 </tbody> 
</table>

#### Charger un fichier

Ce module d&#39;action charge un fichier dans le gestionnaire de fichiers.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Access type] </td> 
   <td>Choisissez si vous souhaitez que le fichier soit privé, public mais non indexable, ou public et indexable. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td>Sélectionnez l’identifiant du dossier dans lequel vous souhaitez charger le fichier. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Overwrite]</td> 
   <td>Activez cette option pour remplacer le fichier s’il existe déjà dans le dossier.</td> 
  </tr> 
 </tbody> 
</table>

### Fichiers Watch

Ce module de déclenchement démarre un scénario lorsqu’un nouveau fichier est enregistré dans le gestionnaire de fichiers.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal de fichiers que le module doit renvoyer au cours de chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>Saisissez ou mappez l’identifiant du dossier contenant les fichiers à surveiller.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Pour inclure uniquement les fichiers dont le nom de fichier contient des caractères spécifiques, saisissez ou mappez les caractères à inclure dans le nom de fichier.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Tâches**

### Tâches

* [Créer une tâche de calendrier](#create-a-calendar-task)
* [Supprimer une tâche de calendrier](#create-a-calendar-task)
* [Surveiller les événements de tâche](#watch-task-events)

#### Créer une tâche de calendrier

Ce module d&#39;action crée une nouvelle tâche pour un calendrier. La connexion utilisée dans ce module doit utiliser les informations d’identification d’un utilisateur disposant d’un compte marketing payant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Saisissez ou mappez un nom pour la nouvelle tâche de calendrier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Saisissez ou mappez une description pour la nouvelle tâche de calendrier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Owner ID]</td> 
   <td>Saisissez ou mappez l’ID du propriétaire de l’utilisateur affecté à cette tâche.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event Date]</td> 
   <td>Saisissez ou mappez la date de cette tâche.<p>Pour obtenir la liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coercition de type dans [!DNL Adobe Workfront Fusion]</a>.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Category]</td> 
   <td>Sélectionnez le type d’événement.<ul><li><b>Article de blog</b><p>Saisissez l’ID du groupe de contenu. Il s’agit de l’identifiant de la page de blog.</p></li><li><b>E-mail</b><p>Saisissez ou mappez le chemin d’accès au modèle d’e-mail que vous souhaitez utiliser.</li><li><b>Page de destination</b><p>Saisissez ou mappez le chemin d’accès au modèle de page de destination que vous souhaitez utiliser.</li><li><b>Valeur personnalisée</b></li><ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td>Indiquez si l’événement a le statut « À faire » ou « Terminé ».</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campaign GUID]</td> 
   <td>Saisissez ou mappez l’identifiant HubSpot interne de la campagne dont fait partie cet événement.</td> 
  </tr> 
 </tbody> 
</table>

#### Supprimer une tâche de calendrier

Ce module d&#39;action supprime une tâche de calendrier. La connexion utilisée dans ce module doit utiliser les informations d’identification d’un utilisateur disposant d’un compte marketing payant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Saisissez ou mappez l’identifiant de la tâche que vous souhaitez supprimer.</td> 
  </tr> 
 </tbody> 
</table>

#### Surveiller les événements de tâche

Ce module de déclenchement démarre un scénario lorsqu’un nouvel événement de tâche figure dans un calendrier. La connexion utilisée dans ce module doit utiliser les informations d’identification d’un utilisateur disposant d’un compte marketing payant. Le module renvoie jusqu’à 500 événements.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal de fichiers que le module doit renvoyer au cours de chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Date]</td> 
   <td>Saisissez ou mappez la date la plus proche pour laquelle vous souhaitez observer les événements. Utilisez le format <code>MM/DD/YYYY h:mm</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End Date]</td> 
   <td>Saisissez ou mappez la date la plus récente pour laquelle vous souhaitez observer les événements. Utilisez le format <code>MM/DD/YYYY h:mm</code>.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Utilisateurs ou utilisatrices**

### Utilisateurs

* [Obtenir un propriétaire](#get-an-owner)
* [Propriétaires de liste](#list-owners)

#### Obtenir un propriétaire

Ce module d’action renvoie les détails d’un propriétaire.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Owner ID]</td> 
   <td> <p>Saisissez ou mappez l’ID du propriétaire pour lequel vous souhaitez renvoyer des détails.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Propriétaires de liste

Ce module de recherche renvoie une liste de tous les propriétaires d’un compte HubSpot.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Billets**

### Tickets

<!--* [Create a Ticket]-->
* [Supprimer un ticket](#delete-a-ticket)
  <!--* [Create a Ticket]-->
  <!--* [Create a Ticket]-->
  <!--* [Create a Ticket]-->
  <!--* [Create a Ticket]-->

<!-- Create a Ticket Need to find a working connection-->

#### [!UICONTROL Delete a Ticket]

Supprime un ticket existant par son ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Saisissez l’ID du ticket que vous souhaitez supprimer. </td> 
  </tr> 
 </tbody> 
</table>

<!-- Get a Ticket  Need to find a working connection-->

<!-- List Tickets  Need to find a working connection-->

&lt;!— Mettre à jour un ticket Besoin de trouver une connexion active—>

<!-- Watch Tickets Need to find a working connection-->

+++

+++**Forms**

### Formulaires

* [Obtenir un fichier téléchargé via le formulaire](#get-a-file-uploaded-via-form)
* [Liste des Forms](#list-forms)
  <!--* [Submit Data to a Form]-->
  <!--* [Watch Submissions for a Form]-->

#### Obtenir un fichier téléchargé via le formulaire

Ce module d’action renvoie un fichier qui a été chargé par le biais d’un formulaire.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File URL]</td> 
   <td>Saisissez ou mappez l’URL du fichier que vous souhaitez récupérer. Elle se trouve dans les métadonnées du formulaire.</td> 
  </tr> 
 </tbody> 
</table>

#### Forms de liste

Ce module d’action renvoie tous les formulaires qui ont été créés dans le compte associé à la connexion utilisée pour ce module.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Saisissez ou mappez le nombre maximal de formulaires que le module renverra au cours d’un cycle d’exécution.</td> 
  </tr> 
 </tbody> 
</table>

<!--#### Submit Data to a Form Need to find a working connection-->



&lt;!—### Regarder les envois pour un formulaire—Besoin de trouver une connexion fonctionnelle>—>

+++

+++**Médias sociaux (diffusion)**

### Réseaux Sociaux (Diffusion)

* [Annuler un message de diffusion](#cancel-a-broadcast-message)
* [Créer un message diffusé](#create-a-broadcast-message)
* [Regarder les messages diffusés](#watch-broadcast-messages)

#### Annuler un message de diffusion

Ce module d’action annule une diffusion planifiée, telle qu’un tweet ou une publication Facebook.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Broadcast ID]</td> 
   <td>Saisissez ou mappez l’identifiant de la diffusion que vous souhaitez annuler.</td> 
  </tr> 
 </tbody> 
</table>

#### Créer un message diffusé

Ce module d’action crée et publie immédiatement un message sur le canal de réseau social spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel ID]</td> 
   <td>Saisissez ou mappez l’identifiant du canal que vous souhaitez utiliser pour cette diffusion.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title]</td> 
   <td>Saisissez ou mappez un titre pour cette diffusion.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Saisissez ou mappez le texte de la diffusion.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Photo URL]</td> 
   <td>Saisissez ou mappez l’URL d’une photo que vous souhaitez inclure dans la diffusion.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Thumbnail URL]</td> 
   <td>Saisissez ou mappez l’URL d’une miniature que vous souhaitez utiliser pour cette diffusion.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Trigger at]</td> 
   <td>Saisissez ou mappez la date et l’heure auxquelles vous souhaitez que la diffusion soit envoyée. Si ce champ est laissé vide, la diffusion est envoyée immédiatement.<p>Pour obtenir la liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coercition de type dans [!DNL Adobe Workfront Fusion]</a>.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Regarder les messages diffusés

Ce module de déclenchement démarre un scénario lorsqu’un message est publié de HubSpot sur le canal de médias sociaux spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Saisissez ou mappez le nombre maximal d’éléments que le module renverra dans un cycle d’exécution.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by Status]</td> 
   <td>Pour démarrer le scénario uniquement lorsque le message se trouve dans un statut spécifique, sélectionnez le statut.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by Channel]</td> 
   <td>Pour démarrer le scénario uniquement lorsque le message se trouve sur un canal spécifique, sélectionnez le canal.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Broadcast ID]</td> 
   <td>Pour démarrer le scénario uniquement lorsque le message se trouve à une date spécifique ou après, saisissez ou mappez la date au format <code>MM/DD/YYYY</code>.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**Publications du blog**

### Publications du blog

<!--* [Create a Blog Post]-->
* [Supprimer un article de blog](#delete-a-blog-post)
  <!--* [List Blog Posts]-->
* [Publish/Dépublication d&#39;un article de blog](#publish--unpublish-a-blog-post)
  <!--* [Watch Blog Posts]-->

<!--
#### Create a Blog Post May need connection
-->


#### Supprimer une publication de blog

Ce module d&#39;action supprime une seule publication de blog.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Saisissez ou mappez l'ID de l'article de blog que vous voulez supprimer.</td> 
  </tr> 
 </tbody> 
</table>

<!--#### List Blog Posts May need connection

This search module retrieves posts from a HubSpot blog.-->

#### Publish / Dépublier un article de blog

Ce module d&#39;action planifie ou annule la publication d&#39;un article de blog.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Saisissez ou mappez l'ID de l'article de blog que vous voulez programmer ou annuler.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td>Choisissez de planifier l'article de blog ou d'annuler un article de blog précédemment planifié.</td> 
  </tr> 
 </tbody> 
</table>

<!--#### Watch Blog PostsMay need connection-->

+++

<!--+++**Workflows**>

<!--### Workflows May need connection

#### Add a Contact to a Workflow


#### Remove a Contact from a Workflow

-->

<!--+++-->

+++**Abonnements**

### Abonnements

* [Mettre à jour l’abonnement par e-mail](#update-email-subscription)
* [Suivre la chronologie des abonnements pour un portail](#watch-subscriptions-timeline-for-a-portal)

#### Mettre à jour l’abonnement par e-mail

Ce module d’action met à jour un abonnement par e-mail dans HubSpot.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>Saisissez ou mappez l’adresse e-mail de l’abonnement que vous souhaitez mettre à jour.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Statuses]</td> 
   <td>Pour chaque statut pour lequel vous souhaitez mettre à jour l’abonnement, cliquez sur <b>Ajouter un élément</b> et saisissez l’identifiant du statut et indiquez si l’adresse e-mail sera abonnée à ce statut.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Portal Subscription Legal Status]</td> 
   <td>Pour enregistrer la base juridique de cet abonnement au RGPD, sélectionnez le statut juridique de cet abonnement.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Portal Subscription Legal Basis Explanation]</td> 
   <td>Pour ajouter une note concernant la base juridique de cet abonnement au RGPD, saisissez ou mappez le texte de la note.</td> 
  </tr> 
 </tbody> 
</table>

#### Suivre la chronologie des abonnements pour un portail

Ce module de déclenchement lance un scénario lorsqu’un nouvel abonnement à la chronologie des e-mails est ajouté au portail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Saisissez ou mappez le nombre maximal d’éléments que le module renverra dans un cycle d’exécution.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Timestamp]</td> 
   <td>Pour renvoyer les résultats à partir d’une date spécifique ou après, saisissez la date au format . <code>MM/DD/YYYY.</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End Timestamp]</td> 
   <td>Pour renvoyer les résultats à partir d’une date spécifique ou avant, saisissez la date au format . <code>MM/DD/YYYY.</code></td> 
  </tr> 
 </tbody> 
</table>

+++

<!--+++**Associations**-->

<!--### Associations-->

<!--#### Associate CRM Objects  May need connection

This action module associates two CRM objects.-->

<!--#### Associate Multiple CRM Objects  May need connection-->



<!--#### Delete an Association May need connection-->



<!--#### Delete Multiple Associations between CRM Objects May need connection-->



<!--#### List Associations for a CRM Object May need connection-->

<!--+++-->

+++**Autre**

### Autre

#### [!UICONTROL Make an API Call]

Permet d’effectuer un appel API personnalisé.

>[!NOTE]
>
>Les points d’entrée suivants ont été abandonnés dans l’API HubSpot le 31 août 2023 et ne peuvent plus être utilisés dans les modules Fusion.
>
>* Répertorier les événements de contenu
>* Répertorier les événements sociaux
>* Répertorier les événements de tâche du calendrier
>* Répertorier tous les événements du calendrier
>* Créer une tâche de calendrier
>* Obtenir la tâche du calendrier par ID
>* Mettre à jour la tâche du calendrier
>* Supprimer une tâche de calendrier

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL HubSpot CRM] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Saisissez un chemin d’accès relatif à https://api.hubapi.com/. Par exemple, /contacts/v1/lists/all/contacts/all.</p> <p>Pour obtenir la liste des points d’entrée disponibles, voir la documentation de l’API <a href="https://legacydocs.hubspot.com/docs/overview">[!DNL HubSpot]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Sélectionnez la méthode HTTP à utiliser :</p> <p>[!UICONTROL GET]</p> <p>pour récupérer les informations d’une entrée.</p> <p>[!UICONTROL POST]</p> <p>pour créer une nouvelle entrée.</p> <p>[!UICONTROL PUT]</p> <p>pour mettre à jour/remplacer une entrée existante.</p> <p>[!UICONTROL PATCH]</p> <p>pour effectuer une mise à jour partielle des entrées.</p> <p>[!UICONTROL DELETE]</p> <p>pour supprimer une entrée.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p> Saisissez les en-têtes de requête de votre choix. Vous n’avez pas à ajouter d’en-têtes d’autorisation ; nous l’avons déjà fait pour vous.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Saisissez la chaîne de requête.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard. Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre fichier JSON, placez les guillemets en dehors de l’instruction conditionnelle.<img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"></p> </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Exemple :** l’appel API suivant renvoie tous les contacts de votre compte [!DNL HubSpot] :
>
>**URL** : `/contacts/v1/lists/all/contacts/all`
>
>**Méthode** : `GET`
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/hubspot-api-config.png)
>
>Les correspondances de la recherche se trouvent dans la sortie du module sous [!UICONTROL Bundle] > [!UICONTROL Body] > [!UICONTROL contacts].
>
>Dans notre exemple, 3 contacts ont été renvoyés :
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/hubspot-api-output.png)

+++

## Créer une nouvelle application

1. Connectez-vous à votre compte de développement [!DNL HubSpot].
1. Sélectionnez l’option **[!UICONTROL Create an App]** .
1. Saisissez le Nom de l’application et [!UICONTROL Save] la boîte de dialogue.
1. Sélectionnez les portées dont vous aurez besoin pour votre webhook.

   Par exemple, ajoutez des portées de contacts pour déclencher le module lorsqu’un nouveau contact est créé ou supprimé.

   Le [!UICONTROL contacts scope] est tout ce dont vous avez besoin pour recevoir des contacts, des offres et des webhooks d&#39;événement d&#39;entreprise.

   >[!IMPORTANT]
   >
   >Ne renseignez pas le champ [!UICONTROL Redirect URL] .
