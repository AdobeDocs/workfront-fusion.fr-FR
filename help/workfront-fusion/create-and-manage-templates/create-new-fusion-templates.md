---
title: Créer des modèles
description: Vous pouvez créer des modèles de scénario dans  [!DNL Adobe]  Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 9cb9bd04-e9ae-4162-a1b9-d71566582b7a
TQID: https://experienceleague.adobe.com/UywwjPpiSAHbtSIo72rBCGlSpwq0N7SAnBrPCXOVncI
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 816
ht-degree: 63%

---

# Créer des modèles

Vous pouvez créer des modèles de scénario dans [!DNL Adobe] Workfront Fusion.

>[!TIP]
>
>Avant de créer un modèle, vous pouvez vérifier l’onglet [!UICONTROL Modèles publics] pour vous assurer que le modèle que vous souhaitez créer n’est pas déjà disponible.

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

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Créer un modèle

Vous pouvez créer un modèle via un processus similaire à la création d’un scénario. Les administrateurs et administratrices de Fusion peuvent également créer des modèles à partir de scénarios existants.

* [Créer un modèle](#build-a-template)
* [Créer un modèle à partir d’un scénario](#create-a-template-from-a-scenario)

### Créer un modèle

1. Cliquez sur **[!UICONTROL Modèles]** ![icône Modèles](assets/templates-icon.png) dans le panneau de navigation de gauche.
1. Cliquez sur **[!UICONTROL Créer un modèle]** dans le coin supérieur droit.
1. (Facultatif) Renommez le modèle en remplaçant le **[!UICONTROL Nom du nouveau modèle]** par défaut dans le coin supérieur gauche.
1. (Facultatif) Pour modifier la langue de votre modèle, cliquez sur **[!UICONTROL Configurer un modèle]** ![icône des paramètres de scénario](assets/scenario-settings-icon.png) et sélectionnez la langue dans le menu déroulant Langue.

   >[!IMPORTANT]
   >
   >La sélection Langues correspond aux langues disponibles dans les paramètres du système et ne concerne que le nom du modèle public et sa description. Vous ne pouvez pas modifier la langue d’un modèle une fois le modèle enregistré.

1. (Facultatif) Pour saisir une description du modèle, cliquez sur **[!UICONTROL Configurer un modèle]** ![Icône Paramètres de scénario](assets/scenario-settings-icon.png) et saisissez la description.
1. Ajoutez des applications, des modules et des outils en suivant les mêmes processus que l’ajout de modules à un scénario.

   Pour obtenir des instructions, consultez les articles sous [Ajouter des modules](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

   Pour ajouter une aide contextuelle aux modules, consultez [Configuration de la fonctionnalité de l’assistant](#set-up-wizard-functionality) dans cet article.

   Pour plus d’informations sur la création d’un scénario, voir [Processus de création d’un scénario](/help/workfront-fusion/create-scenarios/plan-a-scenario/create-a-scenario-workflow.md).

   >[!NOTE]
   >
   >Si votre modèle comprend des modules qui nécessitent l’ajout de la connexion, des informations d’identification ou d’autres informations sensibles à la confidentialité, ces informations ne sont pas partagées avec les utilisateurs et utillisatrices du modèle.

1. (Facultatif) Cliquez sur **[!UICONTROL Exécuter une fois]** pour tester votre modèle.
1. Cliquez sur l’icône **[!UICONTROL Enregistrer]** ![Icône Enregistrer](assets/save-icon.png) pour enregistrer le modèle.

Lorsque vous enregistrez votre modèle, il devient visible pour les membres de votre équipe. Si vous souhaitez que votre modèle soit accessible en dehors de votre équipe, vous devez soumettre une demande pour qu’il soit approuvé et publié. La demande est envoyée à l’équipe Adobe Workfront Fusion pour approbation. Une fois approuvé, le modèle est accessible à d’autres personnes en dehors de votre équipe.

Pour plus d’informations sur la publication de modèles, voir [&#x200B; Publication et partage de modèles Adobe Workfront Fusion &#x200B;](/help/workfront-fusion/create-and-manage-templates/publish-and-share-fusion-templates.md).

### Créer un modèle à partir d’un scénario

>[!NOTE]
>
>Pour créer un modèle à partir d’un scénario, vous devez être un administrateur ou une administratrice Fusion.

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Sélectionnez le scénario à partir duquel vous souhaitez créer un modèle.
1. Cliquez sur le bouton **Administration** dans le coin supérieur droit de la page.
1. Sélectionnez **Cloner comme modèle**.

   Le scénario est copié dans une page Nouveau modèle.
1. (Facultatif) Renommez le modèle en remplaçant le **[!UICONTROL Nom du nouveau modèle]** par défaut dans le coin supérieur gauche.
1. (Facultatif) Pour modifier la langue de votre modèle, cliquez sur **[!UICONTROL Configurer un modèle]** ![icône des paramètres de scénario](assets/scenario-settings-icon.png) et sélectionnez la langue dans le menu déroulant Langue.

   >[!IMPORTANT]
   >
   >La sélection Langues correspond aux langues disponibles dans les paramètres du système et ne concerne que le nom du modèle public et sa description. Vous ne pouvez pas modifier la langue d’un modèle une fois le modèle enregistré.

1. (Facultatif) Pour saisir une description du modèle, cliquez sur **[!UICONTROL Configurer un modèle]** ![Icône Paramètres de scénario](assets/scenario-settings-icon.png) et saisissez la description.
1. Modifiez les applications, modules et outils selon vos besoins, en utilisant les mêmes processus que l’ajout de modules à un scénario.

   Pour obtenir des instructions, consultez les articles sous [Ajouter des modules](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

   Pour ajouter une aide contextuelle aux modules, voir [Configurer une fonctionnalité [!UICONTROL Assistant]](#set-up-wizard-functionality) dans cet article.

   >[!NOTE]
   >
   >Si votre modèle comprend des modules qui nécessitent l’ajout de la connexion, des informations d’identification ou d’autres informations sensibles à la confidentialité, ces informations ne sont pas partagées avec les utilisateurs et utillisatrices du modèle.

1. (Facultatif) Cliquez sur **[!UICONTROL Exécuter une fois]** pour tester votre modèle.
1. Cliquez sur l’icône **[!UICONTROL Enregistrer]** ![Enregistrer](assets/save-icon.png).

## Configurer une fonctionnalité [!UICONTROL Assistant] {#set-up-wizard-functionality}

L’[!UICONTROL assistant] de [!DNL Workfront Fusion template] vous permet de fournir aux futurs utilisateurs et utilisatrices de votre modèle des instructions ou des informations relatives aux champs spécifiques utilisés dans les modules.

1. Lors de la création d’un modèle, cliquez sur un module ajouté au modèle pour afficher les champs du module.
1. Localisez le champ où vous souhaitez ajouter les informations de l’[!UICONTROL assistant], puis activez **[!UICONTROL Utiliser dans l’assistant]** pour ce champ.
1. Saisissez les informations que vous souhaitez rendre visibles aux utilisateurs et utilisatrices dans le champ [!UICONTROL Aide].
1. (Facultatif) Pour permettre aux utilisateurs et utilisatrices de voir ce texte lorsqu’ils utilisent le modèle, activez **[!UICONTROL Utiliser comme valeur par défaut]**.
1. Répétez les étapes 2 à 4 pour chaque champ auquel vous souhaitez fournir des informations.
1. Cliquez sur **[!UICONTROL OK]** pour enregistrer les modifications et fermer le module.
