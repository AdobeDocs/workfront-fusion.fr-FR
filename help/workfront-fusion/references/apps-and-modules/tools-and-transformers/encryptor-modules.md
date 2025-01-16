---
title: Encryptor
description: Les modules Adobe Workfront Fusion Encryptor vous permettent de chiffrer n’importe quelle donnée de texte. Ils prennent actuellement en charge le chiffrement des messages via AES256 et PGP (OpenPGP).
author: Becky
feature: Workfront Fusion
exl-id: 4b119efe-6762-445e-bbc7-c59437fd5060
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 73%

---

# Encryptor

[!DNL Adobe Workfront Fusion] modules [!UICONTROL Encryptor] vous permettent de chiffrer n’importe quelle donnée texte. Ils prennent actuellement en charge le chiffrement des messages via AES256 et PGP ([!UICONTROL OpenPGP]).

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

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], consultez la section licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Chiffrement et déchiffrement des messages à l’aide de PGP

Lors du chiffrement et du déchiffrement via PGP, il est nécessaire d’utiliser un trousseau et de créer une clé privée ou publique (ou les deux).

Pour plus d’informations sur les clés publiques et privées, consultez le glossaire d’[Adobe Workfront Fusion](/help/workfront-fusion/get-started-with-fusion/understand-fusion/fusion-glossary.md). <!--For more information on keychains, see [Keys in [!DNL Adobe Workfront Fusion]]().-->

## Modules [!UICONTROL Encryptor] et leurs champs

Lors de la configuration des modules [!UICONTROL Encryptor], les champs suivants s’affichent. Un titre en gras dans un module indique un champ obligatoire.

### Chiffrer un message PGP

Ce module permet de chiffrer un message à l’aide de clés publiques et privées.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Private key]</td>
        <td>Saisissez la clé privée de l’expéditeur ou de l’expéditrice. Cela permet d’authentifier l’identité de l’expéditeur ou de l’expéditrice.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Public key]</td>
        <td>Saisissez la clé publique de la personne destinataire.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Message]</td>
        <td>Saisissez le message que vous souhaitez chiffrer.</td>
    </tr>

### Déchiffrer un message PGP

Ce module permet de déchiffrer un message à l’aide de clés publiques et privées.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Private key]</td>
        <td>Saisissez la clé privée de la personne destinataire.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Public key]</td>
        <td>Saisissez la clé publique de la personne destinataire. Cela permet d’authentifier l’identité de l’expéditeur ou de l’expéditrice.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Message]</td>
        <td>Mappez le message que vous souhaitez déchiffrer.</td>
    </tr>
</table>
