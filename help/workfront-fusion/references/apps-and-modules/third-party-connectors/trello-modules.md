---
title: Modules Trello
description: Dans un scénario  [!DNL Adobe Workfront Fusion] , vous pouvez automatiser les workflows qui utilisent Trello et le connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: 5df5cd2b-ad4c-4a02-9d0c-7cee35232f93
source-git-commit: 46bb455ecc0820dc68468f9f810bd51074c224fa
workflow-type: tm+mt
source-wordcount: '4370'
ht-degree: 58%

---

# Modules [!UICONTROL Trello]

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!UICONTROL Trello] et le connecter à plusieurs applications et services tiers.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <td> <p>Nouveau : Standard</p><p>Ou</p><p>En cours : Travail ou version ultérieure</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licence Adobe Workfront Fusion **</td> 
   <td>
   <p>Actuel : aucune exigence de licence Workfront Fusion.</p>
   <p>Ou</p>
   <p>Hérité : Workfront Fusion pour l’automatisation et l’intégration du travail </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Nouveau :</p> <ul><li>Sélectionnez ou le package Prime Workfront : votre entreprise doit acheter Adobe Workfront Fusion.</li><li>Package Ultimate Workfront : Workfront Fusion est inclus.</li></ul>
   <p>Ou</p>
   <p>Actuel : votre entreprise doit acheter Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Conditions préalables

Pour utiliser les modules [!DNL Trello], vous devez disposer d’un compte [!UICONTROL Trello].

## Informations sur l’API Trello

Le connecteur Trello utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td> https://api.trello.com/1</td>
  </tr> 
  <tr> 
   <td role="rowheader">Version de l’API</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v4.12.37</td> 
  </tr>
 </tbody> 
 </table>

## Connecter [!UICONTROL Trello] à [!DNL Workfront Fusion]

Pour suivre la procédure de connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], consultez la section [Créer une connexion à  [!DNL Adobe Workfront Fusion]  - Instructions de base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md).

## Modules et champs [!UICONTROL Trello]

Lorsque vous configurez les modules [!UICONTROL Trello], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!UICONTROL Trello] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Panneaux](#boards)
* [Listes](#lists)
* [vignette](#cards)
* [Membres](#members)
* [Listes de contrôle](#checklists)
* [Libellés](#labels)
* [Commentaires](#comments)

### Panneaux

+++ **[!UICONTROL Archive or Unarchive a Board]**

Ce module d’action ferme (archive) ou rouvre (désarchive) un panorama que vous spécifiez.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Saisissez ou mappez l’ID du panorama que vous souhaitez fermer ou rouvrir.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archive or unarchive]</td> 
   <td> <p> Choisissez de fermer (archiver) ou de rouvrir (désarchiver) le panorama.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Assign a Member to a Board]**

Ce module d’action affecte une personne membre à un panorama que vous spécifiez.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Sélectionnez le panorama dans lequel vous souhaitez ajouter une personne membre.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email address]</td> 
   <td> <p> Saisissez ou mappez l’adresse e-mail de la personne membre que vous souhaitez ajouter au panorama.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Member type]</p> </td> 
   <td> <p>Sélectionnez le type de membre que vous souhaitez affecter au nouveau membre.</p> 
    <ul> 
     <li><strong>[!UICONTROL Admin]</strong>: un administrateur de panorama peut effectuer n’importe quelle action sur le panorama.</li> 
     <li><strong>[!UICONTROL Normal]</strong>: un membre normal est simplement un membre du conseil d’administration.</li> 
     <li><strong>[!UICONTROL Observer]</strong>: un observateur est un membre disposant d’un accès en lecture seule au panorama. <br>Les observateurs ne sont disponibles que pour les équipes disposant de [!UICONTROL Trello Business Class].</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Full name]</td> 
   <td> <p> Saisissez ou mappez le nom complet de l’utilisateur que vous souhaitez ajouter au panorama.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a Board]**

Ce module d’action crée un nouveau panorama avec les paramètres sélectionnés.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Saisissez ou mappez un nom pour le nouveau panorama.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td> <p>Saisissez ou mappez la description du panorama si nécessaire.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Organization ID]</p> </td> 
   <td> <p>Saisissez ou mappez l’ID de l’organisation. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Permission level]</p> </td> 
   <td> <p>Les panoramas possèdent des règles de vote et de commentaire différentes pour chaque niveau d’autorisation. Par exemple, si votre forum est [!UICONTROL Private] et que vous définissez les règles de vote et de commentaires comme [!UICONTROL All], vous recevez une erreur. </p> <p>Le vote et les commentaires sont limités aux groupes suivants pour chaque niveau d’autorisation :</p> 
    <ul> 
     <li><strong>[!UICONTROL Private]</strong>: 
      Membres, membres et observateurs</li> 
     <li><strong>[!UICONTROL For organization]</strong>: 
      Membres, membres et observateurs, membres de l'organisation</li> 
     <li><strong>[!UICONTROL Public]</strong>: 
      Membres, Membres et observateurs, Membres de l'organisation, Tous</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Voting]</p> </td> 
   <td> <p>Sélectionnez une option pour spécifier qui peut voter sur ce panorama. Voir le champ [!UICONTROL Permission level] pour connaître les limites de vote sur les niveaux d’autorisation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Comments]</p> </td> 
   <td> <p>Sélectionnez une option pour spécifier qui peut commenter les cartes de ce panorama. Voir le champ [!UICONTROL Permission level] pour commenter les limites sur les niveaux d’autorisation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Invitations]</p> </td> 
   <td> <p>Sélectionnez qui peut inviter d’autres personnes dans ce panorama.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Self-join]</p> </td> 
   <td> <p>Indiquez si les personnes membres de l’équipe peuvent rejoindre le panorama elles-mêmes ou si elles doivent être invitées.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Default labels]</p> </td> 
   <td> <p>Choisissez d’utiliser ou non le jeu de libellés par défaut pour le nouveau panorama.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Default lists]</p> </td> 
   <td> <p>Choisissez s’il faut ajouter l’ensemble de listes par défaut au panorama ([!UICONTROL To Do], [!UICONTROL Doing], [!UICONTROL Done]).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Board source ID]</p> </td> 
   <td> <p>Sélectionnez ou mappez l’ID du panorama que vous souhaitez copier dans le nouveau panorama.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Card Covers]</p> </td> 
   <td> <p>Sélectionnez <strong>[!UICONTROL Yes]</strong> si vous souhaitez activer les couvertures de carte pour le panorama.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Background]</p> </td> 
   <td> <p>Sélectionnez la couleur de l’arrière-plan ou de l’arrière-plan personnalisé.</p> <p>Remarque : les arrière-plans personnalisés ne sont disponibles que pour les abonnés [!UICONTROL Trello Gold and Business Class].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Background ID]</td> 
   <td> <p> Si vous avez choisi d’utiliser un arrière-plan personnalisé dans le champ [!UICONTROL Background] , saisissez ou mappez l’identifiant de l’arrière-plan que vous souhaitez utiliser.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Card aging]</p> </td> 
   <td> <p>Choisissez entre deux modes d’expiration des cartes. </p> 
    <ul> 
     <li><strong>[!UICONTROL Pirate mode]</strong>: les cartes se déchirent, jaunissent et se fissurent comme une vieille carte de pirate en vieillissant.</li> 
     <li><strong>[!UICONTROL Regular mode ]</strong>: les cartes deviennent progressivement plus transparentes à mesure qu’elles vieillissent. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Edit a Board]**

Ce module d’action permet de modifier les paramètres d’un panorama existant.

>[!SUCCESS]
>
><table style="table-layout:auto">
<col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Board ID]</p> </td> 
   <td> <p>Saisissez ou mappez l’ID de [!UICONTROL Trello] unique du panorama que le module doit créer. Vous pouvez récupérer l’ID du panorama à l’aide d’un autre module, tel que le module Surveiller les panoramas.</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/watch-boards.png"> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New name]</td> 
   <td> <p> Saisissez ou mappez un nouveau nom pour le panorama.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New description]</td> 
   <td> <p> Saisissez ou mappez une nouvelle description de panorama.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Organization ID]</p> </td> 
   <td> <p>Saisissez ou mappez l’ID de [!UICONTROL Trello] unique du panorama que le module doit modifier.  </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscribe] </td> 
   <td> <p>Sélectionnez une option pour spécifier si l’utilisateur propriétaire de la connexion utilisée par ce module est abonné au panorama.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Permission level]</p> </td> 
   <td> <p>Les panoramas possèdent des règles de vote et de commentaire différentes pour chaque niveau d’autorisation. Par exemple : si votre forum est [!UICONTROL Private] et que vous définissez les règles de vote et de commentaires comme [!UICONTROL All], vous recevez une erreur. </p> <p>Le vote et les commentaires sont limités aux groupes suivants pour chaque niveau d’autorisation :</p> 
    <ul> 
     <li><strong>[!UICONTROL Private]</strong>: 
      Membres, membres et observateurs</li> 
     <li><strong>[!UICONTROL For organization]</strong>: 
      Membres, membres et observateurs, membres de l'organisation</li> 
     <li><strong>[!UICONTROL Public]</strong>: 
      Membres, Membres et observateurs, Membres de l'organisation, Tous</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Voting]</p> </td> 
   <td> <p>Sélectionnez une option pour spécifier qui peut voter sur ce panorama. Voir le champ [!UICONTROL Permission level] pour connaître les limites de vote sur les niveaux d’autorisation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Comments]</p> </td> 
   <td> <p>Sélectionnez une option pour spécifier qui peut commenter les cartes de ce panorama. Voir le champ [!UICONTROL Permission level] pour commenter les limites sur les niveaux d’autorisation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Invitations] </td> 
   <td> <p>Indiquez qui peut inviter des personnes sur ce panorama.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Self-join]</td> 
   <td> <p> Indiquez si les personnes membres de l’équipe peuvent rejoindre le panorama elles-mêmes ou si elles doivent être invitées.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Card covers]</td> 
   <td> <p> Indiquez si les couvertures de cartes doivent être affichées sur ce panorama.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Background] </td> 
   <td> <p>Sélectionnez la couleur de l’arrière-plan ou de l’arrière-plan personnalisé.</p> <p>Remarque : les arrière-plans personnalisés ne sont disponibles que pour les abonnés [!UICONTROL Trello Gold and Business Class].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Background ID]</td> 
   <td> <p> Si vous avez choisi d’utiliser un arrière-plan personnalisé dans le champ [!UICONTROL Background] , saisissez ou mappez l’identifiant de l’arrière-plan que vous souhaitez utiliser.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Card aging]</p> </td> 
   <td> <p>Choisissez entre deux modes d’expiration des cartes. </p> 
    <ul> 
     <li><strong>[!UICONTROL Pirate mode]</strong>: les cartes se déchirent, jaunissent et se fissurent comme une vieille carte de pirate en vieillissant.</li> 
     <li><strong>[!UICONTROL Regular mode]</strong>: les cartes deviennent progressivement plus transparentes à mesure qu’elles vieillissent. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar feed enabled]</td> 
   <td> <p> Indiquez si le flux de calendrier est activé ou pas.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL <Color> label name]</td> 
   <td> <p> Affectez un nom au libellé de couleur souhaité.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archive] </td> 
   <td> <p>Sélectionnez une option pour indiquer si vous souhaitez archiver (fermer) le panorama. </p> </td> 
  </tr> 
 </tbody> 
</table>


+++

+++ **[!UICONTROL Get a Board]**

Ce module d’action permet de récupérer les détails d’un panorama.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Board ID]</p> </td> 
   <td> <p>Saisissez ou mappez l’identifiant du panorama pour lequel vous souhaitez obtenir des informations.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!DNL Search for Boards]**

Ce module de recherche permet d’obtenir des informations sur un panorama indiqué.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query] </td> 
   <td> <p>Saisissez ou mappez le nom (ou une partie du nom) du panorama sur lequel vous souhaitez obtenir des informations.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned boards]</td> 
   <td> <p> Saisissez le nombre maximum de panoramas que [!DNL Workfront Fusion] renverra au cours d’un cycle d’exécution. Cette valeur doit être inférieure ou égale à 1 000.</p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Partial] </p> </td> 
   <td> <p>Par défaut, ce module recherche dans le contenu des personnes membres les correspondances exactes de chaque mot de votre requête. Lorsque [!UICONTROL Partial] est activé, le module recherche le contenu qui commence par n’importe quel mot de votre requête.</p> <p> Par exemple, si vous utilisez le mot « développement » pour rechercher un panorama intitulé « Rapport sur le statut de mon développement », vous devrez, par défaut, rechercher le mot dans son intégralité. Si les [!UICONTROL Partial] sont activées, vous pouvez rechercher « dev » mais pas « development ».</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Boards] </td> 
   <td> <p>Saisissez « À moi » ou mappez une liste d’identifiants de panoramas séparés par des virgules.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Unassign a Member from a Board]**

Ce module d’action permet de supprimer une personne membre d’un panorama.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Saisissez (mappez ou sélectionnez) l’ID du panorama duquel vous voulez supprimer la personne.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Member] </td> 
   <td> <p>Sélectionnez la personne membre que vous souhaitez supprimer du panorama.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Watch Boards]**

Ce module déclencheur lance un scénario lorsqu’un nouveau panorama est ajouté.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Saisissez ou mappez le nombre maximal de panoramas que le module doit renvoyer au cours de chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Listes

+++ **[!UICONTROL Create a List]**

Ce module d’action crée une liste sur un panorama que vous spécifiez.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Saisissez ou mappez l’ID du panorama dans lequel vous souhaitez créer une liste.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Saisissez ou mappez un nom pour la nouvelle liste.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Choisissez si vous souhaitez ajouter la liste en haut ou l’annexer au bas de la carte.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy list]</td> 
   <td> <p> Si vous copiez une liste, sélectionnez le mode de saisie de l’identifiant de la liste à copier.</p> 
    <ul> 
     <li> <p><strong>Saisie manuelle</strong> </p> <p>Dans le champ <strong>[!UICONTROL List ID]</strong> , saisissez ou mappez l’identifiant de la liste à copier.<br></p> </li> 
     <li> <p><strong>Sélectionner</strong> </p> <p>Sélectionnez le panorama qui contient la liste que vous souhaitez copier, puis sélectionnez la liste.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Edit a List]**

Ce module d’action permet de modifier une liste existante.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td> <p> Saisissez ou mappez l’ID de la liste que vous souhaitez mettre à jour.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Saisissez ou mappez un nouveau nom pour la liste.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p> Mappez ou sélectionnez le panorama où vous souhaitez déplacer la liste.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Choisissez si vous souhaitez ajouter la liste en haut ou l’annexer au bas de la carte.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscribed]</td> 
   <td> <p>Activez cette option si vous souhaitez abonner la personne membre active à la liste.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Get a List]**

Ce module d’action permet de récupérer les détails d’une liste spécifique.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL List ID]</p> </td> 
   <td> <p>Saisissez ou mappez l’ID de la liste pour laquelle vous souhaitez récupérer des informations.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Watch cards moved to a list]**

Ce module déclencheur s’active lorsqu’un panorama est déplacé vers une liste spécifique.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board]</td> 
   <td>Sélectionnez le panorama qui contient la liste dont vous souhaitez surveiller les cartes.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List]</td> 
   <td>Sélectionnez la liste dont vous souhaitez surveiller les cartes.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### vignette

+++ **[!UICONTROL Add an Attachment]**

Ce module d’action ajoute une pièce jointe à la carte sélectionnée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter card ID]</td> 
   <td> <p> Sélectionnez le mode de saisie de l’identifiant de la carte à laquelle vous souhaitez ajouter une pièce jointe.</p> 
    <ul> 
     <li> <p><strong>Saisie manuelle</strong> </p> <p>Dans le champ <strong>[!UICONTROL Card ID]</strong> , saisissez ou mappez l’identifiant de la carte à laquelle vous souhaitez ajouter une pièce jointe.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Sélectionnez le panorama contenant la carte à laquelle vous souhaitez ajouter une pièce jointe, puis sélectionnez la liste contenant la carte, puis sélectionnez la carte.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachment type]</p> </td> 
   <td> <p>Indiquez si vous souhaitez charger le fichier directement ou fournir une URL vers le fichier.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File]</strong> </p> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </li> 
     <li> <p><strong>[!UICONTROL URL]</strong> </p> <p>Saisissez l’URL du fichier et donnez un nom à la pièce jointe.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Archive or Unarchive a Card]**

Ce module d’action permet d’archiver ou de renvoyer une carte sur le panorama.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Card ID]</td> 
   <td> <p> Saisissez ou mappez l’ID de la carte que vous souhaitez archiver ou renvoyer sur le panorama.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archive or unarchive]</td> 
   <td> <p> Choisissez de fermer la carte (archiver) ou de la renvoyer sur le panorama (désarcher).</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a card]**

Ce module d’action crée une carte dans une liste sélectionnée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a list ID]</td> 
   <td> <p> Sélectionnez la manière dont vous souhaitez saisir l’ID de la liste dans laquelle vous souhaitez ajouter une carte.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Dans le champ <strong>[!UICONTROL List ID]</strong> , saisissez ou mappez l’identifiant de la liste dans laquelle vous souhaitez ajouter une carte.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Sélectionnez le panorama contenant la liste dans laquelle vous souhaitez ajouter une carte, puis sélectionnez la liste.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels] </td> 
   <td> <p>Pour chaque libellé que vous souhaitez ajouter à la carte, cliquez sur <b>Ajouter un élément</b> et saisissez l’identifiant du libellé.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Members]</td> 
   <td>Pour chaque membre que vous souhaitez ajouter à la carte, cliquez sur <b>Ajouter un élément</b> et saisissez l’ID du membre. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Saisissez un nom pour la nouvelle carte.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Description]</p> </td> 
   <td> <p>Saisissez la description de la carte.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Choisissez d’ajouter la carte en haut ou d’ajouter la carte au bas de la liste.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due date]</td> 
   <td> <p> Saisissez une date d’échéance pour la carte. Pour une liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coercition de type dans [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due complete]</td> 
   <td> <p> Activez cette option pour marquer la carte comme terminée à la date d’échéance.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File URL]</td> 
   <td> <p>Saisissez ou mappez l’URL d’un fichier que vous souhaitez ajouter en tant que pièce jointe à la carte.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Source file]</p> </td> 
   <td> <p>Saisissez ou mappez les informations d’un fichier que vous souhaitez ajouter en tant que pièce jointe à la carte. Sélectionner un fichier à partir d’un module antérieur, ou mapper le nom et les données du fichier</p> 
     <p>Note : le chargement de fichiers est limité à 10 Mo par pièce jointe. Toutefois, les membres [!UICONTROL Business Class] et [!UICONTROL Trello Gold] ont une limite de chargement de fichier de 250 Mo par pièce jointe.</p> 
     </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy card]</td> 
   <td> <p> Si vous créez une carte en tant que copie d’une carte existante, sélectionnez la manière dont vous souhaitez saisir l’identifiant de la carte à copier.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Dans le champ <strong>[!UICONTROL Card ID]</strong> , saisissez ou mappez l’identifiant de la carte à copier.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Sélectionnez le panorama qui contient la carte à copier, puis la liste qui contient la carte, et enfin la carte.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Edit a Card]**

Ce module d’action permet de modifier une carte existante.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Card ID]</td> 
   <td> <p> Sélectionnez le mode de saisie de l’ID de la carte que vous souhaitez modifier.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Dans le champ <strong>[!UICONTROL Card ID]</strong> , saisissez ou mappez l’identifiant de la carte à modifier.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Sélectionnez le panorama qui contient la carte que vous souhaitez modifier, puis sélectionnez la liste qui contient la carte, puis sélectionnez la carte.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New name]</td> 
   <td> <p>Saisissez ou mappez un nouveau nom pour la carte.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL New description]</p> </td> 
   <td> <p>Saisissez ou mappez une nouvelle description pour la carte.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Move a card]</p> </td> 
   <td> <p>Sélectionnez le panorama ou le panorama et la liste où vous souhaitez déplacer la carte.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Labels] </td> 
   <td> <p>Pour chaque libellé que vous souhaitez ajouter à la carte, cliquez sur <b>Ajouter un élément</b> et saisissez l’identifiant du libellé.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Choisissez si vous souhaitez ajouter la carte en haut ou [!UICONTROL append] la carte en bas de la liste.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due date]</td> 
   <td> <p> Saisissez une date d’échéance pour la carte. Pour une liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coercition de type dans [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Due complete]</td> 
   <td> <p> Activez cette option pour marquer la carte comme terminée à la date d’échéance.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Members] </td> 
   <td> <p>Pour chaque membre que vous souhaitez ajouter à la carte, cliquez sur <b>Ajouter un élément</b> et saisissez ou mappez l’ID du membre.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachment cover ID]</p> </td> 
   <td> <p>Saisissez ou mappez l’ID de l’image jointe que vous souhaitez que la carte utilise comme couverture.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscribe] </td> 
   <td> <p>Indiquez si la personne membre doit être abonnée à la carte.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Archive] </td> 
   <td> <p>Sélectionnez une option pour indiquer si vous souhaitez archiver (fermer) la carte. </p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Get a Card]**

Ce module d’action permet de récupérer les détails d’une carte sélectionnée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board ID]</td> 
   <td> <p>Saisissez l’ID du panorama qui contient la carte dont vous souhaitez récupérer les détails. Cela vous permet de voir les noms des champs personnalisés du panorama.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter card ID]</td> 
   <td> <p> Sélectionnez la manière dont vous souhaitez saisir l’ID de la carte dont vous souhaitez récupérer les détails.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Dans le champ <strong>[!UICONTROL Card ID]</strong> , saisissez ou mappez l’identifiant de la carte dont vous souhaitez récupérer les détails.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Sélectionnez le panorama qui contient la carte dont vous voulez récupérer les détails, puis la liste qui contient la carte, et enfin la carte.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Search for Cards]**

Ce module d’action renvoie les cartes qui correspondent à la requête.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Board] </td> 
   <td> <p>Sélectionnez les panoramas dans lesquels vous souhaitez effectuer une recherche. Si vous ne sélectionnez aucun panorama, tous les panoramas seront inclus dans la recherche.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Query]</p> </td> 
   <td> <p>Saisissez la requête. Vous pouvez affiner votre recherche en utilisant les opérateurs de recherche suivants :</p> 
    <ul> 
     <li><code><strong>-operator</strong></code> <p>Vous pouvez ajouter « - » à n’importe quel opérateur pour effectuer une recherche négative, par exemple <code>[!UICONTROL -has:members]</code> pour rechercher les cartes auxquelles aucune personne membre n’a été affectée.</p> </li> 
     <li><code><strong>@name</strong></code> <p>Renvoie les cartes attribuées à une personne membre. Vous pouvez également utiliser <code>member:</code>. Utilisez <code>@me</code> pour inclure uniquement vos cartes.</p> </li> 
     <li><code><strong>#label</strong></code> <p>Renvoie les cartes étiquetées. Vous pouvez également utiliser <code>label:</code>. Par exemple, <code>label:"FIX IT"</code> renverra les cartes avec le libellé « FIX IT ».</p> </li> 
     <li><code><strong>board:id</strong></code> <p>Renvoie les cartes d’un panorama spécifique. Par exemple, <code>board:Trello</code> renverra des cartes sur les panoramas dont le nom contient [!UICONTROL Trello].</p> </li> 
     <li><code><strong>list:name</strong></code> <p>Renvoie les cartes de la liste nommée « nom ».</p> </li> 
     <li><code><strong>has:attachments</strong></code> <p>Renvoie les cartes avec des pièces jointes. L’opérateur <code>has</code>: peut également être utilisé avec d’autres attributs, tels que <code>has:description</code>, <code>has:cover</code>, <code>has:members</code> ou <code>has:stickers</code>.</p> </li> 
     <li><code><strong>due:day</strong></code> <p>Renvoie les cartes dont l’échéance est dans les 24 prochaines heures. L’opérateur <code>due:</code> peut également être utilisé avec d’autres délais, tels que <code>due:week</code>, <code>due:month</code> ou <code>due:overdue</code>. Vous pouvez également rechercher une période spécifique. Par exemple, l’ajout de <code>due:14</code> à la recherche inclut les cartes dont l’échéance est dans les 14 prochains jours.</p> </li> 
     <li><code><strong>created:day</strong></code> <p>Renvoie les cartes créées au cours des dernières 24 heures. L’opérateur <code> created:</code> peut également être utilisé avec d’autres délais, tels que <code>created:week</code> ou <code>created:month</code>. Vous pouvez également rechercher une période spécifique. Par exemple, l’ajout de <code>created:14</code> à la recherche inclut les cartes créées au cours des 14 derniers jours.</p> </li> 
     <li><code><strong>edited:day</strong></code> <p>Renvoie les cartes modifiées au cours des dernières 24 heures. L’opérateur <code>edited:</code> peut également être utilisé avec d’autres délais, tels que <code>edited:week</code> ou <code>edited:month</code>. Vous pouvez également rechercher une période spécifique. Par exemple, l’ajout de <code>edited:21</code> à la recherche inclut les cartes modifiées au cours des 21 derniers jours.</p> </li> 
     <li><code><strong>description:</strong>, <strong>checklist:</strong>, <strong>comment:</strong>, and <strong>name:</strong></code> <p>Renvoie les cartes correspondant au texte des descriptions, des listes de contrôle, des commentaires ou des noms de cartes. Par exemple, <code>comment:"FIX IT"</code> renverra des cartes avec « CORRIGEZ-LE » dans un commentaire.</p> </li> 
     <li><code><strong>is:open</strong> and <strong>is:archived</strong></code> <p>Renvoie les cartes ouvertes ou archivées. Si aucun n’est spécifié, [!UICONTROL Trello] renvoie les deux types.</p> </li> 
     <li><code><strong>is:starred</strong> </code> <p>N’inclut que les cartes sur les panoramas marqués d’une étoile.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned cards]</td> 
   <td> <p> Saisissez ou mappez le nombre maximal de cartes que vous [!DNL Workfront Fusion] renvoyer au cours d’un cycle d’exécution. Cette valeur doit être inférieure ou égale à 1 000.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Partial] </td> 
   <td> <p>Par défaut, ce module recherche dans le contenu des personnes membres les correspondances exactes de chaque mot de votre requête. Lorsque [!UICONTROL Partial] est activé, le module recherche le contenu qui commence par n’importe quel mot de votre requête.</p> <p> Par exemple, si vous utilisez le mot « développement » pour rechercher un panorama intitulé « Rapport sur le statut de mon développement », vous devrez, par défaut, rechercher le mot dans son intégralité. Si les [!UICONTROL Partial] sont activées, vous pouvez rechercher « dev » mais pas « development ».</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cards] </td> 
   <td> <p>Pour rechercher des cartes spécifiques, cliquez sur <b>Ajouter un élément</b> et ajoutez l’identifiant de la carte.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Watch cards]**

Ce module de déclenchement lance un scénario lorsqu’une nouvelle carte est ajoutée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watched object]</td> 
   <td> <p>Sélectionnez l’emplacement où vous souhaitez surveiller les cartes.</p> 
    <ul> 
     <li><strong>[!UICONTROL All cards]</strong> </li> 
     <li> <p><strong>Cartes sur un panorama spécifique</strong> </p> <p>Sélectionner le panorama dont vous souhaitez surveiller les cartes.</p> </li> 
     <li> <p><strong>[!UICONTROL Cards on specific list]</strong> </p> <p>Sélectionnez le panorama qui contient la liste dont vous souhaitez surveiller les cartes, puis la liste.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Membres

+++ **[!UICONTROL Add a Member to a Card]**

Ce module d’action ajoute la personne membre spécifiée à la carte spécifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter card ID and member ID]</p> </td> 
   <td> <p>Choisissez la manière dont vous souhaitez saisir l’ID de la carte et l’ID de la personne membre.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Saisissez ou mappez le <strong>[!UICONTROL Card ID]</strong> et le <strong>[!UICONTROL Member ID]</strong>.</p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Sélectionnez le panorama qui contient la carte à laquelle vous souhaitez ajouter une personne membre, puis la liste qui contient la carte, la carte elle-même et enfin, la personne membre que vous souhaitez ajouter à la carte.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Assign a Member to a Board]**

Voir « [!UICONTROL Assign a Member to a Board] » sous [Tableaux](#boards).

+++

+++ **[!UICONTROL Search for Members]**

Ce module d’action récupère des informations sur les membres du [!UICONTROL Trello].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query] </td> 
   <td> <p>Saisissez le nom ou le nom d’utilisateur de l’utilisateur que vous souhaitez rechercher.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Partial] </td> 
   <td> <p>Par défaut, ce module recherche dans le contenu des personnes membres les correspondances exactes de chaque mot de votre requête. Lorsque [!UICONTROL Partial] est activé, le module recherche le contenu qui commence par n’importe quel mot de votre requête.</p> <p> Par exemple, si vous utilisez le mot « développement » pour rechercher un panorama intitulé « Rapport sur le statut de mon développement », vous devrez, par défaut, rechercher le mot dans son intégralité. Si les [!UICONTROL Partial] sont activées, vous pouvez rechercher « dev » mais pas « development ».</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned members]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Unassign a Member from a Board]**

Voir « [!UICONTROL Unassign a Member from a Board] » sous [Tableaux](#boards).

+++

### Listes de contrôle

+++ **[!UICONTROL Create a Checklist]**

Ce module d’action crée une liste de contrôle sur la carte sélectionnée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a card ID]</td> 
   <td> <p> Sélectionnez la manière dont vous souhaitez saisir l’ID de la carte sur laquelle vous souhaitez ajouter une liste de contrôle.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Dans le champ <strong>[!UICONTROL Card ID]</strong> , saisissez ou mappez l’identifiant de la carte à laquelle vous souhaitez ajouter une liste de contrôle.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Sélectionnez le panorama qui contient la carte à laquelle vous voulez ajouter une liste de contrôle, puis la liste qui contient la carte, et enfin la carte.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name] </td> 
   <td> <p>Saisissez ou mappez un nom pour la liste de contrôle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Position] </td> 
   <td> <p>Choisissez d’ajouter la liste de contrôle en haut ou d’ajouter la liste de contrôle en bas de la carte.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter checklist ID]</p> </td> 
   <td> <p>Si vous créez la liste de contrôle en copiant une liste existante, saisissez ou mappez l’identifiant d’une liste de contrôle source que vous souhaitez copier dans la nouvelle.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create a Checklist Item]**

Ce module d’action ajoute un élément à une liste de contrôle spécifique.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter checklist ID]</td> 
   <td> <p> Si vous créez une liste de contrôle en copiant une liste existante, sélectionnez la manière dont vous souhaitez saisir l’identifiant de la liste de contrôle dans laquelle vous souhaitez ajouter un élément.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Dans le champ <strong>[!UICONTROL Checklist ID]</strong> , saisissez ou mappez l’identifiant de la carte à laquelle vous souhaitez ajouter une liste de contrôle.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Sélectionnez le panorama qui contient la carte à laquelle vous souhaitez ajouter une liste de contrôle, puis la liste qui contient la carte, puis la carte elle-même, et enfin la liste de contrôle.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Item name]</p> </td> 
   <td> <p>Saisissez ou mappez un nom pour le nouvel élément.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Position]</p> </td> 
   <td> <p>Choisissez si vous souhaitez ajouter l’élément en haut ou [!UICONTROL append] en bas de la liste de contrôle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Checked]</p> </td> 
   <td> <p>Activez cette option si vous souhaitez ajouter l’élément comme étant déjà contrôlé.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Edit a Checklist Item]**

Ce module d’action modifie une liste de contrôle existante.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a Card ID and Checklist Item ID]</td> 
   <td> <p> Sélectionnez la manière dont vous souhaitez saisir l’ID de la carte et la liste de contrôle où vous souhaitez modifier un élément.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Dans le champ <strong>[!UICONTROL Checklist ID]</strong> , saisissez ou mappez l’identifiant de la carte à laquelle vous souhaitez ajouter une liste de contrôle.</p> <p>Dans le champ <strong>[!UICONTROL Checklist Item ID]</strong> , saisissez ou mappez l’identifiant de la liste de contrôle.</p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Sélectionnez le panorama qui contient la carte à laquelle vous souhaitez ajouter une liste de contrôle, puis la liste qui contient la carte, puis la carte elle-même, et enfin la liste de contrôle.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Checklist ID]</td> 
   <td>Sélectionnez ou mappez la liste de contrôle vers laquelle vous souhaitez déplacer l’élément de liste de contrôle.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Item name]</p> </td> 
   <td> <p>Saisissez ou mappez un nom pour le nouvel élément.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Position]</p> </td> 
   <td> <p>Indiquez si vous souhaitez ajouter l’élément en haut ou l’ajouter en bas de la liste de contrôle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL State]</p> </td> 
   <td> <p>Indiquez si l’élément de la liste de contrôle est terminé ou non terminé.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Libellés

+++ **[!UICONTROL Add a Label to a Card]**

Ce module d’action ajoute un libellé à la carte sélectionnée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter card ID]</td> 
   <td> <p> Sélectionnez la manière dont vous souhaitez saisir l’ID de la carte sur laquelle vous souhaitez ajouter une liste de contrôle.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Dans le champ <strong>[!UICONTROL Card ID]</strong> , saisissez ou mappez l’identifiant de la carte à laquelle vous souhaitez ajouter une liste de contrôle. Dans le champ <strong>[!UICONTROL Label ID]</strong>, saisissez ou mappez l’identifiant du libellé que vous souhaitez ajouter.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Sélectionnez le panorama qui contient la carte à laquelle vous voulez ajouter une liste de contrôle, puis la liste qui contient la carte, et enfin la carte. </p> <p>Sélectionnez le libellé que vous souhaitez ajouter à la carte.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

### Commentaires

+++ **[!UICONTROL Create a Comment in a Card]**

Ce module d’action ajoute un commentaire à une carte sélectionnée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a card ID]</td> 
   <td> <p> Sélectionnez la manière dont vous souhaitez saisir l’identifiant de la carte sur laquelle vous souhaitez ajouter un commentaire.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Dans le champ <strong>[!UICONTROL Card ID]</strong> , saisissez ou mappez l’identifiant de la carte sur laquelle vous souhaitez ajouter un commentaire.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Sélectionnez le panorama qui contient la carte sur laquelle vous souhaitez ajouter un commentaire, puis sélectionnez la liste qui contient la carte, puis sélectionnez la carte.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment] </td> 
   <td> <p>Saisissez ou mappez le commentaire que vous souhaitez ajouter à la carte sélectionnée.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL List Comments in a Card]**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a card ID]</td> 
   <td> <p> Sélectionnez la manière dont vous souhaitez saisir l’identifiant de la carte sur laquelle vous souhaitez ajouter un commentaire.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>Dans le champ <strong>[!UICONTROL Card ID]</strong> , saisissez ou mappez l’identifiant de la carte sur laquelle vous souhaitez ajouter un commentaire.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Select]</strong> </p> <p>Sélectionnez le panorama qui contient la carte sur laquelle vous souhaitez ajouter un commentaire, puis sélectionnez la liste qui contient la carte, puis sélectionnez la carte.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned comments]</td> 
   <td> <p> Saisissez le nombre maximal de commentaires que [!DNL Workfront Fusion] renverra au cours d’un cycle d’exécution.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Since] </td> 
   <td> <p>Définissez la date de début de la période au cours de laquelle le commentaire a été créé. Pour une liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coercition de type dans [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Before] </td> 
   <td> <p>Définissez la date de fin de la période au cours de laquelle le commentaire a été créé. Pour une liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coercition de type dans [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Watch Comments]**

Ce module de déclenchement lance un scénario lorsqu’un commentaire est ajouté.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!UICONTROL Trello] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watched object]</td> 
   <td> <p>Sélectionnez l’emplacement où vous souhaitez surveiller les commentaires.</p> 
    <ul> 
     <li><strong>[!UICONTROL All cards] partout</strong> </li> 
     <li> <p><strong>[!UICONTROL Board]</strong> </p> <p>Sélectionnez le panorama dont vous souhaitez surveiller les commentaires.</p> </li> 
     <li> <p><strong>[!UICONTROL List]</strong> </p> <p>Sélectionnez le panorama qui contient la liste dont vous voulez surveiller les commentaires, puis sélectionnez la liste.</p> </li> 
     <li><strong>[!UICONTROL Card]</strong> </li> 
     <li>Sélectionnez le panorama qui contient la carte dont vous voulez surveiller les commentaires, puis sélectionnez la liste qui contient la carte, puis sélectionnez la carte.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>Saisissez ou mappez le nombre maximum de commentaires que vous souhaitez que le module renvoie lors de chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

## ID d’objet [!UICONTROL Trello]

* [Comment trouver l’ID ou le lien court d’une carte dans  [!DNL Trello]](#how-to-find-the-id-or-the-shortlink-of-a-card-in-trello)
* [Comment trouver les ID d’autres objets dans  [!DNL Trello]](#how-to-find-ids-of-other-objects-in-trello)

### Comment trouver l’ID ou le lien court d’une carte dans [!DNL Trello]

Si vous souhaitez modifier une carte ou créer un commentaire, vous devez connaître l’ID de la carte ou son lien court. Vous pouvez obtenir ces informations à partir de la sortie du déclencheur [!UICONTROL New Card]. Le lien court d’une carte peut également être obtenu en ouvrant la carte et en cliquant sur le bouton [!UICONTROL Share] . Le lien court se trouve dans la zone de [!UICONTROL Link to this card], à la fin de l’URL après `https://trello.com/c/`.

![Partager et plus](/help/workfront-fusion/references/apps-and-modules/assets/share-and-more-350x575.png)

### Comment trouver les ID d’autres objets dans [!DNL Trello]

Les ID du panorama, de la liste et des commentaires ne peuvent être obtenus qu’à l’aide de déclencheurs. Le site web [!DNL `trello.com`] n’affiche pas ces ID.
