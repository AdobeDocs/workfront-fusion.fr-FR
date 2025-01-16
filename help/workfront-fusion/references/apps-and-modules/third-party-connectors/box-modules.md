---
title: Modules Box
description: Dans un scénario  [!DNL Adobe Workfront Fusion] , vous pouvez automatiser les workflows qui utilisent Box et le connecter à plusieurs applications et services tiers. Il surveille un dossier spécifié pour vérifier les modifications de fichier, modifier et supprimer des fichiers existants ou charger de nouveaux fichiers dans un dossier.
author: Becky
feature: Workfront Fusion
exl-id: 9e741dce-05a6-4e13-8d58-fbe3b4900d7e
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '993'
ht-degree: 79%

---

# Modules Box

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!DNL Box] et le connecter à plusieurs applications et services tiers. Il surveille un dossier spécifié pour vérifier les modifications de fichier, modifier et supprimer des fichiers existants ou charger de nouveaux fichiers dans un dossier.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

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

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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

Lorsque vous configurez les modules [!DNL Box], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Box] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Déclencheurs

* [[!UICONTROL New event]](#new-event)
* [[!UICONTROL Watch files]](#watch-files)

#### [!UICONTROL New event]

Ce module de déclenchement instantané lance un scénario lorsqu’un fichier est ajouté, déplacé, copié, supprimé, verrouillé ou déverrouillé.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Sélectionnez le webhook que vous souhaitez utiliser pour surveiller les messages sortants. Pour ajouter un webhook, cliquez sur <strong>[!UICONTROL Add]</strong> et saisissez le nom et la connexion du webhook.</p> <p> Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Box] à [!UICONTROL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Connexion à un service - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Maximum number of returned events]</p> </td> 
   <td> <p>Saisissez le nombre maximal d’événements que le module doit renvoyer à chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch files]

Ce module de déclenchement lance un scénario lorsqu’un nouveau fichier est ajouté ou qu’un fichier existant est mis à jour dans un dossier surveillé.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Box] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
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

* [[!UICONTROL Upload] un fichier](#upload-a-file)
* [[!UICONTROL Update a file]](#update-a-file)
* [[!UICONTROL Delete a file]](#delete-a-file)
* [[!UICONTROL Get a file]](#get-a-file)

#### [!UICONTROL Upload a file]

Ce module d’action charge un fichier.

Vous spécifiez le fichier. Vous pouvez également indiquer un nouveau nom pour le fichier.

Le module renvoie l’ID du fichier et tous les champs associés, ainsi que les valeurs et les champs personnalisés auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Box] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Si ce module échoue, tenez compte des points suivants :
>
>* Il est possible que la taille du fichier dépasse la taille maximale autorisée pour votre plan [!DNL Box] ou que vous ayez utilisé la totalité des quotas de stockage de votre compte [!DNL Box]. Pour obtenir plus d’espace de stockage, supprimez les fichiers existants de [!DNL Box] ou mettez à niveau votre compte [!DNL Box].
>* [!DNL Box] ne charge pas plusieurs fichiers portant le même nom dans un même dossier. Si le dossier de destination contient un fichier portant le même nom que le fichier chargé, l’exécution du scénario s’arrête avec une erreur. Pour éviter cela, renommez le fichier. Si vous souhaitez mettre à jour le fichier, utilisez le module **[!UICONTROL Update a file]** .

#### [!UICONTROL Update a file]

Ce module d’action met à jour un fichier.

Vous spécifiez l’identifiant du fichier.

Le module renvoie l’ID du fichier et tous les champs associés, ainsi que les valeurs et les champs personnalisés auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Box] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Saisissez ou mappez l’identifiant unique du fichier que le module doit mettre à jour.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a file]

Ce module d’action supprime un fichier.

Vous spécifiez l’identifiant du fichier.

Le module renvoie l’ID du fichier et tous les champs associés, ainsi que les valeurs et les champs personnalisés auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Box] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Saisissez ou mappez l’identifiant unique du fichier que le module doit mettre à jour.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a file]

Ce module d’action télécharge un fichier.

Vous spécifiez l’identifiant du fichier.

Le module renvoie l’ID du fichier et tous les champs associés, ainsi que les valeurs et les champs personnalisés auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

>[!NOTE]
>
>Ce module est utile pour fournir des fichiers aux modules suivants.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Box] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Saisissez ou mappez l’identifiant unique du fichier que le module doit mettre à jour.</td> 
  </tr> 
 </tbody> 
</table>

<!--
<h2>Possible problems</h2>

<p style="color: #ff1493;">This is drafted out because we don't have a download module for Box yet</p>


<h3>Watch files trigger module doesn't download a file contained in the folder.</h3>

<p>There are several situations when downloading a file fails:</p>



  <li>The current file lock setting does not allow the file to be downloaded or the downloading of the file is disabled. In this case, the file is ignored.</li>



  <li>When the scenario started, the file was being uploaded to the server and was not ready to be downloaded. The scenario run gets stopped and Workfront Fusion tries downloading the file again during the next execution of the scenario.</li>
  
-->
