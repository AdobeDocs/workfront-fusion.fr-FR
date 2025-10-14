---
title: Mapper des éléments à l’aide de fonctions
description: Lorsque vous mappez des éléments, vous pouvez utiliser des fonctions pour créer des formules simples ou complexes.
author: Becky
feature: Workfront Fusion
exl-id: b9d7643e-febf-42e2-9ddc-8ec8eba98e7a
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 33%

---

# Mapper un élément à l’aide de fonctions

Lorsque vous mappez des éléments, vous pouvez utiliser des fonctions pour créer des formules simples ou complexes. Les fonctions disponibles sont similaires à celles d’Excel et de certains langages de programmation :

* Ils évaluent la logique générale, les mathématiques, le texte, les dates et les tableaux.
* Ils vous permettent d’effectuer une logique conditionnelle et des transformations de valeurs d’élément, telles que la conversion d’un texte en majuscules, le rognage de texte, la conversion d’une date dans un autre format, etc.

## Conditions d’accès

+++ Développez pour afficher les exigences d’accès aux fonctionnalités de cet article.

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Package Adobe Workfront</td> 
   <td> <p>Tous</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licence Adobe Workfront</td> 
   <td> <p>Nouveau : Standard</p><p>Ou</p><p>Actuelle : [!UICONTROL Work] ou niveau supérieur</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licence Adobe Workfront Fusion **</td> 
   <td>
   <p>Actuel : aucune exigence de licence Workfront Fusion.</p>
   <p>Ou</p>
   <p>Héritée : n’importe laquelle. </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Nouveau :</p> <ul><li>Plan Workfront [!UICONTROL Select] ou [!UICONTROL Prime] : votre entreprise doit acheter Adobe Workfront Fusion.</li><li>Plan Workfront [!UICONTROL Ultimate] : Workfront Fusion est inclus.</li></ul>
   <p>Ou</p>
   <p>Actuel : votre entreprise doit acheter Adobe Workfront Fusion.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configurations du niveau d’accès*</td> 
   <td> 
     <p>Vous devez être administrateur ou administratrice Workfront Fusion pour votre entreprise.</p>
     <p>Vous devez être un administrateur Workfront Fusion pour votre équipe.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Insérer des fonctions dans les champs

Pour insérer une fonction dans un champ, procédez comme suit :

1. Cliquez sur l’onglet **[!UICONTROL Scénarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez mapper les données.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Cliquez sur le champ dans lequel vous souhaitez insérer une fonction.
1. Sélectionnez l’onglet dans le panneau de mappage qui contient la fonction que vous souhaitez insérer.

   Pour plus d’informations sur les onglets du panneau de mappage, voir [&#x200B; Présentation des fonctions &#x200B;](/help/workfront-fusion/get-started-with-fusion/understand-fusion/function-overview.md)
   1. Cliquez sur le nom de la fonction.

      Ou

      Faites glisser la fonction dans le champ.
1. Configurez les paramètres de la fonction .

   Pour obtenir une explication des paramètres de fonction, passez la souris sur la fonction dans le panneau de mappage.

   Pour plus d’informations sur les fonctions et leurs paramètres, consultez les articles sous [Références de fonction : index d’article](/help/workfront-fusion/references/mapping-panel/functions/functions-toc.md).

1. Continuez à configurer le module ou cliquez sur **OK**.

>[!TIP]
>
>Lorsque vous créez une formule complexe que vous souhaitez réutiliser dans un autre champ, vous pouvez cliquer sur le champ contenant la combinaison, utiliser Cmd-A ou Ctrl-A pour la sélectionner, puis la copier et la coller dans l&#39;autre champ.


>[!BEGINSHADEBOX]

**Exemple :** certains types de données empêchent les utilisateurs et utilisatrices de saisir plus d’un certain nombre de caractères. Vous pouvez utiliser la fonction substring pour limiter une valeur à un certain nombre de caractères.

Dans cet exemple, la fonction substring limite le nom du projet à 50 caractères.

![Exemple de restriction de durée de réunion](assets/example-meet-length-restriction-350x184.png)

>[!ENDSHADEBOX]

## Imbriquer des fonctions

Vous pouvez imbriquer des fonctions entre elles.

>[!BEGINSHADEBOX]

**Exemple :**

Dans cet exemple, la fonction sous-chaîne limite le nom du projet tronqué à 50 caractères.

![Nom tronqué](assets/trimmed-name-under-50.png)

>[!ENDSHADEBOX]

Pour imbriquer une fonction :

1. Cliquez sur le champ dans lequel vous créez une formule.

   Le panneau de mappage s’ouvre.

1. Cliquez sur la première fonction que vous souhaitez ajouter. C&#39;est la fonction à l&#39;extérieur. Dans l’exemple suivant, il s’agit de la fonction `substring` .
1. Dans cette fonction, cliquez où vous souhaitez que la fonction imbriquée aille. Dans cet exemple, la fonction imbriquée remplace le premier paramètre.
1. Dans le panneau de mappage, cliquez sur la fonction imbriquée . Dans cet exemple, il s’agit de la fonction `trim` .
1. Continuez à configurer la fonction selon vos besoins.
1. Continuez à configurer le module ou cliquez sur **OK**.

## Utiliser des fonctions [!DNL Google Sheets]

Si Workfront Fusion ne comporte pas de fonction que vous souhaitez utiliser, mais qu’elle est présentée par [!DNL Google Sheets], vous pouvez l’utiliser en procédant comme suit :

1. Dans [!DNL Google Sheets], créez une feuille de calcul vide.
1. Dans Workfront Fusion, ouvrez votre scénario.
1. Ajoutez le module **[!DNL Google Sheets]** > **[!UICONTROL Mettre à jour une cellule]** au scénario.

1. Configurez le module :

   1. Sélectionnez la feuille de calcul nouvellement créée dans le champ **[!UICONTROL Feuille de calcul]**.
   1. Insérez votre formule contenant la ou les fonctions [!DNL Google Sheets] dans le champ **[!UICONTROL Valeur]**.

      Vous pouvez utiliser la sortie des modules précédents comme vous le faites habituellement.

      ![Utilisation des fonctions Google Sheets](assets/exploit-google-sheet-functions-350x218.png)

1. Insérez le module **[!UICONTROL Google Sheets] > [!UICONTROL Obtenir une cellule]** pour obtenir le résultat calculé.
1. Configurez le module à l’aide du même ID de cellule que celui utilisé à l’étape 4.

   ![Utilisation des fonctions Google Sheets](assets/exploit-google-sheet-functions-2-350x187.png)
