---
title: Ajouter un filtre à un scénario
description: Dans certains scénarios, vous devez travailler uniquement avec des lots qui répondent à des critères spécifiques. Les filtres vous permettent de sélectionner ces lots.
author: Becky
feature: Workfront Fusion
exl-id: b507dca0-0e85-4ab7-8310-b6e6bcb7ae12
source-git-commit: a871a130a1ac023dcb4ce8da7241918da2431d3a
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 45%

---

# Ajouter un filtre à un scénario

Dans certains scénarios, vous devez travailler uniquement avec des lots qui répondent à des critères spécifiques. Les filtres vous permettent de sélectionner ces lots.

Par exemple, vous pouvez créer un scénario avec le déclencheur [!UICONTROL Observer des enregistrements] pour que Workfront capture uniquement les tâches affectées à un utilisateur spécifique.

Vous pouvez ajouter un filtre entre deux modules et vérifier si les lots reçus des modules précédents remplissent des conditions de filtrage spécifiques :

* Si tel est le cas, les lots sont transmis au module suivant dans le scénario.
* Dans le cas contraire, le traitement des lots s’arrête.

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

Vous devez ajouter les deux modules à un scénario avant de pouvoir ajouter un filtre entre eux.

## Ajoutez un filtre entre deux modules :

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez ajouter un filtre.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Cliquez sur l’icône de clé à molette ![icône de clé à molette](assets/wrench-icon.png) entre les modules auxquels vous souhaitez ajouter un filtre, puis sélectionnez **Configurer un filtre**.
1. Dans la zone qui s’affiche, saisissez un **[!UICONTROL Libellé]** pour le filtre.
1. Définissez le filtre **[!UICONTROL Condition]**.

   Saisissez le champ selon lequel vous souhaitez filtrer dans le premier champ, l’opérateur et (si nécessaire) la valeur avec laquelle vous souhaitez comparer le champ.

   >[!TIP]
   >
   >Vous pouvez saisir des valeurs dans les champs de filtre à partir du panneau de mappage
   >Pour plus d’informations sur le mappage, voir [Mapper des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

   Par exemple, si vous souhaitez que le filtre transmette les fichiers dans Adobe Workfront se terminant par XML, vous devez saisir **[!UICONTROL Nom du fichier]** dans la première zone et ..**[!UICONTROL xml]** dans le second champ. Dans le menu déroulant qui sépare les champs, vous pouvez sélectionner **[!UICONTROL Se termine par (non sensible à la casse)]**. Ce filtre s’applique aux lots entrants du premier module (Workfront). Seuls les lots contenant des fichiers XML sont transmis au module suivant.

   ![Configurer un filtre](assets/set-up-filter-box.png)

1. Cliquez sur **[!DNL OK]**.

## Copier un filtre

Actuellement, l’éditeur de scénarios inclut une fonctionnalité permettant de copier un filtre.

>[!NOTE]
>
>Si vous copiez les modules de chaque côté du filtre, le filtre est également copié.
>
>Pour plus d’informations sur la copie de modules, voir [Copie de modules ou de scénarios dans Adobe Workfront Fusion](/help/workfront-fusion/create-scenarios/add-modules/copy-modules-or-scenarios.md).

Pour copier un filtre sans copier de modules, vous pouvez utiliser l’outil de développement Fusion

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez ajouter un filtre.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Ouvrez Fusion DevTool en cliquant sur l’icône DevTool ![icône DevTool](assets/debugger-icon.png) près du bas de l’écran.

   Si l’icône DevTool ne s’affiche pas, consultez [Déboguer un scénario](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md) pour obtenir des instructions sur l’ouverture de l’outil de développement.

1. Cliquez sur l’icône **[!UICONTROL Outils]** ![Outils DevTool](assets/devtools-tools-icon.png) dans la barre latérale gauche.

1. Cliquez sur **[!UICONTROL Copier le filtre]**, puis configurez l’outil **[!UICONTROL Copier le filtre]** dans le panneau latéral droit :

   1. Définissez le module **[!UICONTROL Source]** comme module juste après le filtre que vous souhaitez copier.
   1. Définissez le **[!UICONTROL module cible]** comme le module juste après lequel vous souhaitez placer le filtre.

1. Cliquez sur **[!UICONTROL Exécuter]**.
