---
title: Afficher et résoudre les exécutions incomplètes
description: Le dossier [!UICONTROL Incomplete executions] stocke les exécutions de scénario qui n’ont pas été finalisées avec succès en raison d’une erreur. Chaque exécution incomplète stockée peut être résolue manuellement ou automatiquement.
author: Becky
feature: Workfront Fusion
exl-id: 974b32b4-d86a-48cd-a8d4-1ae2cf309b9b
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 31%

---

# Affichage de l’historique d’exécution d’un scénario

Vous pouvez afficher des informations sur les événements ou les exécutions d’un scénario, ou vous pouvez rechercher des données spécifiques dans toutes les exécutions du scénario.

L’exécution d’un scénario représente une seule exécution du scénario.

Un événement de scénario est une modification apportée au scénario, par exemple la modification, l’activation ou la désactivation de celui-ci.

>[!NOTE]
>
>L’historique d’un scénario affiche tous les événements et exécutions d’un scénario au cours des 30 derniers jours.

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] paquet</td> 
   <td> <p>Tous</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licence</td> 
   <td> <p>Nouveau : [!UICONTROL Standard]</p><p>Ou</p><p>En cours : [!UICONTROL Work] ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licence**</td> 
   <td>
   <p>Actuelle : aucune exigence de licence [!DNL Workfront Fusion] requise.</p>
   <p>Ou</p>
   <p>Héritée : n’importe laquelle. </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Nouveau :</p> <ul><li>[!UICONTROL Select] ou [!UICONTROL Prime] plan de [!DNL Workfront] : votre entreprise doit acheter des [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] plan : [!DNL Workfront Fusion] est inclus.</li></ul>
   <p>Ou</p>
   <p>Actuel : votre entreprise doit acheter [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurations du niveau d’accès*</td> 
   <td> 
     <p>Vous devez être un administrateur ou une administratrice [!DNL Workfront Fusion] de votre organisation.</p>
     <p>Vous devez être un administrateur ou une administratrice [!DNL Workfront Fusion] de votre équipe.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Afficher l’historique des scénarios


### Affichage de l’historique des scénarios dans l’onglet Historique

L’onglet [!UICONTROL History] affiche plus de détails que ce qui est disponible sur la page [!UICONTROL Scenario detail]. Vous pouvez également filtrer et trier les exécutions dans l’onglet [!UICONTROL History] .

1. Cliquez sur l’onglet **[!UICONTROL Scenario]** dans le panneau de gauche, puis sur le scénario.

   Ou

   Si vous travaillez sur le scénario dans l’éditeur de scénarios, cliquez sur la flèche de gauche ![flèche de modification de sortie](assets/exit-editing-arrow.png) près du coin supérieur gauche de la fenêtre.

1. Cliquez sur **Historique** près du nom du scénario.
   ![onglet historique](assets/history-tab.png)

   Les détails suivants sont répertoriés pour chaque exécution du scénario :

   * Date de **[!UICONTROL Started]** de l’exécution
   * ID d’exécution
   * **[!UICONTROL Status]** (succès ou échec)
   * Exécuter **[!UICONTROL Duration]**
   * Nombre de **[!UICONTROL Operations]**
   * Taille du **[!UICONTROL Data Transfer]**

   >[!NOTE]
   >
   >L’historique des scénarios affiche un badge de **traitement** en regard des scénarios récemment exécutés, tandis que les détails de l’exécution sont écrits dans le stockage. Le traitement se produit immédiatement après l’exécution du scénario et ne doit pas durer plus de quelques minutes. Les détails de l’exécution du scénario peuvent ne pas être visibles pendant le traitement de l’exécution.

1. Pour afficher les détails d’exécution d’un scénario spécifique, cliquez sur **Détails** à l’extrême droite. Le lien [!UICONTROL details] n’est visible que si des détails sont disponibles pour l’exécution.
1. Pour afficher les événements, activez le bouton (bascule) **Afficher les événements**.


### Afficher l’historique du scénario sur la page Détails du scénario


1. Cliquez sur l’onglet **[!UICONTROL Scenario]** dans le panneau de gauche, puis sur le scénario.

   Ou

   Si vous travaillez sur le scénario dans l’éditeur de scénarios, cliquez sur la flèche de gauche ![flèche de modification de sortie](assets/exit-editing-arrow.png) près du coin supérieur gauche de la fenêtre.

1. Cliquez sur l’onglet **[!UICONTROL History]** dans le panneau de droite.
1. (Facultatif) Pour plus d’informations sur l’exécution d’un scénario sélectionné, cliquez sur l’exécution dans le panneau de droite.

   Pour plus d’informations sur le traitement des lots, voir [Flux d’exécution de scénario](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md)

   >[!NOTE]
   >
   >* L’historique des scénarios affiche un badge **Historique de traitement** en regard des scénarios récemment exécutés, tandis que les détails de l’exécution sont écrits dans le stockage. Le traitement se produit immédiatement après l’exécution du scénario et ne doit pas durer plus de quelques minutes. Les détails de l’exécution du scénario peuvent ne pas être visibles pendant le traitement de l’exécution.

1. Pour afficher les événements, cliquez sur l’onglet **Événements**.

## Filtrer l’historique d’exécution des scénarios

Vous pouvez filtrer l’historique d’exécution pour n’afficher que les exécutions disposant des valeurs spécifiées.

1. Ouvrez l’historique pleine page d’un scénario, comme décrit dans la section [Afficher l’historique d’exécution du scénario sur l’onglet [!UICONTROL History]](#view-scenario-history-on-the-history-tab) dans cet article.
1. Cliquez sur l’icône [!UICONTROL filter] ![icône de filtre de scénario](assets/fusion-scenario-filter-icon.png) dans l’en-tête de la colonne selon laquelle vous souhaitez effectuer le filtrage.
1. Dans la boîte de dialogue [!UICONTROL filter], saisissez les valeurs en fonction desquelles vous souhaitez effectuer le filtrage.
1. Cliquez sur **[!UICONTROL Save]**.

L’icône de filtre est orange dans les colonnes avec un filtre actif.

<!-- don't see how to do this
## Sort the scenario execution history

You can sort the scenario execution history.

1. Open the full-page history for a scenario as described in [View scenario execution history on the [!UICONTROL History] tab](#view-scenario-execution-history-on-the-history-tab) in this article.
1. Click the [!UICONTROL Sort] icon in the header of the column you want to filter by.
1. Optional: To reverse the order of the sort, click the [!UICONTROL Sort] icon again.
-->

## Rechercher toutes les exécutions d’un scénario

1. Ouvrez l’historique pleine page d’un scénario, comme décrit dans la section [Afficher l’historique d’exécution du scénario sur l’onglet [!UICONTROL History]](#view-scenario-history-on-the-history-tab) dans cet article.
1. Cliquez sur **[!UICONTROL Fulltext search]** en haut de la liste des exécutions.

   Ou

   Tapez **Ctrl+Maj+F** (Windows) ou **Cmd+Maj+F** (Mac)
La fenêtre [!UICONTROL Search in history] s’ouvre.

1. (Facultatif) Pour rechercher des exécutions contenant du texte spécifique, saisissez ce texte dans la barre de recherche de la fenêtre de **[!UICONTROL Search in history]**.

   Pour rechercher du texte exact, entourez le texte de guillemets anglais doubles (&quot;exemple&quot;).

   >[!INFO]
   >
   >**Exemple :** si vous souhaitez trouver l’exécution qui a créé un projet spécifique, saisissez l’ID du projet dans la barre de [!UICONTROL Fulltext search].
   >
   >&quot;625ef2ef0006036bd1794b6e52d737c5&quot;

1. (Facultatif) Pour limiter votre recherche par période, sélectionnez les dates de début et de fin de la recherche souhaitée dans la zone [!UICONTROL By date range].

   >[!NOTE]
   >
   >* Les exécutions ne sont disponibles que pendant les 30 jours précédents.
   >
   >* [!DNL Workfront Fusion] stocke les payloads des webhooks pendant 30 jours. L’accès à une payload webhook plus de 30 jours après sa création entraîne l’erreur « [!UICONTROL Failed to read file from storage.] »


1. (Facultatif) Pour limiter votre recherche par statut, sélectionnez le statut souhaité dans la liste déroulante **[!UICONTROL By status]** .


   Les statuts disponibles sont les suivants :

   * [!UICONTROL All]

   * [!UICONTROL Error]

   * [!UICONTROL Warning]

   * [!UICONTROL Success]

1. (Facultatif) Modifiez l’ordre dans lequel les résultats s’affichent dans la liste déroulante **[!UICONTROL Sort by dates]**.

1. (Facultatif) Pour copier l’identifiant d’exécution d’un scénario, cliquez sur l’icône **[!UICONTROL Copy execution ID]** <img src="assets/copy-fusion-execution-id-icon.png"> dans la ligne de l’exécution souhaitée.

1. (Facultatif) Cliquez sur un résultat du [!UICONTROL Fulltext search] pour examiner le lot de sortie du module de scénario qui contient les informations.
