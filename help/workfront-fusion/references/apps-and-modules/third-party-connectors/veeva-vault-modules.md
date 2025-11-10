---
title: Modules Veeva Vault
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent Veeva Vault et les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
source-git-commit: 4ba05a5f400ba1bdfb97586500baf741b555cd20
workflow-type: tm+mt
source-wordcount: '2325'
ht-degree: 14%

---

# Modules Veeva Vault

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent Veeva Vault et les connecter à plusieurs applications et services tiers.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <td role="rowheader">Licence Adobe Workfront Fusion</td> 
   <td>
   <p>Basé sur les opérations : aucune exigence de licence Workfront Fusion</p>
   <p>Basé sur un connecteur (hérité) : Workfront Fusion pour l’automatisation et l’intégration du travail </p>
   </td> 
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

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Conditions préalables

Pour utiliser les modules Veeva Vault, vous devez disposer d&#39;un compte Veeva Vault.

## Connecter Veeva Vault à Workfront Fusion

Vous pouvez créer une connexion à votre compte Veeva Vault directement depuis un module Veeva Vault.

1. Dans un module Veeva Vault, cliquez sur **Ajouter** en regard du champ Connexion .
1. Remplissez les champs suivants.

   <table style="table-layout:auto"> 
     <col> 
     <col> 
     <tbody> 
      <tr> 
       <td role="rowheader">Nom de la connexion</td> 
       <td> <p>Saisissez un nom pour la connexion.</p> </td> 
      </tr> 
      <tr>
        <td role="rowheader">Environnement</td>
        <td>
          <p>Indiquez si vous vous connectez à un environnement de production ou hors production.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Type</td>
        <td>
          <p>Indiquez si vous vous connectez à un compte de service ou à un compte personnel.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Nom d’utilisateur</td>
        <td>
          <p>Saisissez le nom d'utilisateur du compte Veeva Vault.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Mot de passe</td>
        <td>
          <p>Saisissez le mot de passe du compte Veeva Vault.</p>
        </td>
      </tr>
      <tr> 
       <td role="rowheader">DNS Vault</td> 
       <td>Saisissez votre DNS Veeva Vault (nom de domaine).</p><p>Pour localiser votre DNS Veeva Vault, examinez l'URL que vous utilisez pour accéder à Veeva Vault.</p>Par exemple, dans le <code>https://my-dns.veevavault.com</code> URL, le DNS est <code>my-dns</code>. Il n’est pas nécessaire de saisir l’URL complète.</td> 
      </tr> 
     </tbody> 
    </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour créer la connexion et retourner au module.



## Modules Veeva Vault et leurs champs

Lorsque vous configurez les modules Veeva Vault, Workfront Fusion affiche les champs répertoriés ci-dessous. D&#39;autres champs Veeva Vault peuvent également s&#39;afficher, selon des facteurs tels que votre niveau d&#39;accès dans l&#39;application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Document](#document)
* [Objet](#object)
* [Autre](#other)

### Document

* [Créer un seul document](#create-a-single-document)
* [Création de plusieurs documents](#create-multiple-documents)
* [Supprimer un seul document](#delete-a-single-document)
* [Télécharger un fichier](#download-file)
* [Exporter des documents](#export-documents)
* [Obtenir un seul document](#get-a-single-document)
* [Lancement de l’action utilisateur](#initiate-user-action)
* [Liste des documents](#list-documents)
* [Récupérer les résultats d’exportation du document](#retrieve-document-export-results)
* [Mettre à jour un seul document](#update-a-single-document)
* [Mettre à jour plusieurs documents](#update-multiple-documents)

#### Créer un seul document

Ce module crée un seul document, classeur ou modèle.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Veeva Vault à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Choisissez si vous souhaitez créer un document, un classeur ou un modèle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Sélectionner des champs</p> </td> 
   <td> <p>Sélectionnez les champs pour lesquels vous souhaitez saisir des données, puis saisissez les données dans ces champs.</td> 
  </tr> 
 </tbody> 
</table>

#### Création de plusieurs documents

Ce module crée plusieurs documents ou modèles à l’aide d’un fichier CSV.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Veeva Vault à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Choisissez de créer des modèles ou des documents</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Données de fichier</p> </td> 
   <td> <p>Mappez le fichier CSV qui sera utilisé pour créer les documents.</td> 
  </tr> 
 </tbody> 
</table>

#### Supprimer un seul document

Ce module supprime un seul document, classeur ou modèle.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Veeva Vault à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Choisissez si vous souhaitez supprimer un document, un classeur ou un modèle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>ID de document / ID de relieur / Nom du modèle</p> </td> 
   <td> <p>Sélectionnez les champs à supprimer.</td> 
  </tr> 
 </tbody> 
</table>

#### Télécharger le fichier

Ce module télécharge un document, une version de document ou un modèle de Veeva Vault.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Veeva Vault à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Choisissez si vous souhaitez télécharger un document ou un modèle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type de téléchargement</p> </td> 
   <td> <p>Choisissez si vous souhaitez télécharger un document ou une version de document.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>ID du document / Nom du modèle</p> </td> 
   <td> <p>Saisissez ou mappez l’identifiant du document ou le nom du modèle que vous souhaitez télécharger.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Extraire le document</p> </td> 
   <td> <p>Si vous téléchargez un document, activez cette option pour extraire le document avant de le télécharger.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Version</p> </td> 
   <td> <p>Si vous téléchargez une version de document, sélectionnez la version à télécharger.</td> 
  </tr> 
 </tbody> 
</table>

#### Exporter des documents

Ce module exporte les documents que vous spécifiez, y compris les sources, les rendus et le texte.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Veeva Vault à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Choisissez si vous souhaitez supprimer un document, un classeur ou un modèle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Source</p> </td> 
   <td> <p>Activez cette option pour inclure les fichiers sources dans l’exportation.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Rendus</p> </td> 
   <td> <p>Activez cette option pour inclure les fichiers de rendu dans l’exportation.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Toutes les versions</p> </td> 
   <td> <p>Activez cette option pour inclure toutes les versions des fichiers de document dans l’exportation.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Texte</p> </td> 
   <td> <p>Activez cette option pour inclure le texte du document source dans l’exportation.</p></td> 
  </tr> 
 </tbody> 
</table>

#### Obtenir un seul document

Ce module récupère les métadonnées d’un seul document, d’un seul classeur ou d’un seul modèle.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Veeva Vault à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Choisissez si vous souhaitez récupérer les données d’un document, d’un classeur ou d’un modèle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>ID de document / ID de relieur / Nom du modèle</p> </td> 
   <td> <p>Sélectionnez les champs pour lesquels vous souhaitez récupérer des données.</td> 
  </tr> 
 </tbody> 
</table>

#### Lancement de l’action utilisateur

Ce module lance des actions sur les documents et le classeur, comme l’envoi d’un document pour révision ou la modification de son état.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Veeva Vault à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Choisissez si vous souhaitez effectuer une action sur un document ou un classeur.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Document / Classeur</p> </td> 
   <td> <p>Sélectionnez le document ou le classeur sur lequel vous souhaitez effectuer l’action.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Version du document/Version du classeur</p> </td> 
   <td> <p>Sélectionnez le document ou le classeur sur lequel vous souhaitez effectuer l’action.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>Action</p> </td> 
   <td> <p>Sélectionnez l’action à effectuer sur le document ou le classeur.</td> 
  </tr> 
 </tbody> 
</table>

#### Liste des documents

Ce module répertorie tous les documents du type sélectionné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Veeva Vault à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Choisissez si vous souhaitez répertorier les documents, les classeurs ou les modèles.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nombre maximal de résultats renvoyés</td> 
   <td>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</td> 
  </tr> 
 </tbody> 
</table>

#### Récupérer les résultats d’exportation du document

Ce module renvoie les résultats d’une exportation de document précédemment demandée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Veeva Vault à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Identifiant du traitement</p> </td> 
   <td> <p>Saisissez ou mappez l’identifiant de la tâche pour laquelle vous souhaitez renvoyer des résultats. </p> </td> 
  </tr> 
  </tbody> 
</table>

#### Mettre à jour plusieurs documents

Ce module met à jour plusieurs documents ou modèles à l’aide d’un fichier CSV.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Veeva Vault à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Choisissez de créer des modèles ou des documents</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Données de fichier</p> </td> 
   <td> <p>Mappez le fichier CSV qui sera utilisé pour créer les documents.</td> 
  </tr> 
 </tbody> 
</table>

#### Mettre à jour un seul document

Ce module met à jour un seul document, classeur ou modèle.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Veeva Vault à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Choisissez si vous souhaitez créer un document, une version de document, un classeur ou un modèle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID/Nom</p> </td> 
   <td> <p>Si vous mettez à jour un modèle, saisissez un nouveau nom pour le modèle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Nom du nouveau modèle</p> </td> 
   <td> <p>Saisissez ou mappez l’identifiant ou le nom de l’objet que vous souhaitez mettre à jour.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">  <p>Sélectionner des champs</p> </td> 
   <td> <p>Sélectionnez les champs pour lesquels vous souhaitez saisir des données, puis saisissez les données dans ces champs.</td> 
  </tr> 
 </tbody> 
</table>

### Objet

* [Créer un enregistrement d’objet unique](#create-a-single-object-record)
* [Supprimer un seul enregistrement d’objet](#delete-a-single-object-record)
* [Obtenir un seul objet](#get-a-single-object)
* [Répertorier les enregistrements d’objets](#list-objects-records)
* [Mettre à jour un enregistrement d’objet unique](#update-a-single-object-record)

#### Créer un enregistrement d’objet unique

Ce module crée, copie ou copie en profondeur un enregistrement d’objet unique.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Veeva Vault à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Choisissez de créer ou de copier un enregistrement, ou de copier en profondeur un enregistrement.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Mode de migration</td> 
   <td>Si vous créez ou copiez un enregistrement, activez cette option pour créer ou mettre à jour des enregistrements d’objet dans un état non initial et avec une validation minimale, créer des enregistrements inactifs et définir des champs standard et gérés par le système tels que <code>createdby_v</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Aucun déclencheur</td> 
   <td>Si la valeur est définie sur true et que le mode de migration est activé, le module contourne tous les triggers SDK système, standard, personnalisés et d'action.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom de l'objet</td> 
   <td>Saisissez ou mappez la valeur du champ nom__v de l’objet, telle que <code>product__v</code>, <code>country__v</code> ou <code>custom_object__c</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de l’enregistrement</td> 
   <td>Si vous copiez en profondeur un enregistrement, sélectionnez l’enregistrement à copier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Champs d’enregistrement</td> 
   <td>Si vous copiez un enregistrement en profondeur, sélectionnez les champs pour lesquels vous souhaitez fournir des valeurs, puis fournissez ces valeurs.</td> 
  </tr> 
 </tbody> 
</table>

#### Supprimer un seul enregistrement d’objet

Ce module supprime ou supprime en cascade un seul enregistrement d&#39;objet. La suppression en cascade d&#39;un enregistrement supprime l&#39;enregistrement et tous ses objets enfants.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Veeva Vault à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Choisissez de supprimer un enregistrement ou de supprimer un enregistrement en cascade.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom de l'objet</td> 
   <td>Sélectionnez l’objet à supprimer.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de l’enregistrement</td> 
   <td>Sélectionnez l’identifiant de l’enregistrement à supprimer.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID externe</td> 
   <td>Au lieu de l’ID d’enregistrement, vous pouvez utiliser cet ID externe de document défini par l’utilisateur.</td> 
  </tr> 
 </tbody> 
</table>

#### Obtenir un seul objet

Ce module récupère les métadonnées configurées sur un enregistrement d’objet spécifique dans votre coffre.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Veeva Vault à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom de l'objet</td> 
   <td>Sélectionnez l’objet pour lequel vous souhaitez récupérer les métadonnées.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de l’enregistrement</td> 
   <td>Sélectionnez l’identifiant de l’enregistrement pour lequel vous souhaitez récupérer les métadonnées.</td> 
  </tr> 
 </tbody> 
</table>

#### Répertorier les enregistrements d’objets

Ce module récupère tous les objets Vault dans le coffre authentifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Veeva Vault à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Récupération des libellés localisés</p> </td> 
   <td> <p>Sélectionnez Oui pour récupérer les chaînes localisées (traduites) des champs d'objet label et label_plural.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nombre maximal de résultats renvoyés</td> 
   <td>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</td> 
  </tr> 
 </tbody> 
</table>

<!--#### Update a single object record-->

Ce module met à jour les champs d’un enregistrement d’objet existant.

Ce module crée, copie ou copie en profondeur un enregistrement d’objet unique.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Veeva Vault à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Choisissez de créer ou de copier un enregistrement, ou de copier en profondeur un enregistrement.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Mode de migration</td> 
   <td>Activez cette option pour créer ou mettre à jour des enregistrements d’objet dans un état non initial et avec une validation minimale, créer des enregistrements inactifs et définir des champs standard et gérés par le système tels que <code>createdby_v</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Aucun déclencheur</td> 
   <td>Si le mode de migration est activé, vous pouvez activer cette option pour contourner tous les triggers SDK système, standard, personnalisés et d’action.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom de l'objet</td> 
   <td>Saisissez ou mappez la valeur du champ nom__v de l’objet, telle que <code>product__v</code>, <code>country__v</code> ou <code>custom_object__c</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de l’enregistrement</td> 
   <td>Sélectionnez l’identifiant de l’enregistrement à mettre à jour.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Département</td> 
   <td>Spécifiez l’état du cycle de vie de l’enregistrement lorsque <code>X-VaultAPI-MigrationMode</code> est défini sur « true ».</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Libellé de l’état</td> 
   <td>Spécifiez le type d'état du cycle de vie de l'enregistrement lorsque <code>X-VaultAPI-MigrationMode</code> est défini sur true. Utilisez le format <code>base:object_lifecycle:</code> suivi du type d’état de l’objet .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Champs d’enregistrement</td> 
   <td>Si vous copiez un enregistrement en profondeur, sélectionnez les champs pour lesquels vous souhaitez fournir des valeurs, puis fournissez ces valeurs.</td> 
  </tr> 
 </tbody> 
</table>

### Autre

* [Effectuer un appel API personnalisé.](#make-a-custom-api-call)
* [Effectuer une requête SQL](#make-a-vql-query)
* [Lecture des journaux](#read-logs)

#### Effectuer un appel API personnalisé.

Ce module d&#39;action effectue un appel personnalisé à l&#39;API Veeva Vault.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Veeva Vault à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Saisissez un chemin d’accès relatif à <code>baseurl/api/v</code>.  Par exemple : <code>/objects/documents</code>. N’incluez pas le <code>baseurl/api/v/</code>, car il est déjà inclus.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Méthode</td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">En-têtes</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion ajoute les en-têtes d’autorisation pour vous.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Chaîne de requête</td> 
   <td> <p>Ajoutez la requête pour l’appel API sous la forme d’un objet JSON standard.</p> <p>Par exemple : <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Corps</td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre JSON, placez les guillemets à l’extérieur de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Effectuer une requête SQL

Ce module effectue une requête à l’aide de Vault Query Language (VQL).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Veeva Vault à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type</p> </td> 
   <td> <p>Choisissez de créer des modèles ou des documents</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>Données de fichier</p> </td> 
   <td> <p>Mappez le fichier CSV qui sera utilisé pour créer les documents.</td> 
  </tr> 
 </tbody> 
</table>

#### Lecture des journaux

Ce module renvoie les données des journaux d’audit

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Veeva Vault à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Type d’audit</p> </td> 
   <td> <p>Sélectionnez le type d’audit pour lequel vous souhaitez récupérer les données.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Date de début</p> </td> 
   <td> <p>Saisissez ou mappez la date de début pour les audits que vous souhaitez récupérer.</p><p>Pour obtenir la liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercition</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Date de fin</p> </td> 
   <td> <p>Saisissez ou mappez la date de fin des audits que vous souhaitez récupérer.</p><p>Pour obtenir la liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercition</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>URL du résultat </p> </td> 
   <td> <p>Sélectionnez CSV si vous souhaitez obtenir une URL pour télécharger un CSV du résultat.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nombre maximal de résultats renvoyés</td> 
   <td>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</td> 
  </tr> 
 </tbody> 
</table>


