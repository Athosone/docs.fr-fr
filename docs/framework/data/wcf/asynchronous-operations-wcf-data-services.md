---
title: Opérations asynchrones (services de données WCF)
ms.date: 03/30/2017
helpviewer_keywords:
- WCF Data Services, asynchronous operations
- asynchronous operations [WCF Data Services]
- WCF Data Services, client library
ms.assetid: 679644c7-e3fc-422c-b14a-b44b683900d0
ms.openlocfilehash: ef41b458a3f5b977eaaff523413c1a8d3b1982a3
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59126636"
---
# <a name="asynchronous-operations-wcf-data-services"></a>Opérations asynchrones (services de données WCF)
Les applications Web doivent gérer une latence plus élevée entre le client et le serveur, comparé aux applications qui s'exécutent sur des réseaux internes. Pour optimiser la performance et l'expérience utilisateur de votre application, nous recommandons d'utiliser les méthodes asynchrones des classes <xref:System.Data.Services.Client.DataServiceContext> et <xref:System.Data.Services.Client.DataServiceQuery%601> lors de l'accès aux serveurs [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] sur le Web.  
  
 Bien que les serveurs [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] traitent les requêtes HTTP de façon asynchrone, certaines méthodes des bibliothèques clientes [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] sont synchrones et attendent la fin de l'échange demande-réponse avant de poursuivre l'exécution. Les méthodes asynchrones des bibliothèques clientes [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] n'attendent pas la fin de cet échange et permettent que votre application maintienne une interface utilisateur réactive en même temps.  
  
 Vous pouvez effectuer des opérations asynchrones à l’aide d’une paire de méthodes sur le <xref:System.Data.Services.Client.DataServiceContext> et <xref:System.Data.Services.Client.DataServiceQuery%601> classes qui commencent par *commencer* et *fin* respectivement. Le *commencer* méthodes inscrivent un délégué appelé par le service lors de l’opération est terminée. Le *fin* méthodes doivent être appelées dans le délégué qui est inscrit pour gérer le rappel des opérations terminées. Lorsque vous appelez le *fin* méthode se termine une opération asynchrone, vous devez le faire à partir de la même <xref:System.Data.Services.Client.DataServiceQuery%601> ou <xref:System.Data.Services.Client.DataServiceContext> instance que vous avez utilisé pour démarrer l’opération. Chaque *commencer* méthode prend un `state` paramètre qui peut passer un objet d’état au rappel. Cet objet d’état est récupéré à partir de la <xref:System.IAsyncResult> qui est fourni avec le rappel et est utilisée pour appeler le correspondantes *fin* méthode pour terminer l’opération asynchrone. Par exemple, lorsque vous fournissez l'instance <xref:System.Data.Services.Client.DataServiceQuery%601> comme paramètre `state` lorsque vous appelez la méthode <xref:System.Data.Services.Client.DataServiceQuery%601.BeginExecute%2A> sur l'instance, la même instance <xref:System.Data.Services.Client.DataServiceQuery%601> est retournée par <xref:System.IAsyncResult>. Puis cette instance de <xref:System.Data.Services.Client.DataServiceQuery%601> est utilisée pour appeler la méthode <xref:System.Data.Services.Client.DataServiceQuery%601.EndExecute%2A> pour terminer l'opération de requête. Pour plus d'informations, voir [Procédure : Exécuter des requêtes de Service de données asynchrones](../../../../docs/framework/data/wcf/how-to-execute-asynchronous-data-service-queries-wcf-data-services.md).  
  
> [!NOTE]
>  Seules les opérations asynchrones sont prises en charge par les bibliothèques clientes fournies dans le .NET Framework pour Silverlight. Pour plus d’informations, consultez [WCF Data Services (Silverlight)](https://go.microsoft.com/fwlink/?LinkID=143149).  
  
 Les bibliothèques clientes .NET Framework prennent en charge les opérations asynchrones suivantes :  
  
|Opération|Méthodes|  
|---------------|-------------|  
|Exécution d'un <xref:System.Data.Services.Client.DataServiceQuery%601>.|-   <xref:System.Data.Services.Client.DataServiceQuery%601.BeginExecute%2A><br />-   <xref:System.Data.Services.Client.DataServiceQuery%601.EndExecute%2A>|  
|Exécution d'une requête du <xref:System.Data.Services.Client.DataServiceContext>.|-   <xref:System.Data.Services.Client.DataServiceContext.BeginExecute%2A><br />-   <xref:System.Data.Services.Client.DataServiceContext.EndExecute%2A>|  
|Exécution d'une requête par lot du <xref:System.Data.Services.Client.DataServiceContext>.|-   <xref:System.Data.Services.Client.DataServiceContext.BeginExecuteBatch%2A><br />-   <xref:System.Data.Services.Client.DataServiceContext.EndExecuteBatch%2A>|  
|Chargement d'une entité connexe dans <xref:System.Data.Services.Client.DataServiceContext>.|-   <xref:System.Data.Services.Client.DataServiceContext.BeginLoadProperty%2A><br />-   <xref:System.Data.Services.Client.DataServiceContext.EndLoadProperty%2A>|  
|Enregistrement des modifications apportées aux objets dans <xref:System.Data.Services.Client.DataServiceContext>|-   <xref:System.Data.Services.Client.DataServiceContext.BeginSaveChanges%2A><br />-   <xref:System.Data.Services.Client.DataServiceContext.EndSaveChanges%2A>|  
  
## <a name="threading-considerations-for-asynchronous-operations"></a>Considérations sur le threading relatives aux opérations asynchrones  
 Dans une application multithread, le délégué est inscrit comme un rappel pour l’opération asynchrone n'est pas nécessairement appelé sur le même thread qui a été utilisé pour appeler le *commencer* (méthode), qui crée la demande initiale. Dans une application où le rappel doit être appelé sur un thread spécifique, vous devez marshaler explicitement l’exécution de la *fin* (méthode), qui gère la réponse, au thread souhaité. Par exemple, dans les applications WPF (Windows Presentation Foundation) et Silverlight, la réponse doit être remarshalée au thread de l’interface utilisateur en utilisant la méthode <xref:System.Windows.Threading.Dispatcher.BeginInvoke%2A> sur l’objet <xref:System.Windows.Threading.Dispatcher>. Pour plus d’informations, consultez [interrogation du Service de données (WCF Data Services/Silverlight)](https://docs.microsoft.com/previous-versions/windows/silverlight/dotnet-windows-silverlight/cc903932(v=vs.95)).  
  
## <a name="see-also"></a>Voir aussi

- [Bibliothèque cliente WCF Data Services](../../../../docs/framework/data/wcf/wcf-data-services-client-library.md)
