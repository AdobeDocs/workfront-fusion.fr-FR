---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: 'Extensions d’interface utilisateur personnalisées : index d’article'
description: Extensions personnalisées dans Workfront Fusion
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 603
ht-degree: 3%

---


# Extensions d’interface utilisateur personnalisées : index d’article

Fusion peut afficher votre propre interface utilisateur web dans son interface. Vous créez une petite application web, appelée extension, vous la publiez dans Adobe et elle s’affiche sous la forme d’un bouton dans la navigation de Fusion. Lorsqu’un utilisateur clique dessus, votre interface utilisateur s’affiche dans la zone principale de Fusion et reçoit automatiquement des informations sur la personne connectée, l’organisation et l’équipe dans lesquelles il travaille, etc.

Cette section de la documentation sur la fusion vous guide tout au long du processus, sans supposer une expérience préalable avec Adobe App Builder ou les structures front-end. Il comprend également le code nécessaire, ainsi que des explications de ce code.

## Quand utiliser ce guide

Utilisez ce guide si vous souhaitez ajouter un écran ou un outil personnalisé à Fusion. Vous n’avez pas besoin d’être un développeur expert. Vous devez être à l’aise pour copier des commandes dans un terminal et modifier quelques fichiers texte.

Pour créer une extension d’interface utilisateur personnalisée, vous aurez besoin d’une Adobe ID et d’un accès à une organisation Adobe (le même type d’accès que celui que vous utilisez pour vous connecter à Fusion).

## Ce que vous allez créer

À la fin de ce guide, vous aurez :

1. Un projet Adobe **App Builder** gratuit. C’est là que réside votre extension.
1. Petite application web qui effectue le rendu de votre interface utilisateur personnalisée.
1. Cette application web s’est connectée à l’un des points d’extension de Fusion afin qu’elle apparaisse dans la navigation de Fusion.
1. Votre interface utilisateur lit le contexte en direct à partir de Fusion, tel que l’utilisateur, l’organisation et l’équipe actuels, et réagit lorsque l’utilisateur change d’organisation ou d’équipe.
1. L’extension a été publiée afin que d’autres utilisateurs de votre organisation puissent la voir.

<!--

## How it works, in one picture

```
  Fusion (the "Host")                         Your extension (the "Guest")
  ───────────────────────────────                         ──────────────────────────────
  Left navigation                             A web app hosted by Adobe
   └── Organization                            (App Builder + UI Extensibility)
       └── [Your extension button]  ── click ──▶ Fusion opens your UI in an iframe
                                              and sends it live context:
                                               * signed-in user
                                               * active organization
                                               * active team
                                               * Adobe IMS identifiers
```

Fusion is the **host**. Your extension is the **guest**. They run in separate browser frames and talk to each other through Adobe's **UI Extensibility SDK** (no custom networking required on your side).

-->

## Table des matières

Lisez les pages dans l’ordre la première fois. Plus tard, vous pouvez sauter directement à celui dont vous avez besoin.

| # | Page | Ce qu’il couvre |
| --- | ------ | ---------------- |
| 1 | [Présentation et concepts clés](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-01-overview.md) | Le vocabulaire, l’architecture et l’utilité de chaque point d’extension Fusion. |
| 2 | [Configurer vos outils et votre compte Adobe](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md) | Node.js, interface de ligne de commande d’Adobe I/O, connexion et création de votre projet dans Adobe Developer Console. |
| 3 | [Créer le projet et le configurer pour Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md) | Générez un projet App Builder générique avec la ligne de commande `aio` (et non un modèle spécifique au produit). Ensuite, pointez votre projet vers un point d’extension Fusion et enregistrez votre widget. |
| 5 | [Créer l’interface utilisateur](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md) | Effectuez le rendu de votre écran personnalisé et terminez la connexion (« poignée de main ») avec Fusion. |
| 6 | [Référence du contexte de Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md) | Chaque champ que Fusion vous envoie, ce qu’il signifie et comment réagir aux modifications. |
| 7 | [Publier votre extension](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md) | Créez, déployez et rendez votre extension visible dans Fusion. |
| 8 | [Dépannage](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md) | Correctifs pour les erreurs les plus courantes. |
| 9 | [Présentation de la démonstration](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-09-demo-walkthrough.md) | Un script de copier-coller linéaire : modèle automatique du modèle Experience Cloud Shell générique → recibler vers Fusion → déployer vers les → d’évaluation exécutées dans Fusion. Idéal pour une démonstration en direct. |
| 10 | [Appel des API Workfront et Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md) | Appelez les API principales de votre extension sans accéder à la configuration CORS du navigateur, à l’aide d’un proxy d’action d’exécution. Couvre les en-têtes `require-adobe-auth` et Fusion v3, ainsi qu’un exemple pratique. |

## Note sur la disponibilité

Fusion expose actuellement ces points d’extension :

* `fusion/nav-organization/1` : apparaît sous la section **Organisation**.
* `fusion/nav-team/1` : apparaît sous la section **Équipe**.

Avant de pouvoir effectuer une publication sur l’un de ces sites, le point d’extension doit avoir été intégré à votre organisation Adobe. Si l’étape de publication échoue en indiquant que le point d’extension n’existe pas, reportez-vous à la section [&#x200B; Dépannage &#x200B;](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md).

## Documentation officielle d’Adobe

Ce guide est spécifique à Fusion. Pour la plateforme sous-jacente, les références canoniques sont les suivantes :

* [Présentation de l’extensibilité de l’interface utilisateur](https://developer.adobe.com/uix/docs/)
* [Flux de développement de l’extension d’interface utilisateur](https://developer.adobe.com/uix/docs/guides/development-flow/)
* [Gestion des extensions d’interface utilisateur (publier/approuver/révoquer)](https://developer.adobe.com/uix/docs/guides/publication/)
* [Prise en main d’Adobe App Builder](https://developer.adobe.com/app-builder/docs/getting_started/)
