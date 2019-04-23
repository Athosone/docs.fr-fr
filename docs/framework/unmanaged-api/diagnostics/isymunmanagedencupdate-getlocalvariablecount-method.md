---
title: ISymUnmanagedENCUpdate::GetLocalVariableCount, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedENCUpdate.GetLocalVariableCount
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedENCUpdate::GetLocalVariableCount
helpviewer_keywords:
- ISymUnmanagedENCUpdate::GetLocalVariableCount method [.NET Framework debugging]
- GetLocalVariableCount method [.NET Framework debugging]
ms.assetid: 9777d8bb-4abc-4be8-aa7c-34f853eceb9c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 11a75ca89a3537ce8ee72e8ba24401800eacff20
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59153775"
---
# <a name="isymunmanagedencupdategetlocalvariablecount-method"></a><span data-ttu-id="319d3-102">ISymUnmanagedENCUpdate::GetLocalVariableCount, méthode</span><span class="sxs-lookup"><span data-stu-id="319d3-102">ISymUnmanagedENCUpdate::GetLocalVariableCount Method</span></span>
<span data-ttu-id="319d3-103">Obtient le nombre de variables locales.</span><span class="sxs-lookup"><span data-stu-id="319d3-103">Gets the number of local variables.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="319d3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="319d3-104">Syntax</span></span>  
  
```  
HRESULT GetLocalVariableCount(  
    [in]  mdMethodDef  mdMethodToken,  
    [out] ULONG        *pcLocals);  
```  
  
## <a name="parameters"></a><span data-ttu-id="319d3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="319d3-105">Parameters</span></span>  
 `mdMethodToken`  
 <span data-ttu-id="319d3-106">[in] Le jeton de métadonnées de méthodes.</span><span class="sxs-lookup"><span data-stu-id="319d3-106">[in] The metadata token of methods.</span></span>  
  
 `pcLocals`  
 <span data-ttu-id="319d3-107">[out] Un pointeur vers un `ULONG32` qui reçoit la taille, en caractères, de la mémoire tampon requise pour contenir le nombre de variables locales.</span><span class="sxs-lookup"><span data-stu-id="319d3-107">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the number of local variables.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="319d3-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="319d3-108">Return Value</span></span>  
 <span data-ttu-id="319d3-109">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="319d3-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="319d3-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="319d3-110">Requirements</span></span>  
 <span data-ttu-id="319d3-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="319d3-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="319d3-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="319d3-112">See also</span></span>

- [<span data-ttu-id="319d3-113">ISymUnmanagedENCUpdate, interface</span><span class="sxs-lookup"><span data-stu-id="319d3-113">ISymUnmanagedENCUpdate Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-interface.md)
