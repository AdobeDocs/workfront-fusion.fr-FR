---
title: Ajouter un module dans un scénario
description: Cet article décrit le processus de base d’ajout d’un module à un scénario.
author: Becky
feature: Workfront Fusion
exl-id: f3757468-3e11-4862-a83e-ed447805545b
TQID: 'https://experienceleague.adobe.com/R2JCX7aaYzmYHgiLqj1WDlVFHI-s-qanltoOrycQ5JU'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: cc160f0e8c2465b4f102b6d1755088335b2a9fe5
workflow-type: tm+mt
source-wordcount: '1508'
ht-degree: 8%
---
# Ajouter un module dans un scénario

Un scénario se compose d’une série de modules qui indiquent comment les données doivent être transformées dans une application ou transférées entre les applications et les services web. Vous créez un module en ajoutant et en configurant des modules.

Cet article décrit le processus de base d’ajout d’un module à un scénario. Pour obtenir des instructions plus spécifiques sur l’ajout d’un scénario, consultez les autres articles sous [Ajouter des modules : index des articles](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

>[!NOTE]
>
>Workfront Fusion effectue la transition de l’éditeur de scénarios vers une nouvelle expérience . Au cours de cette transition, les expériences classique et nouvelle sont disponibles et vous pouvez basculer entre elles à tout moment. Nous vous recommandons d’utiliser la nouvelle expérience . Pour plus d’informations, voir [Expériences nouvelles et classiques](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences) dans l’éditeur de scénarios d’article.

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

## Ajouter le premier module à un scénario

Le premier module d’un scénario est généralement un module de déclenchement.

Pour plus d’informations sur les modules de déclenchement, consultez la section [Modules de déclenchement](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) dans la présentation des modules.

* [Ajouter le premier module dans la nouvelle expérience (Recommandé)](#add-the-first-module-in-the-new-experience-recommended)
* [Ajout du premier module à l’expérience classique](#add-the-first-module-in-the-classic-experience)

### Ajouter le premier module dans la nouvelle expérience (Recommandé)

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Commencez à créer un scénario en cliquant sur **Créer un nouveau scénario** dans le coin supérieur droit de l’écran.

   L’éditeur de scénario s’ouvre, avec un module d’espace réservé et la liste des connecteurs disponibles.

   ![Module Espace réservé](/help/workfront-fusion/build-practice-scenarios/assets/new-placeholder-module.png)

   ![Sélecteur d’application et de service](/help/workfront-fusion/build-practice-scenarios/assets/new-connector-picker.png)

1. Sélectionnez le connecteur ou le webhook qui démarrera ce scénario :

   * Parcourez les ressources par catégorie à l’aide du panneau de gauche ([!UICONTROL Favoris], [!UICONTROL Toutes les applications], [!UICONTROL Adobe Workfront], [!UICONTROL Adobe Firefly Services], [!UICONTROL Adobe Creative &amp; Content], [!UICONTROL Adobe Cloud Services], [!UICONTROL IA générative] ou [!UICONTROL Built-in]), ou
   * Saisissez un terme dans la zone de recherche. Les résultats sont mis à jour au fur et à mesure que vous tapez et les correspondances de connecteur sont répertoriées avant les correspondances de nom et de description du module.

1. Cliquez sur le module à ajouter au scénario.

1. Configurez le module .

   Les paramètres du module s’ouvrent dans le panneau sur le côté droit de la zone de travail.

   Pour obtenir des instructions sur la configuration de modules spécifiques, consultez l’article pour les applications sélectionnées, répertoriées dans [Références des applications Fusion et de leurs modules : index des articles](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

>[!NOTE]
>
>* Dans la liste des connecteurs, les badges identifient les applications privées, premium et bêta.
>* Les modules pour les applications volumineuses sont organisés en groupes.
>* Lorsque vous ajoutez un gestionnaire d’erreurs, les directives sont répertoriées en premier.
>* Si un connecteur comporte plusieurs versions, vous pourrez sélectionner la version après avoir sélectionné le connecteur.

>[!NOTE]
>
>Si vous avez supprimé le premier module d’un scénario et souhaitez le remplacer, cliquez sur le module d’espace réservé pour afficher la liste des connecteurs.

### Ajout du premier module à l’expérience classique

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

* [Ajouter un autre module dans la nouvelle expérience (Recommandé)](#add-another-module-in-the-new-experience-recommended)
* [Ajouter un autre module dans l’expérience classique](#add-another-module-in-the-classic-experience)

### Ajouter un autre module dans la nouvelle expérience (Recommandé)

1. Si vous ne vous trouvez pas dans l’éditeur de scénarios du scénario dans lequel vous souhaitez ajouter un module, cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Pour ajouter un module après un autre module, passez la souris sur le bord droit du module après lequel vous souhaitez ajouter un module, puis cliquez sur **Ajouter un autre module** lorsqu’il apparaît.

   La liste des connecteurs s’ouvre. Elle affiche les connecteurs déjà utilisés dans le scénario.

1. (Facultatif) Pour sélectionner un autre connecteur, cliquez sur **Ajouter un autre module** dans la liste, puis sélectionnez le connecteur :

   * Parcourez les ressources par catégorie à l’aide du panneau de gauche ([!UICONTROL Favoris], [!UICONTROL Toutes les applications], [!UICONTROL Adobe Workfront], [!UICONTROL Adobe Firefly Services], [!UICONTROL Adobe Creative &amp; Content], [!UICONTROL Adobe Cloud Services], [!UICONTROL IA générative] ou [!UICONTROL Built-in]), ou
   * Saisissez un terme dans la zone de recherche. Les résultats sont mis à jour au fur et à mesure que vous tapez et les correspondances de connecteur sont répertoriées avant les correspondances de nom et de description du module.

1. Cliquez sur le module à ajouter au scénario.

1. Configurez le module .

   Les paramètres du module s’ouvrent dans le panneau sur le côté droit de la zone de travail.

   Pour obtenir des instructions sur la configuration de modules spécifiques, consultez l’article pour les applications sélectionnées, répertoriées dans [Références des applications Fusion et de leurs modules : index des articles](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

### Ajouter un autre module dans l’expérience classique

1. Si vous ne vous trouvez pas dans l’éditeur de scénarios du scénario dans lequel vous souhaitez ajouter un module, cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Pour ajouter un module à un autre module, pointez sur la poignée droite du module après laquelle vous souhaitez ajouter un module, puis cliquez sur **Ajouter un autre module** lorsqu’il apparaît.

   La liste des connecteurs s’ouvre. Elle affiche les connecteurs déjà utilisés dans le scénario.

1. (Facultatif) Pour sélectionner un autre connecteur, cliquez sur **Ajouter un autre module** dans la liste, puis sélectionnez le connecteur. Vous pouvez saisir le nom du connecteur dans la barre de recherche de la liste pour filtrer la liste.
1. Configurez le module .

   Pour obtenir des instructions sur la configuration de modules spécifiques, consultez l’article pour les applications sélectionnées, répertoriées dans [Références des applications Fusion et de leurs modules : index des articles](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

## Insertion d’un module entre les modules existants d’un scénario

* [Insertion d’un module dans la nouvelle expérience (recommandé)](#insert-a-module-in-the-new-experience-recommended)
* [Insertion d’un module dans l’expérience classique](#insert-a-module-in-the-classic-experience)

### Insertion d’un module dans la nouvelle expérience (recommandé)

1. Si vous ne vous trouvez pas dans l’éditeur de scénarios du scénario dans lequel vous souhaitez ajouter un module, cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Cliquez avec le bouton droit sur le chemin d’accès entre les modules où vous souhaitez insérer un module, puis sélectionnez **Ajouter un module**.

   ![Ajouter un module entre les modules existants](assets/add-a-module-between-modules.png)

   La liste des connecteurs s’ouvre. Elle affiche les connecteurs déjà utilisés dans le scénario.

1. (Facultatif) Pour sélectionner un autre connecteur, cliquez sur **Ajouter un autre module** dans la liste, puis sélectionnez le connecteur :

   * Parcourez les ressources par catégorie à l’aide du panneau de gauche ([!UICONTROL Favoris], [!UICONTROL Toutes les applications], [!UICONTROL Adobe Workfront], [!UICONTROL Adobe Firefly Services], [!UICONTROL Adobe Creative &amp; Content], [!UICONTROL Adobe Cloud Services], [!UICONTROL IA générative] ou [!UICONTROL Built-in]), ou
   * Saisissez un terme dans la zone de recherche. Les résultats sont mis à jour au fur et à mesure que vous tapez et les correspondances de connecteur sont répertoriées avant les correspondances de nom et de description du module.

1. Cliquez sur le module à ajouter au scénario.

1. Configurez le module .

   Les paramètres du module s’ouvrent dans le panneau sur le côté droit de la zone de travail.

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

### Insertion d’un module dans l’expérience classique

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
