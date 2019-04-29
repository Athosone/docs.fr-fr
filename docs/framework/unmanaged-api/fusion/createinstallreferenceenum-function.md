---
title: Fonction CreateInstallReferenceEnum
ms.date: 03/30/2017
api_name:
- CreateInstallReferenceEnum
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- DLLExport
f1_keywords:
- CreateInstallReference
helpviewer_keywords:
- CreateInstallReference function [.NET Framework fusion]
ms.assetid: 80dbbbf8-54fc-4894-b74a-0179d3201083
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d7820b33dcfacae5ede5235607e40d95940fc474
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61771902"
---
# <a name="createinstallreferenceenum-function"></a><span data-ttu-id="adc17-102">Fonction CreateInstallReferenceEnum</span><span class="sxs-lookup"><span data-stu-id="adc17-102">CreateInstallReferenceEnum Function</span></span>
<span data-ttu-id="adc17-103">Obtient un pointeur vers un [IInstallReferenceEnum](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceenum-interface.md) instance qui représente une liste de références d’une application à l’assembly spécifié.</span><span class="sxs-lookup"><span data-stu-id="adc17-103">Gets a pointer to an [IInstallReferenceEnum](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceenum-interface.md) instance that represents a list of an application's references to the specified assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="adc17-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="adc17-104">Syntax</span></span>  
  
```  
HRESULT CreateInstallReferenceEnum (  
    [out] IInstallReferenceEnum **ppRefEnum,  
    [in]  IAssemblyName         *pName,  
    [in]  DWORD                 dwFlags,  
    [in]  LPVOID                pvReserved  
 );  
```  
  
## <a name="parameters"></a><span data-ttu-id="adc17-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="adc17-105">Parameters</span></span>  
 `ppRefEnum`  
 <span data-ttu-id="adc17-106">[out] Retourné `IInstallReferenceEnum` pointeur.</span><span class="sxs-lookup"><span data-stu-id="adc17-106">[out] The returned `IInstallReferenceEnum` pointer.</span></span>  
  
 `pName`  
 <span data-ttu-id="adc17-107">[in] Le [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) qui identifie l’assembly pour lequel énumérer des références.</span><span class="sxs-lookup"><span data-stu-id="adc17-107">[in] The [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) that identifies the assembly for which to enumerate references.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="adc17-108">[in] Indicateurs qui influencent le comportement de l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="adc17-108">[in] Flags that influence the enumerator's behavior.</span></span>  
  
 `pvReserved`  
 <span data-ttu-id="adc17-109">[in] Réservé pour une extensibilité future.</span><span class="sxs-lookup"><span data-stu-id="adc17-109">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="adc17-110">`pvReserved` doit être une référence null.</span><span class="sxs-lookup"><span data-stu-id="adc17-110">`pvReserved` must be a null reference.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="adc17-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="adc17-111">Requirements</span></span>  
 <span data-ttu-id="adc17-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="adc17-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="adc17-113">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="adc17-113">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="adc17-114">**Bibliothèque :** Le fichier fusion.dll et Mscorwks.dll.</span><span class="sxs-lookup"><span data-stu-id="adc17-114">**Library:** Fusion.dll and Mscorwks.dll.</span></span> <span data-ttu-id="adc17-115">Utilisez le fichier Fusion.dll plutôt que Mscorwks.dll pour vous assurer que vous ciblez la version correcte du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="adc17-115">Use Fusion.dll instead of Mscorwks.dll to ensure that you target the correct version of the .NET Framework.</span></span>  
  
 <span data-ttu-id="adc17-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="adc17-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="adc17-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="adc17-117">See also</span></span>

- [<span data-ttu-id="adc17-118">IInstallReferenceEnum, interface</span><span class="sxs-lookup"><span data-stu-id="adc17-118">IInstallReferenceEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceenum-interface.md)
- [<span data-ttu-id="adc17-119">IAssemblyName, interface</span><span class="sxs-lookup"><span data-stu-id="adc17-119">IAssemblyName Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)
- [<span data-ttu-id="adc17-120">Fonctions statiques globales de fusion</span><span class="sxs-lookup"><span data-stu-id="adc17-120">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
