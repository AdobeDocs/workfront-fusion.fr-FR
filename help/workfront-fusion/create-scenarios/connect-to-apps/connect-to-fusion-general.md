---
title: Créer une connexion - Instructions de base
description: De nombreux connecteurs  [!DNL Adobe Workfront Fusion]  ne nécessitent pas de configuration personnalisée lors de la création d’une connexion. Cet article décrit le processus de création de connexion par défaut.
author: Becky
feature: Workfront Fusion
exl-id: e47ab4d9-6612-4d9a-a024-da508a8bbfb2
source-git-commit: ef1a96d9ef4c2c82eaf376c84188e3ed6ea7b2cf
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 42%

---

# Créer une connexion - Instructions de base

De nombreux connecteurs [!DNL Adobe Workfront Fusion] ne nécessitent pas de configuration personnalisée lors de la création d’une connexion. Cet article décrit le processus de création de connexion par défaut.

>[!NOTE]
>
>
>Si Adobe Workfront Fusion ne propose pas d’application pour le service web que vous souhaitez utiliser dans votre scénario, vous pouvez vous connecter au service web à l’aide [!DNL Workfront Fusion] modules HTTP et Webhooks, comme expliqué dans les articles suivants :
>
>* [Connectez Adobe Workfront Fusion à un service web qui utilise l’autorisation de jeton API](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-wf-web-service-uses-api-token-auth.md)
>* [Configurer un webhook pour un service web sans connecteur](/help/workfront-fusion/create-scenarios/add-modules/receive-a-webhook-from-a-web-service.md)

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront 
   <td> <p>Tous</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licence Adobe Workfront</td> 
   <td> <p>Nouveau : Standard</p><p>Ou</p><p>Actuellement : Travail ou licence supérieure</p> </td> 
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
   <p>Nouveau :</p> <ul><li>Sélectionnez ou Prime Workfront Plan : votre entreprise doit acheter Adobe Workfront Fusion.</li><li>Plan Ultimate Workfront : Workfront Fusion est inclus.</li></ul>
   <p>Ou</p>
   <p>Actuel : votre entreprise doit acheter Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Créer une connexion

Pour créer une connexion dans un module [!DNL Workfront Fusion], procédez comme suit :

1. Cliquez sur **[!UICONTROL Add]** en regard de la zone de [!UICONTROL Connection] pour ouvrir le panneau **[!UICONTROL Create a connection]**.
1. (Facultatif) Modifiez le **[!UICONTROL Connection name]** par défaut.
1. Dans le champ Environnement , indiquez s’il s’agit d’un environnement de production ou d’un environnement hors production. Ces informations s’affichent dans la zone Connexions de Fusion.
1. Dans le champ Type , indiquez s’il s’agit d’un compte de service ou personnel. Ces informations s’affichent dans la zone Connexions de Fusion.
1. (Conditionnel) Si l’application nécessite des paramètres de connexion avancés, tels qu’un identifiant, une clé ou une [!UICONTROL secret], saisissez ces informations.

   Vous devrez peut-être cliquer sur **[!UICONTROL Show advanced settings]** pour afficher les champs dans lesquels vous pouvez saisir ce type d’informations.

1. Cliquez sur **[!UICONTROL Continue]**.
1. Dans la fenêtre de connexion qui s’affiche, saisissez vos informations d’identification pour vous connecter à l’application si vous ne l’avez pas déjà fait.
1. (Conditionnel) Si un bouton **[!UICONTROL Allow]** s’affiche, examinez les actions que le connecteur peut effectuer, puis cliquez sur le bouton pour connecter l’application à [!DNL Workfront Fusion].

   >[!NOTE]
   >
   >Certaines applications Microsoft utilisent la même connexion, qui est liée à des autorisations d’utilisateur ou d’utilisatrice. Ainsi, lors de la création d’une connexion, l’écran de consentement aux autorisations affiche les autorisations précédemment accordées à la connexion de cet utilisateur ou de cette utilisatrice, en plus des nouvelles autorisations nécessaires à l’application actuelle.
   >
   >Par exemple, si un utilisateur ou une utilisatrice dispose d’autorisations « Lire le tableau » accordées via le connecteur Excel, puis crée une connexion dans le connecteur Outlook pour lire les e-mails, l’écran de consentement aux autorisations affiche à la fois l’autorisation « Lire le tableau » déjà accordée et l’autorisation « Écrire des e-mails » nouvellement requise.
