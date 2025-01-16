---
title: Modules Microsoft SQL Server
description: Vous pouvez utiliser  [!DNL Adobe Workfront Fusion]  pour vous connecter à Microsoft SQL Server.
author: Becky
feature: Workfront Fusion
exl-id: 8f3293f7-8b45-4e42-8ad8-f9d4969b63fd
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 86%

---

# Modules [!DNL Microsoft SQL Server]

Vous pouvez utiliser [!DNL Adobe Workfront Fusion] pour vous connecter à [!UICONTROL Microsoft SQL Server].

## Conditions d’accès

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] formule*</td>
  <td> <p>[!UICONTROL Pro] ou une version ultérieure</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licence*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licence**</td> 
   <td>
   <p>Exigences de licence actuelles : aucune exigence de licence [!DNL Workfront Fusion] requise.</p>
   <p>Ou</p>
   <p>Ancienne exigence de licence : [!UICONTROL [!DNL Workfront Fusion] pour l’automatisation et l’intégration du travail] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Exigences actuelles du produit : si vous disposez du plan de [!DNL Adobe Workfront] [!UICONTROL Select] ou [!UICONTROL Prime], votre entreprise doit acheter du [!DNL Adobe Workfront Fusion] et [!DNL Adobe Workfront] utiliser les fonctionnalités décrites dans cet article. [!DNL Workfront Fusion] est inclus dans le plan de [!DNL Workfront] [!UICONTROL Ultimate].</p>
   <p>Ou</p>
   <p>Exigences liées aux produits hérités : votre entreprise doit acheter [!DNL Adobe Workfront Fusion] ainsi qu’[!DNL Adobe Workfront] pour utiliser la fonctionnalité décrite dans cet article.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Pour connaître la formule, le type de licence ou l’accès dont vous disposez, contactez votre équipe d’administration [!DNL Workfront].

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).



## Connexion du service  à . [!DNL Microsoft SQL Server][!DNL Workfront Fusion]

Pour savoir comment connecter votre compte [!DNL Microsoft SQL Server] à [!UICONTROL Workfront Fusion], voir [Créer une connexion à [!UICONTROL Adobe Workfront Fusion] - Instructions de base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Certaines applications Microsoft utilisent la même connexion, qui est liée à des autorisations d’utilisateur ou d’utilisatrice. Ainsi, lors de la création d’une connexion, l’écran de consentement aux autorisations affiche les autorisations précédemment accordées à la connexion de cet utilisateur ou de cette utilisatrice, en plus des nouvelles autorisations nécessaires à l’application actuelle.
>
>Par exemple, si un utilisateur ou une utilisatrice dispose d’autorisations « Lire le tableau » accordées via le connecteur Excel, puis crée une connexion dans le connecteur Outlook pour lire les e-mails, l’écran de consentement aux autorisations affiche à la fois l’autorisation « Lire le tableau » déjà accordée et l’autorisation « Écrire des e-mails » nouvellement requise.

## Utilisation des modules [!DNL Microsoft SQL Server]

Vous pouvez exécuter votre logique personnalisée directement sur votre serveur de base de données par le biais de procédures stockées. [!DNL Adobe Workfront Fusion] charge l’interface des paramètres d’entrée/sortie et des ensembles d’enregistrements de manière dynamique afin que chaque paramètre ou valeur puisse faire l’objet d’un mappage individuel. Avant de commencer à configurer votre scénario, assurez-vous que le compte que vous utilisez pour vous connecter à votre base de données a un accès en lecture aux vues `INFORMATION_SCHEMA.ROUTINES` et `INFORMATION_SCHEMA.PARAMETERS`.

Lorsque [!DNL Fusion] établit la connexion avec la destination [!DNL SQL server], l’utilisateur ou utilisatrice [!DNL Fusion] identifie l’hôte (le nom de domaine ou l’adresse IP où le serveur est hébergé) et le port. [!DNL Fusion] peut se connecter à n’importe quel hôte/port disponible.

Pour plus d’informations sur les adresses IP spécifiques utilisées par [!DNL Workfront Fusion], voir [Adresses IP pour accéder à  [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md)

Pour en savoir plus sur la création d’une procédure stockée, consultez la documentation de [!DNL Microsoft SQL Server].

>[!NOTE]
>
>[!DNL Workfront Fusion] ne prend pas en charge les ensembles d’enregistrements multiples. Seul le premier est traité.

## Résolution des [!UICONTROL ER_LOCK_WAIT_TIMEOUT: Lock wait timeout exceeded; try restarting transaction] d’erreur

Cette erreur se produit lorsque vous modifiez les mêmes données à l’aide de plusieurs modules. Elle est causée par les transactions SQL.

Lorsqu’un module SQL est exécuté, il démarre une transaction. La transaction est terminée après l’exécution complète du scénario.

Si un autre module tente d’accéder aux mêmes données, il doit attendre que la transaction précédente soit terminée. Puisque la première transaction sera terminée après la fin du scénario, la deuxième transaction ne pourra jamais commencer.

### Solution :

Activez la validation automatique. La validation automatique termine (valide) chaque transaction immédiatement après l’exécution du module.

1. Cliquez sur l’icône [!UICONTROL Scenario settings] ![](/help/workfront-fusion/references/apps-and-modules/assets/scenario-settings-icon.png)en bas de l’écran).
1. Cochez la case **[!UICONTROL Auto commit]** .
1. Cliquez sur **[!UICONTROL OK]** pour enregistrer les paramètres du scénario.
