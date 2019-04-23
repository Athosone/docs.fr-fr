---
title: Utilisation de l'annotation dans les requêtes
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 50855b30-d5fe-49a9-89d3-3f1bfd670958
ms.openlocfilehash: fd2d98852ca44e3485ddcf4be29d505b39011698
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59208642"
---
# <a name="using-annotation-in-queries"></a><span data-ttu-id="4fff4-102">Utilisation de l'annotation dans les requêtes</span><span class="sxs-lookup"><span data-stu-id="4fff4-102">Using Annotation in Queries</span></span>
<span data-ttu-id="4fff4-103">Grâce aux annotations, vous pouvez baliser arbitrairement des enregistrements de suivi avec une valeur configurable après la génération.</span><span class="sxs-lookup"><span data-stu-id="4fff4-103">Annotations allow you to arbitrarily tag tracking records with a value that can be configured after build time.</span></span> <span data-ttu-id="4fff4-104">Par exemple, vous souhaiterez plusieurs enregistrements de suivi sur plusieurs flux de travail soient balisés avec « Mail Server » == « Mail Server1 ».</span><span class="sxs-lookup"><span data-stu-id="4fff4-104">For example, you might want several tracking records across several workflows to be tagged with "Mail Server" == "Mail Server1".</span></span> <span data-ttu-id="4fff4-105">Lors de l’interrogation ultérieure d’enregistrements de suivi, cela facilite la recherche de tous les enregistrements ayant cette étiquette.</span><span class="sxs-lookup"><span data-stu-id="4fff4-105">This makes it easy to find all records with this tag when querying tracking records later.</span></span>  
  
## <a name="adding-annotations"></a><span data-ttu-id="4fff4-106">Ajout d'annotations</span><span class="sxs-lookup"><span data-stu-id="4fff4-106">Adding Annotations</span></span>  
 <span data-ttu-id="4fff4-107">Une annotation peut être ajoutée à une requête de suivi tel qu'indiqué dans l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="4fff4-107">An annotation can be added to a tracking query as shown in the following example.</span></span>  
  
```xml  
<activityStateQuery activityName="SendEmailActivity">  
  <states>  
    <state name="Closed"/>  
  </states>  
  <annotations>  
    <annotation name="MailServer" value="Mail Server1"/>  
  </annotations>  
</activityStateQuery>  
```  
  
> [!NOTE]
>  <span data-ttu-id="4fff4-108">Ces éléments de requête de suivi peuvent être utilisés pour créer un modèle de suivi.</span><span class="sxs-lookup"><span data-stu-id="4fff4-108">These tracking query elements can be used to create a tracking profile.</span></span> <span data-ttu-id="4fff4-109">Un modèle de suivi peut être créé dans la configuration ou à l'aide du code.</span><span class="sxs-lookup"><span data-stu-id="4fff4-109">A tracking profile can be created either in configuration or using code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4fff4-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fff4-110">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ProfileWorkflowElement>
- <xref:System.Activities.Tracking.TrackingProfile>
- [<span data-ttu-id="4fff4-111">\<participants></span><span class="sxs-lookup"><span data-stu-id="4fff4-111">\<participants></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/participants.md)
- [<span data-ttu-id="4fff4-112">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="4fff4-112">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="4fff4-113">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="4fff4-113">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
