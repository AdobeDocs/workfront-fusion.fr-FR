---
title: Modules de magasin de données
description: Un magasin de données  [!DNL Adobe Workfront Fusion] , similaire à une base de données ou à un tableau simple, peut stocker des données de scénarios, ce qui permet de transférer des données entre des scénarios individuels ou des exécutions de scénarios. Vous pouvez utiliser un magasin de données pour stocker de nouvelles données provenant de différents systèmes lors de la synchronisation.
author: Becky
feature: Workfront Fusion
exl-id: 0338b822-b345-429e-850d-3978b692231d
source-git-commit: 7404dafc0b368a8f1785be7b6a65fe45c0f12172
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 87%

---

# Modules [!UICONTROL Data store]

Un magasin de données [!DNL Adobe Workfront Fusion], similaire à une base de données ou à un tableau simple, peut stocker des données de scénarios, ce qui permet de transférer des données entre des scénarios individuels ou des exécutions de scénarios. Vous pouvez utiliser un magasin de données pour stocker de nouvelles données provenant de différents systèmes lors de la synchronisation.

Les modules de magasin de données vous permettent d’ajouter, de remplacer, de mettre à jour, de récupérer, de supprimer, de rechercher ou de comptabiliser des enregistrements dans votre magasin de données [!DNL Adobe Workfront Fusion].

<!--For information on creating, editing, and troubleshooting data stores, see [Data Stores in [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/references/mapping-panel/data-types/)-->

Pour une vidéo de présentation des entrepôts de données dans Workfront Fusion, voir :

* [Entrepôts de données](https://video.tv.adobe.com/v/3427029/){target=_blank}

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
   <p>Aucune exigence de licence Workfront Fusion.</p>
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

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Conditions préalables

Pour utiliser [!UICONTROL Data Store] modules, vous devez d’abord créer un magasin de données.

Pour plus d’informations sur la création de magasins de données, voir [Créer et gérer des magasins de données](/help/workfront-fusion/create-scenarios/map-data/data-stores.md).

## Modules [!UICONTROL Data store] et leurs champs

Lorsque vous configurez des modules de magasin de données, [!DNL Workfront Fusion] affiche les champs listés ci-dessous. En plus de ces derniers, d’autres champs du magasin de données peuvent s’afficher, en fonction de facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Il n’est pas nécessaire de créer une connexion pour utiliser les entrepôts de données.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [Ajouter/remplacer un enregistrement](#addreplace-a-record)
* [Vérifier l’existence d’un enregistrement](#check-the-existence-of-a-record)
* [Comptabiliser des enregistrements](#count-records)
* [Supprimer un enregistrement](#delete-a-record)
* [Supprimer tous les enregistrements](#delete-all-records)
* [Obtenir un enregistrement](#get-a-record)
* [Rechercher des enregistrements](#search-records)
* [Mettre à jour un enregistrement](#update-a-record)

### [!UICONTROL Add/Replace a Record]

Ce module d’action ajoute ou remplace un enregistrement.

Vous spécifiez le magasin de données et la clé de l’enregistrement.

Le module renvoie l’identifiant de l’enregistrement et de tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

>[!NOTE]
>
>Le module renvoie une erreur lorsque vous essayez d’ajouter un enregistrement qui se trouve déjà dans le magasin de données sous le même nom et que l’option [!UICONTROL Overwrite an existing record] est désactivée.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data store]</td> 
   <td> <p> Sélectionnez ou ajoutez le magasin de données dans lequel vous souhaitez créer un enregistrement. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Key] </td> 
   <td> <p>Saisissez la clé unique de l’enregistrement que le module doit ajouter ou remplacer. La clé peut être utilisée ultérieurement pour récupérer l’enregistrement. Si vous laissez ce champ vide, une clé est générée automatiquement.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Overwrite an existing record] </td> 
   <td> <p>Activez cette option pour écraser l’enregistrement. L’enregistrement que vous souhaitez écraser doit être spécifié dans le champ Clé ci-dessus.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record] </td> 
   <td> <p>Saisissez les valeurs souhaitées dans les champs de l’enregistrement.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Check the Existence of a Record]

Ce module d’action indique si un enregistrement spécifique existe.

Vous spécifiez le magasin de données et la clé de l’enregistrement.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data store] </td> 
   <td> <p>Sélectionnez le magasin de données dans lequel l’existence de l’enregistrement doit être vérifiée.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Key] </td> 
   <td> <p>Saisissez la clé unique de l’enregistrement dont le module doit vérifier l’existence.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Count Records]

Ce module d’action compte les enregistrements dans un magasin de données.

Vous spécifiez le magasin de données.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data store] </td> 
   <td> <p>Sélectionnez le magasin de données qui contient les enregistrements à comptabiliser.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Delete a Record]

Ce module d’action supprime un enregistrement.

Vous spécifiez le magasin de données et la clé de l’enregistrement.

Le module renvoie l’ID de l’enregistrement et tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data store] </td> 
   <td> <p>Sélectionnez le magasin de données dans lequel l’existence de l’enregistrement doit être vérifiée.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Key] </td> 
   <td> <p>Saisissez la clé unique de l’enregistrement que le module doit supprimer.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Delete All Records]

Ce module d’action supprime tous les enregistrements d’un magasin de données spécifique.

Vous spécifiez le magasin de données.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data store] </td> 
   <td> <p>Sélectionnez le magasin de données dans lequel vous souhaitez supprimer tous les enregistrements.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Get a Record]

Ce module d’action récupère un enregistrement.

Vous spécifiez le magasin de données et la clé de l’enregistrement.

Le module renvoie l’identifiant de l’enregistrement et de tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data store]</td> 
   <td> <p> Sélectionnez le magasin de données à partir duquel vous souhaitez récupérer un enregistrement.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Key] </td> 
   <td> <p>Saisissez la clé unique de l’enregistrement que le module doit récupérer.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Search Records]

Ce module de recherche recherche des enregistrements d’un objet dans un magasin de données qui correspondent à la requête de recherche que vous avez spécifiée.

Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data store]</td> 
   <td> <p> Sélectionnez le magasin de données dans lequel vous souhaitez effectuer une recherche.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Filter]</p> </td> 
   <td> <p>Définissez le filtre pour la recherche.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Sort]</p> </td> 
   <td> <p style="font-weight: normal;">Pour chaque champ en fonction duquel vous souhaitez effectuer un tri, renseignez les champs suivants :</p> <p style="font-weight: bold;">[!UICONTROL Key]</p> <p>Sélectionnez le nom de la colonne en fonction de laquelle vous souhaitez trier les résultats.</p> <p style="font-weight: bold;">[!UICONTROL Order]</p> <p>Indiquez si vous souhaitez trier les résultats par ordre croissant ou décroissant.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p> Définissez le nombre maximal de résultats de recherche que [!DNL Workfront Fusion] renvoie pour un seul cycle d’exécution.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Continue the execution of the route even if the module returns no results]</td> 
   <td> <p> Si cette option est activée, l’itinéraire dont fait partie ce module continue le traitement même si ce module ne renvoie aucun résultat.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Update a Record]

Ce module d’action met à jour un enregistrement.

Vous spécifiez le magasin de données et la clé de l’enregistrement.

Le module renvoie l’ID de l’enregistrement et tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data store]</td> 
   <td> <p> Sélectionnez ou ajoutez le magasin de données dans lequel vous souhaitez créer un enregistrement. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Key] </td> 
   <td> <p>Saisissez la clé unique de l’enregistrement que le module doit mettre à jour.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Insert missing record] </td> 
   <td> <p>Activez cette option pour créer un enregistrement si l’enregistrement avec la clé spécifiée n’existe pas déjà.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record]</td> 
   <td> <p> Saisissez les valeurs souhaitées dans les champs de l’enregistrement que vous souhaitez mettre à jour.</p> </td> 
  </tr> 
 </tbody> 
</table>
