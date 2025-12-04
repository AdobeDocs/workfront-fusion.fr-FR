---
title: Éditeur de scénarios
description: L’éditeur de scénario vous permet de créer et de modifier des scénarios dans une interface visuelle.
author: Becky
feature: Workfront Fusion
exl-id: 47ccecf0-751c-4026-96a9-329c33cb6801
source-git-commit: f968b9141173725160cea36575ad4e02a09a5e3f
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 33%

---

# Éditeur de scénarios

L’éditeur de scénario vous permet de créer et de modifier des scénarios dans une interface visuelle.

![Éditeur de scénarios](assets/scenario-editor.jpg)

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tout package de workflow Adobe Workfront et tout package d’automatisation et d’intégration Adobe Workfront.</p><p>Workfront Ultimate</p><p>Packages Workfront Prime et Select, avec un achat supplémentaire de Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licences Adobe Workfront</td> 
   <td> <p>Standard</p><p>Travail ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Si votre entreprise dispose d’un package Workfront Select ou Prime qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acheter Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Ouvrez l’éditeur de scénarios et ajoutez un module :

1. Cliquez sur **[!UICONTROL Scénarios]** ![icône Scénarios](assets/scenarios-icon.png) dans le panneau de gauche.
1. Cliquez sur l’icône de point d’interrogation ![icône de question](assets/question-mark-full-size.png), puis recherchez et cliquez sur l’application ou le service avec lequel vous souhaitez commencer. Pour plus d’informations sur la configuration d’un module, voir [Configuration d’un module](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md).

## Actions disponibles dans l’éditeur de scénario

### Exécuter le scénario

| Action | Détails |
|----------|----------|
| Tester le scénario | Vérifiez que le scénario s’exécute comme prévu avant de l’activer. Une fois activé, le scénario s’exécute selon son planning. Si tout ne s’exécute pas comme prévu, consultez [Ajouter la gestion des erreurs](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md) pour savoir comment gérer les erreurs. |

![bouton exécuter le scénario](assets/run-your-scenario.png)

### Planification

| Action | Détails |
|----------|----------|
| Planifier le scénario | Par défaut, un scénario s’exécute toutes les 15 minutes. Vous pouvez modifier ce paramètre en définissant le moment et la fréquence d’exécution d’un scénario activé. Les scénarios de fusion peuvent être planifiés pour s’exécuter aussi souvent que toutes les 5 minutes. Pour plus d’informations, voir [ Planification d’un scénario ](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md). |

![panneau de planification](assets/scheduling-scenario-editor.png)

### Commandes

Vous devrez peut-être cliquer sur l&#39;icône des trois points dans la zone Contrôles pour afficher certains de ces contrôles.

| Action | Détails |
|----------|----------|
| Enregistrez. <p>![ Icône Enregistrer ](assets/save-icon.png)</p> | Après avoir enregistré votre scénario, une nouvelle version est disponible dans le menu à trois points si vous avez besoin d’y accéder ultérieurement. Les versions de scénario précédemment enregistrées ne sont disponibles que pendant 60 jours. |
| Paramètres du scénario <p>![Icône Paramètres du scénario](assets/scenario-settings-icon.png)</p> | Le panneau des paramètres du scénario contient des paramètres avancés pour le scénario. Pour plus d’informations sur les paramètres disponibles, voir [Configurer les paramètres de scénario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md). |
| Notes  <p>![icône Notes](assets/notes-icon.png)</p> | Prenez des notes sur le scénario. Les autres utilisateurs peuvent afficher ces notes lorsqu’ils se trouvent dans le scénario. |
| Auto-align <p>![Icône d’alignement automatique](assets/auto-align-icon.png)</p> | Alignement automatique des modules dans votre scénario. |
| Modules de recherche ![modules de recherche](assets/search-modules-icon.png)  </p> | Saisissez un terme de recherche pour localiser un module, puis cliquez sur les résultats de la recherche pour accéder à ce module. Vous pouvez effectuer une recherche par nom de module, ID, type ou application. |
| Expliquer le flux  <p>![Icône Expliquer le flux ](assets/explain-flow-icon.png) </p> | Affichez une animation où des points mobiles montrent le flux des données dans le scénario. |
| DevTool <p>![ Icône DevTool ](assets/devtool-icon.png)</p> | À l’aide de l’outil de développement, vous pouvez vérifier toutes les exécutions manuelles de votre scénario, passer en revue toutes les opérations effectuées et afficher les détails de chaque appel API effectué. Vous pouvez identifier le module, l’opération ou la réponse unique à l’origine de l’erreur et utiliser ces connaissances pour affiner votre scénario. Pour plus d’informations, voir [Déboguer un scénario](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md). |
| Exporter le plan directeur  <p>![Icône Exporter le plan directeur](assets/export-blueprint-icon.png) </p> | Exporte un plan directeur du scénario actuel. |
| Importer le plan directeur  <p>![Icône Importer un plan directeur](assets/import-blueprint-icon.png) </p> | Importez un plan directeur de scénario précédemment exporté. |
| Version précédente  <p>![Icône de la version précédente](assets//previous-version-icon.png) </p> | Affichez les versions précédentes de ce scénario. |

![Panneau Contrôles](assets/controls-editor-scenario.png)

### Outils

| Action | Détails |
|----------|----------|
| Contrôle de flux | Configurez les paramètres pour contrôler le flux de données. Pour plus d’informations, [voir le lien nécessaire]. |
| Outils | La section Outils contient plusieurs modules utiles qui peuvent améliorer vos scénarios. Pour plus d’informations, [voir le lien nécessaire]. |
| Analyseur de texte | Utilisez l’outil d’analyse de texte pour analyser le texte à utiliser dans d’autres modules de scénario. L’analyseur de texte ne nécessite pas de connexion. Pour plus d’informations, [voir le lien nécessaire]. |

![panneau outils](assets/tools-scenario-editor.png)

### Favoris

Vous pouvez utiliser l’icône Favoris pour ajouter des modules que vous utilisez souvent.

![Panneau Favoris](assets/favorites-scenario-editor.png)
