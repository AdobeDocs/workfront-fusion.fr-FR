---
name: fusion-doc-request
description: Gérer une demande de documentation Fusion depuis #fusion-documentation Slack template - update the relevant Fusion docs article(s) in this repo, then create a matching task in the Product Documentation Workfront project with the feature description and a formatted release note filled in on the custom form. Use when the user shares a Slack documentation-request thread/message for a Fusion feature, or says something like "please update and create a task" for one.
source-git-commit: 17a2d521197e676e41b4b899f7be142430a18c2f
workflow-type: tm+mt
source-wordcount: '1704'
ht-degree: 0%
---

# Demande de documentation Fusion

Gère le modèle récurrent « Nouvelle demande de documentation de {person} » posté dans le canal Slack `#fusion-documentation` : lire la demande, mettre à jour la documentation, puis créer une tâche de suivi sur le même formulaire personnalisé Workfront utilisé pour chaque demande précédente de ce type.

Il s&#39;agit d&#39;un workflow différent de la compétence `fusion-release-notes`. Cette compétence met à jour un article de référence et crée une tâche Workfront ; elle ne crée pas ou ne met pas à jour de page de note de mise à jour hebdomadaire de Fusion dans ce référentiel, même si la requête indique « Annonce des besoins : oui ». N&#39;utilisez `fusion-release-notes` que si l&#39;utilisateur demande séparément une note de mise à jour hebdomadaire.

## Étape 1 : obtenir les détails de la requête

Si un lien Slack vous est fourni, analysez les propriétés `channel_id` et `message_ts` de l’URL et récupérez le thread (`slack_get_thread_replies` ou `slack_read_thread`, en fonction de l’outil de MCP Slack auquel vous êtes connecté - essayez les deux si l’un d’eux échoue). Conservez le lien permanent/l’URL du thread - cela est nécessaire à l’étape 4.

Les connexions Slack dans cet environnement sont fragiles (jetons expirés, déconnexions en milieu de session). Si une récupération échoue :
- Réessayez une fois.
- Si l’opération échoue toujours, indiquez clairement à l’utilisateur ou à l’utilisatrice que la récupération a échoué et demandez-lui de coller directement le contenu de la requête. Ne devinez pas le contenu et n&#39;abandonnez pas en silence sans le dire.

Le modèle de requête comporte les champs suivants (extrayez chacun d’eux) :

* **Titre de la fonctionnalité**
* **Description**
* **Points à ajouter à la documentation** *(parfois présents - sections/détails spécifiques que le demandeur souhaite voir couverts ; traitez-les comme requis, et non comme facultatifs, s’ils sont fournis)*
* **Date de publication prévue**
* **Annonce requise** *(Oui/Non - à titre d’information uniquement ; voir la note ci-dessus. N&#39;agissez pas sur ce champ.)*

Si la requête renvoie à une page de wiki Confluence avec la spécification complète, récupérez-la (`get_wiki_content`) avant de rédiger la documentation. Ne vous fiez pas uniquement au résumé Slack pour les détails techniques (noms de champ exacts, étapes, libellés d’interface utilisateur). Extrayez-les à partir de la spécification du wiki lorsqu’un lien est créé.

Si la requête renvoie plutôt à une source secondaire hors Confluence (par exemple, une publication de la communauté Experience League, un article d’assistance, un résumé généré par l’IA), vous pouvez l’utiliser pour renseigner les détails techniques qui font défaut au texte de Slack, mais la traiter comme une requête moins fiable que la requête Slack elle-même. Lorsqu’il entre en conflit avec le texte du Slack ou l’ajoute à celui-ci (un nom différent pour le même bouton/champ, un détail qui n’est pas du tout mentionné dans Slack), ne le sélectionnez pas en silence. Écrivez le document en utilisant le libellé de la requête Slack comme source principale et signalez l’incohérence avec un commentaire HTML (par exemple, `<!-- BECKY CHECK ME: Slack calls this "Activate," but the linked community post calls it "Reactivate" - confirm against the live UI. -->`) conformément aux conseils de l’étape 3.

## Étape 2 : créer une branche pour la requête

Avant de toucher des fichiers, créez une branche Git pour cette requête et extrayez-la. Branche de la branche par défaut actuelle (`main`), et non de la branche qui est extraite.

Si l’utilisateur a déjà créé et nommé la branche, utilisez-la au lieu d’en créer une nouvelle et enregistrez ce nom dans le champ `Documentation Branch` de la tâche à l’étape 4.

Nommez la branche `becky-{short-kebab-case-description}`, à partir du **Titre de la fonctionnalité** - le premier mot doit être `becky`, correspondant à la convention de branche existante de ce référentiel (par exemple, `becky-webhook-update`, `becky-storage-beta-sos`). Soyez bref - quelques mots, pas le titre complet.

Si l’arborescence de travail n’est pas propre (modifications non validées provenant d’un travail non lié), arrêtez-la et informez-en l’utilisateur plutôt que de la survoler.

Cette compétence crée et valide la branche, mais ne la transmet pas et n’ouvre pas de demande d’extraction. Laissez cela à l’utilisateur, sauf s’il vous le demande séparément.

## Étape 3 : mettre à jour la documentation

Recherchez le ou les articles existants pertinents dans ce référentiel (repérez les noms de module, les libellés d’interface utilisateur ou les noms de paramètres associés, sans deviner le fichier). Mettez-les à jour pour refléter la modification, en suivant la structure existante de cet article, le niveau de titre et le style de la maison.

* N’inventez pas de détails techniques (noms de champ exacts, portées d’autorisation, étapes de configuration) qui ne figurent pas dans la requête Slack ou la spécification du wiki lié. Si quelque chose n’est pas confirmé, signalez-le sur la ligne en tant que commentaire HTML (par exemple `<!-- BECKY CHECK ME: confirm the exact permission scope before publishing -->`) plutôt que de faire des suppositions, jamais en tant que légende visible. Il ne doit pas s’afficher sur la page publiée.
* Si cela nécessite un tout nouveau fichier d&#39;article (et pas seulement une modification d&#39;un fichier existant), suivez les conventions permanentes de ce référentiel : aucun `exl-id`/`TQID` fabriqué dans frontMATTER, et convertissez le fichier en CRLF/no-BOM après sa création (l&#39;outil `Write` est défini par défaut sur LF).
* Le câblage d’une nouvelle page dans la « table des matières » signifie qu’une page peut être liée à partir d’un sous-index tout en restant invisible pour les lecteurs et lectrices :
  - Le fichier de navigation principal pour la zone de produit (par exemple, `help/workfront-fusion/TOC.md`). C’est ce qui anime réellement l’arborescence de navigation publiée.
  - Tout sous-index/page de destination contenu qui pointe également vers des articles de ce type (par exemple, `apps-and-modules-toc.md` pour une nouvelle page de modules de connecteur).
    Vérifiez explicitement et confirmez que la nouvelle entrée se trouve dans la même liste, au même niveau d’imbrication, que ses articles frères les plus proches dans chaque fichier. Ne supposez pas que l’ajout de l’une à l’autre recouvre l’autre.
* Laissez les modifications apportées au document non validées sur la branche . N’exécutez pas `git commit` (ou `git add`) dans le cadre de cette compétence : l’utilisateur valide lorsqu’il est prêt, après avoir examiné les modifications. Validez uniquement si l’utilisateur vous le demande explicitement.

## Étape 4 : création de la tâche Workfront

Projet : **tâches de documentation du produit - pour les problèmes de développement qui nécessitent une messagerie**. Résolvez son identifiant avec `insights_find_id_by_name` (entité `project`) plutôt que de le coder en dur, au cas où il changerait - consultez les valeurs connues ci-dessous pour le dernier identifiant résolu.

Champs de tâche :

| Champ | Valeur |
|---|---|
| `name` | `Becky - {Feature Title}` |
| `projectID` | dans la recherche de projet ci-dessus |
| `parentID` | l’identifiant de tâche parent (`parentID`, un champ système - pas de préfixe `DE:`) - voir les valeurs connues ci-dessous. Cela fait de la nouvelle tâche une sous-tâche, et non une tâche de niveau supérieur dans le projet. |
| `assignedToID` | l’utilisateur actuel, à partir de `insights_get_current_user` |
| `categoryID` | l’identifiant de formulaire personnalisé de la documentation du produit - voir Valeurs connues ci-dessous. Si ce n&#39;est jamais clair, demandez à `task.task_categoryID` de confirmer une tâche sœur récente dans ce projet. |
| `description` | le texte **complet du message Slack** (tous les champs du modèle de demande, et non une paraphrase), suivi d’un lien vers la conversation Slack |
| `DE:Release notes` | une note de mise à jour formatée, voir format ci-dessous |
| `DE:Preview Date Known` | `Yes`, par défaut |
| `DE:Preview Date` | la date citée dans le message Slack d’origine (la **date de publication prévue de la requête**), par défaut |
| `taskConstraint` + `constraintDate` | Définissez `taskConstraint` sur `MFO` (Doit se terminer le) avec `constraintDate` = la date citée dans le message Slack d’origine (la **date de publication prévue de la requête**), de sorte que la date d’achèvement prévue de la tâche la corresponde également. |
| `DE:Articles to update` | la liste des articles que vous avez créés ou mis à jour pour cette requête (voir ci-dessous) |
| `DE:Documentation Branch` | nom de la branche git sur laquelle se trouvent les modifications apportées au document (voir ci-dessous) |
| Produit/zone | sélectionnez `Fusion` (un champ d’énumération sur le formulaire de documentation du produit ; confirmez le nom exact du champ avec `insights_search_fields` s’il n’est jamais clair) |

`DE:Articles to update` (un champ de texte sur le formulaire Documentation du produit) répertorie chaque fichier d’article que vous avez créé ou modifié à l’étape 3, un chemin relatif au référentiel par ligne (par exemple `help/workfront-fusion/manage-scenarios/explain-errors-with-ai.md`). Incluez les nouveaux articles (ajoutez `(new)` après le chemin d’accès) et les fichiers de table des matières ou d’index que vous avez modifiés. Comme les modifications apportées au document se produisent à l’étape 3, la liste est connue au moment de la création de la tâche. Définissez-la donc dans le même appel de création. Si l’utilisateur vous demande de créer la tâche sans apporter de modifications au document, laissez le champ vide et mettez-le à jour ultérieurement si des modifications au document sont apportées.

`DE:Documentation Branch` (un champ de texte du formulaire Documentation du produit) contient le nom exact de la branche Git sur laquelle portent les modifications du document, par exemple `becky-explain-errors-with-ai`. Utilisez la branche du nom de l’utilisateur ou celle actuellement extraite dans le référentiel que vous avez modifié ; n’inventez pas de nom. Définissez-le dans le même appel de création que les autres champs. Si l’utilisateur vous demande de créer la tâche sans apporter de modifications au document et qu’aucune branche n’existe encore, laissez le champ vide et mettez-le à jour ultérieurement.

Définissez les champs de date de prévisualisation et la date d’achèvement prévue dans le cadre de ce même appel de création - ne les laissez pas en attente d’affichage ultérieur ou d’interrogation. Si l’utilisateur ou l’utilisatrice donne une date différente ultérieurement ou indique que la date n’est pas encore connue, mettez-la à jour en conséquence, mais remplissez-la par défaut à chaque fois.

Les nouvelles tâches utilisent par défaut une contrainte Dès Que Possible de durée 0, en vertu de laquelle `plannedStartDate`/`plannedCompletionDate` sont dérivées du planificateur et une écriture directe vers est silencieusement supprimée (aucune erreur, la date ne change simplement pas). Paramétrer `taskConstraint: "MFO"` avec `constraintDate` est le moyen fiable d’épingler la date d’achèvement prévue à la date citée dans le message Slack. Lire `workfront://knowledge/task/update` avant cette écriture - il s&#39;agit d&#39;un champ de planification/date selon les règles du serveur MCP.

Le champ `description` a une limite stricte de 4 000 caractères. Si le texte complet du message Slack n’est pas adapté :

1. Commencez par créer la tâche avec un `description` court à la place : titre de la fonctionnalité, date de publication prévue, annonce des besoins, résumé d’une ligne de la demande, note que le texte complet de la demande est publié comme premier commentaire sur la tâche et lien du thread Slack.
1. Publiez ensuite le texte intégral et textuel du message Slack (tous les champs du modèle, pas une paraphrase) comme commentaire sur la tâche nouvellement créée, via `comment-stream_create_comment` (`objectCode` `task`, `objectID` l’identifiant de la nouvelle tâche) - cet outil n’a pas de limite de longueur comparable. Incluez `content` (texte brut) et `contentHTML` (structurés avec des en-têtes/listes, et pas seulement des balises `<p>` nues).

Format des notes de mise à jour pour le champ `DE:Release notes`. Commencez toujours par `***FUSION***` sur sa propre ligne, puis une ligne vide, puis le titre. En un coup d’œil, la note est marquée comme appartenant à Fusion (par opposition au Workfront principal) :

```markdown
***FUSION***

## {Feature Title}

{Description of what changed and why it matters, in second person. A sentence or two is enough for a simple change - use multiple paragraphs and/or a bulleted list for anything with several parts or steps, the same way a full weekly release note would.}

For more information, see [{Article title}](/help/workfront-fusion/{path-to-article}.md).
```

Avant l’appel de création, appelez `read_workflow_docs` avec `workfront://tools/create-any-object` - cet appel définit les champs personnalisés et une valeur d’énumération (`DE:Preview Date Known`), qui le requiert selon les règles du serveur MCP.

## Étape 5 : confirmer à l’utilisateur ou à l’utilisatrice

Signalez simplement :

* La branche que vous avez créée (validée localement, non transmise et aucune demande d’extraction ouverte, par étape 2).
* Quel(s) fichier(s) de documents avez-vous modifié et ce que vous avez ajouté.
* Les articles modifiés sont répertoriés dans le champ `Articles to update` de la tâche.
* Nom de branche saisi dans le champ `Documentation Branch` de la tâche.
* Les modifications ne sont pas validées sur la branche, en attente de la révision de l’utilisateur.
* Nom et URL de la tâche.
* Les valeurs de champ exactes que vous définissez, y compris les champs de date de prévisualisation.
* Pour tout ce dont vous n’étiez pas entièrement certain (par exemple, Slack était inatteignable et vous travailliez à partir de texte collé uniquement), l’article du document cible était ambigu ou un détail technique ne figurait pas dans le document source et était marqué au lieu d’être deviné.

## Valeurs connues (issues d’exécutions précédentes)

Confirmez que ces problèmes sont toujours résolus plutôt que de supposer qu’ils sont permanents :

* Le projet « Tâches de documentation du produit - pour les problèmes de développement qui nécessitent une messagerie » est mappé sur l&#39;ID `5e69583f00236b9f767c3e3944100ee4`
* La tâche parent « Becky - Tâches du canal Fusion-Documentation » est mappée à l’ID `6a9b065100003a7554832780c2015e93` (dans le même projet) - résoudre avec `insights_find_id_by_name` (entité `task`) plutôt qu’avec du codage en dur, au cas où il changerait
* Le formulaire personnalisé de documentation du produit (`categoryID`) est `5d7275b9000514604bd969d418725843`
* Champs personnalisés utilisés : `DE:Release notes`, `DE:Preview Date Known`, `DE:Preview Date`, `DE:Articles to update`, `DE:Documentation Branch`
