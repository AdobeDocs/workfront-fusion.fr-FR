---
title: Modifier les Webhooks
description: Vous pouvez modifier les Webhooks existants pour les connecteurs Workfront et Workfront Planning.
author: Becky
feature: Workfront Fusion
exl-id: 86849d21-5a74-43f7-9ccf-dff4421cc981
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 01689332f97c15b317e686d11a27cb4dc7e2e8bd
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 5%
---
# Modifier des webhooks

Vous pouvez modifier les Webhooks existants. À l’avenir, les scénarios qui utilisent ces webhooks utiliseront la nouvelle configuration , ce qui élimine la nécessité de créer un webhook et de l’affecter manuellement à tous les scénarios affectés.

Les Webhooks ne peuvent être modifiés que pour les connecteurs suivants :

* Workfront
* Planification Workfront

>[!IMPORTANT]
>
>Tenez compte des points suivants lors de la mise à jour d’un webhook :
>
>* Le webhook modifié est traité par les abonnements aux événements de Workfront comme un nouvel abonnement. L’historique des abonnements aux événements n’est pas conservé pour la configuration webhook précédente, car il est considéré comme un abonnement aux événements distinct.
>* Le passage de l’ancien au nouvel abonnement à un événement peut ne pas être parfaitement synchronisé. Il est donc possible de recevoir un événement deux fois (si le nouvel abonnement commence à s&#39;exécuter avant l&#39;arrêt de l&#39;ancien) ou de manquer un événement (si l&#39;ancien abonnement s&#39;arrête avant que le nouveau ne commence à s&#39;exécuter).

## Modification d’un webhook

Vous pouvez modifier des Webhooks à partir d’un scénario ou de la liste des Webhooks.

### Modification d’un webhook dans un scénario

>[!NOTE]
>
>Cette fonctionnalité est disponible uniquement pour les scénarios qui disposent d’un module de déclenchement instantané Workfront ou Workfront Planning.

1. Accédez au scénario qui comprend le webhook à modifier.
1. Dans le module de déclenchement du scénario, cliquez sur la liste déroulante en regard du champ Webhook, puis sélectionnez **Modifier l’élément**.

   La fenêtre de configuration du webhook s’ouvre, renseignée avec la configuration existante.

1. Apportez les modifications souhaitées au webhook.
1. Cliquez sur **Enregistrer** pour enregistrer le webhook et revenir au module.

### Modification d’un webhook dans la liste Webhooks

1. Dans le volet de navigation de gauche, sélectionnez **Webhooks** ![icône Webhooks](assets/webhooks-icon.png).
1. Cochez la case en regard du webhook à modifier.
1. Dans la bannière bleue située en bas de l’écran, cliquez sur **Modifier**.
1. Apportez les modifications souhaitées au webhook.
1. Cliquez sur **Enregistrer** pour enregistrer le Webhook et revenir à la liste Webhooks.
