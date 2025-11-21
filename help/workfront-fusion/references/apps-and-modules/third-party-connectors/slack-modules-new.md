---
title: Modules Slack
description: Dans un scénario  [!DNL Adobe Workfront Fusion] , vous pouvez automatiser les workflows qui utilisent Slack, ainsi que le connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
source-git-commit: 0dbe23c5eb7a0d890b7b543f2f310b163baa3793
workflow-type: tm+mt
source-wordcount: '4580'
ht-degree: 37%

---

# Modules [!DNL Slack]

>[!IMPORTANT]
>
>Cet article décrit les modules disponibles dans le nouveau connecteur Slack, publié le 17 novembre 2025.
>
>Pour plus d’informations sur l’ancien connecteur Slack, voir [[!DNL Slack] modules (hérités)](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/slack-modules.md).

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!DNL Slack] et le connecter à plusieurs applications et services tiers.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tout package de workflow Adobe Workfront et tout package d’automatisation et d’intégration Adobe Workfront.</p><p>Workfront Ultimate</p><p>Packages Workfront Prime et Select, avec un achat supplémentaire de Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licences Adobe Workfront</td> 
   <td> <p>Standard</p><p>Travail ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licence Adobe Workfront Fusion</td> 
   <td>
   <p>Basé sur les opérations : aucune exigence de licence Workfront Fusion.</p>
   <p>Basé sur le connecteur (hérité) : Workfront Fusion pour l’automatisation et l’intégration du travail </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Si votre entreprise dispose d’un package Workfront Select ou Prime qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acheter Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Conditions préalables

* Pour utiliser les modules [!DNL Slack], vous devez disposer d’un compte [!DNL Slack].
* Si vous créez des connexions OAuth@, vous devez ajouter les URL suivantes à la place sur la liste autorisée de votre organisation :
   * jeton de robot : `https://oauth.app.workfrontfusion.com/oauth/cb/slack3`
   * jeton d’utilisateur : ` https://oauth.app.workfrontfusion.com/oauth/cb/slack2`

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

Lorsque vous configurez les modules [!DNL Slack], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Slack] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mapper des informations d’un module à l’autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Bouton bascule Mapper](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Messages](#messages)
* [Fichiers](#files)
* [Canaux](#channels)
* [Réactions](#reactions)
* [Favoris](#stars)
* [Éléments enregistrés](#saved-items)
* [Épingles](#pins)
* [Utilisateurs](#users)
* [Rappels](#reminders)
* [Événements](#events)
* [Profil](#profile)
* [Autre](#other)

### Messages

+++ **[!UICONTROL Créer un message]**

Ce module d’action crée un message.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Blocks]</td> 
   <td>Les blocs sont des composants réutilisables que vous pouvez utiliser pour personnaliser et organiser vos messages. Pour plus d’informations sur les blocs, voir <a href="https://api.slack.com/block-kit">Block Kit</a> dans la documentation [!DNL Slack].</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Identifiant du message de thread (horodatage)]</td> 
   <td>Si le nouveau message est une réponse, saisissez la date et l’heure du message auquel vous souhaitez répondre. Ne saisissez pas la date et l’heure d’un message qui est déjà une réponse.</td> 
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
 </tbody> 
</table>

+++

+++ **[!UICONTROL Supprimer un message]**

Ce module d’action supprime un message spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel ID]</p> </td> 
   <td> <p>Saisissez ou mappez l’identifiant du canal.</p> <p>Note : l’identifiant du canal peut être récupéré à l’aide du module [!UICONTROL List Channels].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID (timestamp)]</td> 
   <td> <p> Saisissez ou mappez la date et l’heure du message que vous souhaitez supprimer.</p> <p>Remarque : la date et l’heure peuvent être récupérées à l’aide d’un autre module, tel que le module Watch Private Channel .</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Obtenir un message d’un canal privé]**

Ce module d’action récupère les détails d’un message à partir d’un canal sélectionné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel]</p> </td> 
   <td> <p>Sélectionnez le canal contenant le message.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Message ID (Time stamp)]</p> </td> 
   <td> <p> Saisissez ou mappez la date et l’heure du message dont vous souhaitez récupérer les informations.</p> <p>Remarque : l’horodatage peut être récupéré à l’aide d’un autre module, tel que le module [!UICONTROL Watch Public Channel].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Obtenir un message d’un canal public]**

Ce module d’action renvoie un message doté d’un identifiant donné provenant d’un canal public spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel ID]</p> </td> 
   <td> <p>Sélectionnez le canal contenant le message.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID (Time stamp)]</td> 
   <td> <p> Saisissez ou mappez la date et l’heure du message dont vous souhaitez récupérer les informations.</p> <p>Remarque : l’horodatage peut être récupéré à l’aide d’un autre module, tel que le module [!UICONTROL Watch Public Channel].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Liste des réponses]**

Ce module d’action récupère un thread de messages publiés dans une conversation.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel type]</td> 
   <td>Sélectionnez le type de canal qui contient le message pour lequel vous souhaitez récupérer les réponses, puis sélectionnez le canal.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Identifiant du message parent (horodatage)]</td> 
   <td> <p> Saisissez ou mappez la date et l’heure du message pour lequel vous souhaitez récupérer les réponses.</p> <p>Remarque : l’horodatage peut être récupéré à l’aide d’un autre module, tel que le module [!UICONTROL Watch Public Channel].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal de réponses que le module doit renvoyer au cours de chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Rechercher un message]**

Ce module de recherche renvoie les messages correspondant à une requête de recherche.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td> <p>Saisissez la requête par laquelle vous souhaitez effectuer la recherche. </p> <p>Pour plus d’informations sur la création de formules à partir du panneau de mappage, voir <a href="/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md" class="MCXref xref">Mappage d’éléments à l’aide de fonctions dans [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Saisissez le nombre maximum d’enregistrements que le module doit renvoyer au cours de chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort by] </td> 
   <td> <p>Choisissez si vous souhaitez trier les messages renvoyés en fonction de leur score ou de leur horodatage.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Choisissez si vous souhaitez trier les messages par ordre croissant ou décroissant.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Mettre à jour un message]**

Ce module d’action permet de modifier un message existant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter a channel ID or name]</p> </td> 
   <td> <p>Choisissez le mode de sélection du message que vous souhaitez modifier.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Dans le champ <strong>[!UICONTROL Channel ID or name]</strong>, saisissez ou mappez l’ID du canal qui contient le message, puis saisissez l’<strong>[!UICONTROL Time Stamp (Message ID)]</strong> du message.</p> <p>Note : l’identifiant du canal peut être récupéré à l’aide du module [!UICONTROL List Channels].</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le type de canal, sélectionnez le canal, puis le message.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Text]</p> </td> 
   <td> <p>Saisissez le nouveau contenu texte du message que vous souhaitez mettre à jour.</p> <p>Pour plus d’informations, voir <a href="https://api.slack.com/docs/formatting">Formatage du texte pour les surfaces d’application</a> dans la documentation [!DNL Slack].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blocks]</td> 
   <td>Les blocs sont des composants réutilisables que vous pouvez utiliser pour personnaliser et organiser vos messages. Pour plus d’informations sur les blocs, voir <a href="https://api.slack.com/block-kit">Block Kit</a> dans la documentation [!DNL Slack].</td> 
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

+++

+++ **[!UICONTROL Regarder les messages directs]**

Ce module de déclenchement démarre le scénario lorsqu’un nouveau message est ajouté à un message direct.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel] </td> 
   <td> <p>Sélectionnez la conversation de message direct que vous souhaitez surveiller pour détecter de nouveaux messages.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Saisissez le nombre maximal de messages que le module doit renvoyer au cours de chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Surveiller les messages directs multipartites]**

Ce module de déclenchement démarre le scénario lorsqu’un nouveau message est ajouté à un canal de message direct multipartie.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel] </td> 
   <td> <p>Sélectionnez la conversation de message direct que vous souhaitez surveiller pour détecter de nouveaux messages.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Saisissez le nombre maximal de messages que le module doit renvoyer au cours de chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Surveiller les messages des canaux privés]**

Ce module de déclenchement lance le scénario lorsqu’un nouveau message est ajouté à un canal privé (groupe).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel] </td> 
   <td> <p>Sélectionnez le canal privé dont vous souhaitez surveiller les nouveaux messages.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Saisissez le nombre maximal de messages que le module doit renvoyer au cours de chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Surveiller les messages des canaux publics]**

Ce module de déclenchement lance le scénario lorsqu’un nouveau message est ajouté à un canal public.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel] </td> 
   <td> <p>Sélectionnez le canal public dont vous souhaitez surveiller les nouveaux messages.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Saisissez le nombre maximal de messages que le module doit renvoyer au cours de chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Fichiers

+++ **[!UICONTROL Supprimer un fichier]**

Ce module d&#39;action renvoie et supprime le fichier spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td> <p>Saisissez ou mappez l’identifiant du fichier que vous souhaitez supprimer. </p> <p>Remarque : l’ID de fichier peut être récupéré à l’aide d’un autre module, tel que le module [!DNL Watch Files].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Obtenir un fichier]**

Ce module d’action renvoie des détails sur le fichier spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td> <p>Saisissez ou mappez l’identifiant du fichier que vous souhaitez récupérer. </p> <p>Remarque : l’ID de fichier peut être récupéré à l’aide d’un autre module, tel que le module [!DNL Watch Files].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Répertorier les fichiers]**

Ce module d’action renvoie une liste de fichiers en fonction du filtre spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type] </td> 
   <td> <p>Sélectionnez le ou les types de fichiers à récupérer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel type]</p> </td> 
   <td> <p>Sélectionnez le type de canal représentant le canal à partir duquel vous souhaitez répertorier les fichiers, puis sélectionnez le canal.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Créé par]</td> 
   <td> <p>Sélectionnez un utilisateur pour ne renvoyer que les fichiers créés par l’utilisateur spécifié.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Date from]</td> 
   <td>Saisissez la date au plus tôt à partir de laquelle vous souhaitez renvoyer les fichiers. Pour obtenir la liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Coercition de type dans [!DNL Adobe Workfront Fusion]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Date to]</td> 
   <td>Saisissez la date la plus récente à laquelle vous souhaitez renvoyer les fichiers. Pour obtenir la liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Coercition de type dans [!DNL Adobe Workfront Fusion]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Saisissez ou mappez le nombre maximal de fichiers que le module doit renvoyer au cours de chaque cycle d’exécution du scénario.</td> 
  </tr> 
 </tbody> 
</table>

+++

<!--

+++ **[!UICONTROL Download a File]**

This action module downloads a file from a URL. It must follow the [!UICONTROL Slack] >[!UICONTROL Get a File] module in a scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL private download]</td> 
   <td> <p>Map the <b>[!UICONTROL URL Private download]</b> value from the [!DNL Slack] >[!UICONTROL Get a File] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

-->

+++ **[!UICONTROL Charger un fichier]**

Ce module d’action crée ou charge un fichier dans [!DNL Slack]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channels]</td> 
   <td> <p>Pour chaque canal sur lequel vous souhaitez charger le fichier, cliquez sur <b>[!UICONTROL Add item]</b>, puis sélectionnez le type de canal et le canal.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title]</td> 
   <td>Saisissez un titre pour le fichier que vous souhaitez charger</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de thread (horodatage)]</td> 
   <td> <p>Si vous téléchargez le fichier en tant que réponse, saisissez ou mappez la date et l’heure du message auquel vous souhaitez répondre.</p> <p>Remarque : la date et l’heure peuvent être récupérées à l’aide d’un autre module, tel que le module [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Initial Comment]</td> 
   <td> <p>Saisissez ou mappez le texte du message qui introduit le fichier.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Surveiller des fichiers]**

Ce module de déclenchement lance un scénario lorsqu’un nouveau fichier est ajouté.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Sélectionnez le type de fichier que vous souhaitez que le module regarde.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel type]</td> 
   <td> <p>Sélectionnez le type de canal à surveiller pour les fichiers, puis sélectionnez le canal.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Créé par]</td> 
   <td> <p>Sélectionnez un utilisateur pour ne renvoyer que les fichiers créés par l’utilisateur spécifié.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Saisissez ou mappez le nombre maximal de fichiers que le module doit renvoyer au cours de chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Canaux

+++ **[!UICONTROL Archiver un canal]**

Ce module d’action archive un canal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel ID]</p> </td> 
   <td> <p>Saisissez ou mappez l’identifiant du canal que vous souhaitez archiver.</p> <p>Note : l’identifiant du canal peut être récupéré à l’aide du module [!UICONTROL List Channels].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Créer un canal]**

Ce module d’action crée un canal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Nom]</p> </td> 
   <td> <p>Saisissez ou mappez un nom pour le nouveau canal.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Est privé]</td> 
   <td>Activez cette option pour définir le nouveau canal comme privé.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Obtenir un canal]**

Ce module d’action renvoie des informations concernant un canal d’espace de travail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel ID]</p> </td> 
   <td> <p>Saisissez ou mappez l’identifiant du canal dont vous souhaitez récupérer les informations.</p> <p>Note : l’identifiant du canal peut être récupéré à l’aide du module [!UICONTROL List Channels].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Rejoindre un canal]**

Ce module d’action associe l’utilisateur à un canal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel ID]</p> </td> 
   <td> <p>Saisissez ou mappez l’identifiant du canal que vous souhaitez joindre.</p> <p>Note : l’identifiant du canal peut être récupéré à l’aide du module [!UICONTROL List Channels].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Laisser un canal]**

Ce module d’action supprime l’utilisateur d’un canal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel ID]</p> </td> 
   <td> <p>Saisissez ou mappez l’identifiant du canal que vous souhaitez quitter.</p> <p>Note : l’identifiant du canal peut être récupéré à l’aide du module [!UICONTROL List Channels].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Répertorier les canaux]**

Ce module de recherche renvoie une liste de tous les canaux d’un espace de travail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
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
   <td> <p>Définissez le nombre maximal de canaux que le module doit renvoyer au cours de chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Répertorier les personnes membres du canal]**

Ce module de recherche renvoie une liste d’utilisateurs et d’utilisatrices dans le canal sélectionné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel type]</td> 
   <td>Sélectionnez le type de canal contenant les membres à répertorier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private Channel]</td> 
   <td>Sélectionnez le canal dont vous souhaitez répertorier les personnes membres.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Définissez le nombre maximal de membres que le module doit renvoyer au cours de chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Définir l’objectif d’un canal]**

Ce module d’action modifie l’objectif d’un canal

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel type]</td> 
   <td>Sélectionnez le type de canal dont vous souhaitez modifier l’objectif.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Privé] / Utilisateur / [!UICONTROL Canal de messagerie instantanée multiple]</td> 
   <td>Sélectionnez le canal ou l’utilisateur dont vous souhaitez modifier l’objectif.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Objectif]</td> 
   <td>Saisissez ou mappez le nouvel objectif du canal. Ce champ ne prend pas en charge la mise en forme des liens.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Définir la rubrique d’un canal]**

Ce module d’action modifie la rubrique d’un canal

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel type]</td> 
   <td>Sélectionnez le type de canal pour lequel vous souhaitez modifier la rubrique.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Privé] / [!UICONTROL Utilisateur] / [!UICONTROL Canal de messagerie instantanée multiple]</td> 
   <td>Sélectionnez le canal ou l’utilisateur pour lequel vous souhaitez modifier la rubrique.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Topic]</td> 
   <td>Saisissez ou mappez la nouvelle rubrique du canal. Ce champ ne prend pas en charge la mise en forme des liens.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Désarchiver un canal]**

Ce module d’action désarchive un canal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel ID]</p> </td> 
   <td> <p>Saisissez ou mappez l’identifiant du canal à désarchiver.</p> <p>Note : l’identifiant du canal peut être récupéré à l’aide du module [!UICONTROL List Channels].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Réactions

+++ **[!UICONTROL Ajouter une réaction]**

Ce module d&#39;action ajoute une réaction à un élément.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel type]</td> 
   <td>Sélectionnez le type de canal auquel vous souhaitez ajouter une réaction.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Privé] / [!UICONTROL User] / [!UICONTROL Multiple IM channel]</td> 
   <td>Sélectionnez le canal ou l’utilisateur auquel vous souhaitez ajouter une réaction.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID (timestamp)]</td> 
   <td> <p> Saisissez ou mappez la date et l’heure du message auquel vous souhaitez ajouter une réaction.</p> <p>Remarque : la date et l’heure peuvent être récupérées à l’aide d’un autre module, tel que le module [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reaction (emoji) name]</td> 
   <td>Saisissez ou mappez le nom de l’émoticône que vous souhaitez utiliser pour une réaction. Exemple : <code>thumbsup</code>. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Liste des réactions]**

Ce module d’action renvoie les réactions qu’un utilisateur a effectuées.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL User]</p> </td> 
   <td> <p>Sélectionnez l’utilisateur qui a effectué les réactions que vous souhaitez répertorier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal de réactions que le module doit renvoyer au cours de chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Supprimer une réaction]**

Ce module d&#39;action supprime une réaction d&#39;un élément.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel type]</td> 
   <td>Sélectionnez le type de canal dont vous souhaitez supprimer une réaction.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Privé] / [!UICONTROL User] / [!UICONTROL Multiple IM channel]</td> 
   <td>Sélectionnez le canal ou l’utilisateur dont vous souhaitez supprimer une réaction.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID]</td> 
   <td> <p> Saisissez ou mappez la date et l’heure du message dont vous souhaitez supprimer une réaction.</p> <p>Remarque : la date et l’heure peuvent être récupérées à l’aide d’un autre module, tel que le module [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reaction (emoji) name]</td> 
   <td>Saisissez ou mappez le nom de l’émoticône à supprimer du message. Exemple : <code>thumbsup</code>. </td> 
  </tr> 
 </tbody> 
</table>

+++

### Favoris

+++ **[!UICONTROL Ajouter une étoile]**

Ce module d’action fait d’un canal un canal étoilé.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel type]</td> 
   <td>Sélectionnez le type de canal auquel vous souhaitez ajouter une étoile.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Privé] / [!UICONTROL User] / [!UICONTROL Multiple IM channel]</td> 
   <td>Sélectionnez le canal ou l’utilisateur auquel vous souhaitez ajouter une étoile.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Supprimer une étoile]**

Ce module d’action supprime l’étoile d’un canal étoilé.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel type]</td> 
   <td>Sélectionnez le type de canal auquel vous souhaitez ajouter une étoile.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Privé] / [!UICONTROL User] / [!UICONTROL Multiple IM channel]</td> 
   <td>Sélectionnez le canal ou l’utilisateur auquel vous souhaitez ajouter une étoile.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Éléments enregistrés

+++ **[!UICONTROL Supprimer élément enregistré]**

Ce module d&#39;action supprime un élément des éléments enregistrés.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID (Time stamp)]</td> 
   <td> <p> Saisissez ou mappez la date et l’heure du message que vous souhaitez supprimer des éléments enregistrés.</p> <p>Remarque : la date et l’heure peuvent être récupérées à l’aide d’un autre module, tel que le module [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td> <p>Saisissez ou mappez le fichier à supprimer des éléments enregistrés.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Enregistrer un élément]**

Ce module d’action ajoute un élément aux éléments enregistrés.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID (Time stamp)]</td> 
   <td> <p> Saisissez ou mappez la date et l’heure du message que vous souhaitez enregistrer.</p> <p>Remarque : la date et l’heure peuvent être récupérées à l’aide d’un autre module, tel que le module [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td> <p>Saisissez ou mappez le fichier que vous souhaitez enregistrer.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Épingles

+++ **[!UICONTROL Épingler un élément]**

Ce module d’action épingle un élément à un canal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel type]</td> 
   <td>Sélectionnez le type de canal auquel vous souhaitez épingler un élément.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Privé] / [!UICONTROL Multiple IM channel] / [!UICONTROL User]</td> 
   <td>Sélectionnez le canal ou l’utilisateur auquel vous souhaitez épingler un élément.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID]</td> 
   <td> <p> Saisissez ou mappez la date et l’heure du message que vous souhaitez épingler.</p> <p>Remarque : la date et l’heure peuvent être récupérées à l’aide d’un autre module, tel que le module [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Détacher un élément]**

Ce module d’action détache un élément d’un canal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel type]</td> 
   <td>Sélectionnez le type de canal dont vous souhaitez désépingler un élément.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Privé] / [!UICONTROL Multiple IM channel] / [!UICONTROL User]</td> 
   <td>Sélectionnez le canal ou l’utilisateur dont vous souhaitez désépingler un élément.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID]</td> 
   <td> <p> Saisissez ou mappez la date et l’heure du message que vous souhaitez détacher.</p> <p>Remarque : la date et l’heure peuvent être récupérées à l’aide d’un autre module, tel que le module [!UICONTROL Watch Private Channel].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Utilisateurs et utilisatrices

+++ **[!UICONTROL Obtenir un utilisateur]**

Ce module d’action récupère les détails d’un membre d’un espace de travail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL User ID]</p> </td> 
   <td> <p>Saisissez ou mappez l’ID utilisateur de l’utilisateur pour lequel vous souhaitez récupérer des détails.</p> <p>Remarque : l’ID utilisateur peut être récupéré à l’aide d’un autre module, tel que le module [!DNL List Users].</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Inviter des utilisateurs]**

Ce module d’action invite de 1 à 30 utilisateurs à accéder à un canal public ou privé.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel type]</td> 
   <td>Sélectionnez le type de canal auquel vous souhaitez inviter des utilisateurs.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Canal privé]</td> 
   <td>Sélectionnez le canal vers lequel vous souhaitez inviter des utilisateurs et utilisatrices.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Users]</td> 
   <td> <p>Sélectionnez les utilisateurs que vous souhaitez ajouter au canal.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Donner un coup de pied à un utilisateur]**

Ce module d’action supprime un utilisateur d’un canal.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel type]</td> 
   <td>Sélectionnez le type de canal dont vous souhaitez supprimer un utilisateur.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Canal privé]</td> 
   <td>Sélectionnez le canal dont vous souhaitez supprimer un utilisateur.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Users]</td> 
   <td> <p>Sélectionnez l’utilisateur que vous souhaitez supprimer du canal.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Liste des utilisateurs]**

Ce module d’action renvoie une liste de tous les utilisateurs d’un espace de travail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Limit]</p> </td> 
   <td> <p>Saisissez ou mappez le nombre maximal d’utilisateurs que le module doit renvoyer au cours de chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Rechercher un utilisateur]**

Ce module d’action récupère les détails d’un utilisateur unique en utilisant son adresse e-mail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email] </p> </td> 
   <td> <p>Saisissez ou mappez l’adresse e-mail de l’utilisateur dont vous souhaitez récupérer les détails.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Observer les utilisateurs]**

Ce module de déclenchement démarre le scénario lorsqu’un nouvel utilisateur est ajouté à l’espace de travail [!DNL Slack].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Définissez le nombre maximal d’utilisateurs que le module doit renvoyer au cours de chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Rappels

<!--

+++ **[!UICONTROL List Reminders]**

This action module returns a list of all reminders created by or given to the currently authenticated user.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Limit]</p> </td> 
   <td> <p>Enter or map the maximum number of reminders you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Get a Reminder]**

This action module retrieves details about a specific reminder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Reminder ID]</p> </td> 
   <td> <p>Enter or map the Reminder ID of the reminder you want to retrieve details for.</p> <p>Note: The Reminder ID can be retrieved using another module, such as the [!UICONTROL List Reminders] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

-->

+++ **[!UICONTROL Créer un rappel]**

Ce module d’action crée un rappel.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td>Saisir ou mapper le contenu du rappel</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Time]</td> 
   <td> <p>Saisissez ou mappez la date et l’heure auxquelles ce rappel doit se produire. Saisissez l’une des informations suivantes : </p> 
    <ul> 
     <li> <p>La date et l’heure Unix (jusqu’à cinq ans à partir de maintenant)</p> </li> 
     <li> <p>Nombre de secondes avant le rappel (si dans les 24 heures) </p> </li> 
     <li> <p>Une description en langage naturel (exemples : « dans 15 minutes » ou « chaque jeudi »)</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL User] </p> </td> 
   <td> <p>Sélectionnez l’utilisateur qui reçoit le rappel.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

<!--

+++ **[!UICONTROL Complete a Reminder]**

This action module completes a specific reminder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Reminder ID]</p> </td> 
   <td> <p>Enter or map the Reminder ID of the reminder you want to complete.</p> <p>Note: The Reminder ID can be retrieved using another module, such as the [!UICONTROL List Reminders] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Delete a Reminder]**

This action module deletes a specific reminder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Reminder ID]</p> </td> 
   <td> <p>Enter or map the Reminder ID of the reminder you want to delete.</p> <p>Note: The Reminder ID can be retrieved using another module, such as the [!UICONTROL List Reminders] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

-->

### Événements

+++ **[!UICONTROL Nouvel événement]**

Ce déclencheur instantané démarre un scénario lorsqu’un nouveau message ou un autre événement est créé.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Webhook]</p> </td> 
   <td> <p>Sélectionnez le webhook que vous souhaitez utiliser.</p> <p>Ou</p> <p>Créez un webhook.</p> 
    <ol> 
     <li value="1"> <p>Cliquez sur <b>[!UICONTROL Add]</b>.</p> </li> 
     <li value="2"> <p>Sélectionnez le type d’événement.</p> </li> 
     <li value="3"> <p>Sélectionnez ou ajoutez une connexion. Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!UICONTROL Workfront Fusion], consultez <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!UICONTROL Adobe Workfront Fusion] - Instructions de base</a></p> </li> 
     <li value="4"> <p>Si vous y êtes invité, sélectionnez la chaîne que vous souhaitez regarder.</p> </li> 
     <li value="5"> <p>Cliquez sur <b>[!UICONTROL Save]</b> pour enregistrer le webhook et revenir au module.</p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Profil

+++ **[!UICONTROL Définir un statut]**

Ce module d’action met à jour le statut actuel d’un utilisateur.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connexion] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Status text]</p> </td> 
   <td> <p>Saisissez ou mappez le texte du statut. Tenez compte des points suivants :</p> 
    <ul> 
     <li> <p>Vous pouvez saisir jusqu’à 100 caractères.</p> </li> 
     <li> <p>Vous pouvez utiliser des balises ou d’autres mises en forme, telles que les mentions d’utilisateur.</p> </li> 
     <li> <p>Vous pouvez inclure des émoticônes dans le texte de statut à l’aide de l’<code>:emojiname:</code> de format .</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status emoji]</td> 
   <td> <p>Saisissez ou mappez l’émoticône que vous souhaitez utiliser pour représenter votre statut. Utilisez le format <code>:emojiname:</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status expiration]</td> 
   <td>Saisissez ou mappez la date et l’heure d’expiration du statut. Pour obtenir la liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Type coercition</a>.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Autre

+++ **[!UICONTROL Réaliser un appel API]**

Ce module d’action permet d’effectuer un appel authentifié personnalisé vers l’API [!DNL Slack]. Ainsi, vous pouvez créer une automatisation du flux de données qui ne peut pas être réalisée par les autres modules [!DNL Slack].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Slack] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
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
 </tbody> 
</table>

+++

## Terminologie

La terminologie suivante peut être utile lors de la configuration des modules [!DNL Slack] :

* **DM** : [!UICONTROL message direct]
* **IM** : [!UICONTROL message instantané]
* **Canal privé** : anciennement [!UICONTROL Groupe]
* **Message direct** : anciennement [!UICONTROL IM]
* **Canal** : [!UICONTROL conversation] dans la documentation de l’API, [!UICONTROL canal] dans l’application [!DNL Slack].

