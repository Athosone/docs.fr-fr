---
title: <add> de <services>
ms.date: 03/30/2017
ms.assetid: 6bdc4590-aa9c-4ec8-9345-879d780cd141
ms.openlocfilehash: c07b3377db4f5b434fd021b09de510c1d43ec832
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61673574"
---
# <a name="add-of-services"></a><span data-ttu-id="3c8a8-102">\<Ajouter > de \<services ></span><span class="sxs-lookup"><span data-stu-id="3c8a8-102">\<add> of \<services></span></span>
<span data-ttu-id="3c8a8-103">Spécifie les paramètres d’une instance de <xref:System.Workflow.Runtime.WorkflowRuntime> pour l’hébergement de services de Windows Communication Foundation (WCF) basés sur les flux de travail.</span><span class="sxs-lookup"><span data-stu-id="3c8a8-103">Specifies settings for an instance of <xref:System.Workflow.Runtime.WorkflowRuntime> for hosting workflow-based Windows Communication Foundation (WCF) services.</span></span> <span data-ttu-id="3c8a8-104">Cet élément est de type <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="3c8a8-104">This element is of type <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span></span>  
  
 <span data-ttu-id="3c8a8-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="3c8a8-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="3c8a8-106">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="3c8a8-106">\<behaviors></span></span>  
<span data-ttu-id="3c8a8-107">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="3c8a8-107">\<serviceBehaviors></span></span>  
<span data-ttu-id="3c8a8-108">\<behavior></span><span class="sxs-lookup"><span data-stu-id="3c8a8-108">\<behavior></span></span>  
<span data-ttu-id="3c8a8-109">\<services></span><span class="sxs-lookup"><span data-stu-id="3c8a8-109">\<services></span></span>  
<span data-ttu-id="3c8a8-110">\<add></span><span class="sxs-lookup"><span data-stu-id="3c8a8-110">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3c8a8-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c8a8-111">Syntax</span></span>  
  
```xml  
<workflowRuntime>
  <services>
    <add type="String" />
  </services>
</workflowRuntime>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3c8a8-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="3c8a8-112">Attributes and Elements</span></span>  
 <span data-ttu-id="3c8a8-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="3c8a8-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3c8a8-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="3c8a8-114">Attributes</span></span>  
  
|<span data-ttu-id="3c8a8-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="3c8a8-115">Attribute</span></span>|<span data-ttu-id="3c8a8-116">Description</span><span class="sxs-lookup"><span data-stu-id="3c8a8-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="3c8a8-117">type</span><span class="sxs-lookup"><span data-stu-id="3c8a8-117">type</span></span>|<span data-ttu-id="3c8a8-118">Chaîne indiquant le nom qualifié du type d'assembly correspondant au service à initialiser.</span><span class="sxs-lookup"><span data-stu-id="3c8a8-118">A string that specifies the assembly-qualified type name of the service to be initialized.</span></span> <span data-ttu-id="3c8a8-119">Les services spécifiés doivent suivre certaines règles en ce qui concerne les signatures de leurs constructeurs.</span><span class="sxs-lookup"><span data-stu-id="3c8a8-119">The service specified must follow certain rules about the signatures of their constructors.</span></span> <span data-ttu-id="3c8a8-120">Pour plus d'informations, voir <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="3c8a8-120">See <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement> for more information.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3c8a8-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3c8a8-121">Child Elements</span></span>  
 <span data-ttu-id="3c8a8-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="3c8a8-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="3c8a8-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3c8a8-123">Parent Elements</span></span>  
  
|<span data-ttu-id="3c8a8-124">Élément</span><span class="sxs-lookup"><span data-stu-id="3c8a8-124">Element</span></span>|<span data-ttu-id="3c8a8-125">Description</span><span class="sxs-lookup"><span data-stu-id="3c8a8-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3c8a8-126">\<services></span><span class="sxs-lookup"><span data-stu-id="3c8a8-126">\<services></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/services-of-workflowruntime.md)|<span data-ttu-id="3c8a8-127">Collection de services qui sera ajoutée au moteur de <xref:System.Workflow.Runtime.WorkflowRuntime>.</span><span class="sxs-lookup"><span data-stu-id="3c8a8-127">A collection of services that will be added to the <xref:System.Workflow.Runtime.WorkflowRuntime> engine.</span></span> <span data-ttu-id="3c8a8-128">Les éléments sont de type <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="3c8a8-128">The elements are of type <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span></span>  <span data-ttu-id="3c8a8-129">Les services spécifiés dans la collection sont initialisés par le moteur d’exécution de workflow et ajoutés à ses services lorsque le constructeur <xref:System.Workflow.Runtime.WorkflowRuntime> approprié est appelé.</span><span class="sxs-lookup"><span data-stu-id="3c8a8-129">The services specified in the collection will be initialized by the workflow runtime engine and added to its services when the appropriate <xref:System.Workflow.Runtime.WorkflowRuntime> constructor is called.</span></span> <span data-ttu-id="3c8a8-130">Par conséquent, les services spécifiés dans la collection doivent suivre certaines règles en ce qui concerne les signatures de leurs constructeurs.</span><span class="sxs-lookup"><span data-stu-id="3c8a8-130">Therefore, the services specified in the collection must follow certain rules about the signatures of their constructors.</span></span> <span data-ttu-id="3c8a8-131">Pour plus d'informations, voir <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="3c8a8-131">See <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement> for more information.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3c8a8-132">Notes</span><span class="sxs-lookup"><span data-stu-id="3c8a8-132">Remarks</span></span>  
 <span data-ttu-id="3c8a8-133">Le service spécifié dans cet élément est initialisé par le moteur d'exécution de workflow et ajouté à ses services lorsque le constructeur <xref:System.Workflow.Runtime.WorkflowRuntime> approprié est appelé.</span><span class="sxs-lookup"><span data-stu-id="3c8a8-133">The service specified in this element will be initialized by the workflow runtime engine and added to its services when the appropriate <xref:System.Workflow.Runtime.WorkflowRuntime> constructor is called.</span></span> <span data-ttu-id="3c8a8-134">Par conséquent, le service spécifié doit suivre certaines règles en ce qui concerne les signatures de son constructeur.</span><span class="sxs-lookup"><span data-stu-id="3c8a8-134">Therefore, the service specified must follow certain rules about the signatures of their constructors.</span></span> <span data-ttu-id="3c8a8-135">Pour plus d'informations, voir <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="3c8a8-135">See <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement> for more information.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3c8a8-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="3c8a8-136">Example</span></span>  
  
```xml  
<serviceBehaviors>
  <behavior name="ServiceBehavior">
    <workflowRuntime name="WorkflowServiceHostRuntime"
                     validateOnCreate="true"
                     enablePerformanceCounters="true">
      <services>
        <add type="NetFx.Checkin.Scenario.WorkflowServices.WorkflowBasedServices.Common.TestPersistenceService.FilePersistenceService, NetFx.Checkin.Scenario.WorkflowServices.WorkflowBasedServices.Common" />
      </services>
    </workflowRuntime>
  </behavior>
</serviceBehaviors>
```  
  
## <a name="see-also"></a><span data-ttu-id="3c8a8-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c8a8-137">See also</span></span>

- <xref:System.ServiceModel.Configuration.WorkflowRuntimeElement>
- <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>
- <xref:System.Workflow.Runtime.WorkflowRuntime>
- <span data-ttu-id="3c8a8-138">[Fichiers de Configuration de flux de travail](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="3c8a8-138">[Workflow Configuration Files](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90))</span></span>
