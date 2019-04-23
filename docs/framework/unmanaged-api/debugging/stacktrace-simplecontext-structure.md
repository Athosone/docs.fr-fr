---
title: StackTrace_SimpleContext
ms.date: 03/30/2017
api_name:
- StackTrace_SimpleContext
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- SimpleContext
helpviewer_keywords:
- SimpleContext structure [.NET Framework debugging]
- StackTrace_SimpleContext structure [.NET Framework debugging]
ms.assetid: d4cef11f-a8ca-49bc-a1b8-6631f9e28f3e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b0625dc72d44485dbb69b42cba5387085d1862bb
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59210423"
---
# <a name="stacktracesimplecontext-structure"></a><span data-ttu-id="c0bb3-102">StackTrace_SimpleContext</span><span class="sxs-lookup"><span data-stu-id="c0bb3-102">StackTrace_SimpleContext Structure</span></span>
<span data-ttu-id="c0bb3-103">Fournit un contexte simple qui peut être utilisé à la place d'une structure `CONTEXT` complète.</span><span class="sxs-lookup"><span data-stu-id="c0bb3-103">Provides a simple context that can be used in place of a full `CONTEXT` structure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c0bb3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0bb3-104">Syntax</span></span>  
  
```  
struct StackTrace_SimpleContext  
{  
    ULONG64 StackOffset;       // ESP on x86  
    ULONG64 FrameOffset;       // EBP on x86  
    ULONG64 InstructionOffset; // EIP on x86  
};  
```  
  
## <a name="members"></a><span data-ttu-id="c0bb3-105">Membres</span><span class="sxs-lookup"><span data-stu-id="c0bb3-105">Members</span></span>  
  
|<span data-ttu-id="c0bb3-106">Membre</span><span class="sxs-lookup"><span data-stu-id="c0bb3-106">Member</span></span>|<span data-ttu-id="c0bb3-107">Description</span><span class="sxs-lookup"><span data-stu-id="c0bb3-107">Description</span></span>|  
|------------|-----------------|  
|`StackOffset`|<span data-ttu-id="c0bb3-108">Le pointeur de pile ou le pointeur de pile d’entrée (ESP) sur x86 plateformes.</span><span class="sxs-lookup"><span data-stu-id="c0bb3-108">The stack pointer, or the enter stack pointer (ESP) on x86 platforms.</span></span>|  
|`FrameOffset`|<span data-ttu-id="c0bb3-109">Le décalage de trame ou EBP sur x86 les plateformes.</span><span class="sxs-lookup"><span data-stu-id="c0bb3-109">The frame offset, or the EBP register on x86 platforms.</span></span>|  
|`InstructionOffset`|<span data-ttu-id="c0bb3-110">Le pointeur d’instruction ou le pointeur d’instruction entrée (EIP) sur x86 plateformes.</span><span class="sxs-lookup"><span data-stu-id="c0bb3-110">The instruction pointer, or the enter instruction pointer (EIP) on x86 platforms.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c0bb3-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c0bb3-111">Remarks</span></span>  
 <span data-ttu-id="c0bb3-112">Étant donné que les fonctions de trace de pile doivent généralement retourner uniquement l’adresse offset de frame et adresse de la pile, vous pouvez éventuellement utiliser le `SimpleContext` structure au lieu d’un grand `CONTEXT` structure.</span><span class="sxs-lookup"><span data-stu-id="c0bb3-112">Because stack trace functions typically need to return only the address, frame offset, and stack address, you can optionally use the `SimpleContext` structure instead of a large `CONTEXT` structure.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c0bb3-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0bb3-113">Requirements</span></span>  
 <span data-ttu-id="c0bb3-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c0bb3-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c0bb3-115">**En-tête :** SOS_Stacktrace.h</span><span class="sxs-lookup"><span data-stu-id="c0bb3-115">**Header:** SOS_Stacktrace.h</span></span>  
  
 <span data-ttu-id="c0bb3-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c0bb3-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c0bb3-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0bb3-117">See also</span></span>

- [<span data-ttu-id="c0bb3-118">Structures de débogage</span><span class="sxs-lookup"><span data-stu-id="c0bb3-118">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
- [<span data-ttu-id="c0bb3-119">Débogage</span><span class="sxs-lookup"><span data-stu-id="c0bb3-119">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
