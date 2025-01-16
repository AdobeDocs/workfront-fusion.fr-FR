---
title: Configuration des adresses IP pour Fusion dans la place sur la liste autorisée de données de votre entreprise
description: Fusion utilise des adresses IP et des domaines spécifiques pour la communication web. Ces éléments doivent être ajoutés à la liste autorisée de votre entreprise pour que vous puissiez utiliser Workfront dans votre organisation.
author: Becky
feature: Workfront Fusion
exl-id: 406dd45c-0863-4270-a80e-c1c115e0b367
source-git-commit: 59d739093c88238af7a7e97499fd0c7d7cf6053a
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 49%

---

# Configuration des adresses IP pour Fusion dans la place sur la liste autorisée de données de votre entreprise

Comme Adobe Workfront Fusion communique avec le réseau de votre entreprise, le pare-feu de cette dernière doit être configuré pour autoriser cette communication. Les pare-feux sont des mesures de sécurité très efficaces qui séparent le réseau d’une entreprise d’Internet. Ils garantissent que seules les données et le trafic réseau sélectionnés peuvent entrer ou sortir du réseau de l’entreprise. Le pare-feu autorise ou bloque les données en fonction du site qui les envoie ou les reçoit. En tant qu’administrateur ou administratrice Fusion, vous devez vous assurer que les données envoyées à ou depuis Fusion peuvent passer par le pare-feu de votre entreprise.

Pour ce faire, il vous faut une liste autorisée, qui est pour ainsi dire une « liste » des sites « autorisés » à envoyer ou recevoir des données par le biais du pare-feu. Les sites peuvent être identifiés de deux façons :

* **Adresse IP** : une série de nombres comme 52.31.132.175.
* **Domaine** : partie d’une URL, telle que `thisdomain` dans `www.thisdomain.com`

Fusion utilise des adresses IP et des domaines spécifiques pour la communication web. Ces éléments doivent être ajoutés à la liste autorisée de votre entreprise pour que vous puissiez utiliser Workfront dans votre organisation.

En règle générale, une liste autorisée est configurée par un administrateur réseau. Contactez l’administrateur ou l’administratrice réseau de votre entreprise pour vous assurer que votre pare-feu autorise ces adresses IP. Si vous ne savez pas qui est votre administrateur ou administratrice réseau, le service informatique de votre entreprise peut vous assister.

>[!IMPORTANT]
>
>En tant qu’administrateur ou administratrice de Fusion, vous devez vous assurer que ces adresses IP et domaines sont ajoutés à la place sur la liste autorisée de données de votre organisation. Cela est valable même si vous ne les ajoutez pas vous-même. Fusion ne peut pas configurer la place sur la liste autorisée de votre organisation.

Placer sur la liste autorisée Vous pouvez ajouter tous les domaines et adresses IP Fusion à votre cluster, ou vous pouvez localiser votre cluster Fusion et ajouter uniquement les domaines et adresses IP de ce cluster.

## Ajouter tous les domaines et adresses IP Fusion

Ajoutez les adresses IP suivantes à votre place sur la liste autorisée :

* 52.30.133.50
* 54.220.93.204
* 34.254.76.122
* 54.244.142.219
* 52.39.217.230
* 44.241.82.96
* 100.20.126.137
* 34.223.32.4
* 52.39.176.220
* 20.36.133.48/28
* 20.81.156.240/28
* 172.172.84.48/28

En outre, si votre organisation utilise le filtrage réseau sortant, ajoutez le domaine suivant à votre liste autorisée pour permettre à votre système d’accéder à Workfront Fusion.

* hook.app.workfrontfusion.com
* hook.app-eu.workfrontfusion.com
* hook.app-az.workfrontfusion.com

## Ajoutez des adresses IP et des domaines Fusion pour votre cluster uniquement

### Identification de votre centre de données

Les adresses IP varient en fonction de l’emplacement de stockage de vos données.

Si vous accédez à Fusion par le biais d’une URL, vous pouvez examiner l’URL pour localiser votre centre de données.

| URL | Datacenter |
| --- | --- |
| `https://app.workfrontfusion.com` | centre de données des États-Unis |
| `https://app-eu.workfrontfusion.com` | centre de données de l&#39;UE |
| `https://app-az.workfrontfusion.com` | Cluster Azure |

Si vous accédez à Fusion via `experience.adobe.com`, vous pouvez vérifier l’onglet réseau dans votre navigateur pour identifier le centre de données.

| URL | Datacenter |
| --- | --- |
| Appels à `https://fusion.adobe.com` | centre de données des États-Unis |
| Appels à `https://eu.fusion.adobe.com` | centre de données de l&#39;UE |
| Appels à `https://az.fusion.adobe.com` | Cluster Azure |

### Ajouter des adresses IP et des domaines pour votre centre de données

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] Centre de données de l’UE</td> 
   <td> 
    <ul> 
     <li>52.30.133.50</li> 
     <li>54.220.93.204</li> 
     <li>34.254.76.122</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!DNL Adobe Workfront] Centre de données des États-Unis</p> </td> 
   <td> 
    <ul> 
     <li>54.244.142.219</li> 
     <li>52.39.217.230</li> 
     <li>44.241.82.96</li>
     <li>100.20.126.137</li>
     <li>34.223.32.4</li>
     <li>52.39.176.220</li>
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] sur le cluster Microsoft Azure</td> 
   <td> 
    <ul> 
     <li>20.36.133.48/28</li> 
     <li>20.81.156.240/28</li> 
     <li>172.172.84.48/28</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

De même, si votre entreprise utilise le filtrage de réseau sortant, ajoutez le domaine suivant à votre place sur la liste autorisée pour permettre à votre système d’accéder à Workfront Fusion. Ils sont utilisés pour les Webhooks

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] Centre de données de l’UE</td> 
   <td> <p> hook.app-eu.workfrontfusion.com </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!DNL Adobe Workfront] Centre de données des États-Unis</p> </td> 
   <td> <p>hook.app.workfrontfusion.com </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!DNL Adobe Workfront Fusion] sur le cluster Microsoft Azure</p> </td> 
   <td> <p>hook.app-az.workfrontfusion.com </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Le filtrage de réseau sortant est rare. Vérifiez auprès de votre équipe d’administration réseau si vous devez mettre à jour votre liste autorisée pour l’adapter.
