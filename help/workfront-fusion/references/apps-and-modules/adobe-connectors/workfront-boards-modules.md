---
title: Modules des tableaux Adobe Workfront
description: Vous pouvez utiliser le connecteur de tableaux Adobe Workfront pour automatiser vos processus dans les tableaux Workfront et le connecter à des applications et services tiers.
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: dcc5044d-8fdf-4a74-b664-e965e714ce92
source-git-commit: 899fc717f5107433d6f1aea31c4d079243a85822
workflow-type: tm+mt
source-wordcount: '2868'
ht-degree: 17%

---

# Modules des tableaux [!DNL Adobe Workfront]

>[!NOTE]
>
>Le connecteur Boards Fusion est en version bêta. Par conséquent, la prise en charge de ce connecteur est limitée et peut changer en raison du développement futur des tableaux. En outre, des modifications apportées sans préavis à l’API GraphQL peuvent avoir une incidence sur votre processus Fusion Connector.

Les panoramas Adobe Workfront sont des outils flexibles qui permettent aux équipes de collaborer entre elles. Ils permettent d’accéder à un panorama partagé contenant des colonnes et des cartes.

Vous pouvez utiliser les modules des tableaux Adobe Workfront pour lire ou mettre à jour des enregistrements, effectuer un appel API vers l’API des tableaux Workfront ou déclencher un scénario lorsqu’une action se produit sur un tableau.

<!--For general information on Workfront Boards, see [Boards overview](/help/quicksilver/agile/boards-overview.md).-->

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
   <p>Actuel : aucune exigence de licence Workfront Fusion</p>
   <p>Ou</p>
   <p>Hérité : Workfront Fusion pour l’automatisation et l’intégration du travail </p>
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

Vous devez avoir configuré un panorama dans Adobe Workfront avant de pouvoir vous y connecter.

## Informations sur l’API des tableaux Adobe Workfront

Le connecteur Adobe Workfront Boards utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.23.6</td> 
  </tr>
 </tbody> 
 </table>

## Création d’une connexion aux tableaux Workfront

>[!NOTE]
>
>Vous pouvez utiliser une connexion Workfront pour vous connecter aux tableaux Workfront ou créer une connexion aux tableaux Workfront distincte.

Pour créer une connexion aux tableaux Workfront :

1. Dans un module [!DNL Adobe Workfront Boards], cliquez sur **[!UICONTROL Ajouter]** en regard de la zone Connexion.

1. Remplissez les champs suivants :

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Connection name]</td>
          <td>
            <p>Saisissez un nom pour cette connexion.</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Environment]</td>
          <td>Indiquez si vous vous connectez à un environnement de production ou hors production.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Type]</td>
          <td>Choisissez si vous souhaitez vous connecter à un compte de service ou à un compte personnel.</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client ID]<p>(Facultatif)</p></td>
          <td>Saisissez votre [!UICONTROL Client ID] [!DNL Adobe]. Vous pouvez le trouver dans la section [!UICONTROL Credentials details] d’[!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]<p>(Facultatif)</p></td>
          <td>Saisissez votre [!UICONTROL Client Secret] [!DNL Adobe]. Vous pouvez le trouver dans la section [!UICONTROL Credentials details] d’[!DNL Adobe Developer Console].
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Authentication URL]<p>(Facultatif)</p></td>
          <td>Saisissez l’URL que votre instance de Workfront utilisera pour authentifier cette connexion. <p>La valeur par défaut est <code>https://oauth.my.workfront.com/integrations/oauth2</code>.</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Host prefix]</td>
          <td>Saisissez votre préfixe hôte.<p>La valeur par défaut est <code>origin-</code>.</p>
        </tr>
      </tbody>
    </table>
1. Cliquez sur **[!UICONTROL Continuer]** pour enregistrer la connexion et revenir au module.

## Modules des tableaux Adobe Workfront et leurs champs

Lorsque vous configurez les modules des tableaux Workfront, [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. D’autres champs de tableaux Workfront peuvent également s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [vignette](#cards)
* [Panneaux](#boards)
* [Colonnes](#columns)
* [Balises](#tags)
* [Commentaires](#comments)
* [Autre](#other)

### vignette

* [Ajouter un élément de la liste de contrôle](#add-checklist-item)
* [Ajouter une sous-tâche](#add-subtask)
* [Création d’une carte](#create-a-card)
* [Déplacer une carte](#move-a-card)
* [Lire une carte](#read-a-card)
* [Mise à jour d’une carte](#update-a-card)

#### Ajouter un élément de la liste de contrôle

Ce module d’action ajoute un élément de liste de contrôle à la vignette spécifiée.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>Vous pouvez utiliser une connexion Workfront existante pour vous connecter aux tableaux Workfront ou une connexion aux tableaux Workfront spécifique. </p><p>Pour plus d’informations sur la connexion de votre application [!DNL Workfront] aux [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Création d’une connexion aux tableaux Workfront</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Saisissez ou mappez l’identifiant de la carte à laquelle vous souhaitez ajouter un élément de liste de contrôle.<p>L’ID de la carte se trouve dans l’URL lors de l’affichage de la carte dans Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Checklist items]</td> 
   <td>Pour chaque élément de la liste de contrôle que vous souhaitez ajouter, cliquez sur Ajouter un élément, saisissez le nom de l’élément de la liste de contrôle et indiquez si l’élément est terminé.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Ajouter une sous-tâche

Ce module d’action ajoute une sous-tâche à une carte dans les tableaux. La carte doit être connectée. La sous-tâche est également ajoutée à la tâche Workfront que la carte représente.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>Vous pouvez utiliser une connexion Workfront existante pour vous connecter aux tableaux Workfront ou une connexion aux tableaux Workfront spécifique. </p><p>Pour plus d’informations sur la connexion de votre application [!DNL Workfront] aux [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Création d’une connexion aux tableaux Workfront</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID de carte parent]</td> 
   <td>Saisissez ou mappez l’identifiant de la carte à laquelle vous souhaitez ajouter une sous-tâche.<p>L’ID de la carte se trouve dans l’URL lors de l’affichage de la carte dans Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Saisissez ou mappez l’ID du panorama contenant la carte à laquelle vous souhaitez ajouter une sous-tâche.<p>L’ID du panorama se trouve dans l’URL lors de l’affichage du panorama dans Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Name]</td> 
   <td>Saisissez ou mappez un nom pour la nouvelle sous-tâche.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Création d’une carte

Ce module d’action permet de créer une carte sur un panorama Workfront.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>Vous pouvez utiliser une connexion Workfront existante pour vous connecter aux tableaux Workfront ou une connexion aux tableaux Workfront spécifique. </p><p>Pour plus d’informations sur la connexion de votre application [!DNL Workfront] aux [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Création d’une connexion aux tableaux Workfront</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Saisissez ou mappez l’ID du panorama auquel vous souhaitez ajouter une carte.<p>L’ID du panorama se trouve dans l’URL lors de l’affichage du panorama dans Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column ID]</td> 
   <td>Saisissez ou mappez l’identifiant de la colonne à laquelle vous souhaitez ajouter une sous-tâche.<p>L’ID de colonne se trouve dans les informations renvoyées par le module Lecture de tableau .</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Name]</td> 
   <td>Saisissez ou mappez un nom pour la nouvelle carte.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Déplacer une carte

Ce module d’action déplace une carte vers une autre colonne du même panorama.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>Vous pouvez utiliser une connexion Workfront existante pour vous connecter aux tableaux Workfront ou une connexion aux tableaux Workfront spécifique. </p><p>Pour plus d’informations sur la connexion de votre application [!DNL Workfront] aux [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Création d’une connexion aux tableaux Workfront</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Saisissez ou mappez l’ID de la carte à déplacer.<p>L’ID de la carte se trouve dans l’URL lors de l’affichage de la carte dans Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Saisissez ou mappez l’ID du panorama contenant la carte à déplacer.<p>L’ID du panorama se trouve dans l’URL lors de l’affichage du panorama dans Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID de colonne de destination]</td> 
   <td>Saisissez ou mappez l’identifiant de la colonne vers laquelle vous souhaitez déplacer la carte.<p>L’ID de colonne se trouve dans les informations renvoyées par le module Lecture de tableau .</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL To index]</td> 
   <td>Saisissez ou mappez la position que la carte doit avoir dans la nouvelle colonne.<p>Position supérieure dans la colonne de l'index 0.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Lire une carte

Ce module d’action récupère des informations sur une carte spécifique.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>Vous pouvez utiliser une connexion Workfront existante pour vous connecter aux tableaux Workfront ou une connexion aux tableaux Workfront spécifique. </p><p>Pour plus d’informations sur la connexion de votre application [!DNL Workfront] aux [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Création d’une connexion aux tableaux Workfront</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Saisissez ou mappez l’identifiant de la carte que vous souhaitez lire.<p>L’ID de la carte se trouve dans l’URL lors de l’affichage de la carte dans Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Saisissez ou mappez l’identifiant du panorama contenant la carte que vous souhaitez lire.<p>L’ID du panorama se trouve dans l’URL lors de l’affichage du panorama dans Workfront.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Mise à jour d’une carte

Ce module d’action met à jour les informations d’une carte que vous spécifiez.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>Vous pouvez utiliser une connexion Workfront existante pour vous connecter aux tableaux Workfront ou une connexion aux tableaux Workfront spécifique. </p><p>Pour plus d’informations sur la connexion de votre application [!DNL Workfront] aux [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Création d’une connexion aux tableaux Workfront</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Saisissez ou mappez l’identifiant de la carte à mettre à jour.<p>L’ID de la carte se trouve dans l’URL lors de l’affichage de la carte dans Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Saisissez ou mappez l’ID du panorama contenant la carte à mettre à jour.<p>L’ID du panorama se trouve dans l’URL lors de l’affichage du panorama dans Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Name]</td> 
   <td>Saisissez ou mappez un nouveau nom pour la carte.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Description]</td> 
   <td>Saisissez ou mappez une nouvelle description pour la carte.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Estimation]</td> 
   <td>Saisissez ou mappez une estimation du temps nécessaire pour terminer cette carte.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Due date]</td> 
   <td>Saisissez ou mappez la date d'échéance de cette carte.</p>
   <p>Pour obtenir la liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercition</a>.</p>
   </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Status]</td> 
   <td>Sélectionnez un nouveau statut pour la carte.</p></td> 
  </tr> 
 </tbody> 
</table>

### Panneaux

* [Créer un panorama](#create-a-board)
* [Lire un panorama](#read-a-board)

#### Créer un panorama

Ce module d’action crée un panorama dans Workfront. Vous pouvez indiquer le type de panorama à créer.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>Vous pouvez utiliser une connexion Workfront existante pour vous connecter aux tableaux Workfront ou une connexion aux tableaux Workfront spécifique. </p><p>Pour plus d’informations sur la connexion de votre application [!DNL Workfront] aux [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Création d’une connexion aux tableaux Workfront</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board name]</td> 
   <td>Saisissez ou mappez un nom pour le nouveau panorama.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Template]</td> 
   <td>Sélectionnez le modèle correspondant au type de panorama que vous souhaitez créer.</td> 
  </tr> 
 </tbody> 
</table>

#### Lire un panorama

Ce module d’action renvoie des informations sur un tableau, telles que les cartes, les colonnes, les balises et les membres du tableau.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>Vous pouvez utiliser une connexion Workfront existante pour vous connecter aux tableaux Workfront ou une connexion aux tableaux Workfront spécifique. </p><p>Pour plus d’informations sur la connexion de votre application [!DNL Workfront] aux [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Création d’une connexion aux tableaux Workfront</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Saisissez ou mappez l’ID du panorama pour lequel vous souhaitez récupérer des informations.<p>L’ID du panorama se trouve dans l’URL lors de l’affichage du panorama dans Workfront.</p></td> 
  </tr> 
 </tbody> 
</table>

### Colonnes

* [Créer une colonne](#create-a-column)
* [Rechercher une colonne](#search-for-a-column)
* [Mise à jour d’une colonne](#update-a-column)

#### Créer une colonne

Ce module d’action crée une colonne sur le panorama spécifié.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>Vous pouvez utiliser une connexion Workfront existante pour vous connecter aux tableaux Workfront ou une connexion aux tableaux Workfront spécifique. </p><p>Pour plus d’informations sur la connexion de votre application [!DNL Workfront] aux [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Création d’une connexion aux tableaux Workfront</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Saisissez ou mappez l’identifiant du panorama auquel vous souhaitez ajouter une colonne.<p>L’ID du panorama se trouve dans l’URL lors de l’affichage du panorama dans Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Column ID]</td> 
   <td>Saisissez ou mappez l’identifiant de la colonne à mettre à jour.<p>L’ID de colonne se trouve dans les informations renvoyées par le module Lecture de tableau .</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Nom de colonne]</td> 
   <td>Saisissez ou mappez un nouveau nom pour la colonne.</td> 
  </tr> 
 </tbody> 
</table>

#### Rechercher une colonne

Ce module de recherche renvoie des informations sur la colonne portant le nom spécifié.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>Vous pouvez utiliser une connexion Workfront existante pour vous connecter aux tableaux Workfront ou une connexion aux tableaux Workfront spécifique. </p><p>Pour plus d’informations sur la connexion de votre application [!DNL Workfront] aux [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Création d’une connexion aux tableaux Workfront</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Saisissez ou mappez l’identifiant du panorama contenant la colonne à récupérer.<p>L’ID du panorama se trouve dans l’URL lors de l’affichage du panorama dans Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Nom de colonne]</td> 
   <td>Saisissez ou mappez le nom de la colonne à récupérer.</td> 
  </tr> 
 </tbody> 
</table>

#### Mise à jour d’une colonne

Ce module d&#39;action met à jour le nom ou la limite des travaux en cours de la colonne spécifiée.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>Vous pouvez utiliser une connexion Workfront existante pour vous connecter aux tableaux Workfront ou une connexion aux tableaux Workfront spécifique. </p><p>Pour plus d’informations sur la connexion de votre application [!DNL Workfront] aux [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Création d’une connexion aux tableaux Workfront</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Saisissez ou mappez l’identifiant du panorama contenant la colonne à récupérer.<p>L’ID du panorama se trouve dans l’URL lors de l’affichage du panorama dans Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Nom de colonne]</td> 
   <td>Saisissez ou mappez le nom de la colonne à récupérer.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL WIP Limit]</td> 
   <td>Saisissez ou mappez une nouvelle limite de travail en cours pour la colonne.</td> 
  </tr> 
 </tbody> 
</table>

### Balises

* [Ajouter une balise à une carte](#add-a-tag-to-a-card)
* [Créer une balise](#create-a-tag)

#### Ajouter une balise à une carte

Ce module d’action ajoute une balise à une carte.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>Vous pouvez utiliser une connexion Workfront existante pour vous connecter aux tableaux Workfront ou une connexion aux tableaux Workfront spécifique. </p><p>Pour plus d’informations sur la connexion de votre application [!DNL Workfront] aux [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Création d’une connexion aux tableaux Workfront</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Saisissez ou mappez l’identifiant de la carte à laquelle vous souhaitez ajouter une balise.<p>L’ID de la carte se trouve dans l’URL lors de l’affichage de la carte dans Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Saisissez ou mappez l’identifiant du panorama contenant la carte à laquelle vous souhaitez ajouter une balise.<p>L’ID du panorama se trouve dans l’URL lors de l’affichage du panorama dans Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tag ID]</td> 
   <td>Saisissez ou mappez l’identifiant de la balise que vous souhaitez ajouter.<p>L’ID de balise se trouve dans les informations renvoyées par le module Lecture de tableau .</p></td> 
  </tr> 
 </tbody> 
</table>

#### Créer une balise

Ce module d’action crée une balise et lui affecte une couleur.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>Vous pouvez utiliser une connexion Workfront existante pour vous connecter aux tableaux Workfront ou une connexion aux tableaux Workfront spécifique. </p><p>Pour plus d’informations sur la connexion de votre application [!DNL Workfront] aux [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Création d’une connexion aux tableaux Workfront</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Board ID]</td> 
   <td>Saisissez ou mappez l’identifiant du panorama pour lequel vous souhaitez créer une balise.<p>L’ID du panorama se trouve dans l’URL lors de l’affichage du panorama dans Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tag name]</td> 
   <td>Saisissez ou mappez le nom de la nouvelle balise.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Tag Color]</td> 
   <td>Sélectionnez la couleur de cette balise.</td> 
  </tr> 
 </tbody> 
</table>

### Commentaires

* [Créer un commentaire](#create-a-comment)
* [Lire les commentaires de la carte](#read-card-comments)

#### Créer un commentaire

Ce module d’action a créé un commentaire sur la carte spécifiée.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>Vous pouvez utiliser une connexion Workfront existante pour vous connecter aux tableaux Workfront ou une connexion aux tableaux Workfront spécifique. </p><p>Pour plus d’informations sur la connexion de votre application [!DNL Workfront] aux [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Création d’une connexion aux tableaux Workfront</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Saisissez ou mappez l’identifiant de la carte à laquelle vous souhaitez ajouter un commentaire.<p>L’ID de la carte se trouve dans l’URL lors de l’affichage de la carte dans Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Comment]</td> 
   <td>Saisissez ou mappez le texte du commentaire que vous souhaitez ajouter.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Lire les commentaires de la carte

Ce module d’action récupère les commentaires de la carte spécifiée.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>Vous pouvez utiliser une connexion Workfront existante pour vous connecter aux tableaux Workfront ou une connexion aux tableaux Workfront spécifique. </p><p>Pour plus d’informations sur la connexion de votre application [!DNL Workfront] aux [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Création d’une connexion aux tableaux Workfront</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Card ID]</td> 
   <td>Saisissez ou mappez l’identifiant de la carte pour laquelle vous souhaitez récupérer les commentaires.<p>L’ID de la carte se trouve dans l’URL lors de l’affichage de la carte dans Workfront.</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td>Saisissez le nombre maximal de commentaires que le module doit renvoyer au cours d'un cycle d'exécution.</p></td> 
  </tr> 
 </tbody> 
</table>

### Autre

#### Effectuer un appel API personnalisé.

Ce module d’action effectue un appel personnalisé à l’API Workfront Boards.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
      <td> <p>Vous pouvez utiliser une connexion Workfront existante pour vous connecter aux tableaux Workfront ou une connexion aux tableaux Workfront spécifique. </p><p>Pour plus d’informations sur la connexion de votre application [!DNL Workfront] aux [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Création d’une connexion aux tableaux Workfront</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>Saisissez un chemin relatif vers <code> https://&lt;WORKFRONT_DOMAIN&gt;/boards-service/graphql?</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p><p>Pour la plupart des appels de panorama, la méthode est POST. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard. Cela détermine le type de contenu de la requête.</p> <p>Par exemple,<code> { "Content-type":"application/json-stringify()"}</code></p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Ajoutez la requête pour l’appel API sous la forme d’un objet JSON standard.</p> <p>Pour les tableaux Workfront, cette section est généralement laissée vide.</p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un Graphql incorporé JSON </p> <p>Exemple :</p><p>Cet exemple montre comment mettre à jour le nom d'une colonne. Vous pouvez inclure les <code>boardId</code> et <code>columnId</code> en tant que GUID codés en dur ou mappés à partir d’un module précédent.<p><pre>{<br> « query »: « mutation { updateColumn(boardId: \« \ », columnId: \« \ », updateColumnInput: { name: \« \ » }) { id name }} »<br>}</pre><p>Note :  <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre JSON, placez les guillemets à l’extérieur de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>


#### Effectuer un appel API GraphQL personnalisé

Ce module d’action envoie une requête GraphQL personnalisée à l’API Workfront Boards.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
      <td> <p>Vous pouvez utiliser une connexion Workfront existante pour vous connecter aux tableaux Workfront ou une connexion aux tableaux Workfront spécifique. </p><p>Pour plus d’informations sur la connexion de votre application [!DNL Workfront] aux [!DNL Workfront Fusion], voir <a href="#create-a-connection-to-workfront-boards" class="MCXref xref">Création d’une connexion aux tableaux Workfront</a> dans cet article.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Sélectionnez la méthode de cet appel. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td> <p>Ajoutez la requête pour l’appel API sous la forme d’un objet JSON standard.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Nom de l’opération]</td> 
   <td> <p>Saisissez un nom pour cette opération. Cela peut faciliter le suivi et le débogage de l’appel .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source de données des variables]</td> 
   <td> <p>Indiquez si les variables proviennent d’un formulaire ou d’une collection.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variables]</td> 
   <td> <p>Pour chaque variable à ajouter, cliquez sur <b>Ajouter un élément</b> et saisissez la clé et la valeur de la variable.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</td> 
   </tr> 
 </tbody> 
</table>
