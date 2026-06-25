---
name: writing-quality
description: 'Examinez et améliorez la qualité technique de la rédaction des articles pratiques et de la documentation générale de Workfront. Applique le Guide de style et les principes de la documentation de Workfront issus du Développement d’informations techniques de qualité. À utiliser lors de la modification, de la révision ou de la rédaction d’articles pratiques, d’articles de présentation, d’articles de référence ou de documentation générale. Ne pas utiliser pour les notes de mise à jour : utilisez plutôt la compétence formateur de notes de mise à jour .'
source-git-commit: 4d32e8aab5b3b8a12dbc23e61f517fc4fd6dc9e5
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 1%

---


# Qualité d’écriture

passe en revue et améliore la documentation de Workfront à l’aide du guide de style de documentation de Workfront et des principes DQTI ;

## Workflow

Lors de la révision ou de la modification du contenu :

1. Lire le fichier cible
2. Appliquer les règles ci-dessous — résoudre directement les problèmes ou les signaler
3. Préserver l’intention et l’exactitude technique de l’auteur
4. Pour en savoir plus sur la terminologie, la ponctuation et les règles de procédure, voir .claude/commands/_writing-quality-reference.md

## Voix et point de vue

- Utiliser **deuxième personne** (« Vous pouvez... ») lors de l’adressage du lecteur
- Utilisez des contractions pour une tonalité de conversation (ne pas, ne peut pas, c&#39;est, ils sont)
- Utilisez « Nous vous recommandons » pour les bonnes pratiques, et non « C’est recommandé » ou « Vous devriez ».
- Lorsque vous écrivez pour un groupe d’utilisateurs, référencez d’autres rôles à la troisième personne (« Vous pouvez afficher... Cependant, l’administrateur Workfront peut restreindre... »)
- N&#39;utilisez jamais de pronoms sexospécifiques — restructurez la phrase ou utilisez « they »
- Pas de barre oblique pour les choix — utiliser « ou » (« lui ou elle » et non « il ou elle »)

## Clarté (DQTI)

- Une idée par phrase
- Conserver les phrases de moins de 25 mots dans la mesure du possible
- Diriger avec l’action ou le résultat, et non le contexte d’arrière-plan
- Utilisez le mot le plus simple qui véhicule la signification (« use » non « use », « start » non « initiate », « about » non « concerning »)
- Éviter les nominalisations (« créer » et non « la création de », « configurer » et non « la configuration de »)
- Utilisez un langage précis et concret — évitez les termes vagues (« plusieurs », « divers », « certains »)
- Éviter les doubles négatifs
- Utilisez des pronoms facultatifs (« that », « who ») pour clarifier la structure des phrases

## Concretence (DQTI)

- Utiliser des exemples spécifiques plutôt que des descriptions abstraites
- Inclure des valeurs réalistes dans les exemples
- Nommez les éléments, champs et zones exacts de l’interface utilisateur

## Orientation des tâches (DQTI)

- Concentrez-vous sur ce que l’utilisateur ou l’utilisatrice peut *faire*, et non sur ce qu’*le système*
- Procédures de lead avec des verbes impératifs (« Créer une tâche », « Configurer des notifications »)
- Fournissez suffisamment de contexte pour que l’utilisateur puisse agir, mais pas plus
- Insérez un lien vers l’aide détaillée (« Pour plus d’informations, voir [article]. »).

## Majuscules

- **En-têtes** : Cas de phrase toujours (« Créer une tâche » et non « Créer une tâche »)
- **Termes de Workfront** : mettez en majuscule uniquement lorsque vous référencez directement un élément de l’interface utilisateur
   - Référence directe : « Remplissez le champ Date d’achèvement prévue ».
   - Référence indirecte : « Chaque tâche doit avoir une date d’achèvement planifiée. »
   - Conseil : si vous pouvez mettre « le » ou « a » devant le terme, il doit généralement être en minuscules
- **Boutons** : suivez la casse de l’interface utilisateur, sauf les boutons en majuscules → la casse de la phrase.
- **Rôles** : « Administrateur système » pour le rôle dans l’interface utilisateur ; « Administrateur Workfront » pour la personne

## Titres

- Utilisez la commande impérative dans la casse de phrase (« Créer une tâche », « Configurer les niveaux d’accès »)
- Les en-têtes doivent être basés sur une tâche : décrivez ce que l&#39;utilisateur accomplira
- Les articles de présentation se terminent par « présentation » (présentation des projets)
- Diviser de longues sections en plusieurs en-têtes avec des sous-objectifs clairs

## Références croisées et liens

Utilisez ces modèles exacts :

| Situation | Format |
|-----------|--------|
| Lien après avoir donné des informations | « Pour plus d’informations, voir [Nom de l’article]. » |
| Lien sans information préalable | « Pour plus d’informations, voir [Nom de l’article]. » |
| Lien vers une section d’un autre article | « Pour plus d’informations, voir [Nom de la section] dans [Nom de l’article]. » |
| Lien vers une section du même article | « Pour plus d’informations, voir [Nom de la section] dans cet article. » |

- Dans un paragraphe : en ligne avec le texte
- Dans une étape de procédure : sur une nouvelle ligne après l’étape
- Liens multiples : utilisez une liste à puces
- Utiliser « coin supérieur droit »/« coin supérieur gauche » pour les positions à l’écran

## Gras et italique

- **Gras** actions cliquables et éléments d’interface utilisateur dans les étapes de la procédure uniquement
- Ne mettez pas en gras les éléments de l’interface utilisateur en dehors des étapes de la procédure
- Ne mettez pas en gras les noms des boîtes de dialogue, des pages, des icônes ou des menus en dehors des étapes
- Utilisez l’*italique* pour le texte que l’utilisateur doit saisir (« Saisissez *my.workfront.com* dans la zone d’URL »)
- N’utilisez jamais l’italique pour mettre l’accent : restructurez plutôt la phrase.

## Notes, conseils et avertissements

Utilisez avec parcimonie : une utilisation excessive les rend invisibles aux yeux des lecteurs.

- Maximum une note/conseil/avertissement par section
- Ne jamais empiler plusieurs notes
- Combiner des notes connexes dans une note avec une liste à puces
- N’utilisez pas de notes pour annoncer une nouvelle fonctionnalité : relisez plutôt le texte de l’article

| Type | Rôle |
|------|---------|
| `>[!NOTE]` | Informations ne correspondant pas au paragraphe ; éviter toute frustration ; contrôle de version/compatibilité |
| `>[!TIP]` | Des suggestions intéressantes qui facilitent la vie de l’utilisateur |
| `>[!IMPORTANT]` | Informations vitales pour l’étape ou la procédure |
| `>[!WARNING]` | Alerter l’utilisateur d’une perte de données potentielle |

## Procédures

- Utiliser des en-têtes de commande impératifs (« Créer une tâche »)
- Introductions uniquement lorsque cela est nécessaire — le titre devrait suffire
- Format d’introduction préféré : expression infinie + deux points (« Pour créer un mot de passe temporaire : »)
- Les procédures en une seule étape utilisent toujours une liste numérotée
- Utilisez « type » ou « select » — évitez les mots vagues comme « set » ou « specifier »
- Étapes conditionnelles : « (Conditionnel) Si vous êtes membre de plusieurs équipes, sélectionnez... »
- Étapes facultatives : « (facultatif) Pour ajouter un émoticône, cliquez sur... »
- Décrivez la réponse du système avant qu’elle ne se produise ou immédiatement après
- Plusieurs méthodes : commencez par documenter la méthode la plus simple, puis utilisez « Ou ».

### Crochets à angle droit dans les procédures

- Utilisez `>` pour afficher la navigation entre les menus et les onglets : « Cliquer **E-mail** > **Notifications** ».
- Mettre en gras les noms des boutons et non les crochets
- Inclure les espaces autour des crochets
- Ne pas utiliser de crochets pour la navigation dans le menu principal — utiliser le fragment de code du menu principal

## Référence rapide de la ponctuation

| Règle | Exemple |
|------|---------|
| Virgule d&#39;Oxford toujours | « motif, moyens et opportunité » |
| Virgule avant « then » dans les procédures | « Cliquez sur Configuration, puis sur Interface. » |
| Virgule après l’année dans une date au milieu de la phrase | « Le numéro du 2 janvier 2016 de... » |
| Pas de virgule avec le mois-année uniquement | « Janvier 2016 » |
| Deux-points avant une liste, minuscules après | « Sélectionnez l’une des options suivantes : option A » |
| Pas de signe deux-points après les en-têtes de procédure | « Créer une tâche » (et non « Créer une tâche : ») |
| Aem tirets avec parcimonie | Restructurer la phrase si possible |
| Points dans les extensions de fichier | « Charger un fichier .pdf » |

Pour connaître l’ensemble des règles de ponctuation et de terminologie, voir .claude/commands/_writing-quality-reference.md.

## Exhaustivité (DQTI)

- Incluez toutes les informations que l’utilisateur ou l’utilisatrice doit comprendre et utiliser
- Ne pas inclure d&#39;informations dont l&#39;utilisateur n&#39;a pas besoin
- Fournissez toujours un lien « Pour plus d’informations » vers la documentation détaillée
- Valeurs par défaut du système de documents : « (par défaut) » dans les listes, ou décrire dans la phrase

## Organisation (DQTI)

- Structure logique avec divulgation progressive (présentation → détails → référence)
- Contenu le plus récent en premier pour les pages chronologiques (par exemple, notes de mise à jour)
- Une rubrique par section
- Utiliser des listes pour 3 éléments parallèles ou plus
- Utiliser des tableaux pour les comparaisons structurées ou la description des champs
- Évitez les paragraphes de texte accrochés aux murs — divisez-les en blocs digestibles

## Types d’articles

| Type | Rôle | Convention de titre |
|------|---------|-----------------|
| Vue d’ensemble | Contexte, diagrammes, fonctionnement des choses — pas de procédures | Se termine par « aperçu » |
| Procédure | Tâche spécifique avec des étapes claires | Verbe impératif |
| Prise en main | Infos de configuration + liens pour les nouveaux utilisateurs | « Prise en main de... » |
| Référence | Descriptions des champs dans les tableaux | Expression de substantif descriptif |

## Liste de contrôle de validation

Après modification, vérifiez les éléments suivants :

- [ ] Deuxième personne tout au long (« vous »), contractions utilisées
- [ ] le cas de phrase sur tous les en-têtes
- [ ] termes Workfront correctement mis en majuscules (référence directe ou indirecte)
- [ ] Gras uniquement sur les actions cliquables dans les étapes de la procédure
- [ ] Les références croisées utilisent le format standard (« Pour plus d’informations, voir... »).
- [ ] notes/conseils/avertissements non empilés, un maximum par section
- [ ] virgule d’Oxford utilisée de manière cohérente
- [ Les étapes de la procédure ] utilisent des verbes spécifiques (tapez, sélectionnez, cliquez — et non pas « définir » ou « spécifier »)
- [ ] Étapes conditionnelles/facultatives correctement libellées
- [ ] Pas de pronoms de genre
- [ ] Les phrases sont claires, concrètes et axées sur la tâche
