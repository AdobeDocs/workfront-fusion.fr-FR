---
title: FAQ sur la planification de scénario
description: Les informations de cet article peuvent s’avérer utiles lorsque vous commencez à créer des scénarios dans Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 6a1d672d-0bd7-4a3a-b96d-6d8b4c97522d
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 31%

---

# FAQ sur la planification de scénario

Les informations de cet article peuvent s’avérer utiles lorsque vous commencez à créer des scénarios dans Workfront Fusion.

## Qu’est-ce qu’un scénario ?

### Réponse

Un scénario définit une séquence d’étapes à exécuter par Adobe Workfront Fusion. Pour chaque scénario, vous spécifiez la source de données, les données à utiliser et la manière dont les données doivent être traitées. Fusion vous permet de créer des scénarios simples ou complexes, capables de répondre aux cas d’utilisation de votre organisation.

Pour plus d’informations sur les scénarios, voir [Présentation des scénarios](/help/workfront-fusion/get-started-with-fusion/understand-fusion/scenario-overview.md).

## Combien de modules puis-je utiliser dans un scénario ?

### Réponse

Vous pouvez utiliser autant de modules que vous le souhaitez dans un scénario. Vous pouvez séparer les modules en itinéraires et spécifier quelles données doivent transiter par chaque itinéraire. Vous pouvez également utiliser la sortie d’un module comme entrée d’un autre module.

Bien qu’il n’y ait pas de limite au nombre de modules dans un scénario, plus de 150 modules peuvent affecter les performances du scénario.

Pour plus d’informations sur les modules, voir [Présentation des modules](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md).

## Workfront Fusion peut-il fonctionner avec les fichiers ?

### Réponse

Oui. Workfront Fusion peut recevoir, enregistrer, transformer, convertir et chiffrer des fichiers. Fusion propose également un large éventail de fonctionnalités intégrées conçues pour permettre aux utilisateurs de travailler de manière efficace et créative avec les données contenues dans les fichiers.

Pour plus d’informations sur l’utilisation des fichiers dans Fusion, consultez [Mappage d’un fichier entre des modules](/help/workfront-fusion/create-scenarios/map-data/map-files.md).

## Certains déclencheurs permettent aux scénarios de s’exécuter instantanément. Que signifie « instantanément » ?

### Réponse

Les scénarios peuvent s’exécuter à intervalles réguliers en fonction du planning que vous spécifiez, par exemple toutes les heures ou toutes les 5 minutes. Il existe des déclencheurs spéciaux, appelés déclencheurs instantanés (webhooks), qui peuvent démarrer votre scénario immédiatement après avoir reçu des données d’un service donné. Fusion traite immédiatement les données reçues, sans attendre la prochaine exécution planifiée.

Pour plus d’informations sur la différence entre les déclencheurs interrogés et instantanés, voir [Modules de déclenchement](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) dans la présentation du module d’article.

## Qu’est-ce qu’une opération ?

### Réponse

Une opération est une tâche effectuée par un module. Une opération se produit, par exemple, chaque fois qu’un déclencheur s’exécute et chaque fois qu’une action exécute une tâche.

Certains plans Fusion sont basés sur le nombre d’opérations utilisées par votre organisation.

Pour plus d’informations sur les opérations, voir [Opérations](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/operations-in-workfront-fusion.md).

## Qu’est-ce que le transfert de données ?

### Réponse

Le transfert de données correspond à la quantité de données transférées par le biais de votre scénario. Par exemple, un scénario qui récupère une image 100KB de Workfront, puis charge l’image vers un fournisseur de stockage de documents. La quantité de données utilisée dans ce scénario est 200KB.

## Qu’est-ce qu’une connexion ?

### Réponse

Une connexion est le lien entre votre compte Workfront Fusion et le service tiers que vous souhaitez utiliser. La connexion peut être créée lors de la modification d’un scénario.

Pour plus d’informations, voir [Présentation de la connexion](/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md).

## Qu’est-ce qu’un agrégateur ?

### Réponse

Un [!UICONTROL agrégateur] fusionne les données en une seule collection. Il s’agit par exemple de fichiers compressés dans une archive zip et envoyés en pièce jointe à un e-mail.

Pour plus d’informations, voir [[!UICONTROL Module Agrégateur]](/help/workfront-fusion/references/modules/aggregator-module.md).

## Que se passe-t-il si je laisse Workfront Fusion traiter un email contenant plusieurs pièces jointes ?

### Réponse

Si vous utilisez le module d’[!UICONTROL e-mail] [!UICONTROL Récupérer les pièces jointes], chaque pièce jointe est envoyée individuellement via les autres modules du scénario. Des modules similaires sont également disponibles dans d’autres applications qui reçoivent plusieurs fichiers à la fois.
