---
title: Exécution de scénario, cycles et phases
description: Cet article décrit les événements qui se produisent pendant l’exécution d’un scénario  [!DNL Adobe Workfront Fusion] , tels que l’initialisation, les opérations, les engagements et les restaurations.
author: Becky
feature: Workfront Fusion
exl-id: abf41be5-df32-4eaf-b3f4-93ddf005bfe3
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 31%

---

# Exécution de scénarios, cycles et phases

Chaque exécution de scénario commence par la phase d’initialisation, se poursuit par au moins un cycle composé des phases d’opération et de validation/restauration, et se termine par la phase de finalisation

* Initialisation
* Cycle 1
   * Opération (lecture ou écriture)
   * Engagement ou restauration
* Cycle 2
   * Opération (lecture ou écriture)
   * Engagement ou restauration
* ...
* #n de cycle
   * Opération (lecture ou écriture)
   * Engagement ou restauration
* Finalisation

A plus petite échelle, chaque module suit également ces phases. Vous trouverez des informations sur les phases du module dans les informations de lot traitées, dans la bulle numérotée en haut à droite de chaque module une fois le scénario exécuté. Pour plus d’informations sur la recherche des informations de bundle traité, voir [Informations sur les bundles traités](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md#information-about-processed-bundles) dans l’article Flux d’exécution de scénario.

Vous trouverez des informations sur les phases de scénario les plus importantes dans les détails d’exécution.

## Phases d’exécution du scénario

### Initialisation

Pendant la phase d&#39;initialisation, toutes les connexions nécessaires (connexion à une base de données, service de messagerie, etc.) sont créées et vérifiées pour s&#39;assurer que le module est capable d&#39;effectuer les opérations prévues.

### Cycles

Chaque cycle représente une unité de travail indivisible composée d’une série d’opérations, chacune avec une validation ou une restauration.

Vous pouvez définir le nombre maximal de cycles dans le panneau [!UICONTROL scenario settings]. Le nombre par défaut est 1.

* [Opération](#operation)
* [Valider](#commit)
* [Restaurer](#rollback)

#### Opération

Pendant la phase de fonctionnement, on effectue une opération de lecture ou d&#39;écriture:

* Une opération de lecture consiste à obtenir des données d&#39;un service qui sont ensuite traitées par d&#39;autres modules selon un scénario prédéfini. Par exemple, le module [!UICONTROL Workfront] >[!UICONTROL Watch records] renvoie les nouveaux lots (enregistrements) créés depuis la dernière exécution du scénario.
* Une opération d&#39;écriture consiste à envoyer des données à un service donné pour traitement ultérieur. Par exemple, le module [!DNL Workfront] >[!UICONTROL Upload Document] charge un fichier dans Workfront.

#### Valider

Si la phase d’opération est réussie, la phase de validation commence, au cours de laquelle toutes les opérations effectuées par les modules sont validées. Cela signifie que [!DNL Workfront Fusion] envoie des informations sur son succès à tous les services impliqués dans la phase de fonctionnement.

### Restaurer

Si une erreur se produit au cours de la phase d&#39;opération ou de validation sur un module, la phase est abandonnée et la phase de restauration est démarrée, rendant toutes les opérations au cours du cycle donné annulées.

>[!IMPORTANT]
>
>Tous les modules [!DNL Workfront Fusion] qui prennent en charge la restauration (également connue sous le nom de transactionnalité) comportent la balise ACID.
>
>![Modules acides](assets/acid-modules.png)
>
>Les modules qui ne portent pas cette balise ne peuvent pas être ramenés à leur état initial lorsque des erreurs se produisent dans d’autres modules. Un exemple typique de module non-ACID est l&#39;action [!UICONTROL Email] >[!UICONTROL Send an Email]. Une fois l’e-mail envoyé, vous ne pouvez pas annuler l’envoi.

### Finalisation

Au cours de la phase de finalisation, les connexions ouvertes (par exemple, les connexions FTP, les connexions aux bases de données, etc.) sont fermées et le scénario terminé.

## Ressources

Pour plus d’informations, voir [Configurer les paramètres de scénario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md).
