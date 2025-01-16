---
title: Modules Google Slides
description: Les modules Google Slides Adobe Workfront Fusion vous permettent de créer, de mettre à jour, de répertorier ou de supprimer des présentations et de charger des images vers des présentations dans votre compte Google Slides.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 6f5f97b9-b06a-4336-b349-ee9e2606d4bf
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1237'
ht-degree: 73%

---

# Modules [!DNL Google Slides]

Les modules [!DNL Adobe Workfront Fusion] [!DNL Google Slides] vous permettent de créer, de mettre à jour, de répertorier ou supprimer des présentations et de charger des images dans des présentations dans votre compte [!DNL Google Slides].

Pour utiliser [!DNL Google Slides] avec [!DNL Workfront Fusion], vous devez avoir un compte [!DNL Google]. Si vous n’avez pas encore de compte [!DNL Google],vous pouvez en créer un sur la page d’aide des comptes [!DNL Google].

Vous devez également avoir [!DNL Google Slides] dans votre [!DNL Google Drive].

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

* [[!UICONTROL Watch Presentations]](#watch-presentations)
* [[!UICONTROL List Presentations]](#list-presentations)
* [[!UICONTROL Get a Presentation]](#get-a-presentation)
* [[!UICONTROL Get a Page/Thumbnail]](#get-a-pagethumbnail)
* [[!UICONTROL Create a Presentation From a Template]](#create-a-presentation-from-a-template)
* [[!UICONTROL Upload an Image To a Presentation]](#upload-an-image-to-a-presentation)
* [[!UICONTROL Refresh a Chart]](#refresh-a-chart)
* [[!UICONTROL Add/Delete a Slide]](#adddelete-a-slide)

#### [!UICONTROL Watch Presentations]

Se déclenche lorsqu’une nouvelle présentation est créée ou mise à jour.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Slides] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
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
   <td> <p>Le nombre maximal de présentations que Workfront Fusion doit renvoyer lors d’un cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Presentations]

Récupère une liste de toutes les présentations.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Slides] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive location]</td> 
   <td> <p>Sélectionnez le [!DNL Google Drive] où se trouvent les présentations que vous souhaitez répertorier :</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Lecteur partagé]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td> <p>Sélectionnez l’emplacement du dossier des présentations que vous souhaitez répertorier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Nombre maximal de présentations que [!DNL Workfront Fusion] doit renvoyer pendant un cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Presentation]

Obtient la dernière version d’une présentation spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Slides] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Sélectionnez le [!DNL Google Drive] où se trouvent les présentations que vous souhaitez répertorier :</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Lecteur partagé]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p> Sélectionnez la présentation que vous souhaitez récupérer.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Page/Thumbnail]

Obtient la dernière version de la page spécifiée ou de la miniature d’une page dans la présentation.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Slides] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
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

#### [!UICONTROL Create a Presentation From a Template]

Crée une nouvelle présentation en remplaçant toutes les balises telles que `{{Name}}`, `{{Email}}` dans un modèle contenant des données fournies.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Slides] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
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
   <td> <p> Saisissez le chemin d’accès ou l’ID de présentation d’une présentation existante que vous souhaitez copier. Ce champ s'affiche si vous créez le [!UICONTROL By Mapping] de présentation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Sélectionnez le [!DNL Google Drive] où se trouvent les présentations que vous souhaitez répertorier :</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Lecteur partagé]</li> 
    </ul> <p>Ce champ s'affiche si vous créez le [!UICONTROL By Dropdown] de présentation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p> Sélectionnez l’ID de présentation de la présentation que vous souhaitez utiliser comme modèle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Values] </td> 
   <td> <p>Ajoutez les valeurs :</p> 
    <ul> 
     <li><strong>[!UICONTROL Tag]</strong>: saisissez la balise à remplacer dans la présentation. Par exemple, <code>&#123;&#123;Name&#125;&#125;</code></li> 
     <li><strong>[!UICONTROL Replaced Value]</strong>: saisissez la valeur avec laquelle la balise existante doit être remplacée. Par exemple, si une chaîne <tr><ul><tr><tr><tr><code>&#123;&#123;Name&#125;&#125;/code> in the presentation and the replaced value is Sample, then the <code>&#123;&#123;Name&#125;&#125;</code> will be replaced by <code>Sample</code>.</li> 
    </ul> </td> 
  </tr> 
   
   <td role="rowheader">[!UICONTROL New Drive Location]</td> 
   <td> <p>Select the [!DNL Google Drive] where you want to store or add the new presentation:</p> 
     
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Shared Drive]</li> 
    </ul> </td> 
  </tr> 
   
   <td role="rowheader"> <p>[!UICONTROL New Document's Location]</p> </td> 
   <td> <p>Select the folder where you want to store or add the presentation.</p> </td> 
  </tr> 
   
   <td role="rowheader">[!UICONTROL Shared] </td> 
   <td> <p>Select if you want to share the presentation.</p> </td> 
  </tr> 
   
   <td role="rowheader">[!UICONTROL Sharing with Other's Email Address]</td> 
   <td> <p> Enter the email address with whom you want to share the presentation. If you are not entering an email address and selecting only shared field, the presentation is shareable to anyone.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload an Image To a Presentation]

télécharge une image avec les données fournies.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Slides] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
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
   <td> <p>Sélectionnez le [!DNL Google Drive] où se trouvent les présentations que vous souhaitez répertorier :</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Lecteur partagé]</li> 
    </ul> <p>Ce champ s'affiche si vous créez le [!UICONTROL By Dropdown] de présentation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p> Sélectionnez l’ID de présentation de la présentation sur laquelle vous chargez une image.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Values]</td> 
   <td> <p>Valeurs Ajoutez les valeurs :</p> 
    <ul> 
     <li><strong>[!UICONTROL Tag]</strong>: saisissez la balise à laquelle vous souhaitez ajouter l’URL.</li> 
     <li><strong>[!UICONTROL Image URL]</strong>: saisissez le chemin d’accès ou l’URL de l’image à charger.</li> 
    </ul> <p>Note : les images doivent avoir une taille inférieure à 50 Mo, ne peuvent pas dépasser 25 mégapixels et doivent être au format PNG, JPEG ou GIF.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Refresh a Chart]

Actualise les données de graphique stockées dans une présentation spécifiée par ID.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Slides] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose a drive]</td> 
   <td> <p>Sélectionnez le [!DNL Google Drive] où se trouvent les présentations que vous souhaitez répertorier :</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared With Me]</li> 
     <li>[!UICONTROL [!DNL Google] Lecteur partagé]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Presentation ID]</td> 
   <td> <p>Sélectionnez l’ID de présentation de la présentation qui comprend le graphique à actualiser.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Chart Object ID]</td> 
   <td> <p> Sélectionnez le graphique que vous souhaitez actualiser.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add/Delete a Slide]

Crée une diapositive vide ou supprime une diapositive existante sur la présentation spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Slides] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the method]</td> 
   <td> <p>Indiquez si vous souhaitez ajouter une nouvelle diapositive ou supprimer une diapositive.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Presentation ID]</td> 
   <td> <p>Sélectionnez l’ID de présentation de la présentation pour laquelle vous souhaitez ajouter ou supprimer une diapositive.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Predefined layout type]</td> 
   <td> <p> Sélectionnez la mise en page de diapositive prédéfinie que vous souhaitez que votre diapositive ajoutée utilise. Spécifiez des valeurs pour tout champ supplémentaire (tel que [!UICONTROL Title]).</p> 
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
 </tbody> 
</table>

### Autre

* [[!UICONTROL Make an API Call]](#make-an-api-call)
* [[!UICONTROL Insert Links in a Presentation]](#insert-links-in-a-presentation)

#### [!UICONTROL Make an API Call]

Exécute un appel API autorisé arbitraire.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Slides] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Saisissez un chemin relatif à https://developers.google.com/slides/. Par exemple, présentation.</p> <p>Pour obtenir la liste des points d’entrée disponibles, reportez-vous à la section Documentation de l’API <a href="https://developers.google.com/slides/reference/rest">[!DNL Google Slides]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Méthodes de requête HTTP dans [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
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

>[!INFO]
>
>**Exemple :** un appel API vous permet d’obtenir les détails de présentation de l’ID de présentation que vous avez saisi. Vous pouvez trouver l’ID de la présentation dans l’URL lorsque vous ouvrez la présentation dans [!DNL Google Slides].
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/api-call-350x13.png)
>
>L’appel API suivant renvoie les détails de la présentation :
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/presentation-details.png)
>
>Les correspondances de la recherche se trouvent dans la sortie du module sous [!UICONTROL Bundle] > [!UICONTROL Body] > [!UICONTROL presentationId].
>
>Dans notre exemple, les détails de présentation demandés ont été renvoyés :
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/presentation-details-2.png)

#### [!UICONTROL Insert Links in a Presentation]

Ce module rend tous les liens d’une présentation cliquables ou insère un lien dans tous les textes d’entrée correspondants.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Slides] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
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
     <li>[!UICONTROL [!DNL Google] Lecteur partagé]</li> 
    </ul> <p>Ce champ s'affiche si vous créez le [!UICONTROL By Dropdown] de présentation.</p> </td> 
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
   <td>Pour chaque élément de texte pour lequel vous souhaitez ajouter un lien, ajoutez l’élément ainsi que le lien associé à la liste. Chaque fois que l’élément apparaît dans la présentation, il est automatiquement lié au site spécifié.</td> 
  </tr> 
 </tbody> 
</table>
