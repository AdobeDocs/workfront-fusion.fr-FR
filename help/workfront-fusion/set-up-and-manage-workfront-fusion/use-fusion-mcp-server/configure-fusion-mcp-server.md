---
title: Configuration du serveur MCP Adobe Workfront Fusion
description: Connectez Adobe Workfront Fusion à une plateforme d’IA agentic compatible avec MCP ou à un collègue (autonome ou dans le rail de droite de Fusion).
source-git-commit: 6d447c16d199c69ae670f59bb56cf79464cbe057
workflow-type: tm+mt
source-wordcount: '1177'
ht-degree: 1%
---

# Configuration du serveur MCP Adobe Workfront Fusion

Le serveur MCP Adobe Workfront Fusion vous permet de travailler avec les scénarios, les exécutions, les connexions, les webhooks, les entrepôts de données de votre entreprise Fusion, etc., par le biais d’une conversation en langage naturel sur une plateforme agentique d’IA prise en charge.

Pour obtenir la liste des outils disponibles sur le serveur MCP Adobe Workfront Fusion, consultez [Outils du serveur MCP Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-fusion-mcp-server/fusion-mcp-server-tools.md).

## Plateformes d’IA et d’ingénierie prises en charge

Le serveur MCP Fusion fonctionne avec n’importe quelle plateforme agentique d’IA prenant en charge le protocole MCP (Model Context Protocol) et les serveurs MCP distants (HTTP diffusables) avec OAuth.

>[!NOTE]
>
> Actuellement, Adobe ne publie pas de connecteur Workfront Fusion dans le répertoire des connecteurs Claude ou dans le répertoire de l’application/du plug-in ChatGPT. Pour utiliser Fusion avec Claude, ChatGPT ou Microsoft Copilot, ajoutez-le en tant que **serveur MCP personnalisé** par URL, comme décrit dans cet article.

Cet article décrit les étapes de connexion pour :

* [Collègue Adobe ](#use-fusion-with-coworker) : collègue en tant que travailleur autonome et collègue dans le rail de droite de Fusion
* [Claude](#connect-fusion-to-claude) : Connecteur personnalisé
* [ChatGPT](#connect-fusion-to-chatgpt) : serveur MCP personnalisé
* [Une solution MCP personnalisée](#connect-fusion-to-a-custom-mcp-solution)

>[!IMPORTANT]
>
>Si vous utilisez une autre plateforme compatible avec MCP, telle que Gemini, Cursor ou VS Code, suivez la documentation de cette plateforme pour ajouter un serveur MCP personnalisé. Lorsque vous êtes invité à saisir l’URL du serveur MCP, saisissez :
>
>```
>https://mcp.fusion.adobe.com/mcp
>```

## Conditions préalables

Avant de pouvoir connecter Fusion à une plateforme agentique d’IA, vous devez :

* posséder une licence Adobe Workfront Fusion active et avoir accès à au moins une organisation Fusion ;
* disposer d’un rôle d’utilisateur Fusion et de rôles d’équipe qui accordent l’accès aux données que vous souhaitez utiliser ;
* Connectez-vous avec un Adobe ID (système Adobe Identity Management, IMS).
* Avoir accès à une plateforme d’IA agentic compatible avec MCP, ou à un collègue.

## Utilisation de Fusion avec un collègue

Un collègue est un agent d’IA Adobe. Fusion est intégré à Coworker, de sorte que vous n’avez pas besoin de saisir une URL MCP ou d’enregistrer une application OAuth. Vous pouvez utiliser Coworker avec Fusion à deux endroits :

* [Collègue (autonome)](#use-fusion-in-coworker) : utilisez Fusion avec vos autres applications Adobe.
* [Coworker dans le rail de droite de Fusion ](#use-coworker-in-the-fusion-right-rail) : ouvrez Coworker dans un panneau à l’intérieur de l’interface utilisateur de Fusion.

Les deux utilisent les mêmes outils de MCP Fusion, votre Adobe ID et vos autorisations Fusion. Les paramètres des outils de MCP Lecture ou Écriture s’appliquent aux deux. Les actions destructrices, telles que la suppression, l’effacement de la file d’attente ou le remplacement, demandent toujours une confirmation.

### Utiliser Fusion dans un collègue

1. Ouvrez Collègue.
2. Ouvrez **Personnalisation** > **Intégrations**
3. Recherchez **fusion-mcp** et cliquez sur **Test**.
4. Si vous avez accès à plusieurs organisations Fusion, elles sont automatiquement sélectionnées. Vous pouvez demander à votre collègue de changer d’organisation ultérieurement si nécessaire.

### Utilisation de Coworker dans le rail de droite de Fusion

Dans Fusion, Collègue s’ouvre dans le rail de droite.

1. Connectez-vous à Workfront Fusion.
2. Cliquez sur l’icône **Collègue** dans le rail de droite.
3. Posez une question dans le panneau.

### Exemples de prompts

* *Afficher tous les scénarios dont l’exécution a échoué au cours des dernières 24 heures.*
* *Répertorier tous les scénarios créés ou supprimés cette semaine, triés en fonction du plus récent en premier.*
* *À quoi sert ce scénario ?*
* *Pourquoi cette exécution a-t-elle échoué ?*

## Connecter Fusion à Claude

Ajoutez Fusion comme connecteur personnalisé.

>[!NOTE]
>
> Dans Claude Team/Enterprise, vous devez être propriétaire pour ajouter un connecteur personnalisé. Pour plus d’informations, consultez [Prise en main des connecteurs personnalisés à l’aide de MCP distant](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp) dans la documentation Claude.

1. Se connecter à [Claude](https://claude.ai).
2. Dans le menu de gauche, sélectionnez **Personnaliser**.
3. Sélectionnez **Connecteurs**.
4. Sélectionnez **+**, puis **Ajouter un connecteur personnalisé**.
5. Saisissez un nom (par exemple, « Workfront Fusion ») et l’URL du serveur MCP :

   ```
   https://mcp.fusion.adobe.com/mcp
   ```

6. Cliquez sur **Connecter**.
7. Authentifiez-vous. Sélectionnez un profil et une organisation Fusion.

Pour Claude Code, vous pouvez ajouter le serveur à partir de la ligne de commande :

```
claude mcp add --transport http fusion-mcp https://mcp.fusion.adobe.com/mcp
```

## Connecter Fusion à ChatGPT

Ajoutez Fusion comme serveur MCP personnalisé.

### ChatGPT Bureau ou Codex

1. Dans ChatGPT, ouvrez **Settings**.
2. Cliquez sur **Plugins**.
3. Cliquez sur **Ajouter un serveur**.
4. Saisissez le nom du serveur.
5. Pour le type, sélectionnez **HTTP diffusable**.
6. Saisissez l’URL du serveur MCP :

   ```
   https://mcp.fusion.adobe.com/mcp
   ```

7. Cliquer sur **Enregistrer**.
8. Cliquez sur **S’authentifier** pour le nouveau serveur et connectez-vous.
9. Assurez-vous que le bouton (bascule) situé en regard du serveur est activé.

### ChatGPT sur le web

1. Connectez-vous à [ChatGPT](https://chatgpt.com).
2. Accédez à [](https://chatgpt.com/plugins). (Il se peut que le mode Développeur doive être activé sous **Paramètres** ; dans les plans Entreprise/Entreprise, un administrateur doit autoriser les connecteurs personnalisés.)
3. Cliquez sur **+**.
4. Saisissez un **nom**.
5. Pour **Connexion**, sélectionnez **URL du serveur** et saisissez l’URL du serveur MCP.
6. Laissez **Authentification** défini sur **OAuth**.
7. Lisez le message relatif au risque et cochez la case.
8. Cliquez sur **Créer**, puis connectez-vous avec votre.

## Connexion de Fusion à une solution MCP personnalisée

Si vous créez votre propre application ou votre propre agent, connectez-vous directement au serveur MCP Fusion.

## Passer à une autre organisation Fusion

Vous n’avez pas besoin de vous déconnecter pour changer d’organisation. Le serveur MCP Fusion peut changer d’organisation principale au cours d’une session :

* _Quelles sont mes organisations Fusion ?_
* _Passer à l’organisation 1234._

L’agent utilise `fusion_orgs_list` et `fusion_orgs_set`. Le commutateur s’applique uniquement à la conversation/session en cours. Les organisations situées dans différentes zones du centre de données (par exemple, aux États-Unis et dans l’UE) sont toutes disponibles via la même URL MCP.

## Résolution des problèmes de configuration et d’authentification

| Problème | Cause probable | Corriger |
| --- | --- | --- |
| Vous ne trouvez pas de connecteur Fusion dans le répertoire Claude ou ChatGPT. | Adobe ne publie pas de connecteur de répertoire pour Fusion. | Ajoutez Fusion en tant que serveur MCP personnalisé à l’aide de l’URL décrite dans cet article. |
| Vous ne pouvez pas ajouter de connecteur personnalisé dans Claude ou ChatGPT. | Votre plan limite les connecteurs personnalisés aux propriétaires ou aux administrateurs. | Demandez à votre administrateur Claude ou ChatGPT d&#39;ajouter le connecteur ou d&#39;autoriser les serveurs MCP personnalisés. |
| Vous vous êtes connecté, mais vous ne voyez aucune donnée ou les données incorrectes. | La mauvaise organisation Fusion est active. | Demandez à l’agent de répertorier vos organisations et de passer à la bonne. |
| L&#39;authentification a échoué ou la connexion a cessé de fonctionner. | Expiration de la session ou erreur de connexion. | Déconnectez-vous et reconnectez le serveur. |
| Un message indiquant que l’accès au MCP est désactivé s’affiche. | L’accès MCP est désactivé pour votre organisation Fusion. | Demandez à votre administrateur Fusion de l’activer. |
| L’agent peut lire les scénarios, mais ne peut pas les créer, les exécuter, les mettre à jour ni les supprimer. | Les outils MCP d&#39;écriture sont désactivés ou votre rôle d&#39;équipe ne l&#39;autorise pas. | Demandez à votre administrateur Fusion d’activer les outils d’écriture ou de vous accorder le rôle d’équipe requis. |
| L’authentification d’application personnalisée est refusée. | L’URL de rappel ne figure pas dans la liste autorisée. | Demandez à votre administrateur d’ajouter l’URL de rappel exacte. |
| Fusion n’est pas répertorié dans Coworker, ou Coworker est absent du rail de droite Fusion. | Fonctionnalité non activée pour votre organisation. <!-- BECKY CHECK ME: confirm whether this is the correct admin guidance before publishing. --> | Contactez votre administrateur Fusion. |

## Questions fréquentes

### Existe-t-il un connecteur Fusion officiel pour Claude ou ChatGPT ?

Pas pour le moment. Utilisez l’URL du serveur MCP personnalisé. Coworker (autonome et dans le rail de droite de Fusion) a Fusion intégré.

### Puis-je utiliser plusieurs organisations Fusion ?

Oui. Vous pouvez changer d’organisation active au cours d’une conversation sans vous reconnecter.

### Que peut faire l&#39;agent pour moi ?

L’agent agit comme vous, en utilisant votre rôle Fusion et les autorisations de l’équipe. Il ne peut pas accéder à ce à quoi vous ne pouvez pas accéder dans Fusion. Les actions destructrices nécessitent une confirmation explicite.

### L’agent voit-il mes secrets de connexion ?

Non. Les outils de connexion et clés renvoient des métadonnées (nom, type, portées, expiration), et non des informations d’identification ou des valeurs secrètes.
