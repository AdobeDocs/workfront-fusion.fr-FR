---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Créer un scénario de base
description: Découvrez comment créer un scénario d’automatisation simple avec Adobe Workfront Fusion. Les scénarios d’automatisation permettent d’automatiser les processus Workfront, y compris la manipulation et la transformation des données. Cet exemple vous guide tout au long du processus de création d’un scénario qui recherche une tâche  [!DNL Workfront]  dans Workfront et la convertit en projet.
author: Becky
feature: Workfront Fusion
exl-id: 5284dee1-e890-4357-a28d-29e09ac02822
source-git-commit: 8884aef2237ad358c774110b81ac17b9efb386d4
workflow-type: tm+mt
source-wordcount: '1305'
ht-degree: 27%

---

# Créer un scénario de base

Le rôle d’[!DNL Adobe Workfront Fusion] consiste à automatiser vos processus afin que vous puissiez vous concentrer sur de nouvelles tâches, plutôt que de répéter les mêmes tâches encore et encore. La plateforme fonctionne en liant les actions dans et entre les applications et les services pour créer un scénario qui transfère et transforme vos données automatiquement. Le scénario que vous créez recherche les données dans une application ou un service et traite ces données pour obtenir le résultat souhaité.

Cet exemple vous guide tout au long du processus de création d’un scénario qui recherche une requête dans Workfront et la convertit en projet.

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] paquet</td> 
   <td> <p>Tous</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licence</td> 
   <td> <p>Nouveau : [!UICONTROL Standard]</p><p>Ou</p><p>En cours : [!UICONTROL Work] ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licence**</td> 
   <td>
   <p>Actuelle : aucune exigence de licence [!DNL Workfront Fusion] requise.</p>
   <p>Ou</p>
   <p>Héritée : n’importe laquelle. </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Nouveau :</p> <ul><li>[!UICONTROL Select] ou [!UICONTROL Prime] plan de [!DNL Workfront] : votre entreprise doit acheter des [!DNL Adobe Workfront Fusion].</li><li>[!UICONTROL Ultimate] [!DNL Workfront] plan : [!DNL Workfront Fusion] est inclus.</li></ul>
   <p>Ou</p>
   <p>Actuel : votre entreprise doit acheter [!DNL Adobe Workfront Fusion].</p>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++



## Créer un scénario pratique

### Commencer à créer le scénario

1. Dans la zone **Scénarios**, cliquez sur **Créer un scénario**.

   Pour localiser la zone des Scénarios, voir [Accès à Workfront Fusion](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/navigate-workfront-fusion.md).

   L’éditeur de scénarios s’affiche, contenant un module vide au centre.

1. Sélectionnez le nom de l’espace réservé **[!UICONTROL New scenario]** dans le coin supérieur gauche, puis saisissez un nom.
1. Continuez avec [ Ajouter et configurer le premier module ](#add-and-configure-the-first-module).

### Ajouter et configurer le premier module

1. Cliquez sur le module vide pour choisir l’application à partir de laquelle vous allez sélectionner un module.

   Une liste d&#39;applications s&#39;affiche à droite du module.

1. Sélectionnez **[!DNL Adobe Workfront]**. S’il n’est pas visible, cliquez sur la barre de recherche au bas de la liste, saisissez « Workfront », puis sélectionnez-le lorsqu’il apparaît dans la liste.

   La liste est modifiée afin d’afficher tous [!DNL Workfront] modules que vous pouvez utiliser.

1. Cliquez sur le module **[!UICONTROL Search]** .

   La fenêtre de configuration du module s’ouvre.

1. Dans la zone de [!UICONTROL Connection], sélectionnez votre connexion Workfront.

   Si vous ne disposez pas d’une connexion Workfront, voir [Créer une connexion](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)
1. Dans la zone de [!UICONTROL Record Type], sélectionnez **[!UICONTROL Issue]**. Cette option permet au module de rechercher uniquement les événements, notamment les requêtes.

   Vous pouvez trouver des **[!UICONTROL Issue]** dans la liste si vous commencez à taper le mot « [!UICONTROL Issue] ».

1. Dans la zone de **[!UICONTROL Result Set]**, sélectionnez **[!UICONTROL First Matching Record]**.

   Cela définit le module pour renvoyer uniquement le premier enregistrement qu’il trouve et qui répond aux critères.
1. Dans la zone **[!UICONTROL Search criteria]** , configurez les critères pour renvoyer la tâche spécifique.

   1. Dans la première zone sous [!UICONTROL Search Criteria], sélectionnez le champ que vous souhaitez inclure dans votre recherche. Pour cet exemple, sélectionnez **[!UICONTROL Name]**.

      Vous pouvez trouver des **[!UICONTROL Name]** dans la liste si vous commencez à taper le mot « [!UICONTROL name] ».
   1. Pour l’opérateur/opératrice, cliquez sur la flèche de liste déroulante en regard de **Exist** et remplacez-la par [!UICONTROL **Contient (non-respect de la casse)**].

      Cela permet au module de trouver des projets dont le nom contient les mots que vous avez choisis, même si vous ne saisissez pas le nom en entier ou si vous saisissez le nom avec une casse incorrecte (par exemple, tout en majuscules).
   1. Dans le dernier champ sous [!UICONTROL Search Criteria], saisissez un mot ou une expression dont vous savez qu’il se trouve dans le nom de la tâche que vous recherchez.

1. Dans la liste **[!UICONTROL Outputs]**, sélectionnez les champs que le module doit afficher. Pour cet exemple, sélectionnez les champs **[!UICONTROL ID]** et **[!UICONTROL Name]** .

   >[!TIP]
   >
   >Vous pouvez utiliser **Cmd+F** (système d’exploitation [!DNL Mac]) ou **Ctrl+F** (système d’exploitation [!DNL Windows]) pour trouver rapidement un champ.

1. Cliquez sur **[!UICONTROL OK]** pour enregistrer la configuration du module.

1. Cliquez avec le bouton droit sur le module, cliquez sur **[!UICONTROL Rename]**, puis saisissez un nom décrivant ce que vous souhaitez que le module fasse (par exemple, « Rechercher des requêtes »), puis cliquez sur **[!UICONTROL OK]**.

   Le nom apparaît juste en dessous du module. En dessous, [!DNL Workfront Fusion] inclut une brève description du type d’action effectuée par le module.

   ![](assets/module-renamed-wf.png)

1. Continuez avec [Ajouter et configurer le deuxième module](#add-and-configure-the-second-module).

## Ajouter et configurer le deuxième module

1. Pointez sur le cercle partiel à droite de la balise du module, puis cliquez sur **[!UICONTROL Add another module]**.
1. Sélectionnez [!DNL Adobe Workfront] dans la liste des applications, puis choisissez le module **[!UICONTROL Convert object]**.
1. Dans le champ [!UICONTROL Connection] , sélectionnez la même connexion Workfront que celle utilisée dans le module précédent .
1. Dans le champ **[!UICONTROL Record type]** , sélectionnez **[!UICONTROL issue]**, car le module convertira un événement.
1. Dans le champ **[!UICONTROL Convert to]** , sélectionnez **Projet**.
1. En regard du champ ID de tâche , cliquez sur le bouton (bascule) de mappage pour l’activer.

   Le bouton bascule devient bleu lorsqu’il est activé. Vous pouvez ainsi mapper l’identifiant de tâche du module précédent.

   ![Basculement de carte](assets/map-toggle.png)
1. Cliquez sur le champ **[!UICONTROL Task ID]** .

   Un panneau s’ouvre, vous permettant de sélectionner les éléments à utiliser comme identifiant de la tâche à convertir en projet. Étant donné que vous avez activé le mappage, le panneau inclut la sortie de tous les modules précédents. Vous avez sélectionné ID comme sortie du module précédent. Il est donc désormais disponible dans le panneau.

   Ce panneau est appelé panneau de mappage. Pour plus d’informations sur le panneau de mappage, voir [Présentation du mappage](/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md).
1. Sélectionnez **ID** dans le panneau de mappage.

   Un bloc d’identifiant s’affiche dans le champ d’identifiant. Il indique le numéro du module à partir duquel il est mappé, ainsi que le champ qui est mappé.

   ![Identifiant de carte](assets/map-id.png)

1. Cliquez sur le champ **ID du modèle**, commencez à saisir le nom du modèle Workfront que vous souhaitez utiliser pour ce projet, puis sélectionnez-le lorsqu’il apparaît dans la liste.
1. Cliquez sur **[!UICONTROL OK]** pour enregistrer la configuration du module.

1. Cliquez avec le bouton droit sur le module, cliquez sur **[!UICONTROL Rename]**, puis saisissez un nom décrivant ce que vous souhaitez que le module fasse (par exemple, « Convertir en projet »), puis cliquez sur **[!UICONTROL OK]**.

1. Continuez pour [Tester le scénario](#test-the-scenario).

## Tester le scénario

Avant d’activer votre scénario, il est important de le tester en l’exécutant au moins une fois et en visualisant les résultats. Cela vous permet de comprendre comment les données circulent dans le scénario et de détecter les éventuelles erreurs.

Dans ce scénario, un test réussi permet de localiser la requête et de la convertir en projet.

1. Cliquez sur **[!UICONTROL Run once]** dans le coin inférieur gauche de l’éditeur de scénarios.
1. Une fois l’exécution du scénario terminée, cliquez sur la bulle située au-dessus du premier module pour afficher des informations sur le lot de données traité par le module, y compris les données extraites de la requête renvoyée par le module.

1. Cliquez sur la bulle de l’inspecteur d’exécution au-dessus du deuxième module pour afficher l’entrée (la requête) et la sortie (le projet converti).

   Pour plus d&#39;informations sur les données des bulles d&#39;inspection, voir :

   * Pour obtenir des informations générales, voir [Flux d’exécution de scénario](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md).
   * Pour plus d’informations sur les lots traités, voir [Exécution de scénario, cycles et phases](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).

1. Dans [!DNL Workfront Fusion], cliquez sur **[!UICONTROL Save]** près du coin inférieur gauche pour enregistrer votre progression dans le scénario.

   >[!IMPORTANT]
   >
   >Sauvegardez souvent lorsque vous affinez et testez un scénario.

>[!TIP]
>
>Nous vous recommandons d’ajouter des notes sur chaque module, ce qui est facultatif mais utile.
>
>1. Cliquez avec le bouton droit sur un module, puis sélectionnez **[!UICONTROL Add a note]**.
>1. Dans la note qui s’affiche, saisissez un aperçu du module.
>
>    Vous pouvez ajouter plusieurs notes pour un module.
>
>1. Fermez la zone de **[!UICONTROL Notes]**.
>
>     Une fois que vous avez ajouté une note à un scénario, un point orange s’affiche sur l’icône **[!UICONTROL Notes]** ![](assets/notes-icon-w-dot.png) en bas de l’éditeur de scénarios.
>
>1. Cliquez sur l’icône **[!UICONTROL Notes]** ![](assets/notes-icon-w-dot.png) pour afficher vos notes.
>

## Activer le scénario

La dernière étape de la création d’un scénario consiste à l’activer.

Ce scénario recherchant un problème spécifique, il n’est pas nécessaire de l’activer. L’activation d’un scénario entraîne son exécution selon un planning ou lorsqu’une action spécifique se produit dans une application. Une fois que vous avez activé un scénario, celui-ci s’exécute par défaut toutes les 15 minutes. Vous pouvez modifier cela en définissant quand et à quelle fréquence vous souhaitez qu’il s’exécute.

Pour plus d’informations sur l’activation des scénarios, voir [ Activer ou désactiver un scénario](/help/workfront-fusion/manage-scenarios/activate-deactivate-scenarios.md).

Pour plus d’informations sur les planifications, voir [Planification d’un scénario](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

## Étapes suivantes

* [Ajoutez un module de déclenchement](/help/workfront-fusion/build-practice-scenarios/add-a-webhook-to-basic-scenario.md) pour permettre au scénario de rechercher régulièrement de nouvelles requêtes et de les convertir en projets.
* [Ajoutez un webhook](/help/workfront-fusion/build-practice-scenarios/add-a-webhook-to-basic-scenario.md) pour permettre l’exécution du scénario à chaque fois qu’une requête est saisie.
* [Ajoutez un filtre](/help/workfront-fusion/build-practice-scenarios/add-filter-basic-scenario.md) pour vous assurer que seules certaines requêtes sont converties en projets.
* [Ajoutez une fonction](/help/workfront-fusion/build-practice-scenarios/use-function-to-build-practice-scenario.md) qui personnalise le nom du nouveau projet.
