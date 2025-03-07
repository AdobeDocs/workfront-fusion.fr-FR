---
title: Déclencheurs instantanés (webhooks)
description: De nombreux services proposent des webhooks pour envoyer des notifications instantanées chaque fois que le service est modifié. Pour traiter ces notifications, nous vous recommandons d’utiliser des déclencheurs instantanés. Cet article décrit l’utilisation et la fonctionnalité des déclencheurs instantanés dans Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 5bfda2b2-dc1c-4ff6-9236-b480bfda2e58
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '848'
ht-degree: 28%

---

# Déclencheurs instantanés (webhooks)

De nombreux services fournissent des Webhooks pour diffuser des notifications instantanées chaque fois qu’une certaine modification (événement) se produit dans le service. Pour traiter ces événements, il est recommandé d’utiliser des déclencheurs instantanés. Les déclencheurs instantanés affichent la balise `Instant` dans la liste des modules d&#39;un connecteur donné.

![Instantané](assets/instant.png)

>[!TIP]
>
>Vous pouvez vérifier la liste des modules d’un connecteur pour voir s’il dispose d’un déclencheur instantané, ou vous pouvez vérifier la documentation du connecteur sous [Références des applications Fusion et de leurs modules](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).
>
>Pour consulter la documentation sur les déclencheurs instantanés d’Adobe Workfront, voir [Triggers](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#triggers) dans l’article Modules Workfront.

Si un connecteur n’inclut pas de webhook, vous pouvez effectuer l’une des opérations suivantes :

* Créez un webhook personnalisé à l’aide du module Webhook.
Pour plus d’informations, voir [Webhooks](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md).
* Utilisez des déclencheurs d’interrogation pour interroger régulièrement le service.
Pour plus d’informations, voir [ Planification d’un scénario ](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md)

Pour une introduction vidéo aux webhooks dans Workfront Fusion, consultez :

* [Présentation des webhooks](https://video.tv.adobe.com/v/3427025/){target=_blank}
* [Webhooks intermédiaires](https://video.tv.adobe.com/v/3427030/){target=_blank}

## Planifier des déclencheurs instantanés

Lorsque vous configurez un déclencheur instantané, vous êtes invité à choisir le moment où il s’exécute.

![Paramètre de planification](assets/schedule-setting.png)

Sélectionnez `Immediately` pour exécuter immédiatement le scénario lorsque [!DNL Workfront Fusion] reçoit de nouveaux événements du service. Ces événements sont immédiatement envoyés dans une file d’attente, puis traités dans le scénario, un par un, dans l’ordre de réception des données.

Lorsque le scénario s’exécute, la quantité totale d’événements en attente dans la file d’attente est comptabilisée et le scénario effectue autant de cycles que d’événements en attente, en traitant un événement par cycle.

Pour plus d’informations sur les cycles, voir [Exécution du scénario, cycles et phases](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).

>[!NOTE]
>
>* Un cycle n’est pas la même chose qu’un scénario. Il peut y avoir plusieurs cycles dans une exécution de scénario.
>* Lorsque vous exécutez un scénario avec un déclencheur instantané programmé pour être exécuté `Immediately`, les exceptions suivantes s’appliquent :
>
>     * L’intervalle entre deux exécutions n’est pas soumis à l’intervalle minimal selon le plan de tarification.
>
>       Par exemple, une fois que le scénario a terminé son exécution, la file d’attente du webhook est à nouveau vérifiée. Si des webhooks sont en attente, le scénario s’exécute à nouveau immédiatement, en traitant à nouveau tous les webhooks en attente.
>   
>     * Le paramètre de scénario Nombre maximal de cycles est ignoré et défini sur 100, ce qui signifie que pas plus de 100 webhooks en attente seront traités au cours d’une seule exécution de scénario (au rythme d’1 événement par cycle).
>


Si vous utilisez un autre paramètre de planification que [!UICONTROL Immediately], le scénario s’exécute aux intervalles que vous spécifiez. Étant donné que plusieurs webhooks peuvent être regroupés dans la file d’attente pendant l’intervalle, nous vous recommandons de définir l’option [!UICONTROL Maximum number of cycles] sur une valeur supérieure à la valeur par défaut 1 afin de traiter d’autres webhooks dans une seule exécution de scénario :

1. Cliquez sur l’icône [!UICONTROL Scenario settings] ![icône des paramètres du scénario](assets/scenario-settings-icon.png) au bas de votre scénario.
1. Dans le panneau **[!UICONTROL Scenario settings]** qui s’affiche, saisissez un nombre dans le champ **[!UICONTROL Max number of cycles]** pour indiquer le nombre d’événements de la file d’attente que vous souhaitez exécuter chaque fois que vous exécutez le scénario.

Les événements restants dans la file d’attente seront traités la prochaine fois que le scénario sera exécuté, jusqu’au nombre défini dans le champ Nombre maximal de cycles .

## Mécanismes de sécurisation des webhooks

Pour garantir de bonnes performances, Workfront Fusion dispose des mécanismes de sécurisation suivants pour les webhooks.

### Limites de débit

La limite de débit actuelle est de 5 webhooks par seconde. Si la limite est dépassée, un code d’état `429` est renvoyé.

### Expiration des webhooks inactifs

Un webhook qui n’a pas été affecté à un scénario depuis plus de 120 heures est supprimé.

### Payloads des webhooks

[!DNL Workfront Fusion] stocke les payloads des webhooks pendant 30 jours. L’accès à une payload webhook plus de 30 jours après sa création génère une [!UICONTROL `Failed to read file from storage.`] d’erreur

### Gestion des erreurs

Lorsqu’il comporte une erreur avec un déclencheur instantané, le scénario :

* S’arrête immédiatement lorsque le scénario est configuré pour s’exécuter [!UICONTROL Immediately].
* S’arrête après 3 tentatives infructueuses (3 erreurs) lorsque le scénario est défini pour s’exécuter comme prévu.

Si une erreur se produit lors de l’exécution du scénario, l’événement est replacé dans la file d’attente pendant la phase de restauration du déclencheur d’instant. Dans ce cas, vous pouvez corriger le scénario et l’exécuter à nouveau.

Pour plus d’informations, consultez [Restauration](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md#rollback) dans l’article Exécution du scénario, cycles et phases.

Si votre scénario comporte un module de réponse webhook, l’erreur est envoyée à la réponse webhook. Le module de réponse Webhook est toujours exécuté en dernier (lorsque l’option [!UICONTROL Auto commit] des paramètres du scénario n’est pas activée).

Pour plus d’informations, voir [Réponse aux Webhooks](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md#responding-to-webhooks) dans l’article Webhooks.

### Désactivation de webhook

Les webhooks sont désactivés automatiquement si l’une des conditions suivantes s’applique :

* Le webhook n’est connecté à aucun scénario depuis plus de 5 jours.
* Le webhook est utilisé uniquement dans les scénarios inactifs, qui sont inactifs depuis plus de 30 jours.

Les webhooks désactivés sont automatiquement supprimés et désenregistrés s’ils ne sont connectés à aucun scénario et s’ils ont le statut Désactivé depuis plus de 30 jours.

## Webhooks personnalisés

Vous pouvez créer vos propres webhooks. Pour plus d’informations, voir [Webhooks](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md).

## Ressources

Pour plus d’informations sur les cycles, voir [Exécution du scénario, cycles et phases](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).
