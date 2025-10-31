---
title: Créer une connexion - Instructions de base
description: De nombreux connecteurs Adobe Workfront Fusion ne nécessitent pas de configuration personnalisée lors de la création d’une connexion. Cet article décrit le processus de création de connexion par défaut.
author: Becky
feature: Workfront Fusion
exl-id: e47ab4d9-6612-4d9a-a024-da508a8bbfb2
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 31%

---

# Créer une connexion - Instructions de base

De nombreux connecteurs Adobe Workfront Fusion ne nécessitent pas de configuration personnalisée lors de la création d’une connexion. Cet article décrit le processus de création de connexion par défaut.

>[!NOTE]
>
>
>Si Adobe Workfront Fusion ne propose pas d’application pour le service web que vous souhaitez utiliser dans votre scénario, vous pouvez vous connecter au service web à l’aide des modules HTTP et Webhooks de Workfront Fusion, comme expliqué dans les articles suivants :
>
>* [Connectez Adobe Workfront Fusion à un service web qui utilise l’autorisation de jeton API](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-wf-web-service-uses-api-token-auth.md)
>* [Configurer un webhook pour un service web sans connecteur](/help/workfront-fusion/create-scenarios/add-modules/receive-a-webhook-from-a-web-service.md)

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

## Créer une connexion

Pour créer une connexion à une application donnée, vous devez être dans un module pour cette application. Par exemple, pour créer une connexion à Workfront, vous devez être dans un module Workfront.

Pour créer une connexion dans un module Workfront Fusion :

1. Dans n’importe quel module de l’application donnée, cliquez sur **[!UICONTROL Ajouter]** en regard de la zone [!UICONTROL Connexion] pour ouvrir le panneau **[!UICONTROL Créer une connexion]**.
1. (Facultatif) Modifiez le **[!UICONTROL Nom de la connexion]** par défaut.
1. Dans le champ Environnement , indiquez s’il s’agit d’un environnement de production ou d’un environnement hors production.
1. Dans le champ Type , indiquez s’il s’agit d’un compte de service ou personnel.
1. (Le cas échéant) Si l’application nécessite des paramètres de connexion avancés, tels qu’un identifiant, une clé ou [!UICONTROL secret], saisissez ces informations.

   Vous devrez peut-être cliquer sur **[!UICONTROL Afficher les paramètres avancés]** pour afficher les champs dans lesquels vous pouvez saisir ce type d’informations.

1. Cliquez sur **[!UICONTROL Continuer]**.
1. Dans la fenêtre de connexion qui s’affiche, saisissez vos informations d’identification pour vous connecter à l’application si vous ne l’avez pas déjà fait.
1. (Conditionnel) Si un bouton **[!UICONTROL Autoriser]** s’affiche, examinez les actions que le connecteur peut effectuer, puis cliquez sur le bouton pour connecter l’application à Workfront Fusion.

   >[!NOTE]
   >
   >* Les champs Environnement et Type sont fournis à titre d’information uniquement et ne modifient pas la fonctionnalité de la connexion. Ces informations s’affichent dans la zone Connexions de Fusion, ce qui vous permet de déterminer la connexion à utiliser pour un cas d’utilisation donné dans votre organisation.
   >* Certaines applications Microsoft utilisent la même connexion, qui est liée à des autorisations d’utilisateur ou d’utilisatrice. Ainsi, lors de la création d’une connexion, l’écran de consentement aux autorisations affiche les autorisations précédemment accordées à la connexion de cet utilisateur ou de cette utilisatrice, en plus des nouvelles autorisations nécessaires à l’application actuelle.
   >
   >   Par exemple, si un utilisateur ou une utilisatrice dispose d’autorisations « Lire le tableau » accordées via le connecteur Excel, puis crée une connexion dans le connecteur Outlook pour lire les e-mails, l’écran de consentement aux autorisations affiche à la fois l’autorisation « Lire le tableau » déjà accordée et l’autorisation « Écrire des e-mails » nouvellement requise.
