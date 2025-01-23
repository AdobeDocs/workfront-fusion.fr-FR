---
title: Modules Adobe Acrobat Sign
description: Les modules  [!DNL Adobe Acrobat Sign]  vous permettent de lancer un scénario  [!DNL Adobe Workfront Fusion]  basé sur les événements de votre compte  [!DNL Adobe]  Acrobat Sign, de créer, lire ou mettre à jour des accords et d’autres enregistrements, de rechercher des enregistrements à l’aide des critères que vous avez définis et de charger des documents.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 0ef9d40e-8ad6-434e-8fa0-076920ff29ea
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '5488'
ht-degree: 77%

---

# Modules [!DNL Adobe Acrobat Sign]

Les modules [!DNL Adobe Acrobat Sign] vous permettent de lancer un scénario [!DNL Adobe Workfront Fusion] basé sur les événements de votre compte [!DNL Adobe Acrobat Sign], de créer, lire ou mettre à jour des accords et d’autres enregistrements, de rechercher des enregistrements à l’aide des critères que vous avez définis et de charger des documents.

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

## Informations sur l’API [!DNL Adobe Acrobat Sign]

Le connecteur Adobe Acrobat Sign utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Version de l’API</td> 
   <td> v6 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.35.1</td> 
  </tr>
 </tbody> 
</table>


## Recommandations pour l’utilisation du connecteur [!DNL Adobe Acrobat Sign]

L’application [!DNL Adobe Sign] rend l’automatisation des processus commerciaux d’eSignature dans [!DNL Fusion] beaucoup plus facile et plus puissante.

Les nouveaux utilisateurs et utilisatrices d’[!DNL Adobe Sign] doivent prêter une attention particulière à certaines des contraintes liées à la mise à jour des accords. Les accords ne sont généralement pas modifiés une fois qu’ils ont été conclus. Nous recommandons aux nouveaux utilisateurs et aux nouvelles utilisatrices de [!DNL Adobe Sign] de se concentrer sur la création de nouveaux accords à l’aide du module de création d’accords. Cela facilitera les automatisations de [!DNL Fusion] et fonctionnera mieux avec [!DNL Adobe Sign].

Les accords [!DNL Adobe Sign] ont besoin d’un champ avec lequel travailler. Il existe plusieurs options pour ce faire, mais la plus simple et la plus courante consiste à charger un document transitoire et à le faire correspondre à votre accord.

![](/help/workfront-fusion/references/apps-and-modules/assets/adobe-sign-recommendations-350x168.png)

## Modules et champs [!DNL Adobe Acrobat Sign]

Lorsque vous configurez les modules [!DNL Adobe Acrobat Sign], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Adobe Acrobat Sign] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Déclencheurs](#triggers)
* [Actions](#actions)
* [Recherches](#searches)

### Déclencheurs

<!--
* [Watch for agreements](#watch-for-agreements) 
* [Watch for events](#watch-for-events)
-->

+++ **[!UICONTROL Watch for agreements]**

Ce module déclencheur lance un scénario lorsqu’un accord est créé ou mis à jour.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
<td>Pour savoir comment connecter votre compte [!DNL Adobe Acrobat Sign] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a></td>  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Indiquez si vous souhaitez surveiller les nouveaux enregistrements, les enregistrements mis à jour ou les deux.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type] </td> 
   <td>Sélectionnez le type d’enregistrement que vous souhaitez surveiller.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Find text]</td> 
   <td> <p>Saisissez les termes que vous souhaitez rechercher. Le module renvoie les enregistrements qui contiennent ces termes comme valeurs de champ.</p> <p>Pour plus d’informations sur la recherche de champs dans [!DNL Adobe Acrobat Sign], voir « Fonctionnement de la recherche de texte » dans <a href="https://helpx.adobe.com/fr/sign/using/adobesign-search-users-agreements.html#HowSearchWorks">Recherche Adobe Sign - Fonctionnement</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned agreements]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Watch for events]**

Ce module déclencheur lance un scénario lorsqu’un événement que vous sélectionnez se produit.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td>Sélectionnez le webhook que vous souhaitez utiliser ou cliquez sur <b>[!UICONTROL Add]</b> et renseignez les champs suivants.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name]</td> 
   <td> <p>Saisissez un nom pour le webhook.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Adobe Acrobat Sign] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scopes]</td> 
   <td> 
    <ul> 
     <li> <p>[!UICONTROL Account]</p> </li> 
     <li> <p>[!UICONTROL Group]</p> </li> 
     <li> <p>[!UICONTROL User]</p> </li> 
     <li> <p>[!UICONTROL Resource]</p> <p>Si vous sélectionnez [!UICONTROL Resource], saisissez l’ID de ressource et le type de ressource.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource level]</td> 
   <td> <p>Sélectionnez le type de ressource que vous souhaitez surveiller.</p> 
    <ul> 
     <li> <p>[!UICONTROL Agreements]</p> </li> 
     <li> <p>[!UICONTROL Widgets]</p> </li> 
     <li> <p>[!UICONTROL Megasigns]</p> </li> 
     <li> <p>[!UICONTROL Library Documents]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook subscription events]</td> 
   <td>Sélectionnez les événements [!DNL Adobe Sign] que vous voulez que le module surveille.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application display name]</td> 
   <td>Le nom d’affichage de l’application avec laquelle le webhook est créé.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application name]</td> 
   <td>Le nom d’affichage de l’application avec laquelle le webhook est créé.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Problem notification emails]</td> 
   <td> <p>Ce paramètre ne fonctionne que pour les comptes d’administration.</p> <p>Pour chaque adresse e-mail à laquelle vous souhaitez envoyer des e-mails de notification de problème, cliquez sur <b>[!UICONTROL Add]</b> et saisissez l’adresse e-mail.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Agreement conditional parameters]</td> 
   <td>Si vous souhaitez ajouter des paramètres conditionnels, sélectionnez <b>[!UICONTROL Yes]</b> sur le type d’enregistrement auquel vous souhaitez ajouter des paramètres, puis sélectionnez <b>[!UICONTROL Yes]</b> sur les paramètres que vous souhaitez activer.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Actions

<!--
* [Create a record](#create-a-record) 
* [Create an agreement](#create-an-agreement) 
* [Create related records](#create-related-records) 
* [Custom API Call](#custom-api-call) 
* [List records](#list-records) 
* [Read a record](#read-a-record) 
* [Read related records](#read-related-records) 
* [Update a record](#update-a-record) 
* [Update related record](#update-related-record) 
* [Upload document](#upload-document)
-->

+++ **[!UICONTROL Create a record]**

Ce module d’action crée un enregistrement du type sélectionné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour savoir comment connecter votre compte [!DNL Adobe Acrobat Sign] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td>Ajoutez les en-têtes de la demande sous la forme d’un objet JSON standard. Par exemple : <code>{"Content-type":"application/json"}</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Sélectionnez le type d’enregistrement que vous souhaitez créer.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Group]</b> </p> </li> 
     <li> <p><b>[!UICONTROL Library document]</b> </p> </li> 
     <li> <p><b>[!UICONTROL User]</b> </p> </li> 
     <li> <p><b>[!UICONTROL Web form] ([!UICONTROL Widget])</b> </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group info]</td> 
   <td> <p>Saisissez ou mappez les [!UICONTROL Name] et les [!UICONTROL ID] du groupe et indiquez si ce groupe est le groupe par défaut pour le compte.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Library document info]</td> 
   <td> <p>Remplissez les champs suivants :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Files to send]</b> </p> <p>Pour chaque fichier à ajouter, cliquez sur <b>[!UICONTROL Add item]</b> et renseignez les champs.</p> 
      <ul> 
       <li><b>[!UICONTROL Transient document ID]</b> <p>Saisir l’identifiant du document transitoire</p> </li> 
       <li> <p><b>[!UICONTROL URL file transfer]</b> </p> <p>Remplissez les champs suivants :</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Mime-Type]</b> </p> <p>Saisissez le type MIME du fichier d’origine. Les types MIME (Multipurpose Internet Mail Extension) sont des libellés qui permettent aux logiciels d’identifier les différents types des données partagées sur Internet. Les serveurs web et les navigateurs utilisent le type MIME pour déterminer ce qu’il convient de faire avec un fichier. Par exemple, un fichier dont le type MIME est <code>text/html</code> sera traité différemment dans un navigateur qu’un fichier dont le type MIME est <code>image/jpeg</code>.</p> </li> 
         <li> <p><b>[!UICONTROL Name]</b> </p> <p>Saisissez un nom pour le fichier.</p> </li> 
         <li> <p><b>[!UICONTROL URL]</b> </p> <p>Saisissez l’URL du fichier que vous souhaitez envoyer.</p> </li> 
        </ul> </li> 
       <li> <p><b>[!UICONTROL Notarize]</b> </p> <p>Indiquez si ce document doit être notarié.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Library template name]</b> </p> <p>Saisir ou mapper le nom du modèle de bibliothèque</p> </li> 
     <li> <p><b>[!UICONTROL Sharing mode]</b> </p> <p>Indiquez qui doit avoir accès au document de bibliothèque.</p> </li> 
     <li> <p><b>[!UICONTROL Library document state]</b> </p> <p>Indiquez si le document est en cours de création ou s’il est actif.</p> </li> 
     <li> <p><b>[!UICONTROL Library template type]</b> </p> <p>Pour chaque type de modèle de bibliothèque que vous souhaitez utiliser, cliquez sur <b>[!UICONTROL Add item]</b> et sélectionnez le type de modèle.</p> </li> 
     <li> <p><b>[!UICONTROL Last event date]</b> </p> <p>Saisissez la dernière date à laquelle un événement s’est produit sur le document de bibliothèque.</p> <p>Pour une liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coercition de type dans [!DNL Adobe Workfront Fusion]</a>.</p> </li> 
     <li> <p><b>[!UICONTROL Library document status]</b> </p> <p>Sélectionnez le statut du document de bibliothèque.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User info]</td> 
   <td> <p>Remplissez les champs suivants :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Email]</b> </p> <p>Saisissez l’adresse e-mail de l’utilisateur ou de l’utilisatrice.</p> </li> 
     <li> <p><b>[!UICONTROL Is account admin]</b> </p> <p>Cochez cette option si l’utilisateur créé ou l’utilisatrice créée est administrateur ou administratrice de compte.</p> </li> 
     <li> <p><b>[!UICONTROL User ID]</b> </p> <p>Saisissez l’identifiant unique de la personne.</p> </li> 
     <li> <p><b>[!UICONTROL Account ID]</b> </p> <p>Saisissez l’identifiant unique du compte [!DNL Adobe Acrobat Sign] associé à cette personne.</p> </li> 
     <li> <p><b>[!UICONTROL First name]</b> </p> <p>Saisissez le prénom de la personne.</p> </li> 
     <li> <p><b>[!UICONTROL Last name]</b> </p> <p>Saisissez le nom de famille de la personne.</p> </li> 
     <li> <p><b>[!UICONTROL Company]</b> </p> <p>Saisissez le nom de l’entreprise de la personne.</p> </li> 
     <li> <p><b>[!UICONTROL Initials]</b> </p> <p>Saisissez les initiales de la personne.</p> </li> 
     <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Saisissez les paramètres régionaux de la personne. Cela détermine la langue de l’interface utilisateur. </p> </li> 
     <li> <p><b>[!UICONTROL Phone]</b> </p> <p>Saisissez le numéro de téléphone de la personne.</p> </li> 
     <li> <p><b>Identifiant du groupe principal</b> </p> <p>Saisissez le groupe auquel la nouvelle personne est ajoutée. Si rien n’est saisi, la personne sera ajoutée au groupe par défaut du compte.</p> </li> 
     <li> <p><b>[!UICONTROL Job title]</b> </p> <p>Saisissez l’intitulé du poste de la personne.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Web form info]</td> 
   <td> <p>Remplissez les champs suivants.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL File info]</b> </p> <p>Pour chaque fichier que vous souhaitez ajouter au formulaire web, cliquez sur Ajouter et remplissez les champs suivants :</p> 
      <ul> 
       <li> <p>[!UICONTROL File type]</p> <p>[!UICONTROL Document]</p> </li> 
       <li> <p>[!UICONTROL Transient document]</p> </li> 
       <li> <p>[!UICONTROL URL file info]</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Web form name]</b> </p> <p>Saisissez un nom pour le formulaire web. Ce nom est utilisé pour identifier le formulaire web dans des endroits tels que les e-mails et les sites web.</p> </li> 
     <li> <p><b>[!UICONTROL Web form state]</b> </p> <p>Sélectionnez le statut dans lequel le nouveau formulaire web doit être créé.</p> </li> 
     <li> <p><b>[!UICONTROL Web form participant set info]</b> </p> 
      <ul> 
       <li> <p><b>[!UICONTROL Member info]</b> </p> <p>Pour chaque membre que vous souhaitez ajouter au jeu de participants, cliquez sur <b>[!UICONTROL Add item]</b>. </p> 
        <ul> 
         <li> <p><b>[!UICONTROL Email]</b> </p> <p>Laissez cette option vide.</p> </li> 
         <li> <p><b>[!UICONTROL Security option]</b> </p> <p>Si vous souhaitez ajouter une option de sécurité pour authentifier cet utilisateur, sélectionnez <b>[!UICONTROL Yes]</b>, puis sélectionnez l’option de sécurité et renseignez les champs de votre choix.</p> </li> 
        </ul> </li> 
       <li> <p><b>[!UICONTROL Role]</b> </p> <p>Sélectionnez le rôle. Les personnes membres de cet ensemble de participantes et participants partagent le rôle.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Web form additional participant sets info]</b> </p> 
      <ul> 
       <li> <p><b>[!UICONTROL Member info]</b> </p> <p>Pour chaque membre que vous souhaitez ajouter au jeu de participants, cliquez sur <b>[!UICONTROL Add item]</b>.</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Email]</b> </p> <p>Laissez cette option vide.</p> </li> 
         <li> <p><b>[!UICONTROL Security option]</b> </p> <p>Si vous souhaitez ajouter une option de sécurité pour authentifier cet utilisateur, sélectionnez <b>[!UICONTROL Yes]</b>, puis sélectionnez l’option de sécurité et renseignez les champs de votre choix.</p> </li> 
        </ul> </li> 
       <li> <p><b>[!UICONTROL Role]</b> </p> </li> 
       <li> <p><b>[!UICONTROL Web form participant ID] </b> </p> <p>Saisissez l’identifiant du participant ou de la participante au formulaire web.</p> </li> 
       <li> <p><b>[!UICONTROL Order]</b> </p> <p>Indiquez l’ordre dans lequel cet ensemble de participantes et participants doit interagir avec le formulaire web. Par exemple, le groupe de participantes et participants dont la valeur d’ordre est 1 doit passer en premier, 2 doit passer ensuite, et ainsi de suite. Les numéros d’ordre doivent commencer par 1 et ne pas comporter de trous dans la série. </p> </li> 
       <li> <p><b>[!UICONTROL Provider participant set info]</b> </p> <p>Si la personne participante est inconnue, indiquez si le fournisseur doit fournir des informations sur la personne participante et saisissez un message contenant les informations requises pour la personne participante inconnue.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Authentication failure info]</b> </p> <p>Si vous souhaitez fournir une page d’erreur ou d’échec à vos utilisateurs, sélectionnez <b>[!UICONTROL Yes]</b>, puis renseignez les champs suivants :</p> 
      <ul> 
       <li> <p><b>[!UICONTROL URL]</b> </p> <p>Saisissez l’URL de la page d’erreur.</p> </li> 
       <li> <p><b>[!UICONTROL Deframe]</b> </p> <p>Activez cette option si vous souhaitez que la page d’erreur apparaisse dans le formulaire web.</p> </li> 
       <li> <p><b>[!UICONTROL Delay]</b> </p> <p>Saisissez le délai, en secondes, avant que la personne ne soit redirigée vers la page d’erreur.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL CC info]</b> </p> <p>Pour chaque adresse e-mail à laquelle vous souhaitez envoyer un e-mail lors de la signature de l’accord final sur le formulaire web, cliquez sur <b>[!UICONTROL Add item]</b> et saisissez l’adresse e-mail.</p> </li> 
     <li> <p><b>[!UICONTROL Completion info]</b> </p> <p style="font-style: normal;">Si vous souhaitez fournir une page de succès à vos utilisateurs, sélectionnez <b>[!UICONTROL Yes]</b>, puis renseignez les champs suivants :</p> 
      <ul> 
       <li> <p><b>[!UICONTROL URL]</b> </p> <p>Saisissez l’URL de la page de succès.</p> </li> 
       <li> <p><b>[!UICONTROL Deframe]</b> </p> <p>Activez cette option si vous souhaitez que la page de succès apparaisse à l’intérieur du formulaire web.</p> </li> 
       <li> <p><b>[!UICONTROL Delay]</b> </p> <p>Saisissez le délai, en secondes, avant que la personne ne soit redirigée vers la page de succès.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Group ID]</b> </p> <p>Saisissez l’identifiant du groupe auquel le formulaire web appartient. Si rien n’est saisi, le formulaire web appartient au groupe principal de l’utilisateur ou de l’utilisatrice du compte.</p> </li> 
     <li> <p><b>[!UICONTROL Last event date]</b> </p> <p>Saisissez la date du dernier événement survenu sur le formulaire web. Utilisez le format <code>yyyy-MM-dd'T'HH:mm:ssZ</code>.</p> </li> 
     <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Saisissez les paramètres régionaux de la personne. Cela détermine la langue de l’interface utilisateur. </p> </li> 
     <li> <p><b>[!UICONTROL Security optio]n</b> </p> <p>Saisissez le mot de passe utilisé pour sécuriser le document. Vous devez communiquer séparément ce mot de passe à toutes les parties concernées.</p> </li> 
     <li> <p><b>[!UICONTROL Vaulting info]</b> </p> <p>Si votre compte est configuré pour l’archivage des documents et l’option d’activation par accord, vous pouvez activer cette option pour l’archivage de cet accord.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create an agreement]**

Ce module d’action crée un accord, l’envoie pour signature et renvoie l’identifiant de l’accord.

>[!NOTE]
>
>Nous vous recommandons de charger le document à signer en tant que document transitoire, puis de le mapper au champ [!UICONTROL File to send] dans le module de [!UICONTROL Create an agreement]. Pour un exemple, voir « Charger un document » dans cet article.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
<td>Pour savoir comment connecter votre compte [!DNL Adobe Acrobat Sign] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a></td>  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td>Ajoutez les en-têtes de la demande sous la forme d’un objet JSON standard. Par exemple : <code>{"Content-type":"application/json"}</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Files to send]</td> 
   <td> <p>Pour chaque élément que vous souhaitez inclure dans le contrat, cliquez sur <b>[!UICONTROL Add Item]</b> et renseignez les champs suivants :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL File Type]</b> </p> 
      <ul> 
       <li> <p><b>[!UICONTROL Document]</b> </p> <p>Remplissez les champs suivants :</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Created date]</b> </p> <p>Saisissez ou mappez la date de création du document au format <code>yyyy-MM-dd'T'HH:mm:ssZ</code>. Par exemple, <code>2016-02-25T18:46:19Z</code> représente l’heure UTC.</p> </li> 
         <li> <p><b>[!UICONTROL ID]</b> </p> <p>Saisissez ou mappez l’identifiant du document.</p> </li> 
         <li> <p><b>[!UICONTROL Label]</b> </p> <p>Saisissez ou mappez un libellé unique pour le fichier. Dans le cas d’un workflow personnalisé, le fichier sera mappé à l’élément de fichier correspondant dans la définition du workflow. Ceci doit être spécifié dans le cas d’une demande de création d’un accord dans un workflow personnalisé.</p> </li> 
         <li> <p><b>[!UICONTROL Number of pages]</b> </p> <p>Saisissez ou mappez le nombre de pages du document.</p> </li> 
         <li> <p><b>[!UICONTROL Mime-Type]</b> </p> <p>Saisissez ou mappez le type MIME du fichier d’origine. Les types MIME (Multipurpose Internet Mail Extension) sont des libellés qui permettent aux logiciels d’identifier les différents types des données partagées sur Internet. Les serveurs web et les navigateurs utilisent le type MIME pour déterminer ce qu’il convient de faire avec un fichier. Par exemple, un fichier dont le type MIME est <code>text/html</code> sera traité différemment dans un navigateur qu’un fichier dont le type MIME est <code>image/jpeg</code>.</p> </li> 
         <li> <p><b>[!UICONTROL Name]</b> </p> <p>Saisissez ou mappez un nom pour le document.<br></p> </li> 
        </ul> </li> 
       <li> <p><b>[!UICONTROL Library document ID]</b> </p> <p>Saisissez l’identifiant du document de bibliothèque.</p> </li> 
       <li> <p><b>[!UICONTROL Transient document ID]</b> </p> <p>Saisir l’identifiant du document transitoire</p> </li> 
       <li> <p><b>[!UICONTROL URL file transfer]</b> </p> <p>Remplissez les champs suivants :</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Mime-Type]</b> </p> <p>Saisissez le type MIME du fichier d’origine. Les types MIME (Multipurpose Internet Mail Extension) sont des libellés qui permettent aux logiciels d’identifier les différents types des données partagées sur Internet. Les serveurs web et les navigateurs utilisent le type MIME pour déterminer ce qu’il convient de faire avec un fichier. Par exemple, un fichier dont le type MIME est <code>text/html</code> sera traité différemment dans un navigateur qu’un fichier dont le type MIME est <code>image/jpeg</code>.</p> </li> 
         <li> <p><b>[!UICONTROL Name]</b> </p> <p>Saisissez un nom pour le fichier.</p> </li> 
         <li> <p><b>[!UICONTROL URL]</b> </p> <p>Saisissez l’URL du fichier que vous souhaitez envoyer.</p> </li> 
        </ul> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Label]</b> </p> <p>Saisissez un libellé pour le fichier.</p> </li> 
     <li> <p><b>[!UICONTROL Notarize]</b> </p> <p>Activez cette option pour indiquer que le fichier doit être notarié.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Agreement name]</td> 
   <td>Saisissez un nom pour le nouvel accord. Ce nom est utilisé pour identifier l’accord dans des emplacements tels que des e-mails et des sites web.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Participant sets info]</td> 
   <td> <p>Pour chaque jeu de participants à ajouter, cliquez sur <b>[!UICONTROL Add item]</b> et renseignez les champs suivants.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Members]</b> </p> <p>Pour chaque personne que vous souhaitez ajouter au jeu de participants, cliquez sur <b>[!UICONTROL Add item]</b> et saisissez son adresse e-mail.</p> </li> 
     <li> <p><b>[!UICONTROL Order]</b> </p> <p>Précisez l’ordre dans lequel cet ensemble de participantes et participants doit signer l’accord. Par exemple, le groupe de participantes et participants dont la valeur d’ordre est 1 doit signer en premier, 2 doit signer ensuite, et ainsi de suite. Les numéros d’ordre doivent commencer par 1 et ne pas comporter de trous dans la série. </p> </li> 
     <li> <p><b>[!UICONTROL Role]</b> </p> <p>Sélectionnez un rôle pour cet ensemble de participantes et participants. Tous les participantes et participants de l’ensemble reçoivent ce rôle.</p> </li> 
     <li> <p><b>[!UICONTROL ID]</b> </p> <p>Saisissez ou mappez l’identifiant de cet ensemble de participantes et participants.</p> </li> 
     <li> <p><b>[!UICONTROL Label]</b> </p> <p>Saisissez ou mappez un libellé unique pour l’ensemble de participantes et participants. Pour les workflows personnalisés, le libellé spécifié dans l’ensemble de participation doit être mappé à l’étape de participation dans le workflow.</p> </li> 
     <li> <p><b>[!UICONTROL Name]</b> </p> <p>Saisissez un nom pour l’ensemble de participantes et participants. Ce nom doit être unique dans l’accord.</p> </li> 
     <li> <p><b>[!UICONTROL Private message]</b> </p> <p>Saisissez ou mappez un message pour cet ensemble de participantes et participants. Tous les participantes et participants de l’ensemble reçoivent ce message.</p> </li> 
     <li> <p><b>[!UICONTROL Visible pages]</b> </p> <p>Si la visibilité limitée des documents est activée pour cet accord, spécifiez quels fichiers sont visibles pour cet ensemble de participantes et participants. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Signature type]</td> 
   <td> <p>Sélectionnez le type de signature requis pour l’accord.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL E-sign]</b> </p> <p>L’accord doit être signé électroniquement.</p> </li> 
     <li> <p><b>[!UICONTROL Written]</b> </p> <p>L’accord doit être signé à la main et l’accord signé doit être scanné et chargé.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td> <p>Sélectionnez un état pour cet accord.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Authoring]</b> </p> <p>Vous pouvez toujours modifier ou ajouter des champs à cet accord.</p> </li> 
     <li> <p><b>[!UICONTROL Draft]</b> </p> <p>Vous pouvez concevoir au fur et à mesure cet accord avant de l’envoyer.</p> </li> 
     <li> <p><b>[!UICONTROL In Process]</b> </p> <p>Cet accord sera envoyé immédiatement.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL CCs]</td> 
   <td> <p>Vous pouvez envoyer cet accord aux parties intéressées qui n’ont pas besoin de le signer, telles que les parties prenantes. Celles-ci reçoivent un e-mail au début du processus de signature et un autre lorsque la signature finale est reçue. Elles reçoivent également une copie PDF de l’accord. </p> <p>Pour chaque personne que vous souhaitez mettre en copie conforme dans ce contrat, cliquez sur <b>[!UICONTROL Add item]</b> et renseignez les champs suivants :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Email]</b> </p> <p>Saisissez ou mappez l’adresse e-mail que vous souhaitez ajouter en copie à l’accord.</p> </li> 
     <li> <p><b>[!UICONTROL Label]</b> </p> <p>Saisissez ou mappez un libellé pour cette adresse e-mail, tel qu’indiqué dans la description du workflow.</p> </li> 
     <li> <p><b>[!UICONTROL Visible pages]</b> </p> </li> 
     <li> <p>Si la visibilité limitée des documents est activée pour cet accord, spécifiez quels fichiers sont visibles pour cet ensemble de participantes et participants. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email option]</td> 
   <td> <p>Pour chaque type d’e-mail, sélectionnez si ce type d’e-mail est envoyé à toutes les personnes participants ou à aucune d’entre elles.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Completion emails]</b> </p> <p>Envoyez un e-mail lorsque cet accord est complété, annulé, expiré ou refusé.</p> </li> 
     <li> <p><b>[!UICONTROL In-Flight emails]</b> </p> <p>Envoyez un e-mail lorsque cet accord est délégué ou remplacé.</p> </li> 
     <li> <p><b>[!UICONTROL Agreement initiation emails]</b> </p> <p>Envoyez un e-mail lorsque cet accord est créé ou lorsqu’une action est requise sur celui-ci.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL External ID]</td> 
   <td> <p>Saisissez ou mappez un identifiant pour cet accord. Vous pouvez le spécifier lors de la création de l’accord et l’utiliser pour localiser l’accord dans des modules ou des requêtes ultérieurs.</p> <p>Remarque : la valeur de l’identifiant externe est visible par tous les participantes et participants via l’API, elle ne doit donc pas être utilisée pour contenir un jeton sensible.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Merge field info]</td> 
   <td> <p>Pour chaque champ du contrat pour lequel vous souhaitez définir une valeur par défaut, cliquez sur <b>[!UICONTROL Add item]</b> et saisissez la valeur par défaut et le nom du champ.</p> <p>Les valeurs seront présentées aux personnes signataires pour les champs modifiables. Pour les champs en lecture seule, les valeurs fournies ne seront pas modifiables pendant le processus de signature.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Notary info]</td> 
   <td> <p>Remplissez les champs suivants :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Appointment]</b> </p> <p>Saisissez ou mappez une proposition de date et d’heure pour le rendez-vous consacré à la notarisation de cet accord.</p> </li> 
     <li> <p><b>[!UICONTROL Note]</b> </p> <p>Saisissez ou mappez les notes que vous souhaitez inclure à propos de la session de notarisation.</p> </li> 
     <li> <p><b>[!UICONTROL Payment]</b> </p> <p>Choisissez si la personne chargée de la notarisation est payée par la personne signataire ou la personne expéditrice de l’accord.</p> </li> 
     <li> <p><b>[!UICONTROL Notary Type]</b> </p> <p>Sélectionnez le type de notaire.</p> 
      <ul> 
       <li> <p>[!UICONTROL Provider notary]</p> <p>La personne chargée de la notarisation est fournie par le fournisseur de services notariaux.</p> </li> 
       <li> <p>[!UICONTROL BYON notary]</p> <p>La personne chargée de la notarisation est fournie par le client ou la cliente.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Post sign option]</td> 
   <td> <p>Indiquez si vous souhaitez que les personnes signataires soient dirigées vers une page qui confirme la réussite après la signature de l’accord. Si vous sélectionnez <b>[!UICONTROL Yes]</b>, renseignez les champs suivants :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Redirect delay]</b> </p> <p>Saisissez ou mappez un nombre qui représente le nombre de secondes avant que la personne signataire ne soit redirigée vers la page de confirmation de réussite. Si cette valeur est supérieure à 0, la personne voit d’abord le message de confirmation de réussite standard d’[!DNL Adobe Sign], puis, après un moment, est redirigée vers votre page de confirmation de réussite.</p> </li> 
     <li> <p><b>[!UICONTROL Redirect URL]</b> </p> <p>Saisissez ou mappez une URL accessible publiquement vers laquelle la personne sera dirigée après avoir terminé avec succès le processus de signature.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Security option]</td> 
   <td> <p>Saisissez ou mappez le mot de passe secondaire utilisé pour sécuriser le document PDF. </p> <p>Important : [!DNL Adobe Sign] ne partage jamais ce mot de passe, vous devez donc le communiquer séparément à toutes les parties concernées.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Vaulting info]</td> 
   <td>Si votre compte est configuré pour l’archivage des documents et l’option d’activation par accord, vous pouvez activer cette option pour l’archivage de cet accord.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create related records]**

Ce module d’action crée des enregistrements liés à un module de votre choix.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Adobe Acrobat Sign] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Ajoute automatiquement des en-têtes d’autorisation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Sélectionnez le type d’enregistrement de l’enregistrement d’origine auquel vous souhaitez associer les enregistrements créés.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Agreement]/[!UICONTROL Library document]/[!UICONTROL User]/[!UICONTROL Widget ID]</td> 
   <td>Saisissez ou mappez l’identifiant de l’objet auquel vous souhaitez associer l’enregistrement créé.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Agreement related field]</td> 
   <td> <p>Sélectionnez le type de champ connexe que vous souhaitez créer.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Form fields]</b> </p> <p>Saisissez l’identifiant du modèle qui contient les champs que vous souhaitez créer.</p> </li> 
     <li> <p><b>[!UICONTROL Reminders]</b> </p> <p>Remplissez les champs suivants :</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Recipient participant ID]</b> </p> <p>Pour chaque participant pour lequel vous souhaitez recevoir un rappel, cliquez sur [!UICONTROL Add item], puis saisissez son identifiant.</p> </li> 
       <li> <p><b>[!UICONTROL Status]</b> </p> <p>Pour les nouveaux enregistrements, le statut doit être [!UICONTROL Active].</p> </li> 
       <li> <p><b>[!UICONTROL First reminder delay]</b> </p> <p>Saisissez le délai en heures avant l’envoi du premier rappel. La valeur minimale autorisée est d’1 heure et la valeur maximale ne peut pas être supérieure à la différence entre l’heure de création de l’accord et l’heure d’expiration de l’accord en heures. Si ce délai n’est pas défini, le premier rappel sera basé sur la fréquence.</p> </li> 
       <li> <p><b>[!UICONTROL Reminder frequency]</b> </p> <p>Définissez la fréquence à laquelle vous souhaitez envoyer le rappel. Si la fréquence n’est pas indiquée, le rappel ne sera envoyé qu’une seule fois.</p> </li> 
       <li> <p><b>[!UICONTROL Last sent date]</b> </p> <p>Ce champ est automatiquement défini par le système.</p> </li> 
       <li> <p><b>[!UICONTROL Next sent date]</b> </p> <p>Ce champ doit être vide ou [!UICONTROL ONCE].</p> </li> 
       <li> <p><b>[!UICONTROL Note]</b> </p> <p>Saisissez une note à joindre au rappel. Cela permet d’expliquer à la personne pourquoi sa participation est requise.</p> </li> 
       <li> <p><b>[!UICONTROL Start reminder counter from]</b> </p> <p>Indiquez si le rappel est envoyé en fonction de la date de création de l’accord ou de sa disponibilité.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Signer identity report]</b> </p> <p>Saisissez le mot de passe utilisé pour sécuriser le document PDF.</p> </li> 
     <li> <p><b>[!UICONTROL Views]</b> </p> <p>Saisissez les champs suivants.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Name]</b> </p> <p>Sélectionnez le nom de la vue que vous souhaitez créer.</p> </li> 
       <li> <p><b>[!UICONTROL Auto login user]</b> </p> <p>Sélectionnez <b>[!UICONTROL Yes]</b> pour connecter automatiquement l’utilisateur à l’URL renvoyée.</p> </li> 
       <li> <p><b>[!UICONTROL Frame Parent]</b> </p> <p>Entrez ou mappez une liste d’URL de domaines parent séparée par des virgules, les URL renvoyés pouvant être encadrés par la balise iframe. Si ce champ est laissée vide, les pages [!DNL Adobe Acrobat Sign] ne sont pas visibles dans l’iframe.</p> </li> 
       <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Saisissez la langue dans laquelle vous souhaitez créer la vue. </p> </li> 
       <li> <p><b>[!UICONTROL No chrome flag]</b> </p> <p>Sélectionnez <b>[!UICONTROL Yes]</b> pour afficher la page incorporée sans en-tête ni pied de page de navigation.</p> </li> 
       <li> <p><b>[!UICONTROL Can edit files]</b> </p> <p>Sélectionnez <b>[!UICONTROL Yes]</b> si vous souhaitez que la section Chargement de fichier soit modifiée en ajoutant ou en supprimant des fichiers. Il ne s’agit pas d’un mécanisme de contrôle d’accès. La valeur par défaut est [!UICONTROL Yes].</p> </li> 
       <li> <p><b>[!UICONTROL Library document]</b> </p> <p>Sélectionnez <b>[!UICONTROL Yes]</b> si vous souhaitez que les liens des documents de bibliothèque soient visibles. La valeur par défaut est [!UICONTROL Yes].</p> </li> 
       <li> <p><b>[!UICONTROL Local file]</b> </p> <p>Sélectionnez <b>[!UICONTROL Yes]</b> si vous souhaitez que le bouton de chargement de fichier local apparaisse. La valeur par défaut est [!UICONTROL Yes].</p> </li> 
       <li> <p><b>[!UICONTROL Web connectors]</b> </p> <p>Sélectionnez <b>[!UICONTROL Yes]</b> si vous souhaitez que les liens joignent des documents provenant de sources web. La valeur par défaut est Oui.</p> </li> 
       <li> <p><b>[!UICONTROL Is preview selected]</b> </p> <p>Sélectionnez <b>[!UICONTROL Yes]</b> pour définir la page Composer sur le mode Création.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Member share]</b> </p> <p>Pour chaque membre avec lequel vous souhaitez partager le contrat, cliquez sur <b>[!UICONTROL Add item]</b> et saisissez l’adresse e-mail du membre, ainsi qu’un message destiné à ce membre.</p> </li> 
     <li> <p>[!UICONTROL Delegate participant set]</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Participant set ID]</b> </p> <p>Saisir l’ID de l’ensemble de participantes et participants</p> </li> 
       <li> <p><b>[!UICONTROL Member info]</b> </p> <p>Pour chaque membre que vous souhaitez ajouter, cliquez sur [!UICONTROL Add item] et saisissez l’adresse e-mail et les informations téléphoniques du membre.</p> </li> 
       <li> <p><b>[!UICONTROL Private message]</b> </p> <p>Saisissez un message. Toutes les personnes membres de l’ensemble de participantes et participants reçoivent ce message.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Library view info]</td> 
   <td> <p>Remplissez les champs suivants :</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Name]</b> </p> <p>Saisissez un nom pour le modèle de bibliothèque. Ce nom est utilisé dans les e-mails et sur les sites web.</p> </li> 
     <li> <p><b>[!UICONTROL Auto login user]</b> </p> <p>Sélectionnez <b>[!UICONTROL Yes]</b> pour connecter automatiquement l’utilisateur à l’URL renvoyée.</p> </li> 
     <li> <p><b>[!UICONTROL Frame parent]</b> </p> <p>Entrez ou mappez une liste d’URL de domaines parent séparée par des virgules, les URL renvoyés pouvant être encadrés par la balise iframe. Si ce champ est laissée vide, les pages [!DNL Adobe Acrobat Sign] ne sont pas visibles dans l’iframe.</p> </li> 
     <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Saisissez la langue dans laquelle vous souhaitez créer la vue. </p> </li> 
     <li> <p><b>[!UICONTROL No chrome flag]</b> </p> <p>Sélectionnez <b>[!UICONTROL Yes]</b> pour afficher la page incorporée sans en-tête ni pied de page de navigation.</p> </li> 
     <li> <p><b>[!UICONTROL Send view configuration]</b> </p> <p>Sélectionnez <b>[!UICONTROL Yes]</b> si vous souhaitez configurer la vue [!UICONTROL Send], puis renseignez les champs suivants.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Agreement name]</b> </p> <p>Saisissez ou mappez le nom de l’accord pour le document de bibliothèque sur la page de composition.</p> </li> 
       <li> <p><b>[!UICONTROL Can edit files]</b> </p> <p>Sélectionnez <b>[!UICONTROL Yes]</b> si vous souhaitez que la section Chargement de fichier soit modifiée en ajoutant ou en supprimant des fichiers. Il ne s’agit pas d’un mécanisme de contrôle d’accès. La valeur par défaut est [!UICONTROL Yes].</p> </li> 
       <li> <p><b>[!UICONTROL Local file]</b> </p> <p>Sélectionnez <b>[!UICONTROL Yes]</b> si vous souhaitez que les liens des documents de bibliothèque soient visibles. La valeur par défaut est [!UICONTROL Yes].</p> </li> 
       <li> <p><b>[!UICONTROL Web connectors]</b> </p> <p>Sélectionnez <b>[!UICONTROL Yes]</b> si vous souhaitez que les liens joignent des documents provenant de sources web. La valeur par défaut est [!UICONTROL Yes].</p> </li> 
       <li> <p><b>L’aperçu est-il sélectionné ?</b> </p> <p>Sélectionnez <b>[!UICONTROL Yes]</b> pour définir la page Composer sur le mode Création.</p> </li> 
      </ul> <p> </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User view info]</td> 
   <td> <p>Remplissez les champs suivants.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Name]</b> </p> <p>Sélectionnez le nom de la vue utilisateur demandée.</p> </li> 
     <li> <p><b>[!UICONTROL Auto login user]</b> </p> <p>Sélectionnez <b>[!UICONTROL Yes]</b> pour connecter automatiquement l’utilisateur. Sélectionnez <b>[!UICONTROL No]</b> pour exiger des informations d’identification. La valeur par défaut est [!UICONTROL No].</p> </li> 
     <li> <p><b>[!UICONTROL Frame parent]</b> </p> <p>Entrez ou mappez une liste d’URL de domaines parent séparée par des virgules, les URL renvoyés pouvant être encadrés par la balise iframe. Si elle reste vide, les pages d’[!DNL Adobe Acrobat Sign] ne sont pas visibles dans l’iframe.</p> </li> 
     <li> <p><b>Pas d’indicateur Chrome</b> </p> <p>Sélectionnez <b>[!UICONTROL Yes]</b> pour afficher la page incorporée sans en-tête ni pied de page de navigation.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Widget related fields]</td> 
   <td> <p>Sélectionnez l’enregistrement lié que vous souhaitez créer.</p> 
    <ul> 
     <li> <p>[!UICONTROL Views]</p> <p>Remplissez les champs suivants.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Name]</b> </p> <p>Sélectionnez le nom de la vue du formulaire web demandée.</p> </li> 
       <li> <p><b>[!UICONTROL Auto login user]</b> </p> <p>Sélectionnez <b>[!UICONTROL Yes]</b> pour connecter automatiquement l’utilisateur. Sélectionnez <b>[!UICONTROL No]</b> pour exiger des informations d’identification. La valeur par défaut est [!UICONTROL No].</p> </li> 
       <li> <p><b>[!UICONTROL Frame parent]</b> </p> <p>Entrez ou mappez une liste d’URL de domaines parent séparée par des virgules, les URL renvoyés pouvant être encadrés par la balise iframe. Si ce champ est laissée vide, les pages [!DNL Adobe Acrobat Sign] ne sont pas visibles dans l’iframe.</p> </li> 
       <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Saisissez la langue dans laquelle vous souhaitez créer la vue. </p> </li> 
       <li> <p><b>[!UICONTROL No chrome flag]</b> </p> <p>Sélectionnez <b>[!UICONTROL Yes]</b> pour afficher la page incorporée sans en-tête ni pied de page de navigation.</p> </li> 
       <li> <p>[!UICONTROL Personalized signing view configuration]</p> <p>Si vous souhaitez configurer une vue de signature personnalisée, sélectionnez <b>[!UICONTROL Yes]</b> et renseignez les champs suivants :</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Email]</b> </p> <p>Saisissez l’adresse e-mail de la personne qui recevra le formulaire web nouvellement créé.</p> </li> 
         <li> <p><b>[!UICONTROL Comment]</b> </p> <p>Entrez un commentaire décrivant la façon dont l’entité appelant l’API a établi l’identité de la personne signataire. Cette information apparaît dans le journal d’audit d’[!DNL Adobe Acrobat Sign].</p> </li> 
         <li> <p><b>[!UICONTROL Expiration]</b> </p> <p>Entrez une date d’expiration pour la personnalisation de ce formulaire web. </p> <p>Pour consulter une liste des formats de date et d’heure pris en charge, voir la section <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Coercition de type dans [!DNL Adobe Workfront Fusion]</a>.</p> </li> 
         <li> <p><b>[!UICONTROL Reusable]</b> </p> <p>Sélectionnez <b>[!UICONTROL Yes]</b> si vous souhaitez que le signataire prévu puisse signer le formulaire plusieurs fois.</p> </li> 
        </ul> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Member share]</b> </p> <p>Pour chaque membre avec lequel vous souhaitez partager le contrat, cliquez sur <b>[!UICONTROL Add item]</b> et saisissez l’adresse e-mail du membre, ainsi qu’un message destiné à ce membre.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Custom API Call]**
Ce module vous permet d’effectuer un appel API personnalisé.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Adobe Acrobat Sign] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Saisir un chemin relatif à <code>https://api.[region].adobesign.com/api/rest/v6/</code></p> <p>Remarque : pour obtenir la liste des points d’entrée disponibles, reportez-vous à la référence de l’API [!DNL Adobe Sign].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Ajoute automatiquement des en-têtes d’autorisation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String] </td> 
   <td> <p>Saisissez la chaîne de requête.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre JSON, placez les guillemets à l’extérieur de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload a transient document]</td> 
   <td> <p>Si vous souhaitez charger un document transitoire, saisissez le fichier source du document que vous souhaitez charger.</p> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL List records]**

Ce module d’action répertorie tous les enregistrements du type sélectionné auxquels le compte a accès.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Adobe Acrobat Sign] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Ajoute automatiquement des en-têtes d’autorisation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Sélectionnez le type d’enregistrement pour lequel vous souhaitez récupérer des enregistrements associés.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Locale]</td> 
   <td> <p>Saisissez les paramètres régionaux de la personne. Cela détermine la langue de l’interface utilisateur. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL External ID]</td> 
   <td>Saisissez ou mappez l’ID externe (un ID attribué en dehors d’[!DNL Adobe Acrobat Sign]) pour les accords que vous souhaitez renvoyer.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group ID]</td> 
   <td>Saisissez l’ID du groupe associé aux enregistrements que vous souhaitez répertorier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show hidden (records)]</td> 
   <td>Activez cette option si vous souhaitez inclure les enregistrements masqués dans vos résultats.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cursor] / [!UICONTROL Start index]</td> 
   <td> <p>Saisissez le numéro du premier enregistrement que le module doit renvoyer. </p> <p>Remarque : ce champ est combiné avec le champ [!UICONTROL Maximum number of returned records] pour la pagination. Par exemple, si la [!UICONTROL Maximum number of returned events] est 100 et que la [!UICONTROL Start index] est 101, le module renvoie les enregistrements 101 à 200, ou la deuxième page de résultats.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned records]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit [action] au cours de chaque cycle d’exécution du scénario.</p> <p>Remarque : ce champ est combiné avec le champ [!UICONTROL Cursor] ou [!UICONTROL Start Index] pour la pagination. Par exemple, si la [!UICONTROL Maximum number of returned events] est 100 et que la [!UICONTROL Start index] est 101, le module renvoie les enregistrements 101 à 200, ou la deuxième page de résultats.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent domain URLs]</td> 
   <td> <p>Entrez ou mappez une liste d’URL de domaines parent séparée par des virgules, les URL renvoyés pouvant être encadrés par la balise iframe. Si ce champ est laissée vide, les pages [!DNL Adobe Acrobat Sign] ne sont pas visibles dans l’iframe.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Read a record]**

Ce module d’action permet de récupérer des informations au sujet d’un seul enregistrement.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Adobe Acrobat Sign] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Ajoute automatiquement des en-têtes d’autorisation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Sélectionnez le type d’enregistrement pour lequel vous souhaitez récupérer des enregistrements associés.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record ID]</td> 
   <td>Saisissez ou mappez l’identifiant de l’enregistrement que vous souhaitez récupérer.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Read related records]**

Consultez les informations complémentaires relatives à un seul enregistrement.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Adobe Acrobat Sign] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Ajoute automatiquement des en-têtes d’autorisation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Sélectionnez le type d’enregistrement pour lequel vous souhaitez récupérer des enregistrements associés.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record ID] (Exemple : [!UICONTROL Account ID])</td> 
   <td>Saisissez ou mappez l’identifiant de l’enregistrement pour lequel vous souhaitez extraire des enregistrements associés.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Other fields]</td> 
   <td>Saisissez les informations dans des champs spécifiques en fonction du type d’enregistrement et des champs connexes.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Update a record]**

Ce module d’action met à jour un seul enregistrement dans [!DNL Adobe Acrobat Sign].

>[!IMPORTANT]
>
>* En guise de bonne pratique, si vous prévoyez d’apporter des modifications substantielles à un accord, nous vous recommandons de créer un nouvel accord plutôt que de mettre à jour l’accord existant.
>* Certaines mises à jour comportent des champs obligatoires. Lorsque vous configurez votre mise à jour, veillez à remplir tous les champs obligatoires. Les champs obligatoires sont en gras dans les modules [!DNL Workfront Fusion].
>



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Adobe Acrobat Sign] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Ajoute automatiquement des en-têtes d’autorisation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record ID] </td> 
   <td>Saisissez ou mappez l’identifiant de l’enregistrement que vous souhaitez mettre à jour.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Sélectionnez le type d’enregistrement à mettre à jour.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Other fields]</td> 
   <td> <p>Saisissez les informations dans des champs spécifiques en fonction du type d’enregistrement et des champs connexes.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Agreement]</b> </p> <p>En guise de bonne pratique, si vous prévoyez d’apporter des modifications substantielles à un accord, nous vous recommandons de créer un nouvel accord plutôt que de mettre à jour l’accord existant.</p> </li> 
     <li> <p><b>[!UICONTROL Library document]</b> </p> <p>Sélectionnez les champs que vous souhaitez mettre à jour, puis remplissez les champs sélectionnés :</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Status]</b> </p> <p>Sélectionnez le nouveau statut du document de bibliothèque.</p> </li> 
       <li> <p><b>[!UICONTROL Name]</b> </p> <p>Saisir ou mapper le nom du modèle de bibliothèque</p> </li> 
       <li> <p><b>[!UICONTROL Sharing mode]</b> </p> <p>Indiquez qui doit avoir accès au document de bibliothèque.</p> </li> 
       <li> <p><b>[!UICONTROL Library template type]</b> </p> <p>Pour chaque type de modèle de bibliothèque que vous souhaitez utiliser, cliquez sur <b>[!UICONTROL Add item]</b> et sélectionnez le type de modèle.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL User]</b> </p> <p>Sélectionnez les champs que vous souhaitez mettre à jour, puis remplissez les champs sélectionnés :</p> 
      <ul> 
       <li> <p><b>[!UICONTROL First name]</b> </p> <p>Saisissez le prénom de la personne.</p> </li> 
       <li> <p><b>[!UICONTROL Last name]</b> </p> <p>Saisissez le nom de famille de la personne.</p> </li> 
       <li> <p><b>[!UICONTROL Company]</b> </p> <p>Saisissez le nom de l’entreprise de la personne.</p> </li> 
       <li> <p><b>[!UICONTROL Phone]</b> </p> <p>Saisissez le numéro de téléphone de la personne.</p> </li> 
       <li> <p><b>[!UICONTROL Primary group ID]</b> </p> <p>Saisissez le groupe auquel la nouvelle personne est ajoutée. Si rien n’est saisi, la personne sera ajoutée au groupe par défaut du compte.</p> </li> 
       <li> <p><b>[!UICONTROL Job title]</b> </p> <p>Saisissez l’intitulé du poste de la personne.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Web form] ([!UICONTROL widget])</b> </p> <p>Saisissez les informations dans des champs spécifiques en fonction du type d’enregistrement et des champs connexes.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Update related record]**

Ce module d’action met à jour les enregistrements relatifs à un objet spécifique.

>[!IMPORTANT]
>
>* En guise de bonne pratique, si vous prévoyez d’apporter des modifications substantielles à un accord, nous vous recommandons de créer un nouvel accord plutôt que de mettre à jour l’accord existant.
>* Certaines mises à jour comportent des champs obligatoires. Lorsque vous configurez votre mise à jour, veillez à remplir tous les champs obligatoires. Les champs obligatoires sont en gras dans les modules [!DNL Workfront Fusion].
>



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Adobe Acrobat Sign] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Ajoute automatiquement des en-têtes d’autorisation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Sélectionnez le type d’enregistrement auquel les champs liés sont associés.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Agreement]/[!UICONTROL Library document]/[!UICONTROL User]/[!UICONTROL Widget ID]</td> 
   <td>Saisissez ou mappez l’identifiant de l’objet auquel vous souhaitez associer l’enregistrement créé.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Other fields]</td> 
   <td> <p>Saisissez les informations dans des champs spécifiques en fonction du type d’enregistrement et des champs connexes.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Agreement]</b> </p> <p>En guise de bonne pratique, si vous prévoyez d’apporter des modifications substantielles à un accord, nous vous recommandons de créer un nouvel accord plutôt que de mettre à jour l’accord existant.</p> </li> 
     <li> <p><b>[!UICONTROL Library document]</b> </p> <p>Sélectionnez les champs que vous souhaitez mettre à jour, puis remplissez les champs sélectionnés :</p> 
      <ul> 
       <li> <p><b>[!UICONTROL State]</b> </p> <p>Sélectionnez le nouveau statut du document de bibliothèque.</p> </li> 
       <li> <p><b>[!UICONTROL Note]</b> </p> <p>Saisissez ou mappez le texte de la note.</p> </li> 
       <li> <p><b>[!UICONTROL Visibility]</b> </p> <p>Choisissez si le document de bibliothèque est affiché ou masqué.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL User]</b> </p> <p>Sélectionnez les champs que vous souhaitez mettre à jour, puis remplissez les champs sélectionnés :</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Group info list]</b> </p> <p>Remplissez les champs suivants.</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Status]</b> </p> <p>Sélectionnez le nouveau statut de la personne.</p> </li> 
         <li> <p><b>[!UICONTROL ID]</b> </p> <p>Saisissez l’identifiant unique du groupe.</p> </li> 
         <li> <p><b>[!UICONTROL Is group admin]</b> </p> <p>Sélectionnez <b>[!UICONTROL Yes]</b> pour faire de cet utilisateur un administrateur de groupe.</p> </li> 
         <li> <p><b>Est le groupe principal</b> </p> <p>Sélectionnez <b>[!UICONTROL Yes]</b> pour mettre à jour ce groupe vers le groupe principal de l’utilisateur.</p> </li> 
         <li> <p><b>[!UICONTROL Created date]</b> </p> <p>Saisissez la date de création du groupe.</p> <p>Pour obtenir la liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">Coercition de type dans [!UICONTROL Adobe Workfront Fusion]</a>.</p> </li> 
         <li> <p><b>[!UICONTROL Name]</b> </p> <p>Saisissez ou mappez le nom du groupe.</p> </li> 
         <li> <p><b>[!UICONTROL Library document creation visible]</b> </p> <p>Ces paramètres déterminent si la personne peut créer des documents de bibliothèque.</p> 
          <ul> 
           <li> <p>[!UICONTROL Value]</p> <p>Autoriser</p> </li> 
           <li> <p>[!UICONTROL Inherited]</p> <p>Hériter des paramètres de groupe d’un groupe ou d’un compte</p> </li> 
          </ul> </li> 
         <li> <p><b>[!UICONTROL Send restricted to workflows]</b> </p> <p>Ces paramètres déterminent si la personne peut créer des accords uniquement à l’aide de workflows.</p> 
          <ul> 
           <li> <p>[!UICONTROL Value]</p> <p>Autoriser</p> </li> 
           <li> <p>[!UICONTROL Inherited]</p> <p>Hériter des paramètres de groupe d’un groupe ou d’un compte</p> </li> 
          </ul> </li> 
         <li> <p><b>[!UICONTROL User can send]</b> </p> 
          <ul> 
           <li> <p>[!UICONTROL Value]</p> <p>Autoriser</p> </li> 
           <li> <p>[!UICONTROL Inherited]</p> <p>Hériter des paramètres de groupe d’un groupe ou d’un compte</p> </li> 
          </ul> </li> 
        </ul> </li> 
      </ul> 
      <ul> 
       <li> <p><b>[!UICONTROL State]</b> </p> <p>Sélectionnez le nouveau statut de la personne et saisissez un commentaire expliquant pourquoi vous souhaitez activer ou désactiver la personne.</p> </li> 
       <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Saisissez les paramètres régionaux de la personne. Cela détermine la langue de l’interface utilisateur. </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Web form] ([!UICONTROL widget])</b> </p> <p>Saisissez les informations dans des champs spécifiques en fonction du type d’enregistrement et des champs connexes.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Upload document]**

Chargez un document transitoire. Un document transitoire est disponible pendant 7 jours après son chargement.

>[!NOTE]
>
>Nous recommandons de charger le document à signer en tant que document transitoire, puis de l’associer au champ Fichier à envoyer dans le module Créer un accord.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Adobe Acrobat Sign] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Ajoute automatiquement des en-têtes d’autorisation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record ID]</td> 
   <td>Saisissez ou mappez l’identifiant de l’enregistrement que vous souhaitez mettre à jour.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL MIME type]</td> 
   <td>Saisissez le type MIME du fichier d’origine. Les types MIME (Multipurpose Internet Mail Extension) sont des libellés qui permettent aux logiciels d’identifier les différents types des données partagées sur Internet. Les serveurs web et les navigateurs utilisent le type MIME pour déterminer ce qu’il convient de faire avec un fichier. Par exemple, un fichier de type MIME <code>text/html</code> sera traité différemment dans un navigateur par rapport à un fichier de type MIME <code>image/jpeg</code>.</td> 
  </tr> 
 </tbody> 
</table>

**Exemple :** dans ce workflow, le document à signer (précédemment téléchargé depuis Workfront) est chargé en tant que document transitoire.

![](/help/workfront-fusion/references/apps-and-modules/assets/sign-example-1-350x308.png)

Le module [!UICONTROL Upload document] fournit au document un identifiant de [!DNL Adobe Acrobat Sign] qui peut être référencé dans les modules ultérieurs. Lorsque le contrat est créé, l’ID du document chargé est inclus dans le champ [!UICONTROL Files to send].

![](/help/workfront-fusion/references/apps-and-modules/assets/sign-example-2-350x356.png)

+++

### Recherches

+++ **[!UICONTROL Search agreements]**

Ce module de recherche permet de rechercher des accords sur la base des critères que vous avez définis.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Adobe Acrobat Sign] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text filter]</td> 
   <td> <p>Recherchez du texte dans les métadonnées de l’accord. </p> 
    <ul> 
     <li> <p><b>[!UICONTROL Find text]</b> </p> <p>Saisissez le texte que vous souhaitez trouver dans les métadonnées de l’accord. Chaque mot est traité comme un élément de texte distinct. </p> </li> 
     <li> <p><b>[!UICONTROL Find text in]</b> </p> <p>Sélectionnez les champs de métadonnées dans lesquels vous souhaitez trouver du texte. Si vous ne sélectionnez rien, les modules effectuent une recherche dans toutes les métadonnées.</p> </li> 
    </ul> <p>Le module renvoie tout accord contenant le texte saisi dans l’un des champs sélectionnés. Exemple : en saissant « campagne de printemps » et en sélectionnant les options Titre et Note, vous obtiendrez tous les accords dont le titre ou la note contient les mots « printemps » ou « campagne »</p> <p>Pour plus d’informations sur la recherche de champs dans [!DNL Adobe Acrobat Sign], voir « Fonctionnement de la recherche de texte » dans Recherche <a href="https://helpx.adobe.com/fr/sign/using/adobesign-search-users-agreements.html#HowSearchWorks">[!DNL Adobe Sign] - Fonctionnement</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Created date]</td> 
   <td>Sélectionnez les dates. Le module ne renvoie que les enregistrements dont la date de création correspond à ce critère.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expiration date]</td> 
   <td>Sélectionnez les dates. Le module ne renvoie que les enregistrements dont la date d’expiration correspond à ce critère.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p role="rowheader">[!UICONTROL Modified date]</p> </td> 
   <td>Sélectionnez les dates. Le module ne renvoie que les enregistrements dont la date de modification correspond à ce critère.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL External ID]</td> 
   <td> <p> L’identifiant externe est un identifiant attribué à l’accord par la personne qui l’envoie, qui peut prendre n’importe quelle forme, mais qui se présente généralement sous la forme « &lt;groupID&gt;:&lt;ID&gt; ».</p> <p>Pour chaque ID externe à ajouter, cliquez sur <b>[!UICONTROL Add]</b> et saisissez ou mappez l’ID externe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group ID]</td> 
   <td> <p>L’identifiant du groupe est un identifiant attribué lors de la création du groupe.</p> <p>Pour chaque ID externe à ajouter, cliquez sur <b>[!UICONTROL Add]</b> et saisissez ou mappez l’ID externe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td> <p>Il s’agit de l’identifiant attribué à l’accord spécifique. </p> <p>Pour chaque ID externe à ajouter, cliquez sur <b>[!UICONTROL Add]</b> et saisissez ou mappez l’ID externe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent ID]</td> 
   <td> <p>Il s’agit de l’identifiant attribué à l’objet parent de l’accord. </p> <p>Pour chaque ID externe à ajouter, cliquez sur <b>[!UICONTROL Add]</b> et saisissez ou mappez l’ID externe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Participant email]</td> 
   <td> <p>L’adresse e-mail d’un participant ou d’une participante. </p> <p>Pour chaque ID externe à ajouter, cliquez sur <b>[!UICONTROL Add]</b> et saisissez ou mappez l’ID externe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Role]</td> 
   <td>Sélectionnez les rôles que vous souhaitez voir figurer dans les résultats renvoyés.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort by]</td> 
   <td>Si vous souhaitez que le module trie les résultats, sélectionnez le champ sur lequel vous souhaitez trier les résultats.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort orde]r</td> 
   <td>Si vous souhaitez que le module trie les résultats, sélectionnez le tri croissant ou décroissant.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status]</td> 
   <td>Sélectionnez les statuts que vous souhaitez voir figurer dans les résultats renvoyés.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Sélectionnez les types d’accords que vous souhaitez voir figurer dans les résultats renvoyés.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subtypes]</td> 
   <td>Sélectionnez les sous-types d’accords que vous souhaitez voir figurer dans les résultats renvoyés. Seuls les accords sur les modèles de bibliothèques comportent des sous-types.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User ID]</td> 
   <td> <p>L’identifiant d’utilisateur ou d’utilisatrice avec lequel l’accord est partagé.</p> <p>Pour chaque ID utilisateur que vous souhaitez ajouter, cliquez sur <b>[!UICONTROL Add]</b> et saisissez ou mappez l’ID utilisateur.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td>Sélectionnez le niveau de visibilité que vous souhaitez voir figurer dans les résultats renvoyés.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start index]</td> 
   <td> <p>Saisissez la position du premier résultat que vous souhaitez renvoyer. Combinez-le avec la [!UICONTROL maximum returned results] pour paginer les résultats</p> <p>Exemple : si vous obtenez 100 résultats à la fois, saisissez 100 pour obtenir les résultats de 100 à 200.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned results]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit [action] au cours de chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++
