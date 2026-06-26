---
title: Utilisation de packages de fonctions personnalisées
description: Lorsque vous mappez des éléments, vous pouvez utiliser des fonctions pour créer des formules simples ou complexes.
author: Becky
feature: Workfront Fusion
source-git-commit: 4ec81401b5a76edd620b9779414ee578966b4315
workflow-type: tm+mt
source-wordcount: '2042'
ht-degree: 6%

---


# Utilisation de packages de fonctions personnalisées

Les packages vous permettent de créer et d’exécuter votre propre logique personnalisée dans Adobe Workfront Fusion, sans quitter l’interface de Fusion. Lorsque les modules standard ne font pas exactement ce dont vous avez besoin, vous pouvez utiliser une fonction pour transformer des données, effectuer un calcul, appeler un service externe ou encapsuler une routine que vous souhaitez réutiliser. Vous pouvez ensuite la tester, la mettre en ligne et l’utiliser à partir de vos scénarios.

Des fonctions complexes peuvent nécessiter des ressources telles que des variables et des dépendances telles que des bibliothèques. Pour ces fonctions, vous pouvez créer un package qui inclut la fonction et ses ressources.

Un package peut inclure :

* **Fonctions** : logique exécutée lors de l’exécution d’un scénario.
* **Variables** : valeurs réutilisables, telles qu’une URL de base ou une clé API, que la fonction du package utilise.
* **Dépendances** : en dehors des bibliothèques sur lesquelles vos fonctions peuvent s’appuyer.
* **Historique** : versions antérieures de chaque fonction, enregistrées automatiquement, que vous pouvez référencer.


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
   <p><ul><li>Si votre organisation dispose d’un package Workfront Select ou Prime qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acquérir Adobe Workfront Fusion.</li><li>Vous devez disposer d’une licence Adobe App Builder pour utiliser des fonctions personnalisées.</ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur le contenu de ce tableau, consultez [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Configurer la connexion à l’environnement d’exécution

>[!NOTE]
>
>Il s’agit d’une configuration unique.

La première fois que votre équipe utilise cette fonctionnalité, vous devez configurer l’environnement qui exécute les fonctions. Vous ne le faites qu&#39;une seule fois par équipe.

1. Cliquez sur l’onglet **Packages** ![Icône Packages](assets/packages-icon.png) dans le panneau de navigation de gauche.

   Si l’environnement n’a pas été configuré, l’écran **Environnement d’exécution non configuré** s’affiche.

1. Cliquez sur **Initialiser l’exécution**.

1. Pour saisir un autre nom que le nom par défaut, saisissez le nom dans le champ **Nom de la connexion**.

1. Sélectionnez le projet Adobe App Builder auquel ce package appartiendra :

   * Pour sélectionner un projet existant, commencez à saisir le nom du projet, puis sélectionnez-le lorsqu’il apparaît.
   * Pour créer un projet, saisissez un nom qui n’existe pas déjà et cliquez sur **Créer**.
   * Si vous laissez ce champ vide, Fusion utilise un projet par défaut.

1. Sélectionnez **Continuer**.

   Fusion termine la configuration et vous êtes prêt à créer des packages.

   Votre environnement s’affiche sous la forme d’un onglet de connexion en haut de la page.

   ![Onglet Environnement comme connexion](assets/package-environment-as-connection.png)

1. (Conditionnel) Pour ajouter un environnement supplémentaire, cliquez sur l’icône Plus et suivez les instructions de cette section.

1. (Conditionnel) Pour supprimer un environnement existant, passez la souris sur l’onglet de connexion de l’environnement et cliquez sur **X** lorsqu’il apparaît.

   >[!WARNING]
   >
   >La suppression d’une connexion déconnecte Fusion de cet environnement. Les packages qu’il contient ne sont plus disponibles dans Fusion via cette connexion.

## Création et ouverture d’un package

1. Cliquez sur l’onglet **Packages** ![Icône Packages](assets/packages-icon.png) dans le panneau de navigation de gauche.

1. Sélectionnez l’onglet de la connexion sur laquelle vous souhaitez travailler.

1. Cliquez sur **Créer un package**.

1. Saisissez un nom et sélectionnez **Créer**.

   Le package s’ouvre automatiquement.

1. Pour rouvrir un package ultérieurement, sélectionnez-le dans la liste Packages et sélectionnez **Afficher**.
1. Pour supprimer un package, sélectionnez-le dans la liste Packages et choisissez **Supprimer**.

   >[!WARNING]
   >
   >La suppression d’un package le supprime définitivement, ainsi que tout son contenu.

## Gestion d’un package

Un package ouvert est organisé en quatre zones :

* **Fonctions** : créez, testez et publiez la fonction.
* **Variables** : configurez les variables de la fonction.
* **Dépendances** : installez des dépendances, telles que des bibliothèques externes, pour cette fonction.
* **Historique** : affichez les versions antérieures de chaque fonction.

En plus de ces quatre zones, un compteur de stockage en haut indique la part de votre espace utilisée. Chaque package est limité à une taille totale de **21 Mo**. Cela inclut les fonctions, les variables et les dépendances, y compris les versions enregistrées.

Si vous manquez d’espace, nous vous recommandons de supprimer les dépendances, variables ou versions antérieures inutilisées pour en libérer.

Pour revenir à la liste des packages, sélectionnez la flèche Précédent en regard du nom du package.

<!--Create toc here-->
* [Fonctions](#functions)
* [Variables](#variables)
* [Dépendances](#dependencies)
* [Historique](#history)

### Fonctions

La zone **Fonctions** affiche une liste des fonctions du package, y compris le nom de la fonction, son statut, sa taille et le nombre d’entrées attendu.

* [Affichage et gestion de la liste des fonctions](#view-and-manage-the-functions-list)
* [Créez ou modifiez une fonction dans la zone Packages](#create-or-edit-a-function-in-the-packages-area)
* [Apporter des modifications à une fonction active](#make-changes-to-a-live-function)
* [Suppression d’une fonction](#delete-a-function)

#### Affichage et gestion de la liste des fonctions

Pour filtrer la liste Fonctions :

1. Filtrez par statut en cliquant sur **Tous**, **Brouillons** ou **Publié**.
1. Utilisez la barre de recherche pour rechercher des fonctions spécifiques.

Une fonction peut avoir le statut brouillon ou publié.

* **Brouillon** : les fonctions à l’état de brouillon sont des travaux en cours. Vous pouvez modifier et tester librement sans affecter les données actives.
* **Publié** : les versions publiées sont en ligne. Vos scénarios exécutent des versions publiées de fonctions.

L’utilisation de brouillons permet d’apporter des modifications en toute sécurité. Vous pouvez affiner un brouillon, le tester, puis le publier lorsque vous êtes satisfait(e).

| Statut | Signification |
|---|---|
| **Publié** | Une version active existe. |
| **Brouillon** | La fonction est toujours en cours ou une fonction active comporte des modifications que vous n&#39;avez pas encore publiées. |

#### Créez ou modifiez une fonction dans la zone Packages

1. Cliquez sur l’onglet **Packages** ![Icône Packages](assets/packages-icon.png) dans le panneau de navigation de gauche.
1. Dans la zone **Fonctions**, sélectionnez **Créer une fonction**.

   Ou

   Cochez la case en regard d’une fonction existante, puis sélectionnez **Modifier** dans la barre d’actions située au bas de la page.

1. (Conditionnel) Si vous créez une fonction, dans le champ **Nouvelle fonction**, saisissez un nom pour la fonction.

1. (Facultatif et conditionnel) Pour renommer une fonction existante, cliquez sur l’icône Modifier en regard du nom de la fonction et saisissez le nouveau nom.

1. Dans l’onglet **Code**, saisissez la logique de la fonction.

   Tenez compte des points suivants lors de la création de votre fonction :

   * Les fonctions doivent être écrites en JavaScript.
   * Vous pouvez lire les entrées que vous définissez, réutiliser vos variables et appeler vos autres fonctions.
   * Lorsque vous tapez, des suggestions s’affichent.

1. Pour nettoyer le formatage des fonctions, cliquez sur **embellir**.

1. (Facultatif) Dans l’onglet **Paramètres**, définissez les entrées attendues par votre fonction.

   Pour plus d’informations sur les entrées, voir [Définir des entrées](#define-inputs) dans cet article.

1. Dans l’onglet **Test**, testez votre fonction.

   Pour obtenir des instructions, voir [Tester une fonction](#test-a-function) dans cet article.

1. Pour enregistrer cette fonction en tant que brouillon, cliquez sur **Enregistrer en tant que brouillon**.

   Ou

   Pour publier la fonction, cliquez sur **Publier**.

   >[!NOTE]
   >
   >La publication d’une fonction efface son historique de versions. La version publiée devient le point de départ actuel et les brouillons précédents ne sont plus conservés.

* [Définir les entrées](#define-inputs)
* [Tester une fonction](#test-a-function)

##### Définir les entrées

Vous pouvez utiliser l’onglet **Paramètres** pour décrire les informations dont votre fonction a besoin à chaque exécution.

1. Cliquez sur l’onglet **Packages** ![Icône Packages](assets/packages-icon.png) dans le panneau de navigation de gauche.
1. Dans la zone **Fonctions**, sélectionnez **Créer une fonction**.

   Ou

   Cochez la case en regard d’une fonction existante, puis sélectionnez **Modifier** dans la barre d’actions située au bas de la page.

1. Cliquez sur l’onglet **Paramètres**.

1. Pour chaque paramètre à ajouter, cliquez sur **Ajouter un paramètre** et configurez les éléments suivants :

* **Name** : nom de l’entrée
* **Libellé** : nom convivial affiché lorsque vous testez la fonction
* **Type** : type de données, tel que du texte, un nombre, true/false ou un objet structuré.
* **Obligatoire** : indique si une valeur doit être fournie.

Ces entrées deviennent les champs que vous renseignez lors du test et les valeurs que votre scénario transmet lorsqu’il exécute la fonction.

##### Tester une fonction

Nous vous recommandons de tester une fonction avant de la publier.

1. Cliquez sur l’onglet **Packages** ![Icône Packages](assets/packages-icon.png) dans le panneau de navigation de gauche.
1. Dans la zone **Fonctions**, sélectionnez **Créer une fonction**.

   Ou

   Cochez la case en regard d’une fonction existante, puis sélectionnez **Modifier** dans la barre d’actions située au bas de la page.

1. Cliquez sur l’onglet **Test**.

1. Saisissez une valeur pour chaque entrée.

1. Exécutez la fonction :

   * Sélectionnez **Tester le brouillon** pour essayer votre version de travail en cours.
   * Sélectionnez **Exécuter publié** pour exécuter la version active.

1. Examinez le résultat, y compris s’il a réussi, combien de temps et la sortie renvoyée.

>[!NOTE]
>
>L’option **Exécuter publié** n’est disponible qu’après la publication d’une fonction.

#### Apporter des modifications à une fonction active

Une fois la fonction publiée, le bouton **Publier** devient un menu :

* **Republier** — Poussez vos dernières modifications de brouillon vers la version active.
* **Dépublier** — mettre la fonction hors service. Votre travail est conservé en tant que brouillon afin que vous puissiez y revenir.

#### Suppression d’une fonction

1. Cliquez sur l’onglet **Packages** ![Icône Packages](assets/packages-icon.png) dans le panneau de navigation de gauche.
1. Cochez la case en regard d’une fonction existante, puis sélectionnez **Supprimer** dans la barre d’actions située au bas de la page.

>[!WARNING]
>
>La suppression d’une fonction la supprime complètement, ainsi que son historique. Tout scénario ou fonction qui l’utilise cessera de fonctionner.

### Variables

Les variables sont des valeurs réutilisables que vos fonctions peuvent utiliser, telles qu’une URL de base, un identifiant de compte ou une clé API. En les stockant en tant que variables, vous définissez une valeur une fois et la mettez à jour à un seul endroit, au lieu de la mettre à jour sur de nombreuses fonctions.

* [Créer ou modifier une variable](#create-or-edit-a-variable)
* [Suppression d’une variable](#delete-a-variable)

#### Créer ou modifier une variable

1. Cliquez sur l’onglet **Packages** ![Icône Packages](assets/packages-icon.png) dans le panneau de navigation de gauche.
1. Dans l’onglet **Variables**, sélectionnez **Nouvelle variable**.

   Ou


   Cliquez sur l’icône **Modifier** en regard de la variable à modifier.

1. Renseignez les détails :

   * **Clé** : saisissez le nom que vos fonctions utilisent pour faire référence à la valeur.

   Pour renommer cette variable, modifiez la valeur Clé .
   * **Valeur** : saisissez la valeur à stocker.
   * **Type** : indiquez si le type de valeur est du texte, un nombre, une valeur booléenne (true/false) ou un objet structuré.
   * **Description** : saisissez une note facultative pour vous rappeler à quoi elle sert.
   * **Public** : activez cette option si vous souhaitez utiliser la variable dans le concepteur de scénarios. Lorsqu’elle est désactivée, la variable n’est disponible que dans les fonctions du package.
   * **Secret** : activez cette option pour masquer les valeurs sensibles, telles que les clés. La valeur est masquée dans la liste des variables et est également assainie afin de ne pas être exposée dans le concepteur de scénarios. Vos fonctions reçoivent toujours la valeur réelle lorsqu’elles s’exécutent.

1. Sélectionnez **Créer une variable** ou **Enregistrer les modifications**.

#### Suppression d’une variable

1. Cliquez sur l’onglet **Packages** ![Icône Packages](assets/packages-icon.png) dans le panneau de navigation de gauche.
1. Dans l’onglet **Variables**, cliquez sur l’icône **Supprimer** en regard de la variable à supprimer.

>[!WARNING]
>
>Les fonctions qui utilisent une variable supprimée cesseront de fonctionner.

### Dépendances

Certaines fonctions nécessitent des bibliothèques supplémentaires pour faire leur travail. L’onglet **Dépendances** vous permet d’ajouter et de gérer ces bibliothèques.

* [Ajout de bibliothèques](#add-libraries)
* [Suppression d’une bibliothèque](#remove-a-library)

#### Ajout de bibliothèques

1. Cliquez sur l’onglet **Packages** ![Icône Packages](assets/packages-icon.png) dans le panneau de navigation de gauche.
1. Dans l’onglet **Dépendances**, saisissez un ou plusieurs noms de bibliothèque, séparés par des virgules. Vous pouvez demander une version spécifique en l’ajoutant après le nom (par exemple, `axios, lodash@4.17.21`).

1. Cliquez sur **Installer**.

#### Suppression d’une bibliothèque

1. Cliquez sur l’onglet **Packages** ![Icône Packages](assets/packages-icon.png) dans le panneau de navigation de gauche.
1. Dans l’onglet **Dépendances**, cliquez sur l’icône **Supprimer** en regard de la bibliothèque à supprimer.

>[!WARNING]
>
>Les fonctions qui reposent sur une bibliothèque supprimée peuvent cesser de fonctionner.

### Historique

Chaque fois que vous enregistrez un brouillon d’une fonction, Fusion conserve une copie. L’onglet **Historique** vous permet d’afficher et de restaurer des versions antérieures.

1. Cliquez sur l’onglet **Packages** ![Icône Packages](assets/packages-icon.png) dans le panneau de navigation de gauche.
1. Dans l’onglet **Historique**, sélectionnez une fonction sur la gauche pour afficher d’abord ses versions enregistrées, la plus récente.
1. Sélectionnez une version pour afficher exactement ce qu’elle contenait à ce moment.
1. Pour restaurer une version, cliquez sur **Restaurer en tant que brouillon**.

   La version est restaurée en tant que nouveau brouillon, afin que vous puissiez la réviser et la tester avant de la publier. Votre version active reste en place jusqu’à la publication.
1. Pour supprimer une version, sélectionnez-la, cliquez sur **Supprimer la version** et confirmez.

>[!NOTE]
>
>* La publication d’une fonction efface son historique. L’historique suit les modifications que vous apportez pendant que vous travaillez sur un brouillon, jusqu’à la publication.
>* La suppression d’une version est irréversible.



## Utilisation d’un package dans un scénario

L’objectif de la création de fonctions et de variables est de les mettre à profit dans vos scénarios. Pour utiliser des fonctions et des variables, utilisez le connecteur **Adobe App Builder**.

* **Utiliser la fonction à partir du package** : ce module exécute l’une de vos fonctions en tant qu’étape d’un scénario. Choisissez le package et la fonction, renseignez les entrées que vous avez définies, et le résultat de la fonction est transmis aux modules qui suivent.
* **Utiliser la variable du package** : ce module intègre l’une de vos variables de package dans un scénario afin que vous puissiez mapper sa valeur à d’autres modules.

Pour obtenir des informations et des instructions, voir [Modules Adobe App Builder](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-app-builder.md).

<!--

To add one:

1. In the scenario designer, add a module and choose the **Adobe App Builder** connector.

1. Select **Use function from package** or **Use variable from package**.

1. Choose the package and the function or variable you want, then map the inputs or value as needed.

>[!NOTE]
>
>Publish a function before using it in a scenario, and turn on **Public** for any variable you want to use there.

-->





