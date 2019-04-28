---
title: 1010 - ActivityCompleted
ms.date: 03/30/2017
ms.assetid: d256284e-3fd2-4c33-82f4-abb617575706
ms.openlocfilehash: 355281e6aa8f621bd2f9c0862e641fafec872750
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62008369"
---
# <a name="1010---activitycompleted"></a><span data-ttu-id="10de0-102">1010 - ActivityCompleted</span><span class="sxs-lookup"><span data-stu-id="10de0-102">1010 - ActivityCompleted</span></span>
## <a name="properties"></a><span data-ttu-id="10de0-103">Properties</span><span class="sxs-lookup"><span data-stu-id="10de0-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="10de0-104">Id</span><span class="sxs-lookup"><span data-stu-id="10de0-104">ID</span></span>|<span data-ttu-id="10de0-105">1010</span><span class="sxs-lookup"><span data-stu-id="10de0-105">1010</span></span>|  
|<span data-ttu-id="10de0-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="10de0-106">Keywords</span></span>|<span data-ttu-id="10de0-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="10de0-107">WFRuntime</span></span>|  
|<span data-ttu-id="10de0-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="10de0-108">Level</span></span>|<span data-ttu-id="10de0-109">Information</span><span class="sxs-lookup"><span data-stu-id="10de0-109">Information</span></span>|  
|<span data-ttu-id="10de0-110">Canal</span><span class="sxs-lookup"><span data-stu-id="10de0-110">Channel</span></span>|<span data-ttu-id="10de0-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="10de0-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="10de0-112">Description</span><span class="sxs-lookup"><span data-stu-id="10de0-112">Description</span></span>  
 <span data-ttu-id="10de0-113">Indique que l'exécution d'une activité est terminée.</span><span class="sxs-lookup"><span data-stu-id="10de0-113">Indicates an activity has completed execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="10de0-114">Message</span><span class="sxs-lookup"><span data-stu-id="10de0-114">Message</span></span>  
 <span data-ttu-id="10de0-115">L'activité « %1 », DisplayName : « %2 », InstanceId : « %3 » s'est terminée à l'état « %4 ».</span><span class="sxs-lookup"><span data-stu-id="10de0-115">Activity '%1', DisplayName: '%2', InstanceId: '%3' has completed in the '%4' state.</span></span>  
  
## <a name="details"></a><span data-ttu-id="10de0-116">Détails</span><span class="sxs-lookup"><span data-stu-id="10de0-116">Details</span></span>  
  
|<span data-ttu-id="10de0-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="10de0-117">Data Item Name</span></span>|<span data-ttu-id="10de0-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="10de0-118">Data Item Type</span></span>|<span data-ttu-id="10de0-119">Description</span><span class="sxs-lookup"><span data-stu-id="10de0-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="10de0-120">Activité</span><span class="sxs-lookup"><span data-stu-id="10de0-120">Activity</span></span>|<span data-ttu-id="10de0-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="10de0-121">xs:string</span></span>|<span data-ttu-id="10de0-122">Nom de type de l'activité.</span><span class="sxs-lookup"><span data-stu-id="10de0-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="10de0-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="10de0-123">DisplayName</span></span>|<span data-ttu-id="10de0-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="10de0-124">xs:string</span></span>|<span data-ttu-id="10de0-125">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="10de0-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="10de0-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="10de0-126">InstanceId</span></span>|<span data-ttu-id="10de0-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="10de0-127">xs:string</span></span>|<span data-ttu-id="10de0-128">ID d'instance de l'activité.</span><span class="sxs-lookup"><span data-stu-id="10de0-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="10de0-129">État</span><span class="sxs-lookup"><span data-stu-id="10de0-129">State</span></span>|<span data-ttu-id="10de0-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="10de0-130">xs:string</span></span>|<span data-ttu-id="10de0-131">État de l'activité.</span><span class="sxs-lookup"><span data-stu-id="10de0-131">The state of the activity.</span></span>|  
|<span data-ttu-id="10de0-132">AppDomain</span><span class="sxs-lookup"><span data-stu-id="10de0-132">AppDomain</span></span>|<span data-ttu-id="10de0-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="10de0-133">xs:string</span></span>|<span data-ttu-id="10de0-134">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="10de0-134">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
