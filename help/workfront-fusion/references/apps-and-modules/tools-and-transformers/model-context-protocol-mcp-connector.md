---
title: Modules MCP (Model Context Protocol)
description: Le module Model Context Protocol (MCP) permet de traiter une invite utilisateur à l’aide de MCP.
author: Becky
feature: Workfront Fusion
source-git-commit: d8ae176db714d2b9f041b74a62e8276171745c4b
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 14%

---

# Modules MCP (Model Context Protocol)

Le protocole MCP (Model Context Protocol) permet de connecter en toute sécurité des modèles de langage d’IA à d’autres applications. Vous configurez des serveurs MCP qui permettent au modèle d’IA d’accéder à l’application. Vous pouvez ensuite envoyer une invite au modèle d’IA, qui peut renvoyer des informations depuis l’application.

Par exemple, vous pouvez configurer un serveur MCP pour connecter un modèle d’IA à Gmail. Lorsque vous envoyez l’invite « Donnez-moi mes 5 derniers e-mails de Gmail », elle peut accéder à votre Gmail et renvoyer les e-mails.

Le module Model Context Protocol (MCP) permet de traiter une invite utilisateur à l’aide d’un modèle de langue et de serveurs MCP.

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

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Module Model Context Protocol et ses champs

Lorsque vous configurez le module MCP, [!DNL Adobe Workfront Fusion] affiche les champs répertoriés ci-dessous. Un titre en gras dans un module indique un champ obligatoire.

### Traiter l&#39;invite utilisateur

Ce module d’action traite une invite à l’aide du modèle de langue et des serveurs MCP que vous spécifiez.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Clé LLM (Large Language Model)]</td> 
   <td> <p>Saisissez ou mappez la clé API pour le modèle de langue volumineux que vous souhaitez utiliser pour cette invite. </p> <p>Actuellement, seule la clé API Anthropic est prise en charge.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL MCP servers]</td> 
   <td> <p>Pour chaque serveur MCP que vous souhaitez rendre disponible pour cette invite, cliquez sur <b>Ajouter un élément</b> et saisissez le nom et l'hôte du serveur. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entrez votre invite]</td> 
   <td> <p>Saisissez ou mappez l’invite pour le modèle de langue volumineuse. </p> </td> 
  </tr> 
 </tbody> 
</table>
