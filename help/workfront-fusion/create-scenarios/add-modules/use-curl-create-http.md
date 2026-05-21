---
title: Utiliser cURL pour ajouter un module HTTP
description: Vous pouvez coller une requête cURL dans votre scénario, puis Fusion crée un module HTTP configuré à partir de la requête cURL.
author: Becky
feature: Workfront Fusion
exl-id: 6d466809-860d-4f72-9044-ebe2df943674
TQID: https://experienceleague.adobe.com/vPAMsVLVV7C3ykPPXgbMgDTosd0M3hYKYVL-OFszXqw
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 269
ht-degree: 39%

---

# Utiliser cURL pour ajouter un module HTTP

Vous pouvez coller une requête cURL dans votre scénario, puis Fusion crée un module HTTP configuré à partir de la requête cURL.

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tout package de workflow Adobe Workfront et tout package d’automatisation et d’intégration Adobe Workfront</p><p>Workfront Ultimate</p><p>Packages Workfront Prime et Select, avec l’achat supplémentaire de Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licences Adobe Workfront</td> 
   <td> <p>Standard</p><p>Travail ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Si votre organisation dispose d’un package Workfront Select ou Prime qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acquérir Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

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
