---
title: ISymUnmanagedDocument::GetLanguage, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetLanguage
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetLanguage
helpviewer_keywords:
- ISymUnmanagedDocument::GetLanguage method [.NET Framework debugging]
- GetLanguage method [.NET Framework debugging]
ms.assetid: c6639418-e9f2-4a99-8ce2-ec9876e0bc79
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 05ce47953358b7025e30080fbbaf288a6c0e879d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59104589"
---
# <a name="isymunmanageddocumentgetlanguage-method"></a><span data-ttu-id="74397-102">ISymUnmanagedDocument::GetLanguage, méthode</span><span class="sxs-lookup"><span data-stu-id="74397-102">ISymUnmanagedDocument::GetLanguage Method</span></span>
<span data-ttu-id="74397-103">Obtient l’identificateur de langue de ce document</span><span class="sxs-lookup"><span data-stu-id="74397-103">Gets the language identifier of this document</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="74397-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74397-104">Syntax</span></span>  
  
```  
HRESULT GetLanguage(  
    [out, retval]  GUID*  pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="74397-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74397-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="74397-106">[out] Pointeur vers une variable qui reçoit l’identificateur de langue.</span><span class="sxs-lookup"><span data-stu-id="74397-106">[out] A pointer to a variable that receives the language identifier.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="74397-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="74397-107">Return Value</span></span>  
 <span data-ttu-id="74397-108">S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="74397-108">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="74397-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74397-109">See also</span></span>

- [<span data-ttu-id="74397-110">ISymUnmanagedDocument, interface</span><span class="sxs-lookup"><span data-stu-id="74397-110">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
