---
title: Intercepteurs (services de données WCF)
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF Data Services, customizing
- query interceptors [WCF Data Services]
ms.assetid: e33ae8dc-8069-41d0-99a0-75ff28db7050
ms.openlocfilehash: 17926e144fae206d702c2bcb4f88dd2093442ed5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61876224"
---
# <a name="interceptors-wcf-data-services"></a>Intercepteurs (services de données WCF)
[!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] permet à une application d’intercepter les messages de demande afin que vous pouvez ajouter une logique personnalisée à une opération. Vous pouvez utiliser cette logique personnalisée pour valider les données dans les messages entrants. Vous pouvez également l'utiliser pour restreindre davantage l'étendue d'une requête d'interrogation, comme l'insertion d'une stratégie d'autorisation personnalisée sur la base de chaque demande.  
  
 L'interception est effectuée par les méthodes attribuées spécialement dans le service de données. Ces méthodes sont appelées par [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] au point approprié dans le traitement du message. Les intercepteurs sont définis sur une base de jeu par entité, et les méthodes d’intercepteur ne peut pas accepter de paramètres de la demande, telles que les opérations de service peuvent. Les méthodes d’intercepteur de requête, qui sont appelées lors du traitement d’une requête HTTP GET, doivent retourner une expression lambda qui détermine si une instance d’entité de l’intercepteur doit être retournée par les résultats de requête. Cette expression est utilisée par le service de données pour affiner davantage l'opération demandée. L'exemple suivant illustre la définition d'un intercepteur de requête.  
  
 [!code-csharp[Astoria Northwind Service#QueryInterceptorDef](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_service/cs/northwind2.svc.cs#queryinterceptordef)]
 [!code-vb[Astoria Northwind Service#QueryInterceptorDef](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_service/vb/northwind2.svc.vb#queryinterceptordef)]  
  
 Pour plus d'informations, voir [Procédure : Intercepter les Messages de Service de données](../../../../docs/framework/data/wcf/how-to-intercept-data-service-messages-wcf-data-services.md).  
  
 Les intercepteurs de modification, appelés lors du traitement d'opérations de non-requête, doivent retourner `void` (`Nothing` en Visual Basic). Les méthodes d'intercepteur de requête doivent accepter les deux paramètres suivants :  
  
1. Un paramètre d'un type qui est compatible avec le type d'entité du jeu d'entités. Lorsque le service de données appelle l'intercepteur de modification, la valeur de ce paramètre reflétera les informations d'entité envoyées par la demande.  
  
2. Un paramètre de type <xref:System.Data.Services.UpdateOperations>. Lorsque le service de données appelle l'intercepteur de modification, la valeur de ce paramètre reflétera l'opération que tente d'effectuer la demande.  
  
 L'exemple suivant illustre la définition d'un intercepteur de modification.  
  
 [!code-csharp[Astoria Northwind Service#ChangeInterceptorDef](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_service/cs/northwind2.svc.cs#changeinterceptordef)]
 [!code-vb[Astoria Northwind Service#ChangeInterceptorDef](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_service/vb/northwind2.svc.vb#changeinterceptordef)]  
  
 Pour plus d'informations, voir [Procédure : Intercepter les Messages de Service de données](../../../../docs/framework/data/wcf/how-to-intercept-data-service-messages-wcf-data-services.md).  
  
 Les attributs suivants sont pris en charge pour l'interception.  
  
 **[QueryInterceptor(** *EntitySetName* **)]**  
 Les méthodes qui appliquent l'attribut <xref:System.Data.Services.QueryInterceptorAttribute> sont appelées lorsqu'une demande HTTP GET est reçue pour la ressource de jeu d'entités ciblée. Ces méthodes doivent toujours retourner une expression lambda sous la forme `Expression<Func<T,bool>>`.  
  
 **[ChangeInterceptor(** *EntitySetName* **)]**  
 Les méthodes qui appliquent l'attribut <xref:System.Data.Services.ChangeInterceptorAttribute> sont appelées lorsqu'une demande HTTP différente d'une demande HTTP GET est reçue pour la ressource de jeu d'entités ciblée. Ces méthodes doivent toujours retourner `void` (`Nothing` en Visual Basic).  
  
 Pour plus d'informations, voir [Procédure : Intercepter les Messages de Service de données](../../../../docs/framework/data/wcf/how-to-intercept-data-service-messages-wcf-data-services.md).  
  
## <a name="see-also"></a>Voir aussi

- [Opérations de service](../../../../docs/framework/data/wcf/service-operations-wcf-data-services.md)
