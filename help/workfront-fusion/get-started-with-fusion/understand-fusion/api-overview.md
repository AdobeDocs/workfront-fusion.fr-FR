---
title: Vue d’ensemble de l’API
description: Les interfaces de programmation d’applications (API) permettent aux applications et aux services de communiquer entre eux. Fusion utilise des API pour communiquer avec l’application à laquelle vous vous connectez. Chaque application dispose d’une API distincte.
author: Becky
feature: Workfront Fusion
source-git-commit: b30aac8040cc0b6bcad92914b1c0997a8ddebdd5
workflow-type: ht
source-wordcount: '431'
ht-degree: 100%

---

# Vue d’ensemble des API dans Fusion

<!--Add me to TOCs-->

Les interfaces de programmation d’applications (API) permettent aux applications et aux services de communiquer entre eux. Fusion utilise des API pour communiquer avec les applications auxquelles vous vous connectez.

Les API sont créées et contrôlées par les propriétaires de l’application. Par exemple, l’API Workfront appartient à l’équipe Workfront d’Adobe et l’API Microsoft Graph appartient à Microsoft. Le propriétaire de l’API définit les actions disponibles via l’API.

## Considérations

Le fait que les API sont définies par leurs propriétaires et non par Fusion implique un point essentiel :

* **Vous pouvez utiliser Fusion pour vous connecter à toute application ou service disposant d’une API publique** que Fusion propose ou non un connecteur dédié à cette application ou à ce service. Vous pouvez utiliser les connecteurs universels de Fusion pour inclure ces applications ou services dans vos scénarios.

  Pour obtenir la liste des connecteurs universels, consultez [Connecteurs universels](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors).

* **Les modifications apportées à l’API d’une application par son propriétaire peuvent affecter le fonctionnement de Fusion.** S’il s’agit de modifications majeures, Fusion peut avoir besoin de mettre à jour des modules ou des types de connexion, ou dans des cas extrêmes, de créer un nouveau connecteur pour l’application.

  Pour plus d’informations sur ces cas extrêmes, connus sous le nom de « modifications avec rupture », consultez [Modifications avec rupture](#breaking-changes) dans cet article.


## Modifications avec rupture

La dépréciation est souvent à l’origine des modifications avec rupture, lorsqu’un propriétaire d’API retire la disponibilité d’une partie ou de la totalité d’une API. Lorsque cela se produit, l’équipe de Fusion met tout en œuvre pour adapter rapidement le fonctionnement de Fusion à la nouvelle version de l’API de l’application. Pour cela, on utilise habituellement de nouveaux modules, types de connexion ou connecteurs.

Comme les scénarios Fusion sont configurés avec vos données, vous devrez peut-être mettre à jour vos scénarios.

* Si les modifications étaient liées à l’authentification ou à l’autorisation, vous devrez peut-être mettre à jour les connexions pour cette application.
* Si les modifications étaient liées à une action spécifique (point d’entrée) dans l’API, vous devrez peut-être mettre à jour tout module lié à cette action vers une nouvelle version du module.
* Si l’ensemble de la version d’API utilisée par Fusion est obsolète, vous devrez peut-être mettre à jour tous les modules de ce connecteur vers une nouvelle version du connecteur.

Dans a plupart des cas, vous pouvez effectuer une mise à niveau vers la nouvelle version d’un module sans avoir à le reconfigurer.

Pour plus d’informations et d’instructions sur la mise à niveau d’un module, consultez [Mettre à niveau un module vers une nouvelle version](/help/workfront-fusion/manage-scenarios/update-module-to-new-version.md).
