---
name: fusion-doc-request
description: Gérer une demande de documentation Fusion à partir du modèle
source-git-commit: 6726c582294758de0bbab19d6014ad80bb66e553
workflow-type: tm+mt
source-wordcount: '1120'
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

&#x200B;* **Titre de la fonctionnalité**
&#x200B;* **Description**
&#x200B;* **Points à ajouter à la documentation** *(parfois présents - sections/détails spécifiques que le demandeur souhaite voir couverts ; traitez-les comme requis, et non comme facultatifs, le cas échéant)*
&#x200B;* **Date de publication prévue**
&#x200B;* **Annonce des besoins** *(Oui/Non - à titre d’information uniquement ; voir la note ci-dessus. N’agissez pas sur ce champ.)*

Si la requête renvoie à une page de wiki Confluence avec la spécification complète, récupérez-la (`get_wiki_content`) avant de rédiger la documentation. Ne vous fiez pas uniquement au résumé Slack pour les détails techniques (noms de champ exacts, étapes, libellés d’interface utilisateur). Extrayez-les à partir de la spécification du wiki lorsqu’un lien est créé.

Si la requête renvoie plutôt à une source secondaire hors Confluence (par exemple, une publication de la communauté Experience League, un article d’assistance, un résumé généré par l’IA), vous pouvez l’utiliser pour renseigner les détails techniques qui font défaut au texte de Slack, mais la traiter comme une requête moins fiable que la requête Slack elle-même. Lorsqu’il entre en conflit avec le texte du Slack ou l’ajoute à celui-ci (un nom différent pour le même bouton/champ, un détail qui n’est pas du tout mentionné dans Slack), ne le sélectionnez pas en silence. Écrivez le document en utilisant le libellé de la requête Slack comme source principale et signalez la différence en ligne avec un commentaire HTML (par exemple, `<!-- BECKY CHECK ME: Slack calls this "Activate," but the linked community post calls it "Reactivate" - confirm against the live UI. -->`) conformément aux conseils de l’étape 2.

## Étape 2 : mettre à jour la documentation

Recherchez le ou les articles existants pertinents dans ce référentiel (repérez les noms de module, les libellés d’interface utilisateur ou les noms de paramètres associés, sans deviner le fichier). Mettez-les à jour pour refléter la modification, en suivant la structure existante de cet article, le niveau de titre et le style de la maison.

&#x200B;* N’inventez pas de détails techniques (noms de champ exacts, portées d’autorisation, étapes de configuration) qui ne figurent pas dans la requête Slack ou la spécification du wiki lié. Si quelque chose n’est pas confirmé, signalez-le sur la ligne en tant que commentaire HTML (par exemple, `<!-- BECKY CHECK ME: confirm the exact permission scope before publishing -->`) plutôt que comme une supposition, et jamais en tant que légende visible. Il ne doit pas s’afficher sur la page publiée.
&#x200B;* Si cela nécessite un tout nouveau fichier d&#39;article (et pas seulement une modification d&#39;un fichier existant), suivez les conventions permanentes de ce référentiel : aucun `exl-id`/`TQID` fabriqué dans frontMATTER, et convertissez le fichier en CRLF/no-BOM après sa création (l&#39;outil `Write` par défaut est LF).
&#x200B;* Le câblage d’une nouvelle page dans la « table des matières » signifie qu’une page peut être liée à partir d’un sous-index tout en restant invisible pour les lecteurs et lectrices :
  - Le fichier de navigation principal pour la zone de produit (par exemple, `help/workfront-fusion/TOC.md`) : il s’agit de ce qui génère réellement l’arborescence de navigation publiée.
  - Tout sous-index/page de destination contenu qui renvoie également vers des articles de ce type (par exemple, `apps-and-modules-toc.md` pour une nouvelle page de modules de connecteur).
    Vérifiez explicitement et confirmez que la nouvelle entrée se trouve dans la même liste, au même niveau d’imbrication, que ses articles frères les plus proches dans chaque fichier. Ne supposez pas que l’ajout de l’une à l’autre recouvre l’autre.

## Étape 3 : création de la tâche Workfront

Projet : **tâches de documentation du produit - pour les problèmes de développement qui nécessitent une messagerie**. Résolvez son identifiant avec `insights_find_id_by_name` (entité `project`) plutôt que de le coder en dur, au cas où il changerait. Consultez les valeurs connues ci-dessous pour connaître le dernier identifiant résolu.

Champs de tâche :

| Champ | Valeur |
|---|---|
| `name` | `Becky - {Feature Title}` |
| `projectID` | dans la recherche de projet ci-dessus |
| `parentID` | l’identifiant de la tâche parent (`parentID`, un champ système - aucun préfixe `DE:`) - voir les valeurs connues ci-dessous. Cela fait de la nouvelle tâche une sous-tâche, et non une tâche de niveau supérieur dans le projet. |
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

&#x200B;* Quel(s) fichier(s) de documents avez-vous modifié et ce que vous avez ajouté.
&#x200B;* Nom et URL de la tâche.
&#x200B;* Les valeurs de champ exactes que vous définissez, y compris les champs de date de prévisualisation.
&#x200B;* Pour tout ce dont vous n’étiez pas entièrement certain (par exemple, Slack était inatteignable et vous travailliez à partir de texte collé uniquement), l’article du document cible était ambigu ou un détail technique ne figurait pas dans le document source et était marqué au lieu d’être deviné.

## Valeurs connues (issues d’exécutions précédentes)

Confirmez que ces problèmes sont toujours résolus plutôt que de supposer qu’ils sont permanents :

&#x200B;* Le projet « Tâches de documentation du produit - pour les problèmes de développement qui nécessitent une messagerie » est mappé sur l’ID `5e69583f00236b9f767c3e3944100ee4`
&#x200B;* La tâche parent « Becky - Tâches du canal Fusion-Documentation » est mappée à l’ID `6a9b065100003a7554832780c2015e93` (dans le même projet) - résolvez avec `insights_find_id_by_name` (entité `task`) plutôt qu’avec du codage en dur, au cas où il changerait
&#x200B;* Le formulaire personnalisé de la documentation du produit (`categoryID`) est `5d7275b9000514604bd969d418725843`
&#x200B;* Champs personnalisés utilisés : `DE:Release notes`, `DE:Preview Date Known`, `DE:Preview Date`
