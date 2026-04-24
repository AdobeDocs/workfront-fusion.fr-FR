---
title: Modules GitLab
description: Adobe Workfront Fusion nécessite une licence Adobe Workfront Fusion en plus d’une licence Adobe Workfront.
author: Becky
feature: Workfront Fusion
exl-id: fabbadce-5669-4363-834e-6d7428520f62
source-git-commit: 6aad13e81c083754d7aad53dec103715bd6b8807
workflow-type: tm+mt
source-wordcount: '4099'
ht-degree: 98%

---

# Modules [!UICONTROL GitLab]

Adobe Workfront Fusion nécessite une licence Adobe Workfront Fusion en plus d’une licence Adobe Workfront.

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent [!UICONTROL GitLab] et les connecter à plusieurs applications et services tiers.

>[!NOTE]
>
>Avant de lire cet article, consultez la documentation de l’API et familiarisez-vous avec les fonctionnalités de [!DNL GitLab].

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

## Connecter [!DNL GitLab] à Workfront Fusion {#connect-gitlab-to-workfront-fusion}

1. Dans n’importe quel module de [!DNL Gitlab] Workfront Fusion, cliquez sur **[!UICONTROL Ajouter]** en regard du champ de connexion.
1. Configurez les champs suivants :

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection name]</td> 
      <td> <p>Saisissez un nom pour la connexion.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL [!DNL GitLab] URL]</td> 
      <td>Saisissez l’URL de votre instance [!DNL GitLab].</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Access Token]</td> 
      <td><p>Saisissez votre [!UICONTROL Private Token] ou [!UICONTROL Personal Access Token].</p><p>Pour plus d’informations sur la localisation ou la création d’un jeton d’accès personnel [!DNL GitLab], voir « Créer un jeton d’accès personnel » dans <a href="https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html">Jetons d’accès personnels</a> de la documentation [!DNL GitLab].</p></td> 
     </tr> 
    </tbody> 
   </table>


1. Cliquez sur **[!UICONTROL Continuer]**.
1. Cliquez sur **[!UICONTROL Autoriser]** pour créer la connexion et revenir au module.

## Modules [!DNL GitLab] et leurs champs

Lorsque vous configurez les modules [!DNL GitLab], Workfront Fusion affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL GitLab] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, consultez [Mappage d’informations d’un module à l’autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Bouton (bascule) de mappage](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Déclencheurs

+++**[!UICONTROL Contrôler les statuts de version]**

Ce module déclencheur instantané démarre un scénario lorsque le statut d’une version est modifié.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Sélectionnez le webhook que vous souhaitez utiliser pour ce déclencheur ou ajoutez un nouveau webhook. </p><p>Pour ajouter un webhook, <ol><li>cliquez sur <b>[!UICONTROL Add]</b> en regard du champ [!UICONTROL webhook].</li><li>Saisissez les informations suivantes : <ul><li>Un nom pour le webhook.</li><li>La connexion que vous souhaitez utiliser pour ce webhook.</li><li>Le projet pour lequel vous souhaitez que le webhook contrôle les modifications de statut de version.</li></ul></li><li>Cliquez sur <b>[!UICONTROL Save]</b> pour enregistrer le webhook et revenir au module. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Contrôler les commentaires d’engagement/de demande de fusion/de problème/d’extrait]**

Ce module déclencheur instantané lance un scénario lorsqu’un commentaire est publié sur un engagement, une demande de fusion, un problème ou un extrait de code.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Sélectionnez le webhook que vous souhaitez utiliser pour ce déclencheur ou ajoutez un nouveau webhook. </p><p>Pour ajouter un webhook, <ol><li>cliquez sur <b>[!UICONTROL Add]</b> en regard du champ [!UICONTROL webhook].</li><li>Saisissez les informations suivantes : <ul><li>Un nom pour le webhook.</li><li>La connexion que vous souhaitez utiliser pour ce webhook.</li><li>Le projet pour lequel vous souhaitez que le webhook contrôle les commentaires.</li></ul></li><li>Cliquez sur <b>[!UICONTROL Save]</b> pour enregistrer le webhook et revenir au module. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Contrôler les engagements (push)]**

Ce module déclencheur instantané lance un scénario lorsqu’un engagement est envoyé à un référentiel. Ce module ne lance pas de scénario lorsqu’une balise est envoyée.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Sélectionnez le webhook que vous souhaitez utiliser pour ce déclencheur ou ajoutez un nouveau webhook. </p><p>Pour ajouter un webhook, <ol><li>cliquez sur <b>[!UICONTROL Add]</b> en regard du champ [!UICONTROL webhook].</li><li>Saisissez les informations suivantes : <ul><li>Un nom pour le webhook.</li><li>La connexion que vous souhaitez utiliser pour ce webhook.</li><li>Le projet pour lequel vous souhaitez que le webhook contrôle les engagements.</li></ul></li><li>Cliquez sur <b>[!UICONTROL Save]</b> pour enregistrer le webhook et revenir au module. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Contrôler les commentaires de problème]**

Ce module déclencheur instantané lance un scénario lorsqu’un commentaire est publié sur un problème.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Sélectionnez le webhook que vous souhaitez utiliser pour ce déclencheur ou ajoutez un nouveau webhook. </p><p>Pour ajouter un webhook, <ol><li>cliquez sur <b>[!UICONTROL Add]</b> en regard du champ [!UICONTROL webhook].</li><li>Saisissez les informations suivantes : <ul><li>Un nom pour le webhook.</li><li>La connexion que vous souhaitez utiliser pour ce webhook.</li><li>Le projet pour lequel vous souhaitez que le webhook contrôle les commentaires de problème.</li></ul></li><li>Cliquez sur <b>[!UICONTROL Save]</b> pour enregistrer le webhook et revenir au module. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Contrôler les problèmes]**

Ce module [!UICONTROL déclencheur instantané] lance un scénario lorsqu’un problème est créé ou lorsqu’un problème existant est mis à jour, fermé ou rouvert.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Sélectionnez le webhook que vous souhaitez utiliser pour ce déclencheur ou ajoutez un nouveau webhook. </p><p>Pour ajouter un webhook, <ol><li>cliquez sur <b>[!UICONTROL Add]</b> en regard du champ [!UICONTROL webhook].</li><li>Saisissez les informations suivantes : <ul><li>Un nom pour le webhook.</li><li>La connexion que vous souhaitez utiliser pour ce webhook.</li><li>Le projet pour lequel vous souhaitez que le webhook contrôle les problèmes.</li></ul></li><li>Cliquez sur <b>[!UICONTROL Save]</b> pour enregistrer le webhook et revenir au module. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Contrôler les demandes de fusion]**

Ce module de déclenchement instantané démarre un scénario lorsque l’un des événements suivants se produit :

* Une nouvelle demande de fusion est créée.
* Une demande de fusion existante est mise à jour, fusionnée ou fermée.
* Une validation est ajoutée dans la branche source.


<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Sélectionnez le webhook que vous souhaitez utiliser pour ce déclencheur ou ajoutez un nouveau webhook. </p><p>Pour ajouter un webhook, <ol><li>cliquez sur <b>[!UICONTROL Add]</b> en regard du champ [!UICONTROL webhook].</li><li>Saisissez les informations suivantes : <ul><li>Un nom pour le webhook.</li><li>La connexion que vous souhaitez utiliser pour ce webhook.</li><li>Le projet pour lequel vous souhaitez que le webhook contrôle les demandes de fusion.</li></ul></li><li>Cliquez sur <b>[!UICONTROL Save]</b> pour enregistrer le webhook et revenir au module. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Contrôler les commentaires de demande de fusion]**

Ce module de déclenchement instantané démarre un scénario lorsqu’un commentaire est fait sur une demande de fusion.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Sélectionnez le webhook que vous souhaitez utiliser pour ce déclencheur ou ajoutez un nouveau webhook. </p><p>Pour ajouter un webhook, <ol><li>cliquez sur <b>[!UICONTROL Add]</b> en regard du champ [!UICONTROL webhook].</li><li>Saisissez les informations suivantes : <ul><li>Un nom pour le webhook.</li><li>La connexion que vous souhaitez utiliser pour ce webhook.</li><li>Le projet pour lequel le webhook doit contrôler les commentaires de demande de fusion.</li></ul></li><li>Cliquez sur <b>[!UICONTROL Save]</b> pour enregistrer le webhook et revenir au module. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Contrôler le statut du pipeline]**

Ce module de déclenchement instantané démarre un scénario lorsque le statut d’un pipeline change.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Sélectionnez le webhook que vous souhaitez utiliser pour ce déclencheur ou ajoutez un nouveau webhook. </p><p>Pour ajouter un webhook, <ol><li>cliquez sur <b>[!UICONTROL Add]</b> en regard du champ [!UICONTROL webhook].</li><li>Saisissez les informations suivantes : <ul><li>Un nom pour le webhook.</li><li>La connexion que vous souhaitez utiliser pour ce webhook.</li><li>Le projet pour lequel le webhook doit contrôler les modifications de statut de pipeline.</li></ul></li><li>Cliquez sur <b>[!UICONTROL Save]</b> pour enregistrer le webhook et revenir au module. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Contrôler les projets]**

Ce module de déclenchement planifié lance un scénario lors de l’ajout d’un nouveau projet dont la personne authentifiée est membre.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour des instructions sur la connexion de votre compte [!DNL GitLab] à Workfront Fusion, consultez <a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">Connecter [!DNL GitLab] à Workfront Fusion</a> dans cet article.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Nbre max. de résultats</td> 
   <td> <p>Saisissez ou mappez le nombre maximal d’enregistrements que le module doit surveiller pour chaque cycle d’exécution de scénario.</p> </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Contrôler des branches de référentiel]**

Ce module de déclenchement planifié lance un scénario lorsqu’une nouvelle branche est ajoutée à un référentiel.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour des instructions sur la connexion de votre compte [!DNL GitLab] à Workfront Fusion, consultez <a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">Connecter [!DNL GitLab] à Workfront Fusion</a> dans cet article.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Nbre max. de résultats</td> 
   <td> <p>Saisissez ou mappez le nombre maximal d’enregistrements que le module doit surveiller pour chaque cycle d’exécution de scénario.</p> </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Contrôler les balises de référentiel]**

Ce module de déclenchement instantané lance un scénario lors de la création ou de la suppression d’une balise dans un référentiel.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Sélectionnez le webhook que vous souhaitez utiliser pour ce déclencheur ou ajoutez un nouveau webhook. </p><p>Pour ajouter un webhook, <ol><li>cliquez sur <b>[!UICONTROL Add]</b> en regard du champ [!UICONTROL webhook].</li><li>Saisissez les informations suivantes : <ul><li>Un nom pour le webhook.</li><li>La connexion que vous souhaitez utiliser pour ce webhook.</li><li>Le projet pour lequel le webhook doit contrôler les balises.</li></ul></li><li>Cliquez sur <b>[!UICONTROL Save]</b> pour enregistrer le webhook et revenir au module. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Contrôler les commentaires d’extrait]**

Ce module de déclenchement instantané lance un scénario lorsqu’un nouveau commentaire est effectué sur un extrait.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Sélectionnez le webhook que vous souhaitez utiliser pour ce déclencheur ou ajoutez un nouveau webhook. </p><p>Pour ajouter un webhook, <ol><li>cliquez sur <b>[!UICONTROL Add]</b> en regard du champ [!UICONTROL webhook].</li><li>Saisissez les informations suivantes : <ul><li>Un nom pour le webhook.</li><li>La connexion que vous souhaitez utiliser pour ce webhook.</li><li>Le projet pour lequel vous souhaitez que le webhook contrôle les commentaires.</li></ul></li><li>Cliquez sur <b>[!UICONTROL Save]</b> pour enregistrer le webhook et revenir au module. </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Contrôler les choses à faire]**

Ce module déclencheur planifié lance un scénario lorsqu’une chose à faire est ajoutée. Lorsqu’aucun filtre n’est appliqué, le déclencheur est exécuté si une chose à faire en attente est ajoutée.

Pour plus d’informations sur les champs, voir [Obtenir une liste de choses à faire](https://docs.gitlab.com/ee/api/todos.html#get-a-list-of-todos) dans la documentation de [!DNL GitLab].

+++

+++**[!UICONTROL Contrôler la page wiki]**

Ce module déclencheur instantané lance un scénario lorsqu’une page wiki est créée ou modifiée.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Sélectionnez le webhook que vous souhaitez utiliser pour ce déclencheur ou ajoutez un nouveau webhook. </p><p>Pour ajouter un webhook, <ol><li>cliquez sur <b>[!UICONTROL Add]</b> en regard du champ [!UICONTROL webhook].</li><li>Saisissez les informations suivantes : <ul><li>Un nom pour le webhook.</li><li>La connexion que vous souhaitez utiliser pour ce webhook.</li><li>Le projet pour lequel vous souhaitez que le webhook contrôle les pages wiki.</li></ul></li><li>Cliquez sur <b>[!UICONTROL Save]</b> pour enregistrer le webhook et revenir au module. </td> 
   </tr> 
   </tbody> 
</table>

+++

### Actions

+++**[!UICONTROL Accepter la demande de fusion]**

Ce module d’action fusionne les modifications soumises avec la demande de fusion donnée.

Pour plus d’informations sur les champs, voir [Accepter la demande de fusion](https://docs.gitlab.com/ee/api/merge_requests.html#accept-mr) dans la documentation de [!DNL GitLab].

+++

+++**[!UICONTROL Annuler une version]**

Ce module d’action annule une seule version d’un projet.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour des instructions sur la connexion de votre compte [!DNL GitLab] à Workfront Fusion, consultez <a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">Connecter [!DNL GitLab] à Workfront Fusion</a> dans cet article.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p>Sélectionnez ou mappez le projet contenant la version que vous souhaitez annuler.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Build ID]</td> 
   <td>Sélectionnez ou mappez la version que vous souhaitez annuler.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Merge commit message]</td> 
   <td> Saisissez ou mappez un message d’engagement pour la fusion.
    </td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Should remove source branch]</td> 
   <td>Indiquez si vous souhaitez supprimer la branche source une fois la fusion terminée.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Merge when build succeeds]</td> 
   <td>Indiquez si la demande de fusion doit être fusionnée une fois la version terminée.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL SHA]</td> 
   <td>S’il est présent, ce SHA doit correspondre à la méthode HEAD de la branche source. S’il ne correspond pas, la fusion échoue.</td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Annuler les versions d’un pipeline]**

Ce module d’action annule les versions pour un seul pipeline.

Pour plus d’informations sur les champs, voir [Annuler des traitements d’un pipeline](https://docs.gitlab.com/ee/api/pipelines.html#cancel-a-pipelines-jobs) dans la documentation de [!DNL GitLab].

+++

+++**[!UICONTROL Annuler la fusion en cas de réussite du pipeline]**

Si une demande de fusion est définie pour s’enclencher lorsqu’un pipeline réussit, ce module d’action annule cette opération.

Pour plus d’informations sur les champs, voir [Annuler la fusion si le pipeline réussit](https://docs.gitlab.com/ee/api/merge_requests.html) dans la documentation de [!DNL GitLab].

+++

+++**[!UICONTROL Sélectionner un engagement]**

Ce module d’action sélectionne un engagement sur une branche donnée.

Pour plus d’informations sur les champs, voir [Sélectionner un engagement](https://docs.gitlab.com/ee/api/commits.html#cherry-pick-a-commit) dans la documentation de [!DNL GitLab].

+++

+++**[!UICONTROL Créer un libellé]**

Ce module d’action crée un libellé pour le référentiel donné.

Pour plus d’informations sur les champs, voir [Créer un libellé](https://docs.gitlab.com/ee/api/labels.html#create-a-new-label) dans la documentation de [!DNL GitLab].

+++

+++**[!UICONTROL Créer un pipeline]**

Ce module d’action crée un pipeline pour le projet donné.

Pour plus d’informations sur les champs, voir [Créer un pipeline](https://docs.gitlab.com/ee/api/pipelines.html#create-a-new-pipeline) dans la documentation de [!DNL GitLab].

+++

+++**[!UICONTROL Créer une version]**

Ce module d’action ajoute des notes de mise à jour à la balise git existante.

Pour plus d’informations sur les champs, voir [Créer une version](https://docs.gitlab.com/ee/api/releases/#create-a-release) dans la documentation de [!DNL GitLab].

+++

+++**[!UICONTROL Créer une balise]**

Ce module d’action crée une balise dans le référentiel qui renvoie à la référence fournie.

Pour plus d’informations sur les champs, voir [Créer une balise](https://docs.gitlab.com/ee/api/tags.html#create-a-new-tag) dans la documentation de [!DNL GitLab].

+++

+++**[!UICONTROL Créer une chose à faire]**

Ce module d’action crée une chose à faire pour la personne concernée sur le problème sélectionné. La personne concernée est la personne identifiée par les informations d’identification sur la connexion utilisée pour ce module.

Pour plus d’informations sur les champs, voir la section [Créer une chose à faire](https://docs.gitlab.com/ee/api/issues.html#create-a-todo) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Créer une chose à faire sur une demande de fusion]**

Ce module d’action crée une chose à faire pour la personne concernée sur la demande de fusion sélectionnée. La personne concernée est la personne identifiée par les informations d’identification sur la connexion utilisée pour ce module.

Pour plus d’informations sur les champs, voir [Créer une chose à faire](https://docs.gitlab.com/ee/api/merge_requests.html#create-a-todo) dans la documentation [!DNL GitLab]

+++

+++**[!UICONTROL Créer une demande de fusion]**

Ce module d’action crée une nouvelle demande de fusion sur un projet.

Pour plus d’informations sur les champs, voir la section [Créer une demande de fusion](https://docs.gitlab.com/ee/api/merge_requests.html#create-mr) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Créer un fichier dans le référentiel]**

Ce module d’action crée un fichier dans le référentiel sélectionné.

Pour plus d’informations sur les champs, voir la section [Créer un fichier dans le référentiel](https://docs.gitlab.com/ee/api/repository_files.html#create-new-file-in-repository) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Créer une note de problème]**

Ce module d’action crée une note de problème pour un problème de projet unique.

Pour plus d’informations sur les champs, voir la section [Créer une note de problème](https://docs.gitlab.com/ee/api/notes.html#create-new-issue-note) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Créer une note de demande de fusion]**

Ce module d’action crée une note pour une seule demande de fusion.

Pour plus d’informations sur les champs, voir la section [Créer une note de demande de fusion](https://docs.gitlab.com/ee/api/notes.html#create-new-merge-request-note) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Créer un jalon]**

Ce module d’action crée un jalon pour un projet.

Pour plus d’informations sur les champs, voir la section [Créer un jalon](https://docs.gitlab.com/ee/api/milestones.html#create-new-milestone) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Créer une note d’extrait de code]**

Ce module d’action crée une note pour un seul extrait de code. Les notes des extraits de code sont des commentaires que les utilisateurs et utilisatrices peuvent publier sur un extrait de code.

Pour plus d’informations sur les champs, voir la section [Créer une note d’extrait de code](https://docs.gitlab.com/ee/api/notes.html#create-new-snippet-note) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Créer une branche de référentiel]**

Ce module d’action crée une seule branche de référentiel.

Pour plus d’informations sur les champs, voir la section [Créer une branche de référentiel](https://docs.gitlab.com/ee/api/branches.html#create-repository-branch) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Créer une variable de version]**

Ce module d’action crée une variable de version.

Pour plus d’informations sur les champs, voir la section [Créer une variable](https://docs.gitlab.com/ee/api/project_level_variables.html#create-variable) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Supprimer une demande de fusion]**

Ce module d’action est réservé aux administrateurs et administratrices et aux personnes propriétaires de projets. Il supprime la demande de fusion en question.

Pour plus d’informations sur les champs, voir la section [Supprimer une demande de fusion](https://docs.gitlab.com/ee/api/merge_requests.html#delete-a-merge-request) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Supprimer un fichier existant dans le référentiel]**

Ce module d’action supprime un fichier existant du référentiel.

Pour plus d’informations sur les champs, voir la section [Supprimer un fichier existant du référentiel](https://docs.gitlab.com/ee/api/repository_files.html#delete-existing-file-in-repository) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Supprimer une branche du référentiel]**

Ce module d’action supprime une branche du référentiel.

Pour plus d’informations sur les champs, voir la section [Supprimer une branche du référentiel](https://docs.gitlab.com/ee/api/branches.html#delete-repository-branch) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Modifier le problème]**

Ce module d’action met à jour un problème de projet existant. Cet appel est également utilisé pour marquer la clôture d’un problème.

Pour plus d’informations sur les champs, voir la section [Modifier un problème](https://docs.gitlab.com/ee/api/issues.html#edit-issue) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Modifier jalon]**
Ce module d&#39;action met à jour un jalon de projet existant.

Pour plus d’informations sur les champs, voir la section [Modifier un jalon](https://docs.gitlab.com/ee/api/milestones.html#edit-milestone) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Effacer une version]**

Ce module d’action efface une version d’un projet (supprime les artefacts et le log de traitement).

Pour plus d’informations sur les champs, voir [Effacer un traitement](https://docs.gitlab.com/ee/api/jobs.html#erase-a-job) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Obtenir une liste de choses à faire]**

Ce module de recherche permet de récupérer une liste des choses à faire.

Pour plus d’informations sur les champs, voir [Obtenir une liste des choses à faire](https://docs.gitlab.com/ee/api/todos.html#get-a-list-of-todos) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Obtenir une version unique]**

Ce module d’action permet de récupérer un seul traitement d’un projet.

Pour plus d’informations sur les champs, voir [Obtenir un traitement unique](https://docs.gitlab.com/ee/api/jobs.html#get-a-single-job) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Obtenir une balise de référentiel unique]**

Ce module d’action permet de récupérer une balise de référentiel spécifique déterminée par son nom.

Pour plus d’informations sur les champs, voir [Obtenir une balise de référentiel unique](https://docs.gitlab.com/ee/api/tags.html#get-a-single-repository-tag) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Obtenir un déploiement spécifique]**

Ce module d’action permet de récupérer un déploiement spécifique.

Pour plus d’informations sur les champs, voir [Obtenir un déploiement spécifique](https://docs.gitlab.com/ee/api/deployments.html#get-a-specific-deployment) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Obtenir tous les problèmes affectés à un seul jalon]**

Ce module de recherche permet de récupérer tous les problèmes affectés à un seul jalon du projet.

Pour plus d’informations sur les champs, voir [Obtenir tous les problèmes affectés à un seul jalon](https://docs.gitlab.com/ee/api/milestones.html#get-all-issues-assigned-to-a-single-milestone) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Obtenir un fichier du référentiel]**

Ce module d’action permet de récupérer des informations sur un fichier dans le référentiel, comme son nom, sa taille ou son contenu.

Pour plus d’informations sur les champs, voir [Obtenir un fichier du référentiel](https://docs.gitlab.com/ee/api/repository_files.html#get-file-from-repository) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Obtenir les utilisateurs et utilisatrices du projet]**

Ce module de recherche permet de récupérer les utilisateurs et utilisatrices du projet.

Pour plus d’informations sur les champs, voir [Obtenir les utilisateurs et utilisatrices du projet](https://docs.gitlab.com/ee/api/projects.html#get-project-users) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Obtenir un problème unique]**

Ce module d’action permet de récupérer les détails d’un problème.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour créer une connexion, voir <a href="#connect-gitlab-to-workfront-fusion" class="MCXref xref">[!UICONTROL Connect [!DNL GitLab] to Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project]</td> 
   <td> <p>Sélectionnez le projet qui contient le problème dont vous voulez récupérer les détails.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Issue ID]</td> 
   <td> <p>Saisissez ou mappez le nom du problème pour lequel vous souhaitez récupérer des détails.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Obtenir une note de problème unique]**

Ce module d’action permet de récupérer une seule note pour un problème de projet spécifique.

Pour plus d’informations sur les champs, voir [Obtenir une note de problème unique](https://docs.gitlab.com/ee/api/notes.html#get-single-issue-note) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Obtenir une demande de fusion unique]**

Ce module d’action permet de récupérer des informations sur une demande de fusion unique.

Pour plus d’informations sur les champs, voir [Obtenir une demande de fusion unique](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Obtenir les modifications d’une demande de fusion unique]**

Ce module de recherche récupère des informations sur la demande de fusion, y compris ses fichiers et ses modifications.

Pour plus d’informations sur les champs, voir [Obtenir les modifications d’un demande de fusion unique](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr-changes) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Obtenir les engagements d’une demande de fusion unique]**

Ce module d’action permet de récupérer une liste de engagements de demande de fusion.

Pour plus d’informations sur les champs, voir [Obtenir les engagements d’une demande de fusion unique](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr-commits) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Obtenir une note de demande de fusion unique]**

Ce module d’action renvoie une note unique pour une demande de fusion donnée.

Pour plus d’informations sur les champs, voir [Obtenir une note pour une demande de fusion unique](https://docs.gitlab.com/ee/api/notes.html#get-single-merge-request-note) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Obtenir un jalon]**

Ce module d’action récupère les détails d’un jalon.

Pour plus d’informations sur les champs, voir [Obtenir un jalon unique](https://docs.gitlab.com/ee/api/milestones.html#get-single-milestone) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Obtenir un projet unique]**

Ce module d’action récupère les détails d’un projet.

Pour plus d’informations sur les champs, voir [Obtenir un projet unique](https://docs.gitlab.com/ee/api/projects.html#get-single-project) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Obtenir une branche de référentiel unique]**

Ce module d’action récupère les détails d’une branche de référentiel.

Pour plus d’informations sur les champs, voir [Obtenir une branche de référentiel unique](https://docs.gitlab.com/ee/api/branches.html#get-single-repository-branch) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Obtenir une note d’extrait de code]**

Ce module récupère une note unique pour un extrait de code donné.

Pour plus d’informations sur les champs, voir [Obtenir une note d’un extrait de code unique](https://docs.gitlab.com/ee/api/notes.html#get-single-snippet-note) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Obtenir les commentaires d’un engagement]**

Ce module de recherche récupère les commentaires d’un engagement dans un projet.

Pour plus d’informations sur les champs, voir [Obtenir les commentaires d’un engagement](https://docs.gitlab.com/ee/api/commits.html#get-the-comments-of-a-commit) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Obtenir le diff d‘un engagement]**

Ce module d’action récupère le diff d’un engagement dans un projet.

Pour plus d’informations sur les champs, voir [Obtenir le diff d’un engagement](https://docs.gitlab.com/ee/api/commits.html#get-the-diff-of-a-commit) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Conserver les artefacts]**

Empêche la suppression des artefacts lorsque l’expiration est fixée.

Pour plus d’informations sur les champs, voir [Conserver les artefacts](https://docs.gitlab.com/ee/api/job_artifacts.html#keep-artifacts) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Répertorier toutes les notes de demande de fusion]**

Ce module de recherche permet d’obtenir une liste de toutes les notes relatives à une demande de fusion unique.

Pour plus d’informations sur les champs, voir [Répertorier toutes les notes de demande de fusion](https://docs.gitlab.com/ee/api/notes.html#list-all-merge-request-notes) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Répertorier toutes les notes d’extrait de code]**

Ce module permet d’obtenir une liste de toutes les notes pour un extrait de code unique. Les notes des extraits de code sont des commentaires que les utilisateurs et utilisatrices peuvent publier sur un extrait de code.

Pour plus d’informations sur les champs, voir [Liste de tous les fragments de code](https://docs.gitlab.com/ee/api/notes.html#list-all-snippet-notes) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Répertorier les versions d’un engagement]**

Ce module de recherche renvoie une liste de versions pour un engagement spécifique dans un projet.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour créer une connexion, voir la section <a href="#connect-gitlab-to-workfront-fusion" class="MCXref xref">[!UICONTROL Connect [!DNL GitLab] to Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p>Sélectionnez le projet qui contient l’engagement dont vous voulez répertorier les versions.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scope]</td> 
   <td> Pour limiter la recherche aux versions ayant un statut spécifique, sélectionnez le statut. Le fait de laisser ce champ vide renvoie toutes les versions de l’engagement.  </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Répertorier les problèmes]**

Ce module de recherche renvoie tous les problèmes en fonction des paramètres de filtrage spécifiés.

Pour plus d’informations sur les champs, voir [Répertorier les problèmes](https://docs.gitlab.com/ee/api/issues.html#list-issues) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Répertorier les problèmes qui se clôturent lors de la fusion.]**

Ce module de recherche récupère tous les problèmes qui se clôtureraient par la fusion de la demande de fusion fournie.

Pour plus d’informations sur les champs, voir [Répertorier les problèmes qui seront clôturés lors de la fusion](https://docs.gitlab.com/ee/api/merge_requests.html#list-issues-that-will-close-on-merge) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Répertorier les libellés]**

Ce module de recherche permet de récuperer tous les libellés du projet.

Pour plus d’informations sur les champs, voir [Répertorier les libellés](https://docs.gitlab.com/ee/api/labels.html#list-labels) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Répertorier les demandes de fusion]**

Ce module de recherche permet de récupérer toutes les demandes de fusion en fonction des paramètres de filtrage.

Pour plus d’informations sur les champs, voir la section [Répertorier les demandes de fusion](https://docs.gitlab.com/ee/api/merge_requests.html#list-merge-requests) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Répertorier les projets détenus]**

Ce module de recherche permet de récupérer les projets dont la personne authentifiée est propriétaire.

Pour plus d’informations sur les champs, voir la section [Répertorier les projets des utilisateurs et utilisatrices](https://docs.gitlab.com/ee/api/projects.html#list-all-projects) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Répertorier les versions de projet]**

Ce module de recherche permet de récupérer la liste des versions d’un projet.

Pour plus d’informations sur les champs, voir la section [Répertorier les traitements de projet](https://docs.gitlab.com/ee/api/jobs.html#list-project-jobs) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Répertorier les déploiements de projet]**

Ce module de recherche permet de récupérer une liste des déploiements dans un projet.

Pour plus d’informations sur les champs, voir la section [Répertorier les déploiements de projet](https://docs.gitlab.com/ee/api/deployments.html#list-project-deployments) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Répertorier les notes sur les problèmes d’un projet]**

Ce module de recherche permet de récupérer une liste de toutes les notes relatives à un problème donné.

Pour plus d’informations sur les champs, voir la section [Répertorier les notes sur les problèmes d’un projet](https://docs.gitlab.com/ee/api/notes.html#list-project-issue-notes) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Répertorier les problèmes d’un projet]**

Ce module de recherche renvoie tous les problèmes relatifs à un projet donné.

Pour plus d’informations sur les champs, voir la section [Répertorier les problèmes d’un projet](https://docs.gitlab.com/ee/api/issues.html#list-project-issues) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Répertorier les jalons d’un projet]**

Ce module de recherche permet de récupérer tous les jalons du projet.

Pour plus d’informations sur les champs, voir la section [Répertorier les jalons d’un projet](https://docs.gitlab.com/ee/api/milestones.html#list-project-milestones) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Répertorier les pipelines d’un projet]**

Ce module de recherche permet de récupérer tous les pipelines du projet.

Pour plus d’informations sur les champs, voir la section [Répertorier les pipelines d’un projet](https://docs.gitlab.com/ee/api/pipelines.html#list-project-pipelines) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Répertorier les balises de référentiel du projet]**

Ce module de recherche permet de récupérer une liste des balises de référentiel d’un projet, triées par nom dans l’ordre alphabétique inverse.

Pour plus d’informations sur les champs, voir la section [Répertorier les balises de référentiel du projet](https://docs.gitlab.com/ee/api/tags.html#list-project-repository-tags) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Répertorier les variables du projet]**

Ce module de recherche permet de récupérer la liste des variables d’un projet.

Pour plus d’informations sur les champs, voir la section [Répertorier les variables du projet](https://docs.gitlab.com/ee/api/project_level_variables.html#list-project-variables) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Répertorier les projets]**

Ce module de recherche permet de récupérer tous les projets dont la personne authentifiée est membre.

Pour plus d’informations sur les champs, voir la section [Répertorier tous les projets](https://docs.gitlab.com/ee/api/projects.html#list-all-projects) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Répertorier les branches du référentiel]**

Ce module recherche les branches du référentiel en fonction du terme de recherche.

Pour plus d’informations sur les champs, voir la section [Répertorier les branches du référentiel](https://docs.gitlab.com/ee/api/branches.html#list-repository-branches) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Répertorier les engagements du référentiel]**

Ce module de recherche permet de récupérer une liste des engagements du référentiel dans un projet.

Pour plus d’informations sur les champs, voir la section [Répertorier les engagements du référentiel](https://docs.gitlab.com/ee/api/commits.html#list-repository-commits) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Répertorier les contributeurs et contributrices du référentiel]**

Ce module de recherche permet de récupérer la liste des contributeurs et contributrices d’un référentiel.

Pour plus d’informations sur les champs, voir la section [Contributeurs et contributrices](https://docs.gitlab.com/ee/api/repositories.html#contributors) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Répertorier l’arborescence du référentiel]**

Ce module de recherche permet de récupérer une liste des fichiers et des répertoires du référentiel dans un projet.

Pour plus d’informations sur les champs, voir la section [Répertorier l’arborescence du référentiel](https://docs.gitlab.com/ee/api/repositories.html#list-repository-tree) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Marquer une chose à faire comme terminée]**

Ce module d’action marque une chose à faire en attente donnée par son ID pour la personne concernée comme étant terminée.

Pour plus d’informations sur les champs, voir la section [Marquer une chose à faire comme terminée](https://docs.gitlab.com/ee/api/todos.html#mark-a-todo-as-done) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Modifier une note de problème existante]**

Modifie une note existante d’un problème.

Pour plus d’informations sur les champs, voir la section [Modifier une note de problème existante](https://docs.gitlab.com/ee/api/notes.html#modify-existing-issue-note) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Modifier une note de demande de fusion existante]**

Modifie la note existante d’une demande de fusion.

Pour plus d’informations sur les champs, voir la section [Modifier une note de demande de fusion existante](https://docs.gitlab.com/ee/api/notes.html#modify-existing-merge-request-note) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Modifier une note d’extrait de code existante]**

Ce module d’action modifie une note existante d’un extrait de code.

Pour plus d’informations sur les champs, voir la section [Modifier une note d’extrait de code existante](https://docs.gitlab.com/ee/api/notes.html#modify-existing-snippet-note) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Nouveau problème]**

Ce module d’action crée un problème de projet.

Pour plus d’informations sur les champs, voir la section [Nouveau problème](https://www.integromat.com/en/help/app/gitlab) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Lire une version]**

Ce module d’action déclenche une action manuelle pour démarrer un traitement.

Pour plus d’informations sur les champs, voir la section [Lire un traitement](https://docs.gitlab.com/ee/api/jobs.html#play-a-job) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Publier un commentaire sur l’engagement]**

Ce module d’action ajoute un commentaire à un engagement.

Pour plus d’informations sur les champs, voir la section [Publier un commentaire sur l’engagement](https://docs.gitlab.com/ee/api/commits.html#post-comment-to-commit) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Supprimer la variable]**

Ce module d’action supprime la variable d’un projet.

Pour plus d’informations sur les champs, voir la section [Supprimer la variable](https://docs.gitlab.com/ee/api/project_level_variables.html#remove-variable) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Réessayer une version]**

Ce module d’action réessaie une version unique dans un engagement.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour créer une connexion, voir la section <a href="#connect-gitlab-to-workfront-fusion" class="MCXref xref">[!UICONTROL Connect [!DNL GitLab] to Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project ID]</td> 
   <td> <p>Sélectionnez le projet qui contient la version que vous voulez réessayer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Build ID]</td> 
   <td> Sélectionnez la version que vous souhaitez réessayer. </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Réessayer les traitements qui ont échoué dans un pipeline.]**

Ce module d’action retente les versions qui ont échoué dans un pipeline.

Pour plus d’informations sur les champs, voir la section [Réessayer des traitements dans un pipeline](https://docs.gitlab.com/ee/api/pipelines.html#retry-jobs-in-a-pipeline) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Obtenir une variable]**

Ce module permet de récupérer les détails d’une variable spécifique d’un projet.

Pour plus d’informations sur les champs, voir la section [Afficher les détails de la variable](https://docs.gitlab.com/ee/api/project_level_variables.html#show-variable-details) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Mettre à jour une version]**

Ce module d’action met à jour une version.

Pour plus d’informations sur les champs, voir la section [Mettre à jour une version](https://docs.gitlab.com/ee/api/releases/#update-a-release) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Mettre à jour une demande de fusion]**

Ce module d’action met à jour une demande de fusion existante. Vous pouvez modifier la branche cible, le titre ou même fermer la demande de fusion.

Pour plus d’informations sur les champs, voir la section [Mettre à jour une demande de fusion](https://docs.gitlab.com/ee/api/merge_requests.html#update-mr) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Mettre à jour une variable]**

Ce module d’action met à jour la variable d’un projet.

Pour plus d’informations sur les champs, voir la section [Mettre à jour une variable](https://docs.gitlab.com/ee/api/project_level_variables.html#update-variable) dans la documentation [!DNL GitLab].

+++
