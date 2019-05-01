---
title: ICorDebugProcess::ReadMemory, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.ReadMemory
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::ReadMemory
helpviewer_keywords:
- ReadMemory method [.NET Framework debugging]
- ICorDebugProcess::ReadMemory method [.NET Framework debugging]
ms.assetid: 28e4b2f6-9589-445c-be24-24a3306795e7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 218279684304b766a9bf009f5891ac4910254a3c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61994381"
---
# <a name="icordebugprocessreadmemory-method"></a><span data-ttu-id="ba0a5-102">ICorDebugProcess::ReadMemory, méthode</span><span class="sxs-lookup"><span data-stu-id="ba0a5-102">ICorDebugProcess::ReadMemory Method</span></span>
<span data-ttu-id="ba0a5-103">Lit une zone spécifiée de mémoire pour ce processus.</span><span class="sxs-lookup"><span data-stu-id="ba0a5-103">Reads a specified area of memory for this process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ba0a5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba0a5-104">Syntax</span></span>  
  
```  
HRESULT ReadMemory(  
    [in]  CORDB_ADDRESS address,   
    [in]  DWORD size,  
    [out, size_is(size), length_is(size)] BYTE buffer[],  
    [out] SIZE_T *read);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ba0a5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba0a5-105">Parameters</span></span>  
 `address`  
 <span data-ttu-id="ba0a5-106">[in] Un `CORDB_ADDRESS` valeur qui spécifie l’adresse de base de la mémoire à lire.</span><span class="sxs-lookup"><span data-stu-id="ba0a5-106">[in] A `CORDB_ADDRESS` value that specifies the base address of the memory to be read.</span></span>  
  
 `size`  
 <span data-ttu-id="ba0a5-107">[in] Le nombre d’octets à lire à partir de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="ba0a5-107">[in] The number of bytes to be read from memory.</span></span>  
  
 `buffer`  
 <span data-ttu-id="ba0a5-108">[out] Une mémoire tampon qui reçoit le contenu de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="ba0a5-108">[out] A buffer that receives the contents of the memory.</span></span>  
  
 `read`  
 <span data-ttu-id="ba0a5-109">[out] Un pointeur vers le nombre d’octets transférés vers la mémoire tampon spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ba0a5-109">[out] A pointer to the number of bytes transferred into the specified buffer.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ba0a5-110">Notes</span><span class="sxs-lookup"><span data-stu-id="ba0a5-110">Remarks</span></span>  
 <span data-ttu-id="ba0a5-111">Le `ReadMemory` méthode est principalement destinée à être utilisée par le débogage d’interopérabilité pour inspecter les régions de mémoire qui sont utilisées par la partie non managée de l’élément débogué.</span><span class="sxs-lookup"><span data-stu-id="ba0a5-111">The `ReadMemory` method is primarily intended to be used by interop debugging to inspect memory regions that are being used by the unmanaged portion of the debuggee.</span></span> <span data-ttu-id="ba0a5-112">Cette méthode peut également être utilisée pour lire le code Microsoft intermediate language (MSIL) et le code natif compilé par JIT.</span><span class="sxs-lookup"><span data-stu-id="ba0a5-112">This method can also be used to read Microsoft intermediate language (MSIL) code and native JIT-compiled code.</span></span>  
  
 <span data-ttu-id="ba0a5-113">Les points d’arrêt gérés ne sont plus à partir des données qui sont retournées dans le `buffer` paramètre.</span><span class="sxs-lookup"><span data-stu-id="ba0a5-113">Any managed breakpoints will be removed from the data that is returned in the `buffer` parameter.</span></span> <span data-ttu-id="ba0a5-114">Aucun réglage n’est effectué pour les points d’arrêt natifs définis [ICorDebugProcess2::SetUnmanagedBreakpoint](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess2-setunmanagedbreakpoint-method.md).</span><span class="sxs-lookup"><span data-stu-id="ba0a5-114">No adjustments will be made for native breakpoints set by [ICorDebugProcess2::SetUnmanagedBreakpoint](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess2-setunmanagedbreakpoint-method.md).</span></span>  
  
 <span data-ttu-id="ba0a5-115">Aucune mise en cache de mémoire de processus n’est effectuée.</span><span class="sxs-lookup"><span data-stu-id="ba0a5-115">No caching of process memory is performed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ba0a5-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba0a5-116">Requirements</span></span>  
 <span data-ttu-id="ba0a5-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ba0a5-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ba0a5-118">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ba0a5-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ba0a5-119">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ba0a5-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ba0a5-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ba0a5-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
