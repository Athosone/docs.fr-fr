---
title: CorDebugUnmappedStop, énumération
ms.date: 03/30/2017
api_name:
- CorDebugUnmappedStop
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugUnmappedStop
helpviewer_keywords:
- CorDebugUnmappedStop enumeration [.NET Framework debugging]
ms.assetid: a684f7d7-d0c2-4690-b721-639e613f11f8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c1cea8adcd12ecb3078e4469e6b018ed49064e0b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61723314"
---
# <a name="cordebugunmappedstop-enumeration"></a><span data-ttu-id="a368d-102">CorDebugUnmappedStop, énumération</span><span class="sxs-lookup"><span data-stu-id="a368d-102">CorDebugUnmappedStop Enumeration</span></span>
<span data-ttu-id="a368d-103">Spécifie le type de code non mappé qui peut déclencher un arrêt dans l'exécution du code par l'exécution pas à pas.</span><span class="sxs-lookup"><span data-stu-id="a368d-103">Specifies the type of unmapped code that can trigger a halt in code execution by the stepper.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a368d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a368d-104">Syntax</span></span>  
  
```  
typedef enum CorDebugUnmappedStop {  
    STOP_NONE               = 0x0,  
    STOP_PROLOG             = 0x01,  
    STOP_EPILOG             = 0x02,  
    STOP_NO_MAPPING_INFO    = 0x04,  
    STOP_OTHER_UNMAPPED     = 0x08,  
    STOP_UNMANAGED          = 0x10,  
    STOP_ALL                = 0xffff,  
} CorDebugUnmappedStop;  
```  
  
## <a name="members"></a><span data-ttu-id="a368d-105">Membres</span><span class="sxs-lookup"><span data-stu-id="a368d-105">Members</span></span>  
  
|<span data-ttu-id="a368d-106">Membre</span><span class="sxs-lookup"><span data-stu-id="a368d-106">Member</span></span>|<span data-ttu-id="a368d-107">Description</span><span class="sxs-lookup"><span data-stu-id="a368d-107">Description</span></span>|  
|------------|-----------------|  
|`STOP_NONE`|<span data-ttu-id="a368d-108">N’arrêtez pas dans n’importe quel type de code non mappé.</span><span class="sxs-lookup"><span data-stu-id="a368d-108">Do not stop in any type of unmapped code.</span></span>|  
|`STOP_PROLOG`|<span data-ttu-id="a368d-109">Arrêter dans le code de prologue.</span><span class="sxs-lookup"><span data-stu-id="a368d-109">Stop in prolog code.</span></span>|  
|`STOP_EPILOG`|<span data-ttu-id="a368d-110">Arrêter dans le code d’épilogue.</span><span class="sxs-lookup"><span data-stu-id="a368d-110">Stop in epilog code.</span></span>|  
|`STOP_NO_MAPPING_INFO`|<span data-ttu-id="a368d-111">Arrêter dans le code qui ne possède aucune information de mappage.</span><span class="sxs-lookup"><span data-stu-id="a368d-111">Stop in code that has no mapping information.</span></span>|  
|`STOP_OTHER_UNMAPPED`|<span data-ttu-id="a368d-112">Arrêter dans le code non mappé qui ne tient pas dans le prologue, épilogue, aucune information de mappage ou catégorie non managé.</span><span class="sxs-lookup"><span data-stu-id="a368d-112">Stop in unmapped code that does not fit into the prolog, epilog, no-mapping-information, or unmanaged category.</span></span>|  
|`STOP_UNMANAGED`|<span data-ttu-id="a368d-113">Arrêter en code non managé.</span><span class="sxs-lookup"><span data-stu-id="a368d-113">Stop in unmanaged code.</span></span> <span data-ttu-id="a368d-114">Cette valeur est valide uniquement avec le débogage d’interopérabilité.</span><span class="sxs-lookup"><span data-stu-id="a368d-114">This value is valid only with interop debugging.</span></span>|  
|`STOP_ALL`|<span data-ttu-id="a368d-115">Arrêter dans tous les types de code non mappé.</span><span class="sxs-lookup"><span data-stu-id="a368d-115">Stop in all types of unmapped code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a368d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="a368d-116">Remarks</span></span>  
 <span data-ttu-id="a368d-117">Utilisez le [ICorDebugStepper::SetUnmappedStopMask](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-setunmappedstopmask-method.md) méthode pour définir les indicateurs qui spécifient le code non mappé dans lequel l’exécution pas à pas s’arrête.</span><span class="sxs-lookup"><span data-stu-id="a368d-117">Use the [ICorDebugStepper::SetUnmappedStopMask](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-setunmappedstopmask-method.md) method to set the flags that specify the unmapped code in which the stepper will stop.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a368d-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a368d-118">Requirements</span></span>  
 <span data-ttu-id="a368d-119">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a368d-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a368d-120">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a368d-120">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a368d-121">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a368d-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a368d-122">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a368d-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a368d-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a368d-123">See also</span></span>

- [<span data-ttu-id="a368d-124">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="a368d-124">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
