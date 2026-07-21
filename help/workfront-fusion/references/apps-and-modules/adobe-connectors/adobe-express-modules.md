---
title: Modules Adobe Express
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent Adobe Express.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
source-git-commit: eab04db9a38020ed973f98d7f8f290ccd183251c
workflow-type: tm+mt
source-wordcount: '1372'
ht-degree: 19%

---

# Modules Adobe Express

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent Adobe Express et les connecter à plusieurs applications et services tiers.

Si vous avez besoin d’instructions pour créer un scénario, consultez les articles sous [Créer un scénario : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

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
   <td role="rowheader">Licence Adobe Workfront Fusion</td> 
   <td>
   <p>Basé sur les opérations : aucune exigence de licence Workfront Fusion</p>
   <p>Basé sur un connecteur (hérité) : Workfront Fusion pour l’automatisation et l’intégration du travail </p>
   </td> 
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

Pour plus d’informations sur les licences Adobe Workfront Fusion, consultez [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Conditions préalables

Avant de pouvoir utiliser le connecteur Adobe Express, vous devez vous assurer que les conditions préalables suivantes sont remplies :

* Vous devez disposer d’un compte Adobe Express actif.

## Création d’une connexion à Adobe Express

Pour créer une connexion pour vos modules Adobe Express :

1. Dans n’importe quel module, cliquez sur **[!UICONTROL Ajouter]** en regard de la zone Connexion .

1. Remplissez les champs suivants :

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">Nom de la connexion</td>
        <td>
          <p>Saisissez un nom pour cette connexion.</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">Environnement</td>
        <td>Indiquez si vous vous connectez à un environnement de production ou hors production.</td>
        </tr>
        <tr>
        <td role="rowheader">Type</td>
        <td>Indiquez si vous vous connectez à un compte de service ou à un compte personnel.</td>
        </tr>
        <tr>
        <td role="rowheader">ID client</td>
        <td>Saisissez votre identifiant client Adobe. Vous trouverez cette information dans la section Informations d’identification du Adobe Developer Console.</td>
        </tr>
        <tr>
        <td role="rowheader">Clé secrète client</td>
        <td>Saisissez votre clé secrète client Adobe. Vous trouverez cette information dans la section Informations d’identification du Adobe Developer Console.</td>
        </tr>
      </tbody>
    </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour enregistrer la connexion et revenir au module.


## Modules Adobe Express et leurs champs

Lorsque vous configurez les modules Adobe Express, Workfront Fusion affiche les champs répertoriés ci-dessous. Selon des facteurs tels que votre niveau d’accès dans l’application ou le service, d’autres champs Adobe Express peuvent s’afficher en plus de ceux-ci. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, consultez [Mappage d’informations d’un module à l’autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Bouton (bascule) de mappage](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Actions

#### Exportation d’un rendu

Ce module exporte un document au format JPG ou PNG. Il peut fournir des URL présignées pour les rendus de page, qui sont valides pendant quatre heures.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Express, voir <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Création d’une connexion à Adobe Express</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Document</td> 
   <td>Sélectionnez le document pour lequel vous souhaitez exporter un rendu.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Numéros de page</td> 
   <td>Saisissez ou mappez les numéros de page à inclure dans le rendu. Chaîne de numéros de page séparés par des virgules pour laquelle la demande de rendu est effectuée. Par exemple, « 1, 2, 3 ». Vous pouvez également spécifier des plages de pages. Par exemple, « 1-3 » inclut les pages 1, 2 et 3. Un autre exemple est « 1,3-5 », qui comprend les pages 1, 3, 4 et 5. « 1- » peut être utilisé pour spécifier toutes les pages, tandis que « 5- » indique la page 5 à la dernière page. Si elle n’est pas fournie, la première page est prise en compte par défaut. Les numéros de page commencent à partir de 1.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Type de rendu</td> 
   <td>Sélectionnez le type de rendu à exporter : image, vidéo ou PDF</td> 
  </tr>
  <tr> 
   <td role="rowheader">Format</td> 
   <td>Sélectionnez le format de fichier du rendu.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Type de PDF</td> 
   <td>Si vous exportez un PDF, choisissez d’exporter un PDF standard ou d’imprimer.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Taille</td> 
   <td>Si vous exportez une image ou une vidéo, saisissez ou mappez la taille, en pixels, du côté le plus long. Les proportions sont conservées. Pour l’image, la taille minimale prise en charge est de 1 px et la taille maximale prise en charge est de 8 192 px. Si elle n’est pas fournie, la taille par défaut de la page est prise en compte.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Téléchargement de fichiers PDF individuels</td> 
   <td>Si vous exportez un PDF, indiquez si les pages sont téléchargées en tant que fichiers PDF distincts. Lorsque la valeur est true, chaque page est téléchargée en tant que son propre fichier PDF. Lorsque la valeur est false, toutes les pages sont regroupées dans un seul fichier PDF.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Configuration</td> 
   <td>Si vous exportez un PDF, choisissez si vous souhaitez que le PDF soit en configuration d’impression ou standard.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Étape d’accessibilité</td> 
   <td>Si vous exportez un PDF standard, indiquez si vous souhaitez inclure des balises d’accessibilité dans le PDF.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Saigner</td> 
   <td>Si vous exportez un PDF d’impression, choisissez d’inclure ou non les paramètres de fond perdu dans l’exportation</td> 
  </tr>
  <tr> 
   <td role="rowheader">Paramètres de fond perdu &gt; Quantité</td> 
   <td>Entrez le montant de la marge de fond perdu.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Paramètres de fond perdu &gt; Unités</td> 
   <td>Indiquez si la valeur correspond aux pouces ou aux millimètres.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Recadrer</td> 
   <td>Si vous exportez un PDF d’impression, choisissez d’inclure ou non les paramètres de recadrage dans l’exportation</td> 
  </tr>
  <tr> 
   <td role="rowheader">Paramètres de recadrage &gt; Quantité</td> 
   <td>Entrez le montant de la marge de recadrage.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Paramètres de recadrage &gt; Unités</td> 
   <td>Indiquez si la valeur correspond aux pouces ou aux millimètres.</td> 
  </tr>
 </tbody> 
</table>

#### Générer des variations

Ce module crée une variation de document en fonction des paramètres d’entrée fournis. Après le traitement, il stocke temporairement le document généré et le met à la disposition de l’utilisateur dans un dossier désigné. Le document reste accessible pendant 30 jours, après quoi le système le supprime automatiquement.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Express, voir <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Création d’une connexion à Adobe Express</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Document</td> 
   <td>Sélectionnez le document pour lequel vous souhaitez générer des variations.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Numéros de page</td> 
   <td>Saisissez ou mappez les numéros de page à inclure dans le rendu. Chaîne de numéros de page séparés par des virgules pour laquelle la demande de variation est effectuée. Par exemple, « 1, 2, 3 ». Vous pouvez également spécifier des plages de pages. Par exemple, « 1-3 » inclut les pages 1, 2 et 3. Un autre exemple est « 1,3-5 », qui comprend les pages 1, 3, 4 et 5. « 1- » peut être utilisé pour spécifier toutes les pages, tandis que « 5- » indique la page 5 à la dernière page. Si elle n’est pas fournie, la première page est prise en compte par défaut. Les numéros de page commencent à partir de 1.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Nom du document préféré.</td> 
   <td>Saisissez ou mappez un nom pour le nouveau document. Si vous ne fournissez pas de nom ou si le nom est déjà utilisé, le système génère un nom unique.</td> 
  </tr>
  <tr> 
   <td role="rowheader">ID de projet</td> 
   <td>Saisissez l’ID du projet dans lequel les variations seront stockées.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Autres champs</td> 
   <td>Saisissez des valeurs pour d’autres champs. Les champs disponibles sont basés sur le document sélectionné.</td> 
  </tr>
 </tbody> 
</table>


### Recherches

#### Récupérer des documents balisés

Ce module récupère une liste de documents balisés, ainsi que les métadonnées pertinentes.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Express, voir <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Création d’une connexion à Adobe Express</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Démarrer l’index</td> 
   <td>Saisissez ou mappez l’index de début de pagination. Utilisez cette option lorsque vous avez récupéré une autre liste de résultats et que vous souhaitez continuer cette liste. L’index par défaut est 0.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Nombre maximal de résultats renvoyés</td> 
   <td>Saisissez ou mappez le nombre maximal de résultats que le module doit renvoyer pour chaque cycle d'exécution.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Trier par</td> 
   <td>Sélectionnez l’attribut en fonction duquel vous souhaitez trier les résultats.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Direction</td> 
   <td>Sélectionnez si vous souhaitez trier les résultats par ordre croissant ou décroissant.</td> 
  </tr>
 </tbody> 
</table>

#### Récupérer les détails du document

Ce module récupère les détails des pages et des éléments balisés dans un document spécifié. Elle renvoie une liste paginée des pages du document et des métadonnées sur chaque page. Si le document comporte des éléments balisés, l’API inclut leurs détails respectifs, tels que la taille et la position. Si le document ne comporte pas d’éléments balisés, il renvoie un tableau vide. La réponse inclut des informations de pagination pour aider les utilisateurs et utilisatrices à parcourir les pages du document. Un maximum de 10 pages peut être renvoyé en 1 cycle.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Express, voir <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Création d’une connexion à Adobe Express</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Document</td> 
   <td>Sélectionnez le document pour lequel vous souhaitez renvoyer des pages et des détails.</td> 
  </tr>
  <tr> 
   <td role="rowheader">Page de démarrage</td> 
   <td>Saisissez ou mappez le numéro de page de la première page dont les détails seront récupérés.</td>

#### Récupération du statut d’une tâche

Ce module récupère le statut d’une tâche à l’aide de son identifiant de tâche. Selon le type de tâche, la réponse peut inclure des détails spécifiques à la tâche.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à Adobe Express, voir <a href="#create-a-connection-to-adobe-express" class="MCXref xref" >Création d’une connexion à Adobe Express</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID du traitement</td> 
   <td>Saisissez ou mappez l’identifiant de la tâche pour laquelle vous souhaitez récupérer des détails.</td> 
  </tr>

