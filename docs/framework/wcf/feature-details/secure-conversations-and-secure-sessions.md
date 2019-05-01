---
title: Conversations sécurisées et sessions sécurisées
ms.date: 03/30/2017
ms.assetid: 48cb104a-532d-40ae-aa57-769dae103fda
ms.openlocfilehash: 9b2c22d6db5a773bfb3f3a41e458b530fc889d71
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61991001"
---
# <a name="secure-conversations-and-secure-sessions"></a>Conversations sécurisées et sessions sécurisées
Une fonctionnalité de Windows Communication Foundation (WCF) est la capacité d’établir des sessions sécurisées entre deux points de terminaison qui s’authentifient mutuellement et mettez-vous d’accord à un processus de signature numérique et le chiffrement. Par exemple, le point de terminaison de service peut demander qu'un point de terminaison de client envoie un jeton de sécurité basé sur un certificat X.509 pour l'authentification. Une fois que le client est authentifié, le point de terminaison de service renvoie un jeton de contexte de sécurité (SCT) au client, utilisé ensuite pour sécuriser tous les messages suivants dans la session. L'établissement de cette session sécurisée permet d'améliorer l'ensemble des messages échangés entre les deux points de terminaison, parce que le SCT a une clé symétrique. Les clés asymétriques, sur lesquelles les certificats X.509 sont basés, requièrent beaucoup plus de puissance de calcul que les clés symétriques pour générer une signature numérique ou chiffrer un jeu de données.  
  
 La stratégie de démarrage (définie dans la section 6.2.7 de la [WS-SecurityPolicy](https://go.microsoft.com/fwlink/?LinkId=99817) standard) contient les assertions de sécurité de message utilisées pour sécuriser le canal et authentifier le client avant l’échange RST/SCT et RSTR/SCT. Certaines liaisons standards de WCF est un `Security.Message.EstablishSecurityContext` propriété qui contrôle si la conversation sécurisée est utilisée. Lorsque vous utilisez des liaisons personnalisées le programme d’amorçage est indiqué par imbrication éléments de liaison de sécurité, soit par le biais [ \<secureConversationBootstrap >](../../../../docs/framework/configure-apps/file-schema/wcf/secureconversationbootstrap.md) dans le fichier de configuration, ou en appelant <xref:System.ServiceModel.Channels.SecurityBindingElement.CreateSecureConversationBindingElement%2A> dans le code.  
  
 Pour plus d’informations sur les sessions, consultez [à l’aide de Sessions](../../../../docs/framework/wcf/using-sessions.md).  
  
## <a name="see-also"></a>Voir aussi

- [Sessions, instanciation et accès concurrentiel](../../../../docs/framework/wcf/feature-details/sessions-instancing-and-concurrency.md)
- [Guide pratique pour Créer un Service qui requiert des Sessions](../../../../docs/framework/wcf/feature-details/how-to-create-a-service-that-requires-sessions.md)
