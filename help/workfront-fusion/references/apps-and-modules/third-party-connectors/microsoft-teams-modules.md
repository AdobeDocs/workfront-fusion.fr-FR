---
title: Modules Microsoft Teams
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent des équipes et les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
source-git-commit: f5b49cca308fad01167aed27e4716a3d630cb026
workflow-type: tm+mt
source-wordcount: '3642'
ht-degree: 13%

---

# Modules Microsoft Teams

<!-- ADD REDIRECTS -->

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent Microsoft Teams et les connecter à plusieurs applications et services tiers.

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
   <p>Actuel : aucune exigence de licence Workfront Fusion</p>
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

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Conditions préalables

Pour utiliser les modules Microsoft Teams, vous devez disposer d’un compte Microsoft Teams capable d’effectuer l’action dans le module.

## Connexion du service Microsoft Teams à Workfront Fusion

Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir [Création d’une connexion à Adobe Workfront Fusion - Instructions de base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Certaines applications Microsoft utilisent la même connexion, qui est liée à des autorisations d’utilisateur ou d’utilisatrice. Ainsi, lors de la création d’une connexion, l’écran de consentement aux autorisations affiche les autorisations précédemment accordées à la connexion de cet utilisateur ou de cette utilisatrice, en plus des nouvelles autorisations nécessaires à l’application actuelle.
>
>Par exemple, si un utilisateur ou une utilisatrice dispose d’autorisations « Lire le tableau » accordées via le connecteur Excel, puis crée une connexion dans le connecteur Outlook pour lire les e-mails, l’écran de consentement aux autorisations affiche à la fois l’autorisation « Lire le tableau » déjà accordée et l’autorisation « Écrire des e-mails » nouvellement requise.

## Modules Microsoft Teams et leurs champs

Lorsque vous configurez des modules Microsoft Teams, Workfront Fusion affiche les champs répertoriés ci-dessous. D’autres champs Microsoft Teams peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Equipe](#team)
* [Canal](#channel)
* [Message](#message)
* [Membre](#member)
* [Réunion en ligne](#online-meeting)
* [Autre](#other)

### Equipe

* [Créer une équipe à partir d’un groupe](#create-a-team-from-a-group)
* [Créer un groupe Office 365](#create-an-office-365-group)
* [Supprimer une équipe ou un groupe](#delete-a-team-or-group)
* [Obtenir une équipe](#get-a-team)
* [Liste de toutes les équipes et de tous les groupes](#list-all-teams-and-groups)
* [Liste des équipes jointes](#list-joined-teams)
* [Mettre à jour une équipe](#update-a-team)
* [Surveiller les équipes](#watch-teams)

#### Créer une équipe à partir d’un groupe

Ce module d&#39;action crée une équipe à partir d&#39;un groupe Microsoft Office 365 existant et configure les paramètres de la nouvelle équipe.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de groupe</td> 
   <td> <p>Sélectionnez le groupe à partir duquel créer une équipe.</p> 
   </tr> 
  <tr> 
   <td role="rowheader">Autoriser les membres à créer et mettre à jour des canaux</td> 
   <td>Choisissez si vous souhaitez autoriser les membres à créer et mettre à jour des canaux.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Autoriser les membres à supprimer des canaux</td> 
   <td>Choisissez si vous souhaitez autoriser les membres à supprimer des canaux.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Autoriser les membres à ajouter et supprimer des applications</td> 
   <td>Choisissez si vous souhaitez autoriser les membres à ajouter et supprimer des applications.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Autoriser les membres à créer, mettre à jour et supprimer des onglets</td> 
   <td>Choisissez si vous souhaitez autoriser les membres à créer, mettre à jour et supprimer des onglets.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Autoriser les membres à créer et supprimer des connecteurs</td> 
   <td>Choisissez si vous souhaitez autoriser les membres à créer et supprimer des connecteurs.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Autoriser les utilisateurs à modifier leurs messages</td> 
   <td>Choisissez si vous souhaitez autoriser les utilisateurs à modifier leurs messages.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Autoriser les utilisateurs à supprimer leurs messages</td> 
   <td>Choisissez si vous souhaitez autoriser les utilisateurs à supprimer leurs messages.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Autoriser les propriétaires à supprimer des messages</td> 
   <td>Indiquez si vous souhaitez autoriser les propriétaires à supprimer des messages.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Autoriser les mentions @team</td> 
   <td>Choisissez si vous souhaitez autoriser les mentions @team.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Autoriser les mentions @channel</td> 
   <td>Choisissez si vous souhaitez autoriser les mentions @channel.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Autoriser Giphy</td> 
   <td>Choisissez si vous souhaitez autoriser l'utilisation de Giphy pour cette équipe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Autoriser les autocollants et les mèmes</td> 
   <td>Choisissez si vous souhaitez autoriser les utilisateurs à inclure des autocollants et des mèmes.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Autoriser les mèmes personnalisés</td> 
   <td>Choisissez si vous souhaitez autoriser les utilisateurs à inclure des mèmes personnalisés.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Autoriser les invités à créer et mettre à jour des canaux</td> 
   <td>Choisissez si vous souhaitez autoriser les invités à créer et mettre à jour des canaux.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Autoriser les invités à supprimer des chaînes</td> 
   <td>Choisissez si vous souhaitez autoriser les invités à supprimer des canaux.</td> 
  </tr> 
 </tbody> 
</table>

#### Créer un groupe Office 365

Ce module d&#39;action crée un groupe dans Microsoft Office 365.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom d’affichage</td> 
   <td> <p>Saisissez ou mappez le nom que ce groupe affiche dans son carnet d’adresses.</p> 
   </tr> 
  <tr> 
   <td role="rowheader">Alias du groupe</td> 
   <td>Saisissez ou mappez l’alias de messagerie de ce groupe. Vous pouvez inclure des lettres minuscules, des chiffres et des traits de soulignement. Pour le type de groupe Office 365, il s'agit de l'alias de messagerie du groupe ([Alias]@[Votre domaine].onmicrosoft.com). Pour le type Groupe de sécurité , l’alias fonctionne comme un surnom.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type de groupe</td> 
   <td>Choisissez si vous créez un groupe Office 365 ou un groupe de sécurité.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Description</td> 
   <td>Saisissez ou mappez une description pour ce groupe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sécurité activée</td> 
   <td>Activez cette option si vous souhaitez que la sécurité du groupe soit activée.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Propriétaires</td> 
   <td>Sélectionnez les propriétaires de ce groupe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Membres</td> 
   <td>Sélectionnez les membres de ce groupe.</td> 
  </tr> 
 </tbody> 
</table>

#### Supprimer une équipe ou un groupe

Ce module d&#39;action supprime l&#39;équipe ou le groupe spécifié.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de groupe</td> 
   <td> <p>Saisissez ou mappez l’identifiant du groupe que vous souhaitez supprimer.</p> 
   </tr> 
 </tbody> 
</table>

#### Obtenir une équipe

Ce module récupère les propriétés et les relations de l&#39;équipe Microsoft ou du groupe Office 365 spécifié.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID de groupe</td> 
   <td> <p>Saisissez ou mappez l’identifiant du groupe pour lequel vous souhaitez récupérer des détails.</p> 
   </tr> 
 </tbody> 
</table>

#### Liste de toutes les équipes et de tous les groupes

Ce module répertorie toutes les équipes des groupes Microsoft Teams et Office 365 associés à l&#39;organisation. Vous pouvez filtrer pour renvoyer uniquement les résultats qui répondent aux critères que vous spécifiez.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filtre</td> 
   <td> <p>Vous pouvez définir un filtre pour renvoyer uniquement les équipes et les groupes qui répondent aux critères que vous sélectionnez.</p> <p>Pour chaque filtre, saisissez le champ que le filtre doit évaluer, l’opérateur et la valeur que le filtre doit autoriser. Vous pouvez utiliser plusieurs filtres en ajoutant des règles ET ou OU.</p> </td> 
   </tr> 
  <tr> 
   <td>Nombre maximal de résultats renvoyés</td> 
   <td>Définissez le nombre maximal d’équipes ou de groupes que Workfront Fusion renverra au cours d’un cycle d’exécution.</td> 
  </tr> 
 </tbody> 
</table>


#### Liste des équipes jointes

Ce module d&#39;action répertorie les équipes qui ont été rejointes par l&#39;utilisateur associé à la connexion utilisée dans ce module.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>Nombre maximal de résultats renvoyés</td> 
   <td>Définissez le nombre maximal d’équipes ou de groupes que Workfront Fusion renverra au cours d’un cycle d’exécution.</td> 
  </tr> 
 </tbody> 
</table>

#### Mettre à jour une équipe

Ce module d&#39;action met à jour les propriétés des équipes spécifiées dans le groupe Microsoft Teams ou Office 365.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Nom d’affichage</td> 
   <td> <p>Saisissez ou mappez le nom que ce groupe affiche dans son carnet d’adresses.</p> 
   </tr> 
  <tr> 
   <td role="rowheader">Alias du groupe</td> 
   <td>Saisissez ou mappez l’alias de messagerie de ce groupe. Vous pouvez inclure des lettres minuscules, des chiffres et des traits de soulignement. Pour le type de groupe Office 365, il s'agit de l'alias de messagerie du groupe ([Alias]@[Votre domaine].onmicrosoft.com). Pour le type de groupe de sécurité , l’alias fonctionne comme un surnom.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Description</td> 
   <td>Saisissez ou mappez une description pour ce groupe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Sécurité activée</td> 
   <td>Activez cette option si vous souhaitez que la sécurité du groupe soit activée.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Visibilité</td> 
   <td>Spécifiez la visibilité du groupe Office 365.</td> 
  </tr> 
 </tbody> 
</table>

#### Surveiller les équipes

Ce module de déclenchement démarre un scénario lors de la création d’une équipe.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filtre</td> 
   <td> <p>Vous pouvez définir un filtre afin de surveiller uniquement les équipes et les groupes qui répondent aux critères de votre sélection.</p> <p>Pour chaque filtre, saisissez le champ que le filtre doit évaluer, l’opérateur et la valeur que le filtre doit autoriser. Vous pouvez utiliser plusieurs filtres en ajoutant des règles ET ou OU.</p> </td> 
   </tr> 
  <tr> 
   <td>Nombre maximal de résultats renvoyés</td> 
   <td>Définissez le nombre maximal d’équipes ou de groupes que Workfront Fusion renverra au cours d’un cycle d’exécution.</td> 
  </tr> 
 </tbody> 
</table>

### Canal

* [Création d’un canal](#create-a-channel)
* [Suppression d’un canal](#delete-a-channel)
* [Obtenir un canal](#get-a-channel)
* [Liste des canaux](#list-channels)
* [Mise à jour d’un canal](#update-a-channel)

#### Création d’un canal

Ce module d&#39;action crée un canal pour l&#39;équipe spécifiée.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID d’équipe</td> 
   <td> <p>Dans Microsoft Teams, sélectionnez l’équipe pour laquelle vous souhaitez créer un canal.</p> </td> 
   </tr> 
  <tr> 
   <td>Nom du canal</td> 
   <td>Saisissez ou mappez un nom pour le nouveau canal.</td> 
  </tr> 
  <tr> 
   <td>Descriptions</td> 
   <td>Saisissez ou mappez une description pour le nouveau canal.</td> 
  </tr> 
 </tbody> 
</table>

#### Suppression d’un canal

Ce module d’action supprime le canal spécifié d’une équipe Microsoft.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID d’équipe</td> 
   <td> <p>Saisissez ou mappez l’identifiant de l’équipe dans Microsoft Teams à partir de laquelle vous souhaitez supprimer un canal.</p> </td> 
   </tr> 
  <tr> 
   <td>Identifiant du canal</td> 
   <td>Saisissez ou mappez l’identifiant du canal que vous souhaitez supprimer.</td> 
  </tr> 
  </tbody> 
</table>

#### Obtenir un canal

Ce module récupère les propriétés et les relations d’un canal.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID d’équipe</td> 
   <td> <p>Saisissez ou mappez l’identifiant de l’équipe dans Microsoft Teams propriétaire du canal pour lequel vous souhaitez récupérer des détails.</p> </td> 
   </tr> 
  <tr> 
   <td>Identifiant du canal</td> 
   <td>Saisissez ou mappez l’identifiant du canal pour lequel vous souhaitez récupérer des détails.</td> 
  </tr> 
  </tbody> 
</table>

#### Liste des canaux

Ce module répertorie les canaux détenus par l’équipe spécifiée dans Microsoft Teams.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID d’équipe</td> 
   <td> <p>Dans Microsoft Teams, sélectionnez l’équipe pour laquelle vous souhaitez répertorier les canaux.</p> </td> 
   </tr> 
  <tr> 
   <td>Nombre maximal de résultats renvoyés</td> 
   <td>Définissez le nombre maximal de canaux que Workfront Fusion renverra au cours d’un cycle d’exécution.</td> 
  </tr> 
  </tbody> 
</table>

#### Mise à jour d’un canal

Ce module d’action met à jour la description du canal spécifié.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID d’équipe</td> 
   <td> <p>Dans Microsoft Teams, sélectionnez l’équipe propriétaire du canal à mettre à jour.</p> </td> 
   </tr> 
  <tr> 
   <td>Nom du canal</td> 
   <td>Saisissez ou mappez le nom du canal que vous souhaitez mettre à jour.</td> 
  </tr> 
  <tr> 
   <td>Description</td> 
   <td>Saisissez ou mappez la nouvelle description du canal.</td> 
  </tr> 
 </tbody> 
</table>

### Message

* [Répondre à un message de canal](#reply-to-a-channel-message)
* [Envoyer un message](#send-a-message)
* [Messages Watch](#watch-messages)
* [Regarder les nouvelles réponses](#watch-new-replies)

#### Répondre à un message de canal

Ce module d’action crée une réponse à un message dans le canal spécifié.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID d’équipe</td> 
   <td> <p>Dans Microsoft Teams, sélectionnez l’équipe propriétaire du canal contenant le message auquel vous souhaitez répondre.</p> </td> 
   </tr> 
  <tr> 
   <td>Identifiant du canal</td> 
   <td>Sélectionnez le canal contenant le message auquel vous souhaitez répondre.</td> 
  </tr> 
  <tr> 
   <td>Identifiant du message</td> 
   <td>Saisissez ou mappez l’identifiant du message auquel vous souhaitez répondre.</td> 
  </tr> 
  <tr> 
   <td>Type de contenu</td> 
   <td>Choisissez si vous souhaitez envoyer le message au format texte brut ou au format HTML.</td> 
  </tr> 
  <tr> 
   <td>Message de réponse</td> 
   <td>Saisissez ou mappez le corps du message de réponse que vous souhaitez envoyer.</td> 
  </tr> 
 </tbody> 
</table>

#### Envoyer un message

Ce module d&#39;action envoie un message au canal d&#39;une équipe ou à une conversation.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type de message/td&gt; 
   <td> <p>Choisissez si vous envoyez un message de canal ou un message de conversation.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">ID d’équipe</td> 
   <td> <p>Si vous envoyez un message à un canal, saisissez ou mappez l’identifiant de l’équipe dans Microsoft Teams propriétaire du canal auquel vous souhaitez envoyer un message.</p> </td> 
   </tr> 
  <tr> 
   <td>Identifiant du canal</td> 
   <td>Si vous envoyez un message à un canal, saisissez ou mappez l’identifiant du canal auquel vous souhaitez envoyer un message.</td> 
  </tr> 
  <tr> 
   <td>Créer une conversation</td> 
   <td>Si vous envoyez un message de conversation, choisissez si vous souhaitez créer une conversation.
   <ul><li><b>Oui</b><p>Choisissez si vous souhaitez une discussion en tête-à-tête ou en groupe, puis sélectionnez le membre que vous souhaitez inclure dans la discussion. Vous devez sélectionner l’utilisateur associé à la connexion que ce module utilise, et une conversation en tête-à-tête ne doit contenir que cet utilisateur et un autre utilisateur.</p><p>Si vous créez une conversation de groupe, vous pouvez définir une rubrique dans le champ Rubrique .</p>
   <li><b>Non</b><p>Saisissez ou mappez l’identifiant de l’équipe propriétaire du canal auquel vous souhaitez envoyer un message, puis saisissez ou mappez l’identifiant du canal.</td> 
  </tr> 
  <tr> 
   <td>Message</td> 
   <td>Saisissez ou mappez le corps du message que vous souhaitez envoyer.</td> 
  </tr> 
  <tr> 
   <td>Type de contenu</td> 
   <td>Choisissez si vous souhaitez envoyer le message au format texte brut ou au format HTML.</td> 
  </tr> 
 </tbody> 
</table>

#### Messages Watch

Ce module de déclenchement démarre un scénario lorsqu’un message est envoyé au canal d’une équipe ou à une conversation.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type des messages à regarder</td> 
   <td> <p>Choisissez si vous souhaitez regarder des messages de canal ou des messages de conversation.</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">ID d’équipe</td> 
   <td> <p>Si vous regardez des messages de canal, sélectionnez l’équipe dans Microsoft Teams qui détient le canal que vous regardez pour les messages.</p> </td> 
   </tr> 
  <tr> 
   <td>Identifiant du canal</td> 
   <td>Si vous regardez des messages de canal, sélectionnez le canal que vous souhaitez regarder pour les messages.</td> 
  </tr> 
  <tr> 
   <td>ID de conversation</td> 
   <td>Si vous regardez des messages de chat, sélectionnez le chat que vous souhaitez regarder pour les messages.</td> 
  </tr> 
  <tr> 
   <td>Nombre maximum de messages retournés</td> 
   <td>Définissez le nombre maximal de messages que Workfront Fusion renverra au cours d’un cycle d’exécution.</td> 
  </tr> 
 </tbody> 
</table>

#### Regarder les nouvelles réponses

Ce module de déclenchement lance un scénario lorsqu’une nouvelle réponse est reçue par le message spécifié.

Ce module n&#39;est pas disponible pour les comptes personnels.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID d’équipe</td> 
   <td> <p>Dans Microsoft Teams, sélectionnez l’équipe propriétaire du canal que vous observez pour les réponses.</p> </td> 
   </tr> 
  <tr> 
   <td>Identifiant du canal</td> 
   <td>Sélectionnez le canal que vous souhaitez observer pour les réponses.</td> 
  </tr> 
  <tr> 
   <td>Identifiant du message</td> 
   <td>Sélectionnez le chat que vous souhaitez observer pour les réponses.</td> 
  </tr> 
  <tr> 
   <td>Nombre maximum de réponses renvoyées</td> 
   <td>Définissez le nombre maximal de réponses que Workfront Fusion renverra au cours d’un cycle d’exécution.</td> 
  </tr> 
 </tbody> 
</table>

### Membre

* [Ajouter une personne membre](#add-a-member)
* [Ajouter un membre à un groupe](#add-a-member-to-a-group)

#### Ajouter une personne membre

Ce module d’action ajoute un membre à Microsoft Teams.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Nom du membre</td> 
   <td> <p>Saisissez ou mappez le nom du membre que vous souhaitez ajouter à Microsoft Teams.</p> </td> 
   </tr> 
  <tr> 
   <td>Mot de passe</td> 
   <td>Saisissez ou mappez le mot de passe du membre.</td> 
  </tr> 
 </tbody> 
</table>

#### Ajouter un membre à un groupe

Ce module d&#39;action ajoute un membre à un groupe Office 365.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID de groupe</td> 
   <td> <p>Sélectionnez le groupe auquel vous souhaitez ajouter un membre.</p> </td> 
   </tr> 
  <tr> 
   <td>ID de membre</td> 
   <td>Sélectionnez le membre que vous souhaitez ajouter au groupe.</td> 
  </tr> 
 </tbody> 
</table>

### Réunion en ligne

* [Créer une réunion en ligne](#create-an-online-meeting)
* [Supprimer une réunion en ligne](#delete-an-online-meeting)
* [Obtenir une réunion en ligne](#get-an-online-meeting)
* [Mettre à jour une réunion en ligne](#update-an-online-meeting)

#### Créer une réunion en ligne

Ce module d&#39;action crée une réunion autonome qui n&#39;est pas associée à un événement sur le calendrier de l&#39;utilisateur. Cette réunion n&#39;apparaîtra pas sur le calendrier de l&#39;utilisateur.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">Objet</td> 
   <td>Saisissez ou mappez un objet pour cette réunion.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Date et heure de début</td> 
   <td>Saisissez ou mappez la date et l'heure auxquelles vous souhaitez que la réunion commence. Pour obtenir la liste des formats de date pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercition</a>.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Date et heure de fin</td> 
   <td>Saisissez ou mappez la date et l'heure de fin de la réunion. Pour obtenir la liste des formats de date pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercition</a>.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Présentateurs et présentatrices autorisés</td> 
   <td>Sélectionnez le groupe qui est autorisé à faire une présentation lors de cette réunion.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Attendus</td> 
   <td>Pour chaque participant que vous souhaitez ajouter à la réunion, cliquez sur <b>Ajouter un élément</b> et sélectionnez le nom et le rôle du participant.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Autoriser les participants à activer leurs caméras</td> 
   <td>Choisissez si vous souhaitez autoriser les participants à activer leurs propres caméras.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Autoriser les participants à activer leur microphone</td> 
   <td>Choisissez si vous souhaitez autoriser les participants à activer leurs propres microphones.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Autoriser la conversation de réunion</td> 
   <td>Choisissez si vous souhaitez activer, désactiver ou limiter la conversation de la réunion à la durée de l'appel de la réunion</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Autoriser les réactions des équipes</td> 
   <td>Choisissez si vous souhaitez activer les réactions des équipes pour cette réunion.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">ID de thread</td> 
   <td>Saisissez ou mappez l'ID d'un thread associé à cette réunion.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Identifiant du message</td> 
   <td>Saisissez ou mappez l'ID d'un message associé à cette réunion.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Identifiant du message de la chaîne de réponse</td> 
   <td>Saisissez ou mappez l'ID de la chaîne de réponse associée à cette réunion.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Annoncer l’entrée et la sortie</td> 
   <td>Choisissez si vous souhaitez que la réunion annonce le moment où les participants rejoignent ou quittent l'événement.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Étendue</td> 
   <td>Sélectionnez le groupe de participants qui peuvent contourner l'attente dans la salle d'attente. Ces participants rejoindront directement la réunion.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Permettre aux utilisateurs d'accès à distance de contourner la salle d'attente</td> 
   <td>Choisissez si vous souhaitez permettre aux utilisateurs d'accès à distance de contourner la salle d'attente.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Enregistrement automatique</td> 
   <td>Choisissez si vous souhaitez enregistrer la réunion automatiquement.</td> 
   </tr> 
   </tbody> 
</table>

#### Supprimer une réunion en ligne

Ce module d&#39;action supprime la réunion en ligne avec l&#39;ID spécifié.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID de réunion</td> 
   <td> <p>Saisissez ou mappez l'ID de la réunion à supprimer.</p> </td> 
   </tr> 
 </tbody> 
</table>

#### Obtenir une réunion en ligne

Ce module d&#39;action récupère les détails de la réunion en ligne avec l&#39;ID spécifié.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID de réunion</td> 
   <td> <p>Saisissez ou mappez l'ID de la réunion dont vous souhaitez récupérer les détails.</p> </td> 
   </tr> 
 </tbody> 
</table>

#### Mettre à jour une réunion en ligne

Ce module d&#39;action met à jour la réunion en ligne avec l&#39;ID spécifié.



<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID de réunion</td> 
   <td>Saisissez ou mappez l'ID de la réunion à mettre à jour.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Objet</td> 
   <td>Saisissez ou mappez un objet pour cette réunion.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Date et heure de début</td> 
   <td>Saisissez ou mappez la date et l'heure auxquelles vous souhaitez que la réunion commence. Pour obtenir la liste des formats de date pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercition</a>.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Date et heure de fin</td> 
   <td>Saisissez ou mappez la date et l'heure de fin de la réunion. Pour obtenir la liste des formats de date pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercition</a>.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Présentateurs et présentatrices autorisés</td> 
   <td>Sélectionnez le groupe qui est autorisé à faire une présentation lors de cette réunion.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Attendus</td> 
   <td>Pour chaque participant que vous souhaitez ajouter à la réunion, cliquez sur <b>Ajouter un élément</b> et sélectionnez le nom et le rôle du participant.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Autoriser les participants à activer leurs caméras</td> 
   <td>Choisissez si vous souhaitez autoriser les participants à activer leurs propres caméras.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Autoriser les participants à activer leur microphone</td> 
   <td>Choisissez si vous souhaitez autoriser les participants à activer leurs propres microphones.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Autoriser la conversation de réunion</td> 
   <td>Choisissez si vous souhaitez activer, désactiver ou limiter la conversation de la réunion à la durée de l'appel de la réunion</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Autoriser les réactions des équipes</td> 
   <td>Choisissez si vous souhaitez activer les réactions des équipes pour cette réunion.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">ID de thread</td> 
   <td>Saisissez ou mappez l'ID d'un thread associé à cette réunion.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Identifiant du message</td> 
   <td>Saisissez ou mappez l'ID d'un message associé à cette réunion.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Identifiant du message de la chaîne de réponse</td> 
   <td>Saisissez ou mappez l'ID de la chaîne de réponse associée à cette réunion.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Annoncer l’entrée et la sortie</td> 
   <td>Choisissez si vous souhaitez que la réunion annonce le moment où les participants rejoignent ou quittent l'événement.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Étendue</td> 
   <td>Sélectionnez le groupe de participants qui peuvent contourner l'attente dans la salle d'attente. Ces participants rejoindront directement la réunion.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Permettre aux utilisateurs d'accès à distance de contourner la salle d'attente</td> 
   <td>Choisissez si vous souhaitez permettre aux utilisateurs d'accès à distance de contourner la salle d'attente.</td> 
   </tr> 
   <tr> 
   <td role="rowheader">Enregistrement automatique</td> 
   <td>Choisissez si vous souhaitez enregistrer la réunion automatiquement.</td> 
   </tr> 
   </tbody> 
</table>

### Autre

* [Vérifier la présence des utilisateurs](#check-presence-of-users)
* [Effectuer un appel API personnalisé.](#make-a-custom-api-call)
* [Rechercher des utilisateurs](#search-users)

#### Vérifier la présence des utilisateurs

Ce module d’action vérifie si les utilisateurs sélectionnés sont présents sur Microsoft Teams.

Ce module ne prend pas en charge les comptes personnels.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">ID d’utilisateur</td> 
   <td> <p>Sélectionnez les utilisateurs pour lesquels vous souhaitez vérifier la présence.</p> </td> 
   </tr> 
 </tbody> 
</table>

#### Effectuer un appel API personnalisé.

Ce module d’action effectue une requête personnalisée à l’API Microsoft Teams.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Saisissez un chemin relatif à <code>https://graph.microsoft.com</code>. Exemple :<code> /v1.0/groups</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion ajoute les en-têtes d’autorisation pour vous.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Ajoutez la requête pour l’appel API sous la forme d’un objet JSON standard.</p> <p>Par exemple : <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre JSON, placez les guillemets à l’extérieur de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### Rechercher des utilisateurs

Ce module recherche des utilisateurs à l’aide des critères que vous spécifiez.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">Connexion </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte Microsoft Teams à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">Création d’une connexion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Filtre</td> 
   <td> <p>Vous pouvez définir un filtre pour renvoyer uniquement les utilisateurs et utilisatrices qui répondent aux critères de votre choix.</p> <p>Pour chaque filtre, saisissez le champ que le filtre doit évaluer, l’opérateur et la valeur que le filtre doit autoriser. Vous pouvez utiliser plusieurs filtres en ajoutant des règles ET ou OU.</p> </td> 
   </tr> 
  <tr> 
   <td>Nombre maximal de résultats renvoyés</td> 
   <td>Définissez le nombre maximal d’équipes ou de groupes que Workfront Fusion renverra au cours d’un cycle d’exécution.</td> 
  </tr> 
 </tbody> 
</table>



