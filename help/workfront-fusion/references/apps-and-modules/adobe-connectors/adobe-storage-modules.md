---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: apps-and-their-modules
title: Modules de stockage Adobe
description: Dans un  [!DNL Adobe Workfront Fusion] , vous devez créer et gérer des projets dans le Adobe Admin Console.
author: Becky
feature: Workfront Fusion
hide: true
hidefromtoc: true
source-git-commit: 70a2d06da6be6c892df12faa3a168e66daef118e
workflow-type: tm+mt
source-wordcount: '1351'
ht-degree: 18%

---

# Modules de stockage Adobe

Dans un scénario [!DNL Adobe Workfront Fusion], vous devez créer et gérer des projets dans le Adobe Admin Console.

Si vous avez besoin d’instructions pour créer un scénario, consultez les articles sous [Créer un scénario : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <p>Actuel : aucune exigence de licence Workfront Fusion.</p>
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

## Création d’une connexion au stockage Adobe

La création d’une connexion au stockage Adobe nécessite une configuration dans Adobe Developer Console ainsi que dans Fusion.

### Configuration du projet dans le Adobe Developer Console

Vous devez ajouter l’API à votre projet dans le Adobe Developer Console.

1. Ouvrez votre projet dans Adobe Developer Console.
1. Cliquez sur **Ajouter au projet**, puis sélectionnez **API**.
1. Dans la liste des API disponibles, sélectionnez **Adobe Cloud Platform et API Collaboration**.
1. Sur l’écran Sélectionner le type d’authentification , sélectionnez **OAuth serveur à serveur** et cliquez sur **Suivant**.
1. Ajoutez un nom pour les informations d’identification.
1. Cliquez sur **Suivant** puis sur **Enregistrer l’API configurée**.
1. Notez les informations d’identification fournies, que vous utiliserez lors de la configuration de la connexion dans Workfront Fusion.
1. Passez à [Transformer votre compte technique en administrateur dans Adobe Admin Console](#make-your-technical-account-an-admin-in-the-adobe-admin-console).

### Transformer votre compte technique en administrateur dans Adobe Admin Console

Sur la page Adobe Admin Console , sélectionnez l’onglet Produits dans la barre de navigation supérieure, puis sélectionnez Workfront Fusion

1. Recherchez et copiez l’adresse e-mail de l’utilisateur du compte technique de votre entreprise.
1. Si une liste s’affiche, sélectionnez le lien en haut.
1. Il s’agit de votre instance de production où travaillent vos utilisateurs et utilisatrices.
1. Dans la liste qui s’affiche, avec l’onglet Profils de produit sélectionné, cliquez sur le nom du lien Profil de produit Workfront .

   Cette liste comprend toutes les personnes déjà affectées à votre instance de production de Workfront.

1. Sélectionnez l’onglet **Administration** au-dessus de la liste des utilisateurs et des utilisatrices.
1. Sélectionnez **Ajouter un administrateur ou une administratrice**.
1. Dans la zone Ajouter des administrateurs de profil de produit , saisissez les adresses e-mail du compte technique, puis sélectionnez **Enregistrer**.

   Le compte technique est transformé en administrateur.

1. Passez à [Création de la connexion dans Workfront Fusion](#create-the-connection-in-workfront-fusion).

### Création de la connexion dans Workfront Fusion

Pour créer une connexion pour vos modules [!DNL Adobe Storage], procédez comme suit :

1. Cliquez sur **[!UICONTROL Add]** en regard de la zone Connexion .

1. Remplissez les champs suivants :

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>Sélectionnez <code>Server to server</code>.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Saisissez un nom pour cette connexion.</p>
        </td>
        </tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Saisissez votre [!UICONTROL Client ID] de [!UICONTROL Adobe]. Pour plus d'informations, consultez la section [!UICONTROL Credential details] du projet dans la [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Saisissez votre [!UICONTROL Client Secret] de [!DNL Adobe]. Pour plus d'informations, consultez la section [!UICONTROL Credential details] du projet dans la [!DNL Adobe Developer Console].</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL IMS Organization ID]</td>
        <td>Saisissez ou mappez votre ID d’organisation Adobe IMS. Il s’agit d’une chaîne avec le <code> 123abc@AdobeOrg</code> de formulaire, où la section avant le caractère @ est un nombre hexadécimal. Cette valeur figure dans le chemin d’URL de votre organisation dans Adobe Admin Console ou dans la console Adobe.IO pour votre intégration de la gestion des utilisateurs.</td>
        </tr>
      </tbody>
    </table>

1. Cliquez sur **[!UICONTROL Continue]** pour enregistrer la connexion et revenir au module .

## Modules de stockage Adobe et leurs champs

Lorsque vous configurez les modules de gestion des utilisateurs d’Adobe, Workfront Fusion affiche les champs répertoriés ci-dessous. D’autres champs User Management Adobe peuvent s’afficher en plus de ceux-ci, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Magasins ESM](#esm-stores)
* [Invitations](#invitations)
* [Autre](#other)

### Magasins ESM

* [Création d’un magasin ESM](#create-an-esm-store)
* [Suppression d’un magasin ESM](#delete-an-esm-store)
* [Ignorer un magasin ESM](#discard-an-esm-store)
* [Restaurer un magasin ESM](#restore-an-esm-store)

#### Création d’un magasin ESM

Ce module d’action met en place un nouveau magasin de gestion du stockage d’entreprise (ESM) pour organiser et gérer les ressources critiques de l’entreprise.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion au stockage Adobe, voir <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Création d’une connexion au stockage Adobe</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom du projet</td> 
   <td>Saisissez ou mappez un nom pour le nouveau projet.</td> 
  </tr> 
 </tbody> 
</table>

#### Suppression d’un magasin ESM

Ce module d’action supprime définitivement un magasin ESM existant et toutes ses données associées. Cette action ne peut pas être annulée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion au stockage Adobe, voir <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Création d’une connexion au stockage Adobe</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de magasin</td> 
   <td>Saisissez ou mappez l’identifiant du magasin que vous souhaitez supprimer.</td> 
  </tr> 
 </tbody> 
</table>

#### Ignorer un magasin ESM

Ce module d’action marque un magasin EMS pour suppression, ce qui permet une période de grâce avant une suppression définitive.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion au stockage Adobe, voir <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Création d’une connexion au stockage Adobe</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de magasin</td> 
   <td>Saisissez ou mappez l’ID du magasin que vous souhaitez ignorer.</td> 
  </tr> 
 </tbody> 
</table>

#### Restaurer un magasin ESM

Ce module d’action récupère un magasin ESM supprimé précédemment et restaure l’accès à ses données et configurations.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion au stockage Adobe, voir <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Création d’une connexion au stockage Adobe</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de magasin</td> 
   <td>Saisissez ou mappez l’identifiant du magasin que vous souhaitez restaurer.</td> 
  </tr> 
 </tbody> 
</table>

### Invitations

#### Inviter un utilisateur

Ce module d&#39;action envoie une invitation afin d&#39;accorder à un nouvel utilisateur l&#39;accès à une boutique ESM spécifique, ce qui permet la collaboration et la gestion de fichiers.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion</td> 
   <td>Pour obtenir des instructions sur la création d’une connexion au stockage Adobe, voir <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Création d’une connexion au stockage Adobe</a> dans cet article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adresse e-mail</td> 
   <td>Saisissez ou mappez l’adresse e-mail de l’utilisateur que vous souhaitez inviter à rejoindre le magasin.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de ressource</td> 
   <td>Saisissez ou mappez l’identifiant de la ressource à laquelle vous souhaitez inviter l’utilisateur.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Rôle</td> 
   <td>Sélectionnez le rôle que vous souhaitez attribuer à l’utilisateur nouvellement invité pour la ressource.<ul><li>Propriétaire</li><li>Éditeur</li><li>Observateur</li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">Peut réaliser des commentaires</td> 
   <td>Activez cette option pour permettre à l’utilisateur de commenter la ressource.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Peut partager</td> 
   <td>Activez cette option pour permettre à l’utilisateur de partager la ressource avec d’autres utilisateurs.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Acceptation obligatoire</td> 
   <td>Activez cette option pour vous assurer que l’utilisateur doit accepter l’invitation avant de pouvoir collaborer sur la ressource.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Utiliser les montages</td> 
   <td>Activez cette option si un point de montage vers la ressource doit être créé pour l’invité. L’option Acceptation obligatoire doit être activée pour activer cette option.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type de notification</td> 
   <td>Saisissez ou mappez le type de notification Adobe que vous souhaitez utiliser pour avertir l’utilisateur ou l’utilisatrice de l’invitation. Si ce champ n’est pas renseigné, le type de notification est basé sur le type MIME de la ressource.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom du modèle</td> 
   <td>Saisissez ou mappez l’ID Adobe Post Office du modèle que vous souhaitez utiliser pour l’e-mail d’invitation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Paramètre local</td> 
   <td>Saisissez les paramètres régionaux de l’utilisateur sous la forme d’un code de langue et d’un code de pays. <p>Exemple : <code>en-us</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Externe</td> 
   <td>Définissez cette option sur true si vous souhaitez envoyer des notifications à l’aide d’un système externe au service d’invitations Adobe. La notification externe est prise en charge uniquement lorsque l’acceptation n’est pas obligatoire.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type de ressource</td> 
   <td>Saisissez ou mappez le type de ressource.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Message</td> 
   <td>Saisissez ou mappez un message à inclure dans l’e-mail d’invitation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL cible</td> 
   <td>Saisissez ou mappez l’URL que l’invité peut utiliser pour afficher la ressource.</td> 
  </tr> 
 </tbody> 
</table>

### Autre

#### Effectuer un appel API personnalisé.

Ce module d’action effectue une requête HTTP personnalisée à l’API de stockage Adobe.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connexion</td>
   <td>Pour obtenir des instructions sur la création d’une connexion au stockage Adobe, voir <a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >Création d’une connexion au stockage Adobe</a> dans cet article.</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>URL</p>
      </td>
      <td>
        <p>Saisir un chemin relatif à <code>https://ccprojects.adobe.io/api/v3/.</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Méthode</p>
      </td>
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">En-têtes</td>
      <td>
        <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p>
        <p>Par exemple, <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] ajoute automatiquement des en-têtes d’autorisation et des en-têtes x-api-key.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Chaîne de requête  </td>
      <td>
        <p>Saisissez la chaîne de requête.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Corps</td>
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lors de l’utilisation d’instructions conditionnelles telles que <code>if</code> dans votre fichier JSON, placez les guillemets en dehors de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>



