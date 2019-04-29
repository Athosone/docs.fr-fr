---
title: ISymUnmanagedDocument::GetSourceRange, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetSourceRange
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetSourceRange
helpviewer_keywords:
- ISymUnmanagedDocument::GetSourceRange method [.NET Framework debugging]
- GetSourceRange method [.NET Framework debugging]
ms.assetid: 20fefee7-1040-41ba-93dc-bd42f68b90c2
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 59420cfd29c3228aece9fc5ae02b950db6099ea0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61939853"
---
# <a name="isymunmanageddocumentgetsourcerange-method"></a><span data-ttu-id="0a54e-102">ISymUnmanagedDocument::GetSourceRange, méthode</span><span class="sxs-lookup"><span data-stu-id="0a54e-102">ISymUnmanagedDocument::GetSourceRange Method</span></span>
<span data-ttu-id="0a54e-103">Retourne la plage spécifiée de la source incorporée dans la mémoire tampon donnée.</span><span class="sxs-lookup"><span data-stu-id="0a54e-103">Returns the specified range of the embedded source into the given buffer.</span></span> <span data-ttu-id="0a54e-104">La mémoire tampon doit être suffisamment grande pour contenir la source.</span><span class="sxs-lookup"><span data-stu-id="0a54e-104">The buffer must be large enough to hold the source.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0a54e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a54e-105">Syntax</span></span>  
  
```  
HRESULT GetSourceRange(  
    [in]  ULONG32  startLine,  
    [in]  ULONG32  startColumn,  
    [in]  ULONG32  endLine,  
    [in]  ULONG32  endColumn,  
    [in]  ULONG32  cSourceBytes,  
    [out] ULONG32  *pcSourceBytes,  
    [out, size_is(cSourceBytes),  
        length_is(*pcSourceBytes)] BYTE source[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0a54e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a54e-106">Parameters</span></span>  
 `startLine`  
 <span data-ttu-id="0a54e-107">[in] La ligne de départ dans le document actif.</span><span class="sxs-lookup"><span data-stu-id="0a54e-107">[in] The starting line in the current document.</span></span>  
  
 `startColumn`  
 <span data-ttu-id="0a54e-108">[in] La colonne de départ dans le document actif.</span><span class="sxs-lookup"><span data-stu-id="0a54e-108">[in] The starting column in the current document.</span></span>  
  
 `endLine`  
 <span data-ttu-id="0a54e-109">[in] La dernière ligne dans le document actif.</span><span class="sxs-lookup"><span data-stu-id="0a54e-109">[in] The final line in the current document.</span></span>  
  
 `endColumn`  
 <span data-ttu-id="0a54e-110">[in] La dernière colonne dans le document actif.</span><span class="sxs-lookup"><span data-stu-id="0a54e-110">[in] The final column in the current document.</span></span>  
  
 `cSourceBytes`  
 <span data-ttu-id="0a54e-111">[in] La taille de la source, en octets.</span><span class="sxs-lookup"><span data-stu-id="0a54e-111">[in] The size of the source, in bytes.</span></span>  
  
 `pcSourceBytes`  
 <span data-ttu-id="0a54e-112">[out] Pointeur vers une variable qui reçoit la taille de la source.</span><span class="sxs-lookup"><span data-stu-id="0a54e-112">[out] A pointer to a variable that receives the source size.</span></span>  
  
 `source`  
 <span data-ttu-id="0a54e-113">[out] La taille et la longueur de la plage spécifiée du document source, en octets.</span><span class="sxs-lookup"><span data-stu-id="0a54e-113">[out] The size and length of the specified range of the source document, in bytes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0a54e-114">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0a54e-114">Return Value</span></span>  
 <span data-ttu-id="0a54e-115">S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="0a54e-115">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0a54e-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a54e-116">See also</span></span>

- [<span data-ttu-id="0a54e-117">ISymUnmanagedDocument, interface</span><span class="sxs-lookup"><span data-stu-id="0a54e-117">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
