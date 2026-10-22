---
title: Modules MCP Adobe Fusion
description: Avec le module MCP d’Adobe Fusion, vous pouvez envoyer une invite en anglais clair au serveur MCP d’Adobe Fusion et laisser un modèle d’IA effectuer la requête.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 06ba1c54288fff09f866bffa5c3fce7381c71ad2
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 16%
---
# Modules MCP Adobe Fusion

Le connecteur MCP Adobe Fusion envoie une invite en anglais brut au serveur MCP (Adobe Fusion Model Context Protocol). Un modèle d’IA interprète votre requête et appelle les outils Fusion nécessaires pour la terminer.

Le connecteur fonctionne uniquement avec le serveur MCP Adobe Fusion hébergé. Vous ne pouvez pas le pointer vers un autre serveur MCP.

Pour plus d’informations sur MCP dans les scénarios Fusion, voir [Ajouter une invite d’IA à votre scénario](/help/workfront-fusion/create-scenarios/add-modules/add-an-ai-prompt-to-your-scenario.md).

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tout package de workflow Adobe Workfront et tout package d’automatisation et d’intégration Adobe Workfront</p><p>Workfront Ultimate</p><p>Packages Workfront Prime et Select, avec l’achat supplémentaire de Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licences Adobe Workfront</td> 
   <td> <p>Standard</p><p>Travail ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Si votre organisation dispose d’un package Workfront Select ou Prime qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acquérir Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation Workfront](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Connexion d’Adobe Fusion MCP à Workfront Fusion

Vous pouvez créer une connexion directement depuis le module MCP d’Adobe Fusion.

1. Dans le module MCP d’Adobe Fusion, cliquez sur **[!UICONTROL Ajouter]** en regard du champ **Connexion**.
1. Remplissez les champs suivants :

   <table style="table-layout:auto">
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">Nom de la connexion</td>
        <td>
          <p>Saisissez un nom pour cette connexion.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Environnement</td>
        <td>
          <p>Indiquez si vous vous connectez à un environnement de production ou hors production.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Type</td>
        <td>
          <p>Indiquez si vous vous connectez à un compte de service ou à un compte personnel.</p>
        </td>
      </tr>
    </tbody>
   </table>

1. Cliquez sur **[!UICONTROL Continuer]**.

Vous êtes redirigé vers la page de connexion d’Adobe. Connectez-vous avec votre compte Adobe et approuvez l’accès. Vous êtes redirigé vers Workfront Fusion et la nouvelle connexion est disponible dans le module .

## Module MCP Adobe Fusion et ses champs

### Traiter une invite utilisateur

Ce module d’action envoie une invite en anglais clair au serveur MCP d’Adobe Fusion. Un modèle d’IA interprète l’invite, appelle les outils Fusion nécessaires pour la terminer et renvoie le résultat.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>Clé LLM <i>(facultative, avancée)</i></td> 
   <td> <p>Par défaut, ce module traite votre invite à l’aide d’Adobe Managed AI et vous n’avez pas besoin de sélectionner de clé.</p> <p>Pour utiliser votre propre fournisseur d’IA à la place, sélectionnez une clé LLM existante ou créez-en une en cliquant sur <b>Ajouter</b> et saisissez les informations suivantes :</p>
     <ul>
       <li><b>Nom de la clé</b> : saisissez le nom de la nouvelle clé.</li>
       <li><b>LLM</b> : sélectionnez le modèle de langue volumineux auquel cette clé est associée. Les fournisseurs pris en charge sont OpenAI, Anthropic et Amazon Bedrock.</li>
       <li><b>Clé</b> : saisissez ou mappez votre clé API pour le fournisseur sélectionné.</li>
       <li><b>Modèle</b> : sélectionnez le modèle LLM que la clé utilisera.</li>
       <li><b>Autres champs</b> : saisissez les valeurs des autres champs requis par votre gestion du cycle de vie des informations.</li>
      </ul>
    </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion d’Adobe Fusion MCP à Workfront Fusion, voir <a href="#connect-adobe-fusion-mcp-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Fusion MCP à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>Outils en lecture seule <i>(facultatif)</i></td> 
   <td> <p>Sélectionnez des outils en lecture seule spécifiques pour restreindre l’IA. Si aucun n’est sélectionné, tous les outils en lecture seule de cette catégorie sont autorisés.</p> </td> 
  </tr> 
  <tr> 
   <td>Outils d’écriture/suppression <i>(facultatif)</i></td> 
   <td> <p>Sélectionnez des outils d’écriture ou de suppression spécifiques pour restreindre l’IA. Si aucun n’est sélectionné, tous les outils d’écriture et de suppression de cette catégorie sont autorisés.</p> <p>Pour garantir qu’un scénario sans assistance n’engage jamais une action destructrice, nous vous recommandons de laisser ce champ défini sur une sélection délibérément vide plutôt que de le laisser libre.</p> </td> 
  </tr> 
  <tr> 
   <td>Entrez votre invite</td> 
   <td> <p>Saisissez ou mappez l’instruction, en langage clair, que l’IA doit exécuter.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Restreindre les outils que l’IA peut appeler

Vous pouvez limiter les outils Fusion que l’IA peut appeler en sélectionnant outils dans les champs Outils en lecture seule et Outils en écriture/suppression .

* Si vous laissez un champ vide, l’IA peut appeler chaque outil de cette catégorie.
* Si vous laissez les deux champs vides, l’IA peut appeler chaque outil du serveur MCP Fusion.

Pour empêcher un scénario sans assistance d’effectuer une action d’écriture ou de suppression, sélectionnez uniquement les outils que vous souhaitez autoriser dans le champ Outils en lecture seule , puis sélectionnez au moins un outil dans le champ Outils d’écriture/suppression pour que l’appel d’IA vous convienne.

Les noms d’outils figurant dans les listes proviennent du serveur MCP Fusion.

#### Traitement de l’invite par le module

* Le module n&#39;a pas de tour de relance. Si votre invite n’est pas claire, l’IA émet une hypothèse raisonnable et l’indique dans la réponse au lieu de vous poser une question.
* L’IA vérifie les informations qui peuvent être modifiées à l’aide des outils .
* L’IA n’effectue aucune action d’écriture ou de suppression au-delà de ce que votre invite demande.
* Le module requiert une connexion valide. Il ne fonctionne pas sans.

#### Sortie

Le module renvoie les informations suivantes, que vous pouvez mapper dans les modules suivants du scénario :

* **Réponse** : réponse finale de l’IA, sous forme de texte.
* **Journal d&#39;audit** : enregistrement de la session, y compris les outils appelés, leurs arguments et résultats, ainsi que le minutage.
* **Résumé** : totaux pour la session, y compris le nombre d’appels d’outil réussis et le statut final.
