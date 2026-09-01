---
title: Initialiser le stockage
description: Lorsque l’utilisateur accède pour la première fois au stockage , un écran d’initialisation lui est associé et il établit une connexion sécurisée au stockage Adobe pour le compte de l’équipe.
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: a2632cb3184cd555555136288e78ab1e05e4ea9d
workflow-type: tm+mt
source-wordcount: 216
ht-degree: 0%

---

# Initialisation du stockage dans Workfront Fusion

La zone de stockage Fusion doit être initialisée avant de pouvoir afficher les référentiels, les dossiers et les fichiers dans votre espace de stockage cloud Adobe.

Pour une présentation du stockage, voir [Présentation du stockage](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/storage-overview.md).

## Initialiser le stockage

1. Dans Workfront Fusion, cliquez sur **Stockage** dans le volet de navigation de gauche.
1. Cliquez sur **Initialiser le stockage**.

Fusion crée automatiquement une connexion sécurisée au stockage Adobe pour le compte de l’équipe.

Une fois la connexion établie, Fusion charge les référentiels de stockage de l’équipe.

## Résolution des problèmes d’initialisation

| Message | Raison | Ce que l’utilisateur doit faire |
| -------- | -------- | ------------------------ |
| **Accès limité** | L’organisation ne s’intègre pas à Adobe IMS. | Contactez l’administrateur de l’organisation pour terminer l’intégration IMS. |
| **Organisation non concordante** | L’utilisateur est connecté à une organisation Adobe différente de celle sélectionnée dans Fusion. | Déconnectez-vous, puis reconnectez-vous avec l’organisation Adobe IMS appropriée. |
| **Accès refusé** | Le compte de l’utilisateur ne dispose pas des autorisations requises ou le stockage Adobe n’est pas disponible pour l’organisation. | Vérifiez les autorisations du compte avec l’administrateur de l’organisation. Après la résolution, cliquez sur **Réessayer**. |
| **Aucun stockage trouvé** | La connexion a été établie, mais aucun référentiel n’a été trouvé. | Vérifiez que le stockage Adobe est configuré pour l’organisation. Après vérification, cliquez sur **Charger le stockage** pour réessayer. |
