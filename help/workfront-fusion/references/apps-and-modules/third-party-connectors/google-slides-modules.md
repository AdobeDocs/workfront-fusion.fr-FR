---
title: Modules Google Slides
description: Les modules Google Slides Adobe Workfront Fusion vous permettent de créer, de mettre à jour, de répertorier ou de supprimer des présentations et de charger des images vers des présentations dans votre compte Google Slides.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 6f5f97b9-b06a-4336-b349-ee9e2606d4bf
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2031'
ht-degree: 54%

---

# Modules [!DNL Google Slides]

Les modules Adobe Workfront Fusion [!DNL Google Slides] vous permettent de créer, mettre à jour, répertorier et/ou supprimer des présentations et de charger des images dans des présentations de votre compte [!DNL Google Slides].

Pour utiliser [!DNL Google Slides] avec Workfront Fusion, il est nécessaire d’avoir un compte [!DNL Google]. Si vous n’avez pas encore de compte [!DNL Google],vous pouvez en créer un sur la page d’aide des comptes [!DNL Google].

Vous devez également avoir [!DNL Google Slides] dans votre [!DNL Google Drive].

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

Pour utiliser les modules [!DNL Google Slides], vous devez disposer d’un compte [!DNL Google].

## Informations sur l’API des diapositives Google

Le connecteur Google Slides utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td> https://slides.googleapis.com/v1</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Version de l’API</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.5.9</td> 
  </tr>
 </tbody> 
 </table>

## Modules [!DNL Google Slides] et leurs champs

Lorsque vous configurez les modules [!DNL Google Slides], Workfront Fusion affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Google Slides] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Présentation](#presentation)
* [Autre](#other)

### Présentation

* [[!UICONTROL Ajouter/supprimer une diapositive]](#adddelete-a-slide)
* [[!UICONTROL Créer une présentation à partir d’un modèle]](#create-a-presentation-from-a-template)
* [[!UICONTROL Obtenir une page/miniature]](#get-a-pagethumbnail)
* [[!UICONTROL Obtenir une présentation]](#get-a-presentation)
* [[!UICONTROL Répertorier les présentations]](#list-presentations)
* [[!UICONTROL Actualiser un graphique]](#refresh-a-chart)
* [[!UICONTROL Charger une image vers une présentation]](#upload-an-image-to-a-presentation)
* [[!UICONTROL Surveiller les présentations]](#watch-presentations)

#### [!UICONTROL Ajouter/supprimer une diapositive]

Ce module d&#39;action crée une diapositive ou supprime une diapositive existante dans la présentation spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Slides] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the method]</td> 
   <td> <p>Indiquez si vous souhaitez ajouter une nouvelle diapositive ou supprimer une diapositive.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Enter a Slide ID]</td> 
   <td> <p>Si vous supprimez une diapositive, indiquez si vous souhaitez saisir manuellement l’ID de la diapositive ou sélectionner la diapositive dans une liste.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Presentation ID]</td> 
   <td> <p>Sélectionnez la présentation ou mappez l'identifiant de présentation de la présentation pour laquelle vous souhaitez ajouter ou supprimer une diapositive.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Slide Object ID]</td> 
   <td> <p>Si vous supprimez une diapositive et choisissez de la saisir manuellement, saisissez ou mappez l’ID de la diapositive. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Predefined layout type]</td> 
   <td> <p> Sélectionnez la mise en page de diapositive prédéfinie que vous souhaitez que votre diapositive ajoutée utilise. Spécifiez les valeurs de tous les champs supplémentaires (tels que [!UICONTROL Title]).</p> 
    <ul> 
     <li>[!UICONTROL Blank layout, with no placeholders]</li> 
     <li>[!UICONTROL Layout with a caption at the bottom]</li> 
     <li>[!UICONTROL Layout with a title and subtitle]</li> 
     <li>[!UICONTROL Layout with a title and body]</li> 
     <li>[!UICONTROL Layout with a title and two columns]</li> 
     <li>[!UICONTROL Layout with only a title]</li> 
     <li>[!UICONTROL Layout with a section title]</li> 
     <li>[!UICONTROL Layout with a title and subtitle on one side and description on the other]</li> 
     <li>[!UICONTROL Layout with one title and one body, arranged in a single column]</li> 
     <li>[!UICONTROL Layout with a main point]</li> 
     <li>[!DNL Layout with a big number heading]</li> 
    </ul> <p>Ce champ est disponible si vous avez choisi d’ajouter une diapositive.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Content]</td> 
   <td> <p>Saisissez ou mappez le contenu texte de la diapositive. Les champs sont disponibles en fonction du modèle que vous avez sélectionné.</p> <p>Ce champ est disponible si vous avez choisi d’ajouter une diapositive.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Créer une présentation à partir d’un modèle]

Ce module d&#39;action crée une présentation en copiant une présentation et en remplaçant toutes les balises telles que `{{Name}}`, `{{Email}}` avec les données fournies.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Slides] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title] </td> 
   <td> <p>Saisissez un nom pour la nouvelle présentation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy a Presentation]</td> 
   <td> <p> Sélectionnez l’option si vous copiez une présentation existante :</p> 
    <ul> 
     <li>[!UICONTROL By Mapping]</li> 
     <li>[!UICONTROL By Dropdown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy of Existing Presentation ID]</td> 
   <td> <p> Saisissez le chemin d’accès ou l’ID de présentation d’une présentation existante que vous souhaitez copier. Ce champ s’affiche si vous créez la présentation [!UICONTROL By Mapping].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Sélectionnez le [!DNL Google Drive] où se trouvent les présentations que vous souhaitez répertorier :</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Shared Drive]</li> 
    </ul> <p>Ce champ s’affiche si vous créez la présentation [!UICONTROL By Dropdown].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p> Sélectionnez la présentation ou saisissez ou mappez l'identifiant de présentation de la présentation à utiliser comme modèle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Values] </td> 
   <td> <p>Ajoutez les valeurs :</p> 
    <ul> 
     <li><strong>[!UICONTROL Tag]</strong> : saisissez la balise à remplacer dans la présentation. Par exemple, <code>&#123;&#123;Name&#125;&#125;</code></li> 
     <li><strong>[!UICONTROL Replaced Value]</strong> : saisissez la valeur de remplacement de la balise existante. Par exemple, si une chaîne <code>&#123;&#123;Name&#125;&#125;</code> dans la présentation et que la valeur remplacée est Exemple, la <code>&#123;&#123;Name&#125;&#125;</code> est remplacée par <code>Sample</code>.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New Drive Location]</td> 
   <td> <p>Sélectionnez l'[!DNL Google Drive] où vous souhaitez stocker ou ajouter la nouvelle présentation :</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Shared Drive]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Emplacement du nouveau document]</p> </td> 
   <td> <p>Sélectionnez le dossier dans lequel vous souhaitez stocker ou ajouter la présentation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Shared] </td> 
   <td> <p>Sélectionnez cette option si vous souhaitez partager la présentation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sharing with Other's Email Address]</td> 
   <td> <p> Saisissez l'adresse e-mail avec laquelle vous souhaitez partager la présentation. Si vous activez l'option Partagé sans saisir d'e-mail dans ce champ, la présentation peut être partagée par n'importe qui.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obtenir une page/miniature]

Ce module d&#39;action obtient la dernière version de la page spécifiée ou de la miniature d&#39;une page de la présentation.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Slides] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Saisir une présentation et un ID de page]</td> 
   <td> <p> Choisissez de saisir manuellement un ID de présentation et de page ou sélectionnez-les dans une liste.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p> Sélectionnez l’ID de présentation que vous souhaitez récupérer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Page Object ID]</td> 
   <td> <p> Sélectionnez la diapositive pour laquelle vous souhaitez afficher les détails de l’objet de la page.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show Page Thumbnail]</td> 
   <td> <p> Cochez la case si vous souhaitez afficher les informations sur la miniature de la page.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obtenir une présentation]

Ce module d&#39;action obtient la dernière version d&#39;une présentation spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Slides] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Sélectionnez le [!DNL Google Drive] où se trouvent les présentations que vous souhaitez répertorier :</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Shared Drive]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p> Sélectionnez la présentation que vous souhaitez récupérer.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Répertorier les présentations]

Ce module récupère une liste de toutes les présentations à l&#39;emplacement donné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Slides] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive location]</td> 
   <td> <p>Sélectionnez le [!DNL Google Drive] où se trouvent les présentations que vous souhaitez répertorier :</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Shared Drive]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td> <p>Sélectionnez l’emplacement du dossier des présentations que vous souhaitez répertorier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal de présentations que le module doit renvoyer au cours d'un cycle d'exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Actualiser un graphique]

Ce module d&#39;action actualise les données du graphique stockées dans une présentation spécifiée par l&#39;ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Slides] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Saisir un ID de présentation]</td> 
   <td> <p> Choisissez de saisir manuellement un ID de présentation ou de le sélectionner dans une liste.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Si vous sélectionnez la présentation dans une liste, sélectionnez le [!DNL Google Drive] où se trouvent les présentations à répertorier :</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Shared Drive]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p>Sélectionnez la présentation ou saisissez ou mappez l'identifiant de présentation de la présentation qui comprend le graphique à actualiser.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Chart Object ID]</td> 
   <td> <p> Si vous saisissez des données manuellement, saisissez ou mappez l'identifiant du graphique à actualiser.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Charger une image vers une présentation]

télécharge une image avec les données fournies.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Slides] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Presentation]</td> 
   <td> <p>Choisissez le mode de sélection de la présentation sur laquelle vous chargez une image.</p> 
    <ul> 
     <li>[!UICONTROL By Mapping]</li> 
     <li>[!DNL By Dropdown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Si vous choisissez dans une liste déroulante, sélectionnez l'[!DNL Google Drive] où se trouve la présentation à laquelle vous souhaitez ajouter une image :</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Shared Drive]</li> 
    </ul>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p> Sélectionnez l’ID de présentation de la présentation sur laquelle vous chargez une image.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sélectionner la méthode]</td> 
   <td> <p> Sélectionnez le mode de remplacement de l’image.</p>
   <ul>
   <li><p><b>Charger une image en remplaçant la balise de texte</b></p><p>Dans le champ Valeurs , pour chaque image à charger, cliquez sur <b>Ajouter un élément</b> et saisissez la balise de l’image et l’URL de la nouvelle image.</p></li>
   <li><p><b>Charger une image en remplaçant l’image</b></p><p>Dans le champ Valeurs , pour chaque image à charger, cliquez sur <b>Ajouter un élément</b> et saisissez l’ID d’objet de l’image, la méthode de remplacement et l’URL de la nouvelle image.</p></li>
   </ul>
  <p>Note : les images doivent avoir une taille inférieure à 50 Mo, ne peuvent pas dépasser 25 mégapixels et doivent être au format PNG, JPEG ou GIF.</p>   </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Surveiller les présentations]

Ce module de déclenchement démarre un scénario lorsqu&#39;une nouvelle présentation est créée ou mise à jour.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Slides] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch] </td> 
   <td> <p>Sélectionnez l’option pour surveiller les présentations :</p> 
    <ul> 
     <li> <p>[!UICONTROL Created Date]</p> </li> 
     <li> <p>[!UICONTROL Modified Date]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal de présentations que Workfront Fusion doit renvoyer au cours d’un cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Autre

* [[!UICONTROL Insérer des liens dans une présentation]](#insert-links-in-a-presentation)
* [[!UICONTROL Effectuer un appel API]](#make-an-api-call)

#### [!UICONTROL Insérer des liens dans une présentation]

Ce module rend tous les liens d’une présentation cliquables ou insère un lien dans tous les textes d’entrée correspondants.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Slides] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a Presentation]</td> 
   <td> <p>Choisissez le mode de sélection de la présentation sur laquelle vous chargez une image.</p> 
    <ul> 
     <li>[!UICONTROL By Mapping]</li> 
     <li>[!UICONTROL By Dropdown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Sélectionnez le [!DNL Google Drive] où se trouvent les présentations que vous souhaitez répertorier :</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Shared Drive]</li> 
    </ul> <p>Ce champ s’affiche si vous créez la présentation [!UICONTROL By Dropdown].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p>Sélectionnez l’emplacement du dossier des présentations que vous souhaitez répertorier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select]</td> 
   <td> <p>Indiquez si vous souhaitez que tous les liens d’une présentation soient cliquables ou si vous souhaitez insérer un lien dans tous les textes de saisie correspondants.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text Inputs]</td> 
   <td>Si vous insérez un lien, pour chaque élément de texte auquel vous souhaitez ajouter un lien, cliquez sur <b>Ajouter un élément</b> et saisissez le texte et son lien associé. Chaque fois que l'élément apparaît dans la présentation, il est automatiquement lié au site spécifié.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Effectuer un appel API]

Exécute un appel API autorisé arbitraire.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Slides] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Saisissez un chemin relatif à <code>https://developers.google.com/slides/</code>. Par exemple, présentation.</p> <p>Pour obtenir la liste des points d’entrée disponibles, reportez-vous à la section Documentation de l’API <a href="https://developers.google.com/slides/reference/rest">[!DNL Google Slides]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Saisissez les en-têtes de requête de votre choix. Vous n’avez pas besoin d’ajouter des en-têtes d’autorisation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Saisissez la chaîne de requête.</p> </td> 
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

>[!BEGINSHADEBOX]

**Exemple :** un appel API vous permet d’obtenir les détails de présentation de l’ID de présentation que vous avez saisi. Vous pouvez trouver l’ID de la présentation dans l’URL lorsque vous ouvrez la présentation dans [!DNL Google Slides].

![Exemple d’appel API](/help/workfront-fusion/references/apps-and-modules/assets/api-call-350x13.png)

L’appel API suivant renvoie les détails de la présentation :

![Détails de la présentation](/help/workfront-fusion/references/apps-and-modules/assets/presentation-details.png)

Les correspondances de la recherche se trouvent dans la sortie du module sous [!UICONTROL Lot] > [!UICONTROL Corps] > [!UICONTROL presentationId].

Dans notre exemple, les détails de présentation demandés ont été renvoyés :

![Détails de la présentation](/help/workfront-fusion/references/apps-and-modules/assets/presentation-details-2.png)

>[!ENDSHADEBOX]
