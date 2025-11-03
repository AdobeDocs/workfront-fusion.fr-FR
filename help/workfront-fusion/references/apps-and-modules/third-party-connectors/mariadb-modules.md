---
title: Modules MariaDB
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent  [!DNL MariaDB], et le connecter à plusieurs applications et services tiers.
author: Becky
draft: Probably
feature: Workfront Fusion
exl-id: 41179cfe-c0f9-4d18-ab7e-374670ac688b
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 70%

---

# Modules [!DNL MariaDB]

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent [!DNL MariaDB] et les connecter à plusieurs applications et services tiers.

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

Pour utiliser les modules [!DNL MariaDB], vous devez disposer d’un compte [!DNL MariaDB].

## Connecter [!DNL MariaDB] à Workfront Fusion

Vous pouvez créer une connexion à votre compte [!DNL MariaDB] directement à partir d’un module [!DNL MariaDB].

1. Dans n’importe quel module [!DNL MariaDB], cliquez sur **[!UICONTROL Ajouter]** en regard du champ [!UICONTROL Connexion].
1. Configurez les champs suivants :

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td> <p>Saisissez un nom pour la nouvelle connexion.</p> </td> 
     </tr> 
        <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>Indiquez si cette connexion est destinée à un environnement de production ou hors production.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>Indiquez si vous vous connectez à un compte de service ou à un compte personnel.</td>
        </tr>
     <tr> 
      <td role="rowheader">[!UICONTROL Host]</td> 
      <td> <p>Saisissez l’adresse IP ou le nom d’hôte de votre instance de base de données. Cet hôte doit être accessible de l’extérieur de votre réseau.</p> <p>Exemple : <code>[!DNL mariadb.hwoh2j5h.us-east-1.rds.amazon.com]</code></p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Port]</td> 
      <td>Le port par défaut est 3306. Si vous utilisez un port non standard, définissez ce numéro en fonction de votre port. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Database &#x200B;]</td> 
      <td>Saisissez le nom de la base de données avec laquelle vous souhaitez interagir.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL User]</td> 
      <td>Saisissez votre nom d’utilisateur ou d’utilisatrice.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Password]</td> 
      <td>Saisissez votre mot de passe.</td> 
     </tr> 
    </tbody> 
   </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour créer la connexion et retournez au module.

## Modules [!DNL MariaDB] et leurs champs

Lorsque vous configurez les modules [!DNL MariaDB], Workfront Fusion affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL MariaDB] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Exécuter une requête (avancé)

Ce module d’action extrait des informations de votre base de données, sur la base d’une requête que vous fournissez.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour plus d’informations sur la connexion de votre compte [!DNL MariaDB] à Workfront Fusion, voir <a href="#connect-mariadb-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL MariaDB] à Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td> <p>Saisissez la requête SQL que vous souhaitez que le module utilise pour récupérer les données.</p> <p>Important : les variables utilisées dans la requête ne sont pas nettoyées. Veillez à nettoyer correctement les variables afin d’éviter les injections SQL.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Sélectionner des lignes dans un tableau (avancé)]

Ce module lit les enregistrements de votre base de données.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour plus d’informations sur la connexion de votre compte [!DNL MariaDB] à Workfront Fusion, voir <a href="#connect-mariadb-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL MariaDB] à Workfront Fusion</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table]</td> 
   <td> <p>Sélectionnez le tableau qui contient les enregistrements que vous souhaitez lire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Définissez le filtre par lequel vous souhaitez sélectionner les lignes.</p> 
    <ul> 
     <li> <p>Sélectionnez le champ dans lequel vous souhaitez effectuer une recherche.</p> </li> 
     <li> <p>Sélectionnez l’opérateur que vous souhaitez utiliser pour votre recherche.</p> </li> 
     <li> <p>Saisissez ou mappez la valeur que vous souhaitez rechercher.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort] </td> 
   <td> <p>Pour chaque niveau par lequel vous souhaitez trier vos résultats, cliquez sur <strong>[!UICONTROL Add item]</strong>, puis sélectionnez le champ par lequel vous souhaitez trier les résultats et indiquez si vous souhaitez les trier par ordre croissant ou décroissant.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>
