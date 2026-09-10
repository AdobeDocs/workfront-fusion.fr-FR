---
title: Modules MCP Adobe Experience Manager
description: Avec le module MCP de Adobe Experience Manager, vous pouvez envoyer une invite en anglais clair au serveur MCP de Adobe Experience Manager et laisser un modèle d’IA effectuer la requête.
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 4c23409465b4be9fd10ff6938a750bc662ba2fe4
workflow-type: tm+mt
source-wordcount: 1020
ht-degree: 12%

---

# Modules MCP Adobe Experience Manager

Le connecteur MCP Adobe Experience Manager est une intégration Fusion dédiée au serveur MCP (Model Context Protocol) Adobe Experience Manager. Contrairement à un connecteur standard, où chaque module effectue une action fixe, ce connecteur comporte un seul module qui accepte une instruction ouverte en anglais simple et permet à un modèle d’IA de décider quelles opérations Adobe Experience Manager sont nécessaires pour y répondre, dans des domaines tels que les sites, les ressources numériques, les fragments de contenu, les dossiers, le référentiel de contenu et l’IA dédiée au contenu.

Ce connecteur est dédié au propre serveur MCP de Adobe Experience Manager. Il ne prend pas en charge d’autres serveurs MCP non liés. Pour un connecteur, vous pouvez pointer vers n’importe quel serveur MCP à la place, utilisez le connecteur de l’agent MCP.

Pour plus d’informations sur le connecteur de l’agent MCP, voir [Module de l’agent MCP](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/model-context-protocol-mcp-connector.md).

>[!NOTE]
>
>Les réponses de ce module sont générées par l’IA et peuvent parfois être imparfaites, même si toutes les mesures de protection disponibles sont en place. Ce module est adapté à l&#39;automatisation où un humain ne révise pas chaque exécution en temps réel, mais il n&#39;est pas une garantie du comportement déterministe que vous obtiendriez d&#39;un module Adobe Experience Manager traditionnel.

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tout package de workflow Adobe Workfront et tout package d’automatisation et d’intégration Adobe Workfront</p><p>Workfront Ultimate</p><p>Packages Workfront Prime et Select, avec l’achat supplémentaire de Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licences Adobe Workfront</td> 
   <td> <p>Standard</p><p>Travail ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licence Adobe Workfront Fusion</td> 
   <td>
   <p>Basé sur les opérations : disponible pour les organisations disposant de licences basées sur les opérations</p>
   <p>Basé sur un connecteur (hérité) : Workfront Fusion pour l’automatisation et l’intégration du travail </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Si votre organisation dispose d’un package Workfront Select ou Prime qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acquérir Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences Adobe Workfront Fusion, consultez [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Conditions préalables

* Vous devez disposer d’un compte Adobe Experience Manager pour utiliser ce module.

## Connexion de Adobe Experience Manager MCP à Workfront Fusion {#connect-adobe-experience-manager-mcp-to-workfront-fusion}

Le connecteur MCP Adobe Experience Manager utilise OAuth pour se connecter à Adobe Experience Manager. Il n’existe aucun champ de connexion à renseigner manuellement, tel qu’un nom d’utilisateur, un mot de passe ou une clé API.

Pour créer une connexion, procédez comme suit :

1. Dans le module Adobe Experience Manager MCP , cliquez sur **[!UICONTROL Ajouter]** en regard du champ Connexion .
1. Choisissez si vous vous connectez à un environnement de production ou hors production.
1. Choisissez si vous vous connectez à un compte Service ou à un compte personnel
1. Cliquez sur **Continuer**.

   Vous êtes redirigé vers la page de connexion d’Adobe.
1. Sur la page de connexion d’Adobe, connectez-vous et approuvez l’accès.

Vous êtes redirigé vers Workfront Fusion et la nouvelle connexion est disponible dans le module .

## Module Adobe Experience Manager MCP et ses champs

Actuellement, il n’existe qu’un seul module dans le connecteur MCP Adobe Experience Manager.

### Traiter une invite utilisateur

Ce module d’action envoie une instruction en anglais clair au serveur MCP de Adobe Experience Manager et renvoie la réponse de l’IA.

Chaque exécution de ce module est une exécution autonome unique, similaire à l’envoi d’un e-mail plutôt qu’à une conversation en direct. L’IA ne peut pas poser de question complémentaire et attendre votre réponse. Au lieu de cela, il fait son meilleur jugement et renvoie une réponse complète. Si votre invite est ambiguë, l’IA énonce toute hypothèse qu’elle a faite dans le cadre de sa réponse, plutôt que de s’arrêter pour vous demander de clarifier.

>[!IMPORTANT]
>
>Ce module n’exécute une action d’écriture ou de suppression que lorsque votre invite en demande une. Il ne prend aucune action supplémentaire que vous n’avez pas demandée, même dans la même exécution où il exécute quelque chose d’autre que vous avez demandé.

Comme chaque exécution est indépendante, le module ne possède pas de mémoire des exécutions précédentes par lui-même. Pour créer une expérience de conversation à plusieurs tours sur plusieurs exécutions, stockez la question et la réponse précédentes. Vous pouvez utiliser un magasin de données à cet effet, puis inclure cet historique en tant que texte au début de votre prochaine invite, suivi de la nouvelle question.

Pour plus d’informations sur les magasins de données, voir [Magasin de données](/help/workfront-fusion/create-scenarios/data-stores/data-store-overview.md).

<table style="table-layout:auto"> 
 <col/>
 <col/>
 <tbody>
  <tr>
   <td role="rowheader">Clé LLM <i>(facultative, avancée)</i></td>
   <td><p>Par défaut, ce module traite votre invite à l’aide du propre service d’IA d’Adobe et vous n’avez pas besoin de sélectionner de clé.</p><p>Pour utiliser votre propre fournisseur d’IA à la place, sélectionnez une clé LLM existante ou créez-en une en cliquant sur <b>Ajouter</b> et saisissez les informations suivantes :</p>
    <ul>
     <li><b>Nom de la clé</b> : saisissez le nom de la nouvelle clé.</li>
     <li><b>LLM</b> : sélectionnez le modèle de langue volumineux auquel cette clé est associée. Les fournisseurs pris en charge sont OpenAI, Anthropic Claude et Amazon Bedrock.</li>
     <li><b>Clé</b> : saisissez ou mappez votre clé API pour le fournisseur sélectionné.</li>
     <li><b>Modèle</b> : sélectionnez le modèle LLM que la clé utilisera.</li>
     <li><b>Autres champs</b> : saisissez les valeurs des autres champs requis par votre gestion du cycle de vie des informations.</li>
    </ul>
   </td>
  </tr>
  <tr>
   <td role="rowheader">Connexion</td>
   <td><p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-mcp-to-workfront-fusion" class="MCXref xref">Connexion de Adobe Experience Manager MCP à Workfront Fusion</a> dans cet article.</p></td>
  </tr>
  <tr>
   <td role="rowheader">Invite de l'utilisateur</td>
   <td><p>Saisissez ou mappez l’instruction, en langage clair, que l’IA doit exécuter.</p><p>Exemple : <i>recherchez toutes les ressources du dossier marketing qui n’ont pas été mises à jour depuis 90 jours.</i></p></td>
  </tr>
  <tr>
   <td role="rowheader">Outils en lecture seule <i>(facultatif)</i></td>
   <td><p>Limitez les actions Adobe Experience Manager en lecture seule que l’IA est autorisée à appeler : les actions qui ne font que rechercher quelque chose, comme rechercher une ressource ou lire le contenu d’une page, et qui ne changent jamais rien.</p><p>Si vous laissez ce champ vide, toutes les actions en lecture seule sont autorisées.</p></td>
  </tr>
  <tr>
   <td role="rowheader">Outils d’écriture/suppression <i>(facultatif)</i></td>
   <td><p>Limitez les actions Adobe Experience Manager d’écriture ou de suppression que l’IA est autorisée à appeler : actions qui changent quelque chose, comme la mise à jour d’une page, la publication de contenu ou la suppression d’une ressource.</p><p>Si vous laissez ce champ vide, toutes les actions d’écriture et de suppression sont autorisées. Pour garantir qu’un scénario sans assistance n’engage jamais une action destructrice, nous vous recommandons de laisser ce champ défini sur une sélection délibérément vide plutôt que de le laisser libre.</p></td>
  </tr>
 </tbody>
</table>

Le module renvoie la réponse finale de l’IA, sous forme de texte, ainsi qu’un enregistrement de ce qui s’est passé lors de la production de cette réponse, y compris les outils appelés, si chaque appel a réussi et la durée du traitement.
