---
title: Modules JSONata
description: Le connecteur JSONata d’Adobe Workfront Fusion fournit un module pour traiter les données au format JSON afin qu’Adobe Workfront Fusion puisse continuer à utiliser le contenu des données.
author: Becky
feature: Workfront Fusion
exl-id: 8c117ecb-3c05-47d4-a629-18dbc546e2a2
source-git-commit: da3bf98f8254228598372fed8c06d6318718721f
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 20%

---

# Modules [!UICONTROL JSONata]

Le connecteur [!DNL Adobe Workfront Fusion] [!UICONTROL JSONata] vous permet d’interroger des objets JSON. Ce module ne nécessite pas de connexion.

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
   <td> <p>Nouvelle : [!UICONTROL Standard]</p><p>Ou</p><p>Actuelle : [!UICONTROL Work] ou niveau supérieur</p> </td> 
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
   <p>Nouveau :</p> <ul><li>Plan de [!DNL Workfront] [!UICONTROL Select] ou [!UICONTROL Prime] : votre entreprise doit acheter des [!DNL Adobe Workfront Fusion].</li><li>Plan de [!DNL Workfront] [!UICONTROL Ultimate] : [!DNL Workfront Fusion] est inclus.</li></ul>
   <p>Ou</p>
   <p>Actuel : votre entreprise doit acheter [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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

**Exemple** :

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
