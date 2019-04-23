---
title: COR_DEBUG_IL_TO_NATIVE_MAP, structure
ms.date: 03/30/2017
api_name:
- COR_DEBUG_IL_TO_NATIVE_MAP
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_DEBUG_IL_TO_NATIVE_MAP
helpviewer_keywords:
- COR_DEBUG_IL_TO_NATIVE_MAP structure [.NET Framework debugging]
ms.assetid: 06f3b504-085f-4142-934a-25381fe23d4c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 03ce77dd7407db8289abfefba13d71a9af053e10
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59142049"
---
# <a name="cordebugiltonativemap-structure"></a><span data-ttu-id="b07da-102">COR_DEBUG_IL_TO_NATIVE_MAP, structure</span><span class="sxs-lookup"><span data-stu-id="b07da-102">COR_DEBUG_IL_TO_NATIVE_MAP Structure</span></span>
<span data-ttu-id="b07da-103">Contient les décalages qui sont utilisés pour mapper du code MSIL (Microsoft Intermediate Language) à du code natif.</span><span class="sxs-lookup"><span data-stu-id="b07da-103">Contains the offsets that are used to map Microsoft intermediate language (MSIL) code to native code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b07da-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b07da-104">Syntax</span></span>  
  
```  
typedef struct COR_DEBUG_IL_TO_NATIVE_MAP {  
    ULONG32  ilOffset;  
    ULONG32  nativeStartOffset;  
    ULONG32  nativeEndOffset;  
} COR_DEBUG_IL_TO_NATIVE_MAP;  
```  
  
## <a name="members"></a><span data-ttu-id="b07da-105">Membres</span><span class="sxs-lookup"><span data-stu-id="b07da-105">Members</span></span>  
  
|<span data-ttu-id="b07da-106">Membre</span><span class="sxs-lookup"><span data-stu-id="b07da-106">Member</span></span>|<span data-ttu-id="b07da-107">Description</span><span class="sxs-lookup"><span data-stu-id="b07da-107">Description</span></span>|  
|------------|-----------------|  
|`ilOffset`|<span data-ttu-id="b07da-108">Le décalage du code MSIL.</span><span class="sxs-lookup"><span data-stu-id="b07da-108">The offset of the MSIL code.</span></span>|  
|`nativeStartOffset`|<span data-ttu-id="b07da-109">Le décalage du début du code natif.</span><span class="sxs-lookup"><span data-stu-id="b07da-109">The offset of the start of the native code.</span></span>|  
|`nativeEndOffset`|<span data-ttu-id="b07da-110">Le décalage de la fin du code natif.</span><span class="sxs-lookup"><span data-stu-id="b07da-110">The offset of the end of the native code.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b07da-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b07da-111">Requirements</span></span>  
 <span data-ttu-id="b07da-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b07da-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b07da-113">**En-tête :** CorProf.idl, CorDebug.idl</span><span class="sxs-lookup"><span data-stu-id="b07da-113">**Header:** CorProf.idl, CorDebug.idl</span></span>  
  
 <span data-ttu-id="b07da-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b07da-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b07da-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b07da-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b07da-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b07da-116">See also</span></span>

- [<span data-ttu-id="b07da-117">GetILToNativeMapping, méthode</span><span class="sxs-lookup"><span data-stu-id="b07da-117">GetILToNativeMapping Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-getiltonativemapping-method.md)
- [<span data-ttu-id="b07da-118">GetILToNativeMapping, méthode</span><span class="sxs-lookup"><span data-stu-id="b07da-118">GetILToNativeMapping Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcode-getiltonativemapping-method.md)
- [<span data-ttu-id="b07da-119">Structures de débogage</span><span class="sxs-lookup"><span data-stu-id="b07da-119">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
- [<span data-ttu-id="b07da-120">Débogage</span><span class="sxs-lookup"><span data-stu-id="b07da-120">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
