---
title: Modules JWT
description: L’application Adobe Workfront Fusion [!UICONTROL JWT] fournit un module qui crée des jetons JWT en fonction de l’algorithme fourni.
author: Becky
feature: Workfront Fusion
exl-id: 380f60db-b2ec-411a-86ee-0d5699f19b41
TQID: https://experienceleague.adobe.com/90zhDiLzi34ES2MPE-hg26mmSHZ-XQIgZJIFeW4vwy4
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 528
ht-degree: 18%

---

# Module [!UICONTROL JWT]

L’application Adobe Workfront Fusion [!UICONTROL JWT] fournit un module qui crée des jetons JWT en fonction de l’algorithme fourni.

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
   <p>Si votre organisation dispose d’un package Workfront Select ou Prime qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acquérir Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++



## Informations sur l’API JWT

Le connecteur JWT utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
   <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.1.5</td> 
  </tr>
 </tbody> 
 </table>

## Module JWT et ses champs

### Générer le JWT

Ce module génère un jeton JWT en fonction de l’algorithme sélectionné.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Algorithm]</td> 
   <td> <p>Sélectionnez l’algorithme avec lequel vous souhaitez générer le jeton JWT.</p> <ul>
   <li><b></b> : HMAC à l’aide de l’algorithme de hachage SHA-256</li>
   <li><b></b> : HMAC à l’aide de l’algorithme de hachage SHA-384</li>
   <li><b></b> : HMAC à l’aide de l’algorithme de hachage SHA-512</li>
   <li><b></b> : RSASSA-PKCS1-v1_5 avec l’algorithme de hachage SHA-256</li>
   <li><b></b> : RSASSA-PKCS1-v1_5 avec l’algorithme de hachage SHA-384</li>
   <li><b></b> : RSASSA-PKCS1-v1_5 avec l’algorithme de hachage SHA-512</li>
   <li><b></b> : RSASSA-PSS utilisant l’algorithme de hachage SHA-256 (uniquement pour le nœud ^6.12.0 OU &gt;=8.0.0)</li>
   <li><b></b> : RSASSA-PSS utilisant l’algorithme de hachage SHA-384 (uniquement pour le nœud ^6.12.0 OU &gt;=8.0.0)</li>
   <li><b></b> : RSASSA-PSS utilisant l’algorithme de hachage SHA-512 (uniquement pour le nœud ^6.12.0 OU &gt;=8.0.0)</li>
   <li><b></b> : ECDSA utilisant la courbe P-256 et l’algorithme de hachage SHA-256</li>
   <li><b></b> : ECDSA utilisant la courbe P-384 et l’algorithme de hachage SHA-384</li>
   <li><b></b> : ECDSA utilisant la courbe P-521 et l’algorithme de hachage SHA-512</li>
   </ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Payload] </td> 
   <td> <p>Pour chaque élément de payload à ajouter, cliquez sur <b>Ajouter un élément</b> et saisissez la clé et la valeur de l’élément.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Options] </td> 
   <td> <p>Pour chaque élément d’option que vous souhaitez ajouter, cliquez sur <b>Ajouter un élément</b> et saisissez la clé et la valeur de l’élément.</p> <p>Les clés suivantes sont disponibles :
   <ul>
   <li><b>algorithme</b> : (par défaut : RS256)</li>
   <li><b>expiresIn</b> : exprimé en secondes ou sous la forme d’une chaîne décrivant une durée (par exemple, 2 jours, 10 heures, 7 j). Une valeur numérique est interprétée comme un nombre de secondes. Si vous utilisez une chaîne, veillez à indiquer les unités de temps (jours, heures, etc.), sinon l’unité de millisecondes est utilisée par défaut (120 équivaut à 120 ms).</li>
   <li><b>notBefore</b> : exprimé en secondes ou sous la forme d’une chaîne décrivant une période (par exemple, 2 jours, 10 heures, 7 jours). Une valeur numérique est interprétée comme un nombre de secondes. Si vous utilisez une chaîne, veillez à indiquer les unités de temps (jours, heures, etc.), sinon l’unité de millisecondes est utilisée par défaut (120 équivaut à 120 ms).
</li>
   <li><b>audience</b></li>
   <li><b>émetteur</b></li>
   <li><b>jwtid</b></li>
   <li><b>subject</b></li>
   <li><b>noTimestamp</b></li>
   <li><b>en-tête</b></li>
   <li><b>keyid</b></li>
   <li><b>mutatePayload</b> : si <code>true</code>, la fonction sign modifie directement l’objet de payload. Cela s’avère utile si vous avez besoin d’une référence brute à la payload après que des revendications lui ont été appliquées, mais avant qu’elle ne soit codée en jeton.</li>
   <li><b>allowInsecureKeySizes</b> : si <code>true</code>, autorise l’utilisation de clés privées avec un module inférieur à 2048 pour RSA.</li>
   <li><b>allowInvalidAsymmetricKeyTypes</b> : si <code>true</code>, autorise les clés asymétriques qui ne correspondent pas à l’algorithme spécifié. Cette option est destinée uniquement à des fins de rétrocompatibilité et doit être évitée.</li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>
