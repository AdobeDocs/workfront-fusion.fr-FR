---
title: Mappage d’un fichier entre des modules
description: Certains modules ont la capacité de traiter des fichiers. Ces modules peuvent soit renvoyer un fichier de sortie à envoyer pour traitement ultérieur, soit exiger qu’un fichier leur soit transmis pour traitement. Avant que ces modules puissent travailler ensemble pour traiter les fichiers, ils doivent être mis en correspondance les uns avec les autres.
author: Becky
feature: Workfront Fusion
exl-id: 25c632f4-169e-4d3c-989a-f57b398bd3f0
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 27%

---

# Mappage d’un fichier entre des modules

Certains modules peuvent traiter des fichiers. Ces modules peuvent renvoyer un fichier de sortie à envoyer pour un traitement ultérieur ou exiger qu’un fichier leur soit transmis pour traitement. Les fichiers peuvent être mappés, de sorte qu’un fichier généré par un module puisse être traité par un autre.

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tout package de workflow Adobe Workfront et tout package d’automatisation et d’intégration Adobe Workfront</p><p>Workfront Ultimate</p><p>les packages Workfront Prime et Select, avec un achat supplémentaire de Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licences Adobe Workfront</td> 
   <td> <p>Standard</p><p>Travail ou supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Si votre entreprise dispose d’un package Select ou Prime Workfront qui n’inclut pas l’automatisation et l’intégration de Workfront, elle doit acheter Adobe Workfront Fusion.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Mappage de fichiers des modules sources vers les modules cibles

Les modules peuvent traiter des fichiers qui nécessitent deux informations :

* Nom du fichier
* Contenu du fichier (données)

Si des modules précédents génèrent un fichier, vous pouvez sélectionner le module source ; le nom et les données du fichier généré par ce module sont mappés au module cible.

Vous pouvez également saisir ce nom et ces données manuellement ou les mapper à partir des modules précédents. Cela peut s’avérer pratique lorsque vous renommez un fichier, par exemple.

>[!NOTE]
>
>Si vous devez traiter un fichier à partir d’une URL, nous vous recommandons d’utiliser le module `HTTP > Get a File` pour télécharger le fichier à partir de l’URL, puis de mapper le fichier du module `HTTP > Get a File` au champ du module souhaité dans votre scénario.
>
>![Mapper un fichier](assets/map-source-file.png)

Pour mapper un fichier :

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez mapper un fichier.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Dans le module cible, qui est la cible que vous mappez, recherchez la zone **Fichier Source**.
1. Pour mapper un fichier généré par un module précédent, sélectionnez le module qui génère le fichier.

   ![Document de téléchargement Workfront](assets/wf-download-document.png)

1. Pour mapper manuellement le nom et les données, sélectionnez Mapper, puis saisissez ou mappez le nom et les données du fichier.

   ![Utilisation de l’option de mappage](assets/use-the-map-option.png)

1. Continuez à configurer le module ou cliquez sur **OK**.
