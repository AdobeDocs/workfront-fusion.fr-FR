---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: connections-annd-webhooks
title: Gérer les connexions
description: Pour la plupart des applications, vous devez créer une connexion, avec laquelle  [!DNL Adobe Workfront Fusion]  peut communiquer avec le service tiers donné en fonction des paramètres du scénario.
author: Becky
feature: Workfront Fusion
exl-id: 26d7caad-8e12-4f04-ac7c-f71686c90ee6
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 47%

---

# Gérer les connexions

Une connexion représente l’autorisation et les droits utilisés par Fusion pour accéder à l’application. Vous pouvez créer une ou plusieurs connexions pour chaque application et utiliser la même connexion dans plusieurs modules ou scénarios.

Vous pouvez gérer ces connexions dans la zone Connexions .

Pour plus d’informations sur les connexions, voir [ Présentation de la connexion ](/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md).

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

## Affichage et gestion des connexions

Vous pouvez gérer toutes les connexions à partir de la zone Connexions .

>[!NOTE]
>
>Les connexions appartiennent à des équipes. Si vous ne trouvez pas la connexion que vous recherchez, vérifiez que vous consultez l’équipe appropriée.
>
>Pour sélectionner une nouvelle équipe, cliquez sur le nom de l’équipe dans le volet de navigation de gauche, puis sélectionnez une nouvelle équipe.

1. Pour ouvrir la zone Connexions, cliquez sur **Connexions** ![Icône Connexions](assets/connections-icon.png) dans le volet de navigation de gauche.
1. Recherchez la connexion à gérer, puis effectuez une ou plusieurs des étapes suivantes dans la ligne pour cette connexion.
1. (Facultatif) Attribuez un environnement et un type de connexion en cliquant sur les listes déroulantes **Environnement** et **Type** et en sélectionnant une option.
1. (Facultatif) Pour afficher les autorisations accordées à Workfront Fusion pour la connexion, cliquez sur l’icône Affichage ![Afficher les autorisations de connexion](assets/view-connection-permissions.png) pour cette connexion.
1. (Facultatif) Pour renommer une connexion, mettez en surbrillance son nom et saisissez le nouveau nom.
1. (Facultatif) Pour réautoriser une connexion, cliquez sur **Réautoriser**.
1. (Facultatif) Pour supprimer une connexion, cliquez sur **Supprimer**, puis sur **Vraiment ?**.
1. (Facultatif) Pour vérifier que la connexion au service a été établie avec succès, cliquez sur **Vérifier**.

## Renouveler une connexion

[!DNL Workfront Fusion] obtient généralement des droits d’accès à un service donné pendant une période illimitée. Certaines applications exigent que l’autorisation d’accès soit renouvelée après un certain temps. Dans ce cas, [!DNL Workfront Fusion] vous avertit par e-mail peu de temps avant l’expiration de ses droits d’accès.

Pour renouveler une connexion :

1. Pour ouvrir la zone Connexions, cliquez sur **Connexions** ![Icône Connexions](assets/connections-icon.png) dans le volet de navigation de gauche.
1. Recherchez la connexion à renouveler.
1. Dans la ligne correspondant à cette connexion, cliquez sur le bouton **[!UICONTROL Reauthorize]** dans la zone de **[!UICONTROL Connections]**.

## Ressources

* Pour plus d’informations sur les métadonnées de connexion, telles que l’environnement et le type, consultez [Métadonnées de connexion](/help/workfront-fusion/references/connections/connection-metadata.md).
