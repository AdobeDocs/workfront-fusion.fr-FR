---
title: Outils
description: La section  [!DNL Adobe Workfront Fusion Tools]  comprend plusieurs modules utiles qui peuvent améliorer votre scénario.
author: Becky
feature: Workfront Fusion
exl-id: d9425f5b-4f4a-42da-9aca-1c1783be5fa7
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2292'
ht-degree: 86%

---

# [!UICONTROL Outils]

La section [!DNL Adobe Workfront Fusion Tools] comprend plusieurs modules utiles qui peuvent améliorer votre scénario.

[!UICONTROL Outils] les modules sont disponibles à partir de la liste des applications ou à partir de l’icône [!UICONTROL Outils] ![Icône Outils](/help/workfront-fusion/references/apps-and-modules/assets/tools-icon-small.png) située en bas de l’écran.

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
   <td> <p>Nouveau : Standard</p><p>Ou</p><p>En cours : Travail ou version ultérieure</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Licence Adobe Workfront Fusion **</td> 
   <td>
   <p>Aucune exigence de licence Workfront Fusion</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Produit</td> 
   <td>
   <p>Nouveau :</p> <ul><li>Sélectionnez ou le package Prime Workfront : votre entreprise doit acheter Adobe Workfront Fusion.</li><li>Package Ultimate Workfront : Workfront Fusion est inclus.</li></ul>
   <p>Ou</p>
   <p>Actuel : votre entreprise doit acheter Adobe Workfront Fusion.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Pour plus d’informations sur les informations contenues dans ce tableau, voir [Conditions d’accès requises dans la documentation](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Pour plus d’informations sur les licences Adobe Workfront Fusion, voir [Licences Adobe Workfront Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## [!UICONTROL Outils] et leurs champs

* [Déclencheurs](#triggers)
* [Actions](#actions)
* [Agrégateurs](#aggregators)
* [Transformateurs](#transformers)

### Déclencheurs

#### [!UICONTROL Déclencheur de base]

Ce module vous permet de créer un déclencheur personnalisé et de définir ses lots d’entrée.

Vous pouvez utiliser ce module, par exemple, pour les contacts ou toute autre liste dont l’envoi est programmé vers une adresse e-mail spécifiée (comme les modules du type [!UICONTROL E-mail] > [!UICONTROL Envoyer un e-mail], ou [!DNL Gmail] > [!UICONTROL Envoyer un e-mail]), ou en tant que simple rappel à déclencher quand vous le souhaitez.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Bundle]</td> 
   <td> <p>Créez des lots personnalisés en ajoutant des éléments de tableau. Pour chaque élément à ajouter au lot, cliquez sur <b>Ajouter un élément</b> et saisissez le nom et la valeur de l’élément.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [[!UICONTROL Obtenir plusieurs variables]](#get-multiple-variables)
* [[!UICONTROL Obtenir une variable]](#get-variable)
* [[!UICONTROL Fonction « Incrémenter »]](#increment-function)
* [[!UICONTROL Définir plusieurs variables]](#set-multiple-variables)
* [[!UICONTROL Définir une variable]](#set-variable)
* [[!UICONTROL Veille]](#sleep)

#### [!UICONTROL Obtenir plusieurs variables]

Ce module récupère les valeurs qui ont été créées précédemment par le module [!UICONTROL Définir une variable] ou [!UICONTROL Définir plusieurs variables].

Ce module peut lire des variables qui ont été définies n’importe où dans le scénario, même si la variable a été définie dans un itinéraire différent de celui où se trouve le module [!UICONTROL Obtenir plusieurs variables]. La seule condition est que le module [!UICONTROL Outils] > [!UICONTROL Définir une variable] ou [!UICONTROL Outils] > [!UICONTROL Définir plusieurs variables] soit exécuté avant le module [!UICONTROL Outils] > [!UICONTROL Obtenir plusieurs variables]. Pour plus d’informations sur l’ordre dans lequel les modules sont exécutés, voir [Ajouter un module Routeur et configurer des itinéraires](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Variables]</td>
        <td>Pour chaque variable que le module doit obtenir, cliquez sur <b>Ajouter un élément</b> et saisissez le nom de la variable.</td>
    </tr>
</table>

>[!BEGINSHADEBOX]

**Exemples :** vous trouverez ci-dessous des utilisations possibles des modules [!UICONTROL Définir]/[!UICONTROL Obtenir une/plusieurs variable(s)] :

* Pour stocker une valeur calculée en vue d’une utilisation ultérieure, même sur un autre itinéraire. Cela s’avère utile lorsque la valeur est utilisée dans plusieurs modules et que la formule de calcul de la valeur est trop complexe.
* Pour déboguer une formule, procédez comme suit : Si une formule utilisée dans un module ne semble pas donner un résultat correct, copiez-la et collez-la dans un module [!UICONTROL Définir la variable] que vous insérez avant le module concerné. Déconnectez le ou les modules après le module [!UICONTROL Définir la variable] et exécutez le scénario. Vérifiez la sortie du module [!UICONTROL Définir la variable], ajustez ou simplifiez la formule, exécutez à nouveau le scénario, puis continuez jusqu’à ce que le problème soit résolu.

>[!ENDSHADEBOX]


#### [!UICONTROL Obtenir une variable]

Ce module récupère une valeur qui a été créée précédemment par le module [!UICONTROL Définir une variable] ou [!UICONTROL Définir plusieurs variables].

Ce module peut lire les variables qui ont été définies n’importe où dans le scénario, même si la variable a été définie sur un itinéraire différent de celui où se trouve le module [!UICONTROL Obtenir une variable]. La seule condition requise est que le module [!UICONTROL Outils] > [!UICONTROL Définir une variable] ou [!UICONTROL Outils] > [!UICONTROL Définir plusieurs variables] soit exécuté avant l’exécution du module [!UICONTROL Outils] > [!UICONTROL Obtenir une variable]. Pour plus d’informations sur l’ordre dans lequel les modules sont exécutés, voir [Ajouter un module Routeur et configurer des itinéraires](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variable name]</td> 
   <td> <p>Mappez le nom de la variable que vous souhaitez que le module obtienne.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Fonction Incrémenter]

Ce module renvoie une valeur incrémentée de 1 après chaque cycle ou chaque exécution de scénario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reset a value]</td> 
   <td> <p>Sélectionnez cette option lorsque vous souhaitez que le module réinitialise la valeur. C’est à ce moment que vous souhaitez que la valeur recommence à la première valeur.</p> 
    <ul> 
     <li>[!UICONTROL After one cycle]</li> 
     <li>[!UICONTROL After one scenario run]</li> 
     <li>[!UICONTROL Never]</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Exemple :**

Ce module peut être utilisé pour implémenter une affectation « circulaire » de tâches, de prospects, d’e-mails, etc., aux utilisateurs d’un groupe. L’algorithme choisit les personnes cessionnaires d’un groupe dans un ordre rationnel, allant généralement du haut vers le bas d’une liste. Lorsque l’algorithme atteint la fin de la liste, il attribue l’affectation suivante à l’utilisateur ou à l’utilisatrice en haut de la liste et continue à effectuer des affectations vers le bas de la liste.

Le scénario suivant envoie un e-mail à la première personne destinataire après chaque exécution d’un scénario à numéro impair, et à la deuxième personne destinataire après chaque exécution d’un scénario à numéro pair.

![Exemple d’e-mail](/help/workfront-fusion/references/apps-and-modules/assets/example-email.png)

Pour créer ce scénario, procédez comme suit :

1. Définissez le champ **[!UICONTROL Réinitialiser une valeur]** du module sur Jamais.
1. Définissez l’itinéraire des valeurs impaires. Définissez le filtre pour cet itinéraire à l’aide de la fonction mathématique modulaire qui équivaut à `1` :

   ![Nombres impairs](/help/workfront-fusion/references/apps-and-modules/assets/odd.png)

**Note** : n’oubliez pas de modifier l’opérateur [!UICONTROL Égal à] en remplaçant l’opérateur par défaut [!UICONTROL Texte] par l’opérateur [!UICONTROL Numérique].

1. Définissez l’itinéraire des valeurs paires à l’aide de la fonction mathématique modulaire qui équivaut à `0` :

La fonction Incrémenter en ajoute une chaque fois que le scénario s’exécute. Les filtres vérifient l’incrément et agissent sur sa valeur, en s’assurant que les e-mails sont répartis de manière égale.

>[!ENDSHADEBOX]

#### [!UICONTROL Définir plusieurs variables]

Ce module crée des variables qui peuvent être mappées par d’autres modules de l’itinéraire. La variable peut également être mappée aux modules [!UICONTROL Obtenir une variable] ou [!UICONTROL Obtenir plusieurs variables] pour n’importe quel itinéraire dans le scénario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Variables]</td> 
   <td>Pour chaque variable à ajouter, cliquez sur <b>Ajouter un élément</b> et saisissez le nom et la valeur de la variable.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Variable lifetime] </td> 
   <td> <p>Sélectionnez la durée de validité des variables (conservez la même valeur).</p> 
    <ul> 
     <li><strong>[!UICONTROL One cycle]</strong> : la variable est valide pour un cycle. Cela s’avère utile lorsque plusieurs webhooks dans une exécution de scénario sont reçus, car d’autres webhooks créent d’autres cycles. </li> 
     <li><strong>[!UICONTROL One execution]</strong> : la variable est valide pour une exécution de scénario. Une exécution peut contenir un ou plusieurs cycles.</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Définir une variable]

Ce module crée une variable qui peut être mappée par d’autres modules de l’itinéraire. La variable peut également être mappée aux modules [!UICONTROL Obtenir une variable] ou [!UICONTROL Obtenir plusieurs variables] pour n’importe quel itinéraire dans le scénario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Variable name] </td> 
   <td>Saisissez le nom de la variable. Ce nom s’affiche lors du mappage de la variable dans d’autres modules. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Variable lifetime] </td> 
   <td> <p>Sélectionnez la durée de validité des variables (conservez la même valeur).</p> 
    <ul> 
     <li><strong>[!UICONTROL One cycle]</strong> : la variable est valide pour un cycle. Utile lorsque plusieurs webhooks dans un scénario d’exécution sont reçus (plus de webhooks = plus de cycles). </li> 
     <li><strong>[!UICONTROL One execution]</strong> : la variable est valide pour une exécution de scénario. Une exécution peut contenir un ou plusieurs cycles.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Variable value] </td> 
   <td>Saisissez ou mappez la valeur de la variable. </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Veille]

Ce module vous permet de retarder le flux du scénario jusqu’à 300 secondes (5 minutes).

Cette fonction peut s’avérer utile, par exemple, si vous souhaitez réduire la [!DNL target] de chargement du serveur de service ou pour imiter le comportement humain lors de l’envoi de SMS ou d’e-mails en masse.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Delay]</p> </td> 
   <td> <p>Saisissez le nombre de secondes pendant lesquelles le scénario sera suspendu.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!TIP]
>
>Si vous souhaitez suspendre le flux pendant des périodes plus longues, nous vous recommandons de diviser votre scénario en deux scénarios :
>
>* un premier scénario contenant la partie avant la pause,
>* le deuxième scénario contenant la partie après.
>
>Le premier scénario consiste à stocker toutes les informations nécessaires dans un entrepôt de données, ainsi que la date et l’heure actuelles. Le deuxième scénario recherche périodiquement dans l’entrepôt de données des enregistrements dont la date et l’heure sont antérieures au retard prévu, récupère les enregistrements, finalise le traitement des données et supprime les enregistrements de l’entrepôt de données.
>
><!--For more information on data stores, see [Data Stores in Adobe Workfront Fusion]().-->
>
>Pour plus d’informations sur des modules d’entrepôt de données spécifiques, voir [[!UICONTROL modules d’entrepôt de données]](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/data-store-modules.md).

### Agrégateurs

* [[!UICONTROL Agrégateur numérique]](#numeric-aggregator)
* [[!UICONTROL Agrégateur de tableau]](#table-aggregator)
* [[!UICONTROL Agrégateur de texte]](#text-aggregator)

#### [!UICONTROL Agrégateur numérique]

Ce module permet de récupérer des valeurs numériques, puis d’appliquer l’une des fonctions sélectionnées (SUM, AVG, COUNT, MAX, MIN) et de renvoyer le résultat dans un seul lot.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Source module]</p> </td> 
   <td> <p>Sélectionnez le module à partir duquel vous souhaitez agréger les champs.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Aggregate function]</p> </td> 
   <td> <p>Sélectionnez la fonction à utiliser pour agréger les valeurs.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Group by]</p> </td> 
   <td> <p>Définissez une expression selon laquelle vous souhaitez regrouper la sortie agrégée. Cette expression peut contenir un ou plusieurs éléments mappés. Les données agrégées sont ensuite séparées en groupes à l’aide de la valeur de cette expression. Chaque groupe génère un lot distinct avec une clé (l’expression évaluée) et une valeur (la valeur agrégée). Vous pouvez utiliser la clé comme filtre dans les modules suivants.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Stop processing after an empty aggregation]</td> 
   <td>Activez cette option pour arrêter le scénario lorsqu’il n’y a aucun résultat.</td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Value]</p> </td> 
   <td> <p>Saisissez ou mappez la valeur que vous souhaitez agréger.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Agrégateur de tableau]

Ce module fusionne les valeurs des champs sélectionnés des lots reçus en un seul lot à l’aide d’un séparateur de colonne et de ligne spécifié (ce qui vous permet de créer un tableau).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Source module]</p> </td> 
   <td> <p>Sélectionnez le module à partir duquel vous souhaitez agréger les champs.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Aggregated fields]</td> 
   <td> <p> Sélectionnez dans le module sélectionné ci-dessus les champs contenant les valeurs que vous souhaitez agréger dans le lot unique.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Column separator]</p> </td> 
   <td> <p>Sélectionnez ou saisissez le type de séparateur qui séparera les colonnes de valeurs de champ dans le lot obtenu. Si vous sélectionnez [!UICONTROL Other], saisissez le caractère à utiliser pour séparer les valeurs dans le champ du séparateur.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Row separator]</p> </td> 
   <td> <p>Sélectionnez ou saisissez le type de séparateur qui séparera les lignes de valeur de champ dans le lot obtenu. Si vous sélectionnez [!UICONTROL Other], saisissez le caractère à utiliser pour séparer les valeurs dans le champ du séparateur.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Group by]</p> </td> 
   <td> <p>Définissez une expression selon laquelle vous souhaitez regrouper la sortie agrégée. Cette expression peut contenir un ou plusieurs éléments mappés. Les données agrégées seront ensuite séparées en groupes à l’aide de la valeur de cette expression. Chaque groupe génère un lot distinct avec une clé (l’expression évaluée) et une valeur (la valeur agrégée). Vous pouvez utiliser la clé comme filtre dans les modules suivants.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Stop processing after an empty aggregation]</td> 
   <td>Sélectionnez cette option pour arrêter le scénario lorsqu’il n’y a aucun résultat.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Agrégateur de texte]

Ce module fusionne les valeurs des champs sélectionnés des lots reçus en un seul lot.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Source module]</p> </td> 
   <td> <p>Sélectionnez le module à partir duquel vous souhaitez agréger les champs.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Row separator]</p> </td> 
   <td> <p>Sélectionnez ou saisissez le type de séparateur qui séparera les lignes de valeur de champ dans le lot obtenu. Si vous sélectionnez [!UICONTROL Other], saisissez le caractère à utiliser pour séparer les valeurs dans le champ du séparateur.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Group by]</p> </td> 
   <td> <p>Définissez une expression contenant un ou plusieurs éléments mappés. Les données agrégées sont séparées en groupes ayant la même valeur d’expression. Chaque groupe génère une sortie en tant que lot distinct contenant une clé avec l’expression évaluée et le texte agrégé. Ce faisant, vous pouvez utiliser la clé comme filtre dans les modules suivants.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Stop processing after an empty aggregation]</td> 
   <td>Sélectionnez cette option pour arrêter le scénario lorsqu’il n’y a aucun résultat.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Text]</td> 
   <td> <p> Saisissez ou mappez le texte que vous souhaitez que le module agrège.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**Exemple :** vous pouvez utiliser l’agrégateur de texte pour insérer d’autres valeurs (par exemple, les noms de clientes et clients ou les notes) dans un lot unique et envoyer un e-mail contenant toutes les valeurs du corps de l’e-mail ou de son objet.

>[!ENDSHADEBOX]

### Transformateurs

* [[!UICONTROL Composer une chaîne de caractères]](#compose-a-string)
* [[!UICONTROL Convertir l’encodage du texte]](#convert-the-encoding-of-the-text)
* [[!UICONTROL Changer]](#switch)

#### [!UICONTROL Composer une chaîne de caractères]

Convertit n’importe quelle valeur en type de données chaîne de caractères (texte). Cela facilite le mappage lors du mappage, par exemple, de données binaires.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p>Saisissez ou mappez les données que vous souhaitez convertir en texte.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Convertir l’encodage du texte]

Convertit le texte d’entrée saisi (ou les données binaires) en codage sélectionné.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Input data]</p> </td> 
   <td> <p>Saisissez ou mappez le contenu à convertir.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Input data codepage]</td> 
   <td> <p>Sélectionnez le type de codage des données d’entrée. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Output data codepage]</p> </td> 
   <td> <p>Sélectionnez le type d’encodage de vos données cible (sortie).</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Changer]

Vérifie la valeur d’entrée pour une correspondance avec la liste de valeurs fournie. Renvoie une sortie basée sur le résultat.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Input]</p> </td> 
   <td> <p>Saisissez l’expression que vous souhaitez évaluer.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Use regular expressions to match]</td> 
   <td> <p>Activez cette option pour utiliser des expressions régilères. Le module détermine les cas en fonction de l’expression régulière, plutôt qu’en fonction d’une correspondance exacte.</p> 
    <div> 
     <p>Une expression régulière est une séquence de caractères dans laquelle chaque caractère est soit un métacaractère, ayant une signification spéciale, soit un caractère régulier ayant une signification littérale. Ces caractères et métacaractères identifient un motif qui peut être utilisé pour rechercher du texte. Par exemple, si vous souhaitez rechercher des noms, vous pouvez configurer une expression régulière pour rechercher un motif constitué de deux mots consécutifs commençant par des majuscules. Les expressions régulières sont un puissant outil de recherche et de manipulation de texte.</p> 
     <p>Le présent article ne vise pas à aborder la question des expressions régulières. Nous vous recommandons les ressources suivantes :</p> 
     <ul> 
      <li>Pour obtenir la liste complète des métacaractères, voir <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions">Expressions régulières</a> dans la documentation web MDN.</li> 
      <li>Pour consulter un tutoriel sur la création d’expressions régulières, nous vous recommandons <a href="https://regexone.com/">RegexOne</a>.</li> 
      <li>Pour tester des expressions régulières, nous vous recommandons le site web <a href="https://regex101.com/">Regular Expressions 101</a>. Sélectionnez le ECMAScript (JavaScript) FLAVOR dans le panneau de gauche.</li> 
     </ul> 
    </div> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Cases] </td> 
   <td> Pour chaque cas à ajouter, cliquez sur <b>Ajouter un élément</b> et saisissez le modèle et la sortie de l’élément. <p>Si l’entrée contient une valeur saisie dans le champ [!UICONTROL Pattern], la valeur saisie dans le champ [!UICONTROL Output] est renvoyée.</p> <p>Si l’entrée ne correspond à aucune des valeurs que vous avez définies dans un champ [!UICONTROL Pattern], l’un des scénarios suivants se produit :</p> 
    <ul> 
     <li>La valeur du champ [!UICONTROL Else] est renvoyée.</li> 
     <li>Si aucune valeur n’est renseignée dans le champ [!UICONTROL Else], aucune sortie n’est renvoyée.</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Else]</p> </td> 
   <td> <p>Saisissez la valeur renvoyée lorsque les critères définis dans le champ Cases ne sont pas remplis. </p> </td> 
  </tr> 
 </tbody> 
</table>
