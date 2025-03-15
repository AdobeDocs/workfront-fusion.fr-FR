---
title: Modules Microsoft Office 365 Excel
description: Dans un scénario  [!DNL Adobe Workfront Fusion] , vous pouvez automatiser les workflows qui utilisent Microsoft 365 Excel et les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 059bc82b-f1bc-4b92-a44b-51c1daf14f08
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '2637'
ht-degree: 78%

---

# Modules [!DNL Microsoft Office 365 Excel]

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!DNL Microsoft 365 Excel] et le connecter à plusieurs applications et services tiers.

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

Pour utiliser [!DNL Microsoft office 365 Excel], vous devez disposer d’un compte Microsoft.

## Informations sur l’API Microsoft Office 365 Excel

Le connecteur Microsoft Office 365 Excel utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td> https://graph.microsoft.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Version de l’API</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v2.0.16</td> 
  </tr>
 </tbody> 
 </table>



## Connexion du service [!DNL Office 365 Excel] à [!DNL Workfront Fusion].

Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365 Excel] à [!UICONTROL Workfront Fusion], voir [Créer une connexion à [!UICONTROL Adobe Workfront Fusion] : instructions de base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Certaines applications Microsoft utilisent la même connexion, qui est liée à des autorisations d’utilisateur ou d’utilisatrice. Ainsi, lors de la création d’une connexion, l’écran de consentement aux autorisations affiche les autorisations précédemment accordées à la connexion de cet utilisateur ou de cette utilisatrice, en plus des nouvelles autorisations nécessaires à l’application actuelle.
>
>Par exemple, si un utilisateur ou une utilisatrice dispose d’autorisations « Lire le tableau » accordées via le connecteur Excel, puis crée une connexion dans le connecteur Outlook pour lire les e-mails, l’écran de consentement aux autorisations affiche à la fois l’autorisation « Lire le tableau » déjà accordée et l’autorisation « Écrire des e-mails » nouvellement requise.

## Modules [!DNL Microsoft Office 365 Excel] et leurs champs

Lorsque vous configurez les modules [!DNL Microsoft 365 Excel], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Microsoft 365 Excel] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Classeur](#workbook)
* [Feuille de travail](#worksheet)
* [Tableau](#table)
* [Autre](#other)

### Classeur

* [Télécharger un classeur](#download-a-workbook)
* [Rechercher des classeurs](#search-workbooks)
* [Surveiller des classeurs](#watch-workbooks)

#### [!UICONTROL Télécharger un classeur]

Ce module d’action télécharge le contenu du classeur Excel spécifié.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Download a workbook]</td> 
   <td> <p>Sélectionnez le mode d’identification du classeur à télécharger.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL By entering an ID manually]</strong> </p> <p>Dans le champ [!UICONTROL Workbook ID], saisissez ou mappez l’identifiant du classeur spécifique que le module doit télécharger.</p> </li> 
     <li> <p><strong>[!UICONTROL By selecting from the path]</strong> </p> <p>Dans le champ [!UICONTROL Workbook], sélectionnez le classeur que vous souhaitez que le module télécharge, y compris son chemin d’accès s’il ne se trouve pas dans le dossier racine.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody>

#### [!UICONTROL Rechercher des classeurs]

Ce module d’action recherche des classeurs [!DNL Excel].

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Sélectionnez le dossier dans lequel vous souhaitez rechercher des classeurs.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Filter]</p> </td> 
   <td> <p>Vous pouvez définir un filtre afin de rechercher uniquement les classeurs qui répondent aux critères sélectionnés.</p> <p>Pour chaque filtre, saisissez le champ que le filtre doit évaluer, l’opérateur et la valeur que le filtre doit autoriser. Vous pouvez utiliser plusieurs filtres en ajoutant des règles ET ou OU.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal de feuilles de calcul que le module doit renvoyer au cours de chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>
</table>

#### [!UICONTROL Surveiller des classeurs]

Ce module de déclenchement démarre un scénario lorsqu’un classeur est créé.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Sélectionnez le dossier que vous souhaitez utiliser pour surveiller les nouveaux classeurs.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Filter]</p> </td> 
   <td> <p>Vous pouvez définir un filtre afin de ne surveiller que les classeurs qui répondent aux critères que vous sélectionnez.</p> <p>Pour chaque filtre, saisissez le champ que le filtre doit évaluer, l’opérateur et la valeur que le filtre doit autoriser. Vous pouvez utiliser plusieurs filtres en ajoutant des règles ET ou OU.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal de classeurs que le module doit renvoyer au cours de chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Feuille de travail

* [[!UICONTROL Ajouter une feuille de travail]](#add-a-worksheet)
* [[!UICONTROL Ajouter une ligne de feuille de travail]](#add-a-worksheet-row)
* [[!UICONTROL Supprimer une ligne de feuille de travail]](#delete-a-worksheet-row)
* [[!UICONTROL Répertorier des lignes de feuille de travail]](#list-worksheet-rows)
* [[!UICONTROL Répertorier des feuilles de calcul]](#list-worksheets)
* [[!UICONTROL Mettre à jour une ligne de feuille de travail]](#update-a-worksheet-row)
* [[!UICONTROL Surveiller des lignes de feuille de travail]](#watch-worksheet-rows)

#### [!UICONTROL Ajouter une feuille de travail]

Ce module d’action crée une feuille de travail dans le classeur sélectionné.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL Workbook] </td>
   <td> <p>Sélectionnez le classeur auquel vous souhaitez ajouter une feuille de calcul, y compris le chemin d’accès si le classeur ne se trouve pas dans le répertoire racine.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Name] </td>
   <td> <p>Saisissez ou mappez un nom pour la nouvelle feuille de travail.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ajouter une ligne de feuille de travail]

Ce module d’action ajoute une nouvelle ligne à la feuille de travail sélectionnée.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Workbook] </td>
   <td> <p>Sélectionnez le classeur qui contient la feuille de calcul dans laquelle vous souhaitez ajouter une ligne, y compris le chemin d'accès si le classeur ne se trouve pas dans le répertoire racine.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Worksheet] </td>
   <td> <p>Sélectionnez la feuille de travail dans laquelle vous souhaitez ajouter une ligne.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Type of values being entered]</p> </td> 
   <td> <p>Sélectionnez le type de valeur à renseigner dans la feuille de travail. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Formulas]</strong> </p> <p> Excel tente d’évaluer l’expression spécifiée. Les noms des fonctions d’une formule sont en anglais. Exemple : <code>[!DNL =SUM(A1:A10)]</code></p> </li> 
     <li> <p><strong>[!UICONTROL Formulas local]</strong> </p> <p>Excel tente d’évaluer l’expression spécifiée. Les noms des fonctions sont dans la langue de l’application Excel. Exemple : <code>=SUM(A1, 1.5)</code> vs <code>=SUMME(A1; 1,5)</code></p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Excel n’évalue pas la valeur. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Row]</td>
    <td>Pour chaque colonne, saisissez la valeur à lui donner dans la nouvelle ligne.</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Supprimer une ligne de feuille de travail]

Ce module d’action supprime une ligne d’une feuille de travail.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Workbook] </td>
   <td> <p>Sélectionnez le classeur qui contient la feuille de travail et la ligne à supprimer.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Worksheet]</td>
   <td> <p> Sélectionnez la feuille de travail contenant la ligne à supprimer.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Row ID]</td>
   <td>Saisissez ou mappez l’identifiant de la ligne à supprimer.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Lister les lignes de feuille de travail]

Ce module d’action récupère une liste de lignes d’une feuille de travail spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL Workbook] </td>
   <td> <p>Sélectionnez le classeur qui contient la feuille de calcul contenant les lignes à répertorier, y compris le chemin d'accès si le classeur ne se trouve pas dans le répertoire racine.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Worksheet] </td>
   <td> <p>Sélectionnez la feuille de travail qui contient les lignes que vous souhaitez répertorier.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Limit]</td>
   <td> <p>Saisissez ou mappez le nombre maximal de lignes de feuille de travail que le module doit renvoyer au cours de chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Répertorier des feuilles de calcul]

Ce module d’action récupère une liste de feuilles de calcul dans le classeur spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Workbook] </td>
   <td> <p>Sélectionnez le classeur qui contient les feuilles de calcul que le module doit répertorier.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Limit]</td>
   <td> <p>Saisissez ou mappez le nombre maximal de feuilles de calcul que le module doit renvoyer au cours de chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mettre à jour une ligne de feuille de travail]

Ce module d’action met à jour une ligne de feuille de travail existante.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Workbook] </td>
   <td> <p>Sélectionnez le classeur qui contient la feuille de travail et la ligne à mettre à jour.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Worksheet] </td>
   <td> <p>Sélectionnez la feuille de travail contenant la ligne à mettre à jour.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Type of values being entered]</p> </td> 
   <td> <p>Sélectionnez le type de valeur à renseigner dans la feuille de travail. </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Formulas]</strong> </p> <p> Excel tente d’évaluer l’expression spécifiée. Les noms des fonctions d’une formule sont en anglais. Exemple : <code>[!DNL =SUM(A1:A10)]</code></p> </li> 
     <li> <p><strong>[!UICONTROL Formulas local]</strong> </p> <p>Excel tente d’évaluer l’expression spécifiée. Les noms des fonctions sont dans la langue de l’application Excel. Exemple : <code>=SUM(A1, 1.5)</code> vs <code>=SUMME(A1; 1,5)</code></p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Excel n’évalue pas la valeur. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Row ID]</td> 
   <td>Sélectionnez le numéro de la ligne à mettre à jour.</td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Row]</td>
    <td>Pour chaque colonne, saisissez la valeur à lui donner dans la nouvelle ligne.</td>
    </tr> 
 </tbody> 
</table>

#### [!UICONTROL Surveiller des lignes de feuille de travail]

Ce module déclencheur lance un scénario lorsqu’une nouvelle ligne est ajoutée à la feuille.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Workbook] </td>
   <td> <p>Sélectionnez le classeur qui contient la feuille de travail dans laquelle vous souhaitez surveiller les nouvelles lignes.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL Worksheet] </td>
   <td> <p>Sélectionnez la feuille Excel dans laquelle vous souhaitez surveiller les nouvelles lignes.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL Ignorer les lignes vides] </td>
   <td> <p>Activez cette option pour ne pas renvoyer de lots pour les lignes vides dans la feuille de calcul.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Limit]</td>
   <td> <p>Saisissez ou mappez le nombre maximal de lignes de feuille de travail que le module doit renvoyer au cours de chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Tableau

* [[!UICONTROL Ajouter un tableau]](#add-a-table)
* [[!UICONTROL Ajouter une ligne de tableau]](#add-a-table-row)
* [[!UICONTROL Supprimer un tableau]](#delete-a-table)
* [[!UICONTROL Obtenir un tableau]](#get-a-table)
* [[!UICONTROL Lister les lignes de tableau]](#list-table-rows)
* [[!UICONTROL Lister les tableaux]](#list-tables)
* [[!UICONTROL Mettre à jour un tableau]](#update-a-table)
* [[!UICONTROL Surveiller les lignes de tableau]](#watch-table-rows)

#### [!UICONTROL Ajouter un tableau]

Ce module d’action crée un élément de tableau dans la feuille de travail Excel.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workbook] </td> 
   <td> <p>Sélectionnez le classeur qui contient la feuille de travail dans laquelle vous souhaitez ajouter un tableau.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Worksheet] </td> 
   <td> <p>Sélectionnez la feuille de travail dans laquelle vous souhaitez ajouter un tableau.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Has headers]</td> 
   <td> <p>Activez cette option pour définir la première ligne comme en-têtes de tableau.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Address]</p> </td> 
   <td> <p>Définissez la taille du tableau en indiquant les cellules supérieure gauche et inférieure droite. Exemple : <code>A1:C10</code> crée un tableau de 3 colonnes et 10 lignes.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Ajouter une ligne de tableau]

Ce module d’action modifie un tableau existant.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Workbook] </td>
   <td> <p>Sélectionnez le classeur qui contient le tableau dans lequel vous souhaitez ajouter une ligne.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Worksheet] </td>
   <td> <p>Sélectionnez la feuille de travail contenant le tableau dans lequel vous souhaitez ajouter une ligne.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Table]</td>
   <td>Sélectionnez le tableau dans lequel vous souhaitez ajouter une ligne.</td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL Row]</td>
    <td>Pour chaque colonne, saisissez la valeur à lui donner dans la nouvelle ligne.</td>
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Row ID]</p> </td> 
   <td> <p>Pour ajouter une ligne à un emplacement spécifique du tableau, saisissez ou mappez un numéro de ligne. Le module insère la nouvelle ligne après cette ligne.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Supprimer un tableau]

Ce module d’action supprime le tableau spécifié d’une feuille de travail [!DNL Excel].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Supprimer une table]</td> 
   <td> <p>Sélectionnez le mode d’identification du tableau à supprimer.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez l'ID du classeur contenant la table à supprimer, puis saisissez ou mappez l'ID de la feuille de calcul contenant la table.</p> <p>Dans le champ [!UICONTROL Table Name], saisissez ou mappez le nom du tableau à supprimer.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le classeur et la feuille de travail qui contiennent le tableau à supprimer, puis sélectionnez-le.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obtenir un tableau]

Ce module d’action récupère les métadonnées du tableau spécifié.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> 
     <p >[!UICONTROL Connection]</p>
   </td> 
   <td> 
     <p>Pour obtenir des instructions sur la connexion de votre compte Office 365 à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p>
    --&gt; </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get a table]</td> 
   <td> <p>Sélectionnez le mode d’identification du tableau que vous souhaitez récupérer.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez l'ID du classeur contenant la table à récupérer, puis saisissez ou mappez l'ID de la feuille de calcul contenant la table.</p> <p>Dans le champ [!UICONTROL Table Name], saisissez ou mappez le nom du tableau à récupérer.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le classeur et la feuille de travail qui contiennent le tableau à récupérer, puis sélectionnez le tableau.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Répertorier des lignes de tableau]

Ce module de recherche récupère une liste de toutes les lignes d’un tableau dans un classeur.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Workbook] </td>
   <td> <p>Sélectionnez le classeur qui contient le tableau comprenant les lignes à répertorier.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Worksheet] </td>
   <td> <p>Sélectionnez la feuille de travail qui contient le tableau comprenant les lignes à répertorier.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Table] </td>
   <td> <p>Sélectionnez le tableau contenant les lignes à répertorier.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Limit]</td>
   <td> <p>Saisissez ou mappez le nombre maximal de lignes de tableau que le module doit renvoyer pour chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Lister des tableaux]

Ce module de recherche récupère une liste de tous les objets de tableau.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[!UICONTROL Workbook] </td>
   <td> <p>Sélectionnez le classeur qui contient les tableaux que vous souhaitez répertorier.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Worksheet] </td>
   <td> <p>Sélectionnez la feuille de travail qui contient les tableaux que vous souhaitez répertorier.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Limit]</td>
   <td> <p>Saisissez ou mappez le nombre maximum de tableaux que le module doit renvoyer pour chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mettre à jour un tableau]

Ce module d’action met à jour un tableau existant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Update a table]</td> 
   <td> <p>Sélectionnez le mode d’identification du tableau à mettre à jour.</p> 
    <ul> 
     <li> <p><strong>Saisie manuelle</strong> </p> <p>Dans le champ [!UICONTROL Workbook ID], saisissez ou mappez l’identifiant du classeur qui contient le tableau à mettre à jour.</p> <p>Dans le champ [!UICONTROL Table Name], saisissez ou mappez le nom du tableau à mettre à jour.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Sélectionnez le classeur et la feuille de travail qui contiennent le tableau à mettre à jour, puis sélectionnez le tableau.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td> <p>Si vous souhaitez renommer le tableau, saisissez ou mappez un nouveau nom pour le tableau.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show Headers]</td> 
   <td> <p>Activez cette option pour afficher les en-têtes du tableau mis à jour.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show totals]</td> 
   <td>Activez cette option pour afficher les valeurs totales du tableau.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Style]</td> 
   <td>Appliquez un style pour le nouveau tableau.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Surveiller les lignes de tableau]

Ce déclencheur lance un scénario lorsqu’une nouvelle ligne est ajoutée à un tableau.

>[!NOTE]
>
>Le tableau désigne ici l’élément de tableau incorporé dans le classeur. Il ne s’agit pas du tableau complet (classeur/feuille).

![Table incorporée](/help/workfront-fusion/references/apps-and-modules/assets/embedded-table-350x420.png)

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Workbook]</p> </td> 
   <td> <p>Sélectionnez le classeur qui contient le tableau à surveiller.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Worksheet] </td>
   <td> <p> Sélectionnez la feuille de travail contenant le tableau à surveiller.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Table]</p> </td> 
   <td> <p>Sélectionnez le tableau à surveiller.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Limit]</td>
   <td> <p>Saisissez ou mappez le nombre maximal de lignes que le module doit renvoyer pour chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Autre

* [[!UICONTROL Effectuer un appel API]](#make-an-api-call)
* [[!UICONTROL Récupérer les données]](#retrieve-data)

#### [!UICONTROL Effectuer un appel API]

Ce module d’action vous permet d’effectuer un appel API personnalisé.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Saisissez un chemin relatif à <code>https://graph.microsoft.com</code>. Exemple :<code> /v1.0/me/drive/root/children</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion ajoute les en-têtes d’autorisation pour vous.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Ajoutez la requête pour l’appel API sous la forme d’un objet JSON standard.</p> <p>Par exemple : <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :   <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre JSON, placez les guillemets à l’extérieur de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Récupérer les données]

Cette action récupère les données de la plage de feuilles de travail définie et renvoie un lot pour chaque ligne.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workbook] </td> 
   <td> <p>Sélectionnez le classeur qui contient les données à récupérer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Worksheet] </td> 
   <td> <p>Sélectionnez la feuille de travail contenant les données à récupérer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Range] </td> 
   <td> <p>Indiquez la zone de la feuille à partir de laquelle vous souhaitez récupérer les données en indiquant les cellules supérieure gauche et inférieure droite. Exemple : <code>A1:D10</code></p> </td> 
  </tr> 
 </tbody> 
</table>
