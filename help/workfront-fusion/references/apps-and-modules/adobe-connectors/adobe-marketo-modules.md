---
title: Modules Marketo
description: Dans un scénario  [!DNL Adobe Workfront Fusion] , vous pouvez automatiser les workflows qui utilisent  [!DNL Marketo]et le connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: da417ac7-e532-45f7-86d9-3643b5f9f203
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '2165'
ht-degree: 76%

---

# Modules [!DNL Marketo]

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!DNL Marketo] et le connecter à plusieurs applications et services tiers.

Pour une vidéo d’introduction au connecteur Marketo, voir :

* [Marketo](https://video.tv.adobe.com/v/3427026/){target=_blank}

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

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

Pour utiliser les modules [!DNL Marketo], vous devez disposer d’un compte [!DNL Marketo].

## Informations sur l’API Marketo

Le connecteur Marketo utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Version de l’API</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.14.19</td> 
  </tr>
 </tbody> 
 </table>

## Connecter [!DNL Marketo] à Workfront Fusion {#connect-marketo-to-workfront-fusion}

Vous pouvez créer une connexion à votre compte [!DNL Marketo] directement depuis n’importe quel module de [!DNL Marketo].

1. Dans un module Marketo, cliquez sur **Ajouter** en regard du champ Connexion .
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
          <p>Saisissez un nom pour la nouvelle connexion.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>
          <p>Indiquez si vous vous connectez à un environnement de production ou hors production.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>
          <p>Indiquez si vous vous connectez à un compte de service ou à un compte personnel.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Account / Munchkin ID]</td>
        <td>
          <p>Saisissez votre compte [!DNL Marketo] ou [!DNL Marketo] identifiant [!UICONTROL Munchkin]. Il s’agit de la partie unique de l’URL de base ou du point d’entrée attribué à votre compte que vous utilisez pour accéder à [!DNL Marketo] via son API [!UICONTROL REST]. Pour obtenir des instructions sur la localisation de ce paramètre, consultez [URL de base](https://developers.marketo.com/rest-api/base-url/) dans la documentation [!DNL Marketo].</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Saisissez votre identifiant client Marketo. Pour obtenir des instructions sur la localisation de ce paramètre, voir [Authentification](https://developers.marketo.com/rest-api/authentication/) dans la documentation [!DNL Marketo].</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Saisissez votre secret client Marketo. Pour plus d’informations sur leur localisation, voir [Authentification](https://developers.marketo.com/rest-api/authentication/) dans la documentation [!DNL Marketo].</td>
      </tr>
     </tbody>
    </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour créer la connexion et revenez au module.

## Modules [!DNL Marketo] et leurs champs

Lorsque vous configurez les modules [!DNL Marketo], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Marketo] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Déclencheurs](#triggers)
* [Actions](#actions)
* [Recherches](#searches)

### Déclencheurs

* [[!UICONTROL Regarder des événements (instantané)]](#watch-events-instant)
* [[!UICONTROL Surveiller les enregistrements]](#watch-records)

#### [!UICONTROL Regarder des événements (instantané)]

Ce module de déclenchement lance un scénario lorsqu’un enregistrement est créé ou mis à jour.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Webhook]</p> </td> 
   <td> <p>Saisissez le webhook que le module doit utiliser.</p> <p>Pour plus d’informations sur les Webhooks, voir <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md" class="MCXref xref">Webhooks</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Regarder des enregistrements]

Ce module de déclenchement lance un scénario lorsqu’un enregistrement est créé ou mis à jour.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Marketo] à [!DNL Workfront Fusion], voir <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Marketo] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement que vous souhaitez créer.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Activity]</strong> </p> <p>Sélectionnez le type d’activité que vous souhaitez regarder. </p> <p>Le module ne recherche que les nouvelles activités.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Lead]</strong> </p> <p>Dans le champ <b>Type d’événement</b>, indiquez si vous souhaitez rechercher de nouveaux enregistrements, des enregistrements mis à jour, des enregistrements nouveaux et mis à jour ou des mises à jour de champs spécifiques. Si vous choisissez de regarder les mises à jour de champs spécifiques, sélectionnez le champ que le module doit rechercher.</p> </li> 
     <li> <p><strong>[!UICONTROL Program]</strong> </p> <p>Dans le champ <b>Type d’événement</b>, indiquez si vous souhaitez rechercher de nouveaux enregistrements, des enregistrements mis à jour ou les deux.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Sélectionnez les champs à inclure dans le lot de sortie pour ce module.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [[!UICONTROL Ajouter des leads à une liste]](#add-leads-to-a-list)
* [[!UICONTROL Cloner un programme]](#clone-a-program)
* [[!UICONTROL Créer un enregistrement]](#create-a-record)
* [[!UICONTROL Appel API personnalisé]](#custom-api-call)
* [[!UICONTROL Télécharger un fichier]](#download-a-file)
* [[!UICONTROL Lire un enregistrement]](#read-a-record)
* [[!UICONTROL Supprimer des leads d’une liste]](#remove-leads-from-a-list)
* [[!UICONTROL Planifier une campagne]](#schedule-a-campaign)
* [[!UICONTROL Mettre à jour un enregistrement]](#update-a-record)
* [[!UICONTROL Charger un fichier]](#upload-a-file)

#### [!UICONTROL Ajouter des leads à une liste]

Ce module d’action ajoute un ou plusieurs prospects à une liste à l’aide de l’identifiant de prospect. Vous pouvez ajouter jusqu’à 300 prospects à la fois.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Marketo] à [!DNL Workfront Fusion], voir <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Marketo] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td>Saisissez ou mappez l’identifiant de la liste dans laquelle vous souhaitez ajouter des leads.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Lead IDs]</td> 
   <td> <p>Pour chaque lead à ajouter à la liste, cliquez sur <b>[!UICONTROL Add]</b>, puis saisissez ou mappez l’ID du lead à ajouter. Vous pouvez ajouter jusqu’à 300 leads pour que le module les ajoute à la liste.</p> <p>Cliquez sur le bouton Mapper pour mapper une collection existante de leads que vous souhaitez ajouter à la liste.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Cloner un programme]

Ce module d’action effectue une copie d’un programme à l’aide de l’ID du programme existant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Marketo] à [!DNL Workfront Fusion], voir <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Marketo] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Existing Program ID]</td> 
   <td>Saisissez ou mappez l’ID du programme que vous souhaitez copier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL New Program Name]</p> </td> 
   <td> <p>Saisissez ou mappez un nom pour le nouveau programme.</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>Saisissez ou mappez l’ID du dossier dans lequel vous souhaitez que le nouveau programme soit situé.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Créer un enregistrement]

Ce module d’action crée un nouvel enregistrement dans [!DNL Marketo].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Marketo] à [!DNL Workfront Fusion], voir <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Marketo] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement que vous souhaitez créer.</p> 
    <ul> 
     <li> <p>[!UICONTROL Company]</p> </li> 
     <li> <p>[!UICONTROL Folder]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL Program]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select fields to map]</td> 
   <td>Si vous créez une entreprise ou un lead, sélectionnez les champs pour lesquels vous souhaitez définir des valeurs lors de la création du nouvel enregistrement, puis saisissez des valeurs pour ces champs.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Program Type]</td> 
   <td>Si vous créez un programme, sélectionnez le type de programme que vous souhaitez créer.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Program Channel] </td> 
   <td>Si vous créez un programme, sélectionnez le canal du programme dans lequel vous souhaitez créer le programme.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] / [!UICONTROL Program Name]</td> 
   <td>Si vous créez un dossier ou un programme, saisissez ou mappez un nom pour le nouvel enregistrement.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td> <p>Si vous créez un dossier ou un programme, saisissez ou mappez une description pour le nouvel enregistrement.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent Folder ID]</td> 
   <td>Si vous créez un dossier ou un programme, saisissez ou mappez l’identifiant du dossier parent dans lequel vous souhaitez créer le nouvel enregistrement.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Costs]</td> 
   <td>Si vous créez un programme, ajoutez des coûts.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td>Si vous créez un programme, ajoutez des balises.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Appel API personnalisé]

Ce module d’action vous permet d’effectuer un appel personnalisé et authentifié vers l’API [!DNL Marketo]. Ainsi, vous pouvez créer une automatisation du flux de données qui ne peut pas être réalisée par les autres modules [!DNL Marketo].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Marketo] à [!DNL Workfront Fusion], consultez la section <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Marketo] à [!DNL Workfront Fusion]</a> de cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Saisissez un chemin d’accès relatif à <code>https://{your-base-url}.mktorest.com/</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion] ajoute les en-têtes d’autorisation pour vous.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Ajoutez la requête pour l’appel API sous la forme d’un objet JSON standard.</p> <p>Par exemple : <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>Pour chaque champ que vous souhaitez ajouter à votre appel API, cliquez sur <b>Ajouter un élément</b> et saisissez la clé et la valeur du champ.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Télécharger un fichier]

Ce module d’action télécharge un fichier à l’aide de l’identifiant de fichier.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Marketo] à [!DNL Workfront Fusion], voir la section <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Marketo] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Saisissez ou mappez l’identifiant du fichier que vous souhaitez télécharger.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Lire un enregistrement]

Ce module d’action lit des informations concernant un enregistrement à l’aide de son identifiant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Marketo] à [!DNL Workfront Fusion], voir <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Marketo] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement que vous souhaitez créer.</p> 
    <ul> 
     <li> <p>[!UICONTROL Campaign]</p> </li> 
     <li> <p>[!UICONTROL Company]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL List]</p> </li> 
     <li> <p>[!UICONTROL Program]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Sélectionnez les informations que vous souhaitez inclure dans le bundle de sortie pour ce module.
Les champs sont disponibles en fonction du [!UICONTROL Record Type] que vous avez sélectionné.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL &lt;Object&gt; ID]</td> 
   <td>Saisissez ou mappez l’identifiant de l’objet dont vous souhaitez récupérer les informations.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Supprimer des leads d’une liste]

Ce module d’action supprime un ou plusieurs prospects d’une liste à l’aide de l’identifiant de prospect. Vous pouvez supprimer jusqu’à 300 prospects à la fois.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Marketo] à [!DNL Workfront Fusion], voir <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Marketo] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td>Saisissez ou mappez l’ID de la liste dans laquelle vous souhaitez supprimer des leads.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Lead IDs]</td> 
   <td> <p>Pour chaque lead à supprimer de la liste, cliquez sur <b>[!UICONTROL Add item]</b>, puis saisissez ou mappez l’identifiant du lead à supprimer. Vous pouvez ajouter jusqu’à 300 leads pour que le module les supprime de la liste. </p> <p>Cliquez sur le bouton Mapper pour mapper une collection de leads existante à supprimer de la liste.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Planifier une campagne]

Ce module d’action planifie une campagne existante pour une certaine date.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Marketo] à [!DNL Workfront Fusion], voir <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Marketo] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campaign ID]</td> 
   <td>Saisissez ou mappez l’ID de la campagne que vous souhaitez planifer.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Schedule for Date]</p> </td> 
   <td>Sélectionnez la date d’exécution de la campagne. Si ce champ n’est pas renseigné, la campagne s’exécute cinq minutes après le début du scénario.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mettre à jour un enregistrement]

Ce module d’action met à jour un enregistrement existant à l’aide de son identifiant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Marketo] à [!DNL Workfront Fusion], voir <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Marketo] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement que vous souhaitez créer.</p> 
    <ul> 
     <li> <p>[!UICONTROL Company]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL Program]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Company] / [!UICONTROL Lead] / [!UICONTROL Program ID]</td> 
   <td>Saisissez ou mappez l’identifiant de l’enregistrement que vous souhaitez mettre à jour.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select fields to map]</td> 
   <td>Si vous mettez à jour une société ou un prospect, sélectionnez les champs pour lesquels vous souhaitez mettre à jour les valeurs, puis saisissez les valeurs de ces champs.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Program Name]</td> 
   <td>Si vous mettez à jour un programme, saisissez ou mappez un nouveau nom pour le programme.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td> <p>Si vous mettez à jour un programme, saisissez ou mappez une nouvelle description du programme.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Date]</td> 
   <td>Si vous mettez à jour un programme, saisissez ou mappez une nouvelle date de début pour le programme.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End Date]</td> 
   <td>Si vous mettez à jour un programme, saisissez ou mappez une nouvelle date de fin pour le programme.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Costs]</td> 
   <td>Si vous mettez à jour un programme, ajoutez des frais.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td>Si vous mettez à jour un programme, ajoutez des balises.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Charger un fichier]

Ce module d’action charge un nouveau fichier vers [!UICONTROL Marketo].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Marketo] à [!DNL Workfront Fusion], voir la section <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Marketo] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>Saisissez ou mappez l’identifiant du dossier dans lequel vous souhaitez que le nouveau fichier se trouve.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Saisissez une description pour le fichier chargé.</td> 
  </tr> 
 </tbody> 
</table>

### Recherches

* [[!UICONTROL Répertorier des enregistrements]](#list-records)
* [[!UICONTROL Rechercher des enregistrements]](#update-a-record)

#### [!UICONTROL Répertorier des enregistrements]

Ce module d’action récupère tous les enregistrements d’un type spécifique.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Marketo] à [!DNL Workfront Fusion], voir <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Marketo] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement que vous souhaitez répertorier.</p> 
    <ul> 
     <li> <p>[!UICONTROL Read all campaigns]</p> </li> 
     <li> <p>[!UICONTROL Read all programs]</p> </li> 
     <li> <p>[!UICONTROL Read all leads] </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field]</td> 
   <td>Si vous avez choisi de récupérer des leads, choisissez si vous souhaitez récupérer des leads à partir d’une liste ou d’un programme.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Sélectionnez les informations que vous souhaitez inclure dans le bundle de sortie pour ce module.
Les champs sont disponibles en fonction du [!UICONTROL Record Type] que vous avez sélectionné.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Rechercher des enregistrements]

Ce module de recherche récupère une liste d’enregistrements correspondant à des critères de recherche spécifiques.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Marketo] à [!DNL Workfront Fusion], voir <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Marketo] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement à rechercher.</p> 
    <ul> 
     <li> <p>[!UICONTROL Campaigns]</p> </li> 
     <li> <p>[!UICONTROL Leads]</p> </li> 
     <li> <p>[!UICONTROL Programs]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Field]</p> </td> 
   <td> <p>Sélectionnez le champ en fonction duquel effectuer la recherche.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Value / values]</td> 
   <td>Saisissez la valeur du champ que vous souhaitez rechercher. Si le champ vous permet de rechercher plusieurs valeurs, pour chaque valeur que vous souhaitez rechercher, cliquez sur <b>[!UICONTROL Add item]</b> et saisissez la valeur.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td> <p>Sélectionnez les informations que vous souhaitez inclure dans le bundle de sortie pour ce module.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>
