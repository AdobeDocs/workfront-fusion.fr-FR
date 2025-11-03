---
title: Modules MIME
description: Vous pouvez utiliser les types MIME dans Adobe Workfront Fusion. Les types MIME (Multipurpose Internet Mail Extension) sont des libellés qui permettent aux logiciels d’identifier les différents types des données partagées sur Internet. Les serveurs web et les navigateurs utilisent le type MIME pour déterminer ce qu’il convient de faire avec un fichier. Par exemple, un fichier de type MIME texte/HTML sera traité dans un navigateur différemment d’un fichier de type MIME image/JPEG. Les types MIME fonctionnent indépendamment du système d’exploitation et du matériel.
author: Becky
feature: Workfront Fusion
exl-id: 9259356b-5b42-4b6d-9854-fce9718d14e3
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 74%

---

# Modules [!UICONTROL MIME]

Vous pouvez utiliser les types MIME dans Adobe Workfront Fusion. Les types MIME (Multipurpose Internet Mail Extension) sont des libellés qui permettent aux logiciels d’identifier les différents types des données partagées sur Internet. Les serveurs web et les navigateurs utilisent le type MIME pour déterminer ce qu’il convient de faire avec un fichier. Par exemple, un fichier de type MIME `text/html` sera traité dans un navigateur différemment d’un fichier de type MIME `image/jpeg`. Les types MIME fonctionnent indépendamment du système d’exploitation et du matériel.

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

+++



## Modules [!UICONTROL MIME] et leurs champs

* [Obtenir une extension de fichier](#get-a-file-extension)
* [Obtenir un type MIME](#get-a-mime-type)

### [!UICONTROL Obtenir une extension de fichier]

Ce module du transformateur renvoie l’extension de fichier d’origine pour un type MIME donné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL MIME type]</td> 
   <td> <p>Saisissez ou mappez le type MIME pour lequel vous souhaitez déterminer l’extension de fichier. </p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Obtenir un type MIME]

Ce module de transformation renvoie le type MIME associé à un nom de fichier, un chemin d’accès ou une extension donnés.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL File]</td> 
   <td> <p>Saisissez ou mappez le fichier pour lequel vous souhaitez déterminer le type MIME. </p> <p>Vous pouvez saisir le fichier à l’aide des éléments suivants :</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File path]</strong> </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Exemple : </b></span></span>/file/image.jpeg</p> </li> 
     <li><strong>[!UICONTROL File name]</strong>  <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Exemple : </b></span></span>image.jpeg</p> </li> 
     <li><strong>[!UICONTROL File extension]</strong>  <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Exemple : </b></span></span>jpeg</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
