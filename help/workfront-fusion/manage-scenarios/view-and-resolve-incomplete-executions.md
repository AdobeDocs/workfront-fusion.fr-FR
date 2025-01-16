---
title: Afficher et résoudre les exécutions incomplètes
description: Le dossier [!UICONTROL Incomplete executions] stocke les exécutions de scénario qui n’ont pas été finalisées avec succès en raison d’une erreur. Chaque exécution incomplète stockée peut être résolue manuellement ou automatiquement.
author: Becky
feature: Workfront Fusion
exl-id: 8891b4d7-a39a-4f14-8521-8c2ca186ca6e
source-git-commit: 3d06958b6f706f4f974230853fb6553232656fd3
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 60%

---

# Afficher et résoudre les exécutions incomplètes

Le dossier [!UICONTROL Incomplete executions] stocke les exécutions de scénario qui n’ont pas été finalisées avec succès en raison d’une erreur. Chaque exécution incomplète stockée peut être résolue manuellement ou automatiquement.

>[!NOTE]
>
>Par défaut, le stockage des exécutions incomplètes est désactivé. Pour l’activer, activez l’option [!UICONTROL Allow storing incomplete executions] dans les paramètres avancés du scénario.
>
>Pour plus d’informations sur les paramètres de scénario, voir [Configurer les paramètres de scénario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md).

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] paquet</td> 
   <td> <p>Tous</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licence</td> 
   <td> <p>Nouveau : [!UICONTROL Standard]</p><p>Ou</p><p>En cours : [!UICONTROL Work] ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licence**</td> 
   <td>
   <p>Actuelle : aucune exigence de licence [!DNL Workfront Fusion] requise.</p>
   <p>Ou</p>
   <p>Héritée : n’importe laquelle. </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Nouveau :</p> <ul><li>[!UICONTROL Select] ou [!UICONTROL Prime] plan de [!DNL Workfront] : votre entreprise doit acheter des [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] plan : [!DNL Workfront Fusion] est inclus.</li></ul>
   <p>Ou</p>
   <p>Actuel : votre entreprise doit acheter [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurations du niveau d’accès*</td> 
   <td> 
     <p>Vous devez être un administrateur ou une administratrice [!DNL Workfront Fusion] de votre organisation.</p>
     <p>Vous devez être un administrateur ou une administratrice [!DNL Workfront Fusion] de votre équipe.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Afficher les exécutions incomplètes

Si un module rencontre une erreur lors de son fonctionnement, une nouvelle exécution incomplète est ajoutée au dossier Exécutions incomplètes. Chaque exécution incomplète contient le plan directeur du scénario et tous les lots pouvant être mappés dans le module qui a échoué. La liste des exécutions incomplètes peut être ouverte en cliquant sur l’onglet [!UICONTROL Incomplete Executions] sur la page des détails du scénario.

<!--

![](assets/incomplete-executions-tab-350x102.png)

-->

Pour plus d’informations, voir [Erreurs entraînant des exécutions incomplètes](#errors-resulting-into-incomplete-executions) dans cet article.

>[!NOTE]
>
>La taille limite actuelle du dossier d’exécutions incomplètes non résolues par organisation est de 500 Mo. Si votre entreprise dépasse cette limite, l’erreur suivante peut s’afficher :
>
>`"There is NOT ENOUGH SPACE to add a bundle to the IEQ. The reason is: Too many incomplete executions."`
>
>Pour plus d’informations, voir [Activer la perte de données](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#enable-data-loss) dans l’article Configuration des paramètres de scénario.


## Résolvez les exécutions incomplètes à partir de l’onglet Exécutions incomplètes

Lorsqu’une nouvelle exécution incomplète est stockée, vous pouvez la résoudre comme suit :

1. Ouvrez le scénario concerné.
1. Cliquez sur l’onglet **[!UICONTROL Incomplete Executions]** .
1. Recherchez l’exécution incomplète que vous souhaitez résoudre, puis cliquez sur **[!UICONTROL Details]**.


## Résoudre les exécutions incomplètes à partir de l’onglet Historique

Si vous souhaitez consulter le journal de toutes les opérations du module avant de tenter de résoudre l’exécution incomplète, vous pouvez résoudre le problème d’exécution incomplète à partir du dossier [!UICONTROL History] :

1. Ouvrez le scénario concerné.
1. Cliquez sur l’onglet **[!UICONTROL History]** .
1. Recherchez l’échec d’exécution du scénario, puis cliquez sur **[!UICONTROL Details]**.
1. Ouvrez le journal du module, où toutes les opérations du module sont affichées.
1. Recherchez l’opération ayant échoué et cliquez sur **[!UICONTROL Resolve]** :

   ![](assets/resolve-btn-350x188.png)

## Options relatives aux exécutions incomplètes

Les options suivantes du panneau [!UICONTROL Scenario settings] déterminent si et comment les exécutions incomplètes sont stockées :

* Autoriser le stockage d’exécutions incomplètes
* Traitement séquentiel
* Activer la perte de données

Pour plus d’informations sur ces options, voir [Configurer les paramètres de scénario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md).

## Erreurs entraînant des exécutions incomplètes

Il existe plusieurs catégories d’erreurs qui entraînent le stockage d’exécutions incomplètes. Ces erreurs peuvent inclure les suivantes :

* Des erreurs de validation dues à des données incomplètes ou erronées. Le plus souvent, cela est dû à un élément manquant qui est nécessaire pour traiter avec succès toutes les données passant par un module.
* Des erreurs dues à l’indisponibilité de la destination finale en raison d’un échec temporaire ou à long terme de la connexion (par exemple, lors de la connexion à un serveur de messagerie ou FTP distant).

Si une erreur se produit sur le premier module du scénario, l’exécution s’arrête immédiatement et aucune exécution incomplète n’est stockée.

Si une erreur se produit sur un autre module et qu’aucun itinéraire de gestionnaire d’erreur n’est associé, alors l’un des événements suivants se produit :

* Si le type d’erreur est `ConnectionError`, `RateLimitError`, `OutOfSpaceError` ou `ModuleTimeoutError`, un enregistrement d’exécution incomplète avec reprise automatique est stocké.
* Si le type d’erreur est `DataError`, `InvalidConfigurationError`, `InvalidAccessTokenError`, `UnexpectedError`, `MaxFileSizeExceededError`, ou `MaxResultsExceededError`, un enregistrement d’exécution incomplète sans reprise automatique est stocké.
* Si le type d’erreur est autre que ci-dessus, l’exécution échoue.
