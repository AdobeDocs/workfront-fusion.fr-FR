---
title: Modules Adobe Experience Manager Forms
description: Avec le connecteur  [!DNL Adobe Experience Manager Forms]  pour compte  [!DNL Adobe Workfront Fusion], you can start a scenario based on events in your [!DNL Adobe Experience Manager Forms] , créez, chargez et mettez à jour des ressources, et copiez ou déplacez des dossiers et des ressources.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: e0d7a655-1353-4d24-83d4-7da73d859a63
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 76%

---

# Modules [!DNL Adobe Experience Manager Forms]

Avec le conecteur [!DNL Adobe Experience Manager Forms] pour [!DNL Adobe Workfront Fusion], vous pouvez démarrer un scénario en fonction des événements de votre compte [!DNL Adobe Experience Manager Forms] en créant un webhook.

Vous pouvez configurer un formulaire dans [!DNL Adobe Experience Manager Forms] pour envoyer des soumissions de formulaire à ce webhook.

## Conditions d’accès

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] formule*</td>
  <td> <p>[!UICONTROL Pro] ou une version ultérieure</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licence*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licence**</td> 
   <td>
   <p>Exigences de licence actuelles : aucune exigence de licence [!DNL Workfront Fusion] requise.</p>
   <p>Ou</p>
   <p>Ancienne exigence de licence : [!UICONTROL [!DNL Workfront Fusion] pour l’automatisation et l’intégration du travail] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Exigences actuelles du produit : si vous disposez du plan de [!DNL Adobe Workfront] [!UICONTROL Select] ou [!UICONTROL Prime], votre entreprise doit acheter du [!DNL Adobe Workfront Fusion] et [!DNL Adobe Workfront] utiliser les fonctionnalités décrites dans cet article. [!DNL Workfront Fusion] est inclus dans le plan de [!DNL Workfront] [!UICONTROL Ultimate].</p>
   <p>Ou</p>
   <p>Exigences liées aux produits hérités : votre entreprise doit acheter [!DNL Adobe Workfront Fusion] ainsi qu’[!DNL Adobe Workfront] pour utiliser la fonctionnalité décrite dans cet article.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Pour connaître la formule, le type de licence ou l’accès dont vous disposez, contactez votre équipe d’administration [!DNL Workfront].

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Conditions préalables

* Vous devez disposer d’un compte [!DNL Adobe Experience Manager Forms] pour utiliser ce module.

## Informations sur l’API Adobe Experience Manager Assets

Le connecteur Adobe Experience Manager Assets utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.2.27</td> 
  </tr>
 </tbody> 
 </table>

## Créer une connexion à Adobe Experience Manager Forms

Pour créer une connexion pour vos modules [!DNL Adobe Experience Manager Forms] :

1. Cliquez sur **[!UICONTROL Add]** en regard de la zone Connexion .

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
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>
          <p>Indiquez si cette connexion se connecte à un environnement de production ou hors production.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>
          <p>Indiquez si ce compte est un compte de service ou un compte personnel.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Instance URL without a trailing slash]</td>
        <td>
          <p>Saisissez l’URL d’accès au compte, sans la barre oblique finale.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL IMS endpoint]</td>
        <td>
          <p><code>https://ims-na1.adobelogin.com</code></p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Saisissez votre ID client [!DNL Adobe]. Pour plus d'informations, consultez la section [!UICONTROL Credentials details] de la [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Saisissez votre secret client [!DNL Adobe]. Pour plus d'informations, consultez la section [!UICONTROL Credentials details] de la [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Org ID]</td>
        <td>Saisissez votre ID d’organisation [!DNL Adobe]. Pour plus d'informations, consultez la section [!UICONTROL Credentials details] de la [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Technical account ID]</td>
        <td>Saisissez l’ID de votre compte technique [!DNL Adobe]. Pour plus d'informations, consultez la section [!UICONTROL Credentials details] de la [!DNL Adobe Developer Console].
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Meta Scopes]</td>
        <td>Saisissez les portées méta appropriées.       </td>
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

1. Cliquez sur **[!UICONTROL Continue]** pour enregistrer la connexion et revenir au module .

## Module Adobe Experience Manager Forms et ses champs

Actuellement, il n’existe qu’un seul module dans le connecteur Adobe Experience Manager Forms.

### Regarder des événements de formulaire

Ce déclencheur instantané (webhook) vous permet de lancer un scénario lorsqu’une action Envoyer se produit sur un formulaire Adobe Experience Manager.

>[!IMPORTANT]
>
>Ce module nécessite également une configuration dans Adobe Experience Manager. Après avoir configuré ce webhook, vous devez ouvrir Adobe Experience Manager et configurer votre formulaire pour envoyer des soumissions au webhook.
>
><!--For instructions on the required form configuration, see insert url here-->

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name]</td> 
   <td> <p>Saisissez un nom pour le webhook.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Adobe Experience Manager] à [!DNL Workfront Fusion], consultez <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/aem-forms-modules.md#create-a-connection-to-adobe-experience-manager-forms" class="MCXref xref">Créer une connexion à [!DNL Adobe Experience Manager Forms]</a>.</p> </td> 
  </tr>

Le module crée un webhook et vous donne l’adresse du webhook, que vous pouvez entrer dans la boîte de dialogue d’envoi du formulaire dans [!DNL Adobe Experience Manager Forms].
