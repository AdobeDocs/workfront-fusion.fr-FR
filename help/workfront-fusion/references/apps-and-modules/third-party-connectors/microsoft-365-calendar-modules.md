---
title: Calendrier Microsoft Office 365
description: Dans un scénario  [!DNL Adobe Workfront Fusion] , vous pouvez automatiser les workflows qui utilisent le calendrier Microsoft Office 365, et les connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: fdecf740-e735-4569-b1a2-7c25c751ba42
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '1585'
ht-degree: 73%

---

# [!DNL Microsoft Office 365 Calendar]

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!DNL Microsoft Office 365 Calendar] et le connecter à plusieurs applications et services tiers.

Pour utiliser [!DNL Office 365 Calendar] avec [!DNL Adobe Workfront Fusion], vous devez disposer d’un compte [!DNL Office 365 Excel]. Vous pouvez en créer un à l’adresse [www.office.com](https://www.office.com/).

Pour obtenir des instructions sur la connexion de votre compte Office 365 à [!DNL Workfront Fusion], voir [Créer une connexion à Adobe  [!DNL Workfront Fusion]  - Instructions de base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md).

Une fois le consentement accordé, vous êtes redirigé vers la page d’administration de [!UICONTROL Workfront Fusion], où vous pouvez continuer à créer votre scénario.

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

Pour utiliser les modules [!DNL Microsoft Office 365 Calendar], vous devez disposer d’un compte [!DNL Microsoft Office 365 Calendar].

## Informations sur l’API du calendrier Microsoft Office 365

Le connecteur Calendrier Microsoft Office 365 utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td> https://graph.microsoft.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Version de l’API</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v2.0.10</td> 
  </tr>
 </tbody> 
 </table>

## Connexion du service [!DNL Office 365 Calendar] à [!DNL Workfront Fusion].

Pour savoir comment connecter votre compte [!DNL Office 365 Calendar] à [!UICONTROL Workfront Fusion], voir [Créer une connexion à [!UICONTROL Adobe Workfront Fusion] - Instructions de base](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>Certaines applications Microsoft utilisent la même connexion, qui est liée à des autorisations d’utilisateur ou d’utilisatrice. Ainsi, lors de la création d’une connexion, l’écran de consentement aux autorisations affiche les autorisations précédemment accordées à la connexion de cet utilisateur ou de cette utilisatrice, en plus des nouvelles autorisations nécessaires à l’application actuelle.
>
>Par exemple, si un utilisateur ou une utilisatrice dispose d’autorisations « Lire le tableau » accordées via le connecteur Excel, puis crée une connexion dans le connecteur Outlook pour lire les e-mails, l’écran de consentement aux autorisations affiche à la fois l’autorisation « Lire le tableau » déjà accordée et l’autorisation « Écrire des e-mails » nouvellement requise.

## Modules [!DNL Microsoft Office 365 Calendar] et leurs champs

Lorsque vous configurez les modules [!DNL Microsoft Office 365 Calendar], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Microsoft Office 365 Calendar] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Événement](#event)
* [Calendrier](#calendar)
* [Autre](#other)

### Événement

* [[!UICONTROL Watch Events]](#watch-events)
* [[!UICONTROL Search Events]](#search-events)
* [[!UICONTROL Get an Event]](#get-an-event)
* [[!UICONTROL Create an Event]](#create-an-event)
* [[!UICONTROL Update an Event]](#update-an-event)
* [[!UICONTROL Delete an Event]](#delete-an-event)

#### [!UICONTROL Watch Events]

Ce module de déclenchement récupère les détails d’un événement lorsque celui-ci est créé, mis à jour, supprimé, démarré ou se termine dans le calendrier sélectionné.

>[!NOTE]
>
>Pour rechercher les occurrences supprimées d’une série d’événements, sélectionnez [!UICONTROL By Updated Time] dans le champ [!UICONTROL Watch events] . Ce module ne recherche pas les événements uniques supprimés ni les séries d’événements supprimées.


<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch events]</td> 
   <td> <p>Sélectionnez le mode de surveillance des événements.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL By Created Time]</strong> </p> <p>Surveillez les nouveaux événements.</p> </li> 
     <li> <p><strong>[!UICONTROL By Updated Time]</strong> </p> <p>Surveillez les événements mis à jour.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar Group ID]</td> 
   <td>Sélectionnez le [!UICONTROL calendar group] qui contient le calendrier dans lequel vous souhaitez regarder les événements.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar]</td> 
   <td> <p>Sélectionnez le calendrier spécifique à surveiller.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Définissez les conditions de filtrage pour filtrer les résultats par objet, identifiant d’événement ou corps.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Saisissez le nombre maximum de messages que [!DNL Workfront Fusion] doit renvoyer pendant un cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search Events]

Ce module de recherche récupère les détails d’un événement lorsque celui-ci est créé, mis à jour, supprimé, démarré ou se termine dans le calendrier sélectionné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar Group ID]</td> 
   <td>Sélectionnez le [!UICONTROL calendar group] qui contient le calendrier dans lequel vous souhaitez regarder les événements.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar]</td> 
   <td> <p>Sélectionnez le calendrier spécifique à surveiller.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Définissez les conditions de filtrage pour filtrer les résultats. Vous pouvez filtrer selon les propriétés suivantes :</p> 
    <ul> 
     <li>[!UICONTROL Subject]</li> 
     <li>[!UICONTROL Event ID]</li> 
     <li>[!UICONTROL Created Date Time]</li> 
     <li>[!UICONTROL Last Modified Date Time]</li> 
     <li>[!UICONTROL Body Preview]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
   <td> <p>Sélectionnez le mode de classement des résultats.</p> 
    <ul> 
     <li><strong>[!UICONTROL Subject]</strong>, croissant ou décroissant</li> 
     <li><strong>[!UICONTROL Created Date Time]</strong>, croissant ou décroissant</li> 
     <li><strong>[!UICONTROL Last Modified Date Time]</strong>, croissant ou décroissant</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Saisissez le nombre maximal d’événements que [!DNL Workfront Fusion] doit renvoyer pendant un cycle d’exécution de scénario.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an Event]

Ce module d’action récupère les détails de l’événement spécifié.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td> <p>Saisissez ou mappez l’ID de l’événement dont vous souhaitez récupérer les détails.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an Event]

Ce module d’action crée un nouvel événement.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>Saisissez ou mappez un titre pour l’événement créé.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start date]</td> 
   <td> Saisissez le moment où l’événement commence, en indiquant une date et une heure. Utilisez le format <code>({date}T{time}</code>; par exemple, <code>2017-08-29T04:00:00.0000000</code>. Pour obtenir la liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coercition de type dans [!DNL Adobe Workfront Fusion]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End date]</td> 
   <td> Saisissez le moment où l’événement se termine, en indiquant une date et une heure. Utilisez le format <code>{date}T{time}</code> ; par exemple, <code>2017-08-29T04:00:00.0000000</code>. Pour obtenir la liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coercition de type dans [!DNL Adobe Workfront Fusion]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reminder on]</td> 
   <td>Indiquez si vous souhaitez activer un rappel pour cet événement.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reminder]</td> 
   <td>Saisissez ou mappez le nombre de minutes avant le début de l’événement lorsque le rappel doit se déclencher.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>Sélectionnez l’importance de cet événement.</p> 
    <ul> 
     <li>[!UICONTROL Low]</li> 
     <li>[!UICONTROL Medium]</li> 
     <li>[!UICONTROL High]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sensitivity] </td> 
   <td> <p>Sélectionnez la sensibilité de cet événement.</p> 
    <ul> 
     <li><strong>[!UICONTROL Normal]</strong> </li> 
     <li> <p><strong>[!UICONTROL Personal]</strong> </p> <p>Un message « [!UICONTROL Please treat this as Personal] » apparaît.</p> </li> 
     <li> <p><strong>[!UICONTROL Private]</strong> </p> <p>Un message « [!UICONTROL Please treat this as Private] » apparaît. Cet événement n'est pas transféré ou redirigé par les règles de la boîte de réception de la personne destinataire.</p> </li> 
     <li> <p><strong>[!UICONTROL Confidential]</strong> </p> <p>Un message « [!UICONTROL Please treat this as Confidential] » apparaît. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content type]</td> 
   <td>Indiquez si le contenu du corps est en texte brut ou en HTML.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td>Saisissez ou mappez le corps du message associé à l’événement. Il peut s’agir d’un format HTML ou texte (comme spécifié dans le champ [!UICONTROL Body Content Type] ci-dessus).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Location]</td> 
   <td> <p>Saisissez les détails de l’emplacement de l’événement.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Response requested]</td> 
   <td>Sélectionnez <strong>[!UICONTROL Yes]</strong> pour demander à l’invité d’envoyer une réponse à l’invitation à l’événement.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show as]</td> 
   <td> <p>Sélectionnez le mode d’affichage de l’événement pour les personnes qui consultent votre calendrier.</p> 
    <ul> 
     <li>[!UICONTROL Free]</li> 
     <li>[!UICONTROL Tentative]</li> 
     <li>[!UICONTROL Busy]</li> 
     <li>[!UICONTROL Out of office]</li> 
     <li>[!UICONTROL Working elsewhere]</li> 
     <li>[!UICONTROL Unknown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attendees]</p> </td> 
   <td> <p>Ajoutez des personnes participant à l’événement.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Saisissez le nom de la personne participante.</p> </li> 
     <li> <p><strong>[!UICONTROL Email]</strong> </p> <p>Saisissez l’adresse e-mail de la personne participante.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Category]</td> 
   <td>Saisissez ou mappez les catégories que vous souhaitez que l’événement affiche comme sur le calendrier.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update an Event]

Ce module d’action met à jour un événement existant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td>Saisissez, mappez ou sélectionnez l’identifiant de l’événement que vous souhaitez mettre à jour.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>Saisissez ou mappez un titre pour l’événement créé.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start date]</td> 
   <td> Saisissez le moment où l’événement commence, en indiquant une date et une heure. Utilisez le format <code>{date}T{time}</code> ; par exemple, <code>2017-08-29T04:00:00.0000000</code>. Pour obtenir la liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coercition de type dans [!DNL Adobe Workfront Fusion]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End date]</td> 
   <td> Saisissez le moment où l’événement se termine, en indiquant une date et une heure. Utilisez le format <code>({date}T{time}</code> ; par exemple, <code>2017-08-29T04:00:00.0000000</code>. Pour obtenir la liste des formats de date et d’heure pris en charge, voir <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">Coercition de type dans [!DNL Adobe Workfront Fusion]</a>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reminder on]</td> 
   <td>Indiquez si vous souhaitez activer un rappel pour cet événement.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reminder]</td> 
   <td>Saisissez ou mappez le nombre de minutes avant le début de l’événement lorsque le rappel doit se déclencher.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>Sélectionnez l’importance de cet événement.</p> 
    <ul> 
     <li>[!UICONTROL Low]</li> 
     <li>[!UICONTROL Medium]</li> 
     <li>[!UICONTROL High]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sensitivity] </td> 
   <td> <p>Sélectionnez la sensibilité de cet événement.</p> 
    <ul> 
     <li><strong>[!UICONTROL Normal]</strong> </li> 
     <li> <p><strong>[!UICONTROL Personal]</strong> </p> <p>Un message « [!UICONTROL Please treat this as Personal] » apparaît.</p> </li> 
     <li> <p><strong>[!UICONTROL Private]</strong> </p> <p>Un message « [!UICONTROL Please treat this as Private] » apparaît. Cet événement n'est pas transféré ou redirigé par les règles de la boîte de réception de la personne destinataire.</p> </li> 
     <li> <p><strong>[!UICONTROL Confidential]</strong> </p> <p>Un message « [!UICONTROL Please treat this as Confidential] » apparaît. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content type]</td> 
   <td>Indiquez si le contenu du corps du message associé à l’événement est en texte brut ou en HTML.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td>Saisissez ou mappez le corps du message associé à l’événement. Il peut s’agir d’un format HTML ou texte (comme spécifié dans le champ [!UICONTROL Body Content Type] ci-dessus).</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Location]</td> 
   <td> <p>Saisissez les détails de l’emplacement de l’événement.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Response requested]</td> 
   <td>Sélectionnez <strong>[!UICONTROL Yes]</strong> pour demander à l’invité d’envoyer une réponse à l’invitation à l’événement.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show as]</td> 
   <td> <p>Sélectionnez le mode d’affichage de l’événement pour les personnes qui consultent votre calendrier.</p> 
    <ul> 
     <li>[!UICONTROL Free]</li> 
     <li>[!UICONTROL Tentative]</li> 
     <li>[!UICONTROL Busy]</li> 
     <li>[!UICONTROL Out of office]</li> 
     <li>[!UICONTROL Working elsewhere]</li> 
     <li>[!DNL Unknown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attendees]</p> </td> 
   <td> <p>Ajoutez des personnes participant à l’événement.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>Saisissez le nom de la personne participante.</p> </li> 
     <li> <p><strong>[!UICONTROL Email]</strong> </p> <p>Saisissez l’adresse e-mail de la personne participante.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Category]</td> 
   <td>Saisissez ou mappez les catégories que vous souhaitez que l’événement affiche comme sur le calendrier.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an Event]

Ce module d’action supprime un événement existant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td> <p>Saisissez ou mappez l’ID de l’événement que vous souhaitez supprimer.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Calendrier

* [[!UICONTROL List Calendars]](#list-calendars)
* [[!UICONTROL Get a Calendar]](#get-a-calendar)
* [[!UICONTROL Create a Calendar]](#create-a-calendar)
* [[!UICONTROL Update a Calendar]](#update-a-calendar)
* [[!UICONTROL Delete a Calendar]](#delete-a-calendar)

#### [!UICONTROL List Calendars]

Ce module de recherche récupère une liste de tous les calendriers de la personne authentifiée.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar Group ID]</td> 
   <td>Sélectionnez le [!UICONTROL calendar group] qui contient les calendriers à répertorier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Saisissez le nombre maximal de calendriers que [!DNL Workfront Fusion] doit renvoyer pendant un cycle d’exécution de scénario.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Calendar]

Ce module d’action récupère les détails d’un seul calendrier.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar ID]</td> 
   <td> <p>Saisissez ou mappez l’ID du calendrier dont vous souhaitez récupérer les détails.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Calendar]

Ce module d’action crée un nouveau calendrier dans votre compte Google.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar name]</td> 
   <td> <p>Saisissez un nom pour le nouveau calendrier.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a Calendar]

Ce module d’action modifie un calendrier existant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar ID]</td> 
   <td>Saisissez le [!UICONTROL Calendar ID] du calendrier à mettre à jour. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New Calendar name]</td> 
   <td> <p>Saisissez un nom pour le nouveau calendrier.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Calendar]

Ce module d&#39;action supprime un calendrier existant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar ID]</td> 
   <td>Saisissez l’ID [!UICONTROL Calendar] pour le calendrier à supprimer.</td> 
  </tr> 
 </tbody> 
</table>

### Autre

#### [!UICONTROL Make an API Call]

Ce module vous permet d’effectuer un appel API personnalisé.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Office 365] à [!DNL Workfront Fusion], voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion à [!DNL Adobe Workfront Fusion] - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Saisissez un chemin relatif à <code>https://graph.microsoft.com</code>. Exemple :<code> /v1.0/me/events</code></p> </td> 
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
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :   <p>Lors de l’utilisation d’instructions conditionnelles telles que <code>if</code> dans votre fichier JSON, placez les guillemets en dehors de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>
