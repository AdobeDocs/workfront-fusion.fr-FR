---
title: Modules de modèle Microsoft Word
description: Dans un scénario d’Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent des modèles Microsoft Word et les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: a5ba5634-226b-4886-a4f1-3a14948c1605
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1353'
ht-degree: 83%

---

# Modules [!DNL Microsoft Word Template]

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent [!DNL Microsoft Word Templates] et les connecter à plusieurs applications et services tiers.

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

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Conditions préalables

Pour utiliser [!DNL Miscrosoft Word Templates] avec Adobe Workfront Fusion, il est nécessaire d’avoir un compte [!DNL Office 365]. Vous pouvez en créer un au `www.office.com`.



## Connexion du service [!DNL Office] à Workfront Fusion

Pour obtenir des instructions sur la connexion de votre compte [!DNL Office] à [!UICONTROL Workfront Fusion], voir [Créer une connexion à [!UICONTROL Adobe Workfront Fusion] : instructions de base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Certaines applications Microsoft utilisent la même connexion, qui est liée à des autorisations d’utilisateur ou d’utilisatrice. Ainsi, lors de la création d’une connexion, l’écran de consentement aux autorisations affiche les autorisations précédemment accordées à la connexion de cet utilisateur ou de cette utilisatrice, en plus des nouvelles autorisations nécessaires à l’application actuelle.
>
>Par exemple, si un utilisateur ou une utilisatrice dispose d’autorisations « Lire le tableau » accordées via le connecteur Excel, puis crée une connexion dans le connecteur Outlook pour lire les e-mails, l’écran de consentement aux autorisations affiche à la fois l’autorisation « Lire le tableau » déjà accordée et l’autorisation « Écrire des e-mails » nouvellement requise.

## Utiliser des modules [!DNL Microsoft Word Templates]

Vous pouvez utiliser un module [!DNL Microsoft Word Template] pour fusionner les données de plusieurs services web en un document [!DNL Microsoft Word].

Par exemple, vous pouvez utiliser ce modèle [!DNL Microsoft Word] :

![Modèle Word antérieur](/help/workfront-fusion/references/apps-and-modules/assets/word-template-before-filled-350x62.png)

Pour créer ce document :

![modèle Word rempli](/help/workfront-fusion/references/apps-and-modules/assets/word-template-exampled-filled-350x85.png)

## À propos des balises de valeur

Un modèle [!DNL Microsoft Word] est un document [!DNL Microsoft Word] normal (fichier .docx) avec des balises spéciales dans son texte qui déterminent où et comment fusionner ou remplir des données. Il existe trois types de balises :

* [Balise de valeur simple](#simple-value-tag)
* [Balise de condition](#condition-tag)
* [Balise de boucle](#loop-tag)

### Balise de valeur simple {#simple-value-tag}

Une balise de valeur simple est simplement remplacée par une valeur correspondante. Le nom de la balise correspond à la valeur du champ [!UICONTROL Key], qui est placée entre des accolades doubles, par exemple `{{name}}`.

**Exemple :** pour créer un document qui indique « Bonjour, Petr ! », vous pouvez utiliser un module [!DNL Microsoft Word Template] pour créer le modèle suivant :

```
> Hi {{name}}!
```

Pour ce faire, vous devez configurer le module comme suit :

![Valeur simple du modèle Word](/help/workfront-fusion/references/apps-and-modules/assets/word-template-simple-value-350x286.png)

### Balise de condition {#condition-tag}

Vous pouvez utiliser une balise de condition pour renvoyer à la ligne le texte qui doit être renvoyé uniquement lorsque certaines conditions sont remplies. Pour renvoyer le texte à la ligne, placez-le entre les balises de condition d’ouverture et de fermeture, telles que « hasPhone » si la condition indique si les données incluent ou non un numéro de téléphone. Le nom d’une balise d’ouverture est précédé d’un signe de hachage #, le nom d’une balise de fermeture est précédé d’une barre oblique /, comme illustré dans l’exemple ci-dessous.

**Exemple :** pour produire un document qui comprend le numéro de téléphone d’un client ou d’une cliente si les données d’entrée incluent un numéro de téléphone, mais pas d’adresse e-mail, vous pouvez utiliser un module [!DNL Microsoft Word Template] et créer le modèle suivant :

```
> {{#hasPhone}}Phone: {{phone}} {{/hasPhone}}
> {{#hasEmail}}Email: {{email}} {{/hasEmail}}
```

Pour ce faire, vous devez configurer le module comme suit :

![Modèle Word conditionnel](/help/workfront-fusion/references/apps-and-modules/assets/word-template-conditional-350x501.png)

Dans le document, le numéro de téléphone se présente comme suit :

```
> Phone: 4445551234
```

### Balise de boucle {#loop-tag}

Vous pouvez utiliser un libellé de boucle, également appelée balise de section, pour répéter une section de texte. Enveloppez le texte en le plaçant entre les balises de boucle d’ouverture et de fermeture. Le nom d’une balise d’ouverture est précédé d’un signe dièse # ; le nom d’une balise de fermeture est précédé d’une barre oblique /.

**Exemple :** pour produire un document qui répertorie le nom et le numéro de téléphone de chaque contact dans une liste de clientes et de clients, vous pouvez utiliser un module [!DNL Microsoft Word Template] et créer le modèle suivant :

```
> {{#contact}}
>     {{name}}, {{phone}}
> {{/contact}}
```

Pour ce faire, vous devez configurer le module comme suit :


![Remplir un document](/help/workfront-fusion/references/apps-and-modules/assets/word-template-fill-out-a-document-350x732.png)

Le module crée le document suivant :

```
> Jan Toman, 4445551234
> Eduard Salo, 4445552345
```

## Modules [!DNL Microsoft Word Template]

Ces modules ne nécessitent pas de connexion.

* [Remplir un document](#fill-out-a-document)
* [Remplir un document avec un lot de données](#fill-a-document-with-a-batch-of-data)

### [!UICONTROL Remplir un document] {#fill-out-a-document}

Ce module du transformateur permet de remplir un document avec les données indiquées. Il peut être utilisé avec des balises de valeurs simples, des balises conditionnelles ou des balises de boucle.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start delimiter of the text being replaced]</td> 
   <td> <p>Saisissez le ou les caractères que vous souhaitez marquer au début du texte remplacé. </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Exemple : </b></span></span>Saisissez <code>&#91;&#91;</code> pour remplacer <code>[[replace_me]]</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL End delimiter of the text being replaced]</p> </td> 
   <td> <p>Saisissez le ou les caractères que vous souhaitez marquer la fin du texte remplacé. </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Exemple : </b></span></span>Saisissez <code>&#93;&#93;</code> remplacer <code>[[replace_me]]</code></p>. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p> Sélectionnez un fichier source à partir d’un module précédent ou mappez les données du fichier source.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name of filled out file]</td> 
   <td>Saisissez un nom de fichier (extension incluse) pour le fichier de sortie cible.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data source]</td> 
   <td> <p>Sélectionnez une option pour indiquer si les données que vous utilisez proviennent d’un formulaire ou d’une collecte de données brutes (données informatiques non traitées).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Values]</td> 
   <td> <p>Il doit s’agir d’un tableau de collections dans lequel :</p> 
    <ul> 
     <li>chaque collection correspond à une entrée de données et contient un élément ; <code>entry</code></li> 
     <li>L’élément <code>entry </code> contient une collection du <code>key </code> et <code>value</code></li> 
     <li>l’élément <code>key </code> contient le nom de la balise.</li> 
     <li>L’élément <code>value </code> contient la valeur de la balise.</li> 
    </ul> 
    <p>Pour ajouter une entrée :</p>
    <ol> 
     <li> Cliquez sur <b>[!UICONTROL Add Item]</b>. </li> 
     <li>Sélectionnez le type de valeur de l’entrée.</li> 
     <li>Ajoutez le nom et la valeur. Pour plus d’informations, voir l’exemple du type de valeur choisi dans cet article. 
      <ul> 
       <li><a href="#simple-value-tag" class="MCXref xref">Balise de valeur simple</a></li> 
       <li><a href="#condition-tag" class="MCXref xref">Balise de condition</a></li> 
       <li><a href="#loop-tag" class="MCXref xref">Balise de boucle</a></li> 
      </ul></li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Remplir un document avec un lot de données] {#fill-a-document-with-a-batch-of-data}

Ce module d’agrégation s’avère utile si vos entrées de données sont des lots distincts. Grâce à ce module, vous pouvez facilement configurer la structure requise pour le champ Valeur et mapper les éléments à chaque élément de valeur. Contrairement au module Remplir un document, le champ Valeurs du module Remplir un document avec un lot de données n’autorise qu’une seule entrée contenant des variables.

Vous pouvez également utiliser ce module si vos entrées de données sont fournies sous la forme d’un tableau, en utilisant le module *Itérateur* pour transformer le contenu du tableau en une série de lots.

Les valeurs réelles sont créées et renseignées pour chaque lot entrant. Le modèle est produit une fois tous les lots d’entrée traités.

Ce module d’agrégation est particulièrement utile pour la création de listes ou de rapports.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
   <td>Sélectionnez le module qui est la source de votre texte.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start delimiter of the text being replaced]</td> 
   <td> <p>Saisissez le ou les caractères que vous souhaitez marquer au début du texte remplacé. </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Exemple : </b></span></span>Saisissez <code>&#91;&#91;</code> pour remplacer <code>[[replace_me]]</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL End delimiter of the text being replaced]</p> </td> 
   <td> <p>Saisissez le ou les caractères que vous souhaitez marquer la fin du texte remplacé. </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>Exemple : </b></span></span>Saisissez <code>&#93;&#93;</code> pour remplacer <code>[[replace_me]]</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group by]</td> 
   <td> Définissez une expression contenant un ou plusieurs éléments mappés. Les données agrégées sont séparées en groupes ayant la même valeur d’expression. Chaque groupe génère une sortie en tant que lot distinct contenant une clé avec l’expression évaluée et le texte agrégé. Ce faisant, vous pouvez utiliser la clé comme filtre dans les modules suivants.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stop processing after an empty aggregation]</td> 
   <td>Activez cette option pour arrêter le traitement lorsqu’une agrégation ne contient aucun bundle.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p> Sélectionnez un fichier source à partir d’un module précédent ou mappez les données du fichier source.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name of filled out file]</td> 
   <td>Saisissez un nom de fichier (extension incluse) pour le fichier de sortie cible.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Values]</td> 
   <td> <p>Il doit s’agir d’un tableau de collections dans lequel :</p> 
    <ul> 
     <li>chaque collection correspond à une entrée de données et contient un élément ; <code>entry</code></li> 
     <li>L’élément <code>entry </code> contient une collection du <code>key </code> et <code>value</code></li> 
     <li>l’élément <code>key </code> contient le nom de la balise.</li> 
     <li>L’élément <code>value </code> contient la valeur de la balise.</li> 
    </ul> 
    <p>Pour ajouter une entrée :</p>
    <ol> 
     <li> Cliquez sur <b>[!UICONTROL Add Item]</b>. </li> 
     <li>Sélectionnez le type de valeur de l’entrée.</li> 
     <li>Ajoutez le nom et la valeur. Pour plus d’informations, voir l’exemple du type de valeur choisi dans cet article. 
      <ul> 
       <li><a href="#simple-value-tag" class="MCXref xref">Balise de valeur simple</a></li> 
       <li><a href="#condition-tag" class="MCXref xref">Balise de condition</a></li> 
       <li><a href="#loop-tag" class="MCXref xref">Balise de boucle</a></li> 
      </ul></li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>
