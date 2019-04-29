---
title: <workflowControlEndpoint>
ms.date: 03/30/2017
ms.assetid: 6c89e76c-643b-4b6a-9b25-628f753d7027
ms.openlocfilehash: a9c16d1036a8177120cd152d4ac211ad084d588e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61769640"
---
# <a name="workflowcontrolendpoint"></a><span data-ttu-id="96e84-101">\<workflowControlEndpoint></span><span class="sxs-lookup"><span data-stu-id="96e84-101">\<workflowControlEndpoint></span></span>
<span data-ttu-id="96e84-102">Cet élément de configuration définit un point de terminaison standard permettant de contrôler l'exécution d'instances de flux de travail (créer, exécuter, interrompre, arrêter, etc.).</span><span class="sxs-lookup"><span data-stu-id="96e84-102">This configuration element defines a standard endpoint for controlling the execution of workflow instances (create, run, suspend, terminate, etc).</span></span>  
  
<span data-ttu-id="96e84-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="96e84-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="96e84-104">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="96e84-104">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="96e84-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96e84-105">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <workflowControlEndpoint>
      <standardEndpoint name="String" />
    </workflowControlEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="96e84-106">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="96e84-106">Attributes and Elements</span></span>  
 <span data-ttu-id="96e84-107">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="96e84-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="96e84-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="96e84-108">Attributes</span></span>  
  
|<span data-ttu-id="96e84-109">Attribut</span><span class="sxs-lookup"><span data-stu-id="96e84-109">Attribute</span></span>|<span data-ttu-id="96e84-110">Description</span><span class="sxs-lookup"><span data-stu-id="96e84-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="96e84-111">name</span><span class="sxs-lookup"><span data-stu-id="96e84-111">name</span></span>|<span data-ttu-id="96e84-112">Chaîne qui spécifie le nom de la configuration du point de terminaison standard.</span><span class="sxs-lookup"><span data-stu-id="96e84-112">A String that specifies the name of the configuration of the standard endpoint.</span></span> <span data-ttu-id="96e84-113">Le nom est utilisé dans l'attribut `endpointConfiguration` du point de terminaison de service pour lier un point de terminaison standard à sa configuration.</span><span class="sxs-lookup"><span data-stu-id="96e84-113">The name is used in the `endpointConfiguration` attribute of the service endpoint to link a standard endpoint to its configuration.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="96e84-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="96e84-114">Child Elements</span></span>  
 <span data-ttu-id="96e84-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="96e84-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="96e84-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="96e84-116">Parent Elements</span></span>  
  
|<span data-ttu-id="96e84-117">Élément</span><span class="sxs-lookup"><span data-stu-id="96e84-117">Element</span></span>|<span data-ttu-id="96e84-118">Description</span><span class="sxs-lookup"><span data-stu-id="96e84-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="96e84-119">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="96e84-119">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="96e84-120">Collection de points de terminaison standard qui sont des points de terminaison prédéfinis dont une ou plusieurs propriétés (adresse, liaison, contrat) sont fixes.</span><span class="sxs-lookup"><span data-stu-id="96e84-120">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="96e84-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96e84-121">See also</span></span>

- <xref:System.ServiceModel.Activities.WorkflowControlEndpoint>
