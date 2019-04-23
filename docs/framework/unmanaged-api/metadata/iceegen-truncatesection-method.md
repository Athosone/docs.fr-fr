---
title: ICeeGen::TruncateSection, méthode
ms.date: 03/30/2017
api_name:
- ICeeGen.TruncateSection
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::TruncateSection
helpviewer_keywords:
- TruncateSection method [.NET Framework metadata]
- ICeeGen::TruncateSection method [.NET Framework metadata]
ms.assetid: 0451d752-1e5c-4c9a-8bad-6cd35b7ba3df
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 1036d6080bf17eea288724c7980ce53dfa2121f7
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59116319"
---
# <a name="iceegentruncatesection-method"></a><span data-ttu-id="a99cc-102">ICeeGen::TruncateSection, méthode</span><span class="sxs-lookup"><span data-stu-id="a99cc-102">ICeeGen::TruncateSection Method</span></span>
<span data-ttu-id="a99cc-103">Tronque la section de code spécifié par la longueur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a99cc-103">Truncates the specified code section by the specified length.</span></span>  
  
 <span data-ttu-id="a99cc-104">Cette méthode est obsolète et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="a99cc-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a99cc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a99cc-105">Syntax</span></span>  
  
```  
HRESULT TruncateSection (  
    [in]  HCEESECTION     section,  
    [in]  ULONG           len  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a99cc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a99cc-106">Parameters</span></span>  
 `section`  
 <span data-ttu-id="a99cc-107">[in] La section à tronquer.</span><span class="sxs-lookup"><span data-stu-id="a99cc-107">[in] The section to truncate.</span></span>  
  
 `len`  
 <span data-ttu-id="a99cc-108">[in] La longueur, en octets, de laquelle tronquer la section.</span><span class="sxs-lookup"><span data-stu-id="a99cc-108">[in] The length, in bytes, by which to truncate the section.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a99cc-109">Notes</span><span class="sxs-lookup"><span data-stu-id="a99cc-109">Remarks</span></span>  
 <span data-ttu-id="a99cc-110">Appelez `TruncateSection` uniquement si vous avez des exigences de section spéciale qui ne sont pas gérées par d’autres méthodes.</span><span class="sxs-lookup"><span data-stu-id="a99cc-110">Call `TruncateSection` only if you have special section requirements that are not handled by other methods.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a99cc-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a99cc-111">Requirements</span></span>  
 <span data-ttu-id="a99cc-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a99cc-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a99cc-113">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="a99cc-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a99cc-114">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a99cc-114">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="a99cc-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a99cc-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a99cc-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a99cc-116">See also</span></span>

- [<span data-ttu-id="a99cc-117">ICeeGen, interface</span><span class="sxs-lookup"><span data-stu-id="a99cc-117">ICeeGen Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)
