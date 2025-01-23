---
title: Modules du calendrier Google
description: Dans un scénario  [!DNL Adobe Workfront Fusion] , vous pouvez automatiser les workflows qui utilisent le calendrier Google et les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: 6e514204-cd8e-4f30-bbbb-b8fbe48fc670
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '3306'
ht-degree: 83%

---

# Modules [!DNL Google Calendar]

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!UICONTROL Google Calendar] et le connecter à plusieurs applications et services tiers.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

## Conditions d’accès

Vous devez disposer des accès suivants pour utiliser les fonctionnalités de cet article :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] formule*</td>
  <td> <p>[!UICONTROL Pro] ou une version ultérieure</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licence*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licence**</td> 
   <td>
   <p>Exigences de licence actuelles : aucune exigence de licence [!DNL Workfront Fusion] requise.</p>
   <p>Ou</p>
   <p>Ancienne exigence de licence : [!UICONTROL [!DNL Workfront Fusion] pour l’automatisation et l’intégration du travail] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Exigences actuelles du produit : si vous disposez du plan de [!DNL Adobe Workfront] [!UICONTROL Select] ou [!UICONTROL Prime], votre entreprise doit acheter du [!DNL Adobe Workfront Fusion] et [!DNL Adobe Workfront] utiliser les fonctionnalités décrites dans cet article. [!DNL Workfront Fusion] est inclus dans le plan de [!DNL Workfront] [!UICONTROL Ultimate].</p>
   <p>Ou</p>
   <p>Exigences liées aux produits hérités : votre entreprise doit acheter [!DNL Adobe Workfront Fusion] ainsi qu’[!DNL Adobe Workfront] pour utiliser la fonctionnalité décrite dans cet article.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Pour connaître la formule, le type de licence ou l’accès dont vous disposez, contactez votre équipe d’administration [!DNL Workfront].

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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

Lorsque vous configurez les modules [!DNL Google Calendar], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Google Calendar] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Événements](#events)
* [Calendriers](#calendars)
* [Règles de contrôle d’accès](#access-control-rules)
* [Itérateurs (obsolète)](#iterators-deprecated)
* [Autre](#other)

### Événements

* [[!UICONTROL Watch events]](#watch-events)
* [[!UICONTROL Search events]](#search-events)
* [[!UICONTROL Get an event]](#get-an-event)
* [[!UICONTROL Create an event]](#create-an-event)
* [[!UICONTROL Update an event]](#update-an-event)
* [[!UICONTROL Delete an event]](#delete-an-event)


#### [!UICONTROL Watch events]

Ce module de déclenchement exécute un scénario lorsqu’un nouvel événement est ajouté, mis à jour, supprimé, démarré ou se termine dans le calendrier que vous indiquez. Le module renvoie tous les champs standard associés à l’enregistrement ou aux enregistrements, ainsi que les champs et valeurs personnalisés auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Calendar] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à Adobe [!DNL Workfront Fusion] - Instructions de base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar] </td> 
   <td> <p>Sélectionnez le calendrier avec lequel vous souhaitez que le module fonctionne.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch Events]</td> 
   <td> <p>Indiquez si vous souhaitez surveiller les événements par date de création, date de mise à jour, date de début ou date de fin.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show deleted events]</td> 
   <td> <p>Activez cette option pour inclure les événements qui ont été supprimés.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query] </td> 
   <td> <p>Saisissez le texte à rechercher.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p> Définissez le nombre maximal d’événements avec lesquels [!DNL Workfront Fusion] fonctionne pendant un cycle (nombre de répétitions par exécution de scénario). Si la valeur est définie sur une valeur trop élevée, la connexion peut être interrompue du côté du service tiers donné (délai d’expiration). [!DNL Workfront Fusion] n’a aucune influence sur cela. Nous vous recommandons de définir une valeur inférieure et de définir une valeur supérieure pour le nombre maximal de cycles ou d’exécuter le scénario plus fréquemment.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search events]

Ce module d’action recherche un événement dans le calendrier sélectionné.

Vous indiquez le calendrier et les paramètres de la recherche.

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
   <td>[!UICONTROL Calendar ID]</td> 
   <td> <p>Sélectionnez le calendrier que vous souhaitez rechercher.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p> Entrez ou mappez la date de début de l’événement. Ce module récupère également les événements qui commencent avant cette date et qui se produisent toujours à la date de début saisie. </p> <p>Pour obtenir la liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coercition de type dans [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> Saisissez ou mappez la date de fin de l’événement. </p> <p> Pour obtenir la liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coercition de type dans [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
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
     <li><strong>[!UICONTROL Start Time]</strong>: classez par date et heure de début (croissant). Cette option n’est disponible que lors de l’interrogation d’événements uniques.</li> 
     <li><strong>[!UICONTROL Updated Time]</strong>: Classez par heure de dernière modification (ascendante).</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p>Définissez le nombre maximal d’événements que [!DNL Workfront Fusion] renvoie pendant un cycle d’exécution.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an event]

Ce module d’action renvoie les métadonnées d’un événement unique dans le calendrier indiqué.

Vous indiquez le calendrier et l’événement.

Le module renvoie l’identifiant de l’événement et tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Calendar] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à Adobe [!DNL Workfront Fusion] - Instructions de base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar ID]</td> 
   <td> <p>Saisissez ou mappez l’identifiant du calendrier qui contient l’événement que vous souhaitez obtenir.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event ID] </td> 
   <td> <p>Saisissez l’identifiant d’événement de l’événement [!DNL Google Calendar] existant que vous souhaitez obtenir.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an event]

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
   <td>[!UICONTROL Create an Event]</td> 
   <td> <p>Sélectionnez le mode de création de l’événement.</p> 
    <ul> 
     <li><b>[!UICONTROL In Detail]</b><p>Cette option vous permet de fournir plus de détails sur l’événement.<br></p></li> 
     <li><b>[!UICONTROL Quickly]</b><p>Il vous suffit de sélectionner le calendrier et de saisir un nom pour l’événement. Vous pouvez inclure des informations sur l’heure et l’endroit dans le nom, et [!DNL Google Calendar] planifiera l’événement pour cet endroit et cette heure.</p></li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar ID]</td> 
   <td> <p>Choisissez le calendrier dans lequel vous souhaitez que l’événement apparaisse.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Color]</td> 
   <td>Sélectionnez la couleur que l’événement doit afficher dans le calendrier.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event name]</td> 
   <td> <p> Saisissez ou mappez un nom pour l’événement. </p> <p>Note : Si vous avez sélectionné [!UICONTROL Quick add] dans le champ [!UICONTROL Create an event], vous pouvez inclure la date et l'heure de l'événement et [!DNL Workfront Fusion] crée l'événement pour cette date et cette heure. Exemple : <code>Appointment at Capitol Hill on June 3rd 10am-10:25am</code>. Si vous avez sélectionné [!UICONTROL Quick add] mais n’incluez pas de date ni d’heure dans le nom de l’événement, l’événement est créé à partir de l’heure actuelle et dure une heure.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL All day event]</td> 
   <td>Activez cette option si l’événement est un événement qui dure toute la journée (il n’a alors pas besoin d’heure de début ni de fin).</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p>S’il s’agit d’un événement qui dure toute la journée, saisissez la date de début de l’événement. </p> <p>Pour obtenir la liste des formats de date pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coercition de type dans [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> S’il s’agit d’un événement qui dure toute la journée, saisissez la date de fin de l’événement. </p> <p>Pour obtenir la liste des formats de date pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coercition de type dans [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
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
   <td>Activez cette option pour utiliser les paramètres de rappel par défaut. Si vous définissez un rappel personnalisé dans le champ [!UICONTROL Reminder] , cette valeur est définie sur Non.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Reminder] </td> 
   <td> <p>Ajoutez un rappel pour l’événement. Pour chaque rappel, sélectionnez la méthode que vous souhaitez utiliser pour le rappel et définissez la durée (en minutes) qui précède l’événement pour lequel vous souhaitez obtenir ce rappel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attendees]</td> 
   <td>Ajoutez les personnes participant à l’événement. Pour chaque personne participant, saisissez ou mappez son nom et son adresse e-mail.</td> 
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
   <td> <p>Choisissez d’envoyer des notifications sur la création d’un nouvel événement à toutes les personnes invitées, à celles qui ne sont pas invitées dans [!DNL Google Calendar], ou à personne.</p> <p>Conseil : nous vous recommandons d’utiliser l’option [!UICONTROL None] uniquement pour les cas d’utilisation de migration.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Guests can modify the event]</td> 
   <td> <p>Activez cette option si vous souhaitez que les personnes invitées puissent modifier cet événement.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Recurrence]</td> 
   <td>Ajoutez des règles de périodicité à cet événement. Chaque règle nécessite une liste de lignes [!UICONTROL RRULE], [!UICONTROL EXRULE], [!UICONTROL RDATE] et [!UICONTROL EXDATE] pour un événement récurrent. Notez que les lignes [!UICONTROL DTSTART] et [!UICONTROL DTEND] ne sont pas autorisées dans ce champ ; les heures de début et de fin de l’événement sont spécifiées dans les champs de début et de fin. Ce champ est omis pour les événements uniques ou les instances d’événements récurrents. Pour plus d’informations, consultez la section <a href="https://tools.ietf.org/html/rfc5545#section-3.8.5">RFC5545</a>.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update an event]

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
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Calendar] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à Adobe [!DNL Workfront Fusion] - Instructions de base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar] </td> 
   <td> <p>Sélectionnez le calendrier que vous souhaitez utiliser.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event ID] </td> 
   <td> <p>Saisissez l’identifiant d’événement de l’événement [!DNL Google Calendar] précédemment créé que vous souhaitez mettre à jour.</p> </td> 
  </tr> 
 </tbody> 
</table>

Pour actualiser les informations relatives à l’événement, il suffit de saisir de nouvelles valeurs dans le champ souhaité. Pour plus d’informations sur les différents champs, voir [[!UICONTROL Create an event]](#create-an-event).

#### [!UICONTROL Delete an event]

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
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Calendar] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à Adobe [!DNL Workfront Fusion] - Instructions de base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar ID]</td> 
   <td> <p>Sélectionnez le calendrier qui contient l’événement que vous souhaitez supprimer.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event ID]</td> 
   <td> <p> Saisissez l’identifiant d’événement de l’événement [!DNL Google Calendar] précédemment créé que vous souhaitez supprimer.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notification about the event deletion]</td> 
   <td>Indiquez si vous souhaitez envoyer des notifications sur la suppression d’événement à toutes les personnes invitées, aux personnes invitées qui n’utilisent pas [!DNL Google Calendar] ou à personne.</td> 
  </tr> 
 </tbody> 
</table>

### Calendriers

* [[!UICONTROL List calendars]](#list-calendars)
* [[!UICONTROL Get a calendar]](#get-a-calendar)
* [[!UICONTROL Create a calendar]](#create-a-calendar)
* [[!UICONTROL Update a calendar]](#update-a-calendar)
* [[!UICONTROL Delete a calendar]](#delete-a-calendar)
* [[!UICONTROL Clear a calendar]](#clear-a-calendar)

#### [!UICONTROL List calendars]

Ce module d’action renvoie les calendriers sur la liste des calendriers d’une personne.

Le module renvoie l’identifiant du calendrier et tous les champs associés, ainsi que tous les champs et valeurs personnalisés auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Calendar] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à Adobe [!DNL Workfront Fusion] - Instructions de base</a></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Minimum access role]</td> 
   <td> <p>Sélectionnez le rôle d’accès minimal pour la personne. Le module renvoie des calendriers en fonction de ce rôle d’accès minimal.</p> 
    <ul> 
     <li><strong>[!UICONTROL Free Busy Reader]</strong>: l’utilisateur ou l’utilisatrice peut lire les informations de disponibilité. </li> 
     <li><strong>[!UICONTROL Owner]</strong>: l’utilisateur peut lire et modifier des événements et peut accéder à des listes de contrôle. </li> 
     <li><strong>[!UICONTROL Reader]</strong>: l’utilisateur ou l’utilisatrice peut lire des événements qui ne sont pas privés. </li> 
     <li><strong>[!UICONTROL Writer]</strong>: l’utilisateur peut lire et modifier des événements.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show hidden calendars]</td> 
   <td>Activez cette option pour inclure les calendriers masqués dans la liste que le module renvoie.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Définissez le nombre maximal de calendriers que [!DNL Workfront Fusion] renvoie pendant un cycle d’exécution.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a calendar]

Ce module d’action permet de récupérer un calendrier.

Vous indiquez l’identifiant du calendrier que vous souhaitez récupérer.

Le module renvoie l’identifiant de l’enregistrement et de tous les champs associés, ainsi que les champs personnalisés et les valeurs auxquels la connexion a accès. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Calendar] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à Adobe [!DNL Workfront Fusion] - Instructions de base</a></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar ID]</td> 
   <td> <p>Sélectionnez le calendrier que vous souhaitez récupérer.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a calendar]

Ce module d’action crée un calendrier.

Spécifiez un nom pour le calendrier.

Le module renvoie l’identifiant du calendrier et tous les champs associés, ainsi que tous les champs et valeurs personnalisés auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Calendar] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à Adobe [!DNL Workfront Fusion] - Instructions de base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar name]</td> 
   <td> <p> Saisissez un nom pour le nouveau calendrier.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a calendar]

Ce module d’action met à jour un calendrier.

Vous indiquez l’identifiant du calendrier que vous souhaitez mettre à jour.

Le module renvoie l’identifiant du calendrier et tous les champs associés, ainsi que tous les champs et valeurs personnalisés auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Calendar] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à Adobe [!DNL Workfront Fusion] - Instructions de base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar ID]</td> 
   <td> <p>Sélectionnez le calendrier à mettre à jour.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar name]</td> 
   <td> <p> Saisissez un nouveau nom pour le calendrier.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a calendar]

Ce module d’action supprime un calendrier.

Indiquez l’identifiant du calendrier que vous souhaitez supprimer.

Le module renvoie l’identifiant du calendrier et tous les champs associés, ainsi que tous les champs et valeurs personnalisés auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Calendar] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à Adobe [!DNL Workfront Fusion] - Instructions de base</a></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar ID]</td> 
   <td> <p>Saisissez ou mappez l’identifiant du calendrier que vous souhaitez supprimer.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Clear a calendar]

Ce module d’action supprime tous les événements du calendrier principal d’un compte.

Vous indiquez la connexion au compte qui contient le calendrier à effacer.

Le module renvoie l’identifiant du calendrier et tous les champs associés, ainsi que tous les champs et valeurs personnalisés auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Google Calendar] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à Adobe [!DNL Workfront Fusion] - Instructions de base</a></p> </td> 
  </tr> 
 </tbody> 
</table>

### Règles de contrôle d’accès

* [[!UICONTROL List access control rules]](#list-access-control-rules)
* [[!UICONTROL Get an access control rule]](#get-an-access-control-rule)
* [[!UICONTROL Create an access control rule]](#create-an-access-control-rule)
* [[!UICONTROL Update an access control rule]](#update-an-access-control-rule)
* [[!UICONTROL Delete an access control rule]](#delete-an-access-control-rule)

#### [!UICONTROL List access control rules]

Ce module d’action renvoie les règles de la liste de contrôle d’accès sur un calendrier.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Calendar] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à Adobe [!DNL Workfront Fusion] - Instructions de base</a></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar ID]</td> 
   <td> <p>Sélectionnez le calendrier qui contient les règles de contrôle d’accès que vous souhaitez récupérer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Définissez le nombre maximum de résultats que [!DNL Workfront Fusion] renvoie au cours d’un cycle d’exécution.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an access control rule]

Ce module d’action renvoie les métadonnées d’une règle de contrôle d’accès.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Calendar] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à Adobe [!DNL Workfront Fusion] - Instructions de base</a></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar ID]</td> 
   <td> <p>Sélectionnez le calendrier qui contient la règle de contrôle d’accès que vous souhaitez récupérer.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Access control rule ID]</td> 
   <td>Sélectionnez la règle de contrôle d’accès que vous souhaitez récupérer.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an access control rule]

Ce module d’action crée une nouvelle règle de contrôle d’accès.

Spécifiez un nom pour le calendrier.

Le module renvoie l’identifiant de la règle de contrôle d’accès et tous les champs associés, ainsi que tous les champs et valeurs personnalisés auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Calendar] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à Adobe [!DNL Workfront Fusion] - Instructions de base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar ID]</td> 
   <td> <p>Sélectionnez le calendrier dans lequel vous souhaitez créer une règle de contrôle d’accès.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Role]</td> 
   <td> <p>Sélectionnez le rôle à affecter à la règle d’accès. </p> 
    <ul> 
     <li><strong>[!UICONTROL Free Busy Reader]</strong>: l’utilisateur ou l’utilisatrice peut lire les informations de disponibilité. </li> 
     <li><strong>[!UICONTROL Owner]</strong>: l’utilisateur peut lire et modifier des événements et peut accéder à des listes de contrôle. </li> 
     <li><strong>[!UICONTROL Reader]</strong>: l’utilisateur ou l’utilisatrice peut lire des événements qui ne sont pas privés. </li> 
     <li><strong>[!UICONTROL Writer]</strong>: l’utilisateur peut lire et modifier des événements.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Type]</td> 
   <td> <p>Sélectionnez le type de portée. </p> 
    <ul> 
     <li><strong>[!UICONTROL Default]</strong>: portée publique. Il s’agit de la valeur par défaut. </li> 
     <li><strong>[!UICONTROL User]</strong>: limite la portée à un seul utilisateur. </li> 
     <li><strong>[!UICONTROL Group]</strong>: limite la portée à un groupe. </li> 
     <li><strong>[!UICONTROL Domain]</strong>: limite la portée à un domaine. </li> 
    </ul> <p>Remarque : les autorisations accordées à la portée [!UICONTROL Default] ou publique s’appliquent à tout utilisateur, authentifié ou non.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Value]</td> 
   <td>Saisissez l’adresse e-mail d’un utilisateur ou d’une utilisatrice ou d’un groupe, ou le nom d’un domaine, en fonction du type de portée.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notifications]</td> 
   <td> <p>Activez cette option pour envoyer des notifications sur le changement d’accès. </p> <p>Note : il n’y a pas de notification pour la suppression d’accès. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update an access control rule]

Ce module d’action met à jour une règle de contrôle d’accès.

Spécifiez un nom pour le calendrier.

Le module renvoie l’identifiant de la règle de contrôle d’accès et tous les champs associés, ainsi que tous les champs et valeurs personnalisés auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Calendar] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à Adobe [!DNL Workfront Fusion] - Instructions de base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar ID]</td> 
   <td> <p>Sélectionnez le calendrier qui contient la règle de contrôle d’accès que vous souhaitez mettre à jour.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Access control rule ID]</td> 
   <td>Sélectionnez la règle de contrôle d’accès que vous souhaitez mettre à jour.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Role]</td> 
   <td> <p>Sélectionnez le rôle à affecter à la règle d’accès. </p> 
    <ul> 
     <li><strong>[!UICONTROL None]</strong>: ce rôle ne fournit aucun accès.</li> 
     <li><strong>[!UICONTROL Free Busy Reader]</strong>: l’utilisateur ou l’utilisatrice peut lire les informations de disponibilité. </li> 
     <li><strong>[!UICONTROL Owner]</strong>: l’utilisateur peut lire et modifier des événements et peut accéder à des listes de contrôle. </li> 
     <li><strong>[!UICONTROL Reader]</strong>: l’utilisateur ou l’utilisatrice peut lire des événements qui ne sont pas privés. </li> 
     <li><strong>[!UICONTROL Writer]</strong>: l’utilisateur peut lire et modifier des événements.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notifications]</td> 
   <td> <p>Activez cette option pour envoyer des notifications sur le changement d’accès. </p> <p>Note : il n’y a pas de notification pour la suppression d’accès. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an access control rule]

Ce module d’action supprime une règle de contrôle d’accès.

Spécifiez un nom pour le calendrier.

Le module renvoie l’identifiant de la règle de contrôle d’accès et tous les champs associés, ainsi que tous les champs et valeurs personnalisés auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Calendar] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à Adobe [!DNL Workfront Fusion] - Instructions de base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar ID]</td> 
   <td> <p>Sélectionnez ou mappez l’identifiant du calendrier qui contient la règle de contrôle d’accès que vous souhaitez supprimer.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Access control rule ID]</td> 
   <td>Sélectionnez ou mappez l’identifiant de la règle de contrôle d’accès que vous souhaitez supprimer.</td> 
  </tr> 
 </tbody> 
</table>

### Itérateurs (obsolète)

Les modules [!UICONTROL iterate attachments] et [!UICONTROL iterate attendees] ont été rendus obsolètes. Pour itérer les pièces jointes ou les participants, utilisez le module [!UICONTROL Flow Control] > [!UICONTROL Iterator] . Pour plus d’informations, voir [Module Itérateur](/help/workfront-fusion/references/modules/iterator-module.md)

### Autre

* [[!UICONTROL Make an API Call]](#make-an-api-call)
* [[!UICONTROL Get Free/Busy Information]](#get-freebusy-information)

#### [!UICONTROL Make an API Call]

Ce module vous permet d’effectuer un appel API personnalisé.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Google Calendar] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à Adobe [!DNL Workfront Fusion] - Instructions de base</a></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td>Saisissez un chemin relatif à <code>https://www.googleapis.com/calendar</code>. Exemple : <code>/v3/users/me/calendarList</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   td&gt; <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard. Par exemple : <code>{"Content-type":"application/json"}</code>. [!DNL Workfront Fusion] ajoute les en-têtes d’autorisation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> Ajoutez la requête pour l’appel API sous la forme d’un objet JSON standard.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :   <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre JSON, placez les guillemets à l’extérieur de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Free/Busy Information]

Ce module d’action renvoie les informations relatives aux informations de disponibilité concernant les statuts libre et occupé d’un ensemble de calendriers.

Le module renvoie l’identifiant du calendrier et tous les champs associés, ainsi que tous les champs et valeurs personnalisés auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

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
   <td>[!UICONTROL Minimum time]</td> 
   <td> <p> Saisissez le début de l’intervalle pour lequel vous souhaitez obtenir des informations.</p> <p> Pour une liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coercition de type dans [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum time]</td> 
   <td> <p> Saisissez la fin de l’intervalle de temps pour lequel vous souhaitez récupérer les informations. </p> <p>Pour une liste des formats de date et de temps pris en charge, consultez la section <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coercition de type dans [!DNL Adobe Workfront Fusion]</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendars]</td> 
   <td> <p>Pour chaque calendrier dont vous souhaitez récupérer les informations, cliquez sur <strong>Ajouter</strong> et saisissez ou mappez l’identifiant du calendrier.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Déclencher un scénario avant un événement

Vous pouvez déclencher un scénario à une heure spécifiée avant un événement à l’aide des rappels par e-mail [!DNL Google Calendar] standard et du module [!UICONTROL Webhooks] > [!UICONTROL Custom mailhook] .

1. Utilisez le module [!UICONTROL Google Calendar] >[!UICONTROL Update an event] pour ajouter un rappel par e-mail à votre événement :

   ![](/help/workfront-fusion/references/apps-and-modules/assets/trigger-scen-before-event-350x209.png)

1. Créez un nouveau scénario à partir du module [!UICONTROL Webhooks] > [!UICONTROL Custom mailhook] .

   1. Copiez l’adresse e-mail du mailhook.
   1. Enregistrez le scénario et exécutez-le.

1. Dans [!DNL Gmail], redirigez les rappels par e-mail de [!DNL Google Calendar] vers l’adresse e-mail du mailhook :

   1. Ouvrez votre **[!UICONTROL [!DNL Gmail] settings]**.
   1. Ouvrez l’onglet **[!UICONTROL Forwarding and POP/IMAP]** .
   1. Cliquez sur **[!UICONTROL Add a forwarding address].**
   1. Collez l&#39;adresse e-mail du crochet copié, cliquez sur&#x200B;**[!UICONTROL Next]**, confirmez en appuyant sur **[!UICONTROL Proceed]** dans la fenêtre contextuelle, puis cliquez sur **[!UICONTROL OK]**.

   1. Dans [!DNL Workfront Fusion], passez au nouveau scénario qui devrait terminer son exécution après avoir reçu l’e-mail de confirmation.
   1. Cliquez sur la bulle au-dessus du module pour inspecter la sortie du module.
   1. Développez l’élément `Text` et copiez le code de confirmation :

      ![](/help/workfront-fusion/references/apps-and-modules/assets/confirmation-code-350x252.png)

   1. Dans Gmail, collez le code de confirmation dans la zone d’édition, puis cliquez sur &#x200B; **[!UICONTROL Verify]** :

      ![](/help/workfront-fusion/references/apps-and-modules/assets/paste-code-350x46.png)

   1. Ouvrez l’onglet **[!UICONTROL Filters and Blocked Addresses]** .
   1. Cliquez sur **[!UICONTROL Create a new filter]**.
   1. Configurez un filtre pour tous les e-mails provenant de `     calendar-notification@google.com` et cliquez sur &#x200B;**[!UICONTROL Create a filter]** :
   1. Sélectionnez **[!UICONTROL Forward it to]** et choisissez l’adresse e-mail du crochet de messagerie dans la liste.
   1. Cliquez sur **[!UICONTROL Create filter]** pour créer le filtre.

1. (Facultatif) Dans [!DNL Workfront Fusion], ajoutez le module [!UICONTROL Text parser] > [!UICONTROL Match pattern] après le module [!UICONTROL Webhooks] > [!UICONTROL Custom mailhook] pour analyser le code d’HTML de l’e-mail et obtenir les informations dont vous avez besoin.

   Par exemple, vous pouvez configurer le module comme suit pour obtenir l’identifiant de l’événement :

   *Motif* : `<meta itemprop="eventId/googleCalendar" content="(?<evenitID>.*?)"/>`

   *Texte* : élément `HTML content` généré à partir du module [!UICONTROL Webhooks] >[!UICONTROL Custom mailhook].
