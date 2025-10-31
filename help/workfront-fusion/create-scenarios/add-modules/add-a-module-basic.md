---
title: Ajouter un module à un scénario
description: Cet article décrit le processus de base d’ajout d’un module à un scénario.
author: Becky
feature: Workfront Fusion
exl-id: f3757468-3e11-4862-a83e-ed447805545b
source-git-commit: c83070a7c2d1d048000a4eace4aaede73c7ec49d
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 3%

---

# Ajouter un module à un scénario

Un scénario se compose d’une série de modules indiquant comment les données doivent être transformées dans une application ou transférées entre des applications et des services web. Vous créez un module en ajoutant et en configurant des modules.

Cet article décrit le processus de base d’ajout d’un module à un scénario. Pour obtenir des instructions plus spécifiques sur l’ajout d’un scénario, consultez les autres articles sous [Ajouter des modules : index des articles](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

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

+++## Ajouter le premier module à un scénario

Le premier module d’un scénario est généralement un module de déclenchement.

Pour plus d’informations sur les modules de déclenchement, consultez la section [Modules de déclenchement](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) dans la présentation des modules.

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
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

1. Si vous ne vous trouvez pas dans l’éditeur de scénarios du scénario dans lequel vous souhaitez ajouter un module, cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Pour ajouter un module à un autre module, pointez sur la poignée droite du module après laquelle vous souhaitez ajouter un module, puis cliquez sur **Ajouter un autre module** lorsqu’il apparaît.

   La liste des connecteurs s’ouvre. Elle affiche les connecteurs déjà utilisés dans le scénario.

1. (Facultatif) Pour sélectionner un autre connecteur, cliquez sur **Ajouter un autre module** dans la liste, puis sélectionnez le connecteur. Vous pouvez saisir le nom du connecteur dans la barre de recherche de la liste pour filtrer la liste.
1. Configurez le module .

   Pour obtenir des instructions sur la configuration de modules spécifiques, consultez l’article pour les applications sélectionnées, répertoriées dans [Références des applications Fusion et de leurs modules : index des articles](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

## Insertion d’un module entre les modules existants d’un scénario

1. Si vous ne vous trouvez pas dans l’éditeur de scénarios du scénario dans lequel vous souhaitez ajouter un module, cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Cliquez sur le chemin en pointillé entre les modules où vous souhaitez insérer un module.
1. Dans le menu qui s’affiche, sélectionnez **Ajouter un module**.

La liste des connecteurs s’ouvre. Elle affiche les connecteurs déjà utilisés dans le scénario.

1. (Facultatif) Pour sélectionner un autre connecteur, cliquez sur **Ajouter un autre module** dans la liste, puis sélectionnez le connecteur. Vous pouvez saisir le nom du connecteur dans la barre de recherche de la liste pour filtrer la liste.
1. Configurez le module .

   Pour obtenir des instructions sur la configuration de modules spécifiques, consultez l’article pour les applications sélectionnées, répertoriées dans [Références des applications Fusion et de leurs modules : index des articles](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

>[!NOTE]
>
>Pour créer un lien vers un module spécifique, ajoutez des `?moduleId=<module-id>` à l’URL lors de l’affichage des pages suivantes :
>
>* Page de modification du scénario (l’URL se termine par `/edit`)
>* Exécution d’un scénario spécifique (l’URL se termine par `/logs/<log-id>`)
>
>`<module-id>` fait référence au nombre en regard du libellé du module lors de l’affichage du scénario.
>
>Cela peut s’avérer utile lors du débogage de scénarios ou de la copie de la configuration du module.
