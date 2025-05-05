---
title: Modules Adobe Experience Manager Assets
description: Avec le connecteur  [!DNL Adobe Experience Manager Assets]  pour [!DNL Adobe Workfront Fusion], vous pouvez créer, charger et mettre à jour des ressources, ainsi que copier ou déplacer des dossiers et des ressources.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 361e6c9c-1497-4f47-85bb-503619744968
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '1727'
ht-degree: 75%

---

# Modules [!DNL Adobe Experience Manager Assets]

Grâce au connecteur [!DNL Adobe Experience Manager Assets] pour [!DNL Adobe Workfront Fusion], vous pouvez créer, charger et mettre à jour des ressources, ainsi que copier ou déplacer des dossiers et des ressources.

Pour une présentation vidéo du connecteur Adobe Experience Manager Assets, voir :

* [Adobe Experience Manager Assets](https://video.tv.adobe.com/v/3427034/){target=_blank}

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
   <p>Hérité : Workfront Fusion pour l’automatisation et l’intégration </p>
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

* Vous devez avoir un compte [!DNL Adobe Experience Manager Assets] pour utiliser ces modules.
* Vous devez configurer le flux [!UICONTROL Serveur à serveur] dans l’[!DNL Adobe Developer console].

  Pour obtenir des instructions sur la configuration du flux [!UICONTROL Serveur à serveur] dans l’[!DNL Adobe Developer console], voir [Générer des jetons d’accès pour les API côté serveur](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html?lang=fr#the-server-to-server-flow).
* Votre compte technique Adobe Experience Manager doit disposer d’autorisations en écriture.

  Pour obtenir des instructions sur l’ajout d’autorisations d’écriture à votre compte technique Adobe Experience Manager, voir [Informations d’identification du service](https://experienceleague.adobe.com/en/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials) dans la documentation de Adobe Experience Manager.

## Informations sur l’API Adobe Experience Manager Assets

Le connecteur Adobe Experience Manager Assets utilise les éléments suivants :

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Balise API</td> 
   <td>v1.8.61</td> 
  </tr>
 </tbody> 
 </table>

## Connecter [!DNL Adobe Experience Manager Assets] à [!DNL Workfront Fusion] {#connect-adobe-experience-manager-assets-to-workfront-fusion}

Pour créer une connexion pour vos modules [!DNL Adobe Experience Manager Assets], procédez comme suit :

1. Cliquez sur [!UICONTROL Ajouter] à côté de la case [!UICONTROL Connexion].

2. Sélectionnez le type de connexion que vous créez :

   * **[!DNL AEM Assets as a Cloud Service]**

     Cette configuration nécessite des informations de l’[!DNL Adobe Admin Console].

   * **[!DNL AEM Assets Basic] ([!DNL Adobe Managed Services])**

     Cette configuration nécessite un nom d’utilisateur ou d’utilisatrice et un mot de passe.

3. Remplissez les champs correspondant au type de connexion que vous créez.

   Pour [!DNL AEM Assets as a Cloud Service], voir [Configurer la connexion pour  [!DNL AEM Assets as a Cloud Service]](#configure-the-connection-for-aem-assets-as-a-cloud-service).

   Pour [!UICONTROL AEM Assets Basic] ([!DNL Adobe Managed Services]), voir [Configurer la connexion pour [!UICONTROL AEM Assets Basic]](#configure-the-connection-for-aemassets-basic-adobe-managed-services).

4. Cliquez sur **[!UICONTROL Continuer]** pour enregistrer la connexion et revenir au module.


### Configurer la connexion pour [!DNL AEM Assets as a Cloud Service]

>[!NOTE]
>
>* Les informations relatives à ces champs sont générées dans le cadre de la configuration du flux [!UICONTROL Serveur à serveur] sur l’[!DNL Adobe Developer Console]. Vous trouverez ces valeurs dans le fichier JSON des identifiants de service généré dans le cadre de cette configuration.
>
>   Pour obtenir des instructions sur la configuration du flux [!UICONTROL Serveur à serveur] sur l’[!UICONTROL Adobe Developer Console], voir [Générer des jetons d’accès pour les API côté serveur](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html?lang=fr#the-server-to-server-flow).
>
>* Votre compte technique Adobe Experience Manager doit disposer d’autorisations en écriture.
>
>   Pour obtenir des instructions sur l’ajout d’autorisations d’écriture à votre compte technique Adobe Experience Manager, voir [Informations d’identification du service](https://experienceleague.adobe.com/en/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials) dans la documentation de Adobe Experience Manager.


<table style="table-layout:auto"> 
          <col/>
          <col/>
          <tbody>
              <tr>
                  <td role="rowheader">[!UICONTROL Connection name]</td>
                  <td>
                      <p>Nommer cette connexion</p>
                  </td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Instance URL without a trailing slash]</td>
                  <td>Saisissez l’URL de votre instance [!DNL Adobe Experience Manager]. N’ajoutez pas une barre oblique <code>/</code> à la fin de l’URL.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Account details fill options]</td>
                  <td>Choisissez si vous souhaitez fournir un fichier JSON décrivant les détails de votre compte ou si vous souhaitez saisir les détails manuellement.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Détails du compte technique au format JSON]</td>
                  <td>Si vous fournissez du code JSON, saisissez ou collez le code JSON décrivant les détails de votre compte.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Client ID]</td>
                  <td>Si vous entrez les détails manuellement, saisissez l'identifiant du client généré dans la configuration [!UICONTROL Serveur à serveur].</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Client Secret]</td>
                  <td>Si vous entrez les détails manuellement, saisissez le secret client généré dans la configuration [!UICONTROL Serveur à serveur].</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Technical account ID]</td>
                  <td>Si vous saisissez les détails manuellement, saisissez l'ID du compte technique. Il s’agit du champ « [!UICONTROL id] » du fichier JSON des informations d’identification client.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Org ID]</td>
                  <td class="">Si vous saisissez les détails manuellement, saisissez l’ID de votre organisation. Il s’agit du champ « [!UICONTROL org] » du fichier JSON des informations d’identification client.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Meta Scopes]</td>
                  <td>Saisissez les métasopes générés dans la configuration [!UICONTROL Server-to-server].</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Private key]</td>
                  <td>Saisissez la clé privée générée lors de la configuration [!UICONTROL Server-to-server]. Pour extraire la clé privée, cliquez sur [!UICONTROL Extract], puis entrez le fichier à extraire et le mot de passe du fichier.</td>
              </tr>
              <tr>
                  <td role="rowheader">[!UICONTROL Authentication URL]</td>
                  <td>Saisissez l’URL d’authentification pour ce compte.</td>
              </tr>
          </tbody>
      </table>


### Configuration de la connexion à AEM Assets Basic (Adobe Managed Services)

<table style="table-layout:auto"> 
        <col/>
        <col />
        <tbody>
            <tr>
                <td role="rowheader">[!UICONTROL Connection name]</td>
                <td>
                    <p>Nommer cette connexion</p>
                </td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Instance URL without a trailing slash]</td>
                <td>Saisissez l’URL de votre instance [!DNL Adobe Experience Manager]. N’incluez pas de barre oblique <code>/</code> à la fin de l’URL.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Username]</td>
                <td>Saisissez le nom d’utilisateur ou d’utilisatrice du compte [!DNL AEM Assets] utilisé pour cette connexion.</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Password]</td>
                <td>Saisissez le mot de passe du compte [!DNL AEM Assets] utilisé pour cette connexion.</td>
            </tr>
        </tbody>
    </table>


## Modules [!DNL Adobe Experience Manager Assets] et leurs champs

Lorsque vous configurez les modules [!DNL Adobe Experience Manager Essentials], [!DNL Workfront Fusion] affiche les champs répertoriés ci-dessous. En plus de ces derniers, des champs [!DNL Adobe Experience Manager Essentials] supplémentaires peuvent s’afficher, selon des facteurs tels que votre niveau d’accès dans l’application ou le service. Un titre en gras dans un module indique un champ obligatoire.

Si le bouton « Mapper » apparaît au-dessus d’un champ ou d’une fonction, vous pouvez l’utiliser pour définir des variables et des fonctions pour ce champ. Pour plus d’informations, voir [Mappage des informations d’un module à un autre](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![Basculement de carte](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Copier un dossier ou une ressource](#copy-a-folder-or-asset)
* [Créer un enregistrement](#create-a-record)
* [Suppression d’un dossier, d’une ressource ou d’un rendu](#delete-a-folder-asset-or-rendition)
* [Obtenir une liste de dossiers](#get-a-folder-listing)
* [Effectuer un appel API personnalisé.](#make-a-custom-api-call)
* [Déplacer un dossier ou une ressource](#move-a-folder-or-asset)
* [Mettre à jour un enregistrement](#update-a-record)
* [Chargement d’un élément](#upload-an-asset)

### [!UICONTROL Copier un dossier ou une ressource]

Ce module d’action copie un dossier ou une ressource vers un autre emplacement de votre compte Adobe Experience Manager Assets.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Adobe Experience Manager Assets] à [!DNL Workfront Fusion], voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Adobe Experience Manager Assets] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Sélectionnez si vous souhaitez copier un dossier ou une ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] / [!UICONTROL Asset]</td> 
   <td>Sélectionnez ou mappez le dossier ou la ressource que vous souhaitez copier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination path]</td> 
   <td>Sélectionnez ou mappez le chemin d’accès à l’emplacement du nouveau dossier ou de la nouvelle ressource.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name of copied folder] / [!UICONTROL asset]</td> 
   <td>Saisissez un nom pour le nouveau dossier ou la nouvelle ressource. Le nom du dossier qui s’affiche dans [!DNL Adobe Experience Manager Assets] est le même que le nom d’origine. Le nom saisi ici apparaît dans l’URL du nouveau dossier ou de la nouvelle ressource.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy children]</td> 
   <td>Si vous copiez un dossier, activez cette option pour copier tous les sous-dossiers ou ressources du dossier.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Overwrite]</td> 
   <td>Activez cette option pour écraser les dossiers ou ressources de l’emplacement de destination portant le même nom que le dossier ou la ressource en cours de copie.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Créer un enregistrement]

Ce module d’action crée un dossier ou un commentaire de ressource.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour savoir comment connecter votre compte [!DNL Adobe Experience Manager Assets] à [!DNL Workfront Fusion], voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Adobe Experience Manager Assets] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object type]</td> 
   <td> <p>Indiquez si vous souhaitez créer un dossier ou un commentaire sur une ressource.</p> 
    <ul> 
     <li> <p>[!UICONTROL Folder]</p> <p>Remplissez les champs suivants :</p> 
      <ul> 
       <li> <p>[!UICONTROL Name]</p> <p>Saisissez un nom pour le dossier. Ce nom apparaîtra dans le chemin d’accès au fichier, il ne doit donc pas comporter d’espaces ou d’autres caractères. </p> </li> 
       <li> <p>[!UICONTROL Title]</p> <p>Saisissez un titre pour le dossier, qui peut être affiché à la place du nom.</p> </li> 
      </ul> </li> 
     <li> <p>[!UICONTROL Asset comment]</p> <p>Remplissez les champs suivants :</p> 
      <ul> 
       <li> <p>[!UICONTROL Asset selection]</p> <p>Sélectionnez ou mappez l’ID de la ressource à laquelle vous souhaitez ajouter un commentaire.</p> </li> 
       <li> <p>[!UICONTROL Comment]</p> <p>Saisissez le texte du commentaire.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Supprimer un dossier, une ressource ou un rendu]

Ce module d’action supprime un dossier, une ressource ou un rendu.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Adobe Experience Manager Assets] à [!DNL Workfront Fusion], voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Adobe Experience Manager Assets] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Indiquez si vous souhaitez supprimer un dossier, une ressource ou un rendu.</p> 
    <ul> 
     <li> <p>[!UICONTROL Folder]</p> <p>Sélectionnez le dossier à supprimer en sélectionnant les dossiers dans son chemin d’accès.</p> </li> 
     <li> <p>[!UICONTROL Asset] </p> <p>Sélectionnez la ressource en sélectionnant les dossiers dans son chemin, puis la ressource à supprimer.</p> </li> 
     <li> <p>[!UICONTROL Rendition]</p> <p>Sélectionnez le rendu en sélectionnant les dossiers dans son chemin d’accès.</p> <p>Saisissez ou mappez le nom du rendu.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Obtenir une liste de dossiers]

Ce module d’action permet de récupérer une représentation d’un dossier existant et de ses entités enfant (dossiers ou ressources).

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Adobe Experience Manager Assets] à [!DNL Workfront Fusion], voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Adobe Experience Manager Assets] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Sélectionnez ou mappez le dossier que vous souhaitez récupérer. Pour ajouter des sous-dossiers au chemin d’accès, cliquez sur l’icône Plus et sélectionnez le sous-dossier.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Effectuer un appel API personnalisé]

Ce module d’action lance un appel personnalisé à l’API [!DNL Adobe Experience Manager Assets].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Adobe Experience Manager Assets] à [!DNL Workfront Fusion], consultez la section <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Adobe Experience Manager Assets] à [!DNL Workfront Fusion]</a> de cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Saisissez un chemin d’accès relatif à l’URL de base [!DNL Adobe Experience Manager].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Sélectionnez la méthode de requête HTTP dont vous avez besoin pour configurer l’appel API. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">Méthodes de requête HTTP</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Ajoutez les en-têtes de la requête sous la forme d’un objet JSON standard.</p> <p>Par exemple, <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] Ajoute automatiquement des en-têtes d’autorisation.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String] </td> 
   <td> <p>Saisissez la chaîne de requête. Pour chaque paire clé/valeur, cliquez sur <b>[!UICONTROL Add item]</b> et saisissez la [!UICONTROL Key] et la [!UICONTROL Value].</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Ajoutez le contenu du corps de l’appel API sous la forme d’un objet JSON standard.</p> <p>Note :  <p>Lorsque vous utilisez des instructions conditionnelles telles que <code>if</code> dans votre fichier JSON, placez les guillemets en dehors de l’instruction conditionnelle.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Déplacer un dossier ou une ressource]

Ce module d’action déplace la ressource ou le dossier au chemin d’accès donné vers un nouvel emplacement.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Adobe Experience Manager Assets] à [!DNL Workfront Fusion], voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Adobe Experience Manager Assets] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Indiquez si vous souhaitez déplacer un dossier ou une ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] / [!UICONTROL Asset]</td> 
   <td>Sélectionnez ou mappez le dossier ou la ressource que vous souhaitez déplacer.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination path]</td> 
   <td>Sélectionnez ou mappez le chemin d’accès à l’emplacement vers lequel vous souhaitez déplacer le dossier ou la ressource.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name of moved folder] / [!UICONTROL asset]</td> 
   <td>Saisissez un nouveau nom pour le dossier déplacé ou la ressource déplacée. Le nom du dossier qui s’affiche sur [!DNL Adobe Experience Manager Assets] est le même que le nom d’origine. Le nom saisi ici apparaît dans l’URL du dossier déplacé ou de la ressource déplacée.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Overwrite]</td> 
   <td>Activez cette option pour remplacer dans l’emplacement de destination tout dossier ou ressource portant le même nom que le dossier ou la ressource déplacé.</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Mettre à jour un enregistrement]

Ce module d’action met à jour un enregistrement existant.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Adobe Experience Manager Assets] à [!DNL Workfront Fusion], voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Adobe Experience Manager Assets] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Indiquez si vous souhaitez supprimer les métadonnées ou un rendu de la ressource.</p> 
    <ul> 
     <li> <p>[!UICONTROL Asset metadata]</p> 
      <ul> 
       <li> <p>Sélectionnez la ressource dont vous souhaitez mettre à jour les métadonnées.</p> </li> 
       <li> <p>Saisissez le nouveau titre de la ressource.</p> </li> 
      </ul> </li> 
     <li> <p>[!UICONTROL Asset rendition]</p> 
      <ul> 
       <li> <p>Sélectionnez la ressource dont vous souhaitez mettre à jour le rendu.</p> </li> 
       <li> <p>Sélectionnez un fichier source à partir d’un module précédent ou mappez le nom et les données du fichier source.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Charger une ressource]

Ce module d’action charge une ressource sur votre compte [!DNL Adobe Experience Manager Assets].

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Pour obtenir des instructions sur la connexion de votre compte [!DNL Adobe Experience Manager Assets] à [!DNL Workfront Fusion], voir <a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">Connecter [!DNL Adobe Experience Manager Assets] à [!DNL Workfront Fusion]</a> dans cet article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination]</td> 
   <td> <p>Sélectionnez le dossier dans lequel vous souhaitez charger une ressource.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Saisissez ou mappez le nom et les données du fichier source.</td> 
  </tr> 
 </tbody> 
</table>
