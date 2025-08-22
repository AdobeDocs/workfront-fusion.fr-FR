---
title: Modules Qualtrics
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent Qualtrics et les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: 80b441b7-c808-4c4f-b9ff-d614650dbb73
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 48%

---

# Modules Qualtrics

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent [!DNL Qualtrics] et les connecter à plusieurs applications et services tiers.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

## Conditions d’accès

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Formule Adobe Workfront*</td>
  <td> <p>[!UICONTROL Pro] ou version supérieure</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licence Adobe Workfront*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licence Adobe Workfront Fusion **</td> 
   <td>
   <p>Exigence de licence actuelle : aucune exigence de licence Workfront Fusion.</p>
   <p>Ou</p>
   <p>Exigence de licence héritée : [!UICONTROL Workfront Fusion for Work Automation and Integration] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Configuration requise actuelle du produit : si vous disposez du plan Adobe Workfront [!UICONTROL Select] ou [!UICONTROL Prime], votre entreprise doit acheter Adobe Workfront Fusion ainsi qu’Adobe Workfront pour utiliser les fonctionnalités décrites dans cet article. Workfront Fusion est inclus dans le plan Workfront [!UICONTROL Ultimate].</p>
   <p>Ou</p>
   <p>Exigences de produit héritées : votre entreprise doit acheter Adobe Workfront Fusion ainsi qu’Adobe Workfront pour utiliser les fonctionnalités décrites dans cet article.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Pour connaître le plan, le type de licence ou l’accès dont vous disposez, contactez votre administrateur ou administratrice Workfront.

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Conditions préalables

Pour utiliser les modules [!DNL Qualtrics], vous devez disposer d’un compte [!UICONTROL Qualtrics].

## Informations sur l’API Qualtrics

Le connecteur Qualtrics utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td> https://{{connection.dataCenterCode}}.qualtrics.com/API/v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Version de l’API</td> 
   <td> v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.1.1</td> 
  </tr>
 </tbody> 
 </table>

## Connexion de [!DNL Qualtrics] à Workfront Fusion

Vous pouvez créer une connexion à votre compte [!DNL Qualtrics] directement depuis un module [!UICONTROL Qualtrics].

1. Dans n’importe quel module [!UICONTROL Qualtrics], cliquez sur **[!UICONTROL Ajouter]** en regard du champ [!UICONTROL Connexion].
1. Saisissez les informations suivantes :

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td> <p>Saisissez un nom pour la nouvelle connexion.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Data Center ID]</td> 
      <td>Utilisez le format <code>&lt;Data Center ID>.qualtrics.com</code>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API Key]</td> 
      <td>Pour localiser votre clé d’API, voir la documentation [!DNL Qualtrics].</td> 
     </tr> 
    </tbody> 
   </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour créer la connexion et revenez au module.

## Modules [!DNL Qualtrics] et leurs champs

Les modules suivants sont disponibles pour le connecteur [!DNL Qualtrics] :

* [!UICONTROL Surveiller la réponse à une nouvelle enquête]
* [!UICONTROL Créer un contact de répertoire]
* [!UICONTROL Supprimer un contact de répertoire]
* [!UICONTROL Obtenir un contact de répertoire]
* [!UICONTROL Mettre à jour un contact de répertoire]
* [!UICONTROL Créer la diffusion d’une nouvelle enquête par SMS]
* [!UICONTROL Diffuser une enquête par e-mail]
* [!UICONTROL Effectuer un appel API]
* [!UICONTROL Répertorier les contacts de répertoire]
