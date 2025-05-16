---
filename: workday-modules
title: Modules Workday
description: Dans un scénario Adobe Workfront Fusion, vous pouvez automatiser les workflows qui utilisent  [!DNL Workday], et le connecter à plusieurs applications et services tiers.
author: Becky
feature: Workfront Fusion
exl-id: 77237a1b-2acd-4350-9cc0-ec43b8b08137
source-git-commit: 40470e5d2183f690ad65f5e1170f78c37dee8603
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 87%

---

# Modules [!DNL Workday]

Dans un scénario [!DNL Adobe Workfront Fusion], vous pouvez automatiser les workflows qui utilisent [!DNL Workday] et le connecter à plusieurs applications et services tiers.

Pour obtenir des instructions sur la création d’un scénario, consultez les articles sous [Créer des scénarios : index d’article](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Pour plus d’informations sur les modules, consultez les articles sous [Modules : index des articles](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <p>Actuel : aucune exigence de licence Workfront Fusion</p>
   <p>Ou</p>
   <p>Hérité : Workfront Fusion pour l’automatisation et l’intégration du travail </p>
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

Pour plus d’informations sur les licences [!DNL Adobe Workfront Fusion], voir Licences [[!DNL Adobe Workfront Fusion] ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Conditions préalables

Pour utiliser les modules [!DNL Workday], vous devez :

* Disposer d’un compte [!DNL Workday].

* Créer une application OAuth dans [!DNL Workday]. Pour obtenir des instructions, voir la documentation [!DNL Workday].

## Informations sur l’API Workday

Le connecteur Workday utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">URL de base</td> 
   <td>https://{{connection.servicesUrl}}/api</td> 
  </tr>
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.6.4</td> 
  </tr>
 </tbody> 
 </table>

## Connecter [!DNL Workday] à [!DNL Workfront Fusion]

1. Dans n’importe quel module [!DNL Workfront Fusion], cliquez sur [!UICONTROL Ajouter] à côté du champ [!UICONTROL Connexion] 

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
                <td  role="rowheader">[!UICONTROL Workday host]</td>
                <td>Saisissez l’adresse de votre hôte [!DNL Workday] sans <code>https://</code>. Par exemple, <code>mycompany.workday.com</code>.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Services URL]</td>
                <td>Saisissez l’adresse de vos services web [!DNL Workday] sans <code>https://</code>. Par exemple, <code>mycompany-services.workday.com</code>.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Tenant name]</td>
                <td>Saisissez le nom du locataire de ce compte [!DNL Workday]. Pour votre locataire, indiquez l’identifiant de votre organisation. Il est visible dans l’URL que vous utilisez pour vous connecter à Workday. Exemple : dans l’adresse <code>https://www.myworkday.com/mycompany</code>, le locataire est <code>mycompany</code>.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Client ID]</td>
                <td>Saisissez l’identifiant du client pour l’application [!DNL Workday] que cette connexion utilise. Vous l’obtenez lorsque vous créez l’application dans [!DNL Workday].</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Client Secret]</td>
                <td>Saisissez le secret du client pour l’application [!DNL Workday] que cette connexion utilise. Vous l’obtenez lorsque vous créez l’application dans [!DNL Workday].</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Session timeout (min)]</td>
                <td >Saisissez le nombre de minutes après lequel votre jeton d’autorisation expire.</td>
            </tr>
        </tbody>
    </table>


3. Cliquez sur [!UICONTROL Continuer] pour enregistrer la connexion et revenir au module.

## Les modules [!DNL Workday] et leurs champs

Lorsque vous configurez les modules [!DNL Workday], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Workday] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Action](#action)

* [Recherche](#search)


### Action

* [[!UICONTROL Créer un enregistrement]](#create-a-record)

* [[!UICONTROL Supprimer un enregistrement]](#delete-a-record)

* [[!UICONTROL Effectuer un appel d’API personnalisé]](#make-a-custom-api-call)

* [[!UICONTROL Mettre à jour un enregistrement]](#update-a-record)


#### [!UICONTROL Créer un enregistrement]

Ce module d’action crée un seul enregistrement dans [!DNL Workday].

<table style="table-layout:auto"> 
    <col/>
    <col/>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Connection]</td>
            <td>Pour obtenir des instructions sur la procédure de connexion de votre compte [!DNL Workday] à Workfront Fusion, consultez <a href="#Connect" class="MCXref xref" >Connecter [!DNL Workday] à [!DNL Workfront Fusion]</a>.</td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Record Type]</td>
            <td>Sélectionnez le type d’enregistrement que vous souhaitez créer.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td>Saisissez ou mappez l’identifiant de l’enregistrement que vous souhaitez créer.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL Subresource ID]</td>
            <td >Saisissez ou mappez l’identifiant de la sous-ressource que vous souhaitez créer.</td>
        </tr>
    </tbody>
</table>

#### [!UICONTROL Supprimer un enregistrement]

Ce module d’action supprime un seul enregistrement dans [!DNL Workday].

<table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Connection]</td>
            <td>Pour obtenir des instructions sur la procédure de connexion de votre compte [!DNL Workday] à [!DNL Workfront Fusion], consultez <a href="#Connect" class="MCXref xref" >Connecter [!DNL Workday] à [!DNL Workfront Fusion]</a>.</td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Record type]</td>
            <td>Sélectionnez le type d’enregistrement que vous souhaitez supprimer.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL Specific record type]</td>
            <td>Sélectionnez le type d’enregistrement que vous souhaitez supprimer. Cette sélection se base sur le type d’enregistrement que vous avez choisi.</td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Subresource ID]</td>
            <td>Saisissez ou mappez l’identifiant de la sous-ressource que vous souhaitez supprimer.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td >Saisissez ou mappez l’identifiant de l’enregistrement que vous souhaitez supprimer.</td>
        </tr>
    </tbody>
</table>


### [!UICONTROL Effectuer un appel d’API personnalisé]

Ce module d’action vous permet d’effectuer un appel personnalisé et authentifié vers l’API [!DNL Workday]. Cela vous permet de créer une automatisation du flux de données qui ne peut pas être réalisée par les autres modules [!DNL Workday].

Lorsque vous configurez ce module, les champs suivants s’affichent.

Le module renvoie le code d’état, ainsi que les en-têtes et le corps de l’appel API.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!DNL Connection]</p> </td> 
            <td>Pour obtenir des instructions sur la procédure de connexion de votre compte [!DNL Workday] à [!DNL Workfront Fusion], consultez <a href="#Connect" class="MCXref xref" >Connecter [!DNL Workday] à [!DNL Workfront Fusion]</a>.</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Saisissez un chemin d’accès relatif à <code style="color: #ff1493;">https://&lt;tenantHostname>/api/&lt;serviceName>/&lt;version>/&lt;tenant></code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion] ajoute les en-têtes d’autorisation pour vous.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Ajoutez la requête pour l’appel API sous la forme d’un objet JSON standard.</p> <p>Par exemple : <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre code JSON, saisissez les guillemets à l’extérieur de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mettre à jour un enregistrement]

Ce module d’action met à jour un seul enregistrement dans [!DNL Workday].

<table style="table-layout:auto"> 
    <col/>
    <col/>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Connection]</td>
            <td>Pour obtenir des instructions sur la procédure de connexion de votre compte [!DNL Workday] à Workfront Fusion, consultez <a href="#Connect" class="MCXref xref" >[!UICONTROL Connect [!DNL Workday] to Workfront Fusion].</a></td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Record Type]</td>
            <td>Sélectionnez le type d’enregistrement à mettre à jour.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td>Saisissez ou mappez l’identifiant de l’enregistrement que vous souhaitez mettre à jour.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL Subresource ID]</td>
            <td >Saisissez ou mappez l’identifiant de la sous-ressource que vous souhaitez mettre à jour.</td>
        </tr>
    </tbody>
</table>

### Recherche

* [[!UICONTROL Lire un enregistrement]](#read-a-record)

* [[!UICONTROL Répertorier des enregistrements]](#list-records)


#### [!UICONTROL Lire un enregistrement]

Ce module d’action lit un seul enregistrement.

<table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Connection]</td>
            <td>Pour obtenir des instructions sur la procédure de connexion de votre compte [!DNL Workday] à Workfront Fusion, consultez <a href="#Connect" class="MCXref xref" >[!UICONTROL Connect [!DNL Workday] to Workfront Fusion]</a>.</td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Record type]</td>
            <td>Sélectionnez le type d’enregistrement que vous souhaitez supprimer.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL Specific record type]</td>
            <td>Sélectionnez le type d’enregistrement que vous souhaitez lire. Cette sélection se base sur le type d’enregistrement que vous avez choisi.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td >Saisissez ou mappez l’identifiant de l’enregistrement que vous souhaitez supprimer.</td>
        </tr>
    </tbody>
</table>

#### [!UICONTROL Répertorier des enregistrements]

Ce module de recherche permet d’obtenir une liste des enregistrements du type spécifié.

<table style="table-layout:auto"> 
      <col/>
      <col/>
      <tbody>
          <tr>
              <td role="rowheader">[!UICONTROL Connection]</td>
              <td>Pour obtenir des instructions sur la procédure de connexion de votre compte [!DNL Workday] à [!DNL Workfront Fusion], consultez la section <a href="#Connect" class="MCXref xref" >Connecter [!DNL Workday] à [!DNL Workfront Fusion]</a>.</td>
          </tr>
          <tr>
              <td  role="rowheader">[!UICONTROL Record Type]</td>
              <td>Sélectionnez le type d’enregistrement que vous souhaitez récupérer.</td>
          </tr>
          <tr>
              <td role="rowheader">[!UICONTROL Limit]</td>
              <td >
                  <p>Saisissez ou mappez le nombre maximum d’enregistrements que vous souhaitez que le module récupère au cours de chaque cycle d’exécution du scénario.</p>
              </td>
          </tr>
      </tbody>
  </table>
