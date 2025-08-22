---
title: Modules Box
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent Box et les connecter à plusieurs applications et services tiers. Il surveille un dossier spécifié pour vérifier les modifications de fichier, modifier et supprimer des fichiers existants ou charger de nouveaux fichiers dans un dossier.
author: Becky
feature: Workfront Fusion
exl-id: 9e741dce-05a6-4e13-8d58-fbe3b4900d7e
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1542'
ht-degree: 28%

---

# Modules Box

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent [!DNL Box] et les connecter à plusieurs applications et services tiers. Il surveille un dossier spécifié pour vérifier les modifications de fichier, modifier et supprimer des fichiers existants ou charger de nouveaux fichiers dans un dossier.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

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

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Conditions préalables

Pour utiliser les modules [!DNL Box], vous devez disposer d’un compte [!DNL Box].

## Informations sur l’API Box

Le connecteur Box utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td> https://api.box.com/2.0
    </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Version de l’API</td> 
   <td> v2.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v3.0.3</td> 
  </tr>
 </tbody> 
 </table>

## Modules [!DNL Box] et leurs champs

Lorsque vous configurez les modules [!DNL Box], Workfront Fusion affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Box] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Déclencheurs](#triggers)
* [Actions](#actions)
* [Recherches](#searches)

### Déclencheurs

* [[!UICONTROL Nouvel événement de fichier]](#new-file-event)
* [Nouvel événement de dossier](#new-folder-event)
* [[!UICONTROL Surveiller des fichiers]](#watch-files)

#### [!UICONTROL Nouvel événement de fichier]

Ce module de déclenchement instantané lance un scénario lorsqu’une action sélectionnée se produit sur un fichier.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Sélectionnez le webhook que vous souhaitez utiliser pour regarder les messages sortants ou ajoutez un webhook. </p><p>Pour ajouter un webhook, cliquez sur <strong>[!UICONTROL Add]</strong> et saisissez le nom et la connexion du webhook, le fichier à surveiller et les déclencheurs à surveiller.</p> <p> Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Box] à [!UICONTROL Workfront Fusion], consultez <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Connexion à un service - Instructions de base</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Nouvel événement de dossier

Ce module de déclenchement instantané lance un scénario lorsque l’action de sélection se produit dans le dossier .

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Sélectionnez le webhook que vous souhaitez utiliser pour regarder les messages sortants ou ajoutez un webhook. </p><p>Pour ajouter un webhook, cliquez sur <strong>[!UICONTROL Add]</strong> et saisissez le nom et la connexion du webhook, le dossier à surveiller et les déclencheurs à surveiller.</p> <p> Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Box] à [!UICONTROL Workfront Fusion], consultez <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Connexion à un service - Instructions de base</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Surveiller des fichiers]

Ce module de déclenchement lance un scénario lorsqu’un nouveau fichier est ajouté ou qu’un fichier existant est mis à jour dans un dossier surveillé.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Box] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  <tr> 
   <td role="rowheader">Observer dans le dossier</td> 
   <td> <p>Sélectionnez le dossier que vous souhaitez observer. Un scénario peut surveiller un seul dossier.</p> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Surveiller</td> 
   <td> <p>Sélectionnez le type de fichiers à surveiller.</p> 
    <ul> 
     <li> <p><strong>Nouveaux fichiers uniquement</strong> </p> <p>Le scénario démarre lorsqu’un nouveau fichier est ajouté.</p> </li> 
     <li> <p><strong>Nouveaux fichiers et toutes les modifications</strong> </p> <p>Le scénario démarre lorsqu’un fichier est ajouté ou lorsque le contenu ou l’attribut d’un fichier (son nom, par exemple) est modifié.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Nombre maximal de fichiers téléchargés</p> </td> 
   <td> <p>Saisissez le nombre maximal de fichiers que le module doit renvoyer à chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

<!--* [[!UICONTROL Delete a file]](#delete-a-file)
* [[!UICONTROL Get a file]](#get-a-file)
* [[!UICONTROL Update a file]](#update-a-file)
* [[!UICONTROL Upload] a file](#upload-a-file)-->
* [Créer un dossier](#create-a-folder)
* [Obtenir un dossier](#get-a-folder)
* [Obtenir les métadonnées du dossier](#get-folder-metadata)
* [Effectuer un appel API](#make-an-api-call)
* [Mettre à jour les métadonnées de dossier](#update-folder-metadata)

<!--#### [!UICONTROL Delete a file] 

This action module deletes a file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Enter or map the unique ID of the file that you want the module to delete.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a file]

This action module downloads a file.

You specify the ID of the file.

>[!NOTE]
>
>This module is useful for providing files to subsequent modules.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Enter or map the unique ID of the file that you want the module to retrieve.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a file] 

This action module updates a file.

You specify the ID of the file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Enter or map the unique ID of the file that you want the module to update.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file] 

This action module uploads a file.

You specify the file. You can also provide a new filename for the file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Select the folder where you want to upload the file.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>If this module is not successful, consider the following:
>
>* The size of the file might exceed the maximum file size limit for your [!DNL Box] plan, or you may have used all of your [!DNL Box] account's storage quota. To get more storage space, delete existing files from [!DNL Box] or upgrade your [!DNL Box] account.
>* [!DNL Box] does not upload more than one files with the same name to a single folder. If the destination folder contains a file with the same name as the file being uploaded, the scenario run terminates with an error. To avoid this, rename the file. If you want to update the file, use the **[!UICONTROL Update a file]** module.-->

#### Créer un dossier

Ce module d’action crée un dossier vide dans le dossier parent spécifié.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Box] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td> <p>Saisissez ou mappez un nom pour le nouveau dossier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent Folder]</td> 
   <td> <p>Sélectionnez le dossier dans lequel vous souhaitez créer le nouveau dossier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder Upload Email Access]</td> 
   <td> <p>Lorsque ce paramètre a été défini, les utilisateurs peuvent envoyer des fichiers par e-mail à l’adresse e-mail qui a été automatiquement créée pour ce dossier. Les options de collaborateurs permettent uniquement les e-mails enregistrés pour les collaborateurs.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Synchronization State]</td> 
   <td> <p>Indique si un dossier doit être synchronisé ou non avec l’appareil d’un utilisateur. Il est utilisé par Box Sync (arrêté) et n'est pas utilisé par Box Drive.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Obtenir un dossier

Ce module d’action récupère les détails d’un dossier, y compris les 100 premières entrées du dossier.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Box] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Sélectionnez le dossier pour lequel vous souhaitez récupérer des détails.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Obtenir les métadonnées du dossier

Ce module d’action récupère les métadonnées du dossier par ID de dossier.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Box] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scope]</td> 
   <td> <p>Sélectionnez l’étendue à utiliser pour cette récupération des métadonnées.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Sélectionnez le dossier pour lequel vous souhaitez récupérer les métadonnées.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Effectuer un appel API

Ce module d&#39;action effectue un appel personnalisé à l&#39;API Box.



<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL Bynder] à Workfront Fusion, voir <a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Bynder] à Workfront Fusion </a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Saisir un chemin relatif à <code>https://api.box.com</code>. <p>Exemple : <code>/2.0/users/me</code></p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple : <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion ajoute les en-têtes d’autorisation pour vous.</p> </td> 
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

#### Mettre à jour les métadonnées de dossier

Ce module d’action crée ou met à jour les métadonnées d’un dossier.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Box] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scope]</td> 
   <td> <p>Sélectionnez l’étendue à utiliser pour cette mise à jour des métadonnées.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Sélectionnez le dossier pour lequel vous souhaitez mettre à jour les métadonnées.</p> </td> 
  </tr> 
 </tbody> 
</table>


### Recherches

#### Recherche de contenu

Ce module de recherche recherche les éléments disponibles pour l’utilisateur ou l’entreprise dans son ensemble.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Box] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td> <p>Saisissez ou mappez la chaîne à rechercher. Cette requête est mise en correspondance avec les noms d'éléments, les descriptions, le contenu textuel des fichiers et divers autres champs des différents types d'éléments.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scope]</td> 
   <td> <p>Choisissez si vous recherchez du contenu associé à l’utilisateur dont les informations d’identification sont utilisées pour la connexion utilisée dans ce module, ou si vous recherchez du contenu associé à l’ensemble de l’entreprise.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td> <p>Choisissez si vous recherchez des fichiers, des dossiers ou des liens web.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort]</td> 
   <td> <p>Choisissez si vous souhaitez trier par pertinence ou par date de modification.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Trash Content]</td> 
   <td> <p>Choisissez si vous souhaitez rechercher du contenu saccagé ou du contenu qui n’a pas été saccagé.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID de dossier parent]</td> 
   <td> <p>Pour effectuer une recherche dans un dossier spécifique, pour chaque dossier à rechercher, cliquez sur <b>Ajouter un élément</b> et saisissez l’identifiant du dossier. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Créé À Partir De]</td> 
   <td> <p>Pour rechercher des ressources créées dans une certaine période, saisissez la date la plus proche dans la période.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Created to]</td> 
   <td> <p>Pour rechercher des ressources créées dans une certaine période, saisissez la dernière date de la période.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mis À Jour À Partir De]</td> 
   <td> <p>Pour rechercher des ressources mises à jour dans une certaine période, saisissez la date la plus proche dans la période.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mise à jour vers]</td> 
   <td> <p>Pour rechercher des ressources mises à jour dans une certaine période, saisissez la dernière date de la période.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>Pour chaque attribut que vous souhaitez renvoyer dans la réponse du module, cliquez sur <b>Ajouter un élément</b> et saisissez le champ .</p><p>Vous pouvez l’utiliser pour demander des champs qui ne sont normalement pas renvoyés dans une réponse standard. Notez que la spécification de ce paramètre a pour effet qu’aucun des champs standard n’est renvoyé dans la réponse, sauf indication explicite. </p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File Extensions]</td> 
   <td> <p>Pour limiter la recherche à des extensions de fichier spécifiques, entrez une liste d’extensions de fichier séparées par des virgules.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size From]</td> 
   <td> <p>Pour rechercher des ressources dans une plage de tailles spécifique, saisissez la petite extrémité de la plage, en octets.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Size To]</td> 
   <td> <p>Pour rechercher des ressources dans une plage de tailles spécifique, saisissez l’extrémité la plus grande de la plage, en octets.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Owner ID]</td> 
   <td> <p>Pour rechercher des ressources appartenant à des utilisateurs spécifiques, saisissez une liste d’ID de propriétaire séparés par des virgules.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal de résultats que le module doit renvoyer dans chaque cycle d'exécution.</p> </td> 
  </tr> 
 </tbody> 
</table>


