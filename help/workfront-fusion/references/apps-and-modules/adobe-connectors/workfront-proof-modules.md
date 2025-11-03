---
title: Modules Workfront Proof
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent  [!DNL Workfront Proof], et le connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion, Workfront Proof, Digital Content and Documents
exl-id: 9e556ae5-e672-4872-9c40-8c8e5f0305be
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: tm+mt
source-wordcount: '3106'
ht-degree: 80%

---

# Modules [!DNL Workfront Proof]

Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent [!DNL Workfront Proof] et les connecter à plusieurs applications et services tiers.

Cela s’avère utile si vous devez exécuter des tâches actuellement non prises en charge dans les relectures sous Workfront ou dans [!DNL Workfront Proof], comme la mise à jour de BAT en fonction de certains événements et la recherche des destinataires d’un BAT.

Le connecteur [!DNL Workfront Proof] n’est pas comptabilisé dans le nombre d’applications actives disponibles pour votre organisation. Tous les scénarios, même s’ils utilisent uniquement l’application [!DNL Workfront Proof], sont comptabilisés dans le nombre total de scénarios de votre entreprise.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

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

+++## informations sur Workfront Proof

Le connecteur Workfront Proof utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Version de l’API</td> 
   <td> v21.3.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.8.92</td> 
  </tr>
 </tbody> 
 </table>

## Connecter [!DNL Workfront Proof] à Workfront Fusion

Vous pouvez créer une connexion à votre compte [!DNL Workfront Proof] directement depuis un module Workfront Fusion.

1. Dans un module Workfront Fusion, cliquez sur [!UICONTROL **Ajouter**] en regard du champ [!UICONTROL Connexion]

2. Remplissez les champs suivants :

   <table style="table-layout:auto"> 
        <col/>
        <col/>
        <tbody>
            <tr>
                <td role="rowheader">
                    <p role="rowheader">[!UICONTROL Connection name]</p>
                </td>
                <td>Saisissez un nom pour la connexion.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Environment]</td>
                <td>Sélectionnez s’il s’agit d’un environnement de production ou d’un environnement de non-production tel que Prévisualisation ou Sandbox.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Type]</td>
                <td>Sélectionnez s’il s’agit d’un compte de service ou d’un compte personnel.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Email / Username]</td>
                <td>Saisissez le nom d’utilisateur ou d’utilisatrice de votre compte [!DNL Workfront Proof].</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Password]</td>
                <td>Saisissez le mot de passe de votre compte [!DNL Workfront Proof].</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Tenant ID]</td>
                <td><strong>Remarque</strong> : les clientes et clients qui n’utilisent pas BYOK doivent laisser ce champ vide. <p>Saisissez l’identifiant du locataire pour ce compte. Si vous avez besoin d’aide pour trouver votre identifiant de locataire, contactez le service clientèle de Workfront.</p></td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Domain Extension]</td>
                <td>Saisissez l’extension de l’URL que vous utilisez pour accéder à votre compte. <p>Exemple : <code>com</code> ou <code>eu</code></p></td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Production, Preview, or Custom Environment]</td>
                <td>Environnement de production, d’aperçu ou personnalisé auquel vous souhaitez vous connecter.</td>
            </tr>
        </tbody>
    </table>


3. Cliquez sur [!UICONTROL **Continuer**] pour enregistrer la connexion et revenir au module.

## Modules [!DNL Workfront Proof] et leurs champs

Lorsque vous configurez les modules [!DNL Workfront Proof], Workfront Fusion affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Workfront Proof] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Déclencheurs](#triggers)
* [Actions](#actions)
* [Recherches](#searches)

### Déclencheurs

* [Regarder les résumés PDF](#watch-for-pdf-summary)
* [[!UICONTROL Regarder l’activité d’une épreuve]](#watch-proof-activity)
* [Regarder les épreuves](#watch-proofs)

#### [!UICONTROL Regarder le résumé PDF]

Ce module de déclenchement instantané exécute un scénario lorsque quelqu’un crée un résumé PDF pour une épreuve.

Un webhook est nécessaire pour ce module.

Le module renvoie tous les champs standard associés à l’épreuve, ainsi que tous les champs et valeurs personnalisés auxquels la connexion a accès. Il crée également un nouvel abonnement aux événements pour les résumés PDF et génère le contenu de l’attribut `pdf_url` envoyé dans la payload. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Webhook name]</td> 
   <td>Saisissez ou mappez un nom pour le nouveau webhook</td> 
  </tr> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Workfront Proof] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Regarder l’activité d’une épreuve]

Ce module de déclenchement exécute un scénario lorsqu’une activité spécifiée se produit sur une épreuve.

Le module renvoie tous les champs standard associés à l’épreuve, ainsi que tous les champs et valeurs personnalisés auxquels la connexion a accès. Il crée également un nouvel abonnement aux événements pour les résumés PDF et génère le contenu de l’attribut `pdf_url` envoyé dans la payload. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Workfront Proof] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Activity type]</td> 
   <td>Choisissez si vous souhaitez observer une nouvelle décision (y compris les modifications du statut de l’épreuve) ou des modifications générales du statut de l’épreuve uniquement.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Regarder les épreuves]

Ce module de déclenchement planifié exécute un scénario lorsque quelqu’un crée ou prend une décision sur une épreuve.

Le module renvoie une liste de tous les enregistrements trouvés au cours de la période spécifiée avec leur type. Il renvoie également les valeurs des champs que vous avez spécifiés. Si le module a trouvé des décisions prises sur l’épreuve, il inclut à la fois la valeur précédente et la valeur actuelle dans des champs séparés. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Cela se produit à un intervalle planifié régulier que vous spécifiez.

Vous devez disposer des autorisations nécessaires pour accéder à la ou aux épreuves dans [!DNL Workfront Proof] afin de pouvoir récupérer ces informations.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Workfront Proof] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Type d’enregistrement</td> 
   <td>Choisissez si vous souhaitez rechercher de nouvelles épreuves ou de nouvelles décisions globales relatives aux épreuves.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Limite</td> 
   <td> <p>Saisissez ou mappez le nombre maximum d’enregistrements que le module doit renvoyer pour chaque cycle d’exécution du scénario.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Éléments par page</td> 
   <td> <p>Pour paginer les résultats, saisissez ou mappez le nombre de résultats renvoyés qui doivent apparaître sur chaque page de résultats. Ce nombre doit être inférieur ou égal à 100.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Actions

* [[!UICONTROL Créer une épreuve]](#create-proof)
* [[!UICONTROL Appel API personnalisé]](#custom-api-call)
* [[!UICONTROL Télécharger l’épreuve]](#download-proof)
* [[!UICONTROL Lire un enregistrement]](#read-a-record)
* [[!UICONTROL Demander le résumé du PDF]](#request-pdf-summary)
* [[!UICONTROL Mettre à jour l’épreuve]](#update-proof)
* [[!UICONTROL Charger un fichier]](#upload-file)

#### [!UICONTROL Créer une épreuve]

<!--Cannot test Jan 2025-->

Ce module d’action crée une nouvelle épreuve ou une nouvelle version d’une épreuve dans [!DNL Workfront Proof].

Vous spécifiez les paramètres de la nouvelle épreuve et de l’épreuve source si vous créez une nouvelle version.

Le module renvoie l’identifiant de la nouvelle épreuve ou version de l’épreuve. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Workfront Proof] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof Type]</td> 
   <td> <p>Indiquez si vous souhaitez que l’épreuve créée ait un workflow de base ou un [!UICONTROL Automated Workflow].</p> <p>Remplissez ensuite les champs qui s’affichent pour le type d’épreuve que vous avez choisi. Par exemple, si vous avez choisi [!UICONTROL Automated Workflow], remplissez le champ <strong>[!UICONTROL Workflow Stages]</strong> pour configurer les étapes.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Allow original file to be downloaded]</td> 
   <td>Indiquez si vous souhaitez autoriser le téléchargement du fichier original à partir duquel l’épreuve a été créée.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Classic Proof Viewer]</td> 
   <td>Indiquez si vous utilisez la visionneuse d’épreuve classique.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Combine all files into single proof]</td> 
   <td>Activez cette option pour combiner tous les fichiers en une seule épreuve multipage.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Create a new proof version]</td> 
   <td>Sélectionnez cette option si vous souhaitez que le module crée une nouvelle version d’une épreuve existante. Ensuite, dans le champ <strong>[!UICONTROL Existing Proof ID]</strong> qui s’affiche, mappez ou saisissez l’identifiant unique de l’épreuve.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Custom Link Label]</td> 
   <td>Saisissez ou mappez un libellé pour le lien d’épreuve personnalisé.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Custom Link URL]</td> 
   <td>Saisissez ou mappez l’URL du lien personnalisé.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Default email notifications for subscribers]</td> 
   <td>Saisissez l’un des nombres suivants pour indiquer les paramètres de notification par e-mail par défaut que vous souhaitez utiliser pour l’épreuve créée.
    <ul>
     <li><strong>1</strong> - Tous les nouveaux commentaires et réponses</li>
     <li><strong>2</strong> - Réponses à mes commentaires</li>
     <li><strong>3</strong> - Résumé quotidien</li>
     <li><strong>4</strong> - Résumé horaire</li>
     <li><strong>5</strong> - Décisions uniquement</li>
     <li><strong>9</strong> - Désactivé</li>
    </ul></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Disable Excel Summary]</td> 
   <td>Indiquez si vous souhaitez désactiver la possibilité de télécharger les commentaires d’épreuves vers un fichier Excel.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Disable PDF Summary]</td> 
   <td>Indiquez si vous souhaitez désactiver la possibilité de télécharger les commentaires d’épreuves vers un fichier PDF.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Disable Subscription Email]</td> 
   <td>Indiquez si vous souhaitez désactiver l’e-mail d’abonnement pour cette épreuve.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Enable Embed Player]</td> 
   <td>Indiquez si vous souhaitez activer le lecteur incorporé pour cette épreuve.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Enable Subscriptions]</td> 
   <td>Indiquez si les personnes qui ne sont pas inscrites sont autorisées à s’abonner à l’épreuve.<br>Si vous sélectionnez cette option, vous pouvez également sélectionner le rôle par défaut des personnes abonnées, comme décrit dans ce tableau.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Enable Subscriptions Validation]</td> 
   <td>Indiquez si vous souhaitez activer la validation d’abonnement par e-mail. Si cette option est activée, la personne abonnée doit cliquer sur un lien dans un e-mail pour accéder à une épreuve.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Enable Team URL]</td> 
   <td>Choisissez si vous voulez que l’épreuve créée masque ou affiche l’URL de l’équipe.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL File Hash] <span style="font-weight: normal;">ou</span> [!UICONTROL File Hashes]</td> 
   <td>Ajoutez l’identifiant du ou des fichiers que vous souhaitez utiliser pour créer une ou plusieurs épreuves.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL File Names]</td> 
   <td>Ajoutez le ou les noms de fichiers pour l’épreuve créée. Ce champ est obligatoire.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Lock proof when all required decisions are made]</td> 
   <td>Indiquez si vous souhaitez que l’épreuve créée soit verrouillée une fois que toutes les décisions requises ont été prises.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Notify recipients about this proof]</td> 
   <td>Sélectionnez une option pour indiquer si vous voulez informer les personnes destinataires de la création de l’épreuve.&gt;</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof name]</td> 
   <td>Saisissez un nom pour l’épreuve créée. Ce champ est obligatoire. Utilisez le symbole barre verticale (|) pour séparer les noms des différentes épreuves.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof owner ID]</td> 
   <td>Saisisez ou mappez l’indentifiant de la personne propriétaire de l’épreuve. Si ce champ n’est pas renseigné, la personne actuelle est propriétaire de l’épreuve.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Reference ID]</td> 
   <td>Saisissez l’identifiant de référence de l’épreuve.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Require electronic signature]</td> 
   <td>Indiquez si vous souhaitez demander une signature électronique à toute personne prenant une décision sur une épreuve.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Require login]</td> 
   <td> <p>Indiquez si vous souhaitez utiliser l’option de connexion obligatoire pour l’épreuve créée. </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Resolution ID]</td> 
   <td>Saisissez l’identifiant de la résolution que vous souhaitez utiliser pour votre épreuve. Pour une liste des identifiants de résolution, consultez la <a href="https://api.proofhq.com/home/objects/soapworkflowproofobject.html">documentation de l’API</a> [!DNL Workfront Proof].</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL SWF]</td> 
   <td>Saisissez le type d’épreuve SWF.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Show] [item]</td> 
   <td>Indiquez si vous souhaitez afficher chaque élément dans l’épreuve.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Workspace ID]</td> 
   <td>Saisissez l’identifiant de l’espace de travail dans lequel vous souhaitez créer l’épreuve. </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Recipients]</td> 
   <td>Ajoutez les adresses e-mail des personnes à qui vous souhaitez affecter l’épreuve créée.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Deadline]</td> 
   <td> <p>Indiquez la date d’échéance pour la relecture de l’épreuve créée. Utilisez le format de date suivant :</p> <p><code>YYYY-MM-DD hh:mm</code></p> </td> 
  </tr> 
 </tbody> 
</table>



#### [!UICONTROL Appel API personnalisé]

Ce module d’action vous permet d’effectuer un appel personnalisé et authentifié à l’API [!DNL Workfront Proof]. Vous pouvez ainsi, automatiser le flux de données d’une façon que les autres modules [!DNL Workfront Proof] ne permettent pas.

Le module renvoie le code d’état, les en-têtes et le corps du texte. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Workfront Proof] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Method]</td> 
   <td>Définissez l’action pour l’appel API. Pour connaître les actions disponibles, voir la <a href="https://api.proofhq.com/">documentation de l’API Workfront Proof</a>.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Body (XML)]</td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre JSON, mettez les guillemets à l’extérieur de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Exemple :**
>
>![Exemple de module d’API de BAT](/help/workfront-fusion/references/apps-and-modules/assets/wfp-api-module-example-350x586.png)

#### [!UICONTROL Télécharger l’épreuve]

Ce module d’action télécharge le fichier source d’une épreuve particulière que vous identifiez à l’aide de son ID.

Vous indiquez l’ID de l’épreuve.

Le module renvoie le contenu du fichier source utilisé pour créer l’épreuve. Vous pouvez mapper cette information dans les modules suivants du scénario.

Vous devez disposer des autorisations nécessaires pour accéder à l’enregistrement dans [!DNL Workfront Proof] afin de pouvoir récupérer ces informations.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Workfront Proof] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof ID]</td> 
   <td> <p>Saisissez l’ID unique de l’épreuve, qui se trouve sur la page [!UICONTROL Proof Details].  </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Lire un enregistrement]

Ce module d’action lit les données d’une seule épreuve dans [!DNL Workfront Proof].

Vous indiquez l’ID de l’épreuve et les informations que vous souhaitez obtenir de l’épreuve.

Le module renvoie les valeurs des champs que vous avez choisis pour l’épreuve, ainsi que leurs types. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Vous devez disposer d’autorisations suffisantes pour accéder à l’enregistrement dans [!DNL Workfront Proof] afin de pouvoir récupérer ces informations.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Workfront Proof] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td>Indiquez si vous souhaitez lire une épreuve, les commentaires d’une épreuve ou les réviseurs ou réviseuses d’une épreuve.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>Sélectionnez les informations que vous souhaitez inclure dans le bundle de sortie pour ce module.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td>Saisissez ou mappez l’ID unique [!DNL Workfront Proof] de l’enregistrement que vous souhaitez que le module lise.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Demander le résumé PDF]

Ce module d’action demande le résumé PDF d’une épreuve particulière dans [!DNL Workfront Proof].

Vous indiquez l’ID de l’épreuve.

Le module renvoie les informations du résumé PDF. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Vous devez disposer d’autorisations suffisantes pour accéder à l’enregistrement dans [!DNL Workfront Proof] afin de pouvoir récupérer ces informations.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Workfront Proof] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof ID]</td> 
   <td> <p>Saisissez l’ID unique [!DNL Workfront Proof] de l’épreuve pour laquelle vous souhaitez demander un résumé PDF.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Callback URL]</td> 
   <td>Saisissez ou mappez l’URL où vous souhaitez que le résumé PDF soit envoyé.</td> 
  </tr> 
 </tbody> 
</table>

##### Erreur possible

* **Erreur** : « [!UICONTROL Vous n’avez pas les privilèges nécessaires pour effectuer cette demande. L’étape doit contenir au moins une personne destinataire.] »
* **Solution** : assurez-vous que vous n’êtes pas la seule personne affectée aux étapes du workflow. Une autre personne doit être affectée aux étapes du workflow.

#### [!UICONTROL Mettre à jour l’épreuve]

Ce module d’action met à jour une épreuve existante dans [!DNL Workfront Proof].

Vous indiquez l’identifiant de l’épreuve et le type d’enregistrement, ainsi que les champs que vous souhaitez inclure dans la sortie.

Le module renvoie tous les champs standard associés à l’enregistrement, ainsi que tous les champs et valeurs personnalisés auxquels la connexion accède. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Vous devez disposer d’autorisations suffisantes pour accéder à l’enregistrement dans [!DNL Workfront Proof] afin de pouvoir récupérer ces informations.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Workfront Proof] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof ID]</td> 
   <td> <p>Saisissez l’ID unique de l’épreuve, qui se trouve sur la page [!UICONTROL Proof Details]. </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Deadline]</td> 
   <td> <p>Indiquez la date d’échéance pour la relecture de l’épreuve créée. Utilisez le format de date <code>YYYY-MM-DD hh:mm</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Default email notifications for subscribers]</td> 
   <td>Sélectionnez l’un des paramètres de notification par e-mail par défaut suivants que vous souhaitez utiliser pour l’épreuve créée.
    <ul>
     <li> [!UICONTROL All new comments and replies]</li>
     <li>[!UICONTROL Replies to my comments]</li>
     <li>[!UICONTROL Daily summary]</li>
     <li> [!UICONTROL Hourly summary]</li>
     <li> [!UICONTROL Decisions only]</li>
     <li> [!UICONTROL Disabled]</li>
    </ul></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Default Role]</td> 
   <td>Sélectionnez le rôle par défaut pour l’épreuve.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Disable Subscription Email]</td> 
   <td>Indiquez si vous souhaitez désactiver l’e-mail d’abonnement pour cette épreuve.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Enable Subscriptions]</td> 
   <td>Indiquez si les personnes qui ne sont pas inscrites sont autorisées à s’abonner à l’épreuve.<br>Si vous sélectionnez cette option, vous pouvez également sélectionner une option dans le champ [!UICONTROL Default Role].</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Enable Subscriptions Validation]</td> 
   <td>Indiquez si vous souhaitez activer la validation d’abonnement par e-mail. Si cette option est activée, la personne abonnée doit cliquer sur un lien dans un e-mail pour accéder à une épreuve.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Enable Team URL]</td> 
   <td>Choisissez si vous voulez que l’épreuve créée masque ou affiche l’URL de l’équipe.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Lock proof when all required decisions are made]</td> 
   <td>Indiquez si vous souhaitez que l’épreuve créée soit verrouillée une fois que toutes les décisions requises ont été prises.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Message]</td> 
   <td>Saisissez ou mappez le message qui doit accompagner l’épreuve.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof ID] </td> 
   <td>Saisissez ou mappez l’identifiant de l’épreuve que vous souhaitez mettre à jour.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof Name]</td> 
   <td>Saisissez ou affichez le nom de l’épreuve que vous souhaitez mettre à jour.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Require login]</td> 
   <td> <p>Indiquez si vous souhaitez utiliser l’option de connexion obligatoire pour l’épreuve créée. </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show Versions Like]</td> 
   <td>Indiquez si vous souhaitez afficher un lien vers d’autres versions de cette épreuve.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject]</td> 
   <td>Saisir ou mapper le sujet de l’épreuve</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Charger fichier]

Ce module d’action charge un fichier à utiliser avec le module [!UICONTROL Créer une épreuve] dans [!DNL Workfront Proof].

Le module renvoie un identifiant de hachage pour le fichier chargé. Vous pouvez mettre en correspondance ces informations dans les modules suivants du scénario.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Workfront Proof] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Recherches

* [[!UICONTROL Répertorier les modèles de workflows]](#list-workflow-templates)
* [[!UICONTROL Rechercher]](#search)

#### [!UICONTROL Répertorier les modèles de workflows]

Ce module de recherche répertorie tous les modèles de workflow disponibles.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la procédure de connexion de votre compte [!DNL Workfront Proof] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Créer une connexion vers Adobe Workfront Fusion - Instructions de base</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>Sélectionnez les informations que vous souhaitez inclure dans le bundle de sortie pour ce module.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p>Saisissez ou mappez le nombre maximum de modèles que vous souhaitez que le module renvoie au cours de chaque cycle d’exécution de scénario.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Rechercher]

Ce module de recherche recherche les enregistrements dans un objet dans [!DNL Workfront Proof] qui correspondent à la requête que vous avez spécifiée.

Le module renvoie l’identifiant de l’épreuve s’il recherche une épreuve. Il renvoie également les identifiants, les e-mails, les noms, les postes et les alias des e-mail, s’il recherche des destinataires. Vous pouvez mapper ces informations dans les modules suivants du scénario.

Vous devez disposer d’autorisations suffisantes pour accéder à l’enregistrement dans [!DNL Workfront Proof] afin de pouvoir récupérer ces informations.

Lorsque vous configurez ce module, les champs suivants s’affichent.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Workfront Proof] à Workfront Fusion, voir <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Création d’une connexion à Adobe Workfront Fusion - Instructions de base</a>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Rechercher]</td> 
   <td> <p>Sélectionnez le type d’enregistrement que le module doit rechercher.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Proof]</strong> </p> <p>Saisissez le nom de l’épreuve que vous souhaitez rechercher.</p> </li> 
     <li> <p><strong>[!UICONTROL Recipient]</strong> </p> <p>Saisissez l’adresse e-mail de la destinataire ou du destinataire que vous souhaitez rechercher.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Result Set]</td> 
   <td>Indiquez si le module doit rechercher <strong>[!UICONTROL All Matching Records]</strong> ou seulement <strong>[!UICONTROL First Matching Record]</strong>.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Sort By]</td> 
   <td>Sélectionnez le champ par lequel vous souhaitez trier les résultats.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Sorting Direction]</td> 
   <td> <p>Sélectionnez si vous souhaitez trier les résultats par ordre croissant ou décroissant.</p> </td> 
  </tr> 
 </tbody> 
</table>

