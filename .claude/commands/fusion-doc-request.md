---
name: fusion-doc-request
description: Gérer une demande de documentation Fusion à partir du modèle
source-git-commit: e354c51f13bd4f15172de068cac9720bd097eb8d
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 0%

---


# Demande de documentation Fusion

Gère le modèle récurrent « Nouvelle demande de documentation de {person} » posté dans le canal Slack `#fusion-documentation` : lire la demande, mettre à jour la documentation, puis créer une tâche de tracking sur le même formulaire personnalisé Workfront utilisé pour chaque demande précédente de ce type.

Il s’agit d’un workflow différent de celui de la compétence `fusion-release-notes`. Cette compétence met à jour un article de référence et crée une tâche Workfront ; elle ne crée pas ou ne met pas à jour de page de note de mise à jour hebdomadaire de Fusion dans ce référentiel, même si la requête indique « Annonce des besoins : oui ». N’utilisez `fusion-release-notes` que si l’utilisateur demande séparément une note de mise à jour hebdomadaire.

## Étape 1 : obtenir les détails de la requête

Si un lien Slack est fourni, analysez le `channel_id` et `message_ts` hors de l’URL et récupérez le thread (`slack_get_thread_replies` ou `slack_read_thread`, selon l’outil de MCP Slack connecté ; essayez les deux si l’un d’eux échoue). Conservez le lien permanent/l’URL du thread - cela est nécessaire à l’étape 3.

Les connexions Slack dans cet environnement sont fragiles (jetons expirés, déconnexions en milieu de session). Si une récupération échoue :
- Réessayez une fois.
- Si l’opération échoue toujours, indiquez clairement à l’utilisateur ou à l’utilisatrice que la récupération a échoué et demandez-lui de coller directement le contenu de la requête. Ne devinez pas le contenu et n&#39;abandonnez pas en silence sans le dire.

Le modèle de requête comporte les champs suivants (extrayez chacun d’eux) :

* **Titre de la fonctionnalité**
* **Description**
* **Points à ajouter à la documentation** *(parfois présents - sections/détails spécifiques que le demandeur souhaite voir couverts ; traitez-les comme requis, et non comme facultatifs, le cas échéant)*
* **Date de publication prévue**
* **Annonce des besoins** *(Oui/Non - à titre d’information uniquement ; voir la note ci-dessus. N’agissez pas sur ce champ.)*

Si la requête renvoie à une page de wiki Confluence avec la spécification complète, récupérez-la (`get_wiki_content`) avant de rédiger la documentation. Ne vous fiez pas uniquement au résumé Slack pour les détails techniques (noms de champ exacts, étapes, libellés d’interface utilisateur). Extrayez-les à partir de la spécification du wiki lorsqu’un lien est créé.

## Étape 2 : mettre à jour la documentation

Recherchez le ou les articles existants pertinents dans ce référentiel (repérez les noms de module, les libellés d’interface utilisateur ou les noms de paramètres associés, sans deviner le fichier). Mettez-les à jour pour refléter la modification, en suivant la structure existante de cet article, le niveau de titre et le style de la maison.

* N’inventez pas de détails techniques (noms de champ exacts, portées d’autorisation, étapes de configuration) qui ne figurent pas dans la requête Slack ou la spécification du wiki lié. Si quelque chose n’est pas confirmé, signalez-le sur la ligne en tant que commentaire HTML (par exemple, `<!-- BECKY CHECK ME: confirm the exact permission scope before publishing -->`) plutôt que comme une supposition, et jamais en tant que légende visible. Il ne doit pas s’afficher sur la page publiée.
* Si cela nécessite un tout nouveau fichier d’article (et pas seulement une modification d’un fichier existant), suivez les conventions permanentes de ce référentiel : aucun `exl-id`/`TQID` fabriqué dans le frontMATTER, connectez la nouvelle page à la table des matières appropriée et convertissez le fichier en CRLF/sans nomenclature après sa création (l’outil `Write` est défini par défaut sur LF).

## Étape 3 : création de la tâche Workfront

Projet : **tâches de documentation du produit - pour les problèmes de développement qui nécessitent une messagerie**. Résolvez son identifiant avec `insights_find_id_by_name` (entité `project`) plutôt que de le coder en dur, au cas où il changerait. Consultez les valeurs connues ci-dessous pour connaître le dernier identifiant résolu.

Champs de tâche :

| Champ | Valeur |
|---|---|
| `name` | `Becky - {Feature Title}` |
| `projectID` | dans la recherche de projet ci-dessus |
| `assignedToID` | l’utilisateur actuel, à partir de `insights_get_current_user` |
| `categoryID` | l’identifiant de formulaire personnalisé de la documentation du produit - voir Valeurs connues ci-dessous. Si ce n’est jamais clair, demandez `task.task_categoryID` sur une tâche sœur récente dans ce projet pour confirmer. |
| `description` | le **texte complet du message Slack** (tous les champs du modèle de demande, et non une paraphrase), suivi d’un lien vers la conversation Slack |
| `DE:Release notes` | une note de mise à jour formatée, voir format ci-dessous |
| `DE:Preview Date Known` | `Yes`, par défaut |
| `DE:Preview Date` | la **date de publication prévue** de la requête, par défaut |
| Produit/zone | sélectionnez `Fusion` (un champ d’énumération du formulaire de documentation du produit ; confirmez le nom exact du champ par `insights_search_fields` s’il est peu clair) |

Définissez les champs de date de prévisualisation dans le cadre de ce même appel de création - ne les laissez pas pour plus tard ou n’attendez pas d’être interrogés. Si l’utilisateur ou l’utilisatrice donne une date différente ultérieurement ou indique que la date n’est pas encore connue, mettez-la à jour en conséquence, mais remplissez-la par défaut à chaque fois.

Format des notes de mise à jour pour le champ `DE:Release notes`. Commencez toujours par `***FUSION***` sur sa propre ligne, puis une ligne vide, puis le titre. La note est marquée comme appartenant à Fusion (par opposition au Workfront principal) en un coup d’œil :

```markdown
***FUSION***

## {Feature Title}

{Description of what changed and why it matters, in second person. A sentence or two is enough for a simple change - use multiple paragraphs and/or a bulleted list for anything with several parts or steps, the same way a full weekly release note would.}

For more information, see [{Article title}](/help/workfront-fusion/{path-to-article}.md).
```

Avant l’appel de création, appelez `read_workflow_docs` avec `workfront://tools/create-any-object` : cet appel définit les champs personnalisés et une valeur d’énumération (`DE:Preview Date Known`), qui la requiert selon les règles du serveur MCP.

## Étape 4 : confirmer à l’utilisateur ou à l’utilisatrice

Signalez simplement :

* Quel(s) fichier(s) de documents avez-vous modifié et ce que vous avez ajouté.
* Nom et URL de la tâche.
* Les valeurs de champ exactes que vous définissez, y compris les champs de date de prévisualisation.
* Pour tout ce dont vous n’étiez pas entièrement certain (par exemple, Slack était inatteignable et vous travailliez à partir de texte collé uniquement), l’article du document cible était ambigu ou un détail technique ne figurait pas dans le document source et était marqué au lieu d’être deviné.

## Valeurs connues (issues d’exécutions précédentes)

Confirmez que ces problèmes sont toujours résolus plutôt que de supposer qu’ils sont permanents :

* Le projet « Tâches de documentation du produit - pour les problèmes de développement qui nécessitent une messagerie » est mappé sur l’ID `5e69583f00236b9f767c3e3944100ee4`
* Le formulaire personnalisé de la documentation du produit (`categoryID`) est `5d7275b9000514604bd969d418725843`
* Champs personnalisés utilisés : `DE:Release notes`, `DE:Preview Date Known`, `DE:Preview Date`
