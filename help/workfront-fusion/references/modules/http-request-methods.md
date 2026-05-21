---
title: Méthodes de requête HTTP
description: Lorsque vous configurez un appel API dans un module, vous devez sélectionner la méthode de requête HTTP. Cet article décrit les méthodes disponibles et les raisons de leur sélection.
author: Becky
feature: Workfront Fusion
exl-id: 481131c9-356a-4c62-a653-d6bba9be5be8
TQID: https://experienceleague.adobe.com/Z11y3dk6PtoN11Gja8S2ZyJlTJZNZfXfcPPrNJWvbRk
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 303
ht-degree: 55%

---

# Méthodes de requête HTTP

Lorsque vous configurez un appel API dans un module, vous devez sélectionner la méthode de requête HTTP. Cet article décrit les méthodes disponibles et les raisons de leur sélection.

## Méthodes HTTP

Utilisez l’une des méthodes HTTP suivantes.

* **[!UICONTROL GET]** : récupère les données d’un serveur web en fonction de vos paramètres. [!UICONTROL GET] demande une représentation de la ressource spécifiée et reçoit un message de réponse [!UICONTROL 200 OK] avec le contenu demandé en cas de succès.
* **[!UICONTROL POST]** : envoie des données à un serveur web en fonction de vos paramètres. Les requêtes [!UICONTROL POST] comprennent des actions telles que le chargement d’un fichier. Plusieurs [!UICONTROL POST]s peuvent avoir un résultat différent d’un seul [!UICONTROL POST]. Soyez donc prudent en cas d’envoi involontaire de plusieurs [!UICONTROL POST]. Si une opération [!UICONTROL POST] réussit, vous recevez un message de réponse [!UICONTROL 200 OK].
* **[!UICONTROL PUT]** : envoie des données à un emplacement du serveur web en fonction de vos paramètres. Les requêtes [!UICONTROL PUT] comprennent des actions telles que le chargement d’un fichier. La différence entre un [!UICONTROL PUT] et un [!UICONTROL POST] est que PUT est idempotent, ce qui signifie que le résultat d’un seul [!UICONTROL PUT] réussi est le même que de nombreux [!UICONTROL PUT] identiques. Si un PUT est réussi, vous recevez un message de réponse 200 (généralement 201 ou 204).
* **[!UICONTROL PATCH]** : (non disponible pour certains modules d’appel API) applique des modifications partielles à une ressource sur un serveur web en fonction de vos paramètres. [!UICONTROL PATCH] n’est pas idempotent, ce qui signifie que le résultat de plusieurs requêtes [!UICONTROL PATCH] pourrait avoir des conséquences inattendues. Si une requête [!UICONTROL PATCH] réussit, vous recevrez un message de réponse 200 (généralement 204).
* **[!UICONTROL DELETE]** : supprime la ressource spécifiée du serveur web en fonction de vos paramètres (si la ressource existe). Si une requête [!UICONTROL DELETE] réussit, vous recevez un message de réponse 200 OK.
