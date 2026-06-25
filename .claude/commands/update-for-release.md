---
name: update-for-release
description: ""
source-git-commit: 4d32e8aab5b3b8a12dbc23e61f517fc4fd6dc9e5
workflow-type: tm+mt
source-wordcount: '1443'
ht-degree: 0%

---


# Mise à jour pour la version (Workfront)

Cette compétence vous guide tout au long de la mise à jour des articles d’aide de Workfront pour une prochaine version. Le workflow est l’inverse de `remove-preview-highlighting` : le nouveau comportement est ajouté aux articles, marqué comme Aperçu, et (plus tard, en disponibilité générale) nettoyé par cette autre compétence.

## Portée

Appliquer lorsque **tous** sont vrais :

1. L’utilisateur met à jour les articles d’aide de Workfront pour une fonctionnalité qui est en cours d’expédition (généralement Aperçu en premier).
2. La modification introduit un nouveau comportement ou une nouvelle interface utilisateur, et non un nettoyage GA. Pour le nettoyage de la disponibilité générale, utilisez plutôt **remove-preview-highlighting**.
3. Le fichier n’est **pas** une note de mise à jour. Pour les notes de mise à jour, utilisez plutôt **release-notes-formatter**.
4. L’utilisateur a indiqué le contexte de la fonctionnalité : au minimum une brève description et une capture d’écran ; idéalement, une URL de PRD (wiki Adobe).

Si la portée n’est pas claire, confirmez avant de commencer.

## Workflow requis (humain dans la boucle)

Ne modifiez **pas** référentiel en bloc. Déplacer un article à la fois. Après chaque article, demandez s’il faut passer au suivant.

### &#x200B;1. Collecter le contexte des fonctionnalités

Confirmez avec l’utilisateur :

- **Changements** (résumé en 1 à 2 phrases du nouveau comportement ou de la nouvelle interface utilisateur).
- **Capture(s) d’écran** la nouvelle interface utilisateur. Si indiqué, enregistrez sous le dossier `assets/` de l’article cible avec un nom de fichier descriptif en majuscules (par exemple, `add-custom-message.png`). Si elle n’est pas fournie, demandez s’il faut en attendre une ou procéder à une référence d’espace réservé.
- **URL PRD** (wiki Adobe), si disponible. Récupérez-le à l’aide de l’outil `user-Adobe Wiki Confluence` MCP `get_wiki_content`. Lisez-la pour trouver les comportements que l’utilisateur ne peut pas voir dans l’interface utilisateur : effets secondaires des notifications, ce qui se passe lorsque quelque chose est modifié ou ajouté ultérieurement, limites de caractères non affichées, autorisations, etc.
- **Disponibilité** : aperçu uniquement, aperçu + version rapide ou GA déjà disponible. Cela entraîne le choix du fragment de code à l’étape 3.
- **Exclusions explicites** : tout article que l’utilisateur souhaite ignorer (par exemple, « cette fonctionnalité n’est pas dans les modèles »).

### &#x200B;2. Articles affectés par l&#39;inventaire

Recherchez le référentiel avec les mots-clés de la zone de fonctionnalité (par exemple, `approval workflow`, `document approval`, le libellé du champ spécifique). Créer une liste de candidats :

- Articles pratiques dans l’arborescence de `help/quicksilver/.../` correspondante.
- Articles de présentation et FAQ qui mentionnent la zone de fonctionnalité.
- **Exclure** `product-announcements/` (les notes de mise à jour utilisent une compétence différente).
- **Exclure** pages de la table des matières/de l’index dont la seule mention est le texte du lien vers un autre article.
- **Exclure** articles que l’utilisateur a dit d’ignorer à l’étape 1.

Présentez la liste des candidats à l’utilisateur. Demandez lequel mettre à jour et lequel ignorer. `help/quicksilver/TOC.md` de référence croisée si un article frère semble manquant.

### &#x200B;3. Sélectionnez le fragment de code de prévisualisation

Lisez `help/_includes/snippets.md` et choisissez par disponibilité :

| Disponibilité | Extrait de code |
| --- | --- |
| Aperçu uniquement — le contenu mis en surbrillance est nouveau dans un article autrement généralement disponible | `{{highlighted-preview}}` |
| Aperçu uniquement — l&#39;article entier est nouveau | `{{highlighted-preview-article-level}}` |
| Aperçu + clients de version rapide, en général | `{{preview-fast-release-general}}` |

Si un fragment de code spécifique à une version existe déjà pour le trimestre en cours, préférez-le à celui du trimestre générique. Confirmez le choix avec l’utilisateur avant de postuler.

### &#x200B;4. Par article — afficher d&#39;abord, modifier après OK

Pour chaque article de la liste confirmée par l’utilisateur :

1. **Lire le fichier.**

2. **Déterminez le modèle de mise en surbrillance.** Demandez à l’utilisateur ou à l’utilisatrice qui correspond à cet article (la réponse peut différer selon l’article) :

   - **Duplication par section** : ajoutez des `in Production` à l’en-tête de section existant. Ajoutez une nouvelle section avec `in Preview` ajouté, encapsulé dans des `<div class="preview"> ... </div>`. À utiliser lorsque le nouveau comportement modifie la procédure de manière significative (étapes supplémentaires, nouvelle image, nouvelles lignes de tableau ou libellé différent). Typique pour les procédures pratiques.
   - **Habillage par ligne** : ajoutez la ou les nouvelles phrases en ligne à l’intérieur de la section existante, enveloppée dans du `<span class="preview"> ... </span>`. À utiliser lorsque l’ajout est une phrase ou deux qui s’adapte naturellement à un paragraphe, une cellule de tableau ou une réponse à une question fréquente existants.
   - **Mixte** : certaines sections du même article utilisent la duplication par section, d’autres utilisent l’encapsulation par ligne. Faites apparaître cette option lorsque l’article comporte à la fois des sections de procédure et des sections de style FAQ.

3. **Placez le fragment de code** sur sa propre ligne immédiatement après le titre H1, avec une ligne vide au-dessus et en dessous. Le fragment de code se trouve **avant** le paragraphe d’introduction.

4. **Regrouper les nouveaux détails dans « toujours inclure » plutôt que dans « à réviser ».** C&#39;est l&#39;étape la plus importante.

   - **Toujours inclure** (appliquer automatiquement, pas d’invite) : comportements invisibles que l’utilisateur ne peut pas observer lors de son interaction avec l’interface utilisateur. Exemples :
      - Effets secondaires (par exemple, « la modification de ce paramètre renvoie l’e-mail à tous les participants »)
      - Comportement sur d’autres objets ou événements ultérieurs
      - Conditions préalables et autorisations
      - Limites non affichées dans l’interface utilisateur
      - Tout ce que l’utilisateur peut uniquement apprendre du PRD, des documents ou de l’équipe produit
   - **À réviser** (présenté à l’utilisateur avec `AskQuestion` à sélection multiple) : faits que l’utilisateur ou l’utilisatrice peut voir à l’écran lors de l’utilisation de la fonctionnalité. Exemples :
      - Un compteur de caractères que l’interface utilisateur affiche déjà (par exemple, `0 / 500`).
      - État développé/réduit par défaut d’un champ
      - État sélectionné par défaut d’une case à cocher visible
      - Libellés du bouton en regard du champ
      - Messages de validation qui apparaissent en ligne

   Pour chaque élément « à réviser », fournissez une justification en une seule phrase (« Aide les débutants à planifier un message plus long », « Aide les utilisateurs qui ne le voient pas lors des étapes suivantes à savoir comment le développer »). Inclure uniquement les articles sélectionnés par l’utilisateur. Le principe par défaut est le suivant : « Si l’utilisateur ou l’utilisatrice peut le voir à l’écran pendant qu’il ou elle effectue la tâche, ne le redémarrez pas », mais l’utilisateur ou l’utilisatrice reçoit l’appel final.

5. **Proposer des modifications.** Affichez les extraits avant/après (ou une description de style diff ciblée) de l’article, couvrant : le placement des fragments de code, les renommes d’en-tête, le nouveau contenu de l’aperçu et son emplacement, la référence de la capture d’écran et tout habillage de `class="preview"` intégré.

6. **Attendez une approbation explicite** (« ok », « apply », « yes ») avant d&#39;écrire le fichier.

7. **Valider.** Après avoir écrit, exécutez `ReadLints` sur le fichier et signalez les problèmes éventuels. Relisez la section modifiée pour confirmer la structure.

8. **Différer les modifications de niveau prose** à la compétence **qualité-écriture**. Ne reproduisez pas de voix, de majuscules, de règles audacieuses ou de modèles de liens ici — lisez `~/.cursor/skills/writing-quality/SKILL.md` si une passe en prose est demandée.

### &#x200B;5. Après chaque article

Demandez s’il faut passer à l’article suivant, arrêter, ignorer ou revoir l’article actuel.

### &#x200B;6. Fin de session — copier/coller la note de mise à jour

Lorsque l’utilisateur termine la session (dit « terminé », « c’est tout », « arrête » ou refuse de passer à l’article suivant), demandez :

> « Vous souhaitez copier/coller une entrée de note de mise à jour pour la page d’amélioration ? »

Si oui, générez un brouillon à l’aide du contexte de la fonctionnalité de l’étape 1 et de l’article d’aide principal mis à jour au cours de cette session. **Ne l’écrivez dans aucun fichier** — fournissez-le uniquement sous forme de texte à copier/coller.

Mettez en forme l’entrée pour qu’elle corresponde à la structure de page de la zone de produit à partir de la compétence **formateur de notes de mise à jour** :

```markdown
## {Feature name}

>[!NOTE]
>
>Preview: {date or TBD}
>Production fast release: {date or TBD}
>Production for everyone: {date or TBD}

{1–3 sentences describing what changed and why it helps users. Lead with the benefit, not the UI action.}

For more information, see [{Primary article title}](/help/quicksilver/{path-to-article}.md).
```

Règles :

- Utilisez `TBD` pour toute date non encore connue ; demandez à l’utilisateur s’il possède les dates.
- Le nom de la fonction est une casse de phrase (mettez uniquement en majuscules le premier mot et les noms propres).
- La description doit se concentrer sur ce que les utilisateurs peuvent désormais faire, et non les détails d’implémentation.
- Lien vers l’article pratique le plus spécifique mis à jour, et non vers une page d’aperçu.
- N’incluez pas de bloc de date `>[!NOTE]` si toutes les dates sont inconnues et que l’utilisateur ne souhaite pas d’espaces réservés. Omettez-le et notez qu’il doit être ajouté ultérieurement.

## Règles de contenu

### Titres

- Ajoutez exactement **`in Production`** aux en-têtes de section existants qui restent comme référence côté production.
- Ajoutez exactement **`in Preview`** aux nouveaux en-têtes de section.
- Conserver le reste de l&#39;en-tête dans la casse de phrase (par `writing-quality`).

### Aperçu des wrappers

- **Niveau de section** : encapsuler en `<div class="preview"> ... </div>`. Placez les balises d’ouverture et de fermeture sur leurs propres lignes, avec une ligne vide au-dessus et en dessous de chaque balise, de sorte que les en-têtes markdown et les listes à l’intérieur s’affichent toujours.
- **En ligne (niveau de phrase)** : insérez des `<span class="preview"> ... </span>` dans le paragraphe existant, la cellule de tableau ou la réponse aux questions fréquentes.
- N&#39;imbriquez jamais un `<span class="preview">` dans un `<div class="preview">`.

### Placement du fragment de code

- La ligne de fragment suit immédiatement le H1, avec une ligne vide au-dessus et en dessous.
- Le fragment se trouve **avant** le paragraphe d’introduction, la légende `>[!IMPORTANT]` et tout bloc d’exigences d’accès.
- Un extrait par article.

### Captures d’écran

- Enregistrez de nouvelles captures d’écran dans le dossier `assets/` de l’article avec un nom de fichier descriptif en majuscules.
- Référencez la nouvelle capture d’écran à partir de la nouvelle section dans l’aperçu. Si la capture d’écran d’une section en production ne reflète plus la fonctionnalité avec précision, laissez-la en place ; elle représente toujours le comportement de production jusqu’à la disponibilité générale.
- Ne fabriquez pas de noms de fichiers de capture d’écran. Si aucune capture d’écran n’a encore été fournie, demandez à l’utilisateur.

### Notes et conseils

- Maximum une `>[!NOTE]` (ou `>[!TIP]`, `>[!IMPORTANT]`, `>[!WARNING]`) par section. Si la section existante comporte déjà une note, combinez les nouveaux contenus associés dans la même note sous la forme d’une liste à puces plutôt que de les empiler.

### Que ne pas faire

- Ne modifiez pas les articles sous `product-announcements/`.
- Ne pas modifier en masse ; un article à la fois, avec une approbation explicite à chaque fois.
- N’incluez pas de faits observables dans l’interface utilisateur sans en avoir préalablement fait état à l’utilisateur.
- Ne modifiez pas le contenu `<!-- ... -->` commentaires HTML, sauf si l’utilisateur ou l’utilisatrice le demande explicitement.
- Ne modifiez pas les champs de front-issue `author:` ou non associés.

## Contrôles qualité avant présentation des modifications

- Le fragment de code apparaît une fois, sur sa propre ligne, après le H1, avec des lignes vides au-dessus et en dessous.
- Les en-têtes de section existants se terminent par `in Production`.
- Les nouveaux en-têtes de section se terminent par `in Preview` et la section se trouve dans `<div class="preview">`.
- Les ajouts intégrés se trouvent à l’intérieur des `<span class="preview">`.
- `ReadLints` est propre sur le fichier modifié.
- L’article se lit correctement dans les deux états (avec le contenu de l’aperçu affiché et masqué).

## Références

- Style de documentation de Workfront : consultez la compétence **qualité-écriture** sur `~/.cursor/skills/writing-quality/SKILL.md`.
- Catalogue de fragments de code : `help/_includes/snippets.md` dans le référentiel de documents.
- Nettoyage GA (workflow inverse) : consultez la compétence **remove-preview-highlighting** à l’`.cursor/skills/remove-preview-highlighting/SKILL.md`.
- Adobe Wiki MCP pour PRDs : `user-Adobe Wiki Confluence` de serveur, `get_wiki_content` d&#39;outils.
