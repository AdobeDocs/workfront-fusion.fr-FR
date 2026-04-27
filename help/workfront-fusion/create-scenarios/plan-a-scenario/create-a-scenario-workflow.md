---
title: Workflow de création d’un scénario
description: Follow this general workflow to create a scenario
author: Becky
feature: Workfront Fusion
exl-id: 49f8edd7-e29a-4ead-9134-a9f0d1cc244d
source-git-commit: 0390bb875eb10278967d7d1c9cd61e5243e5f37e
workflow-type: tm+mt
source-wordcount: '782'
ht-degree: 21%

---

# Workflow de création d’un scénario

Scenarios are built to meet the needs of your organization, with applications and modules that address your use cases. However, creating a scenario follows the same basic workflow regardless of use case. This article describes the basic process of creating a scenario.


* [Create and name the scenario](#create-and-name-the-scenario)
* [Ajouter et configurer le premier module](#configure-the-first-module)
* [Créer des connexions](#create-connections)
* [Add and configure additional modules](#add-and-configure-additional-modules)
* [Map data between modules](#map-data-between-modules)
* [Configure routing](#configure-routing)
* [Configurer la gestion des erreurs](#configure-error-handling)
* [Configurer les paramètres de scénario](#onfigure-scenario-settings)
* [Test and revise](#test-and-revise)
* [Activer le scénario](#activate-the-scenario)
* [Raccourcis clavier du scénario Workfront Fusion](#workfront-fusion-scenario-keyboard-shortcuts)

Raccourcis clavier



## Create and name the scenario

1. Sign into your Workfront Fusion account.
1. Cliquez sur **[!UICONTROL Scénarios]** ![icône Scénarios](assets/scenarios-icon.png) dans le panneau de gauche.

   >[!NOTE]
   >
   >Si le panneau de navigation de gauche ou ses icônes ne s’affichent pas, cliquez sur l’icône menu ![Menu](assets/main-menu-icon-left-nav.png).

1. (Optional)In the [!UICONTROL **Folders**] panel, click the **[!UICONTROL Add folder]** icon ![Add folder icon](assets/add-folder-icon.png), then type a name like &quot;Practice scenarios&quot; for your first folder.

1. (Optional) Open the folder, then click **[!UICONTROL Create a new scenario]** in the upper-right corner of the page.

1. Sélectionnez le nom de l’espace réservé **[!UICONTROL Nouveau scénario]** dans le coin supérieur gauche, puis saisissez un nom tel que « Scénario pratique 1 ».

   ![Name the scenario](assets/name-the-scenario.png)

1. Continue with [Connect the first module](#2-connect-the-first-module) below.

## Ajouter et configurer le premier module

The first module for your scenario is a trigger module, which will start the scenario when certain conditions are met.

For instructions on adding the first module to a scenario, see [Add the first module to a scenario](/help/workfront-fusion/create-scenarios/add-modules/add-a-module-basic.md#add-the-first-module-to-a-scenario) in the article Add a module to a scenario.

For instructions on configuring a module, see [Configure a module](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md)

## Créer des connexions

When configuring a module, you must enter or create a connection. The module uses this connection and the permissions it contains to access date in the application.

For basic instructions on how to create a connection, see [Create a connection - Basic instructions](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md).

For specific use cases involving Google, Microsoft, or applications without dedicated connectors, see the other articles under [Connect to applications: article index](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-apps-toc.md).

## Add and configure additional modules

Continue adding and configuring additional modules.

Pour obtenir des instructions sur l’ajout de modules, consultez les articles répertoriés sous [Ajouter des modules : index des articles](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

## Mappage des données entre les modules

Vous pouvez utiliser la sortie des modules précédents comme entrée dans les modules suivants. Par exemple, vous pouvez créer un projet Workfront dans un module et charger un document dans ce module dans un module suivant.

Pour obtenir des instructions, consultez les articles sous [Mapper des données : index d’article](/help/workfront-fusion/create-scenarios/map-data/map-data-toc.md).

## Configurer le routage

Le routage permet au scénario d’effectuer différentes actions en fonction des valeurs des données.

Pour obtenir des instructions, voir [Ajouter un module Routeur et configurer des itinéraires](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).

## Configurer la gestion des erreurs

La gestion des erreurs permet au scénario de récupérer après une erreur. Vous pouvez choisir la manière dont vous souhaitez que le scénario réagisse dans différentes situations d’erreur.

Pour obtenir des instructions, voir [Ajouter la gestion des erreurs](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md).

## Configurer les paramètres de scénario

Vous pouvez configurer des paramètres pour votre scénario dans son ensemble, par exemple pour planifier un scénario, prendre des notes ou déterminer comment les données sont stockées.

Pour obtenir des instructions, consultez les articles sous [Configurer les paramètres de scénario : index d’article](/help/workfront-fusion/create-scenarios/config-scenarios-settings/config-scenario-settings-toc.md).

## Tester et réviser

Le test de votre scénario vous permet de déterminer si celui-ci fonctionne comme prévu. Vous pouvez ensuite réviser le scénario en fonction de vos résultats, puis effectuer un nouveau test.

1. Cliquez sur **[!UICONTROL Exécuter une fois]** dans le coin inférieur gauche de l’éditeur de scénario.
1. Une fois l’exécution du scénario terminée, cliquez sur la bulle de l’inspecteur d’exécution au-dessus de chaque module pour afficher l’entrée des informations et la sortie de ce module.

   * Pour obtenir des informations générales sur la lecture des informations d’exécution de scénario, voir [Flux d’exécution de scénario](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md).
   * Pour plus d’informations sur les lots traités, voir [Exécution de scénario, cycles et phases dans Adobe Workfront Fusion](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).

1. Dans Workfront Fusion, cliquez sur **[!UICONTROL Enregistrer]** ![Icône Enregistrer](assets/save-icon.png) près du coin inférieur gauche pour enregistrer votre progression dans le scénario.

   >[!IMPORTANT]
   >
   >Sauvegardez souvent lorsque vous affinez et testez un scénario.

## Activer le scénario

Une fois que vous avez activé un scénario, celui-ci s’exécute par défaut toutes les 15 minutes. Vous pouvez modifier cela en définissant quand et à quelle fréquence vous souhaitez qu’il s’exécute.

Pour plus d’informations sur l’activation des scénarios, voir [&#x200B; Activer ou désactiver un scénario](/help/workfront-fusion/manage-scenarios/activate-deactivate-scenarios.md).

Pour plus d’informations sur les planifications, voir [Planification d’un scénario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

## Raccourcis clavier du scénario Workfront Fusion

Vous pouvez utiliser les raccourcis clavier suivants lors de la création ou de la modification d’un scénario :

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <thead> 
  <tr> 
   <th> <p>Action</p> </th> 
   <th>[!DNL Windows]</th> 
   <th> <p>[!DNL MacOS]</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Save] </td> 
   <td>Ctrl+Maj+S</td> 
   <td>Cmd+Maj+S</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Run Once]</td> 
   <td>Ctrl+Maj+Entrée</td> 
   <td>Cmd+Maj+Entrée</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ouvrir l’outil de développement]</td> 
   <td>F12</td> 
   <td>Ctrl+Fn+F12</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select multiple modules]</td> 
   <td>Shift+Drag</td> 
   <td>Shift+Drag</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy]</td> 
   <td>Ctrl+C</td> 
   <td>Cmd+C</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Paste]</td> 
   <td>Ctrl+V</td> 
   <td>Cmd+V</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search for modules]</td> 
   <td>Ctrl+K</td> 
   <td>Cmd+K</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Paste cURL into scenario to create HTTP module</td> 
   <td colspan="2">Copy cURL, then paste anywhere in the scenario editor.<p>For more information, see <a href="/help/workfront-fusion/create-scenarios/add-modules/use-curl-create-http.md">Use cURL to add an HTTP module</a>.</td> 
  </tr> 
 </tbody> 
</table>





