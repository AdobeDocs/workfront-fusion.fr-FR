---
title: Modules SFTP
description: Les modules  [!DNL Adobe Workfront Fusion SFTP]  vous permettent de surveiller les modifications de fichier dans un (sous-)dossier sélectionné, de charger de nouveaux fichiers dans le dossier souhaité, de modifier ou de supprimer des fichiers existants qui se trouvent déjà dans un dossier ou de modifier les autorisations de fichier.
author: Becky
feature: Workfront Fusion
exl-id: bde3cbda-8a19-4d9f-b970-f56d73a1f8dd
source-git-commit: 54c368d335b30f55cab19595a5b4740dde6013a7
workflow-type: tm+mt
source-wordcount: '2222'
ht-degree: 64%

---

# Modules SFTP

Les modules SFTP d’Adobe Workfront Fusion vous permettent de surveiller les modifications apportées aux fichiers d’un dossier ou sous-dossier sélectionné, de charger de nouveaux fichiers dans le dossier souhaité, de modifier ou de supprimer des fichiers existants qui se trouvent déjà dans un dossier ou de modifier les autorisations de fichier.

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

Pour utiliser le protocole SFTP avec Workfront Fusion, il est nécessaire de disposer d’un compte SFTP (tel que l’hébergement web [!DNL GoDaddy]).

## Connexion de SFTP à Workfront Fusion {#connect-sftp-to-workfront-fusion}

Pour connecter votre compte SFTP à Workfront Fusion, vous devez créer une connexion spécifiant l’hôte cible et les informations d’identification SFTP (nom d’utilisateur et mot de passe ou nom d’utilisateur et clé).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection name]</td> 
   <td> <p> Saisissez le nom de votre connexion SFTP.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Environment]</td>
    <td>Indiquez si vous vous connectez à un environnement de production ou hors production.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Type]</td>
    <td>Choisissez si vous souhaitez vous connecter à un compte de service ou à un compte personnel.</td>
  </tr>
  <tr>
   <td role="rowheader"> <p>[!UICONTROL Host]</p> </td> 
   <td> <p>Saisissez le nom d’hôte du serveur SFTP que vous souhaitez connecter.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Port] </td> 
   <td> <p>Saisissez le port du serveur SFTP. Par exemple, 22.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Auth type]</p> </td> 
   <td> <p>Sélectionnez le mode d’autorisation à utiliser pour la connexion au serveur SFTP.</p> 
    <ul> 
     <li><strong>[!UICONTROL User name and password]</strong> : saisissez vos informations d’identification.</li> 
     <li> <p><strong>[!UICONTROL User name and key]</strong> : saisissez votre nom d’utilisateur ou d’utilisatrice et votre clé privée/certificat privé.</p> <p>Chargez la clé privée pour utiliser l’autorisation côté client ou chargez votre certificat (fichier P12 ou PFX) si vous souhaitez utiliser TLS à l’aide de votre certificat auto-signé. Si vous utilisez l’autorisation de certificat côté client, vous pouvez saisir votre certificat d’autorité de certification ici.</p> <p>Workfront Fusion ne conserve ni ne stocke aucune des données (fichiers, mots de passe) que vous fournissez ici. Le fichier et le mot de passe ne sont utilisés que pour extraire une clé privée/un certificat privé.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Algorithmes d'échange de clés] </td> 
   <td> <p>Vous pouvez saisir un ensemble d’algorithmes pour l’échange de clés. Le module donne la priorité aux algorithmes en fonction de l’ordre dans lequel ils ont été ajoutés. Pour chaque algorithme à ajouter, cliquez sur <b>Ajouter un élément</b> et sélectionnez l’algorithme.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Ciphers] </td> 
   <td> <p>Vous pouvez saisir un ensemble de chiffrements pour l’échange de clés. Le module donne la priorité aux chiffrements en fonction de l’ordre dans lequel ils ont été ajoutés. Pour chaque chiffrement que vous souhaitez ajouter, cliquez sur <b>Ajouter un élément</b> et sélectionnez le chiffrement.</p> </td> 
  </tr> 
 </tbody> 
</table>

Après avoir saisi les informations de connexion, cliquez sur **[!UICONTROL Continuer]** pour établir une connexion.

### Options de connexion prises en charge

Le connecteur SFTP prend en charge les éléments suivants lors de la création d’une connexion :

#### Algorithmes d’échange de clés (KEX)

* `ecdh-sha2-nistp256`
* `ecdh-sha2-nistp384`
* `ecdh-sha2-nistp521`
* `diffie-hellman-group-exchange-sha256`
* `diffie-hellman-group14-sha256`
* `diffie-hellman-group16-sha512`
* `diffie-hellman-group18-sha512`
* `diffie-hellman-group14-sha1`

#### Chiffrements

* `aes256-gcm@openssh.com`
* `aes256-gcm`
* `aes128-gcm@openssh.com`
* `aes128-gcm`
* `aes256-ctr`
* `aes192-ctr`
* `aes128-ctr`
* `aes256-cbc`
* `aes192-cbc`
* `aes128-cbc`
* `blowfish-cbc`

#### Formats de clés de l’hôte du serveur

* `ssh-ed25519`
* `ecdsa-sha2-nistp256`
* `ecdsa-sha2-nistp384`
* `ecdsa-sha2-nistp521`
* `ssh-rsa`
* `ssh-dss`
<!--
* `rsa-sha2-256`
* `rsa-sha2-512`
-->

## Modules [!UICONTROL SFTP] et leurs champs

Lorsque vous configurez des modules [!UICONTROL SFTP], Workfront Fusion affiche les champs répertoriés ci-dessous. En outre, des champs [!UICONTROL SFTP] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Déclencheurs

* [Fichiers de contrôle dans un dossier](#watch-files-in-a-folder)
* [Observer les sous-dossiers dans un dossier](#watch-subfolders-in-a-folder)

#### [!UICONTROL Surveiller les fichiers dans un dossier]

Renvoie les fichiers avec des détails lorsqu’un fichier est créé ou modifié dans un dossier spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Pour plus d’informations sur la connexion de votre compte SFTP à Workfront Fusion, voir <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connexion de SFTP à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Saisissez le dossier que vous souhaitez observer. Vous pouvez spécifier un chemin absolu, tel que <code>/home/user/</code>, ou un chemin relatif pointant vers un dossier spécifique de l’utilisateur connecté, tel que <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>Taille de la mémoire tampon [B]</td> 
   <td> <p> Saisissez la taille de la mémoire tampon en octets. Cette valeur définit la taille des morceaux transférés depuis le serveur. Certains serveurs peuvent causer des problèmes ou corrompre des fichiers lorsque la valeur est trop élevée.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned files]</td> 
   <td> <p> Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Surveiller les sous-dossiers dans un dossier]

Renvoie des dossiers avec des détails lorsqu’un dossier est créé ou modifié dans un dossier spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte SFTP à Workfront Fusion, voir <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connexion de SFTP à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Saisissez ou mappez le dossier que vous souhaitez surveiller. Vous pouvez spécifier un chemin absolu, tel que <code>/home/user/</code>. Vous pouvez également spécifier un chemin relatif pointant vers un dossier spécifique de la personne connectée, tel que <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned files]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [Créer un dossier](#create-a-folderr)
* [Suppression d’un fichier](#delete-a-file)
* [Suppression d’un dossier](#delete-a-folder)
* [Obtenir un fichier](#get-a-file)
* [Obtenir les fichiers](#get-files)
* [Répertorier le contenu d’un dossier](#list-a-folders-content)
* [Déplacer un fichier](#move-a-file)
* [Renommer un fichier](#rename-a-file)
* [Mettre à jour les autorisations de fichier](#update-file-permissions)
* [Charger un fichier](#upload-a-file)

#### [!UICONTROL Créer un dossier]

Ce module d’action crée un dossier à l’emplacement spécifié.

>[!NOTE]
>
>Si le dossier existe déjà, le module renvoie une erreur. Pour poursuivre le flux sans interruption, associez un itinéraire de gestionnaire d’erreurs au module afin de détecter l’erreur et utilisez la directive [!UICONTROL Resume] pour poursuivre le flux. Pour plus d’informations sur l’association d’un itinéraire de gestionnaire d’erreurs, voir [ Gestion des erreurs dans Adobe Workfront Fusion](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md). Pour plus d’informations sur l’itinéraire du gestionnaire d’erreurs, voir [Directives relatives à la gestion des erreurs dans Adobe Workfront Fusion](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Pour plus d’informations sur la connexion de votre compte SFTP à Workfront Fusion, voir <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connexion de SFTP à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Spécifiez un dossier existant comme emplacement de stockage pour le nouveau dossier. Vous pouvez spécifier un chemin d’accès absolu tel que <code>/home/user/file.txt</code>. Vous pouvez également spécifier un chemin relatif pointant vers un dossier spécifique de la personne connectée, tel que <code>./</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder Name]</td> 
   <td> <p> Saisissez le nom du dossier.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permissions]</p> </td> 
   <td> <p>Définissez les autorisations souhaitées pour le dossier. Utilisez les paramètres chmod. Par exemple, <code>777</code> ou <code>-rwxrwxrwx</code>.</p> <p>Ces autorisations doivent correspondre au modèle <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>Pour plus d’informations sur chmod, consultez la <a href="https://ss64.com/bash/chmod.html">documentation chmod</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Supprimer un fichier]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Pour plus d’informations sur la connexion de votre compte SFTP à Workfront Fusion, voir <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connexion de SFTP à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path]</td> 
   <td> <p> Saisissez le chemin d’accès au fichier que vous souhaitez supprimer. Vous pouvez spécifier un chemin d’accès absolu tel que <code>/home/user/file.txt</code>. Vous pouvez également spécifier un chemin relatif pointant vers un dossier spécifique de la personne connectée, tel que <code>./file.txt</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Supprimer un dossier]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Pour plus d’informations sur la connexion de votre compte SFTP à Workfront Fusion, voir <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connexion de SFTP à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Folder Path]</td> 
   <td> <p> Indiquez le chemin d’accès au dossier à supprimer. Vous pouvez spécifier un chemin d’accès absolu tel que <code>/home/user/</code>. Vous pouvez également spécifier un chemin relatif pointant vers un dossier spécifique de la personne connectée, tel que <code>./.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obtenir un fichier]

Ce module permet de récupérer les détails d’un fichier, y compris ses données.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Pour plus d’informations sur la connexion de votre compte SFTP à Workfront Fusion, voir <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connexion de SFTP à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Buffer Size [B]]</td> 
   <td> <p> Saisissez la taille de la mémoire tampon en octets. Cette valeur définit la taille des morceaux transférés depuis le serveur. Certains serveurs peuvent causer des problèmes ou corrompre des fichiers lorsque la valeur est trop élevée.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path] </td> 
   <td> <p>Saisissez le chemin d’accès au fichier. Vous pouvez spécifier un chemin d’accès absolu tel que <code>/home/user/file.txt</code>. Vous pouvez également spécifier un chemin relatif pointant vers un dossier spécifique de la personne connectée, tel que <code>./file.txt</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obtenir les fichiers]

Ce module renvoie les fichiers d’un dossier spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Pour plus d’informations sur la connexion de votre compte SFTP à Workfront Fusion, voir <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connexion de SFTP à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Buffer Size [B]]</td> 
   <td> <p> Saisissez la taille de la mémoire tampon en octets. Cette valeur définit la taille des morceaux transférés depuis le serveur. Certains serveurs peuvent causer des problèmes ou corrompre des fichiers lorsque la valeur est trop élevée.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Saisissez ou mappez le dossier qui contient les fichiers ou les dossiers à répertorier. Vous pouvez spécifier un chemin d’accès absolu tel que <code>/home/user/</code>. Vous pouvez également spécifier un chemin relatif pointant vers un dossier spécifique de la personne connectée, tel que <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>Saisissez ou mappez le terme de recherche. Par exemple, si vous souhaitez rechercher des fichiers portant l’extension .txt, saisissez <code>.txt</code>.Vous pouvez également saisir ou mapper le nom du fichier que vous souhaitez rechercher.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort By]</td> 
   <td> <p> Indiquez si vous souhaitez trier les résultats en fonction du nom du fichier, de sa taille, de la date du dernier accès ou de la date de la dernière modification.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort Order]</td> 
   <td> <p> Indiquez si le résultat doit être renvoyé par ordre croissant ou décroissant.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Continue the execution of the route even if the module returns no results]</p> </td> 
   <td>Activez cette option pour vous assurer que ce module n’arrête pas le scénario s’il ne renvoie aucun résultat.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned results]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Lister le contenu d’un dossier]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Pour plus d’informations sur la connexion de votre compte SFTP à Workfront Fusion, voir <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connexion de SFTP à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show] </td> 
   <td> <p>Sélectionnez si vous souhaitez récupérer des fichiers, des dossiers ou les deux.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Saisissez ou mappez le dossier qui contient les fichiers ou les dossiers à répertorier. Vous pouvez spécifier un chemin d’accès absolu tel que <code>/home/user/</code>. Vous pouvez également spécifier un chemin relatif pointant vers un dossier spécifique de la personne connectée, tel que <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>Saisissez ou mappez le terme de recherche. Par exemple, si vous souhaitez rechercher des fichiers portant l’extension .txt, saisissez <code>.txt</code>.Vous pouvez également saisir ou mapper le nom du fichier que vous souhaitez rechercher.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort By]</td> 
   <td> <p> Indiquez si vous souhaitez trier les résultats par nom de fichier, taille, date de dernier accès ou date de dernière modification.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sort Order] </td> 
   <td> <p>Indiquez si le résultat doit être renvoyé par ordre croissant ou décroissant.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Continue the execution of the route even if the module returns no results]</p> </td> 
   <td>Activez cette option pour vous assurer que ce module n’arrête pas le scénario s’il ne renvoie aucun résultat.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned results]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Déplacer un fichier]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Pour plus d’informations sur la connexion de votre compte SFTP à Workfront Fusion, voir <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connexion de SFTP à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path]</td> 
   <td> <p> Saisissez le chemin d’accès au fichier que vous souhaitez déplacer. Vous pouvez spécifier un chemin d’accès absolu tel que <code>/home/user/file.txt</code>. Vous pouvez également spécifier un chemin relatif pointant vers un dossier spécifique de la personne connectée, tel que <code>./file.txt</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL New Folder]</td> 
   <td> <p> Saisissez le chemin d’accès au nouvel emplacement du fichier. Vous pouvez spécifier un chemin d’accès absolu tel que <code>/home/user/</code>. Vous pouvez également spécifier un chemin relatif pointant vers un dossier spécifique de la personne connectée, tel que <code>./.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Renommer un fichier]

Renomme un fichier.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Pour plus d’informations sur la connexion de votre compte SFTP à Workfront Fusion, voir <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connexion de SFTP à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path]</td> 
   <td> <p> Saisissez le chemin d’accès au fichier que vous souhaitez renommer. Vous pouvez spécifier un chemin d’accès absolu tel que <code>/home/user/file.txt</code>. Vous pouvez également spécifier un chemin relatif pointant vers un dossier spécifique de la personne connectée, tel que <code>./file.txt</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL New file name]</td> 
   <td> <p> Saisissez le nouveau nom du fichier, y compris son extension.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mettre à jour les autorisations d’un fichier]

Permet de modifier les autorisations du fichier.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Pour plus d’informations sur la connexion de votre compte SFTP à Workfront Fusion, voir <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connexion de SFTP à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File Path]</td> 
   <td> <p> Saisissez le chemin d’accès au fichier que vous souhaitez déplacer. Vous pouvez spécifier un chemin d’accès absolu tel que <code>/home/user/file.txt</code>. Vous pouvez également spécifier un chemin relatif pointant vers un dossier spécifique de la personne connectée, tel que <code>./file.txt</code>.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permissions]</p> </td> 
   <td> <p>Définissez les autorisations de fichier souhaitées. Utilisez les paramètres chmod. Par exemple, <code>777</code> ou <code>-rwxrwxrwx</code>.</p> <p>Ces autorisations doivent correspondre au modèle <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>Pour plus d’informations sur chmod, consultez la <a href="https://ss64.com/bash/chmod.html">documentation chmod</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Charger un fichier]

Ce module permet de charger un fichier vers le serveur SFTP.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td>
   <td> <p>Pour plus d’informations sur la connexion de votre compte SFTP à Workfront Fusion, voir <a href="#connect-sftp-to-workfront-fusion" class="MCXref xref">Connexion de SFTP à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Spécifiez un dossier existant comme emplacement de stockage du fichier. Vous pouvez spécifier un chemin d’accès absolu tel que <code>/home/user/</code>. Vous pouvez également spécifier un chemin relatif pointant vers un dossier spécifique de la personne connectée, tel que <code>./.</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source File]</td> 
   <td> <p> Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Permissions]</p> </td> 
   <td> <p>Définissez les autorisations souhaitées pour le fichier ou le dossier. Utilisez les paramètres chmod. Par exemple, <code>777</code> ou <code>-rwxrwxrwx</code>.</p> <p>Ces autorisations doivent correspondre au modèle <code>/(.?([r-][w-][x-]){3})|[0-7]{3}/.</code></p> <p>Pour plus d’informations sur chmod, consultez la <a href="https://ss64.com/bash/chmod.html">documentation chmod</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Buffer size (B)]</p> </td> 
   <td> <p>Définissez la taille (en octets) de chaque bloc lors du chargement du fichier. Cela s’avère utile pour les fichiers volumineux ou lorsque les limites de mémoire du serveur nécessitent des chargements plus petits. Si cette valeur n’est pas définie, le fichier est écrit en une seule opération.</p> </td> 
  </tr> 
 </tbody> 
</table>
