---
title: Modules Azure DevOps
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent  [!DNL Azure DevOps], et le connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: c0919a9a-ce99-485c-9627-45353741f6d8
TQID: https://experienceleague.adobe.com/RFI6MFgF-C1Cnn0bvjOLVf3qahyRblEp4dtypNrxqzE
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: b58ad82f-df6b-4b01-81a3-3a02ab9567a0
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 0b7298ce53bf59695ce52cb46cb8d25b6ede5fc8
workflow-type: tm+mt
source-wordcount: 2645
ht-degree: 58%

---

# Modules [!DNL Azure DevOps]

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent [!DNL Azure DevOps] et le connecter à plusieurs applications et services tiers.

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
   <p>Basé sur les opérations : disponible pour les organisations disposant de licences basées sur les opérations</p>
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

Pour utiliser les modules [!DNL Azure DevOps], vous devez disposer d’un compte [!DNL Azure] DevOps.

## Informations sur l’API [!DNL Azure DevOps]

Le connecteur DevOps d’Azure utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Version de l’API</td> 
   <td> v5.1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.29.33</td> 
  </tr>
 </tbody> 
</table>

## Connecter [!DNL Azure DevOps] à Workfront Fusion {#connect-azure-devops-to-workfront-fusion}

* [Connexion d’Azure DevOps à Workfront Fusion à l’aide d’EntraApp](#connect-azure-devops-to-workfront-fusion-using-entraapp)
* [Connecter les opérations de développement Azure à Workfront Fusion à l’aide d’un principal de service](#connect-azure-devops-to-workfront-fusion-using-a-service-principal)

### Connexion d’Azure DevOps à Workfront Fusion à l’aide d’EntraApp

1. Ajoutez un module [!DNL Azure DevOps] à votre scénario.
1. Cliquez sur **[!UICONTROL Ajouter]** à côté du champ [!UICONTROL Connexion].
1. Dans le champ [!UICONTROL Type de connexion], sélectionnez le type de connexion à utiliser.

   >[!NOTE]
   >
   >Le [!UICONTROL [!DNL Azure DevOps] (EntraApp)] vous permet de demander toutes les portées de la connexion.

1. Remplissez les champs suivants :

   <table style="table-layout:auto">
      <tr>
            <td>[!UICONTROL Connection name]</td>
            <td>Saisissez un nom pour la connexion que vous créez.</td>
      </tr>
      <tr>
            <td>[!UICONTROL Organization]</td>
            <td>Saisissez le nom de l’organisation dans laquelle vous avez créé votre application [!DNL Azure DevOps].</td>
      </tr>
      <tr>
            <td>[!UICONTROL App ID]</td>
            <td>Saisissez l’identifiant de l’application DevOps à laquelle vous vous connectez.</td>
      </tr>
      <tr>
            <td>[!UICONTROL Client Secret]</td>
            <td>Saisissez le secret client pour les applications DevOps auxquelles vous vous connectez.</td>
      </tr>
      <tr>
            <td>[!UICONTROL Demander toutes les portées]</td>
            <td>Si vous utilisez le type de connexion [!DNL Azure DevOps] (EntraApp) , activez cette option pour demander toutes les portées de la connexion.</td>
      </tr>
   </table>

1. Pour saisir un ID d’application DevOps Azure ou un secret client, cliquez sur <b>Afficher les paramètres avancés</b> et saisissez-les dans les champs qui s’ouvrent.
1. Cliquez sur **[!UICONTROL Continuer]** pour terminer la configuration de la connexion et poursuivre la création de votre scénario.

### Connecter les opérations de développement Azure à Workfront Fusion à l’aide d’un principal de service

Vous pouvez créer une connexion qui utilise un principal de service (une connexion API d’application) au lieu d’un compte personnel. Cela s’avère utile lorsque vous souhaitez que la connexion s’exécute en tant qu’identité d’application ou de service plutôt qu’en tant que personne spécifique. Cela peut s’avérer utile pour que l’intégration ne se rompe pas si, par exemple, cette personne quitte l’entreprise ou modifie son mot de passe.

Ce type de connexion est disponible pour tous les modules DevOps d’Azure.

>[!NOTE]
>
>L’authentification principale du service ne prend pas en charge toutes les fonctionnalités DevOps d’Azure. Un petit nombre d’actions au niveau administrateur, telles que la gestion des licences utilisateur, nécessitent toujours une connexion à un compte personnel. Utilisez l’authentification principale du service si vous n’en avez besoin que pour les éléments de travail, les tableaux, les référentiels ou les pipelines.

* [Conditions préalables à la connexion d’Azure DevOps à Workfront Fusion à l’aide d’un principal de service](#prerequisites-to-connecting-azure-devops-to-workfront-fusion-using-a-service-principal)
* [Création de l’enregistrement de l’application dans l’ID Microsoft Entra](#create-the-app-registration-in-microsoft-entra-id)
* [Créer un secret client](#create-a-client-secret)
* [Collecter les détails de votre connexion](#collect-your-connection-details)
* [Ajoutez le principal de service à votre organisation DevOps Azure](#add-the-service-principal-to-your-azure-devops-organization)
* [Créer la connexion](#create-the-connection)

#### Conditions préalables à la connexion d’Azure DevOps à Workfront Fusion à l’aide d’un principal de service

Pour créer cette connexion, vous avez besoin des éléments suivants :

* **Accès administrateur global** ou **administrateur de l’application** dans l’ID d’entrée Microsoft, pour enregistrer l’application. Si vous ne disposez pas de cet accès, demandez à un membre de votre équipe informatique ou d’identité de terminer cette étape pour vous.
* **Administrateur de la collecte de projets** accédez à votre organisation DevOps Azure pour ajouter le principal de service en tant que membre. Il s’agit souvent d’une personne différente de celle qui gère l’identifiant Microsoft Entra.
* Nom de votre organisation Azure DevOps. Vous pouvez le retrouver dans votre URL DevOps Azure : `dev.azure.com/<your organization name>`.

#### Création de l’enregistrement de l’application dans l’ID Microsoft Entra

1. Connectez-vous au centre d’administration [!DNL Microsoft Entra].
1. Accédez à **[!UICONTROL Enregistrements des applications]** > **[!UICONTROL Nouvel enregistrement]**.
1. Donnez à l’application un nom clair et reconnaissable. Par exemple, `Workfront Fusion Azure DevOps Integration`.
1. Laissez le champ **[!UICONTROL URI de redirection]** vide. Cette connexion n’implique pas de connexion via un navigateur.
1. Sélectionnez **[!UICONTROL Enregistrer]**.
1. Passez à [Créer un secret client](#create-a-client-secret).

#### Créer un secret client

1. Dans l’enregistrement de votre nouvelle application, accédez à **[!UICONTROL Certificats et secrets]**.
1. Sélectionnez **[!UICONTROL Nouveau secret client]**, ajoutez une description, puis choisissez une période d’expiration.
1. Sélectionnez **[!UICONTROL Ajouter]**.
1. Copiez immédiatement la **[!UICONTROL valeur]** du secret. Il s’affiche une seule fois. Si vous quittez cette page avant de la copier, vous devez en créer une nouvelle.
1. Continuez pour [Collecter les détails de votre connexion](#collect-your-connection-details).

#### Collecter les détails de votre connexion

1. Sur la page **[!UICONTROL Aperçu]** de l’enregistrement de l’application, notez les valeurs suivantes. Vous les saisissez lors de la création de la connexion dans le module .

   <table style="table-layout:auto">
    <col>
    <col>
    <tbody>
     <tr>
      <td role="rowheader">[!UICONTROL Tenant ID]</td>
      <td>Sur la page Aperçu , intitulé <b>ID de répertoire (client)</b>.</td>
      </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Client ID]</td>
      <td>Sur la page Aperçu , intitulé <b>ID d’application (client)</b>.</td>
     </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Client Secret]</td>
      <td>Valeur copiée dans <a href="#create-a-client-secret" class="MCXref xref">Créer un secret client</a>.</td>
     </tr>
     <tr>
      <td role="rowheader">[!UICONTROL Organization]</td>
      <td>Nom de votre organisation Azure DevOps. Par exemple, si votre URL est <code>dev.azure.com/yourorg</code>, saisissez <code>yourorg</code>.</td>
     </tr>
    </tbody>
   </table>

   >[!NOTE]
   >
   >Vous pouvez ignorer la zone **Autorisations API** de l’enregistrement de l’application. Si vous y ajoutez des opérations de développement Azure, seules les **autorisations déléguées** sont disponibles. Les **Autorisations d’application** apparaissent grisées. Cela est normal, car les opérations de développement Azure ne prennent pas en charge l’octroi d’accès de cette manière. Au lieu de cela, l’accès est accordé directement dans les DevOps Azure, dans la partie suivante.

1. Passez à [Ajouter le principal de service à votre organisation DevOps Azure](#add-the-service-principal-to-your-azure-devops-organization).

#### Ajoutez le principal de service à votre organisation DevOps Azure

L’enregistrement de l’application dans Microsoft Entra ID crée uniquement son identité. L’application n’a pas encore accès à vos données DevOps Azure. Cette procédure permet d’accorder cet accès.

1. Connectez-vous à votre organisation Azure DevOps à l’adresse `dev.azure.com/<your organization name>`.
1. Sélectionnez **[!UICONTROL Paramètres de l’organisation]** dans le coin inférieur gauche, puis sélectionnez **[!UICONTROL Utilisateurs]**.
1. Sélectionnez **[!UICONTROL Ajouter des utilisateurs]**.
1. Dans la zone de recherche, effectuez une recherche en fonction du nom d’affichage de l’application, qui est le nom que vous lui avez donné lors de son enregistrement. Ne pas effectuer de recherche par ID client.
1. Sélectionner un niveau d&#39;accès :

   * **[!UICONTROL De base]** est généralement suffisant pour lire et écrire des éléments de travail, des tableaux et des référentiels.
   * Si votre workflow doit parcourir les processus disponibles, tels que les modèles Agile, Scrum ou personnalisés, dans le cadre de la configuration, ajoutez plutôt le principal de service au groupe **[!UICONTROL Administrateurs de collection de projets]**. Il s’agit d’un niveau d’accès plus large, donc n’accordez-le que si vous avez besoin de cette fonctionnalité.

1. Attribuez le principal de service au ou aux projets spécifiques dont il a besoin, en suivant les pratiques d’accès habituelles de votre entreprise.
1. Sélectionnez **[!UICONTROL Ajouter]**.
1. Passez à [&#x200B; Créer la connexion &#x200B;](#create-the-connection).

#### Créer la connexion

1. Dans l’écran de configuration de la connexion du module, sélectionnez le type de connexion **[!UICONTROL Principal de service]**.
1. Saisissez les informations suivantes :

   * [!UICONTROL ID de client]
   * [!UICONTROL Identifiant du client]
   * [!UICONTROL Secret du client]
   * [!UICONTROL Organisation]

1. Enregistrez la connexion.

   Si tout est correctement configuré, la connexion est validée avec succès.

## Modules [!UICONTROL Azure DevOps] et leurs champs

Lorsque vous configurez les modules [!DNL Azure DevOps], Workfront Fusion affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Azure DevOps] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, consultez [Mappage d’informations d’un module à l’autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Bouton (bascule) de mappage](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Déclencheurs](#triggers)
* [Actions](#actions)
* [Recherches](#searches)

### Déclencheurs

#### [!UICONTROL Surveiller des éléments de travail]

Ce module de déclenchement instantané exécute un scénario lorsqu’un enregistrement est ajouté, mis à jour ou supprimé dans [!UICONTROL Azure DevOps].

Le module renvoie tous les champs standard associés à l’enregistrement, ainsi que tous les champs et valeurs personnalisés auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Sélectionnez ou ajoutez un webhook pour le module.</p> <p>Pour plus d’informations sur les webhooks dans les modules de déclenchement, voir <a href="/help/workfront-fusion/references/modules/webhooks-reference.md" class="MCXref xref">Déclencheurs instantanés (webhooks)</a>.</p> <p>Pour plus d’informations sur la création d’un webhook, voir <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md" class="MCXref xref">Webhooks</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [Créer un enregistrement](#create-a-record)
* [Appel API personnalisé](#custom-api-call)
* [Télécharger une pièce jointe](#download-an-attachment)
* [Lier des éléments de travail](#link-work-items)
* [Lire l’enregistrement](#read-record)
* [Mettre à jour un élément de travail](#update-a-work-item)
* [[!UICONTROL Charger une pièce jointe]](#upload-an-attachment)

#### [!UICONTROL Créer un enregistrement]

Ce module d’action crée un projet ou un élément de travail.

Le module génère l’ID de l’objet pour l’élément de travail nouvellement créé, ou l’URL et le code d’état d’un projet nouvellement créé.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Azure DevOps] à Workfront Fusion, voir <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Azure DevOps] à [!UICONTROL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Sélectionnez si vous souhaitez créer un élément de travail ou un projet.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Project]</strong> </p> <p>Remplissez les champs suivants :</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Name]</strong> : saisissez ou mappez un nom pour le nouveau projet.</p> </li> 
       <li> <p><strong>[!UICONTROL Description]</strong> : saisissez ou mappez une description pour le nouveau projet. </p> </li> 
       <li> <p><strong>[!UICONTROL Visibility]</strong> : sélectionnez si vous souhaitez que votre projet soit public ou privé. Les utilisateurs et utilisatrices doivent être connectés à votre organisation et avoir reçu l’autorisation d’accéder au projet pour pouvoir interagir avec un projet privé. Les projets publics sont visibles par les utilisateurs et utilisatrices qui ne sont pas connectés à votre organisation.</p> </li> 
       <li> <p><strong>[!UICONTROL Version control]</strong> : indiquez si vous souhaitez que le projet utilise [!DNL Git] ou [!UICONTROL Team Foundation Version Control (TFCV)] pour la gestion de versions.</p> </li> 
       <li> <p><strong>[!UICONTROL Work item process]</strong> : sélectionnez le processus de travail que vous souhaitez utiliser pour le projet. Les options sont [!UICONTROL Basic], [!UICONTROL Scrum], [!UICONTROL Capability Maturity Model Integration (CMMI)] et [!UICONTROL Agile].</p> <p>Pour plus d’informations sur les processus [!DNL Azure DevOps], voir <a href="https://learn.microsoft.com/fr-fr/azure/devops/boards/work-items/guidance/choose-process?view=azure-devops&tabs=basic-process">Processus par défaut et modèles de processus</a> dans la documentation [!DNL Azure DevOps].</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Work item]</strong> </p> <p>Remplissez les champs suivants :</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Project]</strong> : sélectionnez le projet dans lequel vous souhaitez créer l’élément de travail.</p> </li> 
       <li> <p><strong>[!UICONTROL Work item type]</strong> : sélectionnez le type d’élément de travail que vous souhaitez créer.</p> </li> 
       <li> <p><strong>[!UICONTROL Autres champs]</strong> : dans ces champs, saisissez la valeur que vous souhaitez que l’élément de travail ait pour une propriété donnée. Les champs disponibles dépendent du type d’élément de travail.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Appel API personnalisé]

Ce module d’action vous permet d’effectuer un appel personnalisé et authentifié vers l’API [!DNL Azure DevOps]. Ainsi, vous pouvez créer une automatisation du flux de données qui ne peut pas être réalisée par les autres modules [!DNL Azure DevOps].

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Azure DevOps] à Workfront Fusion, voir <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Azure DevOps] à [!UICONTROL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Base URL]</td> 
   <td> <p>Sélectionner ou mapper l’URL de base que vous utilisez pour vous connecter à votre compte [!DNL Azure DevOps].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Relative URL]</td> 
   <td> <p>Saisissez l’URL relative à laquelle vous souhaitez vous connecter pour cet appel API.</p> <p><b>Exemple : </b><code>{organization}/_apis[/{area}]/{resource}</code> </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL API Version]</td> 
   <td>Sélectionnez ou mappez la version de l’API [!DNL Azure DevOps] à laquelle vous souhaitez vous connecter pour cet appel API. Si aucune version n’est sélectionnée, Workfront Fusion se connecte à la version 5.1 de l’API [!DNL Azure DevOps].</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, consultez <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Ajoutez la requête pour l’appel API sous la forme d’un objet JSON standard.</p> <p>Par exemple : <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre JSON, placez les guillemets à l’extérieur de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Télécharger une pièce jointe]

Ce module d’action télécharge une pièce jointe.

Le module renvoie le contenu du fichier de la pièce jointe.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Azure DevOps] à Workfront Fusion, voir <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Azure DevOps] à [!UICONTROL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Attachment URL]</td> 
   <td> <p>Saisissez ou mappez l’URL de la pièce jointe que vous souhaitez télécharger.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Lier des éléments de travail]

Ce module d’action lie deux éléments de travail et définit la relation entre eux.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Azure DevOps] à Workfront Fusion, voir <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Azure DevOps] à [!UICONTROL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Work item ID]</td> 
   <td>Saisissez ou mappez l’ID de l’élément de travail principal auquel vous souhaitez lier un autre élément de travail.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Linked work item ID]</td> 
   <td>Saisissez ou mappez l’ID de l’élément de travail que vous souhaitez lier à l’élément de travail principal.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Link Type]</td> 
   <td> <p>Définissez la relation entre les éléments de travail que vous souhaitez lier.</p> <p>Pour plus d’informations, consultez le <a href="https://learn.microsoft.com/fr-fr/azure/devops/boards/queries/link-type-reference?view=azure-devops">Guide de référence pour les types de liens</a> dans la documentation [!UICONTROL Azure DevOps].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment]</td> 
   <td>Saisir ou mapper le texte d’un commentaire. Ceci est utile pour expliquer le raisonnement ou l’intention du lien.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Lire l’enregistrement]

Ce module d’action lit les données d’un seul enregistrement dans [!DNL Azure DevOps].

Vous indiquez l’ID de l’enregistrement.

Le module renvoie l’identifiant de l’enregistrement et de tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Azure DevOps] à Workfront Fusion, voir <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Azure DevOps] à [!UICONTROL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Sélectionner si vous voulez lire un projet ou un élément de travail.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Project]</strong> : sélectionnez le projet que vous souhaitez lire.</p> </li> 
     <li> <p><strong>[!UICONTROL Work item]</strong> : sélectionnez le projet qui contient l’élément de travail que vous souhaitez lire, puis sélectionnez le type d’élément de travail.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Sélectionnez les informations que vous souhaitez inclure dans le bundle de sortie pour ce module. Les champs disponibles dépendent du type d’élément de travail.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Saisissez ou mappez l’identifiant de l’enregistrement que vous souhaitez lire.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mettre à jour un élément de travail]

Ce module d’action met à jour un élément de travail existant à l’aide de son identifiant.

Le module renvoie l’identifiant de l’élément de travail mis à jour.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Azure DevOps] à Workfront Fusion, voir <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Azure DevOps] à [!UICONTROL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project]</td> 
   <td>Sélectionnez le projet qui contient l’élément de travail que vous souhaitez mettre à jour.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Work Item Type]</td> 
   <td> <p>Sélectionnez le type d’élément de travail que vous souhaitez mettre à jour.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Other Fields]</td> 
   <td>Dans chacun de ces champs, saisissez la valeur que vous souhaitez donner à l’élément de travail pour une propriété donnée. Les champs disponibles dépendent du type d’élément de travail.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Work item ID]</td> 
   <td>Saisissez ou mappez l’ID de l’élément de travail que vous souhaitez mettre à jour.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Charger une pièce jointe]

Ce module d’action permet de charger un fichier et de le joindre à un élément de travail.

Le module renvoie l’ID de la pièce jointe et l’URL de téléchargement de la pièce jointe.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Azure DevOps] à Workfront Fusion, voir <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Azure DevOps] à [!UICONTROL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project] </td> 
   <td> <p>Sélectionnez le projet dans lequel vous souhaitez charger une pièce jointe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Work item ID]</td> 
   <td> <p>Saisissez ou mappez l’ID de l’élément de travail dans lequel vous souhaitez charger une pièce jointe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment]</td> 
   <td>Saisissez le texte d’un commentaire que vous souhaitez ajouter à la pièce jointe chargée.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file] </td> 
   <td>Sélectionnez un fichier source à partir d’un module précédent, ou saisissez ou mappez le nom et le contenu du fichier source.</td> 
  </tr> 
 </tbody> 
</table>

### Recherches

#### [!UICONTROL Répertorier des éléments de travail]

Ce module d’action récupère tous les éléments de travail d’un type spécifique dans un projet [!DNL Azure DevOps].

Le module renvoie l’ID de l’élément de travail principal et tous les champs associés, ainsi que tous les champs et valeurs personnalisés auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Azure DevOps] à Workfront Fusion, voir <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Azure DevOps] à [!UICONTROL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project]</td> 
   <td>Sélectionnez le projet dont vous souhaitez récupérer les éléments de travail.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Work item type]</td> 
   <td> <p>Sélectionnez le type d’élément de travail que vous souhaitez récupérer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Sélectionnez les propriétés à afficher dans la sortie du module. Les champs disponibles dépendent du type d’élément de travail que vous souhaitez récupérer. Vous devez sélectionner au moins une propriété.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Saisissez ou mappez le nombre maximal d’éléments de travail que Workfront Fusion renvoie au cours d’un cycle d’exécution.</td> 
  </tr> 
 </tbody> 
</table>
