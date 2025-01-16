---
content-type: reference
title: Approuver ou désapprouver des modèles
description: Cet article décrit comment approuver ou désapprouver des modèles Fusion.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: dafecd8b-96e5-46da-9ab6-15f0bc9b52a4
source-git-commit: 23e9f383b25c7b3789c413e557b94418e48a636b
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 22%

---

# Approuver ou refuser des modèles pour l&#39;onglet Public

Les modèles Adobe Workfront Fusion sont des scénarios préconfigurés conçus pour automatiser et rationaliser divers workflows. Ces modèles peuvent aider les utilisateurs à configurer rapidement des intégrations et des automatisations sans avoir à tout créer de zéro.

Si vous êtes un administrateur, vous pouvez choisir si certains modèles doivent être partagés ou non avec l’ensemble de l’organisation dans l’onglet Modèles publics .

Les utilisateurs peuvent envoyer les modèles qu’ils créent pour approbation à partager sur la page Modèles publics . <!--do the have to be requested or can an admin just choose to approve?-->

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto">
  <col>
  <col>
  <tbody>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] plan</td>
      <td><p>Tous</p></td>
    </tr>
    <tr data-mc-conditions="">
      <td role="rowheader">[!DNL Adobe Workfront] licence</td>
      <td><p>Nouveau : [!UICONTROL Standard]</p><p>Ou</p><p>En cours : [!UICONTROL Work] ou supérieur</p></td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront Fusion] licence**</td>
      <td>
        <p>Actuelle : aucune exigence de licence [!DNL Workfront Fusion] requise.</p>
        <p>Ou</p>
        <p>Héritée : n’importe laquelle.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Produit</td>
      <td>
        <p>Nouveau :</p>
        <ul>
          <li>[!UICONTROL Select] ou [!UICONTROL Prime] plan de [!DNL Workfront] : votre entreprise doit acheter des [!DNL Adobe Workfront Fusion].</li>
          <li>[!UICONTROL Ultimate] [!DNL Workfront] Plan : [!DNL Workfront Fusion] est inclus.</li>
        </ul>
        <p>Ou</p>
        <p>Actuel : votre entreprise doit acheter [!DNL Adobe Workfront Fusion].</p>
      </td>
    </tr>
  </tbody>
</table>

<!--
For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md). 

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md).-->

+++

## Approuver ou refuser des modèles [!DNL Workfront Fusion]

La validation d’un modèle le rend visible dans l’onglet [!UICONTROL Public templates] et disponible pour tous les utilisateurs.

La désapprobation d’un modèle le supprime de l’onglet [!UICONTROL Public templates] et le rend disponible uniquement pour l’équipe qui l’a créé.

1. Cliquez sur **[!UICONTROL Administration]** dans le panneau de navigation de gauche pour ouvrir la zone de [!UICONTROL Administration].
1. Cliquez sur **[!UICONTROL Templates]** dans le panneau de navigation de gauche.
1. Si vous souhaitez approuver un modèle, cliquez sur **[!UICONTROL Approve]** à droite du modèle.
1. Si vous souhaitez en désapprouver un, cliquez sur **[!UICONTROL Disapprove]** à droite du modèle.

>[!NOTE]
>
>Si vous validez un modèle précédemment approuvé puis modifié, votre seconde approbation remplacera le modèle d’origine.


## Statuts des modèles

Vous pouvez vérifier le statut sur la page du modèle sous le nom du modèle.

Les statuts possibles sont les suivants :

* **[!UICONTROL Private]** : ce modèle est visible uniquement pour l’auteur du modèle et son équipe.
* **[!UICONTROL Published]** : ce modèle est visible uniquement pour l’auteur du modèle et son équipe. Une fois publié, vous pouvez envoyer le modèle pour approbation, si vous le souhaitez. Vous pouvez également copier un lien partageable.
* **[!UICONTROL Approved]** : ce modèle est visible pour tous les utilisateurs de Workfront Fusion dans l’onglet [!UICONTROL Public templates] . Vous pouvez également copier un lien partageable en cliquant sur [!UICONTROL Options] dans le coin supérieur droit de l’écran.

Vous pouvez également vérifier le statut dans l’onglet [!UICONTROL Team templates] . Si un modèle est publié, une icône s’affiche à droite de son nom.

* **Icône représentant un œil** : le modèle est publié ; il est visible uniquement pour l’équipe ; et aucune demande d’approbation n’a été envoyée.
* **Icône de coche jaune** : le modèle est publié ; il n’est visible que par l’équipe ; et il est en attente d’approbation pour être ajouté à l’onglet Modèles publics .
* **Icône de coche verte** : le modèle est disponible dans l’onglet Modèles publics et est visible par tout utilisateur de Workfront Fusion. Il est également toujours visible dans l’onglet [!UICONTROL Team templates] . L’auteur du modèle ou le membre de son équipe peut toujours le modifier.

Les modèles sans icône ont le statut [!UICONTROL Private]. Ils ne sont pas publiés et ne sont visibles que par l’équipe.


<!--

## Questions about how this works

Editing

1. If an admin edits a template, do they have to publish again? ... Do they have to approve again?
1. What does publishing actually do?
1. Does a user have to submit for approval to share on the Public tab or can admin go through and approve/reject which ones they want? 
1. What is the admin approving? Does a user have to submit it for approval? 



What does "Publishing" mean?
What does "Approving" mean?
If an admin edits a template, do they have to publish again? ... Do they have to approve again?
Does a user have to submit for approval to share on the Public tab or can admin go through and approve/reject which ones they want? 
What is the admin approving? Does a user have to submit it for approval?

-->
