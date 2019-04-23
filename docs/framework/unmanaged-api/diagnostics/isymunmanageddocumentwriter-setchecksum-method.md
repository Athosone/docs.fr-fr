---
title: ISymUnmanagedDocumentWriter::SetCheckSum, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocumentWriter.SetCheckSum
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocumentWriter::SetCheckSum
helpviewer_keywords:
- ISymUnmanagedDocumentWriter::SetCheckSum method [.NET Framework debugging]
- SetCheckSum method [.NET Framework debugging]
ms.assetid: c7e99879-421f-43ce-b193-34733cf30085
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ac3daccfade4f5ae10fe2ebbf83a7a11af34b89b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59196981"
---
# <a name="isymunmanageddocumentwritersetchecksum-method"></a><span data-ttu-id="64d08-102">ISymUnmanagedDocumentWriter::SetCheckSum, méthode</span><span class="sxs-lookup"><span data-stu-id="64d08-102">ISymUnmanagedDocumentWriter::SetCheckSum Method</span></span>
<span data-ttu-id="64d08-103">Définit les informations de la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="64d08-103">Sets checksum information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="64d08-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64d08-104">Syntax</span></span>  
  
```  
HRESULT SetCheckSum(  
    [in]  GUID     algorithmId,  
    [in]  ULONG32  checkSumSize,  
    [in, size_is(checkSumSize)]  BYTE checkSum[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="64d08-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64d08-105">Parameters</span></span>  
 `algorithmId`  
 <span data-ttu-id="64d08-106">[in] GUID qui représente l’identificateur d’algorithme.</span><span class="sxs-lookup"><span data-stu-id="64d08-106">[in] The GUID that represents the algorithm identifier.</span></span>  
  
 `checkSumSize`  
 <span data-ttu-id="64d08-107">[in] Un `ULONG32` qui indique la taille, en octets, de la `checkSum` mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="64d08-107">[in] A `ULONG32` that indicates the size, in bytes, of the `checkSum` buffer.</span></span>  
  
 `checkSum`  
 <span data-ttu-id="64d08-108">[in] La mémoire tampon qui stocke les informations de somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="64d08-108">[in] The buffer that stores the checksum information.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="64d08-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="64d08-109">Return Value</span></span>  
 <span data-ttu-id="64d08-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="64d08-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="64d08-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64d08-111">Requirements</span></span>  
 <span data-ttu-id="64d08-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="64d08-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="64d08-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64d08-113">See also</span></span>

- [<span data-ttu-id="64d08-114">ISymUnmanagedDocumentWriter, interface</span><span class="sxs-lookup"><span data-stu-id="64d08-114">ISymUnmanagedDocumentWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocumentwriter-interface.md)
