---
title: Ajout d’un filtre à un scénario
description: Dans certains scénarios, vous devez travailler uniquement avec des lots qui répondent à des critères spécifiques. Les filtres vous permettent de sélectionner ces lots.
author: Becky
feature: Workfront Fusion
exl-id: b507dca0-0e85-4ab7-8310-b6e6bcb7ae12
source-git-commit: 839f6edf93df8a935b2c5d0a520bdc125fe60288
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 34%

---

# Ajout d’un filtre à un scénario

Dans certains scénarios, vous devez travailler uniquement avec des lots qui répondent à des critères spécifiques. Les filtres vous permettent de sélectionner ces lots.

Par exemple, vous pouvez créer un scénario avec le déclencheur [!UICONTROL Watch records] pour que les [!DNL Workfront] capturent uniquement les tâches affectées à un utilisateur spécifique.

Vous pouvez ajouter un filtre entre deux modules et vérifier si les lots reçus des modules précédents remplissent des conditions de filtrage spécifiques :

* Si tel est le cas, les lots sont transmis au module suivant dans le scénario.
* Dans le cas contraire, le traitement des lots s’arrête.

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

Vous devez ajouter les deux modules à un scénario avant de pouvoir ajouter un filtre entre eux.

## Ajoutez un filtre entre deux modules :

1. Cliquez sur l’onglet **[!UICONTROL Scenarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez ajouter un filtre.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Cliquez sur l’icône de clé à molette ![icône de clé à molette](assets/wrench-icon.png) entre les modules auxquels vous souhaitez ajouter un filtre, puis sélectionnez **Configurer un filtre**.
1. Dans la zone qui s’affiche, saisissez un **[!UICONTROL Label]** pour le filtre.
1. Définissez le **[!UICONTROL Condition]** de filtre.

   Saisissez le champ selon lequel vous souhaitez filtrer dans le premier champ, l’opérateur et (si nécessaire) la valeur avec laquelle vous souhaitez comparer le champ.

   >[!TIP]
   >
   >Vous pouvez saisir des valeurs dans les champs de filtre à partir du panneau de mappage
   >Pour plus d’informations sur le mappage, voir [Mapper des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

   Par exemple, si vous souhaitez que le filtre transmette les fichiers dans [!DNL Adobe Workfront] se terminant par XML, vous devez saisir **[!UICONTROL File name]** dans la première zone et .**[!UICONTROL xml]** dans la deuxième case. Dans le menu déroulant situé entre les deux, sélectionnez **[!UICONTROL Ends with (case insensitive)]**. Ce filtre s’applique aux lots entrants du premier module (Workfront). Seuls les lots contenant des fichiers XML sont transmis au module suivant.

   ![](assets/set-up-filter-box.png)

1. Cliquez sur **[!DNL OK]**.

## Copier un filtre

Actuellement, l’éditeur de scénarios inclut une fonctionnalité permettant de copier un filtre.

>[!NOTE]
>
>Si vous copiez les modules de chaque côté du filtre, le filtre est également copié.
>
>Pour plus d’informations sur la copie de modules, voir [Copier des modules ou des scénarios dans [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/add-modules/copy-modules-or-scenarios.md).

Pour copier un filtre sans copier de modules, vous pouvez utiliser l’outil de développement Fusion

1. Cliquez sur l’onglet **[!UICONTROL Scenarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez ajouter un filtre.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Ouvrez Fusion DevTool en cliquant sur l’icône DevTool ![icône DevTool](assets/debugger-icon.png) près du bas de l’écran.

   Si l’icône DevTool ne s’affiche pas, consultez [Déboguer un scénario](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md) pour obtenir des instructions sur l’ouverture de l’outil de développement.

1. Cliquez sur l’icône **[!UICONTROL Tools]** ![](assets/devtools-tools-icon.png) dans la barre latérale gauche.

1. Cliquez sur **[!UICONTROL Copy Filter]**, puis configurez l’outil **[!UICONTROL Copy Filter]** dans le panneau latéral droit :

   1. Définissez le **[!UICONTROL Source Module]** comme module directement après le filtre que vous souhaitez copier.
   1. Définissez le **[!UICONTROL Target Module]** comme le module juste après lequel vous souhaitez placer le filtre.

1. Cliquez sur **[!UICONTROL Run]**.
