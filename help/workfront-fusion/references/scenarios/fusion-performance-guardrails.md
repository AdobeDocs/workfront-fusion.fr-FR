---
title: Mécanismes de sécurisation des performances de Fusion
description: L’automatisation du travail exige un traitement rapide, c’est pourquoi Adobe Workfront Fusion est conçu pour des performances élevées. Comme les scénarios de longue durée peuvent ralentir le rythme de votre travail, Workfront Fusion a été conçu avec des mécanismes de sécurisation permettant de préserver les performances, pour limiter le temps d’exécution, la taille des données et d’autres paramètres du scénario. Les équipes de conception Workfront Fusion doivent connaître ces mécanismes de sécurisation et les intégrer dans leurs pratiques de conception.
author: Becky
feature: Workfront Fusion
exl-id: d142a521-edbc-4d7b-b5cd-872a9d3d2e1c
source-git-commit: 441b192d50e928ce74e54d8bcc0d89f4af348bb5
workflow-type: tm+mt
source-wordcount: '1072'
ht-degree: 96%

---

# Mécanismes de sécurisation des performances de Fusion

L’automatisation du travail exige un traitement rapide, c’est pourquoi Adobe Workfront Fusion est conçu pour des performances élevées. Comme les scénarios de longue durée peuvent ralentir le rythme de votre travail, Workfront Fusion a été conçu avec des mécanismes de sécurisation permettant de préserver les performances, pour limiter le temps d’exécution, la taille des données et d’autres paramètres du scénario. Les équipes de conception Workfront Fusion doivent connaître ces mécanismes de sécurisation et les intégrer dans leurs pratiques de conception.

## Navigateurs

* Workfront Fusion ne prend en charge que les navigateurs Chrome.

## Scénarios

* Le délai d’expiration par défaut pour l’exécution d’un scénario est de **40 minutes**. Une fois ce délai dépassé, Workfront Fusion interrompt l’exécution du scénario après le cycle suivant ou l’opération suivante, selon le scénario. Cela force l’arrêt du scénario peu après l’atteinte de la limite de 40 minutes.

  Le chaîne de scénarios n’est pas comptabilisée dans le délai d’exécution d’un scénario. Un scénario parent n’accumule pas de temps pendant l’attente de l’exécution d’un scénario enfant.
* La taille maximale d’un plan directeur de scénario est de **5 Mo**, mais nous recommandons de ne pas dépasser **3 Mo** pour la taille du scénario.

  Les modules d’application qui créent ou mettent à jour des données avec un grand nombre de champs peuvent générer des plans directeurs très volumineux.

   * Lors de l’utilisation de l’application Workfront, veillez à sélectionner uniquement les champs nécessaires à vos cas d’utilisation de création ou de mise à jour.
   * Lors de l’utilisation d’autres applications, utilisez des modules API personnalisés pour interagir avec n’importe quel type d’enregistrement comportant un grand nombre de champs.

* Bien qu’il n’y ait pas de limite pour le nombre de modules dans un scénario, les scénarios comportant plus de 150 modules ont une incidence négative sur les performances de votre système Workfront Fusion. Pour cette raison, il est déconseillé de créer des scénarios comportant plus de 150 modules.

## Opérations

* Le délai d’expiration par défaut d’une opération est généralement de **40 secondes**.

<!--
* The operation timeout for calls to Adobe Workfront is **120 seconds**.
-->

## Fichiers

* La capacité totale de traitement des fichiers de Fusion est de **1 Go**. La limite est basée sur un coût total en mémoire. Chaque opération contribue à ce coût. Si un seul fichier de 400 Mo est téléchargé et chargé, le coût total de capacité du fichier sera de 800 Mo.
* Les organisations qui souscrivent à l’offre Workfront Ultimate ont accès à un traitement des fichiers plus important, dépassant 1 Go. Cependant, d’autres facteurs affectent le transfert de données. Le service auquel Fusion se connecte peut limiter la taille des fichiers, ce qui affecte tous les fichiers traités par ce service. De plus, les fichiers volumineux peuvent affecter le temps d’exécution du scénario. Fusion traite les fichiers jusqu’à ce que la limite d’exécution de 40 minutes soit atteinte, auquel cas l’exécution échoue.
* Si un fichier est téléchargé à l’aide d’un module qui prend en charge les fichiers volumineux puis transmis à un module qui ne prend pas en charge les fichiers volumineux, ce module ne traite pas le fichier avec succès. Les fichiers volumineux doivent être gérés exclusivement avec des modules pris en charge dans l’ensemble du workflow.
* Les modules qui ne prennent pas en charge les fichiers volumineux peuvent traiter des fichiers d’une taille maximale de **200 Mo**.

Pour plus d’informations, consultez [Utiliser des fichiers volumineux](/help/workfront-fusion/references/scenarios/fusion-large-files.md).

## Utilisation de la mémoire du serveur

* L’utilisation de la mémoire du serveur pour une seule exécution est limitée à **1 Go**.

  De nombreux facteurs, tels que les fichiers volumineux ou les modules complexes, peuvent affecter l’utilisation de la mémoire du serveur d’une manière difficile à prédire ou à contrôler. Pour cette raison, l’exécution de votre scénario peut dépasser la limite de mémoire de 1 Go, même si le scénario suit tous les autres mécanismes de sécurisation des performances. Le dépassement de la limite de mémoire entraîne l’échec de l’exécution.

## Webhooks

* La taille maximale par défaut d’un payload est de **5 Mo**.
* Les webhooks sont limités à **100 demandes par seconde**. Lorsque cette limite est atteinte, Workfront Fusion envoie un statut 429 ([!UICONTROL Trop de demandes]).
* Workfront Fusion stocke les payloads de webhook pendant 30 jours. L’accès à un payload de webhook plus de 30 jours après sa réception entraîne l’erreur « [!UICONTROL Échec de la lecture du fichier à partir de l’enregistrement.] »
* Les webhooks sont désactivés automatiquement si l’une des conditions suivantes s’applique :

   * Le webhook n’a été connecté à aucun scénario depuis plus de 5 jours.
   * Le webhook est utilisé uniquement dans les scénarios inactifs, qui sont inactifs depuis plus de 30 jours.

* Les webhooks désactivés sont supprimés et désinscrits automatiquement s’ils ne sont connectés à aucun scénario et s’ils sont restés désactivés pendant plus de 30 jours.
* Le délai d’expiration d’une réponse webhook est de 5 minutes.

## Historique de l’exécution

* Les journaux d’historique d’exécution sont limités à une taille de **100 Mo**. Si l’historique d’exécution dépasse cette taille, seuls les 100 premiers Mo s’affichent.
* Si un scénario comporte plusieurs exécutions simultanées, seules 5 exécutions s’affichent dans la zone Exécutions de la page des détails du scénario. Cela est vrai même lorsque plus de 5 exécutions sont en cours d’exécution.

## Exécutions incomplètes

* Les exécutions incomplètes sont limitées à une taille totale de **11 Go** ou **100 exécutions incomplètes** par scénario, selon la limite atteinte en premier. Si une limite est atteinte, aucune autre exécution incomplète ne sera stockée pour ce scénario.
* Workfront Fusion autorise jusqu’à 5 échecs par minute.

## Reprises

* Lors de l’utilisation du module Break et de la spécification de la directive Réessayer, si un scénario échoue consécutivement 10 fois dans un délai de 2 minutes, le scénario est automatiquement désactivé.

## Récursion

La récursion se produit lorsqu’un scénario déclenche une nouvelle exécution de lui-même, ce qui déclenche une nouvelle exécution, et ainsi de suite dans une boucle infinie.

Par exemple, un scénario est déclenché lorsqu’une tâche est créée et que ce scénario crée deux tâches. Les deux nouvelles tâches déclenchent à nouveau le scénario, ce qui crée quatre nouvelles tâches. Chaque fois qu’une tâche est créée, le scénario est déclenché, et chaque fois qu’il s’exécute, le nombre de tâches double. Le nombre de tâches augmente de manière exponentielle.

La récursion peut entraîner des problèmes de performances à la fois pour l’organisation propriétaire du scénario récursif et pour d’autres organisations.

Tenez compte des points suivants concernant la récursion :

* **Lorsqu’un scénario entraîne une récursion, il est désactivé par l’équipe d’ingénierie de Fusion afin d’éviter d’autres problèmes de performances.**
* La récursion étant le résultat de la conception des scénarios, vous devez concevoir les vôtres de manière à ce qu’ils n’incluent pas d’actions qui déclenchent le scénario.

## TLS

* Fusion prend actuellement en charge la version 1.2 de TLS par défaut.
* Fusion peut utiliser TLS 1.3 pour les requêtes HTTPS sortantes si TLS 1.3 est activé pour le service de destination.
* Fusion prend en charge TLS 1.2 et TLS 1.3 pour les requêtes HTTPS entrantes vers les webhooks.
* Les organisations peuvent demander que la version 1.3 de TLS soit activée pour leur instance de Fusion.

>[!NOTE]
>
> Si vous vous connectez à Workfront, sachez que cette fonctionnalité TLS est activée dans Workfront pour les appels aux domaines au format `https://<domain>.my.workfront.com`.
