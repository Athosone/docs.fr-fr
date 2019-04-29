---
title: Événements ETW d'interopérabilité
ms.date: 03/30/2017
helpviewer_keywords:
- interop events [.NET Framework]
- ETW, interop events (CLR)
ms.assetid: eb6eac2e-45f4-4923-a32c-38f203da66df
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 09b2848619256a255cc27f0268d46e5e6db8cbe4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61949303"
---
# <a name="interop-etw-events"></a><span data-ttu-id="b144a-102">Événements ETW d'interopérabilité</span><span class="sxs-lookup"><span data-stu-id="b144a-102">Interop ETW Events</span></span>
<a name="top"></a> <span data-ttu-id="b144a-103">Les événements d'interopérabilité capturent des informations sur la création et la mise en cache du stub MSIL (Microsoft Intermediate Language).</span><span class="sxs-lookup"><span data-stu-id="b144a-103">Interop events capture information about Microsoft intermediate language (MSIL) stub generation and caching.</span></span>  
  
 <span data-ttu-id="b144a-104">Cette catégorie comprend les événements suivants :</span><span class="sxs-lookup"><span data-stu-id="b144a-104">This category consists of the following events:</span></span>  
  
- [<span data-ttu-id="b144a-105">Événement ILStubGenerated</span><span class="sxs-lookup"><span data-stu-id="b144a-105">ILStubGenerated Event</span></span>](#ilstubgenerated_event)  
  
- [<span data-ttu-id="b144a-106">Événement ILStubCacheHit</span><span class="sxs-lookup"><span data-stu-id="b144a-106">ILStubCacheHit Event</span></span>](#ilstubcachehit_event)  
  
<a name="ilstubgenerated_event"></a>   
## <a name="ilstubgenerated-event"></a><span data-ttu-id="b144a-107">Événement ILStubGenerated</span><span class="sxs-lookup"><span data-stu-id="b144a-107">ILStubGenerated Event</span></span>  
 <span data-ttu-id="b144a-108">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="b144a-108">The following table shows the keyword and level.</span></span> <span data-ttu-id="b144a-109">(Pour plus d'informations, consultez [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span><span class="sxs-lookup"><span data-stu-id="b144a-109">(For more information, see [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span></span>  
  
|<span data-ttu-id="b144a-110">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="b144a-110">Keyword for raising the event</span></span>|<span data-ttu-id="b144a-111">Niveau</span><span class="sxs-lookup"><span data-stu-id="b144a-111">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="b144a-112">`InteropKeyword` (0x2000)</span><span class="sxs-lookup"><span data-stu-id="b144a-112">`InteropKeyword` (0x2000)</span></span>|<span data-ttu-id="b144a-113">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="b144a-113">Informational(4)</span></span>|  
  
 <span data-ttu-id="b144a-114">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="b144a-114">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="b144a-115">Événement</span><span class="sxs-lookup"><span data-stu-id="b144a-115">Event</span></span>|<span data-ttu-id="b144a-116">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="b144a-116">Event ID</span></span>|<span data-ttu-id="b144a-117">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="b144a-117">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`ILStubGenerated`|<span data-ttu-id="b144a-118">88</span><span class="sxs-lookup"><span data-stu-id="b144a-118">88</span></span>|<span data-ttu-id="b144a-119">Le stub MSIL a été généré.</span><span class="sxs-lookup"><span data-stu-id="b144a-119">The MSIL stub has been generated.</span></span>|  
  
 <span data-ttu-id="b144a-120">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="b144a-120">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="b144a-121">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="b144a-121">Field name</span></span>|<span data-ttu-id="b144a-122">Type de données</span><span class="sxs-lookup"><span data-stu-id="b144a-122">Data type</span></span>|<span data-ttu-id="b144a-123">Description</span><span class="sxs-lookup"><span data-stu-id="b144a-123">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="b144a-124">ModuleID</span><span class="sxs-lookup"><span data-stu-id="b144a-124">ModuleID</span></span>|<span data-ttu-id="b144a-125">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="b144a-125">win:UInt16</span></span>|<span data-ttu-id="b144a-126">Identificateur du module</span><span class="sxs-lookup"><span data-stu-id="b144a-126">The module identifier.</span></span>|  
|<span data-ttu-id="b144a-127">StubMethodID</span><span class="sxs-lookup"><span data-stu-id="b144a-127">StubMethodID</span></span>|<span data-ttu-id="b144a-128">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="b144a-128">win:UInt64</span></span>|<span data-ttu-id="b144a-129">Identificateur de la méthode stub</span><span class="sxs-lookup"><span data-stu-id="b144a-129">The stub method identifier.</span></span>|  
|<span data-ttu-id="b144a-130">StubFlags</span><span class="sxs-lookup"><span data-stu-id="b144a-130">StubFlags</span></span>|<span data-ttu-id="b144a-131">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="b144a-131">win:UInt64</span></span>|<span data-ttu-id="b144a-132">Indicateurs du stub :</span><span class="sxs-lookup"><span data-stu-id="b144a-132">The flags for the stub:</span></span><br /><br /> <span data-ttu-id="b144a-133">0x1 – Interopérabilité inversée.</span><span class="sxs-lookup"><span data-stu-id="b144a-133">0x1 - Reverse interop.</span></span><br /><br /> <span data-ttu-id="b144a-134">0x2 – COM Interop</span><span class="sxs-lookup"><span data-stu-id="b144a-134">0x2 - COM interop.</span></span><br /><br /> <span data-ttu-id="b144a-135">0x4 – Stub généré par NGen.exe.</span><span class="sxs-lookup"><span data-stu-id="b144a-135">0x4 - Stub generated by NGen.exe.</span></span><br /><br /> <span data-ttu-id="b144a-136">0x8 – Délégué</span><span class="sxs-lookup"><span data-stu-id="b144a-136">0x8 - Delegate.</span></span><br /><br /> <span data-ttu-id="b144a-137">0x10 – Argument variable</span><span class="sxs-lookup"><span data-stu-id="b144a-137">0x10 - Variable arrgument.</span></span><br /><br /> <span data-ttu-id="b144a-138">0x20 – Appelé non managé</span><span class="sxs-lookup"><span data-stu-id="b144a-138">0x20 - Unmanaged callee.</span></span>|  
|<span data-ttu-id="b144a-139">ManagedInteropMethodToken</span><span class="sxs-lookup"><span data-stu-id="b144a-139">ManagedInteropMethodToken</span></span>|<span data-ttu-id="b144a-140">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="b144a-140">win:UInt32</span></span>|<span data-ttu-id="b144a-141">Jeton de la méthode d’interopérabilité managée</span><span class="sxs-lookup"><span data-stu-id="b144a-141">The token for the managed interop method.</span></span>|  
|<span data-ttu-id="b144a-142">ManagedInteropMethodNameSpace</span><span class="sxs-lookup"><span data-stu-id="b144a-142">ManagedInteropMethodNameSpace</span></span>|<span data-ttu-id="b144a-143">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="b144a-143">win:UnicodeString</span></span>|<span data-ttu-id="b144a-144">Espace de noms de la méthode d’interopérabilité managée</span><span class="sxs-lookup"><span data-stu-id="b144a-144">The namespace of the managed interop method.</span></span>|  
|<span data-ttu-id="b144a-145">ManagedInteropMethodName</span><span class="sxs-lookup"><span data-stu-id="b144a-145">ManagedInteropMethodName</span></span>|<span data-ttu-id="b144a-146">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="b144a-146">win:UnicodeString</span></span>|<span data-ttu-id="b144a-147">Nom de la méthode d’interopérabilité managée</span><span class="sxs-lookup"><span data-stu-id="b144a-147">The name of the managed interop method.</span></span>|  
|<span data-ttu-id="b144a-148">ManagedInteropMethodSignature</span><span class="sxs-lookup"><span data-stu-id="b144a-148">ManagedInteropMethodSignature</span></span>|<span data-ttu-id="b144a-149">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="b144a-149">win:UnicodeString</span></span>|<span data-ttu-id="b144a-150">Signature de la méthode d'interopérabilité managée</span><span class="sxs-lookup"><span data-stu-id="b144a-150">The signature of the managed interop method.</span></span>|  
|<span data-ttu-id="b144a-151">NativeMethodSignature</span><span class="sxs-lookup"><span data-stu-id="b144a-151">NativeMethodSignature</span></span>|<span data-ttu-id="b144a-152">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="b144a-152">win:UnicodeString</span></span>|<span data-ttu-id="b144a-153">Signature de la méthode native</span><span class="sxs-lookup"><span data-stu-id="b144a-153">The native method signature.</span></span>|  
|<span data-ttu-id="b144a-154">StubMethodSignature</span><span class="sxs-lookup"><span data-stu-id="b144a-154">StubMethodSignature</span></span>|<span data-ttu-id="b144a-155">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="b144a-155">win:UnicodeString</span></span>|<span data-ttu-id="b144a-156">Signature de la méthode stub</span><span class="sxs-lookup"><span data-stu-id="b144a-156">The stub method signature.</span></span>|  
|<span data-ttu-id="b144a-157">StubMethodILCode</span><span class="sxs-lookup"><span data-stu-id="b144a-157">StubMethodILCode</span></span>|<span data-ttu-id="b144a-158">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="b144a-158">win:UnicodeString</span></span>|<span data-ttu-id="b144a-159">Code MSIL de la méthode stub</span><span class="sxs-lookup"><span data-stu-id="b144a-159">The MSIL code for the stub method.</span></span>|  
|<span data-ttu-id="b144a-160">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="b144a-160">ClrInstanceID</span></span>|<span data-ttu-id="b144a-161">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="b144a-161">win:UInt16</span></span>|<span data-ttu-id="b144a-162">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="b144a-162">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="b144a-163">Retour au début</span><span class="sxs-lookup"><span data-stu-id="b144a-163">Back to top</span></span>](#top)  
  
<a name="ilstubcachehit_event"></a>   
## <a name="ilstubcachehit-event"></a><span data-ttu-id="b144a-164">Événement ILStubCacheHit</span><span class="sxs-lookup"><span data-stu-id="b144a-164">ILStubCacheHit Event</span></span>  
 <span data-ttu-id="b144a-165">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="b144a-165">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="b144a-166">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="b144a-166">Keyword for raising the event</span></span>|<span data-ttu-id="b144a-167">Niveau</span><span class="sxs-lookup"><span data-stu-id="b144a-167">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="b144a-168">`InteropKeyword` (0x2000)</span><span class="sxs-lookup"><span data-stu-id="b144a-168">`InteropKeyword` (0x2000)</span></span>|<span data-ttu-id="b144a-169">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="b144a-169">Informational(4)</span></span>|  
  
 <span data-ttu-id="b144a-170">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="b144a-170">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="b144a-171">Événement</span><span class="sxs-lookup"><span data-stu-id="b144a-171">Event</span></span>|<span data-ttu-id="b144a-172">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="b144a-172">Event ID</span></span>|<span data-ttu-id="b144a-173">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="b144a-173">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`ILStubCacheHit`|<span data-ttu-id="b144a-174">89</span><span class="sxs-lookup"><span data-stu-id="b144a-174">89</span></span>|<span data-ttu-id="b144a-175">Le cache MSIL a fait l’objet d’un accès.</span><span class="sxs-lookup"><span data-stu-id="b144a-175">The MSIL cache has been accessed.</span></span>|  
  
 <span data-ttu-id="b144a-176">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="b144a-176">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="b144a-177">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="b144a-177">Field name</span></span>|<span data-ttu-id="b144a-178">Type de données</span><span class="sxs-lookup"><span data-stu-id="b144a-178">Data type</span></span>|<span data-ttu-id="b144a-179">Description</span><span class="sxs-lookup"><span data-stu-id="b144a-179">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="b144a-180">ModuleID</span><span class="sxs-lookup"><span data-stu-id="b144a-180">ModuleID</span></span>|<span data-ttu-id="b144a-181">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="b144a-181">win:UInt16</span></span>|<span data-ttu-id="b144a-182">Identificateur du module</span><span class="sxs-lookup"><span data-stu-id="b144a-182">The module identifier.</span></span>|  
|<span data-ttu-id="b144a-183">StubMethodID</span><span class="sxs-lookup"><span data-stu-id="b144a-183">StubMethodID</span></span>|<span data-ttu-id="b144a-184">win:UInt64</span><span class="sxs-lookup"><span data-stu-id="b144a-184">win:UInt64</span></span>|<span data-ttu-id="b144a-185">Identificateur de la méthode stub</span><span class="sxs-lookup"><span data-stu-id="b144a-185">The stub method identifier.</span></span>|  
|<span data-ttu-id="b144a-186">ManagedInteropMethodToken</span><span class="sxs-lookup"><span data-stu-id="b144a-186">ManagedInteropMethodToken</span></span>|<span data-ttu-id="b144a-187">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="b144a-187">win:UInt32</span></span>|<span data-ttu-id="b144a-188">Jeton de la méthode d’interopérabilité managée</span><span class="sxs-lookup"><span data-stu-id="b144a-188">The token for the managed interop method.</span></span>|  
|<span data-ttu-id="b144a-189">ManagedInteropMethodNameSpace</span><span class="sxs-lookup"><span data-stu-id="b144a-189">ManagedInteropMethodNameSpace</span></span>|<span data-ttu-id="b144a-190">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="b144a-190">win:UnicodeString</span></span>|<span data-ttu-id="b144a-191">Espace de noms de la méthode d’interopérabilité managée</span><span class="sxs-lookup"><span data-stu-id="b144a-191">The namespace of the managed interop method.</span></span>|  
|<span data-ttu-id="b144a-192">ManagedInteropMethodName</span><span class="sxs-lookup"><span data-stu-id="b144a-192">ManagedInteropMethodName</span></span>|<span data-ttu-id="b144a-193">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="b144a-193">win:UnicodeString</span></span>|<span data-ttu-id="b144a-194">Nom de la méthode d’interopérabilité managée</span><span class="sxs-lookup"><span data-stu-id="b144a-194">The name of the managed interop method.</span></span>|  
|<span data-ttu-id="b144a-195">ManagedInteropMethodSignature</span><span class="sxs-lookup"><span data-stu-id="b144a-195">ManagedInteropMethodSignature</span></span>|<span data-ttu-id="b144a-196">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="b144a-196">win:UnicodeString</span></span>|<span data-ttu-id="b144a-197">Signature de la méthode d'interopérabilité managée</span><span class="sxs-lookup"><span data-stu-id="b144a-197">The signature of the managed interop method.</span></span>|  
|<span data-ttu-id="b144a-198">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="b144a-198">ClrInstanceID</span></span>|<span data-ttu-id="b144a-199">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="b144a-199">win:UInt16</span></span>|<span data-ttu-id="b144a-200">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="b144a-200">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="b144a-201">Retour au début</span><span class="sxs-lookup"><span data-stu-id="b144a-201">Back to top</span></span>](#top)  
  
## <a name="see-also"></a><span data-ttu-id="b144a-202">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b144a-202">See also</span></span>

- [<span data-ttu-id="b144a-203">Événements ETW du CLR</span><span class="sxs-lookup"><span data-stu-id="b144a-203">CLR ETW Events</span></span>](../../../docs/framework/performance/clr-etw-events.md)
