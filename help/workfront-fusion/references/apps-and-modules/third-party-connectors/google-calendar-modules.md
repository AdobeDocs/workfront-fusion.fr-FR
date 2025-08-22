---
title: Modules du calendrier Google
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent le calendrier Google et les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: 6e514204-cd8e-4f30-bbbb-b8fbe48fc670
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2723'
ht-degree: 67%

---

# Modules [!DNL Google Calendar]

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent le calendrier [!UICONTROL Google] et les connecter à plusieurs applications et services tiers.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

## Conditions d’accès

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Formule Adobe Workfront*</td>
  <td> <p>[!UICONTROL Pro] ou version supérieure</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Licence Adobe Workfront*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licence Adobe Workfront Fusion **</td> 
   <td>
   <p>Exigence de licence actuelle : aucune exigence de licence Workfront Fusion.</p>
   <p>Ou</p>
   <p>Exigence de licence héritée : [!UICONTROL Workfront Fusion for Work Automation and Integration] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Configuration requise actuelle du produit : si vous disposez du plan Adobe Workfront [!UICONTROL Select] ou [!UICONTROL Prime], votre entreprise doit acheter Adobe Workfront Fusion ainsi qu’Adobe Workfront pour utiliser les fonctionnalités décrites dans cet article. Workfront Fusion est inclus dans le plan Workfront [!UICONTROL Ultimate].</p>
   <p>Ou</p>
   <p>Exigences de produit héritées : votre entreprise doit acheter Adobe Workfront Fusion ainsi qu’Adobe Workfront pour utiliser les fonctionnalités décrites dans cet article.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Pour connaître le plan, le type de licence ou l’accès dont vous disposez, contactez votre administrateur ou administratrice Workfront.

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Conditions préalables

Pour utiliser les modules [!DNL Google Calendar], vous devez disposer d’un compte [!DNL Google].

## Informations sur l’API du calendrier Google

Le connecteur Calendrier Google utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td> https://www.googleapis.com/calendar/v3</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Version de l’API</td> 
   <td> v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v5.4.5</td> 
  </tr>
 </tbody> 
 </table>

## Modules [!DNL Google Calendar] et leurs champs

Lorsque vous configurez les modules [!DNL Google Calendar], Workfront Fusion affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Google Calendar] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [Déclencheurs](#triggers)
* [Actions](#actions)
* [Itérateurs](#iterators)

### Déclencheurs

* [Surveiller les événements](#watch-events)
* [Regarder les événements (instantané)](#watch-events-instant)

#### Surveiller les événements

Ce module de déclenchement exécute un scénario lorsqu’un nouvel événement est ajouté, mis à jour, supprimé, démarré ou se termine dans le calendrier que vous indiquez. Le module renvoie tous les champs standard associés à l’enregistrement ou aux enregistrements, ainsi que les champs et valeurs personnalisés auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la procédure de connexion de votre compte [!DNL Google Calendar] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion vers Adobe Workfront Fusion - Instructions de base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar] </td> 
   <td> <p>Sélectionnez le calendrier avec lequel vous souhaitez que le module fonctionne.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td> <p>Choisissez de ne regarder que les nouveaux événements ou les nouveaux événements et toutes les modifications.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show deleted events]</td> 
   <td> <p>Activez cette option pour inclure les événements qui ont été supprimés.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query] </td> 
   <td> <p>Saisissez le texte pour lequel vous souhaitez renvoyer des résultats.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Nombre maximal d'événements]</td> 
   <td> <p> Définissez le nombre maximal d’événements avec lesquels Workfront Fusion fonctionne au cours d’un cycle (le nombre de répétitions par exécution de scénario). Si la valeur est définie sur une valeur trop élevée, la connexion peut être interrompue du côté du service tiers donné (délai d’expiration). Workfront Fusion n’a aucune influence sur ce point. Nous vous recommandons de définir une valeur inférieure et de définir une valeur supérieure pour le nombre maximal de cycles ou d’exécuter le scénario plus fréquemment.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Regarder les événements (instantané)

Ce module de déclenchement utilise un hook pour créer une adresse e-mail que vous pouvez utiliser comme invitation à des événements. Le module démarre un scénario basé sur des événements auxquels l’adresse e-mail est invitée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Mailhook] </td> 
   <td> <p>Sélectionnez le mailhook que vous souhaitez utiliser pour ce module. Pour créer un nouveau mailhook, cliquez sur <b>Ajouter</b> et saisissez la connexion que vous souhaitez utiliser pour le mailhook.</p><p>Pour obtenir des instructions sur la procédure de connexion de votre compte [!DNL Google Calendar] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion vers Adobe Workfront Fusion - Instructions de base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Nombre maximal d'événements]</td> 
   <td> <p> Définissez le nombre maximal d’événements avec lesquels Workfront Fusion fonctionne au cours d’un cycle (le nombre de répétitions par exécution de scénario). Si la valeur est définie sur une valeur trop élevée, la connexion peut être interrompue du côté du service tiers donné (délai d’expiration). Workfront Fusion n’a aucune influence sur ce point. Nous vous recommandons de définir une valeur inférieure et de définir une valeur supérieure pour le nombre maximal de cycles ou d’exécuter le scénario plus fréquemment.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [Créer un calendrier](#create-a-calendar)
* [Création d’un événement](#create-an-event)
* [Suppression d’un événement](#delete-an-event)
* [Obtenir des événements](#get-events)
* [Mettre à jour un événement](#update-an-event)

#### Créer un calendrier

Ce module d&#39;action crée un calendrier associé au compte.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la procédure de connexion de votre compte [!DNL Google Calendar] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion vers Adobe Workfront Fusion - Instructions de base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Color] </td> 
   <td> <p>Sélectionnez la couleur à associer au calendrier.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar name] </td> 
   <td> <p>Saisissez ou mappez un nom pour le nouveau calendrier.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Créer un événement]

Ce module d’action crée un événement.

Vous spécifiez le calendrier et les paramètres de l’événement.

Le module renvoie l’identifiant de l’événement et de tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la procédure de connexion de votre compte [!DNL Google Calendar] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion vers Adobe Workfront Fusion - Instructions de base</a></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar]</td> 
   <td> <p>Choisissez le calendrier dans lequel vous souhaitez que l’événement apparaisse.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Color]</td> 
   <td>Sélectionnez la couleur que l’événement doit afficher dans le calendrier.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event name]</td> 
   <td> <p> Saisissez ou mappez un nom pour l’événement. </p> <p>Remarque : si vous avez sélectionné [!UICONTROL Quick add] dans le champ [!UICONTROL Create an event], vous pouvez inclure la date et l’heure de l’événement, et Workfront Fusion crée l’événement pour cette date et cette heure. Exemple : <code>Appointment at Capitol Hill on June 3rd 10am-10:25am</code>. Si vous avez sélectionné [!UICONTROL Quick add] sans inclure de date et d’heure dans le nom de l’événement, l’événement est créé à partir de l’heure actuelle et dure une heure.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL All day event]</td> 
   <td>Activez cette option si l’événement est un événement qui dure toute la journée (il n’a alors pas besoin d’heure de début ni de fin).</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p>Saisissez ou mappez la date et l’heure de début de l’événement. </p> <p>Pour obtenir la liste des formats de date pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercition</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> Saisissez ou mappez la date et l’heure de fin de l’événement. </p> <p>Pour obtenir la liste des formats de date pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercition</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Description]</td> 
   <td>Saisissez ou mappez une description pour l’événement. Ce champ prend en charge le format HTML.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Location]</td> 
   <td>Saisissez l’emplacement de l’événement dans le formulaire texte.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Use the default reminder settings for this event]</td> 
   <td>Activez cette option pour utiliser les paramètres de rappel par défaut. Si vous définissez un rappel personnalisé dans le champ [!UICONTROL Reminder], cette valeur est définie sur Non.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Reminder] </td> 
   <td> <p>Ajoutez un rappel pour l’événement. Pour chaque rappel à ajouter, cliquez sur <b>Ajouter un élément</b>, puis sélectionnez la méthode avec laquelle vous souhaitez recevoir un rappel et définissez la durée (en minutes) avant l’événement pour lequel vous souhaitez recevoir un rappel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attendees]</td> 
   <td>Ajoutez les personnes participant à l’événement. Pour chaque participant, cliquez sur <b>Ajouter un participant</b>, puis saisissez ou mappez son nom et son adresse e-mail.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show me as]</td> 
   <td>Définissez votre statut sur « Occupé » ou « Disponible » à afficher pour les personnes qui ont accès à votre calendrier lors de cet événement.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Visibility] </td> 
   <td> <p>Sélectionnez la visibilité de cet événement. </p> 
    <ul> 
     <li> <p><b>[!UICONTROL Default]</b></p> <p>La visibilité de l’événement est définie dans les paramètres du calendrier.</p> </li> 
     <li> <p><b>[!UICONTROL Public]</b></p> <p>Toutes les personnes avec qui le calendrier est partagé peuvent voir cet événement.</p> </li> 
     <li> <p><b>[!UICONTROL Private]</b></p> <p>Seules les personnes inscrites peuvent voir cet événement.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notification about the event creation]</td> 
   <td> <p>Choisissez d’envoyer des notifications sur la création d’un nouvel événement à toutes les personnes invitées, à celles qui ne sont pas invitées dans [!DNL Google Calendar], ou à personne.</p> <p>Conseil : nous vous recommandons d’utiliser l’option [!UICONTROL None] uniquement pour les cas de migration.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Guests can modify the event]</td> 
   <td> <p>Activez cette option si vous souhaitez que les personnes invitées puissent modifier cet événement.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Recurrence]</td> 
   <td>Ajoutez des règles de périodicité à cet événement. Chaque règle nécessite une liste de lignes [!UICONTROL RRULE], [!UICONTROL EXRULE], [!UICONTROL RDATE] et [!UICONTROL EXDATE] pour un événement récurrent. Notez que les lignes [!UICONTROL DTSTART] et [!UICONTROL DTEND] ne sont pas autorisées dans ce champ ; les heures de début et de fin de l’événement sont spécifiées dans les champs de début et de fin. Ce champ est omis pour les événements uniques ou les instances d’événements récurrents. Pour plus d’informations, consultez la section <a href="https://tools.ietf.org/html/rfc5545#section-3.8.5">RFC5545</a>.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Supprimer un événement]

Ce module d’action supprime un événement.

Spécifiez le calendrier et l’identifiant d’événement.

Le module renvoie l’identifiant de l’événement et de tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la procédure de connexion de votre compte [!DNL Google Calendar] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion vers Adobe Workfront Fusion - Instructions de base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar]</td> 
   <td> <p>Sélectionnez le calendrier qui contient l’événement que vous souhaitez supprimer.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event ID]</td> 
   <td> <p> Saisissez l’identifiant d’événement de l’événement [!DNL Google Calendar] précédemment créé que vous souhaitez supprimer.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Obtenir des événements]

Ce module récupère des informations sur les événements du calendrier sélectionné en fonction des critères que vous spécifiez.

Vous indiquez le calendrier et les paramètres de la recherche.

Le module renvoie l’identifiant des événements et des champs associés, ainsi que des champs et valeurs personnalisés auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td>Pour obtenir des instructions sur la procédure de connexion de votre compte [!DNL Google Calendar] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion vers Adobe Workfront Fusion - Instructions de base</a></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar]</td> 
   <td> <p>Sélectionnez le calendrier pour lequel vous souhaitez récupérer les événements.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p> Entrez ou mappez la date de début de l’événement. Ce module récupère également les événements qui commencent avant cette date et qui se produisent toujours à la date de début saisie. </p> <p>Pour obtenir la liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercition</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> Saisissez ou mappez la date de fin de l’événement. </p> <p> Pour obtenir la liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercition</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Single events]</td> 
   <td> <p> Activez cette option pour traiter les événements récurrents comme des instances uniques. Par exemple, si vous disposez d’une réunion hebdomadaire et que cette option est activée, le module renvoie la réunion de chaque semaine sous la forme d’un événement distinct.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query]</td> 
   <td> <p>Saisissez ou mappez le terme de recherche souhaité. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Order by]</td> 
   <td> <p>Sélectionnez l’ordre des événements renvoyés dans le résultat.</p> 
    <ul> 
     <li><strong>[!UICONTROL Start Time]</strong> : triez par date et heure de début (croissant). Cette option n’est disponible que lors de l’interrogation d’événements uniques.</li> 
     <li><strong>[!UICONTROL Updated Time]</strong> : triez par heure de dernière modification (croissant).</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Nombre maximal d'événements renvoyés]</td> 
   <td> <p>Définissez le nombre maximal d’événements renvoyés par Workfront Fusion au cours d’un cycle d’exécution.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mettre à jour un événement]

Ce module d’action modifie un événement existant.

Spécifiez le calendrier et l’identifiant d’événement.

Le module renvoie l’identifiant de l’événement et de tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la procédure de connexion de votre compte [!DNL Google Calendar] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion vers Adobe Workfront Fusion - Instructions de base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar] </td> 
   <td> <p>Sélectionnez le calendrier que vous souhaitez utiliser.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event ID] </td> 
   <td> <p>Saisissez l’identifiant d’événement de l’événement [!DNL Google Calendar] précédemment créé que vous souhaitez mettre à jour.</p> </td> 
  </tr>   <tr> 
   <td>[!UICONTROL Event name]</td> 
   <td> <p> Saisissez ou mappez un nom pour l’événement. </p> <p>Remarque : si vous avez sélectionné [!UICONTROL Quick add] dans le champ [!UICONTROL Create an event], vous pouvez inclure la date et l’heure de l’événement, et Workfront Fusion crée l’événement pour cette date et cette heure. Exemple : <code>Appointment at Capitol Hill on June 3rd 10am-10:25am</code>. Si vous avez sélectionné [!UICONTROL Quick add] sans inclure de date et d’heure dans le nom de l’événement, l’événement est créé à partir de l’heure actuelle et dure une heure.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL All day event]</td> 
   <td>Activez cette option si l’événement est un événement qui dure toute la journée (il n’a alors pas besoin d’heure de début ni de fin).</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p>Saisissez ou mappez la date et l’heure de début de l’événement. </p> <p>Pour obtenir la liste des formats de date pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercition</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> Saisissez ou mappez la date et l’heure de fin de l’événement. </p> <p>Pour obtenir la liste des formats de date pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Type coercition</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Description]</td> 
   <td>Saisissez ou mappez une description pour l’événement. Ce champ prend en charge le format HTML.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Location]</td> 
   <td>Saisissez l’emplacement de l’événement dans le formulaire texte.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Use the default reminder settings for this event]</td> 
   <td>Activez cette option pour utiliser les paramètres de rappel par défaut. Si vous définissez un rappel personnalisé dans le champ [!UICONTROL Reminder], cette valeur est définie sur Non.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Reminder] </td> 
   <td> <p>Ajoutez un rappel pour l’événement. Pour chaque rappel à ajouter, cliquez sur <b>Ajouter un élément</b>, puis sélectionnez la méthode avec laquelle vous souhaitez recevoir un rappel et définissez la durée (en minutes) avant l’événement pour lequel vous souhaitez recevoir un rappel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attendees]</td> 
   <td>Ajoutez les personnes participant à l’événement. Pour chaque participant, cliquez sur <b>Ajouter un participant</b>, puis saisissez ou mappez son nom et son adresse e-mail.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show me as]</td> 
   <td>Définissez votre statut sur « Occupé » ou « Disponible » à afficher pour les personnes qui ont accès à votre calendrier lors de cet événement.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Visibility] </td> 
   <td> <p>Sélectionnez la visibilité de cet événement. </p> 
    <ul> 
     <li> <p><b>[!UICONTROL Default]</b></p> <p>La visibilité de l’événement est définie dans les paramètres du calendrier.</p> </li> 
     <li> <p><b>[!UICONTROL Public]</b></p> <p>Toutes les personnes avec qui le calendrier est partagé peuvent voir cet événement.</p> </li> 
     <li> <p><b>[!UICONTROL Private]</b></p> <p>Seules les personnes inscrites peuvent voir cet événement.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notification about the event creation]</td> 
   <td> <p>Choisissez d’envoyer des notifications sur la création d’un nouvel événement à toutes les personnes invitées, à celles qui ne sont pas invitées dans [!DNL Google Calendar], ou à personne.</p> <p>Conseil : nous vous recommandons d’utiliser l’option [!UICONTROL None] uniquement pour les cas de migration.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Guests can modify the event]</td> 
   <td> <p>Activez cette option si vous souhaitez que les personnes invitées puissent modifier cet événement.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Recurrence]</td> 
   <td>Ajoutez des règles de périodicité à cet événement. Chaque règle nécessite une liste de lignes [!UICONTROL RRULE], [!UICONTROL EXRULE], [!UICONTROL RDATE] et [!UICONTROL EXDATE] pour un événement récurrent. Notez que les lignes [!UICONTROL DTSTART] et [!UICONTROL DTEND] ne sont pas autorisées dans ce champ ; les heures de début et de fin de l’événement sont spécifiées dans les champs de début et de fin. Ce champ est omis pour les événements uniques ou les instances d’événements récurrents. Pour plus d’informations, consultez la section <a href="https://tools.ietf.org/html/rfc5545#section-3.8.5">RFC5545</a>.</td> 
  </tr>

</tbody> 
</table>

### Itérateurs

#### Itérer les pièces jointes

Ce module d’action effectue une itération sur les pièces jointes d’un événement et génère chaque pièce jointe dans un lot distinct.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module] </td> 
   <td> Dans ce scénario, sélectionnez le module qui génère l’événement contenant les pièces jointes à itérer. </td> 
  </tr> 
 </tbody> 
</table>

#### Itérer les participants

Ce module d’action effectue une itération sur les participants d’un événement et génère chaque participant dans un lot distinct.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module] </td> 
   <td> Sélectionnez le module dans ce scénario qui génère l’événement contenant les participants que vous souhaitez itérer. </td> 
  </tr> 
 </tbody> 
</table>





## Déclencher un scénario avant un événement

Pour déclencher un scénario à un moment précis avant un événement, utilisez les rappels par e-mails standard de [!DNL Google Calendar] et du module [!UICONTROL Webhooks] > [!UICONTROL Mailhook personnalisé].

1. Utilisez le module [!UICONTROL Calendrier Google] > [!UICONTROL Mettre à jour un événement] pour ajouter un rappel par e-mail à votre événement :

   ![Déclencher un scénario avant l’événement](/help/workfront-fusion/references/apps-and-modules/assets/trigger-scen-before-event-350x209.png)

1. Créez un scénario à partir du module [!UICONTROL Webhooks] >[!UICONTROL Mailhook personnalisé].

   1. Copiez l’adresse e-mail du mailhook.
   1. Enregistrez le scénario et exécutez-le.

1. Dans [!DNL Gmail], redirigez les rappels par e-mail de [!DNL Google Calendar] vers l’adresse e-mail du mailhook :

   1. Ouvrez vos paramètres **[!UICONTROL [!DNL Gmail]]**.
   1. Ouvrez l’onglet **[!UICONTROL Transfert et POP/IMAP]**.
   1. Cliquez sur **[!UICONTROL Ajouter une adresse de transfert].**
   1. Collez l’adresse e-mail copiée du mailhook, cliquez sur **[!UICONTROL Suivant]**, confirmez en appuyant sur **[!UICONTROL Continuer]** dans la fenêtre contextuelle, puis cliquez sur **[!UICONTROL OK]**.

   1. Dans Workfront Fusion, passez au nouveau scénario qui doit terminer son exécution en recevant l’e-mail de confirmation.
   1. Cliquez sur la bulle au-dessus du module pour inspecter la sortie du module.
   1. Développez l’élément `Text` et copiez le code de confirmation :

      ![ Code de confirmation ](/help/workfront-fusion/references/apps-and-modules/assets/confirmation-code-350x252.png)

   1. Dans Gmail, collez le code de confirmation dans la boîte de dialogue de modification et cliquez sur **[!UICONTROL Vérifier]** :

      ![Coller le code](/help/workfront-fusion/references/apps-and-modules/assets/paste-code-350x46.png)

   1. Ouvrez l’onglet **[!UICONTROL Filtres et adresses bloqués]**.
   1. Cliquez sur **[!UICONTROL Créer un filtre]**.
   1. Configurez un filtre pour tous les e-mails provenant de `     calendar-notification@google.com` et cliquez sur **[!UICONTROL Créer un filtre]** :
   1. Sélectionnez **[!UICONTROL Transférer à]** et choisissez l’adresse e-mail du mailhook dans la liste.
   1. Cliquez sur **[!UICONTROL Créer un filtre]** pour créer le filtre.

1. (Facultatif) Dans Workfront Fusion, ajoutez le module [!UICONTROL Analyseur de texte] > [!UICONTROL Modèle de correspondance] après le module [!UICONTROL Webhooks] >[!UICONTROL Custom mailhook] pour analyser le code HTML de l’e-mail afin d’obtenir les informations dont vous avez besoin.

   Par exemple, vous pouvez configurer le module comme suit pour obtenir l’identifiant de l’événement :

   *Motif* : `<meta itemprop="eventId/googleCalendar" content="(?<evenitID>.*?)"/>`

   *Texte* : l’élément `HTML content` produit par le module [!UICONTROL Webhooks] > [!UICONTROL Mailhook personnalisé].
