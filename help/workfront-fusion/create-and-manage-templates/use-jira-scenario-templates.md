---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: scenarios
title: Utiliser des modèles pour connecter Adobe Workfront Fusion et Jira
description: Utilisez ces modèles pour automatiser les workflows entre Adobe Workfront Fusion et Jira.
author: Becky
feature: Workfront Fusion
hide: true
hidefromtoc: true
source-git-commit: aa3bdd7d14c86085c36e3859f6d53c0cadb28920
workflow-type: tm+mt
source-wordcount: '4075'
ht-degree: 4%

---

# Utiliser des modèles pour connecter Adobe Workfront Fusion et Jira

Adobe Workfront Fusion propose des modèles qui peuvent automatiser les workflows courants entre Fusion et Jira.

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
   <p>Workfront : si votre entreprise dispose d’un package Select ou Prime Workfront qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acheter Adobe Workfront Fusion.</p><p>Jira : Vous devez disposer d’une licence pour Jira Cloud</p>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">Configurations des niveaux d’accès</td> 
   <td> <p>Workfront : autorisation de création d’utilisateurs, de formulaires personnalisés et de champs personnalisés.</p> <p>Jira : autorisations de création d’utilisateurs, de champs personnalisés et de modification des écrans et des webhooks.</td> 
  </tr> 
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation Workfront](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Conditions préalables

### Workfront

* Vous devez disposer d’un compte technique sur le Adobe Developer Console.

  Pour plus d’informations et d’instructions, voir [Configuration du compte technique](https://developer.adobe.com/cloud-storage/guides/getting-started/technical-account-setup) dans la documentation d’Adobe.
* Vous devez appliquer les autorisations d’administrateur système au compte technique dans la zone Profils de produit Adobe Admin Console .

  Pour plus d’informations et d’instructions, voir [Création d’administrateurs système dans Workfront avec Adobe Admin Console](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/admin-console#create-system-administrators-in-workfront-with-the-adobe-admin-console)

### Jira

Si vous utilisez l’autorisation OAuth2 pour Jira (recommandée), vous devez configurer une application OAuth2 à l’adresse [https://developer.atlassian.com/console](https://developer.atlassian.com/console). Pour plus d’informations et d’instructions, consultez la section [Créer une connexion OAuth2 à Jira](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-modules-new.md#create-an-oauth2-connection-to-jira) dans l’article Modules Jira.

<!--

When configuring this application, you will need the following scopes:

* `read:jira-work` 
* `read:jira-user`
* `write:jira-work`

-->

## Hypothèses

Ces modules supposent ce qui suit :

* Workfront est la source de vérité du projet global de campagne marketing
* Jira est utilisé par les équipes techniques et remplit une partie d’un projet qui a commencé dans Workfront.
* Tous les utilisateurs et utilisatrices de Jira n’ont pas accès à Workfront et vice versa.
* Workfront et Jira sont hébergés dans le cloud.

## Modèle De Données (Mappages De Champs)


| Workfront | Jira | Direction | Notes |
|---|---|---|---|
| ObjId | ID WF * | WF → Jira | Lors De La Création De L’Événement Jira |
| Clé Jira * | Clé de l&#39;événement | Jira → WF | Lors De La Création De L’Événement Jira |
| URL Jira * | - | Jira → WF | Lien cliquable de l’utilisateur dans WF vers Jira |
| - | Lien WF * | WF → Jira | Lien cliquable de l’utilisateur dans Jira vers WF |
| Nom | Résumé | WF → Jira |  |
| Description | Description | WF → Jira |  |
| Statut | Statut WF | WF → Jira | Statut WF |
| Statut Jira * | Statut | Jira → WF | Statut Jira |
| Date d&#39;achèvement prévue | Date d’échéance | WF → Jira | Date d&#39;achèvement prévue |
| Notes | Commentaires | WF ↔ Jira | Copie bidirectionnelle |
| Document | Pièce jointe | WF → Jira | En tant que pièces jointes lors de la création d’un événement et commentaires sur les nouveaux documents après leur création. |

\* Ces champs sont configurés dans le cadre de cette configuration d’intégration. Pour obtenir des instructions, voir [Configuration des conditions préalables dans Workfront, Jira et Workfront Fusion](/help/workfront-fusion/create-and-manage-templates/use-jira-scenario-templates.md#configure-prerequisites-in-workfront-jira-and-workfront-fusion).

## Configuration des conditions préalables dans Workfront, Jira et Workfront Fusion

Pour utiliser les modèles d’intégration Jira, vous devez effectuer les configurations suivantes :

* [Configurer Jira](#configure-jira)
* [Configuration de Workfront](#configure-workfront)
* [Configuration des connexions dans Workfront Fusion](#configure-connections-in-workfront-fusion)

### Configurer Jira

Pour utiliser ces modules, les éléments suivants doivent être créés dans Jira :

* Utilisateur de l’intégration système
* Trois champs personnalisés spécifiques

#### Créer un utilisateur d’intégration système dans Jira

1. Dans Jira, créez un utilisateur spécifique appelé Utilisateur de l’intégration système. Cet utilisateur ne doit être utilisé que par Workfront Fusion et ne doit pas représenter un utilisateur humain. Les informations d’identification de cet utilisateur seront utilisées par les connexions Workfront Fusion.

#### Créer les champs personnalisés nécessaires dans Jira

Cette intégration exige trois champs spécifiques dans le compte Jira auquel elle se connecte. Sans ces champs, l’intégration échoue

1. Dans Jira, accédez à **Paramètres** (icône d’engrenage) et sélectionnez **Éléments de travail**.
1. Dans le volet de navigation de gauche, sélectionnez **Champs personnalisés**.
1. Dans le coin supérieur droit de l’écran, cliquez sur **Créer un champ personnalisé**.
1. Créez les champs suivants :

   | Nom du champ | Type de champ |
   |---|---|
   | ID WF | Champ de texte (une seule ligne) |
   | Statut WF | Champ de texte (une seule ligne) |
   | Lien WF | Champ URL |

   Pour plus d’informations sur la création de liens dans Jira, consultez la documentation Jira sur la création de champs.
1. Ajoutez les champs nouvellement créés à l’écran associé à votre projet Jira.

   Pour plus d’informations sur les écrans dans Jira, consultez la documentation Jira sur la configuration des écrans d’élément de travail.


### Configuration de Workfront

Pour utiliser ces modules, les éléments suivants doivent être créés dans Workfront :

* Utilisateur de l’intégration système
* Un formulaire personnalisé spécifique

#### Création d’un utilisateur d’intégration système dans Workfront

1. Dans Workfront, créez un utilisateur d’intégration système. Cet utilisateur est uniquement utilisé par Workfront Fusion et ne représente pas un utilisateur humain. Les tâches affectées à cet utilisateur déclencheront le scénario qui synchronise Workfront avec Jira.

   Pour obtenir des instructions, voir [Ajouter des utilisateurs](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/add-users) dans la documentation de Workfront.

#### Création d’un formulaire personnalisé dans Workfront

1. Dans Workfront, commencez à créer un formulaire personnalisé.

   Pour obtenir des instructions détaillées, voir [Création d’un formulaire personnalisé](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/customize/custom-forms/design-a-form/design-a-form) dans la documentation de Workfront.
1. Nommez le formulaire « **Champs JIRA** ».
1. Insérez les champs suivants dans le formulaire personnalisé :

| Nom du champ | Type de champ |
|---|---|
| Clé Jira | Champ de texte monoligne |
| URL Jira | Champ de texte monoligne |
| Statut Jira | Champ de texte monoligne |

1. Ajoutez les champs supplémentaires que vous souhaitez mapper entre Jira et Workfront.
1. Enregistrez le formulaire personnalisé.

>[!NOTE]
>
>Nous vous recommandons de restreindre ce formulaire aux modifications effectuées par d&#39;autres utilisateurs. Pour ce faire, assurez-vous que tous les utilisateurs ajoutés au formulaire personnalisé disposent uniquement d’un accès en lecture seule.
>
>Pour obtenir des instructions détaillées, voir [Partager un formulaire personnalisé](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/customize/custom-forms/manage-custom-forms/share-access-to-a-custom-form) dans la documentation de Workfront.

### Configuration des connexions dans Workfront Fusion

Vous devez avoir créé les utilisateurs de l’intégration système dans Jira et Workfront avant de pouvoir créer des connexions.

Lors de la création de ces connexions, veillez à utiliser les informations d&#39;identification des utilisateurs d&#39;intégration système créés.

Si vous le souhaitez, vous pouvez créer ces connexions dans le cadre de la configuration des modèles.

* Pour obtenir des instructions sur la création d’une connexion à Workfront, voir [Connexion de Workfront à Workfront Fusion](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#connect-workfront-to-workfront-fusion) dans l’article Modules Workfront.
* Pour obtenir des instructions sur la création d’une connexion à Jira, consultez [Connexion de Jira à Workfront Fusion](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-modules-new.md#connect-jira-to-workfront-fusion) dans l’article Modules logiciels Jira.


## Scénarios

Huit modèles prêts à l’emploi pour Jira permettent de répliquer des workflows courants et d’accélérer la mise en œuvre. Les modèles sont entièrement personnalisables pour répondre aux besoins spécifiques de l’entreprise et peuvent être étendus en fonction de l’évolution des besoins.

Vous n’avez pas besoin d’implémenter tous les scénarios. La mise en œuvre minimale nécessiterait le scénario 1, qui créerait une intégration unidirectionnelle à un problème JIRA à partir d’une affectation dans Workfront.  Vous pouvez ajouter les scénarios supplémentaires pour ajouter de la robustesse et une interconnectivité plus bidirectionnelle entre Workfront et JIRA.  Vous pouvez également créer des scénarios supplémentaires pour gérer des cas tels que l’intégration de projet à épique ou le problème JIRA à un problème Workfront ou à des tâches.

Toute utilisation de ces modèles ou extensions de ces modèles est considérée comme une configuration personnalisée. Nous vous recommandons d’utiliser Adobe Professional Services ou un partenaire Adobe pour la prise en charge et l’implémentation.

* **[Workfront vers Jira : créer un événement JIRA à partir de l&#39;affectation de tâche ou d&#39;événement Workfront](#scenario-1-workfront-to-jira-create-jira-issue-from-workfront-task-or-issue-assignment)**
* [JIRA vers Workfront : JIRA vers Workfront : envoyez des mises à jour sur les problèmes et des commentaires à Workfront à partir de Jira.](#scenario-2-jira-to-workfront-send-updates-on-issues-and-comments-back-to-workfront-from-jira)
* [Workfront vers Jira : modifications apportées à la tâche Workfront en problème JIRA](#scenario-3-workfront-to-jira-changes-to-workfront-task-to-jira-issue)
* Workfront vers Jira : modifications apportées au problème Workfront en problème JIRA
* Workfront vers Jira : créez un commentaire dans JIRA lorsqu’une nouvelle note est ajoutée sur une tâche ou un problème Workfront
* Workfront vers Jira : création d’un commentaire dans JIRA sur la note supprimée sur la tâche ou l’événement Workfront
* Workfront vers Jira : permet de créer un commentaire dans JIRA en cas de création d’un document sur une tâche ou un problème Workfront.
* Workfront vers Jira : permet de créer un commentaire dans JIRA sur le document supprimé concernant une tâche ou un problème Workfront.

### Paramètres généraux

Lors de la configuration de ces modèles, utilisez les paramètres généraux suivants :

* **JiraBaseURL** : URL de base de l’instance Jira. Exemple : `https://myjira.atlassian.net/`
* **wfBaseURL** : URL de base de l’instance Workfront.  En règle générale : `https://<domain>.my.workfront.com` où `<domain>` correspond à votre nom de domaine Workfront.
* **defaultJIRAReporterID** : ID de l’utilisateur dans JIRA qui crée des problèmes. (Exemple : `557058:5aedf933-2312-40bc-b328-0c21314167f0`)
Vous pouvez obtenir cet identifiant en effectuant l’une des opérations suivantes :
   * Cliquez sur le profil de l’utilisateur dans JIRA et vérifiez l’URL dans votre navigateur.
(Exemple`https://myjira.atlassian.net/jira/people/<JiraUserID>`)
   * Exécutez l’appel API suivant sur votre instance JIRA pour obtenir l’identifiant du compte spécifique dans JIRA :
     `GET /rest/api/3/user/search?query=email@example.com`


### Scénario 1 : Workfront vers Jira : création d’un problème JIRA à partir de l’affectation de tâche ou de problème Workfront

Ce scénario crée un problème Jira lorsqu’une tâche ou un problème Workfront est affecté à l’utilisateur de l’intégration système. Le scénario renseigne les champs Résumé, Description, Échéance, Statut de WF et ID de WF. Une fois l’événement créé, ce scénario télécharge également la liste des pièces jointes et l’historique des notes liées à la tâche ou à l’événement d’origine dans Workfront.

Si une tâche Workfront est affectée, le problème dans Jira est une tâche. Si un problème Workfront est affecté, le problème Jira est un bogue.

+++**Développez pour afficher les instructions de configuration du scénario 1 :Workfront Jira : créer un problème JIRA à partir de l’affectation de tâche ou de problème Workfront**

#### Configuration du module de déclenchement

1. Cliquez sur l’onglet **Modèles** ![icône Modèles](assets/templates-icon.png) dans le panneau de navigation de gauche.
1. Recherchez le modèle à l’aide de la barre de recherche située en haut à gauche de l’écran. Vous pouvez effectuer une recherche par nom de modèle ou applications incluses.
1. Cliquez sur le modèle **Workfront vers Jira : Créer un événement JIRA à partir de l&#39;affectation de tâche ou d&#39;événement Workfront**.

   Une vue du modèle s’ouvre, affichant des informations et une animation du flux de données.
1. Dans le premier module, commencez à ajouter un webhook.
1. Sélectionnez la connexion Workfront que vous avez créée dans [Configurer les connexions dans Workfront Fusion](#configure-connections-in-workfront-fusion).
1. Dans le champ **Type d’enregistrement**, sélectionnez `Assignment`.
1. Dans le champ **État**, sélectionnez `New state`.
1. Configurez le filtre avec les opérations suivantes, à l&#39;aide de l&#39;option **Et** :

   | champ | Opérateur | Valeur |
   |---|---|---|
   | assignedToID | Est égal à | (Saisissez l’ID Workfront de l’utilisateur de l’intégration système) |
   | TaskID | Existe |  |
   | projectID | Est égal à | (Saisissez l’identifiant du ou des projets que le webhook doit surveiller) |

1. Activez l’option **Exclure les mises à jour effectuées par cette connexion**.
1. Dans le champ **Origine de l’enregistrement**, sélectionnez Nouvel enregistrement uniquement.
1. Cliquez sur **Enregistrer** pour enregistrer le webhook, puis sur **OK** pour enregistrer le module de déclenchement.
1. Passez à [Connexion des modules de modèle à Workfront et Jira](#connect-template-modules-to-workfront-and-jira)

#### Connexion des modules de modèle à Workfront et Jira

1. Dans **chaque** module Workfront, dans le champ Connexion , sélectionnez la connexion Workfront que vous avez créée dans [Configurer les connexions dans Workfront Fusion](#configure-connections-in-workfront-fusion), puis cliquez sur **OK** pour enregistrer la connexion à ce module.
1. Dans **each** Module Jira, dans le champ Connexion , sélectionnez la connexion Workfront que vous avez créée dans [Configurer les connexions dans Workfront Fusion](#configure-connections-in-workfront-fusion), puis cliquez sur **OK** pour enregistrer la connexion à ce module.
1. Passez à [&#x200B; Mettre à jour le module Paramètres généraux &#x200B;](#update-the-general-parameters-module).

#### Mise à jour du module Paramètres généraux

1. Dans le deuxième module du modèle (Définition des détails de l’environnement), pour chacune des variables suivantes, cliquez sur **Ajouter un élément** et saisissez le nom et la valeur de la variable

   | Nom de la variable | Valeur de variable |
   |---|---|
   | defaultJiraReporterID | Saisissez l’ID de l’utilisateur par défaut lorsque l’utilisateur créateur n’existe pas dans Jira. Vous pouvez trouver cet identifiant utilisateur en cliquant sur le profil de l’utilisateur et en vérifiant l’URL du navigateur. Exemple : `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | Saisissez l’URL de base du compte Jira auquel vous vous connectez. |
   | wfBaseURL | Saisissez l’URL de base du compte Workfront auquel vous vous connectez. |

1. Passez à [Mappage des champs personnalisés dans Jira](#map-custom-fields-in-jira)

#### Mappez les champs personnalisés dans Jira.

<!--Awaiting feedback-->

+++

### Scénario 2 : JIRA vers Workfront : envoyez des mises à jour sur les problèmes et des commentaires à Workfront à partir de Jira.

Ce scénario crée une tâche ou un problème Workfront lorsqu’un problème est créé dans Jira.

>[!NOTE]
>
>Ce scénario nécessite une connexion OAuth2 pour Jira.
>Pour utiliser l’autorisation OAuth2 pour Jira, vous devez configurer une application OAuth2 sur [https://developer.atlassian.com/console](https://developer.atlassian.com/console). Pour plus d’informations et d’instructions, consultez la documentation Jira.

+++**Développez pour afficher les instructions de configuration du Scénario 2 : JIRA vers Workfront : envoyez des mises à jour sur les problèmes et des commentaires à Workfront à partir de Jira**

1. Cliquez sur l’onglet **Modèles** ![icône Modèles](assets/templates-icon.png) dans le panneau de navigation de gauche.
1. Recherchez le modèle à l’aide de la barre de recherche située en haut à gauche de l’écran. Vous pouvez effectuer une recherche par nom de modèle ou applications incluses.
1. Cliquez sur le modèle **Partie 2 : JIRA vers Workfront : envoyer des mises à jour sur les problèmes et des commentaires à Workfront à partir de Jira** .

   Une vue du modèle s’ouvre, affichant des informations et une animation du flux de données.
1. Dans le premier module, commencez à ajouter un webhook.
1. Sélectionnez une connexion qui utilise les informations d’identification de l’utilisateur de l’intégration système ou créez une connexion à Jira avec les informations d’identification de l’intégration système.

* Pour obtenir des instructions sur la création d’une connexion à Jira, consultez [Connexion de Jira à Workfront Fusion](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-modules-new.md#connect-jira-to-workfront-fusion) dans l’article Modules logiciels Jira.

1. Configuration du filtre webhook

1. Passer à [Configuration d’un webhook dans Jira](#configure-a-webhook-in-jira)

#### Configuration d’un webhook dans Jira

1. Dans Jira, créez un webhook.

   Pour obtenir des instructions, consultez [Webhooks](https://developer.atlassian.com/server/jira/platform/webhooks/) dans la documentation Jira.

1. Lors de la configuration du webhook, utilisez les valeurs suivantes :

   * **JQL** : projet = « yourProjectName » (où yourProjectName = le nom de votre projet JIRA)
   * **Problème** : créé, mis à jour
   * **Commentaire** : créé, supprimé


1. Passez à [Connexion des modules de modèle à Workfront et Jira (module 2)](#connect-template-modules-to-workfront-and-jira-module-2)

#### Connexion des modules de modèle à Workfront et Jira (module 2)

1. Dans **chaque** module Workfront, dans le champ Connexion , sélectionnez la connexion Workfront que vous avez créée dans [Configurer les connexions dans Workfront Fusion](#configure-connections-in-workfront-fusion), puis cliquez sur **OK** pour enregistrer la connexion à ce module.
1. Dans **each** Module Jira, dans le champ Connexion , sélectionnez la connexion Workfront que vous avez créée dans [Configurer les connexions dans Workfront Fusion](#configure-connections-in-workfront-fusion), puis cliquez sur **OK** pour enregistrer la connexion à ce module.
   <!--#### Map custom fields-->

+++

### Scénario 3 : Workfront vers Jira : modifications de la tâche Workfront vers le problème JIRA

+++**Développez pour afficher les instructions de configuration du scénario 3 : modifications WF en Jira (tâches)**

1. Cliquez sur l’onglet **Modèles** ![icône Modèles](assets/templates-icon.png) dans le panneau de navigation de gauche.
1. Recherchez le modèle à l’aide de la barre de recherche située en haut à gauche de l’écran. Vous pouvez effectuer une recherche par nom de modèle ou applications incluses.
1. Cliquez sur le modèle **Partie 3 : Workfront vers Jira : Modifications de la tâche Workfront vers problème JIRA**.

   Une vue du modèle s’ouvre, affichant des informations et une animation du flux de données.

1. Cliquez sur le modèle pour accéder à l’éditeur.
1. Sélectionnez l’organisation et l’équipe qui seront propriétaires de ce scénario.
1. Dans le premier module, commencez à ajouter un webhook.
1. Dans le champ Connexion , sélectionnez la connexion Workfront qui utilise les informations d’identification de l’intégration système.
1. Dans le champ **Type d’enregistrement**, sélectionnez `Task`.
1. Dans le champ **État**, sélectionnez `New state`.
1. Configurez le filtre avec les opérations suivantes, à l&#39;aide de l&#39;option **Et** :

   | champ | Opérateur | Valeur |
   |---|---|---|
   | assignedToID | Est égal à | Saisissez l’ID Workfront de l’utilisateur de l’intégration système |
   | projectID | Est égal à | Saisissez l’identifiant du ou des projets que le webhook doit surveiller. |
   | DE : clé Jira | Existe |  |

1. Activez l’option **Exclure les mises à jour effectuées par cette connexion**.
1. Dans le champ **Origine de l’enregistrement**, sélectionnez `Updated record only`.
1. Cliquez sur **Enregistrer** pour enregistrer le webhook, puis sur **OK** pour enregistrer le module de déclenchement.
1. Dans le deuxième module, définissez les variables suivantes, puis cliquez sur **OK** pour enregistrer le module.

   | Nom de la variable | Valeur de variable |
   |---|---|
   | defaultJiraReporterID | Il s’agit de l’identifiant de l’utilisateur par défaut lorsque l’utilisateur créateur n’existe pas dans Jira. Vous pouvez trouver cet identifiant utilisateur en cliquant sur le profil de l’utilisateur et en vérifiant l’URL du navigateur. Exemple : `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | URL de base du compte Jira auquel vous vous connectez. |
   | wfBaseURL | URL de base du compte Workfront auquel vous vous connectez. |

1. Dans **each** le module Workfront, dans le champ Connexion , sélectionnez la connexion Workfront qui utilise les informations d&#39;identification de l&#39;intégration système, puis cliquez sur **OK** pour enregistrer le module.
1. Dans le module Jira **each**, dans le champ Connexion , sélectionnez la connexion Jira qui utilise les informations d’identification de l’intégration système, puis cliquez sur **OK** pour enregistrer le module.


+++



### Scénario 4 : Workfront vers Jira : modifications du problème Workfront vers le problème JIRA

Ce scénario envoie des mises à jour à partir de problèmes Workfront vers des problèmes JIRA précédemment connectés.

+++**Développez pour afficher les instructions de configuration du scénario 4 : modifications WF en Jira (problèmes)**

1. Cliquez sur l’onglet **Modèles** ![icône Modèles](assets/templates-icon.png) dans le panneau de navigation de gauche.
1. Recherchez le modèle à l’aide de la barre de recherche située en haut à gauche de l’écran. Vous pouvez effectuer une recherche par nom de modèle ou applications incluses.
1. Cliquez sur le modèle **Scénario 4 : modifications WF-to-Jira (problèmes)**.

   Une vue du modèle s’ouvre, affichant des informations et une animation du flux de données.

1. Cliquez sur le modèle pour accéder à l’éditeur.
1. Sélectionnez l’organisation et l’équipe qui seront propriétaires de ce scénario.
1. Dans le premier module, commencez à ajouter un webhook.
1. Dans le champ Connexion , sélectionnez la connexion Workfront qui utilise les informations d’identification de l’intégration système.
1. Dans le champ **Type d’enregistrement**, sélectionnez `??`.
1. Dans le champ **État**, sélectionnez `New state`.
1. Configurez le filtre avec les opérations suivantes, à l&#39;aide de l&#39;option **Et** :

   | champ | Opérateur | Valeur |
   |---|---|---|
   | (Mises à jour sur les événements) |  |  |
   | assignedToID | Est égal à | Saisissez l’ID Workfront de l’utilisateur de l’intégration système |
   | projectID | Est égal à | Saisissez l’identifiant du ou des projets que le webhook doit surveiller. |
   | ID WF | Existe |  |

1. Activez l’option **Exclure les mises à jour effectuées par cette connexion**.
1. Cliquez sur **Enregistrer** pour enregistrer le webhook, puis sur **OK** pour enregistrer le module de déclenchement.
1. Dans le deuxième module, définissez les variables suivantes, puis cliquez sur **OK** pour enregistrer le module.

   | Nom de la variable | Valeur de variable |
   |---|---|
   | defaultJiraReporterID | Il s’agit de l’identifiant de l’utilisateur par défaut lorsque l’utilisateur créateur n’existe pas dans Jira. Vous pouvez trouver cet identifiant utilisateur en cliquant sur le profil de l’utilisateur et en vérifiant l’URL du navigateur. Exemple : `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | URL de base du compte Jira auquel vous vous connectez. |
   | wfBaseURL | URL de base du compte Workfront auquel vous vous connectez. |

1. Dans **each** le module Workfront, dans le champ Connexion , sélectionnez la connexion Workfront qui utilise les informations d&#39;identification de l&#39;intégration système, puis cliquez sur **OK** pour enregistrer le module.
1. Dans le module Jira **each**, dans le champ Connexion , sélectionnez la connexion Jira qui utilise les informations d’identification de l’intégration système, puis cliquez sur **OK** pour enregistrer le module.


+++



### Scénario 5 : Nouvelles notes WF-to-Jira (tâches et problèmes)

+++**Développez pour afficher les instructions de configuration du scénario 5 : nouvelles notes WF-to-Jira (tâches et événements)**

1. Cliquez sur l’onglet **Modèles** ![icône Modèles](assets/templates-icon.png) dans le panneau de navigation de gauche.
1. Recherchez le modèle à l’aide de la barre de recherche située en haut à gauche de l’écran. Vous pouvez effectuer une recherche par nom de modèle ou applications incluses.
1. Cliquez sur le modèle **Scénario 5 : Nouvelles notes WF-to-Jira (tâches et événements)**.

   Une vue du modèle s’ouvre, affichant des informations et une animation du flux de données.
1. Dans le premier module, commencez à ajouter un webhook.
1. Dans le champ Connexion , sélectionnez la connexion Workfront qui utilise les informations d’identification de l’intégration système.
1. Dans le champ **Type d’enregistrement**, sélectionnez `??`.
1. Dans le champ **État**, sélectionnez `New state`.
1. Configurez le filtre avec les opérations suivantes, à l&#39;aide de l&#39;option **Et** :

   | champ | Opérateur | Valeur |
   |---|---|---|
   | (Création et mises à jour sur les notes.) |  |  |
   | assignedToID | Est égal à | Saisissez l’ID Workfront de l’utilisateur de l’intégration système |
   | projectID | Est égal à | Saisissez l’identifiant du ou des projets que le webhook doit surveiller. |

1. Activez l’option **Exclure les mises à jour effectuées par cette connexion**.
1. Cliquez sur **Enregistrer** pour enregistrer le webhook, puis sur **OK** pour enregistrer le module de déclenchement.
1. Dans le deuxième module, définissez les variables suivantes, puis cliquez sur **OK** pour enregistrer le module.

   | Nom de la variable | Valeur de variable |
   |---|---|
   | defaultJiraReporterID | Il s’agit de l’identifiant de l’utilisateur par défaut lorsque l’utilisateur créateur n’existe pas dans Jira. Vous pouvez trouver cet identifiant utilisateur en cliquant sur le profil de l’utilisateur et en vérifiant l’URL du navigateur. Exemple : `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | URL de base du compte Jira auquel vous vous connectez. |
   | wfBaseURL | URL de base du compte Workfront auquel vous vous connectez. |

1. Activez l’option **Exclure les mises à jour effectuées par cette connexion**.
1. Cliquez sur **Enregistrer** pour enregistrer le webhook, puis sur **OK** pour enregistrer le module de déclenchement.
1. Dans **each** le module Workfront, dans le champ Connexion , sélectionnez la connexion Workfront qui utilise les informations d&#39;identification de l&#39;intégration système, puis cliquez sur **OK** pour enregistrer le module.
1. Dans le module Jira **each**, dans le champ Connexion , sélectionnez la connexion Jira qui utilise les informations d’identification de l’intégration système, puis cliquez sur **OK** pour enregistrer le module.


+++




### Scénario 6 : suppression de notes WF-à-Jira (tâches et problèmes)

+++**Développez pour afficher les instructions de configuration du scénario 6:WF-to-Jira supprimez des notes (tâches et événements)**

1. Cliquez sur l’onglet **Modèles** ![icône Modèles](assets/templates-icon.png) dans le panneau de navigation de gauche.
1. Recherchez le modèle à l’aide de la barre de recherche située en haut à gauche de l’écran. Vous pouvez effectuer une recherche par nom de modèle ou applications incluses.
1. Cliquez sur le modèle **Scénario 6 : Supprimer des notes WF-to-Jira (tâches et événements)** .

   Une vue du modèle s’ouvre, affichant des informations et une animation du flux de données.
1. Dans le premier module, commencez à ajouter un webhook.
1. Dans le champ Connexion , sélectionnez la connexion Workfront qui utilise les informations d’identification de l’intégration système.
1. Dans le champ **Type d’enregistrement**, sélectionnez `??`.
1. Dans le champ **État**, sélectionnez `New state`.
1. Configurez le filtre avec les opérations suivantes, à l&#39;aide de l&#39;option **Et** :

   | champ | Opérateur | Valeur |
   |---|---|---|
   | (Supprimer sur les notes.) |  |  |
   | assignedToID | Est égal à | Saisissez l’ID Workfront de l’utilisateur de l’intégration système |
   | projectID | Est égal à | Saisissez l’identifiant du ou des projets que le webhook doit surveiller. |
   | ID WF | Existe |  |

1. Activez l’option **Exclure les mises à jour effectuées par cette connexion**.
1. Cliquez sur **Enregistrer** pour enregistrer le webhook, puis sur **OK** pour enregistrer le module de déclenchement.
1. Dans le deuxième module, définissez les variables suivantes, puis cliquez sur **OK** pour enregistrer le module.

   | Nom de la variable | Valeur de variable |
   |---|---|
   | defaultJiraReporterID | Il s’agit de l’identifiant de l’utilisateur par défaut lorsque l’utilisateur créateur n’existe pas dans Jira. Vous pouvez trouver cet identifiant utilisateur en cliquant sur le profil de l’utilisateur et en vérifiant l’URL du navigateur. Exemple : `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | URL de base du compte Jira auquel vous vous connectez. |
   | wfBaseURL | URL de base du compte Workfront auquel vous vous connectez. |

1. Dans **each** le module Workfront, dans le champ Connexion , sélectionnez la connexion Workfront qui utilise les informations d&#39;identification de l&#39;intégration système, puis cliquez sur **OK** pour enregistrer le module.
1. Dans le module Jira **each**, dans le champ Connexion , sélectionnez la connexion Jira qui utilise les informations d’identification de l’intégration système, puis cliquez sur **OK** pour enregistrer le module.


+++



### Scénario 7 : nouvelles pièces jointes WF-à-Jira (tâches et événements)

+++**Développez pour afficher les instructions de configuration du scénario 7 : nouvelles pièces jointes WF-to-Jira (tâches et événements)**

1. Cliquez sur l’onglet **Modèles** ![icône Modèles](assets/templates-icon.png) dans le panneau de navigation de gauche.
1. Recherchez le modèle à l’aide de la barre de recherche située en haut à gauche de l’écran. Vous pouvez effectuer une recherche par nom de modèle ou applications incluses.
1. Cliquez sur le modèle **Scénario 7 : Nouvelles pièces jointes WF-to-Jira (tâches et événements)**.

   Une vue du modèle s’ouvre, affichant des informations et une animation du flux de données.
1. Dans le premier module, commencez à ajouter un webhook.
1. Dans le champ Connexion , sélectionnez la connexion Workfront qui utilise les informations d’identification de l’intégration système.
1. Dans le champ **Type d’enregistrement**, sélectionnez `??`.
1. Dans le champ **État**, sélectionnez `New state`.
1. Configurez le filtre avec les opérations suivantes, à l&#39;aide de l&#39;option **Et** :

   | champ | Opérateur | Valeur |
   |---|---|---|
   | (Créer sur le document). |  |  |
   | assignedToID | Est égal à | Saisissez l’ID Workfront de l’utilisateur de l’intégration système |
   | projectID | Est égal à | Saisissez l’identifiant du ou des projets que le webhook doit surveiller. |

1. Dans le deuxième module, définissez les variables suivantes.

   | Nom de la variable | Valeur de variable |
   |---|---|
   | defaultJiraReporterID | Il s’agit de l’identifiant de l’utilisateur par défaut lorsque l’utilisateur créateur n’existe pas dans Jira. Vous pouvez trouver cet identifiant utilisateur en cliquant sur le profil de l’utilisateur et en vérifiant l’URL du navigateur. Exemple : `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | URL de base du compte Jira auquel vous vous connectez. |
   | wfBaseURL | URL de base du compte Workfront auquel vous vous connectez. |

1. Activez l’option **Exclure les mises à jour effectuées par cette connexion**.
1. Cliquez sur **Enregistrer** pour enregistrer le webhook, puis sur **OK** pour enregistrer le module de déclenchement.
1. Dans **each** le module Workfront, dans le champ Connexion , sélectionnez la connexion Workfront qui utilise les informations d&#39;identification de l&#39;intégration système, puis cliquez sur **OK** pour enregistrer le module.
1. Dans le module Jira **each**, dans le champ Connexion , sélectionnez la connexion Jira qui utilise les informations d’identification de l’intégration système, puis cliquez sur **OK** pour enregistrer le module.


+++



### Scénario 8 : suppression des pièces jointes WF-à-Jira (tâches et événements)

+++**Développez pour afficher les instructions de configuration du scénario 8 : suppression des pièces jointes WF-à-Jira (tâches et événements)**

1. Cliquez sur l’onglet **Modèles** ![icône Modèles](assets/templates-icon.png) dans le panneau de navigation de gauche.
1. Recherchez le modèle à l’aide de la barre de recherche située en haut à gauche de l’écran. Vous pouvez effectuer une recherche par nom de modèle ou applications incluses.
1. Cliquez sur le modèle **Scénario 8 : suppression de pièces jointes WF-to-Jira (tâches et événements)** .

   Une vue du modèle s’ouvre, affichant des informations et une animation du flux de données.
1. Dans le premier module, commencez à ajouter un webhook.
1. Dans le champ Connexion , sélectionnez la connexion Workfront qui utilise les informations d’identification de l’intégration système.
1. Dans le champ **Type d’enregistrement**, sélectionnez `??`.
1. Dans le champ **État**, sélectionnez `New state`.
1. Configurez le filtre avec les opérations suivantes, à l&#39;aide de l&#39;option **Et** :

   | champ | Opérateur | Valeur |
   |---|---|---|
   | (Supprimer sur le document) |  |  |
   | assignedToID | Est égal à | Saisissez l’ID Workfront de l’utilisateur de l’intégration système |
   | projectID | Est égal à | Saisissez l’identifiant du ou des projets que le webhook doit surveiller. |

1. Dans le deuxième module, définissez les variables suivantes.

   | Nom de la variable | Valeur de variable |
   |---|---|
   | defaultJiraReporterID | Il s’agit de l’identifiant de l’utilisateur par défaut lorsque l’utilisateur créateur n’existe pas dans Jira. Vous pouvez trouver cet identifiant utilisateur en cliquant sur le profil de l’utilisateur et en vérifiant l’URL du navigateur. Exemple : `https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | URL de base du compte Jira auquel vous vous connectez. |
   | wfBaseURL | URL de base du compte Workfront auquel vous vous connectez. |

1. Activez l’option **Exclure les mises à jour effectuées par cette connexion**.
1. Cliquez sur **Enregistrer** pour enregistrer le webhook, puis sur **OK** pour enregistrer le module de déclenchement.
1. Dans **each** le module Workfront, dans le champ Connexion , sélectionnez la connexion Workfront qui utilise les informations d&#39;identification de l&#39;intégration système, puis cliquez sur **OK** pour enregistrer le module.
1. Dans le module Jira **each**, dans le champ Connexion , sélectionnez la connexion Jira qui utilise les informations d’identification de l’intégration système, puis cliquez sur **OK** pour enregistrer le module.


+++

