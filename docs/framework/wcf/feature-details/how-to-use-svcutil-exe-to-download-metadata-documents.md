---
title: 'Procédure : utiliser Svcutil.exe pour télécharger des documents de métadonnées'
ms.date: 03/30/2017
ms.assetid: 15524274-3167-4627-b722-d6cedb9fa8c6
ms.openlocfilehash: cc9fc4acaeafe4583b1e85a24cab97af1689c638
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61972781"
---
# <a name="how-to-use-svcutilexe-to-download-metadata-documents"></a><span data-ttu-id="a6617-102">Procédure : utiliser Svcutil.exe pour télécharger des documents de métadonnées</span><span class="sxs-lookup"><span data-stu-id="a6617-102">How to: Use Svcutil.exe to Download Metadata Documents</span></span>
<span data-ttu-id="a6617-103">Svcutil.exe vous permet de télécharger des métadonnées à partir de systèmes en cours d'exécution et de les enregistrer dans des fichiers locaux.</span><span class="sxs-lookup"><span data-stu-id="a6617-103">You can use Svcutil.exe to download metadata from running services and to save the metadata to local files.</span></span> <span data-ttu-id="a6617-104">Pour les schémas d’URL HTTP et HTTPS, Svcutil.exe tente de récupérer les métadonnées à l’aide de WS-MetadataExchange et [découverte de Service Web XML](https://go.microsoft.com/fwlink/?LinkId=94950).</span><span class="sxs-lookup"><span data-stu-id="a6617-104">For HTTP and HTTPS URL schemes, Svcutil.exe attempts to retrieve metadata using WS-MetadataExchange and [XML Web Service Discovery](https://go.microsoft.com/fwlink/?LinkId=94950).</span></span> <span data-ttu-id="a6617-105">Pour tous les autres schémas d'URL, Svcutil.exe utilise uniquement WS-MetadataExchange.</span><span class="sxs-lookup"><span data-stu-id="a6617-105">For all other URL schemes, Svcutil.exe uses only WS-MetadataExchange.</span></span>  
  
 <span data-ttu-id="a6617-106">Par défaut, Svcutil.exe utilise les liaisons définies dans la classe <xref:System.ServiceModel.Description.MetadataExchangeBindings>.</span><span class="sxs-lookup"><span data-stu-id="a6617-106">By default, Svcutil.exe uses the bindings defined in the <xref:System.ServiceModel.Description.MetadataExchangeBindings> class.</span></span> <span data-ttu-id="a6617-107">Pour configurer la liaison utilisée pour WS-MetadataExchange, vous devez définir un point de terminaison client dans le fichier de configuration de Svcutil.exe (svcutil.exe.config) qui utilise le contrat `IMetadataExchange` et qui porte le même nom que le schéma d’URI (Uniform Resource Identifier) de l’adresse du point de terminaison des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="a6617-107">To configure the binding used for WS-MetadataExchange, you must define a client endpoint in the configuration file for Svcutil.exe (svcutil.exe.config) that uses the `IMetadataExchange` contract and that has the same name as the Uniform Resource Identifier (URI) scheme of the metadata endpoint address.</span></span>  
  
> [!CAUTION]
> <span data-ttu-id="a6617-108">Lors de l’exécution de Svcutil.exe pour obtenir des métadonnées pour un service qui expose deux services différents contrats que contiennent chacune une opération du même nom, Svcutil.exe affiche un message d’erreur indiquant, « Impossible d’obtenir les métadonnées à partir de... » Par exemple, si vous avez un service qui expose un contrat de service appelé `ICarService` qui a une opération `Get(Car c)` et le même service expose un contrat de service appelé `IBookService` qui a une opération `Get(Book b)`.</span><span class="sxs-lookup"><span data-stu-id="a6617-108">When running Svcutil.exe to get metadata for a service that exposes two different service contracts that each contain an operation of the same name, Svcutil.exe displays an error saying, "Cannot obtain Metadata from ...." For example, if you have a service that exposes a service contract called `ICarService` that has an operation `Get(Car c)` and the same service exposes a service contract called `IBookService` that has an operation `Get(Book b)`.</span></span> <span data-ttu-id="a6617-109">Pour remédier à ce problème, effectuez l'une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="a6617-109">To work around this issue, do one of the following:</span></span>
>
> - <span data-ttu-id="a6617-110">Renommez l'une des opérations.</span><span class="sxs-lookup"><span data-stu-id="a6617-110">Rename one of the operations.</span></span>
> - <span data-ttu-id="a6617-111">Affectez au <xref:System.ServiceModel.OperationContractAttribute.Name%2A> un nom différent.</span><span class="sxs-lookup"><span data-stu-id="a6617-111">Set the <xref:System.ServiceModel.OperationContractAttribute.Name%2A> to a different name.</span></span>
> - <span data-ttu-id="a6617-112">Affectez à l'un des espaces de noms des opérations un espace de noms différent à l'aide de la propriété <xref:System.ServiceModel.ServiceContractAttribute.Namespace%2A>.</span><span class="sxs-lookup"><span data-stu-id="a6617-112">Set one of the operations' namespaces to a different namespace using the <xref:System.ServiceModel.ServiceContractAttribute.Namespace%2A> property.</span></span>
  
## <a name="to-download-metadata-using-svcutilexe"></a><span data-ttu-id="a6617-113">Pour télécharger les métadonnées à l'aide de Svcutil.exe</span><span class="sxs-lookup"><span data-stu-id="a6617-113">To download metadata using Svcutil.exe</span></span>  
  
1. <span data-ttu-id="a6617-114">Localisez l'outil Svcutil.exe à l'emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="a6617-114">Locate the Svcutil.exe tool at the following location:</span></span>  
  
     <span data-ttu-id="a6617-115">C:\Program Files\Microsoft SDKs\Windows\v1.0.\bin</span><span class="sxs-lookup"><span data-stu-id="a6617-115">C:\Program Files\Microsoft SDKs\Windows\v1.0.\bin</span></span>  
  
2. <span data-ttu-id="a6617-116">À l'invite de commandes, lancez l'outil en utilisant le format suivant.</span><span class="sxs-lookup"><span data-stu-id="a6617-116">At the command prompt, launch the tool using the following format.</span></span>  
  
    ```  
    svcutil.exe /t:metadata  <url>* | <epr>  
    ```  
  
     <span data-ttu-id="a6617-117">Vous devez spécifier l'option `/t:metadata` pour télécharger les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="a6617-117">You must specify the `/t:metadata` option to download metadata.</span></span> <span data-ttu-id="a6617-118">Sinon, la configuration et le code client seront générés.</span><span class="sxs-lookup"><span data-stu-id="a6617-118">Otherwise, client code and configuration are generated.</span></span>  
  
3. <span data-ttu-id="a6617-119">Le <`url`> argument spécifie l’URL à un point de terminaison de service qui fournit des métadonnées ou à un document de métadonnées hébergé en ligne.</span><span class="sxs-lookup"><span data-stu-id="a6617-119">The <`url`>argument specifies the URL to a service endpoint that provides metadata or to a metadata document hosted online.</span></span> <span data-ttu-id="a6617-120">Le <`epr`> argument spécifie le chemin d’accès dans un fichier XML qui contient un WS-Addressing `EndpointAddress` pour un point de terminaison de service qui prend en charge de WS-MetadataExchange.</span><span class="sxs-lookup"><span data-stu-id="a6617-120">The <`epr`> argument specifies the path to an XML file that contains a WS-Addressing `EndpointAddress` for a service endpoint that supports WS-MetadataExchange.</span></span>  
  
 <span data-ttu-id="a6617-121">Pour plus d’options sur l’utilisation de cet outil pour le téléchargement de métadonnées, consultez [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md).</span><span class="sxs-lookup"><span data-stu-id="a6617-121">For more options about using this tool for metadata download, see [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="a6617-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="a6617-122">Example</span></span>  
 <span data-ttu-id="a6617-123">La commande suivante télécharge des documents de métadonnées à partir d'un service en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="a6617-123">The following command downloads metadata documents from a running service.</span></span>  
  
```  
svcutil /t:metadata http://service/metadataEndpoint  
```  
  
## <a name="see-also"></a><span data-ttu-id="a6617-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6617-124">See also</span></span>

- [<span data-ttu-id="a6617-125">Outil ServiceModel Metadata Utility (Svcutil.exe)</span><span class="sxs-lookup"><span data-stu-id="a6617-125">ServiceModel Metadata Utility Tool (Svcutil.exe)</span></span>](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)
