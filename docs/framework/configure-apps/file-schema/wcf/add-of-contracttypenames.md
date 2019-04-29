---
title: <add> de <contractTypeNames>
ms.date: 03/30/2017
ms.assetid: 03aff6be-5dfb-4a64-ada3-e36227cd43c7
ms.openlocfilehash: 856298cb0639cf19b941f326b5b9a25aa6663088
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61701188"
---
# <a name="add-of-contracttypenames"></a><span data-ttu-id="76957-102">\<add> of \<contractTypeNames></span><span class="sxs-lookup"><span data-stu-id="76957-102">\<add> of \<contractTypeNames></span></span>
<span data-ttu-id="76957-103">Élément de configuration qui spécifie le nom de contrat des services recherchés et les critères généralement utilisés lors de la recherche d'un service.</span><span class="sxs-lookup"><span data-stu-id="76957-103">A configuration element that specifies the contract name of the services being searched for, and the criteria typically used when searching for a service.</span></span> <span data-ttu-id="76957-104">Si plusieurs noms de contrat sont spécifiés, seuls les points de terminaison de service correspondant à TOUS les contrats répondent.</span><span class="sxs-lookup"><span data-stu-id="76957-104">If more than one contract name is specified, only service endpoints matching ALL contracts will reply.</span></span> <span data-ttu-id="76957-105">Notez que dans Windows Communication Foundation (WCF), un point de terminaison peut uniquement prendre en charge un seul contrat.</span><span class="sxs-lookup"><span data-stu-id="76957-105">Note that in Windows Communication Foundation (WCF), an endpoint can only support one contract.</span></span>  
  
 <span data-ttu-id="76957-106">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="76957-106">\<system.ServiceModel></span></span>  
<span data-ttu-id="76957-107">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="76957-107">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="76957-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76957-108">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <dynamicEndpoint>
      <standardEndpoint>
        <discoveryClientSettings discoveryEndpoint="String">
          <findCriteria duration="TimeSpan"
                        maxResults="Integer"
                        scopeMatchBy="Uri">
            <contractTypeNames>
              <add name="String" namespace="String" />
            <contractTypeNames>
            <extensions />
            <scopes>
              <add scope="URI"/>
            </scopes>
          </findCriteria>
        </discoveryClientSettings>
      <standardEndpoint>
    </dynamicEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="76957-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="76957-109">Attributes and Elements</span></span>  
 <span data-ttu-id="76957-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="76957-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="76957-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="76957-111">Attributes</span></span>  
  
|<span data-ttu-id="76957-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="76957-112">Attribute</span></span>|<span data-ttu-id="76957-113">Description</span><span class="sxs-lookup"><span data-stu-id="76957-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="76957-114">name</span><span class="sxs-lookup"><span data-stu-id="76957-114">name</span></span>|<span data-ttu-id="76957-115">Chaîne qui spécifie le nom du type de contrat.</span><span class="sxs-lookup"><span data-stu-id="76957-115">A string that specifies the name of the contract type.</span></span>|  
|<span data-ttu-id="76957-116">namespace</span><span class="sxs-lookup"><span data-stu-id="76957-116">namespace</span></span>|<span data-ttu-id="76957-117">Chaîne qui spécifie l'espace de noms du type de contrat.</span><span class="sxs-lookup"><span data-stu-id="76957-117">A string that specifies the namespace of the contract type.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="76957-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="76957-118">Child Elements</span></span>  
 <span data-ttu-id="76957-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="76957-119">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="76957-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="76957-120">Parent Elements</span></span>  
  
|<span data-ttu-id="76957-121">Élément</span><span class="sxs-lookup"><span data-stu-id="76957-121">Element</span></span>|<span data-ttu-id="76957-122">Description</span><span class="sxs-lookup"><span data-stu-id="76957-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="76957-123">\<contractTypeNames></span><span class="sxs-lookup"><span data-stu-id="76957-123">\<contractTypeNames></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/contracttypenames.md)|<span data-ttu-id="76957-124">Collection de noms de type de contrat.</span><span class="sxs-lookup"><span data-stu-id="76957-124">A collection of contract type names.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="76957-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76957-125">See also</span></span>

- <xref:System.ServiceModel.Discovery.FindCriteria>
- <xref:System.ServiceModel.Discovery.Configuration.FindCriteriaElement>
- <xref:System.ServiceModel.Discovery.Configuration.ContractTypeNameElement>
