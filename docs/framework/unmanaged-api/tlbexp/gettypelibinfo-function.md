---
title: Fonction GetTypeLibInfo
ms.date: 03/30/2017
api_name:
- GetTypeLibInfo
api_location:
- TlbRef.dll
api_type:
- DLLExport
f1_keywords:
- GetTypeLibInfo
helpviewer_keywords:
- GetTypeLibInfo function [.NET Framework]
ms.assetid: a1c4d165-9bdc-4ca8-940e-292d4ffcc338
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d12cbb66464baba4ee706ccb076764fbf025fc5f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61786176"
---
# <a name="gettypelibinfo-function"></a><span data-ttu-id="7c6e0-102">Fonction GetTypeLibInfo</span><span class="sxs-lookup"><span data-stu-id="7c6e0-102">GetTypeLibInfo Function</span></span>
<span data-ttu-id="7c6e0-103">Retourne des informations sur la bibliothèque de types spécifiée en examinant sa [TLIBATTR](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/ns-oaidl-tagtlibattr) structure.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-103">Returns information about the specified type library by examining its [TLIBATTR](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/ns-oaidl-tagtlibattr) structure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7c6e0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c6e0-104">Syntax</span></span>  
  
```  
HRESULT GetTypeLibInfo(  
    [in]   LPWSTR     szFile,  
    [out]  GUID      *pTypeLibID,  
    [out]  LCID      *pTypeLibLCID,  
    [out]  SYSKIND   *pTypeLibPlatform,  
    [out]  USHORT    *pTypeLibMajorVer,  
    [out]  USHORT    *pTypeLibMinorVer  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7c6e0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c6e0-105">Parameters</span></span>  
 `szFile`  
 <span data-ttu-id="7c6e0-106">[in] Le nom de fichier de la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-106">[in] The file name of the type library.</span></span>  
  
 `pTypeLibID`  
 <span data-ttu-id="7c6e0-107">[out] Le GUID de la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-107">[out] The GUID of the type library.</span></span>  
  
 `pTypeLibLCID`  
 <span data-ttu-id="7c6e0-108">[out] ID de localisation de la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-108">[out] The localization ID of the type library.</span></span>  
  
 `pTypeLibPlatform`  
 <span data-ttu-id="7c6e0-109">[out] Un [SYSKIND](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/ne-oaidl-tagsyskind) indicateur qui identifie le système d’exploitation cible pour la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-109">[out] A [SYSKIND](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/ne-oaidl-tagsyskind) flag that identifies the target operating system for the type library.</span></span> <span data-ttu-id="7c6e0-110">Les valeurs courantes sont SYS_WIN32 et SYS_WIN64.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-110">Common values are SYS_WIN32 and SYS_WIN64.</span></span>  
  
 `pTypeLibMajorVer`  
 <span data-ttu-id="7c6e0-111">[out] Numéro de version principale de la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-111">[out] The major version number of the type library.</span></span> <span data-ttu-id="7c6e0-112">Par exemple, pour la version *x.y*, le numéro de version majeure est *x*.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-112">For example, for version *x.y*, the major version number is *x*.</span></span>  
  
 `pTypeLibMinorVer`  
 <span data-ttu-id="7c6e0-113">[out] Numéro de version secondaire de la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-113">[out] The minor version number of the type library.</span></span> <span data-ttu-id="7c6e0-114">Par exemple, pour la version *x.y*, le numéro de version mineure est *y*.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-114">For example, for version *x.y*, the minor version number is *y*.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7c6e0-115">Notes</span><span class="sxs-lookup"><span data-stu-id="7c6e0-115">Remarks</span></span>  
 <span data-ttu-id="7c6e0-116">Le `GetTypeLibInfo` fonction est appelée par le [Tlbexp.exe (exportateur)](../../../../docs/framework/tools/tlbexp-exe-type-library-exporter.md).</span><span class="sxs-lookup"><span data-stu-id="7c6e0-116">The `GetTypeLibInfo` function is called by the [Tlbexp.exe (Type Library Exporter)](../../../../docs/framework/tools/tlbexp-exe-type-library-exporter.md).</span></span> <span data-ttu-id="7c6e0-117">Cet outil génère une bibliothèque de types décrivant les types dans un assembly du common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="7c6e0-117">This tool generates a type library that describes the types in a common language runtime (CLR) assembly.</span></span>  
  
 <span data-ttu-id="7c6e0-118">Si un paramètre est null, la fonction retourne un `HRESULT` de `E_POINTER`.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-118">If any parameter is null, the function returns an `HRESULT` of `E_POINTER`.</span></span> <span data-ttu-id="7c6e0-119">Sinon, il retourne `S_OK`.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-119">Otherwise, it returns `S_OK`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7c6e0-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c6e0-120">Requirements</span></span>  
 <span data-ttu-id="7c6e0-121">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7c6e0-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7c6e0-122">**En-tête :** TlbRef.h</span><span class="sxs-lookup"><span data-stu-id="7c6e0-122">**Header:** TlbRef.h</span></span>  
  
 <span data-ttu-id="7c6e0-123">**Bibliothèque :** TlbRef.lib</span><span class="sxs-lookup"><span data-stu-id="7c6e0-123">**Library:** TlbRef.lib</span></span>  
  
 <span data-ttu-id="7c6e0-124">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7c6e0-124">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7c6e0-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c6e0-125">See also</span></span>

- [<span data-ttu-id="7c6e0-126">Fonctions d’assistance Tlbexp</span><span class="sxs-lookup"><span data-stu-id="7c6e0-126">Tlbexp Helper Functions</span></span>](../../../../docs/framework/unmanaged-api/tlbexp/index.md)
- [<span data-ttu-id="7c6e0-127">LoadTypeLibEx de le dont (fonction)</span><span class="sxs-lookup"><span data-stu-id="7c6e0-127">LoadTypeLibEx Function</span></span>](https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-loadtypelibex)
