---
title: Événement ETW de pile
ms.date: 03/30/2017
helpviewer_keywords:
- stack event [.NET Framework]
- ETW, stack event (CLR)
ms.assetid: f612fa5b-4b62-4593-a19e-85c9b1018dce
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a7cba2bd1dd5b83e29c7a6c192a1a7e5e2d33ecc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61949147"
---
# <a name="stack-etw-event"></a><span data-ttu-id="fb4cc-102">Événement ETW de pile</span><span class="sxs-lookup"><span data-stu-id="fb4cc-102">Stack ETW Event</span></span>
<span data-ttu-id="fb4cc-103">L’événement de pile doit être utilisé conjointement avec d’autres événements pour générer des arborescences d’appels de procédure après le déclenchement d’un événement.</span><span class="sxs-lookup"><span data-stu-id="fb4cc-103">The stack event should be used in conjunction with other events to generate stack traces after an event is raised.</span></span> <span data-ttu-id="fb4cc-104">Il est enregistré quand le fournisseur du runtime est activé.</span><span class="sxs-lookup"><span data-stu-id="fb4cc-104">It is logged when the runtime provider is enabled.</span></span> <span data-ttu-id="fb4cc-105">Il s’agit d’un événement très fréquent, car il est déclenché à chaque déclenchement d’un autre événement runtime.</span><span class="sxs-lookup"><span data-stu-id="fb4cc-105">This is a very high frequency event, because it is raised whenever another runtime event is raised.</span></span> <span data-ttu-id="fb4cc-106">Pour cette raison, nous vous recommandons d’utiliser cet événement avec précaution.</span><span class="sxs-lookup"><span data-stu-id="fb4cc-106">For this reason, we recommend that you use this event with caution.</span></span>  
  
 <span data-ttu-id="fb4cc-107">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="fb4cc-107">The following table shows the keyword and level.</span></span> <span data-ttu-id="fb4cc-108">(Pour plus d'informations, consultez [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span><span class="sxs-lookup"><span data-stu-id="fb4cc-108">(For more information, see [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span></span>  
  
|<span data-ttu-id="fb4cc-109">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="fb4cc-109">Keyword for raising the event</span></span>|<span data-ttu-id="fb4cc-110">Niveau</span><span class="sxs-lookup"><span data-stu-id="fb4cc-110">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="fb4cc-111">`StackKeyword` (0x40000000)</span><span class="sxs-lookup"><span data-stu-id="fb4cc-111">`StackKeyword` (0x40000000)</span></span>|<span data-ttu-id="fb4cc-112">LogAlways(0)</span><span class="sxs-lookup"><span data-stu-id="fb4cc-112">LogAlways(0)</span></span>|  
  
 <span data-ttu-id="fb4cc-113">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="fb4cc-113">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="fb4cc-114">Événement</span><span class="sxs-lookup"><span data-stu-id="fb4cc-114">Event</span></span>|<span data-ttu-id="fb4cc-115">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="fb4cc-115">Event ID</span></span>|<span data-ttu-id="fb4cc-116">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="fb4cc-116">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`CLRStackWalk`|<span data-ttu-id="fb4cc-117">82</span><span class="sxs-lookup"><span data-stu-id="fb4cc-117">82</span></span>|<span data-ttu-id="fb4cc-118">Conjointement avec d’autres événements pour générer les arborescences des appels de procédure après un événement.</span><span class="sxs-lookup"><span data-stu-id="fb4cc-118">In conjunction with other events to generate stack traces following an event.</span></span>|  
  
 <span data-ttu-id="fb4cc-119">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="fb4cc-119">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="fb4cc-120">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="fb4cc-120">Field name</span></span>|<span data-ttu-id="fb4cc-121">Type de données</span><span class="sxs-lookup"><span data-stu-id="fb4cc-121">Data Type</span></span>|<span data-ttu-id="fb4cc-122">Description</span><span class="sxs-lookup"><span data-stu-id="fb4cc-122">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="fb4cc-123">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="fb4cc-123">ClrInstanceID</span></span>|<span data-ttu-id="fb4cc-124">win:Uint16</span><span class="sxs-lookup"><span data-stu-id="fb4cc-124">win:Uint16</span></span>|<span data-ttu-id="fb4cc-125">Identificateur de runtime unique.</span><span class="sxs-lookup"><span data-stu-id="fb4cc-125">Unique runtime identifier.</span></span>|  
|<span data-ttu-id="fb4cc-126">Reserved1</span><span class="sxs-lookup"><span data-stu-id="fb4cc-126">Reserved1</span></span>|<span data-ttu-id="fb4cc-127">win:UInt8</span><span class="sxs-lookup"><span data-stu-id="fb4cc-127">win:UInt8</span></span>|<span data-ttu-id="fb4cc-128">Réservé.</span><span class="sxs-lookup"><span data-stu-id="fb4cc-128">Reserved.</span></span>|  
|<span data-ttu-id="fb4cc-129">Reserved2</span><span class="sxs-lookup"><span data-stu-id="fb4cc-129">Reserved2</span></span>|<span data-ttu-id="fb4cc-130">win:UInt8</span><span class="sxs-lookup"><span data-stu-id="fb4cc-130">win:UInt8</span></span>|<span data-ttu-id="fb4cc-131">Réservé.</span><span class="sxs-lookup"><span data-stu-id="fb4cc-131">Reserved.</span></span>|  
|<span data-ttu-id="fb4cc-132">FrameCount</span><span class="sxs-lookup"><span data-stu-id="fb4cc-132">FrameCount</span></span>|<span data-ttu-id="fb4cc-133">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="fb4cc-133">win:UInt32</span></span>|<span data-ttu-id="fb4cc-134">Nombre de frames dans l’arborescence des appels de procédure.</span><span class="sxs-lookup"><span data-stu-id="fb4cc-134">The number of frames in the stack trace.</span></span>|  
|<span data-ttu-id="fb4cc-135">Stack</span><span class="sxs-lookup"><span data-stu-id="fb4cc-135">Stack</span></span>|<span data-ttu-id="fb4cc-136">win:Pointer</span><span class="sxs-lookup"><span data-stu-id="fb4cc-136">win:Pointer</span></span>|<span data-ttu-id="fb4cc-137">Colonnes de pointeurs d’instruction.</span><span class="sxs-lookup"><span data-stu-id="fb4cc-137">Columns of instruction pointers.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="fb4cc-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb4cc-138">See also</span></span>

- [<span data-ttu-id="fb4cc-139">Événements ETW du CLR</span><span class="sxs-lookup"><span data-stu-id="fb4cc-139">CLR ETW Events</span></span>](../../../docs/framework/performance/clr-etw-events.md)
