---
title: Modules JSONata
description: Le connecteur JSONata d’Adobe Workfront Fusion fournit un module pour traiter les données au format JSON afin qu’Adobe Workfront Fusion puisse continuer à utiliser le contenu des données.
author: Becky
feature: Workfront Fusion
exl-id: 8c117ecb-3c05-47d4-a629-18dbc546e2a2
TQID: https://experienceleague.adobe.com/luvZBccaWY5-8muR71o8C82qVROYJvcuAqt3Ol2LZac
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 329
ht-degree: 30%

---

# Modules [!UICONTROL JSONata]

Le connecteur Adobe Workfront Fusion [!UICONTROL JSONata] vous permet d’interroger des objets JSON. Ce module ne nécessite pas de connexion.

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



## Modules JSONata et leurs champs

### Evaluate

Ce module d’action interroge un objet JSON et renvoie un tableau.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expression]</td> 
   <td>Saisissez l’expression à utiliser pour évaluer l’objet JSON. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data] </td> 
   <td> Saisissez l’objet JSON à évaluer.  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sortie Stringify] </td> 
   <td> Activez cette option pour convertir la sortie en chaîne.  </td> 
  </tr> 
  </tbody>
  </table>

>[!BEGINSHADEBOX]

**Exemple** :

L’objectif est de renvoyer un tableau de noms à partir de l’objet JSON suivant :

```JSON
{
  "people": [
    { "name": "Alice", "age": 30 },
    { "name": "Bob", "age": 25 },
    { "name": "Charlie", "age": 35 }
  ]
}
```

1. Dans le champ d’expression, saisissez `people.name`.
1. Dans le champ de données, saisissez l’objet JSON.

Le module renvoie un tableau de noms extraits de l’objet JSON.

>[!ENDSHADEBOX]



### MCP JSONata

Ce module d’action génère des expressions JSONata en analysant les schémas d’entrée et de sortie spécifiés. Vous fournissez les schémas que le protocole MCP (Model Context Protocol) utilise pour générer l’expression qui transforme l’entrée en sortie.




<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Sélectionnez la connexion que vous utilisez pour vous connecter au grand modèle de langue (LLM) que vous souhaitez utiliser pour ce module.</p> <p>Actuellement, seule la clé API Anthropic est prise en charge.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input schema]</td> 
   <td> <p>Saisissez ou mappez le schéma d’entrée à utiliser pour cette expression.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Schéma de sortie]</td> 
   <td> <p>Saisissez ou mappez le schéma de sortie à utiliser pour cette expression.</p> </td> 
  </tr> 
 </tbody> 
</table>
