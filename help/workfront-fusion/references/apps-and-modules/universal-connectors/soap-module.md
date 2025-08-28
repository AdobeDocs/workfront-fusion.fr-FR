---
title: Module SOAP
description: Vous pouvez utiliser le module SOAP pour vous connecter aux API SOAP dans Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: dbcc04f8-8306-4a81-aed8-1ce0798e145f
source-git-commit: 95d52f8227c8a40c0db165eea9d2877e60446de9
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 53%

---

# Module [!UICONTROL SOAP]

Vous pouvez utiliser le module [!UICONTROL SOAP] pour vous connecter aux API [!UICONTROL SOAP] dans [!UICONTROL Adobe Workfront Fusion].

## Module SOAP et ses champs

Le connecteur SOAP ne comprend qu’un seul module, Exécuter l’action SOAP

### Exécuter l’action SOAP

Ce module d’action exécute l’action SOAP spécifiée.



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

## Module SOAP et ses champs

Lorsque vous configurez des modules SOAP, Workfront Fusion affiche les champs répertoriés ci-dessous.  Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Exécuter l’action SOAP

Ce module d’action exécute une action SOAP, en fonction du WSDL que vous spécifiez.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL WSDL]</td> 
   <td> Sélectionnez le fichier WSDL que le module doit utiliser. Pour créer un fichier WSDL, cliquez sur <b>Ajouter</b> en regard du champ et renseignez les champs. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL HTTP headers]</td> 
   <td> Pour chaque en-tête HTTP à ajouter, cliquez sur <b>Ajouter un élément</b> et saisissez le nom et la valeur de l’en-tête.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL SOAP headers]</td> 
   <td> Pour chaque en-tête SOAP que vous souhaitez ajouter, cliquez sur <b>Ajouter un élément</b> et saisissez le nom, la valeur, l’espace de noms et XMLNS de l’en-tête.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Force SOAP headers]</td> 
   <td> Activez cette option pour configurer les en-têtes pour SOAP 1.2. </td> 
  </tr> 
  </tbody> 
</table>

## Restrictions du module [!UICONTROL SOAP]

>[!NOTE]
>
>Les redirections sont désactivées pendant le chargement du WDSL. Il s’agit d’une fonctionnalité de sécurité, mais cela peut signifier que les redirections non vérifiées sont bloquées lors de l’exécution du module.

Le module [!UICONTROL SOAP] est actuellement en version Beta et ne prend pas en charge :

* les éléments de redéfinition ;
* les restrictions relatives aux chiffres des fractions ;
* les restrictions relatives aux chiffres totaux ;
* les restrictions relatives aux espaces blancs ;
* plusieurs parties dans les messages d’entrée et de sortie, seuls les messages en une seule partie sont pris en charge ;
* Éléments de schéma XML personnalisés définis à l’aide de schémas et d’éléments de codage SOAP.

>[!BEGINSHADEBOX]

**Exemple :**

Les éléments suivants ne sont pas correctement reconnus par [!UICONTROL Workfront Fusion] :

```
<complexType name="ArrayOfFloat">
   <complexContent>
      <restriction base="soapenc:Array">
         <attribute ref="soapenc:arrayType"
            wsdl:arrayType="xsd:integer[]"/>
      </restriction>
   </complexContent>
</complexType>
```

Cet exemple inclut les références `soapenc:Array`, `soapenc:arrayType` et `wsdl:arrayType` qui ne sont pas encore prises en charge dans [!UICONTROL Workfront Fusion].

>[!ENDSHADEBOX]

## Solution de contournement

Si le module [!UICONTROL SOAP] refuse de traiter le fichier WSDL ou renvoie diverses erreurs dans la configuration du module, vous pouvez essayer d’utiliser le module universel **[!UICONTROL HTTP] > [!UICONTROL Effectuer une requête]** à la place :

1. Dans Workfront Fusion, créez un scénario.
1. Insérez le module **[!UICONTROL HTTP] > [!UICONTROL Effectuer une requête]** dans le scénario.
1. Ouvrez la configuration du module et renseignez les champs suivants :

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Method]</td> 
      <td> <p>[!UICONTROL POST]</p> </td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td role="rowheader">[!UICONTROL Body type]</td> 
      <td> <p>[!UICONTROL Raw]</p> </td>
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Content type]</td> 
      <td> <p>[!UICONTROL XML (application/xml)]</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Parse response]</td> 
      <td>[!UICONTROL Enabled]</td> 
     </tr> 
    </tbody> 
   </table>

   <!--![Workaround](/help/workfront-fusion/references/apps-and-modules/assets/workaround-350x443.png)-->

1. Ouvrez une nouvelle fenêtre ou un nouvel onglet du navigateur web.
1. Collez l’URL WSDL dans la barre d’adresse du navigateur web et récupérez le fichier XML.

   L’URL WSDL se termine généralement par `?wsdl`, mais pas nécessairement, par exemple `http://voip.ms/api/v1/server.wsdl`.

1. Si le fichier WSDL ne s’affiche pas directement dans le navigateur web, ouvrez le fichier téléchargé dans un éditeur de texte.
1. Recherchez la balise `<service>` ou `<wsdl:service>` :

   <!--![Service](/help/workfront-fusion/references/apps-and-modules/assets/service-350x65.png)-->

1. Une fois localisée, copiez l’URL à partir de l’attribut `location`.
1. Dans Workfront Fusion, collez l’URL dans le champ URL du module HTTP .
1. Fournissez des valeurs pour les paramètres sélectionnés en remplaçant les points d&#39;interrogation par des valeurs réelles.

   >[!NOTE]
   >
   > Pour obtenir des valeurs spécifiques à partir du fichier WSDL, utilisez une visionneuse WSDL en ligne.

   <!--![Request](/help/workfront-fusion/references/apps-and-modules/assets/request-xml-350x172.png)-->

1. Fermez la configuration du module en cliquant sur **[!UICONTROL OK]**.
1. Exécutez le scénario ou le module.
