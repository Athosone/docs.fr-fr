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
# <a name="how-to-use-metadataresolver-to-obtain-binding-metadata-dynamically"></a>Procédure : utiliser MetadataResolver pour obtenir des métadonnées de liaison de manière dynamique
Cette rubrique indique comment utiliser la classe <xref:System.ServiceModel.Description.MetadataResolver> pour obtenir des métadonnées de liaison dynamiquement.  
  
### <a name="to-dynamically-obtain-binding-metadata"></a>Pour obtenir des métadonnées de liaison dynamiquement  
  
1. Créez un objet <xref:System.ServiceModel.EndpointAddress> avec l'adresse du point de terminaison de métadonnées.  
  
    ```  
    EndpointAddress metaAddress  
      = new EndpointAddress(new   Uri("http://localhost:8080/SampleService/mex"));  
    ```  
  
2. Appelez <xref:System.ServiceModel.Description.MetadataResolver.Resolve%28System.Type%2CSystem.ServiceModel.EndpointAddress%29>, qui passe le type de service et l'adresse du point de terminaison de métadonnées. Une collection de points de terminaison qui implémentent le contrat spécifié est alors retournée. Seules les informations de liaison sont importées à partir des métadonnées, les informations de contrat ne le sont pas. Le contrat fourni est utilisé à la place.  
  
    ```  
    ServiceEndpointCollection endpoints = MetadataResolver.Resolve(typeof(SampleServiceClient),metaAddress);  
    ```  
  
3. Vous pouvez ensuite itérer au sein de la collection de points de terminaison de service afin d'extraire les informations de liaison dont vous avez besoin. Le code suivant itère au sein des points de terminaison, crée un objet client de service qui passe la liaison et l’adresse associée au point de terminaison actuel, puis appelle une méthode sur le service.  
  
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
  
## <a name="see-also"></a>Voir aussi

- [Métadonnées](../../../../docs/framework/wcf/feature-details/metadata.md)
