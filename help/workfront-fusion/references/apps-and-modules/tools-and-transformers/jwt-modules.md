---
title: Modules JWT
description: L’application  [!DNL Adobe Workfront Fusion] [!UICONTROL  JWT] fournit un module qui crée des jetons JWT en fonction de l’algorithme fourni.
author: Becky
feature: Workfront Fusion
exl-id: 380f60db-b2ec-411a-86ee-0d5699f19b41
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 9%

---

# Module [!UICONTROL JWT]

L’application [!DNL Adobe Workfront Fusion] [!UICONTROL JWT] fournit un module qui crée des jetons JWT en fonction de l’algorithme fourni.

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
   <p>Aucune exigence de licence Workfront Fusion</p>
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

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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
   <li><b>HS256</b> : HMAC à l’aide de l’algorithme de hachage SHA-256</li>
   <li><b>HS384</b> : HMAC à l’aide de l’algorithme de hachage SHA-384</li>
   <li><b>HS512</b> : HMAC à l’aide de l’algorithme de hachage SHA-512</li>
   <li><b>RS256</b> : RSASSA-PKCS1-v1_5 avec l’algorithme de hachage SHA-256</li>
   <li><b>RS384</b> : RSASSA-PKCS1-v1_5 avec l’algorithme de hachage SHA-384</li>
   <li><b>RS512</b> : RSASSA-PKCS1-v1_5 avec l’algorithme de hachage SHA-512</li>
   <li><b>PS256</b> : RSASSA-PSS utilisant l’algorithme de hachage SHA-256 (uniquement pour le nœud ^6.12.0 OU &gt;=8.0.0)</li>
   <li><b>PS384</b> : RSASSA-PSS utilisant l’algorithme de hachage SHA-384 (uniquement pour le nœud ^6.12.0 OU &gt;=8.0.0)</li>
   <li><b>PS512</b> : RSASSA-PSS utilisant l’algorithme de hachage SHA-512 (uniquement pour le nœud ^6.12.0 OU &gt;=8.0.0)</li>
   <li><b>ES256</b> : ECDSA utilisant la courbe P-256 et l’algorithme de hachage SHA-256</li>
   <li><b>ES384</b> : ECDSA utilisant la courbe P-384 et l’algorithme de hachage SHA-384</li>
   <li><b>ES512</b> : ECDSA utilisant la courbe P-521 et l’algorithme de hachage SHA-512</li>
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
