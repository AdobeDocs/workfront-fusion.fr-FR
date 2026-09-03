---
title: Modules Workfront Fusion
description: Avec le connecteur Workfront Fusion, vous pouvez gérer votre propre organisation Fusion à partir d’un scénario, y compris les enregistrements, les hooks, les scénarios et les connexions.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 05cd734c1bc65f58d60c2668f91e065342290341
workflow-type: tm+mt
source-wordcount: 1374
ht-degree: 25%

---

# Modules Workfront Fusion

Avec le connecteur Workfront Fusion, vous pouvez gérer votre propre organisation Fusion à partir d’un scénario. Contrairement aux autres connecteurs qui connectent Fusion à une application ou à un service tiers, ce connecteur permet à un scénario d’appeler la propre API de Fusion, comme le fait le connecteur Adobe Workfront pour permettre à un scénario de gérer Workfront.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

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

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation Workfront](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Connexion de Workfront Fusion à Workfront Fusion

1. Dans n’importe quel module Workfront Fusion, cliquez sur **[!UICONTROL Ajouter]** en regard du champ Connexion .
1. Remplissez les champs suivants :

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection type]</td> 
      <td>Sélectionnez le type de connexion que vous souhaitez créer.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection name]</td> 
      <td>Saisissez un nom pour la connexion.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client ID]</td> 
      <td>Saisissez votre [!UICONTROL Client ID] [!DNL Adobe]. Vous pouvez le consulter dans la section des détails [!UICONTROL Credentials] de la [!DNL Adobe Developer Console].</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client Secret]</td> 
      <td>Saisissez votre [!UICONTROL Client Secret] [!DNL Adobe]. Vous pouvez le consulter dans la section des détails [!UICONTROL Credentials] de la [!DNL Adobe Developer Console].</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Organization ID]</td> 
      <td>Saisissez votre identifiant de l’organisation IMS [!DNL Adobe].</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Region]</td> 
      <td>Sélectionnez la région Fusion pour cette connexion.</td> 
     </tr> 
    </tbody> 
   </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour enregistrer la connexion et revenir au module.

## Modules Workfront Fusion et leurs champs

Lorsque vous configurez les modules Workfront Fusion, Workfront Fusion affiche les champs répertoriés ci-dessous. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, consultez [Mappage d’informations d’un module à l’autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Bouton (bascule) de mappage](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Actions](#actions)
* [Exporter](#export)
* [Divers](#misc)

### Actions

* [Cloner un enregistrement](#clone-a-record)
* [Créer un enregistrement](#create-a-record)
* [Supprimer un enregistrement](#delete-a-record)
* [Répertorier les enregistrements](#list-records)
* [Lire un enregistrement](#read-a-record)
* [Mettre à jour un enregistrement](#update-a-record)

#### Cloner un enregistrement

Ce module effectue une copie de l’enregistrement spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de Workfront Fusion à Workfront Fusion, voir <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connexion de Workfront Fusion à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type d'enregistrement</td> 
   <td> Sélectionnez le type d’enregistrement à cloner. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Identifiant du scénario</td> 
   <td> Saisissez ou mappez l’identifiant du scénario que vous souhaitez cloner. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom</td> 
   <td> Saisissez ou mappez un nom pour le nouveau scénario.</td> 
  </tr> 
 </tbody> 
</table>

#### Créer un enregistrement

Ce module crée un enregistrement avec les données spécifiées.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de Workfront Fusion à Workfront Fusion, voir <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connexion de Workfront Fusion à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type d'enregistrement</td> 
   <td> Sélectionnez le type d’enregistrement que vous souhaitez créer. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID d’équipe</td> 
   <td> Saisissez ou mappez l'ID de l'équipe qui possédera cet enregistrement. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom</td> 
   <td> Saisissez ou mappez un nom pour le nouvel enregistrement.</td> 
  </tr> 
 </tbody> 
</table>

#### Supprimer un enregistrement

Ce module supprime un enregistrement spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de Workfront Fusion à Workfront Fusion, voir <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connexion de Workfront Fusion à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type d'enregistrement</td> 
   <td> Sélectionnez le type d’enregistrement que vous souhaitez supprimer. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Autres champs</td> 
   <td>Saisissez des valeurs pour tout autre champ. Les champs disponibles dépendent du type d’enregistrement sélectionné. </td> 
  </tr> 
 </tbody> 
</table>

#### Répertorier les enregistrements

Ce module renvoie une liste paginée d’enregistrements à l’aide d’une pagination basée sur le curseur et de filtres de propriété.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de Workfront Fusion à Workfront Fusion, voir <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connexion de Workfront Fusion à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type d'enregistrement</td> 
   <td>Sélectionnez le type d’enregistrement dont vous souhaitez renvoyer une liste.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Propriété</td> 
   <td>Pour chaque filtre de propriété pour lequel vous souhaitez renvoyer des résultats, cliquez sur <b>Ajouter un élément</b> et saisissez le champ, l’opérateur et la valeur pour lesquels vous souhaitez appliquer un filtre.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Démarrer</td> 
   <td>Saisissez l’emplacement où vous souhaitez commencer les résultats renvoyés. Il est utilisé pour la pagination.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nombre maximal de résultats renvoyés</td> 
   <td>Saisissez ou mappez le nombre maximal d'enregistrements que le module doit renvoyer pour chaque cycle d'exécution.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Classer par</td> 
   <td>Sélectionnez le champ selon lequel vous souhaitez classer les résultats.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Direction</td> 
   <td>Choisissez si vous souhaitez classer les résultats par ordre croissant ou décroissant.</td> 
  </tr> 
 </tbody> 
</table>

#### Lire un enregistrement

Ce module récupère l’enregistrement spécifié

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de Workfront Fusion à Workfront Fusion, voir <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connexion de Workfront Fusion à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type d'enregistrement</td> 
   <td> Sélectionnez le type d’enregistrement que vous souhaitez supprimer. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Autres champs</td> 
   <td>Saisissez des valeurs pour tout autre champ. Les champs disponibles dépendent du type d’enregistrement sélectionné. </td> 
  </tr> 
 </tbody> 
</table>

#### Mettre à jour un enregistrement

Met à jour un enregistrement spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de Workfront Fusion à Workfront Fusion, voir <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connexion de Workfront Fusion à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type d'enregistrement</td> 
   <td> Sélectionnez le type d’enregistrement à mettre à jour. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom</td> 
   <td> Saisissez ou mappez un nouveau nom pour l’enregistrement.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID</td> 
   <td> Saisissez ou mappez l’ID de l’enregistrement que vous souhaitez mettre à jour. </td> 
  </tr> 
 </tbody> 
</table>

### Exporter

#### Exporter les journaux d’activité

Ce module exporte les journaux d’activité.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de Workfront Fusion à Workfront Fusion, voir <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connexion de Workfront Fusion à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type de fichier</td> 
   <td>Sélectionnez le format de fichier dans lequel vous souhaitez exporter les journaux.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Propriété</td> 
   <td>Pour chaque filtre de propriété pour lequel vous souhaitez renvoyer des résultats, cliquez sur <b>Ajouter un élément</b> et saisissez le champ, l’opérateur et la valeur pour lesquels vous souhaitez appliquer un filtre. Vous pouvez également filtrer selon que le champ existe ou non.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Démarrer</td> 
   <td>Saisissez l’emplacement où vous souhaitez commencer les résultats renvoyés. Il est utilisé pour la pagination.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nombre maximal de résultats renvoyés</td> 
   <td>Saisissez ou mappez le nombre maximal d'enregistrements que le module doit renvoyer pour chaque cycle d'exécution.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Classer par</td> 
   <td>Sélectionnez le champ selon lequel vous souhaitez classer les résultats.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Direction</td> 
   <td>Choisissez si vous souhaitez classer les résultats par ordre croissant ou décroissant.</td> 
  </tr> 
 </tbody> 
</table>

### Divers

* [Obtention des statistiques de file d’attente pour un hook](#get-queue-statistics-for-a-hook)
* [Obtenir les dépendances d’enregistrement](#get-record-dependencies)
* [Liste des scénarios pour une connexion](#list-scenarios-for-a-connection)
* [Liste des régions et organisations Fusion](#list-the-fusion-regions-and-organizations)

#### Obtention des statistiques de file d’attente pour un hook

Ce module renvoie des statistiques de file d’attente pour le hook spécifié : le nombre d’événements actuellement mis en file d’attente, la limite de la file d’attente et si le hook est activé.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de Workfront Fusion à Workfront Fusion, voir <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connexion de Workfront Fusion à Workfront Fusion</a> dans cet article.</p> </td> 
  <tr> 
   <td role="rowheader">ID de crochet</td> 
   <td> Saisissez ou mappez l’identifiant du hook pour lequel vous souhaitez renvoyer des détails.</td> 
  </tr> 
 </tbody> 
</table>

#### Obtenir les dépendances d’enregistrement

Ce module récupère les dépendances de l’enregistrement.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de Workfront Fusion à Workfront Fusion, voir <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connexion de Workfront Fusion à Workfront Fusion</a> dans cet article.</p> </td> 
  <tr> 
   <td role="rowheader">Type d'enregistrement</td> 
   <td> Sélectionnez le type d’enregistrement pour lequel vous souhaitez récupérer les dépendances. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Identifiant du scénario</td> 
   <td> Saisissez ou mappez l’identifiant de l’enregistrement pour lequel vous souhaitez récupérer les dépendances. </td> 
  </tr> 
  </tr> 
 </tbody> 
</table>

#### Liste des scénarios pour une connexion

Ce module renvoie une liste paginée de scénarios qui font référence à la connexion donnée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de Workfront Fusion à Workfront Fusion, voir <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connexion de Workfront Fusion à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de connexion</td> 
   <td>Saisissez ou mappez l’identifiant de la connexion pour laquelle vous souhaitez renvoyer des scénarios.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Propriété</td> 
   <td>Pour chaque filtre de propriété pour lequel vous souhaitez renvoyer des résultats, cliquez sur <b>Ajouter un élément</b> et saisissez le champ, l’opérateur et la valeur pour lesquels vous souhaitez appliquer un filtre. Vous pouvez également filtrer selon que le champ existe ou non.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Démarrer</td> 
   <td>Saisissez l’emplacement où vous souhaitez commencer les résultats renvoyés. Il est utilisé pour la pagination.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nombre maximal de résultats renvoyés</td> 
   <td>Saisissez ou mappez le nombre maximal d'enregistrements que le module doit renvoyer pour chaque cycle d'exécution.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Classer par</td> 
   <td>Sélectionnez le champ selon lequel vous souhaitez classer les résultats.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Direction</td> 
   <td>Choisissez si vous souhaitez classer les résultats par ordre croissant ou décroissant.</td> 
  </tr> 
 </tbody> 
</table>

#### Liste des régions et organisations Fusion

Ce module renvoie l’ID de région et d’organisation de chaque organisation Fusion à laquelle la connexion peut accéder, en fonction des informations d’identification et d’accès figurant dans le profil utilisateur IMS des informations d’identification utilisées dans la connexion.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de Workfront Fusion à Workfront Fusion, voir <a href="#connect-workfront-fusion-to-workfront-fusion" class="MCXref xref">Connexion de Workfront Fusion à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
 </tbody> 
</table>



