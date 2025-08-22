---
title: Modules Adobe Target
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent des modules  [!DNL Adobe Target], as well as connect it to multiple third-party applications and services. [!DNL Adobe Target]  vous permettent de créer, lire, mettre à jour ou supprimer des enregistrements, de répertorier tous les enregistrements d’un type donné, de rechercher des enregistrements en fonction des critères que vous spécifiez ou d’effectuer un appel API personnalisé vers l’API  [!DNL Adobe Target] .
author: Becky
feature: Workfront Fusion
exl-id: f3c1ed7b-b69b-478a-8240-1a2ab89e11e5
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2302'
ht-degree: 88%

---

# Modules [!DNL Adobe Target]

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent [!DNL Adobe Target] et les connecter à plusieurs applications et services tiers. Les modules [!DNL Adobe Target] vous permettent de créer, de lire, de mettre à jour ou de supprimer des enregistrements, de répertorier tous les enregistrements d’un type donné, de rechercher des enregistrements en fonction de critères que vous précisez ou d’effectuer un appel API personnalisé à l’API [!DNL Adobe Target].


Si vous avez besoin d’instructions pour créer un scénario, consultez les articles sous [Créer un scénario : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

## Conditions d’accès

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Formule Adobe Workfront*</td>
      <td>
        <p>[!UICONTROL Pro] ou version supérieure</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Licence Adobe Workfront*</td>
      <td>
        <p>[!UICONTROL Plan], [!UICONTROL Work]</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Licence Adobe Workfront Fusion **</td>
      <td>
   <p>Exigence de licence actuelle : aucune exigence de licence Workfront Fusion.</p>
   <p>Ou</p>
   <p>Exigence de licence héritée : [!UICONTROL Workfront Fusion for Work Automation and Integration] </p>
   </td>
    </tr>
    <tr>
      <td role="rowheader">Produit</td>
      <td>
   <p>Configuration requise actuelle du produit : si vous disposez du plan Adobe Workfront [!UICONTROL Select] ou [!UICONTROL Prime], votre entreprise doit acheter Adobe Workfront Fusion ainsi qu’Adobe Workfront pour utiliser les fonctionnalités décrites dans cet article. Workfront Fusion est inclus dans le plan Workfront [!UICONTROL Ultimate].</p>
   <p>Ou</p>
   <p>Exigences de produit héritées : votre entreprise doit acheter Adobe Workfront Fusion ainsi qu’Adobe Workfront pour utiliser les fonctionnalités décrites dans cet article.</p>
   </td>
    </tr>
    </tr>
  </tbody>
</table>


Pour connaître le plan, le type de licence ou l’accès dont vous disposez, contactez votre administrateur ou administratrice Workfront.

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Conditions préalables

Avant d’utiliser le connecteur [!DNL Adobe Target], vous devez vous assurer que les conditions préalables suivantes sont remplies :

* Vous devez disposer d’un compte [!DNL Adobe Target].

## Informations sur l’API Adobe Target

Le connecteur Adobe Target utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.7.33</td> 
  </tr>
 </tbody> 
 </table>

## Créer une connexion à [!DNL Adobe Target]

>[!IMPORTANT]
>
>Les connexions créées après le 3 juin 2024 nécessitent une connexion serveur à serveur Adobe Target.
>
>* Les connexions de compte de service existantes continueront à fonctionner jusqu’en janvier 2025. Vous devez remplacer vos connexions de compte de service par des connexions serveur à serveur Adobe Target avant janvier 2024.
>* Pour créer une connexion serveur à serveur Adobe Target, vous devez faire partie de l’équipe de développement de votre organisation. Le rôle de l’équipe de développement est défini dans Adobe Admin Console.

Pour créer une connexion pour vos modules [!DNL Adobe Target], procédez comme suit :

1. Dans n’importe quel module, cliquez sur **[!UICONTROL Ajouter]** en regard de la zone Connexion .

1. Remplissez les champs suivants :

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Saisissez un nom pour cette connexion.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>Indiquez si vous créez une connexion de compte de service ou de serveur à serveur Adobe Target.<p><b>IMPORTANT : les connexions créées après le 3 juin 2024 nécessitent une connexion serveur à serveur Adobe Target. </b> Les connexions de compte de service existantes continueront à fonctionner jusqu’en janvier 2025. Vous devez remplacer vos connexions de compte de service par des connexions serveur à serveur Adobe Target avant janvier 2024.
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>Indiquez si vous vous connectez à un environnement de production ou hors production.
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>Indiquez si vous vous connectez à un compte de service ou à un compte personnel.
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
        <td role="rowheader">[!UICONTROL Technical account ID]</td>
        <td>Saisissez l’ID de votre compte technique [!DNL Adobe]. Vous pouvez le trouver dans la section [!UICONTROL Credentials details] de l’[!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Organization ID]</td>
        <td>Saisissez votre ID d’organisation [!DNL Adobe]. Vous pouvez le trouver dans la section [!UICONTROL Credentials details] de l’[!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Tenant]</td>
        <td>
          <p> Pour localiser votre locataire, connectez-vous à [!DNL Adobe Experience Cloud], ouvrez [!DNL Target], puis cliquez sur la carte [!DNL Target]. Utilisez la valeur de l’ID de locataire comme indiqué dans le sous-domaine de l’URL.</p>
          <p>Par exemple, si votre URL lors de la connexion à [!DNL Adobe Target] est <code>&lt;https://mycompany.experiencecloud.adobe.com/...></code> alors votre ID de locataire est « mycompany ».</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Meta Scopes]</td>
        <td>Saisir <code>ent_marketing_sdk</code>       </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Private key]</td>
        <td>
          <p>Saisissez la clé privée générée lors de la création de vos informations d’identification dans l’[!DNL Adobe Developer Console]. </p>
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
    </tbody>
    </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour enregistrer la connexion et revenir au module.

## Modules [!DNL Adobe Target] et leurs champs

Lorsque vous configurez les modules [!DNL Adobe Target], Workfront Fusion affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Adobe Target] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Actions](#actions)

* [Recherches](#searches)


### Actions

* [[!UICONTROL Créer un enregistrement]](#create-a-record)

* [[!UICONTROL Effectuer un appel API personnalisé]](#make-a-custom-api-call)

* [[!UICONTROL Supprimer un enregistrement]](#delete-a-record)

* [[!UICONTROL Lire un enregistrement]](#read-a-record)

* [[!UICONTROL Mettre à jour un enregistrement]](#update-a-record)


#### [!UICONTROL Créer un enregistrement]

Ce module d’action crée une activité AB ou XT, une offre ou une audience.

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Connection]</td>
    <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Target], voir <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Créer une connexion à [!DNL Adobe Target]</a> dans cet article.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record type]</td>
    <td>
      <p>Sélectionnez le type d’enregistrement que vous souhaitez créer.</p>
      <ul>
        <li>
        <b>Propriété</b><p>Pour plus de détails sur les champs, voir <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Properties/operation/createProperty">Créer une propriété</a> dans la documentation de l’API Adobe Target.</p>
        </li>
        <li>
        <b>Recommandation d’offre</b><p>Pour plus de détails sur les champs, voir <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Offers/operation/createOffer">Créer une offre de recommandation</a> dans la documentation de l’API Adobe Target.</p>
        </li>
        <li>
          <b>[!UICONTROL Offer JSON]</b>
          <p>Passez à <a href="#offer-fields" class="MCXref xref" >Champs d’offre</a>.</p>
        </li>
        <li>
          <b>[!UICONTROL Offer Content]</b>
          <p>Passez à <a href="#offer-fields" class="MCXref xref" >Champs d’offre</a>.</p>
        </li>
        <li>
        <b>Environnement</b><p>Pour plus de détails sur les champs, voir <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Environments/operation/createEnvironment">Créer un environnement</a> dans la documentation de l’API Adobe Target.</p>
        </li>
        <li>
          <b>[!UICONTROL Audience]</b>
          <p>Pour plus de détails sur les champs, voir <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Audiences/operation/createAudience_1_1">Créer une audience</a> dans la documentation de l’API Adobe Target.</p>
        </li>
        <li>
          <b>[!UICONTROL AB Activity]</b>
          <p>Pour plus de détails sur les champs, voir <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Activities/operation/createActivity_4_1">Créer une activité AB</a> dans la documentation de l’API Adobe Target.</p>
        </li>
        <li>
          <b>[!UICONTROL XT Activity]</b>
          <p>Passez à <a href="#xt-activity-fields" class="MCXref xref" >Champs d’activité XT</a>.</p>
        </li>
        <li>
          <b>[!UICONTROL AP Activity]</b>
          <p>Pour plus de détails sur les champs, voir <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Activities/operation/createActivity_2">Créer une activité AP</a> dans la documentation de l’API Adobe Target.</p>
        </li>
        <li>
          <b>[!UICONTROL Response Token]</b>
          <p>Pour plus de détails sur les champs, voir <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Response-tokens/operation/createResponseToken">Créer un jeton de réponse</a> dans la documentation de l’API Adobe Target.</p>
        </li>
      </ul>
    </td>
  </tr>
</tbody>
</table>

<!--

##### AB Activity fields

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Enter or map a name for this activity. The name can be no more than 250 characters.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Options]</td>
      <td>
        <p>For each option that you want to add to the activity, click <b>[!UICONTROL Add item]</b> and fill in the following fields:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Option local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the option across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Enter or map a name for the option. The name must be no more than 250 characters.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Offer ID]</b>
            </p>
          </li>
          <li>
            <p>Select or map the Offer associated with the option.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Mboxes]</td>
      <td>
        <p>For each Mbox that you want to add to the activity, click <b>[!UICONTROL Add item]</b> and fill in the following fields:</p>
        <ul>
          <li>
            <p>[!UICONTROL Audience IDs]</p>
            <p>For each audience that you want to add to the Mbox, click <b>[!UICONTROL Add item]</b> and select the Audience ID.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Location local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the location across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Enter or map a name for the Location. The name must be no more than 250 characters.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Selectors]</td>
      <td>
        <p>For each selector that you want to add to the activity, click <b>[!UICONTROL Add item]</b> and fill in the following fields:</p>
        <ul>
          <li>
            <p>[!UICONTROL Audience IDs]</p>
            <p>For each audience that you want to add to the Mbox, click <b>[!UICONTROL Add item]</b> and select the Audience ID.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Location local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the location across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Selector]</b>
            </p>
            <p>Enter or map a string to be used to track the location across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Enter or map a name for the Location. The name must be no more than 250 characters.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Experiences]</td>
      <td>
        <p>A list of locations on the page where the content offer is served. A location contains the following:
</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Experience local ID]</b>
            </p>
            <p>Enter or map the ID of the experience</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Enter or map the name of the experience
</p>
          </li>
          <li>
            <p><b>[!DNL Audience IDs]</b>
            </p>
            <p>For each audience that you want to see the experience, click <b>[!UICONTROL Add item]</b> and enter the Audience ID.
</p>
          </li>
          <li>
            <p><b>[!UICONTROL Visitor Percentage]</b>
            </p>
            <p>Enter or map the percentage of visitors that is allocated to the experience</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Metrics]</td>
      <td><p>For details on metrics, see <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Activities/operation/createActivity_4_1">Create AB activity</a> in the Adobe Target API documentation.</p> </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Third Party ID]</td>
      <td>Enter or map an ID to identify this activity. You can choose this ID. This ID must not be the same as another activity, and can be no more than 250 characters.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Starts at]</td>
      <td>Enter or map the date and time to start the activity in the format <code>YYYY-MM-DD hh:mm:ss.z</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ends at]</td>
      <td>Enter or map the date and time to end the activity in the format <code>YYYY-MM-DD hh:mm:ss.z</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL State]</td>
      <td>
        <p>Enter or map the state of the activity.</p>
        <ul>
          <li>
            <p>[!UICONTROL Approved]</p>
          </li>
          <li>
            <p>[!UICONTROL Deactivated]</p>
          </li>
          <li>
            <p>[!UICONTROL Paused]</p>
          </li>
          <li>
            <p>[!UICONTROL Saved] </p>
          </li>
          <li>
            <p>[!UICONTROL Deleted]</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Priority]</td>
      <td>Enter a number that defines the priority of the activity. Higher numbers have higher priority. This value must be between 0 and 999. The default value is 5.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Auto-allocate traffic]</td>
      <td>
        <p>Enable this option to auto-allocate traffic. Auto-allocating sends more traffic to the more successful experience.</p>
        <p>Select or map the evaluation criteria by which to judge which experience is more successful.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Enter or map the workspace that the activity is associated with</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Property IDs] </td>
      <td>For each property that you want to add to the activity, click <b>[!UICONTROL Add item]</b> and select or map the property's ID.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Reporting audiences]</td>
      <td>
        <p>For each reporting audience that you want to add to the activity, click [!UICONTROL Add item] and enter the following information:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Reporting Audience local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the Reporting Audience across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Audience ID]</b>
            </p>
            <p>Enter or map the Segment to be used in reporting</p>
          </li>
          <li>
            <p><b>[!UICONTROL Metric local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the metric across API requests.</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

-->

##### Champs d’activité XT

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Saisissez ou mappez un nom pour cette activité. Le nom ne peut pas dépasser 250 caractères.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Options]</td>
      <td>
        <p>Pour chaque option à ajouter à l’activité, cliquez sur <b>[!UICONTROL Add item]</b> et renseignez les champs suivants :</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Option local ID]</b>
            </p>
            <p>Saisissez ou mappez une chaîne à utiliser pour effectuer le suivi de l’option dans les requêtes d’API.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Saisissez ou mappez un nom pour l’option. Le nom ne doit pas dépasser 250 caractères.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Offer ID]</b>
            </p>
          </li>
          <li>
            <p>Sélectionnez ou mappez l’offre associée à l’option.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Locations]</td>
      <td>
        <p>Pour chaque mBox à ajouter à l’activité, cliquez sur <b>[!UICONTROL Add item]</b> et renseignez les champs suivants :</p>
        <ul>
          <li>
            <p>[!UICONTROL Audience IDs]</p>
            <p>Pour chaque audience à ajouter au fichier mbox, cliquez sur <b>[!UICONTROL Add item]</b> et sélectionnez l’identifiant d’audience.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Location local ID]</b>
            </p>
            <p>Saisissez ou mappez une chaîne à utiliser pour effectuer le suivi de l’emplacement dans les requêtes d’API.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Saisissez ou mappez un nom pour l’emplacement. Le nom ne doit pas dépasser 250 caractères.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Experiences]</td>
      <td>
        <p>Liste des emplacements sur la page où l’offre de contenu est diffusée. Un emplacement contient les éléments suivants :
</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Experience local ID]</b>
            </p>
            <p>Saisissez ou mappez l’ID de l’expérience.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Saisissez ou mappez le nom de l’expérience.

</p>
          </li>
          <li>
            <p><b>[!DNL Audience IDs]</b>
            </p>
            <p>Pour chaque audience dont vous souhaitez voir l’expérience, cliquez sur <b>[!UICONTROL Add item]</b> et saisissez l’identifiant d’audience.

</p>
          </li>
          <li>
            <p><b>[!UICONTROL Visitor Percentage]</b>
            </p>
            <p>Saisissez ou mappez le pourcentage de visiteurs et visiteuses affecté à l’expérience.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Metrics]</td>
      <td> </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Third Party ID]</td>
      <td>Saisissez ou mappez un identifiant pour identifier cette activité. Vous pouvez choisir cet identifiant. Cet identifiant ne doit pas être identique à une autre activité et ne peut pas dépasser 250 caractères.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Starts at]</td>
      <td>Saisissez ou mappez la date et l’heure de début de l’activité au format <code>YYYY-MM-DD hh:mm:ss.z</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ends at]</td>
      <td>Saisissez ou mappez la date et l’heure de fin de l’activité au format <code>YYYY-MM-DD hh:mm:ss.z</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL State]</td>
      <td>
        <p>Saisissez ou mappez l’état de l’activité.</p>
        <ul>
          <li>
            <p>[!UICONTROL Approved]</p>
          </li>
          <li>
            <p>[!UICONTROL Deactivated]</p>
          </li>
          <li>
            <p>[!UICONTROL Paused]</p>
          </li>
          <li>
            <p>[!UICONTROL Saved] </p>
          </li>
          <li>
            <p>[!UICONTROL Deleted]</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Priority]</td>
      <td>Saisissez un nombre qui définit la priorité de l’activité. Les nombres plus élevés ont une priorité plus élevée. Cette valeur doit être comprise entre 0 et 999. La valeur par défaut est 5.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Auto-allocate traffic]</td>
      <td>
        <p>Activez cette option pour affecter automatiquement le trafic. L’affectation automatique envoie plus de trafic vers l’expérience la plus performante.</p>
        <p>Sélectionnez ou mappez les critères d’évaluation selon lesquels vous souhaitez juger quelle expérience est la plus réussie.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Saisissez ou mappez l’espace de travail auquel l’activité est associée.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Property IDs] </td>
      <td>Pour chaque propriété à ajouter à l’activité, cliquez sur <b>[!UICONTROL Add item]</b> et sélectionnez ou mappez l’ID de la propriété.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Reporting audiences]</td>
      <td>
        <p>Pour chaque audience de création de rapports à ajouter à l’activité, cliquez sur [!UICONTROL Add item] et saisissez les informations suivantes :</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Reporting Audience local ID]</b>
            </p>
            <p>Saisissez ou mappez une chaîne à utiliser pour effectuer le suivi de l’audience de création de rapports dans les requêtes d’API.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Audience ID]</b>
            </p>
            <p>Saisissez ou mappez le segment à utiliser dans les rapports.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Metric local ID]</b>
            </p>
            <p>Saisissez ou mappez une chaîne à utiliser pour effectuer le suivi de la mesure dans les requêtes d’API.</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

##### Champs d’offre

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Saisissez ou mappez un nom pour cette activité. Le nom ne peut pas dépasser 250 caractères.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Content]</td>
      <td>
        <p>Saisissez ou mappez le contenu de l’offre qui sera présentée à l’utilisateur ou à l’utilisatrice.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>
        <p>Saisissez ou mappez l’ID de l’espace de travail associé à l’offre. Si rien n’est indiqué, l’offre est associée à l’espace de travail par défaut du compte. Cette fonctionnalité s’applique uniquement aux comptes [!DNL Target] Premium.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>
        <p>Saisissez ou mappez la date et l’heure de modification de cette offre.</p>
      </td>
    </tr>
  </tbody>
</table>

<!--

##### Audience fields

>[!NOTE]
>
>Audiences created through Workfront Fusion can only be edit in Fusion or through the API. They cannot be edited from within Target.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Enter or map a name for this audience. The name can be no more than 250 characters.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Description]</td>
      <td>
        <p>Enter or map a description of this audience.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Origin]</td>
      <td>
        <p>Select whether this audience's origin is from Target or from the cloud.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Target Rule]</td>
      <td>
        <p>Enable the toggle to make rules AND, that is, all rules must be applied.</p>
        <p>For each rule that you want to apply to the audience, click <b>[!UICONTROL Add item]</b> and enter the JSON of the rule you want to apply. </p>
        <div class="example"><span class="autonumber"><span><b>Example: </b></span></span>
          <p>Example 1:</p>
          <p ><code>&lbrace;</code></p>
                    <p ><code>                "page": "url",</code>
                    </p>
                    <p><code>                "equals":&lbrack;</code>
                    </p>
                    <p ><code>                    "http://www.myhomepage.com/"</code>
                    </p>
                    <p><code>                &rbrack;</code>
                    </p>
                    <p ><code>            &rbrace;,</code>
                    </p>
                    <p>Example 2</p>
                    <p ><code>            &lbrace;</code>
                    </p>
                    <p><code>                "geo": "region",</code>
                    </p>
                    <p><code>                "matches": &lbrack;</code>
                    </p>
                    <p ><code>                    "california"</code>
                    </p>
                    <p ><code>                &rbrack;</code>
                    </p>
                    <p ><code>            &rbrace;</code>
                    </p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>
        <p>Enter or map the ID of the workspace associated with the audience. If left blank, the offer is associated with the default workspace of the account. This functionality applies only to [!DNL Target Premium] accounts.</p>
      </td>
    </tr>
  </tbody>
</table>

-->

#### [!UICONTROL Effectuer un appel d’API personnalisé]

Ce module effectue un appel API personnalisé à l’API [!DNL Adobe Target].

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Target], voir <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Créer une connexion à [!DNL Adobe Target]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL [!DNL Target] Base URL]</td>
      <td>Saisissez ou mappez vos URL de base [!DNL Target].</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Path]</p>
      </td>
      <td>
        <p>Saisissez un chemin relatif à {baseURL}.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p>
        <p>Par exemple, <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion ajoute automatiquement des en-têtes d’autorisation et des en-têtes x-api-key.</p>
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
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

#### [!UICONTROL Supprimer un enregistrement]

Ce module d’action supprime une seule activité AB, une seule activité XT, une seule offre ou une seule audience.

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Connection]</td>
    <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Target], voir <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Créer une connexion à [!DNL Adobe Target]</a> dans cet article.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record type]</td>
    <td>Sélectionnez le type d’enregistrement que vous souhaitez supprimer.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record ID]</td>
    <td>Saisissez ou mappez l’identifiant de l’enregistrement que vous souhaitez supprimer.</td>
  </tr>
</tbody>
</table>

#### [!UICONTROL Lire un enregistrement]

Ce module d’action récupère les données d’une seule activité, offre, audience, propriété ou d’un seul rapport.

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Connection]</td>
    <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Target], voir <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Créer une connexion à [!DNL Adobe Target]</a> dans cet article.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record type]</td>
    <td>Sélectionnez le type d’enregistrement à lire.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record ID]</td>
    <td>Saisissez ou mappez l’ID de l’enregistrement à lire.</td>
  </tr>
</tbody>
</table>

#### [!UICONTROL Mettre à jour un enregistrement]

Ce module d’action met à jour un enregistrement dans Target.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Target], voir <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Créer une connexion à [!DNL Adobe Target]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>
        <p>Sélectionnez le type d’enregistrement que vous souhaitez mettre à jour.</p>
       </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Field names]</td>
      <td>Sélectionnez les champs que vous souhaitez mettre à jour. Les champs apparaissent en dessous.
          <p>Pour plus de détails sur les champs, voir la <a href="https://developer.adobe.com/target/administer/admin-api/">documentation de l’API Adobe Target</a>.</p>
      </td>
    </tr>
  </tbody>
</table>

### Recherches

* [[!UICONTROL Obtenir des enregistrements]](#get-records)

* [[!UICONTROL Rechercher]](#search)


#### [!UICONTROL Obtenir des enregistrements]

Ce module de recherche récupère une liste d’enregistrements du type sélectionné.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Target], voir <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Créer une connexion à [!DNL Adobe Target]</a> dans cet article.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>Sélectionnez le type d’enregistrement à mettre à jour.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Sort by]</td>
      <td>Pour chaque champ de tri, cliquez sur <b>[!UICONTROL Add item]</b>, sélectionnez le champ et indiquez si les résultats renvoyés doivent être classés par ordre croissant ou décroissant.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Starts At]</td>
      <td>
        <p>Saisissez la date la plus ancienne pour laquelle vous souhaitez récupérer les enregistrements. </p>
        <p>Pour obtenir la liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercition</a>.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ends At]</td>
      <td>
        <p>Saisissez la date la plus récente pour laquelle vous souhaitez récupérer les enregistrements. </p>
        <p>Pour obtenir la liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercition</a>.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Rechercher]

Ce module de recherche permet de rechercher des activités, des offres ou des audiences en fonction des critères que vous avez spécifiés.

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Connection]</td>
    <td>Pour obtenir des instructions sur la création d’une connexion à [!DNL Adobe Target], voir <a href="#create-a-connection-to-adobe-target" class="MCXref xref" >Créer une connexion à [!DNL Adobe Target]</a> dans cet article.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record type]</td>
    <td>Sélectionnez le type d’enregistrement à mettre à jour.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Sort by]</td>
    <td>Pour chaque champ de tri, cliquez sur <b>[!UICONTROL Add item]</b>, sélectionnez le champ et indiquez si les résultats renvoyés doivent être classés par ordre croissant ou décroissant.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Search criteria]</td>
    <td>Pour chaque règle à configurer, sélectionnez le champ, l’opérateur et la valeur. Cliquez sur <b>[!UICONTROL Add AND rule]</b> pour créer des règles supplémentaires.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Offset]</td>
    <td>
      <p>Saisissez le numéro de la première réponse que le module doit renvoyer. La première réponse renvoyée comporte un décalage de <code>0</code>. Utilisez ce champ en combinaison avec le champ [!UICONTROL Maximum number of returned results] pour paginer les réponses.</p>
      <p>Par exemple, pour afficher la troisième page de réponses, lorsque chaque page contient dix réponses, réglez [!UICONTROL Offset] sur 20 et le [!UICONTROL Maximum number of returned] de résultats sur 10.</p>
    </td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Limit]</td>
    <td>
      <p>Saisissez ou mappez le nombre maximal d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario. Utilisez ce champ conjointement au champ [!UICONTROL Offset] pour paginer les réponses.</p>
      <p>Par exemple, pour afficher la troisième page de réponses, lorsque chaque page contient dix réponses, réglez [!UICONTROL Offset] sur 20 et le [!UICONTROL Maximum number of returned] de résultats sur 10.</p>
    </td>
  </tr>
</tbody>
</table>
