---
title: Modules MCP Adobe Workfront
description: Avec le module MCP d’Adobe Workfront, vous pouvez envoyer une invite en anglais clair au serveur MCP d’Adobe Workfront et laisser un modèle d’IA effectuer la requête.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 71573ee33f852111d4541ee61567a51b137c7df5
workflow-type: tm+mt
source-wordcount: 871
ht-degree: 18%

---

# Modules MCP Adobe Workfront

Le connecteur MCP Adobe Workfront est une intégration Fusion dédiée pour le propre serveur MCP (Model Context Protocol) d’Adobe Workfront. Contrairement à un connecteur standard, où chaque module effectue une action fixe, ce connecteur comporte un seul module qui accepte une instruction ouverte en anglais simple et permet à un modèle d’IA de décider quelles opérations Workfront sont nécessaires pour l’exécuter.

Par exemple, vous pouvez saisir l’invite « Rechercher tous mes projets actifs qui sont en retard et résumer leur statut » et le module renvoie une réponse synthétisée, au lieu d’avoir à enchaîner plusieurs modules Get et Filter.

Vous pouvez restreindre les actions Workfront que l’IA est autorisée à entreprendre, de sorte que même un scénario sans assistance puisse garantir qu’aucune action destructrice inattendue n’est entreprise.

Par défaut, ce module utilise l’IA gérée par Adobe, qui utilise le modèle `claude-sonnet-5` . Vous pouvez configurer le module pour utiliser un autre LLM, à l’aide d’une clé et des autres informations d’identification que vous fournissez.

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
   <p>Si votre organisation dispose d’un package Workfront Select ou Prime qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acquérir Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation Workfront](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Connexion d’Adobe Workfront MCP à Workfront Fusion

Le connecteur MCP Adobe Workfront utilise OAuth 2.0 pour se connecter à Workfront. Contrairement aux autres connecteurs Workfront, il n’existe aucun champ de connexion manuel à remplir, comme un hôte, un ID client ou un secret client.

Pour créer une connexion, procédez comme suit :

1. Dans le module Adobe Workfront MCP , cliquez sur **[!UICONTROL Ajouter]** en regard du champ Connexion .
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
        <td>Indiquez si vous vous connectez à un environnement de production ou hors production.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>Indiquez si vous vous connectez à un compte de service ou à un compte personnel.</td>
      </tr>
    </tbody>
    </table>

1. Cliquez sur **[!UICONTROL Continuer]** pour enregistrer la connexion et revenir au module.

   Si vous n’avez pas encore effectué votre connexion à Workfront, on vous redirige vers un écran de connexion. Connectez-vous et approuvez l’accès.

Vous êtes redirigé vers Workfront Fusion et la nouvelle connexion est disponible dans le module .

>[!NOTE]
>
>Lors de la première utilisation, la connexion s’enregistre automatiquement auprès du serveur MCP Workfront et réutilise cet enregistrement pour chaque connexion que vous créez par la suite.

## Module Adobe Workfront MCP et ses champs

### Traiter une invite utilisateur

Ce module d’action traite une invite en anglais clair par rapport au serveur MCP Workfront, à l’aide du modèle de langue que vous spécifiez, et renvoie la réponse de l’IA.

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
  </tr>   <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Pour plus d’informations sur la connexion de votre application Workfront à Workfront Fusion, voir <a href="#connect-adobe-workfront-mcp-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe Workfront MCP à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>Outils en lecture seule <i>(facultatif)</i></td> 
   <td> <p>Limitez les actions Workfront en lecture seule que l’IA est autorisée à appeler. Si aucun outil n’est sélectionné, tous les outils en lecture seule sont autorisés.</p> </td> 
  </tr> 
  <tr> 
   <td>Outils d’écriture/suppression <i>(facultatif)</i></td> 
   <td> <p>Saisissez les actions d’écriture ou de suppression de Workfront que l’IA est autorisée à appeler. Si vous laissez ce champ vide, tous les outils d’écriture et de suppression sont autorisés.</p> <p>Pour garantir qu’un scénario sans assistance n’engage jamais une action destructrice, nous vous recommandons de laisser ce champ défini sur une sélection délibérément vide plutôt que de le laisser libre.</p> </td> 
  </tr> 
  <tr> 
   <td>Entrez votre invite</td> 
   <td> <p>Saisissez ou mappez l’instruction, en langage clair, que l’IA doit exécuter.</p> <p>Exemple : <i>Rechercher tous les projets qui me sont affectés et qui sont en retard.</i></p> </td> 
  </tr>  </tbody> 
</table>

Pour obtenir la liste des outils que vous pouvez sélectionner pour les champs Outils en lecture seule et Outils en écriture/suppression , consultez [Outils de serveur Adobe Workfront MCP](https://experienceleague.adobe.com/en/docs/workfront/using/basics/workfront-mcp-server/workfront-mcp-server-tools) dans la documentation de Workfront.

Le module renvoie les informations suivantes, que vous pouvez mapper dans les modules suivants du scénario :

* **Réponse** : réponse finale de l’IA, sous forme de texte.
* **Journal d’audit** : enregistrement de la session, y compris l’invite d’origine, l’heure de début et de fin, ainsi que les détails de chaque appel d’outil effectué par l’IA, tels que le nom de l’outil, les arguments, son succès, sa durée et la sortie.
* **Résumé** : totaux pour la session, y compris le nombre d’appels d’outil tentés, le nombre d’appels réussis ou ayant échoué, le temps de traitement total et le statut global.
