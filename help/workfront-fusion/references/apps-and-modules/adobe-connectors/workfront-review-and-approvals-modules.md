---
title: Modules Contenu et validations d’Adobe Workfront
description: Grâce aux modules Contenu et approbations d’Adobe Workfront, vous pouvez obtenir des détails d’approbation, prendre une décision concernant une ressource, ajouter ou supprimer des participants à l’approbation, ajouter ou mettre à jour des étapes d’approbation, verrouiller ou déverrouiller des étapes, et effectuer des appels d’API personnalisés.
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 8b031ed2093d4844f05c52db9fc79ce9e7e4b85c
workflow-type: tm+mt
source-wordcount: 3743
ht-degree: 17%

---

# Modules Adobe Workfront Unified Review and Approvals

Grâce aux modules de révision et d’approbation unifiées d’Adobe Workfront, vous pouvez obtenir des détails d’approbation, prendre une décision concernant une ressource, ajouter ou supprimer des participants à l’approbation, ajouter ou mettre à jour des étapes d’approbation, verrouiller ou déverrouiller des étapes et effectuer des appels d’API personnalisés.

Pour plus d’informations sur la révision et les approbations unifiées de Workfront, voir [Présentation de la révision et de l’approbation unifiées](https://experienceleague.adobe.com/en/docs/workfront/using/review-and-approve-work/document-approvals-overview) dans la documentation de Workfront.

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

## Conditions préalables

Pour accéder au contenu et aux approbations de Workfront, vous devez disposer des éléments suivants :

* Vous devez utiliser une version de Workfront prenant en charge l’espace de stockage dans le cloud Adobe. Si votre organisation ne dispose pas déjà d’une version prise en charge, contactez votre représentant de compte Adobe.

## Se connecter à Adobe Workfront Unified Review and Approvals


1. Dans un module Adobe Workfront Unified Review and Approvals , cliquez sur **Ajouter** en regard du champ Connexion .
1. Remplissez les champs suivants :

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>
          <p>Sélectionnez <b>Connexion Adobe Workfront de serveur à serveur</b>.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Saisissez un nom pour la nouvelle connexion.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Instance name]</td>
        <td>
          <p>Saisissez le nom de votre instance, également appelée domaine.</p><p>Exemple : si votre URL est <code>https://example.my.workfront.com</code>, saisissez <code>example</code>.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Instance lane]</td>
        <td>
          <p>Indiquez le type d’environnement auquel cette connexion doit se connecter.</p><p>Exemple : si votre URL est <code>https://example.my.workfront.com</code>, saisissez <code>my</code>.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Saisissez votre ID client Workfront. Vous le trouverez dans la zone Applications OAuth2 de la zone Configuration dans Workfront. Ouvrez l’application spécifique à laquelle vous vous connectez pour afficher l’ID client.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Saisissez votre secret client Workfront. Vous le trouverez dans la zone Applications OAuth2 de la zone Configuration dans Workfront. Si vous ne disposez pas d’un secret client pour votre application OAuth2 dans Workfront, vous pouvez en générer un autre. Pour obtenir des instructions, consultez la documentation de Workfront.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Scopes]</td>
        <td>Saisissez toutes les étendues applicables à cette connexion.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Host prefix]</td>
        <td>Dans la plupart des cas, cette valeur doit être <code>origin</code>.
      </tr>
    </tbody>
    </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour enregistrer la connexion et revenir au module.

   Si vous n’êtes pas connecté à Workfront Unified Review and Approvals, vous êtes redirigé vers un écran de connexion. Une fois la connexion effectuée, vous pouvez autoriser la connexion.

## Modules Adobe Workfront Unified Review and Approvals

Lorsque vous configurez les modules Workfront, Workfront Fusion affiche les champs répertoriés ci-dessous. Des champs Workfront supplémentaires peuvent s’afficher, selon votre niveau d’accès dans l’application ou le service, par exemple. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, consultez [Mappage d’informations d’un module à l’autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).


![Bouton (bascule) de mappage](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Actions](#actions)
* [Recherches](#searches)
* [Autre](#other)

### Actions

* [Ajouter ou mettre à jour des participants](#add-or-update-participants)
* [Modèles de suppression en bloc](#bulk-delete-templates)
* [Créer un modèle](#create-a-template)
* [Création d’une validation](#create-an-approval)
* [Création d’étapes](#create-stages)
* [Suppression d’une décision sur une étape](#delete-a-decision-on-a-stage)
* [Supprimer une étape](#delete-a-stage)
* [Supprimer un modèle](#delete-a-template)
* [# Supprimer une approbation](#delete-an-approval)
* [Supprimer les décisions](#delete-decisions)
* [Supprimer les participants](#delete-participants)
* [Verrouiller une étape](#lock-a-stage)
* [Prendre une décision](#make-a-decision)
* [Prendre une décision sur une étape](#make-a-decision-on-a-stage)
* [Rappeler un participant sur une scène](#remind-a-participant-on-a-stage)
* [Rappeler au participant](#remind-participant)
* [Adresser un rappel aux participants indécis](#remind-undecided-participants)
* [Rappeler aux participants indécis sur une scène](#remind-undecided-participants-on-a-stage)
* [Déverrouiller une étape](#unlock-a-stage)
* [Mise à jour d’une étape](#update-a-stage)
* [Mise à jour d’un modèle](#update-a-template)
* [Mettre à jour toutes les étapes](#update-all-stages)


#### Ajouter ou mettre à jour des participants

Ce module d&#39;action ajoute ou met à jour les participants à l&#39;étape par défaut d&#39;une approbation.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>ID de document</p>
      </td>
      <td>Saisissez ou mappez l’identifiant de la ressource pour laquelle vous souhaitez ajouter ou mettre à jour un participant.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Ajouter des participants aux étapes</p>
      </td>
      <td>Pour chaque étape à laquelle vous souhaitez ajouter des participants, cliquez sur <b>Ajouter un élément</b> et saisissez l’étape.<p> Ensuite, pour chaque participant que vous souhaitez ajouter à l’étape, cliquez sur <b>Ajouter un élément</b> et saisissez les détails du participant.</p>
      <ul>
      <li><b>ID de participant</b><p>Saisissez ou mappez l’ID du participant.</p></li>
      <li><b>Type de participant</b><p>Indiquez si le participant est un utilisateur ou une équipe.</p></li>
      <li><b>Rôle du participant</b><p>Indiquez si le participant est un approbateur ou un réviseur.</p></li>
      </ul> 
      </td> 
      </tr>
  </tbody>
</table>

#### Modèles de suppression en bloc

Ce module supprime les modèles d&#39;approbation spécifiés.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de modèle</p></td>
      <td>Pour chaque modèle à supprimer, cliquez sur <b>Ajouter un élément</b> et saisissez l’ID du modèle.</td> 
      </tr>
  </tbody>
</table>

#### Créer un modèle

Ce module d&#39;action crée un modèle d&#39;approbation

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Nom</p></td>
      <td>Saisissez ou mappez un nom pour le modèle.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID d'entreprise</p></td>
      <td>Si vous souhaitez ajouter une étendue d'entreprise au modèle, saisissez ou mappez l'ID d'entreprise.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Étapes</p>
      </td>
      <td>Pour chaque étape à ajouter, cliquez sur <b>Ajouter un élément</b> et saisissez les données de l’étape.<p>Pour plus d’informations, voir <a href="#stages-fields" class="MCXref xref" >Champs d’étape</a> dans cet article. </p> </td> 
      </tr>
    <tr>
      <td role="rowheader"><p>Partagé avec</p></td>
      <td>Pour chaque utilisateur avec lequel vous souhaitez partager le modèle, cliquez sur <b>Ajouter un élément</b> puis sur ID utilisateur et niveau d’accès souhaité.</td> 
      </tr>
  </tbody>
</table>

#### Création d’une validation

Ce module d’action crée une approbation pour un document sur l’espace de stockage dans le cloud d’Adobe, y compris les données d’évaluation ou un modèle.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de document</p></td>
      <td>Saisissez ou mappez l’identifiant de la ressource pour laquelle vous souhaitez créer une approbation.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Étapes</p>
      </td>
      <td>Pour chaque étape à ajouter, cliquez sur <b>Ajouter un élément</b> et saisissez les données de l’étape.<p>Pour plus d’informations, voir <a href="#stages-fields" class="MCXref xref" >Champs d’étape</a> dans cet article. </p> </td> 
      </tr>
    <tr>
      <td role="rowheader"><p>ID de modèle</p></td>
      <td>Saisissez ou mappez l'ID du modèle que vous souhaitez utiliser pour cette approbation.</td> 
      </tr>
  </tbody>
</table>

#### Création d’étapes

Ce module d’action crée une approbation avec les données d’étape données.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de document</p></td>
      <td>Saisissez ou mappez l’identifiant de la ressource pour laquelle vous souhaitez créer ou mettre à jour une étape.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Étapes</p>
      </td>
      <td>Pour chaque étape à ajouter, cliquez sur <b>Ajouter un élément</b> et saisissez les données de l’étape.<p>Pour plus d’informations, voir <a href="#stages-fields" class="MCXref xref" >Champs d’étape</a> dans cet article. </p> </td> 
      </tr>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de modèle</p></td>
      <td>Saisissez ou mappez l’identifiant de la ressource pour laquelle vous souhaitez créer des étapes.</td> 
      </tr>
  </tbody>
</table>

#### Suppression d’une décision sur une étape

Ce module supprime la décision de l’utilisateur actuel de l’étape spécifiée. L’utilisateur actuel est l’utilisateur dont les informations d’identification sont utilisées dans la connexion utilisée dans ce module.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de document</p></td>
      <td>Saisissez ou mappez l’ID du document à partir duquel vous souhaitez supprimer une décision.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID d’étape</p></td>
      <td>Saisissez ou mappez l’identifiant de l’étape à supprimer.</td> 
      </tr>
   </tbody>
</table>


#### Supprimer une étape

Ce module d&#39;action supprime l&#39;étape spécifiée de la validation.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de document</p></td>
      <td>Saisissez ou mappez l’ID du document à partir duquel vous souhaitez supprimer une étape.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID d’étape</p></td>
      <td>Saisissez ou mappez l’identifiant de l’étape à supprimer.</td> 
      </tr>
  </tbody>
</table>

#### Supprimer un modèle

Ce module supprime le modèle d&#39;approbation spécifié.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de modèle</p></td>
      <td>Saisissez ou mappez l’identifiant du modèle que vous souhaitez supprimer.</td> 
      </tr>
  </tbody>
</table>

#### Supprimer une approbation

Ce module d&#39;action supprime l&#39;approbation du document donné.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de document</p></td>
      <td>Saisissez ou mappez l’ID du document à partir duquel vous souhaitez supprimer une approbation.</td> 
      </tr>
  </tbody>
</table>

#### Supprimer les décisions

Ce module supprime la décision de l’utilisateur actuel de l’étape spécifiée. L’utilisateur actuel est l’utilisateur dont les informations d’identification sont utilisées dans la connexion utilisée dans ce module.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de document</p></td>
      <td>Saisissez ou mappez l’ID du document à partir duquel vous souhaitez supprimer une décision.</td> 
      </tr>
  </tbody>
</table>

#### Supprimer les participants

Ce module d&#39;action supprime les participants d&#39;une approbation.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de document</p></td>
      <td>Saisissez ou mappez l’identifiant de la ressource à partir de laquelle vous souhaitez supprimer des participants.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Type de participant</p>
      </td>
      <td>Indiquez si les participants sont un utilisateur ou une équipe.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>ID de participant</p>
      </td>
      <td>Saisissez ou mappez l’ID du participant.</td> 
      </tr>
  </tbody>
</table>

#### Verrouiller une étape

Ce module d’action verrouille l’étape d’approbation spécifiée et la définit sur inactive.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de document</p></td>
      <td>Saisissez ou mappez l’identifiant de la ressource à verrouiller.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>ID d’étape</p>
      </td>
      <td>Saisissez ou mappez l’identifiant de l’étape que vous souhaitez verrouiller.</td> 
      </tr>
  </tbody>
</table>

#### Prendre une décision

Ce module d&#39;action applique une décision à une étape d&#39;approbation ou d&#39;approbation.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de document</p></td>
      <td>Saisissez ou mappez l’identifiant de la ressource à verrouiller.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Décision</p></td>
      <td>Sélectionnez la décision à appliquer à l’approbation ou à l’étape.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>ID d’étape</p>
      </td>
      <td>Pour chaque étape à laquelle vous souhaitez appliquer la décision, cliquez sur <b>Ajouter un élément</b> et saisissez l’ID d’étape.</td> 
      </tr>
  </tbody>
</table>

#### Prendre une décision sur une étape

Ce module applique une décision à l’étape spécifiée.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de document</p></td>
      <td>Saisissez ou mappez l’ID du document sur lequel vous souhaitez prendre une décision.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID d’étape</p></td>
      <td>Saisissez ou mappez l’identifiant de l’étape sur laquelle vous souhaitez prendre une décision.</td> 
      </tr>
    <tr>
      <td role="rowheader"><p>Décision</p></td>
      <td>Sélectionnez la décision que vous souhaitez appliquer à cette étape.</td> 
      </tr>
  </tbody>
</table>

#### Rappeler un participant sur une scène

Ce module envoie un rappel à un participant spécifique sur une étape spécifique.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de document</p></td>
      <td>Saisissez ou mappez l’identifiant de la ressource pour laquelle vous souhaitez envoyer un rappel.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>ID d’étape</p>
      </td>
      <td>Saisissez ou mappez l’identifiant de l’étape pour laquelle vous souhaitez envoyer un rappel.</td> 
      </tr>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de participant</p></td>
      <td>Saisissez ou mappez l’ID du participant auquel vous souhaitez envoyer un rappel.</td> 
      </tr>
  </tbody>
</table>

#### Rappeler au participant

Ce module envoie une notification de rappel au participant spécifié.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de document</p></td>
      <td>Saisissez ou mappez l’identifiant de la ressource pour laquelle vous souhaitez envoyer un rappel.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>ID de participant</p>
      </td>
      <td>Saisissez ou mappez l’ID du participant à rappeler.</td> 
      </tr>
      <tr>
      <td role="rowheader">
        <p>Type de participant</p>
      </td>
      <td>Saisissez ou mappez le type de participant à rappeler.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Rôle du participant</p>
      </td>
      <td>Saisissez ou mappez le rôle du participant que vous souhaitez rappeler.</td> 
      </tr>
  </tbody>
</table>

#### Adresser un rappel aux participants indécis

Ce module envoie des notifications de rappel à tous les participants indécis lors de l&#39;approbation spécifiée.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de document</p></td>
      <td>Saisissez ou mappez l’identifiant de la ressource pour laquelle vous souhaitez envoyer un rappel.</td> 
      </tr>
  </tbody>
</table>

#### Rappeler aux participants indécis sur une scène

Ce module envoie des notifications de rappel à tous les participants indécis sur une étape.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de document</p></td>
      <td>Saisissez ou mappez l’identifiant de la ressource pour laquelle vous souhaitez envoyer un rappel.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>ID d’étape</p>
      </td>
      <td>Saisissez ou mappez l’identifiant de l’étape pour laquelle vous souhaitez envoyer un rappel.</td> 
      </tr>
  </tbody>
</table>

#### Déverrouiller une étape

Ce module d’action déverrouille l’étape d’approbation spécifiée et la définit sur active.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de document</p></td>
      <td>Saisissez ou mappez l’identifiant de la ressource à déverrouiller.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>ID d’étape</p>
      </td>
      <td>Saisissez ou mappez l’identifiant de l’étape que vous souhaitez verrouiller.</td> 
      </tr>
  </tbody>
</table>


#### Mise à jour d’une étape

Ce module d’action met à jour les champs de l’étape spécifiée.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de document</p></td>
      <td>Saisissez ou mappez l’ID du document sur lequel vous souhaitez prendre une décision.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID d’étape</p></td>
      <td>Saisissez ou mappez l’identifiant de l’étape sur laquelle vous souhaitez prendre une décision.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Nom de l’étape</p></td>
      <td>Saisissez ou mappez un nom pour le modèle.</td> 
      </tr>
      <td role="rowheader">
        <p>Autres champs</p>
      </td>
      <td>Saisissez les données dans les champs d’étape.<p>Pour plus d’informations, voir <a href="#stages-fields" class="MCXref xref" >Champs d’étape</a> dans cet article. </p> </td> 
      </tr>
    <tr>
      <td role="rowheader"><p>Partagé avec</p></td>
      <td>Pour chaque utilisateur avec lequel vous souhaitez partager le modèle, cliquez sur <b>Ajouter un élément</b> puis sur ID utilisateur et niveau d’accès souhaité.</td> 
      </tr>
  </tbody>
</table>

#### Mise à jour d’un modèle

Ce module met à jour les champs du modèle de validation spécifié.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de modèle</p></td>
      <td>Saisissez ou mappez un nom pour le modèle.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Nom</p></td>
      <td>Saisissez ou mappez l’identifiant du modèle que vous souhaitez mettre à jour.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID d'entreprise</p></td>
      <td>Si vous souhaitez ajouter une étendue d'entreprise au modèle, saisissez ou mappez l'ID d'entreprise.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Étapes</p>
      </td>
      <td>Pour chaque étape à ajouter, cliquez sur <b>Ajouter un élément</b> et saisissez les données de l’étape.<p>Pour plus d’informations, voir <a href="#stages-fields" class="MCXref xref" >Champs d’étape</a> dans cet article. </p> </td> 
      </tr>
    <tr>
      <td role="rowheader"><p>Partagé avec</p></td>
      <td>Pour chaque utilisateur avec lequel vous souhaitez partager le modèle, cliquez sur <b>Ajouter un élément</b> puis sur ID utilisateur et niveau d’accès souhaité.</td> 
      </tr>
  </tbody>
</table>

#### Mettre à jour toutes les étapes

Ce module remplace toutes les étapes d’une approbation existante par les données d’étape données. Le document doit être dans un état modifiable.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de document</p></td>
      <td>Saisissez ou mappez l’identifiant de la ressource pour laquelle vous souhaitez mettre à jour les étapes.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Étapes</p>
      </td>
      <td>Pour chaque étape à mettre à jour, cliquez sur <b>Ajouter un élément</b> et saisissez les données de l’étape.<p>Pour plus d’informations, voir <a href="#stages-fields" class="MCXref xref" >Champs d’étape</a> dans cet article. </p> </td> 
      </tr>
  </tbody>
</table>

### Recherches

* [Obtenir un modèle](#get-a-template)
* [Obtenir les détails d’approbation](#get-approval-details)
* [Obtenir plusieurs approbations](#get-multiple-approvals)
* [Obtenir les approbations suggérées](#get-suggested-approvals)
* [Obtenir les participants suggérés](#get-suggested-participants)
* [Liste des robots](#list-bots)
* [Répertorier les modèles](#list-templates)
* [Rechercher des réviseurs de marque AI](#search-ai-brand-reviews)


#### Obtenir un modèle

Ce module renvoie le modèle d&#39;approbation spécifié.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de modèle</p></td>
      <td>Saisissez ou mappez l'ID du document pour lequel vous souhaitez obtenir les participants à l'approbation suggérés.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Nombre maximal de modèles renvoyés
         </td>
         <td>
              Saisissez ou mappez le nombre maximum de modèles que vous souhaitez que le module renvoie au cours de chaque cycle d’exécution de scénario. 
         </td>
       </tr>
  </tbody>
</table>

#### Obtenir les détails d’approbation

Ce module de recherche récupère les détails d’approbation d’une ressource.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>Document</p>
      </td>
      <td>Saisissez ou mappez l’identifiant de la ressource pour laquelle vous souhaitez récupérer les détails d’approbation.</td> 
      </tr>
  </tbody>
</table>

#### Obtenir plusieurs approbations

Ce module récupère les détails des validations pour une liste de documents d’un type spécifique.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de document</p></td>
      <td>Pour chaque document pour lequel vous souhaitez récupérer les détails d’approbation, cliquez sur <b>Ajouter un élément</b> et saisissez l’ID du document.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Nombre maximal de résultats renvoyés
         </td>
         <td>
              Saisissez ou mappez le nombre maximal de résultats que le module doit renvoyer au cours de chaque cycle d’exécution du scénario. 
         </td>
       </tr>
  </tbody>
</table>

#### Obtenir les approbations suggérées

Ce module renvoie les payloads d’approbation suggérées à partir de versions antérieures du document.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de document</p></td>
      <td>Saisissez ou mappez l'ID du document pour lequel vous souhaitez obtenir des suggestions d'approbation.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Nombre maximum de validations renvoyées
         </td>
         <td>
              Saisissez ou mappez le nombre maximal de validations que le module doit renvoyer au cours de chaque cycle d’exécution du scénario. 
         </td>
       </tr>
  </tbody>
</table>

#### Obtenir les participants suggérés

Ce module renvoie les suggestions des participants de l&#39;approbation de la précédente approbation du document.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID de document</p></td>
      <td>Saisissez ou mappez l'ID du document pour lequel vous souhaitez obtenir les participants à l'approbation suggérés.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Nombre maximum de participants retournés
         </td>
         <td>
              Saisissez ou mappez le nombre maximal de participants que le module doit renvoyer au cours de chaque cycle d'exécution du scénario. 
         </td>
       </tr>
  </tbody>
</table>

#### Liste des robots

Ce module renvoie une liste paginée des comptes de robots.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Page</p></td>
      <td>Saisissez ou mappez la page de résultats que vous souhaitez renvoyer.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Nombre maximal de résultats renvoyés
         </td>
         <td>
              Saisissez ou mappez le nombre maximal de résultats que le module doit renvoyer au cours de chaque cycle d’exécution du scénario. 
         </td>
       </tr>
  </tbody>
</table>

#### Modèles de liste

Ce module renvoie une liste de tous les modèles d’approbation disponibles pour l’utilisateur actuel. L’utilisateur actuel est l’utilisateur dont les informations d’identification sont utilisées dans la connexion utilisée dans ce module.



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
   </tbody>
</table>

#### Rechercher des avis de marque sur l’IA

Ce module renvoie les résultats de la révision de marque de l’IA qui ont été générés pour une version de document dans le cadre d’une approbation.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>ID d’utilisateur du robot</p></td>
      <td>Saisissez ou mappez l’ID utilisateur du robot que vous souhaitez rechercher dans les avis.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID du document parent</p></td>
      <td>Saisissez ou mappez l'ID du document parent que vous souhaitez rechercher dans les révisions.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID de version du document</p></td>
      <td>Saisissez ou mappez l’identifiant de la ressource pour laquelle vous souhaitez envoyer un rappel.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID d’étape</p></td>
      <td>Saisissez ou mappez un ID d’étape pour limiter les résultats à une étape spécifique de l’approbation.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Page</p></td>
      <td>Saisissez ou mappez un numéro de page pour limiter les résultats à cette page.</td> 
      </tr>
       <tr>
         <td role="rowheader">
           Nombre maximal de révisions renvoyées
         </td>
         <td>
              Saisissez ou mappez le nombre maximal de révisions que le module doit renvoyer au cours de chaque cycle d’exécution du scénario. 
         </td>
       </tr>
  </tbody>
</table>

### Autre

* [Effectuer un appel API personnalisé](#make-a-custom-api-call)
* [Champs d’étapes](#stages-fields)


#### Effectuer un appel API personnalisé

Ce module effectue un appel API personnalisé à l’API Adobe Workfront Unified Review and Approvals.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Workfront Unified Review and Approvals, voir <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Se connecter à Adobe Workfront Unified Review and Approvals</a> dans cet article.</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>Chemin relatif</p>
      </td>
      <td>
        <p>Saisissez un chemin d’accès relatif à <code>https://workfront.adobe.io</code>. Par exemple, <code>/unified-approvals/public/api/v1/approvals/&lt;ASSET_TYPE&gt;/&lt;ASSET_ID&gt;</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Méthode</p>
      </td>
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, consultez <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">En-têtes</td>
      <td>
        <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p>
        <p>Par exemple, <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion ajoute automatiquement des en-têtes d’autorisation.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Pour chaque paire clé/valeur à ajouter à la chaîne de requête, cliquez sur <b>Ajouter un élément</b> et saisissez la clé et la valeur.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre JSON, placez les guillemets à l’extérieur de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>



#### Champs d’étapes

Les champs suivants sont disponibles lors de la configuration des étapes. Tous les champs peuvent ne pas être disponibles pour tous les modules.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Nom de l’étape</td>
      <td>Saisissez ou mappez un nom pour l’étape.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Date limite</p></td>
      <td>Si l’échéance correspond à une date spécifique, saisissez ou mappez la date.</td> 
      </tr>
  </tbody>
     <tr>
      <td role="rowheader"><p>Délai en jours ouvrables</p></td>
      <td>Si l’échéance est postérieure à un nombre spécifique de jours ouvrables, saisissez ou mappez le nombre de jours.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Date limite</p></td>
      <td>Si l’échéance est une heure spécifique, saisissez ou mappez l’heure.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Participantes et participants</p></td>
      <td>Pour chaque participant que vous souhaitez ajouter à l’étape, cliquez sur <b>Ajouter un élément</b> et saisissez les détails du participant.      
      <ul>
      <li><b>ID de participant</b><p>Saisissez ou mappez l’ID du participant.</p></li>
      <li><b>Type de participant</b><p>Indiquez si le participant est un utilisateur ou une équipe.</p></li>
      <li><b>Rôle du participant</b><p>Indiquez si le participant est un approbateur ou un réviseur.</p></li>
      </ul> 
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Verrouillage automatique activé</p></td>
      <td>Indiquez si vous souhaitez verrouiller automatiquement l’étape.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Règles de décision</p></td>
      <td>Choisissez si vous souhaitez ne nécessiter qu’une seule décision pour l’étape.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>ID de tâche parent/ID d’étape parent</p></td>
      <td>Pour chaque étape parent que vous souhaitez ajouter à l’étape, cliquez sur <b>Ajouter un élément</b> et saisissez l’ID parent.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Déclencheurs</p></td>
      <td>Pour configurer un déclencheur pour cette étape d’approbation, cliquez sur <b>Ajouter un élément</b> et saisissez les détails du déclencheur.      <ul>
      <li><b>Type</b><p>Sélectionnez <b> Activation </b></p></li>
      <li><b>Lorsque</b><p>Choisissez de déclencher l’étape lorsque l’approbation est créée ou lorsqu’une autre étape est terminée.</p></li>
      <li><b>Étapes</b><p>Pour chaque étape à ajouter au déclencheur, cliquez sur <b>Ajouter un élément</b> et saisissez ou mappez l’ID d’étape.</p></li>
      <li><b>Décisions</b><p>Pour chaque décision que vous souhaitez ajouter au déclencheur, cliquez sur <b>Ajouter un élément</b> et saisissez ou mappez la décision.</p></li>
      </ul> 
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Message personnalisé</p></td>
      <td>Saisissez ou mappez un message personnalisé pour l’étape.</td> 
      </tr>
</table>

