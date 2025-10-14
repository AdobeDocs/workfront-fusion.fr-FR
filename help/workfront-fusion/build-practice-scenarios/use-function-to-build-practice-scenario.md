---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Utiliser une fonction pour mettre à jour un projet dans un scénario de base
description: Découvrez comment ajouter une fonction pour mettre à jour une tâche dans Workfront.
author: Becky
feature: Workfront Fusion
exl-id: aa082ac8-48e8-4569-880e-024dd77feaa1
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 9%

---

# Utiliser une fonction pour mettre à jour un projet dans un scénario de base

La mise à jour d’un élément de travail Workfront est un cas d’utilisation courant pour Workfront Fusion. Dans cet exemple, vous allez utiliser une fonction pour modifier le nom d’un projet en majuscules.

Fusion comprend de nombreux types de fonctions qui vous permettent de transformer et d’exécuter une logique conditionnelle sur vos données. Pour plus d’informations sur l’utilisation des fonctions, voir [Présentation des fonctions](/help/workfront-fusion/get-started-with-fusion/understand-fusion/function-overview.md).

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

## Utiliser une fonction pour mettre à jour un projet

### Ajoutez le module Mettre à jour l’enregistrement à votre scénario

1. Ouvrez le scénario dans l’éditeur de scénarios.
1. Pointez sur le cercle partiel à droite du du deuxième module, puis cliquez sur **[!UICONTROL Ajouter un autre module]**.
1. Sélectionnez Adobe Workfront dans la liste des applications, puis choisissez le module **[!UICONTROL Mettre à jour l&#39;enregistrement]**.
1. Dans le champ ID , sélectionnez le bloc d’ID situé sous le module Convertir l’objet . Il s’agit de l’identifiant du projet qui a été généré par ce module.

   ![ID de l’objet Convert](assets/id-convert-object.png)

1. Dans le champ Type d’enregistrement , sélectionnez Projet, car l’objet à mettre à jour est un projet.
1. Dans la zone Sélectionner les champs à mapper, sélectionnez Nom.

   Un champ Nom s’ouvre.
1. Passez à [&#x200B; Mapper la fonction pour la mise à jour du nom &#x200B;](#map-the-function-for-the-name-update).

### Mappez la fonction pour la mise à jour du nom.

Lorsque ce scénario convertit une demande en projet, le nom du projet est identique à celui de la demande. La fonction ici prend ce nom et met en majuscule toutes les lettres qu&#39;il contient.

1. Cliquez sur le champ **Nom**.

   Le panneau de mappage s’ouvre.
1. Dans le panneau de mappage, cliquez sur l’icône **Texte et fonctions binaires**. ![Icône Fonctions de texte](assets/toolbar-icon-text&binary-functions.png)
1. Sélectionnez la fonction **upper**.

   La fonction apparaît dans le champ Nom, y compris la mise en forme de l’entrée attendue.

   L’entrée de cet exemple est le nom de l’événement à partir duquel le projet a été converti.

1. Déplacez le curseur entre les parenthèses, car c&#39;est là que va se trouver l&#39;entrée.
1. Dans le panneau de mappage, cliquez sur l’icône **Sortie du module**. ![&#x200B; Icône de sortie du module &#x200B;](assets/toolbar-icon-functions-you-map-from-other-modules.png)
1. Sélectionnez le bloc de nom qui a été généré par votre premier module.

   Le bloc de nom apparaît dans la fonction .

   ![Bloc de nom dans la fonction](assets/map-name.png)

1. Cliquez sur **OK** pour enregistrer les paramètres du module.

### Tester et activer

1. Testez le scénario en cliquant sur **Exécuter une fois** dans le coin inférieur gauche de l’écran.
1. Examinez la sortie pour vous assurer que le scénario s’est exécuté comme prévu.
1. Lorsque vous êtes convaincu que le scénario fonctionne comme prévu, cliquez sur le bouton (bascule) **Planification** dans le coin inférieur gauche de l’écran pour **Activé**.

   Le scénario est alors activé. Les scénarios actifs s’exécutent selon le planning défini dans le module de déclenchement.
1. Dans Workfront Fusion, cliquez sur **[!UICONTROL Enregistrer]** près du coin inférieur gauche pour enregistrer votre progression dans le scénario.

   >[!IMPORTANT]
   >
   >Sauvegardez souvent lorsque vous affinez et testez un scénario.

## Ressources

* [Mapper des éléments à l’aide de fonctions](/help//workfront-fusion/create-scenarios/map-data/map-using-functions.md)
