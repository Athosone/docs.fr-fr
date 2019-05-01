---
title: 'Procédure : utiliser MetadataResolver pour obtenir des métadonnées de liaison de manière dynamique'
ms.date: 03/30/2017
ms.assetid: 56ffcb99-fff0-4479-aca0-e3909009f605
ms.openlocfilehash: 3fe09699304de42ed00312f50f3b9e0edb20615d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62047553"
---
# <a name="how-to-use-metadataresolver-to-obtain-binding-metadata-dynamically"></a><span data-ttu-id="df72f-102">Procédure : utiliser MetadataResolver pour obtenir des métadonnées de liaison de manière dynamique</span><span class="sxs-lookup"><span data-stu-id="df72f-102">How to: Use MetadataResolver to Obtain Binding Metadata Dynamically</span></span>
<span data-ttu-id="df72f-103">Cette rubrique indique comment utiliser la classe <xref:System.ServiceModel.Description.MetadataResolver> pour obtenir des métadonnées de liaison dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="df72f-103">This topic shows you how to use the <xref:System.ServiceModel.Description.MetadataResolver> class to dynamically obtain binding metadata.</span></span>  
  
### <a name="to-dynamically-obtain-binding-metadata"></a><span data-ttu-id="df72f-104">Pour obtenir des métadonnées de liaison dynamiquement</span><span class="sxs-lookup"><span data-stu-id="df72f-104">To dynamically obtain binding metadata</span></span>  
  
1. <span data-ttu-id="df72f-105">Créez un objet <xref:System.ServiceModel.EndpointAddress> avec l'adresse du point de terminaison de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="df72f-105">Create an <xref:System.ServiceModel.EndpointAddress> object with the address of the metadata endpoint.</span></span>  
  
    ```  
    EndpointAddress metaAddress  
      = new EndpointAddress(new   Uri("http://localhost:8080/SampleService/mex"));  
    ```  
  
2. <span data-ttu-id="df72f-106">Appelez <xref:System.ServiceModel.Description.MetadataResolver.Resolve%28System.Type%2CSystem.ServiceModel.EndpointAddress%29>, qui passe le type de service et l'adresse du point de terminaison de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="df72f-106">Call <xref:System.ServiceModel.Description.MetadataResolver.Resolve%28System.Type%2CSystem.ServiceModel.EndpointAddress%29>, which passes in the service type and the metadata endpoint address.</span></span> <span data-ttu-id="df72f-107">Une collection de points de terminaison qui implémentent le contrat spécifié est alors retournée.</span><span class="sxs-lookup"><span data-stu-id="df72f-107">This returns a collection of endpoints that implement the specified contract.</span></span> <span data-ttu-id="df72f-108">Seules les informations de liaison sont importées à partir des métadonnées, les informations de contrat ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="df72f-108">Only binding information is imported from the metadata; contract information is not imported.</span></span> <span data-ttu-id="df72f-109">Le contrat fourni est utilisé à la place.</span><span class="sxs-lookup"><span data-stu-id="df72f-109">The supplied contract is used instead.</span></span>  
  
    ```  
    ServiceEndpointCollection endpoints = MetadataResolver.Resolve(typeof(SampleServiceClient),metaAddress);  
    ```  
  
3. <span data-ttu-id="df72f-110">Vous pouvez ensuite itérer au sein de la collection de points de terminaison de service afin d'extraire les informations de liaison dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="df72f-110">You can then iterate through the collection of service endpoints to extract the binding information you need.</span></span> <span data-ttu-id="df72f-111">Le code suivant itère au sein des points de terminaison, crée un objet client de service qui passe la liaison et l’adresse associée au point de terminaison actuel, puis appelle une méthode sur le service.</span><span class="sxs-lookup"><span data-stu-id="df72f-111">The following code iterates through the endpoints, creates a service client object that passes in the binding and address associated with the current endpoint, and then calls a method on the service.</span></span>  
  
    ```  
    foreach (ServiceEndpoint point in endpoints)  
    {  
       if (point != null)  
       {  
          // Create a new wcfClient using retrieved endpoints.  
          using (wcfClient = new SampleServiceClient(point.Binding, point.Address))  
          {  
             Console.WriteLine(  
               wcfClient.SampleMethod("Client used the "  
               + point.Address.ToString() + " address."));  
          }  
      }  
    }  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="df72f-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df72f-112">See also</span></span>

- [<span data-ttu-id="df72f-113">Métadonnées</span><span class="sxs-lookup"><span data-stu-id="df72f-113">Metadata</span></span>](../../../../docs/framework/wcf/feature-details/metadata.md)
