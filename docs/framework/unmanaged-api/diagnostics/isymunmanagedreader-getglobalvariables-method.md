---
title: ISymUnmanagedReader::GetGlobalVariables, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetGlobalVariables
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetGlobalVariables
helpviewer_keywords:
- GetGlobalVariables method [.NET Framework debugging]
- ISymUnmanagedReader::GetGlobalVariables method [.NET Framework debugging]
ms.assetid: a2dd5098-3e58-4be5-b7a2-e4160b3b505a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: e778a5a7baed52941a7f4b990b34d31f8ca84c24
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61986386"
---
# <a name="isymunmanagedreadergetglobalvariables-method"></a><span data-ttu-id="0bc5c-102">ISymUnmanagedReader::GetGlobalVariables, méthode</span><span class="sxs-lookup"><span data-stu-id="0bc5c-102">ISymUnmanagedReader::GetGlobalVariables Method</span></span>
<span data-ttu-id="0bc5c-103">Retourne toutes les variables globales.</span><span class="sxs-lookup"><span data-stu-id="0bc5c-103">Returns all global variables.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0bc5c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0bc5c-104">Syntax</span></span>  
  
```  
HRESULT GetGlobalVariables(  
    [in]  ULONG32  cVars,  
    [out] ULONG32  *pcVars,  
    [out, size_is(cVars),  
        length_is(*pcVars)] ISymUnmanagedVariable *pVars[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0bc5c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0bc5c-105">Parameters</span></span>  
 `cVars`  
 <span data-ttu-id="0bc5c-106">[in] La longueur de la mémoire tampon vers laquelle pointe `pcVars`.</span><span class="sxs-lookup"><span data-stu-id="0bc5c-106">[in] The length of the buffer pointed to by `pcVars`.</span></span>  
  
 `pcVars`  
 <span data-ttu-id="0bc5c-107">[out] Un pointeur vers un `ULONG32` qui reçoit la taille de la mémoire tampon requise pour contenir les variables.</span><span class="sxs-lookup"><span data-stu-id="0bc5c-107">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the variables.</span></span>  
  
 `pVars`  
 <span data-ttu-id="0bc5c-108">[out] Une mémoire tampon qui contient les variables.</span><span class="sxs-lookup"><span data-stu-id="0bc5c-108">[out] A buffer that contains the variables.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0bc5c-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0bc5c-109">Return Value</span></span>  
 <span data-ttu-id="0bc5c-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0bc5c-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0bc5c-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0bc5c-111">Requirements</span></span>  
 <span data-ttu-id="0bc5c-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="0bc5c-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0bc5c-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bc5c-113">See also</span></span>

- [<span data-ttu-id="0bc5c-114">ISymUnmanagedReader, interface</span><span class="sxs-lookup"><span data-stu-id="0bc5c-114">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
