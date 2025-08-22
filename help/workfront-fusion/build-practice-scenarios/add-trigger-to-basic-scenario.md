---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Ajout d’un module de déclenchement à un scénario de base
description: Découvrez comment ajouter un module de déclenchement pour permettre au scénario de rechercher régulièrement de nouvelles requêtes et de les convertir en projets.
author: Becky
feature: Workfront Fusion
exl-id: cd8ac958-b7a6-4536-89d8-c79a2f8940a6
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 11%

---

# Ajout d’un module de déclenchement à un scénario de base

Les modules Trigger sont placés au début d’un scénario. Ces modules démarrent l’exécution d’un scénario lorsqu’il y a eu une modification dans un service donné. La modification peut être la création de nouveaux enregistrements, la suppression d’un enregistrement, la mise à jour d’un enregistrement, etc. Vous spécifiez les critères des modifications qui commencent le scénario.

Les modules d’interrogation vérifient le service à un intervalle de temps défini et renvoient des informations sur les modifications qui se sont produites au cours de cet intervalle de temps. Si aucune modification n’a été apportée, le déclencheur n’exécute pas le scénario.

Dans cet exemple, vous allez ajouter un module déclencheur qui s’exécute toutes les 15 minutes et démarre un scénario si des requêtes ont été envoyées à une file d’attente spécifique. Le scénario convertit ensuite ces requêtes en projet.

Cet exemple montre comment modifier le scénario créé dans [Créer un scénario de base](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md).

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tous</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licence Adobe Workfront</td> 
   <td> <p>Nouveau : Standard</p><p>Ou</p><p>Actuelle : [!UICONTROL Work] ou niveau supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licence Adobe Workfront Fusion **</td> 
   <td>
   <p>Actuel : aucune exigence de licence Workfront Fusion.</p>
   <p>Ou</p>
   <p>Héritée : n’importe laquelle. </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Nouveau :</p> <ul><li>Plan Workfront [!UICONTROL Select] ou [!UICONTROL Prime] : votre entreprise doit acheter Adobe Workfront Fusion.</li><li>Plan Workfront [!UICONTROL Ultimate] : Workfront Fusion est inclus.</li></ul>
   <p>Ou</p>
   <p>Actuel : votre entreprise doit acheter Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Conditions préalables

Vous devez créer le scénario décrit dans [Créer un scénario de base](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md) avant de suivre cette procédure.

## Ajout et configuration du module de déclenchement

### Ajout du module de déclenchement

1. Ouvrez le scénario dans l’éditeur de scénarios.
1. Cliquez avec le bouton droit sur le premier module (Rechercher) et sélectionnez **Supprimer le module**.

   Le module est supprimé, laissant un espace réservé vide.

1. Cliquez sur le module vierge, puis sélectionnez **Adobe Workfront** dans la liste des applications.
1. Sélectionnez **Enregistrement de contrôle**.
1. Assurez-vous que le module utilise la même connexion que le reste des modules du scénario.
1. Dans le champ Type d’enregistrement , sélectionnez **Événement**.
1. Dans le champ Filtrer , sélectionnez **Nouveaux enregistrements uniquement**.
1. Dans la zone Sorties, sélectionnez `ID`, `Name` et `Project ID`.
1. Cliquez sur **OK** pour enregistrer les paramètres du module.

   Une fenêtre Choisir où commencer s’affiche.

1. Sélectionnez **À partir de maintenant**.

### Planification du module de déclenchement

1. Cliquez sur l&#39;horloge sur le module Watch Records.

   La fenêtre du paramètre Planification s’ouvre.

1. Dans le champ Exécuter le scénario , sélectionnez **À intervalles réguliers**.

1. Cliquez sur **OK**.

### Mise à jour du deuxième module

Le premier module ayant été remplacé, le second module doit être mappé au nouveau premier module.

1. Ouvrez le module Convertir l’objet .
1. Dans le champ ID de l’événement , supprimez le bloc d’ID noir. Le bloc est noir, car le module à partir duquel il a été mappé n’est plus disponible.
1. Sélectionnez le bloc d’ID sous le premier module (Enregistrements de contrôle) pour le mapper au second module.
1. Cliquez sur **OK**.

### Tester et activer

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
