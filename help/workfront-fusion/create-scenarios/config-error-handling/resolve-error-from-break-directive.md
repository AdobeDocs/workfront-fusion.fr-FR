---
title: Résoudre les erreurs gérées par la directive Break
description: Parfois, il est utile de réexécuter un module en échec s’il existe une chance que la raison de l’échec puisse se résoudre rapidement.
author: Becky
feature: Workfront Fusion
exl-id: d568942c-2cd5-430c-bdbf-e1496da25b50
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 51%

---

# Résoudre les erreurs gérées par la directive Break

Lorsqu’une erreur est gérée par la directive Break, un enregistrement est créé dans le dossier Exécutions incomplètes . Cet enregistrement stocke l’état de l’exécution du scénario, ainsi que les données des modules précédents. L’enregistrement fait référence au module d’où provient l’erreur et contient des informations concernant les données reçues par le module en tant qu’entrée. Un enregistrement distinct est créé pour chaque paquet de données à l’origine de l’erreur.

Pour plus d’informations, voir [Affichage et résolution des exécutions incomplètes](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tout package de workflow Adobe Workfront et tout package d’automatisation et d’intégration Adobe Workfront</p><p>Workfront Ultimate</p><p>les packages Workfront Prime et Select, avec un achat supplémentaire de Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licences Adobe Workfront</td> 
   <td> <p>Standard</p><p>Travail ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Si votre entreprise dispose d’un package Select ou Prime Workfront qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acheter Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Résoudre les erreurs résultant de la directive Interrompre

Vous pouvez résoudre l’erreur manuellement en mettant à jour le scénario (si nécessaire) et en l’exécutant une fois.

Vous pouvez également configurer le scénario pour qu’il traite automatiquement une exécution incomplète en réexécutant le scénario. Pour configurer le module afin qu’il traite les exécutions incomplètes, procédez comme suit :

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez ajouter la solution de contournement.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Cliquez sur l’icône **Contrôle de flux** ![Contrôle de flux](assets/flow-control-icon.png) et sélectionnez **Saut**.
1. Dans le module Interrompre, activez l’option [!UICONTROL **Terminer automatiquement l’exécution**].
1. Dans le champ **Nombre de tentatives**, saisissez ou mappez le nombre maximum de fois que vous voulez que le module réessaie l’exécution

   Ce nombre doit être compris entre 1 et 100.
1. Dans le champ **Intervalle entre les tentatives**, saisissez ou mappez le nombre de minutes entre chaque nouvelle tentative.

Si cette option est activée, en cas d’erreur, l’exécution incomplète est récupérée (après le délai spécifié dans le champ [!UICONTROL Intervalle entre les tentatives]) et exécutée avec les données d’entrée originales. Cette opération se répète jusqu’à ce que l’exécution du module se termine sans erreur ou jusqu’à ce que le nombre de tentatives spécifié soit atteint.

>[!NOTE]
>
>Si la première tentative échoue, l’intervalle entre les tentatives augmente de manière exponentielle à chaque nouvelle tentative.


Lorsque l’option d’exécution Terminer automatiquement est activée, l’exécution du scénario est marquée comme « Succès », car la reprise automatique du gestionnaire d’erreurs Break gère automatiquement le problème. Dans ce cas, les personnes ne reçoivent pas d’e-mail concernant l’échec de l’exécution.

Lorsque l’option Exécution automatique est désactivée, l’exécution est marquée comme « Avertissement ».

Il existe quelques exceptions à l’enregistrement des exécutions dans la rubrique Exécutions incomplètes et, pour certains types d’erreurs, la reprise automatique de l’exécution d’un scénario n’est pas possible.

## Ressources

Pour plus d’informations, voir [Autoriser le stockage des exécutions incomplètes](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow-storing-incomplete-executions) dans l’article Configuration des paramètres de scénario.
