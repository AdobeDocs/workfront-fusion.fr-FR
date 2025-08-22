---
title: Utiliser cURL pour ajouter un module HTTP
description: Vous pouvez coller une requête cURL dans votre scénario, puis Fusion crée un module HTTP configuré à partir de la requête cURL.
author: Becky
feature: Workfront Fusion
exl-id: 6d466809-860d-4f72-9044-ebe2df943674
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 15%

---

# Utiliser cURL pour ajouter un module HTTP

Vous pouvez coller une requête cURL dans votre scénario, puis Fusion crée un module HTTP configuré à partir de la requête cURL.

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
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Création d’un module HTTP à partir d’une requête cURL


Pour créer un module HTTP à l’aide de cURL :

1. Créez le texte de la requête cURL en dehors de Fusion, par exemple dans un éditeur de texte.
1. Copiez la requête cURL dans le presse-papiers.
1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez créer le module.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Cliquez avec le bouton droit sur un espace blanc dans l’éditeur de scénarios et sélectionnez **Coller**.

   Ou

   Appuyez sur Ctrl + V (Windows) ou Cmd + V (Mac).


   Un module HTML est créé.
1. Faites glisser le module pour le connecter à votre scénario.

## Dépannage

Si votre cURL n’est pas collée dans votre scénario, vérifiez les paramètres de votre navigateur pour vous assurer que le collage à partir du presse-papiers est activé.
