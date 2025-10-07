---
title: Mise à jour d’un module vers une nouvelle version
description: Comme les applications auxquelles Workfront Fusion se connecte peuvent mettre à jour ou publier de nouvelles versions, il est parfois nécessaire que Fusion publie des modules mis à jour pour ces applications.
author: Becky
feature: Workfront Fusion
exl-id: b7f07fa5-9d81-48b3-b0ce-7a18b3b44508
source-git-commit: d0d9d7cdad993ecceaa0abf0ac69e9a9abd78b69
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 16%

---

# Mettre à niveau un module vers une nouvelle version

Comme les applications auxquelles Workfront Fusion se connecte peuvent mettre à jour ou publier de nouvelles versions, il est parfois nécessaire que Fusion publie des modules mis à jour pour ces applications.

Si l’icône verte du module de mise à niveau s’affiche sur un module dans un scénario, Workfront Fusion a publié une nouvelle version de ce module.

![Icône Mettre à jour](assets/update-indicator-workfront.png)

Vous pouvez mettre à jour le module sans créer de scénario.

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
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurations du niveau d’accès*</td> 
   <td> 
     <p>Vous devez être administrateur ou administratrice Workfront Fusion pour votre entreprise.</p>
     <p>Vous devez être un administrateur Workfront Fusion pour votre équipe.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Mise à niveau d’un module Workfront vers une nouvelle version

1. Cliquez sur l’icône **Mettre à niveau le module** ![Icône Mettre à niveau](assets/upgrade-icon.png) du module que vous souhaitez mettre à niveau vers une nouvelle version.
   ![Icône Mettre à jour](assets/update-indicator-workfront.png)
1. Choisissez l’une des options suivantes :

   * Pour sélectionner un nouveau module pour remplacer ce module (au lieu de mettre à niveau le module), cliquez sur **Choisir nouveau**, puis procédez comme décrit dans [Mettre à niveau un module non Workfront vers une nouvelle version](#upgrade-a-non-workfront-module-to-a-new-version).
   * Pour mettre à niveau uniquement ce module, en conservant la configuration du module, cliquez sur **Mettre à niveau**.
   * Pour mettre à niveau tous les modules Workfront du scénario, cliquez sur **Tout mettre à niveau**.

1. Enregistrez le scénario.

>[!NOTE]
>
>Si vous avez mis à niveau les modules Workfront, nous vous recommandons de les ouvrir et de vérifier leur configuration.

## Mettre à niveau un module non Workfront vers une nouvelle version

1. Cliquez sur l’icône **Mettre à niveau le module** ![Icône Mettre à niveau](assets/upgrade-icon.png) du module que vous souhaitez mettre à niveau vers une nouvelle version.
   ![Icône Mettre à jour](assets/update-indicator.png)
1. Cliquez sur **Choisir nouveau**.
1. Sélectionnez le module qui doit remplacer le module précédent.
1. Configurez le module avec les mêmes paramètres que le module existant.
1. Connectez le nouveau module au scénario au même endroit que le module existant.
1. Supprimez l’ancien module.
1. Enregistrez le scénario.
