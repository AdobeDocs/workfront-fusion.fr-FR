---
content-type: reference
title: Types d’erreur
description: Il arrive qu’une erreur se produise pendant l’exécution d’un scénario. Cela se produit généralement lorsqu’un service n’est pas disponible en raison d’un échec de connexion à un service ou d’un échec de validation. Cet article traite des erreurs courantes que vous pouvez rencontrer.
author: Becky
feature: Workfront Fusion
exl-id: abf5f844-d13b-416e-a8b8-2d4ee1786262
source-git-commit: a871a130a1ac023dcb4ce8da7241918da2431d3a
workflow-type: tm+mt
source-wordcount: '1211'
ht-degree: 35%

---

# Types d’erreur

Il arrive qu’une erreur se produise pendant l’exécution d’un scénario. Cela se produit généralement si un service n’est pas disponible en raison d’un échec de connexion au service ou si une validation échoue.

Adobe Workfront Fusion fait la distinction entre plusieurs types d’erreur de base. Le type d’erreur détermine les actions suivantes de votre scénario Fusion.

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tout package de workflow Adobe Workfront et tout package d’automatisation et d’intégration Adobe Workfront</p><p>Workfront Ultimate</p><p>Packages Workfront Prime et Select, avec l’achat supplémentaire de Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licences Adobe Workfront</td> 
   <td> <p>Standard</p><p>Travail ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Si votre organisation dispose d’un package Workfront Select ou Prime qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acquérir Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Erreur de connexion

`ConnectionError`

Les erreurs de connexion sont l’une des erreurs les plus courantes. Elles sont généralement dues à l’indisponibilité du service tiers pour diverses raisons, telles que la surcharge, la maintenance ou la panne. La gestion par défaut de cette erreur dépend du module qui a rencontré l’erreur.

* Si l’erreur se produit dans le premier module, l’exécution du scénario est interrompue par un message d’avertissement. Workfront Fusion tente ensuite à plusieurs reprises de réexécuter le scénario à des intervalles de temps croissants. Si toutes les tentatives échouent, Workfront Fusion désactive le scénario.
* Si l&#39;erreur de connexion se produit sur un autre module que le premier, les étapes suivantes dépendent de l&#39;option Autoriser le stockage des exécutions incomplètes dans les paramètres avancés du scénario :

   * Si cette option est activée, l’exécution du scénario est déplacée vers le dossier [!UICONTROL Exécutions incomplètes] dans lequel Workfront Fusion tente à plusieurs reprises de réexécuter le scénario à des intervalles de temps croissants. Si toutes les tentatives échouent, l’exécution restera dans le dossier des exécutions incomplètes en attendant une résolution manuelle par la personne.

     Pour plus d’informations sur les exécutions incomplètes, voir [Afficher et résoudre les exécutions incomplètes](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).
   * Si cette option est désactivée, l’exécution du scénario se termine par une erreur suivie d’une phase de restauration. Workfront Fusion tente ensuite à plusieurs reprises de réexécuter le scénario à des intervalles de temps croissants. Si toutes les tentatives échouent, Workfront Fusion désactive le scénario.

  Pour plus d’informations sur le paramètre Autoriser le stockage des exécutions incomplètes, voir [Autoriser le stockage des exécutions incomplètes](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow-storing-incomplete-executions) dans l’article Configuration des paramètres de scénario.

### Intervalles de temps de plus en plus longs

L’algorithme utilisé pour augmenter les intervalles de temps entre les tentatives lorsqu’une erreur se produit est connu sous le nom d’exponential backoff. Les intervalles de temps de plus en plus longs sont définis comme suit :

1. 10 minutes
1. 1 heure
1. 3 heures
1. 12 heures
1. 24 heures

Les intervalles de temps croissants permettent d’empêcher les scénarios fréquemment exécutés d’utiliser des opérations sur des tentatives ayant échoué à plusieurs reprises.

>[!BEGINSHADEBOX]

**Exemple :**

Un scénario contient le déclencheur [!DNL Google Sheets] [!UICONTROL Surveiller des lignes]. [!DNL Google Sheets] n’est pas disponible pendant 30 minutes en raison d’opérations de maintenance au démarrage du scénario par Workfront Fusion. Il est donc impossible de récupérer de nouvelles lignes. Le scénario s’arrête et tente un nouvel essai 10 minutes après. Comme [!DNL Google Sheets] n’est toujours pas disponible, Workfront Fusion ne parvient toujours pas à obtenir d’informations sur les nouvelles lignes. La prochaine exécution du scénario est prévue dans 1 heure. [!DNL Google Sheets] est à nouveau disponible à ce moment-là, et le scénario s’exécute avec succès.

>[!ENDSHADEBOX]

## Erreur de données

`DataError`

Une erreur de données est générée lorsqu’un élément est incorrectement mappé et ne réussit pas la validation effectuée du côté de Workfront Fusion ou du côté du service tiers.

Si cette erreur se produit, le scénario, jusqu’à l’emplacement où le module a échoué, est déplacé vers le dossier des exécutions incomplètes, où vous pouvez résoudre le problème. Cependant, le scénario ne s’arrête pas et continue de s’exécuter selon son planning. Pour arrêter l’exécution du scénario lorsque Erreur de données apparaît, activez l’option Traitement séquentiel dans le panneau des paramètres du scénario.

Si vous n’avez pas activé l’option [!UICONTROL Autoriser le stockage des exécutions incomplètes] dans les paramètres du scénario, l’exécution du scénario s’arrête avec l’erreur et une restauration est effectuée.

## Erreur de données dupliquées

`DuplicateDataError`

Si Workfront Fusion tente d’insérer deux fois le même lot dans un service qui n’autorise pas les données en double, une erreur de données en double est générée. Si cette erreur se produit, Workfront Fusion procède de la même manière que pour l’erreur de données.

Pour plus d’informations, voir [Erreur de données](#data-error) dans cet article.


## Erreur de jeton d’accès invalide

`InvalidAccessTokenError`

Une erreur de jeton d’accès non valide se produit lorsque Workfront Fusion ne peut pas accéder à votre compte enregistré auprès d’un service tiers. Cela se produit généralement lorsque vous révoquez les droits d’accès de Workfront Fusion dans l’administration d’un service donné, mais les scénarios qui utilisent ce service continuent de s’exécuter selon le planning.

Si cette erreur se produit, l’exécution du scénario s’arrête immédiatement. Le reste du scénario commençant par le module dans lequel l’erreur s’est produite est déplacé vers le dossier des exécutions incomplètes.

## Erreur de limite de taux

`RateLimitError`

Si une limite fixée par un service donné est dépassée, une erreur de limite de taux est générée. Si cette erreur se produit, Workfront Fusion procède de la même manière que pour l’erreur de connexion.

Pour plus d’informations, voir [Erreur de connexion](#connection-error) dans cet article.

## Erreur de données incomplètes

`IncompleteDataError`

Une erreur de données incomplètes ne se produit qu’avec des déclencheurs. Cette erreur est générée si un déclencheur ne parvient pas à télécharger les données requises à partir d’un service donné.

Si un scénario se termine par l’erreur `IncompleteDataError`, son comportement ultérieur dépendra du paramètre [!UICONTROL Nombre maximal d’erreurs consécutives].

Pour plus d’informations, voir [Nombre d’erreurs consécutives](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#number-of-consecutive-errors) dans l’article Configuration des paramètres de scénario.

>[!BEGINSHADEBOX]

**Exemple :**

Le déclencheur Workfront [!UICONTROL Enregistrement de contrôle] est défini pour surveiller les documents d’un scénario. Le scénario s’exécute pendant que vous téléchargez un document volumineux, tel qu’une longue vidéo. Étant donné que [!UICONTROL Workfront Fusion] tente de télécharger la vidéo alors qu’elle est encore en cours de chargement sur Workfront, le scénario se termine par l’erreur `IncompleteDataError`.

>[!ENDSHADEBOX]

## Erreur d’exécution

`RuntimeError`

Toute erreur qui apparaît lors de l’exécution du scénario et qui ne fait pas partie de ces types d’erreur est signalée comme `RunTimeError`.

Si un scénario se termine par le `RuntimeError`, son comportement ultérieur dépend du paramètre [!UICONTROL Nombre maximal d’erreurs consécutives].

Pour plus d’informations, voir [Nombre d’erreurs consécutives](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#number-of-consecutive-errors) dans l’article Configuration des paramètres de scénario.


>[!NOTE]
>
>Si un scénario commence par un déclencheur instantané et rencontre cette erreur, le paramètre [!UICONTROL Nombre maximal d’erreurs consécutives] est ignoré et le scénario est immédiatement désactivé.
>Pour plus d’informations, voir [Déclencheurs instantanés](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#instant-triggers) dans l’article Présentation des modules.

## Erreur d’incohérence

`InconsistencyError`

Si l’une de ces erreurs se produit pendant la phase de validation ou de restauration, le scénario se termine par une erreur d’incohérence.

Si cette erreur apparaît dans un scénario, l’exécution de celui-ci est immédiatement interrompue.

## Avertissement

Lors de l’exécution d’un scénario, vous pouvez recevoir un avertissement vous informant d’un problème. Un avertissement n’empêche pas la réussite du scénario.

Par exemple, un avertissement peut s’afficher lorsque la taille de fichier maximale autorisée est dépassée et que l’option [!UICONTROL Activer la perte de données] est désactivée.

## Ressources

Pour plus d’informations sur le mappage, voir [Présentation du mappage](/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md).

Pour plus d’informations sur les exécutions incomplètes, voir [Afficher et résoudre les exécutions incomplètes](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md).

Pour plus d’informations sur le panneau des paramètres du scénario, voir [Configurer les paramètres du scénario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md).

Pour plus d’informations sur les planifications, voir [Planification d’un scénario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

Pour plus d’informations sur les phases du scénario, voir [Exécution du scénario, cycles et phases](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).

Pour plus d’informations sur l’option Activer la perte de données , voir [Activer la perte de données](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#enable-data-loss) dans l’article Configuration des paramètres de scénario.
