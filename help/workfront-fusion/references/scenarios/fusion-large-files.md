---
title: Utilisation de fichiers volumineux
description: La prise en charge des fichiers volumineux est actuellement disponible pour les connecteurs Workfront et HTTP.
author: Becky
feature: Workfront Fusion
exl-id: 6df81943-e70c-42b3-aa44-d82343598a51
source-git-commit: a5a98d2e0b246d46389d4574e29f91c74f053472
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 3%

---

# Utilisation de fichiers volumineux

>[!IMPORTANT]
>
>La fonctionnalité de fichiers volumineux n’est disponible que pour les organisations qui utilisent le package Workfront Ultimate.

Des fonctionnalités améliorées de transfert de données sont désormais disponibles dans Workfront Fusion, ce qui permet aux scénarios de traiter des fichiers beaucoup plus volumineux.

Pour gérer des fichiers plus volumineux, vos scénarios doivent être mis à jour.

## Connecteurs prenant en charge les fichiers volumineux

Actuellement, les connecteurs suivants prennent en charge les fichiers volumineux.

>[!NOTE]
>
>* Si un fichier est téléchargé à l’aide d’un module qui prend en charge les fichiers volumineux, puis transmis à un module qui ne prend pas en charge les fichiers volumineux, ce module ne traite pas le fichier avec succès. Les fichiers volumineux doivent être gérés exclusivement avec des modules pris en charge dans l’ensemble du workflow.
>* Les modules qui ne prennent pas en charge les fichiers volumineux peuvent traiter des fichiers d’une taille allant jusqu’à 200 Mo.

* Workfront
   * Charger le document
   * Télécharger document
* Adobe Experience Manager Assets
   * Charger le document
* Workfront Proof
   * Charger fichier
   * Télécharger l&#39;épreuve
* Adobe Authenticator
   * Effectuer un appel API personnalisé
* SharePoint
   * Créer un fichier
   * Obtenir un fichier
* Salesforce
   * Charger fichier
* AWS S3
   * Charger fichier
   * Obtenir le fichier
* HTTP

D’autres connecteurs seront pris en charge dans les prochaines versions.

## Mettez à jour vos scénarios pour gérer les fichiers volumineux

Le module Workfront > Charger le document a été modifié pour gérer les fichiers plus volumineux. L’ancienne version de ce module affiche désormais `(Legacy)` ajouté au nom du module. Dans la plupart des cas, le module hérité continuera à fonctionner.

Si vous envisagez d’utiliser des fichiers plus volumineux, nous vous recommandons de remplacer l’ancien module par le nouveau module Charger un document . Le nouveau module Charger le document empêche les dépassements de délai et autres erreurs.

![Charger un document](assets/new-upload-document.png)

## Questions fréquentes

### Quelle est la nouvelle limite de taille de fichier ?

Les utilisateurs peuvent désormais traiter les fichiers dépassant la limite précédente de 1 Go, ce qui améliore l’efficacité et la productivité.  Bien que la plateforme puisse prendre en charge des fichiers individuels allant jusqu’à 15 Go pour une seule action (comme le chargement d’un fichier), d’autres facteurs affectent le transfert de données. La limite de taille de fichier d’une seule action dépend en fin de compte du service web auquel Fusion se connecte. Le transfert de données est le traitement total d’une seule exécution. Cela signifie que plusieurs actions en une seule exécution contribuent au transfert total de données.

Fusion traite les fichiers jusqu’à ce que la limite d’exécution de 40 minutes soit atteinte. Dans votre scénario Fusion, le chargement, le téléchargement ou le traitement des fichiers volumineux peut prendre un certain temps. Bien qu’il n’existe aucune limite sur la taille des fichiers individuels, le temps d’exécution du scénario est limité à 40 minutes. Par conséquent, si des fichiers volumineux entraînent une exécution de plus de 40 minutes, le scénario échoue. Le temps d’exécution du scénario peut également être affecté par la taille du scénario, la complexité du module et la vitesse du réseau. Par conséquent, nous vous recommandons de tenir compte de ces aspects de vos scénarios lors de l’utilisation de fichiers volumineux.

### Comment fonctionne le nouveau transfert de fichiers de Fusion ?

Lorsque Fusion traite des fichiers, des fichiers plus volumineux sont ajoutés au stockage persistant (stockage de compartiment S3 ou Azure Blob). Lorsqu’un module Fusion exécute une action de fichier, telle que le chargement ou le téléchargement, Fusion utilise le fichier dans le stockage persistant en tant que source plutôt qu’en tant que mémoire active.

### Puis-je travailler avec des fichiers plus volumineux en utilisant des exécutions incomplètes ?

Oui, Fusion prend en charge les exécutions incomplètes avec des fichiers plus volumineux. Notez que les exécutions incomplètes sont limitées en taille pour une organisation et doivent être gérées activement.

### Puis-je utiliser des fichiers plus volumineux avec n’importe quel connecteur ?

Chaque connecteur Fusion doit être mis à jour pour prendre en charge les fichiers plus volumineux. Les connecteurs pris en charge sont Workfront, HTTP et AEM Assets. Les connecteurs Fusion sont toujours limités par la taille de fichier prise en charge par le service web. Les limites de taille de fichier sont généralement incluses dans la documentation de l’API pour les points d’entrée de service web qui téléchargent et chargent des fichiers.

### Cela affecte-t-il les opérations ?

Non, le nombre d’opérations exécutées par un module est le même.

### Quand l’interface utilisateur de Fusion sera-t-elle mise à jour pour afficher les données de transfert de fichiers ?

Cette fonctionnalité a déjà été terminée et déployée en production.

### Quelles sont les différentes manières d’appréhender les nouvelles limites de traitement des fichiers pour faciliter la conception de scénarios ?

Concevoir un scénario qui fonctionne dans la limite d’exécution de 40 minutes peut sembler compliqué. Nous vous recommandons de garder à l’esprit les points suivants lors de la conception d’un scénario :

* **Comprenez les besoins de votre entreprise en termes de temps d’exécution** : la limite de temps d’exécution de la plateforme Fusion est de 40 minutes, mais la plupart des automatisations de processus d’entreprise devraient s’exécuter beaucoup plus rapidement. Par exemple, les automatisations lancées par l’utilisateur avec une continuation dépendante du résultat devraient se terminer bien en deçà de la limite de 40 minutes.
* **Tenir compte du temps d’exécution lors de la conception** : lors de la conception de votre scénario, il est essentiel de comprendre le temps d’exécution du module pour les actions de fichiers individuels, telles que les chargements et les téléchargements. Ces connaissances vous aident à planifier des scénarios qui impliquent plusieurs actions de fichier.  Pour garantir la précision de votre conception, nous vous recommandons d’arrondir le temps d’exécution du module à l’unité supérieure pour inclure une mémoire tampon.
Par exemple, si Fusion télécharge un document en 144 secondes (2,4 minutes), vous pouvez vous attendre à ce qu’une seule exécution effectue plusieurs fois des actions similaires. Dans cet exemple, l’exécution du module prend 144 secondes et vous devez prévoir un temps d’exécution de 3 minutes pour le téléchargement. Si vos exigences incluent à la fois un chargement et un téléchargement, le temps d’exécution attendu est d’environ 6 minutes. Notez que les délais d’exécution de Fusion sont plafonnés à 40 minutes.

* **Actions de consolidation de fichier** : l’exemple le plus courant d’actions de fichier dans un scénario Fusion est un téléchargement et un téléchargement. La plupart des scénarios comportant uniquement ces deux actions s’exécutent en quelques minutes. Dans la mesure du possible, les concepteurs de Fusion doivent limiter leurs scénarios à un téléchargement et à un chargement.

* **Calculer la taille à l’aide du panneau de mappage** : Workfront et les autres services web incluent la taille de fichier d’un fichier dans la sortie du module de téléchargement. Vous pouvez utiliser ces données pour filtrer les fichiers trop volumineux pour un chargement de module ou trop volumineux pour le temps d’exécution du scénario.

* **Isoler les actions de fichier dans leur propre scénario lorsque vous travaillez avec plusieurs fichiers** : les concepteurs de Fusion doivent envisager d’isoler les actions de fichier dans des scénarios distincts. Par exemple, un scénario Fusion déclenché par une nouvelle demande Workfront avec plusieurs fichiers joints peut devoir contenir jusqu’à 30 fichiers. Étant donné que le chargement et le téléchargement de chaque fichier peuvent prendre jusqu’à 3 minutes, le traitement de tous les fichiers en une seule exécution dépasse la limite d’exécution de 40 minutes de Fusion. La solution consiste à créer un scénario d’actions sur les fichiers dédié à la gestion du chargement et du téléchargement des fichiers individuels. Le scénario déclenché par la requête effectue une itération sur les fichiers joints, invoquant le scénario d’actions sur les fichiers pour chaque fichier à l’aide du module HTTP. Cette approche garantit que chaque fichier est traité dans les délais d’exécution.

<!--
## Connectors that do not support large files

Some Fusion connectors do not support large files. For these connectors, Fusion's total processing capacity for files is **1 GB**. 

This limit is based on a total memory cost. Every operation contributes to that cost. If a single file of 400 MB is downloaded and uploaded then the total cost to the file capacity would be 800 MB.

The following connectors do **not** support large files. 

* Archive
* Box
* Convert
* CSV
* Datastores
* Flow control
* FTP
* JSON
* JWT
* Markdown
* Math
* Microsoft Word templates
* MIME
* Microsoft SQL
* SFTP
* Adobe Acrobat Sign
* SOAP
* Tools
* XML

If a connector is not on this list, it does not support large files. For these connectors, Fusion's total processing capacity for files is **1 GB**. 

This limit is based on a total memory cost. Every operation contributes to that cost. If a single file of 400 MB is downloaded and uploaded then the total cost to the file capacity would be 800 MB.-->






<!--## Connectors that support large files

The following connectors support large files.

Workfront
HTTP
Webhooks
Salesforce
Microsoft Email
Workfront Proof
AEM Assets
Email
Slack
Jira
Microsoft Excel
SharePoint
Frame.io
Adobe PDF Services
Marketo
Azure Devops 
Google Email
Jira Server
Google Sheets
Microsoft OneDrive
ServiceNow 
AWS S3
Bynder
OneDrive Business
Adobe Authenticator
Google Drive
Microsoft Dynamics
Google Docs
NetSuite
Airtable
Azure AD
QuickBase 
Adobe Target
Adobe Campaign Classic
Microsoft Calendar
Workfront Planning
HubSpot CRM  
DropBox
Cloud Convert
Egnyte
Adobe Firefly
OpenAI / Chat GPT
Allocadia
Cvent
GitLab 
Google Team Drive
Google Calendar
Workfront SDL Managed Translation
Widen
Workfront Boards
Google Slides
Qualtrics
Microsoft Power BI
Adobe Photoshop
Anaplan
DocuSign 
MariaDB
Adobe Creative Cloud Libraries
Figma
AEM Forms
Datadog
GitHub 
Google Forms
Adobe I/O Events
Trello
Workday
Adobe Journey Optimizer
Adobe Lightroom


If a file is not on this list, it does not support large files. For these connectors, Fusion's total processing capacity for files is **1 GB**. 

This limit is based on a total memory cost. Every operation contributes to that cost. If a single file of 400 MB is downloaded and uploaded then the total cost to the file capacity would be 800 MB.

-->
