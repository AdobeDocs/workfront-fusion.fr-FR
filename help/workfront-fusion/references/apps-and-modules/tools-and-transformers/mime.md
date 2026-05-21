---
title: Modules MIME
description: Vous pouvez utiliser les types MIME dans Adobe Workfront Fusion. Les types MIME (Multipurpose Internet Mail Extension) sont des libellés qui permettent aux logiciels d’identifier les différents types des données partagées sur Internet. Les serveurs web et les navigateurs utilisent le type MIME pour déterminer ce qu’il convient de faire avec un fichier. Par exemple, un fichier de type MIME texte/HTML sera traité dans un navigateur différemment d’un fichier de type MIME image/JPEG. Les types MIME fonctionnent indépendamment du système d’exploitation et du matériel.
author: Becky
feature: Workfront Fusion
exl-id: 9259356b-5b42-4b6d-9854-fce9718d14e3
TQID: https://experienceleague.adobe.com/65lJuH7aL35rZCYDowjJuxuQAh88LHNyL3XRQVDJoOY
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 358
ht-degree: 93%

---

# Modules [!UICONTROL MIME]

Vous pouvez utiliser les types MIME dans Adobe Workfront Fusion. Les types MIME (Multipurpose Internet Mail Extension) sont des libellés qui permettent aux logiciels d’identifier les différents types des données partagées sur Internet. Les serveurs web et les navigateurs utilisent le type MIME pour déterminer ce qu’il convient de faire avec un fichier. Par exemple, un fichier dont le type MIME est `text/html` sera traité différemment dans un navigateur qu’un fichier dont le type MIME est `image/jpeg`. Les types MIME fonctionnent indépendamment du système d’exploitation et du matériel.

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
