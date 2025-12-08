---
title: Glossaire d’Adobe Workfront Fusion
description: Le glossaire suivant explique certains termes courants d’Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 7f098ec2-8594-4e5d-9ce7-d1738a05f9a6
source-git-commit: 190bfe5992fb21b789a7246c4ae732a5dc7672fa
workflow-type: ht
source-wordcount: '924'
ht-degree: 100%

---

# Glossaire d’Adobe Workfront Fusion

Le glossaire suivant explique certains termes courants d’Adobe Workfront Fusion.


<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>Action</p> </td> 
   <td>Un module qui vous permet d’effectuer une action, comme lire ou écrire des données depuis ou dans une application ou un service sélectionné.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Agrégateur</p> </td> 
   <td> <p>Type de module qui fusionne plusieurs lots (plusieurs collections de données) en un seul lot. </p><p>Pour plus d’informations, consultez <a href="/help/workfront-fusion/references/modules/aggregator-module.md" class="MCXref xref">Module agrégateur</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API</td> 
   <td>Les interfaces de programmation d’applications (API) permettent aux applications et aux services de communiquer entre eux. Fusion utilise des API pour communiquer avec l’application à laquelle vous vous connectez. Chaque application dispose d’une API distincte. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Clé API</td> 
   <td>Code unique qui identifie l’utilisateur ou l’utilisatrice, la personne chargée du développement ou le programme qui appelle l’API d’un logiciel, utilisée pour l’authentification. Comme les modules de Fusion fonctionnent en connectant des API, des clés API sont parfois nécessaires. Les clés API sont distribuées par l’application qui en a besoin. Par exemple, si vous avez besoin d’une clé API pour connecter Fusion à Adobe Lightroom, vous pouvez la demander via votre compte Adobe Lightroom.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Application ou service</td> 
   <td> <p>Une application logicielle. Fusion peut se connecter à la plupart des applications, même s’il ne dispose pas d’un connecteur dédié pour telle ou telle application.</p> <p>Une application peut également être une fonction spéciale qui manipule des données, comme un itérateur ou un agrégateur. </p> <p>Un service est une source de données qui peut inclure une API web, une page web, différents types de serveurs (FTP, SMTP, IMAP), etc. </p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Lot</p> </td> 
   <td> <p>Un lot est une unité de données de base qui est renvoyée ou reçue par les modules. Par exemple, un module de recherche qui renvoie trois enregistrements génère trois lots de données, un pour chaque enregistrement. Un lot se compose de plusieurs éléments.</p> </td> 
  </tr> 
  <tr>
   <td role="rowheader"> <p>Connexion</p> </td> 
   <td> <p>Une connexion représente un ensemble d’informations d’identification permettant de se connecter à un service donné. Vous pouvez configurer des connexions à l’intérieur de n’importe quel module, puis utiliser cette connexion dans tout autre module. Une connexion doit être sélectionnée pour chaque module, de sorte que Fusion puisse utiliser ces informations d’identification pour accéder aux informations dont le module a besoin. </p><p>Pour plus d’informations, consultez la section <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md" class="MCXref xref">Vue d’ensemble des connexions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Connecteur</td> 
   <td>Un connecteur correspond à l’ensemble des modules d’une application donnée. Workfront Fusion propose des connecteurs vers de nombreuses applications de travail courantes, telles que Workfront, Salesforce et Jira.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Cycle</p> </td> 
   <td> <p>Un cycle fait référence à deux phases du déroulement d’un scénario : l’opération et la validation. Le scénario peut consister en un ou plusieurs cycles. Pour obtenir des informations plus détaillées, consultez <a href="/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md" class="MCXref xref">Exécution, cycles et phases de scénarios</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Entrepôt de données</p> </td> 
   <td> <p>Outil qui stocke les données des scénarios ou qui vous permet de transférer des données entre des scénarios individuels ou des séries de scénarios. </p><p>Pour plus d’informations, consultez <a href="/help/workfront-fusion/create-scenarios/map-data/data-stores.md" class="MCXref xref">Entrepôts de données</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Filtre</p> </td> 
   <td> <p> Un filtre peut être appliqué entre deux modules et permet de ne travailler qu’avec des lots répondant à certains critères. Il existe un certain nombre de filtres différents que vous pouvez appliquer. </p><p>Pour plus d’informations, consultez <a href="/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md" class="MCXref xref">Ajouter un filtre à un scénario</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID </p> </td> 
   <td> <p>Nom utilisé pour identifier de manière unique un lot. Un ID est généralement utilisé pour différencier un lot qui doit être mis à jour ou supprimé d’un service donné. Les ID peuvent être mappés à partir de la sortie d’un module précédent.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Éléments</p> </td> 
   <td> <p>Partie d’un lot. Les lots peuvent être composés de plusieurs éléments. Il existe plusieurs types d’éléments : texte, nombre, booléen (oui/non), date, heure, buffer (données binaires), collections, menu de sélection, tableau et validation.</p><p> Pour plus d’informations, consultez <a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">Types de données d’élément</a>.</p> </td> 
  </tr>
  <tr> 
   <td role="rowheader"> <p>Itérateur</p> </td> 
   <td> <p>Type de module qui vous permet de prendre un lot de données (une collection de données) et de le diviser en lots distincts. Ces lots peuvent ensuite être traités individuellement par des modules ultérieurs. </p><p>Pour plus d’informations, consultez <a href="/help/workfront-fusion/references/modules/iterator-module.md" class="MCXref xref">le module [!UICONTROL Iterator]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Module</p> </td> 
   <td> <p>Étape unique dans un scénario qui exécute une fonction, telle que la création d’un enregistrement, dans l’application associée ou le service associé.</p> <p>Chaque application ou service possède différents modules qui définissent la manière sa manière de répondre à une requête.</p>  <p> <img src="assets/module.png"> </p> <p>Pour plus d’informations, consultez <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md" class="MCXref xref">Vue d’ensemble des modules</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Opération</p> </td> 
   <td> <p>Tâche effectuée par un module, comme la récupération d’un enregistrement ou le chargement d’un fichier.</p><p>Pour plus d’informations, consultez <a href="/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/operations-in-workfront-fusion.md" class="MCXref xref">Opérations</a>.</p>
  </tr> 
  <tr> 
   <td role="rowheader">Clés publiques/privées</td> 
   <td>Les clés publiques et privées sont utilisées pour chiffrer et déchiffrer les données. La clé publique peut être distribuée, et toute personne la possédant peut chiffrer des données, mais seule la clé privée peut les déchiffrer. De même, un utilisateur ou une utilisatrice disposant d’une clé privée peut chiffrer des données que toute personne disposant de la clé publique peut déchiffrer. Le chiffrage de la clé privée garantit que les données proviennent de la personne qui la possède et sert de validation de la source des données.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Routeur</p> </td> 
   <td>Un routeur permet de dupliquer des données ou d’ajouter de nouveaux itinéraires à un scénario, afin de réacheminer les données et de traiter séparément différents groupes de données.</p><p> Pour plus d’informations, consultez <a href="/help/workfront-fusion/create-scenarios/add-modules/router-module.md" class="MCXref xref">le module [!UICONTROL Router]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Scénario</p> </td> 
   <td> <p>Série d’étapes automatisées créées par l’utilisateur ou par l’utilisatrice, chacune représentée et exécutée par un module. L’objectif d’un scénario est de déplacer et de manipuler des données.</p> <p> <img src="assets/entire-scenario-blank.png" style="width: 350;height: 178;"> </p> <p> Pour plus d’informations, consultez <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/scenario-overview.md" class="MCXref xref">Vue d’ensemble des scénarios</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Segment de scénario</p> </td> 
   <td> <p> Un segment de scénario est une section d’un scénario composée d’une série de modules qui se connectent tous à la même application. Les segments de scénario représentent souvent un workflow court dans l’application.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Déclencheur</p> </td> 
   <td> <p>Un déclencheur est un type de module qui surveille les données nouvelles et mises à jour et qui lance le scénario lorsque certaines conditions configurées dans le module s’appliquent. Les déclencheurs peuvent être configurés pour lancer un scénario selon un planning (interrogation) ou chaque fois que des modifications de données se produisent (déclencheur instantané ou webhook).</p> <p>Pour plus d’informations, consultez <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md" class="MCXref xref">Déclencheurs</a> dans l’article Vue d’ensemble des modules.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Webhook</p> </td> 
   <td> <p>Type spécial de déclencheur qui vous permet d’exécuter un scénario immédiatement après la mise à disposition d’un nouveau lot. </p><p>Pour plus d’informations, consultez <a href="/help/workfront-fusion/references/modules/webhooks-reference.md" class="MCXref xref">Déclencheurs instantanés (webhooks)</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>
