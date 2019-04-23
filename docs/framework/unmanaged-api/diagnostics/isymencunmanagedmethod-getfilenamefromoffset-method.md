---
title: ISymENCUnmanagedMethod::GetFileNameFromOffset, méthode
ms.date: 03/30/2017
api_name:
- ISymENCUnmanagedMethod.GetFileNameFromOffset
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymENCUnmanagedMethod::GetFileNameFromOffset
helpviewer_keywords:
- GetFileNameFromOffset method [.NET Framework debugging]
- ISymENCUnmanagedMethod::GetFileNameFromOffset method [.NET Framework debugging]
ms.assetid: 00e2e194-12f5-436e-a997-2b9d3e844d4f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 494f39855132bc4a9551b78f746517862d285034
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59074727"
---
# <a name="isymencunmanagedmethodgetfilenamefromoffset-method"></a><span data-ttu-id="9ea88-102">ISymENCUnmanagedMethod::GetFileNameFromOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="9ea88-102">ISymENCUnmanagedMethod::GetFileNameFromOffset Method</span></span>
<span data-ttu-id="9ea88-103">Obtient le nom de fichier pour la ligne associée à un décalage.</span><span class="sxs-lookup"><span data-stu-id="9ea88-103">Gets the file name for the line associated with an offset.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9ea88-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ea88-104">Syntax</span></span>  
  
```  
HRESULT GetFileNameFromOffset(  
    [in]  ULONG32  dwOffset,  
    [in]  ULONG32  cchName,  
    [out] ULONG32  *pcchName,  
    [out, size_is(cchName),  
       length_is(*pcchName)] WCHAR szName[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9ea88-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ea88-105">Parameters</span></span>  
 `dwOffset`  
 <span data-ttu-id="9ea88-106">[in] Un `ULONG32` qui contient l’offset.</span><span class="sxs-lookup"><span data-stu-id="9ea88-106">[in] A `ULONG32` that contains the offset.</span></span>  
  
 `cchName`  
 <span data-ttu-id="9ea88-107">[in] Un `ULONG32` qui indique la taille de la `szName` mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="9ea88-107">[in] A `ULONG32` that indicates the size of the `szName` buffer.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="9ea88-108">[out] Un pointeur vers un `ULONG32` qui reçoit la taille, en caractères, de la mémoire tampon requise pour contenir les noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="9ea88-108">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the file names.</span></span>  
  
 `szName`  
 <span data-ttu-id="9ea88-109">[out] La mémoire tampon qui contient les noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="9ea88-109">[out] The buffer that contains the file names.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9ea88-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9ea88-110">Return Value</span></span>  
 <span data-ttu-id="9ea88-111">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="9ea88-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9ea88-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ea88-112">Requirements</span></span>  
 <span data-ttu-id="9ea88-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="9ea88-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9ea88-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ea88-114">See also</span></span>

- [<span data-ttu-id="9ea88-115">ISymENCUnmanagedMethod, interface</span><span class="sxs-lookup"><span data-stu-id="9ea88-115">ISymENCUnmanagedMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymencunmanagedmethod-interface.md)
