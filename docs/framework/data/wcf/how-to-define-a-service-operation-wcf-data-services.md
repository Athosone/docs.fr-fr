---
title: 'Procédure : Définir une opération de Service (WCF Data Services)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Service Operations [WCF Data Services]
- WCF Data Services, service operations
ms.assetid: dfcd3cb1-2f07-4d0b-b16a-6b056c4f45fa
ms.openlocfilehash: dbd14ba9ed24fb3f18946e817f61f8cbf2e9b1b5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59973653"
---
# <a name="how-to-define-a-service-operation-wcf-data-services"></a>Procédure : Définir une opération de Service (WCF Data Services)

[!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] exposent des méthodes définies sur le serveur comme des opérations de service. Opérations de service permettent à un service de données fournir l’accès via un URI à une méthode qui est définie sur le serveur. Pour définir une opération de service, appliquez le [`WebGet]` ou `[WebInvoke]` d’attribut à la méthode. Pour prendre en charge les opérateurs de requête, l’opération de service doit retourner un <xref:System.Linq.IQueryable%601> instance. Les opérations de service peuvent accéder à la source de données sous-jacente via la propriété <xref:System.Data.Services.DataService%601.CurrentDataSource%2A> sur <xref:System.Data.Services.DataService%601>. Pour plus d’informations, consultez [opérations de Service](../../../../docs/framework/data/wcf/service-operations-wcf-data-services.md).

L'exemple dans cette rubrique définit une opération de service nommée `GetOrdersByCity` qui retourne une instance <xref:System.Linq.IQueryable%601> filtrée d'objets `Orders` et  `Order_Details` connexes. L'exemple accède à l'instance <xref:System.Data.Objects.ObjectContext> qui est la source de données pour l'exemple de service de données Northwind. Ce service est créé lorsque vous effectuez la [démarrage rapide WCF Data Services](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md).

### <a name="to-define-a-service-operation-in-the-northwind-data-service"></a>Pour définir une opération de service dans le service de données Northwind

1. Dans le projet de service de données Northwind, ouvrez le fichier Northwind.svc.

2. Dans la classe `Northwind`, définissez une méthode d'opération de service nommée `GetOrdersByCity` comme suit :

     [!code-csharp[Astoria Northwind Service#ServiceOperationDef](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_service/cs/northwind2.svc.cs#serviceoperationdef)]
     [!code-vb[Astoria Northwind Service#ServiceOperationDef](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_service/vb/northwind2.svc.vb#serviceoperationdef)]

3. Dans la méthode `InitializeService` de la classe `Northwind`, ajoutez le code suivant pour permettre l'accès à l'opération de service :

     [!code-csharp[Astoria Northwind Service#ServiceOperationConfig](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_service/cs/northwind2.svc.cs#serviceoperationconfig)]
     [!code-vb[Astoria Northwind Service#ServiceOperationConfig](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_service/vb/northwind2.svc.vb#serviceoperationconfig)]

### <a name="to-query-the-getordersbycity-service-operation"></a>Pour interroger l'opération de service GetOrdersByCity

- Dans un navigateur Web, entrez l'un des URI suivants pour appeler l'opération de service définie dans l'exemple suivant :

  - `http://localhost:12345/Northwind.svc/GetOrdersByCity?city='London'`

  - `http://localhost:12345/Northwind.svc/GetOrdersByCity?city='London'&$top=2`

  - `http://localhost:12345/Northwind.svc/GetOrdersByCity?city='London'&$expand=Order_Details&$orderby=RequiredDate desc`

## <a name="example"></a>Exemple

L'exemple suivant implémente une opération de service nommée `GetOrderByCity` sur le service de données Northwind. Cette opération utilise ADO.NET Entity Framework pour retourner un jeu d’objets `Orders` et `Order_Details` connexes comme une instance <xref:System.Linq.IQueryable%601> basée sur le nom de ville fourni.

> [!NOTE]
> Les opérateurs de requête sont pris en charge sur ce point de terminaison d'opération de service parce que la méthode retourne une instance <xref:System.Linq.IQueryable%601>.

[!code-csharp[Astoria Northwind Service#ServiceOperation](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_service/cs/northwind2.svc.cs#serviceoperation)]
[!code-vb[Astoria Northwind Service#ServiceOperation](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_service/vb/northwind2.svc.vb#serviceoperation)]

## <a name="see-also"></a>Voir aussi

- [Définition de WCF Data Services](../../../../docs/framework/data/wcf/defining-wcf-data-services.md)
