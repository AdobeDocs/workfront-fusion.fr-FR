---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Référence du contexte de Fusion
description: Référence du contexte de Fusion
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 757
ht-degree: 8%

---

# Référence du contexte de Fusion

>[!NOTE]
>
>Cet article suppose que vous connaissez un peu les outils de développement logiciel.

Lorsque votre interface utilisateur appelle `attach(...)`, Fusion partage un objet **context** décrivant la session en cours. Cette page répertorie tous les champs, ce qu’ils signifient et la manière dont les identifiants Fusion et Adobe IMS sont liés.

## Comment lire le contexte

* **Valeurs initiales :** `connection.sharedContext.get("<key>")`
* **Mises à jour :** écouter l’événement `contextchange`. Le dernier objet arrive sur `event.detail.context`.

Pour le modèle de code complet, voir [Création de l’interface utilisateur de l’extension personnalisée](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md).

```js
const organization = connection.sharedContext.get("organization");
const fusionOrgId  = organization?.id;        // Fusion's organization id
const imsOrgId     = connection.sharedContext.get("imsOrgId"); // Adobe IMS org id
```

## Clés de niveau supérieur

| Clé | Type | Description |
| ----- | ------ | ------------- |
| `imsToken` | chaîne | Jeton d’accès Adobe **IMS** de l’utilisateur connecté. Utilisez-le comme jeton d’`Bearer` pour appeler les API Adobe ou Fusion au nom de l’utilisateur. **Comme il s’agit d’un élément sensible, ne le consignez ni n’affichez.** |
| `imsOrgId` | chaîne | L’identifiant de l’organisation Adobe **IMS**, sous la forme `XXXXXXXXXXXX@AdobeOrg`. |
| `imsUserId` | chaîne | L’Adobe **ID utilisateur IMS** de l’utilisateur connecté. |
| `organization` | objet | L’**organisation Fusion active complète**. Pour plus d’informations, consultez [`organization` champs](#organization-fields) dans cet article. |
| `team` | objet \| non défini | L’**équipe Fusion active complète**, lorsqu’elle est active (toujours pertinente pour les `fusion/nav-team/1`). Pour plus d’informations, consultez [`team` champs](#team-fields) dans cet article. |
| `user` | objet | L’**utilisateur Fusion entièrement connecté** Pour plus d’informations, consultez [`user` champs](#user-fields) dans cet article. |

### Fusion ID et IMS ID

Chaque entité possède un **Fusion ID** (utilisé par les propres API de Fusion) et, s’il existe, un **Adobe IMS ID** (utilisé par les API de la plateforme Adobe) :

| Entité | Identifiant de fusion | Identifiant Adobe IMS |
| -------- | ----------- | -------------- |
| Organisation | `organization.id` | `imsOrgId` (également exposé en tant que `organization.externalOrgId`) |
| Équipe | `team.id` | *(Les équipes sont dans Fusion uniquement ; aucun identifiant IMS)* |
| Utilisateur ou utilisatrice | `user.id` | `imsUserId` |

## `organization` champs

Ces champs se trouvent dans l’enregistrement d’organisation actif. La plupart des extensions ne requièrent que des `id`, des `name` et les identifiants .

| Champ | Type | Description |
| ------- | ------ | ------------- |
| `id` | chaîne | ID d’organisation de Fusion. |
| `name` | chaîne | Nom d’affichage de l’organisation |
| `externalOrgId` | chaîne | Identifiant de l’organisation Adobe IMS (même valeur que `imsOrgId`). |
| `externalId` | chaîne | Identifiant externe utilisé par les intégrations Fusion |
| `countryId` | chaîne | Identifiant du paramètre de pays. |
| `timezoneId` | chaîne | Identifiant du paramètre de fuseau horaire |
| `serviceName` | chaîne | Identifiant du service/plan |
| `teamIds` | chaîne[] | ID des équipes dans cette organisation |
| `license` | objet | Limites et droits du plan, tels que les opérations, le transfert de données, les places utilisateur et les indicateurs de fonctionnalité |
| `scenariosCount` | Nombre | Nombre total de scénarios dans l’organisation |
| `activeScenarios` | Nombre | Scénarios actuellement actifs |
| `activeApps` | Nombre | Nombre d&#39;applications ou de connexions actives |
| `operations`, `operationsExt` | Nombre | Compteurs d&#39;utilisation des opérations |
| `transfer`, `transferExt` | Nombre | Compteurs d’utilisation du transfert de données |
| `isPaused` | booléen | Si l’organisation est en pause |
| `isDeleted` | booléen | Si l’organisation est marquée comme supprimée |
| `imsEnabled` | booléen | Si l’organisation est liée à Adobe IMS |
| `usersCount` | Nombre | Nombre d’utilisateurs dans l’organisation |
| `nextReset` | chaîne (date) | La prochaine réinitialisation des compteurs d’utilisation. Voir [Dates](#dates) |

## `team` champs

Ces champs sont présents lorsqu’une équipe est active. Vous devez fournir une solution de secours au cas où l’équipe est `undefined` (par exemple, sur un écran au niveau de l’organisation sans équipe sélectionnée).

| Champ | Type | Description |
| ------- | ------ | ------------- |
| `id` | chaîne | Identifiant de l’équipe Fusion. |
| `name` | chaîne | Nom complet de l&#39;équipe. |
| `organizationId` | chaîne | ID de fusion de l’organisation à laquelle cette équipe appartient. |
| `country` | chaîne | Paramètre de pays de l’équipe. |
| `timezone` | chaîne | Fuseau horaire de l’équipe. |
| `license` | objet | Limites et droits au niveau de l’équipe. |
| `activeScenarios` | Nombre | Scénarios actifs dans l’équipe. |
| `activeApps` | Nombre | Applications ou connexions actives dans l&#39;équipe. |
| `scenarioDrafts` | booléen | Indique si les brouillons de scénario sont activés. |
| `isDeleted` | booléen | Indique si l&#39;équipe est marquée comme supprimée. |
| `created` | chaîne (date) | Lors de la création de l’équipe. Voir [Dates](#dates). |

## `user` champs

Ces champs s’appliquent à l’utilisateur Fusion connecté.

| Champ | Type | Description |
| ------- | ------ | ------------- |
| `id` | chaîne | ID d’utilisateur Fusion. |
| `name` | chaîne | Nom complet. |
| `email` | chaîne | Adresse électronique. |
| `avatar` | chaîne | URL de l’image de l’avatar. |
| `locale` | chaîne | Paramètres régionaux de l’utilisateur, tels que `en`. |
| `language` | chaîne | Langue préférée, si définie. |
| `timezone` | chaîne | Nom du fuseau horaire. |
| `timezoneId` | chaîne | Identifiant du paramètre de fuseau horaire. |
| `countryId` | chaîne | Identifiant du paramètre de pays. |
| `localeId` | chaîne | Identifiant du paramètre régional. |
| `features` | objet | Indicateurs de fonctionnalité par utilisateur (par exemple, `allow_apps`, `public_templates`). |
| `usersAdminsRoleId` | chaîne | ID du rôle d’administrateur de l’utilisateur, le cas échéant. |

>[!NOTE]
>
> L’objet `user` peut inclure des champs internes supplémentaires. Vous ne devez vous fier qu’aux champs documentés ici. D’autres champs peuvent être modifiés sans préavis et certains champs liés à l’authentification ne doivent jamais être consignés ni affichés.

## Dates

Le contexte est sérialisé avant d’atteindre votre extension. Par conséquent, **les champs de date arrivent sous forme de chaînes** (ISO 8601, tel que `"2026-06-24T00:00:00.000Z"`), et non d’objets de `Date` JavaScript. Vous pouvez les convertir si nécessaire :

```js
const resetDate = new Date(context.organization.nextReset);
```

## Mises à jour du contexte

Fusion renvoie l’ensemble du contexte (via `contextchange`) lorsque :

* l’utilisateur **change d’organisation**,
* l’utilisateur **change d’équipe** ou
* les informations de l&#39;utilisateur **connecté** changent.

Lisez toujours à nouveau toutes les clés que vous utilisez dans votre gestionnaire de `contextchange` plutôt que de supposer qu’une seule valeur a été modifiée.

## Bonnes pratiques en matière de sécurité

* **Ne jamais enregistrer, afficher ou conserver les `imsToken`.** Traitez-le comme un mot de passe.
* Envoyez le jeton uniquement aux points d’entrée Adobe/Fusion approuvés, via HTTPS, en tant que jeton `Bearer`.
* Ne stockez pas de données personnelles du contexte au-delà de ce dont votre fonctionnalité a besoin.

## Utiliser le jeton pour appeler les API

Pour transformer `imsToken` (plus `organization.id` / `team.id`) en Workfront réel ou
Les données de fusion, vous ne pouvez pas appeler ces API directement à partir du navigateur, car CORS bloque
c&#39;est ça. Acheminez plutôt l’appel via une petite action d’exécution App Builder. Voir
[Appel des API Workfront et Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md).


Pour continuer le processus de création d’une extension personnalisée, voir [Publier votre extension](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md).
