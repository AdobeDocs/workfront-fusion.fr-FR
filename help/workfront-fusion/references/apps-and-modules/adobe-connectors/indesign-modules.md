---
filename: adobe-indesign-modules
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: apps-and-their-modules
title: Modules Adobe InDesign
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent Adobe InDesign et les connecter à plusieurs applications et services tiers.
author: Becky
source-git-commit: 30ddefa8519e6f2052308482137d0fa018676902
workflow-type: tm+mt
source-wordcount: '1693'
ht-degree: 21%

---


# Modules Adobe InDesign

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent Adobe InDesign et les connecter à plusieurs applications et services tiers.

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

Avant de pouvoir utiliser le connecteur Adobe InDesign, vous devez disposer d’un compte Adobe InDesign actif.

## Création d’une connexion à Adobe InDesign

Pour créer une connexion pour vos modules Adobe InDesign :

1. Dans n’importe quel module Adobe InDesign, cliquez sur **Ajouter** en regard de la zone Connexion .

1. Remplissez les champs suivants :

   <table style="table-layout:auto"> 
      <col>
      </col>
      <col>
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
          <td role="rowheader">ID client</td>
          <td>Saisissez votre identifiant client Adobe. Vous trouverez cette information dans la section Informations d’identification du Adobe Developer Console</td>
        </tr>
        <tr>
          <td role="rowheader">Clé secrète client</td>
          <td>Saisissez votre clé secrète client Adobe. Vous trouverez cette information dans la section Informations d’identification du Adobe Developer Console</td>
        </tr>
        <tr>
          <td role="rowheader">Identifiant IMS de l’organisation</td>
          <td>Saisissez votre ID d’organisation Adobe. Vous trouverez cette information dans la section Informations d’identification du Adobe Developer Console</td>
        </tr>
      </tbody>
    </table>
1. Cliquez sur **Continuer** pour enregistrer la connexion et revenir au module.

## Modules InDesign et leurs champs

Lorsque vous configurez les modules Adobe InDesign, Workfront Fusion affiche les champs répertoriés ci-dessous. Selon des facteurs tels que votre niveau d’accès dans l’application ou le service, d’autres champs Adobe InDesign peuvent s’afficher en plus de ceux-ci. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, consultez [Mappage d’informations d’un module à l’autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Bouton (bascule) de mappage](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Actions

* [Créer un rendu](#create-rendition)
* [Suppression d’un script personnalisé](#delete-a-custom-script)
* [Fusion des données](#merge-data)
* [Remapper les liens](#remap-links)
* [Envoi d’une demande d’exécution de script personnalisé](#submit-a-custom-script-execution-request)

#### Créer un rendu

Ce module d’action crée et renvoie un rendu JPEG, PNG ou PDF d’un document InDesign spécifique. Pour la structure des `StatusCompletedRespons/output/data`, reportez-vous à la section `RenditionOutputData`. Pour obtenir la liste des codes d’erreur possibles dans `FailedEvent`, reportez-vous également à la section `RenditionFailedData`.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe InDesign, voir <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Création d’une connexion à Adobe InDesign</a> dans cet article.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>Type</p>
      </td>
      <td>Sélectionnez le type de fichier du rendu à créer. 
      <ul><li>JPEG</li><li>PNG</li><li>PDF</li></ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Ressources</p>
      </td>
      <td>Pour chaque ressource à ajouter au rendu :<ol><li>Cliquez sur <b> Ajouter un élément </b>.</li><li>Sélectionnez ou mappez la source de la ressource.</li><li>Saisissez une destination. La destination est un chemin relatif à un répertoire de base temporaire (répertoire de travail) où la ressource est téléchargée. Cela identifie les ressources dans les paramètres. Il ne peut pas augmenter à l'aide de '..' ou '/'. Un nom de fichier valide doit exister.</td>
    </tr>
    <tr>
      <td role="rowheader">Document cible</td>
      <td>Saisissez ou mappez le document qui sera traité et rendu. Actuellement, un seul document à la fois est pris en charge.</td>
    </tr>
    <tr>
      <td role="rowheader">Autres champs</td>
   <td>Pour les autres champs, voir les informations incluses dans le module .</td>     </tr>
  </tbody>
</table>

#### Suppression d’un script personnalisé

Ce module d’action supprime un seul script personnalisé enregistré. Toutes les versions du script seront définitivement supprimées.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe InDesign, voir <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Création d’une connexion à Adobe InDesign</a> dans cet article.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>Nom du script</p>
      </td>
      <td>Saisissez ou mappez le nom du script que vous souhaitez supprimer.</td>
    </tr>
  </tbody>
</table>

#### Fusion des données

Ce module crée des documents ou des fichiers PDF InDesign en fusionnant les données CSV avec les modèles InDesign. Les formats de sortie comprennent les documents JPEG, PNG, PDF et InDesign.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe InDesign, voir <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Création d’une connexion à Adobe InDesign</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Ressources</p>
      </td>
      <td>Pour chaque ressource à ajouter à la fusion de données :<ol><li>Cliquez sur <b> Ajouter un élément </b>.</li><li>Sélectionnez ou mappez la source de la ressource.</li><li>Saisissez une destination. La destination est un chemin relatif à un répertoire de base temporaire (répertoire de travail) où la ressource est téléchargée. Cela identifie les ressources dans les paramètres. Il ne peut pas augmenter à l'aide de '..' ou '/'. Un nom de fichier valide doit exister.</td>
    </tr>
    <tr>
      <td role="rowheader">Document cible</td>
      <td>Saisissez ou mappez le document qui sera utilisé comme modèle pour la fusion.</td>
    </tr>
    <tr>
      <td role="rowheader">Source de données</td>
      <td>Saisissez ou mappez les fichiers sources à utiliser.</td>
    </tr>
    <tr>
      <td role="rowheader">Autres champs</td>
   <td>Pour les autres champs, voir les informations incluses dans le module .</td>     </tr>
  </tbody>
</table>

#### Remapper les liens

Ce module remplace les liens basés sur des fichiers dans les documents InDesign par des URL Adobe Experience Manager (AEM). Cela peut s’avérer utile pour travailler avec Adobe Experience Manager à l’aide d’Adobe Asset Link.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe InDesign, voir <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Création d’une connexion à Adobe InDesign</a> dans cet article.</td>
      </tr>
    <tr>
      <td role="rowheader">Jeton AEM</td>
      <td>Saisissez ou mappez le jeton porteur généré pour le compte technique AEM, sans le mot-clé porteur.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Ressources</p>
      </td>
      <td>Pour chaque ressource que vous souhaitez ajouter au module :<ol><li>Cliquez sur <b> Ajouter un élément </b>.</li><li>Sélectionnez ou mappez la source de la ressource.</li><li>Saisissez une destination. La destination est un chemin relatif à un répertoire de base temporaire (répertoire de travail) où la ressource est téléchargée. Cela identifie les ressources dans les paramètres. Il ne peut pas augmenter à l'aide de '..' ou '/'. Un nom de fichier valide doit exister.</td>
    </tr>
    <tr>
      <td role="rowheader">Document cible</td>
      <td>Saisissez ou mappez le document dans lequel vous souhaitez remapper les liens.</td>
    </tr>
    <tr>
      <td role="rowheader">Source de données</td>
      <td>Saisissez ou mappez les fichiers sources à utiliser pour extraire et faire correspondre les balises.</td>
    </tr>
    <tr>
      <td role="rowheader">Autres champs</td>
   <td>Pour les autres champs, voir les informations incluses dans le module .</td>     </tr>
  </tbody>
</table>

#### Envoi d’une demande d’exécution de script personnalisé

Ce module d’action envoie une demande d’exécution pour un script personnalisé. Vous définissez les ressources et paramètres d’entrée que le script personnalisé utilisera pendant l’exécution.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe InDesign, voir <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Création d’une connexion à Adobe InDesign</a> dans cet article.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>ID de script</p>
      </td>
      <td>Saisissez ou mappez l’identifiant du script personnalisé.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Ressources</p>
      </td>
      <td>Pour chaque ressource pour laquelle vous souhaitez envoyer une demande d’exécution, <ol><li>Cliquez sur <b> Ajouter un élément </b>.</li><li>Sélectionnez ou mappez la source de la ressource.</li><li>Saisissez une destination. La destination est un chemin relatif à un répertoire de base temporaire (répertoire de travail) où la ressource est téléchargée. Cela identifie les ressources dans les paramètres. Il ne peut pas augmenter à l'aide de '..' ou '/'. Un nom de fichier valide doit exister.</td>
    </tr>
    <tr>
      <td role="rowheader">Autres champs</td>
   <td>Pour les autres champs, voir les informations incluses dans le module .</td>     </tr>
  </tbody>
</table>

### Recherches

* [Obtenir les détails du script personnalisé](#get-custom-script-details)
* [Obtenir les balises de fusion des données](#get-data-merge-tags)
* [Obtenir des informations sur le document](#get-document-information)
* [Liste des scripts personnalisés](#list-custom-scripts)

#### Obtenir les détails du script personnalisé

Ce module de recherche récupère les détails d’un seul script personnalisé enregistré, y compris la version, le lien de téléchargement, la date d’enregistrement et le nom du script.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe InDesign, voir <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Création d’une connexion à Adobe InDesign</a> dans cet article.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>Nom du script</p>
      </td>
      <td>Saisissez ou mappez le nom du script pour lequel vous souhaitez récupérer des détails.</td>
    </tr>
  </tbody>
</table>

#### Obtenir les balises de fusion des données

Ce module récupère les balises de fusion des données d’un document.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe InDesign, voir <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Création d’une connexion à Adobe InDesign</a> dans cet article.</td>
      </tr>
    <tr>
      <td role="rowheader">
        <p>Ressources</p>
      </td>
      <td>Pour chaque ressource que vous souhaitez ajouter au module :<ol><li>Cliquez sur <b> Ajouter un élément </b>.</li><li>Sélectionnez ou mappez la source de la ressource.</li><li>Saisissez une destination. La destination est un chemin relatif à un répertoire de base temporaire (répertoire de travail) où la ressource est téléchargée. Cela identifie les ressources dans les paramètres. Il ne peut pas augmenter à l'aide de '..' ou '/'. Un nom de fichier valide doit exister.</td>
    </tr>
    <tr>
      <td role="rowheader">Document cible</td>
      <td>Saisissez ou mappez le document à partir duquel vous souhaitez récupérer les balises.</td>
    </tr>
    <tr>
      <td role="rowheader">Source de données</td>
      <td>Saisissez ou mappez les fichiers sources à utiliser pour extraire et faire correspondre les balises.</td>
    </tr>
    <tr>
      <td role="rowheader">Autres champs</td>
   <td>Pour les autres champs, voir les informations incluses dans le module .</td>     </tr>
  </tbody>
</table>

#### Obtenir des informations sur le document

Ce module récupère des informations complètes sur les documents INDD/IDML et renvoie des données en fonction des types d’informations activés spécifiés dans la requête.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe InDesign, voir <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Création d’une connexion à Adobe InDesign</a> dans cet article.</td>
      </tr>
    <tr>
      <td role="rowheader">
        <p>Ressources</p>
      </td>
      <td>Pour chaque ressource que vous souhaitez ajouter au module :<ol><li>Cliquez sur <b> Ajouter un élément </b>.</li><li>Sélectionnez ou mappez la source de la ressource.</li><li>Saisissez une destination. La destination est un chemin relatif à un répertoire de base temporaire (répertoire de travail) où la ressource est téléchargée. Cela identifie les ressources dans les paramètres. Il ne peut pas augmenter à l'aide de '..' ou '/'. Un nom de fichier valide doit exister.</td>
    </tr>
    <tr>
      <td role="rowheader">Document cible</td>
      <td>Saisissez ou mappez le document à partir duquel vous souhaitez récupérer des informations.</td>
    </tr>
     <tr>
      <td role="rowheader">Autres champs</td>
   <td>Pour les autres champs, voir les informations incluses dans le module .</td>     </tr>
  </tbody>
</table>

#### Liste des scripts personnalisés

Ce module récupère les détails de la dernière version de tous les scripts personnalisés enregistrés, y compris la version, le lien de téléchargement, la date d’enregistrement et le nom du script. Les résultats sont paginés en fonction de la longueur de la liste.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe InDesign, voir <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Création d’une connexion à Adobe InDesign</a> dans cet article.</td>
      </tr>
    <tr>
      <td role="rowheader">Numéro de page</td>
      <td>Saisissez ou mappez le numéro de page à partir duquel vous souhaitez commencer.</td>
    </tr>
  <tr> 
   <td>Nombre maximal de résultats renvoyés</td> 
   <td>Définissez le nombre maximal d’équipes ou de groupes que Workfront Fusion renverra au cours d’un cycle d’exécution.</td> 
  </tr> 
  </tbody>
</table>


### Autres

#### Effectuer un appel API personnalisé

Ce module effectue un appel API personnalisé à l’API Adobe InDesign

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à Adobe InDesign, voir <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">Création d’une connexion à Adobe InDesign</a> dans cet article.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>Chemin d’accès</p>
      </td>
      <td>
        <p>Saisir un chemin relatif à <code>https://indesign.adobe.io/v3</code>.</p><p> Exemple : <code>/create-rendition</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Méthode</p>
      </td>
      <td>
        <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir [méthodes de requête HTTP](/help/workfront-fusion/references/modules/http-request-methods.md).</p>
      </td>
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
      <td role="rowheader">Chaîne de requête  </td>
      <td>
        <p>Saisissez la chaîne de requête.</p>
      </td>
    </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lors de l’utilisation d’instructions conditionnelles telles que <code>if</code> dans votre fichier JSON, placez les guillemets en dehors de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  </tbody>
</table>
