---
title: Ajouter un filtre à un scénario
description: Dans certains scénarios, vous devez travailler uniquement avec des lots qui répondent à des critères spécifiques. Les filtres vous permettent de sélectionner ces lots.
author: Becky
feature: Workfront Fusion
exl-id: b507dca0-0e85-4ab7-8310-b6e6bcb7ae12
source-git-commit: bec838423e13c3efe4f3d002f824c203cad6ecf8
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 46%

---

# Ajouter un filtre à un scénario

Dans certains scénarios, vous devez travailler uniquement avec des lots qui répondent à des critères spécifiques. Les filtres vous permettent de sélectionner ces lots.

Par exemple, vous pouvez créer un scénario avec le déclencheur [!UICONTROL Observer des enregistrements] pour que Workfront capture uniquement les tâches affectées à un utilisateur spécifique.

Vous pouvez ajouter un filtre entre deux modules et vérifier si les lots reçus des modules précédents remplissent des conditions de filtrage spécifiques :

* Si tel est le cas, les lots sont transmis au module suivant dans le scénario.
* Dans le cas contraire, le traitement des lots s’arrête.

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

## Conditions préalables

Vous devez ajouter les deux modules à un scénario avant de pouvoir ajouter un filtre entre eux.

## Ajoutez un filtre entre deux modules :

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez ajouter un filtre.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Cliquez sur l’icône de clé à molette ![icône de clé à molette](assets/wrench-icon.png) entre les modules auxquels vous souhaitez ajouter un filtre, puis sélectionnez **Configurer un filtre**.
1. Dans la zone qui s’affiche, saisissez un **[!UICONTROL Libellé]** pour le filtre.
1. Définissez le filtre **[!UICONTROL Condition]**.

   Saisissez le champ selon lequel vous souhaitez filtrer dans le premier champ, l’opérateur et (si nécessaire) la valeur avec laquelle vous souhaitez comparer le champ.

   >[!TIP]
   >
   >Vous pouvez saisir des valeurs dans les champs de filtre à partir du panneau de mappage
   >Pour plus d’informations sur le mappage, voir [Mapper des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

   Par exemple, si vous souhaitez que le filtre transmette les fichiers dans Adobe Workfront se terminant par XML, vous devez saisir **[!UICONTROL Nom du fichier]** dans la première zone et ..**[!UICONTROL xml]** dans le second champ. Dans le menu déroulant qui sépare les champs, vous pouvez sélectionner **[!UICONTROL Se termine par (non sensible à la casse)]**. Ce filtre s’applique aux lots entrants du premier module (Workfront). Seuls les lots contenant des fichiers XML sont transmis au module suivant.

   ![Configurer un filtre](assets/set-up-filter-box.png)

1. Cliquez sur **[!DNL OK]**.

## Copier un filtre

Vous pouvez copier un filtre existant et le coller ailleurs dans le scénario.

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez ajouter un filtre.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Cliquez avec le bouton droit sur les points de connexion entre les modules où se trouve le filtre.
1. Sélectionnez **Copier le filtre**.
1. Cliquez avec le bouton droit sur les points de connexion entre les modules où vous souhaitez coller le filtre.
1. Sélectionner **Coller le filtre
1. (Facultatif) Pour ajuster le filtre, cliquez sur l’icône ou le libellé du filtre et saisissez les valeurs comme décrit dans [Ajouter un filtre entre deux modules](#add-a-filter-between-two-modules) dans cet article.




<!--

Currently, the scenario editor does include a feature for copying a filter.

>[!NOTE]
>
>If you copy the modules on either side of the filter, the filter is also copied.
>
>For more information on copying modules, see [Copy modules or scenarios in Adobe Workfront Fusion](/help/workfront-fusion/create-scenarios/add-modules/copy-modules-or-scenarios.md).

To copy a filter without copying modules, you can use the Fusion DevTool

1. Click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Select the scenario where you want to add a filter.
1. Click anywhere on the scenario to enter the Scenario editor.
1. Open the Fusion DevTool by clicking on the DevTool icon ![DevTool icon](assets/debugger-icon.png) near the bottom of the screen.
   
   If you do not see the DevTool icon, see [Debug a scenario](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md) for instructions on opening the DevTool.
   
1. Click the **[!UICONTROL Tools]** icon ![DevTool tools](assets/devtools-tools-icon.png) in the left side bar.

1. Click **[!UICONTROL Copy Filter]**, then configure the **[!UICONTROL Copy Filter]** tool in the right side panel:

   1. Set the **[!UICONTROL Source Module]** as the module directly after the filter you want to copy.
   1. Set the **[!UICONTROL Target Module]** as the module that you want to place the filter directly after.

1. Click **[!UICONTROL Run]**.

-->
