---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Ajouter un module déclencheur à un scénario de base
description: Découvrez comment ajouter un module de déclenchement pour permettre au scénario de rechercher régulièrement de nouvelles requêtes et de les convertir en projets.
author: Becky
feature: Workfront Fusion
exl-id: cd8ac958-b7a6-4536-89d8-c79a2f8940a6
TQID: https://experienceleague.adobe.com/xepLecibr9U6FpQM0neDy15DbFGF55rR6gVYvo644H4
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
    internal-label: Integrations
source-git-commit: 347280547bea92c0ee498da519495569a3cac661
workflow-type: tm+mt
source-wordcount: '1022'
ht-degree: 14%
---
# Ajouter un module déclencheur à un scénario de base

Les modules Trigger sont placés au début d’un scénario. Ces modules démarrent l’exécution d’un scénario lorsqu’il y a eu une modification dans un service donné. La modification peut être la création de nouveaux enregistrements, la suppression d’un enregistrement, la mise à jour d’un enregistrement, etc. Vous spécifiez les critères des modifications qui commencent le scénario.

Les modules d’interrogation vérifient le service à un intervalle de temps défini et renvoient des informations sur les modifications qui se sont produites au cours de cet intervalle de temps. Si aucune modification n’a été apportée, le déclencheur n’exécute pas le scénario.

Dans cet exemple, vous allez ajouter un module déclencheur qui s’exécute toutes les 15 minutes et démarre un scénario si des requêtes ont été envoyées à une file d’attente spécifique. Le scénario convertit ensuite ces requêtes en projet.

Cet exemple montre comment modifier le scénario créé dans [Créer un scénario de base](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md).

>[!NOTE]
>
>Workfront Fusion effectue la transition de l’éditeur de scénarios vers une nouvelle expérience . Au cours de cette transition, les expériences classique et nouvelle sont disponibles et vous pouvez basculer entre elles à tout moment. Nous vous recommandons d’utiliser la nouvelle expérience . Pour plus d’informations, voir [Expériences nouvelles et classiques](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences) dans l’éditeur de scénarios d’article.

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

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Conditions préalables

Vous devez créer le scénario décrit dans [Créer un scénario de base](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md) avant de suivre cette procédure.

## Ajouter et configurer le module de déclenchement dans la nouvelle expérience (recommandé)

* [Ajout du module de déclenchement](#add-the-trigger-module)
* [Planification du module de déclenchement](#schedule-the-trigger-module)
* [Mise à jour du deuxième module](#update-the-second-module)
* [Tester et activer](#test-and-activate)

### Ajout du module de déclenchement

1. Ouvrez le scénario dans l’éditeur de scénarios.
1. Cliquez avec le bouton droit sur le premier module (Rechercher) et sélectionnez **[!UICONTROL Supprimer le module]**.

   Le module est supprimé, laissant un espace réservé vide.

1. Cliquez sur le module vierge pour ouvrir la liste des applications et services.

   ![Sélecteur d’application et de service](/help/workfront-fusion/build-practice-scenarios/assets/new-connector-picker.png)

1. Sélectionnez ****.
1. Sélectionnez **Enregistrement de contrôle**.
1. Assurez-vous que le module utilise la même connexion que le reste des modules du scénario.
1. Dans le champ Type d’enregistrement , sélectionnez **Événement**.
1. Dans le champ Filtrer , sélectionnez **Nouveaux enregistrements uniquement**.
1. Dans la zone Sorties, sélectionnez `ID`, `Name` et `Project ID`.
1. Cliquez sur **OK** pour enregistrer les paramètres du module.

   Une fenêtre Choisir où commencer s’affiche.

1. Sélectionnez **À partir de maintenant**.

### Planification du module de déclenchement

1. Cliquez sur l’icône d’horloge dans le module Enregistrement de surveillance .

   ![Icône d’horloge dans le module Enregistrement de surveillance](assets/clock-icon-on-watch-record.png)

   La fenêtre du paramètre Planification s’ouvre.

1. Dans le champ Exécuter le scénario , sélectionnez **À intervalles réguliers**.

1. Cliquez sur **OK**.

### Mise à jour du deuxième module

Le premier module ayant été remplacé, le second module doit être mappé au nouveau premier module.

1. Ouvrez le module Convertir l’objet .
1. Dans le champ ID de l’événement , supprimez le bloc d’ID noir. Le bloc est noir, car le module à partir duquel il a été mappé n’est plus disponible.
1. Sélectionnez le bloc d’identifiant sous le premier module (enregistrement de contrôle) pour le mapper au second module.
1. Cliquez sur **OK**.

### Tester et activer

1. Accédez à l’environnement Workfront auquel Fusion se connecte et ajoutez un problème.
1. Cliquez sur l’icône **[!UICONTROL Exécuter une fois]**.

   L’exécution unique est réservée aux icônes dans la nouvelle expérience. Pointez sur l’icône pour afficher l’info-bulle **[!UICONTROL Exécuter une fois]**.

   ![bouton exécuter le scénario](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/run-once-new.png)

1. Examinez la sortie pour vous assurer que le scénario s’est exécuté comme prévu.
1. Lorsque vous êtes convaincu que le scénario fonctionne comme prévu, cliquez sur le bouton (bascule) **Planification** pour **Activé**.

   Le scénario est alors activé.

   ![Basculement de la planification](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/scheduling-new.png)

1. Cliquez sur l’icône **Enregistrer** ![Icône Enregistrer](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/save-icon-new.png) dans la zone Contrôles pour enregistrer votre progression dans le scénario.

   >[!IMPORTANT]
   >
   >Sauvegardez souvent lorsque vous affinez et testez un scénario.

## Ajouter et configurer le module de déclenchement dans l’expérience classique

* [Ajout du module de déclenchement (classique)](#add-the-trigger-module-classic)
* [Planification du module de déclenchement (classique)](#schedule-the-trigger-module-classic)
* [Mise à jour du deuxième module (Classique)](#update-the-second-module-classic)
* [Tester et activer (Classique)](#test-and-activate-classic)

### Ajout du module de déclenchement (classique)

1. Ouvrez le scénario dans l’éditeur de scénarios.
1. Cliquez avec le bouton droit sur le premier module (Rechercher) et sélectionnez **Supprimer le module**.

   Le module est supprimé, laissant un espace réservé vide.

1. Cliquez sur le module vierge, puis sélectionnez **** dans la liste des applications.
1. Sélectionnez **Enregistrement de contrôle**.
1. Assurez-vous que le module utilise la même connexion que le reste des modules du scénario.
1. Dans le champ Type d’enregistrement , sélectionnez **Événement**.
1. Dans le champ Filtrer , sélectionnez **Nouveaux enregistrements uniquement**.
1. Dans la zone Sorties, sélectionnez `ID`, `Name` et `Project ID`.
1. Cliquez sur **OK** pour enregistrer les paramètres du module.

   Une fenêtre Choisir où commencer s’affiche.

1. Sélectionnez **À partir de maintenant**.

### Planification du module de déclenchement (classique)

1. Cliquez sur l’horloge dans le module Enregistrement de surveillance .

   La fenêtre du paramètre Planification s’ouvre.

1. Dans le champ Exécuter le scénario , sélectionnez **À intervalles réguliers**.

1. Cliquez sur **OK**.

### Mise à jour du deuxième module (Classique)

Le premier module ayant été remplacé, le second module doit être mappé au nouveau premier module.

1. Ouvrez le module Convertir l’objet .
1. Dans le champ ID de l’événement , supprimez le bloc d’ID noir. Le bloc est noir, car le module à partir duquel il a été mappé n’est plus disponible.
1. Sélectionnez le bloc d’identifiant sous le premier module (enregistrement de contrôle) pour le mapper au second module.
1. Cliquez sur **OK**.

### Tester et activer (Classique)

1. Accédez à l’environnement Workfront auquel Fusion se connecte et ajoutez un problème.
1. Cliquez sur **[!UICONTROL Exécuter une fois]** dans le coin inférieur gauche de l’éditeur de scénario.
1. Examinez la sortie pour vous assurer que le scénario s’est exécuté comme prévu.
1. Lorsque vous êtes convaincu que le scénario fonctionne comme prévu, cliquez sur le bouton (bascule) **Planification** dans le coin inférieur gauche de l’écran pour **Activé**.

   Le scénario est alors activé.
1. Dans Workfront Fusion, cliquez sur **[!UICONTROL Enregistrer]** près du coin inférieur gauche pour enregistrer votre progression dans le scénario.

   >[!IMPORTANT]
   >
   >Sauvegardez souvent lorsque vous affinez et testez un scénario.

## Ressources

* Pour plus d’informations sur les modules de déclenchement, voir [Modules de déclenchement](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) dans la présentation des modules.
