---
title: 'Procédure : Exécuter des requêtes de Service de données asynchrones (WCF Data Services)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF Data Services, asynchronous operations
- asynchronous operations [WCF Data Services]
ms.assetid: 902a2dc1-d0e9-4b00-90a8-becc4cb1f6a7
ms.openlocfilehash: f89a5004afeffe5aa9a28cb2d43374aede8a935e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61936524"
---
# <a name="how-to-execute-asynchronous-data-service-queries-wcf-data-services"></a>Procédure : Exécuter des requêtes de Service de données asynchrones (WCF Data Services)
En utilisant les bibliothèques clientes [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)], vous pouvez effectuer de façon asynchrone des opérations client-serveur, telles que l'exécution de requêtes et l'enregistrement de modifications. Pour plus d’informations, consultez [opérations asynchrones](../../../../docs/framework/data/wcf/asynchronous-operations-wcf-data-services.md).  
  
> [!NOTE]
>  Dans une application où le rappel doit être appelé sur un thread spécifique, vous devez marshaler explicitement l'exécution de la méthode <xref:System.Data.Services.Client.DataServiceQuery%601.EndExecute%2A>. Pour plus d’informations, consultez [opérations asynchrones](../../../../docs/framework/data/wcf/asynchronous-operations-wcf-data-services.md).  
  
 L'exemple dans cette rubrique utilise l'exemple de service de données Northwind et des classes de service de données clientes générées automatiquement. Ce service et les classes de données client sont créés lorsque vous complétez le [démarrage rapide WCF Data Services](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md).  
  
## <a name="example"></a>Exemple  
 L'exemple suivant montre comment exécuter une requête asynchrone en appelant la méthode <xref:System.Data.Services.Client.DataServiceQuery%601.BeginExecute%2A> pour démarrer la requête. Le délégué inline delegate appelle la méthode <xref:System.Data.Services.Client.DataServiceQuery%601.EndExecute%2A> pour afficher les résultats de la requête.  
  
 [!code-csharp[Astoria Northwind Client#ExecuteQueryAsync](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/source.cs#executequeryasync)]
 [!code-vb[Astoria Northwind Client#ExecuteQueryAsync](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/source.vb#executequeryasync)]  
  
## <a name="see-also"></a>Voir aussi

- [Bibliothèque cliente WCF Data Services](../../../../docs/framework/data/wcf/wcf-data-services-client-library.md)
