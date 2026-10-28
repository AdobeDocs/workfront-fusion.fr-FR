---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Ajouter un webhook à un scénario de base
description: Les Webhooks, également appelés déclencheurs instantanés, sont un type spécifique de module de déclenchement qui peut démarrer un scénario à chaque modification, plutôt que selon un planning donné.
author: Becky
feature: Workfront Fusion
exl-id: 28ecca1f-a9c3-4b3d-95f5-73cb9a5dc4b9
TQID: https://experienceleague.adobe.com/V3cpVf8NzJdGjSZvPA0Hy0Uui-zSdd986plS1Us0oNI
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
    internal-label: Integrations
source-git-commit: 4cd8b43e9ce9a16aca16397ce140cdd2467bf7d4
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 14%
---
# Ajouter un webhook à un scénario de base

Les Webhooks, également appelés déclencheurs instantanés, sont un type spécifique de module de déclenchement qui peut démarrer un scénario à chaque modification, plutôt que selon un planning donné.

Dans cet exemple, vous allez ajouter un webhook pour démarrer un scénario dès que les requêtes ont été envoyées à une file d’attente de requêtes spécifique. Le scénario convertit ensuite ces requêtes en projet.

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

## Ajouter et configurer le webhook dans la nouvelle expérience (recommandé)

* [Ajouter le module webhook](#add-the-webhook-module)
* [Mise à jour du deuxième module](#update-the-second-module)
* [Tester et activer](#test-and-activate)

### Ajouter le module webhook

1. Ouvrez le scénario dans l’éditeur de scénarios.
1. Cliquez avec le bouton droit sur le premier module et sélectionnez **[!UICONTROL Supprimer le module]**.

   Le module est supprimé, laissant un espace réservé vide.

1. Cliquez sur le module vierge pour ouvrir la liste des applications et services.

   ![Sélecteur d’application et de service](/help/workfront-fusion/build-practice-scenarios/assets/new-connector-picker.png)

1. Sélectionnez **&#x200B;**.
1. Sélectionnez **Observer les événements**.
1. Cliquez sur **Ajouter** à côté du champ Webhook.
1. dans le champ Type d’enregistrement , sélectionnez **Problème** afin que le module se déclenche pour les modifications dans les problèmes.
1. Dans le champ Etat , sélectionnez **Nouvel état**. Il s’agit d’un champ obligatoire utilisé pour le filtre, que cet exemple ne couvre pas.
1. Dans le champ Origine de l’enregistrement , sélectionnez **Nouvel enregistrement uniquement**. Cela permet au scénario de se déclencher lorsqu’un événement est ajouté, et non lorsqu’un événement est mis à jour ou supprimé.
1. Cliquez sur **Enregistrer** pour enregistrer la configuration du module.

### Mise à jour du deuxième module

1. Ouvrez le scénario.
1. Cliquez sur le module **Convertir l’objet** pour l’ouvrir.
1. Dans le champ ID de l’événement , supprimez le bloc d’ID noir. Le bloc est noir, car le module à partir duquel il a été mappé n’est plus disponible.
1. Sélectionnez le bloc d’identifiant sous le premier module (Événements Espion) pour le mapper au second module.
1. Cliquez sur **OK**.

### Tester et activer

1. Cliquez sur l’icône **[!UICONTROL Exécuter une fois]**.

   L’exécution unique est réservée aux icônes dans la nouvelle expérience. Pointez sur l’icône pour afficher l’info-bulle **[!UICONTROL Exécuter une fois]**.

   ![bouton exécuter le scénario](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/run-once-new.png)

   Le scénario doit être en cours d’exécution pour surveiller la nouvelle demande.
1. Accédez à l’environnement Workfront auquel Fusion se connecte et ajoutez un problème.

   Le scénario doit s’exécuter.
1. Examinez la sortie pour vous assurer que le scénario s’est exécuté comme prévu.
1. Lorsque vous êtes convaincu que le scénario fonctionne comme prévu, cliquez sur le bouton (bascule) **Planification** pour **Activé**.

   Le scénario est alors activé.

   ![Basculement de la planification](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/scheduling-new.png)

1. Cliquez sur l’icône **Enregistrer** ![Icône Enregistrer](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/save-icon-new.png) dans la zone Contrôles pour enregistrer votre progression dans le scénario.

## Ajouter et configurer le webhook dans l’expérience classique

* [Ajout du module webhook (classique)](#add-the-webhook-module-classic)
* [Mise à jour du deuxième module (Classique)](#update-the-second-module-classic)
* [Tester et activer (Classique)](#test-and-activate-classic)

### Ajout du module webhook (classique)

1. Ouvrez le scénario dans l’éditeur de scénarios.
1. Cliquez avec le bouton droit sur le premier module et sélectionnez **Supprimer le module**.

   Le module est supprimé, laissant un espace réservé vide.

1. Cliquez sur le module vierge, puis sélectionnez **&#x200B;**&#x200B;dans la liste des applications.
1. Sélectionnez **Observer les événements**.
1. Cliquez sur **Ajouter** à côté du champ Webhook.
1. dans le champ Type d’enregistrement , sélectionnez **Problème** afin que le module se déclenche pour les modifications dans les problèmes.
1. Dans le champ Etat , sélectionnez **Nouvel état**. Il s’agit d’un champ obligatoire utilisé pour le filtre, que cet exemple ne couvre pas.
1. Dans le champ Origine de l’enregistrement , sélectionnez **Nouvel enregistrement uniquement**. Cela permet au scénario de se déclencher lorsqu’un événement est ajouté, et non lorsqu’un événement est mis à jour ou supprimé.
1. Cliquez sur **Enregistrer** pour enregistrer la configuration du module.

### Mise à jour du deuxième module (Classique)

1. Ouvrez le scénario.
1. Cliquez sur le module **Convertir l’objet** pour l’ouvrir.
1. Dans le champ ID de l’événement , supprimez le bloc d’ID noir. Le bloc est noir, car le module à partir duquel il a été mappé n’est plus disponible.
1. Sélectionnez le bloc d’identifiant sous le premier module (Événements Espion) pour le mapper au second module.
1. Cliquez sur **OK**.

### Tester et activer (Classique)

1. Cliquez sur **[!UICONTROL Exécuter une fois]** dans le coin inférieur gauche de l’éditeur de scénario.

   Le scénario doit être en cours d’exécution pour surveiller la nouvelle demande.
1. Accédez à l’environnement Workfront auquel Fusion se connecte et ajoutez un problème.

   Le scénario doit s’exécuter.
1. Examinez la sortie pour vous assurer que le scénario s’est exécuté comme prévu.
1. Lorsque vous êtes convaincu que le scénario fonctionne comme prévu, cliquez sur le bouton (bascule) **Planification** dans le coin inférieur gauche de l’écran pour **Activé**.

   Le scénario est alors activé.
1. Dans Workfront Fusion, cliquez sur **[!UICONTROL Enregistrer]** près du coin inférieur gauche pour enregistrer votre progression dans le scénario.
