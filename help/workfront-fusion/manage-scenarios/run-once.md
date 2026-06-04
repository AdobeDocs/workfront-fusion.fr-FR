---
title: Utiliser Exécuter une fois pour tester un scénario
description: Vous pouvez tester un scénario sans déclencheur externe à l’aide du bouton Exécuter une fois .
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 9c05aa1111fd571ea6f0ff86943b2849a39e4973
workflow-type: tm+mt
source-wordcount: 332
ht-degree: 0%

---

# Utiliser Exécuter une fois pour tester un scénario

Lors de la création, de la mise à jour ou de l’affinement d’un scénario, vous pouvez utiliser le bouton « Exécuter une fois » pour déclencher le scénario à la demande. Vous pouvez ainsi tester le scénario sans attendre sa logique de déclenchement, telle que des événements spécifiques ou des intervalles d’interrogation.

Vous pouvez également exécuter un scénario une seule fois pour configurer les structures de données

>[!TIP]
>
>Nous vous recommandons de tester fréquemment au fur et à mesure que vous créez et affinez des scénarios.

## Utiliser la fonctionnalité Exécuter une seule fois

La fonction Exécuter une fois se trouve dans l’éditeur de scénarios.

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez exécuter l’expert en notation de scénario.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Cliquez sur **Exécuter une fois** dans le coin inférieur gauche de l’éditeur de scénarios.
1. (Conditionnel) Si le scénario est déclenché par un webhook ou s’il s’agit d’un scénario enfant, sélectionnez l’entrée pour l’exécution de test.

   * **Attendez un appel webhook externe** : le scénario commencera à écouter un appel webhook entrant. Vous devez déclencher le webhook à partir du système externe pour fournir le webhook.

     Par exemple, si le webhook écoute une nouvelle demande dans Workfront, vous devez créer une nouvelle demande dans Workfront pour la déclencher et terminer la fonctionnalité « Run once » (Exécuter une fois).

     >[!NOTE]
     >
     >Cette option est disponible uniquement pour les scénarios webhook.

   * **Utiliser une entrée d&#39;exécution précédente** : vous devez sélectionner une exécution précédente. L’exécution « Exécuter une fois » utilise les données d’entrée qui ont déclenché l’exécution sélectionnée.

     Pour sélectionner une exécution précédente, sélectionnez-la et cliquez sur **Exécuter**.

     Pour examiner les données d’entrée de l’exécution avant de les sélectionner, cliquez sur **Prévisualiser l’entrée** pour cette exécution.

     >[!NOTE]
     >
     >Le scénario doit avoir terminé les exécutions précédentes avant que cette option ne soit disponible.

   * **Fournir une entrée manuelle** : vous devez fournir la payload webhook pour l’entrée du scénario. Elle doit être au format JSON.

     Pour fournir l’entrée, saisissez le texte dans la zone **Payload du Webhook** et cliquez sur **Exécuter**.
