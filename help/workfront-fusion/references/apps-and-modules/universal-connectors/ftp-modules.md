---
title: Modules FTP
description: Les modules FTP vous permettent de surveiller les modifications de fichier dans un dossier sélectionné, de charger de nouveaux fichiers dans le dossier souhaité et de modifier ou supprimer des fichiers existants qui se trouvent déjà dans un dossier.
author: Becky
feature: Workfront Fusion
exl-id: 1e14f778-ab8c-421f-a4b4-c57be66c7cad
source-git-commit: 54c368d335b30f55cab19595a5b4740dde6013a7
workflow-type: tm+mt
source-wordcount: '1397'
ht-degree: 77%

---

# Modules FTP

Les modules FTP vous permettent de surveiller les modifications de fichier dans un dossier sélectionné, de charger de nouveaux fichiers dans le dossier souhaité et de modifier ou supprimer des fichiers existants qui se trouvent déjà dans un dossier.

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
   <td role="rowheader">Licence Adobe Workfront Fusion</td> 
   <td>
   <p>Basé sur les opérations : aucune exigence de licence Workfront Fusion</p>
   <p>Basé sur un connecteur (hérité) : Workfront Fusion pour l’automatisation et l’intégration du travail </p>
   </td> 
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

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Conditions préalables

Pour utiliser les modules FTP, vous devez disposer d’un compte avec un service FTP.

## Créer une connexion dans un module FTP {#create-a-connection}

1. Dans n’importe quel module FTP, cliquez sur **Ajouter** en regard de la zone de connexion.
1. Remplissez les champs suivants.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Connection name]</td> 
      <td> <p> Saisissez le nom de votre connexion FTP.</p> </td> 
     </tr> 
     <tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Environment]</p> </td> 
      <td> <p>Choisissez si vous utilisez un environnement de production ou hors production.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Type]</p> </td> 
      <td> <p>Choisissez si vous utilisez un compte de service ou un compte personnel.</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Host] </td> 
      <td> <p>Saisissez le nom d’hôte du serveur FTP. Exemple : <code>myftp123.server.com</code></p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Port] </td> 
      <td> <p>Saisissez le numéro de port du serveur FTP. Exemple : <code>21</code></p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL User name] </td> 
      <td> <p>Saisissez le nom d’utilisateur ou d’utilisatrice de votre compte FTP.</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Password] </td> 
      <td> <p>Saisissez le mot de passe de votre compte FTP.</p> </td> 
     </tr> 
     <tr> 
      <td> <p>Utiliser une connexion sécurisée (TLS)</p> </td> 
      <td> <p>Indiquez si vous souhaitez utiliser une connexion sécurisée.</p> <ul><li><p><b>[!UICONTROL No]</b></p> <p>La connexion n’est pas sécurisée.</p></li><li> <p><b> Chiffrement explicite </b> ou <b> Chiffrement implicite </b></p> <p>La connexion est sécurisée à l’aide de SSL.</p> </td> 
     </tr> 
    <tr> 
   <td> <p>[!UICONTROL Reject unauthorized certificates]</p> </td> 
   <td> <p>Activez cette option pour vérifier le certificat du serveur FTP. Si la vérification échoue, la connexion ne sera pas créée. Pour réussir la vérification, le certificat doit répondre à l’un des critères suivants :</p> 
    <ul> 
     <li>être signé par une autorité de certification racine</a></li> 
     <li>être signé par une autorité de certification intermédiaire. Dans ce cas, tous les certificats intermédiaires doivent être installés sur le serveur FTP.</li> 
     <li>être un certificat auto-signé fourni dans le champ [!UICONTROL Self-signed certificate] (voir ci-dessous)</li> </ul>
     <p>Si cette option est désactivée, le certificat du serveur FTP n’est pas vérifié. Nous vous déconseillons vivement de désactiver cette option, car elle rend la connexion non sécurisée et pose un risque sérieux pour la sécurité.</p></td>
    </tr> 
    <tr> 
     <td> <p>[!UICONTROL Self-signed certificate]</p> </td> 
     <td> <p>Cliquez sur le bouton <b>[!UICONTROL Extract]</b> pour ouvrir la boîte de dialogue de chargement.</p> <p>Chargez le certificat pour utiliser le TLS avec votre certificat auto-signé. Workfront Fusion ne conserve ni ne stocke les données que vous fournissez, telles que les fichiers et les mots de passe. Le fichier et le mot de passe sont utilisés uniquement pour extraire le certificat.</p> </td> 
    </tr> 
   </tbody> 
   </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour enregistrer la connexion et revenir au module.

## Modules FTP et leurs champs

* [Déclencheurs](#triggers)
* [Actions](#actions)

### Déclencheurs

#### [!UICONTROL Contrôle des fichiers]

[!UICONTROL Contrôle des fichiers] est le seul module déclencheur pour FTP. Il contrôle le contenu du fichier du dossier sélectionné. Le déclencheur est exécuté lorsqu’un nouveau fichier est ajouté au dossier spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur l’établissement d’une connexion au compte FTP, voir <a href="#create-a-connection" class="MCXref xref">[!UICONTROL Create a connection] dans un module FTP</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Folder]</p> </td> 
   <td> <p>Sélectionnez le dossier que vous souhaitez consulter.</p> <p><b>Remarque :</b> un seul dossier est autorisé par scénario. Les sous-dossiers sont ignorés.</p> <p><b>Conseil :</b> pour observer plusieurs dossiers, créez un scénario distinct pour chacun d’eux.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned files] </td> 
   <td> <p>Définissez le nombre maximal de résultats avec lesquels vous souhaitez que le module fonctionne au cours d’un cycle. Si la valeur est trop élevée, la connexion peut être interrompue du côté du serveur FTP. Workfront Fusion n’a aucune influence sur ce point. Nous vous recommandons de définir une valeur inférieure et de définir une valeur supérieure pour le nombre maximal de cycles ou d’exécuter le scénario plus fréquemment.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [[!UICONTROL Modifier les autorisations]](#change-permissions)
* [[!UICONTROL Créer un dossier]](#create-a-folder)
* [[!UICONTROL Supprimer un fichier]](#delete-a-file)
* [[!UICONTROL Supprimer un dossier]](#delete-a-folder)
* [[!UICONTROL Obtenir un fichier]](#get-a-file)
* [[!UICONTROL Liste des fichiers dans un dossier]](#list-of-files-in-a-folder)
* [[!UICONTROL Déplacer un fichier ou un dossier]](#move-a-file-or-folder)
* [[!UICONTROL Charger] un fichier](#upload-a-file)

#### [!UICONTROL Modifier des autorisations]

Ce module d’action modifie les paramètres d’autorisation d’un fichier ou d’un dossier.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL Connection]</td>
            <td>Pour plus d’informations sur l’établissement d’une connexion au compte FTP, voir <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] dans un module FTP</a> dans cet article.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Change permission settings of]</td>
            <td>
               <p>Indiquez si vous souhaitez modifier les paramètres d’un fichier ou d’un dossier.</p>
            </td>
         </tr>
         <tr>
            <td>[!UICONTROL File path]</td>
            <td>Entrez ou mappez le chemin d’accès au fichier sur le dossier ou le fichier.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Permissions]</td>
            <td>
               <p>Définissez les autorisations de fichier ou de dossier de votre choix. Utilisez les paramètres chmod. Par exemple, saisissez <code>777 </code> ou <code>-rwxrwxrwx</code>.</p>
               <p>Les autorisations doivent correspondre au motif <code> /(.?([r-][w-][x-]){3})|[0-7]{3,4}/</code>.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Créer un dossier]

Ce module d’action crée un dossier.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL Connection]</td>
            <td>Pour plus d’informations sur l’établissement d’une connexion au compte FTP, voir <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] dans un module FTP</a> dans cet article.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Folder path]</td>
            <td>Entrez ou mappez le chemin du fichier sur le nouveau dossier.</td>
         </tr>
         <tr>
            <td>[!UICONTROL New folder name]</td>
            <td>
               <p>Saisissez ou mappez un nom pour le nouveau dossier.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Supprimer un fichier]

Ce module d&#39;action supprime un fichier du dossier spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
            <td>Pour plus d’informations sur l’établissement d’une connexion au compte FTP, voir <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] dans un module FTP</a> dans cet article.</td>
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Sélectionnez le dossier FTP dans lequel vous souhaitez supprimer un fichier.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File name]</td> 
   <td> <p> Saisissez le nom du fichier, y compris son extension de nom de fichier. Exemple : <code>[!DNL image].png</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Supprimer un dossier]

Ce module d’action supprime définitivement le dossier spécifié.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL Connection]</td>
            <td>Pour plus d’informations sur l’établissement d’une connexion au compte FTP, voir <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] dans un module FTP</a> dans cet article.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Folder]</td>
            <td>
               <p>Sélectionnez le dossier FTP dans lequel vous souhaitez supprimer un fichier.</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Obtenir un fichier]

Ce module d’action récupère un fichier du serveur FTP.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur l’établissement d’une connexion au compte FTP, voir <a href="#creating-the-ftp-connection" class="MCXref xref">Créer la connexion FTP</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File path]</td> 
   <td> <p> Saisissez le chemin d’accès au fichier que vous souhaitez obtenir.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Liste des fichiers dans un dossier]

Ce module d’action récupère les informations sur les fichiers et/ou les dossiers.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur l’établissement d’une connexion au compte FTP, voir <a href="#creating-the-ftp-connection" class="MCXref xref">Créer la connexion FTP</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Sélectionnez le dossier FTP dans lequel vous souhaitez effectuer une recherche.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show] </td> 
   <td> <p>Indiquez si vous souhaitez récupérer des informations sur les fichiers ou les dossiers, ou les deux.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>Saisissez le terme de recherche. Si aucun terme de recherche n’est saisi, tous les fichiers ou dossiers du dossier spécifié seront récupérés.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned files]</td> 
   <td> <p>Saisissez ou mappez le nombre maximal de résultats avec lesquels vous souhaitez que le module fonctionne au cours d’un cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Déplacer un fichier ou un dossier]

Ce module d’action déplace un fichier ou un dossier vers un autre emplacement.

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[!UICONTROL Connection]</td>
            <td>Pour plus d’informations sur l’établissement d’une connexion au compte FTP, voir <a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection] dans un module FTP</a> dans cet article.</td>
         </tr>
         <tr>
            <td>[!UICONTROL Old file path]</td>
            <td>
               <p>Saisissez le chemin d’accès à partir duquel vous souhaitez déplacer le fichier. Exemple : <code>/folder1/document.txt</code>.</p>
            </td>
         </tr>
         <tr>
            <td>[!UICONTROL New file path]</td>
            <td>
               <p>Saisissez le chemin vers lequel vous souhaitez déplacer le fichier. Exemple : <code>/folder2/document.txt</code>.</p>
            </td>
         </tr>
   </tbody>
</table>


#### [!UICONTROL Charger un fichier]

Charge un fichier sur le serveur FTP.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td>Pour plus d’informations sur l’établissement d’une connexion au compte FTP, voir <a href="#creating-the-ftp-connection" class="MCXref xref">Créer la connexion FTP</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Sélectionnez le dossier FTP dans lequel vous souhaitez charger le fichier.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file] </td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Append to an already existing file]</td> 
   <td> <p>Si cette option est activée et que le fichier existe déjà sur le serveur FTP, le contenu du fichier est ajouté au fichier existant. Si cette option n’est pas activée, le contenu du fichier est remplacé.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Create folders if don't exist] </td> 
   <td> <p>Si cette option est activée et que le dossier que vous avez entré dans le champ Dossier n’existe pas sur le serveur FTP, le module crée ce dossier.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Dépannage {#troubleshooting}

Si vous rencontrez des problèmes avec l’application FTP pendant la création de la connexion ou l’opération d’un module, essayez d’utiliser l’un des clients FTP les plus courants et d’effectuer la même action (par exemple, créer une connexion ou répertorier des fichiers dans un dossier). avec le client FTP. Si vous rencontrez les mêmes problèmes avec le client FTP, la cause peut être une mauvaise configuration du serveur FTP.
