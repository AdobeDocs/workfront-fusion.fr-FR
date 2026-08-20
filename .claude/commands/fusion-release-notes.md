---
name: fusion-release-notes
description: Créez une page de notes de mise à jour hebdomadaires de Workfront Fusion et connectez-la à la page d’aperçu de l’activité de version et à la table des matières. À utiliser lorsque l’utilisateur souhaite écrire, ajouter ou rédiger une nouvelle note de mise à jour de Fusion ou une page de version hebdomadaire, ou lorsqu’il demande de documenter les nouvelles fonctionnalités de Fusion pour une version. N’utilisez pas pour les notes de mise à jour de Workfront (Quicksilver) dans les annonces de produits/versions de produits. Utilisez le formateur de notes de mise à jour pour ces notes.
source-git-commit: 94492dbd382eee2f4e66e53d53a441ca82492bfb
workflow-type: tm+mt
source-wordcount: '1042'
ht-degree: 0%

---


# Notes de mise à jour de Fusion

Crée une page hebdomadaire de notes de mise à jour d’Adobe Workfront **Fusion** dans `help/workfront-fusion/fusion-product-releases/` et la lie à partir des deux endroits qui la rendent détectable : la page d’aperçu de l’activité de publication et la `help/workfront-fusion/TOC.md`.

Il s’agit d’un système différent des notes de mise à jour de Quicksilver (core Workfront) gérées par la compétence `release-notes-formatter` :

| | Notes de mise à jour de Fusion (cette compétence) | Notes de mise à jour de Quicksilver (`release-notes-formatter`) |
|---|---|---|
| Cadence | Hebdomadaire | Tous les trimestres |
| Répertoire | `help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/` | `help/quicksilver/product-announcements/product-releases/` |
| Légende de date par fonction | Non — le titre de la page porte la semaine | Oui — `>[!NOTE]` bloc par fonction |
| Page d’index | `fusion-release-activity.md` (par année/mois) | `{YY}-q{N}-release-overview.md` (par trimestre) |

## Étape 1 : rassembler les fonctionnalités

Demandez à l&#39;utilisateur (s&#39;il n&#39;a pas déjà été fourni) la liste des fonctionnalités/modifications apportées au document pour la semaine et pour chacune d&#39;elles :

- Titre abrégé d&#39;un long métrage
- Description claire de ce qui a changé et des raisons de son importance
- Le ou les articles d’aide auxquels ils renvoient (vérifiez que le chemin existe, n’essayez pas de deviner).
- Si elle requiert une action de l’utilisateur ou de l’administrateur ou s’il s’agit d’une obsolescence (appelle une légende `>[!IMPORTANT]`)
- **Qu’il s’agisse d’un nouveau lancement de connecteur** (un tout nouveau connecteur/application devient disponible, et pas seulement de nouveaux modules ajoutés à un connecteur existant). Si oui, cela déclenche **Étape 7** — ne passez pas à côté de la question sur une redirection juste parce que la note de mise à jour elle-même est terminée.

## Étape 2 : déterminer le nom et la date du fichier

- Recherchez le lundi (ou la date de publication) de la semaine en cours de documentation et confirmez-le auprès de l’utilisateur ou de l’utilisatrice si vous avez des doutes.
- Chemin du fichier : `help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/fusion-{YYYY}-{M}-{D}.md`
  - `{M}` et `{D}` n’ont **pas de zéros au début** : `fusion-2026-7-20.md`, pas `fusion-2026-07-20.md`.
  - Si le dossier Année n’existe pas encore, créez-le.
- Vérifiez si une page existe déjà pour cette semaine avant d’en créer une nouvelle.

## Étape 3 : écrire la page

### Matière Première

```yaml
---
title: Workfront Fusion release activity Week of {Month} {Day}, {Year}
description: Workfront Fusion release activity Week of {Month} {Day}, {Year}
author: {Author}
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
---
```

Règles :
- `title` et `description` sont identiques.
- Incluez toujours la virgule dans la date (`July 20, 2026`), même si certaines pages plus anciennes l’omettent — ne copiez pas cette incohérence.
- **Utilisez `hidefromtoc: true` pour chaque nouvelle page. N’ajoutez pas de `exl-id` ni de `TQID`.** Celles-ci sont attribuées ultérieurement une fois la page publiée. Il est erroné d’en inventer une. (Les pages à partir de la mi-2026 suivent toutes ce modèle ; consultez `_fusion-release-notes-reference.md` si vous devez vérifier un exemple.)

### Corps

```markdown
# Workfront Fusion release activity: Week of {Month} {Day}, {Year}

This page describes all enhancements made in Adobe Workfront Fusion the week of {Month} {Day}, {Year}.

For a list of all recent changes, see [Adobe Workfront Fusion release activity](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

For a list of recent bug fixes in Workfront Fusion, see the [Workfront Maintenance Updates](https://experienceleague.adobe.com/en/docs/workfront-known-issues/releases/current-updates) page and check for any updates labeled Workfront Fusion Maintenance Update.

## {Feature title}

Feature description paragraph(s) — what changed, why, and how it affects existing scenarios/configurations if relevant.

For more information, see [{Help article title}](/help/workfront-fusion/{path-to-article}.md).

## {Next feature title}

...
```

Notes :
- Un H2 par fonctionnalité, dans l’ordre donné par l’utilisateur (aucune nouvelle commande forcée en premier dans la page ; une seule semaine).
- Aucune légende de date de `>[!NOTE]` par fonction : le titre de la page porte déjà la date.
- Si une fonction nécessite une action ou constitue une modification/obsolescence avec rupture, ajoutez une légende `>[!IMPORTANT]` directement sous le H2, avant la description :

  ```markdown
  ## {Feature title}
  
  >[!IMPORTANT]
  >
  >**Action Required: {short summary of what the user must do and by when}**
  >
  >{Details of the requirement.}
  
  {Regular description paragraph(s).}
  ```

- Chaque fonctionnalité doit se terminer par un « Pour plus d’informations, voir [...] » lien vers l’article d’aide approprié. Vérifiez que la cible du lien existe dans le référentiel.

## Étape 4 : ajouter la page à l’index d’aperçu

Modifier le `help/workfront-fusion/fusion-product-releases/fusion-release-activity.md` :

- Recherchez la section `## Fusion releases in {current year}` (elle n’est **pas** encapsulée dans un bloc `+++` réductible ; seules les années précédentes sont réduites).
- Recherchez ou créez l’en-tête `### {Month} {Year}` pour le mois de la version, directement sous l’en-tête Année.
  - Si l’en-tête du mois n’existe pas encore, ajoutez-le **ci-dessus** le mois précédent (le mois le plus récent en premier).
- Ajoutez la nouvelle page en tant que **première** puce sous cet en-tête de mois (semaine la plus récente en premier) :

  ```markdown
  * [Workfront Fusion release activity: Week of {Month} {Day}, {Year}](/help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/fusion-{YYYY}-{M}-{D}.md)
  ```

- S’il s’agit de la première version d’une nouvelle année, ajoutez un nouvel en-tête `## Fusion releases in {YYYY}` au-dessus de l’en-tête de l’année précédente, et enveloppez la section *année précédente* dans un bloc `+++ **Click to open**`/`+++` réductible si ce n’est pas déjà fait (seule l’année en cours reste développée).

## Étape 5 : ajouter la page à la table des matières

Modifier le `help/workfront-fusion/TOC.md` :

- Recherchez les `* Fusion releases - {YYYY} {#fusion-releases-{YYYY}}` de l’année en cours, imbriquées sous `* Fusion release activity {#fusion-release-activity}`.
- Ajoutez la nouvelle page en tant que **première** entrée sous cet en-tête (la plus récente en premier), correspondant au retrait existant (8 espaces) :

  ```markdown
        * [Workfront Fusion release activity: Week of {Month} {Day}, {Year}](/help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/fusion-{YYYY}-{M}-{D}.md)
  ```

- Si le titre de l&#39;année en cours n&#39;existe pas encore, ajoutez `* Fusion releases - {YYYY} {#fusion-releases-{YYYY}}` au-dessus du titre de l&#39;année précédente.
- **N’ajoutez pas** le préfixe `{hide-from-toc}` aux nouvelles entrées ; il n’est utilisé que pour les entrées plus anciennes une fois qu’elles ne sont plus visibles (voir Incohérences connues ci-dessous).

### Incohérences connues à surveiller (ne pas répliquer)

- Plusieurs entrées de la table des matières de début 2026 sont imbriquées par erreur sous l’en-tête `Fusion releases - 2025` , même si les pages elles-mêmes sont des versions de 2026. Lors de l’ajout d’une nouvelle entrée, vérifiez toujours qu’elle se trouve sous la rubrique correspondant **à son année propre**, et non pas là où se trouve l’entrée précédente.
- Certains titres de pages plus anciens/H1 omettent la virgule avant l’année (`July 13 2026` au lieu de `July 13, 2026`). Utilisez toujours la virgule dans les nouvelles pages.

## Étape 7 : Nouveaux lancements de connecteur — demandez des informations sur une redirection (ne pas ignorer)

**Cette étape s’applique chaque fois que l’étape 1 a identifié un nouveau lancement de connecteur.** Il est facile de considérer la note de mise à jour comme « terminé » après l’étape 5 et d’oublier cela : traitez une nouvelle fonctionnalité de connecteur comme incomplète jusqu’à ce que cette étape soit traitée d’une manière ou d’une autre.

Demandez à l’utilisateur : *« Voulez-vous configurer une redirection pour le nouvel article du connecteur ? »*

- Si **non**, notez-le et passez à autre chose. Rien d&#39;autre à faire.
- Si **oui**, regroupez les éléments suivants :
  - Le **chemin source** (doit commencer par `/en`, sans espaces)
  - Le **destination** — un chemin relatif commençant par `/en`, ou une URL `https` complète (sans espaces)
- Ajoutez la ligne au référentiel de `Adobe-Enterprise-Docs/redirects` frère, sous `redirects/`, un fichier par environnement (`redirects-dev.csv`, `redirects-stage.csv`, `redirects-prod.csv`).
- Règles de ligne (à partir du fichier README de ce référentiel) :
  - Pas de doublons `source`, et pas de doublons `source`/`destination`.
  - La redirection ne doit pas entraîner de boucle de redirection.
- **Cette compétence ajoute uniquement la ligne CSV une fois que l’utilisateur l’a confirmée.** L’augmentation de la requête persistante dans le référentiel `redirects` est une étape distincte que cette compétence ne permet pas d’effectuer : indiquez à l’utilisateur qu’une requête persistante doit toujours être ouverte et fusionnée à cet endroit avant que la redirection ne soit activée (~5 minutes après la fusion pour les redirections 1:1).

## Étape 8 : Liste de contrôle finale

- [ ] Fichier créé au bon chemin d’accès sans zéros au début de la date
- [ ] FrontMATTER utilise du `hidefromtoc: true`, pas de `exl-id`/`TQID` inventé
- [ ] correspondance titre/description, la date comprend une virgule
- [ ] Chaque fonction comporte une description et un lien vérifié « Pour plus d’informations »
- [ ] fonctionnalités Action requise/obsolescence ont une légende `>[!IMPORTANT]`
- [ ] Nouvelle page ajoutée comme entrée la plus récente en `fusion-release-activity.md`, sous l’année/le mois approprié
- [ ] Nouvelle page ajoutée comme entrée la plus récente en `TOC.md`, sous l’en-tête année correcte
- [ ] de nouveaux en-têtes année/mois créés si nécessaire, avec l’année précédente réduite en `fusion-release-activity.md`
- [ ] **Si une fonctionnalité était un nouveau lancement de connecteur : a posé une question sur une redirection (étape 7), et en a configuré une ou a explicitement refusé**

## Ressources supplémentaires

Pour obtenir des exemples complets (une semaine polyvalente simple et une semaine avec une légende `>[!IMPORTANT]` nécessitant une action), consultez la `.claude/commands/_fusion-release-notes-reference.md`.
