---
title: Présentation de la connexion
description: Pour la plupart des applications, il est nécessaire de créer une connexion par laquelle Adobe Workfront Fusion peut communiquer avec le service tiers donné en fonction des paramètres du scénario spécifique.
author: Becky
feature: Workfront Fusion
exl-id: 01132df7-4cc0-4ff3-b4d7-607a06558735
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 22%

---

# Présentation de la connexion

Workfront Fusion nécessite une connexion pour la plupart des applications.  Elle utilise cette connexion pour communiquer avec le service tiers donné.

Par exemple, si vous souhaitez créer un scénario qui récupère des informations de Workfront, vous devez accorder l’autorisation à Workfront Fusion d’accéder à votre compte Workfront.

Une connexion représente l’autorisation et les droits utilisés par Fusion pour accéder à l’application. Vous pouvez créer une ou plusieurs connexions pour chaque application utilisée dans vos scénarios et utiliser la même connexion dans plusieurs modules ou scénarios.

La plupart des connexions ne sont utilisées que pour une seule application. Par exemple, une connexion Workfront ne peut pas être utilisée dans un module [!UICONTROL Salesforce]. Certaines applications  peuvent partager des connexions. [!DNL Adobe] Pour plus d’informations, consultez les articles relatifs à ces applications, répertoriés dans [Applications Fusion et références de leurs modules : index des articles](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).

Les connexions appartiennent à des équipes. Tous les membres d’une équipe ont accès aux connexions de l’équipe et les utilisateurs et utilisatrices en dehors d’une équipe n’ont pas accès aux connexions de l’équipe.

## Droits d’accès

Pour chaque connexion, Workfront Fusion ne nécessite que les droits d’accès nécessaires pour mener à bien un scénario donné. Par exemple, si vous créez un scénario pour télécharger un document à partir de Workfront, Workfront Fusion ne demande pas l’autorisation de créer un projet. Par la suite, si vous constatez que vous devez créer un projet, vous pouvez mettre à jour la connexion ou en créer une nouvelle qui peut créer des projets.

Tous les services ne vous permettent pas de limiter l’accès à des tâches spécifiques. Dans ce cas, Workfront Fusion doit exiger des droits d’accès complets. Pour plus d’informations sur la manière de restreindre l’accès de Workfront Fusion à votre compte enregistré auprès de ces services, consultez la documentation spécifique à l’application répertoriée dans la section [Références des applications Fusion et de leurs modules : index des articles](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md).
