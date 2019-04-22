---
title: ISymUnmanagedScope2::GetConstants, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope2.GetConstants
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope2::GetConstants
helpviewer_keywords:
- ISymUnmanagedScope2::GetConstants method [.NET Framework debugging]
- GetConstants method [.NET Framework debugging]
ms.assetid: f241b620-9ec5-42fd-92ef-3b22329db72a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 08bc85c7a5b53c145375ca34f11ec499e5e7528f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59096821"
---
# <a name="isymunmanagedscope2getconstants-method"></a><span data-ttu-id="7c06b-102">ISymUnmanagedScope2::GetConstants, méthode</span><span class="sxs-lookup"><span data-stu-id="7c06b-102">ISymUnmanagedScope2::GetConstants Method</span></span>
<span data-ttu-id="7c06b-103">Obtient les variables constantes définies dans cette portée.</span><span class="sxs-lookup"><span data-stu-id="7c06b-103">Gets the local constants defined within this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7c06b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c06b-104">Syntax</span></span>  
  
```  
HRESULT GetConstants(  
     [in]  ULONG32  cConstants,  
     [out] ULONG32  *pcConstants,  
     [out, size_is(cConstants),  
         length_is(*pcConstants)] ISymUnmanagedConstant*   
             constants[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7c06b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c06b-105">Parameters</span></span>  
 `cConstants`  
 <span data-ttu-id="7c06b-106">[in] La longueur de la mémoire tampon qui le `pcConstants` paramètre pointe vers.</span><span class="sxs-lookup"><span data-stu-id="7c06b-106">[in] The length of the buffer that the `pcConstants` parameter points to.</span></span>  
  
 `pcConstants`  
 <span data-ttu-id="7c06b-107">[out] Un pointeur vers un `ULONG32` qui reçoit la taille, en caractères, de la mémoire tampon requise pour contenir les constantes.</span><span class="sxs-lookup"><span data-stu-id="7c06b-107">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the constants.</span></span>  
  
 `constants`  
 <span data-ttu-id="7c06b-108">[out] La mémoire tampon qui stocke les constantes.</span><span class="sxs-lookup"><span data-stu-id="7c06b-108">[out] The buffer that stores the constants.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7c06b-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="7c06b-109">Return Value</span></span>  
 <span data-ttu-id="7c06b-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="7c06b-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7c06b-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c06b-111">Requirements</span></span>  
 <span data-ttu-id="7c06b-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="7c06b-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7c06b-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c06b-113">See also</span></span>

- [<span data-ttu-id="7c06b-114">ISymUnmanagedScope2, interface</span><span class="sxs-lookup"><span data-stu-id="7c06b-114">ISymUnmanagedScope2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope2-interface.md)
