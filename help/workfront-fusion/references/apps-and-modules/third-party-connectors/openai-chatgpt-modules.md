---
title: Modules OpenAI (ChatGPT)
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent OpenAI (ChatGPT), et le connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: c8138d82-fa5a-4e69-b3cb-aa232099cb33
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1240'
ht-degree: 93%

---

# Modules [!DNL OpenAI (ChatGPT & DALL-E)]

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!DNL OpenAI (ChatGPT & DALL-E)] et le connecter à plusieurs applications et services tiers.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <td> <p>[!UICONTROL [!DNL Workfront Fusion] pour l’automatisation et l’intégration du travail] </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>Votre entreprise doit acheter [!DNL Adobe Workfront Fusion] ainsi qu’[!DNL Adobe Workfront] pour utiliser les fonctionnalités décrites dans cet article.</td> 
  </tr> 
 </tbody> 
</table>

Pour connaître le plan, le type de licence ou l’accès dont vous disposez, contactez votre administrateur ou administratrice [!DNL Workfront].

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Conditions préalables

Pour utiliser les modules [!DNL OpenAI (ChatGPT & DALL-E)], vous devez disposer d’un compte [!DNL OpenAI] ainsi que d’une clé API et d’un ID d’organisation.

## Informations sur l’API OpenAI (ChatGPT et DALL-E)

Le connecteur OpenAI (ChatGPT et DALL-E) utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Version de l’API</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.11.1</td> 
  </tr>
 </tbody> 
 </table>

## Connexion d’[!DNL OpenAI (ChatGPT & DALL-E)] à [!DNL Workfront Fusion]

Vous pouvez créer une connexion à votre compte [!DNL OpenAI (ChatGPT & DALL-E)] directement à partir d’un module [!DNL OpenAI (ChatGPT & DALL-E)].

1. Dans n’importe quel module de [!DNL OpenAI (ChatGPT & DALL-E)], cliquez sur **[!UICONTROL Add]** en regard du champ [!UICONTROL Connection] .
1. Saisissez les informations suivantes :

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td> <p>Saisissez un nom pour la nouvelle connexion.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API Key]</td> 
      <td>Vous pouvez trouver votre clé API dans vos paramètres d’utilisateur ou d’utilisatrice d’OpenAI.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Organization ID] </td> 
      <td>Vous pouvez trouver l’ID de votre organisation sur la page des paramètres de votre organisation dans OpenAI.</td> 
     </tr> 
    </tbody> 
   </table>

1. Cliquez sur **[!UICONTROL Continue]** pour créer la connexion et revenir au module .


## Modules [!DNL OpenAI (ChatGPT & DALL-E)] et leurs champs

Lorsque vous configurez les modules [!DNL OpenAI (ChatGPT & DALL-E)], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL OpenAI (ChatGPT & DALL-E)] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Créer un achèvement

>[!IMPORTANT]
>
>Ce module est obsolète.

<!--

This action module creates a completion for the provided prompt or chat.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL OpenAI (ChatGPT & DALL-E)] account to Workfront Fusion, see <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connecting [!DNL OpenAI (ChatGPT & DALL-E)] to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> Enter or map the ID of the model to use. You can use the Get models module to see all of your available models. </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Temperature]</td> 
   <td> This value must be between 0 and 2, and determines the randomness of the output. Higher values produce output that is more random, while lower values produce more focused output. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>For information about the optional advanced settings in this module, see the information about creating completions in the <a href="https://platform.openai.com/docs/api-reference/completions/create" class="MCXref xref">OpenAI API documentation</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

-->

### Créer une modération

Ce module d’action détermine si un texte viole la politique de confidentialité d’OpenAI.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL OpenAI (ChatGPT & DALL-E)] à Workfront Fusion, consultez <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connexion d’[!DNL OpenAI (ChatGPT & DALL-E)] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input]</td> 
   <td> Pour chaque échantillon de texte que vous souhaitez inclure, cliquez sur <b>Ajouter un élément</b> et saisissez ou mappez le texte. Incluez l’intégralité de l’exemple de texte.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> Saisissez ou mappez l’ID du modèle à utiliser. Vous pouvez utiliser le module Obtenir des modèles pour voir tous les modèles disponibles. </td> 
  </tr> 
 </tbody> 
</table>

### Créer une modification

Ce module d’action renvoie une version modifiée d’une invite que vous avez fournie, en suivant vos instructions.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL OpenAI (ChatGPT & DALL-E)] à Workfront Fusion, consultez <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connexion d’[!DNL OpenAI (ChatGPT & DALL-E)] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> Saisissez ou mappez l’ID du modèle à utiliser. Vous pouvez utiliser le module Obtenir des modèles pour voir tous les modèles disponibles. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input]</td> 
   <td> Saisissez ou mappez le texte que vous souhaitez modifier. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Instruction]</td> 
   <td> Saisissez ou mappez les instructions relatives à la modification. Exemple : « Corrigez les fautes d’orthographe ». </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>Pour plus d’informations sur les paramètres avancés facultatifs de ce module, voir les informations sur la création de modifications dans la <a href="https://platform.openai.com/docs/api-reference/edits/create" class="MCXref xref">documentation de l’API OpenAI</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Créer une incorporation

Ce module d’action crée un vecteur d’incorporation représentant le texte d’entrée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL OpenAI (ChatGPT & DALL-E)] à Workfront Fusion, consultez <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connexion d’[!DNL OpenAI (ChatGPT & DALL-E)] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> Saisissez ou mappez l’ID du modèle à utiliser. Vous pouvez utiliser le module Obtenir des modèles pour voir tous les modèles disponibles. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input text to embed]</td> 
   <td> Saisissez ou mappez le texte que vous souhaitez incorporer. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User ID]</td> 
   <td> Saisissez ou mappez un identifiant unique représentant votre utilisateur final ou utilisatrice finale, qui peut aider OpenAI à surveiller et à détecter les abus. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> Saisissez ou mappez le nombre maximum de modifications que vous souhaitez voir prises en charge par le module lors de chaque cycle d’exécution de scénario.</td> 
  </tr> 
 </tbody> 
</table>

### Créer un achèvement de chat

Si l’on considère une liste de messages décrivant une conversation, ce module d’action renvoie une réponse.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL OpenAI (ChatGPT & DALL-E)] à Workfront Fusion, consultez <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connexion d’[!DNL OpenAI (ChatGPT & DALL-E)] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> Saisissez ou mappez l’ID du modèle à utiliser. Vous pouvez utiliser le module Obtenir des modèles pour voir tous les modèles disponibles. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Messages]</td> 
   <td>Les messages décrivent la conversation jusqu’à présent. Pour chaque message que vous souhaitez ajouter, cliquez sur <b>Ajouter un élément</b> et remplissez les champs suivants :
   <ul>
   <li> <b>Rôle</b> : sélectionnez le rôle de l’auteur ou de l’autrice de ce message.</li>
   <li> <b>Contenu</b> : saisissez ou mappez le contenu de ce message.</li>
   <li> <b>Nom</b> : entrez ou mappez le nom de l’auteur ou de l’autrice de ce message. Le nom peut contenir des lettres majuscules et minuscules, des chiffres et des traits de soulignement. La longueur maximale du nom est de 64 caractères.</li>
   </ul>
    </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>Pour plus d’informations sur les paramètres avancés facultatifs de ce module, voir les informations sur la création d’achèvements de chat dans la <a href="https://platform.openai.com/docs/api-reference/chat/create" class="MCXref xref">documentation de l’API OpenAI</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--

### Edit image

This action module makes edits or creates variations of existing images.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL OpenAI (ChatGPT & DALL-E)] account to Workfront Fusion, see <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connecting [!DNL OpenAI (ChatGPT & DALL-E)] to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the operation]</td> 
   <td> Select whether you want to create edits or variations of the image.
   <p>NOTE: Images must be a valid PNG file, less than 4MB, and square. If mask is not provided, the image must have transparency, which will be used as the mask.</p> 
 </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Select a source file from a previous module, or map the source file's name and data.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Text description of desired image]</td> 
   <td> <p>If editing an image, enter or map a description of the edits you want to create. Maximum length is 1000 characters.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>For information about the optional advanced settings in this module, see the information about creating image edits or variations in the <a href="https://platform.openai.com/docs/api-reference/images/createEdit" class="MCXref xref">OpenAI API documentation</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

-->

### Générer des images

Ce module d’action génère ou manipule des images avec des modèles Dall-E.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL OpenAI (ChatGPT & DALL-E)] à Workfront Fusion, consultez <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connexion d’[!DNL OpenAI (ChatGPT & DALL-E)] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text description of the desire image]</td> 
   <td> Saisissez ou mappez une description de l’image souhaitée. La longueur maximale de la description est de 1 000 caractères. 
 </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>Pour plus d’informations sur les paramètres avancés facultatifs de ce module, voir les informations sur la création d’images dans la <a href="https://platform.openai.com/docs/api-reference/images/create" class="MCXref xref">documentation de l’API OpenAI</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Obtenir des modèles

Ce module énumère et décrit les différents modèles disponibles dans l’API OpenAI.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL OpenAI (ChatGPT & DALL-E)] à Workfront Fusion, consultez <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connexion d’[!DNL OpenAI (ChatGPT & DALL-E)] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td> Indiquez si vous souhaitez obtenir une liste de tous les modèles ou récupérer un modèle spécifique.
    <ul>
    <li><p><b>Lister les modèles </b></p><p>Cette action répertorie les modèles actuellement disponibles et fournit des informations de base sur chacun d’entre eux, telles que la personne propriétaire et la disponibilité.</p></li>
    <li><p><b>Récupérer le modèle </b></p><p>Saisissez ou mappez l’ID du modèle que vous souhaitez récupérer. </p></li>
   </ul>
 </td> 
  </tr>
 </tbody> 
</table>

### Effectuer un appel API personnalisé

Ce module d’action envoie une requête HTTP personnalisée à l’API OpenAI.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL OpenAI (ChatGPT & DALL-E)] à Workfront Fusion, consultez <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connexion d’[!DNL OpenAI (ChatGPT & DALL-E)] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>Saisir un chemin relatif à <code>https://api.openai.com/v1/</code> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP dans [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion ajoute automatiquement les en-têtes d’autorisation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Ajoutez la requête pour l’appel API sous la forme d’un objet JSON standard.</p> <p>Par exemple : <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre JSON, placez des guillemets à l’extérieur de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

<!--

### Manage Audio

This action modules converts audio to text.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL OpenAI (ChatGPT & DALL-E)] account to Workfront Fusion, see <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connecting [!DNL OpenAI (ChatGPT & DALL-E)] to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the operation]</td> 
   <td> Select whether you want to transcribe the audio into the input language, or into English.
   <p>If transcribing into the input language, you can select the language in this module's advanced settings. </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Select a source file from a previous module, or map the source file's name and data.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> Enter or map the maximum number of edits you want the module to work with during each scenario execution cycle.</td> 
   <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>For information about the optional advanced settings in this module, see the information about creating transcriptions in the <a href="https://platform.openai.com/docs/api-reference/audio/createTranscription" class="MCXref xref">OpenAI API documentation</a>.</p> </td> 
  </tr> 
  </tr> 
 </tbody> 
</table>

-->

### Gérer les fichiers

Ce module d’action permet de répertorier, de supprimer ou de récupérer des fichiers ou un contenu de fichier.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL OpenAI (ChatGPT & DALL-E)] à Workfront Fusion, consultez <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connexion d’[!DNL OpenAI (ChatGPT & DALL-E)] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td> Sélectionnez l’action que vous souhaitez effectuer. 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td> Si vous supprimez un fichier, ou si vous récupérez un fichier ou un contenu de fichier, entrez ou mappez l’ID du fichier. 
  </tr> 
</tbody>
</table>

### Gérer les réglages fins

Gérez les traitements de réglage fin pour adapter un modèle à vos données d’apprentissage spécifiques.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL OpenAI (ChatGPT & DALL-E)] à Workfront Fusion, consultez <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connexion d’[!DNL OpenAI (ChatGPT & DALL-E)] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the operation]</td> 
   <td> Sélectionnez l’action que vous souhaitez effectuer.
   <ul>
   <li><p>Affiner un modèle à partir d’un jeu de données</p><p>Saisissez ou mappez une description pour l’image souhaitée.</p>
     <li><p>Obtenir des informations sur un traitement de réglage fin</p><p>Saisissez ou mappez l’identifiant du traitement.</p>
   <li><p>Annuler un traitement de réglage fin</p><p>Saisissez ou mappez l’identifiant du traitement.</p>
   <li><p>Annuler un traitement de réglage fin</p><p>Saisissez ou mappez l’identifiant du traitement.</p>
   <li><p>Obtenir des mises à jour du statut pour un traitement de réglage fin</p><p>Saisissez ou mappez l’ID du traitement et indiquez si vous souhaitez diffuser ces mises à jour en continu.</p>
   <li><p>Supprimer un modèle affiné</p><p>Saisissez ou mappez l’ID du modèle que vous souhaitez supprimer.</p>
 </ul> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td> Si vous supprimez un fichier, ou si vous récupérez un fichier ou un contenu de fichier, entrez ou mappez l’ID du fichier. 
  </tr> 
</tbody>
