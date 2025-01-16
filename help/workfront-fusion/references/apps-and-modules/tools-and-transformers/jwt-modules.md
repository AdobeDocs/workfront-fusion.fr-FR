---
title: Modules JWT
description: L’application  [!DNL Adobe Workfront Fusion] [!UICONTROL JWT] fournit un module qui crée des jetons JWT en fonction de l’algorithme fourni.
author: Becky
feature: Workfront Fusion
exl-id: 380f60db-b2ec-411a-86ee-0d5699f19b41
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 13%

---

# Module [!UICONTROL JWT]

L’application [!DNL Adobe Workfront Fusion] [!UICONTROL JWT] fournit un module qui crée des jetons JWT en fonction de l’algorithme fourni.

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
   <p>Ancienne exigence de licence : [!UICONTROL [!DNL Workfront Fusion] pour l’automatisation et l’intégration du travail], [!UICONTROL [!DNL Workfront Fusion] pour l’automatisation du travail]</p>
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
