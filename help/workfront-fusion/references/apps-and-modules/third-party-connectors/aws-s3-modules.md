---
title: Modules AWS S3
description: Les modules S3 d’[!DNL Adobe Workfront Fusion AWS] permettent d’effectuer des opérations sur vos compartiments S3.
author: Becky
feature: Workfront Fusion
exl-id: 6b2d9dd5-0b33-4297-aea0-aba26072b26a
TQID: 'https://experienceleague.adobe.com/FDkre6osF2kT7Kz-5VGradQLa7GPSJ6MHPH9-FgM-ag'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
source-git-commit: 7c25013f7a94000651e8331199ad985d40651ae3
workflow-type: tm+mt
source-wordcount: '2637'
ht-degree: 48%
---
# Modules AWS S3

Les modules S3 d’[!DNL Adobe Workfront Fusion AWS] permettent d’effectuer des opérations sur vos compartiments S3.

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
   <td role="rowheader">Licence Adobe Workfront Fusion</td> 
   <td>
   <p>Basé sur les opérations : disponible pour les organisations disposant de licences basées sur les opérations</p>
   <p>Basé sur un connecteur (hérité) : Workfront Fusion pour l’automatisation et l’intégration du travail </p>
   </td> 
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

Pour plus d’informations sur les licences Adobe Workfront Fusion, consultez [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Conditions préalables

Pour utiliser les modules [!UICONTROL AWS S3], vous devez disposer d’un compte [!DNL Amazon Web Service].

## Informations sur l’API S3 d’AWS

Le connecteur AWS S3 utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td><pre><code>https://s3.&#123;&#123;parameters.region&#125;&#125;.amazonaws.com</code></pre></td> 
  </tr>
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.5.21</td> 
  </tr>
 </tbody> 
 </table>

## Connecter [!DNL AWS] à Workfront Fusion {#connect-aws-to-workfront-fusion}

* [Connexion d’AWS à Workfront Fusion à l’aide d’une connexion fédérée](#connect-aws-to-workfront-fusion-using-a-federated-connection)
* [Connexion d’AWS à Workfront Fusion à l’aide d’un utilisateur d’API](#connect-aws-to-workfront-fusion-using-an-api-user)

### Connexion d’AWS à Workfront Fusion à l’aide d’une connexion fédérée

+++ Développez pour afficher les instructions relatives à ce type de connexion.

* [Prérequis pour connecter AWS à Workfront Fusion à l’aide d’une connexion fédérée](#prerequisites-to-connecting-aws-to-workfront-fusion-using-a-federated-connection)
* [Ajout de Workfront Fusion comme fournisseur d’identité dans AWS](#add-workfront-fusion-as-an-identity-provider-in-aws)
* [Créer le rôle IAM](#create-the-iam-role)
* [Création de la connexion dans Workfront Fusion](#create-the-connection-in-workfront-fusion)
* [Ajouter la connexion à la politique d’approbation du rôle](#add-the-connection-to-the-roles-trust-policy)
* [Vérifier la connexion](#verify-the-connection)
* [Dépannage](#troubleshooting)

Une connexion fédérée permet à Workfront Fusion d’accéder à votre compte AWS sans que vous ne créiez un utilisateur IAM ou stockiez une clé d’accès dans Fusion.
Au lieu de cela, vous enregistrez Workfront Fusion en tant que fournisseur d’identité approuvé dans votre compte AWS et vous configurez la connexion Fusion unique autorisée à utiliser un rôle IAM particulier. Lorsque la connexion s’exécute, Fusion présente une preuve d’identité de courte durée et AWS renvoie des informations d’identification temporaires qui expirent d’elles-mêmes. Aucune clé de longue durée n’est jamais créée, stockée ou pivotée.

>[!NOTE]
>
>La configuration de cette connexion nécessite deux visites sur la console AWS. Créez d’abord le rôle, puis la connexion dans Workfront Fusion, et revenez ensuite à AWS pour terminer la politique d’approbation. Cela est dû au fait qu’une partie de la politique d’approbation identifie une connexion spécifique et que cet identifiant n’existe pas tant que la connexion n’a pas été créée.

#### Prérequis pour connecter AWS à Workfront Fusion à l’aide d’une connexion fédérée

Pour créer cette connexion, vous avez besoin des éléments suivants :

* Autorisation de créer un fournisseur d’identité et de créer et modifier des rôles dans l’IAM AWS. Cela signifie généralement la politique ou l’équivalent. Si vous ne disposez pas de cet accès, demandez à quelqu’un sur votre cloud ou
équipe de sécurité pour suivre les étapes d’AWS.
* Possibilité de créer des connexions dans Workfront Fusion.


#### Ajout de Workfront Fusion comme fournisseur d’identité dans AWS

Cette étape indique à AWS que les jetons émis par Workfront Fusion peuvent être approuvés. Vous effectuez cette opération une fois par compte AWS. Si un membre de votre organisation a déjà ajouté ce fournisseur, passez à [Créer le rôle IAM](#create-the-iam-role).

1. Connectez-vous à la console AWS et accédez à **IAM** > **Fournisseurs d’identité**.
1. Sélectionnez **Ajouter un fournisseur**.
1. Pour le type de fournisseur , sélectionnez **OpenID Connect**.
1. Dans l’URL du fournisseur, saisissez ce qui suit, puis sélectionnez **Obtenir l’empreinte numérique** :

   ```
   https://oidc.automations.adobe.com
   ```

1. Dans Audience, saisissez ce qui suit :

   ```
   sts.amazonaws.com
   ```

1. Sélectionnez **Ajouter un fournisseur**.
1. Passez à [ Créer le rôle IAM ](#create-the-iam-role).

#### Créer le rôle IAM

Le rôle définit ce que la connexion est autorisée à faire dans votre compte AWS. Vous créez un rôle par connexion, de sorte que l’accès à chaque connexion puisse être accordé et révoqué indépendamment.

1. Dans IAM, accédez à **Rôles** et sélectionnez **Créer un rôle**.
1. Pour Type d&#39;entité de confiance, sélectionnez **Identité web**.
1. Dans Fournisseur d’identités, sélectionnez `oidc.automations.adobe.com`.
1. Dans Audience, sélectionnez `sts.amazonaws.com`.
1. Sélectionnez **Suivant**, puis joignez les politiques d’autorisation dont cette connexion a besoin.
Accordez uniquement les autorisations que la connexion utilise réellement. Par exemple, une connexion qui ne lit que depuis
un compartiment n’a pas besoin d’être `AmazonS3FullAccess`.
1. Donnez au rôle un nom clair et reconnaissable. Par exemple, `WorkfrontFusionFederatedConnection`.
1. Sélectionnez **Créer un rôle**.
1. Ouvrez le rôle que vous venez de créer et copiez son ARN depuis la zone Résumé . Voici à quoi cela ressemble : `arn:aws:iam::123456789012:role/WorkfrontFusionFederatedConnection`

1. Passez à [Création de la connexion dans Workfront Fusion](#create-the-connection-in-workfront-fusion).

#### Création de la connexion dans Workfront Fusion

1. Dans l’écran de configuration de la connexion du module, sélectionnez le type de connexion fédérée .
1. Saisissez le rôle ARN que vous avez copié dans [Créer le rôle IAM](#create-the-iam-role).
1. Sélectionnez **Créer**.
Workfront Fusion affiche trois valeurs. Vous les utiliserez dans la procédure suivante.

<table>
  <tr>
    <td>Émetteur</td>
    <td>Toujours <code>https://oidc.automations.adobe.com</code>. Cela correspond au fournisseur d’identité que vous avez ajouté dans AWS.</td>
  </tr>
  <tr>
    <td>Objet</td>
    <td>Identifie cette connexion. On dirait <code>fusion:6e5b1c2a345bd8d1ed98b6b4f1459818:28964</code>. Il est différent pour chaque connexion que vous créez.</td>
  </tr>
  <tr>
    <td>Audience</td>
    <td>Toujours <code>sts.amazonaws.com</code>.</td>
  </tr>
</table>

1. Laissez ce panneau ouvert et copiez la valeur Objet .

   >[!NOTE]
   >
   >Ne fermez pas le panneau et ne sélectionnez pas Annuler. La connexion n&#39;est pas terminée tant que vous n&#39;avez pas terminé les procédures restantes. Si vous fermez le panneau, vous devez supprimer la connexion et recommencer, car une nouvelle connexion reçoit un nouvel objet.

1. Passez à [Ajouter la connexion à la politique d’approbation du rôle](#add-the-connection-to-the-roles-trust-policy).

#### Ajouter la connexion à la politique d’approbation du rôle

Tant que vous n’avez pas terminé cette procédure, le rôle n’approuve pas Workfront Fusion en général, mais ne permet pas encore à cette connexion spécifique de l’utiliser.

1. Dans un nouvel onglet du navigateur, revenez à la console AWS et ouvrez le rôle que vous avez créé.
1. Sélectionnez l’onglet **Relations d’approbation** puis sélectionnez **Modifier la politique d’approbation**.
1. Remplacez la politique par ce qui suit, en substituant vos propres valeurs :

   * Remplacez `123456789012` par votre ID de compte AWS
   * Remplacez la valeur `sub` par l’objet que vous avez copié à partir de Workfront Fusion.


   ```
   {
     "Version": "2012-10-17",
     "Statement": [
       {
         "Effect": "Allow", 
         "Principal": {
           "Federated": "arn:aws:iam::123456789012:oidc-provider/oidc.automations.adobe.com"
       },
       "Action": "sts:AssumeRoleWithWebIdentity", "Condition": {
        "StringEquals": {
          "oidc.automations.adobe.com:sub": "fusion:6e5b1c2a345bd8d1ed98b6b4f1459818:28964", 
          "oidc.automations.adobe.com:aud": "sts.amazonaws.com"
        }
       }
      }
    ]
   }
   ```

1. Sélectionnez **Mettre à jour la politique**.
1. Passez à [Vérifier la connexion](#verify-the-connection).

>[!TIP]
>
>Pour permettre à plusieurs connexions d’utiliser le même rôle, répertoriez les objets sous la forme d’un tableau. AWS permet d’utiliser le rôle si le jeton correspond à une valeur de la liste :
>
>```
>"oidc.automations.adobe.com:sub": [ "fusion:6e5b1c2a345bd8d1ed98b6b4f1459818:28964", "fusion:6e5b1c2a345bd8d1ed98b6b4f1459818:29011"
>]
>```
>
>Ne remplacez pas la sous-valeur par un caractère générique. Cela permet à toute connexion de votre organisation d’utiliser le rôle, y compris les connexions créées ultérieurement par d’autres personnes


#### Vérifier la connexion

1. Revenez à l’onglet du navigateur de Workfront Fusion, où le panneau de connexion est toujours ouvert.
1. Cliquer sur **Enregistrer**.

   Workfront Fusion contacte AWS, qui vérifie la politique d’approbation et renvoie les informations d’identification temporaires. Si tout est configuré correctement, la connexion est validée avec succès et vous pouvez poursuivre la configuration du module.
   Si la vérification échoue, le panneau reste ouvert et affiche l’erreur. Corrigez le problème dans AWS et sélectionnez à nouveau Enregistrer. Vous n’avez pas besoin de recréer la connexion et l’objet ne change pas.

À partir de maintenant, la connexion renouvelle ses propres informations d’identification. Il n’y a aucune clé à faire pivoter et rien n’expire que vous devez gérer.

#### Dépannage


<table>
  <tr>
    <th>Erreur</th>
    <th>Signification</th>
    <th>Éléments à vérifier</th>
  </tr>
  <tr>
    <td>InvalidIdentityToken</td>
    <td>AWS n’a pas pu faire correspondre le jeton à un fournisseur d’identité enregistré.</td>
    <td>Vérifiez que vous avez ajouté le fournisseur d’identité décrit dans Ajout de Workfront Fusion en tant que fournisseur d’identité dans AWS et que son URL est exactement https://oidc.automations.adobe.com, sans barre oblique.</td>
  </tr>
  <tr>
    <td>Accès refusé lors de l’attribution du rôle</td>
    <td>Le fournisseur d'identité est enregistré, mais la stratégie d'approbation ne correspond pas à cette connexion.</td>
    <td>Vérifiez que la sous-valeur dans la politique d’approbation est caractère pour caractère identique à l’objet affiché dans Workfront Fusion et que aud est sts.amazonaws.com. Un objet copié à partir d’une autre connexion est la cause la plus courante.</td>
  </tr>
  <tr>
    <td>La connexion fonctionne, puis échoue ultérieurement</td>
    <td> </td>
    <td>Vérifiez si les politiques d’autorisation du rôle ont changé ou si le rôle a été supprimé et recréé. La recréation d’un rôle ne modifie pas son ARN, mais elle réinitialise sa politique d’approbation.</td>
  </tr>
</table>

+++

### Connexion d’AWS à Workfront Fusion à l’aide d’un utilisateur d’API

+++ Développez pour afficher les instructions relatives à ce type de connexion.

Pour connecter [!DNL AWS S3] à Workfront Fusion, vous devez connecter votre compte [!DNL AWS] à Workfront Fusion. Pour ce faire, vous devez d’abord créer un utilisateur ou une utilisatrice d’API dans [!DNL AWS] [!UICONTROL IAM].

1. Connectez-vous à votre compte [!DNL AWS] [!UICONTROL IAM].
1. Accédez à **[!UICONTROL Gestion des identités et des accès]** > **[!UICONTROL Gestion des accès]** > **[!UICONTROL Utilisateurs et utilisatrices]**.

1. Cliquez sur **[!UICONTROL Ajouter un utilisateur ou une utilisatrice]**.
1. Saisissez le nom du nouvel utilisateur ou de la nouvelle utilisatrice et sélectionnez l’option **[!UICONTROL Accès programmatique]** dans la section [!UICONTROL Type d’accès].
1. Cliquez sur **[!UICONTROL Associer directement des politiques existantes]**, puis recherchez **[!UICONTROL AmazonS3FullAccess]** dans la barre de recherche. Cliquez dessus lorsqu’il apparaît, puis cliquez sur **[!UICONTROL Suivant]**.

1. Passez aux autres écrans de la boîte de dialogue, puis cliquez sur **[!UICONTROL Créer un utilisateur ou une utilisatrice]**.
1. Copiez l’**[!UICONTROL ID de clé d’accès]** et la **[!UICONTROL Clé d’accès secrète]** fournis.

1. Accédez à Workfront Fusion et ouvrez la boîte de dialogue **[!UICONTROL Créer une connexion]** du module de [!DNL AWS S3].
1. Saisissez l’[!UICONTROL ID de clé d’accès] et la [!UICONTROL Clé d’accès secrète] de l’étape 7 dans les champs respectifs, puis cliquez sur **[!UICONTROL Continuer]** pour établir la connexion.

La connexion a été établie. Vous pouvez poursuivre la configuration du module.

+++

## Modules [!DNL AWS S3] et leurs champs

* [Actions](#actions)
* [Recherches](#searches)

Lorsque vous configurez les modules [!DNL AWS S3], Workfront Fusion affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL AWS S3] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, consultez [Mappage d’informations d’un module à l’autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Bouton (bascule) de mappage](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Actions](#actions)
* [Recherches](#searches)

### Actions

* [[!UICONTROL Créer un compartiment]](#create-bucket)
* [[!UICONTROL Obtenir un fichier]](#get-file)
* [[!UICONTROL Effectuer un appel API]](#make-an-api-call)
* [[!UICONTROL Charger un fichier]](#upload-file)

#### [!UICONTROL Créer un compartiment]

Ce module d’action crée un compartiment dans AWS.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL AWS] à Workfront Fusion, consultez <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connecter [!DNL AWS] à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Saisissez le nom du nouveau compartiment.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Sélectionnez votre point d’entrée régional. Pour plus d’informations, voir <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">points d’entrée régionaux</a> dans la documentation d’AWS.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obtenir un fichier]

Ce module d’action télécharge un fichier à partir d’un compartiment.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL AWS] à Workfront Fusion, consultez <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connecter [!DNL AWS] à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Sélectionnez votre point d’entrée régional. Pour plus d’informations, voir <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">points d’entrée régionaux</a> dans la documentation [!DNL AWS].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bucket] </td> 
   <td> <p>Sélectionnez le compartiment à partir duquel vous souhaitez télécharger le fichier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Path]</p> </td> 
   <td> <p>Saisissez le chemin d’accès au fichier. Exemple : <code>/photos/2019/February/image023.jpg</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Effectuer un appel API]

Ce module d’action effectue un appel personnalisé à l’API AWS S3.

Pour consulter une discussion détaillée de l’API [!DNL Amazon S3], voir la section Présentation de l’API [[!DNL Amazon S3] [!UICONTROL  REST]](https://docs.aws.amazon.com/AmazonS3/latest/API/Welcome.html).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL AWS] à Workfront Fusion, consultez <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connecter [!DNL AWS] à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Region] </td> 
   <td> <p>Sélectionnez votre point d’entrée régional. Pour plus d’informations, voir <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">points d’entrée régionaux</a> dans la documentation [!DNL AWS].</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL URL]</td> 
   <td> <p>Saisissez une URL hôte. Le chemin doit être relatif à <code> https://s3.&lt;selected-region>.amazonaws.com/</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Method]</td> 
   <td> <p>Sélectionnez la méthode de requête [!UICONTROL HTTP] dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, consultez <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref"> méthodes de requête HTTP[!UICONTROL] dans Adobe Workfront Fusion</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez un en-tête de requête. Pour chaque en-tête à ajouter, cliquez sur <b>Ajouter un élément</b> et saisissez l’en-tête. Vous pouvez utiliser les en-têtes de requête courants qui suivent. Pour obtenir davantage d’en-têtes de requête, voir la documentation de l’API <a href="https://docs.aws.amazon.com/AmazonS3/latest/API/RESTCommonRequestHeaders.html">[!DNL AWS S3]</a>.</p> <p>Workfront Fusion ajoute automatiquement des en-têtes d’autorisation.</p> 
    <table style="table-layout:auto">
     <col> 
     <col> 
     <thead> 
      <tr> 
       <th>Nom de l’en-tête</th> 
       <th> <p> Description</p> </th> 
      </tr> 
     </thead> 
     <tbody> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Content-Length]</p> </td> 
       <td> <p>Longueur du message (sans en-têtes) conformément à la norme RFC 2616. Cet en-tête est obligatoire pour les opérations et les requêtes [!UICONTROL PUT] qui chargent du code XML, telles que la journalisation et les listes de contrôle d’accès.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Content-Type]</p> </td> 
       <td> <p>Type de contenu de la ressource, au cas où le contenu de la requête se trouverait dans le corps. Exemple : <code>text/plain</code>.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Content-MD5]</p> </td> 
       <td> <p>Synthèse MD5 128 bits encodée en base64 du message (sans en-têtes), selon la norme RFC 1864. Cet en-tête peut être utilisé comme contrôle d’intégrité du message pour vérifier que les données sont les mêmes que celles envoyées initialement. Bien que cela soit facultatif, nous vous recommandons d’utiliser le mécanisme [!UICONTROL Content-MD5] comme contrôle d’intégrité de bout en bout. Pour plus d’informations sur l’authentification des requêtes [!UICONTROL REST], consultez <a href="https://docs.aws.amazon.com/AmazonS3/latest/dev/RESTAuthentication.html?r=1821">Signature et authentification de requêtes REST</a> dans la documentation d’AWS.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Date]</p> </td> 
       <td> <p>Date et heure actuelles en fonction du demandeur ou de la demandeuse. Exemple : <code>Wed, 01 Mar 2006 12:00:00 GMT</code>. Lorsque vous spécifiez l’en-tête <code>Authorization </code>, vous devez spécifier l’en-tête <code>x-amz-date</code> ou l’en-tête <code>Date </code>.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Expect]</p> </td> 
       <td> <p>Lorsque votre application utilise [!UICONTROL 100-continue], elle n’envoie pas le corps de la requête tant qu’elle n’a pas reçu d’accusé de réception. Si le message est refusé en raison des en-têtes, le corps du message n’est pas envoyé. Cet en-tête ne peut être utilisé que si vous envoyez un corps.</p> <p>Valeurs valides : [!UICONTROL 100-continue]</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL Host]</p> </td> 
       <td> <p>Pour les requêtes path-style, la valeur est <code>s3.amazonaws.com</code>. Pour les requêtes virtual-style, la valeur est <code>BucketName.s3.amazonaws.com</code>. Pour plus d’informations, consultez <a href="https://docs.aws.amazon.com/AmazonS3/latest/dev/VirtualHosting.html">Hébergement virtuel</a> dans la documentation d’AWS.</p> <p>Cet en-tête est obligatoire pour HTTP 1.1 (la plupart des kits d’outils ajoutent cet en-tête automatiquement). Il est facultatif pour les requêtes HTTP/1.0.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL x-amz-content-sha256]</p> </td> 
       <td> <p>Lorsque vous utilisez la version 4 de la signature pour authentifier la requête, cet en-tête fournit un hachage du payload de la requête. Lors du chargement d’un objet en blocs, définissez la valeur sur <code>STREAMING-AWS4-HMAC-SHA256-PAYLOAD</code> pour indiquer que la signature couvre uniquement les en-têtes et qu’il n’y a aucun payload. Pour plus d’informations, voir <a href="https://docs.aws.amazon.com/AmazonS3/latest/API/sigv4-streaming.html">Calculs de signature pour l’en-tête d’autorisation</a> dans la documentation d’AWS.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL x-amz-date]</p> </td> 
       <td> <p>Date et heure actuelles en fonction du demandeur ou de la demandeuse. Exemple : <code>Wed, 01 Mar 2006 12:00:00 GMT</code>. Lorsque vous spécifiez l’en-tête <code>Authorization </code>, vous devez spécifier l’en-tête <code>x-amz-date</code> ou l’en-tête <code>Date </code>. Si vous spécifiez les deux, la valeur spécifiée pour l’en-tête <code>x-amz-date</code> est prioritaire.</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[!UICONTROL x-amz-security-token]</p> </td> 
       <td> <p>Cet en-tête peut être utilisé dans les scénarios suivants :</p> 
        <ul> 
         <li>Fournir des jetons de sécurité pour les opérations [!DNL Amazon DevPay]. Chaque requête qui utilise [!DNL Amazon DevPay] nécessite deux en-têtes <code>x-amz-security-token</code> : un pour le jeton de produit et un pour le jeton d’utilisation. Lorsqu’[!DNL Amazon S3] reçoit une requête authentifiée, il compare la signature calculée à la signature fournie. Les en-têtes à plusieurs valeurs mal formatés, utilisés pour calculer une signature, peuvent entraîner des problèmes d’authentification.</li> 
         <li>Fournissez un jeton de sécurité lors de l’utilisation d’informations d’identification de sécurité temporaires. Lors de l’exécution de requêtes à l’aide d’informations d’identification de sécurité temporaires obtenues auprès d’IAM, vous devez fournir un jeton de sécurité à l’aide de cet en-tête. Pour en savoir plus sur les informations d’identification de sécurité temporaires, voir la section Effectuer des demandes.</li> 
        </ul> <p>Cet en-tête est obligatoire pour les requêtes qui utilisent [!DNL Amazon DevPay] et celles qui sont signées à l’aide d’informations d’identification de sécurité temporaires.</p> </td> 
      </tr> 
     </tbody> 
    </table> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query String]</td> 
   <td> <p>Ajoutez les chaînes de requête souhaitées, telles que des paramètres ou des champs de formulaire.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Body]</td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :   <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre JSON, placez les guillemets à l’extérieur de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Charger un fichier]

Ce module d’action charge un fichier dans un compartiment AWS S3.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL AWS] à Workfront Fusion, consultez <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connecter [!DNL AWS] à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Sélectionnez votre point d’entrée régional. Pour plus d’informations, voir <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">points d’entrée régionaux</a> dans la documentation [!DNL AWS].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Folder] </p> </td> 
   <td> <p>Indiquez le dossier cible vers lequel vous souhaitez charger un fichier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Headers] (facultatif)</p> </td> 
   <td> <p> Pour chaque en-tête à ajouter, cliquez sur <b>Ajouter un élément</b> et saisissez la clé et la valeur de l’en-tête.</p><p> Pour connaître les en-têtes disponibles, voir <a href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutObject.html">PutObject</a> dans la documentation d’AWS.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Recherches

* [[!UICONTROL Répertorier les fichiers]](#list-files)
* [[!UICONTROL Répertorier les dossiers]](#list-folders)

#### [!UICONTROL Répertorier les fichiers]

Renvoie une liste de fichiers à partir d’un emplacement spécifié.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL AWS] à Workfront Fusion, consultez <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connecter [!DNL AWS] à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Sélectionnez votre point d’entrée régional. Pour plus d’informations, voir <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">points d’entrée régionaux</a> dans la documentation [!DNL AWS].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bucket] </td> 
   <td> <p>Sélectionnez le compartiment [!DNL Amazon S3] dans lequel rechercher des fichiers.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Prefix]</p> </td> 
   <td> <p> Entrez un chemin d’accès à un dossier dans lequel rechercher des fichiers, tel que <code>workfrontfusion/work.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Répertorier des dossiers]

Renvoie une liste de dossiers à partir d’un emplacement spécifié.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL AWS] à Workfront Fusion, consultez <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connecter [!DNL AWS] à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Region] </td> 
   <td> <p>Sélectionnez votre point d’entrée régional. Pour plus d’informations, voir <a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">points d’entrée régionaux</a> dans la documentation [!DNL AWS].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bucket] </td> 
   <td> <p>Sélectionnez le compartiment [!DNL Amazon S3] dans lequel rechercher des dossiers.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Prefix] (facultatif)</p> </td> 
   <td> <p> Chemin d’accès à un dossier dans lequel rechercher des dossiers, par exemple <code>workfrontfusion/work.</code></p> </td> 
  </tr> 
 </tbody> 
</table>
