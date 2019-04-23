---
title: <cancelRequestedQueries>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: eab5af7e-76fa-434d-9d36-873e995cee05
ms.openlocfilehash: 32a37fb3cc2b93046bea133f351185638b0d7545
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59163161"
---
# <a name="cancelrequestedqueries"></a><span data-ttu-id="b71c6-101">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="b71c6-101">\<cancelRequestedQueries></span></span>
<span data-ttu-id="b71c6-102">Représente une collection de requêtes qui permettent d’effectuer le suivi des demandes d’annulation d’une activité enfant par l’activité parent.</span><span class="sxs-lookup"><span data-stu-id="b71c6-102">Represents a collection of queries that are used to track requests to cancel a child activity by the parent activity.</span></span> <span data-ttu-id="b71c6-103">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement de demande d'annulation.</span><span class="sxs-lookup"><span data-stu-id="b71c6-103">The query is necessary for a tracking participant to subscribe to cancel request record objects.</span></span>  
  
 <span data-ttu-id="b71c6-104">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="b71c6-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="b71c6-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="b71c6-105">\<system.serviceModel></span></span>  
<span data-ttu-id="b71c6-106">\<tracking></span><span class="sxs-lookup"><span data-stu-id="b71c6-106">\<tracking></span></span>  
<span data-ttu-id="b71c6-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="b71c6-107">\<trackingProfile></span></span>  
<span data-ttu-id="b71c6-108">\<workflow></span><span class="sxs-lookup"><span data-stu-id="b71c6-108">\<workflow></span></span>  
<span data-ttu-id="b71c6-109">\<cancelRequestedQueries></span><span class="sxs-lookup"><span data-stu-id="b71c6-109">\<cancelRequestedQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b71c6-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b71c6-110">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <cancelRequestQueries>
        <cancelRequestQuery activityName="String" 
                            childActivityName="String"/>
      </cancelRequestQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b71c6-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="b71c6-111">Attributes and Elements</span></span>  
 <span data-ttu-id="b71c6-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="b71c6-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b71c6-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="b71c6-113">Attributes</span></span>  
 <span data-ttu-id="b71c6-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b71c6-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="b71c6-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b71c6-115">Child Elements</span></span>  
  
|<span data-ttu-id="b71c6-116">Élément</span><span class="sxs-lookup"><span data-stu-id="b71c6-116">Element</span></span>|<span data-ttu-id="b71c6-117">Description</span><span class="sxs-lookup"><span data-stu-id="b71c6-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b71c6-118">\<cancelRequestedQuery></span><span class="sxs-lookup"><span data-stu-id="b71c6-118">\<cancelRequestedQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/cancelrequestedquery.md)|<span data-ttu-id="b71c6-119">Requête qui permet d'effectuer le suivi des demande d'annulation d'une activité enfant par l'activité parent.</span><span class="sxs-lookup"><span data-stu-id="b71c6-119">A query that is used to track requests to cancel a child activity by the parent activity</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="b71c6-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b71c6-120">Parent Elements</span></span>  
  
|<span data-ttu-id="b71c6-121">Élément</span><span class="sxs-lookup"><span data-stu-id="b71c6-121">Element</span></span>|<span data-ttu-id="b71c6-122">Description</span><span class="sxs-lookup"><span data-stu-id="b71c6-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b71c6-123">\<workflow></span><span class="sxs-lookup"><span data-stu-id="b71c6-123">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="b71c6-124">Un élément de configuration qui contient toutes les requêtes pour un flux de travail spécifique identifié par le **activityDefinitionId** propriété.</span><span class="sxs-lookup"><span data-stu-id="b71c6-124">A configuration element that contains all queries for a specific workflow identified by the **activityDefinitionId** property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b71c6-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b71c6-125">See also</span></span>

- [<span data-ttu-id="b71c6-126">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="b71c6-126">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="b71c6-127">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="b71c6-127">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
