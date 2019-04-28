---
title: 1041 - WorkflowApplicationPersistableIdle
ms.date: 03/30/2017
ms.assetid: 966adf2f-e21d-44df-a3ec-a8e285e0a316
ms.openlocfilehash: 07be0ae603443a1ef06cb539bba7b227d7b3e325
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61924187"
---
# <a name="1041---workflowapplicationpersistableidle"></a><span data-ttu-id="a4a26-102">1041 - WorkflowApplicationPersistableIdle</span><span class="sxs-lookup"><span data-stu-id="a4a26-102">1041 - WorkflowApplicationPersistableIdle</span></span>
## <a name="properties"></a><span data-ttu-id="a4a26-103">Properties</span><span class="sxs-lookup"><span data-stu-id="a4a26-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="a4a26-104">Id</span><span class="sxs-lookup"><span data-stu-id="a4a26-104">ID</span></span>|<span data-ttu-id="a4a26-105">1041</span><span class="sxs-lookup"><span data-stu-id="a4a26-105">1041</span></span>|  
|<span data-ttu-id="a4a26-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a4a26-106">Keywords</span></span>|<span data-ttu-id="a4a26-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="a4a26-107">WFRuntime</span></span>|  
|<span data-ttu-id="a4a26-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="a4a26-108">Level</span></span>|<span data-ttu-id="a4a26-109">Information</span><span class="sxs-lookup"><span data-stu-id="a4a26-109">Information</span></span>|  
|<span data-ttu-id="a4a26-110">Canal</span><span class="sxs-lookup"><span data-stu-id="a4a26-110">Channel</span></span>|<span data-ttu-id="a4a26-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="a4a26-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="a4a26-112">Description</span><span class="sxs-lookup"><span data-stu-id="a4a26-112">Description</span></span>  
 <span data-ttu-id="a4a26-113">Indique qu'une application de workflow est inactive et persistante.</span><span class="sxs-lookup"><span data-stu-id="a4a26-113">Indicates that a workflow application is idle and persistable.</span></span> <span data-ttu-id="a4a26-114">L'application de workflow sera inactive ou persistante.</span><span class="sxs-lookup"><span data-stu-id="a4a26-114">The workflow application will be idled or persisted.</span></span>  
  
## <a name="message"></a><span data-ttu-id="a4a26-115">Message</span><span class="sxs-lookup"><span data-stu-id="a4a26-115">Message</span></span>  
 <span data-ttu-id="a4a26-116">WorkflowApplication Id : '%1' est inactif et persistant.</span><span class="sxs-lookup"><span data-stu-id="a4a26-116">WorkflowApplication Id: '%1' is idle and persistable.</span></span>  <span data-ttu-id="a4a26-117">L’action suivante sera effectuée : %2.</span><span class="sxs-lookup"><span data-stu-id="a4a26-117">The following action will be taken: %2.</span></span>  
  
## <a name="details"></a><span data-ttu-id="a4a26-118">Détails</span><span class="sxs-lookup"><span data-stu-id="a4a26-118">Details</span></span>  
  
|<span data-ttu-id="a4a26-119">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="a4a26-119">Data Item Name</span></span>|<span data-ttu-id="a4a26-120">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="a4a26-120">Data Item Type</span></span>|<span data-ttu-id="a4a26-121">Description</span><span class="sxs-lookup"><span data-stu-id="a4a26-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="a4a26-122">WorkflowApplicationId</span><span class="sxs-lookup"><span data-stu-id="a4a26-122">WorkflowApplicationId</span></span>|<span data-ttu-id="a4a26-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="a4a26-123">xs:string</span></span>|<span data-ttu-id="a4a26-124">ID d'application de flux de travail</span><span class="sxs-lookup"><span data-stu-id="a4a26-124">The workflow application id</span></span>|  
|<span data-ttu-id="a4a26-125">ActionTaken</span><span class="sxs-lookup"><span data-stu-id="a4a26-125">ActionTaken</span></span>|<span data-ttu-id="a4a26-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="a4a26-126">xs:string</span></span>|<span data-ttu-id="a4a26-127">Mesure qui sera prise sur l'application de workflow.</span><span class="sxs-lookup"><span data-stu-id="a4a26-127">The action that will be taken on the workflow application.</span></span>|  
|<span data-ttu-id="a4a26-128">AppDomain</span><span class="sxs-lookup"><span data-stu-id="a4a26-128">AppDomain</span></span>|<span data-ttu-id="a4a26-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="a4a26-129">xs:string</span></span>|<span data-ttu-id="a4a26-130">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="a4a26-130">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
