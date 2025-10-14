---
title: Modules Microsoft SQL Server
description: Vous pouvez utiliser Adobe Workfront Fusion pour vous connecter à Microsoft SQL Server.
author: Becky
feature: Workfront Fusion
exl-id: 8f3293f7-8b45-4e42-8ad8-f9d4969b63fd
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 68%

---

# Modules [!DNL Microsoft SQL Server]

Vous pouvez utiliser Adobe Workfront Fusion pour vous connecter à [!UICONTROL Microsoft SQL Server].

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
   <td> <p>Nouveau : Standard</p><p>Ou</p><p>En cours : Travail ou version ultérieure</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licence Adobe Workfront Fusion **</td> 
   <td>
   <p>Actuel : aucune exigence de licence Workfront Fusion</p>
   <p>Ou</p>
   <p>Hérité : Workfront Fusion pour l’automatisation et l’intégration du travail </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Nouveau :</p> <ul><li>Sélectionnez ou le package Prime Workfront : votre entreprise doit acheter Adobe Workfront Fusion.</li><li>Package Ultimate Workfront : Workfront Fusion est inclus.</li></ul>
   <p>Ou</p>
   <p>Actuel : votre entreprise doit acheter Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Connexion du service [!DNL Microsoft SQL Server] à Workfront Fusion

Pour obtenir des instructions sur la connexion de votre compte [!DNL Microsoft SQL Server] à [!UICONTROL Workfront Fusion], voir [Créer une connexion à [!UICONTROL Adobe Workfront Fusion] : instructions de base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Certaines applications Microsoft utilisent la même connexion, qui est liée à des autorisations d’utilisateur ou d’utilisatrice. Ainsi, lors de la création d’une connexion, l’écran de consentement aux autorisations affiche les autorisations précédemment accordées à la connexion de cet utilisateur ou de cette utilisatrice, en plus des nouvelles autorisations nécessaires à l’application actuelle.
>
>Par exemple, si un utilisateur ou une utilisatrice dispose d’autorisations « Lire le tableau » accordées via le connecteur Excel, puis crée une connexion dans le connecteur Outlook pour lire les e-mails, l’écran de consentement aux autorisations affiche à la fois l’autorisation « Lire le tableau » déjà accordée et l’autorisation « Écrire des e-mails » nouvellement requise.

## Utilisation des modules [!DNL Microsoft SQL Server]

Vous pouvez exécuter votre logique personnalisée directement sur votre serveur de base de données par le biais de procédures stockées. Adobe Workfront Fusion charge dynamiquement l’interface des paramètres d’entrée/sortie et du jeu d’enregistrements afin que chaque paramètre ou valeur puisse être mappé individuellement. Avant de commencer à configurer votre scénario, assurez-vous que le compte que vous utilisez pour vous connecter à votre base de données a un accès en lecture aux vues `INFORMATION_SCHEMA.ROUTINES` et `INFORMATION_SCHEMA.PARAMETERS`.

Lorsque [!DNL Fusion] établit la connexion avec la destination [!DNL SQL server], l’utilisateur ou utilisatrice [!DNL Fusion] identifie l’hôte (le nom de domaine ou l’adresse IP où le serveur est hébergé) et le port. [!DNL Fusion] peut se connecter à n’importe quel hôte/port disponible.

Pour plus d’informations sur les adresses IP spécifiques utilisées par Workfront Fusion, voir [&#x200B; Adresses IP pour accéder à Adobe Workfront Fusion &#x200B;](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md)

Pour en savoir plus sur la création d’une procédure stockée, consultez la documentation de [!DNL Microsoft SQL Server].

>[!NOTE]
>
>Workfront Fusion ne prend pas en charge plusieurs jeux d’enregistrements. Seul le premier est traité.

## Résoudre l’erreur [!UICONTROL ER_LOCK_WAIT_TIMEOUT : le délai d’attente du verrouillage a été dépassé ; essayez de redémarrer la transaction.]

Cette erreur se produit lorsque vous modifiez les mêmes données à l’aide de plusieurs modules. Elle est causée par les transactions SQL.

Lorsqu’un module SQL est exécuté, il démarre une transaction. La transaction est terminée après l’exécution complète du scénario.

Si un autre module tente d’accéder aux mêmes données, il doit attendre que la transaction précédente soit terminée. Puisque la première transaction sera terminée après la fin du scénario, la deuxième transaction ne pourra jamais commencer.

### Solution :

Activez la validation automatique. La validation automatique termine (valide) chaque transaction immédiatement après l’exécution du module.

1. Cliquez sur l’icône [!UICONTROL Paramètres du scénario] ![Icône Paramètres du scénario](/help/workfront-fusion/references/apps-and-modules/assets/scenario-settings-icon.png) en bas de l’écran.
1. Cliquez sur la case **[!UICONTROL Validation automatique]**.
1. Cliquez sur **[!UICONTROL OK]** et enregistrez les paramètres du scénario.
