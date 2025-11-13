---
title: Modules de chaîne
description: Grâce à ces modules, vous pouvez enchaîner les scénarios, en passant un appel à l’autre.
author: Becky
feature: Workfront Fusion
exl-id: 21429f94-fe4c-4ccc-a8c0-d7573657fecc
source-git-commit: 7f73007e219714c38dd0cf29d2a1e3a4c8f6f3cc
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 4%

---

# Modules de chaîne

>[!NOTE]
>
>Cette fonctionnalité est actuellement disponible dans Beta.

À l’aide des modules de chaîne, vous pouvez connecter un scénario à un autre.

<!--This article will be about the specific module configuration-->

Pour obtenir des instructions sur la planification de scénarios chaînés, voir [Enchaîner plusieurs scénarios](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md).


## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tout package de workflow Adobe Workfront et tout package d’automatisation et d’intégration Adobe Workfront</p><p>Workfront Ultimate</p><p>les packages Workfront Prime et Select, avec un achat supplémentaire de Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licences Adobe Workfront</td> 
   <td> <p>Standard</p><p>Travail ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Si votre entreprise dispose d’un package Select ou Prime Workfront qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acheter Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++



## Modules de chaîne et leurs champs

### Déclencheurs

#### Recevoir des données du parent

Ce module est le module de déclenchement dans le scénario enfant et est déclenché par le module Appeler un scénario enfant dans le scénario parent. Il reçoit des données du scénario parent, qui peuvent être traitées dans le scénario enfant.

Pour configurer l’option Recevoir des données du module parent :

1. Pour utiliser une structure de données existante, dans le champ Structure de données , sélectionnez la structure de données qui sera utilisée pour les données d’entrée du scénario.

   Ou

   Pour créer une nouvelle structure de données à utiliser comme données d’entrée du scénario, cliquez sur **Ajouter** en regard du champ Structure de données et créez la structure de données.

   Pour obtenir des instructions sur la création d’une structure de données, voir [Structures de données](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

1. Cliquez sur **OK** pour enregistrer le module.

### Actions

#### Appeler un scénario enfant

Ce module se trouve dans le scénario parent. Les champs reflètent la structure de données définie dans le module Recevoir les données du parent dans le scénario enfant.

>[!NOTE]
>
>* Vous pouvez sélectionner un scénario enfant existant ou en créer un nouveau à l’aide de ce module.
>* Vous pouvez créer la structure des données lors de la création d’un scénario enfant.

Pour configurer le module Appeler un scénario enfant

1. Ajoutez le module Appeler un scénario enfant à votre scénario.
1. Pour utiliser un scénario enfant existant, dans le champ Chaîne , sélectionnez le scénario enfant à appeler.

   Ou

   Pour créer un nouveau scénario enfant, cliquez sur Ajouter en regard du champ Chaîne . Le scénario enfant s’affiche dans une fenêtre distincte, avec les modules parents Recevoir des données du parent et Renvoyer une réponse du parent .

   Les champs configurés dans le module de déclenchement du scénario enfant apparaissent dans le module Appeler un scénario enfant .

1. Saisissez ou mappez les informations à transmettre au scénario enfant dans le module Appeler un scénario enfant .
1. (Conditionnel) Si vous souhaitez que le scénario parent poursuive son exécution sans attendre de réponse du scénario enfant, activez l’option **Déclencher et oublier**.
1. Cliquez sur **OK** pour enregistrer le module.

>[!NOTE]
>
>Si vous créez un nouveau scénario enfant pour ce module, le scénario enfant s’ouvre dans une fenêtre de navigateur distincte, ce qui vous permet d’afficher et de configurer les scénarios parent et enfant en même temps.

#### Renvoyer la réponse au parent

Se trouve dans le scénario enfant et envoie les données de la structure sélectionnée au scénario parent. Vous pouvez mapper ces données dans des modules ultérieurs dans le scénario parent.

Si votre scénario enfant comporte plusieurs itinéraires, nous vous recommandons d’ajouter ce module à un itinéraire qui s’exécute toujours après tout autre itinéraire.

Pour configurer le module Ajouter un répondeur :

1. Pour utiliser une structure de données existante, dans le champ Structure de données , sélectionnez la structure de données qui sera utilisée pour les données que le scénario enfant renvoie au scénario parent.

   Ou

   Pour créer une nouvelle structure de données pour les données, cliquez sur **Ajouter** en regard du champ Structure de données et créez la structure de données.

   Pour obtenir des instructions sur la création d’une structure de données, voir [Structures de données](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

1. Cliquez sur **OK** pour enregistrer le module.
