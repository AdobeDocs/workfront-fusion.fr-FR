---
title: Mappage des informations d’un module à un autre
description: Le mappage désigne le processus d’affectation des sorties d’un module, structurées en éléments, aux champs d’entrée d’un autre.
author: Becky
feature: Workfront Fusion
exl-id: 1e3f7729-f48e-451e-a90b-d680c9e3bcbc
source-git-commit: 55fe4bc46bc50ad9ccfd1b234e89028cf3cd12d5
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 35%

---

# Mappage des informations d’un module à un autre

Le mappage est le processus d’affectation des sorties d’un module aux champs d’entrée d’un autre module.

Le panneau de mappage s’affiche lorsque vous cliquez sur un champ dans lequel vous pouvez insérer une valeur générée par un module précédent dans un scénario.

Vous pouvez également créer une formule à l’aide de n’importe quelle combinaison de fonctions et d’éléments mappés du panneau de mappage avec du texte statique que vous saisissez. Ces éléments peuvent être imbriqués les uns dans les autres.

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

## Mapper un élément

Après avoir créé une séquence de modules en les liant, chaque module peut traiter les valeurs des éléments générés par les modules qui le précèdent.

Pour affecter des éléments de sortie aux champs d’entrée d’un module :

1. Cliquez sur l’onglet **[!UICONTROL Scenarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez mapper les données.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Cliquez sur le module qui doit traiter la sortie du ou des modules précédents.
1. Dans le panneau Paramètres du module qui s’affiche, cliquez sur un champ dans lequel vous souhaitez utiliser la valeur d’un élément généré par un module précédent.

   Le panneau de mappage s’ouvre.

1. (Facultatif) Pour trouver un champ spécifique dans le panneau de mappage, cliquez sur la barre de recherche du panneau de mappage et saisissez le terme souhaité. Cliquez sur le champ lorsqu’il apparaît dans la liste.

   Les résultats de recherche contiennent le terme de recherche et ne sont pas sensibles à la casse.
1. Pour sélectionner une valeur qui est un élément d&#39;une collection, cliquez sur la flèche en regard de cette collection, puis sélectionnez l&#39;élément lorsqu&#39;il apparaît.

   ![Élément de collection](assets/collection-dropdown.png)

1. Cliquez sur un élément du panneau de mappage pour l’insérer dans le champ.

Pour plus d’informations, voir [Configuration d’un module](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md).


## Dépannage

### Problème : éléments manquants dans le panneau de mappage

Le panneau de mappage affiche les éléments de sortie des modules précédents. Il peut arriver que certains éléments soient absents de ce panneau. Vous pouvez exécuter le module dont la sortie est manquante dans l’éditeur de scénarios, puis le panneau de mappage peut inclure ces éléments dans les modules ultérieurs. La procédure exacte varie en fonction du type de module

* [Déclencheur instantané](#instant-trigger)
* [Déclencheur d’attente active](#polling-trigger)
* [Autres modules](#other-modules)

#### Déclencheur instantané

1. Cliquez avec le bouton droit sur le module , puis cliquez sur **[!UICONTROL Run this module only]** dans le menu qui s’affiche.

   Comme il s’agit d’un déclencheur instantané, il commence à surveiller les événements.

1. Créez l’événement que le module regarde.

   Par exemple, si le module est un module Workfront > Observer les événements qui surveille les affectations de tâche, connectez-vous à Workfront (en tant qu’utilisateur autre que celui utilisé par la connexion Fusion) et affectez une tâche.

1. Lorsque l’exécution du module est terminée, cliquez sur la bulle au-dessus du module pour explorer sa sortie complète.

   Le panneau de mappage pour les modules ultérieurs contient désormais tous les éléments dans la sortie du module.

#### Déclencheur d’attente active

1. Cliquez avec le bouton droit sur le module , puis cliquez sur **[!UICONTROL Run this module only]** dans le menu qui s’affiche.
1. S’il n’y a pas de sortie, cliquez sur **[!UICONTROL Choose where to start]** et ajustez les paramètres.
1. (Conditionnel) S’il n’y a aucun événement à traiter, créez l’événement que le module surveille et répétez l’étape 2.

   Par exemple, si le module est un module Workfront > Observer les enregistrements qui surveille les affectations de tâche, connectez-vous à Workfront (en tant qu’utilisateur autre que celui utilisé par la connexion Fusion) et attribuez une tâche, puis réexécutez le module.

1. Lorsque l’exécution du module est terminée, cliquez sur la bulle au-dessus du module pour explorer sa sortie complète.

   Le panneau de mappage pour les modules ultérieurs contient désormais tous les éléments dans la sortie du module.

#### Autres modules

Vous pouvez choisir d’exécuter les éléments suivants :

* L’ensemble du scénario (ou seulement la partie contenant le module)
* Le module unique

Pour exécuter le module unique :

1. Cliquez avec le bouton droit sur le module, puis cliquez sur **[!UICONTROL Run this module only]** dans le menu qui s&#39;affiche.
1. Fournissez des exemples de valeurs pour les éléments d’entrée, puis cliquez sur **[!UICONTROL OK]** .
1. Lorsque l’exécution du module est terminée, cliquez sur la bulle au-dessus du module pour explorer sa sortie complète.

   Le panneau de mappage pour les modules ultérieurs contient désormais tous les éléments dans la sortie du module.
