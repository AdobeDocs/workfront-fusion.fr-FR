---
title: HTTP > Effectuer une requête d’autorisation de base
description: Adobe Workfront Fusion nécessite une licence Adobe Workfront Fusion en plus d’une licence Adobe Workfront.
author: Becky
feature: Workfront Fusion
exl-id: e544768e-7023-473f-8d51-631b04183743
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 78%

---

# [!UICONTROL HTTP] > [!UICONTROL Effectuer une demande d’autorisation de base] module

Ce module [!DNL Adobe Workfront Fusion] permet de configurer une requête HTTP avec une autorisation de base HTTP et de l’envoyer à un serveur. La réponse HTTP reçue est alors contenue dans le lot de sortie.

>[!NOTE]
>
>Si vous vous connectez à un produit Adobe qui n’a pas encore de connecteur dédié, il est recommandé d’utiliser le module Adobe Authenticator.
>
>Pour plus d’informations, voir [Module Adobe Authenticator](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md).

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

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## [!UICONTROL HTTP] > [!UICONTROL Effectuer une demande d’autorisation de base] configuration du module

Lorsque vous configurez le module [!UICONTROL HTTP] > [!UICONTROL Effectuer une demande d’autorisation de base], [!DNL Adobe Workfront Fusion] affiche les champs répertoriés ci-dessous. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mapper des informations d’un module à l’autre dans  [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Credentials]</td> 
   <td> <p>Sélectionnez la clé contenant vos informations d’authentification de base ou cliquez sur <strong>[!UICONTROL Add]</strong> pour ajouter vos informations d’identification à une nouvelle clé. </p> <p>Note : vous pouvez ajouter d’autres informations d’identification pour basculer facilement entre chaque connexion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Evaluate all states as errors (except for 2xx and 3xx )] </td> 
   <td> <p>Utilisez cette option pour configurer la gestion des erreurs.</p> <p>Pour plus d’informations, voir <a href="/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md" class="MCXref xref"> Gestion des erreurs </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>Saisissez l’URL à laquelle vous souhaitez envoyer une requête, par exemple un point d’entrée API, un site web, etc.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers] </td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard. Par exemple, <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Saisissez les paires clé-valeur de requête souhaitées.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Body type]</p> </td> 
   <td> <p>Le corps du message HTTP est constitué des octets de données transmis dans un message de transaction HTTP, immédiatement après les en-têtes, le cas échéant.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p>Le type de corps Raw convient généralement à la plupart des requêtes HTTP, même dans les cas où la documentation de développement ne spécifie pas les données à envoyer.</p> <p>Spécifiez un formulaire d’analyse des données dans le champ [!UICONTROL Content type].</p> <p>Peu importe le type de contenu sélectionné, les données peuvent être saisies dans n’importe quel format requis ou indiqué par la documentation de développement.</p> </li> 
     <li> <p><strong>[!UICONTROL Application/x-www-form-urlencoded]</strong> </p> <p>Ce type de corps est destiné à [!UICONTROL POST] des données en utilisant <code>application/x-www-form-urlencoded</code>.</p> <p>Pour <code>[!UICONTROL application/x-www-form-urlencoded]</code>, le corps du message HTTP envoyé au serveur est essentiellement une chaîne de requête. Les clés et les valeurs sont encodées dans des paires clé-valeur séparées par <code>&amp;</code> et avec un <code>=</code> entre la clé et la valeur. </p> <p>Pour les données binaires, utilisez plutôt <code>[!UICONTROL multipart/form-data]</code>.</p> <p>Pour chaque paire clé-valeur à ajouter, dans le champ Champs , cliquez sur <b>Ajouter un élément</b> et saisissez la clé et la valeur.</p>
      <div class="example" data-mc-autonum="<b>Example: </b>">
       <span class="autonumber"><span><b>Exemple :</b></span></span> 
       <p>Exemple du format de requête HTTP obtenu :</p> 
       <p><code>field1=value1&amp;field2=value2</code> </p> 
      </div> </li> 
     <li> <p><strong>[!UICONTROL Multipart/form-data]</strong> </p> <p>[!UICONTROL Multipart/form-data] est une requête HTTP à plusieurs parties utilisée pour envoyer des fichiers et des données. Elle est fréquemment utilisée pour charger des fichiers sur le serveur.</p> <p>Ajouter des champs à envoyer dans la requête. Chaque champ doit contenir une paire clé-valeur.</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Text]</strong> </p> <p>Saisissez la clé et la valeur à envoyer dans le corps de la requête.</p> </li> 
       <li> <p><strong>[!UICONTROL File]</strong> </p> <p>Saisissez la clé et indiquez le fichier source à envoyer dans le corps de la requête. Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Parse response]</p> </td> 
   <td> <p>Activez cette option pour analyser automatiquement les réponses et convertir les réponses JSON et XML afin que vous n’ayez pas à utiliser les modules [!UICONTROL JSON] &gt; [!UICONTROL Parse JSON] ou [!UICONTROL XML] &gt; [!UICONTROL Parse XML].</p> <p>Avant de pouvoir utiliser du contenu JSON ou XML analysé, exécutez le module une fois manuellement afin qu’il puisse reconnaître le contenu de la réponse et vous permettre de le mapper dans les modules suivants.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timeout] </td> 
   <td> <p>Spécifiez le délai d’expiration de la requête en secondes (1 à 300). La valeur par défaut est de 40 secondes.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Share cookies with other HTTP modules]</td> 
   <td> <p> Activez cette option pour partager les cookies du serveur avec tous les modules HTTP de votre scénario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Self-signed certificate]</td> 
   <td> <p>Pour ajouter un certificat auto-signé :</p>
          <ol>
            <li value="1">
              <p>Cliquez sur <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li value="2">
              <p>Sélectionnez le type de fichier que vous extrayez.</p>
            </li>
            <li value="3">
              <p>Sélectionnez le fichier contenant le certificat ou .</p>
            </li>
            <li value="4">
              <p>Saisissez le mot de passe du fichier.</p>
            </li>
            <li value="5">
              <p>Cliquez sur <b>[!UICONTROL Save]</b> pour extraire le fichier et revenir à la configuration du module.</p>
            </li>
          </ol>
</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reject connections that are using unverified (self-signed) certificates] </td> 
   <td> <p>Activez cette option pour rejeter les connexions qui utilisent des certificats TLS non vérifiés.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Follow redirect]</td> 
   <td> <p> Activez cette option pour suivre les redirections d’URL avec les réponses 3xx.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Follow all redirects] </td> 
   <td> <p>Activez cette option pour suivre les redirections d’URL avec tous les codes de réponse.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Disable serialization of multiple same query string keys as arrays]</p> </td> 
   <td> <p>Par défaut, [!DNL Workfront Fusion] traite les valeurs multiples de la même clé de paramètre de chaîne de requête URL comme des tableaux. Par exemple, <code>www.test.com?foo=bar&amp;foo=baz</code> sera converti en <code>www.test.com?foo[0]=bar&amp;foo[1]=baz</code>. Activez cette option pour désactiver cette fonction. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Request compressed content]</td> 
   <td> <p> Activez cette option pour demander une version compressée du site web.</p> <p>Ajoute un en-tête <code>[!UICONTROL Accept-Encoding]</code> pour demander un contenu compressé.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Use Mutual TLS]</td> 
   <td> <p>Activez cette option pour utiliser le protocole TLS mutuel dans la requête HTTP.</p> <p>Pour plus d’informations sur le protocole Mutual TLS, voir <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/use-mtls-in-http-modules.md" class="MCXref xref">Utilisation du protocole Mutual TLS dans les modules HTTP</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>
