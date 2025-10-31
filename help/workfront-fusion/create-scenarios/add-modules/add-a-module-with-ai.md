---
title: Génération d’un segment de scénario à l’aide de l’IA
description: Vous pouvez utiliser l’IA pour saisir une invite de texte décrivant ce qu’un segment de votre scénario doit faire. Fusion génère ensuite un ou plusieurs modules qui effectuent ces actions, que vous pouvez utiliser dans votre scénario.
author: Becky
feature: Workfront Fusion
exl-id: d231e33a-6033-4e3c-b1d4-7034797c45a5
source-git-commit: c83070a7c2d1d048000a4eace4aaede73c7ec49d
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 5%

---

# Génération d’un segment de scénario à l’aide de l’IA

<!--DO NOT DELETE - linked through CSH-->

<!--Check if this is in GA before repo goes live. If not, hide this article.-->

<!--Check if they need to have signed the rider and stuff-->

Vous pouvez utiliser l’IA pour saisir une invite de texte décrivant ce qu’un segment de votre scénario doit faire. Fusion génère ensuite un ou plusieurs modules qui effectuent ces actions, que vous pouvez utiliser dans votre scénario.

Les segments de scénario générés contiennent des modules pour un seul connecteur. Pour générer des modules pour un connecteur différent, créez une invite distincte, puis joignez les segments du scénario dans votre scénario.

Comme pour tout ce qui est généré à partir de l’IA, nous vous recommandons de vérifier et de tester les modules générés pour vous assurer qu’ils fonctionnent comme prévu.

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
   <td role="rowheader">Produit</td> 
   <td>
   <p>Si votre entreprise dispose d’un package Select ou Prime Workfront qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acheter Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++## Prérequis

Votre entreprise doit remplir les conditions préalables suivantes pour utiliser cette fonctionnalité :

* Votre entreprise doit avoir participé au programme Beta de l’assistant d’IA pour Workfront.
* Adobe doit disposer d’un contrat Adobe Gen AI signé enregistré pour votre organisation.

  Pour plus d’informations sur la signature du contrat, consultez [Signature du contrat Adobe Gen AI](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview#sign-the-adobe-gen-ai-agreement) dans l’article Présentation de l’assistant AI dans la documentation de Workfront.

## Applications de module d’IA actuellement prises en charge

L’IA dédiée à Fusion peut actuellement générer des modules qui se connectent aux applications suivantes :

* Adobe Firefly
* Azure OpenAI
* Graphique Microsoft
* Planification d’Adobe Workfront
* Adobe Analytics
* Services Adobe PDF
* Adobe Marketo
* Adobe Frame.io
* Dropbox
* NetSuite
* Calendrier Google
* Atlassian Jira
* GitLab
* Spotifier
* Bitbucket
* OpenAI
* Slack

## Génération de modules

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez ajouter un module.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Cliquez sur l’icône **Assistant AI** ![icône de l’assistant AI](assets/ai-assistant-icon.png) près du coin supérieur droit de l’écran.
1. Saisissez une invite de texte dans le panneau de l’assistant d’IA.

   Pour obtenir des conseils sur les invites, voir [Conseils pour créer des invites pour les segments de scénario](#tips-for-creating-prompts-for-scenario-segments) dans cet article.

   L’assistant AI génère le module ou l’ensemble de modules.
1. (Conditionnel) Si nécessaire, ajoutez votre jeton API pour l’application dans les modules.
1. Vérifiez les modules pour vous assurer qu’ils sont configurés pour l’application et l’action appropriées.
1. (Conditionnel) Si la section du scénario généré n’est pas associée à votre scénario, faites-la glisser jusqu’à ce qu’elle soit en place.

Nous vous recommandons de tester les modules pour vous assurer qu’ils fonctionnent comme prévu.

## Conseils pour créer des invites pour les segments de scénario

Les invites de texte doivent inclure au minimum les informations suivantes :

* Application à laquelle vous vous connectez
* Action(s) à effectuer

>[!IMPORTANT]
>
>Vous pouvez générer plusieurs modules à la fois, mais vous ne pouvez générer des modules que pour une seule application à la fois.

>[!BEGINSHADEBOX]

**Exemples** :

* `Delete the records 'xyz-123', 'xyz-456', 'xyz-789' from Adobe Workfront Planning`
Cela inclut le `Workfront Planning` de l’application et le `delete records` d’action. Cette invite crée trois modules, un pour chaque enregistrement qui sera supprimé.
* `Change campaign summary of the record 'xyz-123' from Adobe Workfront Planning`
Cela inclut le `Workfront Planning` de l’application et le `change campaign summary` d’action.
* `Get all field details in the record type with ID 'test-record' from Adobe Workfront Planning`
Cela inclut le `Workfront Planning` de l’application et le `get field details` d’action.

L’exemple suivant n’est PAS correct :

* `Generate an image in Adobe Firefly and upload it to Dropbox`

  Cet exemple est incorrect, car il comprend plusieurs applications

>[!ENDSHADEBOX]

Tenez compte des points suivants lors de la création d’invites de texte :

* Utilisez un langage direct et simple.
* Vérifiez et testez votre segment de scénario. S’il ne s’exécute pas comme prévu, affinez votre invite et réessayez.
