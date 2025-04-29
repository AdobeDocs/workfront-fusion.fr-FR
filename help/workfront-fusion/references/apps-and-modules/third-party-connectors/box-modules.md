---
title: Modules Box
description: Dans un scénario  [!DNL Adobe Workfront Fusion] , vous pouvez automatiser les workflows qui utilisent Box et le connecter à plusieurs applications et services tiers. Il surveille un dossier spécifié pour vérifier les modifications de fichier, modifier et supprimer des fichiers existants ou charger de nouveaux fichiers dans un dossier.
author: Becky
feature: Workfront Fusion
exl-id: 9e741dce-05a6-4e13-8d58-fbe3b4900d7e
source-git-commit: f02c4df01c7fad6bb9cdf4911512eef97e71c82b
workflow-type: tm+mt
source-wordcount: '918'
ht-degree: 70%

---

# Modules Box

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!DNL Box] et le connecter à plusieurs applications et services tiers. Il surveille un dossier spécifié pour vérifier les modifications de fichier, modifier et supprimer des fichiers existants ou charger de nouveaux fichiers dans un dossier.

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

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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

Lorsque vous configurez les modules [!DNL Box], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Box] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Déclencheurs](#triggers)
* [Actions](#actions)

### Déclencheurs

* [[!UICONTROL Nouvel événement]](#new-event)
* [[!UICONTROL Surveiller des fichiers]](#watch-files)

#### [!UICONTROL Nouvel événement]

Ce module de déclenchement instantané lance un scénario lorsqu’un fichier est ajouté, déplacé, copié, supprimé, verrouillé ou déverrouillé.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Sélectionnez le webhook que vous souhaitez utiliser pour surveiller les messages sortants. Pour ajouter un webhook, cliquez sur <strong>[!UICONTROL Add]</strong> et saisissez le nom et la connexion du webhook.</p> <p> Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Box] à [!UICONTROL Workfront Fusion], consultez <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Connexion à un service - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Maximum number of returned events]</p> </td> 
   <td> <p>Saisissez le nombre maximal d’événements que le module doit renvoyer à chaque cycle d’exécution de scénario.</p> </td> 
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
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Box] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  <tr> 
   <td role="rowheader">Dossier</td> 
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

* [[!UICONTROL Supprimer un fichier]](#delete-a-file)
* [[!UICONTROL Obtenir un fichier]](#get-a-file)
* [[!UICONTROL Mettre à jour un fichier]](#update-a-file)
* [[!UICONTROL Charger] un fichier](#upload-a-file)

#### [!UICONTROL Supprimer un fichier]

Ce module d’action supprime un fichier.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Box] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Saisissez ou mappez l’ID unique du fichier que le module doit supprimer.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obtenir un fichier]

Ce module d’action télécharge un fichier.

Vous spécifiez l’identifiant du fichier.

>[!NOTE]
>
>Ce module est utile pour fournir des fichiers aux modules suivants.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Box] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Saisissez ou mappez l’ID unique du fichier que le module doit récupérer.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mettre à jour un fichier]

Ce module d’action met à jour un fichier.

Vous spécifiez l’identifiant du fichier.

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

#### [!UICONTROL Charger un fichier]

Ce module d’action charge un fichier.

Vous spécifiez le fichier. Vous pouvez également indiquer un nouveau nom pour le fichier.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Box] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Sélectionnez le dossier dans lequel vous souhaitez charger le fichier.</p> </td> 
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
>* [!DNL Box] ne charge pas plusieurs fichiers portant le même nom dans un même dossier. Si le dossier de destination contient un fichier portant le même nom que le fichier chargé, l’exécution du scénario s’arrête avec une erreur. Pour éviter cela, renommez le fichier. Si vous souhaitez mettre à jour le fichier, utilisez le module **[!UICONTROL Mettre à jour un fichier]**.
