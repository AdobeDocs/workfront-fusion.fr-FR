---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Ajouter un filtre à un scénario de base
description: Les filtres vous permettent de vous assurer que votre scénario ne progresse que si certaines conditions sont remplies.
author: Becky
feature: Workfront Fusion
exl-id: 78ab27fe-e2dd-4b52-b986-77b4b7ea3b5e
source-git-commit: 6269db7454a63e80de3d770ab1012162d5080565
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 19%

---

# Ajouter un filtre à un scénario de base

Les filtres vous permettent de vous assurer que votre scénario ne progresse que si certaines conditions sont remplies.

Dans cet exemple, vous allez ajouter à votre scénario un filtre qui permet de créer un projet à partir d’une demande uniquement si la demande a été envoyée à une file d’attente de demandes spécifique.

Cet exemple montre comment modifier le scénario créé dans [Créer un scénario de base](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md).

>[!NOTE]
>
>Les modules de déclenchement de Workfront incluent des filtres qui permettent à un scénario de démarrer uniquement si certaines conditions sont remplies. Cependant, comme des filtres entre modules sont utilisés pour chaque cas d’utilisation autre que le déclencheur et le Workfront, il est important d’apprendre à utiliser les filtres entre les modules. Cet exemple utilise un filtre intermodule pour les fonctionnalités qui peuvent être satisfaites avec un filtre intermodule.

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

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation Workfront](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Conditions préalables

Vous devez créer le scénario décrit dans [Créer un scénario de base](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md) avant de suivre cette procédure.

## Ajouter un filtre

### Préparer l’ajout du filtre

1. Ouvrez le scénario.
1. Cliquez sur le premier module pour l’ouvrir.
1. Dans la zone **Sorties**, sélectionnez `Project`.
Vous devriez maintenant avoir `ID`, `Name` et `Project` sélectionnés.
1. Cliquez sur OK pour enregistrer les paramètres du module.
1. Ouvrez Workfront.
1. Dans Workfront, recherchez le projet qui représente la file d’attente des demandes avec laquelle le scénario Fusion fonctionnera.

   Ce projet doit se trouver sur le même compte Workfront que celui pour lequel la connexion Fusion a été configurée.

1. Notez l’ID de projet dans l’URL.

   Exemple : https://\&lt;MyDomain\>.my.workfront.com/project/\&lt;ProjectID\>/tasks

### Ajouter et configurer le filtre

1. Revenez au scénario dans l’éditeur de scénarios.
1. Cliquez sur l’icône de clé à molette ![icône de clé à molette](assets/wrench-icon.png) entre le premier et le deuxième module, puis sélectionnez **Configurer un filtre**.
1. Dans le champ Libellé , saisissez un libellé pour ce filtre, par exemple « Filtrer pour la file d’attente des demandes ».
1. Dans la zone **Condition**, dans le champ supérieur, mappez le `projectID` du premier module.

   ![Mapper l’ID de projet](assets/map-proj-id.png)
1. Laissez l’opérateur **Condition** sur Égal à.
1. Dans le champ inférieur de la zone **Condition**, collez l’ID de projet dont vous avez pris note dans l’URL du projet dans [Préparez l’ajout du filtre](#prepare-to-add-the-filter).
1. Cliquez sur **OK** pour enregistrer les paramètres de filtre.

### Tester et activer

1. Accédez à l’environnement Workfront auquel Fusion se connecte et ajoutez un problème au projet que vous avez spécifié dans le filtre. Ajoutez un autre événement à un autre projet.
1. Cliquez sur **[!UICONTROL Exécuter une fois]** dans le coin inférieur gauche de l’éditeur de scénario.
1. Examinez la sortie pour vous assurer que le scénario s’est exécuté comme prévu.

   Les deux problèmes doivent apparaître dans la sortie du premier module, mais seul le problème du projet spécifié doit apparaître comme entrée dans le deuxième module.
1. Lorsque vous êtes convaincu que le scénario fonctionne comme prévu, cliquez sur le bouton (bascule) **Planification** dans le coin inférieur gauche de l’écran pour **Activé**.

   Le scénario est alors activé.
1. Dans Workfront Fusion, cliquez sur **[!UICONTROL Enregistrer]** près du coin inférieur gauche pour enregistrer votre progression dans le scénario.

   >[!IMPORTANT]
   >
   >Enregistrez souvent lorsque vous affinez et testez un scénario. Vous devrez peut-être créer un nouveau problème dans votre compte Workfront pour déclencher le scénario.

## Ressources

* Pour plus d’informations sur les filtres, voir [Ajouter un filtre à un scénario](/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md).
