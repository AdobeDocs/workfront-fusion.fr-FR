---
title: Module Adobe Authenticator
description: Avec le module Adobe Authenticator, vous pouvez vous connecter à n’importe quel produit Adobe à l’aide d’une API, à l’aide d’une connexion unique.
author: Becky
feature: Workfront Fusion
exl-id: af4da661-eeee-4033-a2bb-a2196e446a3d
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: tm+mt
source-wordcount: '1207'
ht-degree: 65%

---

# Modules Adobe Authenticator

Le module Adobe Authenticator vous permet de vous connecter à n’importe quelle API Adobe à l’aide d’une connexion unique. Cela vous permet de vous connecter plus facilement à des produits Adobe qui n’ont pas encore de connecteur Fusion dédié.

L’avantage des modules HTTP est que vous pouvez créer une connexion, comme dans une application dédiée.

Pour obtenir la liste des API d’Adobe disponibles, voir [API d’Adobe](https://developer.adobe.com/apis). Il se peut que vous ne puissiez utiliser que les API qui vous sont attribuées.

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

* Vous devez avoir accès au produit Adobe auquel vous souhaitez que le module se connecte.
* Vous devez avoir accès à Adobe Developer Console.
* Vous devez disposer d’un projet sur Adobe Developer Console qui inclut l’API à laquelle vous souhaiter connecter le module. Vous pouvez :

   * Créez un projet avec l’API.

     Ou
   * Ajoutez l’API à un projet existant.

  Pour plus d’informations sur la création ou l’ajout d’une API à un projet dans Adobe Developer Console, voir [Créer un projet](https://developer.adobe.com/dep/guides/dev-console/create-project/) dans la documentation Adobe.

## Informations sur l’API Adobe Authenticator

Le connecteur Adobe Authenticator utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.1.4</td> 
  </tr>
 </tbody> 
 </table>

## Créer une connexion

Une connexion Adobe Authenticator se connecte à un seul projet dans Adobe Developer Console. Pour utiliser la même connexion pour plusieurs API Adobe, ajoutez les API au même projet, puis créez une connexion à ce projet.

Vous pouvez créer des connexions distinctes à des projets distincts, mais vous ne pouvez pas utiliser de connexion pour accéder à une API qui ne se trouve pas sur le projet spécifié dans cette connexion.

>[!IMPORTANT]
>
>Avec le connecteur Adobe Authenticator, vous avez le choix entre établir une connexion OAuth serveur à serveur ou une connexion à un compte de service (JWT). Adobe a abandonné les informations d’identification JWT, qui cesseront de fonctionner après le 1er janvier 2025. **Nous vous recommandons donc vivement de créer des connexions OAuth.**
>
>Pour plus d’informations sur ces types de connexions, voir [Authentification serveur à serveur](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/) dans la documentation Adobe.

Pour créer une connexion, procédez comme suit :

1. Dans un module Adobe Authenticator, cliquez sur **Ajouter** en regard du champ Connexion.
1. Remplissez les champs suivants :

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>
          <p>Choisissez si vous souhaitez créer une connexion de serveur à serveur OAuth ou une connexion de compte de service (JWT). Nous vous recommandons vivement de créer des connexions OAuth.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Saisissez un nom pour cette connexion.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Saisissez votre ID client [!DNL Adobe]. Vous pouvez le trouver dans la section [!UICONTROL Credentials details] de l’[!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Saisissez votre secret client [!DNL Adobe]. Vous pouvez le trouver dans la section [!UICONTROL Credentials details] de l’[!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Scopes]</td>
        <td>Si vous avez sélectionné une connexion OAuth, saisissez les portées nécessaires pour cette connexion.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Technical account ID]</td>
        <td>Si vous avez sélectionné une connexion JWT, saisissez votre ID de compte technique [!DNL Adobe]. Vous pouvez le trouver dans la section [!UICONTROL Credentials details] de l’[!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Organization ID]</td>
        <td>Si vous avez sélectionné une connexion JWT, saisissez votre ID d’organisation [!DNL Adobe]. Vous pouvez le trouver dans la section [!UICONTROL Credentials details] de l’[!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Meta Scopes]</td>
        <td>Si vous avez sélectionné une connexion JWT, saisissez les métaportées nécessaires pour cette connexion. </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Private key]</td>
        <td>
          <p>Si vous avez sélectionné une connexion JWT, saisissez la clé privée générée lors de la création de vos informations d’identification dans l’[!DNL Adobe Developer Console]. </p>
          <p>Pour extraire votre clé privée ou votre certificat privé, procédez comme suit :</p>
          <ol>
            <li value="1">
              <p>Cliquez sur <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li value="2">
              <p>Sélectionnez le type de fichier que vous extrayez.</p>
            </li>
            <li value="3">
              <p>Sélectionnez le fichier contenant la clé privée ou le certificat privé.</p>
            </li>
            <li value="4">
              <p>Saisissez le mot de passe du fichier.</p>
            </li>
            <li value="5">
              <p>Cliquez sur <b>[!UICONTROL Save]</b> pour extraire le fichier et revenir à la configuration de la connexion.</p>
            </li>
          </ol>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Base URLs]</td>
        <td>Vous devez ajouter les URL de base que cet authentificateur doit autoriser. Lors de l’utilisation du module « Effectuer un appel API personnalisé » plus loin dans le scénario, vous ajouterez un chemin d’accès relatif à l’URL choisie. En saisissant des URL ici, vous pouvez contrôler à quoi le module Créer un appel API personnalisé peut se connecter, ce qui renforce la sécurité.<p>Pour chaque URL de base que vous souhaitez ajouter à l’authentificateur, cliquez sur <b>Ajouter un élément</b> et saisissez l’URL de base.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Authentication URL]</td>
        <td>Laissez ce champ vide pour utiliser l’URL d’authentification Adobe IMS standard de <code>https://ims-na1.adobelogin.com</code>. Si vous n’utilisez pas Adobe IMS pour l’authentification, saisissez l’URL à utiliser pour l’authentification.</td>
      </tr>
    </tbody>
    </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour enregistrer la connexion et revenir au module.

## Modules

* [Effectuer un appel API personnalisé.](#make-a-custom-api-call)
* [Effectuer un appel API personnalisé (hérité)](#make-a-custom-api-call-legacy)

### Effectuer un appel API personnalisé.

Ce module d’action vous permet d’effectuer un appel vers n’importe quelle API d’Adobe. Il prend en charge les fichiers volumineux, au lieu des corps de texte uniquement.

Ce module a été rendu disponible le 14 novembre 2024. Tout appel Adobe Authenticator > Effectuer un appel API personnalisé configuré avant cette date ne gère pas les fichiers volumineux. Il est désormais considéré comme le module Effectuer un appel API personnalisé (hérité) .

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
     <td role="rowheader">[!UICONTROL Connection]</td>
     <td>Pour obtenir des instructions sur la création d’une connexion au module Adobe Authenticator, voir <a href="#create-a-connection" class="MCXref xref" >Créer une connexion</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Base URL]</p>
      </td>
      <td>
        <p>Saisissez l’URL de base du point API auquel vous souhaitez vous connecter.</p>
      </td>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>Saisissez le chemin d’accès relatif à l’URL de base.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p>
        <p>Par exemple, <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion ajoute automatiquement des en-têtes d’autorisation.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Saisissez la chaîne de requête.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body Type]</td>
   <td> Sélectionnez le type de corps de cette requête API :
   <ul>
   <li>Brut</li>
   <li>application/x-www-form-urlencoded</li>
   <li>multipart/form-data</li>
   </ul>
      </td>
      </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Type de sortie]  </td>
      <td>
        <p>Sélectionnez le type de données que le module doit générer. Si vous ne sélectionnez pas de type, le module en sélectionne un automatiquement.</p>
      </td>
    </tr>
  </tbody>
</table>

### Effectuer un appel API personnalisé (hérité)

Ce module d’action vous permet d’effectuer un appel à n’importe quelle API Adobe.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
     <td role="rowheader">[!UICONTROL Connection]</td>
     <td>Pour obtenir des instructions sur la création d’une connexion au module Adobe Authenticator, voir <a href="#create-a-connection" class="MCXref xref" >Créer une connexion</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Base URL]</p>
      </td>
      <td>
        <p>Saisissez l’URL de base du point API auquel vous souhaitez vous connecter.</p>
      </td>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>Saisissez le chemin d’accès relatif à l’URL de base.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p>
        <p>Par exemple, <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion ajoute automatiquement des en-têtes d’autorisation.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Saisissez la chaîne de requête.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lors de l’utilisation d’instructions conditionnelles telles que <code>if</code> dans votre fichier JSON, placez les guillemets en dehors de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"></p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>
