---
title: Modules de chaîne
description: Grâce à ces modules, vous pouvez enchaîner les scénarios, en passant un appel à l’autre.
author: Becky
feature: Workfront Fusion
hide: true
hidefromtoc: true
source-git-commit: 454e06527fe1a624f36be3b7f3682ff49a61d42d
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 7%

---

# Modules de chaîne

À l’aide des modules de chaîne, vous pouvez connecter un scénario à un autre.

<!--This article will be about the specific module configuration-->

Pour obtenir des instructions sur la planification de scénarios chaînés, voir [Enchaîner plusieurs scénarios](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md).


## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tous</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licence Adobe Workfront</td> 
   <td> <p>Nouveau : Standard</p><p>Ou</p><p>En cours : Travail ou version ultérieure</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licence Adobe Workfront Fusion **</td> 
   <td>
   <p>Aucune exigence de licence Workfront Fusion</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Nouveau :</p> <ul><li>Sélectionnez ou le package Prime Workfront : votre entreprise doit acheter Adobe Workfront Fusion.</li><li>Package Ultimate Workfront : Workfront Fusion est inclus.</li></ul>
   <p>Ou</p>
   <p>Actuel : votre entreprise doit acheter Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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

