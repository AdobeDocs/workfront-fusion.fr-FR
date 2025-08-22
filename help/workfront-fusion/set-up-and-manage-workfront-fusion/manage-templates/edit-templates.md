---
content-type: reference
title: Modifier des modèles
description: Cet article décrit comment modifier des modèles Fusion.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 473dba8b-faa4-432f-9357-c2146e86b261
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 46%

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
      <td role="rowheader">Formule Adobe Workfront</td>
      <td><p>Tous</p></td>
    </tr>
    <tr data-mc-conditions="">
      <td role="rowheader">Licence Adobe Workfront</td>
      <td><p>Nouveau : Standard</p><p>Ou</p><p>Actuelle : [!UICONTROL Work] ou niveau supérieur</p></td>
    </tr>
    <tr>
      <td role="rowheader">Licence Adobe Workfront Fusion **</td>
      <td>
        <p>Actuel : aucune exigence de licence Workfront Fusion.</p>
        <p>Ou</p>
        <p>Héritée : n’importe laquelle.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Produit</td>
      <td>
        <p>Nouveau :</p>
        <ul>
          <li>Plan Workfront [!UICONTROL Select] ou [!UICONTROL Prime] : votre entreprise doit acheter Adobe Workfront Fusion.</li>
          <li>Plan Workfront [!UICONTROL Ultimate] : Workfront Fusion est inclus.</li>
        </ul>
        <p>Ou</p>
        <p>Actuel : votre entreprise doit acheter Adobe Workfront Fusion.</p>
      </td>
    </tr>
  </tbody>
</table>

<!--
For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md). 

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md). -->

+++

## Modification de modèles Workfront Fusion en tant qu’administrateur

1. Cliquez sur **[!UICONTROL Administration]** dans le panneau de navigation de gauche pour ouvrir la zone [!UICONTROL Administration].
1. Cliquez sur **[!UICONTROL Tous les modèles]** dans le panneau de navigation de gauche.
1. Cliquez sur **[!UICONTROL Détail]** à droite du modèle à modifier.
1. (Facultatif) Renommez le modèle en cliquant sur **Options** dans le coin supérieur droit et en sélectionnant **Renommer**.
1. (Facultatif) Pour modifier la langue de votre modèle, cliquez sur **[!UICONTROL Créer un modèle]** ![icône des paramètres de scénario](assets/fusion-scenario-settings-icon.png), puis sélectionnez la langue dans le menu déroulant Langue.

   >[!IMPORTANT]
   >
   >La sélection Langues correspond aux langues disponibles dans les paramètres du système et ne concerne que le nom du modèle public et sa description. Vous ne pouvez pas modifier la langue d’un modèle une fois le modèle enregistré.

1. (Facultatif) Pour modifier la description du modèle, cliquez sur **[!UICONTROL Configurer un modèle]** ![icône des paramètres de scénario](assets/fusion-scenario-settings-icon.png), puis saisissez la description.
1. Ajoutez ou modifiez des applications, des modules et des outils de la même manière que lors de la création d’un scénario standard.

   Pour ajouter une aide contextuelle aux modules, voir [Configurer une fonctionnalité [!UICONTROL Assistant]](#set-up-wizard-functionality) dans cet article.

   <!--For more information on building a scenario, see [Create a scenario in Adobe Workfront Fusion](../../../workfront-fusion/scenarios/create-a-scenario.md).-->

   >[!NOTE]
   >
   >Si votre modèle comprend des modules qui nécessitent l’ajout de la connexion, des informations d’identification ou d’autres informations sensibles à la confidentialité, ces informations ne sont pas partagées avec les utilisateurs et utillisatrices du modèle.

1. (Facultatif) Cliquez sur **[!UICONTROL Exécuter une fois]** pour tester le modèle.
1. Cliquez sur l’icône **[!UICONTROL Enregistrer]** ![Enregistrer](assets/save-icon.png).


## Configurer une fonctionnalité [!UICONTROL Assistant]

L’[!UICONTROL assistant] de [!DNL Workfront Fusion template] vous permet de fournir aux futurs utilisateurs et utilisatrices de votre modèle des instructions ou des informations relatives aux champs spécifiques utilisés dans les modules.

1. Cliquez sur le module ajouté au modèle pour afficher les champs du module.
1. Localisez le champ dans lequel vous souhaitez ajouter des informations [!UICONTROL Assistant] et activez **[!UICONTROL Utiliser dans l’Assistant]** sous ce champ.
1. Saisissez les informations que vous souhaitez rendre visibles aux utilisateurs et utilisatrices dans le champ [!UICONTROL Aide].
1. (Facultatif) Pour permettre aux utilisateurs et utilisatrices de voir ce texte lorsqu’ils utilisent le modèle, activez **[!UICONTROL Utiliser comme valeur par défaut]**.
1. Répétez les étapes 2 à 4 pour chaque champ auquel vous souhaitez fournir des informations.
1. Cliquez sur **[!UICONTROL OK]** pour enregistrer les modifications et fermer le module.

Le processus de publication est le même que dans le cas d’un utilisateur ou d’une utilisatrice standard. Pour plus d’informations, voir la section [Publier et partager des modèles](/help/workfront-fusion/create-and-manage-templates/publish-and-share-fusion-templates.md).

## Statuts des modèles

Vous pouvez vérifier le statut sur la page du modèle sous le nom du modèle.

Les statuts possibles sont les suivants :

* **[!UICONTROL Privé]** : ce modèle est visible uniquement par l’auteur ou l’autrice du modèle et son équipe.
* **[!UICONTROL Publié]** : ce modèle est visible uniquement par l’auteur ou l’autrice du modèle et son équipe. Une fois publié, vous pouvez envoyer le modèle pour approbation, si vous le souhaitez. Vous pouvez également copier un lien partageable.
* **[!UICONTROL Approuvé]** : ce modèle est visible pour tous les utilisateurs et utilisatrices de Workfront Fusion dans l’onglet [!UICONTROL Modèles publics]. Vous pouvez également copier un lien partageable en cliquant sur [!UICONTROL Options] dans le coin supérieur droit de l’écran.

Vous pouvez également vérifier le statut à partir de l’onglet [!UICONTROL Modèles d’équipe]. Si un modèle est publié, une icône s’affiche à droite de son nom.

* **Icône représentant un œil** : le modèle est publié ; il est visible pour l’équipe.
* **Icône de coche jaune** : le modèle est publié ; il n’est visible que par l’équipe ; et il est en attente d’approbation pour être ajouté à l’onglet Modèles publics .
* **Icône de coche verte** : le modèle est disponible dans l’onglet Modèles publics et est visible par tout utilisateur de Workfront Fusion. Il est également toujours visible dans l’onglet [!UICONTROL Modèles d’équipe]. L’auteur du modèle ou le membre de son équipe peut toujours le modifier.

Les modèles sans icônes ont un statut [!UICONTROL Privé]. Ils ne sont pas publiés et ne sont visibles que par l’équipe.

## Recherche des informations SVG d’un modèle

1. Cliquez sur **[!UICONTROL Administration]** dans le panneau de navigation de gauche pour ouvrir la zone [!UICONTROL Administration].
1. Cliquez sur **[!UICONTROL Modèles]** dans le panneau de navigation de gauche.
1. Cliquez sur le modèle pour lequel vous souhaitez rechercher des informations.
1. Cliquez sur **Options** dans le coin supérieur droit.
1. Sélectionnez *Diagramme SVG*.

Vous pouvez y afficher le diagramme SVG et le code SVG.
