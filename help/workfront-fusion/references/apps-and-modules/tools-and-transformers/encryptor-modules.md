---
title: Encryptor
description: Les modules Adobe Workfront Fusion Encryptor vous permettent de chiffrer n’importe quelle donnée de texte. Ils prennent actuellement en charge le chiffrement des messages via AES256 et PGP (OpenPGP).
author: Becky
feature: Workfront Fusion
exl-id: 4b119efe-6762-445e-bbc7-c59437fd5060
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 26%

---

# Encryptor

Les modules Adobe Workfront Fusion [!UICONTROL Encryptor] vous permettent de chiffrer n’importe quelle donnée texte. Ils prennent actuellement en charge le chiffrement des messages via AES256 et PGP ([!UICONTROL OpenPGP]).

Ces modules nécessitent une certaine familiarité avec les processus de chiffrement.

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
   <td role="rowheader">Produit</td> 
   <td>
   <p>Si votre entreprise dispose d’un package Select ou Prime Workfront qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acheter Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++



## Chiffrement et déchiffrement des messages à l’aide de PGP

Lors du chiffrement et du déchiffrement via PGP, il est nécessaire d’utiliser un trousseau et de créer une clé privée ou publique (ou les deux).

Pour plus d’informations sur les clés publiques et privées, consultez le glossaire d’[Adobe Workfront Fusion](/help/workfront-fusion/get-started-with-fusion/understand-fusion/fusion-glossary.md).

Pour plus d&#39;informations sur les clés, voir [Clés](/help/workfront-fusion/references/modules/keys.md).

## Modules [!UICONTROL Encryptor] et leurs champs

Lorsque vous configurez les modules [!UICONTROL Encryptor], les champs suivants s’affichent. Un titre en gras dans un module indique un champ obligatoire.

### Déchiffrement AES (avancé)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Key]</td>
        <td>Sélectionnez la clé que le module doit utiliser. Pour créer une clé, cliquez sur <b>Ajouter</b> et saisissez le nom, la clé et le type de codage de la clé.</td>
    </tr>
    <tr>
        <td>Bits</td>
        <td>Choisissez si vous souhaitez que le module utilise un chiffrement de 128 bits ou de 256 bits.</td>
    </tr>
    <tr>
        <td>Encodage d’entrée</td>
        <td>Sélectionnez le type de codage d’entrée à utiliser :
        <ul>
        <li>Binaire</li>
        <li>Base 64</li>
        <li>Hexadécimal</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Données</td>
        <td>Saisissez ou mappez les données à déchiffrer.</td>
    </tr>
    <tr>
        <td>Encodage de sortie</td>
        <td>Sélectionnez le type de codage de sortie à utiliser :
        <ul>
        <li>ASCII</li>
        <li>Binaire</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Algorithme de chiffrement</td>
        <td>Sélectionnez l’algorithme de chiffrement à utiliser :
        <ul>
        <li>CBC</li>
        <li>GCM</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Encodage du vecteur d'initialisation</td>
        <td>Sélectionnez le codage du vecteur d’initialisation à utiliser :
        <ul>
        <li>UTF-8</li>
        <li>Binaire</li>
        <li>Base 64</li>
        <li>Hexadécimal</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Encodage de balise d’authentification</td>
        <td>Sélectionnez le codage de balise d’authentification à utiliser :
        <ul>
        <li>UTF-8</li>
        <li>Binaire</li>
        <li>Base 64</li>
        <li>Hexadécimal</li>
        </ul>
        </td>
    </tr>
</table>

### Déchiffrement AES (simple)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Key]</td>
        <td>Sélectionnez la clé que le module doit utiliser. Pour créer une clé, cliquez sur <b>Ajouter</b> et saisissez le nom, la clé et le type de codage de la clé.</td>
    </tr>
   <tr>
        <td>Encodage d’entrée</td>
        <td>Sélectionnez le type de codage d’entrée à utiliser :
        <ul>
        <li>Binaire</li>
        <li>Base 64</li>
        <li>Hexadécimal</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Données</td>
        <td>Saisissez ou mappez les données à déchiffrer.</td>
    </tr>
    <tr>
        <td>Encodage de sortie</td>
        <td>Sélectionnez le type de codage de sortie à utiliser :
        <ul>
        <li>ASCII</li>
        <li>Binaire</li>
        <li>UTF-8</li>
        </ul>
        </td>
     </tr>
    <tr>
        <td>Clé secret</td>
        <td>Saisissez ou mappez la clé secrète que vous souhaitez utiliser.</td>
    </tr>
</table>

### Chiffrement AES (avancé)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Key]</td>
        <td>Sélectionnez la clé que le module doit utiliser. Pour créer une clé, cliquez sur <b>Ajouter</b> et saisissez le nom, la clé et le type de codage de la clé.</td>
    </tr>
    <tr>
        <td>Bits</td>
        <td>Choisissez si vous souhaitez que le module utilise un chiffrement de 128 bits ou de 256 bits.</td>
    </tr>
    <tr>
        <td>Encodage d’entrée</td>
        <td>Sélectionnez le type de codage d’entrée à utiliser :
        <ul>
        <li>Binaire</li>
        <li>ASCII</li>
        <li>Hexadécimal</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Données</td>
        <td>Saisissez ou mappez les données à chiffrer.</td>
    </tr>
    <tr>
        <td>Encodage de sortie</td>
        <td>Sélectionnez le type de codage de sortie à utiliser :
        <ul>
        <li>ASCII</li>
        <li>Binaire</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Algorithme de chiffrement</td>
        <td>Sélectionnez l’algorithme de chiffrement à utiliser :
        <ul>
        <li>CBC</li>
        <li>GCM</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Encodage du vecteur d'initialisation</td>
        <td>Sélectionnez le codage de balise d’authentification à utiliser :
        <ul>
        <li>UTF-8</li>
        <li>Binaire</li>
        <li>Base 64</li>
        <li>Hexadécimal</li>
        </ul>
        </td>
    </tr>
</table>

### Chiffrement AES (simple)

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Key]</td>
        <td>Sélectionnez la clé que le module doit utiliser. Pour créer une clé, cliquez sur <b>Ajouter</b> et saisissez le nom, la clé et le type de codage de la clé.</td>
    </tr>
   <tr>
        <td>Encodage d’entrée</td>
        <td>Sélectionnez le type de codage d’entrée à utiliser :
        <ul>
        <li>Binaire</li>
        <li>ASCII</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Données</td>
        <td>Saisissez ou mappez les données à chiffrer.</td>
    </tr>
    <tr>
        <td>Encodage de sortie</td>
        <td>Sélectionnez le type de codage de sortie à utiliser :
        <ul>
        <li>Base 64</li>
        <li>Binaire</li>
        <li>Hexadécimal</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Clé secret</td>
        <td>Saisissez ou mappez la clé secrète que vous souhaitez utiliser.</td>
    </tr>
</table>


### Créer une signature numérique

Ce module permet de déchiffrer un message à l’aide de clés publiques et privées.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Private key]</td>
        <td>Sélectionnez la clé privée à utiliser pour cette signature. Pour ajouter une clé privée, cliquez sur <b>Ajouter</b> et saisissez le nom de la clé, son texte et sa phrase secrète.</td>
    </tr>
    <tr>
        <td>Algorithme </td>
        <td>Choisissez si vous souhaitez utiliser RSA-SHA1 ou RSA-SHA256. </td>
    </tr>
   <tr>
        <td>Encodage d’entrée</td>
        <td>Sélectionnez le type de codage d’entrée à utiliser :
        <ul>
        <li>ASCII</li>
        <li>Binaire</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Encodage de sortie</td>
        <td>Sélectionnez le type de codage de sortie à utiliser :
        <ul>
        <li>Base 64</li>
        <li>Hexadécimal</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>Données</td>
        <td>Saisissez ou mappez les données à partir desquelles vous souhaitez créer la signature.</td>
    </tr>
</table>

### Déchiffrer un message PGP

Ce module permet de déchiffrer un message à l’aide de clés publiques et privées.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Private key]</td>
        <td>Sélectionnez la clé privée du destinataire à utiliser pour ce message. Pour ajouter une clé privée, cliquez sur <b>Ajouter</b> et saisissez le nom de la clé, son texte et sa phrase secrète.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Public key]</td>
        <td>Saisissez la clé publique de l’expéditeur ou expéditrice. Cela permet d’authentifier l’identité de l’expéditeur ou de l’expéditrice.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Message]</td>
        <td>Mappez le message que vous souhaitez déchiffrer.</td>
    </tr>
</table>

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
    </table>
