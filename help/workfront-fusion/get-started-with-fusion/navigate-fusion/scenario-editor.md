---
title: Éditeur de scénarios
description: L’éditeur de scénario vous permet de créer et de modifier des scénarios dans une interface visuelle.
author: Becky
feature: Workfront Fusion
exl-id: 47ccecf0-751c-4026-96a9-329c33cb6801
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 34%

---

# Éditeur de scénarios

L’éditeur de scénario vous permet de créer et de modifier des scénarios dans une interface visuelle.

![Éditeur de scénarios](assets/scenario-editor.jpg)

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

## Ouvrez l’éditeur de scénarios et ajoutez un module :

1. Cliquez sur **[!UICONTROL Scenarios]** ![icône Scénarios](assets/scenarios-icon.png) dans le panneau de gauche.
1. Cliquez sur l’icône de point d’interrogation ![icône de question](assets/question-mark-full-size.png), puis recherchez et cliquez sur l’application ou le service avec lequel vous souhaitez commencer. Pour plus d’informations sur la configuration d’un module, voir [Configuration d’un module](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md).

## Actions disponibles dans l’éditeur de scénario

### Exécuter le scénario

| Action | Détails |
|----------|----------|
| Tester le scénario | Vérifiez que le scénario s’exécute comme prévu avant de l’activer. Une fois activé, le scénario s’exécute selon son planning. Si tout ne s’exécute pas comme prévu, consultez [Ajouter la gestion des erreurs](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md) pour savoir comment gérer les erreurs. |

![bouton exécuter le scénario](assets/run-your-scenario.png)

### Programmation

| Action | Détails |
|----------|----------|
| Planifier le scénario | Par défaut, un scénario s’exécute toutes les 15 minutes. Vous pouvez modifier ce paramètre en définissant le moment et la fréquence d’exécution d’un scénario activé. Les scénarios de fusion peuvent être planifiés pour s’exécuter aussi souvent que toutes les 5 minutes. Pour plus d’informations, voir [ Planification d’un scénario ](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md). |

![panneau de planification](assets/scheduling-scenario-editor.png)

### Contrôles

| Action | Détails |
|----------|----------|
| Enregistrer | Après avoir enregistré votre scénario, une nouvelle version est disponible dans le menu à trois points si vous avez besoin d’y accéder ultérieurement. Les versions de scénario précédemment enregistrées ne sont disponibles que pendant 60 jours. |
| Paramètres du scénario | Le panneau des paramètres du scénario contient des paramètres avancés pour le scénario. Pour plus d’informations sur les paramètres disponibles, voir [Configurer les paramètres de scénario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md). |
| Notes | Prenez des notes sur le scénario. Les autres utilisateurs peuvent afficher ces notes lorsqu’ils se trouvent dans le scénario. |
| Auto-align | Alignement automatique des modules dans votre scénario. |
| Expliquer le flux | Visionnez une animation illustrant le flux de données dans le scénario. |
| Outils de développement | À l’aide de l’outil Devtool, vous pouvez vérifier toutes les exécutions manuelles de votre scénario, passer en revue toutes les opérations effectuées et afficher les détails de chaque appel API effectué. Vous pouvez identifier le module, l’opération ou la réponse unique à l’origine de l’erreur et utiliser ces connaissances pour affiner votre scénario. Pour plus d’informations, voir [Déboguer un scénario](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md). |
| Plus | Dans le menu Plus , vous pouvez importer ou exporter des plans directeurs et restaurer les versions précédentes du scénario. |

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
