---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: connections-annd-webhooks
title: Gérer les connexions
description: Pour la plupart des applications, il est nécessaire de créer une connexion par laquelle Adobe Workfront Fusion peut communiquer avec le service tiers donné en fonction des paramètres du scénario spécifique.
author: Becky
feature: Workfront Fusion
exl-id: 26d7caad-8e12-4f04-ac7c-f71686c90ee6
source-git-commit: 93d06cb917680f9cabc1bad6be0f9cd843449d07
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 21%

---

# Gérer les connexions

Une connexion représente l’autorisation et les droits utilisés par Fusion pour accéder à l’application. Vous pouvez créer une ou plusieurs connexions pour chaque application et utiliser la même connexion dans plusieurs modules ou scénarios.

Vous pouvez gérer ces connexions dans la zone Connexions .

Pour plus d’informations sur les connexions, voir [&#x200B; Présentation de la connexion &#x200B;](/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md).

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
   <td role="rowheader">Licence Adobe Workfront Fusion</td> 
   <td>
   <p>Basé sur les opérations : aucune exigence de licence Workfront Fusion</p>
   <p>Basé sur un connecteur (hérité) : pour vous connecter à des applications en dehors de la famille de produits Workfront, vous devez disposer de Workfront Fusion for Work Automation and Integration </p>
   </td> 
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

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Affichage et gestion des connexions

Vous pouvez gérer toutes les connexions à partir de la zone Connexions .

>[!NOTE]
>
>Les connexions appartiennent à des équipes. Si vous ne trouvez pas la connexion que vous recherchez, vérifiez que vous consultez l’équipe appropriée.
>
>Pour sélectionner une nouvelle équipe, cliquez sur le nom de l’équipe dans le volet de navigation de gauche, puis sélectionnez une nouvelle équipe.

1. Pour ouvrir la zone Connexions, cliquez sur **Connexions** ![Icône Connexions](assets/connections-icon.png) dans le volet de navigation de gauche.
1. Recherchez la connexion à gérer, puis effectuez une ou plusieurs des étapes suivantes dans la ligne pour cette connexion.
1. (Facultatif) Attribuez un environnement et un type de connexion en cliquant sur les listes déroulantes **Environnement** et **Type** et en sélectionnant une option.
1. (Facultatif) Pour afficher les autorisations accordées à Workfront Fusion pour la connexion, cliquez sur l’icône Affichage ![Afficher les autorisations de connexion](assets/view-connection-permissions.png) pour cette connexion.
1. (Facultatif) Pour renommer une connexion, mettez en surbrillance son nom et saisissez le nouveau nom.
1. (Facultatif) Pour réautoriser une connexion, cochez la case en regard de la connexion, puis cliquez sur **Réautoriser** en bas de l’écran.
1. (Facultatif) Pour supprimer une connexion, cochez la case en regard de la connexion, cliquez sur **Supprimer** en bas de l’écran, puis sur **Vraiment ?**.
1. (Facultatif) Pour vérifier que la connexion au service a été établie avec succès, cochez la case en regard de la connexion, puis cliquez sur **Vérifier** en bas de l’écran.
1. (Facultatif) Pour afficher les scénarios actifs qui utilisent cette connexion, cochez la case en regard de la connexion, puis cliquez sur **Récupérer les scénarios actifs**. Vous pouvez ensuite cliquer sur un scénario dans la liste Scénarios actifs pour y accéder.

## Renouveler une connexion

Workfront Fusion obtient généralement des droits d’accès à un service donné pendant une période illimitée. Certaines applications exigent que l’autorisation d’accès soit renouvelée après un certain temps. Dans ce cas, Workfront Fusion vous avertit par e-mail peu de temps avant l’expiration de ses droits d’accès.

Pour renouveler une connexion :

1. Pour ouvrir la zone Connexions, cliquez sur **Connexions** ![Icône Connexions](assets/connections-icon.png) dans le volet de navigation de gauche.
1. Recherchez la connexion à renouveler.
1. Sur la ligne correspondant à cette connexion, cochez la case en regard de la connexion, puis cliquez sur **Réautoriser** en bas de l’écran.

## Ressources

* Pour plus d’informations sur les métadonnées de connexion, telles que l’environnement et le type, consultez [Métadonnées de connexion](/help/workfront-fusion/references/connections/connection-metadata.md).
