---
title: Modules GitLab
description: Adobe Workfront Fusion nécessite une licence Adobe Workfront Fusion en plus d’une licence Adobe Workfront.
author: Becky
feature: Workfront Fusion
exl-id: fabbadce-5669-4363-834e-6d7428520f62
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '3554'
ht-degree: 90%

---

# Modules [!UICONTROL GitLab]

Adobe Workfront Fusion nécessite une licence Adobe Workfront Fusion en plus d’une licence Adobe Workfront.

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!UICONTROL GitLab] et le connecter à plusieurs applications et services tiers.

>[!NOTE]
>
>Avant de lire cet article, consultez la documentation de l’API et familiarisez-vous avec les fonctionnalités de [!DNL GitLab].

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

## Conditions d’accès

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] formule*</td>
  <td> <p>[!UICONTROL Pro] ou une version ultérieure</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licence*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
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

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], consultez la section Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Connecter [!DNL GitLab] à [!DNL Workfront Fusion] {#connect-gitlab-to-workfront-fusion}

1. Dans n’importe quel module de [!DNL Gitlab] de [!DNL Workfront Fusion], cliquez sur **[!UICONTROL Add]** en regard du champ de connexion.
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
      <td><p>Saisissez votre [!UICONTROL Private Token] ou votre [!UICONTROL Personal Access Token].</p><p>Pour plus d’informations sur la localisation ou la création d’un jeton d’accès personnel [!DNL GitLab], voir « Créer un jeton d’accès personnel » dans <a href="https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html">Jetons d’accès personnels</a> de la documentation [!DNL GitLab].</p></td> 
     </tr> 
    </tbody> 
   </table>


1. Cliquez sur **[!UICONTROL Continue]**.
1. Cliquez sur **[!UICONTROL Authorize]** pour créer la connexion et revenir au module .

## Modules [!DNL GitLab] et leurs champs

Lorsque vous configurez les modules [!DNL GitLab], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL GitLab] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Déclencheurs

+++**[!UICONTROL Watch build status]**

Ce module déclencheur instantané démarre un scénario lorsque le statut d’une version est modifié.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Sélectionnez le webhook que vous souhaitez utiliser pour ce déclencheur ou ajoutez un nouveau webhook. </p><p>Pour ajouter un webhook, <ol><li>Cliquez sur <b>[!UICONTROL Add]</b> en regard du champ [!UICONTROL webhook] .</li><li>Saisissez les informations suivantes : <ul><li>Un nom pour le webhook.</li><li>La connexion que vous souhaitez utiliser pour ce webhook.</li><li>Le projet pour lequel vous souhaitez que le webhook contrôle les modifications de statut de version.</li></ul></li><li>Cliquez sur <b>[!UICONTROL Save]</b> pour enregistrer le webhook et revenir au module . </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch commit/MR/issue/snippet comments]**

Ce module déclencheur instantané lance un scénario lorsqu’un commentaire est publié sur un engagement, une demande de fusion, un problème ou un extrait de code.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Sélectionnez le webhook que vous souhaitez utiliser pour ce déclencheur ou ajoutez un nouveau webhook. </p><p>Pour ajouter un webhook, <ol><li>Cliquez sur <b>[!UICONTROL Add]</b> en regard du champ [!UICONTROL webhook] .</li><li>Saisissez les informations suivantes : <ul><li>Un nom pour le webhook.</li><li>La connexion que vous souhaitez utiliser pour ce webhook.</li><li>Le projet pour lequel vous souhaitez que le webhook contrôle les commentaires.</li></ul></li><li>Cliquez sur <b>[!UICONTROL Save]</b> pour enregistrer le webhook et revenir au module . </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch commits (pushes)]**

Ce module déclencheur instantané lance un scénario lorsqu’un engagement est envoyé à un référentiel. Ce module ne lance pas de scénario lorsqu’une balise est envoyée.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Sélectionnez le webhook que vous souhaitez utiliser pour ce déclencheur ou ajoutez un nouveau webhook. </p><p>Pour ajouter un webhook, <ol><li>Cliquez sur <b>[!UICONTROL Add]</b> en regard du champ [!UICONTROL webhook] .</li><li>Saisissez les informations suivantes : <ul><li>Un nom pour le webhook.</li><li>La connexion que vous souhaitez utiliser pour ce webhook.</li><li>Le projet pour lequel vous souhaitez que le webhook contrôle les engagements.</li></ul></li><li>Cliquez sur <b>[!UICONTROL Save]</b> pour enregistrer le webhook et revenir au module . </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch issue comment]**

Ce module déclencheur instantané lance un scénario lorsqu’un commentaire est publié sur un problème.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Sélectionnez le webhook que vous souhaitez utiliser pour ce déclencheur ou ajoutez un nouveau webhook. </p><p>Pour ajouter un webhook, <ol><li>Cliquez sur <b>[!UICONTROL Add]</b> en regard du champ [!UICONTROL webhook] .</li><li>Saisissez les informations suivantes : <ul><li>Un nom pour le webhook.</li><li>La connexion que vous souhaitez utiliser pour ce webhook.</li><li>Le projet pour lequel vous souhaitez que le webhook contrôle les commentaires de problème.</li></ul></li><li>Cliquez sur <b>[!UICONTROL Save]</b> pour enregistrer le webhook et revenir au module . </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch issues]**

Ce module [!UICONTROL instant trigger] démarre un scénario lorsqu’un problème est créé ou lorsqu’un problème existant est mis à jour, fermé ou rouvert.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Sélectionnez le webhook que vous souhaitez utiliser pour ce déclencheur ou ajoutez un nouveau webhook. </p><p>Pour ajouter un webhook, <ol><li>Cliquez sur <b>[!UICONTROL Add]</b> en regard du champ [!UICONTROL webhook] .</li><li>Saisissez les informations suivantes : <ul><li>Un nom pour le webhook.</li><li>La connexion que vous souhaitez utiliser pour ce webhook.</li><li>Le projet pour lequel vous souhaitez que le webhook contrôle les problèmes.</li></ul></li><li>Cliquez sur <b>[!UICONTROL Save]</b> pour enregistrer le webhook et revenir au module . </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch merge requests]**

Ce module de déclenchement instantané démarre un scénario lorsque l’un des événements suivants se produit :

* Une nouvelle requête de fusion est créée.
* Une requête de fusion existante est mise à jour, fusionnée ou fermée.
* Une validation est ajoutée dans la branche source.


<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Sélectionnez le webhook que vous souhaitez utiliser pour ce déclencheur ou ajoutez un nouveau webhook. </p><p>Pour ajouter un webhook, <ol><li>Cliquez sur <b>[!UICONTROL Add]</b> en regard du champ [!UICONTROL webhook] .</li><li>Saisissez les informations suivantes : <ul><li>Un nom pour le webhook.</li><li>La connexion que vous souhaitez utiliser pour ce webhook.</li><li>Le projet pour lequel vous souhaitez que le webhook contrôle les requêtes de fusion.</li></ul></li><li>Cliquez sur <b>[!UICONTROL Save]</b> pour enregistrer le webhook et revenir au module . </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch merge request comments]**

Ce module de déclenchement instantané démarre un scénario lorsqu’un commentaire est fait sur une requête de fusion.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Sélectionnez le webhook que vous souhaitez utiliser pour ce déclencheur ou ajoutez un nouveau webhook. </p><p>Pour ajouter un webhook, <ol><li>Cliquez sur <b>[!UICONTROL Add]</b> en regard du champ [!UICONTROL webhook] .</li><li>Saisissez les informations suivantes : <ul><li>Un nom pour le webhook.</li><li>La connexion que vous souhaitez utiliser pour ce webhook.</li><li>Le projet pour lequel le webhook doit contrôler les commentaires de demande de fusion.</li></ul></li><li>Cliquez sur <b>[!UICONTROL Save]</b> pour enregistrer le webhook et revenir au module . </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch pipeline status]**

Ce module de déclenchement instantané démarre un scénario lorsque le statut d’un pipeline change.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Sélectionnez le webhook que vous souhaitez utiliser pour ce déclencheur ou ajoutez un nouveau webhook. </p><p>Pour ajouter un webhook, <ol><li>Cliquez sur <b>[!UICONTROL Add]</b> en regard du champ [!UICONTROL webhook] .</li><li>Saisissez les informations suivantes : <ul><li>Un nom pour le webhook.</li><li>La connexion que vous souhaitez utiliser pour ce webhook.</li><li>Le projet pour lequel le webhook doit contrôler les modifications de statut de pipeline.</li></ul></li><li>Cliquez sur <b>[!UICONTROL Save]</b> pour enregistrer le webhook et revenir au module . </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch projects]**

Ce module de déclenchement planifié lance un scénario lors de l’ajout d’un nouveau projet dont la personne authentifiée est membre.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la connexion de votre compte [!DNL GitLab] à [!DNL Workfront] Fusion, consultez la section <a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">Connecter [!DNL GitLab] à [!DNL Workfront] Fusion</a> de cet article.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Nbre max. de résultats</td> 
   <td> <p>Saisissez ou mappez le nombre maximal d’enregistrements que le module doit surveiller pour chaque cycle d’exécution de scénario.</p> </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch repository branches]**

Ce module de déclenchement planifié lance un scénario lorsqu’une nouvelle branche est ajoutée à un référentiel.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la connexion de votre compte [!DNL GitLab] à [!DNL Workfront] Fusion, consultez la section <a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">Connecter [!DNL GitLab] à [!DNL Workfront] Fusion</a> de cet article.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Nbre max. de résultats</td> 
   <td> <p>Saisissez ou mappez le nombre maximal d’enregistrements que le module doit surveiller pour chaque cycle d’exécution de scénario.</p> </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch repository tags]**

Ce module de déclenchement instantané lance un scénario lors de la création ou de la suppression d’une balise dans un référentiel.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Sélectionnez le webhook que vous souhaitez utiliser pour ce déclencheur ou ajoutez un nouveau webhook. </p><p>Pour ajouter un webhook, <ol><li>Cliquez sur <b>[!UICONTROL Add]</b> en regard du champ [!UICONTROL webhook] .</li><li>Saisissez les informations suivantes : <ul><li>Un nom pour le webhook.</li><li>La connexion que vous souhaitez utiliser pour ce webhook.</li><li>Le projet pour lequel le webhook doit contrôler les balises.</li></ul></li><li>Cliquez sur <b>[!UICONTROL Save]</b> pour enregistrer le webhook et revenir au module . </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch snippet comments]**

Ce module de déclenchement instantané lance un scénario lorsqu’un nouveau commentaire est effectué sur un extrait.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Sélectionnez le webhook que vous souhaitez utiliser pour ce déclencheur ou ajoutez un nouveau webhook. </p><p>Pour ajouter un webhook, <ol><li>Cliquez sur <b>[!UICONTROL Add]</b> en regard du champ [!UICONTROL webhook] .</li><li>Saisissez les informations suivantes : <ul><li>Un nom pour le webhook.</li><li>La connexion que vous souhaitez utiliser pour ce webhook.</li><li>Le projet pour lequel vous souhaitez que le webhook contrôle les commentaires.</li></ul></li><li>Cliquez sur <b>[!UICONTROL Save]</b> pour enregistrer le webhook et revenir au module . </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL Watch todos]**

Ce module déclencheur planifié lance un scénario lorsqu’une chose à faire est ajoutée. Lorsqu’aucun filtre n’est appliqué, le déclencheur est exécuté si une chose à faire en attente est ajoutée.

Pour plus d’informations sur les champs, voir [Obtenir une liste de choses à faire](https://docs.gitlab.com/ee/api/todos.html#get-a-list-of-todos) dans la documentation de [!DNL GitLab].

+++

+++**[!UICONTROL Watch wiki page]**

Ce module déclencheur instantané lance un scénario lorsqu’une page wiki est créée ou modifiée.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td><p>Sélectionnez le webhook que vous souhaitez utiliser pour ce déclencheur ou ajoutez un nouveau webhook. </p><p>Pour ajouter un webhook, <ol><li>Cliquez sur <b>[!UICONTROL Add]</b> en regard du champ [!UICONTROL webhook] .</li><li>Saisissez les informations suivantes : <ul><li>Un nom pour le webhook.</li><li>La connexion que vous souhaitez utiliser pour ce webhook.</li><li>Le projet pour lequel vous souhaitez que le webhook contrôle les pages wiki.</li></ul></li><li>Cliquez sur <b>[!UICONTROL Save]</b> pour enregistrer le webhook et revenir au module . </td> 
   </tr> 
   </tbody> 
</table>

+++

### Actions

+++**[!UICONTROL Accept merge request]**

Ce module d’action fusionne les modifications soumises avec la demande de fusion donnée.

Pour plus d’informations sur les champs, voir [Accepter la demande de fusion](https://docs.gitlab.com/ee/api/merge_requests.html#accept-mr) dans la documentation de [!DNL GitLab].

+++

+++**[!UICONTROL Cancel a build]**

Ce module d’action annule une seule version d’un projet.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour savoir comment connecter votre compte [!DNL GitLab] à [!DNL Workfront] Fusion, voir <a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">Connecter [!DNL GitLab] à [!DNL Workfront] Fusion</a> dans cet article.</td> 
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

+++**[!UICONTROL Cancel a pipeline's builds]**

Ce module d’action annule les versions pour un seul pipeline.

Pour plus d’informations sur les champs, voir [Annuler des traitements d’un pipeline](https://docs.gitlab.com/ee/api/pipelines.html#cancel-a-pipelines-jobs) dans la documentation de [!DNL GitLab].

+++

+++**[!UICONTROL Cancel merge when pipeline succeeds]**

Si une demande de fusion est définie pour s’enclencher lorsqu’un pipeline réussit, ce module d’action annule cette opération.

Pour plus d’informations sur les champs, voir [Annuler la fusion si le pipeline réussit](https://docs.gitlab.com/ee/api/merge_requests.html) dans la documentation de [!DNL GitLab].

+++

+++**[!UICONTROL Cherry pick a commit]**

Ce module d’action sélectionne un engagement sur une branche donnée.

Pour plus d’informations sur les champs, voir [Sélectionner un engagement](https://docs.gitlab.com/ee/api/commits.html#cherry-pick-a-commit) dans la documentation de [!DNL GitLab].

+++

+++**[!UICONTROL Create a new label]**

Ce module d’action crée un libellé pour le référentiel donné.

Pour plus d’informations sur les champs, voir [Créer un libellé](https://docs.gitlab.com/ee/api/labels.html#create-a-new-label) dans la documentation de [!DNL GitLab].

+++

+++**[!UICONTROL Create a new pipeline]**

Ce module d’action crée un pipeline pour le projet donné.

Pour plus d’informations sur les champs, voir [Créer un pipeline](https://docs.gitlab.com/ee/api/pipelines.html#create-a-new-pipeline) dans la documentation de [!DNL GitLab].

+++

+++**[!UICONTROL Create a new release]**

Ce module d’action ajoute des notes de mise à jour à la balise git existante.

Pour plus d’informations sur les champs, voir [Créer une version](https://docs.gitlab.com/ee/api/releases/#create-a-release) dans la documentation de [!DNL GitLab].

+++

+++**[!UICONTROL Create a new tag]**

Ce module d’action crée une balise dans le référentiel qui renvoie à la référence fournie.

Pour plus d’informations sur les champs, voir [Créer une balise](https://docs.gitlab.com/ee/api/tags.html#create-a-new-tag) dans la documentation de [!DNL GitLab].

+++

+++**[!UICONTROL Create a todo]**

Ce module d’action crée une chose à faire pour la personne concernée sur le problème sélectionné. La personne concernée est la personne identifiée par les informations d’identification sur la connexion utilisée pour ce module.

Pour plus d’informations sur les champs, voir la section [Créer une chose à faire](https://docs.gitlab.com/ee/api/issues.html#create-a-todo) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Create a todo on a merge request]**

Ce module d’action crée une chose à faire pour la personne concernée sur la demande de fusion sélectionnée. La personne concernée est la personne identifiée par les informations d’identification sur la connexion utilisée pour ce module.

Pour plus d’informations sur les champs, voir [Créer une chose à faire](https://docs.gitlab.com/ee/api/merge_requests.html#create-a-todo) dans la documentation [!DNL GitLab]

+++

+++**[!UICONTROL Create merge request]**

Ce module d’action crée une nouvelle demande de fusion sur un projet.

Pour plus d’informations sur les champs, voir la section [Créer une demande de fusion](https://docs.gitlab.com/ee/api/merge_requests.html#create-mr) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Create new file in repository]**

Ce module d’action crée un fichier dans le référentiel sélectionné.

Pour plus d’informations sur les champs, voir la section [Créer un fichier dans le référentiel](https://docs.gitlab.com/ee/api/repository_files.html#create-new-file-in-repository) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Create new issue note]**

Ce module d’action crée une note de problème pour un problème de projet unique.

Pour plus d’informations sur les champs, voir la section [Créer une note de problème](https://docs.gitlab.com/ee/api/notes.html#create-new-issue-note) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Create new merge request note]**

Ce module d’action crée une note pour une seule demande de fusion.

Pour plus d’informations sur les champs, voir la section [Créer une note de demande de fusion](https://docs.gitlab.com/ee/api/notes.html#create-new-merge-request-note) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Create a new milestone]**

Ce module d’action crée un jalon pour un projet.

Pour plus d’informations sur les champs, voir la section [Créer un jalon](https://docs.gitlab.com/ee/api/milestones.html#create-new-milestone) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Create new snippet note]**

Ce module d’action crée une note pour un seul extrait de code. Les notes des extraits de code sont des commentaires que les utilisateurs et utilisatrices peuvent publier sur un extrait de code.

Pour plus d’informations sur les champs, voir la section [Créer une note d’extrait de code](https://docs.gitlab.com/ee/api/notes.html#create-new-snippet-note) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Create repository branch]**

Ce module d’action crée une seule branche de référentiel.

Pour plus d’informations sur les champs, voir la section [Créer une branche de référentiel](https://docs.gitlab.com/ee/api/branches.html#create-repository-branch) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Create build variable]**

Ce module d’action crée une variable de version.

Pour plus d’informations sur les champs, voir la section [Créer une variable](https://docs.gitlab.com/ee/api/project_level_variables.html#create-variable) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Delete a merge request]**

Ce module d’action est réservé aux administrateurs et administratrices et aux personnes propriétaires de projets. Il supprime la demande de fusion en question.

Pour plus d’informations sur les champs, voir la section [Supprimer une demande de fusion](https://docs.gitlab.com/ee/api/merge_requests.html#delete-a-merge-request) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Delete existing file in repository]**

Ce module d’action supprime un fichier existant du référentiel.

Pour plus d’informations sur les champs, voir la section [Supprimer un fichier existant du référentiel](https://docs.gitlab.com/ee/api/repository_files.html#delete-existing-file-in-repository) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Delete repository branch]**

Ce module d’action supprime une branche du référentiel.

Pour plus d’informations sur les champs, voir la section [Supprimer une branche du référentiel](https://docs.gitlab.com/ee/api/branches.html#delete-repository-branch) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Edit issue]**

Ce module d’action met à jour un problème de projet existant. Cet appel est également utilisé pour marquer la clôture d’un problème.

Pour plus d’informations sur les champs, voir la section [Modifier un problème](https://docs.gitlab.com/ee/api/issues.html#edit-issue) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Edit Milestone]**
Ce module d&#39;action met à jour un jalon de projet existant.

Pour plus d’informations sur les champs, voir la section [Modifier un jalon](https://docs.gitlab.com/ee/api/milestones.html#edit-milestone) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Erase a build]**

Ce module d’action efface une version d’un projet (supprime les artefacts et le log de traitement).

Pour plus d’informations sur les champs, voir [Effacer un traitement](https://docs.gitlab.com/ee/api/jobs.html#erase-a-job) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Get a list of todos]**

Ce module de recherche permet de récupérer une liste des choses à faire.

Pour plus d’informations sur les champs, voir [Obtenir une liste des choses à faire](https://docs.gitlab.com/ee/api/todos.html#get-a-list-of-todos) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Get a single build]**

Ce module d’action permet de récupérer un seul traitement d’un projet.

Pour plus d’informations sur les champs, voir [Obtenir un traitement unique](https://docs.gitlab.com/ee/api/jobs.html#get-a-single-job) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Get a single repository tag]**

Ce module d’action permet de récupérer une balise de référentiel spécifique déterminée par son nom.

Pour plus d’informations sur les champs, voir [Obtenir une balise de référentiel unique](https://docs.gitlab.com/ee/api/tags.html#get-a-single-repository-tag) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Get a specific deployment]**

Ce module d’action permet de récupérer un déploiement spécifique.

Pour plus d’informations sur les champs, voir [Obtenir un déploiement spécifique](https://docs.gitlab.com/ee/api/deployments.html#get-a-specific-deployment) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Get all issues assigned to a single milestone]**

Ce module de recherche permet de récupérer tous les problèmes affectés à un seul jalon du projet.

Pour plus d’informations sur les champs, voir [Obtenir tous les problèmes affectés à un seul jalon](https://docs.gitlab.com/ee/api/milestones.html#get-all-issues-assigned-to-a-single-milestone) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Get file from repository]**

Ce module d’action permet de récupérer des informations sur un fichier dans le référentiel, comme son nom, sa taille ou son contenu.

Pour plus d’informations sur les champs, voir [Obtenir un fichier du référentiel](https://docs.gitlab.com/ee/api/repository_files.html#get-file-from-repository) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Get project users]**

Ce module de recherche permet de récupérer les utilisateurs et utilisatrices du projet.

Pour plus d’informations sur les champs, voir [Obtenir les utilisateurs et utilisatrices du projet](https://docs.gitlab.com/ee/api/projects.html#get-project-users) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Get a single issue]**

Ce module d’action permet de récupérer les détails d’un problème.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour créer une connexion, voir <a href="#connect-gitlab-to-workfront-fusion" class="MCXref xref">[!UICONTROL Connect [!DNL GitLab] à Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project]</td> 
   <td> <p>Sélectionnez le projet qui contient le problème dont vous voulez récupérer les détails.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Issue ID]</td> 
   <td> <p>Saisissez ou mappez le nom du problème pour lequel vous souhaitez obtenir des détails.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL Get single issue note]**

Ce module d’action permet de récupérer une seule note pour un problème de projet spécifique.

Pour plus d’informations sur les champs, voir [Obtenir une note de problème unique](https://docs.gitlab.com/ee/api/notes.html#get-single-issue-note) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Get single merge request]**

Ce module d’action permet de récupérer des informations sur une requête de fusion unique.

Pour plus d’informations sur les champs, voir [Obtenir une requête de fusion unique](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Get single merge request changes]**

Ce module de recherche récupère des informations sur la requête de fusion, y compris ses fichiers et ses modifications.

Pour plus d’informations sur les champs, voir [Obtenir les modifications d’un requête de fusion unique](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr-changes) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Get single merge request commits]**

Ce module d’action permet de récupèrer une liste de engagements de requête de fusion.

Pour plus d’informations sur les champs, voir [Obtenir les engagements d’une requête de fusion unique](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr-commits) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Get single merge request note]**

Ce module d’action renvoie une note unique pour une demande de fusion donnée.

Pour plus d’informations sur les champs, voir [Obtenir une note pour une demande de fusion unique](https://docs.gitlab.com/ee/api/notes.html#get-single-merge-request-note) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Get a Milestone]**

Ce module d’action récupère les détails d’un jalon.

Pour plus d’informations sur les champs, voir [Obtenir un jalon unique](https://docs.gitlab.com/ee/api/milestones.html#get-single-milestone) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Get single project]**

Ce module d’action récupère les détails d’un projet.

Pour plus d’informations sur les champs, voir [Obtenir un projet unique](https://docs.gitlab.com/ee/api/projects.html#get-single-project) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Get single repository branch]**

Ce module d’action récupère les détails d’une branche de référentiel.

Pour plus d’informations sur les champs, voir [Obtenir une branche de référentiel unique](https://docs.gitlab.com/ee/api/branches.html#get-single-repository-branch) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Get snippet note]**

Ce module récupère une note unique pour un extrait de code donné.

Pour plus d’informations sur les champs, voir [Obtenir une note d’un extrait de code unique](https://docs.gitlab.com/ee/api/notes.html#get-single-snippet-note) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Get the comments of a commit]**

Ce module de recherche récupère les commentaires d’un engagement dans un projet.

Pour plus d’informations sur les champs, voir [Obtenir les commentaires d’un engagement](https://docs.gitlab.com/ee/api/commits.html#get-the-comments-of-a-commit) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Get the diff of a commit]**

Ce module d’action récupère le diff d’un engagement dans un projet.

Pour plus d’informations sur les champs, voir [Obtenir le diff d’un engagement](https://docs.gitlab.com/ee/api/commits.html#get-the-diff-of-a-commit) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Keep artifacts]**

Empêche la suppression des artefacts lorsque l’expiration est fixée.

Pour plus d’informations sur les champs, voir [Conserver les artefacts](https://docs.gitlab.com/ee/api/job_artifacts.html#keep-artifacts) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL List all merge request notes]**

Ce module de recherche permet d’obtenir une liste de toutes les notes relatives à une demande de fusion unique.

Pour plus d’informations sur les champs, voir [Répertorier toutes les notes de demande de fusion](https://docs.gitlab.com/ee/api/notes.html#list-all-merge-request-notes) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL List all snippet notes]**

Ce module permet d’obtenir une liste de toutes les notes pour un extrait de code unique. Les notes des extraits de code sont des commentaires que les utilisateurs et utilisatrices peuvent publier sur un extrait de code.

Pour plus d’informations sur les champs, voir [??](https://docs.gitlab.com/ee/api/notes.html#list-all-snippet-notes) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL List commit builds]**

Ce module de recherche renvoie une liste de versions pour un engagement spécifique dans un projet.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour créer une connexion, voir <a href="#connect-gitlab-to-workfront-fusion" class="MCXref xref">[!UICONTROL Connect [!DNL GitLab] à Workfront Fusion]</a> dans cet article.</td> 
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

+++**[!UICONTROL List issues]**

Ce module de recherche renvoie tous les problèmes en fonction des paramètres de filtrage spécifiés.

Pour plus d’informations sur les champs, voir [Répertorier les problèmes](https://docs.gitlab.com/ee/api/issues.html#list-issues) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL List Issues That Close on Merge]**

Ce module de recherche récupère tous les problèmes qui se clôtureraient par la fusion de la demande de fusion fournie.

Pour plus d’informations sur les champs, voir [Répertorier les problèmes qui seront clôturés lors de la fusion](https://docs.gitlab.com/ee/api/merge_requests.html#list-issues-that-will-close-on-merge) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL List Labels]**

Ce module de recherche permet de récuperer tous les libellés du projet.

Pour plus d’informations sur les champs, voir [Répertorier les libellés](https://docs.gitlab.com/ee/api/labels.html#list-labels) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL List merge requests]**

Ce module de recherche permet de récupérer toutes les demandes de fusion en fonction des paramètres de filtrage.

Pour plus d’informations sur les champs, voir la section [Répertorier les demandes de fusion](https://docs.gitlab.com/ee/api/merge_requests.html#list-merge-requests) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL List Owned Projects]**

Ce module de recherche permet de retrouver les projets dont la personne authentifiée est propriétaire.

Pour plus d’informations sur les champs, voir la section [Répertorier les projets des utilisateurs et utilisatrices](https://docs.gitlab.com/ee/api/projects.html#list-all-projects) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL List project builds]**

Ce module de recherche permet d’obtenir la liste des versions d’un projet.

Pour plus d’informations sur les champs, voir la section [Répertorier les traitements de projet](https://docs.gitlab.com/ee/api/jobs.html#list-project-jobs) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL List project deployments]**

Ce module de recherche permet d’obtenir une liste des déploiements dans un projet.

Pour plus d’informations sur les champs, voir la section [Répertorier les déploiements de projet](https://docs.gitlab.com/ee/api/deployments.html#list-project-deployments) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL List project issue notes]**

Ce module de recherche permet d’obtenir une liste de toutes les notes relatives à un problème donné.

Pour plus d’informations sur les champs, voir la section [Répertorier les notes sur les problèmes d’un projet](https://docs.gitlab.com/ee/api/notes.html#list-project-issue-notes) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL List project issues]**

Ce module de recherche renvoie tous les problèmes relatifs à un projet donné.

Pour plus d’informations sur les champs, voir la section [Répertorier les problèmes d’un projet](https://docs.gitlab.com/ee/api/issues.html#list-project-issues) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL List project milestones]**

Ce module de recherche permet de retrouver tous les jalons du projet.

Pour plus d’informations sur les champs, voir la section [Répertorier les jalons d’un projet](https://docs.gitlab.com/ee/api/milestones.html#list-project-milestones) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL List project pipelines]**

Ce module de recherche permet de retrouver tous les pipelines du projet.

Pour plus d’informations sur les champs, voir la section [Répertorier les pipelines d’un projet](https://docs.gitlab.com/ee/api/pipelines.html#list-project-pipelines) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL List project repository tags]**

Ce module de recherche permet de récupérer une liste des balises de référentiel d’un projet, triées par nom dans l’ordre alphabétique inverse.

Pour plus d’informations sur les champs, voir la section [Répertorier les balises de référentiel du projet](https://docs.gitlab.com/ee/api/tags.html#list-project-repository-tags) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL List project variables]**

Ce module de recherche permet d’obtenir la liste des variables d’un projet.

Pour plus d’informations sur les champs, voir la section [Répertorier les variables du projet](https://docs.gitlab.com/ee/api/project_level_variables.html#list-project-variables) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL List projects]**

Ce module de recherche permet de retrouver tous les projets dont la personne authentifiée est membre.

Pour plus d’informations sur les champs, voir la section [Répertorier tous les projets](https://docs.gitlab.com/ee/api/projects.html#list-all-projects) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL List repository branches]**

Ce module recherche les branches du référentiel en fonction du terme de recherche.

Pour plus d’informations sur les champs, voir la section [Répertorier les branches du référentiel](https://docs.gitlab.com/ee/api/branches.html#list-repository-branches) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL List repository commits]**

Ce module de recherche permet d’obtenir une liste des engagements du référentiel dans un projet.

Pour plus d’informations sur les champs, voir la section [Répertorier les engagements du référentiel](https://docs.gitlab.com/ee/api/commits.html#list-repository-commits) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL List repository contributors]**

Ce module de recherche permet d’obtenir la liste des contributeurs et contirbutrices d’un référentiel.

Pour plus d’informations sur les champs, voir la section [Contributeurs et contributrices](https://docs.gitlab.com/ee/api/repositories.html#contributors) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL List repository tree]**

Ce module de recherche permet d’obtenir une liste des fichiers et des répertoires du référentiel dans un projet.

Pour plus d’informations sur les champs, voir la section [Répertorier l’arborescence du référentiel](https://docs.gitlab.com/ee/api/repositories.html#list-repository-tree) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Mark a todo as done]**

Ce module d’action marque une chose à faire en attente donnée par son ID pour la personne concernée comme étant terminée.

Pour plus d’informations sur les champs, voir la section [Marquer une chose à faire comme terminée](https://docs.gitlab.com/ee/api/todos.html#mark-a-todo-as-done) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Modify existing issue note]**

Modifie une note existante d’un problème.

Pour plus d’informations sur les champs, voir la section [Modifier une note de problème existante](https://docs.gitlab.com/ee/api/notes.html#modify-existing-issue-note) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Modify existing merge request note]**

Modifie la note existante d’une demande de fusion.

Pour plus d’informations sur les champs, voir la section [Modifier une note de demande de fusion existante](https://docs.gitlab.com/ee/api/notes.html#modify-existing-merge-request-note) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Modify existing snippet note]**

Ce module d’action modifie une note existante d’un extrait de code.

Pour plus d’informations sur les champs, voir la section [Modifier une note d’extrait de code existante](https://docs.gitlab.com/ee/api/notes.html#modify-existing-snippet-note) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL New issue]**

Ce module d’action crée un problème de projet.

Pour plus d’informations sur les champs, voir la section [Nouveau problème](https://www.integromat.com/en/help/app/gitlab) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Play a build]**

Ce module d’action déclenche une action manuelle pour démarrer un traitement.

Pour plus d’informations sur les champs, voir la section [Lire un traitement](https://docs.gitlab.com/ee/api/jobs.html#play-a-job) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Post comment to commit]**

Ce module d’action ajoute un commentaire à un engagement.

Pour plus d’informations sur les champs, voir la section [Publier un commentaire sur l’engagement](https://docs.gitlab.com/ee/api/commits.html#post-comment-to-commit) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Remove variable]**

Ce module d’action supprime la variable d’un projet.

Pour plus d’informations sur les champs, voir la section [Supprimer la variable](https://docs.gitlab.com/ee/api/project_level_variables.html#remove-variable) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Retry a build]**

Ce module d’action réessaie une version unique dans un engagement.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour créer une connexion, voir <a href="#connect-gitlab-to-workfront-fusion" class="MCXref xref">[!UICONTROL Connect [!DNL GitLab] à Workfront Fusion]</a> dans cet article.</td> 
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

+++**[!UICONTROL Retry Failed Jobs in a Pipeline]**

Ce module d’action retente les versions qui ont échoué dans un pipeline.

Pour plus d’informations sur les champs, voir la section [Réessayer des traitements dans un pipeline](https://docs.gitlab.com/ee/api/pipelines.html#retry-jobs-in-a-pipeline) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Get a Variable]**

Ce module permet d’obtenir les détails d’une variable spécifique d’un projet.

Pour plus d’informations sur les champs, voir la section [Afficher les détails de la variable](https://docs.gitlab.com/ee/api/project_level_variables.html#show-variable-details) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Update a release]**

Ce module d’action met à jour une version.

Pour plus d’informations sur les champs, voir la section [Mettre à jour une version](https://docs.gitlab.com/ee/api/releases/#update-a-release) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Update merge request]**

Ce module d’action met à jour une demande de fusion existante. Vous pouvez modifier la branche cible, le titre ou même fermer la demande de fusion.

Pour plus d’informations sur les champs, voir la section [Mettre à jour une demande de fusion](https://docs.gitlab.com/ee/api/merge_requests.html#update-mr) dans la documentation [!DNL GitLab].

+++

+++**[!UICONTROL Update a Variable]**

Ce module d’action met à jour la variable d’un projet.

Pour plus d’informations sur les champs, voir la section [Mettre à jour une variable](https://docs.gitlab.com/ee/api/project_level_variables.html#update-variable) dans la documentation [!DNL GitLab].

+++
