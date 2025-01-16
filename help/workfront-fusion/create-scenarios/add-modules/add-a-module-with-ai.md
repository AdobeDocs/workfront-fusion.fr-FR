---
title: Génération d’un segment de scénario à l’aide de l’IA
description: Vous pouvez utiliser l’IA pour saisir une invite de texte décrivant ce qu’un segment de votre scénario doit faire. Fusion génère ensuite un ou plusieurs modules qui effectuent ces actions, que vous pouvez utiliser dans votre scénario.
author: Becky
feature: Workfront Fusion
exl-id: d231e33a-6033-4e3c-b1d4-7034797c45a5
source-git-commit: 55fe4bc46bc50ad9ccfd1b234e89028cf3cd12d5
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 10%

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

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] paquet</td> 
   <td> <p>Tous</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licence</td> 
   <td> <p>Nouveau : [!UICONTROL Standard]</p><p>Ou</p><p>En cours : [!UICONTROL Work] ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licence**</td> 
   <td>
   <p>Actuelle : aucune exigence de licence [!DNL Workfront Fusion] requise.</p>
   <p>Ou</p>
   <p>Héritée : n’importe laquelle. </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Nouveau :</p> <ul><li>[!UICONTROL Select] ou [!UICONTROL Prime] plan de [!DNL Workfront] : votre entreprise doit acheter des [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] plan : [!DNL Workfront Fusion] est inclus.</li></ul>
   <p>Ou</p>
   <p>Actuel : votre entreprise doit acheter [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Applications de module d’IA actuellement prises en charge

L’IA dédiée à Fusion peut actuellement générer des modules qui se connectent aux applications suivantes :

* Adobe Firefly
* Azure OpenAI
* Graphique Microsoft
* Planification d’Adobe Workfront
* Adobe Analytics
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

1. Cliquez sur l’onglet **[!UICONTROL Scenarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez ajouter un module.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Cliquez sur l’icône Générer avec l’IA ![Générer avec l’IA](assets/generate-with-ai-icon-beta.png) en bas de la page de l’éditeur de scénarios.

   Ou

   Commencez à ajouter un module et sélectionnez **Générer avec l’IA** dans la liste des applications. Cette option n’apparaît pas lors de l’ajout du premier module (déclencheur) à un scénario.

   Le panneau Assistant d’IA s’ouvre.
1. (Conditionnel) Si c’est la première fois que l’IA vous permet d’ajouter un segment de scénario, lisez le contrat qui s’affiche et cliquez sur **Accepter**.
1. Saisissez une invite de texte dans la zone.

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

**Exemples** :

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
