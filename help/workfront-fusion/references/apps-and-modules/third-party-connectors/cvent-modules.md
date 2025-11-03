---
title: Modules Cvent
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent Cvent et les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: b7e16180-1db8-4aff-bb7b-69ca98194b00
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1129'
ht-degree: 66%

---

# Modules [!DNL Cvent]

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent [!DNL Cvent] et les connecter à plusieurs applications et services tiers.

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

Pour utiliser les modules [!DNL Cvent], vous devez disposer d’un compte [!DNL Cvent].

## Informations sur l’API Cent

Le connecteur Cvent utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Version de l’API</td> 
   <td> V200611.ASMX </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.7.14</td> 
  </tr>
 </tbody> 
 </table>

## Connexion de [!DNL Cvent] à Adobe Workfront Fusion {#connect-cvent-to-adobe-workfront-fusion}

>[!NOTE]
>
>Les modules [!DNL Cvent] fonctionnent par l’intermédiaire d’une API [!UICONTROL SOAP]. Pour créer une connexion à [!DNL Cvent], vous devez vous assurer des points suivants :
>
>* Vous avez un accès [!UICONTROL SOAP] à l’API [!DNL Cvent].
>* Les adresses IP Workfront Fusion ont été ajoutées à la place sur la liste autorisée de données de votre organisation.
>
>  Pour obtenir la liste des adresses IP de Workfront Fusion, voir [Configuration des adresses IP pour Fusion dans la place sur la liste autorisée de données de votre entreprise](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md)


Vous pouvez créer une connexion à votre compte [!DNL Cvent] directement à partir d’un module [!DNL Cvent].

1. Dans n’importe quel module [!DNL Cvent], cliquez sur **[!UICONTROL Ajouter]** à côté du champ [!UICONTROL Connexion].
1. Sélectionnez la zone géographique à laquelle vous souhaitez vous connecter.

   * [!UICONTROL Amérique du Nord]
   * [!UICONTROL Europe]
   * [!UICONTROL Sandbox]

1. Cliquez sur **[!UICONTROL Continuer]** pour créer la connexion et retourner au module.

## Modules [!DNL Cvent] et leurs champs

Lorsque vous configurez les modules [!DNL Cvent], Workfront Fusion affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Cvent] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Actions](#actions)
* [Recherches](#searches)

### Actions

* [[!UICONTROL Personnaliser un appel API]](#create-meeting-request)
* [[!UICONTROL Lire un enregistrement]](#read-a-record)
* [[!UICONTROL Enregistrer une personne invitée]](#register-invitee)
* [[!UICONTROL Ajouter une personne invitée]](#add-invitee)
* [[!UICONTROL Supprimer un contact]](#delete-contact)
* [[!UICONTROL Mettre à jour un contact]](#update-contact)
* [[!UICONTROL Créer une demande de réunion]](#create-meeting-request)

#### [!UICONTROL Personnaliser un appel API]

Ce module d’action vous permet d’effectuer un appel personnalisé et authentifié à l’API [!DNL Cvent]. Cela vous permet de créer une automatisation du flux de données qui ne peut pas être réalisée par les autres modules [!DNL Cvent].

Lorsque vous configurez ce module, les champs suivants s’affichent.

Le module renvoie le code d’état, ainsi que les en-têtes et le corps de l’appel API.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Cvent] à Workfront Fusion, voir <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Connexion de [!DNL Cvent] à Adobe Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Opération</td> 
   td&gt; <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Corps (XML)</td> 
   <td> <p>Saisissez ou mappez le corps de l’appel API. Il ne doit comprendre que le XML. Le module inclura automatiquement les en-têtes d’authentification. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Lire un enregistrement]

Ce module d’action permet de lire les informations relatives à un enregistrement spécifique.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Cvent] à Workfront Fusion, voir <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Connexion de [!DNL Cvent] à Adobe Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Record type]</p> </td> 
   <td>Sélectionnez le type d’élément de l’enregistrement que vous souhaitez lire.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contact] / [!UICONTROL Event] / [!UICONTROL Invitee ID]</td> 
   <td> <p>Saisissez ou mappez l’identifiant de l’élément que vous souhaitez lire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Sélectionnez les champs que vous souhaitez inclure dans la sortie du module. Les champs sont disponibles en fonction du type d’élément que vous avez sélectionné.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Enregistrer une personne invitée]

Ce module d’action enregistre une personne invitée à un événement.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Cvent] à Workfront Fusion, voir <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Connexion de [!DNL Cvent] à Adobe Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Identifiant de personne invitée</p> </td> 
   <td> <p>Saisissez ou mappez l’identifiant de la personne invitée que vous souhaitez inscrire à un événement.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Identifiant d’événement</td> 
   <td> <p>Saisissez ou mappez l’identifiant de l’événement auquel vous souhaitez inscrire la personne invitée.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ajouter une personne invitée]

Ce module d’action invite un contact à un événement.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Cvent] à Workfront Fusion, voir <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Connexion de [!DNL Cvent] à Adobe Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Contact ID]</p> </td> 
   <td> <p>Saisissez ou mappez l’identifiant du contact que vous souhaitez ajouter à un événement.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td> <p>Saisissez ou mappez l’identifiant de l’événement auquel vous souhaitez ajouter le contact.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Supprimer un contact]

Ce module d’action supprime un seul contact dans Cvent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Cvent] à Workfront Fusion, voir <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Connexion de [!DNL Cvent] à Adobe Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contact ID]</td> 
   <td> <p>Saisissez ou mappez l’identifiant du contact que vous souhaitez supprimer.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mettre à jour un contact]

Ce module d’action met à jour un contact existant en utilisant son identifiant.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Cvent] à Workfront Fusion, voir <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Connexion de [!DNL Cvent] à Adobe Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Contact ID]</p> </td> 
   <td> <p>Saisissez ou mappez l’identifiant du contact que vous souhaitez mettre à jour.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>Sélectionnez les champs pour lesquels vous souhaitez saisir des informations, puis remplissez les valeurs souhaitées pour ces champs.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom fields]</td> 
   <td> <p>Sélectionnez les champs pour lesquels vous souhaitez saisir des informations, puis remplissez les valeurs souhaitées pour ces champs.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Créer une demande de réunion]

Ce module d’action ajoute une demande de réunion à votre compte.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Cvent] à Workfront Fusion, voir <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Connexion de [!DNL Cvent] à Adobe Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Form ID]</p> </td> 
   <td> <p>Saisissez ou mappez l’identifiant du formulaire que vous souhaitez utiliser pour créer la demande de réunion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Meeting Request Fields]</td> 
   <td> <p>Sélectionnez les champs de la demande de réunion pour lesquels vous souhaitez saisir des informations, puis indiquez les valeurs souhaitées pour ces champs.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event Request Fields]</td> 
   <td> <p>Sélectionnez les champs de demande d’événement pour lesquels vous souhaitez saisir des informations, puis renseignez les valeurs souhaitées pour ces champs.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL RFP Request Fields]</td> 
   <td> <p>Sélectionnez les champs de l’appel d’offres pour lesquels vous souhaitez saisir des informations, puis indiquez les valeurs souhaitées pour ces champs.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Recherches

#### [!UICONTROL Répertorier des enregistrements]

Ce module de recherche permet d’obtenir des informations sur tous les enregistrements d’un type spécifique.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Cvent] à Workfront Fusion, voir <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">Connexion de [!DNL Cvent] à Adobe Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Record type]</p> </td> 
   <td> <p>Sélectionnez le type d’enregistrement que vous souhaitez répertorier.</p> 
    <ul> 
     <li> <p>Tous les événements de votre compte [!DNL Cvent]</p> </li> 
     <li> <p>Toutes les sessions d’un événement</p> </li> 
     <li> <p>Toutes les personnes invitées à un événement</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td> <p>Si vous répertoriez des personnes invitées ou des sessions, saisissez ou mappez l’identifiant de l’événement auquel ces personnes invitées ou sessions sont associées.</p> </td> 
  </tr> 
 </tbody> 
</table>
