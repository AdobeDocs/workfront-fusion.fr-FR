---
name: remove-preview-highlighting
description: ""
source-git-commit: 4d32e8aab5b3b8a12dbc23e61f517fc4fd6dc9e5
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 0%

---


# Supprimer la mise en surbrillance de l’aperçu (Workfront)

## Portée

Appliquer uniquement lorsque **tous** sont vrais :

1. L’utilisateur a appelé ce workflow (par exemple, dit **« supprimer la mise en surbrillance de l’aperçu »** ou clairement dans le même but).
2. Le chemin d’accès au fichier Markdown ne contient **pas** de **`product-announcements`** (excluez l’arborescence complète des dossiers, par exemple les notes de mise à jour, les versions bêta, les annonces sous `help/quicksilver/product-announcements/`).
3. Le fichier Markdown est **non** répertorié sous **[Chemins exclus](#excluded-paths)** ci-dessous.
4. Le fichier Markdown apparaît dans `git log` comme ayant un contenu d’aperçu **ajouté ou modifié** par l’utilisateur Git actuel dans la période spécifiée par l’utilisateur (voir l’étape d’inventaire).
5. L’article contient **au moins l’un** :
   - Aperçu-environnement **langage dans des paragraphes de corps en prose ou de fragments de code** (modèles standard : « informations mises en évidence », « environnement d’aperçu », « pas encore disponible pour tous », notes de mise à jour rapides)—**pas** une correspondance provenant de **texte du lien** sur une page de table des matières/d’index (voir ci-dessous) ; ou
   - tout élément HTML avec **`class="preview"`** (par exemple, `<span class="preview">`, `<div class="preview">`) ; ou
   - Extrait de code d’aperçu **variable** tel que **`{{highlighted-preview}}`** ou **`{{highlighted-preview-article-level}}`**.

Si la portée n’est pas claire, confirmez avant de modifier.

**Table des matières / pages d’index — toujours ignorer ce cas :** **Jamais** placez un fichier dans l’inventaire lorsque le **seul** libellé lié à l’aperçu est **à l’intérieur** du texte d’affichage d’un lien Markdown pointant vers **un autre** article (par exemple *Envoyez un rapport dans l’environnement de sandbox de prévisualisation*) et **le fichier a** no ****, `class="preview"`no **des variables de fragment de code et** no **en** prose en dehors de links ****. Il ne s’agit pas d’une mise en surbrillance de la prévisualisation sur cette page ; il s’agit uniquement d’une mention Table des matières. S’applique à n’importe quel index/table des matières et non à un seul fichier.

### Chemins exclus

Ne les ajoutez jamais à l’inventaire ou ne les modifiez jamais dans ce workflow, sauf si l’utilisateur ou l’utilisatrice les remplace explicitement :

- `help/quicksilver/documents/adobe-workfront-for-experience-manager-assets-essentials/send-to-aem.md` : les limites de prévisualisation et de production parallèles nécessitent une décision éditoriale délibérée en dehors de l’automatisation.
- `help/quicksilver/reports-and-dashboards/reports/creating-and-managing-reports/create-manage-reports.md` — table des matières des rapports ; seul le signal « preview » est le lien vers l’article Prévisualiser la diffusion de Sandbox .

## Workflow requis (humain dans la boucle)

Ne modifiez **pas** référentiel en bloc sans approbation.

1. **Inventaire**\
   a. **Demandez à l’utilisateur quelle version trimestrielle** il supprime la mise en surbrillance de l’aperçu pour (par exemple, « T3 2026 » ou « 2026.07 »).\
   b. **Récupérez le calendrier des versions** à partir de `https://wiki.corp.adobe.com/spaces/AWF/pages/3631617814/2026+Monthly+Release+Calendar` à l’aide de l’outil MCP adobe-wiki. Rechercher :
   - La **Date de publication de production** de la version trimestrielle **précédente** → `--since`.
   - La **Date de publication de production** de la `--until` de → trimestrielle **cible**.
   - Les versions trimestrielles sont identifiées par la colonne « Nom de la version trimestrielle » (par exemple, 2026.01, 2026.04, 2026.07, 2026.10).
   - **Si la date actuelle se situe au 4e trimestre (octobre à décembre) :** après avoir récupéré le calendrier de l’année en cours, demandez à l’utilisateur de fournir l’URL du calendrier des versions de l’année suivante, puis récupérez-la également afin que toutes les dates de production trimestrielles nécessaires soient disponibles.
c. Déterminez l’utilisateur Git actuel, puis exécutez les opérations suivantes en utilisant les dates de publication de production de l’étape b :

   ```bash
   GIT_USER=$(git config user.name)
   git log --since="YYYY-MM-DD" --until="YYYY-MM-DD" \
     --author="$GIT_USER" --name-only --pretty=format: \
     -- "help/quicksilver/**/*.md" | sort -u | grep -v '^$'
   ```

   d. À partir de ces résultats, **filtrez les fichiers où les validations de l’utilisateur actuel dans la période ont en fait ajouté ou modifié le contenu de l’aperçu**. Pour chaque fichier candidat, vérifiez si les validations de l’utilisateur ont introduit des marqueurs d’aperçu :

   ```bash
   git log --since="YYYY-MM-DD" --until="YYYY-MM-DD" \
     --author="$GIT_USER" -p -- "<file>" | \
   grep -q '^\+.*class="preview"\|^\+.*{{highlighted-preview\|^\+.*highlighted information\|^\+.*not yet generally available'
   ```

   Inclure le fichier uniquement si ce grep correspond (code de sortie 0). Cela permet d’éviter les faux positifs lorsqu’un utilisateur a apporté une modification non liée à un fichier dont la mise en surbrillance de l’aperçu a été ajoutée par une autre personne.

   e. **Omettre** tout chemin sous **`product-announcements`**, tout chemin **[Exclu](#excluded-paths)** et toute page **Table des matières/index** selon la règle de table des matières ci-dessus.\
   f. Présentez la liste triée résultante. Si l’utilisateur indique qu’un fichier répertorié ne dispose pas de mise en surbrillance de l’aperçu, supprimez-le de l’exécution et resserrez les critères plutôt que de forcer les modifications.

2. **Début**\
   Demandez-lui s’il faut commencer par le **premier** article de la liste (ou par un chemin d’accès aux noms d’utilisateur).

3. **Par article — afficher d&#39;abord, modifier après OK**
   - Lire le fichier.
   - Proposez des modifications de manière claire : **avant/après les extraits** ou une description de style diff ciblée de ce qui va changer.
   - **Attendez** une approbation explicite (par exemple, « ok », « apply », « yes ») avant d&#39;écrire le fichier.

4. **Après chaque fichier**\
   Demandez si vous devez passer à l’article **suivant** (ou arrêter/ignorer).

## Règles de contenu (GA : la prévisualisation du contenu devient le document)

Lors de la suppression de la mise en surbrillance de l’aperçu pour **disponibilité générale**, l’objectif est le suivant : **conserver le comportement qui a été documenté pour l’aperçu**, déposer les branches **obsolètes « en production » / ancien processus**, puis **supprimer les libellés et les wrappers de prévisualisation uniquement** afin que la rubrique se lise comme étant à jour pour tous les clients.

### Étapes parallèles

- Si l’article comporte une étape (ou un élément numéroté) **encadrée comme « en production »** (ou l’équivalent : production actuelle / comportement de production existant) **et** une étape **parallèle** encadrée comme **»dans l’aperçu »** (ou l’environnement de prévisualisation) :
   - **Supprimez** l’étape en production (l’ancien chemin).
   - **Conservez** la **substance** de l’étape dans la prévisualisation, mais **reformulez** afin qu’elle ne soit **pas** spécifique à la prévisualisation (supprimez « dans la prévisualisation », « Aperçu de l’environnement », etc.). Ajustez la numérotation pour que la liste reste cohérente.

Si la structure est ambiguë (pas de parallèle clair), **arrêtez** et affichez les deux candidats ; demandez à l’utilisateur quel bloc conserver.

### Sections parallèles

- Si une **section** (en-tête + corps) porte sur **dans l’environnement de production »** et qu’il existe une **section parallèle** **sur « dans l’environnement de prévisualisation »** :
   - **Supprimez** la section environnement de production (le contenu remplacé).
   - **Remplacez** par le contenu de la section d’aperçu, puis **supprimez** le libellé preview-environment et les wrappers **`class="preview"`** afin que la section soit neutre (prête pour la mise à disposition générale).

### Fragments de code et avis dans la partie supérieure de l’article

- Supprimez **blocs standard de prévisualisation uniquement** (plages/div ou paragraphes qui expliquent uniquement que le contenu mis en surbrillance est en prévisualisation uniquement, version rapide, sandbox, etc.). une fois la fonctionnalité mise à disposition générale.
- Supprimez les liens ou les phrases dont l’objectif **uniquement** est la disponibilité de l’aperçu, sauf si l’utilisateur ou l’utilisatrice indique de conserver une autre notification.

### `class="preview"` HTML

- Supprimez les **ouverture et fermeture des balises** pour les éléments qui utilisent **`class="preview"`**, **conservation du contenu interne** (markdown/HTML à l’intérieur de la balise).
- Gérez les balises **`<span class="preview">`** et **`<div class="preview">`**, ainsi que le même modèle sur d’autres balises (par exemple, **`<p class="preview">`**, **`<li class="preview">`**) lorsqu’elles apparaissent dans le corps du contenu **visible** (non commenté).
- Conserver la structure des listes/tableaux ; corriger les listes rompues ou les espaces blancs errants après l’encapsulation.

### Sections commentées (commentaires d’HTML)

- **Ne supprimez** ne dépliez ou ne **modifiez** aucun contenu dans **`<!-- … -->`** commentaires HTML **à moins que l’utilisateur n’indique explicitement** que faire (par exemple, supprimer l’ensemble du commentaire, supprimer les classes d’aperçu dans le commentaire uniquement, supprimer les commentaires pour la disponibilité générale).
- Si le contenu ou la **`class="preview"`** liés à la prévisualisation apparaît **uniquement** dans les commentaires, **appelez-le** lors de la révision de l’article : dites ce qui se trouve dans le commentaire et **demandez** que faire. **Par défaut : ne modifiez pas les sections commentées.**

### Que ne pas faire

- N’exécutez pas ce workflow sur les chemins d’accès sous **`product-announcements`** (notes de mise à jour et connexes), car l’inventaire doit les exclure.
- N’inventoriez ou ne modifiez pas les chemins répertoriés sous **[Chemins exclus](#excluded-paths)**, sauf si l’utilisateur demande explicitement à en inclure un.
- **Ne supprimez pas** ne modifiez pas automatiquement les blocs **`<!-- … -->`)** commentés ; suivez **sections commentées** ci-dessus.
- Ne supprimez pas le « Prévisualisation » lorsqu’il n’est **pas** concernant ce modèle de disponibilité des fonctionnalités (par exemple, [Prévisualisation de l’environnement Sandbox](·) en tant que **nom du produit** dans un contexte non lié) ; faites preuve de jugement et demandez si vous n’êtes pas sûr.
- Ne modifiez pas `author:` ou le frontMATTER sans rapport à moins que l&#39;utilisateur ne le demande.
- N’ignorez pas l’étape **afficher → approuver**.

## Contrôles qualité avant présentation des modifications

- Aucune **`class="preview"`** restante sur la portée convenue du changement.
- Aucun en-tête en double orphelin ni numéro d’étape rompu.
- L’introduction se lit correctement **sans** en contradiction avec la disponibilité générale (pas de prévisualisation uniquement pour les fonctionnalités livrées).

## Références

- Respectez les conventions de style de documentation et de référentiel **[Workfront ](https://experienceleague.adobe.com/?lang=fr)** (règles de validation/RP si l’utilisateur effectue une validation).
