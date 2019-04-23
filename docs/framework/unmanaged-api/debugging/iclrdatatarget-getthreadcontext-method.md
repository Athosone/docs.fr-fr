---
title: ICLRDataTarget::GetThreadContext, méthode
ms.date: 03/30/2017
api_name:
- ICLRDataTarget.GetThreadContext
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget::GetThreadContext
helpviewer_keywords:
- ICLRDataTarget::GetThreadContext method [.NET Framework debugging]
- GetThreadContext method, ICLRDataTarget interface [.NET Framework debugging]
ms.assetid: b9d8c3b5-3a2e-4225-95d4-dd052c4532c3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 88d563918709a6cf31d9c14a52bbd461ae004420
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59116153"
---
# <a name="iclrdatatargetgetthreadcontext-method"></a><span data-ttu-id="91b20-102">ICLRDataTarget::GetThreadContext, méthode</span><span class="sxs-lookup"><span data-stu-id="91b20-102">ICLRDataTarget::GetThreadContext Method</span></span>
<span data-ttu-id="91b20-103">Obtient le contexte d’exécution actuel pour le thread donné dans le processus cible.</span><span class="sxs-lookup"><span data-stu-id="91b20-103">Gets the current execution context for the given thread in the target process.</span></span> <span data-ttu-id="91b20-104">Cette méthode est appelée par les services d’accès de données common language runtime.</span><span class="sxs-lookup"><span data-stu-id="91b20-104">This method is called by the common language runtime data access services.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="91b20-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91b20-105">Syntax</span></span>  
  
```  
HRESULT GetThreadContext (  
    [in] ULONG32            threadID,  
    [in] ULONG32            contextFlags,  
    [in] ULONG32            contextSize,  
    [out, size_is(contextSize)]   
        BYTE                *context  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="91b20-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91b20-106">Parameters</span></span>  
 `threadID`  
 <span data-ttu-id="91b20-107">[in] L’identificateur de système d’exploitation d’un thread dans le processus cible.</span><span class="sxs-lookup"><span data-stu-id="91b20-107">[in] The operating system identifier of a thread in the target process.</span></span>  
  
 `contextFlags`  
 <span data-ttu-id="91b20-108">[in] Indicateurs qui spécifient quelles parties du contexte à retourner.</span><span class="sxs-lookup"><span data-stu-id="91b20-108">[in] Flags that specify which parts of the context to return.</span></span> <span data-ttu-id="91b20-109">L’implémentation retourne au moins ces parties du contexte.</span><span class="sxs-lookup"><span data-stu-id="91b20-109">The implementation will return at least these parts of the context.</span></span>  
  
 `contextSize`  
 <span data-ttu-id="91b20-110">[in] La taille du contexte.</span><span class="sxs-lookup"><span data-stu-id="91b20-110">[in] The size of the context.</span></span>  
  
 `context`  
 <span data-ttu-id="91b20-111">[out] Pointeur vers une mémoire tampon dans laquelle placer le contexte.</span><span class="sxs-lookup"><span data-stu-id="91b20-111">[out] Pointer to a buffer in which to place the context.</span></span>  
  
 <span data-ttu-id="91b20-112">Les données dans le `context` mémoire tampon doit être au format Win32 `CONTEXT` structure.</span><span class="sxs-lookup"><span data-stu-id="91b20-112">The data in the `context` buffer must be in the format of the Win32 `CONTEXT` structure.</span></span> <span data-ttu-id="91b20-113">Le contexte spécifie des données de Registre spécifiques au processeur, la définition de Win32 `CONTEXT` structure varie selon l’architecture du processeur.</span><span class="sxs-lookup"><span data-stu-id="91b20-113">The context specifies processor-specific register data, so the definition of the Win32 `CONTEXT` structure depends on the processor's architecture.</span></span> <span data-ttu-id="91b20-114">Consultez le fichier d’en-tête WinNT.h pour la définition de Win32 `CONTEXT` structure.</span><span class="sxs-lookup"><span data-stu-id="91b20-114">Refer to the WinNT.h header file for the definition of the Win32 `CONTEXT` structure.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="91b20-115">Notes</span><span class="sxs-lookup"><span data-stu-id="91b20-115">Remarks</span></span>  
 <span data-ttu-id="91b20-116">Cette méthode est implémentée par le writer de l'application de débogage.</span><span class="sxs-lookup"><span data-stu-id="91b20-116">This method is implemented by the writer of the debugging application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="91b20-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91b20-117">Requirements</span></span>  
 <span data-ttu-id="91b20-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="91b20-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="91b20-119">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="91b20-119">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="91b20-120">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="91b20-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="91b20-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="91b20-121">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="91b20-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91b20-122">See also</span></span>

- [<span data-ttu-id="91b20-123">ICLRDataTarget, interface</span><span class="sxs-lookup"><span data-stu-id="91b20-123">ICLRDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md)
