---
title: Modules Google Forms
description: Les modules  [!DNL Adobe Workfront Fusion Google Forms]  vous permettent de surveiller, sélectionner, ajouter, mettre à jour ou supprimer des réponses sur Google Forms.
author: Becky
feature: Workfront Fusion
exl-id: dc017957-c0f8-4206-916f-21ccda346fb9
source-git-commit: ca8cee58b6586dbcd1a7ff7bffb0131b59dbb897
workflow-type: tm+mt
source-wordcount: '1199'
ht-degree: 77%

---

# Modules [!DNL Google Forms]

Les modules [!DNL Adobe Workfront Fusion] [!DNL Google Forms] vous permettent de surveiller, sélectionner, ajouter, mettre à jour ou supprimer des réponses sur [!DNL Google Forms].

Pour utiliser [!DNL Google Docs] avec [!DNL Adobe Workfront Fusion], vous devez posséder un compte [!DNL Google]. Si vous n’avez pas encore de compte [!DNL Google], vous pouvez en créer un sur la page d’aide des comptes [!DNL Google].

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
   <p>Actuel : aucune exigence de licence Workfront Fusion.</p>
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

Pour utiliser les modules [!DNL Google Forms], vous devez disposer d’un compte [!DNL Google].

## Informations sur l’API Google Forms

Le connecteur Google Forms utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>2.0.10</td> 
  </tr>
 </tbody> 
 </table>

## Créer une feuille de calcul à partir du formulaire

Pour utiliser vos réponses de formulaire, vous devez d’abord créer la feuille de calcul de réponse.

1. Ouvrez votre formulaire.
1. Accédez à l’onglet **[!UICONTROL Responses]** .
1. Cliquez sur l’icône **[!UICONTROL Create Spreadsheet]** ![icône de feuille de calcul](/help/workfront-fusion/references/apps-and-modules/assets/spreadsheet-icon.png).

1. Indiquez si vous souhaitez créer une feuille de calcul ou une feuille de calcul existante.
1. Cliquez sur **[!UICONTROL Create]**.

## Modules [!DNL Google Forms] et leurs champs

Lorsque vous configurez les modules [!DNL Google Forms], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Google Forms] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Déclencheurs](#triggers)
* [Actions](#actions)
* [Recherches](#searches)

### Déclencheurs

#### [!UICONTROL Watch Responses]

Contrôle le formulaire pour trouver de nouvelles réponses.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>Sélectionnez la feuille de calcul qui contient les réponses du formulaire dont vous voulez contrôler les nouvelles réponses.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> Sélectionnez la feuille contenant les réponses du formulaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Row with headers]</td> 
   <td>Spécifiez la ligne d’en-tête du tableau. La ligne par défaut est <code>A1:Z1</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Value Render Option]</td> 
   <td> <p>Indiquez le mode de rendu des valeurs dans la sortie.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Formatted value]</strong> </p> <p>Les valeurs sont calculées et mises en forme dans la réponse selon la mise en forme de la cellule. La mise en forme est basée sur les paramètres régionaux de la feuille de calcul et non sur ceux de l’utilisateur ou de l’utilisatrice qui s’en sert. Par exemple, si <code>A1</code> est <code>1. 23</code> et que <code>A2 </code> est <code>=A1</code> et mis en forme en tant que devise, alors <code>A2</code> renvoie <code>$1. 23</code>.</p> </li> 
     <li> <p><strong>[!UICONTROL Unformatted value]</strong> </p> <p>Les valeurs sont calculées mais ne sont pas mises en forme dans la réponse. Par exemple, si <code>A1</code> est <code>1. 23</code> et que <code>A2 </code> est <code>=A1</code> et mis en forme en tant que devise, alors <code>A2</code> renvoie le nombre <code>1. 23</code>.</p> </li> 
     <li> <p><strong>[!UICONTROL Formula]</strong> </p> <p>Les valeurs ne sont pas calculées. La réponse inclut les formules. Par exemple, si <code>A1</code> est <code>1. 23</code> et que <code>A2 </code> est <code>=A1</code> et mis en forme en tant que devise, alors <code>A2</code> renvoie <code>=A1</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Date and time render option]</td> 
   <td>Sélectionnez le format des dates, des heures et de la durée dans la sortie. Ce champ est ignoré si [!UICONTROL Value Render Option] est défini sur [!UICONTROL Formatted Value].</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p> Définissez le nombre maximal de réponses que [!DNL Workfront Fusion] traitera au cours d’un cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [[!UICONTROL Add a Response]](#add-a-response)
* [[!UICONTROL Delete a Response]](#delete-a-response)
* [[!UICONTROL Update a Response]](#update-a-response)

#### [!UICONTROL Add a Response]

Ce module ajoute une nouvelle réponse au bas de la feuille de calcul du formulaire.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>Sélectionnez la feuille de calcul qui contient la feuille à laquelle vous souhaitez ajouter une réponse.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> Sélectionnez la feuille contenant les réponses du formulaire.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Values]</p> </td> 
   <td> <p>Saisissez les valeurs souhaitées dans les colonnes de la feuille. Les colonnes sont disponibles en fonction de la feuille.</p> <p>Pour la colonne [!UICONTROL Timestamp], utilisez la valeur suivante :</p><pre>formatDate(now;DD/MM/YYYY HH:mm;UTC)</pre> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Value input option]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> Les valeurs saisies par l’utilisateur ou l’utilisatrice ne sont pas traitées et sont stockées en l’état. </p> </li> 
     <li> <p><strong>[!UICONTROL User entered]</strong></p> <p>Les valeurs sont traitées comme si l’utilisateur ou l’utilisatrice les avait saisies dans l’interface utilisateur. Les nombres restent des nombres, mais les chaînes peuvent être converties en nombres, en dates ou en autres formats en suivant les mêmes règles que celles qui s’appliquent lors d’une saisie de texte dans une cellule dans l’interface utilisateur de [!DNL Google Sheets].</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Insert data option]</td> 
   <td> <p>Indiquez le mode de modification des données existantes lors de la saisie de nouvelles données. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Overwrite]</strong> </p> <p>Les nouvelles données remplacent les données existantes dans les zones où elles sont écrites. L’ajout de données à la fin de la feuille insère de nouvelles lignes ou colonnes afin que les données puissent être écrites.</p> </li> 
     <li> <p><strong>[!UICONTROL Insert rows]</strong></p> <p>Des lignes sont insérées pour les nouvelles données.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Response]

Ce module supprime une réponse sélectionnée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>Sélectionnez la feuille de calcul qui contient la feuille dans laquelle vous souhaitez supprimer une réponse.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> Sélectionnez la feuille contenant les réponses du formulaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Row number]</p> </td> 
   <td> <p>Saisissez ou mettez en corresponsance le nombre de lignes à supprimer.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a Response]

Ce module met à jour la réponse sélectionnée.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>Sélectionnez la feuille de calcul qui contient la feuille dans laquelle vous souhaitez mettre à jour une réponse.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> Sélectionnez la feuille contenant les réponses du formulaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Row number]</p> </td> 
   <td> <p>Saisissez ou mettez en corresponsance le nombre de lignes à mettre à jour.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Values]</p> </td> 
   <td> <p>Saisissez les nouvelles valeurs des colonnes souhaitées. Les colonnes sont disponibles en fonction de la feuille.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Value input option]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> Les valeurs saisies par l’utilisateur ou l’utilisatrice ne sont pas traitées et sont stockées en l’état. </p> </li> 
     <li> <p><strong>[!UICONTROL User entered]</strong></p> <p>Les valeurs sont traitées comme si l’utilisateur ou l’utilisatrice les avait saisies dans l’interface utilisateur. Les nombres restent des nombres, mais les chaînes peuvent être converties en nombres, en dates ou en autres formats en suivant les mêmes règles que celles qui s’appliquent lors d’une saisie de texte dans une cellule dans l’interface utilisateur de [!DNL Google Sheets].</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Recherches

* [[!UICONTROL Search Responses]](#search-responses)
* [[!UICONTROL Search Responses (Advanced])](#search-responses-advanced)

#### [!UICONTROL Search Responses]

Ce module renvoie les réponses correspondant aux critères définis.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
    <td>Connexion</td>
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Spreadsheet]</td>
   <td> <p>Sélectionnez le formulaire dans lequel vous souhaitez effectuer une recherche.</p> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL Sheet] </td>
   <td> <p>Sélectionnez la feuille contenant les réponses du formulaire.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Column range]</td>
   <td> <p> Sélectionnez la plage de colonnes à rechercher.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Définissez le filtre de recherche des réponses.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Sort Order] </td>
   <td> <p>Choisissez si vous souhaitez trier les réponses renvoyées par ordre croissant ou décroissant.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Order By]</td>
   <td> <p> Sélectionnez la colonne par laquelle vous souhaitez trier les réponses renvoyées.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Value Render Option]</td> 
   <td> <p>Indiquez le mode de rendu des valeurs dans la sortie.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Formatted value]</strong></p> <p>Les valeurs sont calculées et mises en forme dans la réponse selon la mise en forme de la cellule. La mise en forme est basée sur les paramètres régionaux de la feuille de calcul et non sur ceux de l’utilisateur ou de l’utilisatrice qui s’en sert. Par exemple, si <code>A1</code> est <code>1. 23</code> et que <code>A2 </code> est <code>=A1</code> et mis en forme en tant que devise, alors <code>A2</code> renvoie <code>$1. 23</code>.</p> </li> 
     <li> <p><strong>[!UICONTROL Unformatted value]</strong> </p> <p>Les valeurs sont calculées mais ne sont pas mises en forme dans la réponse. Par exemple, si <code>A1</code> est <code>1. 23</code> et que <code>A2 </code> est <code>=A1</code> et mis en forme en tant que devise, alors <code>A2</code> renvoie le nombre <code>1. 23</code>.</p> </li> 
     <li> <p><strong>[!UICONTROL Formula]</strong> </p> <p>Les valeurs ne sont pas calculées. La réponse inclut les formules. Par exemple, si <code>A1</code> est <code>1. 23</code> et que <code>A2 </code> est <code>=A1</code> et mis en forme en tant que devise, alors <code>A2</code> renvoie <code>=A1</code>.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL Date and time render option]</td>
    <td>Sélectionnez le format des dates, des heures et de la durée dans la sortie. Ce champ est ignoré si [!UICONTROL Value Render] option est définie sur Valeur formatée. </td>
  </tr> 
  <tr>
    <td role="rowheader">[!UICONTROL Maximum number of returned responses]</td>
   <td> <p> Définissez le nombre maximal de réponses que [!DNL Workfront Fusion] renvoie au cours d’un cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search Responses (Advanced)]

Ce module effectue une recherche à l’aide de [[!DNL Google Charts Query Language]](https://developers.google.com/chart/interactive/docs/querylanguage?hl=fr). Ce module ne renvoie pas de numéro de ligne.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Spreadsheet]</td>
   <td> <p>Sélectionnez la feuille de calcul qui contient la feuille dans laquelle vous souhaitez effectuer une recherche.</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Sheet]</td>
   <td> <p> Sélectionnez la feuille contenant les réponses du formulaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td> <p>Définissez la requête à l’aide de <a href="https://developers.google.com/chart/interactive/docs/querylanguage?hl=fr">[!DNL Google Charts Query Language]</a>.</p> <p>Exemple : <code>select * where C = "John"</code> récupère toutes les valeurs de la ligne à l’endroit où la colonne C est « John ».</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Maximum number of returned rows]</td>
   <td> <p> Définissez le nombre maximal de réponses que [!DNL Workfront Fusion] renvoie au cours d’un cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>
