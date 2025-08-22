---
title: Déboguer un scénario
description: Le Devtool d’Adobe Workfront Fusion vous permet de comprendre des scénarios et de résoudre les problèmes qui y sont liés. Le Devtool ajoute un panneau supplémentaire aux outils de développement Chrome. Grâce à ce panneau du débogueur, vous pouvez vérifier toutes les exécutions manuelles de votre scénario, réviser toutes les opérations effectuées et afficher les détails de chaque appel API effectué. Vous pouvez voir quel module, quelle opération ou quelle réponse unique a provoqué l’erreur et utiliser ces connaissances pour affiner votre scénario.
author: Becky
feature: Workfront Fusion
exl-id: 34215370-27e3-4c28-8bd1-a16268900b86
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1483'
ht-degree: 73%

---

# Déboguer un scénario

L’outil Adobe Workfront Fusion Developer vous aide à comprendre et à résoudre les problèmes liés aux scénarios. À l’aide de l’outil Devtool, vous pouvez vérifier toutes les exécutions manuelles de votre scénario, passer en revue toutes les opérations effectuées et afficher les détails de chaque appel API effectué. Vous pouvez voir quel module, quelle opération ou quelle réponse unique a provoqué l’erreur et utiliser ces connaissances pour affiner votre scénario.

>[!NOTE]
>
>La connexion au panneau du débogueur sera limitée ou indisponible pour les scénarios confidentiels, les exécutions automatiques et les opérations réussies.

Pour une vidéo d’introduction et une présentation de l’outil Fusion Devtool, voir

* [Outil de développement de Fusion](https://video.tv.adobe.com/v/3427031/){target=_blank}
* [Présentation du Devtool](https://experienceleague.adobe.com/fr/docs/workfront-learn/tutorials-workfront/fusion/troubleshooting-and-error-handling/dev-tool-walkthrough)

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tous</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licence Adobe Workfront</td> 
   <td> <p>Nouveau : Standard</p><p>Ou</p><p>Actuelle : [!UICONTROL Work] ou niveau supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licence Adobe Workfront Fusion **</td> 
   <td>
   <p>Actuel : aucune exigence de licence Workfront Fusion.</p>
   <p>Ou</p>
   <p>Héritée : n’importe laquelle. </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Nouveau :</p> <ul><li>Plan Workfront [!UICONTROL Select] ou [!UICONTROL Prime] : votre entreprise doit acheter Adobe Workfront Fusion.</li><li>Plan Workfront [!UICONTROL Ultimate] : Workfront Fusion est inclus.</li></ul>
   <p>Ou</p>
   <p>Actuel : votre entreprise doit acheter Adobe Workfront Fusion.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurations du niveau d’accès*</td> 
   <td> 
     <p>Vous devez être administrateur ou administratrice Workfront Fusion pour votre entreprise.</p>
     <p>Vous devez être un administrateur Workfront Fusion pour votre équipe.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Accès à l’outil de développement

Si vous utilisez Fusion dans Adobe Unified Shell ou avez mis à jour votre expérience avec Fusion, vous pouvez accéder à l’outil Développement à partir de l’éditeur de scénarios.

1. Cliquez sur l’icône **Outils d’assistance** ![Outils d’assistance](assets/debugger-icon.png) située en bas de l’écran.

Ou :

1. Accédez à l’éditeur de scénarios pour le scénario que vous souhaitez déboguer.

   Pour localiser l’éditeur de scénarios, voir [L’éditeur de scénarios](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md).

1. Cliquez avec le bouton droit dans une zone vide de la page (et non sur un module).
1. Sélectionnez **Ouvrir le Devtool**.

## Utilisation de l’outil de développement Workfront Fusion

Le Devtool de Workfront Fusion est divisé en trois sections principales. Vous pouvez les trouver dans le panneau de gauche de votre fenêtre Devtool.

* [Live Stream](#live-stream)
* [Débogueur de scénario](#scenario-debugger)
* [Outils](#tools)

### Live Stream

Le Live Stream affiche ce qui se passe en arrière-plan lorsque vous cliquez sur Exécuter une fois dans votre scénario.

1. Cliquez sur l’icône **[!UICONTROL Diffusion en direct]** ![Icône de diffusion en direct](assets/live-stream-icon.png) pour ouvrir la section Diffusion en direct .
1. Effectuez l’une des opérations suivantes :

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <thead> 
     <tr> 
      <th>Action</th> 
      <th>Instructions</th> 
     </tr> 
    </thead> 
    <tbody> 
     <tr> 
      <td role="rowheader">Afficher les informations sur la requête</td> 
      <td> <p>Vous pouvez afficher les informations suivantes pour chaque module dans votre scénario.</p> 
       <ul> 
        <li> <p>En-têtes de la requête (URL du point d’entrée de l’API, méthode HTTP, heure et date d’appel de la requête, en-têtes de la requête et chaîne de requête)</p> </li> 
        <li> <p>Corps de la requête</p> </li> 
        <li> <p>En-têtes de la réponse</p> </li> 
        <li> <p>Corps de la réponse</p> </li> 
       </ul> <p>Pour afficher ces informations, cliquez sur l’onglet approprié dans le panneau de droite de l’outil Workfront Fusion Devtool.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Rechercher des événements par contenu</p> </td> 
      <td> <p>Saisissez le terme de recherche dans le champ de recherche du panneau de gauche de l’outil de développement Workfront Fusion pour afficher uniquement les requêtes contenant le terme de recherche.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Effacer la liste des requêtes </p> </td> 
      <td> <p>Cliquez sur l’icône de corbeille dans le coin supérieur droit du panneau de gauche du Devtool pour effacer la liste des requêtes enregistrées par le Devtool de Workfront Fusion. </p> </td> 
     </tr> 
     <!--<tr> 
      <td role="rowheader"> <p>Enable Console Logging</p> </td> 
      <td> <p>Click the computer icon <img src="assets/console-computer-icon.png"> in the top-right corner of the Devtool's left panel.</p> <p>Logging in the console is enabled when the computer icon is green.</p> </td> 
     </tr>-->
     <tr> 
      <td role="rowheader"> <p>Récupérer la requête au format JSON brut ou cURL</p> </td> 
      <td> 
       <ul> 
        <li> <p><strong>JSON brut</strong> </p> <p>Cliquez sur <strong>[!UICONTROL Copy RAW]</strong> dans le coin supérieur droit du volet de droite du Devtool.</p> </li> 
        <li> <p><strong>cURL</strong> </p> <p>Cliquez sur <strong>[!UICONTROL Copy cURL]</strong> dans le coin supérieur droit du volet de droite du Devtool.</p> </li> 
       </ul> </td> 
     </tr> 
    </tbody> 
   </table>

### Débogueur de scénario

Le débogueur de scénario est utile pour les scénarios plus complexes. Il affiche l’historique du scénario qui s’exécute et vous permet de rechercher les modules par leur nom ou ID.

1. Cliquez sur l’icône **[!UICONTROL Débogueur de scénario]** ![icône du débogueur](assets/scenario-debugger-icon.png) pour ouvrir le débogueur de scénario.
1. (Facultatif) Saisissez le terme de recherche (nom ou ID de module) dans le champ de recherche.
1. Cliquez sur le nom du module.
1. Cliquez sur l’opération pour afficher les détails de la requête.

### Outils

L’outil de développement Workfront Fusion comporte des outils qui facilitent la configuration de votre scénario.

1. Cliquez sur l’icône **[!UICONTROL Outils]** ![Icône des outils de la console](assets/console-tools-icon.png) pour ouvrir les outils.
1. Sélectionnez l’outil que vous souhaitez utiliser.
1. Configurez les champs comme indiqué ci-dessous.
1. Cliquez sur **[!UICONTROL Exécuter]**.

Outils et leurs champs :

* [Cibler un module](#focus-a-module)
* [Rechercher des modules par mappage](#find-modules-by-mapping)
* [Obtenir les métadonnées de l’application](#get-app-metadata)
* [Copier le mappage](#copy-mapping)
* [Copier le filtre](#copy-filter)
* [Copier le nom du module](#copy-module-name)
* [Permuter la connexion](#swap-connection)
* [Permuter la variable](#swap-variable)
* [Base 64](#base-64)
* [Remapper la source](#remap-source)

#### [!UICONTROL Cibler un module]

Ouvre les paramètres du module spécifié par ID.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Module ID]</td>
        <td>Saisissez l’ID du module pour ouvrir ses paramètres.</td>
    </tr>
</table>

#### [!UICONTROL Rechercher des modules par mappage]

Permet de rechercher les valeurs des modules pour un terme spécifique. La sortie inclut les ID des modules qui contiennent le terme recherché.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Keyword]</td> 
   <td> <p> Saisissez le terme à rechercher. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Use Only Values]</p> </td> 
   <td> <p>Activez cette option pour rechercher uniquement dans les valeurs des champs du module.</p> <p>Désactivez cette option pour rechercher également dans les noms des champs du module.</p> <p>La recherche est effectuée par le biais des paramètres de nom et de libellé.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obtenir les métadonnées de l’application]

Récupère les métadonnées de l’application par le nom ou l’ID du module de l’application. Cette fonction est utile, par exemple, lorsque vous devez connaître la version de l’application utilisée dans votre scénario.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Source Module]</td>
        <td>Sélectionnez le module dont vous souhaitez récupérer les métadonnées.</td>
    </tr>
</table>

#### [!UICONTROL Copier le mappage]

Copie les valeurs du module source vers le module cible.

>[!CAUTION]
>
>Veillez à définir les modules source et cible appropriés. Si vous sélectionnez un autre type de module, les valeurs du module cible seront supprimées.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
   <td> <p> Sélectionnez le module ou saisissez l’ID du module dont vous souhaitez copier les valeurs de champ.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Target Module]</p> </td> 
   <td> <p>Sélectionnez le module ou saisissez l’ID du module dans lequel vous souhaitez insérer les valeurs du module source.</p> <p>Important : les valeurs du module cible seront remplacées.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Copier le filtre]

Copie les paramètres de filtre du module source vers le module cible.

>[!NOTE]
>
>L’action de copie est effectuée sur le filtre placé sur le côté gauche du module sélectionné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
   <td> <p> Sélectionnez le module ou saisissez l’identifiant du module à partir duquel vous souhaitez copier les valeurs de filtre.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Target Module]</p> </td> 
   <td> <p>Sélectionnez le module ou saisissez l’identifiant du module dans lequel vous souhaitez insérer les valeurs de filtre du module source.</p> <p>Important : les valeurs du module cible seront remplacées.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Preserve Fallback Route setting]</p> </td> 
   <td> <p>Le filtre source est défini comme l’itinéraire de secours. Activez cette option pour définir également le filtre cible comme itinéraire de secours.</p> </td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Copier le nom du module]

Copie le nom du module sélectionné dans le presse-papiers.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Module] </td> 
   <td> <p>Sélectionnez le module dont vous souhaitez copier le nom.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Permuter la connexion]

Duplique une connexion du module source à tous les modules de la même application dans le scénario.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Source Module]</td>
        <td>Sélectionnez le module ou saisissez l’identifiant du module à partir duquel vous souhaitez dupliquer la connexion.</td>
    </tr>
</table>

#### [!UICONTROL Permuter la variable]

Recherche les variables spécifiées dans le scénario et les remplace par une nouvelle variable.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variable to Find]</td> 
   <td> <p> Recherchez la pilule de variable à remplacer dans le module de variable de votre scénario et copiez-la dans ce champ ([!UICONTROL Variable to Find]). Dans le champ, elle apparaît avec des accolades doubles. Exemple : <code>&#123;&#123;5.value&#125;&#125;</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Replace With]</p> </td> 
   <td> <p>Recherchez la pilule de variable avec laquelle vous souhaitez remplacer la variable dans le module de variables de votre scénario et copiez-la dans ce champ ([!UICONTROL Variable to Find]). Dans le champ, elle apparaît avec des accolades doubles. Exemple : <code>&#123;&#123;5.value&#125;&#125;</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Module]</p> </td> 
   <td> <p>Sélectionnez le module de variables dans lequel vous souhaitez remplacer la variable. Si aucun module n’est sélectionné, la variable sera remplacée dans l’ensemble du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Base 64]

Permet de coder les données saisies en Base64 ou de décoder du Base64. Certaines requêtes sont codées en Base64. Cet outil est utile lorsque vous souhaitez rechercher des données spécifiques dans la requête codée.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Operation] </td> 
   <td> <p>Indiquez si vous souhaitez coder les données du champ [!UICONTROL Raw Data] en Base64 ou décoder Base64 en données brutes.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Raw Data]</p> </td> 
   <td> <p> Saisissez les données que vous souhaitez encoder en Base64, ou les données Base64 que vous souhaitez décoder en données brutes, en fonction de l’option sélectionnée dans le champ [!UICONTROL Operation] ci-dessus.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remapper la source]

Vous permet de modifier la source de mappage d’un module à un autre.

Vous devez d’abord ajouter le module que vous voulez utiliser comme module source à l’itinéraire de votre scénario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module] </td> 
   <td> <p> Sélectionnez le module que vous souhaitez remplacer en tant que source de mappage pour les autres modules de votre scénario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Target Module]</p> </td> 
   <td> <p>Sélectionnez le module à utiliser comme nouvelle source de mappage.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Module to Edit]</p> </td> 
   <td> <p>Sélectionnez le module pour lequel vous souhaitez modifier le mappage si vous ne souhaitez pas modifier le mappage dans l’ensemble du scénario. </p> </td> 
  </tr> 
 </tbody> 
</table>
