---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: 'Activité Version de Workfront Fusion : semaine du 16 novembre 2020'
description: Cette page décrit toutes les améliorations apportées à Adobe Workfront Fusion au cours de la semaine du 16 novembre 2020.
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
exl-id: 69e4a458-fd32-4dcd-be43-19a9467cf678
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 94%

---

# Activité Version de Workfront Fusion : semaine du 16 novembre 2020

Cette page décrit toutes les améliorations apportées à Adobe Workfront Fusion au cours de la semaine du 16 novembre 2020.

Pour obtenir la liste de toutes les modifications récentes, voir [Activité de publication d’Adobe Workfront Fusion](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

Pour obtenir la liste des correctifs récents dans Workfront Fusion, reportez-vous à la page [Mises à jour de maintenance Workfront](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html) et recherchez toutes les mises à jour intitulées Mise à jour de maintenance de Workfront Fusion.

## Mises à jour du connecteur Jira Cloud

Pour élargir les possibilités d’utilisation du connecteur Jira Cloud, nous avons ajouté trois modules :

* Ajouter un problème au sprint
* Lister les enregistrements
* Rechercher des enregistrements

Nous avons également mis à jour les modules existants pour prendre en charge le type d’objet « Sprint ». Auparavant, l’objet « Sprint » n’était accessible que par le biais du module d’appel API personnalisé.

## L’identifiant d’exécution est désormais disponible pour le mappage dans les scénarios.

L’identifiant d’exécution d’un scénario est désormais disponible dans le panneau de mappage. Cet identifiant représente une exécution spécifique du scénario et peut être utilisé comme métadonnée. Par exemple, l’identifiant d’exécution peut être sauvegardé avec un enregistrement créé par Fusion, afin que vous puissiez déterminer ultérieurement l’exécution de Fusion qui a créé l’enregistrement. Vous le trouverez dans le panneau de mappage, sous Fonctions générales.

## Raccourcis clavier pour les scénarios de Workfront Fusion 2.0

Pour faciliter l’élaboration des scénarios, nous avons ajouté quelques raccourcis clavier :

* Ctrl/Cmd+Maj+Entrée : exécuter un scénario une seule fois
* Ctrl/Cmd+Maj+S : enregistrer un scénario

## Mises à jour du connecteur Excel d’Office 365

Pour élargir les possibilités d’utilisation du connecteur Excel d’Office 365, nous avons ajouté de nouveaux modules. Vous pouvez désormais effectuer les opérations suivantes :

* Déclencher un module à partir des modifications apportées aux classeurs
* Effectuer des recherches dans des classeurs ou les télécharger
* Répertorier les feuilles de calcul, les lignes de feuilles de calcul, les tableaux ou les lignes de tableaux
* Mettre à jour une ligne de tableau ou de feuille de calcul
* Supprimer une ligne de tableau ou de feuille de calcul
* Récupérer des métadonnées pour un tableau
* Effectuer un appel API personnalisé.

Les modules précédemment disponibles sont toujours présents dans l’application.


## Utiliser OAuth 2.0 dans les connexions de votre application Workfront

Nous avons mis à jour le connecteur Workfront afin qu’il utilise OAuth 2.0. Cette mise à jour facilite les modifications dans les connexions de votre application Workfront. Par exemple, si un élément relatif à votre connexion change (un mot de passe, par exemple), vous n’avez plus besoin de mettre à jour chacune des connexions de vos scénarios. En outre, OAuth2 offre d’autres avantages, tels que l’amélioration de la sécurité et la possibilité d’utiliser l’authentification unique (SSO).

Les connexions existantes ne nécessitent aucune modification pour le moment. Vous pouvez toutefois autoriser de nouveau les connexions existantes si vous souhaitez bénéficier des avantages d’OAuth 2.0.
