---
title: Modules Airtable
description: Adobe Workfront Fusion nécessite une licence Adobe Workfront Fusion en plus d’une licence Adobe Workfront.
author: Becky
feature: Workfront Fusion
exl-id: 3b445b50-5812-4ded-9788-f467991e0b52
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '1858'
ht-degree: 98%

---

# Modules Airtable


Avec le connecteur [!DNL Airtable] pour [!DNL Adobe Workfront Fusion], vous pouvez démarrer un scénario en fonction des événements de votre compte [!DNL Airtable], créer, charger et mettre à jour des enregistrements, rechercher des enregistrements et effectuer des appels API personnalisés vers l’API Airtable.

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
   <td> <p>[!UICONTROL [!DNL Workfront Fusion] pour l’automatisation et l’intégration du travail] </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>Votre entreprise doit acheter [!DNL Adobe Workfront Fusion] ainsi qu’[!DNL Adobe Workfront] pour utiliser les fonctionnalités décrites dans cet article.</td> 
  </tr> 
 </tbody> 
</table>

Pour connaître le plan, le type de licence ou l’accès dont vous disposez, contactez votre administrateur ou administratrice [!DNL Workfront].

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Conditions préalables

Vous devez disposer d’un compte Airtable pour utiliser les fonctionnalités de cet article.

<!--
<p>For more information, see the tutorial .</p>
-->

## Informations sur l’API Airtable

Le connecteur Airtable utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td>https://api.airtable.com/v0</td> 
  </tr>
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v3.3.28</td> 
  </tr>
 </tbody> 
 </table>

## Connecter Airtable à Workfront Fusion {#connect-airtable-to-workfront-fusion}

<!--

1. Log in to your Airtable account.
1. Open your account overview and generate the API key.
-->
1. Ouvrez Workfront Fusion et la boîte de dialogue **Créer une connexion** du module souhaité.
1. Saisissez un nom pour la connexion.
1. (Facultatif) Cliquez sur Afficher les paramètres avancés, puis saisissez votre ID client Airtable et votre secret client.
1. Cliquez sur le bouton **Continuer** pour créer la connexion et revenir au module.

## Modules Airtable et leurs champs

### Enregistrements

* [Créer un enregistrement](#create-a-record)
* [Supprimer un enregistrement](#delete-a-record)
* [Obtenir un enregistrement](#get-a-record)
* [Rechercher des enregistrements](#search-records)
* [Mettre à jour un enregistrement](#update-a-record)
* [Mettre à jour et insérer un enregistrement](#upsert-a-record)
* [Surveillez des enregistrements](#watch-records)
* [Regarder des réponses](#watch-responses)
* [Effectuer un appel API](#make-an-api-call)

#### Créer un enregistrement {#create-a-record}

Ce module d’action crée un nouvel enregistrement.

Vous indiquez les données que vous souhaitez dans l’enregistrement et leur emplacement de stockage.

Le module renvoie tous les champs standard associés à l’enregistrement, ainsi que tous les champs et valeurs personnalisés auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Connexion </td> 
   <td> <p>Pour des instructions sur la connexion de votre compte Airtable à Workfront Fusion, voir <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Connecter Airtable à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>Base </td> 
   <td> <p>Sélectionnez la base à laquelle doit appartenir le nouvel enregistrement.</p> </td> 
  </tr> 
  <tr> 
   <td>Tableau </td> 
   <td> <p>Sélectionnez le tableau auquel doit appartenir le nouvel enregistrement.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Enregistrement</p> </td> 
   <td> <p>Saisissez les valeurs du nouvel enregistrement. Les champs disponibles dépendent du tableau que vous avez sélectionné.</p> <!--<p>For more information on field types, search for "Supported field types" in the Airtable documentation.</p> 
    <ul> 
     <li> <p><strong>Text</strong>: string</p> <p>A single line of text.</p> </li> 
     <li> <p><strong>Long text</strong>: string</p> <p>Multiple lines of text, which may contain "mention tokens", for example:</p><pre>&lt;airtable:mention id="menE1i9oBaGX3DseR"&gt;@Alex&lt;/airtable:mention&gt;</pre> </li> 
     <li><strong>Attachment</strong> : Add the attachment. Airtable will download the file from the provided <code>url</code> and keep its own copy of it. If the File name field is left empty, Airtable generates the name automatically.</li> 
     <li><strong>Checkbox</strong>: Select one of the options.</li> 
     <li><strong>Multiple select</strong>: Select multiple options in the checklist.</li> 
     <li><strong>Single select</strong>: Select one option from the drop-down menu.</li> 
     <li><strong>Collaborator</strong>: Enter the email that uniquely identifies a user in Airtable who this base is shared with.</li> 
     <li><strong>Date</strong>: UTC date, for example, 2019-09-05 (ISO 8601 formatted date)</li> 
     <li>Phone number:</li> 
     <li><strong>Emails</strong>: A valid email address.</li> 
     <li><strong>URL</strong>: A valid URL (for example, airtable.com or https://airtable.com/universe).</li> 
     <li><strong>Number</strong>: Enter a number.</li> 
     <li><strong>Currency</strong>: Currency value.</li> 
     <li><strong>Percent</strong>: A percentage value. Must be higher than or equal to 0.</li> 
     <li><strong>Duration</strong>: Enter the duration time. If you need help, see the information about the duration field type in the Airtable support documentation. </li> 
     <li><strong>Rating</strong>: Enter the number. For example, "3 stars" is 3. A rating cannot be 0.</li> 
     <li><strong>Link</strong>: Enter the linked records IDs from the table. The order of record IDs will be reversed compared to what you see in the app.</li> 
     <li><strong>Rollup</strong>: Computed value: COUNT(values)</li> 
     <li><strong>Lookup</strong>: Array of long text fields</li> 
     <li><strong>Autonumber</strong>: Automatically incremented unique counter for each record.</li> 
     <li> <p><strong>Barcode</strong>: The barcode object may contain the following two properties, both of which are optional.</p> <p>Barcode data (text)</p> <p>Barcode symbology, for example, "upce" or "code39" (type)</p> </li> 
    </ul> --></td> 
  </tr> 
  <tr> 
   <td>Liens intelligents</td> 
   <td> <p>Activez cette option pour saisir des noms plutôt que des ID d’enregistrement pour les champs liés à un autre tableau. L’enregistrement est automatiquement créé dans le tableau lié en cas d’absence de correspondance.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Supprimer un enregistrement {#delete-a-record}

Ce module d’action supprime un enregistrement particulier.

Vous spécifiez l’ID et les emplacements de l’enregistrement.

Le module renvoie l’ID de l’enregistrement et tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Connexion </td> 
   <td> <p>Pour des instructions sur la connexion de votre compte Airtable à Workfront Fusion, voir <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Connecter Airtable à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>Base </td> 
   <td> <p>Sélectionnez la base contenant l’enregistrement que vous souhaitez supprimer.</p> </td> 
  </tr> 
  <tr> 
   <td>Tableau </td> 
   <td> <p>Sélectionnez le tableau contenant l’enregistrement à supprimer.</p> </td> 
  </tr> 
  <tr> 
   <td>ID de l’enregistrement</td> 
   <td> <p>Saisissez ou mappez l’ID Airtable unique de l’enregistrement que vous souhaitez que le module supprime. Vous pouvez récupérer l’ID, par exemple, à l’aide du module Rechercher des enregistrements.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Obtenir un enregistrement {#get-a-record}

Ce module d’action récupère les détails des enregistrements.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Connexion </td> 
   <td> <p>Pour des instructions sur la connexion de votre compte Airtable à Workfront Fusion, voir <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Connecter Airtable à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>Base </td> 
   <td> <p>Sélectionnez la base contenant le tableau avec l’enregistrement que vous souhaitez récupérer.</p> </td> 
  </tr> 
  <tr> 
   <td>Tableau</td> 
   <td> <p> Sélectionnez le tableau contenant l’enregistrement pour lequel vous souhaitez récupérer les détails.</p> </td> 
  </tr> 
  <tr> 
   <td>ID de l’enregistrement</td> 
   <td> <p> Saisissez ou mappez l’ID de l’enregistrement pour lequel vous souhaitez récupérer des détails.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Rechercher des enregistrements {#search-records}

Ce module recherche les enregistrements dans un objet d’Airtable correspondant à la requête que vous spécifiez.

Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Connexion </td> 
   <td> <p>Pour des instructions sur la connexion de votre compte Airtable à Workfront Fusion, voir <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Connecter Airtable à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>Base </td> 
   <td> <p>Sélectionnez la base à rechercher pour les enregistrements.</p> </td> 
  </tr> 
  <tr> 
   <td>Tableau </td> 
   <td> <p>Sélectionnez le tableau à rechercher pour les enregistrements.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Formule</p> </td> 
   <td> <p>Formule de filtrage des enregistrements. La formule est évaluée pour chaque enregistrement et si le résultat n’est pas <code>0</code>, <code>false</code>, <code>""</code>, <code>NaN</code>, <code>[]</code> ou <code>#Error!</code>, l’enregistrement est inclus dans la réponse.</p> <p>Si elle est combinée avec <code>view</code>, seuls les enregistrements de cette vue qui correspondent à la formule sont renvoyés.</p> <p>Par exemple, pour inclure uniquement les enregistrements dont le nom n’est pas vide, transmettez ce qui suit :<code> NOT({Name} = '')</code></p> <p>Pour en savoir plus, recherchez des informations sur les références de champs de formule dans la documentation d’assistance Airtable.</p> </td> 
  </tr> 
  <tr> 
   <td>Trier </td> 
   <td> <p>Sélectionnez la direction du tri et le champ selon lequel vous souhaitez trier les résultats.</p> </td> 
  </tr> 
  <tr> 
   <td>Afficher </td> 
   <td> <p>Sélectionnez la vue dans laquelle vous souhaitez rechercher des enregistrements.</p> </td> 
  </tr> 
  <tr> 
   <td>Limite</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Mettre à jour un enregistrement {#update-a-record}

Ce module d’action met à jour un enregistrement particulier.

Vous indiquez l’ID de l’enregistrement et les nouvelles données que vous souhaitez qu’il contienne.

Le module renvoie tous les champs standard associés à l’enregistrement, ainsi que tous les champs et valeurs personnalisés auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Connexion </td> 
   <td> <p>Pour des instructions sur la connexion de votre compte Airtable à Workfront Fusion, voir <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Connecter Airtable à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>Base </td> 
   <td> <p>Sélectionnez la base contenant l’enregistrement que vous souhaitez mettre à jour.</p> </td> 
  </tr> 
  <tr> 
   <td>Tableau </td> 
   <td> <p>Sélectionnez le tableau contenant l’enregistrement que vous souhaitez mettre à jour.</p> </td> 
  </tr> 
  <tr> 
   <td>ID de l’enregistrement </td> 
   <td> <p>Saisissez ou mappez lID Airtable unique de l’enregistrement que vous souhaitez que le module mette à jour. Vous pouvez récupérer l’ID, par exemple, à l’aide du module Rechercher des enregistrements.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Enregistrement</p> </td> 
   <td> <p>Saisissez les valeurs du nouvel enregistrement. Les champs disponibles dépendent du tableau sélectionné.</p> <!--<p>In order to delete the content of the field, use the erase function. </p>  <p>Field types (via airtable.com/api):</p> 
    <ul> 
     <li> <p><strong>Text</strong>: string</p> <p>A single line of text.</p> </li> 
     <li> <p><strong>Long text</strong>: string</p> <p>The string can contain multiple lines of text with "mention tokens." For example:</p><pre>&lt;airtable:mention id="menE1i9oBaGX3DseR"&gt;@Alex&lt;/airtable:mention&gt;</pre> </li> 
     <li><strong>Attachment</strong>: Add the attachment. Airtable will download the file from the provided url and keep its own copy of it. If the File name field is left empty, Airtable will generate the name automatically.</li> 
     <li><strong>Checkbox</strong>: Select one of the options.</li> 
     <li><strong>Multiple select</strong>: Select multiple options in the checklist.</li> 
     <li><strong>Single select</strong>: Select one option from the drop-down menu.</li> 
     <li><strong>Collaborator</strong>: Enter the email that uniquely identifies a user in Airtable who this base is shared with.</li> 
     <li><strong>Date</strong>: UTC date, for example, 2019-09-05. (ISO 8601 formatted date)</li> 
     <li><strong>Phone number</strong>: A telephone number, for example, (415) 555-9876.</li> 
     <li><strong>Email</strong>valid email address.</li> 
     <li><strong>URL</strong>: lid URL such as airtable.com or https://airtable.coiverse.</li> 
     <li><strong>Number</strongnter a number.</li> 
     <li><strong>Currency</stro Currency value.</li> 
     <li><strong>Percent</stronA percentage value; must be equal to or more than 0i> 
     <li><strong>Duration</strong>: Enter the duration time. If you need help, see the information about the duration field type in the Airtable support documentation.</li> 
     <li><strong>Rating</strong>: Enter the number. For example, "3 stars" is 3. A rating cannot be 0.</li> 
     <li><strong>Link</strong>: Enter the linked records IDs from the table. The order of record IDs is reversed compared to what you see in the app.</li> 
     <li><strong>Rollup</strong>: Computed value: COUNT(values)</li> 
     <li><strong>Lookup</strong>: Array of long text fields</li> 
     <li><strong>Autonumber</strong>: Automatically incremented unique counter for each record.</li> 
     <li> <p><strong>Barcode</strong>: The barcode object may contain the following two properties, both of which are optional.</p> <p>Barcode data (text)</p> <p>Barcode symbology, for example, "upce" or "code39" (type)</p> </li> 
    </ul> --></td> 
  </tr> 
  <tr> 
   <td>Liens intelligents</td> 
   <td> <p>Saisissez des noms plutôt que des ID d’enregistrement pour les champs liés à un autre tableau. L’enregistrement est automatiquement créé dans le tableau lié en cas d’absence de correspondance.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Insérer un enregistrement

Ce module d’action met à jour ou insère un enregistrement particulier.

Vous indiquez l’ID de l’enregistrement et les nouvelles données que vous souhaitez qu’il contienne.

Le module renvoie tous les champs standard associés à l’enregistrement, ainsi que tous les champs et valeurs personnalisés auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Connexion </td> 
   <td> <p>Pour des instructions sur la connexion de votre compte Airtable à Workfront Fusion, voir <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Connecter Airtable à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>Base </td> 
   <td> <p>Sélectionnez la base contenant l’enregistrement que vous souhaitez mettre à jour.</p> </td> 
  </tr> 
  <tr> 
   <td>Tableau </td> 
   <td> <p>Sélectionnez le tableau contenant l’enregistrement que vous souhaitez mettre à jour.</p> </td> 
  </tr> 
  <tr> 
   <td>ID de l’enregistrement </td> 
   <td> <p>Si vous mettez à jour un enregistrement, saisissez ou mappez l’ID Airtable unique de l’enregistrement que vous souhaitez que le module mette à jour. Vous pouvez récupérer l’ID, par exemple, à l’aide du module Rechercher des enregistrements.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Enregistrement</p> </td> 
   <td> <p>Saisissez les valeurs du nouvel enregistrement. Les champs disponibles dépendent du tableau sélectionné.</p> <!-- <p>In order to delete the content of the field, use the erase function. </p>  <p>Field types (via airtable.com/api):</p> 
    <ul> 
     <li> <p><strong>Text</strong>: string</p> <p>A single line of text.</p> </li> 
     <li> <p><strong>Long text</strong>: string</p> <p>The string can contain multiple lines of text with "mention tokens." For example:</p><pre>&lt;airtable:mention id="menE1i9oBaGX3DseR"&gt;@Alex&lt;/airtable:mention&gt;</pre> </li> 
     <li><strong>Attachment</strong>: Add the attachment. Airtable will download the file from the provided url and keep its own copy of it. If the File name field is left empty, Airtable will generate the name automatically.</li> 
     <li><strong>Checkbox</strong>: Select one of the options.</li> 
     <li><strong>Multiple select</strong>: Select multiple options in the checklist.</li> 
     <li><strong>Single select</strong>: Select one option from the drop-down menu.</li> 
     <li><strong>Collaborator</strong>: Enter the email that uniquely identifies a user in Airtable who this base is shared with.</li> 
     <li><strong>Date</strong>: UTC date, for example, 2019-09-05. (ISO 8601 formatted date)</li> 
     <li><strong>Phone number</strong>: A telephone number, for example, (415) 555-9876.</li> 
     <li><strong>Email</strong>valid email address.</li> 
     <li><strong>URL</strong>: lid URL such as airtable.com or https://airtable.coiverse.</li> 
     <li><strong>Number</strongnter a number.</li> 
     <li><strong>Currency</stro Currency value.</li> 
     <li><strong>Percent</stronA percentage value; must be equal to or more than 0i> 
     <li><strong>Duration</strong>: Enter the duration time. If you need help, see the information about the duration field type in the Airtable support documentation.</li> 
     <li><strong>Rating</strong>: Enter the number. For example, "3 stars" is 3. A rating cannot be 0.</li> 
     <li><strong>Link</strong>: Enter the linked records IDs from the table. The order of record IDs is reversed compared to what you see in the app.</li> 
     <li><strong>Rollup</strong>: Computed value: COUNT(values)</li> 
     <li><strong>Lookup</strong>: Array of long text fields</li> 
     <li><strong>Autonumber</strong>: Automatically incremented unique counter for each record.</li> 
     <li> <p><strong>Barcode</strong>: The barcode object may contain the following two properties, both of which are optional.</p> <p>Barcode data (text)</p> <p>Barcode symbology, for example, "upce" or "code39" (type)</p> </li> 
    </ul> --></td> 
  </tr> 
  <tr> 
   <td>Liens intelligents</td> 
   <td> <p>Saisissez des noms plutôt que des ID d’enregistrement pour les champs liés à un autre tableau. L’enregistrement est automatiquement créé dans le tableau lié en cas d’absence de correspondance.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Surveillez des enregistrements {#watch-records}

Ce module de déclenchement lance un scénario lorsqu’un enregistrement est créé ou mis à jour dans le tableau spécifié.

>[!NOTE]
>
>Pour utiliser ce module, le champ Heure de création ou Heure de dernière modification doit être créé dans votre tableau.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Connexion </td> 
   <td> <p>Pour des instructions sur la connexion de votre compte Airtable à Workfront Fusion, voir <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Connecter Airtable à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>Base </td> 
   <td> <p>Sélectionnez la base que vous souhaitez surveiller pour de nouveaux enregistrements.</p> </td> 
  </tr> 
  <tr> 
   <td>Tableau </td> 
   <td> <p>Sélectionnez le tableau sur lequel rechercher les nouveaux enregistrements.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Configuration du déclencheur</p> </td> 
   <td> <p>Champ Déclencheur</p> <p>Champ <code>Created Time</code> ou <code>Last Modified Time</code> utilisé pour trier les enregistrements. Si vous n’avez pas de champ <code>Created Time</code> ou <code>Last Modified Time</code> dans votre schéma, vous devez en créer un. </p> <p>Champ Libellé</p> <p>Champ utilisé comme libellé pour un enregistrement, par exemple, dans la boîte de dialogue Choisir où commencer.</p> </td> 
  </tr> 
  <tr> 
   <td>Limite</td> 
   <td> <p>Saisissez ou mappez le nombre maximal d’enregistrements que le module doit surveiller pour chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
  <tr> 
   <td>Afficher</td> 
   <td> <p>Sélectionnez la vue à utiliser.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>Formule</p> </td> 
   <td> <p>Formule de filtrage des enregistrements. La formule est évaluée pour chaque enregistrement et si le résultat n’est pas <code>0</code>, <code>false</code>, <code>""</code>, <code>NaN</code>, <code>[]</code> ou <code>#Error!</code>, l’enregistrement est inclus dans la réponse.</p> <p>Si elle est combinée avec <code>view</code>, seuls les enregistrements de cette vue qui correspondent à la formule sont renvoyés.</p> <p>Par exemple, pour inclure uniquement les enregistrements dont le nom n’est pas vide, transmettez ce qui suit :<code> NOT({Name} = '')</code></p> <p>Pour en savoir plus, consultez les informations sur les références de champ de formule dans la documentation de l’assistance Airtable.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Regarder des réponses

Ce module de déclenchement lance un scénario lorsqu’un formulaire est envoyé.

>[!NOTE]
>
>Cette fonctionnalité est disponible uniquement pour le forfait Airtable Pro payant.

L’URL du webhook doit être générée dans Workfront Fusion, puis ajoutée à la configuration du formulaire dans Airtable.

1. Ajoutez le module Regarder les nouvelles réponses à votre scénario Workfront Fusion.
1. Générez et copiez l’URL du webhook.

   <!--For instructions, see [ (webhooks) in Adobe Workfront Fusion](/help/workfront-fusion/).-->

1. Connectez-vous à votre compte Airtable.
1. Ouvrez la Base et le tableau à utiliser pour le formulaire et créez une vue de formulaire.
1. Définissez le formulaire selon vos besoins, faites défiler le formulaire vers le bas et activez l’option Rediriger vers l’URL après l’envoi du formulaire.
1. Saisissez l’URL du webhook générée à l’étape 2 dans la boîte de dialogue affichée et ajoutez ?record_id={record_id} juste après l’URL du webhook pour inclure l’ID d’enregistrement dans la sortie du module, puis cliquez sur Enregistrer. L’URL qui en résulte, par exemple, se présente comme suit :
1. Revenez à votre scénario Workfront Fusion et exécutez le module Regarder des réponses uniquement pour charger les champs d’Airtable et pour pouvoir mapper ces champs dans les autres modules.
1. Envoyez le formulaire dans Airtable, où l’option Rediriger vers l’URL après l’envoi du formulaire est activée et où l’URL du webhook est ajoutée (étape 6 ci-dessus).

   Le module Regarder des réponses est déclenché et les données souhaitées sont chargées.

1. Ajoutez le module Airtable > Obtenir un enregistrement juste après le module Airtable > Regarder des réponses et mappez le paramètre record_id au champ ID d’enregistrement.

Désormais, chaque fois que le formulaire est envoyé, le module Regarder des réponses dans votre scénario Workfront Fusion est déclenché et le module Obtenir un enregistrement renvoie les détails du formulaire envoyé.

#### Effectuer un appel API

#### Appel API personnalisé

Ce module d’action vous permet d’effectuer un appel authentifié personnalisé vers l’API [!DNL Airtable]. Vous pouvez ainsi créer une automatisation du flux de données que les autres modules [!DNL Airtable] ne peuvent pas réaliser.

L’action est basée sur le type d’entité (type d’objet Allocadia) que vous spécifiez.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>Connexion</p> </td> 
   <td> <p>Pour savoir comment connecter votre compte Airtable à Workfront Fusion, voir la section <a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">Connecter Airtable à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>Saisissez un chemin d’accès relatif à <code>https://api.airtable.com/</code>. Exemple : <code>v0/{base}/{table}</code> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Méthode</td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">En-têtes</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] ajoute les en-têtes d’autorisation pour vous.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Chaîne de requête</td> 
   <td> <p>Ajouter la requête pour l’appel API sous la forme d’une clé et d’une valeur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Corps</td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lors de l’utilisation d’instructions conditionnelles telles que <code>if</code> dans votre fichier JSON, placez les guillemets en dehors de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>
