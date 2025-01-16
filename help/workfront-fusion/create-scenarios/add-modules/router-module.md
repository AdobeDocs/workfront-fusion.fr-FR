---
title: Ajouter un module Routeur et configurer des itinéraires
description: Le module routeur vous permet de diviser votre flux en plusieurs itinéraires et de traiter les données de chaque itinéraire différemment. Une fois qu’un module routeur reçoit un lot, il le transfère vers chaque itinéraire connecté dans l’ordre où les itinéraires ont été joints au module routeur.
author: Becky
feature: Workfront Fusion
exl-id: 8344cde4-df3e-4b72-9d10-46ff4b186400
source-git-commit: 839f6edf93df8a935b2c5d0a520bdc125fe60288
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 15%

---

# Ajouter un module Routeur et configurer des itinéraires

Le module Routeur vous permet de diviser votre scénario en plusieurs itinéraires et de traiter les données de chaque itinéraire différemment. Lorsqu&#39;un module de routeur reçoit un lot, il le transmet à chaque route connectée dans l&#39;ordre dans lequel les routes ont été attachées au module de routeur.

Les itinéraires sont traités de manière séquentielle, et non en parallèle. Un lot n’est pas envoyé vers l’itinéraire suivant tant qu’il n’a pas été complètement traité par l’itinéraire précédent.


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

## Ajouter un module Routeur à un scénario

Vous devez ajouter un module Routeur avant de configurer des itinéraires.

1. Cliquez sur l’onglet **[!UICONTROL Scenarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez ajouter un routeur.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Dans l&#39;éditeur de scénarios, cliquez sur la poignée droite du module après lequel vous souhaitez ajouter le routeur.
1. Sélectionnez **[!UICONTROL Flow Control]** > **Router** dans la liste des modules qui s’affiche.

   ![](assets/connect-the-router-350x108.png)

   Ou

   Pour insérer le module Router entre deux modules, cliquez sur l&#39;icône de clé à molette sous l&#39;itinéraire reliant les deux modules et sélectionnez **[!UICONTROL Add a router]** dans le menu.

   ![](assets/insert-router-350x191.png)
1. Ajoutez la première route au routeur en cliquant sur la poignée droite du routeur et ajoutez un module, comme pour ajouter un module.
1. Pour ajouter un autre itinéraire, cliquez sur le module de routeur. Un itinéraire s’affiche. Ajoutez des modules à cet itinéraire, si vous le souhaitez.

   Vous pouvez ajouter autant d’itinéraires que vous le souhaitez.

1. Pour vérifier l’ordre des itinéraires, cliquez sur l’icône Alignement automatique ![icône Alignement automatique](assets/auto-align.png).

   Les itinéraires sont organisés dans l’ordre dans lequel ils s’exécutent. L’itinéraire supérieur s’exécute en premier.

1. (Facultatif) Pour modifier l&#39;ordre des itinéraires, annulez la liaison des itinéraires en cliquant avec le bouton droit sur le chemin du routeur et en sélectionnant Annuler la liaison, puis en les faisant glisser vers le module de routeur dans l&#39;ordre souhaité. La première route jointe sera la première route à exécuter (la route supérieure).

1. Passez à [Ajouter un filtre à un itinéraire](#add-a-filter-to-a-route).

## Ajouter un filtre à un itinéraire

Vous pouvez placer un filtre sur un itinéraire après le module Routeur pour filtrer les lots. Seuls les lots qui passent par le filtre seront gérés par les modules sur l’itinéraire.

Si les données franchissent le filtre de plusieurs itinéraires, les données sont gérées par les deux itinéraires. L’itinéraire supérieur gère d’abord les données.

1. Cliquez sur l’onglet **[!UICONTROL Scenarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez ajouter un filtre.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Cliquez sur l’icône clé à molette ![Clé à molette](assets/wrench-icon.png) sur le chemin d’accès où vous souhaitez définir un filtre. Il s&#39;agit du chemin entre le module de routage et le premier module de la route.
1. Sélectionnez **Configurer un filtre.**
1. Dans le champ libellé du panneau qui s’affiche, ajoutez un libellé. Ce libellé s’affiche dans le scénario.
1. Configurez les conditions de filtrage.

   Pour plus d’informations, voir [Ajouter un filtre à un scénario](/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md).

1. Cliquez sur **[!UICONTROL OK]** pour enregistrer la configuration des filtres.

1. Passez à [ Configurer un itinéraire de secours ](#configure-a-fallback-route).

## Configuration d’un itinéraire de secours

L’itinéraire de secours est l’itinéraire qui s’exécute sur les lots qui ne transmettent aucun filtre à un autre itinéraire.

Vous pouvez activer un itinéraire de secours dans le panneau de filtrage.

1. Cliquez sur l’onglet **[!UICONTROL Scenarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez ajouter un itinéraire de secours.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Cliquez sur l’icône clé à molette ![Clé à molette](assets/wrench-icon.png) sur le chemin d’accès où vous souhaitez définir un filtre. Il s&#39;agit du chemin entre le module de routage et le premier module de la route.
1. Sélectionnez **Configurer un filtre.**
1. Dans le champ libellé du panneau qui s’affiche, ajoutez un libellé. Ce libellé s’affiche dans le scénario.
1. Cochez la case itinéraire de secours .

   ![](assets/fallback-route-350x260.png)

1. Cliquez sur **[!UICONTROL OK]** pour enregistrer la configuration des filtres.

L’itinéraire de secours est signalé par une flèche différente dans le module Router :

![](assets/arrow-sign-in-router-module-350x361.png)

## Exemple : cas d’utilisation `if/else`

>[!BEGINSHADEBOX]

Un cas d’utilisation type de la route de secours consiste à poursuivre le flux avec une route si la condition est remplie et avec une autre route si elle ne l’est pas. comme dans les étapes suivantes :

Dans cet exemple, le premier itinéraire est configuré avec un filtre. Il s’agit du composant `if`.

![](assets/set-up-a-filter-2-350x242.png)

La deuxième route est configurée comme route de secours. Il s’agit du composant `else`.

![](assets/enable-fallback-route-option-350x238.png)

>[!ENDSHADEBOX]
