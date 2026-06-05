---
title: Redéclencher l’exécution d’un scénario spécifique
description: Vous pouvez déclencher à nouveau l’exécution d’un scénario spécifique pour traiter les données à l’aide d’un plan directeur de scénario mis à jour ou pour afficher son flux de données.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 0c732add9c1ec75d7aed43bb7097bb1c95aa6408
workflow-type: tm+mt
source-wordcount: 523
ht-degree: 18%

---

# Redéclencher l’exécution d’un scénario spécifique

Vous pouvez déclencher à nouveau l’exécution d’un scénario spécifique pour traiter les données à l’aide d’un plan directeur de scénario mis à jour ou pour afficher son flux de données. Lorsque vous redéclenchez une exécution, le scénario s’exécute à l’aide des données de cette exécution.

Par exemple, si vous mettez à jour un scénario pour ajouter une action telle que la création d’un problème, vous pouvez déclencher à nouveau une exécution qui s’est produite avant la mise à jour. Le scénario mis à jour s’exécute à l’aide de l’événement déclencheur du scénario d’origine, mais inclut l’action mise à jour. Dans cet exemple, le scénario crée un problème dans le cadre de la nouvelle exécution.

Le redéclenchement est disponible pour les scénarios comportant des déclencheurs webhook et pour les scénarios enfants.

Lors du redéclenchement d’un scénario qui utilise un webhook, l’événement webhook d’origine peut être utilisé à nouveau. Vous n’avez donc pas besoin de recréer l’événement pour redéclencher le scénario.

Lors de l’utilisation de scénarios chaînés, le redéclenchement peut également être appliqué à un scénario enfant. Le scénario enfant peut être redéclenché à l’aide des données envoyées à partir du scénario parent dans l’exécution d’origine, sans redéclencher le scénario parent.

Pour plus d’informations sur les webhooks, consultez la section [Déclencheurs instantanés (webhooks)](/help/workfront-fusion/references/modules/webhooks-reference.md).

Pour plus d’informations sur le chaînage de scénarios, voir [Enchaîner plusieurs scénarios](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md).

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

## Redéclencher une exécution

Vous pouvez redéclencher l’exécution d’un scénario à partir du diagramme du scénario, de la zone Historique du scénario ou de la page d’exécution du scénario spécifique.

### Redéclencher une exécution à partir du diagramme de scénarios

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Sélectionnez le scénario qui a exécuté l’exécution à redéclencher.

   Le diagramme du scénario s’ouvre.
1. Recherchez l’exécution à redéclencher dans la liste Exécutions sur le côté droit de la page.
1. Cliquez sur **Redéclencher** pour ce scénario.

![Redéclencher à partir du diagramme](assets/retrigger-from-diagram.png)

### Redéclencher une exécution à partir de l’historique des scénarios

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Sélectionnez le scénario qui a exécuté l’exécution à redéclencher.

   Le diagramme du scénario s’ouvre.

1. Cliquez sur l’onglet **Historique** juste en dessous du nom du scénario.
1. Recherchez l’exécution à redéclencher. Vous pouvez utiliser la recherche en texte intégral pour la localiser si nécessaire.
1. Cliquez sur **Redéclencher** pour ce scénario.

![Redéclencher à partir de l’historique](assets/retrigger-from-history.png)

### Redéclencher un scénario à partir de la page d’exécution du scénario

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Sélectionnez le scénario qui a exécuté l’exécution à redéclencher.

   Le diagramme du scénario s’ouvre.
1. Recherchez l’exécution à redéclencher dans la liste Exécutions sur le côté droit de la page.
1. Cliquez sur l’exécution pour l’ouvrir.
1. Sur la page d’exécution, cliquez sur **Redéclencher**.


![Redéclencher à partir de l’exécution](assets/retrigger-from-execution.png)






