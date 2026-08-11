---
title: Définir les options de notification
description: Les options de notification par e-mail sont définies au niveau de l’équipe.
author: Becky
feature: Workfront Fusion
exl-id: 570a09fc-01a9-4952-8a2b-8bfdd86d0bd8
TQID: https://experienceleague.adobe.com/-HytP4gfrhiiSn-dg5ndg1YC6NTMC-NURYzSFgO5kIo
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 90a58033e240271b88d01b9daef9763f38264056
workflow-type: tm+mt
source-wordcount: 665
ht-degree: 15%

---

# Définir les options de notification

Si votre entreprise utilise Adobe Unified Shell, vous recevez des notifications via la zone des Notifications Adobe.

Si votre organisation n’a pas été migrée vers Adobe Unified Shell, vous pouvez choisir les notifications qu’une équipe reçoit. Les notifications sont définies au niveau de l’équipe.

Vous pouvez contrôler les situations pour lesquelles des notifications sont envoyées :

* Envoyer une notification en cas d’avertissement : Fusion envoie une notification lorsqu’une exécution de scénario consigne un avertissement.
* Envoyer une notification en cas d’erreur : Fusion envoie une notification lorsqu’une exécution de scénario échoue.
* Avertir lorsque le scénario est désactivé : Fusion envoie une notification lorsqu’un scénario est désactivé automatiquement, par exemple après trop d’erreurs consécutives.

Vous pouvez définir des notifications au niveau de l’équipe ou du scénario. Les notifications au niveau du scénario remplacent les notifications définies au niveau de l’équipe. En d’autres termes, si un paramètre de scénario est en contradiction directe avec un paramètre d’équipe, le paramètre de scénario est suivi. Les paramètres de notification d’équipe indiquent s’il existe des remplacements pour ce paramètre.

Par défaut, tous les types de notification sont activés dans Workfront Fusion.

>[!IMPORTANT]
>
>Pour recevoir des notifications de Workfront Fusion, les notifications Fusion doivent être activées dans les paramètres de notification d’Adobe CX Enterprise. Pour accéder à ces paramètres, cliquez sur la cloche de notification dans le coin supérieur droit de l’écran, puis sur l’icône des paramètres.

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
  <tr data-mc-conditions=""> 
   <td role="rowheader">Rôle</td> 
   <td> 
     <p>Vous devez être membre de l’organisation et de l’équipe Fusion pour lesquelles vous ajustez les paramètres de notification.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation Workfront](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Afficher et gérer les paramètres de notification au niveau de l’équipe

1. Dans Workfront Fusion, cliquez sur **Présentation de l’équipe** dans le volet de navigation de gauche.
1. Cliquez sur l’onglet **Options de notification**.

   La liste Options de notification s’ouvre. S’il existe des remplacements, leur nombre s’affiche en regard de ce paramètre.

1. (Conditionnel) S’il existe des remplacements, pour voir quels scénarios remplacent le paramètre de notification de l’équipe, cliquez sur le menu à trois points de ce paramètre.

   Vous pouvez cliquer sur un scénario dans ce menu pour y accéder directement.

   ![Menu Remplacer le scénario](assets/view-notification-override.png)

1. Pour restaurer les paramètres par défaut d’un type de notification, consultez [Restaurer les paramètres par défaut des notifications](#restore-notification-defaults) dans cet article.

Les modifications apportées à la liste des options de Notifications sont enregistrées automatiquement.

## Définition des paramètres de notification au niveau du scénario

Le paramètre de notification pour chaque scénario est défini dans le panneau Paramètres du scénario de ce scénario.

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez ajouter un filtre.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Cliquez sur l’icône [!UICONTROL Paramètres du scénario] ![Icône Paramètres du scénario](assets/scenario-settings-icon.png) au bas de votre scénario.
1. Dans le panneau Paramètres du scénario, cliquez sur **Afficher les paramètres avancés** au bas du panneau.
1. Ajustez les paramètres **Notifier en cas d’avertissement**, **Notifier en cas d’erreur** et **Notifier lorsque le scénario est désactivé** selon vos besoins.
1. Cliquez sur **OK** pour enregistrer et quitter les paramètres du scénario.

## Restaurer les paramètres par défaut des notifications

Vous pouvez restaurer le paramètre de notification par défaut d’une équipe à partir de l’onglet Options de notification . Cette option définit l’option de notification sur activée et supprime tous les remplacements de notification de scénario pour ce type de notification.

Si le type de notification est actuellement défini sur les valeurs par défaut, l’icône **Restaurer les valeurs par défaut** n’est pas visible.

1. Dans Workfront Fusion, cliquez sur **Présentation de l’équipe** dans le volet de navigation de gauche.
1. Cliquez sur l’onglet **Options de notification**.

   La liste Options de notification s’ouvre. Si un type de notification n’est pas actuellement défini sur les valeurs par défaut, l’icône Restaurer les valeurs par défaut est visible pour ce type de notification.

   ![Rétablir le paramètre visible par défaut](assets/restore-notification-defaults.png)

1. Pour restaurer les paramètres par défaut pour ce type de notification, y compris les remplacements de scénario, cliquez sur l’icône **Réinitialiser aux valeurs par défaut** ![Réinitialiser aux valeurs par défaut](assets/restore-default-icon.png) pour ce type de notification.

Les modifications apportées à la liste des options de Notifications sont enregistrées automatiquement.

<!--

## Set notification options

If your organization is not on the Adobe Unified Shell, you can set notification settings directly in Fusion.

Email notification options are set on the team level.

1. In the left navigation panel, click **[!UICONTROL Team]**
1. Select the **[!UICONTROL Notification Options]** tab.
1. Enable the notifications that you want the team to receive.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">'[!UICONTROL Warning in scenario run]'</td> 
      <td> <p>Receive an email when there is a warning in a scenario run</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Errors in scenario run]</td> 
      <td>Receive an email when there is an error in a scenario run.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Scenario deactivation]</p> </td> 
      <td><p>Receive an email when a scenario deactivates.</p><p>In some cases, a scenario might be deactivated by the Workfront Fusion engineering team because the scenario is causing performance or other issues. In these cases, you do not receive notifications in Workfront Fusion. </p></td>

</tr>
</tbody>
</table>

Changes to notification options save automatically.

-->
