---
title: ICLRDataTarget2::FreeVirtual, méthode
ms.date: 03/30/2017
api_name:
- ICLRDataTarget2.FreeVirtual
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget2::FreeVirtual
helpviewer_keywords:
- ICLRDataTarget::FreeVirtual method [.NET Framework debugging]
- FreeVirtual method [.NET Framework debugging]
ms.assetid: 26fb69f8-1467-4711-bd24-cb117c63938f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b30bd3e97af8d222f629c5b4f9f318a9b6379e78
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61697951"
---
# <a name="iclrdatatarget2freevirtual-method"></a><span data-ttu-id="f2925-102">ICLRDataTarget2::FreeVirtual, méthode</span><span class="sxs-lookup"><span data-stu-id="f2925-102">ICLRDataTarget2::FreeVirtual Method</span></span>
<span data-ttu-id="f2925-103">Appelé par les services d’accès aux données du common language runtime (CLR) à la mémoire précédemment allouée dans l’espace d’adressage du processus cible.</span><span class="sxs-lookup"><span data-stu-id="f2925-103">Called by the common language runtime (CLR) data access services to free memory that was previously allocated in the address space of the target process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f2925-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2925-104">Syntax</span></span>  
  
```  
HRESULT FreeVirtual(  
    [in] CLRDATA_ADDRESS addr,  
    [in] ULONG32 size,  
    [in] ULONG32 typeFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f2925-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2925-105">Parameters</span></span>  
 `addr`  
 <span data-ttu-id="f2925-106">[in] Un `CLRDATA_ADDRESS` valeur qui spécifie l’adresse de départ de la mémoire à libérer.</span><span class="sxs-lookup"><span data-stu-id="f2925-106">[in] A `CLRDATA_ADDRESS` value that specifies the starting address of the memory to be freed.</span></span>  
  
 `size`  
 <span data-ttu-id="f2925-107">[in] La taille, en octets, de la mémoire à libérer.</span><span class="sxs-lookup"><span data-stu-id="f2925-107">[in] The size, in bytes, of the memory to be freed.</span></span>  
  
 `typeFlags`  
 <span data-ttu-id="f2925-108">[in] Indicateurs qui contrôlent la libération de mémoire.</span><span class="sxs-lookup"><span data-stu-id="f2925-108">[in] Flags that control the freeing of memory.</span></span> <span data-ttu-id="f2925-109">Consultez Win32 `VirtualFree` (fonction).</span><span class="sxs-lookup"><span data-stu-id="f2925-109">See the Win32 `VirtualFree` function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f2925-110">Notes</span><span class="sxs-lookup"><span data-stu-id="f2925-110">Remarks</span></span>  
 <span data-ttu-id="f2925-111">Le `FreeVirtual` méthode sert de wrapper logique pour Win32 `VirtualFree` (fonction).</span><span class="sxs-lookup"><span data-stu-id="f2925-111">The `FreeVirtual` method serves as a logical wrapper for the Win32 `VirtualFree` function.</span></span>  
  
 <span data-ttu-id="f2925-112">Cette méthode est implémentée par le writer de l'application de débogage.</span><span class="sxs-lookup"><span data-stu-id="f2925-112">This method is implemented by the writer of the debugging application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f2925-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2925-113">Requirements</span></span>  
 <span data-ttu-id="f2925-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f2925-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f2925-115">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="f2925-115">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="f2925-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f2925-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f2925-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f2925-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f2925-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2925-118">See also</span></span>

- [<span data-ttu-id="f2925-119">ICLRDataTarget2, interface</span><span class="sxs-lookup"><span data-stu-id="f2925-119">ICLRDataTarget2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-interface.md)
- [<span data-ttu-id="f2925-120">AllocVirtual, méthode</span><span class="sxs-lookup"><span data-stu-id="f2925-120">AllocVirtual Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-allocvirtual-method.md)
