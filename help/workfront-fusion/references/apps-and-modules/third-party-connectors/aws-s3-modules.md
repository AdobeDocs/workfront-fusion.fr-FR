---
title: Modules AWS S3
description: Les modules S3 d’ [!DNL Adobe Workfront Fusion AWS]  permettent d’effectuer des opérations sur vos compartiments S3.
author: Becky
feature: Workfront Fusion
exl-id: 6b2d9dd5-0b33-4297-aea0-aba26072b26a
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1462'
ht-degree: 68%

---

# Modules AWS S3

Les modules S3 d’[!DNL Adobe Workfront Fusion AWS] permettent d’effectuer des opérations sur vos compartiments S3.

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
   <td>https://s3.{{parameters.region}}.amazonaws.com</td> 
  </tr>
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.5.21</td> 
  </tr>
 </tbody> 
 </table>

## Connecter [!DNL AWS] à Workfront Fusion {#connect-aws-to-workfront-fusion}

Pour connecter [!DNL AWS S3] à Workfront Fusion, vous devez connecter votre compte [!DNL AWS] à Workfront Fusion. Pour ce faire, vous devez d’abord créer un utilisateur ou une utilisatrice d’API dans [!DNL AWS] [!UICONTROL IAM].

1. Connectez-vous à votre compte [!DNL AWS] [!UICONTROL IAM].
1. Accédez à **[!UICONTROL Gestion des identités et des accès]** > **[!UICONTROL Gestion des accès]** > **[!UICONTROL Utilisateurs et utilisatrices]**.

1. Cliquez sur **[!UICONTROL Ajouter un utilisateur ou une utilisatrice]**.
1. Saisissez le nom du nouvel utilisateur ou de la nouvelle utilisatrice et sélectionnez l’option **[!UICONTROL Accès programmatique]** dans la section [!UICONTROL Type d’accès].
1. Cliquez sur **[!UICONTROL Associer directement des politiques existantes]**, puis recherchez **[!UICONTROL AmazonS3FullAccess]** dans la barre de recherche. Cliquez dessus lorsqu’il apparaît, puis cliquez sur **[!UICONTROL Suivant]**.

1. Passez aux autres écrans de la boîte de dialogue, puis cliquez sur **[!UICONTROL Créer un utilisateur ou une utilisatrice]**.
1. Copiez l’**[!UICONTROL ID de clé d’accès]** et la **[!UICONTROL Clé d’accès secrète]** fournis.

1. Accédez à Workfront Fusion et ouvrez la boîte de dialogue [!DNL AWS S3]Créer une connexion **[!UICONTROL du module de]**.
1. Saisissez l’[!UICONTROL ID de clé d’accès] et la [!UICONTROL Clé d’accès secrète] de l’étape 7 dans les champs respectifs, puis cliquez sur **[!UICONTROL Continuer]** pour établir la connexion.

La connexion a été établie. Vous pouvez poursuivre la configuration du module.

## Modules [!DNL AWS S3] et leurs champs

Lorsque vous configurez les modules [!DNL AWS S3], Workfront Fusion affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL AWS S3] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

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
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL AWS] à Workfront Fusion, voir <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL AWS] à Workfront Fusion</a> dans cet article.</p> </td> 
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
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL AWS] à Workfront Fusion, voir <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL AWS] à Workfront Fusion</a> dans cet article.</p> </td> 
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

Pour consulter une discussion détaillée de l’API [!DNL Amazon S3], voir la section Présentation de l’API [[!DNL Amazon S3] [!UICONTROL &#x200B; REST]](https://docs.aws.amazon.com/AmazonS3/latest/API/Welcome.html).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL AWS] à Workfront Fusion, voir <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL AWS] à Workfront Fusion</a> dans cet article.</p> </td> 
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
   <td> <p>Sélectionnez la méthode de requête [!UICONTROL HTTP] dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, consultez <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref"> méthodes de requête HTTP dans Adobe Workfront Fusion</a>.</p> </td> 
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
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL AWS] à Workfront Fusion, voir <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL AWS] à Workfront Fusion</a> dans cet article.</p> </td> 
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
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL AWS] à Workfront Fusion, voir <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL AWS] à Workfront Fusion</a> dans cet article.</p> </td> 
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
   <td> <p>Pour plus d’informations sur la connexion de votre compte [!DNL AWS] à Workfront Fusion, voir <a href="#connect-aws-to-workfront-fusion" class="MCXref xref">Connexion de [!DNL AWS] à Workfront Fusion</a> dans cet article.</p> </td> 
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
