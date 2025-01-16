---
title: Exécuter l’expert en notation de scénario
description: L’expert en notation de scénario peut vous aider à vous assurer que votre scénario est configuré de manière à suivre les bonnes pratiques. Il vérifie votre scénario et fournit des recommandations pour sa structure et son organisation.
author: Becky
feature: Workfront Fusion
exl-id: b668e7f6-dac5-4ac9-b3f3-109f70eaa2c4
source-git-commit: 55fe4bc46bc50ad9ccfd1b234e89028cf3cd12d5
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 20%

---

# Exécuter l’expert en notation de scénario

L’expert en notation de scénario peut vous aider à vous assurer que votre scénario est configuré de manière à suivre les bonnes pratiques. Il vérifie votre scénario et fournit des recommandations pour sa structure et son organisation.

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

## Exécuter l’expert en notation de scénario

1. Cliquez sur l’onglet **[!UICONTROL Scenarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez exécuter l’expert en notation de scénario.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Cliquez sur l’icône d’expert en notation de scénario ![expert en notation de scénario](assets/scoring-expert-icon.png) en bas de l’écran.

   Le panneau d’experts en notation de scénario s’ouvre.
1. Cliquez sur **Évaluer**.

L’expert en notation de scénario renvoie une note sur 10 et indique les vérifications qui ont réussi ou échoué. Si une vérification a échoué, l’expert en notation de scénario fournit des recommandations sur la manière de s’assurer que le scénario répond à ces vérifications.

![ Score du scénario ](assets/scenario-score.png)

## Vérifications du score du scénario

L’expert en notation de scénario effectue les vérifications suivantes :

* Le scénario doit être nommé.
* Tous les modules doivent être étiquetés.
* Le scénario doit s’exécuter selon un planning défini.

  Pour obtenir des instructions, voir [Planification d’un scénario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).
* La taille du plan directeur du scénario doit être inférieure à 5 Mo.

  Pour plus d’informations, voir [ Mécanismes de sécurisation des performances de Fusion ](/help/workfront-fusion/references/scenarios/fusion-performance-guardrails.md#scenarios).
* Si un module de déclenchement instantané Workfront est utilisé, il doit être filtré.

  Pour obtenir des instructions, voir [Filtres d’abonnement aux événements dans le module  [!DNL Workfront] > [!UICONTROL Watch Events]](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules).
