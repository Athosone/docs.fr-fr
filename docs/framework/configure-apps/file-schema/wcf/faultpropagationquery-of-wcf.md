---
title: <faultPropagationQuery> de WCF
ms.date: 03/30/2017
ms.assetid: fabafbc8-3e45-4feb-8321-0725e9f4079c
ms.openlocfilehash: e5793852d49a052d05f6cb2f4efbe166d67afc62
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61701045"
---
# <a name="faultpropagationquery-of-wcf"></a><span data-ttu-id="c70a6-102">\<faultPropagationQuery> of WCF</span><span class="sxs-lookup"><span data-stu-id="c70a6-102">\<faultPropagationQuery> of WCF</span></span>

<span data-ttu-id="c70a6-103">Représente une requête qui permet d'effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="c70a6-103">Represents a query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="c70a6-104">Cet événement se produit chaque fois qu'un FaultHandler traite une erreur.</span><span class="sxs-lookup"><span data-stu-id="c70a6-104">This event occurs each time a FaultHandler processes a fault.</span></span> <span data-ttu-id="c70a6-105">Vous devez utiliser cette requête pour effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="c70a6-105">You should use such query to track the handling of faults that occur within an activity.</span></span> <span data-ttu-id="c70a6-106">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner aux enregistrements de propagation d'erreur.</span><span class="sxs-lookup"><span data-stu-id="c70a6-106">The query is necessary for a  tracking participant to subscribe to fault propagation records.</span></span>

<span data-ttu-id="c70a6-107">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="c70a6-107">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>

<span data-ttu-id="c70a6-108">\<system.serviceModel>\\</span><span class="sxs-lookup"><span data-stu-id="c70a6-108">\<system.serviceModel>\\</span></span>
<span data-ttu-id="c70a6-109">\<suivi > \\</span><span class="sxs-lookup"><span data-stu-id="c70a6-109">\<tracking>\\</span></span>
<span data-ttu-id="c70a6-110">\<profiles>\\</span><span class="sxs-lookup"><span data-stu-id="c70a6-110">\<profiles>\\</span></span>
<span data-ttu-id="c70a6-111">\<trackingProfile>\\</span><span class="sxs-lookup"><span data-stu-id="c70a6-111">\<trackingProfile>\\</span></span>
<span data-ttu-id="c70a6-112">\<workflow>\\</span><span class="sxs-lookup"><span data-stu-id="c70a6-112">\<workflow>\\</span></span>
<span data-ttu-id="c70a6-113">\<faultPropagationQueries>\\</span><span class="sxs-lookup"><span data-stu-id="c70a6-113">\<faultPropagationQueries>\\</span></span>
<span data-ttu-id="c70a6-114">\<faultPropagationQuery></span><span class="sxs-lookup"><span data-stu-id="c70a6-114">\<faultPropagationQuery></span></span>

## <a name="syntax"></a><span data-ttu-id="c70a6-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c70a6-115">Syntax</span></span>

```xml
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <faultPropagationQueries>
          <faultPropagationQuery faultSourceActivityName="String"
                                 faultHandlerActivityName="String" />
        </faultPropagationQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="c70a6-116">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="c70a6-116">Attributes and elements</span></span>

<span data-ttu-id="c70a6-117">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="c70a6-117">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="c70a6-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="c70a6-118">Attributes</span></span>

|<span data-ttu-id="c70a6-119">Attribut</span><span class="sxs-lookup"><span data-stu-id="c70a6-119">Attribute</span></span>|<span data-ttu-id="c70a6-120">Description</span><span class="sxs-lookup"><span data-stu-id="c70a6-120">Description</span></span>|
|---------------|-----------------|
|`faultSourceActivityName`|<span data-ttu-id="c70a6-121">Chaîne qui spécifie le nom de l’activité de gestionnaire d’erreur qui a propagé l’erreur.</span><span class="sxs-lookup"><span data-stu-id="c70a6-121">A string that specifies the name of the fault handler activity that propagated the fault.</span></span> <span data-ttu-id="c70a6-122">La valeur par défaut est \*, ce qui indique que les enregistrements de propagation d’erreur sont retournés pour toutes les activités.</span><span class="sxs-lookup"><span data-stu-id="c70a6-122">The default is \*, which indicates that fault propagation records are returned for all activities.</span></span>|
|`faultHandlerActivityName`|<span data-ttu-id="c70a6-123">Chaîne qui spécifie le nom de l'activité à l'origine de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="c70a6-123">A string that specifies the name of the activity that was the source of the fault.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="c70a6-124">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c70a6-124">Child elements</span></span>

<span data-ttu-id="c70a6-125">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c70a6-125">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="c70a6-126">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c70a6-126">Parent elements</span></span>

|<span data-ttu-id="c70a6-127">Élément</span><span class="sxs-lookup"><span data-stu-id="c70a6-127">Element</span></span>|<span data-ttu-id="c70a6-128">Description</span><span class="sxs-lookup"><span data-stu-id="c70a6-128">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="c70a6-129">\<faultPropagationQueries></span><span class="sxs-lookup"><span data-stu-id="c70a6-129">\<faultPropagationQueries></span></span>](faultpropagationqueries-of-wcf.md)|<span data-ttu-id="c70a6-130">Représente une liste des éléments de configuration qui permettent d'effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="c70a6-130">Represents a list of configuration elements that are used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="c70a6-131">Cet événement se produit chaque fois qu'un FaultHandler traite une erreur.</span><span class="sxs-lookup"><span data-stu-id="c70a6-131">This event occurs each time a FaultHandler processes a fault.</span></span>|

## <a name="see-also"></a><span data-ttu-id="c70a6-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c70a6-132">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.FaultPropagationQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.FaultPropagationQuery?displayProperty=nameWithType>
- [<span data-ttu-id="c70a6-133">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="c70a6-133">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="c70a6-134">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="c70a6-134">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
