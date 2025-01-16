---
title: Méthodes de requête HTTP
description: Lorsque vous configurez un appel API dans un module, vous devez sélectionner la méthode de requête HTTP. Cet article décrit les méthodes disponibles et les raisons de leur sélection.
author: Becky
feature: Workfront Fusion
exl-id: 481131c9-356a-4c62-a653-d6bba9be5be8
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 3%

---

# Méthodes de requête HTTP

Lorsque vous configurez un appel API dans un module, vous devez sélectionner la méthode de requête HTTP. Cet article décrit les méthodes disponibles et les raisons de leur sélection.

## Méthodes HTTP

Utilisez l’une des méthodes HTTP suivantes.

* **[!UICONTROL GET]** : récupère les données d’un serveur web en fonction de vos paramètres. [!UICONTROL GET] demande une représentation de la ressource spécifiée et reçoit un message de réponse [!UICONTROL 200 OK] avec le contenu demandé en cas de réussite.
* **[!UICONTROL POST]** : envoie les données à un serveur web en fonction de vos paramètres. Les requêtes [!UICONTROL POST] incluent des actions telles que le chargement d’un fichier. L’envoi de plusieurs [!UICONTROL POST] peut avoir un résultat différent de celui d’un seul [!UICONTROL POST]. Par conséquent, faites attention à ne pas envoyer involontairement plusieurs [!UICONTROL POST]. Si une [!UICONTROL POST] réussit, vous recevez un message de réponse [!UICONTROL 200 OK].
* **[!UICONTROL PUT]** : envoie les données à un emplacement du serveur web en fonction de vos paramètres. Les requêtes [!UICONTROL PUT] incluent des actions telles que le chargement d’un fichier. La différence entre un [!UICONTROL PUT] et un [!UICONTROL POST] réside dans le fait que le PUT est idempotent, ce qui signifie que le résultat d’un seul [!UICONTROL PUT] réussi est le même que celui de nombreux [!UICONTROL PUT] identiques. Si un PUT réussit, vous recevez un message de réponse 200 (généralement 201 ou 204).
* **[!UICONTROL PATCH]** : (non disponible pour certains modules d’appel API) applique des modifications partielles à une ressource sur un serveur web en fonction de vos paramètres. [!UICONTROL PATCH] n’est pas idempotent, ce qui signifie que le résultat de plusieurs [!UICONTROL PATCH] peut avoir des conséquences inattendues. Si une [!UICONTROL PATCH] réussit, vous recevrez un message de réponse 200 (généralement 204).
* **[!UICONTROL DELETE]** : supprime la ressource spécifiée du serveur web en fonction de vos paramètres (si la ressource existe). Si une [!UICONTROL DELETE] réussit, vous recevez un message de réponse 200 OK.
