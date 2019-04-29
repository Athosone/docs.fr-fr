---
title: <trackingProfile>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 154830ff-ddd3-4397-a3b5-5b334907777f
ms.openlocfilehash: 747660df58604dd9384abefccb51ea665f97e2e3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61614971"
---
# <a name="trackingprofile"></a><span data-ttu-id="6e464-101">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="6e464-101">\<trackingProfile></span></span>
<span data-ttu-id="6e464-102">Représente une section de configuration pour la création d’un abonnement pour le suivi des enregistrements dans un participant de suivi de workflow.</span><span class="sxs-lookup"><span data-stu-id="6e464-102">Represents a configuration section for creating a subscription to workflow tracking records in a tracking participant.</span></span> <span data-ttu-id="6e464-103">Un modèle de suivi contient des requêtes de suivi qui permettent à un participant au suivi de s'abonner à des événements de flux de travail émis lorsque l'état d'une instance de flux de travail change au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="6e464-103">A tracking profile contains tracking queries that permit a tracking participant to subscribe to workflow events that are emitted when the state of a workflow instance changes at runtime.</span></span> <span data-ttu-id="6e464-104">Les requêtes définies dans la section de modèle de suivi déterminent les types d'événements retournés par l'abonnement.</span><span class="sxs-lookup"><span data-stu-id="6e464-104">The queries defined within the tracking profile section define the kinds of events that are returned by the subscription.</span></span>  
  
 <span data-ttu-id="6e464-105">Pour plus d’informations de suivi de workflow et sa configuration, consultez [suivi et traçage de Workflow](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md) et [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="6e464-105">For more information in workflow tracking and its configuration, see [Workflow Tracking and Tracing](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md) and [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="6e464-106">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="6e464-106">\<system.serviceModel></span></span>  
<span data-ttu-id="6e464-107">\<tracking></span><span class="sxs-lookup"><span data-stu-id="6e464-107">\<tracking></span></span>  
<span data-ttu-id="6e464-108">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="6e464-108">\<trackingProfile></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6e464-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e464-109">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <tracking>
    <profiles>
      <participants>
        <add name="String" 
             profileName="String" 
             type="String" />
      </participants>
      <trackingProfile name="String">
        <workflow activityDefinitionId="String">
          <activityScheduledQueries>
            <activityScheduledQuery activityName="String" 
                                    childActivityName="String"/>
          </activityScheduledQueries>
          <activityStateQueries>
            <activityStateQuery activityName="String" />
            <arguments>
              <argument name="String" />
            </arguments>
            <states>
              <state name="String"  />
            </states>
            <variables>
              <variable name="String" />
            </variables>
          </activityStateQueries>
          <bookmarkResumptionQueries>
            <bookmarkResumptionQuery name="String" />
          </bookmarkResumptionQueries>
          <cancelRequestQueries>
            <cancelRequestQuery activityName="String" 
                                childActivityName="String"/>
          </cancelRequestQueries>
          <customTrackingQueries>
            <customTrackingQuery activityName="String" 
                                 name="String"/>
          </customTrackingQueries>
          <faultPropagationQueries>
            <faultPropagationQuery activityName="String" 
                                   faultHandlerActivityName="String" />
          </faultPropagationQueries>
          <workflowInstanceQueries>
            <workflowInstanceQuery>
              <states>
                <state name="String" />
              </states>
            </workflowInstanceQuery>
          </workflowInstanceQueries>
        </workflow>
      </trackingProfile>
    </profiles>
  </tracking>
</system.serviceModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6e464-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="6e464-110">Attributes and Elements</span></span>  
 <span data-ttu-id="6e464-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="6e464-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6e464-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="6e464-112">Attributes</span></span>  
  
|<span data-ttu-id="6e464-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="6e464-113">Attribute</span></span>|<span data-ttu-id="6e464-114">Description</span><span class="sxs-lookup"><span data-stu-id="6e464-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="6e464-115">name</span><span class="sxs-lookup"><span data-stu-id="6e464-115">name</span></span>|<span data-ttu-id="6e464-116">Chaîne qui spécifie le nom du modèle de suivi.</span><span class="sxs-lookup"><span data-stu-id="6e464-116">A string that specifies the name of the tracking profile.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6e464-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6e464-117">Child Elements</span></span>  
  
|<span data-ttu-id="6e464-118">Élément</span><span class="sxs-lookup"><span data-stu-id="6e464-118">Element</span></span>|<span data-ttu-id="6e464-119">Description</span><span class="sxs-lookup"><span data-stu-id="6e464-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6e464-120">\<participants></span><span class="sxs-lookup"><span data-stu-id="6e464-120">\<participants></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/participants.md)|<span data-ttu-id="6e464-121">Élément de configuration qui contient toutes les requêtes d'un flux de travail spécifique identifié par la propriété <xref:System.ServiceModel.Activities.Tracking.Configuration.ProfileWorkflowElement.ActivityDefinitionId%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="6e464-121">A configuration element that contains all queries for a specific workflow identified by the <xref:System.ServiceModel.Activities.Tracking.Configuration.ProfileWorkflowElement.ActivityDefinitionId%2A?displayProperty=nameWithType> property.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="6e464-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="6e464-122">Parent Elements</span></span>  
  
|<span data-ttu-id="6e464-123">Élément</span><span class="sxs-lookup"><span data-stu-id="6e464-123">Element</span></span>|<span data-ttu-id="6e464-124">Description</span><span class="sxs-lookup"><span data-stu-id="6e464-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6e464-125">\<tracking></span><span class="sxs-lookup"><span data-stu-id="6e464-125">\<tracking></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/tracking.md)|<span data-ttu-id="6e464-126">Représente une section de configuration permettant de définir les paramètres de suivi d'un service de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="6e464-126">Represents a configuration section for defining tracking settings for a workflow service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6e464-127">Notes</span><span class="sxs-lookup"><span data-stu-id="6e464-127">Remarks</span></span>  
 <span data-ttu-id="6e464-128">Les modèles de suivi contiennent des requêtes de suivi qui permettent à un participant au suivi de s'abonner à des événements de flux de travail émis lorsque l'état d'une instance de flux de travail change au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="6e464-128">Tracking profiles contains tracking queries that permit a tracking participant to subscribe to workflow events that are emitted when the state of a workflow instance changes at runtime.</span></span> <span data-ttu-id="6e464-129">Selon vos exigences d’analyse, vous pouvez écrire un profil très général, qui s’abonne à un petit jeu de modifications d’état de haut niveau d’un workflow.</span><span class="sxs-lookup"><span data-stu-id="6e464-129">Depending on your monitoring requirements you may write a profile that is very coarse, which subscribes to a small set of high-level state changes on a workflow.</span></span> <span data-ttu-id="6e464-130">Inversement, vous pouvez créer un profil très spécifique dont les événements résultants sont suffisamment riches pour reconstruire ultérieurement un flux d'exécution détaillé.</span><span class="sxs-lookup"><span data-stu-id="6e464-130">Conversely, you may create a very specific profile whose resulting events are rich enough to reconstruct a detailed execution flow later.</span></span>  
  
 <span data-ttu-id="6e464-131">Les modèles de suivi sont structurés comme des abonnements déclaratifs aux enregistrements de suivi qui vous permettent d'interroger le runtime de flux de travail pour rechercher des enregistrements de suivi particuliers.</span><span class="sxs-lookup"><span data-stu-id="6e464-131">Tracking profiles are structured as declarative subscriptions for tracking records that allow you to query the workflow runtime for specific tracking records.</span></span> <span data-ttu-id="6e464-132">Il existe un certain nombre de types de requêtes qui permettent de vous abonner à différentes classes de <xref:System.Activities.Tracking.TrackingRecord> objets.</span><span class="sxs-lookup"><span data-stu-id="6e464-132">There are a handful of query types that allow you subscribe to different classes of <xref:System.Activities.Tracking.TrackingRecord> objects.</span></span> <span data-ttu-id="6e464-133">Pour obtenir une liste complète des requêtes, consultez [ \<participants >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/participants.md) et [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)...</span><span class="sxs-lookup"><span data-stu-id="6e464-133">For a complete list of queries, see [\<participants>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/participants.md) and [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)..</span></span>  
  
 <span data-ttu-id="6e464-134">L’exemple suivant montre un modèle de suivi dans un fichier de configuration qui permet à un participant de suivi pour vous abonner à la `Started` et `Completed` les événements de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="6e464-134">The following example shows a tracking profile in a configuration file that allows a tracking participant to subscribe to the `Started` and `Completed` workflow events.</span></span>  
  
```xml  
<system.serviceModel>  
  <tracking>    
    <trackingProfile name="Sample Tracking Profile">  
      <workflow activityDefinitionId="*">  
         <workflowInstanceQueries>  
            <workflowInstanceQuery>  
            <states>  
              <state name="Started"/>  
              <state name="Completed"/>  
            </states>  
          </workflowInstanceQuery>  
        </workflowInstanceQueries>  
      </workflow>  
    </trackingProfile>          
   </profiles>  
  </tracking>  
</system.serviceModel>  
```  
  
## <a name="see-also"></a><span data-ttu-id="6e464-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e464-135">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ProfileElement>
- <xref:System.Activities.Tracking.TrackingProfile>
- [<span data-ttu-id="6e464-136">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="6e464-136">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="6e464-137">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="6e464-137">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
