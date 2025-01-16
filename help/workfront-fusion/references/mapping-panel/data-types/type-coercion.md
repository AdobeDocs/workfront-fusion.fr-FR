---
title: Coercition de type
description: Ce document décrit le comportement d’ [!DNL Adobe Workfront Fusion]  dans des situations où il reçoit des valeurs dans des formats de données attendus et inattendus.
author: Becky
feature: Workfront Fusion
exl-id: a8bdd36d-c01f-4019-a3ea-fb185101500e
source-git-commit: b7c511c51a2f27292cd0cb754673515e67c8a397
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 91%

---

# Coercition de type

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!DNL Adobe Workfront] formule*</td> 
   <td> <p>[!DNL Pro] ou une version ultérieure</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licence*</td> 
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adobe Workfront Fusion] licence**</td> 
   <td>
   <p>Exigences de licence actuelles : aucune exigence de licence [!DNL Workfront Fusion] requise.</p>
   <p>Ou</p>
   <p>Ancienne exigence de licence : [!UICONTROL [!DNL Workfront Fusion] pour l’automatisation et l’intégration du travail] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Exigences actuelles relatives aux produits : si vous disposez du plan de [!DNL Adobe Workfront] [!UICONTROL Select] ou [!UICONTROL Prime], votre entreprise doit acheter des [!DNL Adobe Workfront Fusion] et [!DNL Adobe Workfront] utiliser les fonctionnalités décrites dans cet article. [!DNL Workfront Fusion] est inclus dans le plan de [!DNL Workfront] [!UICONTROL Ultimate].</p>
   <p>Ou</p>
   <p>Exigences liées aux produits hérités : votre entreprise doit acheter [!DNL Adobe Workfront Fusion] ainsi qu’[!DNL Adobe Workfront] pour utiliser la fonctionnalité décrite dans cet article.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Pour connaître la formule, le type de licence ou l’accès dont vous disposez, contactez votre équipe d’administration [!DNL Workfront].

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [[!DNL Adobe Workfront Fusion] licences](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

### Coercition de type

Ce document décrit le comportement d’[!DNL Adobe Workfront Fusion] dans des situations où il reçoit des valeurs dans des formats de données attendus et inattendus.

<table style="table-layout:auto">
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Attendu</th> 
   <th>Reçu</th> 
   <th> <p>Description</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Tableau </td> 
   <td>Tableau </td> 
   <td> <p>La valeur est transmise telle quelle.</p> </td> 
  </tr> 
  <tr> 
   <td>Tableau </td> 
   <td>Autre </td> 
   <td> <p>Si la valeur reçue n’est pas de type tableau, [!DNL Workfront Fusion] crée un tableau et le premier (ainsi que le seul) élément est la valeur reçue.</p> </td> 
  </tr> 
  <tr> 
   <td>booléen </td> 
   <td>booléen </td> 
   <td> <p>La valeur est transmise telle quelle.</p> </td> 
  </tr> 
  <tr> 
   <td>booléen </td> 
   <td>Nombre </td> 
   <td> <p>La valeur est convertie en Oui logique, même si la valeur est 0.</p> </td> 
  </tr> 
  <tr> 
   <td>booléen </td> 
   <td>Texte </td> 
   <td> <p>Si la valeur est égale, fausse ou vide, elle est convertie en Non logique. Dans le cas contraire, elle est convertie en Oui logique.</p> </td> 
  </tr> 
  <tr> 
   <td>booléen </td> 
   <td>Autre </td> 
   <td> <p>La valeur est convertie en Oui logique lorsque la valeur reçue existe (elle n’est pas nulle).</p> </td> 
  </tr> 
  <tr> 
   <td>Buffer </td> 
   <td>Buffer </td> 
   <td> <p>La valeur n’est transmise sans modification que si la page de code est conforme aux attentes. Si la page de code diffère, [!DNL Workfront Fusion] essaiera de convertir la valeur reçue vers la page de code demandée. Si cette conversion n’est pas prise en charge, [!DNL Workfront Fusion] renverra une erreur de validation.</p> </td> 
  </tr> 
  <tr> 
   <td>Buffer </td> 
   <td>booléen </td> 
   <td> <p>La valeur est convertie en texte (vrai/faux), puis en données binaires en suivant les étapes mentionnées ci-dessus pour la conversion en texte.</p> </td> 
  </tr> 
  <tr> 
   <td>Buffer </td> 
   <td>Date </td> 
   <td> <p>La valeur est convertie en texte ISO 8601, puis en données binaires suivant les étapes mentionnées pour la conversion en texte.</p> </td> 
  </tr> 
  <tr> 
   <td>Buffer </td> 
   <td>Nombre </td> 
   <td> <p>La valeur est convertie en texte, puis en données binaires en suivant les étapes mentionnées ci-dessus pour la conversion en texte.</p> </td> 
  </tr> 
  <tr> 
   <td>Buffer </td> 
   <td>Texte </td> 
   <td> <p>La valeur est convertie en données binaires et codée comme prévu. Si l’encodage attendu n’est pas spécifié, l’encodage utf8 sera utilisé.</p> </td> 
  </tr> 
  <tr> 
   <td>Buffer </td> 
   <td>Autre </td> 
   <td> <p>[!DNL Workfront Fusion] Renvoie une erreur de validation.</p> </td> 
  </tr> 
  <tr> 
   <td>Collection </td> 
   <td>Collection </td> 
   <td> <p>La valeur est transmise telle quelle.</p> </td> 
  </tr> 
  <tr> 
   <td>Collection </td> 
   <td>Autre </td> 
   <td> <p>[!DNL Workfront Fusion] Renvoie une erreur de validation.</p> </td> 
  </tr> 
  <tr> 
   <td>Date </td> 
   <td>Date </td> 
   <td> <p>La valeur est transmise telle quelle.</p> </td> 
  </tr> 
  <tr> 
   <td>Date </td> 
   <td>Texte </td> 
   <td> <p>[!DNL Workfront Fusion] Essaiera de convertir le texte en date. Si la conversion échoue, elle renvoie une erreur de validation. La date doit contenir le jour, le mois et l’année. La date peut contenir l’heure et le fuseau horaire. Le fuseau horaire par défaut est basé sur vos paramètres. Exemples :</p> <p><code>2016-06-20T17:26:44.356Z</code> </p> <p><code>2016-06-20 19:26:44 GMT+02:00</code> </p> <p><code>2016-06-20 19:26+0200</code> </p> <p><code>2016-06-20 17:26:44</code> </p> <p><code>2016-06-20</code> </p> <p><code>2016/06/20 17:26:44</code> </p> <p><code>2016/06/20 19:26:44+02:00</code> </p> <p><code>2016/06/20 17:26</code> </p> <p><code>2016/06/20 5:26 PM</code> </p> <p><code>2016/06/20</code> </p> <p><code>06/20/2016 17:26:44</code> </p> <p><code>06/20/2016 19:26:44+02:00</code> </p> <p><code>06/20/2016 17:26</code> </p> <p><code>06/20/2016 5:26 PM</code> </p> <p><code>06/20/2016</code> </p> <p><code>20.6.2016 17:26:44</code> </p> <p><code>20.6.2016 19:26:44+02:00</code> </p> <p><code>20.6.2016 17:26</code> </p> <p><code>20.6.2016</code> </p> </td> 
  </tr> 
  <tr> 
   <td>Date </td> 
   <td>Autre </td> 
   <td> <p>[!DNL Workfront Fusion] Renvoie une erreur de validation.</p> </td> 
  </tr> 
  <tr> 
   <td>Nombre </td> 
   <td>Nombre </td> 
   <td> <p>La valeur est transmise telle quelle.</p> </td> 
  </tr> 
  <tr> 
   <td>Nombre </td> 
   <td>Texte </td> 
   <td> <p>[!DNL Workfront Fusion] Essaiera de convertir le texte en nombre. Si la conversion échoue, elle renvoie une erreur de validation.</p> </td> 
  </tr> 
  <tr> 
   <td>Nombre </td> 
   <td>Autre </td> 
   <td> <p>[!DNL Workfront Fusion] Renvoie une erreur de validation.</p> </td> 
  </tr> 
  <tr> 
   <td>Texte </td> 
   <td>Texte </td> 
   <td> <p>La valeur est transmise telle quelle.</p> </td> 
  </tr> 
  <tr> 
   <td>Texte </td> 
   <td>Tableau </td> 
   <td> <p>Si le tableau donné prend en charge la conversion en texte, la valeur est convertie. Dans le cas contraire, [!DNL Workfront Fusion] renverra une erreur de validation.</p> </td> 
  </tr> 
  <tr> 
   <td>Texte </td> 
   <td>booléen </td> 
   <td> <p>La valeur est convertie en texte (vrai/faux).</p> </td> 
  </tr> 
  <tr> 
   <td>Texte </td> 
   <td>Buffer </td> 
   <td> <p>Si le codage de texte est spécifié pour les données binaires, la valeur est convertie en texte. Dans le cas contraire, [!DNL Workfront Fusion] renverra une erreur de validation.</p> </td> 
  </tr> 
  <tr> 
   <td>Texte </td> 
   <td>Date </td> 
   <td> <p>La valeur est convertie en texte ISO 8601.</p> </td> 
  </tr> 
  <tr> 
   <td>Texte </td> 
   <td>Nombre </td> 
   <td> <p>La valeur est convertie en texte.</p> </td> 
  </tr> 
  <tr> 
   <td>Texte </td> 
   <td>Autre </td> 
   <td> <p>[!DNL Workfront Fusion] Renvoie une erreur de validation.</p> </td> 
  </tr> 
  <tr> 
   <td>heure </td> 
   <td>heure </td> 
   <td> <p>La valeur est transmise telle quelle.</p> </td> 
  </tr> 
  <tr> 
   <td>heure </td> 
   <td>Texte </td> 
   <td> <p>[!DNL Workfront Fusion] essaiera de convertir l’heure au format <code>hours:minutes:seconds</code>. Si la conversion échoue, elle renvoie une erreur de validation.</p> </td> 
  </tr> 
  <tr> 
   <td>heure </td> 
   <td>Autre </td> 
   <td> <p>[!DNL Workfront Fusion] Renvoie une erreur de validation.</p> </td> 
  </tr> 
 </tbody> 
</table>
