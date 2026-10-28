---
title: Afficher l’exécution d’un scénario spécifique
description: Vous pouvez afficher les détails d’une exécution de scénario spécifique, y compris le filtrage et la recherche d’événements de scénario.
author: Becky
feature: Workfront Fusion
exl-id: 34dd9836-9a1b-4ce2-b24e-ae769888a52a
TQID: 'https://experienceleague.adobe.com/Msh3ArxBUIu6YDZjL7eXpxlEBiYABHN-Q7xUlJ-qU0g'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: cc160f0e8c2465b4f102b6d1755088335b2a9fe5
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 16%
---
# Afficher l’exécution d’un scénario spécifique

Vous pouvez afficher les détails d’une exécution de scénario spécifique, y compris le filtrage et la recherche d’événements de scénario.

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

## Afficher une exécution spécifique

Vous pouvez afficher une exécution à partir de l’historique des scénarios du scénario.


1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche, puis cliquez sur le scénario.

   Ou

   Si vous travaillez sur le scénario dans l’éditeur de scénarios, cliquez sur la flèche de gauche ![flèche de modification de sortie](assets/exit-editing-arrow.png) près du coin supérieur gauche de la fenêtre.

1. Cliquez sur **Historique** près du nom du scénario.
   ![onglet historique](assets/history-tab.png)


1. Recherchez l’exécution à afficher, puis cliquez sur **Détails** à l’extrémité droite de la ligne correspondant à cette exécution. Le lien [!UICONTROL Détails] n’est visible que si les détails de l’exécution sont disponibles.

   Le diagramme de scénario s’ouvre avec le panneau des détails de l’exécution ouvert à droite.

   Les modules qui ont généré la sortie pour cette exécution sont marqués avec des titres verts.

   Les modules qui n’ont pas été exécutés sont grisés.

1. Pour afficher la sortie d’un module, cliquez sur la bulle des détails de sortie près du module. Le nombre dans la bulle représente le nombre de lots générés par le module.

   ![Bulle de sortie près d&#39;un module](assets/new-output-bubble.png)

1. Pour afficher les lots qui ont passé par un filtre, cliquez sur le filtre. Le nombre près du filtre représente le nombre de lots qui ont passé par le filtre.
1. Pour rechercher un module ou un événement spécifique dans le panneau d’exécution, saisissez le terme de recherche dans la zone **Rechercher des événements d’exécution**. Les résultats s’affichent au fur et à mesure que vous tapez.
1. Pour limiter les résultats de recherche du panneau d’exécution par statut, tel que Succès ou Avertissement, cliquez sur le menu déroulant **Filtre de statut** et sélectionnez le statut.




>[!NOTE]
>
>Pour créer un lien vers un module spécifique, ajoutez des `?moduleId=<module-id>` à l’URL lors de l’affichage des pages suivantes :
>
>* Page de modification du scénario (l’URL se termine par `/edit`)
>* Exécution d’un scénario spécifique (l’URL se termine par `/logs/<log-id>`)
>
>`<module-id>` fait référence au nombre en regard du libellé du module lors de l’affichage du scénario.
>
>Cela peut s’avérer utile lors du débogage de scénarios ou de la copie de la configuration du module.

## Vérifier une exécution dans le nouvel éditeur de scénarios

Dans la nouvelle expérience , lorsque vous ouvrez une exécution à partir de l’historique d’exécution, les commandes proches du côté droit de la zone de travail vous aident à identifier le problème sans modifier le scénario :

![Vérifier une exécution](assets/review-an-execution.png)

| Commande | Détails |
| ---------- | ---------- |
| Aller à l&#39;erreur ou à l&#39;avertissement suivant | Indique le nombre de modules ayant rencontré un problème dans le cycle en cours. Chaque clic passe au suivant, d’abord les erreurs, puis les avertissements, de gauche à droite. Il centre le module et ouvre la première opération ayant échoué. Le bouton est masqué lorsque l’exécution ne comportait aucune erreur ou avertissement. |
| Modules de recherche | Recherchez un module par nom et centrez-le sur la zone de travail. Appuyez sur Ctrl+K (Windows) ou Commande+K (Mac). |
| Notes | Afficher ou masquer les notes du scénario. Ce contrôle s’affiche uniquement lorsque le scénario comporte des notes. Celles-ci sont en lecture seule ici. |
| Expliquer le flux | Animez l’ordre dans lequel les modules du scénario s’exécutent. Cliquez à nouveau dessus ou appuyez sur Échap pour arrêter. |
| Zoom avant, Zoom arrière, Focus et réduction | Fonctionne de la même manière qu’en mode d’édition. |

Le commutateur **Vue compacte** est également disponible dans le coin supérieur droit. Lorsque vous révisez une exécution, la mise en page n’est modifiée que lorsque vous examinez cette exécution. Cela ne modifie pas le paramètre de la vue compacte à modifier et rien n’est enregistré dans le scénario.

Sélectionnez un événement dans l’exécution pour centrer et mettre en surbrillance le module correspondant. Lorsque les détails de l’opération sont disponibles, le panneau de requête et de réponse s’ouvre. Si le panneau ne contient aucune donnée, les détails de la requête et de la réponse n’ont pas été conservés pour cette exécution. Pour les collecter en vue d’exécutions ultérieures, voir [ Journaux de débogage temporaires ](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#temporary-debug-logs).
