---
title: Configuration d’un module
description: Vous devez configurer les paramètres de chaque module que vous créez.
author: Becky
feature: Workfront Fusion
exl-id: ae82d1fe-31e1-424a-9c1a-42dc1a20b749
source-git-commit: c83070a7c2d1d048000a4eace4aaede73c7ec49d
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 41%

---

# Configuration d’un module

Vous devez configurer les paramètres de chaque module que vous créez.

Par exemple, le module Workfront > Charger le document nécessite que vous spécifiiez l’enregistrement dans lequel vous souhaitez charger un document.

>[!NOTE]
>
>Outre les paramètres du module, vous pouvez également ajuster les paramètres d’un scénario. Vous pouvez renommer votre scénario, modifier sa planification et spécifier des paramètres supplémentaires, entre autres actions.

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

+++## Configurer les paramètres d&#39;un module

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez ajouter un filtre.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Ajoutez un nouveau module à un scénario.

   Ou

   Cliquez sur le module que vous souhaitez configurer.

1. Si cela est nécessaire pour le module, créez une **[!UICONTROL Connexion]** à votre compte d’utilisateur enregistré pour ce service donné, comme décrit dans la section [Vue d’ensemble des connexions](/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md).
1. Dans chaque champ, saisissez le texte approprié.

   Ou

   Mappez la sortie d’un module précédent dans le champ .

   Pour plus d’informations sur le mappage, voir [Présentation du mappage](/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md).

   Pour plus d’informations sur les différents types de données d’élément que Workfront Fusion peut reconnaître (comme la date, le nombre et le texte), voir [Types de données d’élément](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md).

   >[!NOTE]
   >
   >Les paramètres en gras sont requis.

1. (Le cas échéant) Si le module a des options avancées que vous souhaitez afficher et utiliser, sélectionnez **[!UICONTROL Afficher les paramètres avancés]**.
