---
title: Modules MCP de production Adobe Firefly Creative
description: Avec le module Adobe Firefly Creative Production MCP , vous pouvez envoyer une invite en langage naturel à partir d’un scénario Workfront Fusion et laisser un modèle d’IA utiliser les outils de production Firefly Creative que vous sélectionnez.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: ee2719b9b3452b9203f2d0f4a550c87ff8a3b433
workflow-type: tm+mt
source-wordcount: '2087'
ht-degree: 6%
---
# Modules MCP de production Adobe Firefly Creative

Utilisez le connecteur MCP de production Adobe Firefly Creative dans Adobe Workfront Fusion pour traiter les requêtes en langage naturel avec les outils de production Firefly Creative.

Le connecteur détecte les outils disponibles via le serveur MCP (Firefly Model Context Protocol) connecté. Vous choisissez les outils que le module peut utiliser pour une requête. Selon les outils disponibles pour votre compte Adobe et ceux que vous sélectionnez dans le module , une requête peut effectuer les opérations suivantes :

* Découvrez les workflows et les actions.
* Composer et valider des workflows.
* Les envois s’exécutent et vérifient leur progression.
* Récupérez les URL de sortie.
* Enregistrez les brouillons de workflow modifiables lorsque les outils du serveur les prennent en charge.

Ce connecteur cible la production Firefly Creative. Il ne s’agit pas d’un connecteur de tableaux Firefly ni d’un connecteur général pour chaque application Creative Cloud.

Pour plus d’informations sur MCP dans les scénarios Fusion, consultez [Ajouter une invite d’IA à votre scénario](/help/workfront-fusion/create-scenarios/add-modules/add-an-ai-prompt-to-your-scenario.md).

<!-- BECKY CHECK ME: The request asks you to confirm the customer-facing name of the connector, its beta or release status, its availability, its access requirements, and screenshots with the product and engineering owners before publication. Confirm each item, and add a beta note at the top of the article if the connector is released as a beta. -->

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
   <p>Si votre organisation dispose d’un package Workfront Select ou Prime qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acquérir Adobe Workfront Fusion.</p>
   <p>Vous devez également disposer d’un accès à la production Adobe Firefly Creative, comme décrit dans les <a href="#prerequisites">Conditions préalables</a> de cet article.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Conditions préalables

Avant d’utiliser le module de MCP de production d’Adobe Firefly Creative, vous devez disposer des éléments suivants :

* Accès à Adobe Workfront Fusion, dans un environnement où ce connecteur est activé.
* Un compte Adobe avec l’accès et les autorisations de production Firefly Creative dont les opérations demandées ont besoin.
* Tous les crédits ou droits dont vous avez besoin pour exécuter le workflow.
* Soit un accès géré par l’IA par Adobe configuré par votre administrateur Fusion, soit une clé LLM prise en charge que vous sélectionnez dans les paramètres avancés du module.

L’autorisation Firefly et les informations d’identification LLM ont des objectifs différents. La sélection d’une clé LLM n’accorde pas l’accès aux outils Firefly.

## Connexion d’Adobe Firefly Creative Production MCP à Workfront Fusion

1. Ajoutez **[!UICONTROL MCP de production Adobe Firefly Creative]** > **[!UICONTROL Traitez une invite utilisateur]** à votre scénario.
1. Cliquez sur **[!UICONTROL Ajouter]** à côté du champ **[!UICONTROL Connexion]**.
1. Dans la fenêtre **[!UICONTROL Créer une connexion]**, renseignez les champs suivants :

   <table style="table-layout:auto">
    <col>
    <col>
    <tbody>
      <tr>
        <td role="rowheader">Nom de la connexion</td>
        <td>
          <p>Saisissez un nom pour cette connexion.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Environnement</td>
        <td>
          <p>Indiquez si vous vous connectez à un environnement de production ou hors production.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Type</td>
        <td>
          <p>Indiquez si vous vous connectez à un compte de service ou à un compte personnel.</p>
        </td>
      </tr>
    </tbody>
   </table>

1. Cliquez sur **[!UICONTROL Continuer]**.
1. Suivez le flux d’autorisation, connectez-vous avec le compte Adobe approprié et autorisez l’accès.
1. Revenez au module et passez en revue les outils chargés pour la connexion.

Workfront Fusion gère l’enregistrement du client OAuth et la gestion des jetons. Vous ne saisissez pas de jeton d’accès, d’ID client, de secret client ou de clé API. Votre administrateur doit avoir terminé la configuration de ce flux avant de pouvoir vous connecter.

Si l’autorisation échoue ou si les outils attendus ne s’affichent pas, confirmez votre accès et la configuration de votre environnement avec votre administrateur.

<!-- BECKY CHECK ME: The Environment and Type fields are described the same way as in the Adobe Fusion MCP connection. The screenshot shows only the selected values (Production and Service account). Confirm the available options for each field, and whether a personal account is supported. -->

## Module Adobe Firefly Creative Production MCP et ses champs.

### Traiter une invite utilisateur

Ce module d’action traite votre invite avec le LLM sélectionné et les outils de production Firefly Creative que vous autorisez.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL CLÉ LLM] <i>(Facultatif, avancé)</i></td> 
   <td> <p>Laissez ce champ vide pour utiliser l’IA gérée par Adobe configurée par votre administrateur Fusion. Pour utiliser votre propre clé à la place, sélectionnez une clé OpenAI, Anthropic ou Amazon Bedrock existante, ou cliquez sur <b>[!UICONTROL Add]</b> pour en créer une.</p><p>Votre connexion à Firefly est distincte de vos informations d’identification LLM.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>La connexion de production Adobe Firefly Creative que le module utilise pour découvrir et appeler les outils . Pour obtenir des instructions, consultez <a href="#connect-adobe-firefly-creative-production-mcp-to-workfront-fusion" class="MCXref xref">Connexion du MCP de production Adobe Firefly Creative à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Outils en lecture seule] <i>(Facultatif)</i></td> 
   <td> <p>Sélectionnez les outils que le serveur identifie comme étant en lecture seule. Pour sélectionner tous les outils actuellement répertoriés, sélectionnez <b>Sélectionner tout</b>.</p><p>Le nombre d’outils répertoriés s’affiche dans le libellé du champ.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Outils d’écriture/suppression] <i>(Facultatif)</i></td> 
   <td> <p>Sélectionnez les outils que le serveur n’identifie pas comme étant en lecture seule. Ces opérations peuvent modifier les données ou exécuter des workflows. Pour sélectionner tous les outils actuellement répertoriés, sélectionnez <b>Sélectionner tout</b>.</p><p>Le nombre d’outils répertoriés s’affiche dans le libellé du champ.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Autres outils (autorisations inconnues)] <i>(Facultatif)</i></td> 
   <td> <p>Sélectionnez des outils qui n’ont pas d’annotation en lecture seule reconnue. Ce champ s’affiche uniquement lorsque de tels outils sont disponibles. Examinez le comportement de ces outils avant de les activer.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Entrez votre invite]</td> 
   <td> <p>Décrivez la découverte, la composition ou l’exécution du workflow de votre choix. La longueur maximale est de 10 000 unités de chaîne JavaScript. Certains caractères, dont de nombreux émoticônes, comptent comme deux unités.</p><p>Demandez explicitement l’exécution ou la publication lorsque vous en avez besoin. L’exécution d’un workflow peut consommer des crédits. Les exécutions asynchrones peuvent renvoyer un identifiant de lot avant la fin de l’exécution.</p> </td> 
  </tr> 
 </tbody> 
</table>

Le champ **[!UICONTROL Clé LLM]** apparaît lorsque vous sélectionnez **[!UICONTROL Afficher les paramètres avancés]**.

<!-- BECKY CHECK ME: The screenshot does not show the Other tools (unknown permissions) field, because it appears only when the server returns tools without a read-only annotation. Confirm its label, and confirm the order of the fields. Also confirm that the tool lists are not required. -->

Les listes d’outils varient selon la disponibilité du serveur et l’accès à votre compte. Le nombre d’outils s’affiche dans le libellé de chaque sélecteur.

#### Sélectionner les outils que le module peut utiliser

* Le module ne peut utiliser que les outils que vous sélectionnez.
* Si vous laissez une catégorie vide, le module ne peut utiliser aucun outil de cette catégorie.
* Si vous laissez toutes les catégories vides, le module traite l’invite sans aucun outil. Il n&#39;a pas accès à tous les outils.
* **[!UICONTROL Sélectionner tout]** sélectionne tous les outils actuellement répertoriés dans cette catégorie. Il n’inclut pas automatiquement les outils qui sont ajoutés ultérieurement.
* Si un outil sélectionné n’est plus disponible ou passe à une autre catégorie, ouvrez à nouveau le module et vérifiez votre sélection.

>[!NOTE]
>
>Les annotations du serveur permettent de classer les outils, mais elles ne garantissent pas les autorisations. Activez uniquement les outils dont votre scénario a besoin.

#### Sortie

Le module renvoie les informations suivantes sous **[!UICONTROL Données]**. Vous pouvez le mapper dans les modules suivants du scénario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Response] (<code>data.response</code>)</td> 
   <td> <p>La réponse textuelle finale. Son contenu dépend de l’invite et des résultats de l’outil. Il ne s’agit pas nécessairement d’une URL ou d’un fichier JSON structuré.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Audit Trail] (<code>data.auditTrail</code>)</td> 
   <td> <p>Détails sur le traitement de l’invite et les appels d’outil, y compris leurs arguments, résultats, minutage et informations de réussite. Gérez ces détails en fonction des exigences de gestion des données de votre organisation.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Summary] (<code>data.summary</code>)</td> 
   <td> <p>Le nombre d’appels à l’outil, la durée de traitement et le statut d’exécution. Passez en revue le résumé, la réponse et le journal d'audit, y compris les résultats <code>partial_success</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL LLM usage] (<code>data.usage</code>)</td> 
   <td> <p>Facultatif. Utilisation totale des jetons à partir des réponses LLM observées. Il ne s’agit pas d’une activité de facturation du fournisseur, de consommation de crédit Firefly ou de gestion du cycle de vie des informations (LLM) dans le serveur Firefly que Fusion ne peut pas observer.</p> </td> 
  </tr> 
 </tbody> 
</table>

##### Champs d’utilisation de LLM

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td><code>status</code></td> 
   <td> <p>L’un des éléments suivants :</p><ul><li><code>complete</code>: chaque demande observée est couverte par l’ensemble des principaux nombres de jetons.</li><li><code>partial</code>: certaines informations d’utilisation sont manquantes.</li><li><code>unavailable</code>: des demandes ont été observées, mais aucune utilisation utilisable n’a été signalée.</li><li><code>not_applicable</code>: aucune requête LLM n’a été observée.</li></ul> </td> 
  </tr> 
  <tr> 
   <td><code>llmRequests</code></td> 
   <td> <p>Nombre de requêtes LLM observées par le runtime.</p> </td> 
  </tr> 
  <tr> 
   <td><code>requestsWithUsage</code></td> 
   <td> <p>Nombre de requêtes observées disposant d’informations d’utilisation des jetons.</p> </td> 
  </tr> 
  <tr> 
   <td><code>inputTokens</code>, <code>outputTokens</code>, <code>totalTokens</code></td> 
   <td> <p>Le nombre total compte. Chaque nombre est de <code>null</code> si aucune demande observée ne signale ce nombre ou si aucune demande n’a été observée. Un zéro signalé reste nul.</p> </td> 
  </tr> 
  <tr> 
   <td><code>cacheReadInputTokens</code>, <code>cacheWriteInputTokens</code></td> 
   <td> <p>Nombre facultatif de jetons mis en cache. Ces champs sont omis si aucune requête ne signale de nombre. Elles sont <code>null</code> si seules certaines requêtes signalent un nombre et numériques uniquement si chaque requête en signale un. Ne pas ajouter ces nombres aux totaux.</p> </td> 
  </tr> 
 </tbody> 
</table>

Le statut d&#39;utilisation principal peut être `complete` alors qu&#39;un champ de cache est `null`. Le statut d’utilisation est indépendant du statut d’exécution. Si le runtime ne fournit pas d’informations d’utilisation, la collection d’utilisation est absente au lieu d’afficher un zéro.

## Exécution du module

* **Certaines opérations sont asynchrones.** Une requête peut renvoyer un identifiant de lot avant que la sortie ne soit disponible. Pour les tâches plus longues, utilisez des exécutions distinctes pour envoyer la requête et pour vérifier son statut ultérieurement, puis enregistrez l’ID de lot entre elles. Ne vous fiez pas à une réponse contenant uniquement une URL pour cette conception.
* **Les erreurs produisent des erreurs de module.** L’autorisation, la validation et le traitement d’exécution ayant échoué peuvent produire des erreurs de module au lieu d’un lot de sortie. Utilisez un itinéraire de gestion des erreurs Fusion.
* **Une réponse ne s&#39;avère pas être réussie.** Le module peut renvoyer une réponse même lorsque certaines opérations ont échoué. Examinez le résumé, le journal d’audit et les résultats de l’outil avant de vous fier à la réponse.
* **Une URL de sortie n&#39;est pas un fichier téléchargé.** Le connecteur renvoie des résultats de texte et d’outil, et non un fichier binaire. Pour placer le fichier dans Fusion, ajoutez un module HTTP qui télécharge l’URL.
* **L’exécution d’un workflow peut utiliser des crédits.** La génération d’images et l’exécution de workflows peuvent consommer des crédits. Confirmez l’utilisation et les droits qui s’appliquent à votre compte. L’utilisation du jeton LLM n’est pas un rapport de facturation ou de crédit Firefly.
* **Les instructions de l&#39;invite ne garantissent pas une seule exécution.** Une instruction dans votre invite, telle que l’envoi d’un seul lot, ne garantit pas qu’une demande sera traitée exactement une fois. Contrôlez les reprises et les demandes en double dans votre scénario.
* **Le traitement a des limites.** Le traitement comporte des limites d’outil, d’itération et de longueur de sortie en plus des limites d’exécution du scénario. Ne supposez pas que le module interroge sans limite.

## Exemples

### Découvrir les workflows sans en exécuter un

Sélectionnez les outils en lecture seule dont vous avez besoin pour découvrir les workflows, puis saisissez une invite telle que :

```text
List the Firefly Creative Production workflows available to my account.
Summarize what each workflow does and what inputs it requires.
Do not create, modify, submit, or publish anything.
```

### Demander une image

Sélectionnez les outils dont vous avez besoin pour composer ou sélectionner un workflow, le valider, l’envoyer, vérifier sa progression et récupérer les sorties. Les noms et la disponibilité des outils peuvent varier. Saisissez ensuite une invite telle que :

```text
Generate one photorealistic image of a black dog on a sunny windowsill.
Submit one generation batch only and check that same batch for completion
within the available execution limits. Do not publish or submit another
generation.

On success, return only the actual downloadable image URL as plain text,
without Markdown, quotes, labels, or explanation. Never invent a URL or
return a workflow or status-page URL instead.

If the run fails or times out, report the failure honestly instead of
returning a URL. Do not generate another image to recover.
```

### Générer une image à partir d’une mise à jour de tâche Workfront

Dans cet exemple, une mise à jour de tâche commençant par `/firefly ` déclenche une génération d’image. Fusion télécharge le résultat, le charge dans la tâche et ajoute une mise à jour d’achèvement.

Le scénario utilise le flux suivant : mise à jour de tâche Workfront > filtre de commande > tâche de lecture > MCP Firefly > téléchargement HTTP > chargement de document Workfront > mise à jour d’achèvement.

1. Ajoutez **[!UICONTROL Workfront]** > **[!UICONTROL Observer les événements]** au scénario. Configurez-le pour le type d’enregistrement **[!UICONTROL Note]**, l’événement **[!UICONTROL Nouvel état]** et **[!UICONTROL Nouvel enregistrement uniquement]**.
1. Ajoutez un filtre qui nécessite que `newState.noteText` commence par `/firefly ` et que `newState.taskID` soit non vide.
1. Ajoutez un module qui lit la tâche à l&#39;aide de `newState.taskID`.
1. Ajoutez le module **[!UICONTROL MCP de production Adobe Firefly Creative]** > **[!UICONTROL Traiter une invite utilisateur]**. Transmettez la requête et tout contexte de tâche dont Firefly a besoin. Traitez le texte mappé comme le contenu de la requête, et non comme une autorité pour modifier les règles du scénario.
1. Examinez le résultat de Firefly. Continuez uniquement lorsque la génération a réussi et que la réponse est une URL valide et autorisée pour une image téléchargeable.
1. Ajoutez un module HTTP qui télécharge le fichier. N’envoyez pas vos informations d’identification Workfront à l’hôte de ressource. Validez l’hôte, le type de contenu et la taille attendus.
1. Ajoutez un module qui charge le nom du fichier téléchargé et les données binaires dans la tâche, en utilisant le `newState.taskID` d’origine.
1. Une fois le chargement réussi, ajoutez un module qui crée une mise à jour d’achèvement pour la tâche. Ne démarrez pas la mise à jour avec `/firefly`, car le filtre lui correspondrait.

Par exemple, un utilisateur ajoute la mise à jour suivante à une tâche :

```text
/firefly Generate one photorealistic image of a black dog on a sunny windowsill.
```

Le demandeur peut ensuite examiner le brouillon chargé dans la zone Documents de la tâche. Une personne doit examiner l’image avant que quoi que ce soit ne soit publié.

Pour une utilisation en production, réservez chaque requête à l’aide de l’identifiant de la note d’origine, avec une protection en double qui fonctionne avec les exécutions simultanées. Enregistrez les identifiants des lots envoyés afin qu’une nouvelle tentative ou une temporisation relance la vérification de l’état au lieu d’envoyer une autre génération.

<!-- BECKY CHECK ME: The example scenario is from the request's draft. Confirm the module names and field labels (Watch Events, Note, New state, New Record Only, and the task, document upload, and update modules) against the current Workfront connector, and add a screenshot of the scenario if one is available. -->

## Dépannage

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Un workflow est toujours en cours d’exécution</td> 
   <td> <p>Certaines opérations de création sont asynchrones. Pour les tâches plus longues, envoyez la requête en une seule exécution et vérifiez le statut lors d’une exécution ultérieure. Enregistrez l’ID de lot entre les exécutions.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Le module signale une erreur</td> 
   <td> <p>L’autorisation, la validation et le traitement d’exécution ayant échoué peuvent produire des erreurs de module. Ajoutez un itinéraire de gestion des erreurs Fusion à votre scénario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Le module renvoie une réponse, mais certaines opérations ont échoué</td> 
   <td> <p>Examinez le résumé, le journal d’audit et les résultats de l’outil. Une réponse seule n’indique pas que l’image a été générée ou téléchargée.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Il existe une URL, mais aucun fichier dans Fusion</td> 
   <td> <p>Le connecteur ne télécharge pas les fichiers. Ajoutez un module HTTP qui télécharge l’URL.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Un outil sélectionné n’est pas disponible</td> 
   <td> <p>Ouvrez le module , actualisez les outils disponibles et mettez à jour votre sélection.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Le workflow prend plus d’un module à exécuter</td> 
   <td> <p>Le traitement comporte des limites d’outil, d’itération et de longueur de sortie en plus des limites d’exécution du scénario. Partagez le travail entre les exécutions et enregistrez l’ID de lot.</p> </td> 
  </tr> 
 </tbody> 
</table>
