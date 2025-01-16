---
title: Ajouter un module à un scénario
description: Cet article décrit le processus de base d’ajout d’un module à un scénario.
author: Becky
feature: Workfront Fusion
exl-id: f3757468-3e11-4862-a83e-ed447805545b
source-git-commit: 55fe4bc46bc50ad9ccfd1b234e89028cf3cd12d5
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 8%

---

# Ajouter un module à un scénario

Un scénario se compose d’une série de modules indiquant comment les données doivent être transformées dans une application ou transférées entre des applications et des services web. Vous créez un module en ajoutant et en configurant des modules.

Cet article décrit le processus de base d’ajout d’un module à un scénario. Pour obtenir des instructions plus spécifiques sur l’ajout d’un scénario, consultez les autres articles sous [Ajouter des modules : index des articles](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

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

## Ajouter le premier module à un scénario

Le premier module d’un scénario est généralement un module de déclenchement.

Pour plus d’informations sur les modules de déclenchement, consultez la section [Modules de déclenchement](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) dans la présentation des modules.

1. Cliquez sur l’onglet **[!UICONTROL Scenarios]** dans le panneau de gauche.
1. Commencez à créer un scénario en cliquant sur **Créer un nouveau scénario** dans le coin supérieur droit de l’écran.

   L’éditeur de scénario s’ouvre, avec un module d’espace réservé (point d’interrogation) et la liste des connecteurs disponibles.

   ![Module Espace réservé](assets/placeholder-module.png)

1. Sélectionnez le connecteur ou le webhook qui démarrera ce scénario. Vous pouvez saisir le nom du connecteur dans la barre de recherche de la liste pour filtrer la liste.
1. Configurez le module .

   Pour obtenir des instructions sur la configuration de modules spécifiques, consultez l’article pour les applications sélectionnées, répertoriées dans [Références des applications Fusion et de leurs modules : index des articles](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

>[!NOTE]
>
>Si vous avez supprimé le premier module d’un scénario et souhaitez le remplacer, cliquez sur le module d’espace réservé (point d’interrogation) pour afficher la liste des connecteurs.

## Ajouter un autre module à un scénario

1. Si vous ne vous trouvez pas dans l’éditeur de scénarios du scénario dans lequel vous souhaitez ajouter un module, cliquez sur l’onglet **[!UICONTROL Scenarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez exporter un plan directeur.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Pour ajouter un module à un autre module, pointez sur la poignée droite du module après laquelle vous souhaitez ajouter un module, puis cliquez sur **Ajouter un autre module** lorsqu’il apparaît.

   La liste des connecteurs s’ouvre. Elle affiche les connecteurs déjà utilisés dans le scénario.

1. (Facultatif) Pour sélectionner un autre connecteur, cliquez sur **Ajouter un autre module** dans la liste, puis sélectionnez le connecteur. Vous pouvez saisir le nom du connecteur dans la barre de recherche de la liste pour filtrer la liste.
1. Configurez le module .

   Pour obtenir des instructions sur la configuration de modules spécifiques, consultez l’article pour les applications sélectionnées, répertoriées dans [Références des applications Fusion et de leurs modules : index des articles](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

## Insertion d’un module entre les modules existants d’un scénario

1. Si vous ne vous trouvez pas dans l’éditeur de scénarios du scénario dans lequel vous souhaitez ajouter un module, cliquez sur l’onglet **[!UICONTROL Scenarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez exporter un plan directeur.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Cliquez sur le chemin en pointillé entre les modules où vous souhaitez insérer un module.
1. Dans le menu qui s’affiche, sélectionnez **Ajouter un module**.

La liste des connecteurs s’ouvre. Elle affiche les connecteurs déjà utilisés dans le scénario.

1. (Facultatif) Pour sélectionner un autre connecteur, cliquez sur **Ajouter un autre module** dans la liste, puis sélectionnez le connecteur. Vous pouvez saisir le nom du connecteur dans la barre de recherche de la liste pour filtrer la liste.
1. Configurez le module .

   Pour obtenir des instructions sur la configuration de modules spécifiques, consultez l’article pour les applications sélectionnées, répertoriées dans [Références des applications Fusion et de leurs modules : index des articles](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).
