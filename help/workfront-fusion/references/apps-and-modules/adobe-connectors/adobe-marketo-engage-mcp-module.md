---
title: Module Adobe Marketo Engage MCP
description: Le module MCP de Adobe Marketo Engage vous permet d’envoyer une invite en langage naturel au serveur MCP (Model Context Protocol) de Adobe Marketo Engage.
author: Becky
feature: Workfront Fusion
exl-id: 3f29ab35-7a90-4afb-a283-4faaacec5b15
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: b58ad82f-df6b-4b01-81a3-3a02ab9567a0
    internal-label: APIs
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
  - id: e14a7f57-c82c-4874-a495-5d036cbbdc3d
    internal-label: Resource management
subfeature_v2:
  - id: b70a979b-965d-47a9-a360-e7ec2a19b8c1
    internal-label: Digital content and documents
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 9e08c421a53c7ca499715fa8e32be6c10fbde1d9
workflow-type: tm+mt
source-wordcount: '1579'
ht-degree: 11%
---
# Module Adobe Marketo Engage MCP

Le module MCP de Adobe Marketo Engage vous permet d’envoyer une invite en langage naturel au serveur MCP (Model Context Protocol) de Adobe Marketo Engage, à l’aide d’un modèle d’IA pour interpréter la requête et appeler les propres outils de Marketo pour y répondre. Contrairement à un connecteur Marketo traditionnel où chaque module effectue une action fixe, telle que « Créer un prospect », ce connecteur comporte un seul module qui accepte une instruction ouverte en anglais simple et permet à l’IA de décider quelles opérations Marketo sont nécessaires pour y répondre.

Ce connecteur est spécifiquement destiné au serveur MCP de Marketo Engage

Pour vous connecter à des MCP pour d’autres applications, voir [Ajouter une invite d’IA à votre scénario](/help/workfront-fusion/create-scenarios/add-modules/add-an-ai-prompt-to-your-scenario.md).

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

* Vous devez disposer d’un compte Adobe Marketo Engage et d’une instance Marketo valide.

## Connexion de Adobe Marketo Engage MCP à Workfront Fusion {#connect-adobe-marketo-engage-mcp-to-workfront-fusion}

Vous pouvez créer une connexion à votre instance Marketo directement depuis le module MCP de Adobe Marketo Engage.

1. Dans le module MCP de Adobe Marketo Engage, cliquez sur **Ajouter** en regard du champ **Connexion**.
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
          <p>Saisissez un nom pour la nouvelle connexion.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>
          <p>Indiquez si vous vous connectez à un environnement de production ou hors production.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>
          <p>Indiquez si vous vous connectez à un compte de service ou à un compte personnel.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>
          <p>Saisissez l’ID client pour votre service d’API REST Marketo, tel que créé dans Marketo LaunchPoint.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>
          <p>Saisissez le secret client pour votre service API REST Marketo, tel que créé dans Marketo LaunchPoint.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Munchkin ID]</td>
        <td>
          <p>Saisissez l’identifiant Munchkin de votre instance Marketo (par exemple, « 123-ABC-456 »). L’ID Munchkin s’affiche dans Marketo sous <b>Admin → Munchkin</b>.</p>
        </td>
      </tr>
    </tbody>
   </table>

1. Cliquez sur **Continuer** pour créer la connexion et revenir au module.

>[!IMPORTANT]
>
> * Utilisez un utilisateur Marketo dédié uniquement avec l’API et disposant du rôle et des autorisations minimum requis pour le scénario, plutôt que de réutiliser un compte d’administrateur.
> * La création de la connexion ne valide pas les informations d’identification. Fusion les enregistre sans appel de test, de sorte que la connexion peut sembler créée avec succès même si une valeur est incorrecte ou mal orthographiée. Si des informations d’identification sont incorrectes, l’échec se produit généralement plus tard, lorsque le module tente d’atteindre Marketo pour la première fois ou lorsque le chargement des listes d’outils échoue.

## Le module : « Traitement d’une invite utilisateur »

Il s’agit du seul module fourni par le connecteur. Un scénario l’utilise en fournissant :

1. **Connexion** : la connexion Marketo créée ci-dessus.
2. **Entrez votre invite** — l’instruction, en anglais simple (par exemple, « trouvez chaque prospect ajouté à la liste des webinaires de printemps au cours de la dernière semaine et dites-moi lesquels n’ont pas de nom de société défini »).
3. **Outils** (facultatif) — décrit ci-dessous. Ces champs n’apparaissent qu’une fois la connexion sélectionnée.
4. **Clé LLM** (facultatif, avancé) - décrit ci-dessous.

Elle renvoie la réponse finale de l’IA sous forme de texte, ainsi qu’un journal d’audit complet de ce qui s’est passé lors de la production de cette réponse.

## Module Adobe Marketo Engage MCP et ses champs

### Traiter une invite utilisateur

Ce module d’action envoie une instruction en anglais clair au serveur MCP de Adobe Marketo Engage et renvoie la réponse de l’IA.

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
   <td><p>Pour plus d’informations sur la connexion de votre compte Marketo à Workfront Fusion, voir <a href="#connect-adobe-marketo-engage-mcp-to-workfront-fusion" class="MCXref xref">Connexion de Adobe Marketo Engage MCP à Workfront Fusion</a> dans cet article.</p></td>
  </tr>
  <tr>
   <td role="rowheader">Invite utilisateur</td>
   <td><p>Saisissez ou mappez l’instruction, en langage clair, que l’IA doit exécuter.</p><p>Exemple : <i>recherchez tous les prospects ajoutés à la liste du webinaire de printemps au cours des 7 derniers jours et résumez les secteurs d’activité les plus courants.</i></p></td>
  </tr>
 </tbody>
</table>

### Sortie de module

La sortie est un lot unique contenant les éléments suivants :

* Réponse : réponse finale de l’IA, sous forme de texte. Vous pouvez mapper ces données dans des modules ultérieurs.
* Journal d’audit : enregistrement détaillé de l’exécution, y compris un ID de session, l’invite d’origine, les heures de début et de fin, la durée totale, le statut global, la réponse finale et une liste d’appels d’outil. Chaque entrée d’appel d’outil enregistre l’outil Marketo exécuté, ses arguments, sa sortie, son heure et sa durée de début et de fin, s’il a réussi et son ordre dans la séquence.
* Résumé : la même exécution s’est résumée à des nombres : nombre total d’appels à l’outil, appels réussis, appels ayant échoué, temps de traitement et statut.

### Modèles d’IA

Par défaut, le module utilise automatiquement son propre service d’IA géré Adobe, sans clé ni informations d’identification à saisir.

Vous pouvez plutôt sélectionner une clé LLM spécifique à utiliser OpenAI, Anthropic Claude ou Amazon Bedrock, si votre entreprise dispose d’un compte avec l’un de ces éléments.

### Choisir les actions Marketo que l’IA est autorisée à entreprendre

Une fois la connexion sélectionnée, le module demande au serveur MCP Marketo quels outils il propose et les présente sous forme de listes à sélection multiple, chacune indiquant le nombre d’outils qu’elle contient :

* Outils en lecture seule : actions qui recherchent uniquement des informations et ne les modifient jamais, telles que la recherche d’un prospect, la mise en liste des membres de la campagne ou la lecture des détails d’un programme.
* Outils d’écriture/suppression : actions qui modifient quelque chose, comme la création ou la mise à jour d’un prospect, l’ajout d’une personne à une liste, l’activation d’une campagne ou la validation ou l’envoi d’un e-mail.
* Autres outils : troisième liste qui s’affiche uniquement si le serveur Marketo propose des outils qu’il n’a pas étiquetés comme étant en lecture seule ou non. Elles sont présentées séparément plutôt que d’être considérées comme sûres ou dangereuses. Si le serveur attribue tous les libellés, cette liste n’apparaît pas.

Si aucun outil n’est sélectionné, l’IA peut tous les utiliser. Vous pouvez restreindre une liste à des actions spécifiques. Par exemple, la sélection de seulement 2 actions spécifiques « écriture » tout en laissant « lecture seule » seule signifie que l’IA peut rechercher librement tout ce dont elle a besoin, mais ne peut effectuer que ces 2 types spécifiques de modifications. Le fait de laisser une liste vide signifie que toutes les actions de cette catégorie sont autorisées. Restreindre l’IA nécessite de choisir activement les actions spécifiques à autoriser dans cette catégorie. Vous pouvez ainsi vous assurer que l’IA n’entreprendra pas d’action destructrice inattendue contre les données marketing actives, tout en lui permettant de collecter librement des informations.

Comme les listes sont lues en direct à partir du serveur Marketo, les outils affichés peuvent changer à mesure qu’Adobe met à jour ce serveur.

### Aucun historique de conversation persistant

Chaque exécution de ce module est une exécution autonome unique. L’IA ne peut pas poser de question complémentaire et attendre une réponse. Il doit plutôt faire de son mieux et donner une réponse complète et définitive en une seule fois. Si une requête est ambiguë, l’IA fera une hypothèse raisonnable, indiquera cette hypothèse dans sa réponse et poursuivra. Il ne s’arrêtera pas et ne demandera pas à l’utilisateur de clarifier, car il n’y a aucun moyen pour qu’il reçoive une réponse au cours d’une seule exécution.

L’IA a également pour instruction de vérifier les faits à l’aide d’un appel d’outil plutôt que de compter sur la mémoire, car les données de Marketo peuvent avoir changé depuis l’exécution précédente.

L’IA n’effectue une action d’écriture, de mise à jour ou de suppression que lorsque l’invite en a réellement demandé une. Il n’entreprendra aucune action qui n’a pas été demandée, notamment l’activation ou la désactivation de campagnes, la création ou la suppression de prospects et de listes, ainsi que la validation ou l’envoi d’e-mails, même lors de la même exécution où il effectue une autre action que l’utilisateur a demandée.

Comme chaque exécution est indépendante, l’IA ne dispose d’aucune mémoire d’une exécution précédente par elle-même. Un scénario qui souhaite une expérience de conversation à plusieurs tours doit explicitement fournir cet historique dans le cadre de la nouvelle invite, par exemple en stockant la question et la réponse précédentes dans le magasin de données de Fusion, ou transmis entre les modules, et en l’incluant comme texte au début de la nouvelle invite, suivi de la nouvelle question. Aucun ID de session ou de conversation ne mémorise automatiquement les exécutions précédentes.

## Exemples de prompts

Vous pouvez utiliser des invites telles que :

* *Répertoriez les prospects qui ont rejoint le programme « Lancement de produits du 3e trimestre » au cours des 7 derniers jours et résumez les secteurs dans lesquels ils se trouvent.*
* *Vérifiez si la campagne intelligente &#39;Série de bienvenue&#39; est actuellement active, et dites-moi combien de personnes y participent.*
* *Recherchez le formulaire utilisé sur notre page de tarification et dites-moi quels champs sont marqués comme obligatoires.*
* *Ajouter le prospect avec `jane@example.com` d’e-mail à la liste statique « Clients VIP ».*
* *Résumez les performances de chaque e-mail dans le programme &#39;Newsletter du printemps&#39;.*

<!--

## What a content writer should NOT claim

* Connection form: Do not describe the connection as an OAuth or "sign in with Adobe" flow. It is not one. It is three credential fields that the user copies out of Marketo's LaunchPoint and Munchkin admin pages. Screenshots or steps borrowed from the AEM MCP connector docs would be wrong here.
* Credential validation: Do not imply that the connection form validates the credentials. It saves them without testing them.
* Module scope: This is not a substitute for individual Marketo action modules. It is a single, flexible AI-driven module, not a set of deterministic single-purpose modules.
* Reliability: Results are AI-generated and can occasionally be imperfect, even with every safeguard above in place. This is appropriate for automation where a human is not reviewing every single run in real time, but it is not a guarantee of 100% deterministic behavior the way a traditional Marketo module is. This deserves extra emphasis for Marketo specifically, because a write action here can email real customers or alter real lead records.
* Tool restrictions: The read/write tool split limits what categories of Marketo actions the AI can take. It is not a way to sandbox or limit what the AI is capable of reasoning about or discussing in its answer text.
* Tool naming: Do not name specific Marketo MCP tools or actions unless they are verified against the live tool list. This document intentionally describes capability areas, such as leads, lists, campaigns, programs, emails, forms, snippets, and bulk operations, rather than exact tool names, since the server's exact tool set may evolve.
* API limits: Do not state Marketo API rate limits, quotas, or daily call caps as if this connector defines them. Any such limit comes from the user's own Marketo subscription and REST API allowance; verify with the Marketo team before publishing numbers.

## Reference links used while compiling this

* Adobe Marketo Engage MCP server (developer documentation):
  https://experienceleague.adobe.com/fr/docs/marketo-developer/marketo/mcp-server

  -->
