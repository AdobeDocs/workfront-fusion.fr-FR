---
name: document-fusion-module
description: Documentez un nouveau module de connecteur Adobe Workfront Fusion en l’ajoutant à l’article de connecteur approprié sous help/workfront-fusion/references/apps-and-modules/. À utiliser lorsque l’utilisateur demande d’ajouter, de documenter ou de décrire un nouveau module Fusion ou lorsqu’il fournit des captures d’écran d’un panneau de configuration du module Fusion et souhaite que l’article correspondant soit mis à jour.
source-git-commit: 976db79104d226a16a35dc04e8c8cb111eb745db
workflow-type: tm+mt
source-wordcount: '1609'
ht-degree: 0%

---


# Documentation d’un module connecteur Fusion

Utilisez cette compétence pour ajouter un ou plusieurs nouveaux modules à un article du connecteur Workfront Fusion (par exemple, `adobe-firefly-modules.md`, `adobe-photoshop-modules.md`, `azure-dev-ops.md`).

## Entrées requises (par module)

Avant de remplir les champs d’un module, l’utilisateur **doit** fournit tous les éléments suivants. S’il en manque, arrêtez-vous et demandez-le avant de continuer.

1. **Nom du module** — exactement comme il apparaît dans l’interface utilisateur de Fusion (par exemple, `Generate adaptive composite`).
2. **Chemin d’accès à l’article du connecteur** — l’agent le localise et le confirme à l’utilisateur (voir Phase 1).
3. **URL de l’API** pour l’opération d’API sous-jacente. Cela est nécessaire afin que l’objectif de chaque champ puisse être référencé de manière croisée par rapport à la spécification de l’API.
4. **Capture d’écran du panneau de configuration du module en mode standard** (`Show advanced settings` **non coché**).
5. **Capture d’écran du panneau de configuration du module en mode avancé** (`Show advanced settings` **coché**) ou une déclaration explicite indiquant que le module ne comporte aucun champ avancé.

## Workflow

Il s’agit d’un processus en plusieurs phases. Le rythme est important : travaillez *avec* l&#39;utilisateur, pas avant lui. Confirmez la progression à chaque limite de phase et restez ouvert aux corrections à tout moment.

### Phase 1 — Portée des travaux

1. **Demandez s’il s’agit d’un ou de plusieurs modules** : *« Ajoutez-vous un ou plusieurs modules à un article de connecteur ?«*

2. **Rassemblez d’emblée chaque nom de module** en fonction de la réponse :
   - **Module unique** : demandez son nom exact tel qu’il apparaît dans l’interface utilisateur de Fusion.
   - **Modules multiples** : demandez tous les noms en une seule fois OU demandez une capture d’écran du connecteur qui les répertorie (par exemple, l’écran d’aperçu du connecteur dans Fusion qui affiche les libellés des mosaïques pour chaque module). Dans les deux cas, terminez cette étape par une liste confirmée de chaque nouveau module à ajouter.

3. **Recherchez vous-même l’article du connecteur** en recherchant les `help/workfront-fusion/references/apps-and-modules/` en fonction du nom du connecteur induit par le ou les modules. Utilisez les outils `Glob` ou `Grep`.

4. **Confirmez le chemin de l’article avec l’utilisateur** : *« En fonction du ou des noms de module, cette action doit être `help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-firefly-modules.md`. Est-ce exact? »*

5. **Lisez l’article sur le connecteur** pour découvrir sa structure et ses conventions existantes. Faites attention à :
   - Style de titre (généralement `### Module name` dans la casse de phrase)
   - Ordre des modules existants (généralement alphabétique)
   - Libellé `Connection` lignes
   - Mode d’écriture des champs imbriqués (par exemple, `Image > Source`)
   - Toutes les conventions d’annotation ou de note de bas de page existantes

### Phase 2 - Placez des espaces réservés pour chaque module à l&#39;avant

Même s’il n’y a qu’un seul nouveau module, cela donne à l’utilisateur une feuille de route visuelle claire. S’il existe plusieurs nouveaux modules, placez-les tous maintenant.

Pour chaque nouveau module, insérez une section d’espace réservé dans l’ordre alphabétique :

```markdown
### Module name

<!-- PLACEHOLDER: Add description of the Module name module here. -->

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Connector Name], see <a href="#create-a-connection-to-connector-name" class="MCXref xref" >Create a connection to [!DNL Connector Name]</a> in this article.</td> 
  </tr> 
  <!-- PLACEHOLDER: Add field rows for the Module name module here. -->
 </tbody> 
</table>
```

Affichez à l’utilisateur la liste des espaces réservés qui ont été ajoutés (par exemple, « Espaces réservés ajoutés pour : Générer un composite adaptatif, Générer des images avec Image5, Générer un composite précis, Générer une vidéo »). Demandez ensuite par quoi commencer : *« Par quoi souhaiteriez-vous commencer ?«*

### Phase 3 — Boucle de documentation par module

Pour chaque module, terminez complètement cette boucle avant de passer au suivant :

#### 3 bis. Obtenir l’URL de l’API

Demandez à l’utilisateur l’URL d’API : *« Veuillez partager l’URL d’API pour l’opération d’API sous-jacente de `<module name>`. »*

Lorsque vous l’avez :
- `WebFetch` sur l’URL.
- Si la page est vide ou rendue par JS (ce qui est courant avec les documents Adobe Developer), recherchez une page de guide des fonctionnalités associée (généralement à une URL `.../guides/how-tos/...`) et récupérez-la à la place.
- Si vous n’avez toujours pas de chance, revenez à `WebSearch` pour le nom de l’opération.

Utilisez ce que vous apprenez comme contexte d’arrière-plan pour les descriptions de champ ultérieurement. Ne la videz pas sur l’utilisateur ou l’utilisatrice ; reconnaissez-le simplement brièvement : *« J’ai reçu le contexte de l’API, prêt pour la capture d’écran de l’affichage standard »*

#### 3 ter. Obtenir la capture d’écran de l’affichage standard

Demander : *« Veuillez partager une capture d’écran du panneau de configuration du module avec `Show advanced settings`**non cochée**. Après avoir examiné les champs standard, je demanderai la vue avancée, mais ne l’envoyez pas encore. »*

#### 3 quater. Documenter les champs standards

À partir de la capture d’écran de l’affichage standard, capturez tous les champs visibles de haut en bas. Pour chaque champ :

1. Utilisez le libellé d’interface utilisateur exact du champ comme en-tête de ligne. Pour les champs groupés, joignez-les avec ` > ` :

   ```
   [!UICONTROL Background > Image > Source]
   ```

2. Lisez le texte d’aide sous le champ de la capture d’écran (la légende grise/jaune). Utilisez-la comme base de la description.
3. Effectuez une référence croisée au contexte de l’API à l’étape 3a pour identifier ce que le champ représente (par exemple, `background.fillAreaMask` est « la zone de l’arrière-plan où l’objet sera placé »).
4. Écrivez la description en combinant **ce qu’est le champ** (à partir de l’API) avec **comment le fournir** (à partir du texte d’aide de l’interface utilisateur et du type de champ).

Ignorez les champs qui ne sont pas visibles dans la capture d’écran, même si l’API les prend en charge. N’inventez pas de champs.

Une fois les champs standard en place, résumez-les brièvement à l’utilisateur (par exemple, « Champs standard ajoutés : Connexion, Invite, Format, etc. »), puis passez à l’étape 3d.

#### 3d. Obtenir la capture d’écran de l’affichage avancé

Demander : *« Maintenant, partagez une capture d’écran du panneau de configuration du module avec `Show advanced settings`**coché**. Si le module ne comporte aucun champ avancé, dites-le et nous passerons à autre chose*

#### 3 sexies. Documenter les champs avancés

Utilisation à partir de la capture d’écran de la vue avancée :

1. Identifiez les champs qui *ne sont pas* sont déjà dans la vue standard ; il s’agit des champs avancés.
2. Pour chaque champ avancé, suivez le même processus de description à l’étape 3c.
3. Ajoutez `*` au nom du champ dans le `<td role="rowheader">` :

   ```html
   <td role="rowheader">[!UICONTROL Seeds]*</td>
   ```

4. Après la `</table>` de clôture, ajoutez cette note de bas de page sur sa propre ligne :

   ```markdown
   * These fields are advanced fields, and do not display unless you select **[!UICONTROL Show advanced settings]**.
   ```

Si l’utilisateur indique que le module ne comporte aucun champ avancé, ignorez entièrement les étapes 3d et 3e.

#### 3 septies. Rédiger la description du module

Maintenant (pas auparavant), remplacez l’espace réservé de description en haut de la section par un brouillon d’une seule phrase basé sur le contexte de l’API et ce que les champs impliquent. Proposez-le toujours en tant que brouillon pour l’utilisateur ou l’utilisatrice :

> *« J&#39;ai rédigé cette description : &#39;...&#39;. Vous souhaitez l’utiliser, le modifier ou le remplacer ? »*

#### 3 octies. Conclusion par module

Donnez à l’utilisateur un résumé final des champs documentés du module (standard + avancés) et posez-lui toutes les questions ouvertes :

- Des champs ont-ils été coupés dans les captures d’écran ?
- La description du module est-elle acceptable ?
- Un élément doit-il être marqué comme obsolète ou digne d’être noté ?

Attendez confirmation avant de dire que le module est terminé. Demandez ensuite : *« Prêt à passer au module suivant ?«* (ou « Nous en avons fini avec cet article de connecteur »).

### Phase 4 — Vérification finale

Une fois tous les modules documentés, exécutez cette liste de contrôle pour chacun d’eux :

- [ L’en-tête ] module est `### ` (H3) et utilise la casse de phrase.
- [ ] module apparaît dans l’ordre alphabétique par rapport à ses modules frères.
- [ ] première ligne est `Connection` et utilise le libellé standard du lien de connexion.
- [ ] Chaque champ documenté est visible dans les captures d’écran de l’utilisateur.
- [ ] champs Avancés sont marqués d’une note de `*` et une seule note de bas de page existe sous le tableau.
- [ ] Aucun champ n’a été inventé à partir de la seule API.
- [ ] descriptions des listes déroulantes Source utilisent les libellés exacts des options de l’interface utilisateur (voir « Convention des champs de Source » ci-dessous).
- [ ] description du module est un résumé d’une phrase décrivant la fonction du module.

## convention des champs Source

Les champs source d’image des connecteurs Fusion présentent généralement une liste déroulante avec deux options. **Utilisez les libellés exacts affichés dans la capture d’écran de l’utilisateur** — les différentes générations de modules utilisent des libellés différents :

| Si la liste déroulante affiche... | Utiliser ce format |
|---|---|
| **Télécharger l’image** et **URL de l’image** (modules plus récents) | `<ul><li><b>Upload Image</b><p>Upload the image, or map the image file from a previous module.</p></li><li><b>Image URL</b><p>Enter or map the URL of the image.</p></li></ul>` |
| **Fichier** et **URL présignée** (modules plus anciens) | `<ul><li><b>File</b><p>Select a source file from a previous module, or map the source file's reference image file name and reference image file.</p></li><li><b>Presigned URL</b><p>Enter or map the URL of the source image.</p></li></ul>` |

Si la capture d’écran n’affiche pas les options de liste déroulante ouvertes, demandez à l’utilisateur de les partager.

## Style de description du champ

- Faites correspondre la voix et la structure des entrées de module existantes dans le même article.
- Gardez les descriptions courtes : une ou deux phrases par champ suffisent généralement.
- Utilisez le balisage `[!UICONTROL ...]` pour tout nom de champ de l’interface utilisateur référencé à partir d’un autre champ.
- Utilisez des `<code>...</code>` pour les valeurs littérales (`<code>en-US</code>`, `<code>0.0</code>`).
- Pour les champs de plage numérique, indiquez explicitement la plage autorisée : *« Saisissez un nombre compris entre 0 et 1...«*.
- Pour les listes déroulantes avec des options discrètes, énumérez-les sous la forme d’un `<ul>` avec des `<b>Option</b>` suivis d’une description `<p>`.

## Champs courants et descriptions recommandées

Réutilisez-les par souci de cohérence entre les modules :

**Valeurs de départ** (lorsque le champ autorise plusieurs valeurs de départ via Ajouter un élément) :
> Cliquez sur **Ajouter un élément** pour ajouter une valeur de départ, puis saisissez ou mappez un entier. Utilisez une adresse de contrôle par variation. Le nombre de valeurs de départ doit correspondre à la valeur **Nombre de variations** si les deux sont fournis.

**Nombre de variations** (remplacez la plage par la plage réelle de la capture d’écran) :
> Entrez un nombre compris entre [min] et [max]. Le module génère ce nombre de variations [type de sortie].

**Limite** (limite du cycle d’exécution de Fusion standard ; à inclure uniquement si elle est visible dans la capture d’écran) :
> Saisissez ou mappez le nombre maximal de résultats avec lesquels vous souhaitez que le module fonctionne au cours d’un cycle d’exécution.

**Paramètres régionaux** :
> Saisissez ou mappez une langue et un code de région pour adapter le contenu généré à un pays et une langue spécifiques. Les paramètres régionaux doivent être fournis dans le code de langue ISO 639-1 et la région ISO 3166-1. Exemple : `en-US`

## Être ouvert aux corrections à tout moment

L’utilisateur peut corriger les erreurs antérieures du flux de travail intermédiaire : formulation des valeurs de départ, libellés déroulants, positionnement des champs, division avancée/standard, etc. Traiter toute correction comme faisant autorité et mise à jour sans renvoi. Après la correction, résumez brièvement ce qui a été modifié.

Si l’utilisateur ou l’utilisatrice introduit un nouveau flux intermédiaire de convention (par exemple, « marquons les champs avancés avec `*` et ajoutons une note de bas de page »), adoptez-le pour le reste de la session et appliquez-le rétroactivement à tous les modules déjà documentés.

## Que faire si les informations sont en conflit

Lorsque la spécification de l’API et l’interface utilisateur sont en désaccord (cela se produit souvent) :

1. **Faites confiance à l’interface utilisateur** car c’est ce que l’utilisateur voit réellement dans Fusion.
2. **Notez la différence** dans votre réponse à l’utilisateur ou à l’utilisatrice afin qu’il ou elle puisse décider d’enquêter davantage.
3. **N’inventez pas d’explication** dans le corps de l’article : conservez-la factuelle par rapport à ce qui se trouve dans l’interface utilisateur.

Si deux captures d&#39;écran de l&#39;utilisateur se contredisent (par exemple, l&#39;une montre `Blend`, une autre montre `Harmonization` pour le même module), arrêtez-vous et demandez laquelle est correcte avant d&#39;écrire. Identifiez la capture d’écran qui appartient probablement à un module différent en référençant de manière croisée la spécification de l’API.
