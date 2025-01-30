---
title: Module Itérateur
description: Un module Itérateur est un type spécial de module qui convertit un tableau en une série de lots. Chaque élément du tableau est généré sous la forme d’un lot.
author: Becky
feature: Workfront Fusion
exl-id: 43d39955-3dd7-453d-8eb0-3253a768e114
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '570'
ht-degree: 28%

---

# Module [!UICONTROL Iterator]

Un [!UICONTROL Iterator] est un type de module qui convertit un tableau en une série de lots. Chaque élément du tableau est généré sous la forme d’un lot.

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
   <td> Nouveau : Standard<p>Ou</p><p>Actuellement : Travail ou licence supérieure</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adobe Workfront Fusion] licence</td> 
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


Pour connaître la formule, le type de licence ou l’accès dont vous disposez, contactez votre équipe d’administration [!DNL Workfront].

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [[!DNL Adobe Workfront Fusion] licences](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Configuration du module [!UICONTROL Iterator]

Le module Itérateur général comporte un seul champ, le champ [!UICONTROL Array]. Ce champ contient le tableau à convertir ou à fractionner en lots distincts.

![Configurer l’itérateur](assets/set-up-iterator.jpg)

D&#39;autres connecteurs peuvent comprendre des modules itérateurs spécifiques à cet itérateur. Ils contiennent un champ de module Source qui vous permet de sélectionner le module qui génère le tableau à itérer.

![Itérateurs spécialisés](assets/specialized-iterators.jpg)

Pour plus d’informations, voir [Configuration d’un module](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md).

>[!BEGINSHADEBOX]

**Exemples :**

* Le scénario ci-dessous montre comment récupérer des e-mails avec des pièces jointes et enregistrer les pièces jointes en tant que fichiers uniques dans un dossier [!DNL Dropbox] sélectionné.

  Les e-mails peuvent contenir un tableau de pièces jointes. Le module [!UICONTROL Iterator] après le premier module permet au scénario de traiter chaque pièce jointe séparément. Le module [!UICONTROL Iterator] divise le tableau de pièces jointes en lots uniques. Chaque lot, accompagné d’une pièce jointe, est ensuite enregistré un par un dans un dossier [!DNL Dropbox] sélectionné. Le champ [!UICONTROL Array] du module Itérateur doit contenir le tableau `Attachments`.

  ![Tableau des pièces jointes](assets/attachments-array.jpg)

>[!ENDSHADEBOX]


## Dépannage

### Problème : le panneau Mappage n’affiche pas les éléments mappables sous le module [!UICONTROL Iterator]

Lorsqu’un module [!UICONTROL Iterator] ne dispose pas d’informations sur la structure des éléments du tableau, le panneau de mappage dans les modules suivant le module [!UICONTROL Iterator] affiche uniquement deux éléments sous le module [!UICONTROL Iterator] : `Total number of bundles` et `Bundle order position`.

![Le panneau Mappage ne s’affiche pas](assets/mapping-panel-doesnt-display.png)

En effet, chaque module est chargé de fournir des informations sur les éléments qu’il génère, de sorte que ces éléments puissent être correctement affichés dans le panneau de mappage dans les modules suivants. Cependant, plusieurs modules peuvent ne pas être en mesure de fournir ces informations dans certains cas. Par exemple, [!UICONTROL JSON] > [!UICONTROL Parse JSON] ou [!UICONTROL Webhooks] > [!UICONTROL Custom Webhook] modules avec une structure de données manquante ne fourniraient pas les informations.

#### Solution

La solution consiste à exécuter manuellement le scénario. Cela force le module à créer une sortie. Fusion peut ensuite appliquer le format de cette sortie aux modules suivants du scénario.

Par exemple, un scénario comprend un module [!UICONTROL JSON] > [!UICONTROL Parse JSON] sans structure de données.

![Analyser la chaîne JSON](assets/json-parse-json.png)

Un module [!UICONTROL Iterator] connecté à ce module JSON ne peut pas mapper la sortie du module au champ Tableau dans le panneau de configuration du module [!UICONTROL Iterator].

![Connecter le module itérateur](assets/connect-iterator-module.png)

Pour résoudre ce problème :

Démarrez manuellement le scénario dans l’éditeur de scénarios.

>[!NOTE]
>
>Pour empêcher l’exécution de l’ensemble du scénario, vous pouvez :
>
>* Annulez le lien entre les modules après le module [!UICONTROL JSON] > [!UICONTROL Parse JSON] pour empêcher le flux de continuer.
>   Ou
>* Cliquez avec le bouton droit sur le module [!UICONTROL JSON] > [!UICONTROL Parse JSON] et choisissez **[!UICONTROL Run this module only]** dans le menu contextuel pour exécuter uniquement le module [!UICONTROL JSON] > [!UICONTROL Parse JSON].

Une fois le [!UICONTROL JSON] > [!UICONTROL Parse JSON] exécuté, il peut fournir des informations sur ses sorties à tous les modules suivants, y compris le module Itérateur. Le panneau de mappage dans la configuration du module Itérateur affiche alors les éléments :

![Le panneau Mappage affiche les éléments](assets/mapping-panel-displays-items.png)

en outre, le panneau de mappage dans les modules connectés après le module [!UICONTROL Iterator] affiche les éléments contenus dans le tableau :

![Éléments contenus dans un tableau](assets/items-contained-in-array.png)
