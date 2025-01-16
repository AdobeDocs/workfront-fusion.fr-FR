---
title: Types de données d’élément
description: Vos scénarios  [!DNL Adobe Workfront Fusion]  peuvent contenir les types d’éléments répertoriés ci-dessous dans un lot.
author: Becky
feature: Workfront Fusion
exl-id: 3ad65959-5c19-4727-bc9d-4ff1d238ad8b
source-git-commit: b7c511c51a2f27292cd0cb754673515e67c8a397
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 80%

---

# Types de données d’élément

Vous pouvez contenir les types d’éléments répertoriés ci-dessous dans un lot.

Pour plus d’informations sur les types d’éléments [!DNL Workfront Fusion] permettent la conversion entre eux, voir [Type coercition](/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md).

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>Texte</p> </td> 
   <td> <p>Type d’élément le plus courant. Pour certains éléments de texte, [!DNL Adobe Workfront Fusion] vérifie si la longueur maximale ou minimale autorisée est respectée ou si l’élément effectue la validation du format (e-mail, URL ou nom de fichier).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Nombre</p> </td> 
   <td> <p>Pour certains éléments numériques, [!DNL Workfront Fusion] peut valider l’entrée pour une plage spécifiée (valeur minimale ou maximale autorisée).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Booléen (oui/non)</p> </td> 
   <td> <p>Ce type est utilisé pour les éléments qui n’ont que deux valeurs possibles : true ou false. </p> <p>Lors de la définition de modules, le type booléen peut apparaître sous deux formes différentes :</p> 
    <ul> 
     <li> <p>La case à cocher obligatoirement s’affiche si le champ est obligatoire et doit être renseigné.</p> <p> <img src="assets/boolean-checkbox-350x158.jpg" style="width: 350;height: 158;"> </p> </li> 
     <li> <p>Les champs facultatifs qui peuvent rester vides s’affichent sous forme de zone de sélection, ce qui permet d’effectuer une sélection parmi trois valeurs : <code>Yes</code>, <code>No</code>, et <code>Not defined</code> (par défaut).</p> <p> <img src="assets/boolean-convert-file-350x129.jpg" style="width: 350;height: 129;"> </p> </li> 
    </ul> <p>Vous pouvez cliquer sur <strong>[!UICONTROL Map]</strong> si vous devez mapper la valeur à un élément d’un autre module.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Date</p> </td> 
   <td> <p>Les dates sont saisies au format de date ISO 8601, par exemple : <code>2015-09-18T11:58Z</code>. Vous pouvez modifier le fuseau horaire dans les paramètres de votre profil. </p> <p>Si vous cliquez sur un champ qui nécessite une date, un calendrier contextuel s’affiche dans les paramètres du module. L’heure n’est pas nécessaire pour certains éléments.</p> <p>Les valeurs des éléments de date sont formatées à l’aide du fuseau horaire local et web sélectionné dans votre profil. Vous pouvez afficher la version ISO 8601 de la valeur d’un élément de date en pointant la souris sur l’élément.</p> <p>Note : si la valeur ISO ne s’affiche pas, l’élément est probablement du texte et non pas une date.</p> <p>L’heure est saisie au format <code>hours:minutes:seconds</code>, par exemple : <code>14:03:52</code>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Buffer (données binaires)</p> </td> 
   <td> <p>Le contenu du fichier est généralement envoyé sous forme de contenu de type buffer (contenu de l’image, fichier vidéo, etc.). Dans certains cas, les données de texte sont incluses dans ce type (par exemple, un fichier texte). [!DNL Workfront Fusion] peut automatiquement convertir des données de texte en code binaire puis en texte et du texte en données de texte puis en code binaire. Pour plus d’informations, voir <a href="/help/workfront-fusion/create-scenarios/map-data/map-files.md" class="MCXref xref">Mappage de fichiers</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Collection</p> </td> 
   <td> <p>Une collection est un élément composé de plusieurs sous-éléments. L’élément Expéditeur ou expéditrice d’un e-mail est un exemple de collection : il contient le nom de l’expéditeur ou de l’expéditrice (type texte) et son adresse e-mail (type texte).</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Sélectionner (menu)</p> </td> 
   <td> <p>Lorsque vous configurez les paramètres du module, vous pouvez choisir parmi plusieurs éléments du même type. Par exemple, le menu de sélection de dossier dans les paramètres des modules [!DNL Dropbox]. </p> <p>Lors de la définition des modules, le menu de sélection peut apparaître sous deux formes :</p> <p> <p>Si plusieurs sélections sont possibles, plusieurs éléments avec des cases à cocher s’affichent.</p> <p> <img src="assets/image-kb-type-list-multi-350x232.jpg" style="width: 350;height: 232;"> </p> </p> <p>Si une seule option est possible, un menu déroulant s’affiche.</p> <p> <img src="assets/select-menu-dropdown-350x130.jpg" style="width: 350;height: 130;"> </p> <p>Si vous devez mapper un élément à partir d’un autre module, utilisez le bouton <strong>Mapper</strong>. Ce bouton ouvre un champ de texte au lieu du menu de sélection. Pour plus d’informations sur le mappage, voir <a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md" class="MCXref xref">Présentation du mappage</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Tableau</p> </td> 
   <td> <p>Vous pouvez utiliser le type de tableau pour utiliser plusieurs valeurs du même type, y compris des collections. Prenons l’exemple des modules [!UICONTROL Email] : ils renvoient un tableau de pièces jointes dont chaque pièce jointe contient le nom, le contenu, la taille, etc. Pour plus d’informations, voir <a href="/help/workfront-fusion/create-scenarios/map-data/map-an-array.md" class="MCXref xref">Mapper un tableau ou un élément de tableau</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Validation</p> </td> 
   <td> <p>[!DNL Workfront Fusion] peut effectuer la validation sur chaque type d’élément. Si un élément ne passe pas la validation, le module arrête le traitement en raison d’une erreur de données. Pour plus d’informations, voir <a href="/help/workfront-fusion/references/errors/error-processing.md" class="MCXref xref">Types d’erreur </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>
