---
title: Opérations
description: Dans Adobe Workfront Fusion, une opération est une tâche effectuée par un module. À des fins de suivi, toute action effectuée avec succès par un module est une opération.
author: Becky
feature: Workfront Fusion
exl-id: c14e2bb2-1cce-48ff-8bea-acc9829d3cf2
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 78%

---

# Opérations

Dans Adobe Workfront Fusion, une opération est une tâche effectuée par un module. À des fins de suivi, toute action effectuée avec succès par un module est une opération.

## Éléments à prendre en compte lors du comptage du nombre d’opérations

* En général, toute exécution réussie d’une étape-action est considérée comme une opération.
* Le premier module d’un scénario ne s’exécute qu’une seule fois et est toujours compté comme une opération, même s’il ne renvoie pas de lot.
* Le nombre d’exécutions des autres modules dépend du nombre de lots qu’ils doivent traiter.  Une exécution d’un module pour un lot constitue une seule opération. Le module agrégateur fait exception à la règle, puisqu’il est compté comme une opération pour chaque ensemble de lots traités.
* Les opérations sont comptabilisées à l’étape [!UICONTROL Finalization] de l’exécution d’un scénario.
* Les éléments suivants ne sont **pas** comptés comme des opérations :
   * Toutes les étapes de filtrage.
   * Toute action qui provoque une erreur ou qui est interrompue.
   * Tout itinéraire qui n’est pas exécuté parce que les règles de l’itinéraire n’ont pas été satisfaites, tels que les itinéraires de secours ou les itinéraires désactivés.
   * Toute action qui ne s’exécute pas, soit parce qu’un filtre n’a pas autorisé le passage des données, soit parce que le scénario s’est arrêté en raison d’une erreur.

## Limites d’opérations

Votre organisation peut avoir une limite mensuelle d’opérations. Celle-ci est basée sur la formule [!DNL Workfront] que votre organisation a acheté. Le plan de [!DNL Workfront] [!UICONTROL Ultimate] offre un nombre illimité d’opérations.

Si votre organisation a une limite mensuelle, vous serez averti lorsque votre organisation approchera de la limite. Si votre entreprise dépasse la limite, [!DNL Workfront] contactera pour vous assurer que votre plan répond à vos besoins.

## Consulter le nombre d’opérations effectuées au cours des 30 derniers jours

Vous pouvez consulter des graphiques qui indiquent le nombre d’opérations effectuées. Ces graphiques sont disponibles aux endroits suivants :

* **Tableau de bord de l’organisation** : opérations utilisées par l’ensemble de l’organisation.
* **Tableau de bord de l’équipe** : opérations utilisées par les scénarios détenus par cette équipe
* **page Détails du scénario** : opérations utilisées par ce scénario
