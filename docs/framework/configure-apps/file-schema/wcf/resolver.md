---
title: <resolver>
ms.date: 03/30/2017
ms.assetid: 0c00200c-f135-4e5c-a024-76b72bcbc021
ms.openlocfilehash: 39dcb868bd3ff25451509616e1dac7d41f94cfa1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61783121"
---
# <a name="resolver"></a><span data-ttu-id="0fa60-101">\<resolver></span><span class="sxs-lookup"><span data-stu-id="0fa60-101">\<resolver></span></span>
<span data-ttu-id="0fa60-102">Spécifie un programme de résolution d'homologue utilisé pour résoudre un ID de maille d'homologues en un jeu d'adresses de nœuds d'homologues représentant plusieurs nœuds faisant partie de la maille.</span><span class="sxs-lookup"><span data-stu-id="0fa60-102">Specifies a peer resolver that is used to resolve a peer mesh ID to a set of peer node addresses that represents several nodes that participate in the mesh.</span></span>  
  
 <span data-ttu-id="0fa60-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="0fa60-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="0fa60-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="0fa60-104">\<bindings></span></span>  
<span data-ttu-id="0fa60-105">\<netPeerBinding></span><span class="sxs-lookup"><span data-stu-id="0fa60-105">\<netPeerBinding></span></span>  
<span data-ttu-id="0fa60-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="0fa60-106">\<binding></span></span>  
<span data-ttu-id="0fa60-107">\<resolver></span><span class="sxs-lookup"><span data-stu-id="0fa60-107">\<resolver></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0fa60-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0fa60-108">Syntax</span></span>  
  
```xml  
<resolver mode="Auto/Custom/Pnrp"
          referralPolicy="DoNotShare/Service/Share">
</resolver>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0fa60-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="0fa60-109">Attributes and Elements</span></span>  
 <span data-ttu-id="0fa60-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="0fa60-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0fa60-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="0fa60-111">Attributes</span></span>  
  
|<span data-ttu-id="0fa60-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="0fa60-112">Attribute</span></span>|<span data-ttu-id="0fa60-113">Description</span><span class="sxs-lookup"><span data-stu-id="0fa60-113">Description</span></span>|  
|---------------|-----------------|  
|`mode`|<span data-ttu-id="0fa60-114">Chaîne qui spécifie si l'instance du programme de résolution d'homologue associée à ce service est spécifique au PNRP, à un programme de résolution personnalisé ou si elle est déterminée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="0fa60-114">A string that specifies whether the peer resolver instance associated with this service is either PNRP-specific, a custom resolver, or automatically determined.</span></span> <span data-ttu-id="0fa60-115">Cet attribut est de type <xref:System.ServiceModel.PeerResolvers.PeerResolverMode>.</span><span class="sxs-lookup"><span data-stu-id="0fa60-115">This attribute is of type <xref:System.ServiceModel.PeerResolvers.PeerResolverMode>.</span></span>|  
|`referralPolicy`|<span data-ttu-id="0fa60-116">Chaîne qui spécifie la manière dont les références sont partagées parmi des homologues.</span><span class="sxs-lookup"><span data-stu-id="0fa60-116">A string that specifies the way referrals are shared among peers.</span></span> <span data-ttu-id="0fa60-117">Cet attribut est de type <xref:System.ServiceModel.PeerResolvers.PeerReferralPolicy>.</span><span class="sxs-lookup"><span data-stu-id="0fa60-117">This attribute is of type <xref:System.ServiceModel.PeerResolvers.PeerReferralPolicy>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0fa60-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0fa60-118">Child Elements</span></span>  
  
|<span data-ttu-id="0fa60-119">Élément</span><span class="sxs-lookup"><span data-stu-id="0fa60-119">Element</span></span>|<span data-ttu-id="0fa60-120">Description</span><span class="sxs-lookup"><span data-stu-id="0fa60-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0fa60-121">\<headers></span><span class="sxs-lookup"><span data-stu-id="0fa60-121">\<headers></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers.md)|<span data-ttu-id="0fa60-122">Spécifie les paramètres pour un service de programme de résolution d'homologue personnalisé.</span><span class="sxs-lookup"><span data-stu-id="0fa60-122">Specifies settings for a custom peer resolver service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="0fa60-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0fa60-123">Parent Elements</span></span>  
  
|<span data-ttu-id="0fa60-124">Élément</span><span class="sxs-lookup"><span data-stu-id="0fa60-124">Element</span></span>|<span data-ttu-id="0fa60-125">Description</span><span class="sxs-lookup"><span data-stu-id="0fa60-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0fa60-126">\<binding></span><span class="sxs-lookup"><span data-stu-id="0fa60-126">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="0fa60-127">Définit toutes les fonctions de liaison de la [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="0fa60-127">Defines all binding capabilities of the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0fa60-128">Notes</span><span class="sxs-lookup"><span data-stu-id="0fa60-128">Remarks</span></span>  
 <span data-ttu-id="0fa60-129">Un programme de résolution de nom d'homologue est un service de découverte utilisé par les canaux homologues afin de rechercher des nœuds d'homologues faisant partie d'une maille d'homologues.</span><span class="sxs-lookup"><span data-stu-id="0fa60-129">A peer name resolver is a discovery service used by peer channels to find peer nodes that participate in a peer mesh.</span></span> <span data-ttu-id="0fa60-130">Il est également utilisé pour « inscrire » un nœud avec un maillage d'homologue, le mécanisme par lequel le nœud homologue est connu et disponible à partir du maillage d'homologue.</span><span class="sxs-lookup"><span data-stu-id="0fa60-130">It is also used to "register" a node with a peer mesh, the mechanism by which the peer node becomes known and available from the peer mesh.</span></span> <span data-ttu-id="0fa60-131">Pour plus d’informations sur les programmes de résolution homologues, consultez [programmes de résolution homologues](../../../../../docs/framework/wcf/feature-details/peer-resolvers.md).</span><span class="sxs-lookup"><span data-stu-id="0fa60-131">For more information on peer resolvers, see [Peer Resolvers](../../../../../docs/framework/wcf/feature-details/peer-resolvers.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0fa60-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fa60-132">See also</span></span>

- <xref:System.ServiceModel.PeerResolver>
- <xref:System.ServiceModel.PeerResolvers.PeerResolverSettings>
- <xref:System.ServiceModel.NetPeerTcpBinding.Resolver%2A>
- <xref:System.ServiceModel.Configuration.NetPeerTcpBindingElement.Resolver%2A>
- <xref:System.ServiceModel.Configuration.PeerResolverElement>
- [<span data-ttu-id="0fa60-133">Programmes de résolution d’homologue</span><span class="sxs-lookup"><span data-stu-id="0fa60-133">Peer Resolvers</span></span>](../../../../../docs/framework/wcf/feature-details/peer-resolvers.md)
- <span data-ttu-id="0fa60-134">[Ajout d’un programme de résolution personnalisé à une Application PeerChannel](https://docs.microsoft.com/previous-versions/ms730105(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="0fa60-134">[Adding a Custom Resolver to a PeerChannel Application](https://docs.microsoft.com/previous-versions/ms730105(v=vs.90))</span></span>
