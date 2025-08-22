---
title: Coercition de type
description: Ce document décrit le comportement d’Adobe Workfront Fusion dans des situations où il reçoit des valeurs dans des formats de données attendus et inattendus.
author: Becky
feature: Workfront Fusion
exl-id: a8bdd36d-c01f-4019-a3ea-fb185101500e
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 60%

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
    <td role="rowheader">Formule Adobe Workfront*</td> 
   <td> <p>[!DNL Pro] ou une version ultérieure</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licence Adobe Workfront*</td> 
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licence [!UICONTROL Adobe Workfront Fusion]**</td> 
   <td>
   <p>Exigence de licence actuelle : aucune exigence de licence Workfront Fusion.</p>
   <p>Ou</p>
   <p>Exigence de licence héritée : [!UICONTROL Workfront Fusion for Work Automation and Integration] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Configuration requise actuelle du produit : si vous disposez du plan Adobe Workfront [!UICONTROL Select] ou [!UICONTROL Prime], votre entreprise doit acheter Adobe Workfront Fusion ainsi qu’Adobe Workfront pour utiliser les fonctionnalités décrites dans cet article. Workfront Fusion est inclus dans le plan Workfront [!UICONTROL Ultimate].</p>
   <p>Ou</p>
   <p>Exigences de produit héritées : votre entreprise doit acheter Adobe Workfront Fusion ainsi qu’Adobe Workfront pour utiliser les fonctionnalités décrites dans cet article.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Pour connaître le plan, le type de licence ou l’accès dont vous disposez, contactez votre administrateur ou administratrice Workfront.

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

### Coercition de type

Ce document décrit le comportement d’Adobe Workfront Fusion dans des situations où il reçoit des valeurs dans des formats de données attendus et inattendus.

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
   <td> <p>Si la valeur reçue n’est pas du type tableau, Workfront Fusion crée un tableau et le premier (et le seul) élément est la valeur reçue.</p> </td> 
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
   <td> <p>La valeur n’est transmise sans modification que si la page de code est conforme aux attentes. Si la page de code diffère, Workfront Fusion tente de convertir la valeur reçue en page de code demandée. Si cette conversion n’est pas prise en charge, Workfront Fusion renvoie une erreur de validation.</p> </td> 
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
   <td> <p>Workfront Fusion renvoie une erreur de validation.</p> </td> 
  </tr> 
  <tr> 
   <td>Collection </td> 
   <td>Collection </td> 
   <td> <p>La valeur est transmise telle quelle.</p> </td> 
  </tr> 
  <tr> 
   <td>Collection </td> 
   <td>Autre </td> 
   <td> <p>Workfront Fusion renvoie une erreur de validation.</p> </td> 
  </tr> 
  <tr> 
   <td>Date </td> 
   <td>Date </td> 
   <td> <p>La valeur est transmise telle quelle.</p> </td> 
  </tr> 
  <tr> 
   <td>Date </td> 
   <td>Texte </td> 
   <td> <p>Workfront Fusion tentera de convertir le texte en date. Si la conversion échoue, elle renvoie une erreur de validation. La date doit contenir le jour, le mois et l’année. La date peut contenir l’heure et le fuseau horaire. Le fuseau horaire par défaut est basé sur vos paramètres. Exemples :</p> <p><code>2016-06-20T17:26:44.356Z</code> </p> <p><code>2016-06-20 19:26:44 GMT+02:00</code> </p> <p><code>2016-06-20 19:26+0200</code> </p> <p><code>2016-06-20 17:26:44</code> </p> <p><code>2016-06-20</code> </p> <p><code>2016/06/20 17:26:44</code> </p> <p><code>2016/06/20 19:26:44+02:00</code> </p> <p><code>2016/06/20 17:26</code> </p> <p><code>2016/06/20 5:26 PM</code> </p> <p><code>2016/06/20</code> </p> <p><code>06/20/2016 17:26:44</code> </p> <p><code>06/20/2016 19:26:44+02:00</code> </p> <p><code>06/20/2016 17:26</code> </p> <p><code>06/20/2016 5:26 PM</code> </p> <p><code>06/20/2016</code> </p> <p><code>20.6.2016 17:26:44</code> </p> <p><code>20.6.2016 19:26:44+02:00</code> </p> <p><code>20.6.2016 17:26</code> </p> <p><code>20.6.2016</code> </p> </td> 
  </tr> 
  <tr> 
   <td>Date </td> 
   <td>Autre </td> 
   <td> <p>Workfront Fusion renvoie une erreur de validation.</p> </td> 
  </tr> 
  <tr> 
   <td>Nombre </td> 
   <td>Nombre </td> 
   <td> <p>La valeur est transmise telle quelle.</p> </td> 
  </tr> 
  <tr> 
   <td>Nombre </td> 
   <td>Texte </td> 
   <td> <p>Workfront Fusion tentera de convertir le texte en nombre. Si la conversion échoue, elle renvoie une erreur de validation.</p> </td> 
  </tr> 
  <tr> 
   <td>Nombre </td> 
   <td>Autre </td> 
   <td> <p>Workfront Fusion renvoie une erreur de validation.</p> </td> 
  </tr> 
  <tr> 
   <td>Texte </td> 
   <td>Texte </td> 
   <td> <p>La valeur est transmise telle quelle.</p> </td> 
  </tr> 
  <tr> 
   <td>Texte </td> 
   <td>Tableau </td> 
   <td> <p>Si le tableau donné prend en charge la conversion en texte, la valeur est convertie. Dans le cas contraire, Workfront Fusion renverra une erreur de validation.</p> </td> 
  </tr> 
  <tr> 
   <td>Texte </td> 
   <td>booléen </td> 
   <td> <p>La valeur est convertie en texte (vrai/faux).</p> </td> 
  </tr> 
  <tr> 
   <td>Texte </td> 
   <td>Buffer </td> 
   <td> <p>Si le codage de texte est spécifié pour les données binaires, la valeur est convertie en texte. Dans le cas contraire, Workfront Fusion renverra une erreur de validation.</p> </td> 
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
   <td> <p>Workfront Fusion renvoie une erreur de validation.</p> </td> 
  </tr> 
  <tr> 
   <td>heure </td> 
   <td>heure </td> 
   <td> <p>La valeur est transmise telle quelle.</p> </td> 
  </tr> 
  <tr> 
   <td>heure </td> 
   <td>Texte </td> 
   <td> <p>Workfront Fusion tentera de convertir l’heure au format <code>hours:minutes:seconds</code>. Si la conversion échoue, elle renvoie une erreur de validation.</p> </td> 
  </tr> 
  <tr> 
   <td>heure </td> 
   <td>Autre </td> 
   <td> <p>Workfront Fusion renvoie une erreur de validation.</p> </td> 
  </tr> 
 </tbody> 
</table>
