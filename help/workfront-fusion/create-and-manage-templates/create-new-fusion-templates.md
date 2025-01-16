---
title: Création de modèles
description: Vous pouvez créer des modèles de scénario dans  [!DNL Adobe]  Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 9cb9bd04-e9ae-4162-a1b9-d71566582b7a
source-git-commit: 7acc27ab2ce80b964b7f9fbb302816aa75964ab5
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 40%

---

# Création de modèles

Vous pouvez créer des modèles de scénario dans [!DNL Adobe] Workfront Fusion.

>[!TIP]
>
>Avant de créer un modèle, vous pouvez vérifier l’onglet [!UICONTROL Public templates] pour vous assurer que le modèle que vous souhaitez créer n’est pas déjà disponible.

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

## Créer un modèle

Vous pouvez créer un modèle via un processus similaire à la création d’un scénario. Les administrateurs et administratrices de Fusion peuvent également créer des modèles à partir de scénarios existants.

* [Créer un modèle](#build-a-template)
* [Créer un modèle à partir d’un scénario](#create-a-template-from-a-scenario)

### Créer un modèle

1. Cliquez sur **[!UICONTROL Templates]** ![](assets/templates-icon.png) dans le panneau de navigation de gauche.
1. Cliquez sur **[!UICONTROL Create a new template]** dans le coin supérieur droit.
1. (Facultatif) Renommez le modèle en remplaçant le **[!UICONTROL New template name]** par défaut dans le coin supérieur gauche.
1. (Facultatif) Pour modifier la langue de votre modèle, cliquez sur **[!UICONTROL Set up a template]** ![](assets/scenario-settings-icon.png) et sélectionnez la langue dans le menu déroulant Langue .

   >[!IMPORTANT]
   >
   >La sélection Langues correspond aux langues disponibles dans les paramètres du système et ne concerne que le nom du modèle public et sa description. Vous ne pouvez pas modifier la langue d’un modèle une fois le modèle enregistré.

1. (Facultatif) Pour saisir une description du modèle, cliquez sur **[!UICONTROL Set up a template]** ![](assets/scenario-settings-icon.png) et saisissez la description.
1. Ajoutez des applications, des modules et des outils en suivant les mêmes processus que l’ajout de modules à un scénario.

   Pour obtenir des instructions, consultez les articles sous [Ajouter des modules](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

   Pour ajouter une aide contextuelle aux modules, consultez [Configuration de la fonctionnalité de l’assistant](#set-up-wizard-functionality) dans cet article.

   Pour plus d’informations sur la création d’un scénario, voir [Processus de création d’un scénario](/help/workfront-fusion/create-scenarios/plan-a-scenario/create-a-scenario-workflow.md).

   >[!NOTE]
   >
   >Si votre modèle comprend des modules qui nécessitent l’ajout de la connexion, des informations d’identification ou d’autres informations sensibles à la confidentialité, ces informations ne sont pas partagées avec les utilisateurs et utillisatrices du modèle.

1. (Facultatif) Cliquez sur **[!UICONTROL Run once]** pour tester votre modèle.
1. Cliquez sur l’icône **[!UICONTROL Save]** ![](assets/save-icon.png) pour enregistrer le modèle.

Lorsque vous enregistrez votre modèle, il devient visible pour les membres de votre équipe. Si vous souhaitez que votre modèle soit accessible en dehors de votre équipe, vous devez soumettre une demande pour qu’il soit approuvé et publié. La demande est envoyée à l’équipe Adobe Workfront Fusion pour approbation. Une fois approuvé, le modèle est accessible à d’autres personnes en dehors de votre équipe.

Pour plus d’informations sur la publication de modèles, voir [Publier et partager des modèles  [!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/create-and-manage-templates/publish-and-share-fusion-templates.md).

### Créer un modèle à partir d’un scénario

>[!NOTE]
>
>Pour créer un modèle à partir d’un scénario, vous devez être un administrateur ou une administratrice Fusion.

1. Cliquez sur l’onglet **[!UICONTROL Scenarios]** dans le panneau de gauche.
1. Sélectionnez le scénario à partir duquel vous souhaitez créer un modèle.
1. Cliquez sur le bouton **Administration** dans le coin supérieur droit de la page.
1. Sélectionnez **Cloner comme modèle**.

   Le scénario est copié dans une page Nouveau modèle.
1. (Facultatif) Renommez le modèle en remplaçant le **[!UICONTROL New template name]** par défaut dans le coin supérieur gauche.
1. (Facultatif) Pour modifier la langue de votre modèle, cliquez sur **[!UICONTROL Set up a template]** ![](assets/scenario-settings-icon.png) et sélectionnez la langue dans le menu déroulant Langue .

   >[!IMPORTANT]
   >
   >La sélection Langues correspond aux langues disponibles dans les paramètres du système et ne concerne que le nom du modèle public et sa description. Vous ne pouvez pas modifier la langue d’un modèle une fois le modèle enregistré.

1. (Facultatif) Pour saisir une description du modèle, cliquez sur **[!UICONTROL Set up a template]** ![](assets/scenario-settings-icon.png) et saisissez la description.
1. Modifiez les applications, modules et outils selon vos besoins, en utilisant les mêmes processus que l’ajout de modules à un scénario.

   Pour obtenir des instructions, consultez les articles sous [Ajouter des modules](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

   Pour ajouter une aide contextuelle aux modules, consultez [Configuration de [!UICONTROL Wizard] fonctionnalité](#set-up-wizard-functionality) dans cet article.

   >[!NOTE]
   >
   >Si votre modèle comprend des modules qui nécessitent l’ajout de la connexion, des informations d’identification ou d’autres informations sensibles à la confidentialité, ces informations ne sont pas partagées avec les utilisateurs et utillisatrices du modèle.

1. (Facultatif) Cliquez sur **[!UICONTROL Run once]** pour tester votre modèle.
1. Cliquez sur l’icône **[!UICONTROL Save]** ![](assets/save-icon.png).

## Configurer la fonctionnalité de [!UICONTROL Wizard] {#set-up-wizard-functionality}

Le [!UICONTROL Wizard] [!DNL Workfront Fusion template] vous permet de fournir aux futurs utilisateurs de votre modèle des instructions ou des informations relatives aux champs spécifiques utilisés dans les modules.

1. Lors de la création d’un modèle, cliquez sur un module ajouté au modèle pour afficher les champs du module.
1. Localisez le champ dans lequel vous souhaitez ajouter des informations de [!UICONTROL Wizard] et activez les **[!UICONTROL Use in Wizard]** pour ce champ.
1. Saisissez les informations que vous souhaitez rendre visibles pour les utilisateurs dans le champ [!UICONTROL Help] .
1. (Facultatif) Pour permettre aux utilisateurs de voir ce texte lors de l’utilisation du modèle, activez **[!UICONTROL Use as default value]**.
1. Répétez les étapes 2 à 4 pour chaque champ auquel vous souhaitez fournir des informations.
1. Cliquez sur **[!UICONTROL OK]** pour enregistrer les modifications et fermer le module.
