---
title: Copie de modules ou de scénarios
description: Vous pouvez copier des modules, des groupes de modules ou des scénarios entiers dans Adobe Workfront Fusion. Cette fonctionnalité vous permet de réutiliser des scénarios ou des parties de scénarios sans avoir à les créer à nouveau.
author: Becky
feature: Workfront Fusion
exl-id: 5cece7d4-b2c7-4276-8a6f-f65bad799c7a
source-git-commit: 55fe4bc46bc50ad9ccfd1b234e89028cf3cd12d5
workflow-type: tm+mt
source-wordcount: '845'
ht-degree: 53%

---

# Copie de modules ou de scénarios

Vous pouvez copier des modules, des groupes de modules ou des scénarios entiers dans Adobe Workfront Fusion. Cette fonctionnalité vous permet de réutiliser des scénarios ou des parties de scénarios sans avoir à les créer à nouveau.

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

## Conditions préalables

Les modules doivent exister dans un scénario avant de pouvoir les copier.

## Copier un module ou un groupe de modules

Lorsque vous copiez un module, la copie conserve toutes les valeurs de champ et tous les paramètres du module d’origine.

Vous pouvez coller le module ou les modules dans une autre zone du même scénario ou dans un autre scénario.

Tenez compte des points suivants lorsque vous collez des modules dans un autre scénario :

* Les valeurs de champ qui extraient des informations d’un autre module que vous n’avez pas copié ne peuvent plus accéder à ces informations. Vous devez définir ces champs pour extraire les informations du nouveau scénario.
* Si vous collez les modules dans un scénario appartenant à une autre équipe ou organisation, toutes les connexions doivent être mises à jour vers les connexions appartenant à l’équipe ou à l’organisation propriétaire du nouveau scénario.

### Copier des modules

Copier un groupe de modules revient à copier un module.

1. Cliquez sur l’onglet **[!UICONTROL Scenarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez copier un module.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Cliquez avec le bouton droit sur le module à copier.

   >[!NOTE]
   >
   >Vous pouvez sélectionner plusieurs modules en maintenant la touche [!UICONTROL shift] enfoncée et en cliquant sur les modules à copier. Copier un groupe de modules copie également toutes les lignes de connexion, tous les filtres ou toute logique de routage entre eux.

1. Sélectionnez **[!UICONTROL Copy module]**.
1. Déplacez le curseur vers la zone du scénario où vous souhaitez copier le scénario.
1. Cliquez avec le bouton droit et sélectionnez **[!UICONTROL Paste]**.
1. Connectez les modules collés au scénario en les faisant glisser à l’emplacement souhaité dans le scénario.

   Vous pouvez également utiliser des raccourcis clavier pour copier et coller.

## Copier un scénario par clonage

Le clonage d’un scénario crée une copie du scénario, que vous pouvez ensuite modifier.

1. Ouvrez la page de détails du scénario :

   1. Cliquez sur l’onglet **[!UICONTROL Scenario]** dans le panneau de gauche, puis cliquez sur un scénario dont vous souhaitez obtenir des détails.

      Ou

      Si vous travaillez sur le scénario dans l’éditeur de scénarios, cliquez sur la flèche de gauche ![](assets/exit-editing-arrow.png) près du coin supérieur gauche de la fenêtre.

1. Cliquez avec le bouton droit sur **[!UICONTROL Options]** dans le coin supérieur droit de la page.
1. Sélectionnez **[!UICONTROL Clone]**.
1. (Facultatif) Saisissez un nom pour le nouveau scénario.
1. (Facultatif) Activez **[!UICONTROL Keep the states of any new modules the same as those being duplicated]** pour vous assurer que le scénario copié inclut également des informations sur les enregistrements les plus récents traités par le scénario d’origine.
1. Cliquez sur **[!UICONTROL Save]** pour créer le scénario.

## Copier un scénario à l’aide de plans directeurs

Les plans directeurs du scénario représentent la disposition, le mappage et les valeurs de champ d’un scénario donné à un moment donné. Vous pouvez exporter un plan directeur de scénario dans un fichier JSON sur votre ordinateur, puis l’importer lors de la création d’un scénario. Les scénarios importés à partir d’un plan directeur de scénario peuvent être modifiés.

Un plan directeur de scénario représente l’ensemble du scénario. Si vous souhaitez ne copier que certains modules d’un scénario, reportez-vous à la section [Copier un module ou un groupe de modules](#copy-a-module-or-a-group-of-modules) dans cet article.

### Exporter un plan directeur de scénario

1. Cliquez sur l’onglet **[!UICONTROL Scenarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez exporter un plan directeur.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Dans le scénario, cliquez sur le menu **[!UICONTROL More]** dans la zone des paramètres du scénario.
1. Cliquez sur **[!UICONTROL Export Blueprint]**.

   Un fichier JSON est créé et téléchargé sur votre ordinateur. Vous pouvez localiser ce fichier dans votre dossier [!DNL Downloads].

### Importer un plan directeur

>[!IMPORTANT]
>
>Si vous importez un plan directeur dans un scénario existant, le plan directeur du scénario remplace le scénario existant. Vous ne pouvez pas ajouter un plan directeur à un scénario existant.

1. Commencez par créer un scénario.
1. Dans le scénario, cliquez sur le menu **[!UICONTROL More]** dans la zone des paramètres du scénario.
1. Cliquez sur **[!UICONTROL Import Blueprint]**.
1. Dans la boîte de dialogue qui s’affiche, cliquez sur **[!UICONTROL Browse]**
1. Accédez au plan directeur à importer, puis cliquez sur **[!UICONTROL Open]**.
1. Cliquez sur **[!UICONTROL Save]**.

   Un fichier JSON est créé et téléchargé sur votre ordinateur. Vous pouvez localiser ce fichier dans votre dossier [!UICONTROL Downloads].

## Copier et réutiliser des scénarios à l’aide de modèles

Vous pouvez créer des modèles comme point de départ pour vos scénarios [!DNL Workfront Fusion]. Lorsque vous créez un scénario à partir d’un modèle, vous pouvez modifier le scénario sans modifier le modèle. Les valeurs de champ ne sont pas enregistrées dans les modèles.

Pour plus d’informations sur la création d’un scénario à l’aide d’un modèle, voir [Créer des scénarios avec des modèles](/help/workfront-fusion/create-scenarios/add-modules/create-scenarios-with-fusion-templates.md).

## Dépannage

Si vous copiez et collez des modules comme décrit dans [Copiez un module ou un groupe de modules](#copy-a-module-or-a-group-of-modules) et que rien n’apparaît lorsque vous collez des modules, vérifiez les paramètres du site de votre navigateur pour vous assurer que le collage à partir du presse-papiers est autorisé.
