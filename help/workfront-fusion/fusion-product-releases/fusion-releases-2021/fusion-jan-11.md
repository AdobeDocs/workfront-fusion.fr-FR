---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: 'Activité Version de Workfront Fusion : semaine du 11 janvier 2021'
description: Cette page décrit toutes les améliorations apportées à Adobe Workfront Fusion durant la semaine du 11 janvier 2021.
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
exl-id: d5732b6c-b039-4bf7-a7e6-e59b6e8f1a63
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 100%

---

# Activité Version de Workfront Fusion : semaine du 11 janvier 2021

Cette page décrit toutes les améliorations apportées à Adobe Workfront Fusion durant la semaine du 11 janvier 2021.

Pour obtenir la liste de toutes les modifications récentes, voir [Activité de publication d’Adobe Workfront Fusion](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

Pour obtenir la liste des correctifs récents dans Workfront Fusion, reportez-vous à la page [Mises à jour de maintenance Workfront](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html) et recherchez toutes les mises à jour intitulées Mise à jour de maintenance de Workfront Fusion.

## Connecteur et modules Widen désormais disponibles

Vous pouvez désormais utiliser Workfront Fusion pour vous connecter à votre compte Widen. Avec les modules Widen, vous pouvez effectuer les opérations suivantes :

* Ajouter ou retirer des ressources d’une collection
* Télécharger ou charger des fichiers
* Lire ou mettre à jour les métadonnées des ressources
* Rechercher des ressources en fonction des critères que vous spécifiez
* Récupérer une liste de ressources dans une collection
* Effectuer un appel API personnalisé.

## Connecteur et modules Datadog désormais disponibles

Vous pouvez désormais utiliser Workfront Fusion pour vous connecter à votre compte Datadog.

Avec les modules Datadog, vous pouvez effectuer les opérations suivantes :

* Publier les points de la série chronologique
* Effectuer un appel API personnalisé

## Connecteur et modules Cvent désormais disponibles

Vous pouvez désormais utiliser Workfront Fusion 2.0 pour vous connecter à votre compte Cvent.

Avec les modules Cvent, vous pouvez effectuer les opérations suivantes :

* Créer une demande de réunion
* Lire des enregistrements tels que des contacts, des événements ou des invitations
* Répertorier les enregistrements en fonction des critères spécifiés
* Enregistrer ou ajouter des personnes invitées à des événements spécifiques
* Mettre à jour ou supprimer des contacts
* Effectuer un appel API personnalisé.


## Connecteur et modules Microsoft Dynamic 365 désormais disponibles

Vous pouvez désormais utiliser Workfront Fusion 2.0 pour vous connecter à votre compte Microsoft Dynamics 365. Avec les modules Microsoft Dynamics 365, vous pouvez effectuer les opérations suivantes :

* Déclencher un scénario lorsque des enregistrements sont ajoutés ou mis à jour dans Microsoft Dynamics 365.
* Créer, lire, mettre à jour ou supprimer un enregistrement Microsoft Dynamics 365.
* Effectuer un appel API personnalisé

## Connecteur et modules DocuSign désormais disponibles

Vous pouvez désormais utiliser Workfront Fusion 2.0 pour vous connecter à votre compte Docusign. Avec les modules Docusign, vous pouvez effectuer les opérations suivantes :

* Déclencher un scénario lorsqu’une enveloppe modifie son statut.
* Créer une enveloppe.
* Lire, envoyer ou ajouter une personne destinataire à une enveloppe existante.
* Ajouter ou modifier des champs personnalisés dans des documents.
* Télécharger un document sous la forme d’un champ.
* Charger un fichier vers une enveloppe.
* Effectuer un appel API personnalisé.


## Rechercher l’historique d’exécution de votre scénario

Nous vous avons facilité la recherche d’informations spécifiques provenant d’exécutions de scénarios précédentes. La nouvelle recherche de texte intégral de Fusion permet de rechercher dans l’historique d’exécution toutes les données contenues dans un lot. Par exemple, pour identifier l’exécution qui a créé une tâche spécifique, vous pouvez utiliser la recherche de texte intégral pour rechercher cet ID de tâche.

Auparavant, la recherche d’informations d’exécution spécifiques nécessitait d’afficher chaque exécution individuellement.

## Mises à jour de l’entrepôt de données Fusion 2.0

Afin que vous puissiez plus facilement personnaliser vos entrepôts de données, nous avons ajouté de nouvelles fonctionnalités. Maintenant, lorsque vous affichez un entrepôt de données, vous pouvez effectuer les opérations suivantes :

* Effectuer un glisser-déposer pour réorganiser les colonnes
* Modifier un seule cellule
* Ajouter plusieurs lignes


## Effectuer une demande d’autorisation par clé API via le connecteur HTTP

Afin d’accroître la flexibilité d’accès aux API, nous avons ajouté un nouveau module au connecteur HTTP. Désormais, vous pouvez utiliser le connecteur HTTP pour effectuer une requête lorsque le service web auquel vous accédez nécessite l’utilisation d’une clé API.

## Nouvelles fonctions disponibles dans le panneau de mappage

Pour vous aider à personnaliser et simplifier les formules de vos modules, nous avons ajouté de nouvelles fonctions.

* La fonction

  ```
  omit
  ```

  est une fonction générale qui omet les clés données de l’objet et renvoie le reste.
* La fonction

  ```
  pick
  ```

  est une fonction générale qui sélectionne uniquement les clés données de l’objet.
* La fonction

  ```
  escapeMarkdown
  ```

  est une fonction de chaîne qui échappe toutes les balises Markdown d’un texte.
