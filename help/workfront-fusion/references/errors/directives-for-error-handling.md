---
content-type: reference
title: Directives relatives au traitement des erreurs
description: Cet article décrit les directives que vous pouvez utiliser pour la gestion des erreurs dans vos scénarios Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: d7b0141f-d99d-4ab7-a60f-ed552a76f05d
source-git-commit: a871a130a1ac023dcb4ce8da7241918da2431d3a
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 42%

---

# Directives pour la gestion des erreurs

Les directives de gestion des erreurs vous permettent de choisir ce qui se produit lorsqu’un scénario rencontre une erreur.

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

## Directives pour la gestion des erreurs

Les directives de gestion des erreurs suivantes sont disponibles dans Workfront Fusion.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>Restauration</p> <p> <img src="assets/rollback.png"> </p> </td> 
   <td> <ul><li><p>L’exécution du scénario est arrêtée immédiatement.</li><li>Une phase de restauration est lancée sur tous les modules, dans une tentative de les restaurer tous à leur état initial. </li><li>Les modules suivants ne sont pas traités.</p></li><li> <p>Dans la plupart des cas, le scénario est désactivé après le nombre d’erreurs consécutives spécifié dans les paramètres du scénario. Pour plus d’informations, voir <a href="/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#number-of-consecutive-errors" class="MCXref xref">Nombre d’erreurs consécutives</a>.</p> </li><li><p>Le statut d’exécution du scénario est marqué comme « Erreur ».</p></li></ul> <p><b>Remarque </b> : il s’agit du comportement par défaut si aucun itinéraire de gestionnaire d’erreurs n’est associé au module et que le paramètre <a href="/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow-storing-incomplete-executions" class="MCXref xref">Autoriser le stockage des exécutions incomplètes</a>Autoriser le stockage des exécutions incomplètes sous les paramètres du scénario  n’est pas coché.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Valider</p> <p> <img src="assets/commit.png"> </p> </td> 
   <td> <ul><li><p>L’exécution du scénario est arrêtée immédiatement.</li><li>Une phase de validation est lancée sur tous les modules. </li><li>Les modules suivants ne sont pas traités.</p></li><li> <p>Tous les lots non traités sont ignorés.</p> </li><li><p>Le statut d’exécution du scénario est marqué comme « succès ». </p> </li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Reprendre</p> <p> <img src="assets/resume.png"> </p> </td> 
   <td> <ul><li><p>Une sortie de substitution est spécifiée et fournie au module qui rencontre une erreur.</p> </li><li><p>Les modules suivants sont traités.</p></li><li> <p>Le statut d’exécution du scénario est marqué comme « succès ».</p></li></ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Ignorer</p> <p> <img src="assets/ignore.png"> </p> </td> 
   <td><ul><li> <p>L’erreur est ignorée.</li><li> Les modules suivants ne sont pas traités.</p> </li><li><p>S’il existe des bundles non traités, l’exécution du scénario se poursuit normalement.</p> </li><li><p>Le statut d’exécution du scénario est marqué comme « succès ».</p> </li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Interrompre</p> <p> <img src="assets/break.png"> </p> </td> 
   <td><ul><li> <p>Le statut de l’exécution du scénario est stocké dans la file d’attente des exécutions incomplètes où l’erreur peut être résolue manuellement. Pour plus d’informations, voir <a href="/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md" class="MCXref xref">Affichage et résolution des exécutions incomplètes</a>.</p> <p>Il existe toutefois quelques exceptions. Pour plus d’informations, voir <a href="/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow" class="MCXref xref">Autoriser le stockage des exécutions incomplètes</a> dans l’article Configuration des paramètres de scénario</a>.</p></li><li> <p>Les modules suivants ne sont pas traités.</p></li><li> <p>S’il existe des bundles non traités, l’exécution du scénario se poursuit normalement.</p> </li><li><p>Le statut d’exécution du scénario est marqué comme « avertissement » lorsque l’option [!UICONTROL Automatically complete execution] est désactivée.</p></li></ul> <p>Pour plus d’informations, consultez la section <a href="#break" class="MCXref xref">[!UICONTROL Break]</a> de cet article</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Réessayer</p> <p> <img src="assets/retry.png"> </p> </td> 
   <td> <p>Dans certains cas, il peut s’avérer utile de réexécuter un module défaillant lorsqu’il y a une chance que la raison de la défaillance passe au fil du temps.</p> <p>Workfront Fusion n’offre pas actuellement la directive de reprise, mais plusieurs solutions de contournement peuvent être utilisées pour imiter sa fonctionnalité. Pour plus d’informations, voir <a href="/help/workfront-fusion/create-scenarios/config-error-handling/retry.md" class="MCXref xref">Gestion des reprises d’erreurs</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>* Les directives de gestion des erreurs ne peuvent pas être utilisées en dehors d’une route de gestion des erreurs.
>* Workfront Fusion ne propose actuellement pas de module de génération qui vous permettrait de générer facilement des erreurs de manière conditionnelle. Il est toutefois possible d’utiliser une solution pour imiter ses fonctionnalités.
>
>  Pour plus d’informations, voir [Configurer `throw` solution de contournement d’erreur](/help/workfront-fusion/create-scenarios/config-error-handling/throw.md).

## Ressources

* Pour plus d’informations sur la restauration et la phase de restauration, consultez [Restauration](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md#rollback) dans l’article Exécution du scénario, cycles et phases.
* Pour plus d’informations sur la phase de validation, consultez la section [Validation](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md#commit) dans l’article Exécution du scénario, cycles et phases.
