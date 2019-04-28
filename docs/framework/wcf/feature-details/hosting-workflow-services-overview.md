---
title: Vue d'ensemble de l'hébergement de services de workflow
ms.date: 03/30/2017
ms.assetid: 19f3704f-06bf-4eeb-8724-5224e02d7ead
ms.openlocfilehash: dbe271e30e9c4e98a52c01ffaa21de25c127c7ff
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61855892"
---
# <a name="hosting-workflow-services-overview"></a><span data-ttu-id="b6a09-102">Vue d'ensemble de l'hébergement de services de workflow</span><span class="sxs-lookup"><span data-stu-id="b6a09-102">Hosting Workflow Services Overview</span></span>
<span data-ttu-id="b6a09-103">Les services de workflow doivent être hébergés pour s'exécuter.</span><span class="sxs-lookup"><span data-stu-id="b6a09-103">Workflow services must be hosted to execute.</span></span> <span data-ttu-id="b6a09-104"><xref:System.ServiceModel.WorkflowServiceHost> est l'hôte de workflow prêt à l'emploi qui prend en charge plusieurs instances, la configuration et la messagerie WCF (bien que les workflows n'aient pas besoin d'utiliser la messagerie afin d'être hébergés).</span><span class="sxs-lookup"><span data-stu-id="b6a09-104">The <xref:System.ServiceModel.WorkflowServiceHost> is the out-of-the-box workflow host that supports multiple instances, configuration, and WCF messaging (although the workflows aren’t required to use messaging in order to be hosted).</span></span>  <span data-ttu-id="b6a09-105">Il permet également la persistance, le suivi et le contrôle de l'instance par un ensemble de comportements de service.</span><span class="sxs-lookup"><span data-stu-id="b6a09-105">It also integrates with persistence, tracking, and instance control through a set of service behaviors.</span></span>  <span data-ttu-id="b6a09-106">Tout comme le <xref:System.ServiceModel.ServiceHost> de WCF, <xref:System.ServiceModel.WorkflowServiceHost> peut être auto-hébergé dans n'importe quelle application .NET managée, ou hébergée sur le Web (comme un fichier .xamlx) dans IIS / WAS.</span><span class="sxs-lookup"><span data-stu-id="b6a09-106">Just like WCF’s <xref:System.ServiceModel.ServiceHost>, the <xref:System.ServiceModel.WorkflowServiceHost> can be self-hosted in any managed .NET application, or web-hosted (as a .xamlx file) in IIS / WAS.</span></span>  <span data-ttu-id="b6a09-107">Les rubriques de cette section décrivent comment héberger un service de workflow.</span><span class="sxs-lookup"><span data-stu-id="b6a09-107">Topics in this section describe how to host a workflow service.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="b6a09-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="b6a09-108">In This Section</span></span>  
 [<span data-ttu-id="b6a09-109">Hébergement de services de workflow</span><span class="sxs-lookup"><span data-stu-id="b6a09-109">Hosting Workflow Services</span></span>](../../../../docs/framework/wcf/feature-details/hosting-workflow-services.md)  
 <span data-ttu-id="b6a09-110">Décrit l'hébergement de services de workflow.</span><span class="sxs-lookup"><span data-stu-id="b6a09-110">Describes hosting workflow services.</span></span>  
  
 [<span data-ttu-id="b6a09-111">Éléments internes de l’hôte du service de workflow</span><span class="sxs-lookup"><span data-stu-id="b6a09-111">Workflow Service Host Internals</span></span>](../../../../docs/framework/wcf/feature-details/workflow-service-host-internals.md)  
 <span data-ttu-id="b6a09-112">Décrit comment <xref:System.ServiceModel.WorkflowServiceHost> traite les messages entrants.</span><span class="sxs-lookup"><span data-stu-id="b6a09-112">Describes how <xref:System.ServiceModel.WorkflowServiceHost> processes incoming messages.</span></span>  
  
 [<span data-ttu-id="b6a09-113">Extensibilité de l’hôte du service de workflow</span><span class="sxs-lookup"><span data-stu-id="b6a09-113">Workflow Service Host Extensibility</span></span>](../../../../docs/framework/wcf/feature-details/workflow-service-host-extensibility.md)  
 <span data-ttu-id="b6a09-114">Décrit comment étendre les fonctionnalités de l'hôte de service de workflow.</span><span class="sxs-lookup"><span data-stu-id="b6a09-114">Describes how to extend the functionality of the workflow service host.</span></span>  
  
 [<span data-ttu-id="b6a09-115">Point de terminaison de contrôle de workflow</span><span class="sxs-lookup"><span data-stu-id="b6a09-115">Workflow Control Endpoint</span></span>](../../../../docs/framework/wcf/feature-details/workflow-control-endpoint.md)  
 <span data-ttu-id="b6a09-116">Décrit comment définir un point de terminaison qui vous permet de créer des instances de workflow.</span><span class="sxs-lookup"><span data-stu-id="b6a09-116">Describes how to define an endpoint that allows you to create workflow instances.</span></span>
  
 [<span data-ttu-id="b6a09-117">Guide pratique pour Héberger un Service de flux de travail avec Windows Server AppFabric</span><span class="sxs-lookup"><span data-stu-id="b6a09-117">How to: Host a Workflow Service with Windows Server App Fabric</span></span>](../../../../docs/framework/wcf/feature-details/how-to-host-a-workflow-service-with-windows-server-app-fabric.md)  
 <span data-ttu-id="b6a09-118">Décrit comment héberger un service de workflow existant dans Windows Server App Fabric.</span><span class="sxs-lookup"><span data-stu-id="b6a09-118">Demonstrates how to host an existing workflow service in Windows Server App Fabric.</span></span>  
  
 [<span data-ttu-id="b6a09-119">Configuration de WorkflowServiceHost</span><span class="sxs-lookup"><span data-stu-id="b6a09-119">Configuring WorkflowServiceHost</span></span>](../../../../docs/framework/wcf/feature-details/configuring-workflowservicehost.md)  
 <span data-ttu-id="b6a09-120">Décrit comment contrôler la persistance, le suivi, l'inactivité et le comportement en cas d'exception non gérée.</span><span class="sxs-lookup"><span data-stu-id="b6a09-120">Describes how to control persistence, tracking, idle, and unhandled exception behavior.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="b6a09-121">Référence</span><span class="sxs-lookup"><span data-stu-id="b6a09-121">Reference</span></span>  
 <xref:System.ServiceModel.Activities.WorkflowServiceHost>  
  
 <xref:System.ServiceModel.Activities.WorkflowService>  
  
 <xref:System.ServiceModel.Activation.ServiceHostFactory>  
  
 <xref:System.ServiceModel.Activation.ServiceHostFactoryBase>  
  
 <xref:System.ServiceModel.Activation.WorkflowServiceHostFactory>  
  
## <a name="related-sections"></a><span data-ttu-id="b6a09-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b6a09-122">Related Sections</span></span>  
 [<span data-ttu-id="b6a09-123">Services de workflow</span><span class="sxs-lookup"><span data-stu-id="b6a09-123">Workflow Services</span></span>](../../../../docs/framework/wcf/feature-details/workflow-services.md)
