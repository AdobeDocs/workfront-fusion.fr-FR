---
title: Générer un segment de scénario à l’aide de l’IA
description: Vous pouvez utiliser l’IA pour saisir une invite de texte décrivant ce que vous avez besoin d’un segment de votre scénario pour faire. Fusion génère ensuite un ou plusieurs modules qui effectuent ces actions, que vous pouvez utiliser dans votre scénario.
author: Becky
feature: Workfront Fusion
exl-id: d231e33a-6033-4e3c-b1d4-7034797c45a5
source-git-commit: 2bec2607d55e4ba2ffd6ddcae6daa51071b204c4
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 19%

---

# Générer un segment de scénario à l’aide de l’IA

<!--DO NOT DELETE - linked through CSH-->

<!--Check if this is in GA before repo goes live. If not, hide this article.-->

<!--Check if they need to have signed the rider and stuff-->

Vous pouvez utiliser l’IA pour saisir une invite de texte décrivant ce que vous avez besoin d’un segment de votre scénario pour faire. Fusion génère ensuite un ou plusieurs modules qui effectuent ces actions, que vous pouvez utiliser dans votre scénario.

Les segments de scénario générés contiennent des modules pour un connecteur unique. Pour générer des modules pour un connecteur différent, créez une invite distincte, puis joignez les segments de scénario dans votre scénario.

Comme pour tout ce qui est généré par l’IA, nous vous recommandons de vérifier et de tester les modules générés pour vous assurer qu’ils fonctionnent comme prévu.

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

## Conditions préalables

Pour utiliser cette fonctionnalité, votre organisation doit remplir les conditions préalables suivantes :

* Votre organisation doit avoir participé au programme bêta Workfront AI Assistant.
* Adobe devez avoir signé un accord d’IA Adobe Gen dans vos dossiers pour votre organisation.

  Pour plus d’informations sur la signature de l’accord, voir [Signer le contrat](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview#sign-the-adobe-gen-ai-agreement) d’IA de Adobe génération dans l’article Présentation de AI Assistant dans la documentation Workfront.

## Applications de module d’IA actuellement prises en charge

Fusion AI peut actuellement générer des modules qui se connectent aux applications suivantes :

* Adobe Firefly
* Azure OpenAI
* Microsoft Graph
* Adobe Workfront Planning
* Adobe Analytics
* Services Adobe PDF
* Adobe Marketo
* Adobe Frame.io
* Dropbox
* Netsuite
* Calendrier Google
* Atlassian Jira
* GitLab
* Spotify
* Intervalle de bits
* L’IA OpenAI
* Slack

## Génération des modules

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez ajouter un module.
1. Cliquez n’importe où dans le scénario pour accéder à l’éditeur de scénarios.
1. Cliquez sur l’icône **&#x200B;**![&#x200B; AI Assistant](assets/ai-assistant-icon.png) AI près du coin supérieur droit de l’écran.
1. Saisissez une invite de texte dans le panneau AI Assistant.

   Pour obtenir des conseils sur les invites, voir [Conseils pour la création d’invites pour les segments](#tips-for-creating-prompts-for-scenario-segments) de scénario dans cet article.

   AI Assistant génère le module ou l’ensemble de modules.
1. (Conditionnel) Si nécessaire, ajoutez votre jeton API pour l’application dans les modules.
1. Vérifiez les modules pour vous assurer qu’ils sont configurés pour l’application et l’action appropriées.
1. (Conditionnel) Si la section Scénario généré n’est pas jointe à votre scénario, faites-la glisser sur place.

Nous vous recommandons de tester les modules pour vous assurer qu’ils fonctionnent comme prévu.

## Conseils pour la création d’invites pour les segments de scénario

Les invites texte doivent inclure au minimum les informations suivantes :

* Application à laquelle vous vous connectez
* L’action ou les actions que vous souhaitez effectuer

>[!IMPORTANT]
>
>Vous pouvez générer plusieurs modules à la fois, mais vous ne pouvez générer que des modules pour une application à la fois.

>[!BEGINSHADEBOX]

**Exemples** :

* `Delete the records 'xyz-123', 'xyz-456', 'xyz-789' from Adobe Workfront Planning`Cela inclut l’application `Workfront Planning` et l’action `delete records`. Cette invite crée trois modules, un pour chaque enregistrement qui sera supprimé.
* `Change campaign summary of the record 'xyz-123' from Adobe Workfront Planning`Cela inclut l’application `Workfront Planning` et l’action `change campaign summary`.
* `Get all field details in the record type with ID 'test-record' from Adobe Workfront Planning`Cela inclut l’application `Workfront Planning` et l’action `get field details`.

L’exemple suivant n’est PAS correct :

* `Generate an image in Adobe Firefly and upload it to Dropbox`

  Cet exemple est incorrect car il inclut plusieurs applications

>[!ENDSHADEBOX]

Tenez compte des points suivants lors de la création d’invites de texte :

* Utilisez un langage direct et simple.
* Vérifiez et testez votre segment de scénario. S’il ne fonctionne pas comme prévu, affinez votre invite et réessayez.
