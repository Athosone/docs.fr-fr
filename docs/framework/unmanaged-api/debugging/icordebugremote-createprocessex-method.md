---
title: ICorDebugRemote::CreateProcessEx, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugRemote.CreateProcessEx
api_location:
- CorDebug.dll
api_type:
- COM
f1_keywords:
- ICorDebugRemoteTarget::CreateProcessEx
helpviewer_keywords:
- CreateProcessEx method, ICorDebugRemote interface [.NET Framework debugging]
- ICorDebugRemote::CreateProcessEx method [.NET Framework debugging]
ms.assetid: 41af93c7-e448-4251-8d4d-413d38c635f2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a38812803127857281f9766fa3ed551971ec0330
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61782783"
---
# <a name="icordebugremotecreateprocessex-method"></a><span data-ttu-id="aa0e6-102">ICorDebugRemote::CreateProcessEx, méthode</span><span class="sxs-lookup"><span data-stu-id="aa0e6-102">ICorDebugRemote::CreateProcessEx Method</span></span>
<span data-ttu-id="aa0e6-103">Lance un processus sur un ordinateur distant sous le débogueur.</span><span class="sxs-lookup"><span data-stu-id="aa0e6-103">Launches a process on a remote machine under the debugger.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aa0e6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa0e6-104">Syntax</span></span>  
  
```  
HRESULT CreateProcessEx (  
    [in]  ICorDebugRemoteTarget*      pRemoteTarget,  
    [in]  LPCWSTR                     lpApplicationName,  
    [in]  LPWSTR                      lpCommandLine,  
    [in]  LPSECURITY_ATTRIBUTES       lpProcessAttributes,  
    [in]  LPSECURITY_ATTRIBUTES       lpThreadAttributes,  
    [in]  BOOL                        bInheritHandles,  
    [in]  DWORD                       dwCreationFlags,  
    [in]  PVOID                       lpEnvironment,  
    [in]  LPCWSTR                     lpCurrentDirectory,  
    [in]  LPSTARTUPINFOW              lpStartupInfo,  
    [in]  LPPROCESS_INFORMATION       lpProcessInformation,  
    [in]  CorDebugCreateProcessFlags  debuggingFlags,  
    [out] ICorDebugProcess**          ppProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="aa0e6-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aa0e6-105">Parameters</span></span>  
 `pRemoteTarget`  
 <span data-ttu-id="aa0e6-106">[in] Pointeur vers un [icordebugremotetarget, Interface](../../../../docs/framework/unmanaged-api/debugging/icordebugremotetarget-interface.md).</span><span class="sxs-lookup"><span data-stu-id="aa0e6-106">[in] Pointer to an [ICorDebugRemoteTarget Interface](../../../../docs/framework/unmanaged-api/debugging/icordebugremotetarget-interface.md).</span></span> <span data-ttu-id="aa0e6-107">Utilisé pour déterminer l’ordinateur distant sur lequel le processus sera lancé.</span><span class="sxs-lookup"><span data-stu-id="aa0e6-107">Used to determine the remote machine on which the process will be launched.</span></span>  
  
 `lpApplicationName`  
 <span data-ttu-id="aa0e6-108">[in] Pointeur vers une chaîne se terminant par null qui spécifie le module doit être exécuté par le processus lancé.</span><span class="sxs-lookup"><span data-stu-id="aa0e6-108">[in] Pointer to a null-terminated string that specifies the module to be executed by the launched process.</span></span> <span data-ttu-id="aa0e6-109">Le module est exécuté dans le contexte de sécurité du processus appelant.</span><span class="sxs-lookup"><span data-stu-id="aa0e6-109">The module is executed in the security context of the calling process.</span></span>  
  
 `lpCommandLine`  
 <span data-ttu-id="aa0e6-110">[in] Pointeur vers une chaîne se terminant par null qui spécifie la ligne de commande doit être exécuté par le processus lancé.</span><span class="sxs-lookup"><span data-stu-id="aa0e6-110">[in] Pointer to a null-terminated string that specifies the command line to be executed by the launched process.</span></span>  
  
 `lpProcessAttributes`  
 <span data-ttu-id="aa0e6-111">[in] Non utilisé pour le débogage distant.</span><span class="sxs-lookup"><span data-stu-id="aa0e6-111">[in] Unused for remote debugging.</span></span>  
  
 `lpThreadAttributes`  
 <span data-ttu-id="aa0e6-112">[in] Non utilisé pour le débogage distant.</span><span class="sxs-lookup"><span data-stu-id="aa0e6-112">[in] Unused for remote debugging.</span></span>  
  
 `bInheritHandles`  
 <span data-ttu-id="aa0e6-113">[in] Non utilisé pour le débogage distant.</span><span class="sxs-lookup"><span data-stu-id="aa0e6-113">[in] Unused for remote debugging.</span></span>  
  
 `dwCreationFlags`  
 <span data-ttu-id="aa0e6-114">[in] Non utilisé pour le débogage distant.</span><span class="sxs-lookup"><span data-stu-id="aa0e6-114">[in] Unused for remote debugging.</span></span>  
  
 `lpEnvironment`  
 <span data-ttu-id="aa0e6-115">[in] Pointeur vers un bloc d’environnement pour le nouveau processus.</span><span class="sxs-lookup"><span data-stu-id="aa0e6-115">[in] Pointer to an environment block for the new process.</span></span>  
  
 `lpCurrentDirectory`  
 <span data-ttu-id="aa0e6-116">[in] Pointeur vers une chaîne se terminant par null qui spécifie le chemin complet vers le répertoire actif pour le processus.</span><span class="sxs-lookup"><span data-stu-id="aa0e6-116">[in] Pointer to a null-terminated string that specifies the full path to the current directory for the process.</span></span> <span data-ttu-id="aa0e6-117">Si ce paramètre est null, le nouveau processus aura le même lecteur actuel et le répertoire en tant que le processus appelant.</span><span class="sxs-lookup"><span data-stu-id="aa0e6-117">If this parameter is null, the new process will have the same current drive and directory as the calling process.</span></span>  
  
 `lpStartupInfo`  
 <span data-ttu-id="aa0e6-118">[in] Non utilisé pour le débogage distant.</span><span class="sxs-lookup"><span data-stu-id="aa0e6-118">[in] Unused for remote debugging.</span></span>  
  
 `lpProcessInformation`  
 <span data-ttu-id="aa0e6-119">[in] Non utilisé pour le débogage distant.</span><span class="sxs-lookup"><span data-stu-id="aa0e6-119">[in] Unused for remote debugging.</span></span>  
  
 `debuggingFlags`  
 <span data-ttu-id="aa0e6-120">[in] Non utilisé pour le débogage distant.</span><span class="sxs-lookup"><span data-stu-id="aa0e6-120">[in] Unused for remote debugging.</span></span>  
  
 `ppProcess`  
 <span data-ttu-id="aa0e6-121">[out] Pointeur vers l’adresse d’un objet « ICorDebugProcess Interface » qui représente le processus.</span><span class="sxs-lookup"><span data-stu-id="aa0e6-121">[out] A pointer to the address of a"ICorDebugProcess Interface" object that represents the process.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="aa0e6-122">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="aa0e6-122">Return Value</span></span>  
 <span data-ttu-id="aa0e6-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="aa0e6-123">S_OK</span></span>  
 <span data-ttu-id="aa0e6-124">Lancé avec succès le processus sur l’ordinateur distant et retourné une « Interface ICorDebugProcess » pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="aa0e6-124">Successfully launched the process on the remote machine and returned an "ICorDebugProcess Interface" for debugging.</span></span>  
  
 <span data-ttu-id="aa0e6-125">E_FAIL (ou autres codes de retour E_)</span><span class="sxs-lookup"><span data-stu-id="aa0e6-125">E_FAIL (or other E_ return codes)</span></span>  
 <span data-ttu-id="aa0e6-126">Impossible de lancer le processus sur l’ordinateur distant et retourner une « ICorDebugProcess Interface » pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="aa0e6-126">Unable to launch the process on the remote machine and return an "ICorDebugProcess Interface" for debugging.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="aa0e6-127">Notes</span><span class="sxs-lookup"><span data-stu-id="aa0e6-127">Remarks</span></span>  
 <span data-ttu-id="aa0e6-128">Le débogage en mode mixte n’est pas pris en charge dans Silverlight.</span><span class="sxs-lookup"><span data-stu-id="aa0e6-128">Mixed-mode debugging is not supported in Silverlight.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="aa0e6-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa0e6-129">Requirements</span></span>  
 <span data-ttu-id="aa0e6-130">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="aa0e6-130">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aa0e6-131">**En-tête :** CorDebug.idl</span><span class="sxs-lookup"><span data-stu-id="aa0e6-131">**Header:** CorDebug.idl</span></span>  
  
 <span data-ttu-id="aa0e6-132">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="aa0e6-132">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="aa0e6-133">**Versions du .NET framework :** 4.5, 4, 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="aa0e6-133">**.NET Framework Versions:** 4.5, 4, 3.5 SP1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aa0e6-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa0e6-134">See also</span></span>

- [<span data-ttu-id="aa0e6-135">ICorDebugRemote, interface</span><span class="sxs-lookup"><span data-stu-id="aa0e6-135">ICorDebugRemote Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugremote-interface.md)
- [<span data-ttu-id="aa0e6-136">ICorDebug, interface</span><span class="sxs-lookup"><span data-stu-id="aa0e6-136">ICorDebug Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)

- [<span data-ttu-id="aa0e6-137">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="aa0e6-137">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
