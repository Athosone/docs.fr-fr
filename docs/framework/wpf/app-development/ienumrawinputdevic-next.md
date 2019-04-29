---
title: IEnumRAWINPUTDEVIC:Next
ms.date: 03/30/2017
helpviewer_keywords:
- Next method [WPF]
ms.assetid: 3698b44d-510e-4d18-b32b-85f17188ee26
ms.openlocfilehash: 05867af48b64cd1898b13fa055859c8cc0367c8c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61949576"
---
# <a name="ienumrawinputdevicnext"></a><span data-ttu-id="12488-102">IEnumRAWINPUTDEVIC:Next</span><span class="sxs-lookup"><span data-stu-id="12488-102">IEnumRAWINPUTDEVIC:Next</span></span>
<span data-ttu-id="12488-103">Énumère les prochaines `celt` [RAWINPUTDEVICE](/windows/desktop/api/winuser/ns-winuser-rawinputdevice) structures dans la liste de l’énumérateur, en les retournant dans `rgelt` , ainsi que le nombre réel d’éléments énumérés dans `pceltFetched`.</span><span class="sxs-lookup"><span data-stu-id="12488-103">Enumerates the next `celt` [RAWINPUTDEVICE](/windows/desktop/api/winuser/ns-winuser-rawinputdevice) structures in the enumerator's list, returning them in `rgelt` along with the actual number of enumerated elements in `pceltFetched`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="12488-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12488-104">Syntax</span></span>  
  
```  
HRESULT Next(  
      [in] ULONG celt,  
      [out, size_is(celt), length_is(*pceltFetched)] RAWINPUTDEVICE *rgelt,  
      [out] ULONG *pceltFetched);  
```  
  
## <a name="parameters"></a><span data-ttu-id="12488-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12488-105">Parameters</span></span>  
 `celt`  
  
 <span data-ttu-id="12488-106">[in] Nombre de [RAWINPUTDEVICE](/windows/desktop/api/winuser/ns-winuser-rawinputdevice) retournés dans des structures `rgelt`.</span><span class="sxs-lookup"><span data-stu-id="12488-106">[in] Number of [RAWINPUTDEVICE](/windows/desktop/api/winuser/ns-winuser-rawinputdevice) structures returned in `rgelt`.</span></span>  
  
 `rgelt`  
  
 <span data-ttu-id="12488-107">[out] Tableau de taille celt (ou supérieure) destiné à recevoir les structures RAWINPUTDEVICE énumérées.</span><span class="sxs-lookup"><span data-stu-id="12488-107">[out] Array of size celt (or larger) to receive enumerated RAWINPUTDEVICE structures.</span></span>  
  
 `pceltFetched`  
  
 <span data-ttu-id="12488-108">[out] Pointeur vers le nombre d'éléments réellement fournis dans `rgelt`.</span><span class="sxs-lookup"><span data-stu-id="12488-108">[out] Pointer to the number of elements actually supplied in `rgelt`.</span></span> <span data-ttu-id="12488-109">L'appelant peut passer `NULL` si `rgelt` a la valeur un.</span><span class="sxs-lookup"><span data-stu-id="12488-109">Caller can pass in `NULL` if `rgelt` is one.</span></span>  
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="12488-110">Valeur de propriété/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="12488-110">Property Value/Return Value</span></span>  
 <span data-ttu-id="12488-111">HRESULT : S_OK si le nombre d’éléments fournis est `celt`; Sinon, S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="12488-111">HRESULT: S_OK if the number of elements supplied is `celt`; S_FALSE otherwise.</span></span>
