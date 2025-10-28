---
title: Modules Veeva Vault
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent Veeva Vault et les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
source-git-commit: 4f5a4cf8691e5bb47eec6f6b2842369c5c6fbad8
workflow-type: tm+mt
source-wordcount: '1516'
ht-degree: 16%

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

## Modules Veeva Vault et leurs champs

Lorsque vous configurez les modules Veeva Vault, Workfront Fusion affiche les champs répertoriés ci-dessous. D&#39;autres champs Veeva Vault peuvent également s&#39;afficher, selon des facteurs tels que votre niveau d&#39;accès dans l&#39;application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Document

* [Créer un seul document](#create-a-single-document)
* [Création de plusieurs documents](#create-multiple-documents)
* [Supprimer un seul document](#delete-a-single-document)
* [Exporter des documents](#export-documents)
* [Obtenir un seul document](#get-a-single-document)
* [Lancement de l’action utilisateur](#initiate-user-action)
* [Liste des documents](#list-documents)
* [Récupérer les résultats d’exportation du document](#retrieve-document-export-results)
* [Mettre à jour plusieurs documents](#update-multiple-documents)
* [Mettre à jour un seul document](#update-a-single-document)

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



#### Liste des objets

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


