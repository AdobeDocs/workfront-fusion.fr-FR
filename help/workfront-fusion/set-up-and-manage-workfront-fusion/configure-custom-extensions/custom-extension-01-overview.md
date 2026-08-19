---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Présentation de l’extensibilité de l’interface utilisateur
description: Extensions personnalisées dans Workfront Fusion
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: 925a8ee910434c474d527c2914897d7c42e4a3d1
workflow-type: tm+mt
source-wordcount: 835
ht-degree: 1%

---

# Présentation de l’extensibilité de l’interface utilisateur

L’extensibilité de l’interface utilisateur vous permet d’importer votre logique et votre interface utilisateur personnalisées dans Adobe Workfront Fusion. En utilisant Adobe App Builder, vous pouvez modifier l’expérience Workfront Fusion de votre entreprise afin de mieux répondre aux besoins de l’entreprise, tout en vous appuyant sur les fonctionnalités de base de Fusion.

Cet article donne une vue d’ensemble de l’extensibilité de l’interface utilisateur et de la manière dont votre extension personnalisée communique avec Workfront Fusion.

## Structure de l’extension

* [Hôtes et invités](#hosts-and-guests)
* [La technologie sous-jacente](#the-technology-underneath)

### Hôtes et invités

Fusion peut afficher l’interface utilisateur qui n’a pas été créée par l’équipe de Workfront Fusion. Pour s’assurer que ces modifications de l’interface utilisateur n’affectent pas les fonctionnalités de base de Fusion, l’interface utilisateur s’exécute dans son propre cadre de navigateur isolé (un `<iframe>`), complètement distinct du code de Fusion.

* **Hôte** : application qui *contient* l’extension. Ici, c&#39;est **Fusion**. L’hôte décide où les extensions peuvent apparaître et quelles données il partage avec elles.
* **Invité** : *Votre extension*. Il s’agit d’une petite application web que l’hôte charge dans un iframe.

Lors de la création d’une extension d’interface utilisateur, vous ne modifiez pas Fusion. Vous créez et publiez un invité que Fusion peut utiliser une fois l’invité publié.

### La technologie sous-jacente

Votre invité repose sur deux technologies Adobe :

* **Adobe App Builder** : une plateforme d’hébergement et d’outils gratuite pour les petites applications web et les actions sans serveur. Votre extension est une application App Builder. App Builder vous permet d’héberger votre interface utilisateur (sur le réseau de diffusion de contenu `*.adobeio-static.net` d’Adobe) et un outil de ligne de commande appelé `aio` pour la créer, la créer et la publier.
* **SDK d’extensibilité de l’interface utilisateur d’Adobe (UIX)** : les bibliothèques qui permettent à l’hôte et à l’invité de parler. Vous n&#39;utiliserez qu&#39;un seul paquet, `@adobe/uix-guest`, de votre côté. Fusion utilise le package de `@adobe/uix-host` correspondant sur son côté.

<!--

```
   ┌────────── Browser ─────────────────────────────┐
   │                                                                   │
   │   Fusion (Host)                      Your extension (Guest)       │
   │   ────────────                       ─────────────────────        │
   │   @adobe/uix-host   ◀── messages ──▶  @adobe/uix-guest            │
   │        │                                    │                     │
   │   renders an iframe ───────────────▶  your React/HTML UI          │
   │                                                                   │
   └───────────────────────────────────────────────────────────────────┘

   Your UI files are hosted by Adobe App Builder at
   https://<your-app>.adobeio-static.net
```

-->

## Points d’extension

Un point d’extension est un « slot » nommé dans l’hôte où un invité est autorisé à apparaître. Fusion définit ses créneaux, et vous choisissez celui que l&#39;invité utilisera.

Un nom de point d&#39;extension comporte trois parties : `service/name/version`.

Fusion offre les points d’extension suivants :

| Point d&#39;extension | Emplacement de l’interface utilisateur dans Fusion | Quand l’utiliser |
| --- | --- | ---- |
| `fusion/nav-organization/1` | Dans la section **Organisation** du volet de navigation de gauche. | Votre outil concerne l&#39;ensemble de l&#39;organisation. |
| `fusion/nav-team/1` | Sous la section **Équipe** du volet de navigation de gauche (affiché lorsqu’une équipe est sélectionnée). | Votre outil concerne une équipe spécifique. |

* `fusion` est le **service** (le produit, Fusion).
* `nav-organization` / `nav-team` est le **nom** (emplacement spécifique).
* `1` est la **version**.

Une extension peut implémenter un ou deux points d’extension. La plupart des extensions utilisent un point.

En fonction du point d’extension sélectionné, Fusion ajoute un bouton avec le titre de l’extension à la section de navigation correspondante. Cliquez dessus pour ouvrir une page dédiée dans la zone de contenu principale de Fusion et y charger votre interface utilisateur.

## Frames inclus dans une extension d’interface utilisateur

>[!IMPORTANT]
>
>Cette section aborde un aspect des extensions d’interface utilisateur qui peut prêter à confusion. Nous vous recommandons de le lire attentivement.

Lorsque Fusion charge votre invité, votre extension s’exécute dans **deux** images :

1. **Cadre d’enregistrement (invisible).** S’exécute en premier, en arrière-plan. Le cadre d’enregistrement indique à Fusion ce que votre extension offre. Par exemple, elle peut indiquer qu’elle dispose d’un widget de tableau de bord et envoyer le titre du widget et l’URL de son interface utilisateur. Le cadre d’enregistrement effectue cette opération en appelant `register(...)`. Aucune interface utilisateur n’est visible.
1. **Cadre de l’interface utilisateur (visible).** Il s’agit de la page que Fusion présente à l’utilisateur. Il doit s’annoncer auprès de l’hôte en appelant `attach(...)`. S’il n’appelle jamais `attach`, Fusion attend et finit par s’arrêter avec une erreur.

>[!BEGINSHADEBOX]

Cet exemple montre le flux lorsqu’un utilisateur clique sur le bouton de l’extension.

1. Cliquez sur le bouton.
1. Fusion charge votre cadre d&#39;ENREGISTREMENT (masqué).

   ```
   register({ methods: { dashboard: { getWidget() {...} } } })
   ```

   `getWidget()` renvoie l’URL de votre interface utilisateur visible
1. Fusion charge votre cadre d’interface utilisateur (visible) à cette URL.

   ```
   attach({ id }) 
   ```

   Ceci est obligatoire, sinon Fusion expire
1. Fusion envoie du contexte et votre interface utilisateur s’affiche.

>[!ENDSHADEBOX]

Les deux cadres sont écrits lorsque vous créez l’interface utilisateur. L’important est de se rappeler que la page visible **doit** appeler `attach`.

Pour plus d’informations sur la création de l’interface utilisateur, voir [Créer l’interface utilisateur d’extension personnalisée](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md).

## Contexte de Fusion

Une fois l’extension attachée, Fusion partage un objet `context` avec votre invité. Il contient les éléments suivants :

* **Utilisateur** : profil Fusion de l’utilisateur connecté et ID utilisateur Adobe IMS.
* **Organisation** : enregistrement d’organisation Fusion complet de l’organisation active et ID d’organisation Adobe IMS.
* **Équipe** : l’équipe active, le cas échéant.
* **Jeton d’accès Adobe IMS** : il appelle les API Adobe ou Fusion au nom de l’utilisateur ou de l’utilisatrice, si nécessaire.

Fusion envoie également des mises à jour. Par exemple, si l’utilisateur change d’organisation ou d’équipe alors que l’interface utilisateur est ouverte, Fusion envoie le nouveau contexte afin que l’interface utilisateur puisse réagir instantanément.

Pour obtenir la liste complète des champs de contexte, voir [Référence de contexte de Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).

## Créer une extension d’interface utilisateur

Pour créer une extension d’interface utilisateur, procédez comme suit :

1. [Installation des outils et création d’un projet Adobe](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md).
1. [Générez un projet App Builder vierge, pointez-le vers un point d’extension Fusion et enregistrez votre widget](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md).
1. [Créer l’interface utilisateur et se connecter à Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md).
1. [Utilisez le contexte que Fusion envoie](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).
1. [Publiez pour que Fusion puisse le trouver](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md).
1. (Facultatif) [Appeler les API Workfront/Fusion pour obtenir des données réelles sans CORS](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md).

Pour lancer le processus, accédez à [&#x200B; Configuration de vos outils et de votre compte Adobe &#x200B;](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md).


