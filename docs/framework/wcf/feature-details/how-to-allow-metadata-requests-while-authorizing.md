---
title: 'Procédure : autoriser les requêtes de métadonnées pendant l’autorisation'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- allowing metadata requests while authorizing [WCF]
ms.assetid: 90cec34f-b619-452b-a056-8b1c0de49d05
ms.openlocfilehash: bea4f7e90df29678697fe6708bdc6a73145522db
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59317699"
---
# <a name="how-to-allow-metadata-requests-while-authorizing"></a>Procédure : autoriser les requêtes de métadonnées pendant l’autorisation
Pendant l'autorisation personnalisée, il peut être nécessaire d'autoriser le traitement d'une demande de métadonnées. La rubrique suivante présente les étapes de validation d'une telle demande.  
  
 Pour plus d’informations sur l’autorisation de Windows Communication Foundation (WCF), consultez [autorisation](../../../../docs/framework/wcf/feature-details/authorization-in-wcf.md).  
  
### <a name="to-allow-metadata-requests-during-authorization"></a>Pour autoriser les demandes de métadonnées pendant l'autorisation  
  
1. Créez une extension de la classe <xref:System.ServiceModel.ServiceAuthorizationManager>.  
  
2. Remplacez la méthode <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccessCore%2A> . La méthode retourne la valeur `true` ou `false` selon que l'autorisation est accordée ou non. Les informations relatives à la procédure en cours se trouvent dans le <xref:System.ServiceModel.OperationContext> passé comme paramètre à la méthode.  
  
3. Dans la substitution, vérifiez le nom de contrat, l'espace de noms et l'action comme illustré dans l'exemple suivant. Si les conditions sont valides, retournez `true.`  
  
4. Utilisez le point d'extensibilité pour employer la classe. Pour plus d'informations, voir [Procédure : Créer un gestionnaire d’autorisation personnalisé pour un Service](../../../../docs/framework/wcf/extending/how-to-create-a-custom-authorization-manager-for-a-service.md).  
  
## <a name="example"></a>Exemple  
 L'exemple suivant illustre une substitution de la méthode <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccessCore%2A>.  
  
 [!code-csharp[C_HowtoCheckForMexRequestsInAuthorization#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howtocheckformexrequestsinauthorization/cs/source.cs#1)]
 [!code-vb[C_HowtoCheckForMexRequestsInAuthorization#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howtocheckformexrequestsinauthorization/vb/source.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.ServiceAuthorizationManager>
- [Autorisation](../../../../docs/framework/wcf/feature-details/authorization-in-wcf.md)
- [Gestion des revendications et autorisation avec le modèle d’identité](../../../../docs/framework/wcf/feature-details/managing-claims-and-authorization-with-the-identity-model.md)
