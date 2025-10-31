---
title: Afficher et résoudre les exécutions incomplètes
description: Le dossier [!UICONTROL Exécutions incomplètes] stocke les exécutions de scénario qui n’ont pas été finalisées correctement en raison d’une erreur. Chaque exécution incomplète stockée peut être résolue manuellement ou automatiquement.
author: Becky
feature: Workfront Fusion
exl-id: 8891b4d7-a39a-4f14-8521-8c2ca186ca6e
source-git-commit: 42be02d6a59a5d7b8faccdcfe40e8b967153c6eb
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 65%

---

# Afficher et résoudre les exécutions incomplètes

Le dossier [!UICONTROL Exécutions incomplètes] stocke les exécutions de scénario qui n’ont pas été finalisées correctement en raison d’une erreur. Chaque exécution incomplète stockée peut être résolue manuellement ou automatiquement.

>[!NOTE]
>
>Par défaut, le stockage des exécutions incomplètes est désactivé. Pour l’activer, activez l’option [!UICONTROL Autoriser le stockage d’exécutions incomplètes] dans les paramètres avancés du scénario.
>
>Pour plus d’informations sur les paramètres de scénario, voir [Configurer les paramètres de scénario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md).

## Prévisualisation mise en surbrillance pour l’article complet {#highlighted-preview-article-level}

<span class="preview">Les informations de cette page font référence à des fonctionnalités qui ne sont pas encore disponibles de façon générale. Il est disponible uniquement dans l’environnement de sandbox de prévisualisation.</span>## Afficher les exécutions incomplètes

Si un module rencontre une erreur lors de son fonctionnement, une nouvelle exécution incomplète est ajoutée au dossier Exécutions incomplètes. Chaque exécution incomplète contient le plan directeur du scénario et tous les lots pouvant être mappés dans le module qui a échoué. La liste des exécutions incomplètes peut être ouverte en cliquant sur l’onglet [!UICONTROL &#x200B; Exécutions incomplètes &#x200B;] de la page des détails du scénario.

<!--

![Incomplete executions tab](assets/incomplete-executions-tab-350x102.png)

-->

Pour plus d’informations, voir [Erreurs entraînant des exécutions incomplètes](#errors-resulting-into-incomplete-executions) dans cet article.

>[!NOTE]
>
>La limite de taille actuelle du dossier des exécutions incomplètes non résolues par scénario est de 10 Mo. Si votre scénario dépasse cette limite, l’erreur suivante peut s’afficher :
>
>`DLQ limit per scenario has been exceeded`
>
>Les équipes sont limitées à un total de 500 Mo pour toutes les exécutions incomplètes non résolues.
>
>Pour plus d’informations, voir [Activer la perte de données](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#enable-data-loss) dans l’article Configuration des paramètres de scénario.


## Résolvez les exécutions incomplètes à partir de l’onglet Exécutions incomplètes

Lorsqu’une nouvelle exécution incomplète est stockée, vous pouvez la résoudre comme suit :

1. Ouvrez le scénario concerné.
1. Cliquez sur l’onglet **[!UICONTROL Exécutions incomplètes]**.
1. Recherchez l’exécution incomplète que vous souhaitez résoudre, puis cliquez sur **[!UICONTROL Détails]**.
1. Ouvrez le journal du module, où toutes les opérations du module sont affichées.
1. Recherchez l’opération ayant échoué et cliquez sur **[!UICONTROL Résoudre]** :

   ![bouton Résoudre](assets/resolve-btn-350x188.png)



## Résoudre les exécutions incomplètes à partir de l’onglet Historique

Si vous souhaitez consulter le journal de toutes les opérations du module avant de tenter de résoudre l’exécution incomplète, vous pouvez résoudre l’exécution incomplète à partir du dossier [!UICONTROL Historique] :

1. Ouvrez le scénario concerné.
1. Cliquez sur l’onglet **[!UICONTROL Historique]**.
1. Recherchez l’échec d’exécution du scénario, puis cliquez sur **[!UICONTROL Détails]**.
1. Ouvrez le journal du module, où toutes les opérations du module sont affichées.
1. Recherchez l’opération ayant échoué et cliquez sur **[!UICONTROL Résoudre]** :

   ![bouton Résoudre](assets/resolve-btn-350x188.png)

## Options relatives aux exécutions incomplètes

Les options suivantes dans le panneau [!UICONTROL Paramètres du scénario] déterminent si et comment les exécutions incomplètes sont stockées :

* Autoriser le stockage d’exécutions incomplètes
* Traitement séquentiel
* Activer la perte de données

Pour plus d’informations sur ces options, voir [Configurer les paramètres de scénario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md).

## Erreurs entraînant des exécutions incomplètes

Il existe plusieurs catégories d’erreurs qui entraînent le stockage d’exécutions incomplètes. Ces erreurs peuvent inclure les suivantes :

* Des erreurs de validation dues à des données incomplètes ou erronées. Le plus souvent, cela est dû à un élément manquant qui est nécessaire pour traiter avec succès toutes les données passant par un module.
* Des erreurs dues à l’indisponibilité de la destination finale en raison d’un échec temporaire ou à long terme de la connexion (par exemple, lors de la connexion à un serveur de messagerie ou FTP distant).

Si une erreur se produit sur le premier module du scénario, l’exécution s’arrête immédiatement et aucune exécution incomplète n’est stockée.

Si une erreur se produit sur un autre module et qu’aucun itinéraire de gestionnaire d’erreur n’est associé, alors l’un des événements suivants se produit :

* Un enregistrement d’exécution incomplet avec reprise automatique est stocké pour les types d’erreur suivants :

   * `ConnectionError`
   * `RateLimitError`
   * `OutOfSpaceError`
   * `ModuleTimeoutError`

* Un enregistrement d’exécution incomplet sans reprise automatique est stocké pour les types d’erreur suivants :

   * `DataError`
   * `InvalidConfigurationError`
   * `InvalidAccessTokenError`
   * `UnexpectedError`
   * `MaxFileSizeExceededError`
   * `MaxResultsExceededError`

* Si le type d’erreur est autre que ci-dessus, l’exécution échoue.
