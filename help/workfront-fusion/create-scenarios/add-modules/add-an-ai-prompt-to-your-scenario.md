---
title: Ajouter une invite d’IA à votre scénario
description: Vous pouvez inclure dans votre scénario une invite d’IA qui se connecte à votre
author: Becky
feature: Workfront Fusion
source-git-commit: 09e8ca28c12990a699816671d07f85288d973bc7
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Ajouter une invite d’IA à votre scénario

Vous pouvez inclure une invite d’IA dans votre scénario à l’aide du protocole MCP (Model Context Protocol) associé à des modèles de langage (LLM) volumineux. En les configurant dans le module Agent MCP, vous pouvez utiliser l’intelligence artificielle pour configurer des workflows efficaces, sécurisés et flexibles.

>[!NOTE]
>
>Cette fonctionnalité est distincte de la possibilité d’ajouter des modules à un scénario à l’aide de l’IA.
>
>Pour plus d’informations sur l’ajout de modules avec l’IA, voir [Générer un segment de scénario à l’aide de l’IA](/help/workfront-fusion/create-scenarios/add-modules/add-a-module-with-ai.md).

## Présentation de Model Context Protocol

Le protocole MCP (Model Context Protocol) permet de connecter en toute sécurité des modèles de langage d’IA à d’autres applications. Vous configurez des serveurs MCP qui permettent au modèle d’IA d’accéder à l’application. Vous pouvez ensuite envoyer une invite au modèle d’IA, qui peut renvoyer des informations depuis l’application.

Par exemple, vous pouvez configurer un serveur MCP pour connecter un modèle d’IA à Gmail. Lorsque vous envoyez l’invite « Donnez-moi mes 5 derniers e-mails de Gmail » au modèle de langue volumineux, il analyse cette invite et l’envoie au serveur MPC Gmail, qui peut ensuite accéder à votre Gmail et renvoyer les e-mails.

Le module Agent MCP vous permet de traiter une invite utilisateur à l’aide d’un modèle de langue et de serveurs MCP.

## Avantages de l’utilisation de MCP dans vos scénarios Fusion

L’utilisation du MCP dans vos scénarios offre les avantages suivants :

* L’utilisation du MCP dans votre scénario réduit la nécessité de réfléchir à toutes les situations et variantes possibles d’une action. L’utilisation d’une invite élimine la nécessité d’utiliser des données d’expression régulière ou d’analyse pour tenir compte de ces variations.
* Vous pouvez fournir du contexte à l’invite en utilisant des éléments mappés à partir de modules précédents, ou d’autres fonctions dans le panneau de mappage.
* L’utilisation d’une invite peut se révéler plus efficace et plus flexible que la création d’un scénario avec des modules spécifiques, dans la mesure où elle permet d’appliquer un raisonnement à l’invite et de sélectionner la meilleure ligne de conduite dans le contexte disponible.
* Comme vous configurez les serveurs MCP auxquels le module peut se connecter, vous contrôlez la sécurité de ce serveur et pouvez vous assurer que la sécurité répond aux besoins de votre entreprise.

>[!NOTE]
>
>La fonctionnalité disponible dépend des outils disponibles dans le serveur MCP et n’est pas contrôlée par Fusion.

## Ajouter une invite d’IA à votre scénario

Vous pouvez ajouter une invite d’IA à votre scénario à l’aide du module Agent MCP .

Pour obtenir des instructions, voir [Module de l’agent MCP](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/model-context-protocol-mcp-connector.md).
