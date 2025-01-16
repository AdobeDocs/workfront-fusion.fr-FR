---
title: Modules Adobe Journey Optimizer
description: Dans un scénario  [!DNL Adobe Workfront Fusion] , vous pouvez automatiser les workflows qui utilisent  [!DNL Adobe Journey Optimizer] et le connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: 1d0ccf4d-9f06-4210-86ec-7da7970f6a47
source-git-commit: 3ba5d67806e0d495bd4a91589d06cfb9adb25c0c
workflow-type: tm+mt
source-wordcount: '3276'
ht-degree: 26%

---

# Modules [!DNL Adobe Journey Optimizer]

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!DNL Adobe Journey Optimizer] et le connecter à plusieurs applications et services tiers. Les modules [!DNL Adobe Journey Optimizer] vous permettent de créer, lire, mettre à jour ou supprimer des enregistrements, ou d’effectuer un appel API personnalisé à l’API [!DNL Adobe Journey Optimizer].


Si vous avez besoin d’instructions pour créer un scénario, consultez les articles sous [Créer un scénario : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] formule*</td>
      <td>
        <p>[!UICONTROL Pro] ou une version ultérieure</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] licence*</td>
      <td>
        <p>[!UICONTROL Plan], [!UICONTROL Work]</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront Fusion] licence**</td>
      <td>
   <p>Exigences de licence actuelles : aucune exigence de licence [!DNL Workfront Fusion] requise.</p>
   <p>Ou</p>
   <p>Ancienne exigence de licence : [!UICONTROL [!DNL Workfront Fusion] pour l’automatisation et l’intégration du travail] </p>
   </td>
    </tr>
    <tr>
      <td role="rowheader">Produit</td>
      <td>
   <p>Exigences actuelles du produit : si vous disposez du plan de [!DNL Adobe Workfront] [!UICONTROL Select] ou [!UICONTROL Prime], votre entreprise doit acheter du [!DNL Adobe Workfront Fusion] et [!DNL Adobe Workfront] utiliser les fonctionnalités décrites dans cet article. [!DNL Workfront Fusion] est inclus dans le plan de [!DNL Workfront] [!UICONTROL Ultimate].</p>
   <p>Ou</p>
   <p>Exigences liées aux produits hérités : votre entreprise doit acheter [!DNL Adobe Workfront Fusion] ainsi qu’[!DNL Adobe Workfront] pour utiliser la fonctionnalité décrite dans cet article.</p>
   </td>
    </tr>
  </tbody>
</table>


Pour connaître la formule, le type de licence ou l’accès dont vous disposez, contactez votre équipe d’administration [!DNL Workfront].

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Conditions préalables

Avant d’utiliser le connecteur [!DNL Adobe Journey Optimizer], vous devez vous assurer que les conditions préalables suivantes sont remplies :

* Vous devez disposer d’un compte [!DNL Adobe Journey Optimizer].

## Informations sur l’API Adobe Journey Optimizer

Le connecteur Adobe Journey Optimizer utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td>{{connection.url}}</td> 
  </tr>
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.7.11</td> 
  </tr>
 </tbody> 
 </table>

## Création d’une connexion à Adobe Journey Optimizer

Vous pouvez créer une connexion dans n’importe quel module Adobe Journey Optimizer.

1. Cliquez sur **[!UICONTROL Add]** en regard de la zone Connexion .

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
        <td>Indiquez si vous vous connectez à un compte de service ou à un compte personnel.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Saisissez votre [!UICONTROL Client ID] de [!UICONTROL Adobe]. Pour plus d’informations, consultez la section [!UICONTROL Credentials] les détails du [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Saisissez votre [!UICONTROL Client Secret] de [!DNL Adobe]. Pour plus d’informations, consultez la section [!UICONTROL Credentials] les détails du [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Organization ID]</td>
        <td>Saisissez votre [!UICONTROL Organization ID] de [!DNL Adobe]. Pour plus d’informations, consultez la section [!UICONTROL Credentials] les détails du [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Sandbox Name]</td>
        <td>Saisissez le nom du sandbox que cette connexion utilisera.</td>
        </tr>
      </tbody>
    </table>



   <!--Markdown 0032 placeholder-->


## Modules [!DNL Adobe Journey Optimizer] et leurs champs

Lorsque vous configurez les modules [!DNL Adobe Journey Optimizer], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Adobe Journey Optimizer] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Gestion de la configuration](#configuration-management)
* [Gestion des packages](#package-management)
* [Gestion des enregistrements](#record-management)
* [Gestion des messages](#message-management)
* [Contrôles de statut](#status-checks)
* [Recherches](#searches)
* [Autre](#other)




### Gestion de la configuration

* [Création d’une configuration](#create-a-configuration)
* [Déploiement d’une configuration](#deploy-a-configuration)
* [Mise à jour d’une configuration](#update-a-configuration)
* [Annulation du déploiement d’une configuration](#undeploy-a-configuration)
* [Vérifier si la configuration peut être déployée](#check-if-configuration-can-be-deployed)
* [Suppression d’une configuration](#delete-a-configuration)
* [Obtenir une configuration](#get-a-configuration)

#### Création d’une configuration

Ce module d’action crée une configuration de plafonnement ou de limitation.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select configuration type]</td> 
   <td>Choisissez si vous créez une configuration de plafonnement ou de limitation.<ul><li><p><b>Limitation</b></p>Passez à <a href="#capping-fields" class="MCXref xref" >Champs de limitation</a>.</li><li><p><b>Limitation</b></p>Passez à <a href="#throttling-fields" class="MCXref xref" >Champs de limitation</a>.</li></ul></td> 
  </tr> 
   </tbody> 
</table>

##### Champs de limitation

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Saisissez ou mappez l’URL du point d’entrée que vous souhaitez configurer.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL IMS Org ID]</td> 
   <td>Saisissez ou mappez l’ID Adobe IMS de l’organisation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Methods]</td> 
   <td>Sélectionnez les méthodes à utiliser dans cette configuration.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Service]</td> 
   <td>Indiquez si vous utilisez une action ou une source de données pour cette configuration.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum HTTP connections]</td> 
   <td>Saisissez ou mappez le nombre maximal de connexions simultanées à ce point d’entrée.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum calls]</td> 
   <td>Saisissez ou mappez le nombre maximal d’appels à effectuer au cours de la période spécifiée dans le champ Période.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Time period (milliseconds)]</td> 
   <td>Saisissez ou mappez le nombre de millisecondes associé au champ Nombre maximal d’appels .</td> 
  </tr> 
 </tbody> 
</table>

##### Champs de limitation

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Saisissez ou mappez un nom pour cette configuration.</td> 
<tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Saisissez ou mappez une description pour cette configuration.</td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL URL pattern]</td> 
   <td>Saisissez ou mappez l’URL du point d’entrée que vous souhaitez ralentir.</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Methods]</td> 
   <td>Sélectionnez les méthodes à utiliser dans cette configuration.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Max throughput]</td> 
   <td>Indiquez si vous utilisez une action ou une source de données pour cette configuration.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum HTTP connections]</td> 
   <td>Saisissez ou mappez le nombre maximal de connexions simultanées à ce point d’entrée.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum calls]</td> 
   <td>Saisissez ou mappez le débit maximal souhaité pour ce point d’entrée. Cette valeur doit être comprise entre 200 et 5 000.</td> 
  </tr> 
 </tbody> 
</table>

#### Déploiement d’une configuration

Ce module d’action déploie la configuration de plafonnement ou de limitation spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select configuration type]</td> 
   <td>Choisissez si vous déployez une configuration de plafonnement ou de limitation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Configuration ID]</td> 
   <td>Saisissez ou mappez l’identifiant de la configuration que vous souhaitez déployer.</td> 
  </tr> 
 </tbody> 
</table>

#### Mise à jour d’une configuration

Ce module d’action met à jour la configuration de plafonnement ou de limitation spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select configuration type]</td> 
   <td>Indiquez si vous mettez à jour une configuration de plafonnement ou de limitation.<ul><li><p><b>Limitation</b></p>Pour les champs, reportez-vous à la section <a href="#capping-fields" class="MCXref xref" >Limitation des champs</a> dans la section Créer une configuration de cet article.</li><li><p><b>Limitation</b></p>Pour les champs, reportez-vous à la section <a href="#throttling-fields" class="MCXref xref" >Limitation des champs</a> dans la section Créer une configuration de cet article.</li></ul></td> 
  </tr> 
  </tbody> 
</table>

#### Annulation du déploiement d’une configuration

Ce module d’action annule le déploiement d’une configuration de plafonnement ou de limitation. Le statut de configuration est rétabli au statut précédant le déploiement (`created` ou `updated`).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select configuration type]</td> 
   <td>Indiquez si vous annulez le déploiement d’une configuration de plafonnement ou de limitation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Configuration ID]</td> 
   <td>Saisissez ou mappez l’identifiant de la configuration que vous souhaitez annuler le déploiement.</td> 
  </tr> 
 </tbody> 
</table>

#### Vérifier si la configuration peut être déployée

Ce module d’action vérifie si une configuration de plafonnement ou de limitation peut être déployée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select configuration type]</td> 
   <td>Indiquez si vous vérifiez une configuration de plafonnement ou de limitation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Configuration ID]</td> 
   <td>Saisissez ou mappez l’identifiant de la configuration que vous souhaitez vérifier.</td> 
  </tr> 
 </tbody> 
</table>

#### Suppression d’une configuration

Ce module d’action supprime une configuration de plafonnement ou de limitation.

Si la configuration a été déployée, elle doit être annulée avant de pouvoir être supprimée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select configuration type]</td> 
   <td>Indiquez si vous supprimez une configuration de plafonnement ou de limitation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Configuration ID]</td> 
   <td>Saisissez ou mappez l’identifiant de la configuration à supprimer.</td> 
  </tr> 
 </tbody> 
</table>

#### Obtenir une configuration

Ce module d’action renvoie la configuration de plafonnement ou de limitation identifiée par l’identifiant spécifié. La dernière définition est renvoyée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select configuration type]</td> 
   <td>Indiquez si vous récupérez une configuration de plafonnement ou de limitation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Configuration ID]</td> 
   <td>Saisissez ou mappez l’identifiant de la configuration que vous souhaitez récupérer.</td> 
  </tr> 
 </tbody> 
</table>




### Gestion des packages

* [Créer un package](#create-a-package)
* [Mise à jour d’un package](#update-a-package)
* [Supprimer un package](#delete-a-package)
* [Recherche d’un package](#look-up-a-package)
* [Importer un package](#import-a-package)
* [Publish d’un package](#publish-a-package)
* [Soumettre un import](#submit-an-import)



#### Créer un package

Ce module d’action crée un package multi-artefacts.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Saisissez ou mappez un nom pour le package.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Saisissez ou mappez une description du package.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expiration date]</td> 
   <td>Saisissez ou mappez la date et l’heure qui définissent la date d’expiration du package. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package type]</td> 
   <td>Sélectionnez le type de package que vous souhaitez créer.<ul><li><p><b>Plein</b></p>Le package inclut tous les artefacts</p></li><li><p><b>Partiel</b></p><p>Le package inclut uniquement les artefacts que vous ajoutez. </p></li><ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Artifacts]</td> 
   <td>Si vous créez un package partiel, pour chaque artefact que vous souhaitez ajouter, cliquez sur <b>Ajouter un artefact</b> et spécifiez l’identifiant, le type et le titre de l’artefact. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Sandbox]</td> 
   <td>Saisissez ou mappez le nom et l’ID d’organisation IMS du sandbox qui contient les éléments que vous souhaitez que le package contienne.</td> 
  </tr> 
 </tbody> 
</table>

#### Mise à jour d’un package

Ce module d’action ajoute ou supprime des artefacts d’un package ou met à jour les métadonnées du package.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select action]</td> 
   <td>Sélectionnez l’action à effectuer.<ul><li><p><b>Ajouter un artefact</b></p><p>Pour chaque artefact que vous souhaitez ajouter, cliquez sur <b>Ajouter un artefact</b> et indiquez l’identifiant, le type et le titre de l’artefact, puis saisissez ou mappez la date d’expiration du package. </p></li><li><p><b>Supprimer l’artefact</b></p><p>Pour chaque artefact à supprimer, cliquez sur <b>Ajouter un artefact</b> et indiquez l’identifiant, le type et le titre de l’artefact. </p></li><li><p><b>Mettre à jour les métadonnées</b></p><p>Saisissez de nouvelles valeurs pour le nom, la description, le nom du sandbox source ou l’ID d’organisation IMS.</p></li></ul></td> 
  </tr> 
 </tbody> 
</table>

#### Supprimer un package

Ce module d’action supprime un package multi-artefacts.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package ID]</td> 
   <td>Saisissez ou mappez l’identifiant du package que vous souhaitez supprimer.</td> 
  </tr> 
 </tbody> 
</table>

#### Recherche d’un package

Ce module d’action récupère les détails du package spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package ID]</td> 
   <td>Saisissez ou mappez l’identifiant du package pour lequel vous souhaitez renvoyer des détails.</td> 
  </tr> 
 </tbody> 
</table>

#### Importer un package

Ce module d’action récupère les objets en conflit dans le sandbox cible spécifié. Les objets en conflit représentent des objets similaires déjà présents dans le sandbox cible.

Vous devez publier un package avant de pouvoir l’importer.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package ID]</td> 
   <td>Saisissez ou mappez l’identifiant du package que vous souhaitez importer.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Target sandbox]</td> 
   <td>Saisissez ou mappez le nom du sandbox dans lequel vous souhaitez importer le package.</td> 
  </tr> 
 </tbody> 
</table>

#### Publish d’un package

Vous devez publier un package avant de pouvoir l’importer.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package ID]</td> 
   <td>Saisissez ou mappez l’identifiant du package que vous souhaitez publier.</td> 
  </tr> 
 </tbody> 
</table>

#### Soumettre un import

Ce module d&#39;action envoie un import pour un package après avoir vérifié les conflits et fourni les substitutions. Le résultat est fourni sous la forme d’une payload, qui démarre la tâche d’importation pour le sandbox de destination, comme indiqué dans la payload.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package ID]</td> 
   <td>Saisissez ou mappez l’identifiant du package que vous souhaitez publier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Saisissez ou mappez un nom pour la tâche d’importation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Saisir ou mapper une description de la tâche d’importation</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (Destination sandbox) Name]</td> 
   <td>Saisissez ou mappez le nom du sandbox auquel vous envoyez l’importation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (Destination sandbox) IMS Org ID]</td> 
   <td>Saisissez ou mappez l’ID d’organisation Adobe IMS pour le sandbox auquel vous envoyez l’importation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (Source sandbox) ID]</td> 
   <td>Saisissez ou mappez l’identifiant du sandbox qui contient le package que vous souhaitez publier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (Source sandbox) Type]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (Source sandbox) Link]</td> 
   <td>Saisissez ou mappez le lien pour le package que vous souhaitez publier.</td> 
  </tr> 
 </tbody> 
</table>


<!--

### Artifact management

* [Copy artifacts synchronously](#copy-artifacts-synchronously)
* [Export artifacts asynchronously](#export-artifacts-asynchronously)
* [Import artifacts asynchronously](#import-artifacts-asynchronously)

#### Copy artifacts synchronously

This action module copies artifacts from a source sandbox into a destination sandbox.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Journey Optimizer], see <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Create a connection to [!DNL Adobe Journey Optimizer]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Enter or map a name for the new file</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Enter or map a description for the new file</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination sandbox]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Artifacts]</td> 
   <td>For each artifact you want to copy, click <b>Add artifact</b> and continue to <a href="#artifact-fields" class="MCXref xref" >Artifact fields</a>.</td> 
  </tr> 
 </tbody> 
</table>

##### Artifact fields

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Enter or map the ID of the artifact.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Enter or map the artifact type, such as <code>REGISTRY_SCHEMA<code> or <code>JOURNEY</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Version]</td> 
   <td>Enter or map the visibility of the artifact. This applies only to Registry objects.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td>Enter or map the visibility (tenant or global). This applies only to Registry objects.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Found]</td> 
   <td>Select <b>Yes</b> if this item was found using a GET operation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tasks]</td> 
   <td>For each task you want to add, click <b>Add task</b> and fill in the following:
   <ul>
   <li><p><b>Method</b></p></li>
   <li><p><b>Action</b></p></li>
   <li><p><b>Using</b></p></li>
   <li><p><b>With</b></p></li>
   </ul>
   </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Messages]</td> 
   <td>For each task you want to add, click <b>Add message</b> and fill in the following:
   <ul>
   <li><p><b>Status</b></p><p>Enter or map the status that this message represents, such as <code>ERROR</code>.</li>
   <li><p><b>Attempt</b></p><p>Enter or map the attempt number related to this message. This may be useful if different attempts produce different messages.</p></li>
   <li><p><b>Message</b></p><p>Enter or map the text of the message.</li>
   <li><p><b>Object</b></p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

#### Export Artifacts asynchronously

This action module exports artifacts from the specified sandbox.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Journey Optimizer], see <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Create a connection to [!DNL Adobe Journey Optimizer]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Enter or map a name for the export file</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Enter or map a description for the export file</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Artifacts]</td> 
   <td>For each artifact you want to export, click <b>Add artifact</b> and continue to <a href="#artifact-fields" class="MCXref xref" >Artifact fields</a>.</td> 
  </tr> 
 </tbody> 
</table>

##### Artifact fields

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Enter or map the ID of the artifact.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Enter or map the artifact type, such as <code>REGISTRY_SCHEMA<code> or <code>JOURNEY</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Version]</td> 
   <td>Enter or map the visibility of the artifact. This applies only to Registry objects.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td>Enter or map the visibility (tenant or global). This applies only to Registry objects.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Found]</td> 
   <td>Select <b>Yes</b> if this item was found using a GET operation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tasks]</td> 
   <td>For each task you want to add, click <b>Add task</b> and fill in the following:
   <ul>
   <li><p><b>Method</b></p></li>
   <li><p><b>Action</b></p></li>
   <li><p><b>Using</b></p></li>
   <li><p><b>With</b></p></li>
   </ul>
   </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Messages]</td> 
   <td>For each task you want to add, click <b>Add message</b> and fill in the following:
   <ul>
   <li><p><b>Status</b></p><p>Enter or map the status that this message represents, such as <code>ERROR</code>.</li>
   <li><p><b>Attempt</b></p><p>Enter or map the attempt number related to this message. This may be useful if different attempts produce different messages.</p></li>
   <li><p><b>Message</b></p><p>Enter or map the text of the message.</li>
   <li><p><b>Object</b></p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



#### Import Artifacts asynchronously

This action module imports a snapshot containing artifacts.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Journey Optimizer], see <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Create a connection to [!DNL Adobe Journey Optimizer]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Snapshot ID]</td> 
   <td>Enter or map the ID of the snapshot you want to import.</td> 
  </tr> 
 </tbody> 
</table>

-->

### Gestion des enregistrements

* [Créer un enregistrement](#create-a-record)
* [Mettre à jour un enregistrement](#update-a-record)
* [Supprimer un enregistrement](#delete-a-record)
* [Correctif d’un enregistrement](#patch-a-record)
* [Obtenir un enregistrement](#get-a-record)

#### Créer un enregistrement

Ce module d’action crée un modèle de contenu ou un fragment de contenu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select content type]</td> 
   <td>Choisissez si vous créez un modèle de contenu ou un fragment de contenu.<ul><li><p><b>Modèle de contenu</b></p>Passez à <a href="#template-fields" class="MCXref xref" >Champs de modèle</a>.</li><li><p><b>Fragment de contenu</b></p>Passez à <a href="#fragment-fields" class="MCXref xref" >Champs de fragment</a>.</li></ul></td> 
  </tr> 
  </tbody> 
</table>

##### Champs de modèle

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Saisissez ou mappez un nom pour ce modèle de contenu.</td> 
<tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Saisissez ou mappez une description pour ce modèle de contenu.</td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Sélectionnez le type de modèle que vous souhaitez créer.</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channels]</td> 
   <td>Sélectionnez les canaux inclus dans ce modèle.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content template origin]</td> 
   <td>Sélectionnez la source de ce modèle.</td>  
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata]</td> 
   <td>Pour inclure des propriétés personnalisées dans le nouveau modèle, sélectionnez « Ajouter des métadonnées » et saisissez ou mappez la clé et la valeur des métadonnées. Répétez l’opération pour chaque champ personnalisé à inclure.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email HTML]</td> 
   <td>Saisissez ou mappez l’HTML de l’e-mail inclus dans ce modèle.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Editor context]</td> 
   <td>Pour inclure des propriétés personnalisées dans l’e-mail, sélectionnez « Ajouter le contexte de l’éditeur » et saisissez ou mappez la clé et la valeur du contexte. Répétez l’opération pour chaque champ personnalisé à inclure.</td> 
  </tr> 
 </tbody> 
</table>

##### Champs de fragment

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Saisissez ou mappez un nom pour ce fragment de contenu.</td> 
<tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Saisissez ou mappez une description pour ce fragment de contenu.</td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Sélectionnez le type de modèle que vous souhaitez créer.</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channels]</td> 
   <td>Sélectionnez les canaux inclus dans ce modèle.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content fragment origin]</td> 
   <td>Sélectionnez la source de ce fragment.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata]</td> 
   <td>Pour inclure des propriétés personnalisées dans le nouveau modèle, sélectionnez « Ajouter des métadonnées » et saisissez ou mappez la clé et la valeur des métadonnées. Répétez l’opération pour chaque champ personnalisé à inclure.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content]</td> 
   <td>Saisissez ou mappez le contenu du fragment.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Editor context]</td> 
   <td>Pour inclure des propriétés personnalisées dans l’e-mail, sélectionnez « Ajouter le contexte de l’éditeur » et saisissez ou mappez la clé et la valeur du contexte. Répétez l’opération pour chaque champ personnalisé à inclure.</td> 
  </tr> 
 </tbody> 
</table>

#### Mettre à jour un enregistrement

Ce module d’action met à jour un modèle ou un fragment de contenu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select content type]</td> 
   <td>Indiquez si vous mettez à jour une configuration de plafonnement ou de limitation.<ul><li><p><b>Modèle</b></p>Pour les champs, voir <a href="#template-fields" class="MCXref xref" >Champs de modèle</a> dans la section Créer un enregistrement de cet article.</li><li><p><b>Fragment</b></p>Pour les champs, reportez-vous à la section <a href="#fragment-fields" class="MCXref xref" >Champs de fragment</a> de la section Créer un enregistrement de cet article.</li></ul></td> 
  </tr> 
  </tbody> 
  </table>

#### Supprimer un enregistrement

Ce module d’action supprime un modèle ou un fragment de contenu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select content type]</td> 
   <td>Choisissez si vous supprimez un modèle de contenu ou un fragment de contenu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Template/Fragment ID]</td> 
   <td>Saisissez ou mappez l’identifiant du modèle ou du fragment à supprimer.</td> 
  </tr> 
 </tbody> 
</table>

#### Correctif d’un enregistrement

Ce module d’action met à jour un enregistrement à l’aide du PATCH au format du pointeur JSON

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select content type]</td> 
   <td>Indiquez si vous appliquez un correctif à un modèle de contenu ou à un fragment de contenu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Template/Fragment ID]</td> 
   <td>Saisissez ou mappez l’identifiant du modèle ou du fragment à corriger.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Payload data]</td> 
   <td>Pour ajouter un enregistrement à la payload de ce correctif : <ol><li>Cliquez sur <b> Ajouter un enregistrement </b>.</li><li>Sélectionnez l’opération : Ajouter, Supprimer ou Remplacer.</li><li>Dans le champ Chemin d’accès , indiquez si vous souhaitez appliquer un correctif au nom ou à la description.</li><li> Dans le champ De, saisissez ou mappez une chaîne contenant une valeur de pointeur JSON.</li><li>Dans le champ Valeur , saisissez la valeur à utiliser dans l’opération.</li></ol></td> 
  </tr> 
 </tbody> 
</table>

#### Obtenir un enregistrement

Ce module d’action renvoie le modèle de contenu ou le fragment de contenu identifié par l’identifiant spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select content type]</td> 
   <td>Choisissez si vous récupérez un modèle de contenu ou un fragment de contenu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Template/Fragment ID]</td> 
   <td>Saisissez ou mappez l’identifiant du modèle ou du fragment que vous souhaitez récupérer.</td> 
  </tr> 
 </tbody> 
</table>


### Gestion des messages

* [Déclencher l’exécution unitaire d’un message](#trigger-a-unitary-message-execution)
* [Déclencher un message basé sur une audience](#trigger-an-audience-based-message)
* [Vérifier le statut d’un message basé sur une audience](#check-the-status-for-audience-based-message)



#### Déclencher l’exécution unitaire d’un message

Ce module d&#39;action déclenche un message unitaire aux destinataires que vous spécifiez.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Request ID]</td> 
   <td>Saisissez ou mappez l’identifiant de la demande associée à ce message.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campaign ID]</td> 
   <td>Saisissez ou mappez l’identifiant de la campagne associée à ce message.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Recipients]</td> 
   <td>Pour chaque destinataire à qui vous souhaitez envoyer ce message, cliquez sur <b>Ajouter un destinataire</b> et saisissez les informations suivantes :
   <ul>
   <li><p><b>Type</b></p>Sélectionnez <code>aep</code>.</li>
   <li><p><b>Identifiant utilisateur</b></p>Saisissez ou mappez l’identifiant de profil Adobe Experience Platform du destinataire.</li>
   <li><p><b>Espace de noms</b></p>Saisissez ou mappez l’espace de noms du profil Adobe Experience Platform du destinataire.</li>
   <li><p><b>Adresse e-mail</b></p></li>
   <li><p><b>Numéro de téléphone mobile</b></p></li>
   <li><p><b>Prénom</b></p></li>
   <li><p><b>Nom</b></p></li>
   <li><p><b>Produit</b></p>Saisissez ou mappez le produit associé à ce message. Il est utilisé pour la substitution dynamique de variables dans le contenu du message.</li>
   </ul></td> 
  </tr> 
 </tbody> 
</table>

#### Déclencher un message basé sur une audience

Ce module d’action déclenche l’exécution d’un message basé sur une audience, en fonction de la requête et de la campagne que vous spécifiez.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Request ID]</td> 
   <td>Saisissez ou mappez l’identifiant de la demande associée à ce message.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campaign ID]</td> 
   <td>Saisissez ou mappez l’identifiant de la campagne associée à ce message.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Product]</td> 
   <td>Saisissez ou mappez le produit associé à ce message. Il est utilisé pour la substitution dynamique de variables dans le contenu du message.</td> 
  </tr> 
 </tbody> 
</table>

#### Vérifier le statut des messages basés sur une audience

Ce module d’action vérifie l’état d’un message par lots basé sur une audience.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message execution ID]</td> 
   <td>Saisissez ou mappez l’identifiant de l’exécution du message que vous souhaitez vérifier.</td> 
  </tr> 
 </tbody> 
</table>

### Contrôles de statut

<!--* [Check service health](#check-service-health)-->
* [Vérifier les dépendances d’import](#check-the-import-dependencies)
* [Vérification du statut d’une tâche d’importation](#check-the-status-of-an-import-job)

<!--

#### Check service health

This action module checks that the service represented by the connection is running.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Journey Optimizer], see <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Create a connection to [!DNL Adobe Journey Optimizer]</a> in this article.</td> 
  </tr> 
 </tbody> 
</table>

-->

#### Vérifier les dépendances d’import

Ce module d’action vérifie les dépendances pour les artefacts de package. Vous pouvez ainsi vérifier si vous disposez des autorisations nécessaires pour importer des artefacts de package.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package ID]</td> 
   <td>Saisissez ou mappez l’identifiant du package pour lequel vous souhaitez vérifier les autorisations.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Target sandbox]</td> 
   <td>Saisissez ou mappez le nom du sandbox dans lequel vous souhaitez importer le package.</td> 
  </tr> 
 </tbody> 
</table>

#### Vérification du statut d’une tâche d’importation

Ce module d’action vérifie si une tâche d’importation a réussi ou échoué.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Job ID]</td> 
   <td>Saisissez ou mappez l’identifiant de la tâche pour laquelle vous souhaitez récupérer des données.</td> 
  </tr> 
 </tbody> 
</table>

### Recherches

* [Répertorier tous les objets dépendants](#list-all-dependent-objects)
* [Configurations de liste](#list-configurations)
* [Liste des traitements d’export et d’import](#list-export-and-import-jobs)
* [Liste des packages](#list-packages)
* [Répertorier les enregistrements](#list-records)

#### Répertorier tous les objets dépendants

Ce module de recherche répertorie tous les objets dépendants pour les objets du package spécifié

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package objects]</td> 
   <td>Pour chaque objet du package pour lequel vous souhaitez renvoyer un objet dépendant, cliquez sur <b>Ajouter un objet</b> et saisissez le nom et le type de l’objet.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package ID]</td> 
   <td>Saisissez ou mappez l’identifiant du package pour lequel vous souhaitez répertorier les objets dépendants.</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Target sandbox]</td> 
   <td>Saisissez ou mappez le nom du sandbox qui contient le package pour lequel vous souhaitez répertorier les objets dépendants.</td> 
  </tr> 
 </tbody> 
</table>

#### Configurations de liste

Ce module d’action répertorie toutes les configurations de plafonnement ou de limitation.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select configuration type]</td> 
   <td>Choisissez si vous souhaitez répertorier les configurations de plafonnement ou de limitation.</td> 
  </tr> 
 </tbody> 
</table>

#### Liste des traitements d’export et d’import

Ce module de recherche répertorie la tâche d’exportation et d’importation actuelle. Vous pouvez utiliser des paramètres de requête pour filtrer la liste.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned results]</td> 
      <td>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
      <td>Choisissez de classer les résultats par date de création ou date de modification.</td>
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Query parameter]</td> 
   <td>Pour chaque paramètre de requête sur lequel vous souhaitez appliquer un filtre, cliquez sur <b>Ajouter un paramètre de requête</b>, sélectionnez le champ et l’opérateur, puis saisissez la valeur du champ pour le filtre.</td> 
  </tr> 
 </tbody> 
</table>



#### Liste des packages

Ce module de recherche répertorie tous les packages de votre organisation. Vous pouvez utiliser des paramètres de requête pour filtrer la liste.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned results]</td> 
      <td>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
      <td>Choisissez de classer les résultats par date de création ou date de modification.</td>
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Query parameter]</td> 
   <td>Pour chaque paramètre de requête sur lequel vous souhaitez appliquer un filtre, cliquez sur <b>Ajouter un paramètre de requête</b>, sélectionnez le champ et l’opérateur, puis saisissez la valeur du champ pour le filtre.</td> 
  </tr> 
 </tbody> 
</table>

#### Répertorier les enregistrements

Ce module de recherche répertorie toutes les configurations de plafonnement ou de limitation.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select content type]</td> 
   <td>Choisissez si vous récupérez un modèle de contenu ou un fragment de contenu.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
   <td>Saisissez ou mappez le nom du paramètre selon lequel vous souhaitez trier cette liste. Ajoutez des <code>-</code> ou des <code>+</code> pour trier par ordre décroissant ou croissant. Si aucun signe n’est spécifié, la liste est triée par ordre décroissant.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start]</td> 
   <td>Ce champ est utilisé pour la pagination. Saisissez ou mappez les critères de la page suivante par rapport à la propriété spécifiée dans le champ Trier par .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
   <td>Saisissez ou mappez le nom du paramètre selon lequel vous souhaitez trier cette liste. Ajoutez des <code>-</code> ou des <code>+</code> pour trier par ordre décroissant ou croissant. Si aucun signe n’est spécifié, la liste est triée par ordre décroissant.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by property]</td> 
   <td>Pour chaque filtre de propriété à ajouter, cliquez sur <b>Ajouter un élément</b> et saisissez la clé et la valeur de la propriété. Les enregistrements qui incluent la valeur spécifiée pour la propriété sont inclus dans la liste.</td> 
  </tr> 
 </tbody> 
</table>


### Autre


#### Effectuer un appel API personnalisé.

Ce module d’action effectue un appel API personnalisé à l’API Adobe Journey Optimizer.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Journey Optimizer], voir <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Créer une connexion à [!DNL Adobe Journey Optimizer]</a> dans cet article.</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>Saisissez un chemin d’accès relatif à l’URL de base.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP dans [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p>
        <p>Par exemple, <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] ajoute automatiquement des en-têtes d’autorisation, de <code>x-api-key</code> et de <code>x-gw-ims-org-id</code>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Saisissez la chaîne de requête.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lors de l’utilisation d’instructions conditionnelles telles que <code>if</code> dans votre fichier JSON, placez les guillemets en dehors de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>







<!--

* [Check if configuration can be deployed](#check-if-configuration-can-be-deployed)
* [Check service health](#check-service-health)
* [Check the import dependencies](#check-the-import-dependencies)
* [Check the status for audience-based message](#status-for-audience-based-message)
* [Copy artifacts synchronously](#copy-artifacts-synchronously)
* [Create a configuration](#create-a-configuration)
* [Create a package](#create-a-package)
* [Create a record](#create-a-record)
* [Delete a configuration](#delete-a-configuration)
* [Delete a package](#delete-a-package)
* [Delete a record](#delete-a-record)
* [Deploy a configuration](#deploy-a-configuration)
* [Export artifacts asynchronously](#export-artifacts-asynchronously)
* [Get a configuration](#get-a-configuration)
* [Get a record](#get-a-record)
* [Import a package](#import-a-package)
* [Import artifacts asynchronously](#import-artifacts-asynchronously)
* [List all dependent objects](#list-all-dependent-objects)
* [List export and import jobs](#list-import-and-export-jobs)
* [Look up a package](#look-up-a-package)
* [Make a custom API call](#make-a-custom-api-call)
* [Patch a record](#patch-a-record)
* [Publish a package](#publish-a-package)
* [Submit an import](#submit-an-import)
* [Trigger a unitary message execution](#trigger-a-unitary-message-execution)
* [Trigger an audience-based message](#trigger-an-audience-based-message)
* [Undeploy a configuration](#undeploy-a-configuration)
* [Update a configuration](#update-a-configuration)
* [Update a package](#update-a-package)
* [Update a record](#update-a-record)
* [List configurations](#list-configurations)
* [List packages](#list-packages)
* [List records](#list-records)

-->
