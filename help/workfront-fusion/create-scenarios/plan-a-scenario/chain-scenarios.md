---
title: Chain Multiple Scenarios Together
description: You can chain scenarios together, allowing one scenario to trigger another, and returning the data output by the second scenario to the first.
author: Becky
feature: Workfront Fusion
exl-id: def8d4c1-fc20-4b93-b1fd-be2f60300464
source-git-commit: 0390bb875eb10278967d7d1c9cd61e5243e5f37e
workflow-type: tm+mt
source-wordcount: '1266'
ht-degree: 12%

---

# Enchaîner plusieurs scénarios

>[!NOTE]
>
>This feature is currently in Beta.

You can chain scenarios together, allowing one scenario to trigger another, and returning the data output by the second scenario to the first. This allows more modular scenario creation, where you do not have to duplicate scenario sections in multiple scenarios.

Vous pouvez appeler plusieurs scénarios enfants à partir d’un scénario parent, et appeler un scénario enfant à partir de plusieurs scénarios parents. Vous pouvez également imbriquer des scénarios enfants, en les appelant les uns des autres.

When a parent scenario is waiting for a child scenario to return data, that time does not count against the parent scenario&#39;s timeout. For example, a parent scenario calls 5 child scenarios, each of which takes 10 minutes to run, for a total of 50 minutes. The modules in the parent scenario itself take 15 minutes to run. The parent scenario does not time out, even though a total of 65 minutes has passed, which is over the timeout limit of 40 minutes.

For more information on Fusion&#39;s performance guardrails, including timeouts, see [Fusion performance guardrails](/help/workfront-fusion/references/scenarios/fusion-performance-guardrails.md).

Pour obtenir des instructions sur la configuration des modules Chain, voir [Modules Chain](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md).

## Parent and child scenarios

* The **parent** scenario calls another scenario, using the **Chain** > **Call a child scenario** module. It receives the output of the child scenario, which it can process in later scenario modules.
* The **child** scenario is called by the parent scenario. Its trigger module receives data from the parent scenario, and returns output to the parent scenario.

The parent scenario requires a response from the child scenario. Child scenarios that do not return data are currently not supported.

## Data structures in chained scenarios

Workfront Fusion uses data structures to transfer information from the parent scenario to the child scenario. The data structure is configured in the child scenario. When the child scenario is selected from the parent scenario, the fields for the data structure used as the child scenario&#39;s input appear in the parent scenario. You can map values to these fields, which are passed to the child scenario when it is triggered.

Pour plus d’informations sur les modules à configurer dans les scénarios parent et enfant, voir [Chaîne de modules](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md).

Pour plus d’informations sur les structures de données, voir [Structures de données](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

## Flux de données

1. Les données circulent dans le scénario parent.
1. Les données atteignent le module Appeler un scénario enfant . Les données sont mappées aux champs du module Appeler un scénario enfant , qui correspondent aux champs de la structure de données utilisée dans le module de déclenchement du scénario enfant.
1. Les données du scénario Appeler un enfant sont transmises au scénario enfant.
1. Le scénario enfant traite les données et effectue des actions.
1. Le scénario enfant se termine par la réponse Renvoyer au module parent.
1. La sortie de la réponse renvoyée au module parent est transmise au scénario parent.
1. La sortie du scénario « Appeler un enfant » est la sortie du scénario enfant . Cette sortie peut être traitée ultérieurement dans le scénario parent.

## Cas d’utilisation

Tenez compte des cas d’utilisation suivants pour le chaînage de scénarios :

* **Logique réutilisable** : vous pouvez enchaîner des scénarios pour les actions répétées utilisées dans plusieurs scénarios. Par exemple, si plusieurs scénarios archivent du contenu, vous pouvez créer un seul scénario enfant appelé « Archiver le contenu » que vous pouvez ensuite utiliser comme scénario enfant pour tous les workflows qui archivent du contenu.

* **Gestion des erreurs** : il est courant pour les organisations de disposer des mêmes actions de gestion des erreurs dans plusieurs scénarios, par exemple une itinéraire de gestion des erreurs qui envoie un journal des erreurs à un magasin de données et crée une notification Slack. Vous pouvez créer un scénario enfant avec ces actions et enchaîner ce scénario dans des itinéraires de gestion des erreurs dans plusieurs scénarios.

* **Prolonger le temps** : vous pouvez utiliser le chaînage pour les opérations par lots volumineuses avec des actions à long terme, par exemple lorsque vous exportez et importez des fichiers. Cette opération prend un certain temps s’il y a de nombreux fichiers. Comme les scénarios enfants ne sont pas comptabilisés dans le délai d’expiration du scénario parent, vous pouvez dépasser le temps d’exécution en utilisant plusieurs scénarios enfants pour exporter ou importer les fichiers.

* **Remplacement des itérateurs** Le remplacement des itérateurs par des scénarios enfants peut réduire l’utilisation de la mémoire, par exemple dans des opérations complexes dans une itération qui provoque une erreur de mémoire insuffisante. Vous pouvez créer un scénario distinct pour l’opération complexe et remplacer l’itérateur par Appeler un module de scénario enfant

* **Rechercher et créer un enregistrement** : par exemple, vous pouvez créer un scénario qui recherche un utilisateur. S’ils existent, le scénario les ajoute en tant qu’approbateurs avec l’accès dont ils ont besoin pour les réviser et les approuver. S’ils n’existent pas, le scénario crée une demande d’intégration d’un nouvel utilisateur pour l’administrateur.

## Affichage de l’historique d’exécution pour les scénarios chaînés

Vous pouvez afficher l&#39;historique d&#39;exécution des scénarios chaînés en affichant l&#39;historique de chaque scénario inclus dans la chaîne. Par exemple, l’historique d’exécution du scénario parent inclut des informations sur les modules et les données traités directement dans le scénario parent. Pour afficher l’historique d’exécution des modules et des données traités dans un scénario enfant, ouvrez le scénario enfant et affichez-y l’historique d’exécution.

Nous vous recommandons d’utiliser le bouton **Accéder au scénario enfant** dans le module Appeler un scénario enfant pour accéder rapidement au scénario enfant, où vous pouvez afficher son historique d’exécution. Le scénario enfant s’ouvre dans une autre fenêtre du navigateur, ce qui vous permet d’afficher les scénarios parents et enfants en même temps.

![Bouton Accéder au scénario enfant](assets/go-to-the-child-button.png)

## Erreurs et exécutions incomplètes

### Gestion des erreurs

Si le scénario enfant génère des erreurs, cela peut avoir une incidence sur la récupération des données chez vos parents.

Nous vous recommandons de configurer la gestion des erreurs dans le scénario enfant afin de vous assurer que si une erreur se produit dans le scénario enfant, le scénario parent n’est pas bloqué en attendant la réponse du scénario enfant.

## Bonnes pratiques

Tenez compte des bonnes pratiques suivantes lors du chaînage d’un scénario.

### Éviter la récursivité lors du chaînage de scénarios

La récursion se produit lorsqu’un scénario déclenche une nouvelle exécution de lui-même, ce qui déclenche une nouvelle exécution, et ainsi de suite dans une boucle infinie.

La récursion peut entraîner des problèmes de performances à la fois pour l’organisation propriétaire du scénario récursif et pour d’autres organisations.

Lors du chaînage de scénarios, suivez ces pratiques pour éviter la récursivité :

* Assurez-vous que **les scénarios enfants ne peuvent pas déclencher le scénario parent**. Par exemple, si un scénario parent est déclenché lors de la création d’une requête, assurez-vous que les scénarios enfants ne créent pas de requêtes.
* Assurez-vous que **les scénarios enfants ne s’appellent pas**. Par exemple, si le scénario enfant A appelle le scénario enfant B, assurez-vous que le scénario enfant B n’appelle pas le scénario enfant A.
* Assurez-vous qu’**un scénario ne peut pas s’appeler**. Par exemple, un scénario est déclenché lorsqu’une tâche est créée et que ce scénario crée deux tâches. Les deux nouvelles tâches déclenchent à nouveau le scénario, ce qui crée quatre nouvelles tâches. Chaque fois qu’une tâche est créée, le scénario est déclenché, et chaque fois qu’il s’exécute, le nombre de tâches double. Le nombre de tâches augmente de manière exponentielle.

>[!IMPORTANT]
>
>* **Lorsqu’un scénario entraîne une récursion, il est désactivé par l’équipe d’ingénierie de Fusion afin d’éviter d’autres problèmes de performances.**
>* La récursion étant le résultat de la conception des scénarios, vous devez concevoir les vôtres de manière à ce qu’ils n’incluent pas d’actions qui déclenchent le scénario.
>* Vous pouvez afficher un diagramme des relations entre les scénarios parents et enfants.
>   Pour obtenir des instructions, voir [Afficher les relations de scénario chaîné](/help/workfront-fusion/manage-scenarios/view-chained-scenario-relationships.md).

### Utilisation de la gestion des erreurs pour garantir une réponse

Comme le scénario parent attend une réponse du scénario enfant avant de pouvoir continuer, vous devez vous assurer que le scénario enfant est créé de sorte qu’il fournisse une réponse même s’il rencontre une erreur.
