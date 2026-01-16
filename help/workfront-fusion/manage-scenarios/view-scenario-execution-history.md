---
title: Afficher l’historique de l’exécution d’un scénario
description: Vous pouvez afficher des informations sur les événements ou les exécutions d’un scénario, ou vous pouvez rechercher des données spécifiques dans toutes les exécutions du scénario.
author: Becky
feature: Workfront Fusion
exl-id: 974b32b4-d86a-48cd-a8d4-1ae2cf309b9b
source-git-commit: ab12dbf0dbad25a8300eb1201fa3e0fde9148acc
workflow-type: tm+mt
source-wordcount: '911'
ht-degree: 65%

---

# Afficher l’historique de l’exécution d’un scénario

Vous pouvez afficher des informations sur les événements ou les exécutions d’un scénario, ou vous pouvez rechercher des données spécifiques dans toutes les exécutions du scénario.

L’exécution d’un scénario représente une seule exécution du scénario.

Un événement de scénario est une modification apportée au scénario, par exemple la modification, l’activation ou la désactivation de celui-ci.

>[!NOTE]
>
>L’historique d’un scénario affiche toutes les exécutions d’un scénario au cours des 30 derniers jours.

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

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation Workfront](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Afficher l’historique des scénarios


### Affichage de l’historique des scénarios dans l’onglet Historique

L’onglet [!UICONTROL Historique] affiche plus de détails que la page [!UICONTROL Détails du scénario]. Vous pouvez également filtrer et trier les exécutions dans l’onglet [!UICONTROL Historique].

>[!NOTE]
>
>Si vous affichez l’historique d’un scénario pendant son exécution, Fusion affiche une note vous informant que les données sont toujours en cours de traitement et seul l’historique partiel du scénario s’affiche jusqu’à ce que le traitement soit terminé.

1. Cliquez sur l’onglet **[!UICONTROL Scénario]** dans le panneau de gauche, puis sur le scénario.

   Ou

   Si vous travaillez sur le scénario dans l’éditeur de scénarios, cliquez sur la flèche de gauche ![flèche de modification de sortie](assets/exit-editing-arrow.png) près du coin supérieur gauche de la fenêtre.

1. Cliquez sur **Historique** près du nom du scénario.
   ![onglet historique](assets/history-tab.png)

   Les détails suivants sont répertoriés pour chaque exécution du scénario :

   * Date à laquelle l’exécution a été **[!UICONTROL démarrée]**.
   * ID d’exécution
   * **[!UICONTROL Statut]** (succès ou échec)
   * **[!UICONTROL Durée]** de l’exécution
   * Nombre d’**[!UICONTROL opérations]**
   * Taille du **[!UICONTROL transfert de données]**

   >[!NOTE]
   >
   >L’historique des scénarios affiche un badge de **traitement** en regard des scénarios récemment exécutés, tandis que les détails de l’exécution sont écrits dans le stockage. Le traitement se produit immédiatement après l’exécution du scénario et ne doit pas durer plus de quelques minutes. Les détails de l’exécution du scénario peuvent ne pas être visibles pendant le traitement de l’exécution.

1. Pour afficher les détails d’exécution d’un scénario spécifique, cliquez sur **Détails** à l’extrême droite. Le lien [!UICONTROL Détails] n’est visible que si les détails de l’exécution sont disponibles.

   Pour plus d’informations sur l’affichage des détails d’exécution du scénario, voir [Afficher une exécution de scénario spécifique](/help/workfront-fusion/manage-scenarios/view-a-specific-scenario-execution.md).
1. Pour afficher les événements, activez le bouton (bascule) **Afficher les événements**.


### Afficher l’historique du scénario sur la page Détails du scénario


1. Cliquez sur l’onglet **[!UICONTROL Scénario]** dans le panneau de gauche, puis sur le scénario.

   Ou

   Si vous travaillez sur le scénario dans l’éditeur de scénarios, cliquez sur la flèche de gauche ![flèche de modification de sortie](assets/exit-editing-arrow.png) près du coin supérieur gauche de la fenêtre.

1. Cliquez sur l’onglet **[!UICONTROL Historique]** dans le panneau de droite.
1. (Facultatif) Pour plus d’informations sur l’exécution d’un scénario sélectionné, cliquez sur l’exécution dans le panneau de droite.

   Pour plus d’informations sur le traitement des lots, voir [Flux d’exécution de scénario](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md)

   >[!NOTE]
   >
   >* L’historique des scénarios affiche un badge **Historique de traitement** en regard des scénarios récemment exécutés, tandis que les détails de l’exécution sont écrits dans le stockage. Le traitement se produit immédiatement après l’exécution du scénario et ne doit pas durer plus de quelques minutes. Les détails de l’exécution du scénario peuvent ne pas être visibles pendant le traitement de l’exécution.

1. Pour afficher les événements, cliquez sur l’onglet **Événements**.

## Filtrer l’historique d’exécution des scénarios

Vous pouvez filtrer l’historique d’exécution pour n’afficher que les exécutions disposant des valeurs spécifiées.

1. Ouvrez l’historique pleine page d’un scénario comme décrit dans [Afficher l’historique de l’exécution d’un scénario sur l’onglet [!UICONTROL Historique]](#view-scenario-history-on-the-history-tab) de cet article.
1. Cliquez sur l’icône [!UICONTROL filtre] ![icône de filtre de scénario](assets/fusion-scenario-filter-icon.png) dans l’en-tête de la colonne selon laquelle vous souhaitez effectuer le filtrage.
1. Dans la boîte de dialogue [!UICONTROL filtre], saisissez les valeurs à utiliser pour filtrer les données.
1. Cliquer sur **[!UICONTROL Enregistrer]**.

L’icône de filtre est orange dans les colonnes avec un filtre actif.

<!-- don't see how to do this
## Sort the scenario execution history

You can sort the scenario execution history.

1. Open the full-page history for a scenario as described in [View scenario execution history on the [!UICONTROL History] tab](#view-scenario-execution-history-on-the-history-tab) in this article.
1. Click the [!UICONTROL Sort] icon in the header of the column you want to filter by.
1. Optional: To reverse the order of the sort, click the [!UICONTROL Sort] icon again.
-->

## Rechercher toutes les exécutions d’un scénario

1. Ouvrez l’historique pleine page d’un scénario comme décrit dans [Afficher l’historique de l’exécution d’un scénario sur l’onglet [!UICONTROL Historique]](#view-scenario-history-on-the-history-tab) de cet article.
1. Cliquez sur **[!UICONTROL Recherche de texte intégral]** en haut de la liste des exécutions.

   Ou

   Saisir **Ctrl+Maj+F** (Windows) ou **Cmd+Maj+F** (Mac)
La fenêtre [!UICONTROL Rechercher l’historique] s’ouvre.

1. (Facultatif) Pour rechercher des exécutions qui contiennent du texte spécifique, saisissez le texte dans la barre de recherche de la fenêtre **[!UICONTROL Rechercher l’historique]**.

   Pour rechercher du texte exact, entourez le texte de guillemets anglais doubles (&quot;exemple&quot;).

   >[!INFO]
   >
   >**Exemple :** si vous souhaitez trouver l’exécution qui a créé un projet spécifique, saisissez l’ID du projet dans la barre [!UICONTROL Recherche de texte intégral].
   >
   >&quot;625ef2ef0006036bd1794b6e52d737c5&quot;

1. (Facultatif) Pour limiter votre recherche par période, sélectionnez les dates de début et de fin de votre recherche dans la zone [!UICONTROL Par période].

   >[!NOTE]
   >
   >* Les exécutions ne sont disponibles que pendant les 30 jours précédents.
   >
   >* Workfront Fusion stocke les payloads de webhook pendant 30 jours. L’accès à un payload de webhook plus de 30 jours après sa création génère l’erreur « [!UICONTROL Échec de la lecture du fichier à partir du stockage.] »


1. (Facultatif) Pour limiter votre recherche par statut, sélectionnez le statut de votre choix dans le menu déroulant **[!UICONTROL Par statut]**.


   Les statuts disponibles sont les suivants :

   * [!UICONTROL Tous]

   * [!UICONTROL Erreur]

   * [!UICONTROL Avertissement]

   * [!UICONTROL Succès]

1. (Facultatif) Modifiez l’ordre dans lequel les résultats s’affichent dans le menu déroulant **[!UICONTROL Trier par date]**.

1. (Facultatif) Pour copier un ID d’exécution de scénario, cliquez sur l’icône **[!UICONTROL Copier l’ID d’exécution]** <img src="assets/copy-fusion-execution-id-icon.png"> dans la ligne de l’exécution souhaitée.

1. (Facultatif) Cliquez sur un résultat de la [!UICONTROL recherche de texte intégral] pour examiner le lot de sortie du module de scénario qui contient les informations.
