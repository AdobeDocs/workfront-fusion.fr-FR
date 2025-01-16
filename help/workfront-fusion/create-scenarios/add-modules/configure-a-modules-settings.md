---
title: Configuration d’un module
description: Vous devez configurer les paramètres de chaque module que vous créez.
author: Becky
feature: Workfront Fusion
exl-id: ae82d1fe-31e1-424a-9c1a-42dc1a20b749
source-git-commit: 55fe4bc46bc50ad9ccfd1b234e89028cf3cd12d5
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 42%

---

# Configuration d’un module

Vous devez configurer les paramètres de chaque module que vous créez.

Par exemple, le module Workfront > Charger le document nécessite que vous spécifiiez l’enregistrement dans lequel vous souhaitez charger un document.

>[!NOTE]
>
>Outre les paramètres du module, vous pouvez également ajuster les paramètres d’un scénario. Vous pouvez renommer votre scénario, modifier sa planification et spécifier des paramètres supplémentaires, entre autres actions.

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

## Configurer les paramètres d’un module

1. Cliquez sur l’onglet **[!UICONTROL Scenarios]** dans le panneau de gauche.
1. Sélectionnez le scénario dans lequel vous souhaitez ajouter un filtre.
1. Cliquez n’importe où sur le scénario pour accéder à l’éditeur de scénarios.
1. Ajoutez un nouveau module à un scénario.

   Ou

   Cliquez sur le module que vous souhaitez configurer.

1. Si le module l’exige, créez une **[!UICONTROL Connection]** sur le compte utilisateur enregistré pour ce service donné, comme décrit dans la section [Présentation des connexions](/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md).
1. Dans chaque champ, saisissez le texte approprié.

   Ou

   Mappez la sortie d’un module précédent dans le champ .

   Pour plus d’informations sur le mappage, voir [Présentation du mappage](/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md).

   Pour plus d’informations sur les différents types de données d’élément que [!DNL Workfront Fusion] pouvez reconnaître (tels que la date, le nombre et le texte), voir [Types de données d’élément](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md).

   >[!NOTE]
   >
   >Les paramètres en gras sont requis.

1. (Conditionnel) Si le module comporte des options avancées que vous souhaitez afficher et utiliser, sélectionnez **[!UICONTROL Show advanced settings]**.
