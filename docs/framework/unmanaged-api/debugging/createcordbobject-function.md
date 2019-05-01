---
title: Fonction CreateCordbObject
ms.date: 03/30/2017
api_name:
- CreateCoredbObject
api_location:
- mscordbi_macx86.dll
api_type:
- COM
f1_keywords:
- CreateCordbObject
helpviewer_keywords:
- remote debugging API [Silverlight]
- CreateCordbObject function
- Silverlight, remote debugging
ms.assetid: b259821d-4fa7-464d-85cf-304dfffc8089
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f546d7707c40f7f26a46177ae972a988e54e1e45
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61965826"
---
# <a name="createcordbobject-function"></a><span data-ttu-id="657bb-102">Fonction CreateCordbObject</span><span class="sxs-lookup"><span data-stu-id="657bb-102">CreateCordbObject Function</span></span>
<span data-ttu-id="657bb-103">Crée une interface de débogueur ([ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)) qui fournit des fonctionnalités d’instanciation d’une session de débogage managée sur un processus distant.</span><span class="sxs-lookup"><span data-stu-id="657bb-103">Creates a debugger interface ([ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)) that provides functionality for instantiating a managed debugging session on a remote process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="657bb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="657bb-104">Syntax</span></span>  
  
```  
HRESULT CordbCreateObject (  
       [in]  int         iDebuggerVersion,   
       [out] IUnknown**  ppCordb  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="657bb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="657bb-105">Parameters</span></span>  
 `iDebuggerVersion`  
 <span data-ttu-id="657bb-106">[in] Version de débogage du processus cible.</span><span class="sxs-lookup"><span data-stu-id="657bb-106">[in] Debugger version of the target process.</span></span> <span data-ttu-id="657bb-107">Ce paramètre doit être CorDebugVersion_2_0 pour le débogage distant.</span><span class="sxs-lookup"><span data-stu-id="657bb-107">This parameter must be CorDebugVersion_2_0 for remote debugging.</span></span>  
  
 `ppCordb`  
 <span data-ttu-id="657bb-108">[out] Pointeur vers un pointeur vers un objet qui sera être casté en un [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) interface et retourné.</span><span class="sxs-lookup"><span data-stu-id="657bb-108">[out] Pointer to a pointer to an object that will be cast to an [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) interface and returned.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="657bb-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="657bb-109">Return Value</span></span>  
 <span data-ttu-id="657bb-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="657bb-110">S_OK</span></span>  
 <span data-ttu-id="657bb-111">Le nombre de CLR dans le processus a été correctement déterminé, et les tableaux de handles et de chemin d’accès correspondants ont été correctement remplis.</span><span class="sxs-lookup"><span data-stu-id="657bb-111">The number of CLRs in the process was successfully determined, and the corresponding handle and path arrays were properly filled.</span></span>  
  
 <span data-ttu-id="657bb-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="657bb-112">E_INVALIDARG</span></span>  
 <span data-ttu-id="657bb-113">`ppCordb` est null ou `iDebuggerVersion` n'est pas CorDebugVersion_2_0.</span><span class="sxs-lookup"><span data-stu-id="657bb-113">`ppCordb` is null, or `iDebuggerVersion` is not CorDebugVersion_2_0.</span></span>  
  
 <span data-ttu-id="657bb-114">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="657bb-114">E_OUTOFMEMORY</span></span>  
 <span data-ttu-id="657bb-115">Impossible d'allouer suffisamment de mémoire pour `ppCordb`.</span><span class="sxs-lookup"><span data-stu-id="657bb-115">Unable to allocate enough memory for `ppCordb`</span></span>  
  
 <span data-ttu-id="657bb-116">E_FAIL (ou autres codes de retour E_)</span><span class="sxs-lookup"><span data-stu-id="657bb-116">E_FAIL (or other E_ return codes)</span></span>  
 <span data-ttu-id="657bb-117">Autres échecs.</span><span class="sxs-lookup"><span data-stu-id="657bb-117">Other failures.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="657bb-118">Notes</span><span class="sxs-lookup"><span data-stu-id="657bb-118">Remarks</span></span>  
 <span data-ttu-id="657bb-119">Le [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) interface retournée dans `ppCordb` est l’interface de débogage de niveau supérieur pour tous les services de débogage managés.</span><span class="sxs-lookup"><span data-stu-id="657bb-119">The [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) interface that is returned in `ppCordb` is the top-level debugging interface for all managed debugging services.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="657bb-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="657bb-120">Requirements</span></span>  
 <span data-ttu-id="657bb-121">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="657bb-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="657bb-122">**En-tête :** CoreClrRemoteDebuggingInterfaces.h</span><span class="sxs-lookup"><span data-stu-id="657bb-122">**Header:** CoreClrRemoteDebuggingInterfaces.h</span></span>  
  
 <span data-ttu-id="657bb-123">**Bibliothèque :** mscordbi_macx86.dll</span><span class="sxs-lookup"><span data-stu-id="657bb-123">**Library:** mscordbi_macx86.dll</span></span>  
  
 <span data-ttu-id="657bb-124">**Versions du .NET framework :** 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="657bb-124">**.NET Framework Versions:** 3.5 SP1</span></span>
