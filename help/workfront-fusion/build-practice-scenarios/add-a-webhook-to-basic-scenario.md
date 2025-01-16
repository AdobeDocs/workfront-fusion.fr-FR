---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Ajout d’un webhook à un scénario de base
description: Les Webhooks, également appelés déclencheurs instantanés, sont un type spécifique de module de déclenchement qui peut démarrer un scénario à chaque modification, plutôt que selon un planning donné.
author: Becky
feature: Workfront Fusion
exl-id: 28ecca1f-a9c3-4b3d-95f5-73cb9a5dc4b9
source-git-commit: 3ba5d67806e0d495bd4a91589d06cfb9adb25c0c
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 11%

---

# Ajout d’un webhook à un scénario de base

Les Webhooks, également appelés déclencheurs instantanés, sont un type spécifique de module de déclenchement qui peut démarrer un scénario à chaque modification, plutôt que selon un planning donné.

Dans cet exemple, vous allez ajouter un webhook pour démarrer un scénario dès que les requêtes ont été envoyées à une file d’attente de requêtes spécifique. Le scénario convertit ensuite ces requêtes en projet.

Cet exemple montre comment modifier le scénario créé dans [Créer un scénario de base](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md).

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
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Conditions préalables

Vous devez créer le scénario décrit dans [Créer un scénario de base](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md) avant de suivre cette procédure.

## Ajouter et configurer le webhook


### Ajouter le module webhook

1. Ouvrez le scénario dans l’éditeur de scénarios.
1. Cliquez avec le bouton droit sur le premier module et sélectionnez **Supprimer le module**.

   Le module est supprimé, laissant un espace réservé vide.

1. Cliquez sur le module vierge, puis sélectionnez **Adobe Workfront** dans la liste des applications.
1. Sélectionnez **Observer les événements**.
1. Cliquez sur **Ajouter** en regard du champ Webhook.
1. dans le champ Type d’enregistrement , sélectionnez **Problème** afin que le module se déclenche pour les modifications dans les problèmes.
1. Dans le champ Etat , sélectionnez **Nouvel état**. Il s’agit d’un champ obligatoire utilisé pour le filtre, que cet exemple ne couvre pas.
1. Dans le champ Origine de l’enregistrement , sélectionnez **Nouvel enregistrement uniquement**. Cela permet au scénario de se déclencher lorsqu’un événement est ajouté, et non lorsqu’un événement est mis à jour ou supprimé.
1. Cliquez sur **Enregistrer** pour enregistrer la configuration du module.

## Mise à jour du deuxième module

1. Ouvrez le scénario.
1. Cliquez sur le module **Convertir l’objet** pour l’ouvrir.
1. Dans le champ ID de l’événement , supprimez le bloc d’ID noir. Le bloc est noir, car le module à partir duquel il a été mappé n’est plus disponible.
1. Sélectionnez le bloc d’identifiant sous le premier module (Événements Espion) pour le mapper au second module.
1. Cliquez sur **OK**.



### Tester et activer

1. Cliquez sur **[!UICONTROL Run once]** dans le coin inférieur gauche de l’éditeur de scénarios.

   Le scénario doit être en cours d’exécution pour surveiller la nouvelle demande.
1. Accédez à l’environnement Workfront auquel Fusion se connecte et ajoutez un problème.

   Le scénario doit s’exécuter.
1. Examinez la sortie pour vous assurer que le scénario s’est exécuté comme prévu.
1. Lorsque vous êtes convaincu que le scénario fonctionne comme prévu, cliquez sur le bouton (bascule) **Planification** dans le coin inférieur gauche de l’écran pour **Activé**.

   Le scénario est alors activé.
1. Dans [!DNL Workfront Fusion], cliquez sur **[!UICONTROL Save]** près du coin inférieur gauche pour enregistrer votre progression dans le scénario.
