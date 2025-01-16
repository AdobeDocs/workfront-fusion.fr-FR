---
title: Modules GitHub
description: Dans unscénario  [!DNL Adobe Workfront Fusion] , vous pouvez automatiser les workflows qui utilisent GitHub et les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: d9e6c26c-8770-40bc-a83a-8c05f86e4a3f
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1494'
ht-degree: 80%

---

# Modules [!DNL GitHub]

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!UICONTROL GitHub] et le connecter à plusieurs applications et services tiers.

## Conditions d’accès

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] formule*</td>
  <td> <p>[!UICONTROL Pro] ou une version ultérieure</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licence*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licence**</td> 
   <td>
   <p>Exigences de licence actuelles : aucune exigence de licence [!DNL Workfront Fusion] requise.</p>
   <p>Ou</p>
   <p>Ancienne exigence de licence : [!UICONTROL [!DNL Workfront Fusion] pour l’automatisation et l’intégration du travail] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Exigences actuelles du produit : si vous disposez du plan de [!DNL Adobe Workfront] [!UICONTROL Select] ou [!UICONTROL Prime], votre entreprise doit acheter du [!DNL Adobe Workfront Fusion] et [!DNL Adobe Workfront] utiliser les fonctionnalités décrites dans cet article. [!DNL Workfront Fusion] est inclus dans le plan de [!DNL Workfront] [!UICONTROL Ultimate].</p>
   <p>Ou</p>
   <p>Exigences liées aux produits hérités : votre entreprise doit acheter [!DNL Adobe Workfront Fusion] ainsi qu’[!DNL Adobe Workfront] pour utiliser la fonctionnalité décrite dans cet article.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Pour connaître la formule, le type de licence ou l’accès dont vous disposez, contactez votre équipe d’administration [!DNL Workfront].

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Conditions préalables

Pour utiliser les modules [!DNL GitHub], vous devez disposer d’un compte [!DNL GitHub].

## Connecter [!DNL GitHub] à [!DNL Workfront Fusion]

Pour savoir comment connecter votre compte [!DNL GitHub] à [!UICONTROL Workfront Fusion], voir [Créer une connexion à [!UICONTROL Adobe Workfront Fusion] - Instructions de base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

## Modules [!DNL GitHub] et leurs champs.

Lorsque vous configurez des modules [!DNL GitHub], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL GitHub] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Déclencheurs](#triggers)
* [Actions](#actions)

### Déclencheurs

* [[!UICONTROL Watch Issues]](#watch-issues)
* [[!UICONTROL Watch Repositories]](#watch-repositories)
* [[!UICONTROL Watch Forks]](#watch-forks)
* [[!UICONTROL Watch Comments]](#watch-comments)
* [[!UICONTROL Watch Pull Requests]](#watch-pull-requests)

#### [!UICONTROL Watch Issues]

Ce module se déclenche lorsqu’un nouveau problème est ajouté ou qu’un problème existant est modifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL GitHub] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL I want to watch]</td> 
   <td>Indiquez si vous souhaitez surveiller tous les référentiels ou un seul référentiel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Si vous avez choisi de ne surveiller les problèmes que dans un seul référentiel, sélectionnez le référentiel à surveiller.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned issues]</td> 
   <td>Définissez le nombre maximal de résultats avec lesquels [!DNL Workfront Fusion] fonctionnera avec pendant un cycle. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch]</td> 
   <td>Sélectionnez si vous souhaitez ne regarder que les nouveaux problèmes ou les nouveaux problèmes et toutes les modifications.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Vous pouvez filtrer les problèmes que vous souhaitez regarder en fonction de votre association à eux.</p> 
    <ul> 
     <li>[!UICONTROL All issues]</li> 
     <li>[!UICONTROL Only issues assigned to me]</li> 
     <li>[!UICONTROL Only issues created by me]</li> 
     <li>[!UICONTROL Only issues mentioning me]</li> 
     <li>[!UICONTROL Only issues I'm subscribed to updates for]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td>Sélectionnez si vous souhaitez ne regarder que les problèmes ouverts ou uniquement les problèmes clôturés. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels]</td> 
   <td>Ajoutez une balise. Le module recherche les problèmes liés à cette balise.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Repositories]

Ce module se déclenche lorsqu’un référentiel est créé ou modifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL GitHub] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned repositories]</td> 
   <td>Définissez le nombre maximal de résultats avec lesquels [!DNL Workfront Fusion] fonctionnera avec pendant un cycle. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch]</td> 
   <td>Sélectionnez si vous souhaitez regarder les nouveaux référentiels et toutes les modifications, ou uniquement les nouveaux référentiels.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Forks]

Ce module se déclenche lors de la création d’une duplication.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL GitHub] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Sélectionnez le référentiel sur lequel vous souhaitez regarder les duplications.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned forks]</td> 
   <td>Définissez le nombre maximal de résultats avec lesquels [!DNL Workfront Fusion] fonctionnera avec pendant un cycle. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Comments]

Ce module se déclenche lorsqu’un nouveau commentaire est ajouté ou qu’un commentaire existant est modifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL GitHub] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Sélectionnez le référentiel que vous souhaitez regarder.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Issue number]</td> 
   <td>Si vous souhaitez limiter la recherche en recherchant uniquement les nouveaux commentaires apportés à un problème spécifique, saisissez le numéro du problème.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned issues]</td> 
   <td>Définissez le nombre maximal de résultats avec lesquels [!DNL Workfront Fusion] fonctionnera avec pendant un cycle. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch]</td> 
   <td>Sélectionnez si vous souhaitez ne regarder que les nouveaux commentaires ou les commentaires et toutes les modifications.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Pull Requests]

Ce module se déclenche lorsqu’une nouvelle demande de tirage est ajoutée ou qu’une demande de tirage existante est modifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL GitHub] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Sélectionnez le référentiel que vous souhaitez regarder.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned pull requests]</td> 
   <td>Définissez le nombre maximal de résultats avec lesquels [!DNL Workfront Fusion] fonctionnera avec pendant un cycle. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td>Indiquez si vous souhaitez surveiller les requêtes de [!UICONTROL only open pull], les [!UICONTROL only closed ones] ou toutes les requêtes d’extraction. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch]</td> 
   <td>Sélectionnez si vous souhaitez ne regarder que les nouvelles demandes de tirage ou les nouvelles demandes de tirage et toutes les modifications.</td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [[!UICONTROL Search for an issue]](#search-for-an-issue)
* [[!UICONTROL Create an issue]](#create-an-issue)
* [[!UICONTROL Update an issue]](#update-an-issue)
* [[!UICONTROL Get an issue]](#get-an-issue)
* [[!UICONTROL Add assignees]](#add-assignees)
* [[!UICONTROL Remove assignees]](#remove-assignees)
* [[!UICONTROL Add labels to an issue]](#add-labels-to-an-issue)
* [[!UICONTROL Remove a label from an issue]](#remove-a-label-from-an-issue)
* [[!UICONTROL Create a comment]](#create-a-comment)
* [[!UICONTROL List comments]](#list-comments)

#### [!UICONTROL Search for an issue]

Ce module recherche des problèmes qui correspondent à vos critères de recherche.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL GitHub] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned issues]</td> 
   <td>Définissez le nombre maximal de résultats avec lesquels [!DNL Workfront Fusion] fonctionnera pendant un cycle (le nombre de répétitions par exécution de scénario). </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort by]</td> 
   <td> <p>Sélectionnez le mode de tri des résultats de recherche.</p> 
    <ul> 
     <li> <p>[!UICONTROL Best match] </p> </li> 
     <li>[!UICONTROL Date created]</li> 
     <li>[!UICONTROL Date updated]</li> 
     <li>[!UICONTROL Number of comments]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort direction]</td> 
   <td> <p>Sélectionnez ascendant ou descendant. </p> <p>Pour les dates, si vous sélectionnez <strong>[!UICONTROL descending]</strong>, la date la plus récente est renvoyée en premier. </p> <p>Par [!UICONTROL number of comments], si vous sélectionnez <strong>[!UICONTROL descending]</strong>, le problème contenant le plus grand nombre de commentaires sera renvoyé en premier.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td>Saisissez ou mappez votre demande de recherche. Pour une description détaillée des options de recherche, voir <a href="https://docs.github.com/fr/search-github/searching-on-github/searching-issues-and-pull-requests">Rechercher des problèmes et des demandes d’extraction</a> sur le site d’aide de [!DNL GitHub].</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an issue]

Ce module crée un problème dans le référentiel sélectionné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL GitHub] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Sélectionnez le référentiel dans lequel vous souhaitez créer un problème.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assignee]</td> 
   <td>Sélectionnez les personnes que vous souhaitez affecter au problème. Les cessionnaires disponibles comprennent toute personne bénéficiant d’autorisations d’écriture sur le référentiel et les membres de l’entreprise disposant d’autorisations de lecture sur le référentiel. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Milestone]</td> 
   <td>Sélectionnez le jalon que vous souhaitez associer au nouveau problème. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels]</td> 
   <td>Sélectionnez les libellés à appliquer au nouveau problème. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title]</td> 
   <td>Saisissez ou mappez un titre pour le nouveau problème.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Saisissez ou mappez le corps du problème, comme une description ou des informations supplémentaires.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update an issue]

Ce module met à jour un problème [!DNL GitHub] existant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL GitHub] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Sélectionnez le référentiel dans lequel vous souhaitez mettre à jour un problème.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assignee]</td> 
   <td>Sélectionnez les personnes que vous souhaitez affecter au problème. Les cessionnaires disponibles incluent toute personne disposant d’autorisations d’écriture sur le référentiel et les membres de l’organisation disposant d’autorisations de lecture sur le référentiel. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Milestone]</td> 
   <td>Sélectionnez le jalon que vous souhaitez associer au problème. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels]</td> 
   <td>Sélectionnez les libellés à appliquer au problème. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Saisissez ou mappez le numéro du problème que vous souhaitez mettre à jour. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td>Sélectionnez le statut vers lequel vous souhaitez mettre à jour le problème.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title]</td> 
   <td>Saisissez ou mappez un titre pour le problème.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Saisissez ou mappez le corps du problème, comme une description ou des informations supplémentaires.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an issue]

Ce module récupère les détails du problème indiqué.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL GitHub] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Sélectionnez le référentiel contenant le problème sur lequel vous souhaitez récupérer les détails.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Saisissez ou mappez le numéro du problème dont vous souhaitez récupérer les détails. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add assignees]

Ce module ajoute des cessionnaires au problème indiqué.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL GitHub] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Sélectionnez le référentiel contenant le problème auquel vous souhaitez ajouter les cessionnaires.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assignee]</td> 
   <td>Sélectionnez les personnes que vous souhaitez affecter au problème. Les cessionnaires disponibles incluent toute personne disposant d’autorisations d’écriture sur le référentiel et les membres de l’organisation disposant d’autorisations de lecture sur le référentiel. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Saisissez ou mappez le numéro du problème auquel vous souhaitez ajouter des cessionnaires. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove assignees]

Ce module supprime les cessionnaires du problème indiqué.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL GitHub] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Sélectionnez le référentiel contenant le problème à partir duquel vous souhaitez supprimer les cessionnaires.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assignee]</td> 
   <td>Sélectionnez les personnes que vous souhaitez supprimer du problème. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Saisissez ou mappez le numéro du problème à partir duquel vous souhaitez supprimer les cessionnaires. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add labels to an issue]

Ce module ajoute des libellés à un problème. Les libellés sont définis au niveau du référentiel et ne peuvent être créés que par une personne disposant d’un accès en écriture au référentiel.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL GitHub] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Sélectionnez le référentiel contenant le problème auquel vous souhaitez ajouter des libellés.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels]</td> 
   <td>Sélectionnez les libellés à ajouter au problème.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Saisissez ou mappez le numéro du problème auquel vous souhaitez ajouter des libellés.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove a label from an issue]

Ce module supprime un seul libellé d’un problème.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL GitHub] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Sélectionnez le référentiel contenant le problème à partir duquel vous souhaitez supprimer un libellé.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels]</td> 
   <td>Sélectionnez le libellé à supprimer du problème.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Saisissez ou mappez le numéro du problème à partir duquel vous souhaitez supprimer un libellé.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a comment]

Ce module crée un commentaire sur le problème indiqué.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL GitHub] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Sélectionnez le référentiel contenant le problème sur lequel vous souhaitez créer un commentaire.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Saisissez ou mappez le numéro du problème sur lequel vous souhaitez créer un commentaire.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>Saisissez ou mappez le contenu du commentaire.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List comments]

Ce module répertorie tous les commentaires sur le problème indiqué.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL GitHub] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Repository]</td> 
   <td>Sélectionnez le référentiel contenant le problème à partir duquel vous souhaitez répertorier les commentaires.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number]</td> 
   <td>Saisissez ou mappez le numéro du problème à partir duquel vous souhaitez répertorier les commentaires.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Since]</td> 
   <td>Le module renvoie les commentaires créés après cette date. Pour obtenir la liste des formats de date pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coercition de type dans [!DNL Adobe Workfront Fusion]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned comments]</td> 
   <td>Définissez le nombre maximal de résultats avec lesquels [!DNL Workfront Fusion] fonctionnera avec pendant un cycle. </td> 
  </tr> 
 </tbody> 
</table>

<!--
<h2>Troubleshooting</h2>
-->

<!--
<h3>Module does not receive any events</h3>
-->

<!--
<p>If a module does not receive any events, check the webhook settings in Github and make sure that:</p>
-->

<!--
  <p>You have set the correct type of event that the chosen module should receive</p>
  -->

<!--
  <p>You have entered the correct Payload URL</p>
  -->
