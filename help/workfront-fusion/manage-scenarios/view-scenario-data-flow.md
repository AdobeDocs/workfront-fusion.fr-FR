---
title: Afficher le flux de données dans un scénario
description: Vous pouvez regarder un scénario en cours d’exécution pour voir comment les données y circulent.
author: Becky
feature: Workfront Fusion
source-git-commit: 43f4dd92f7b15e32d956c889f7dccb1527f81d2d
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 25%

---

# Afficher le flux de données dans un scénario en cours d’exécution

Vous pouvez regarder un scénario en cours d’exécution pour voir comment les données y circulent.

Lorsqu’un scénario s’exécute, le module actif est marqué par un anneau croissant autour du module. L’anneau indique uniquement que le module est en cours d’exécution, et non sa progression. Les modules qui fonctionnent rapidement peuvent n’afficher qu’une petite partie de l’anneau.

![Entourer le module](assets/ring-around-module.png)

Une fois le module exécuté, un indicateur de sortie s’affiche.

![Indicateur de sortie ](assets/data-flow-output.png)

Si le module traite plusieurs lots, l&#39;anneau apparaît pour chaque lot traité, et l&#39;indicateur de sortie compte pour chaque lot qu&#39;il sort.

Pour plus d’informations sur le flux de données du scénario, voir [Flux d’exécution du scénario](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md).

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
   <td> <p>Nouvelle : [!UICONTROL Standard]</p><p>Ou</p><p>Actuelle : [!UICONTROL Work] ou niveau supérieur</p> </td> 
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
   <p>Nouveau :</p> <ul><li>Plan de [!DNL Workfront] [!UICONTROL Select] ou [!UICONTROL Prime] : votre entreprise doit acheter des [!DNL Adobe Workfront Fusion].</li><li>Plan de [!DNL Workfront] [!UICONTROL Ultimate] : [!DNL Workfront Fusion] est inclus.</li></ul>
   <p>Ou</p>
   <p>Actuel : votre entreprise doit acheter [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurations du niveau d’accès*</td> 
   <td> 
     <p>Vous devez être un administrateur ou une administratrice [!DNL Workfront Fusion] de votre organisation.</p>
     <p>Vous devez être un administrateur ou une administratrice [!DNL Workfront Fusion] de votre équipe.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Afficher le flux de données dans un scénario en cours d’exécution

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez afficher le flux de données.
1. Si le scénario n’est pas en cours d’exécution, activez-le ou cliquez sur **Exécuter une fois** pour lancer l’exécution du scénario.
1. Sélectionnez l’exécution à afficher dans la section En cours d’exécution du panneau Historique d’exécution.

![ En cours d’exécution ](assets/currently-running.png)


