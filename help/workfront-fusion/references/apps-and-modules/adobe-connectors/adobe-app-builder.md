---
title: Module Adobe App Builder
description: Le connecteur Adobe App Builder vous permet d’utiliser des fonctions personnalisées dans vos scénarios.
author: Becky
feature: Workfront Fusion
exl-id: 92661a0c-436b-4fbd-808a-a4fbe3cd2339
source-git-commit: 02c396f33b6398635462bac8741f446eb82bf5a9
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 18%
---
# Module Adobe App Builder

Vous pouvez créer des fonctions personnalisées dans la zone Fonctions de Fusion. Vous ajoutez ensuite ces fonctions à vos scénarios sous la forme d’un module Adobe App Builder .

Les fonctions personnalisées fonctionnent via Adobe App Builder. Votre entreprise doit donc disposer d’une licence Adobe App Builder pour les utiliser.

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tout package de workflow Adobe Workfront et tout package d’automatisation et d’intégration Adobe Workfront</p><p>Workfront Ultimate</p><p>Packages Workfront Prime et Select, avec l’achat supplémentaire de Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licences Adobe Workfront</td> 
   <td> <p>Standard</p><p>Travail ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p><ul><li>Si votre organisation dispose d’un package Workfront Select ou Prime qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acquérir Adobe Workfront Fusion.</li><li>Vous devez disposer d’une licence Adobe App Builder pour utiliser des fonctions personnalisées.</ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Création d’une connexion à Adobe App Builder

La connexion utilise les informations d’identification Adobe I/O Runtime d’un espace de travail de projet App Builder. Avant de créer la connexion, récupérez ces informations d’identification à partir du Adobe Developer Console.

### Obtenir vos informations d’identification d’exécution

1. Connectez-vous à [Adobe Developer Console](https://developer.adobe.com/console) avec l’organisation qui dispose de votre licence App Builder.
1. Ouvrez le projet App Builder contenant vos fonctions, puis sélectionnez l’espace de travail auquel vous souhaitez vous connecter (par exemple, **Production**).
1. Cliquez sur **Télécharger tout** dans le coin supérieur droit pour télécharger le fichier JSON de configuration de l’espace de travail.
1. Ouvrez le fichier et recherchez la section `runtime`. Il contient les éléments suivants :

   * `namespace` : valeur à renseigner dans le champ **Espace de noms**
   * `auth` : une valeur au format `username:password`. La partie avant les deux-points est le **nom d&#39;utilisateur**, et la partie après les deux-points est le **mot de passe**.

   >[!NOTE]
   >
   >Vous pouvez également rechercher l’espace de noms et les valeurs d’authentification en exécutant `aio runtime namespace get` ou `aio app use` dans l’interface de ligne de commande Adobe I/O.

### Créer la connexion

1. Dans le module , cliquez sur **Ajouter** en regard du champ **Connexion**.
1. Remplissez les champs suivants :

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection name]</td> 
      <td>Saisissez un nom pour cette connexion.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Environment]</td> 
      <td>Indiquez si vous vous connectez à un environnement de production ou hors production.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Type]</td> 
      <td>Sélectionnez <b>Compte de service</b>.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Username]</td> 
      <td>Saisissez le nom d'utilisateur à partir de la valeur <code>auth</code> de votre espace de travail (la partie avant les deux-points).</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Password]</td> 
      <td>Saisissez le mot de passe à partir de la valeur <code>auth</code> de votre espace de travail (la partie après les deux-points).</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Namespace]</td> 
      <td>Saisissez la valeur <code>namespace</code> dans la section <code>runtime</code> du fichier de configuration de votre espace de travail.</td> 
     </tr> 
    </tbody> 
   </table>

1. Cliquez sur **Continuer** pour enregistrer la connexion.

## Modules Adobe App Builder

### Exécution d’un bloc de code personnalisé

Ce module vous permet d’exécuter un bloc de code. Vous configurez le bloc de code lorsque vous configurez le module, qui est exécuté lorsque le module s’exécute lors de l’exécution d’un scénario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Sélectionnez la connexion contenant la fonction personnalisée que vous souhaitez exécuter. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Code block]</td> 
   <td>Saisissez le bloc de code que le module doit exécuter.<p>Pour formater le code afin de le lire plus facilement, cliquez sur l'icône <b>Formater le code</b>.</td> 
  </tr> 
   </tbody> 
</table>

### Exécuter une fonction personnalisée à partir d’un package

Ce module exécute une fonction à partir d’un package.

Pour plus d&#39;informations sur les packages, consultez [Utilisation de packages de fonctions personnalisées](/help/workfront-fusion/create-scenarios/map-data/use-custom-function-packages.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Sélectionnez la connexion contenant la fonction personnalisée que vous souhaitez exécuter. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package]</td> 
   <td>Sélectionnez le package contenant la fonction que vous souhaitez exécuter dans le scénario.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variable] </td> 
   <td>Sélectionnez la fonction que vous souhaitez exécuter dans le scénario.</p></td> 
  </tr> 
   </tbody> 
</table>

### Utiliser la variable depuis le package

Ce module intègre une variable configurée dans un package à votre scénario.

Pour plus d&#39;informations sur les packages, consultez [Utilisation de packages de fonctions personnalisées](/help/workfront-fusion/create-scenarios/map-data/use-custom-function-packages.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Sélectionnez la connexion contenant la fonction personnalisée que vous souhaitez exécuter. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package]</td> 
   <td>Sélectionnez le package qui comprend la variable que vous souhaitez importer dans le scénario.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variable] </td> 
   <td>Sélectionnez la variable que vous souhaitez importer dans le scénario.</p></td> 
  </tr> 
   </tbody> 
</table>

### Exécuter une fonction personnalisée ou un bloc de code

Ce module vous permet d’utiliser une fonction JavaScript personnalisée configurée précédemment et stockée dans la zone Fonctions .

Pour obtenir des instructions sur la configuration d’une fonction personnalisée, voir [Mapper des données à l’aide de fonctions personnalisées](/help/workfront-fusion/create-scenarios/map-data/map-using-custom-functions.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Sélectionnez la connexion contenant la fonction personnalisée que vous souhaitez exécuter. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td>Sélectionnez la fonction personnalisée que vous souhaitez exécuter.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Paramètres  </td> 
   <td>Saisissez les valeurs des paramètres de la fonction. Les paramètres disponibles sont basés sur les paramètres configurés lors de la création de la fonction.<p>Si un paramètre possède une valeur par défaut, vous ne le verrez pas dans le champ, mais vous pouvez le remplacer en saisissant ou en mappant une valeur dans le champ.</p></td> 
  </tr> 
   </tbody> 
</table>


