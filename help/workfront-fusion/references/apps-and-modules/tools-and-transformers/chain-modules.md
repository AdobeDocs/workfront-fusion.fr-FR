---
title: Modules de chaîne
description: Grâce à ces modules, vous pouvez enchaîner les scénarios, en passant un appel à l’autre.
author: Becky
feature: Workfront Fusion
exl-id: 21429f94-fe4c-4ccc-a8c0-d7573657fecc
TQID: https://experienceleague.adobe.com/AlHUrliXikCc3OVHiBTjLNQFndCf5qLzOLuBvnDTUfA
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 81d1dfcdb5c15f6a93e2793f9a0e41821b65c7e3
workflow-type: tm+mt
source-wordcount: 883
ht-degree: 10%

---

# Modules de chaîne

>[!IMPORTANT]
>
>Cette fonctionnalité est disponible dans Beta et n’est pas recommandée pour les workflows de production critiques. En tant que fonctionnalité Beta, le comportement peut changer et les cas Edge peuvent ne pas être entièrement gérés.
>
>Pour les intégrations stables, envisagez de déclencher un second scénario par le biais d’un webhook à l’aide d’un module de requête HTTP . Ce modèle utilise des primitives entièrement prises en charge et donne à chaque scénario un contrôle d’exécution indépendant.
>
>Si vous choisissez d’utiliser des scénarios enchaînés, consultez [Enchaîner plusieurs scénarios ensemble](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md) pour obtenir des conseils de conception.

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
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tout package de workflow Adobe Workfront et tout package d’automatisation et d’intégration Adobe Workfront</p><p>Workfront Ultimate</p><p>Packages Workfront Prime et Select, avec l’achat supplémentaire de Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licences Adobe Workfront</td> 
   <td> <p>Standard</p><p>Travail ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Si votre organisation dispose d’un package Workfront Select ou Prime qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acquérir Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

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

>[!IMPORTANT]
>
> Examinez les points suivants avant de configurer ce module dans un scénario de production :
>
> * **N’activez pas l’option Valider le dernier déclencheur (CTL)** sur ce scénario lorsque les options Déclenchement et oubli sont désactivées. CTL relance le scénario lorsqu’il est suspendu en attendant une réponse enfant, créant ainsi une boucle de reprise illimitée.
> * **Soyez prudent lorsque vous placez ce module dans un itérateur.** L’envoi d’un scénario enfant pour chaque élément dans un grand itérateur crée une charge de plateforme importante. Envisagez d’intégrer la logique du scénario enfant ou de pré-calculer les recherches partagées en dehors de l’itérateur.
> * **Déclencher et oublier** signifie que le parent n’a aucune visibilité sur l’exécution ou le succès de l’enfant. À utiliser uniquement lorsque les échecs enfants sont surveillés indépendamment.
>
> Pour obtenir des conseils de conception complets, voir [Enchaînement de plusieurs scénarios](https://experienceleague.adobe.com/fr/docs/workfront-fusion/using/create-scenarios/plan-a-scenario/chain-scenarios).

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

>[!IMPORTANT]
>
> Si votre scénario enfant comporte plusieurs itinéraires, vous **devez** vous assurer que la réponse Retour au module parent est accessible à partir de chaque chemin d’exécution. Si le module de réponse de retour se trouve sur un itinéraire qui est ignoré ou qui n’est pas exécuté, le scénario parent attend indéfiniment une réponse qui n’arrive jamais.
>
> Ajoutez la réponse Retour au module parent après votre routeur, sur une route qui s&#39;exécute toujours quel que soit le résultat du routeur, ou ajoutez la gestion des erreurs pour vous assurer qu&#39;une réponse est toujours renvoyée même lorsqu&#39;une erreur se produit.

Pour configurer le module Ajouter un répondeur :

1. Pour utiliser une structure de données existante, dans le champ Structure de données , sélectionnez la structure de données qui sera utilisée pour les données que le scénario enfant renvoie au scénario parent.

   Ou

   Pour créer une nouvelle structure de données pour les données, cliquez sur **Ajouter** en regard du champ Structure de données et créez la structure de données.

   Pour obtenir des instructions sur la création d’une structure de données, voir [Structures de données](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

1. Cliquez sur **OK** pour enregistrer le module.
