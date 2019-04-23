---
title: ICorProfilerInfo::GetAssemblyInfo, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetAssemblyInfo
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- GetAssemblyInfo Method
helpviewer_keywords:
- GetAssemblyInfo method [.NET Framework profiling]
- ICorProfilerInfo::GetAssemblyInfo method [.NET Framework profiling]
ms.assetid: 7a3c97c3-1e31-47b1-bf23-386785c509c4
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ad4ebe4e1255ce13974063eef3d0a4feeb5dd92b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59083052"
---
# <a name="icorprofilerinfogetassemblyinfo-method"></a><span data-ttu-id="7a413-102">ICorProfilerInfo::GetAssemblyInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="7a413-102">ICorProfilerInfo::GetAssemblyInfo Method</span></span>
<span data-ttu-id="7a413-103">Accepte un ID d'assembly et retourne le nom de l'assembly et l'ID de son module de manifeste.</span><span class="sxs-lookup"><span data-stu-id="7a413-103">Accepts an assembly ID, and returns the assembly's name and the ID of its manifest module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7a413-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a413-104">Syntax</span></span>  
  
```  
HRESULT GetAssemblyInfo(  
    [in]  AssemblyID  assemblyId,  
    [in]  ULONG       cchName,  
    [out] ULONG       *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]  
          WCHAR       szName[] ,  
    [out] AppDomainID *pAppDomainId,  
    [out] ModuleID    *pModuleId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7a413-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a413-105">Parameters</span></span>  
 `assemblyId`  
 <span data-ttu-id="7a413-106">[in] Identificateur de l'assembly.</span><span class="sxs-lookup"><span data-stu-id="7a413-106">[in] The identifier of the assembly.</span></span>  
  
 `cchName`  
 <span data-ttu-id="7a413-107">[in] Longueur, en caractères, de `szName`.</span><span class="sxs-lookup"><span data-stu-id="7a413-107">[in] The length, in characters, of `szName`.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="7a413-108">[out] Pointeur vers la longueur totale en caractères du nom de l'assembly.</span><span class="sxs-lookup"><span data-stu-id="7a413-108">[out] A pointer to the total character length of the assembly's name.</span></span>  
  
 `szName`  
 <span data-ttu-id="7a413-109">[out] Mémoire tampon de caractères larges fournie par l'appelant.</span><span class="sxs-lookup"><span data-stu-id="7a413-109">[out] A caller-provided wide character buffer.</span></span> <span data-ttu-id="7a413-110">Suite au retour de la méthode, celle-ci contient le nom de l'assembly.</span><span class="sxs-lookup"><span data-stu-id="7a413-110">When the function returns, it will contain the assembly's name.</span></span>  
  
 `pAppDomainId`  
 <span data-ttu-id="7a413-111">[out] Pointeur vers l'ID du domaine d'application qui contient l'assembly.</span><span class="sxs-lookup"><span data-stu-id="7a413-111">[out] A pointer to the ID of the application domain that contains the assembly.</span></span>  
  
 `pModuleId`  
 <span data-ttu-id="7a413-112">[out] Pointeur vers l'ID du module du manifeste de l'assembly.</span><span class="sxs-lookup"><span data-stu-id="7a413-112">[out] A pointer to the ID of the assembly's manifest module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7a413-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7a413-113">Remarks</span></span>  
 <span data-ttu-id="7a413-114">Suite au retour de cette méthode, vous devez vérifier que la mémoire tampon `szName` est suffisamment grande pour contenir le nom complet de l'assembly.</span><span class="sxs-lookup"><span data-stu-id="7a413-114">After this method returns, you must verify that the `szName` buffer was large enough to contain the full name of the assembly.</span></span> <span data-ttu-id="7a413-115">Pour ce faire, comparez la valeur vers laquelle `pcchName` pointe à celle du paramètre `cchName`.</span><span class="sxs-lookup"><span data-stu-id="7a413-115">To do this, compare the value that `pcchName` points to with the value of the `cchName` parameter.</span></span> <span data-ttu-id="7a413-116">Si `pcchName` pointe vers une valeur supérieure à `cchName`, allouez une mémoire tampon `szName` plus grande, mettez à jour `cchName` pour refléter la nouvelle taille et rappelez `GetAssemblyInfo`.</span><span class="sxs-lookup"><span data-stu-id="7a413-116">If `pcchName` points to a value that is larger than `cchName`, allocate a larger `szName` buffer, update `cchName` with the new, larger size, and call `GetAssemblyInfo` again.</span></span>  
  
 <span data-ttu-id="7a413-117">Vous pouvez également commencer par appeler `GetAssemblyInfo` avec un tampon `szName` de longueur nulle pour obtenir la taille correcte du tampon.</span><span class="sxs-lookup"><span data-stu-id="7a413-117">Alternatively, you can first call `GetAssemblyInfo` with a zero-length `szName` buffer to obtain the correct buffer size.</span></span> <span data-ttu-id="7a413-118">Vous pouvez ensuite ajuster la taille de la mémoire tampon en fonction de la valeur retournée dans `pcchName` et rappeler `GetAssemblyInfo`.</span><span class="sxs-lookup"><span data-stu-id="7a413-118">You can then adjust the buffer size based on the value returned in `pcchName` and call `GetAssemblyInfo` again.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7a413-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a413-119">Requirements</span></span>  
 <span data-ttu-id="7a413-120">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7a413-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7a413-121">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="7a413-121">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="7a413-122">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7a413-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7a413-123">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7a413-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7a413-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a413-124">See also</span></span>

- [<span data-ttu-id="7a413-125">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="7a413-125">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
- [<span data-ttu-id="7a413-126">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="7a413-126">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [<span data-ttu-id="7a413-127">Profilage</span><span class="sxs-lookup"><span data-stu-id="7a413-127">Profiling</span></span>](../../../../docs/framework/unmanaged-api/profiling/index.md)
