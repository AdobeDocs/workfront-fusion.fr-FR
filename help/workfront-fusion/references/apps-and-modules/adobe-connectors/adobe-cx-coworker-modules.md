---
title: Modules Adobe CX Enterprise Coworker
description: Utilisez le connecteur Adobe CX Enterprise Coworker dans Adobe Workfront Fusion pour envoyer une invite en langage naturel à Coworker et utiliser sa réponse dans un scénario.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 6efe84af0487893a3c33ba2bf6e3db5200f25446
workflow-type: tm+mt
source-wordcount: '1974'
ht-degree: 8%
---
# Modules Adobe CX Enterprise Coworker

Utilisez le connecteur Adobe CX Enterprise Coworker dans Adobe Workfront Fusion pour envoyer une invite en langage naturel à Coworker et utiliser sa réponse dans un scénario. Coworker interprète votre demande et peut utiliser les outils disponibles sur votre compte pour effectuer le travail.

Le connecteur fournit deux modules :

* **[!UICONTROL Exécuter une invite]** lance une nouvelle requête et, par défaut, attend le résultat.
* **[!UICONTROL Obtenir le statut d’exécution]** vérifie une requête que vous avez démarrée précédemment.

## Conditions d’accès

<!-- BECKY CHECK ME: This table is copied from other Fusion connector articles. The source material does not list access requirements, but says you need an Adobe account that has access to Coworker. Confirm the requirements and whether Coworker needs its own license or entitlement. -->

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

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Conditions préalables

Vous devez disposer d’un compte Adobe ayant accès à Adobe CX Enterprise Coworker.

## Connexion d’Adobe CX Enterprise Coworker à Workfront Fusion

Connectez-vous avec un compte Adobe ayant accès à Coworker et aux services nécessaires à votre demande.

Pour créer une connexion, procédez comme suit :

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
      <tr>
        <td role="rowheader">ID client</td>
        <td>
          <p>Saisissez ou mappez un remplacement facultatif pour cette connexion. Sinon, utilisez l’ID client géré par la plateforme de ce type de compte. Enregistrez l’URL de rappel Fusion affichée pour le compte de collaborateur dédié.</p>
        </td>
      <tr>
        <td role="rowheader">Secret client</td>
        <td>
          <p>Saisissez ou mappez un remplacement facultatif pour cette connexion. Sinon, utilisez le clientSecret géré par la plateforme de ce type de compte. Utiliser les informations d’identification émises pour l’environnement IMS configuré.</p>
        </td>
    </tbody>
   </table>

1. Cliquez sur **[!UICONTROL Continuer]**.

Si vous ne pouvez pas vous connecter ou utiliser un service requis, contactez votre administrateur.

## Modules Adobe CX Enterprise Coworker et leurs champs

>[!WARNING]
>
>N’incluez jamais de mots de passe ou d’autres informations d’identification dans une invite.

### Obtenir le statut d’exécution

Ce module d&#39;action vérifie l&#39;état actuel d&#39;une tâche démarrée par **[!UICONTROL Exécuter une invite]**.

Ce module vérifie la tâche une fois. Elle ne démarre pas de nouvelle tâche et ne continue pas à vérifier jusqu’à ce que la tâche soit terminée. Si le résultat est toujours en attente, vérifiez à nouveau ultérieurement.

>[!NOTE]
>
>Ne convertissez pas l’ID de tâche en nombre, ne l’arrondissez pas et ne le reformatez pas. Si un collègue a répondu immédiatement à l’invite d’origine sans ID de tâche, vous n’avez pas besoin de vérifier le statut.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Include raw result] <i>(Facultatif, avancé)</i></td> 
   <td> <p>Cette option est désactivée par défaut. Inclure la réponse complète du collaborateur dans la sortie. La réponse peut contenir des informations sensibles.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Sélectionnez la même connexion que celle que vous avez utilisée lors de l’exécution d’origine <b>[!UICONTROL Run a Prompt]</b>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Task ID]</td> 
   <td> <p>Mappez l’ID de tâche renvoyé par <b>[!UICONTROL Run a Prompt]</b>. Conservez-le sous forme de texte tel qu’il est renvoyé.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Exécuter une invite

Ce module d&#39;action envoie une instruction à Coworker, telle que la synthèse de texte ou la collecte d&#39;informations à l&#39;aide des outils disponibles pour votre compte.

Chaque exécution envoie l’invite une fois et démarre une nouvelle conversation. Il n’est pas nécessaire de sélectionner un modèle d’IA ou de fournir une clé de fournisseur d’IA distincte.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>Sélectionnez la connexion de votre collègue. Pour plus d’informations, voir <a href="#connect-adobe-cx-coworker-to-workfront-fusion" class="MCXref xref">Connexion d’Adobe CX Enterprise Coworker à Workfront Fusion</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL User prompt]</td> 
   <td> <p>Saisissez vos instructions. Vous pouvez utiliser plusieurs lignes et mapper les informations des modules précédents.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Wait for completion] <i>(Optional, advanced)</i></td> 
   <td> <p>Cette option est activée par défaut. Activez cette option si vous souhaitez que le module attende la fin de la tâche ou requiert une attention particulière. Désactivez-la pour renvoyer immédiatement le résultat initial.</p><p>Pour plus d’informations, voir <a href="#wait-for-completion">Attente de l’achèvement</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Include raw result] <i>(Facultatif, avancé)</i></td> 
   <td> <p>Cette option est désactivée par défaut. Activez cette option si vous souhaitez que le module inclue la réponse complète de Coworker dans la sortie. La réponse peut contenir des informations sensibles.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
> Nous vous recommandons de ne pas indiquer **[!UICONTROL Inclure le résultat brut]** sauf si vous avez besoin de la réponse complète pour un objectif spécifique. Les résultats bruts peuvent contenir des informations sensibles et ne constituent pas un enregistrement complet garanti de chaque action. Vérifiez ce que contient un résultat brut avant de l’enregistrer, de le partager ou de le transmettre à un autre service.

#### Attendre la fin

Lorsque l’option **[!UICONTROL Attendre la fin]** est activée, le module vérifie la tâche après une attente de cinq secondes. Si la tâche est toujours en attente, le module attend encore cinq secondes avant de vérifier à nouveau. Chaque vérification prend également du temps pour recevoir une réponse. La vérification du statut n’envoie pas à nouveau l’invite.

L’attente s’arrête lorsque la tâche est terminée, échoue, est annulée ou rejetée, ou nécessite votre entrée ou votre autorisation. Si Coworker fournit une réponse immédiate, le module la renvoie sans autre vérification.

Lorsque l’option **[!UICONTROL Attendre l’achèvement]** est désactivée, le module renvoie le premier résultat sans attendre que la tâche soit terminée. Inspectez **[!UICONTROL État]**, **[!UICONTROL Terminé]** et **[!UICONTROL Nécessite de l’attention]** pour décider de la marche à suivre. Une tâche peut déjà être terminée lorsque le premier résultat est obtenu.

L’attente est soumise au délai d’expiration du module de Fusion. Si le module expire ou s’arrête, il se peut que Coworker continue à travailler. Dans ce cas, il se peut que vous ne receviez pas de sortie ni d’ID de tâche.

Pour un travail plus long, désactivez l’attente et enregistrez le **[!UICONTROL ID de tâche]** initial afin de pouvoir vérifier la tâche ultérieurement. N’exécutez pas à nouveau automatiquement l’invite après une temporisation. La première requête est peut-être déjà en cours, et la répéter peut dupliquer les modifications.


## Sortie de module

Les deux modules renvoient les informations suivantes lorsqu’ils se terminent sans erreur.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Task ID]</td> 
   <td> <p>Identifie la tâche. Ce champ est vide lorsque le collègue fournit une réponse immédiate sans créer de tâche. Utilisez cette valeur avec <b>[!UICONTROL Get Execution Status]</b>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Context ID]</td> 
   <td> <p>Permet d’identifier la conversation. Ce n'est pas un moyen de poursuivre la conversation.</p><p>Pour plus d’informations, voir <a href="#use-previous-answers">Utiliser les réponses précédentes</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td> <p>État actuel de la tâche. Voir <a href="#task-states" class="MCXref xref">États des tâches</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Completed]</td> 
   <td> <p>True si la tâche est terminée ou si un collègue fournit une réponse immédiate.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Requires attention]</td> 
   <td> <p>Vrai quand un collègue a besoin d'entrée ou d'autorisation.</p><p>Pour plus d’informations, voir <a href="#requests-that-need-attention">Demandes nécessitant une attention particulière</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Texte de l'assistant final]</td> 
   <td> <p>Réponse finale à la fin de la tâche. Ce champ est vide lorsque la tâche est en attente ou requiert une attention particulière. Une réponse terminée peut également ne pas contenir de texte de réponse.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text artifacts (peut inclure du texte intermédiaire)]</td> 
   <td> <p>Texte renvoyé pendant le travail. Chaque élément peut inclure un identifiant d’artefact, un nom et un texte. Ces éléments ne sont pas nécessairement des réponses définitives.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Raw result (opt-in)]</td> 
   <td> <p>La réponse complète. Ceci est inclus uniquement lorsque <b>[!UICONTROL Include raw result]</b> est activé.</p> </td> 
  </tr> 
 </tbody> 
</table>

Utilisez **[!UICONTROL Texte d’assistant final]** pour la réponse au lieu de combiner tous les artefacts de texte. Les artefacts peuvent inclure des descriptions de progression ou tout autre texte intermédiaire.

### Demandes nécessitant une attention particulière

Un collègue peut avoir besoin d’informations supplémentaires ou d’une autorisation avant de pouvoir continuer. Dans ce cas, la mention **[!UICONTROL Nécessite une attention]** est définie sur true et la mention **[!UICONTROL Terminé]** sur false. Acheminez le résultat à une personne au lieu de le traiter comme un travail terminé.

Ces modules ne peuvent pas répondre à une question de relance ni approuver une action en votre nom. **[!UICONTROL Obtenir le statut d’exécution]** peut vérifier si le statut de la tâche a changé, mais elle ne résout pas la demande d’entrée ou d’autorisation.

### Utiliser les réponses précédentes

Chaque exécution **[!UICONTROL Exécuter une invite]** lance une nouvelle conversation. Pour faire référence à une réponse précédente, incluez la question et la réponse appropriées en tant que texte dans votre nouvelle invite. Cela donne un contexte au collaborateur, mais ne reprend pas la conversation précédente.

**[!UICONTROL ID de contexte]** identifie la conversation associée au résultat. Vous ne pouvez pas le fournir à ces modules pour poursuivre une conversation.

>[!IMPORTANT]
>
>**[!UICONTROL Terminé]** ne garantit pas que l’action commerciale demandée a réussi. Par exemple, un collègue peut terminer en expliquant qu’un outil requis n’est pas disponible. Examinez la réponse et vérifiez tout résultat requis avant de passer à l’action suivante.

### États de la tâche

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"><code>submitted</code>, <code>working</code></td> 
   <td> <p>La tâche est en attente. <b>[!UICONTROL Completed]</b> est faux. <b>[!UICONTROL Run a Prompt]</b> continue d'attendre lorsque l'attente est activée. Sinon, enregistrez l’ID de tâche et vérifiez ultérieurement.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><code>completed</code></td> 
   <td> <p><b>[!UICONTROL Completed]</b> est vrai. Vérifiez <b>[!UICONTROL Texte de l’assistant final]</b> et le résultat attendu.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><code>input-required</code>, <code>auth-required</code></td> 
   <td> <p>La tâche a besoin d'attention. <b>[!UICONTROL Completed]</b> est faux et <b>[!UICONTROL Requires attention]</b> est vrai. L'attente s'arrête. Acheminez le résultat pour examen humain.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><code>failed</code>, <code>canceled</code>, <code>rejected</code></td> 
   <td> <p>Le module signale une erreur au lieu d’un résultat normal.</p> </td> 
  </tr> 
 </tbody> 
</table>

Un résultat en attente ou nécessitant votre attention n’est pas un achèvement réussi, même si le module renvoie sans erreur.

## Exemples

### Résumer une mise à jour

1. Ajoutez **[!UICONTROL Exécuter une invite]** et sélectionnez votre connexion.
1. Saisissez ce qui suit dans le champ **[!UICONTROL Invite utilisateur]** :

   ```text
   Summarize the following project update in three bullet points.
   Use only the supplied text; do not call tools or change any records.
   
   The planning workshop is complete. Two dependencies need confirmation.
   The team will review the delivery estimate on Friday.
   ```

1. Laissez **[!UICONTROL Attendre la fin]** activé et **[!UICONTROL Inclure le résultat brut]** désactivé.
1. Si **[!UICONTROL Nécessite de l’attention]** est vrai, acheminez le résultat pour révision humaine. Si **[!UICONTROL Terminé]** est vrai, mappez **[!UICONTROL Texte de l’assistant final]** à l’étape suivante.

Le libellé généré par l’IA peut varier. Examinez les résultats lorsque la précision est importante.

### Vérifier une tâche plus longue ultérieurement

1. Ajoutez **[!UICONTROL Exécuter une invite]**, sélectionnez votre connexion et saisissez vos instructions.
1. Désactivez **[!UICONTROL Attendre la fin]**.
1. Inspectez le résultat initial.

   * Si la tâche est terminée, traitez le résultat.
   * Si la tâche nécessite une attention particulière, acheminez le résultat pour révision.
   * Si la tâche est en attente, enregistrez le **[!UICONTROL Identifiant de tâche]** en tant que texte et notez la connexion que vous avez utilisée.

1. Ultérieurement, utilisez **[!UICONTROL Obtenir le statut d’exécution]** avec cette connexion et cet ID de tâche.
1. Si la tâche est toujours en attente, organisez une autre vérification dans les limites de votre scénario. Traitez le résultat une fois que vous avez terminé et gérez l’attention ou les erreurs séparément.

N’exécutez pas à nouveau l’invite d’origine simplement pour vérifier sa progression.

## Considérations relatives à l’utilisation

* Un collègue peut utiliser les outils et effectuer les actions autorisées par votre compte, y compris les modifications apportées aux enregistrements. Utilisez des invites approuvées et un compte avec un accès approprié.
* Ces modules ne permettent pas de restreindre des outils individuels. Des instructions telles que « ne rien modifier » décrivent votre intention, mais il ne s’agit pas d’un mode de lecture seule appliqué.
* Les outils et les compétences disponibles varient selon le compte. Le connecteur ne fournit pas de sélecteur de compétences ni ne garantit une action particulière, telle que la création d’un parcours ou la mise à jour d’un projet. Ne présumez pas que les demandes qui doivent être approuvées se termineront sans assistance.
* Le connecteur démarre et vérifie les requêtes de collaborateur. Il ne surveille pas les modifications apportées au projet et n’enregistre pas automatiquement les réponses dans une autre application. Ajoutez le déclencheur, le stockage et les modules de suivi appropriés à votre scénario, si nécessaire.
* Les réponses générées par l’IA peuvent être incomplètes ou inexactes. Validez les résultats importants avant de les utiliser pour apporter des modifications ou prendre des décisions.
* Le connecteur ne relance pas automatiquement une requête ayant échoué. Assurez-vous que la gestion des erreurs de votre scénario ne répète pas une invite dont le résultat est incertain.

## Dépannage

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Un champ obligatoire est manquant</td> 
   <td> <p>Sélectionnez une connexion et saisissez l’invite ou l’ID de tâche requis.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">La connexion échoue ou l'accès est refusé</td> 
   <td> <p>Connectez-vous à nouveau et vérifiez que votre compte Adobe a accès à Coworker et aux services requis. Contactez votre administrateur si nécessaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Tâche introuvable</td> 
   <td> <p>Vérifiez que l’identifiant de tâche n’est pas modifié et que vous utilisez la connexion d’origine. Une nouvelle tâche peut ne pas être visible immédiatement. Vérifiez le statut ultérieurement au lieu d’envoyer à nouveau l’invite.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Échec de la vérification de l’état</td> 
   <td> <p>Si l’erreur inclut l’ID de tâche accepté, utilisez <b>[!UICONTROL Get Execution Status]</b> pour rechercher cette tâche. Ne redémarrez pas automatiquement l’invite.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">L’exécution d’une invite expire ou perd sa réponse</td> 
   <td> <p>La tâche a peut-être commencé même si vous n’avez pas reçu son identifiant. Vérifiez avant de répéter la demande pour éviter tout travail en double.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Fusion expire en attendant</td> 
   <td> <p>Mon collègue travaille peut-être encore. Vérifiez la tâche si vous disposez de son identifiant. Pour les futures tâches longues, désactivez l’attente et enregistrez d’abord l’identifiant initial.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Un collègue ou un service requis n’est pas disponible</td> 
   <td> <p>Partagez l’erreur affichée avec votre administrateur ou votre administratrice, sans informations d’identification ni contenu de résultat sensible.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!-- BECKY CHECK ME: Confirm the exact module and field labels in the UI (Run a Prompt, Get Execution Status, User prompt, Wait for completion, Include raw result, Task ID, and the output item names). Also confirm that the module is listed under "Adobe CX Enterprise Coworker" in the app picker. -->
