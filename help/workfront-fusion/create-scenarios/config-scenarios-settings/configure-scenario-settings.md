---
content-type: reference
title: Configurer les paramètres du scénario
description: Vous pouvez configurer des paramètres spécifiques pour les scénarios dans le panneau Paramètres du scénario .
author: Becky
feature: Workfront Fusion
exl-id: 105e3d39-b0ef-4c22-901d-fb4f29e685a9
source-git-commit: 3afa631a44c6dae8b1e6def6f842a9ced9de741e
workflow-type: tm+mt
source-wordcount: '1188'
ht-degree: 46%

---

# Configurer les paramètres du scénario

Vous pouvez configurer des paramètres spécifiques pour les scénarios dans le panneau Paramètres du scénario .

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] plan</td> 
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
   <p>Nouveau :</p> <ul><li>[!UICONTROL Select] ou [!UICONTROL Prime] plan de [!DNL Workfront] : votre entreprise doit acheter des [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] Plan : [!DNL Workfront Fusion] est inclus.</li></ul>
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

Pour plus d’informations sur ce tableau, consultez [Conditions d’accès requises dans la documentation Workfront](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Ouvrir les paramètres du scénario

1. Cliquez sur **Scénarios** dans le panneau de gauche.
1. Recherchez le scénario souhaité, puis cliquez sur son nom.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Cliquez sur l’icône en forme d’engrenage près du coin inférieur gauche de la page.

   ![](assets/scenario-settings-350x221.png)

   Dans le panneau [!UICONTROL Scenario settings] qui s’affiche, vous pouvez configurer différents paramètres avancés pour le scénario.
1. Activez ou désactivez les paramètres du scénario, au besoin. Voir [Options des paramètres du scénario](#scenario-settings-options) ci-dessous.

## Options des paramètres de scénario

### [!UICONTROL Sequential processing]

Cette option force toutes les exécutions à se produire dans l’ordre. Elle est principalement pertinente pour les Webhooks et les exécutions incomplètes.

Lorsque le traitement séquentiel est activé, les exécutions parallèles du scénario sont désactivées.

**Webhooks instantanés** : si un déclencheur webhook est configuré comme `instant` et que le « traitement séquentiel » est activé, toutes les payloads webhook instantanés sont mis en file d’attente et traités dans l’ordre dans lequel ils arrivent. Cela peut s’avérer utile lors du traitement d’événements provenant de systèmes externes dans un ordre exact.

>[!NOTE]
>
>Le traitement est automatiquement retardé car chaque payload est traitée avant le lancement de la suivante.

**Exécutions incomplètes** : si l’option « Exécutions incomplètes » est également activée, si une erreur se produit lors de l’exécution d’un scénario, celui-ci est mis en pause. L’un des événements suivants se produit ensuite :

* Si l’option Traitement séquentiel est **activée**, Workfront Fusion arrête le traitement de la séquence préexistante jusqu’à ce que toutes les exécutions incomplètes soient résolues.
* Si l’option Traitement séquentiel est **désactivée**, le scénario continue de s’exécuter selon son planning, accompagné de tentatives répétées de réexécuter les exécutions incomplètes.

  Pour plus d’informations sur les exécutions incomplètes, voir [Afficher et résoudre les exécutions incomplètes](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

  >[!NOTE]
  >
  >Le traitement séquentiel peut entraîner un retard dans l’exécution d’un scénario. Lorsqu’un scénario instantané se déclenche ou qu’un scénario prévu doit s’exécuter, si des exécutions incomplètes sont toujours dans la file d’attente, ce scénario ne commencera qu’après la fin de toutes les exécutions en attente.
  >
  >Si le cas d’utilisation de vos scénarios ne nécessite pas de traitement séquentiel, nous vous recommandons de désactiver l’option de traitement séquentiel.

  Pour plus d’informations sur la planification, voir [Planification d’un scénario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

### Les données sont confidentielles.

Une fois qu’un scénario a été exécuté, vous pouvez afficher par défaut des informations sur les données qui ont été traitées par les modules du scénario. Si vous ne souhaitez pas que ces informations soient stockées, activez l’option [!UICONTROL Data is confidential].

>[!IMPORTANT]
>
>Si vous activez cette option, il peut être difficile de résoudre les erreurs qui peuvent se produire lors de l’exécution d’un scénario.

### [!UICONTROL Allow storing incomplete executions]

Cette option détermine comment [!DNL Adobe Workfront Fusion] s’exécute si une erreur se produit lors de l’exécution d’un scénario. Lorsque cette option est activée, le scénario est mis en pause et déplacé vers le dossier d’exécution incomplète. Cela vous permet de résoudre le problème et de reprendre l’exécution à l’endroit où le scénario s’est arrêté. Si cette option est désactivée, l’exécution du scénario s’arrête et une phase de restauration est lancée.

Pour plus d’informations sur les exécutions incomplètes, voir [Afficher et résoudre les exécutions incomplètes](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

### Activer la perte de données

Cette option concerne l’activation de la perte de données si [!DNL Workfront Fusion] ne parvient pas à enregistrer un lot dans la file d’attente des exécutions incomplètes (par exemple, en raison d’un manque d’espace libre). Lorsque cette option est activée, les données sont perdues afin d’éviter des interruptions dans l’exécution globale du scénario. Cela s’avère utile dans les cas où la priorité la plus élevée est l’exécution continue et où les données erronées entrantes ne sont pas si importantes.

Par ailleurs, lors de l’exécution d’un scénario, il peut arriver qu’un module rencontre un fichier plus volumineux que la taille maximale autorisée. Dans ce cas, [!DNL Workfront Fusion] procède selon le paramétrage de l&#39;option [!UICONTROL Enable data loss] et un message d&#39;avertissement s&#39;affiche.

Pour plus d’informations sur les exécutions incomplètes, voir [Afficher et résoudre les exécutions incomplètes](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

Pour plus d’informations sur la taille de fichier maximale, voir [Mécanismes de sécurisation des performances de Fusion](/help/workfront-fusion/references/scenarios/fusion-performance-guardrails.md#files).

Pour plus d&#39;informations sur les avertissements, voir [Types d&#39;erreur](/help/workfront-fusion/references/errors/error-processing.md).

### [!UICONTROL Auto commit]

Les paramètres [!UICONTROL Auto commit] s’appliquent aux transactions et définissent la manière de traiter un scénario. Si l’option Validation automatique est activée, la phase de validation de chaque module démarre immédiatement après avoir terminé la phase d’opération. Lorsque l’option Validation automatique est désactivée, aucune validation n’a lieu tant que les opérations ne sont pas exécutées pour tous les modules (il s’agit du mode par défaut).

### Nombre maximal de cycles

>[!NOTE]
>
>Vous devez activer la case à cocher **Afficher les paramètres avancés** pour afficher cette option.


La définition de davantage de cycles peut s’avérer utile lorsque vous souhaitez empêcher l’interruption de connexion à un service tiers et vous assurer que tous les enregistrements sont traités dans un seul scénario d’exécution.

* Si le scénario commence par un déclencheur d’attente active, le paramètre définit le nombre maximal de cycles autorisés lors de l’exécution du scénario.

  Pour plus d’informations sur l’interrogation des déclencheurs, voir [Interrogation des déclencheurs](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#polling-triggers) dans la présentation du module d’article.

* Si le scénario commence par un déclencheur instantané, le paramètre est ignoré et tous les événements en attente sont traités lors d’une seule exécution de scénario, un événement par cycle.

  Pour plus d’informations sur les déclencheurs instantanés, consultez [Déclencheurs instantanés](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#instant-triggers) dans la présentation du module d’article.

* Si le scénario ne commence pas par un déclencheur (instantané/d’attente active), le nombre maximal de cycles spécifié est toujours effectué.

>[!BEGINSHADEBOX]

**Exemples :** [!DNL Workfront] > [!UICONTROL Watch record] recherche les nouveaux événements qui se présentent et [!DNL Workfront] >[!UICONTROL Convert object] convertit la nouvelle demande en projet et lui affecte le modèle approprié.

![](assets/scenario-settings-ex-1-350x157.png)

Un paramètre [!UICONTROL more cycles] est appliqué uniquement lorsque vous planifiez l’exécution du scénario. Lorsque vous utilisez le bouton [!UICONTROL Run once], les paramètres du cycle sont pris en compte.

#### Le nombre maximal de cycles est défini sur 1 (valeur par défaut).

![](assets/max-number-cycles-1-350x201.png)

Le nombre maximal de cycles dans le module Workfront > Enregistrements de contrôle est défini sur `10`.
Si 100 requêtes sont envoyées à [!DNL Workfront] et que le champ Nombre maximal de cycles est défini sur 10, 90 fichiers ne sont pas traités après l’exécution d’un scénario. Les 10 fichiers suivants sont traités lors de la prochaine exécution planifiée du scénario.

#### Le nombre maximal de cycles est défini sur 10.

Le nombre maximal de cycles dans le module Workfront > Enregistrements de contrôle est défini sur `10`.

Si 100 fichiers sont ajoutés au dossier du Dropbox et que l’option Nombre maximal de cycles est définie sur 10, alors 10 fichiers sont traités au cours du premier cycle, les 10 fichiers suivants au cours du deuxième cycle, les 10 fichiers suivants au cours du troisième cycle, etc., jusqu’à ce que tous les fichiers soient traités.

Tous les fichiers sont traités dans un scénario d’exécution.

Vous pouvez voir les cycles déjà exécutés dans les détails du scénario :

![](assets/scenario-detail-350x207.png)

Pour plus d’informations sur cette page, voir [Détails du scénario](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-details.md).

>[!ENDSHADEBOX]

### Nombre d’erreurs consécutives

Définit le nombre maximum de tentatives d&#39;exécution consécutives avant que l&#39;exécution d&#39;un scénario ne soit désactivée (hors `DataError`, `DuplicateDataError` et `ConnectionError`).

Pour plus d’informations sur les erreurs, voir [Types d’erreur](/help/workfront-fusion/references/errors/error-processing.md).

>[!NOTE]
>
>Si un scénario commence par un déclencheur instantané, le paramètre est ignoré et le scénario est désactivé immédiatement une fois la première erreur survenue.
