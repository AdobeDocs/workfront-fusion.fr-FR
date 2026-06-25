---
title: Affichage et gestion des versions de scénario
description: Vous pouvez afficher, restaurer, renommer ou télécharger des plans directeurs pour les versions précédentes d’un scénario.
author: Becky
feature: Workfront Fusion
exl-id: e7fd0351-b840-422c-b861-82ae110c703b
TQID: https://experienceleague.adobe.com/xVihxZH-fwPCIkryQAQEOWgeShtPTMXth4jEl5OLdbo
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 14095350b645736fc64160a94204f828fd5f68c8
workflow-type: tm+mt
source-wordcount: 633
ht-degree: 18%

---

# Affichage et gestion des versions de scénario

Adobe Workfront Fusion enregistre une version de votre scénario à chaque fois qu’il change.

Vous pouvez afficher, restaurer, renommer ou télécharger des plans directeurs pour les versions précédentes d’un scénario.

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

## Affichage et gestion de l’historique des versions d’un scénario

1. Cliquez sur **[!UICONTROL Scénarios]** ![icône Scénarios](assets/scenarios-icon.png) dans le panneau de gauche, puis cliquez sur le scénario pour l’ouvrir.
1. Cliquez sur l’icône [!UICONTROL Plus] ![Plus](assets/more-icon.png) en bas de l’écran, puis sur **[!UICONTROL Versions précédentes]**.

   Une liste des versions précédentes s’affiche.
1. (Facultatif) Pour renommer la version, cliquez sur le menu Plus ![Plus](assets/more-icon-vertical.png) sur la ligne correspondant à cette version, sélectionnez **Modifier**, puis saisissez un nom dans le champ. Cliquez sur **Enregistrer** pour enregistrer le nouveau nom.

   Nous vous recommandons de donner un nom qui décrit les modifications apportées à cette version.
1. (Facultatif) Pour télécharger le plan directeur d’une version précédente, cliquez sur le menu Plus ![Plus](assets/more-icon-vertical.png) sur la ligne correspondant à cette version, puis sélectionnez **Télécharger**.
1. (Facultatif) Pour comparer les modifications entre deux versions, cliquez sur **Afficher les modifications** pour cette version.

   Pour plus d’informations et d’instructions sur la comparaison des versions, voir [Comparer les versions de scénario](#compare-scenario-versions) dans cet article.
1. (Facultatif) Pour restaurer la version, cliquez sur **Restaurer** sur la ligne correspondant à cette version


   >[!NOTE]
   >
   >La version de scénario restaurée n’est pas enregistrée automatiquement. Si vous souhaitez l’enregister, vous devez procéder manuellement.



## Comparaison des versions de scénario

&#x200B;
La fonctionnalité Afficher les modifications indique les différences entre deux versions de scénario, côte à côte, afin que vous puissiez voir exactement ce qui a été modifié avant de décider de restaurer une ancienne version.

1. Cliquez sur **[!UICONTROL Scénarios]** ![icône Scénarios](assets/scenarios-icon.png) dans le panneau de gauche, puis cliquez sur le scénario pour l’ouvrir.
1. Cliquez sur l’icône [!UICONTROL Plus] ![Plus](assets/more-icon.png) en bas de l’écran, puis sur **[!UICONTROL Versions précédentes]**.

   Une liste des versions précédentes s’affiche.
&#x200B;
1. Cliquez sur **Afficher les modifications** pour la version du scénario que vous souhaitez afficher.
1. La vue **Vérifier les modifications** s’ouvre et compare cette version à votre scénario actuel.

   Le panneau Réviser les modifications s’ouvre sur une vue côte à côte de deux versions de scénario.

   * La version actuelle s’affiche sur la gauche.
   * Sur la droite, vous voyez la version sur laquelle vous avez cliqué. Il s’agit de la version que vous pouvez restaurer.

   Pour comprendre les modifications, consultez la section [Examiner les modifications](#examine-changes) de cet article.

1. Pour sélectionner une autre version pour l’un ou l’autre côté, cliquez sur le menu déroulant **Comparer à partir de** ou **Comparer à** près du haut du panneau et sélectionnez une autre version de scénario.
1. Pour permuter les côtés, cliquez sur le bouton ⇄**entre les scénarios.**
1. Pour revenir au scénario sur le côté droit, cliquez sur **Revenir à la version sélectionnée**

   Les versions restaurées sont enregistrées en tant que nouvelles versions et peuvent donc être rétablies à l’avenir.

   Pour revenir au scénario qui se trouve actuellement sur le côté gauche, permutez les côtés afin qu’il se trouve sur la droite, puis cliquez sur **Revenir à la version sélectionnée**.


### Examiner les modifications

&#x200B;
Chaque modification est affichée sur le côté auquel elle appartient et colorée par ce que la restauration ferait
faire :

* Rouge (gauche) : cette modification ne se trouve pas dans la version à droite et serait supprimée si la version était restaurée.
* Vert (droite) : cette modification se trouve dans la version à droite et serait ajoutée si la version était restaurée.

Si quelque chose a été modifié, au lieu d’être supprimé ou ajouté, la valeur s’affiche en rouge à gauche et en vert à droite.
&#x200B;
Les modifications sont regroupées en sections :
&#x200B;

* **Scénario** : nom, description et type.
* **Paramètres du scénario** : options de planification et de traitement.
* **Modules** : modules ajoutés, supprimés, déplacés ou reconfigurés.
* **Flux** : branches ajoutées, supprimées ou réorganisées.
* **Itinéraires du routeur** : Itinéraires et leur contenu.
* **Gestionnaires d’erreurs** : branches de gestion des erreurs.
* **Groupes orphelins** : modules déconnectés sur la zone de travail.
&#x200B;
Si les deux versions sont identiques, la vue affiche le message/ **Aucune différence trouvée**.
&#x200B;
