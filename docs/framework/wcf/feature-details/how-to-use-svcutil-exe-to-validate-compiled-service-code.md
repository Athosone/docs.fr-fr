---
title: 'Procédure : utiliser Svcutil.exe pour valider le code de service compilé'
ms.date: 03/30/2017
ms.assetid: d0d820fb-41c2-45b8-8f22-0fa5aeebbbaa
ms.openlocfilehash: 599f5624b7eb0c32cbcc0a78e6c7f989ce470b58
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62038751"
---
# <a name="how-to-use-svcutilexe-to-validate-compiled-service-code"></a><span data-ttu-id="b61d5-102">Procédure : utiliser Svcutil.exe pour valider le code de service compilé</span><span class="sxs-lookup"><span data-stu-id="b61d5-102">How to: Use Svcutil.exe to Validate Compiled Service Code</span></span>
<span data-ttu-id="b61d5-103">Vous pouvez utiliser la [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) pour détecter les erreurs dans les configurations et les implémentations de service sans héberger le service.</span><span class="sxs-lookup"><span data-stu-id="b61d5-103">You can use the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) to detect errors in service implementations and configurations without hosting the service.</span></span>  
  
### <a name="to-validate-a-service"></a><span data-ttu-id="b61d5-104">Pour valider un service</span><span class="sxs-lookup"><span data-stu-id="b61d5-104">To validate a service</span></span>  
  
1. <span data-ttu-id="b61d5-105">Compilez votre service dans un fichier exécutable et un ou plusieurs assemblys dépendants.</span><span class="sxs-lookup"><span data-stu-id="b61d5-105">Compile your service into an executable file and one or more dependent assemblies.</span></span>  
  
2. <span data-ttu-id="b61d5-106">Ouvrez une invite de commandes du Kit de développement SDK.</span><span class="sxs-lookup"><span data-stu-id="b61d5-106">Open an SDK command prompt</span></span>  
  
3. <span data-ttu-id="b61d5-107">À l'invite de commandes, lancez l'outil Svcutil.exe à l'aide du format suivant.</span><span class="sxs-lookup"><span data-stu-id="b61d5-107">At the command prompt, launch the Svcutil.exe tool using the following format.</span></span> <span data-ttu-id="b61d5-108">Pour plus d’informations sur les différents paramètres, consultez la section de validation de Service de la [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) rubrique.</span><span class="sxs-lookup"><span data-stu-id="b61d5-108">For more information on the various parameters, see the Service Validationsection of the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) topic.</span></span>  
  
    ```  
    svcutil.exe /validate /serviceName:<serviceConfigName>  <assemblyPath>*  
    ```  
  
     <span data-ttu-id="b61d5-109">Vous devez utiliser l'option `/serviceName` pour indiquer le nom de configuration du service que vous souhaitez valider.</span><span class="sxs-lookup"><span data-stu-id="b61d5-109">You must use the `/serviceName` option to indicate the configuration name of the service you want to validate.</span></span>  
  
     <span data-ttu-id="b61d5-110">L’argument `assemblyPath` spécifie le chemin d’accès au fichier exécutable du service et un ou plusieurs assemblys qui contiennent les types de services à valider.</span><span class="sxs-lookup"><span data-stu-id="b61d5-110">The `assemblyPath` argument specifies the path to the executable file for the service and one or more assemblies that contain the service types to be validated.</span></span> <span data-ttu-id="b61d5-111">L'assembly exécutable doit avoir un fichier de configuration associé pour fournir la configuration du service.</span><span class="sxs-lookup"><span data-stu-id="b61d5-111">The executable assembly must have an associated configuration file to provide the service configuration.</span></span> <span data-ttu-id="b61d5-112">Vous pouvez utiliser des caractères génériques de ligne de commande standard pour fournir plusieurs assemblys.</span><span class="sxs-lookup"><span data-stu-id="b61d5-112">You can use standard command-line wildcards to provide multiple assemblies.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b61d5-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="b61d5-113">Example</span></span>  
 <span data-ttu-id="b61d5-114">La commande suivante illustre le service myServiceName implémenté dans le fichier exécutable myServiceHost.exe.</span><span class="sxs-lookup"><span data-stu-id="b61d5-114">The following command the service myServiceName implemented in the myServiceHost.exe executable file.</span></span>  <span data-ttu-id="b61d5-115">Le fichier de configuration pour le service (myServiceHost.exe.config) est chargé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="b61d5-115">The configuration file for the service (myServiceHost.exe.config) is automatically loaded.</span></span>  
  
```  
svcutil /validate /serviceName:myServiceName myServiceHost.exe  
```  
  
## <a name="see-also"></a><span data-ttu-id="b61d5-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b61d5-116">See also</span></span>

- [<span data-ttu-id="b61d5-117">Outil ServiceModel Metadata Utility (Svcutil.exe)</span><span class="sxs-lookup"><span data-stu-id="b61d5-117">ServiceModel Metadata Utility Tool (Svcutil.exe)</span></span>](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)
