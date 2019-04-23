---
title: ICeeGen::GetSectionBlock, méthode
ms.date: 03/30/2017
api_name:
- ICeeGen.GetSectionBlock
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::GetSectionBlock
helpviewer_keywords:
- GetSectionBlock method [.NET Framework metadata]
- ICeeGen::GetSectionBlock method [.NET Framework metadata]
ms.assetid: 05c78aaf-5bbd-497e-9ae2-55f4fae0c5fb
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7e600f29a9036bb28031bd7854bc8cbb34c4566a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59200647"
---
# <a name="iceegengetsectionblock-method"></a><span data-ttu-id="f8fdf-102">ICeeGen::GetSectionBlock, méthode</span><span class="sxs-lookup"><span data-stu-id="f8fdf-102">ICeeGen::GetSectionBlock Method</span></span>
<span data-ttu-id="f8fdf-103">Obtient un bloc de section de la base de code.</span><span class="sxs-lookup"><span data-stu-id="f8fdf-103">Gets a section block of the code base.</span></span>  
  
 <span data-ttu-id="f8fdf-104">Cette méthode est obsolète et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="f8fdf-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f8fdf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8fdf-105">Syntax</span></span>  
  
```  
HRESULT GetSectionBlock (  
    [in]  HCEESECTION    section,     
    [in]  ULONG          len,  
    [in]  ULONG          align     = 1,  
    [out] void           **ppBytes = 0  
);   
```  
  
## <a name="parameters"></a><span data-ttu-id="f8fdf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8fdf-106">Parameters</span></span>  
 `section`  
 <span data-ttu-id="f8fdf-107">[in] La section à partir de laquelle récupérer un bloc de la base de code.</span><span class="sxs-lookup"><span data-stu-id="f8fdf-107">[in] The section from which to retrieve a block of the code base.</span></span>  
  
 `len`  
 <span data-ttu-id="f8fdf-108">[in] La longueur du bloc à récupérer.</span><span class="sxs-lookup"><span data-stu-id="f8fdf-108">[in] The length of the block to be retrieved.</span></span>  
  
 `align`  
 <span data-ttu-id="f8fdf-109">[in] L’octet par rapport au début de la section, avec lequel aligner le premier octet du bloc.</span><span class="sxs-lookup"><span data-stu-id="f8fdf-109">[in] The byte, relative to the beginning of the section, with which to align the first byte of the block.</span></span> <span data-ttu-id="f8fdf-110">Il s’agit de la position du bloc dans la section.</span><span class="sxs-lookup"><span data-stu-id="f8fdf-110">This is the position of the block within the section.</span></span>  
  
 `ppBytes`  
 <span data-ttu-id="f8fdf-111">[out] Pointeur vers un emplacement qui reçoit l’adresse du bloc récupéré.</span><span class="sxs-lookup"><span data-stu-id="f8fdf-111">[out] A pointer to a location that receives the address of the retrieved block.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f8fdf-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f8fdf-112">Remarks</span></span>  
 <span data-ttu-id="f8fdf-113">Appelez `GetSectionBlock` uniquement si vous avez des exigences de section spéciale qui ne sont pas gérées par d’autres méthodes.</span><span class="sxs-lookup"><span data-stu-id="f8fdf-113">Call `GetSectionBlock` only if you have special section requirements that are not handled by other methods.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f8fdf-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8fdf-114">Requirements</span></span>  
 <span data-ttu-id="f8fdf-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f8fdf-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f8fdf-116">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="f8fdf-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f8fdf-117">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f8fdf-117">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="f8fdf-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f8fdf-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f8fdf-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8fdf-119">See also</span></span>

- [<span data-ttu-id="f8fdf-120">ICeeGen, interface</span><span class="sxs-lookup"><span data-stu-id="f8fdf-120">ICeeGen Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)
