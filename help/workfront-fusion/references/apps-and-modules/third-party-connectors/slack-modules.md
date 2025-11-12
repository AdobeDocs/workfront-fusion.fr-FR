---
title: Modules Slack (hérités)
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent Slack et les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: c9c68a4c-f592-42d1-b15f-a525b9aa3944
source-git-commit: c5c1f632ce5cc3b4f357118e7bdb8ec852bd91fb
workflow-type: tm+mt
source-wordcount: '2039'
ht-degree: 59%

---

# Modules [!DNL Slack] (hérités)

<!--

>[!IMPORTANT]
>
>This article describes modules available in the legacy Slack connector, which is no longer available. This article will be removed in the near future. 
>
>For information on the new Slack connector, released on November 14, 2025, see [[!DNL Slack] modules (Legacy)](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/slack-modules.md).

-->

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent [!DNL Slack] et les connecter à plusieurs applications et services tiers.

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

Pour utiliser les modules [!DNL Slack], vous devez disposer d’un compte [!DNL Slack].

## Informations sur l’API Slack

Le connecteur Slack utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td>{{ifempty(parameters.domain, 'https://slack.com/api/')}}</td> 
  </tr>
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v4.0.15</td> 
  </tr>
 </tbody> 
 </table>

## Modules [!DNL Slack] et leurs champs

Lorsque vous configurez les modules [!DNL Slack], Workfront Fusion affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Slack] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Messages](#messages)
* [Conversations](#channels)
* [Autre](#other)

### Messages

* [Création d’un message](#create-a-message)
* [Supprimer un message](#delete-a-message)
* [Obtenir un message de canal privé](#get-a-private-channel-message)
* [Obtenir un message de canal public](#get-a-public-channel-message)
* [Mettre à jour un message](#update-a-message)
* [Regarder les messages de canal privé](#watch-private-channel-messages)
* [Regarder les messages de canal public](#watch-public-channel-messages)

### [!UICONTROL Créer un message]

Ce module d’action crée un message.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter a channel ID or name]</p> </td> 
   <td> <p>Choisissez le mode de sélection du canal dans lequel vous souhaitez créer un message.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Dans le champ <strong>[!UICONTROL Channel ID or name]</strong>, saisissez ou mappez l’identifiant ou le nom du canal sur lequel vous souhaitez publier le message.</p> <p>Note : l’identifiant du canal peut être récupéré à l’aide du module [!UICONTROL List Channels].</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le type de canal, puis sélectionnez le canal.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Text]</p> </td> 
   <td> <p>Saisissez le texte du message que vous souhaitez créer.</p> <p>Note : pour plus d’informations sur le formatage du texte, voir <a href="https://api.slack.com/reference/surfaces/formatting">Formatage du texte pour les surfaces d’application</a> dans la documentation [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL As user]</td> 
   <td>Activez cette option pour publier le message en tant qu’utilisateur propriétaire des informations d’identification utilisées par la connexion pour ce module.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Thread message ID (time stamp)]</td> 
   <td>Si le nouveau message est une réponse, saisissez la date et heure du message auquel vous souhaitez répondre. Ne saisissez pas la date et l’heure d’un message qui est déjà une réponse.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reply broadcast]</td> 
   <td> <p>Sélectionner <strong>[!UICONTROL Yes]</strong> si les deux conditions suivantes s’appliquent :</p> 
    <ul> 
     <li> <p>Le nouveau message est une réponse à un autre message.</p> </li> 
     <li> <p>Vous souhaitez que le nouveau message soit visible par toutes les personnes du canal.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Attachments]</td> 
   <td>Pour chaque élément que vous souhaitez joindre au message, cliquez sur <b>Ajouter un élément</b> et renseignez les détails de l’élément.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Icon emoji]</td> 
   <td>Saisissez ou mappez l’émoticône à utiliser comme icône pour ce message, au format <code>:icon-name:</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Icon URL]</td> 
   <td>Saisissez ou mappez l’URL de l’image à utiliser comme icône pour ce message. </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Link names]</p> </td> 
   <td> <p>Activez cette option pour permettre aux noms et aux canaux d’utiliser le format <code>@username</code> ou <code>#channel</code>. </p> <p>Pour plus d’informations, voir <a href="https://api.slack.com/docs/formatting">Formatage du texte pour les surfaces d’application</a> dans la documentation [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Parse message text]</p> </td> 
   <td> <p>Activez cette option pour autoriser l’analyse automatique. </p> <p>Pour plus d’informations, voir <a href="https://api.slack.com/docs/formatting">Formatage du texte pour les surfaces d’application</a> dans la documentation [!DNL Slack].</p> <p>Note : si vous avez utilisé les options [!UICONTROL Link names] ou [!UICONTROL Parse message text] dans le message d’origine, vous devez les spécifier également lors de l’exécution du module [!UICONTROL Update a Message].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Use markdown]</p> </td> 
   <td> <p>Activez cette option pour autoriser [!DNL Slack] à utiliser Markdown dans le texte.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Unfurl primarily text-based content]</p> </td> 
   <td> <p>Activez cette option pour permettre le déploiement de contenu principalement textuel. </p> <p>Pour plus d’informations sur le déploiement dans [!DNL Slack], voir <a href="https://api.slack.com/reference/messaging/link-unfurling">Déploiement de liens dans les messages</a> dans la documentation [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Unfurl media content]</p> </td> 
   <td> <p>Activez cette option pour permettre le déploiement du contenu multimédia. </p> <p>Pour plus d’informations sur le déploiement dans [!DNL Slack], voir <a href="https://api.slack.com/reference/messaging/link-unfurling">Déploiement de liens dans les messages</a> dans la documentation [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User name]</td> 
   <td>Spécifiez le nom d’utilisateur utilisé pour publier le message. Si aucun nom d’utilisateur n’est spécifié, le nom « Robot » est utilisé.</td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Supprimer un message]

Ce module d’action supprime un message spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel ID]</p> </td> 
   <td> <p>Saisissez ou mappez l’identifiant du canal.</p> <p>Note : l’identifiant du canal peut être récupéré à l’aide du module [!UICONTROL List Channels].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID]</td> 
   <td> <p> Saisissez ou mappez l’horodatage du message que vous souhaitez supprimer.</p> <p>Remarque : l’horodatage peut être récupéré à l’aide d’un autre module, tel que le module Observer les messages de canal privé .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL As user]</td> 
   <td> <p> Activez cette option pour supprimer le message en tant qu’utilisateur avec les informations d’identification utilisées dans la connexion.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obtenir un message d’un canal privé]

Ce module d’action récupère les détails d’un message à partir d’un canal sélectionné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel ID]</p> </td> 
   <td> <p>Saisissez (mappez) l’identifiant du canal.</p> <p>Note : l’identifiant du canal peut être récupéré à l’aide du module [!UICONTROL List Channels].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Message ID (Time stamp)]</p> </td> 
   <td> <p> Saisissez ou mappez l’horodatage du message pour lequel vous souhaitez récupérer des informations.</p> <p>Remarque : l'horodatage peut être récupéré à l'aide d'un autre module, tel que le module [!UICONTROL Watch Private Channel Messages].</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obtenir un message de canal public]**

Ce module d’action renvoie un message avec un identifiant donné à partir d’un canal public spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel ID]</p> </td> 
   <td> <p>Saisissez ou mappez l’identifiant du canal.</p> <p>Note : l’identifiant du canal peut être récupéré à l’aide du module [!UICONTROL List Channels].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID (Time stamp)]</td> 
   <td> <p> Saisissez ou mappez l’horodatage du message pour lequel vous souhaitez récupérer des informations.</p> <p>Remarque : l'horodatage peut être récupéré à l'aide d'un autre module, tel que le module [!UICONTROL Watch Public Channel Messages].</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mettre à jour un message]

Ce module d’action permet de modifier un message existant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter a channel ID or name]</p> </td> 
   <td> <p>Choose how you want to select the message you want to .</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>In the <strong>[!UICONTROL Channel ID or name]</strong> field, enter or map the Channel ID or of the channel that contains the message, then enter the <strong>[!UICONTROL Time Stamp (Message ID)]</strong> of the message.</p> <p>Note: The Channel ID can be retrieved using the [!UICONTROL List Channels] module.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Select the type of channel, then select the channel, then select the message.</p> </li> 
    </ul> </td> 
  </tr> -->
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel ID]</p> </td> 
   <td> <p>Saisissez ou mappez l’identifiant du canal contenant le message à mettre à jour.</p> <p>Note : l’identifiant du canal peut être récupéré à l’aide du module [!UICONTROL List Channels].</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Message ID (Time stamp)]</p> </td> 
   <td> <p> Saisissez ou mappez l’horodatage du message pour lequel vous souhaitez récupérer des informations.</p> <p>Remarque : l'horodatage peut être récupéré à l'aide d'un autre module, tel que le module [!UICONTROL Watch Public Channel Messages].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Text]</p> </td> 
   <td> <p>Saisissez le nouveau contenu texte du message que vous souhaitez mettre à jour.</p> <p>Pour plus d’informations, voir <a href="https://api.slack.com/docs/formatting">Formatage du texte pour les surfaces d’application</a> dans la documentation [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL As user]</td> 
   <td>Activez cette option pour mettre à jour le message en tant qu’utilisateur propriétaire des informations d’identification utilisées par la connexion pour ce module.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Attachments]</td> 
   <td>Pour chaque élément que vous souhaitez joindre au message, cliquez sur <b>Ajouter un élément</b> et renseignez les détails de l’élément.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Link names]</p> </td> 
   <td> <p>Activez cette option pour permettre aux noms et aux canaux d’utiliser le format <code>@username</code> ou <code>#channel</code>. </p> <p>Pour plus d’informations, voir <a href="https://api.slack.com/docs/formatting">Formatage du texte pour les surfaces d’application</a> dans la documentation [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Parse message text]</p> </td> 
   <td> <p>Activez cette option pour autoriser l’analyse automatique. </p> <p> Pour plus d’informations, voir la section <a href="https://api.slack.com/docs/formatting">Mettre en forme du texte pour les surfaces d’application</a> dans la documentation [!DNL Slack].</p> <p>Note : si vous avez utilisé les options [!UICONTROL Link names] ou [!UICONTROL Parse message text] dans le message d’origine, vous devez également les spécifier lors de l’exécution du module Mettre à jour un message.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Surveiller les messages des canaux privés]

Ce module de déclenchement lance le scénario lorsqu’un nouveau message est ajouté à un canal privé (groupe).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel] </td> 
   <td> <p>Sélectionnez le canal privé dont vous souhaitez surveiller les nouveaux messages.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Définissez le nombre maximal de messages que Workfront Fusion renverra au cours d’un cycle d’exécution.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Surveiller les messages des canaux publics]

Ce module de déclenchement lance le scénario lorsqu’un nouveau message est ajouté à un canal public.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel] </td> 
   <td> <p>Sélectionnez le canal public dont vous souhaitez surveiller les nouveaux messages.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Définissez le nombre maximal de messages que Workfront Fusion renverra au cours d’un cycle d’exécution.</p> </td> 
  </tr> 
 </tbody> 
</table>



### Conversations

* [Obtenir un canal](#get-a-channel)
* [Liste des canaux](#list-channels)
* [Liste des membres dans le canal](#list-members-in-channel)

#### [!UICONTROL Obtenir un canal]

Ce module d’action renvoie des informations concernant un canal d’espace de travail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel ID]</p> </td> 
   <td> <p>Saisissez ou mappez l’identifiant du canal dont vous souhaitez récupérer les informations.</p> <p>Note : l’identifiant du canal peut être récupéré à l’aide du module [!UICONTROL List Channels].</p> </td> 
  </tr> 
 </tbody>

#### [!UICONTROL Répertorier les canaux]

Ce module de recherche renvoie une liste de tous les canaux d’un espace de travail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Exclude archived]</p> </td> 
   <td> <p>Sélectionnez [!UICONTROL Yes] pour exclure les canaux archivés dans les résultats.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type] </td> 
   <td> <p>Sélectionnez le ou les types de canaux à récupérer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Définissez le nombre maximal de canaux que Workfront Fusion renverra au cours d’un cycle d’exécution.</p> </td> 
  </tr> 
 </tbody> 
</table>
</table>

#### [!UICONTROL Répertorier les personnes membres du canal]

Ce module de recherche renvoie une liste d’utilisateurs et d’utilisatrices dans le canal sélectionné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
<tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter a channel ID or name]</p> </td> 
   <td> <p>Choisissez le mode de sélection du message que vous souhaitez modifier.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Dans le champ <strong>[!UICONTROL Channel ID or name]</strong>, saisissez ou mappez l’identifiant du canal ou du canal dont vous souhaitez répertorier les utilisateurs.</p> <p>Note : l’identifiant du canal peut être récupéré à l’aide du module [!UICONTROL List Channels].</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le type de canal, puis sélectionnez le canal.</p> </li> 
    </ul> </td> 
  </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Définissez le nombre maximal de membres que Workfront Fusion renverra au cours d’un cycle d’exécution.</p> </td> 
  </tr> 
 </tbody> 
</table>


### Autre

#### [!UICONTROL Réaliser un appel API]

Ce module d’action permet d’effectuer un appel authentifié personnalisé vers l’API [!DNL Slack]. Ainsi, vous pouvez créer une automatisation du flux de données qui ne peut pas être réalisée par les autres modules [!DNL Slack].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Saisissez un chemin relatif vers <code>https://slack.com/api/</code>. Exemple : <code>/users/identity</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion] ajoute les en-têtes d’autorisation pour vous.</p> </td> 
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
  <tr> 
   <td role="rowheader">[!UICONTROL Base URL]</td> 
   <td>Sélectionnez l’URL de base à utiliser pour l’appel API.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envoi d’un jeton d’accès]</td> 
   <td>Indiquez si vous souhaitez envoyer le jeton d’accès sous la forme d’un en-tête ou d’un paramètre de requête.</td> 
  </tr> 
 </tbody> 
</table>

## Terminologie

La terminologie suivante peut être utile lors de la configuration des modules [!DNL Slack] :

* **DM** : [!UICONTROL message direct]
* **IM** : [!UICONTROL message instantané]
* **Canal privé** : anciennement [!UICONTROL Groupe]
* **Message direct** : anciennement [!UICONTROL IM]
* **Canal** : [!UICONTROL conversation] dans la documentation de l’API, [!UICONTROL canal] dans l’application [!DNL Slack].
