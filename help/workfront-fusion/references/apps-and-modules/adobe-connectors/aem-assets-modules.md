---
title: Modules Adobe Experience Manager Assets
description: Avec le connecteur Adobe Experience Manager Assets pour Adobe Workfront Fusion, vous pouvez créer, charger et mettre à jour des ressources, ainsi que copier ou déplacer des dossiers et des ressources.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 361e6c9c-1497-4f47-85bb-503619744968
source-git-commit: d4bdc4005a3b7b22d64adc8ca1d20bcf534ddfd1
workflow-type: tm+mt
source-wordcount: '3734'
ht-degree: 22%

---

# Modules Adobe Experience Manager Assets

Avec le connecteur Adobe Experience Manager Assets pour Adobe Workfront Fusion, vous pouvez créer, charger et mettre à jour des ressources, ainsi que copier ou déplacer des dossiers et des ressources.

Pour une présentation vidéo du connecteur Adobe Experience Manager Assets, voir :

* [Adobe Experience Manager Assets](https://video.tv.adobe.com/v/3427034/){target=_blank}

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

* Vous devez disposer d’un compte Adobe Experience Manager Assets pour utiliser ces modules.
* Vous devez configurer un flux serveur à serveur dans la console Adobe Developer.

  Pour obtenir des instructions sur la configuration du flux serveur à serveur dans la console Adobe Developer, voir [&#x200B; Génération de jetons d’accès pour les API côté serveur &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html?lang=fr#the-server-to-server-flow).
* Votre compte technique Adobe Experience Manager doit disposer d’autorisations en écriture.

  Pour obtenir des instructions sur l’ajout d’autorisations d’écriture à votre compte technique Adobe Experience Manager, voir [Informations d’identification du service](https://experienceleague.adobe.com/en/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials) dans la documentation de Adobe Experience Manager.

## Informations sur l’API Adobe Experience Manager Assets

Le connecteur Adobe Experience Manager Assets utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.8.61</td> 
  </tr>
 </tbody> 
 </table>

## Connexion d’Adobe Experience Manager Assets à Workfront Fusion {#connect-adobe-experience-manager-assets-to-workfront-fusion}

Pour créer une connexion pour vos modules Adobe Experience Manager Assets :

1. Cliquez sur Ajouter en regard de la zone Connexion .

2. Sélectionnez le type de connexion que vous créez :

   * **AEM Assets as a Cloud Service**

     Cette configuration nécessite des informations de la part du Adobe Admin Console.

   * **AEM Assets Basic (Adobe Managed Services)**

     Cette configuration nécessite un nom d’utilisateur ou d’utilisatrice et un mot de passe.

3. Remplissez les champs correspondant au type de connexion que vous créez.

   Pour AEM Assets as a Cloud Service, voir [Configuration de la connexion pour AEM Assets as a Cloud Service](#configure-the-connection-for-aem-assets-as-a-cloud-service).

   Pour AEM Assets Basic (Adobe Managed Services), voir [Configurer la connexion pour AEM Assets Basic](#configure-the-connection-for-aemassets-basic-adobe-managed-services).

4. Cliquez sur **Continuer** pour enregistrer la connexion et revenir au module.


### Configuration de la connexion à AEM Assets as a Cloud Service

>[!NOTE]
>
>* Les informations de ces champs sont générées dans le cadre de la configuration du flux serveur à serveur sur le Adobe Developer Console. Vous trouverez ces valeurs dans le fichier JSON des identifiants de service généré dans le cadre de cette configuration.
>
>   Pour obtenir des instructions sur la configuration du flux serveur à serveur sur Adobe Developer Console, voir [Génération de jetons d’accès pour les API côté serveur](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html?lang=fr#the-server-to-server-flow).
>
>* Votre compte technique Adobe Experience Manager doit disposer d’autorisations en écriture.
>
>   Pour obtenir des instructions sur l’ajout d’autorisations d’écriture à votre compte technique Adobe Experience Manager, voir [Informations d’identification du service](https://experienceleague.adobe.com/en/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials) dans la documentation de Adobe Experience Manager.


<table style="table-layout:auto"> 
          <col/>
          <col/>
          <tbody>
              <tr>
                  <td role="rowheader">Nom de la connexion</td>
                  <td>
                      <p>Saisissez un nom pour cette connexion.</p>
                  </td>
              </tr>
              <tr>
                  <td role="rowheader">URL de l’instance sans barre oblique</td>
                  <td>Saisissez l’URL de votre instance Adobe Experience Manager. N’ajoutez pas une barre oblique <code>/</code> à la fin de l’URL.</td>
              </tr>
              <tr>
                  <td role="rowheader">Options de remplissage des détails du compte</td>
                  <td>Choisissez si vous souhaitez fournir un fichier JSON décrivant les détails de votre compte ou si vous souhaitez saisir les détails manuellement.</td>
              </tr>
              <tr>
                  <td role="rowheader">Détails du compte technique au format JSON</td>
                  <td>Si vous fournissez du code JSON, saisissez ou collez le code JSON décrivant les détails de votre compte.</td>
              </tr>
              <tr>
                  <td role="rowheader">ID client</td>
                  <td>Si vous saisissez les détails manuellement, saisissez l’identifiant client généré dans la configuration serveur à serveur.</td>
              </tr>
              <tr>
                  <td role="rowheader">Clé secrète client</td>
                  <td>Si vous saisissez les détails manuellement, saisissez le secret client généré dans la configuration serveur à serveur.</td>
              </tr>
              <tr>
                  <td role="rowheader">Identifiant de compte technique</td>
                  <td>Si vous saisissez les détails manuellement, saisissez l'ID du compte technique. Il s’agit du champ « id » dans le fichier JSON des informations d’identification du client.</td>
              </tr>
              <tr>
                  <td role="rowheader">ID d’organisation</td>
                  <td class="">Si vous saisissez les détails manuellement, saisissez l’ID de votre organisation. Il s’agit du champ « org » dans le fichier JSON des informations d’identification du client.</td>
              </tr>
              <tr>
                  <td role="rowheader">Portées de Meta</td>
                  <td>Saisissez les étendues de Meta générées dans la configuration serveur à serveur.</td>
              </tr>
              <tr>
                  <td role="rowheader">Clé privée</td>
                  <td>Saisissez la clé privée générée lors de la configuration serveur à serveur. Pour extraire la clé privée, cliquez sur Extraire, puis saisissez le fichier à extraire et son mot de passe.</td>
              </tr>
              <tr>
                  <td role="rowheader">URL d'authentification</td>
                  <td>Saisissez l’URL d’authentification pour ce compte.</td>
              </tr>
          </tbody>
      </table>


### Configuration de la connexion à AEM Assets Basic (Adobe Managed Services)

<table style="table-layout:auto"> 
        <col/>
        <col />
        <tbody>
            <tr>
                <td role="rowheader">Nom de la connexion</td>
                <td>
                    <p>Saisissez un nom pour cette connexion.</p>
                </td>
            </tr>
            <tr>
                <td role="rowheader">URL de l’instance sans barre oblique</td>
                <td>Saisissez l’URL de votre instance Adobe Experience Manager. N’ajoutez pas une barre oblique <code>/</code> à la fin de l’URL.</td>
            </tr>
            <tr>
                <td role="rowheader">Nom d’utilisateur</td>
                <td>Saisissez le nom d’utilisateur du compte AEM Assets utilisé par cette connexion.</td>
            </tr>
            <tr>
                <td role="rowheader">Mot de passe</td>
                <td>Saisissez le mot de passe du compte AEM Assets utilisé par cette connexion.</td>
            </tr>
        </tbody>
    </table>


## Modules Adobe Experience Manager Assets et leurs champs

Lorsque vous configurez les modules Adobe Experience Manager Assets, Workfront Fusion affiche les champs répertoriés ci-dessous. Selon des facteurs tels que votre niveau d’accès dans l’application ou le service, d’autres champs Adobe Experience Manager Assets peuvent s’afficher en plus de ceux-ci. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Opérations sur les fichiers](#files-operations)
* [Autre](#other)
* [Assets (API de création)](#assets-author-api)
* [Événements (API de création)](#events-author-api)
* [Métadonnées (API de création)](#metadata-author-api)
* [Importer (API de création)](#import-author-api)
* [Relations (API de création)](#relations-author-api)
* [Dossiers (API des dossiers)](#folders-folders-api)

### Opérations sur les fichiers

* [Fin du chargement](#complete-upload)
* [Obtenir un stockage prédéfini](#get-presigned-storage)
* [Lancement du chargement](#initiate-upload)
* [Chargement d’un élément](#upload-an-asset)

#### Fin du chargement

Ce module d’action termine un chargement initié, une fois toutes les parties du fichier chargées.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom du fichier</td> 
   <td> <p>Saisissez ou mappez un nom pour le fichier chargé.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Charger le jeton</td> 
   <td>Saisissez ou mappez le jeton de chargement pour le fichier binaire, comme fourni par le lancement.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type MIME</td> 
   <td>Saisissez ou mappez le type MIME du fichier complété.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URI complet</td> 
   <td>Saisissez ou mappez l’URI complet du fichier.</td> 
  </tr> 
 </tbody> 
</table>


#### Obtenir un stockage prédéfini

Ce module d’action crée une URL présignée temporaire pour charger ou télécharger des fichiers en toute sécurité à partir d’AEM sans nécessiter d’informations d’identification directes.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type de recherche</td> 
   <td> <p>Indiquez si vous souhaitez rechercher la ressource en fonction de son chemin d’accès ou de son identifiant.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ressource</td> 
   <td>Sélectionnez le chemin d’accès à la ressource.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">UDID</td> 
   <td>Saisissez ou mappez l’UDID de la ressource.</td> 
  </tr> 
 </tbody> 
</table>

#### Lancement du chargement

Ce module d’action lance un chargement.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Destination</td> 
   <td> <p>Sélectionnez le dossier dans lequel vous souhaitez charger un fichier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom du fichier</td> 
   <td> <p>Saisir ou associer un nom au fichier chargé</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Taille de fichier max</td> 
   <td>Saisissez ou mappez la taille, en octets, du fichier chargé.</td> 
  </tr> 
 </tbody> 
</table>


#### Chargement d’un élément

Ce module d’action charge une ressource dans votre compte Adobe Experience Manager Assets.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Destination</td> 
   <td> <p>Sélectionnez le dossier dans lequel vous souhaitez charger une ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">fichier Source</td> 
   <td>Saisissez ou mappez le nom et les données du fichier source.</td> 
  </tr> 
 </tbody> 
</table>

### Autre


* [Copier un dossier ou une ressource](#copy-a-folder-or-asset)
* [Créer un enregistrement](#create-a-record)
* [Suppression d’un dossier, d’une ressource ou d’un rendu](#delete-a-folder-asset-or-rendition)
* [Obtenir une liste de dossiers](#get-a-folder-listing)
* [Effectuer un appel API personnalisé.](#make-a-custom-api-call)
* [Déplacer un dossier ou une ressource](#move-a-folder-or-asset)
* [Mettre à jour un enregistrement](#update-a-record)



#### Copier un dossier ou une ressource

Ce module d’action copie un dossier ou une ressource vers un autre emplacement de votre compte Adobe Experience Manager Assets.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type d'enregistrement</td> 
   <td> <p>Sélectionnez si vous souhaitez copier un dossier ou une ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Dossier/ressource</td> 
   <td>Sélectionnez ou mappez le dossier ou la ressource que vous souhaitez copier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Chemin destination</td> 
   <td>Sélectionnez ou mappez le chemin d’accès à l’emplacement du nouveau dossier ou de la nouvelle ressource.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom du dossier/de la ressource copiés</td> 
   <td>Saisissez un nom pour le nouveau dossier ou la nouvelle ressource. Le nom du dossier qui s’affiche dans Adobe Experience Manager Assets est identique au nom d’origine. Le nom saisi ici apparaît dans l’URL du nouveau dossier ou de la nouvelle ressource.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Copier les enfants</td> 
   <td>Si vous copiez un dossier, activez cette option pour copier tous les sous-dossiers ou ressources du dossier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Remplacer</td> 
   <td>Activez cette option pour écraser les dossiers ou ressources de l’emplacement de destination portant le même nom que le dossier ou la ressource en cours de copie.</td> 
  </tr> 
 </tbody> 
</table>



#### Créer un enregistrement

Ce module d’action crée un dossier ou un commentaire de ressource.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type d’objet</td> 
   <td> <p>Indiquez si vous souhaitez créer un dossier ou un commentaire sur une ressource.</p> 
    <ul> 
     <li> <p>Dossier</p> <p>Remplissez les champs suivants :</p> 
      <ul> 
       <li> <p>Nom</p> <p>Saisissez un nom pour le dossier. Ce nom apparaîtra dans le chemin d’accès au fichier, il ne doit donc pas comporter d’espaces ou d’autres caractères. </p> </li> 
       <li> <p>Titre</p> <p>Saisissez un titre pour le dossier, qui peut être affiché à la place du nom.</p> </li> 
      </ul> </li> 
     <li> <p>Commentaire sur la ressource</p> <p>Remplissez les champs suivants :</p> 
      <ul> 
       <li> <p>Sélection de ressources</p> <p>Sélectionnez ou mappez l’ID de la ressource à laquelle vous souhaitez ajouter un commentaire.</p> </li> 
       <li> <p>Commentaire</p> <p>Saisissez le texte du commentaire.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Suppression d’un dossier, d’une ressource ou d’un rendu

Ce module d’action supprime un dossier, une ressource ou un rendu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type d'enregistrement</td> 
   <td> <p>Indiquez si vous souhaitez supprimer un dossier, une ressource ou un rendu.</p> 
    <ul> 
     <li> <p>Dossier</p> <p>Sélectionnez le dossier à supprimer en sélectionnant les dossiers dans son chemin d’accès.</p> </li> 
     <li> <p>Ressource</p> <p>Sélectionnez la ressource en sélectionnant les dossiers dans son chemin, puis la ressource à supprimer.</p> </li> 
     <li> <p>Rendu</p> <p>Sélectionnez le rendu en sélectionnant les dossiers dans son chemin d’accès.</p> <p>Saisissez ou mappez le nom du rendu.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Obtenir une liste de dossiers

Ce module d’action permet de récupérer une représentation d’un dossier existant et de ses entités enfant (dossiers ou ressources).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Dossier</td> 
   <td>Sélectionnez ou mappez le dossier que vous souhaitez récupérer. Pour ajouter des sous-dossiers au chemin d’accès, cliquez sur l’icône Plus et sélectionnez le sous-dossier.</td> 
  </tr> 
 </tbody> 
</table>

#### Effectuer un appel API personnalisé.

Ce module d’action effectue un appel API personnalisé à l’API Adobe Experience Manager Assets.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>URL</p> </td> 
   <td> <p>Saisissez un chemin d’accès relatif à votre URL de base Adobe Experience Manager.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Méthode</p> </td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">En-têtes</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p> Workfront Fusion ajoute automatiquement des en-têtes d’autorisation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Chaîne de requête</td> 
   <td> <p>Saisissez la chaîne de requête. Pour chaque paire Clé/Valeur, cliquez sur <b>Ajouter un élément</b> et saisissez la Clé et la Valeur.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Corps</td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre JSON, placez les guillemets à l’extérieur de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Déplacer un dossier ou une ressource

Ce module d’action déplace la ressource ou le dossier au chemin d’accès donné vers un nouvel emplacement.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type d'enregistrement</td> 
   <td> <p>Indiquez si vous souhaitez déplacer un dossier ou une ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Dossier/ressource</td> 
   <td>Sélectionnez ou mappez le dossier ou la ressource que vous souhaitez déplacer.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Chemin destination</td> 
   <td>Sélectionnez ou mappez le chemin d’accès à l’emplacement vers lequel vous souhaitez déplacer le dossier ou la ressource.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom du dossier/de la ressource déplacé(e)</td> 
   <td>Saisissez un nouveau nom pour le dossier déplacé ou la ressource déplacée. Le nom du dossier qui s’affiche dans Adobe Experience Manager Assets est identique au nom d’origine. Le nom saisi ici apparaît dans l’URL du dossier déplacé ou de la ressource déplacée.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Remplacer</td> 
   <td>Activez cette option pour remplacer dans l’emplacement de destination tout dossier ou ressource portant le même nom que le dossier ou la ressource déplacé.</td> 
  </tr> 
 </tbody> 
</table>

#### Mettre à jour un enregistrement

Ce module d’action met à jour un enregistrement existant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type d'enregistrement</td> 
   <td> <p>Indiquez si vous souhaitez supprimer les métadonnées ou un rendu de la ressource.</p> 
    <ul> 
     <li> <p>Métadonnées de ressource</p> 
      <ul> 
       <li> <p>Sélectionnez la ressource dont vous souhaitez mettre à jour les métadonnées.</p> </li> 
       <li> <p>Saisissez le nouveau titre de la ressource.</p> </li> 
      </ul> </li> 
     <li> <p>Rendu de ressource</p> 
      <ul> 
       <li> <p>Sélectionnez la ressource dont vous souhaitez mettre à jour le rendu.</p> </li> 
       <li> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Assets (API de création)

* [Supprimer la ressource](#delete-asset)
* [Obtenir le statut du traitement](#get-job-status)

#### Supprimer la ressource

Ce module d’action supprime une ressource unique par son identifiant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de ressource</td> 
   <td> <p>Saisissez ou mappez l’identifiant de la ressource à supprimer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Forcer</td> 
   <td>Activez cette option pour forcer la suppression de la ressource, même si elle est référencée.</td> 
  </tr> 
 </tbody> 
</table>

#### Obtenir le statut du traitement

Ce module d’action obtient le statut actuel d’une tâche asynchrone.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Identifiant du traitement</td> 
   <td> <p>Saisissez ou mappez l’identifiant de la tâche pour laquelle vous souhaitez obtenir le statut.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Événements (API de création)

#### Surveiller les événements

Ce module de déclenchement lance un scénario lorsqu’un événement se produit dans AEM Assets.

Le module contient un seul champ : Webhook. Sélectionnez un webhook existant à utiliser pour ces événements ou créez-en un.

Pour créer un webhook :

1. Cliquez sur **Ajouter** en regard du champ Webhook.
1. Remplissez les champs suivants :

   <table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">Nom du Webhook</td>
        <td>Saisissez le nom de ce webhook.</td>
       </tr>
       <tr>
         <td role="rowheader">Connexion</td>
        <td>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</td>
       </tr>
     </tbody>
   </table>

1. Cliquez sur Enregistrer pour enregistrer le webhook et revenir au module .


### Métadonnées (API de création)

* [Obtention des métadonnées de ressource](#get-asset-metadata)
* [Mettre à jour les métadonnées d’une ressource](#update-asset-metadata)

#### Obtention des métadonnées de ressource

Ce module d’action récupère les métadonnées sur la ressource spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de ressource</td> 
   <td> <p>Saisissez ou mappez l’identifiant de la ressource pour laquelle vous souhaitez obtenir les métadonnées.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Mettre à jour les métadonnées d’une ressource

Ce module d’action met à jour les métadonnées de la ressource spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de ressource</td> 
   <td> <p>Saisissez ou mappez l’identifiant de la ressource pour laquelle vous souhaitez mettre à jour les métadonnées.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Mises à jour</td> 
   <td> <p>Pour chaque élément de métadonnées à mettre à jour, cliquez sur <b>Ajouter un élément</b> et sélectionnez l’opération. Les autres champs de la zone Ajouter un élément dépendent de l’opération sélectionnée.</p> </td> 
  </tr> 
 </tbody> 
</table>


### Importer (API de création)

* [Obtenir les résultats de la tâche d’importation](#get-import-job-results)
* [Obtention de l’état du traitement d’importation](#get-import-job-status)
* [Chargement d’une ressource à partir d’une URL](#upload-an-asset-from-a-url)

#### Obtenir les résultats de la tâche d’importation

Ce module d’action récupère les résultats de la tâche d’importation spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de tâche d'importation</td> 
   <td> <p>Saisissez ou mappez l’identifiant de la tâche pour laquelle vous souhaitez récupérer les résultats.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Obtention de l’état du traitement d’importation

Ce module d’action récupère le statut de la tâche d’importation spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de tâche d'importation</td> 
   <td> <p>Saisissez ou mappez l’identifiant de la tâche dont vous souhaitez récupérer le statut.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Chargement d’une ressource à partir d’une URL

Ce module d’action charge une nouvelle ressource en important les fichiers des URL spécifiées.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Titre</td> 
   <td> <p>Saisissez ou mappez un titre pour la ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Description</td> 
   <td> <p>Saisissez ou mappez une description pour la ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Objet</td> 
   <td> <p>Saisissez ou mappez un objet pour la ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Créateur ou créatrice</td> 
   <td> <p>Saisissez ou mappez le créateur de la ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Date d'expiration</td> 
   <td> <p>Saisissez ou mappez la date d’expiration de la ressource.</p><p>Pour obtenir la liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercition</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Métadonnées personnalisées</td> 
   <td> <p>Pour chaque élément de métadonnées personnalisées que vous souhaitez ajouter à la ressource, cliquez sur <b>Ajouter un élément</b> et saisissez le nom et la valeur des métadonnées.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Chemin ou ID du dossier</td> 
   <td> <p>Indiquez si vous souhaitez spécifier le dossier de destination par son chemin d’accès ou son identifiant, puis sélectionnez le chemin d’accès ou saisissez l’identifiant.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Fichiers à importer</td> 
   <td> <p>Pour chaque fichier à importer, cliquez sur <b>Ajouter un élément&lt;/&gt; et renseignez les détails du fichier. <code>Title</code> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"></td> 
   <td> <p></p> </td> 
  </tr> 
 </tbody> 
</table>

### Relations (API de création)

* [Créer des relations de ressources](#create-asset-relations)
* [Supprimer la relation de l’actif](#create-asset-relations)
* [Obtenir les types de relations des ressources](#get-asset-relation-types)
* [Obtenir les relations des ressources](#get-asset-relations)

#### Créer des relations de ressources

Ce module d’action crée de nouvelles relations de ressource pour la ressource sélectionnée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de ressource</td> 
   <td> <p>Saisissez ou mappez l’ID de ressource auquel vous souhaitez mettre en relation d’autres ressources.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ressources connexes</td> 
   <td> <p>Pour chaque élément que vous souhaitez mettre en relation avec l’élément sélectionné, cliquez sur <b>Ajouter un élément</b> et saisissez ou mappez l’identifiant de l’élément et le type de relation.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Supprimer la relation de l’actif

Ce module d’action supprime une relation de ressource pour une ressource.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de ressource</td> 
   <td> <p>Saisissez ou mappez la ressource d’ID à partir de laquelle vous souhaitez supprimer une relation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Ressources connexes</td> 
   <td> <p>Saisissez ou mappez le type de relation à supprimer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Fournir un identifiant spécifique de la ressource associée à supprimer</td> 
   <td> <p>Cochez cette case pour supprimer une relation spécifique. Si cette case est décochée, toutes les relations du type sélectionné sont supprimées.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de ressource associé</td> 
   <td> <p>Si vous supprimez une relation spécifique, saisissez ou mappez l'identifiant de la relation à supprimer.</p> </td> 
  </tr> 
 </tbody> 
</table>


#### Obtenir les types de relations des ressources

Ce module répertorie les types de relations d&#39;actif qui existent pour l&#39;actif spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de ressource</td> 
   <td> <p>Saisissez ou mappez l’actif d’ID pour lequel vous souhaitez répertorier les types de relation.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Obtenir les relations des ressources

Ce module répertorie les relations de ressource pour la ressource spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de ressource</td> 
   <td> <p>Saisissez ou mappez la ressource d’ID pour laquelle vous souhaitez répertorier les relations.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Types de relation</td> 
   <td> <p>Saisissez ou mappez une liste séparée par des virgules des types de relations pour lesquels vous souhaitez répertorier les relations.</p> </td> 
  </tr> 
 </tbody> 
</table>



### Dossiers (API des dossiers)

* [Créer des dossiers](#create-folders)
* [Supprimer un dossier par ID](#delete-a-folder-by-id)
* [Supprimer des dossiers par chemin](#delete-folders-by-path)
* [Obtenir les résultats des tâches de dossiers](#get-folders-job-results)
* [Obtention de l&#39;état de la tâche de dossiers](#get-folders-job-status)
* [Répertorier les dossiers](#list-folders)

#### Créer des dossiers

Ce module d’action permet de créer un dossier dans Adobe Experience Manager Assets.



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Dossiers à créer</td> 
   <td> <p>Pour chaque dossier à créer, cliquez sur <b>Ajouter un élément</b> et saisissez les informations suivantes :</p>
   <ul>
   <li><b>Nouvel emplacement du dossier</b><p>Sélectionnez le chemin d’accès à l’emplacement où vous souhaitez créer le dossier.</p></li>
       <li> <b>Nom</b> <p>Saisissez un nom pour le dossier. Ce nom apparaîtra dans le chemin d’accès au fichier, il ne doit donc pas comporter d’espaces ou d’autres caractères. </p> </li> 
       <li> <b>Titre</b> <p>Saisissez un titre pour le dossier, qui peut être affiché à la place du nom.</p> </li> 
   </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### Supprimer un dossier par ID

Ce module d&#39;action supprime le dossier Adobe Experience Manager Assets avec l&#39;identifiant spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de dossier</td> 
   <td> Saisissez ou mappez l’identifiant du dossier que vous souhaitez supprimer.</td>
  </tr> 
 <tr> 
   <td role="rowheader">Supprimer les sous-dossiers</td> 
   <td> Activez cette option pour supprimer le dossier et tous ses sous-dossiers.</td>
  </tr> 
 <tr> 
   <td role="rowheader">Forcer</td> 
   <td> Activez cette option pour forcer la suppression des dossiers, même s’ils sont référencés.</td>
  </tr> 
 </tbody> 
</table>

#### Supprimer des dossiers par chemin

Ce module d’action supprime les dossiers Adobe Experience Manager Assets aux chemins spécifiés.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Chemins d’accès aux dossiers</td> 
   <td>Pour chaque dossier à supprimer, cliquez sur <b>Ajouter un élément</b> et sélectionnez le chemin d’accès au dossier.</td>
  </tr> 
 <tr> 
   <td role="rowheader">Supprimer les sous-dossiers</td> 
   <td> Activez cette option pour supprimer le dossier et tous ses sous-dossiers.</td>
  </tr> 
 <tr> 
   <td role="rowheader">Forcer</td> 
   <td> Activez cette option pour forcer la suppression de la ressource, même si elle est référencée.</td>
  </tr> 
 </tbody> 
</table>

#### Obtenir les résultats des tâches de dossiers

Ce module récupère les résultats d’une tâche asynchrone créée par l’API du dossier Adobe Experience Manager Assets.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Identifiant du traitement</td> 
   <td> Saisissez ou mappez l’identifiant de la tâche pour laquelle vous souhaitez récupérer les résultats.</td>
  </tr> 
 </tbody> 
</table>

#### Obtention de l&#39;état de la tâche de dossiers

Ce module récupère le statut d’une tâche asynchrone créée par l’API Dossier Adobe Experience Manager Assets.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Identifiant du traitement</td> 
   <td> Saisissez ou mappez l’identifiant de la tâche pour laquelle vous souhaitez récupérer le statut.</td>
  </tr> 
 </tbody> 
</table>


#### Répertorier les dossiers

Ce module répertorie les sous-dossiers du dossier spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre compte Adobe Experience Manager Assets à Workfront Fusion, voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Experience Manager Assets à Workfront Fusion</a> dans cet article.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">Chemin ou ID du dossier</td> 
   <td> <p>Indiquez si vous souhaitez spécifier le dossier de destination par son chemin d’accès ou son identifiant, puis sélectionnez le chemin d’accès ou saisissez l’identifiant.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--
i! I added a lot of modules to the AEM Assets connector and we need new documentation for them. The connector is available in the QA environment. Heres the added modules and a brief description of them, more info about them can be found in the Assets Author Api docs and the Folders Api docs. Im not fully confident that i kept all the best practices for naming things :sweat_smile:, i hope you can take a look at that as well. Let me know if theres anything i can tell about the modules and thanks again in advance!
Author API
Assets
Delete Asset
Deletes an asset when provided an Asset ID, There is a force parameter that when toggled will delete the folder regardless if it's referenced.
Return either nothing if the deletion takes less than a few seconds or a job ID which can be used in another module to track the job of deleting the folder.
Get assets job status
Given an assets job ID will return the state that the job is currently in (PROCESSING, COMPLETED, etc.)
Events
AEM Assets events
The costumer can create a web hook in this module and register it in the Adobe admin console
Metadata
Get asset metadata
Given asset ID returns assets metadata.
Update asset metadata
Given asset ID, there are 6 patch operations that can be done with the metadata. The operations are visible in the module as well as the documentation.
Import
Get import job results
Given Job ID returns it's result.
Get import job status
Given Job ID returns its status.
Upload an asset from url
Takes global metadata which applies to all the assets and local ones which apply individually.In both it is also possible to specify custom metadata.
Also takes the folder path or folder ID to place the assets there and url-s of the assets.
Relations
Create asset relation
Given asset ID and a list of related asset ID as well as the relation types creates those relationships.
Delete asset relations
Given asset ID and relation type deletes all relations of that type. Can also specify a related asset to target only that.
 there is a checkbox that is checked by default and when unchecked reveals a field where the user can specify the related user ID.
Get asset relation types
Given asset ID returns all the relation types that the asset has.
Get asset relations
Given asset ID returns all relations. Can also specify a specific type of relation.
Folders API
Create folders
Given a list of folders with their path, name, title, creates them.
Delete a folder by ID
Given Folder ID deletes the folder. There is also a way to specify if it should delete folders recursively and if it should be forced.
Return either nothing if the deletion takes less than a few seconds or a job ID which can be used in another module to track the job of deleting the folder.
Delete folders by path
Given a list of paths, deletes everything in them. There is also a way to specify if it should delete folders recursively and if it should be forced.
Return either nothing if the deletion takes less than a few seconds or a job ID which can be used in another module to track the job of deleting the folder.
Get folders job results
Given job ID returns its result.
Get folders job status
Given job ID returns its status.
List Folders
List folders under the given folder. In the module you can choose the root folder either by ID or by Path.
-->

