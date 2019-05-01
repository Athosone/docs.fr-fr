---
title: Icordebugmergedassemblyrecord::GetPublicKey, méthode
ms.date: 03/30/2017
ms.assetid: 6f4e78ba-082b-489d-8b58-4c35fbcc7a5b
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 610e46d5cb550a266c5558c49239d1818c1e85de
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61988115"
---
# <a name="icordebugmergedassemblyrecordgetpublickey-method"></a><span data-ttu-id="1993e-102">Icordebugmergedassemblyrecord::GetPublicKey, méthode</span><span class="sxs-lookup"><span data-stu-id="1993e-102">ICorDebugMergedAssemblyRecord::GetPublicKey Method</span></span>
<span data-ttu-id="1993e-103">Obtient la clé publique de l'assembly.</span><span class="sxs-lookup"><span data-stu-id="1993e-103">Gets the assembly's public key.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1993e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1993e-104">Syntax</span></span>  
  
```  
HRESULT GetPublicKey(  
   [in] ULONG32 cbPublicKey,   
   [out] ULONG32 *pcbPublicKey,   
   [out, size_is(cbPublicKey), length_is(*pcbPublicKey)] BYTE pbPublicKey[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1993e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1993e-105">Parameters</span></span>  
 `cbPublicKey`  
 <span data-ttu-id="1993e-106">[in] Nombre maximal d'octets dans le tableau `pbPublicKey`.</span><span class="sxs-lookup"><span data-stu-id="1993e-106">[in] The maximum number of bytes in the `pbPublicKey` array.</span></span>  
  
 `pcbPublicKey`  
 <span data-ttu-id="1993e-107">[out] Pointeur vers le nombre réel d'octets écrits dans le tableau `pbPublicKey`.</span><span class="sxs-lookup"><span data-stu-id="1993e-107">[out] A pointer to the actual number of bytes written to the `pbPublicKey` array.</span></span>  
  
 `pbPublicKey`  
 <span data-ttu-id="1993e-108">[in] Pointeur vers un tableau d'octets contenant la clé publique de l'assembly.</span><span class="sxs-lookup"><span data-stu-id="1993e-108">[out] A pointer to a byte array that contains the assembly's public key.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1993e-109">Notes</span><span class="sxs-lookup"><span data-stu-id="1993e-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="1993e-110">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="1993e-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1993e-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1993e-111">Requirements</span></span>  
 <span data-ttu-id="1993e-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1993e-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1993e-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1993e-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1993e-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1993e-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1993e-115">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1993e-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1993e-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1993e-116">See also</span></span>

- [<span data-ttu-id="1993e-117">ICorDebugMergedAssemblyRecord, interface</span><span class="sxs-lookup"><span data-stu-id="1993e-117">ICorDebugMergedAssemblyRecord Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmergedassemblyrecord-interface.md)
- [<span data-ttu-id="1993e-118">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="1993e-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
