---
title: Affichage du tableau de bord des informations pour une organisation
description: Les administrateurs et administratrices de Fusion peuvent afficher un tableau de bord qui affiche les mesures d’exécution pour une organisation.
author: Becky
feature: Workfront Fusion
exl-id: 8f80f86a-69e5-48a1-9812-87322a4959a6
TQID: 'https://experienceleague.adobe.com/tBZCbpImQxY42gOE8e04aQwCJC8EKgrDTIAt6Sw1KaU'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 45c755a2f6152b6e230864e4c840d0334705bd22
workflow-type: tm+mt
source-wordcount: '1307'
ht-degree: 5%
---
# Affichage du tableau de bord des informations pour une organisation

Le tableau de bord Fusion Insights vous permet de voir rapidement quels scénarios sont les plus exécutés, où les retards se produisent et avec quelle efficacité vos pools de salariés fonctionnent. Vous bénéficiez ainsi d’une visibilité en temps réel sur les volumes d’exécution, la profondeur de file d’attente, l’utilisation du pool et les performances au niveau du scénario.

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Workflow Adobe Workfront Automatisation et intégration d’Ultimate et d’Adobe Workfront Ultimate</p><p>Workfront Ultimate</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licences Adobe Workfront</td> 
   <td> <p>Standard</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurations des niveaux d’accès</td> 
   <td> 
     <p>Vous devez être administrateur ou administratrice Workfront Fusion pour votre entreprise.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation Workfront](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Composants du tableau de bord Insights

>[!NOTE]
>
>Les mesures sont affichées par pool de traitement. Pour afficher un autre pool de traitement, cliquez sur le champ Pool près du coin supérieur gauche du tableau de bord, puis sélectionnez le pool pour lequel vous souhaitez afficher les mesures.

<!--

>[!NOTE]
>
>Organizations can request provisioning for one additional worker pool (for a total of 2).

-->

Dans le tableau de bord Fusion Insights, vous pouvez voir les mesures suivantes.

* **Journaux Des Exécutions Ayant Échoué**
Ce tableau répertorie chaque exécution de scénario d’échec ou d’avertissement dans votre organisation. Vous pouvez ainsi rechercher et résoudre les problèmes d’exécution sans quitter le tableau de bord.
* **Opérations de l’organisation**
Ce graphique permet d’afficher le nombre d’opérations utilisées dans votre organisation. Vous pouvez sélectionner des équipes ou des scénarios spécifiques et afficher les opérations de la dernière semaine, du dernier mois ou de la dernière année.
* **Principaux scénarios par opération**
Ce graphique vous permet d’afficher les scénarios qui utilisent le plus d’opérations. Vous pouvez sélectionner des équipes spécifiques ou afficher les données du dernier jour, de la dernière semaine ou du dernier mois.

<!--

* **Executions waiting to be processed**
   This chart shows the number of executions waiting to be processed (also known as the execution backlog) at a given point in time. 

   A high number of executions waiting to be processed may affect performance in your Fusion instance. You will receive a notification if your execution backlog reaches 5000 executions. We recommend identifying responsible scenarios and modifying or disabling them. If the high execution backlog persists, the Fusion team will protect the performance of your Fusion instance by disabling the responsible scenarios.
* **Pool Utilization**
   This chart shows worker pool utilization over time. If this chart routinely shows worker pool utilization, you may want to assign some scenarios to another pool.

   If a pool is nearing 100% utilization, other resources that use the same pool may be delayed or disrupted. If this occurs, we recommend reassigning a high-usage scenario to another worker pool, or modifying existing scenarios to be less resource intensive.
* **Executions per scenario**
   This chart displays executions per scenario. Different colors represent different scenarios. When you hover over the chart, a window appears that shows which color is which scenario.

   You can use this chart to identify which scenarios may be causing an execution backlog or high worker pool utilization. 
* **Duration of executions**
   This chart displays executions per scenario. Different colors represent different scenarios. When you hover over the chart, a window appears that shows which color is which scenario.

   You can use this chart to identify scenarios that are taking longer than usual, including those affected by issues with a connected app or service.

-->

## Affichage du tableau de bord Fusion Insights

1. Dans Fusion, cliquez sur **Insights** dans le volet de navigation de gauche.

   Le tableau de bord s’ouvre.

1. Pour afficher les données à un moment donné, passez la souris sur un tableau de bord et placez le curseur sur le moment voulu pour l’afficher.

   Une ligne s’affiche au-dessus de ce moment dans tous les graphiques, et une fenêtre affichant les données de ce moment s’affiche sur chaque graphique.
1. Pour afficher les données d’un scénario spécifique dans le graphique Exécutions par scénario ou Durée des exécutions, cliquez sur une barre de couleur du scénario pour lequel vous souhaitez afficher les données. Pour revenir à la vue affichant tous les scénarios, cliquez de nouveau sur le graphique.
1. Pour accéder à un scénario spécifique affiché dans le graphique Exécutions par scénario ou le graphique Durée des exécutions, faites un clic droit sur une barre de couleur du scénario et sélectionnez **Ouvrir le scénario dans un nouvel onglet**.
1. Pour développer un graphique, cliquez sur l’icône **Développer** ![icône Développer](assets/expand-icon.png) dans le coin supérieur droit de ce graphique.
1. Pour modifier la période du tableau de bord, sélectionnez le champ Période dans le coin supérieur droit du tableau de bord, puis sélectionnez une nouvelle période. La période disponible la plus longue est de 24 heures et la plus courte est de 15 minutes.
1. Pour actualiser les graphiques, cliquez sur l’icône Actualiser située en haut à droite du tableau de bord.
1. Pour afficher un autre pool de traitement, cliquez sur le champ Pool près du coin supérieur gauche du tableau de bord, puis sélectionnez le pool à afficher.

## Personnalisation du tableau de bord Insights

Vous pouvez choisir les widgets qui apparaissent dans le tableau de bord des Insights et dans quel ordre.

### Ajout, suppression ou réorganisation de widgets

1. Dans le volet de navigation de gauche, cliquez sur **Insights** ![icône Insights](assets/insights-icon.png).
1. Cliquez sur **[!UICONTROL Personnaliser]** dans l’en-tête Insights.

   Un panneau latéral s’ouvre. Il répertorie chaque widget sous la forme d’une carte qui affiche un aperçu, le nom du widget et une description.

1. Pour afficher ou masquer un widget, cliquez sur sa carte ou cliquez sur le bouton **[!UICONTROL Ajouter un widget]** ou **[!UICONTROL Supprimer le widget]** sur la carte.

   Les widgets affichés comportent une coche.
1. Pour réorganiser les widgets, faites glisser une vignette de widget vers un nouvel emplacement dans le panneau.

   Un espace réservé en tirets et une barre de dépôt indiquent l’endroit où la carte se posera.

Vos choix sont enregistrés par navigateur. Les widgets ajoutés dans les versions ultérieures s’affichent automatiquement dans le panneau.

Si vous supprimez tous les widgets, la page affiche un message « Aucun widget sur cette page ».

## Actualiser le tableau de bord des informations

Pour recharger les données de chaque widget, cliquez sur **[!UICONTROL Actualiser]** en regard de **[!UICONTROL Personnaliser]**.

* Chaque widget conserve ses filtres.
* Le bouton **[!UICONTROL Actualiser]** affiche un statut En attente jusqu’à ce que tous les widgets aient terminé leur chargement.
* Les graphiques conservent le graphique précédent sous une double flèche de chargement et le journal des exécutions estompe son tableau sous une double flèche pendant le rechargement des données.
* Si une actualisation échoue, les widgets conservent leurs dernières données correctes.

## Suivez la visite guidée des insights

La première fois que vous ouvrez le tableau de bord Insights, une boîte de dialogue de bienvenue vous offre la possibilité de commencer une visite ou de l’ignorer.

La visite met en surbrillance chaque widget, dans l’ordre enregistré, ainsi que le bouton et le panneau **[!UICONTROL Personnaliser]**, le bouton **[!UICONTROL Actualiser]** et le bouton **[!UICONTROL Relire la visite]** dans la barre de titre.

Pour redémarrer la visite à tout moment, cliquez sur l’icône d’informations de la visite ![icône d’informations](assets/insights-tour-information.png) dans la barre de titre.

La visite ne commence pas lorsque vous ouvrez le tableau de bord Insights à partir d’un lien dans un scénario. Pour plus d’informations, voir [Ouvrir le tableau de bord Insights à partir d’un scénario](#open-the-insights-dashboard-from-a-scenario) dans cet article.

## Rechercher des scénarios et des équipes par ID

Dans les widgets **[!UICONTROL Opérations de l’organisation]** et **[!UICONTROL Principaux scénarios par opérations]**, les champs **[!UICONTROL Scénario]** et **[!UICONTROL Équipe]** correspondent sur l’ID et le nom. Chaque option affiche son identifiant sous le nom , par exemple « ID 123 ».

* Les listes chargent les 500 premiers scénarios et les 200 premières équipes. Si vous saisissez un ID qui ne figure pas dans la liste chargée, Fusion le recherche automatiquement après un court délai.
* Si vous effacez un scénario, l’équipe qui a été remplie automatiquement pour ce scénario est également effacée.

>[!NOTE]
>
>Le filtre de scénario dans le journal des exécutions ne correspond pas à l’ID .

## Ouverture du tableau de bord Insights à partir d’un scénario

Vous pouvez ouvrir le tableau de bord des informations avec le widget **[!UICONTROL Opérations d’organisation]** filtré pour un scénario et une équipe spécifiques.

Pour accéder à la page Insights à partir d’un scénario :

1. Ouvrez la page de détails du scénario :

   1. Cliquez sur l’onglet **[!UICONTROL Scenario]** dans le panneau de gauche, puis sur un scénario dont vous souhaitez obtenir des détails.

      Ou

      Si vous travaillez sur le scénario dans l’éditeur de scénarios, cliquez sur la flèche de gauche ![flèche de modification de sortie](assets/exit-editing-arrow.png) près du coin supérieur gauche de la fenêtre.
      1. Cliquez sur l’onglet **Rapports** en haut de la page.

* Le widget **[!UICONTROL Opérations de l’organisation]** s’ouvre, filtré pour ce scénario et cette équipe, et la page défile jusqu’au widget.
* Si vous avez supprimé le widget de la page, un avertissement avec un bouton **[!UICONTROL Ajouter un widget]** s’affiche à la place.

## Utiliser le mode sombre

Le tableau de bord Insights et ses widgets suivent automatiquement les paramètres du mode sombre. Lorsque vous modifiez le paramètre, la page est immédiatement mise à jour, sans rechargement, et conserve votre état actuel. Le mode clair reste inchangé.

## Accès au widget Performances

Le widget **[!UICONTROL Performances]** ne s’affiche que pour les utilisateurs et utilisatrices disposant de l’une des autorisations suivantes :

* Organisation Modifier dans l’organisation active
* Vue Organisation dans la page d’administration.

Le widget est masqué de la page et du panneau **[!UICONTROL Personnaliser]** pour les autres utilisateurs. Si l’accès est accordé ultérieurement à un utilisateur, le widget revient à sa position enregistrée. L’ouverture directe de l’URL d’Insights ne contourne pas cette vérification.

## Filtrer et trier les exécutions dans le journal d’exécution

Utilisez le Journal d’exécution pour rechercher les exécutions de scénario ayant échoué ou renvoyé un avertissement dans l’ensemble de votre organisation, et réactivez tous les scénarios qui ont été automatiquement désactivés après des échecs répétés.

1. Dans le journal d’exécution, filtrez les exécutions selon l’une des méthodes suivantes :

   * [!UICONTROL Équipe]
   * [!UICONTROL Scénario]
   * [!UICONTROL Type d’exécution]
   * [!UICONTROL Période &#x200B;]
   * [!UICONTROL État de désactivation]
   * [!UICONTROL &#x200B; Message d’erreur &#x200B;]

   Pour la plupart des filtres, vous pouvez choisir de ne faire correspondre que les valeurs sélectionnées ou tout le reste, à l’exception de celles-ci.

1. Cliquez sur une exécution pour afficher plus de détails sur son erreur.
1. Pour réactiver un ou plusieurs scénarios qui ont été automatiquement désactivés après des échecs répétés, sélectionnez les exécutions, puis cliquez sur **Activer**.

   >[!NOTE]
   >
   >Avant de réactiver un scénario, recherchez la cause de ses échecs, tels que des informations d’identification expirées ou un problème de connecteur, afin que le scénario n’échoue pas immédiatement à nouveau.
