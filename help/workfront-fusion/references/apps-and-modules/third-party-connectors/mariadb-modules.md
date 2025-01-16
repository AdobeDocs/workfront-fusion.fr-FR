---
title: Modules MariaDB
description: Dans un scénario  [!DNL Adobe Workfront Fusion] , vous pouvez automatiser les workflows qui utilisent  [!DNL MariaDB] et le connecter à plusieurs applications et services tiers.
author: Becky
draft: Probably
feature: Workfront Fusion
exl-id: 41179cfe-c0f9-4d18-ab7e-374670ac688b
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 77%

---

# Modules [!DNL MariaDB]

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!DNL MariaDB] et le connecter à plusieurs applications et services tiers.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

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

Pour utiliser les modules [!DNL MariaDB], vous devez disposer d’un compte [!DNL MariaDB].

## Connecter [!DNL MariaDB] à [!DNL Workfront Fusion]

Vous pouvez créer une connexion à votre compte [!DNL MariaDB] directement à partir d’un module [!DNL MariaDB].

1. Dans n’importe quel module de [!DNL MariaDB], cliquez sur **[!UICONTROL Add]** en regard du champ [!UICONTROL Connection] .
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
      <td role="rowheader">[!UICONTROL Host]</td> 
      <td> <p>Saisissez l’adresse IP ou le nom d’hôte de votre instance de base de données. Cet hôte doit être accessible de l’extérieur de votre réseau.</p> <p>Exemple : <code>[!DNL mariadb.hwoh2j5h.us-east-1.rds.amazon.com]</code></p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Port]</td> 
      <td>Le port par défaut est 3306. Si vous utilisez un port non standard, définissez ce numéro en fonction de votre port. </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Database Name]</td> 
      <td>Saisissez le nom de la base de données avec laquelle vous souhaitez interagir.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Username]</td> 
      <td>Saisissez votre nom d’utilisateur ou d’utilisatrice.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Password]</td> 
      <td>Saisissez votre mot de passe.</td> 
     </tr> 
    </tbody> 
   </table>

1. Cliquez sur **[!UICONTROL Continue]** pour créer la connexion et revenir au module .

## Modules [!DNL MariaDB] et leurs champs

Lorsque vous configurez les modules [!DNL MariaDB], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL MariaDB] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

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
   <td>Pour obtenir des instructions sur la connexion de votre compte [!DNL MariaDB] à [!DNL Workfront Fusion], voir <a href="#connect-mariadb-to-workfront-fusion" class="MCXref xref">Connecter [!DNL MariaDB] à [!DNL Workfront Fusion]</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td> <p>Saisissez la requête SQL que vous souhaitez que le module utilise pour récupérer les données.</p> <p>Important : les variables utilisées dans la requête ne sont pas nettoyées. Veillez à nettoyer correctement les variables afin d’éviter les injections SQL.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Select rows from a table (advanced)]

Ce module lit les enregistrements de votre base de données.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la connexion de votre compte [!DNL MariaDB] à [!DNL Workfront Fusion], voir <a href="#connect-mariadb-to-workfront-fusion" class="MCXref xref">Connecter [!DNL MariaDB] à [!DNL Workfront Fusion]</a> dans cet article.</td> 
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
   <td> <p>Pour chaque niveau selon lequel vous souhaitez trier vos résultats, cliquez sur <strong>[!UICONTROL Add item]</strong>, puis sélectionnez le champ selon lequel vous souhaitez trier les résultats et si vous souhaitez trier par ordre croissant ou décroissant</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>
