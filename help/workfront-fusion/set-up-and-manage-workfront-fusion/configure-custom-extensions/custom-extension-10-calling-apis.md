---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Appel des API Workfront et Fusion à partir de votre extension
description: Appel des API Workfront et Fusion à partir de votre extension
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: 925a8ee910434c474d527c2914897d7c42e4a3d1
workflow-type: tm+mt
source-wordcount: 1083
ht-degree: 0%

---


# Appel des API Workfront et Fusion à partir de votre extension

>[!NOTE]
>
>Cet article suppose que vous connaissez un peu les outils de développement logiciel.

La référence de contexte Fusion vous donne le jeton IMS de l’utilisateur connecté. L’étape suivante naturelle consiste donc à appeler les API Workfront ou Fusion et à afficher les données réelles. Ceci n’est pas possible en raison de la norme CORS. Cet article explique comment contourner cette limitation à l’aide d’une action d’exécution App Builder en tant que proxy côté serveur. Il comprend un exemple (le tableau de bord des abonnements aux événements).

## Pourquoi un appel direct au navigateur échoue (CORS)

Votre interface utilisateur visible s’exécute dans un `<iframe>` diffusé à partir du réseau CDN d’Adobe (`https://<your-app>.adobeio-static.net`). Lorsque cette page `fetch(...)` à une API Workfront ou Fusion d’une **origine différente**, le navigateur applique le partage de ressources entre origines multiples (CORS). À moins que l’API ne renvoie explicitement le `Access-Control-Allow-Origin` pour l’origine du réseau CDN, le navigateur bloque la réponse. Ces API ne placent sur la liste autorisée pas les origines d’extension arbitraires. Par conséquent, les appels directs depuis l’invité échouent.

Pour plus d’informations sur CORS, voir [CORS](https://developer.mozilla.org/docs/Web/HTTP/CORS).

## Appeler votre propre action d’exécution sans CORS

Le correctif pour cela est d’appeler votre propre action d’exécution sans CORS.

Les applications App Builder peuvent inclure des actions d’exécution, qui sont de petites fonctions sans serveur exécutées sur Adobe I/O Runtime côté serveur. Les appels serveur à serveur ne sont pas soumis à la norme CORS du navigateur. Et comme l’action fait partie de votre application, l’invité peut l’appeler avec une URL relative, qui est de même origine et donc non bloquée.

```
  Guest UI (browser, adobeio-static.net)
     │  fetch('/api/v1/web/<app>/wf-proxy?...')   ← relative = same-origin, no CORS
     ▼
  Your runtime action  (Adobe I/O Runtime, server-side)
     │  fetch('https://fusion.adobe.com/api/v3/...')  ← server-to-server, no CORS
     ▼
  Workfront / Fusion API
```

L’action reçoit le jeton IMS de l’utilisateur de l’invité et le transfère en amont, de sorte que les appels sont toujours effectués au nom de l’utilisateur avec ses autorisations.

## Étape 1 : déclarer l’action

Les actions d’exécution sont déclarées en `app.config.yaml` sous la `runtimeManifest` de l’extension. Ajoutez une action `wf-proxy` en regard de votre extension :

```yaml
extensions:
  fusion/nav-organization/1:
    $include: src/fusion-nav-organization-1/ext.config.yaml
    runtimeManifest:
      packages:
        fusion-uix-guest:                # ← your package name; part of the action URL
          license: Apache-2.0
          actions:
            wf-proxy:
              function: src/fusion-nav-organization-1/actions/wf-proxy/index.js
              web: 'yes'                  # exposes it at /api/v1/web/<package>/wf-proxy
              runtime: nodejs:22
              inputs:
                LOG_LEVEL: debug
              annotations:
                require-adobe-auth: false # see note below
                final: true
```

L’action devient accessible à l’adresse :

```
/api/v1/web/<package>/<action>     e.g.  /api/v1/web/fusion-uix-guest/wf-proxy
```

### `require-adobe-auth` : true ou false

Cette annotation contrôle si la passerelle Adobe valide un jeton IMS avant l’exécution de votre action.

* **`true`:** valeur par défaut sécurisée.  La passerelle rejette les appels non authentifiés. Cependant, le programme de validation détermine strictement les en-têtes attendus et peut rejeter les requêtes ou supprimer les en-têtes personnalisés dont votre appel en amont a besoin. Si cela se produit, il s’affiche sous la forme d’un `401`, même si votre jeton est valide.
* **`false`:** ignore la vérification de la passerelle. Votre action est alors invocable publiquement, vous **devez donc** appliquer l’autorisation vous-même. Demandez un porteur de `Authorization` dans l’action et rejetez-le s’il est manquant, puis transmettez-le en amont, où Workfront et Fusion le valident. Associé à une place sur la liste autorisée cible stricte, décrite à l’étape 2, il s’agit du chemin fiable pour un proxy qui doit transmettre des en-têtes personnalisés.

>[!TIP]
>
> `true` d&#39;abord. Si vous voyez une `401` que vous ne pouvez pas expliquer car le jeton est valide et fonctionne ailleurs, passez à `false` **et** vérifiez et la sécurité du porteur dans votre action afin que celle-ci soit toujours appliquée en amont.

## Étape 2 : écrire l’action pour un proxy

Créez des `src/fusion-nav-organization-1/actions/wf-proxy/index.js`. Deux règles assurent la sécurité : une liste autorisée des cibles en amont afin que l’action ne puisse pas être utilisée comme relais ouvert et un jeton porteur requis qui est transféré en amont.

```js
const fetch = require('node-fetch')
const { Core } = require('@adobe/aio-sdk')
const { errorResponse, getBearerToken, checkMissingRequestInputs } = require('../utils')

// Page-through query params (see "Paginate list results" below).
const pageQuery = (p) => {
  const q = new URLSearchParams()
  if (p.start != null) q.set('start', p.start)
  if (p.limit != null) q.set('limit', p.limit)
  return q
}

// Only these upstreams may be reached. Never build the URL from arbitrary input.
const TARGETS = {
  subscriptions: {
    method: 'GET',
    url: () => 'https://<your-wf-host>/attask/eventsubscription/api/v1/subscriptions',
  },
  hooks: {
    method: 'GET',
    // Fusion hooks are team-scoped: teamId is a REQUIRED query param (see below).
    url: (p) => {
      const q = pageQuery(p)
      if (p.teamId) q.set('teamId', p.teamId)
      return `https://fusion.adobe.com/api/v3/hooks?${q.toString()}`
    },
  },
  scenarios: {
    method: 'GET',
    url: (p) => {
      const q = pageQuery(p)
      if (p.fusionOrgId) q.set('organizationId', p.fusionOrgId)
      return `https://fusion.adobe.com/api/v3/scenarios?${q.toString()}`
    },
  },
}

async function main (params) {
  const logger = Core.Logger('main', { level: params.LOG_LEVEL || 'info' })
  try {
    const missing = checkMissingRequestInputs(params, ['target'], ['Authorization'])
    if (missing) return errorResponse(400, missing, logger)

    const target = TARGETS[params.target]
    if (!target) return errorResponse(400, `unknown target '${params.target}'`, logger)

    const token = getBearerToken(params)              // reads params.__ow_headers.authorization
    const headers = { authorization: `Bearer ${token}`, 'content-type': 'application/json' }
    if (params.orgId) headers['x-gw-ims-org-id'] = params.orgId        // Adobe IMS org id
    if (params.fusionOrgId) headers['x-organization-id'] = params.fusionOrgId  // Fusion tenant id
    if (params.teamId) headers['x-team-id'] = params.teamId            // Fusion team id

    const res = await fetch(target.url(params), { method: target.method, headers })
    const text = await res.text()
    let body
    try { body = JSON.parse(text) } catch (e) { body = text }

    if (!res.ok) {
      return { statusCode: res.status, body: { error: `upstream ${res.status}`, target: params.target, details: body } }
    }
    return { statusCode: 200, body }
  } catch (error) {
    logger.error(error)
    return errorResponse(500, 'server error: ' + error.message, logger)
  }
}

exports.main = main
```

`getBearerToken`, `errorResponse` et `checkMissingRequestInputs` proviennent des `actions/utils.js` générés, où le modèle les utilise comme modèles automatiques. `getBearerToken` lit `params.__ow_headers.authorization`, où la passerelle place l’en-tête `Authorization` entrant.

## Étape 3 : appeler l’action de l’invité

Dans l’interface utilisateur, `fetch` l’action avec une URL relative (même origine) et envoyez le jeton IMS en tant que porteur. Transmettez les identifiants d’organisation et d’équipe dont les éléments en amont ont besoin en tant que paramètres de requête.

```js
const PROXY_URL = "/api/v1/web/fusion-uix-guest/wf-proxy";

async function callProxy(target, token, { imsOrgId, fusionOrgId, teamId, start, limit } = {}) {
  const params = new URLSearchParams({ target });
  if (imsOrgId) params.set("orgId", imsOrgId);          // → x-gw-ims-org-id
  if (fusionOrgId) params.set("fusionOrgId", fusionOrgId); // → x-organization-id
  if (teamId) params.set("teamId", teamId);             // → x-team-id
  if (start != null) params.set("start", start);        // pagination offset
  if (limit != null) params.set("limit", limit);        // pagination page size
  const res = await fetch(`${PROXY_URL}?${params.toString()}`, {
    headers: { authorization: `Bearer ${token}` },
  });
  if (!res.ok) throw new Error(`${target} request failed: ${res.status}`);
  return res.json();
}
```

Tirez `token`, `imsOrgId`, `fusionOrgId` et `teamId` du contexte :

```js
const token       = connection.sharedContext.get("imsToken");
const imsOrgId    = connection.sharedContext.get("imsOrgId");
const fusionOrgId = connection.sharedContext.get("organization")?.id; // Fusion tenant id
const teamId      = connection.sharedContext.get("team")?.id;
```

Pour plus d’informations sur le contexte, voir [Référence du contexte de Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md).

## Spécificités de l’API Fusion v3

Ce qui a fonctionné pour le tableau de bord par rapport à `https://fusion.adobe.com/api/v3` :

| En-tête / paramètre | Valeur | Notes |
| ---------------- | ------- | ------- |
| `Authorization` | `Bearer <imsToken>` | Jeton IMS de l’utilisateur du contexte. |
| `x-organization-id` | `organization.id` | Identifiant du client Fusion et non de l’organisation IMS. Fusion identifie le client par ce biais. |
| `x-team-id` | `team.id` | Envoyer lorsque l’appel est de portée équipe. |
| `x-gw-ims-org-id` | `imsOrgId` | Identifiant de l’organisation Adobe IMS, pour la passerelle. |

Notez les avertissements suivants :

* **`GET /api/v3/hooks`a une portée d’équipe :** `teamId` est un **paramètre de requête obligatoire** (`/api/v3/hooks?teamId=...`). Sans cela, on obtient un `400`. Cela signifie que les hooks reviennent pour l’*équipe active uniquement* ; pour couvrir une organisation, boucler les équipes et fusionner.
* **`GET /api/v3/scenarios`** fonctionne avec `organizationId` (`/api/v3/scenarios?organizationId=...`).

>[!NOTE]
>
> La référence officielle est Adobe [API Workfront Fusion](https://developer.adobe.com/workfront-fusion-apis/). Les exigences d’en-tête/authentification varient selon la passerelle. Ce tableau reflète les besoins réels de la démonstration. Si un appel renvoie `401`/`400`, revérifiez d’abord ces en-têtes.

## Paginer les résultats de la liste

Les points d’entrée de liste Fusion v3 (hooks, scénarios) renvoient une **page** à la fois, et non l’ensemble. Une réponse ressemble à ceci :

```json
{
  "items": [ /* ...this page of records... */ ],
  "_page": { "start": 0, "limit": 100, "total": 342 }
}
```

Les enregistrements sont sous **`items`** et les métadonnées de pagination sont sous **`_page`**. La page contient les paramètres de requête **`start`** (décalage) et **`limit`** (taille de la page). Le proxy ci-dessus passe par les deux. Vous devez donc paginer dans l’invité en bouclant jusqu’à ce que vous ayez tout collecté :

```js
const PAGE_LIMIT = 100;

async function fetchAllPages(target, token, opts = {}) {
  const all = [];
  let start = 0;
  // Stop when a page returns fewer than PAGE_LIMIT items, or when _page.total is reached.
  for (;;) {
    const res = await callProxy(target, token, { ...opts, start, limit: PAGE_LIMIT });
    const items = res.items ?? [];
    all.push(...items);

    const total = res._page?.total;
    const done = items.length < PAGE_LIMIT || (total != null && all.length >= total);
    if (done) break;
    start += PAGE_LIMIT;
  }
  return all;
}
```

Si vous préférez conserver la pagination en dehors du navigateur, effectuez la même boucle dans l’action d’exécution et renvoyez le tableau de `items` fusionné dans une seule réponse. Dans les deux cas, ne supposez pas que la première page correspond à l’ensemble des résultats. Une équipe comportant plusieurs pages de points d’extension ressemblerait à des scénarios manquants.

## Liste de contrôle de sécurité

* **Placer sur la liste autorisée en amont.** Ne construisez jamais l’URL cible à partir d’une entrée client brute. Mappez une clé `target` courte à une URL fixe, comme à l’étape 2. Cela empêche votre action de devenir un relais ouvert.
* **Exiger le jeton porteur** dans l’action et le transférer en amont. Laissez Workfront et Fusion appliquer les autorisations de l’utilisateur.
* **Ne jamais enregistrer le jeton.** `imsToken` s’agit d’informations d’identification. Gardez `LOG_LEVEL` à l&#39;esprit ce que `stringParameters` imprime.
* **Transférer uniquement via HTTPS** aux hôtes Adobe et Workfront approuvés.

## Exemple travaillé : le tableau de bord des abonnements aux événements

Le tableau de bord de démonstration associe trois sources pour montrer, par abonnement à un événement Workfront, si un scénario Fusion correspondant est sain :

1. `fetchSubscriptions()` → abonnements aux événements Workfront (avec les compteurs reçus/transmis).
1. `fetchHooks(teamId)` → hooks Fusion pour l’équipe active (paginée avec `fetchAllPages`).
1. `fetchScenarios(fusionOrgId)` → Scénarios Fusion pour l’organisation (paginé avec `fetchAllPages`).

Le **join** les enchaîne, mais il y a un hic à signaler : un abonnement Workfront et le hook Fusion qu&#39;il pointe en direct sur **différents hôtes**, donc leurs champs d&#39;URL ne sont pas égaux octet pour octet. Ce qui est stable est le **jeton à la fin de l’URL du webhook** (le dernier segment de chemin d’accès). Correspond à ce jeton de fin, et non à l’URL complète. Le `scenarioId` du hook correspond ensuite au `id` d’un scénario :

```
subscription.targetUrl  ──(trailing token)──▶  hook.url
                                                hook.scenarioId  ──▶  scenario.id
```

```js
// Reduce a webhook URL to its trailing token so hosts/bases can differ.
function hookKey(url) {
  if (!url) return "";
  const path = String(url).trim().toLowerCase().split(/[?#]/)[0].replace(/\/+$/, "");
  const i = path.lastIndexOf("/");
  return i >= 0 ? path.slice(i + 1) : path;
}

// Index hooks by token, then look each subscription up by the same token.
const hooksByToken = new Map(hooks.map((h) => [hookKey(pick(h, ["url", "address", "targetUrl"], "")), h]));
const hook = hooksByToken.get(hookKey(pick(sub, ["url", "endpointUrl", "targetUrl", "target.url", "callbackUrl"], "")));
```

Le statut est dérivé de la jointure :

* **Cassé** : aucun crochet correspondant ou le crochet est `gone`.
* **Filtrage** : apparié, mais `passed < received` (les événements arrivent mais sont filtrés avant l’exécution du scénario).
* **Sain** : apparié et réussi.

Comme les formes réelles de payload varient, le client mappe les champs de manière défensive, en essayant plusieurs clés candidates par champ, de sorte qu’une différence d’API mineure ne rompt pas la table :

```js
function pick(obj, keys, fallback) {
  for (const key of keys) {
    const value = key.split(".").reduce((acc, part) => (acc == null ? acc : acc[part]), obj);
    if (value != null) return value;
  }
  return fallback;
}
```

Ce n&#39;est qu&#39;un exemple parmi d&#39;autres. Le même modèle de proxy fonctionne pour toute API Workfront ou Fusion dont vous avez besoin.
