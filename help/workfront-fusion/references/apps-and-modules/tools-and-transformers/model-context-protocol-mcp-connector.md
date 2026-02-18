---
title: Modules MCP (Model Context Protocol)
description: Le module Model Context Protocol (MCP) permet de traiter une invite utilisateur à l’aide de MCP.
author: Becky
feature: Workfront Fusion
hide: true
hidefromtoc: true
exl-id: 748055ad-d305-4513-9a5c-9c970b74a96e
source-git-commit: 97abe6bf0ff7b10a139268f02f8a1a24f3e31b47
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 18%

---

# Module de l’agent MCP

<!--SET UP REDIRECTS-->

Le protocole MCP (Model Context Protocol) permet de connecter en toute sécurité des modèles de langage d’IA à d’autres applications. Vous configurez des serveurs MCP qui permettent au modèle d’IA d’accéder à l’application. Vous pouvez ensuite envoyer une invite au modèle d’IA, qui peut renvoyer des informations depuis l’application.

Par exemple, vous pouvez configurer un serveur MCP pour connecter un modèle d’IA à Gmail. Lorsque vous envoyez l’invite « Donnez-moi mes 5 derniers e-mails de Gmail », elle peut accéder à votre Gmail et renvoyer les e-mails.

Le module Model Context Protocol (MCP) permet de traiter une invite utilisateur à l’aide d’un modèle de langue et de serveurs MCP.

Pour plus d’informations sur MCP dans les scénarios Fusion, voir [Ajouter une invite d’IA à votre scénario](/help/workfront-fusion/create-scenarios/add-modules/add-an-ai-prompt-to-your-scenario.md).

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
   <td role="rowheader">Produit</td> 
   <td>
   <p>Si votre organisation dispose d’un package Workfront Select ou Prime qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acquérir Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation Workfront](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Conditions préalables

* Vous devez avoir configuré les serveurs MCP auxquels vous avez l’intention de vous connecter.
* Vous devez disposer d&#39;une clé LLM pour le modèle LLM (Large Language Model) sélectionné.

## Module Model Context Protocol et ses champs

### Traiter l&#39;invite utilisateur

Ce module d’action traite une invite à l’aide du modèle de langue et des serveurs MCP que vous spécifiez.

>[!NOTE]
>
>Ce module doit renvoyer un objet . Elle ne renvoie pas de sortie telle que des chaînes ou des nombres.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Clé LLM</td> 
   <td> Sélectionnez une clé LLM existante ou créez-en une en cliquant sur <b>Ajouter</b> et saisissez les informations suivantes : 
     <ul>
       <li><b>Nom de la clé</b> : saisissez le nom de la nouvelle clé.</li>
       <li><b>LLM</b> : sélectionnez le modèle de langue volumineux auquel cette clé est associée.</li>
       <li><b>Clé</b> : saisissez ou mappez votre clé API pour le modèle sélectionné.</li>
       <li><b>Modèle</b> : sélectionnez le modèle LLM que la clé utilisera.</li>
       <li><b>Jetons max</b> : saisissez ou mappez le nombre maximal de jetons que le LLM peut générer dans sa réponse.<p>Un jeton équivaut généralement à quatre caractères, soit .75 d’un mot en anglais. « Hello world » serait égal à deux jetons et « Authentification » serait égal à un à deux jetons.</li>
      </ul>
    </td> 
  </tr> 
  <tr> 
   <td>Serveurs MCP</td> 
   <td> <p>Pour chaque serveur MCP auquel vous souhaitez vous connecter, cliquez sur <b>Ajouter</b> et saisissez les informations suivantes : </p> 
     <ul>
       <li><b>Connexion</b> : sélectionnez la connexion que Fusion utilisera pour se connecter au serveur MCP.</li>
       <li><b>Hôte du serveur MCP</b> : saisissez l’URL du serveur MCP.</li>
       <li><b>Nom du serveur MCP</b> : saisissez ou mappez un nom pour ce serveur MCP.</li>
       <li><b>En-têtes</b> : ajoutez des en-têtes applicables.</li>
       <li><b>Type de serveur MCP</b> : sélectionnez le type de serveur.</li>
      </ul>
    </td> 
  </tr> 
  <tr> 
   <td>Entrez votre invite </td> 
   <td> <p>Saisissez ou mappez l’invite à traiter.</p> </td> 
  </tr> 
 </tbody> 
</table>


