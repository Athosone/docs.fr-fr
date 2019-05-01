---
title: 'Procédure : utiliser ChannelFactory'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d48f01b5-582b-4c8b-b547-8adddae7e371
ms.openlocfilehash: 7d542a3dcae514e75194b49c23a8dec5dd7e8c3b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62047254"
---
# <a name="how-to-use-the-channelfactory"></a>Procédure : utiliser ChannelFactory
La classe <xref:System.ServiceModel.ChannelFactory%601> générique est utilisée dans les scénarios avancés qui requièrent la création d'une fabrication de canal pouvant être utilisée pour créer plusieurs canaux.  
  
### <a name="to-create-and-use-the-channelfactory-class"></a>Pour créer et utiliser la classe ChannelFactory  
  
1. Générez et exécutez un service Windows Communication Foundation (WCF). Pour plus d’informations, consultez [conception et implémentation de Services](../../../../docs/framework/wcf/designing-and-implementing-services.md), [configuration des Services](../../../../docs/framework/wcf/configuring-services.md), et [Services d’hébergement](../../../../docs/framework/wcf/hosting-services.md).  
  
2. Utilisez le [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) pour générer le contrat (interface) pour le client.  
  
3. Dans le code client, utilisez la classe <xref:System.ServiceModel.ChannelFactory%601> pour créer plusieurs écouteurs de point de terminaison.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[c_HowToUseChannelFactory#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howtousechannelfactory/cs/source.cs#1)]
 [!code-vb[c_HowToUseChannelFactory#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howtousechannelfactory/vb/source.vb#1)]
