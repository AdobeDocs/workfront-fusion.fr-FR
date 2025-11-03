---
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent Anaplan et les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: 81c9b141-4e40-430f-99f1-c44b7a833bcd
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '2029'
ht-degree: 71%

---

# Modules [!DNL Anaplan]

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent [!DNL Anaplan] et les connecter à plusieurs applications et services tiers.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tout package de workflow Adobe Workfront et tout package d’automatisation et d’intégration Adobe Workfront</p><p>Workfront Ultimate</p><p>les packages Workfront Prime et Select, avec un achat supplémentaire de Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licences Adobe Workfront</td> 
   <td> <p>Standard</p><p>Travail ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licence Adobe Workfront Fusion</td> 
   <td>
   <p>Basé sur les opérations : aucune exigence de licence Workfront Fusion</p>
   <p>Basé sur un connecteur (hérité) : Workfront Fusion pour l’automatisation et l’intégration du travail </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Si votre entreprise dispose d’un package Select ou Prime Workfront qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acheter Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Conditions préalables

Avant d’utiliser le connecteur [!DNL Anaplan], assurez-vous que les conditions préalables suivantes sont remplies :

* Vous devez avoir un compte [!UICONTROL Anaplan] actif.
* Vous devez configurer des espaces de travail, des modèles et d’autres objets [!DNL Anaplan] dans votre compte [!UICONTROL Anaplan] avant que Workfront Fusion puisse interagir avec eux.

## Informations sur l’API Anaplan

Le connecteur Anaplan utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td>https://api.anaplan.com/2/0/
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Version de l’API</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.11.5</td> 
 </tbody> 
</table>

## Connecter [!DNL Anaplan] à Workfront Fusion {#connect-anaplan-to-workfront-fusion}

Pour créer une connexion pour vos modules [!DNL Anaplan], procédez comme suit :

1. Cliquez sur **[!UICONTROL Ajouter]** en regard de la zone [!UICONTROL Connexion].
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
        <td role="rowheader">[!UICONTROL email]</td>
        <td>
          <p>Saisissez l’adresse e-mail de ce compte Anaplan</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Password]</td>
        <td>Saisissez le mot de passe de ce compte Anaplan.</td>
      </tr>
     </tbody>
    </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour enregistrer la connexion et revenir au module.

<!--1. Click **[!UICONTROL Add]** next to the [!UICONTROL Connection] box.
1. Select the connection type.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!DNL Anaplan] [!UICONTROL Basic]</td> 
      <td> <p>An [!DNL Anaplan] [!UICONTROL Basic] connection requires only an email address and password to create the connection. </p> <p>Enter a name for the connection, then enter your email address and the password of your [!DNL Anaplan] account.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!DNL Anaplan] [!UICONTROL CA Certificate]</td> 
      <td> <p>An [!DNL Anaplan] [!UICONTROL CA Certificate] connection requires a [!UICONTROL Certificate Key], [!UICONTROL Encoded Data], and [!UICONTROL Encoded Signed Data]. You can generate these in your [!DNL Anaplan] account. For instructions, see the [!DNL Anaplan] documentation.</p> <p>Enter a name for the connection, then enter the [!UICONTROL Certificate Key], [!UICONTROL Encoded Data], and [!UICONTROL Encoded Signed Data] that you generated in your [!DNL Anaplan] account.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Click **[!UICONTROL Continue]** to save the connection and return to the module.-->

## Modules [!DNL Anaplan] et leurs champs

Lorsque vous configurez les modules [!DNL Anaplan], Workfront Fusion affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Anaplan] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Déclencheurs](#triggers)
* [Actions](#actions)
* [Recherches](#searches)

### Déclencheurs

#### [!DNL Watch records]

Ce module de déclenchement lance un scénario lorsqu’un enregistrement du type choisi est créé ou mis à jour.

>[!NOTE]
>
>Ce module renvoie les données des nouveaux enregistrements. Il ne renvoie pas les données des enregistrements existants modifiés.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Anaplan], voir <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Anaplan] à Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type d’objet à surveiller</td> 
   <td>Sélectionnez le type d’élément à surveiller. Le scénario commence lorsque ce type d’enregistrement est créé ou mis à jour.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID d’&lt;Object&gt;</td> 
   <td>Saisissez l’identifiant de l’objet dans Anplan, tel qu’un modèle ou un module, associé aux objets que vous souhaitez surveiller.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Limite</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [[!UICONTROL Créer un élément de liste]](#create-a-list-item)
* [Supprimer un enregistrement](#delete-a-record)
* [Exporter des données](#export-data)
* [Importer des données](#import-data)
* [[!UICONTROL Lancer un appel API personnalisé]](#make-a-custom-api-call)
* [[!UICONTROL Lire un enregistrement]](#read-a-record)
* [[!UICONTROL Exécuter une action]](#run-an-action)
* [[!UICONTROL Mettre à jour un enregistrement]](#update-a-record)
* [[!UICONTROL Charger un fichier]](#upload-a-file)

#### [!UICONTROL Créer un élément de liste]

Ce module d’action ajoute un nouvel élément à une liste dans Anaplan.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Connection]</td>
        <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Anaplan], voir <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Anaplan] à Workfront Fusion</a> dans cet article.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Workspace ID]</td>
        <td>Sélectionnez ou mappez l’identifiant de l’espace de travail Anaplan qui contient la liste dans laquelle vous souhaitez ajouter un élément.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Model ID]</td>
        <td>Sélectionnez ou mappez l’identifiant du modèle qui contient la liste dans laquelle vous souhaitez ajouter un élément.</td>
    </tr>
    <tr>
        <td>[!UICONTROL List ID]</td>
        <td>Sélectionnez ou mappez l’identifiant de la liste dans laquelle vous souhaitez créer un élément.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Name]</td>
        <td>Saisissez un nom pour le nouvel élément.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Code]</td>
        <td>Saisissez le code du nouvel élément. Les codes sont des codes générés par la personne qui vous permettent de distinguer les éléments de ligne portant le même nom.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Parent]</td>
        <td>Saisissez le nom de l’élément parent sous lequel vous souhaitez créer l’élément.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Properties]</td>
        <td>Si la liste dans laquelle vous souhaitez ajouter un élément comporte des propriétés personnalisées, sélectionnez les propriétés pour lesquelles vous souhaitez ajouter des valeurs, puis ajoutez les valeurs.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Subsets]</td>
        <td>Si la liste à laquelle vous souhaitez ajouter des éléments comporte des sous-ensembles personnalisés, sélectionnez les sous-ensembles auxquels vous souhaitez ajouter l’élément.</td>
    </tr>
</table>

#### [!UICONTROL Supprimer un enregistrement]

Ce module d’action supprime un enregistrement existant.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Anaplan], voir <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Anaplan] à Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Sélectionnez ou mappez l’identifiant de l’espace de travail Anaplan qui contient l’objet que vous souhaitez supprimer.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model ID]</td> 
   <td>Saisissez ou mappez l’identifiant du modèle qui contient l’objet que vous souhaitez supprimer.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type d'enregistrement</td> 
   <td> <p>Sélectionnez le type d’objet à supprimer.</p> 
    <ul> 
     <li> <p><b>Actions</b> </p> <p>Sélectionnez ou mappez l’action à supprimer.</p> </li> 
     <li> <p><b>Élément de liste</b> </p> <p>Sélectionnez la liste dans laquelle vous souhaitez supprimer un élément, puis saisissez ou mappez l’identifiant ou le code de l’élément à supprimer.</p>  </li> 
     <li> <p><b>[!UICONTROL File]</b> </p> <p>Sélectionnez ou mappez le fichier à supprimer.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>



#### [!UICONTROL Exporter des données]

Ce module d’action récupère les données d’Anaplan à l’aide des Définitions d’exportation .

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Anaplan], voir <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Anaplan] à Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Sélectionnez ou mappez l’identifiant du Workspace Anaplan contenant les données à exporter.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model ID]</td> 
   <td>Saisissez ou mappez l’identifiant du modèle contenant les données à exporter.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de définition de l’exportation</td> 
   <td> <p>Saisissez ou mappez l’identifiant de la définition d’exportation Anaplan que vous souhaitez utiliser.</p> 
   </td> 
  </tr> 
 </tbody> 
</table>

#### Importer des données

Ce module d’action importe des données dans Anaplan.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Anaplan], voir <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Anaplan] à Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>Sélectionnez ou mappez l’identifiant du Workspace Anaplan sur lequel vous souhaitez importer les données.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model ID]</td> 
   <td>Saisissez ou mappez l'identifiant du modèle sur lequel vous souhaitez importer les données.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de définition de l’exportation</td> 
   <td> <p>Saisissez ou mappez l'ID de la définition d'importation Anaplan que vous souhaitez utiliser.</p> 
   </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Lancer un appel API personnalisé]

Ce module vous permet d’effectuer un appel API personnalisé à l’API [!DNL Anaplan].

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Anaplan], voir <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Anaplan] à Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Saisir un chemin relatif à <code>https://api.anaplan.com/2/0/</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion ajoute automatiquement des en-têtes d’autorisation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String] </td> 
   <td> <p>Saisissez la chaîne de requête.</p> </td> 
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

#### [!UICONTROL Lire un enregistrement]

Ce module d’action lit un seul enregistrement.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Anaplan], voir <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Anaplan] à Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement à lire.</p> 
    <ul> 
     <li> <p><b>Modèle</b> </p> <p>Sélectionnez ou mappez l’identifiant du modèle à lire.</p> </li> 
     <li> <p><b>Liste de modèles</b> </p> <p>Sélectionnez ou mappez les identifiants de l’espace de travail et du modèle qui contiennent la liste que vous souhaitez lire, puis sélectionnez la liste. Dans le champ [!UICONTROL Data type], indiquez si vous souhaitez lire des données ou des métadonnées.</p> </li> 
     <li> <p><b>Version du modèle</b> </p> <p>Sélectionnez ou mappez l’identifiant du modèle que vous souhaitez lire.</p> </li> 
     <li> <p><b>Utilisateur ou utilisatrice</b> </p> <p>Indiquez si vous souhaitez renvoyer des données sur le ou la propriétaire du compte utilisé ou sur une autre personne. Si vous sélectionnez une autre personne, sélectionnez son nom.</p> </li> 
     <li> <p><b>Espace de travail</b> </p> <p>Sélectionnez ou mappez l’identifiant de l’espace de travail que vous souhaitez lire.</p> </li> 
     <li> <p><b>Afficher</b> </p> <p>Sélectionnez ou mappez l'identifiant du modèle contenant la vue que vous souhaitez lire.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Exécuter une action]

Ce module d’action importe, exporte, supprime ou traite une action.

<table style="table-layout:auto"> 
     <col/>
     <col/>
     <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection]</td>
        <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Anaplan], voir <a href="#Connect" class="MCXref xref" >[!UICONTROL Connect Anaplan to Workfront Fusion]</a> dans cet article.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Workspace ID]</td>
        <td>Sélectionnez ou mappez l’identifiant de l’espace de travail[!DNL Anaplan] dans lequel vous souhaitez effectuer l’action.</td>
      </tr>
      <tr >
        <td role="rowheader">[!UICONTROL Model ID]</td>
        <td>Sélectionnez ou mappez l’identifiant du modèle dans lequel vous souhaitez effectuer l’action.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Action type]</td>
        <td>
          <p>Sélectionnez l’action que vous souhaitez effectuer.</p>
            <ul>
              <li>
                <p><b>[!UICONTROL Delete]</b>
                </p>
                <p>Saisissez ou mappez l’identifiant de l’action que vous souhaitez supprimer.</p>
              </li>
              <li>
                <p><b>[!UICONTROL Export]</b>
                </p>
                <p>Saisissez ou mappez l’identifiant de la définition d’exportation que vous souhaitez utiliser. Vous pouvez exporter vers les formats de fichier suivants :</p>
                  <ul>
                    <li>
                      <p>XLS</p>
                    </li>
                    <li>
                      <p>XLSX</p>
                    </li>
                    <li>
                      <p>CSV</p>
                    </li>
                  </ul>
                </li>
                <li>
                  <p><b>[!UICONTROL Import] </b>
                  </p>
                  <p style="font-weight: normal;">Saisissez ou mappez l’identifiant de la définition d’importation que vous souhaitez utiliser.</p>
                </li>
                <li>
                 <p><b>[!UICONTROL Process]</b>
                 </p>
                  <p>Saisissez ou mappez l’identifiant du processus que vous souhaitez utiliser. </p>
                </li>
              </ul>
            </td>
          </tr>
        </tbody>
      </table>


#### [!UICONTROL Mettre à jour un enregistrement]

Ce module d’action met à jour un seul enregistrement dans [!UICONTROL Anaplan].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Anaplan], voir <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Anaplan] à Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement que vous souhaitez mettre à jour.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL List item]</b> </p> <p>Pour les champs, voir <a href="#create-a-list-item" class="MCXref xref">Créer un élément de liste</a> dans cet article.</p> </li> 
     <li> <p><b>[!UICONTROL Module cell data]</b> </p> <p>Lorsque vous mettez à jour les données de cellule, tous les calculs en aval qui utilisent ces données sont également mis à jour.</p> <p>Remplissez les champs suivants :</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Model ID]</b> </p> <p>Sélectionnez ou mappez le modèle qui contient la cellule que vous souhaitez mettre à jour.</p> </li> 
       <li> <p><b>[!UICONTROL Module ID]</b> </p> <p>Sélectionnez ou mappez le module contenant la cellule que vous souhaitez mettre à jour.</p> </li> 
       <li> <p><b>[!UICONTROL Line item name]</b> </p> <p>Sélectionnez ou mappez l’élément de ligne de la cellule à mettre à jour.</p> </li> 
       <li> <p style="font-weight: bold;">[!UICONTROL Dimension ID]</p> <p>Sélectionnez ou mappez la dimension qui se trouve sur l’élément de ligne.</p> 
       <p><b>Note :</b> 
       <ul>
       <li> La clé de Dimension (valeur) doit être : <code>dimensionName</code> (suivant) ou <code>dimensionId</code> (ID).</li>
       <li>La clé d’élément (valeur) doit être <code>itemName</code> (texte), <code>itemCode</code> (texte) ou <code>itemId</code> (ID).</li>
       <li>Les clés de Dimension et d’élément doivent être du même type (texte ou identifiant).
       </ul>
        </p> 
        <p>Pour plus d’informations sur les dimensions, recherchez Dimensions dans le [!DNL Anaplan Anapedia].</p> </li> 
       <li> <p><b>[!UICONTROL Value]</b> </p> <p>Saisissez ou mappez la nouvelle valeur pour la cellule.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Model current fiscal year]</b> </p> <p>Saisissez l’identifiant de l’espace de travail et l’identifiant du modèle pour lequel vous souhaitez mettre à jour l’année fiscale, puis saisissez ou mappez la nouvelle année pour le modèle.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Charger le fichier pour action]

Ce module d’action charge un fichier existant dans Anaplan vers des emplacements supplémentaires dans Anaplan.
<table style="table-layout:auto">
<col>
<col>
<tbody>
<tr>
<td role="rowheader">[!UICONTROL Connection]</td>
<td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Anaplan], voir <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Anaplan] à Workfront Fusion</a> dans cet article.</td>
</tr>
<tr>
<td role="rowheader">[!UICONTROL Workspace ID]</td>
<td>Sélectionnez ou mappez l’identifiant de l’espace de travail [!DNL Anaplan] dans lequel vous souhaitez charger un fichier.</td>
</tr>
<tr>
<td role="rowheader">[!UICONTROL Model ID]</td>
<td>Sélectionnez ou mappez l’identifiant du modèle dans lequel vous souhaitez charger un fichier.</td>
</tr>
<tr>
<td role="rowheader">[!UICONTROL File ID]</td>
<td>Sélectionnez ou mappez l’identifiant du fichier que vous souhaitez charger.</td>
</tr>
</tbody>
</table>
</div>

### Recherches

#### [!UICONTROL Obtenir un enregistrement]

Ce module de recherche renvoie tous les enregistrements accessibles du type sélectionné.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Anaplan], voir <a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL Anaplan] à Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record types]</td> 
   <td> <p>Sélectionnez le type d’enregistrement que vous souhaitez récupérer.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Workspaces]</b> </p> </li> 
       <li> <p><b>[!UICONTROL Models]</b> </p> </li> 
       <li> <p><b>[!UICONTROL Line items]</b> </p> <p>Sélectionnez ou mappez l’identifiant du modèle qui contient les éléments [!DNL line] que vous souhaitez récupérer.</p> </li> 
       <li> <p><b>[!UICONTROL Model lists]</b> </p> <p>Sélectionnez ou mappez l’identifiant de l’espace de travail et l’identifiant du modèle qui contiennent les listes de modèles que vous souhaitez récupérer.</p> </li> 
       <li> <p><b>[!UICONTROL Model calendar]</b> </p> <p>Sélectionnez ou mappez l’identifiant de l’espace de travail qui contient le calendrier du modèle que vous souhaitez récupérer.</p> </li> 
       <li> <p><b>[!UICONTROL Versions du modèle]</b> </p> </li> 
       <li> <p>Sélectionnez ou mappez l’identifiant du modèle contenant les versions de modèle à récupérer.</p> </li> 
       <li> <p><b>[!UICONTROL Users]</b> </p> </li> 
       <li> <p><b>[!UICONTROL Views]</b> </p> <p>Choisissez si vous souhaitez choisir la vue par module ou par modèle, puis sélectionnez ou mappez l’identifiant du module ou du modèle qui contient la vue que vous souhaitez récupérer.</p> </li> 
      </ul> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Return workspace size]</td> 
   <td>Activez cette option pour renvoyer une estimation de la taille actuelle de l’espace de travail. Cette estimation est basée sur la taille de tous les modules de l’espace de travail.</td> 
  </tr> 
 </tbody> 
</table>
