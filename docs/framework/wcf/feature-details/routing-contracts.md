---
title: Contrats de routage
ms.date: 03/30/2017
ms.assetid: 9ceea7ae-ea19-4cf9-ba4f-d071e236546d
ms.openlocfilehash: 660652caa804b8c19f6dd18bcba51bf4abc3ba12
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59145351"
---
# <a name="routing-contracts"></a>Contrats de routage
Les contrats de routage définissent les modèles de messages que le service de routage peut traiter.  Chaque contrat est sans type et permet au service de recevoir un message sans connaissance du schéma ni de l'action du message. Cela permet au service de routage de router des messages de manière générique, sans configuration supplémentaire pour les caractéristiques sous-jacentes des messages routés.  
  
## <a name="routing-contracts"></a>Contrats de routage  
 Puisque le service de routage accepte un objet Message WCF générique, le plus important lorsque vous sélectionnez un contrat est de prendre en compte la forme du canal utilisé lors de la communication avec les clients et les services. Lors du traitement des messages, le service de routage utilise des pompes de messages symétriques, en conséquence, la forme du contrat entrant doit généralement correspondre à la forme du contrat sortant. Toutefois, il existe des cas où les répartiteur du modèle de Service peuvent modifier les formes, telles que lorsque le répartiteur convertit un canal duplex dans un canal de demande-réponse, ou supprime la prise en charge de la session à partir d’un canal lorsqu’il n’est pas obligatoire et n’est pas utilisé (autrement dit Lorsque **SessionMode.Allowed**, la conversion une **IInputSessionChannel** dans un **IInputChannel**).  
  
 Pour prendre en charge ces pompes de messages, le service de routage fournit des contrats dans l'espace de noms <xref:System.ServiceModel.Routing>, qui doivent être utilisés lors de la définition des points de terminaison de service utilisés par le service de routage. Ces contrats sont sans type, ce qui autorise la réception de tout type ou action de message et permet au service de routage de gérer des messages sans connaître le schéma de message spécifique. Pour plus d’informations sur les contrats utilisés par le Service de routage, consultez [contrats de routage](../../../../docs/framework/wcf/feature-details/routing-contracts.md).  
  
 Les contrats fournis par le service de routage se trouvent dans l'espace de noms <xref:System.ServiceModel.Routing> et sont décrits dans le tableau suivant.  
  
|Contrat|Forme|Forme de canal|  
|--------------|-----------|-------------------|  
|<xref:System.ServiceModel.Routing.ISimplexDatagramRouter>|SessionMode = SessionMode.Allowed<br /><br /> AsyncPattern = true<br /><br /> IsOneWay = true|IInputChannel -> IOutputChannel|  
|<xref:System.ServiceModel.Routing.ISimplexSessionRouter>|SessionMode = SessionMode.Required<br /><br /> AsyncPattern = true<br /><br /> IsOneWay = true|IInputSessionChannel -> IOutputSessionChannel|  
|<xref:System.ServiceModel.Routing.IRequestReplyRouter>|SessionMode = SessionMode.Allowed<br /><br /> AsyncPattern = true|IReplyChannel -> IRequestChannel|  
|<xref:System.ServiceModel.Routing.IDuplexSessionRouter>|SessionMode=SessionMode.Required<br /><br /> CallbackContract=typeof(ISimplexSession)<br /><br /> AsyncPattern = true<br /><br /> IsOneWay = true<br /><br /> TransactionFlow(TransactionFlowOption.Allowed)|IDuplexSessionChannel -> IDuplexSessionChannel|  
  
## <a name="see-also"></a>Voir aussi

- [Service de routage](../../../../docs/framework/wcf/feature-details/routing-service.md)
- [Introduction au routage](../../../../docs/framework/wcf/feature-details/routing-introduction.md)
