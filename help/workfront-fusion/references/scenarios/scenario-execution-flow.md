---
content-type: overview
title: Flux d’exécution du scénario
description: Cet article explique comment un scénario s’exécute et comment les données y circulent. Il explique également où vous pouvez trouver des informations sur vos données traitées et comment les lire.
author: Becky
feature: Workfront Fusion
exl-id: bd4f05e2-df3c-4848-9a70-3df18ca4461b
source-git-commit: 0ef6dde9566ca3b97c1c52d6055f0ce44f575cee
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Flux d’exécution du scénario

Cet article explique comment un scénario s’exécute et comment les données y circulent, ainsi que la manière d’afficher les données traitées par chaque module.

Pour afficher le flux de données dans un scénario actif, consultez [Affichage du flux de données dans un scénario en cours d’exécution](/help/workfront-fusion/manage-scenarios/view-scenario-data-flow.md).

## Flux d’exécution du scénario

Une fois qu’un scénario est correctement défini et activé, il s’exécute selon le planning défini.

Au début du scénario, le premier module réagit à un événement qu’il a été chargé de surveiller. Lorsqu’il renvoie des données, celles-ci sont regroupées en lots. Le scénario renvoie un lot pour chaque événement. Par exemple, si un module est défini pour surveiller les problèmes, il renvoie un lot de données pour chaque problème détecté.

Si le module de déclenchement renvoie des lots de données, ces lots sont transmis au module suivant et le scénario se poursuit, en transmettant les lots à travers chaque module successif, un par un.

Si les lots sont traités correctement par tous les modules, le scénario est marqué comme réussi dans la page des détails du scénario.

### Exemple : [!UICONTROL [!DNL Workfront Fusion] pour l’automatisation du travail]

>[!BEGINSHADEBOX]

**Exemple :** dans ce scénario, qui surveille les requêtes entrantes dans [!DNL Workfront], puis les convertit en projets [!DNL Workfront], les données sont transmises comme suit :

La première étape du scénario, réalisée par le premier module, consiste à surveiller les demandes. Chaque requête qu’il détecte est considérée comme un lot. Si le module s’exécute sans trouver de lot, le scénario se termine après le premier module.

Si le premier module renvoie un lot, le lot passe par le reste du scénario. Dans cet exemple, le lot accède au deuxième module , qui convertit la requête en projet.

![Flux d’exécution du scénario Workfront](assets/example-execution-flow-wf-only.png)

>[!ENDSHADEBOX]

### Exemple : [!UICONTROL [!DNL Workfront Fusion] pour l’automatisation et l’intégration du travail]

>[!BEGINSHADEBOX]

**Exemple :** dans ce scénario, qui télécharge des documents depuis [!DNL Adobe Workfront] et les envoie vers un dossier dans [!DNL Dropbox], les données sont transmises comme suit :

La première étape du scénario, effectuée par le premier module, consiste à rechercher des documents dans Workfront. Chaque document trouvé est considéré comme un lot. Si le module s’exécute sans trouver de lot, le scénario se termine après le premier module.

Si un lot est renvoyé, le lot passe par le reste du scénario. Dans cet exemple, le reste du scénario est constitué du deuxième module , qui charge le lot dans le dossier [!DNL Dropbox].

![Flux d’exécution du scénario d’intégration](assets/example-execution-flow-wf-dropbox.png)

Si le premier module renvoie plusieurs lots, le premier lot est chargé sur [!DNL Dropbox] avant le second. Ensuite, le deuxième lot est chargé, puis le troisième, et ainsi de suite.

>[!ENDSHADEBOX]

## Informations sur les lots traités

Pour chaque module, le lot passe par un processus en 4 étapes avant de passer au module suivant ou d’atteindre sa destination finale.

* Initialisation
* Opération
* Validation/Restauration
* Finalisation

>[!NOTE]
>
>Le scénario plus large passe également par ce processus. Pour plus d’informations sur ce processus au niveau du scénario, voir [Exécution du scénario, cycles et phases](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).

Une fois l’exécution d’un scénario terminée, chaque module affiche une icône indiquant le nombre d’opérations effectuées. Vous pouvez cliquer sur cette icône pour afficher les informations détaillées sur les lots traités pour chaque étape du processus. Vous pouvez voir quels paramètres de module ont été utilisés et quels lots ont été renvoyés par chaque module.

![Lots traités](assets/Info-processed-bundles.png)

Dans cet example, le module a reçu des informations d&#39;entrée telles que:

* Identifiant du problème détecté
* Objet vers lequel le problème sera converti (projet)
* L’identifiant du modèle qu’il utilisera pour créer le projet
* Type d’enregistrement de l’objet trouvé (OPTASK, qui pose problème)

Après traitement, le module a renvoyé les informations de sortie suivantes :

* ID du projet nouvellement créé.

Si le module a détecté plusieurs problèmes, les informations sont capturées séparément pour chaque lot. Il y aurait une zone de l&#39;Opération 2 avec des sections d&#39;entrée et de sortie décrivant le deuxième lot, et ainsi de suite.

## Erreurs lors de l’exécution d’un scénario

Une erreur peut se produire pendant l’exécution du scénario. Par exemple, si vous avez supprimé le modèle que le module utilisera pour créer le nouveau projet, le scénario se termine par un message d’erreur. Pour plus d’informations sur la gestion des erreurs, voir [Types d’erreur](/help/workfront-fusion/references/errors/error-processing.md).

## Ressources

* Pour plus d’informations sur la configuration d’un scénario, voir [Éditeur de scénarios](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md).
* Pour plus d’informations sur la page des détails du scénario, voir [Détails du scénario](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-details.md).
* Pour plus d’informations sur l’activation d’un scénario, voir [ Activer ou désactiver un scénario](/help/workfront-fusion/manage-scenarios/activate-deactivate-scenarios.md).
* Pour plus d’informations sur la planification d’un scénario, voir [Planification d’un scénario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).
* Pour plus d’informations sur les modules, voir [Présentation des modules](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md).
