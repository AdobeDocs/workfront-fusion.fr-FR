---
content-type: reference
title: Modifier des modèles
description: Cet article décrit comment modifier des modèles Fusion.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 473dba8b-faa4-432f-9357-c2146e86b261
source-git-commit: 86b0d7b16a4ed7e15888f6ee1a58f0279e96fb70
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 25%

---

# Modifier des modèles

Les modèles Adobe Workfront Fusion sont des scénarios préconfigurés conçus pour automatiser et rationaliser divers workflows. Ces modèles peuvent vous aider à configurer rapidement des intégrations et des automatisations sans avoir à tout créer de zéro.

Si vous êtes administrateur, vous avez l’autorisation d’afficher, de modifier, de renommer, de publier, d’approuver et de supprimer les modèles créés par d’autres personnes.

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

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md). -->

+++

## Modifier les modèles [!DNL Workfront Fusion] en tant qu’administrateur et administratrice

1. Cliquez sur **[!UICONTROL Administration]** dans le panneau de navigation de gauche pour ouvrir la zone de [!UICONTROL Administration].
1. Cliquez sur **[!UICONTROL All Templates]** dans le panneau de navigation de gauche.
1. Cliquez sur **[!UICONTROL Detail]** à droite du modèle que vous souhaitez modifier.
1. (Facultatif) Renommez le modèle en cliquant sur **Options** dans le coin supérieur droit et en sélectionnant **Renommer**.
1. (Facultatif) Pour modifier la langue de votre modèle, cliquez sur **[!UICONTROL Create a new template]** ![](assets/fusion-scenario-settings-icon.png), puis sélectionnez la langue dans le menu déroulant Langue .

   >[!IMPORTANT]
   >
   >La sélection Langues correspond aux langues disponibles dans les paramètres du système et ne concerne que le nom du modèle public et sa description. Vous ne pouvez pas modifier la langue d’un modèle une fois le modèle enregistré.

1. (Facultatif) Pour modifier la description du modèle, cliquez sur **[!UICONTROL Set up a template]** ![](assets/fusion-scenario-settings-icon.png), puis saisissez la description.
1. Ajoutez ou modifiez des applications, des modules et des outils de la même manière que lors de la création d’un scénario standard.

   Pour ajouter une aide contextuelle aux modules, consultez [Configuration de [!UICONTROL Wizard] fonctionnalité](#set-up-wizard-functionality) dans cet article.

   <!--For more information on building a scenario, see [Create a scenario in [!DNL Adobe Workfront Fusion]](../../../workfront-fusion/scenarios/create-a-scenario.md).-->

   >[!NOTE]
   >
   >Si votre modèle comprend des modules qui nécessitent l’ajout de la connexion, des informations d’identification ou d’autres informations sensibles à la confidentialité, ces informations ne sont pas partagées avec les utilisateurs et utillisatrices du modèle.

1. (Facultatif) Cliquez sur **[!UICONTROL Run once]** pour tester le modèle.
1. Cliquez sur l’icône **[!UICONTROL Save]** ![](assets/save-icon.png).


## Configurer la fonctionnalité de [!UICONTROL Wizard]

Le [!UICONTROL Wizard] [!DNL Workfront Fusion template] vous permet de fournir aux futurs utilisateurs de votre modèle des instructions ou des informations relatives aux champs spécifiques utilisés dans les modules.

1. Cliquez sur le module ajouté au modèle pour afficher les champs du module.
1. Localisez le champ dans lequel vous souhaitez ajouter des informations de [!UICONTROL Wizard] et activez-**[!UICONTROL Use in Wizard]** sous ce champ.
1. Saisissez les informations que vous souhaitez rendre visibles pour les utilisateurs dans le champ [!UICONTROL Help] .
1. (Facultatif) Pour permettre aux utilisateurs de voir ce texte lors de l’utilisation du modèle, activez **[!UICONTROL Use as default value]**.
1. Répétez les étapes 2 à 4 pour chaque champ auquel vous souhaitez fournir des informations.
1. Cliquez sur **[!UICONTROL OK]** pour enregistrer les modifications et fermer le module.

Le processus de publication est le même que dans le cas d’un utilisateur ou d’une utilisatrice standard. Pour plus d&#39;informations, consultez la section [Publish et partager des modèles](/help/workfront-fusion/create-and-manage-templates/publish-and-share-fusion-templates.md).

## Statuts des modèles

Vous pouvez vérifier le statut sur la page du modèle sous le nom du modèle.

Les statuts possibles sont les suivants :

* **[!UICONTROL Private]** : ce modèle est visible uniquement pour l’auteur du modèle et son équipe.
* **[!UICONTROL Published]** : ce modèle est visible uniquement pour l’auteur du modèle et son équipe. Une fois publié, vous pouvez envoyer le modèle pour approbation, si vous le souhaitez. Vous pouvez également copier un lien partageable.
* **[!UICONTROL Approved]** : ce modèle est visible pour tous les utilisateurs de Workfront Fusion dans l’onglet [!UICONTROL Public templates] . Vous pouvez également copier un lien partageable en cliquant sur [!UICONTROL Options] dans le coin supérieur droit de l’écran.

Vous pouvez également vérifier le statut dans l’onglet [!UICONTROL Team templates] . Si un modèle est publié, une icône s’affiche à droite de son nom.

* **Icône représentant un œil** : le modèle est publié ; il est visible pour l’équipe.
* **Icône de coche jaune** : le modèle est publié ; il n’est visible que par l’équipe ; et il est en attente d’approbation pour être ajouté à l’onglet Modèles publics .
* **Icône de coche verte** : le modèle est disponible dans l’onglet Modèles publics et est visible par tout utilisateur de Workfront Fusion. Il est également toujours visible dans l’onglet [!UICONTROL Team templates] . L’auteur du modèle ou le membre de son équipe peut toujours le modifier.

Les modèles sans icône ont le statut [!UICONTROL Private]. Ils ne sont pas publiés et ne sont visibles que par l’équipe.

## Recherche des informations sur le SVG d’un modèle

1. Cliquez sur **[!UICONTROL Administration]** dans le panneau de navigation de gauche pour ouvrir la zone de [!UICONTROL Administration].
1. Cliquez sur **[!UICONTROL Templates]** dans le panneau de navigation de gauche.
1. Cliquez sur le modèle pour lequel vous souhaitez rechercher des informations.
1. Cliquez sur **Options** dans le coin supérieur droit.
1. Sélectionnez *Diagramme SVG*.

Vous pouvez y afficher le diagramme du SVG et le code du SVG.
