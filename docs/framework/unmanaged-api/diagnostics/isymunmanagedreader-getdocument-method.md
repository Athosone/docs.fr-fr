---
title: ISymUnmanagedReader::GetDocument, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetDocument
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetDocument
helpviewer_keywords:
- ISymUnmanagedReader::GetDocument method [.NET Framework debugging]
- GetDocument method [.NET Framework debugging]
ms.assetid: bb203853-6a6d-4027-b9e9-603a7f28b9d3
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2a173c23ea33532f05e30d072677715e15d04018
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59093681"
---
# <a name="isymunmanagedreadergetdocument-method"></a><span data-ttu-id="e9458-102">ISymUnmanagedReader::GetDocument, méthode</span><span class="sxs-lookup"><span data-stu-id="e9458-102">ISymUnmanagedReader::GetDocument Method</span></span>
<span data-ttu-id="e9458-103">Recherche un document.</span><span class="sxs-lookup"><span data-stu-id="e9458-103">Finds a document.</span></span> <span data-ttu-id="e9458-104">Le langage du document, le fournisseur et le type sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="e9458-104">The document language, vendor, and type are optional.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e9458-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9458-105">Syntax</span></span>  
  
```  
HRESULT GetDocument (  
    [in]  WCHAR  *url,  
    [in]  GUID   language,  
    [in]  GUID   languageVendor,  
    [in]  GUID   documentType,  
    [out, retval] ISymUnmanagedDocument** pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e9458-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9458-106">Parameters</span></span>  
 `url`  
 <span data-ttu-id="e9458-107">[in] L’URL qui identifie le document.</span><span class="sxs-lookup"><span data-stu-id="e9458-107">[in] The URL that identifies the document.</span></span>  
  
 `language`  
 <span data-ttu-id="e9458-108">[in] Le langage du document.</span><span class="sxs-lookup"><span data-stu-id="e9458-108">[in] The document language.</span></span> <span data-ttu-id="e9458-109">Ce paramètre est optionnel.</span><span class="sxs-lookup"><span data-stu-id="e9458-109">This parameter is optional.</span></span>  
  
 `languageVendor`  
 <span data-ttu-id="e9458-110">[in] L’identité du fournisseur de langage du document.</span><span class="sxs-lookup"><span data-stu-id="e9458-110">[in] The identity of the vendor for the document language.</span></span> <span data-ttu-id="e9458-111">Ce paramètre est optionnel.</span><span class="sxs-lookup"><span data-stu-id="e9458-111">This parameter is optional.</span></span>  
  
 `documentType`  
 <span data-ttu-id="e9458-112">[in] Le type du document.</span><span class="sxs-lookup"><span data-stu-id="e9458-112">[in] The type of the document.</span></span> <span data-ttu-id="e9458-113">Ce paramètre est optionnel.</span><span class="sxs-lookup"><span data-stu-id="e9458-113">This parameter is optional.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="e9458-114">[out] Pointeur vers l’interface retournée.</span><span class="sxs-lookup"><span data-stu-id="e9458-114">[out] A pointer to the returned interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e9458-115">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e9458-115">Return Value</span></span>  
 <span data-ttu-id="e9458-116">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e9458-116">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e9458-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9458-117">Requirements</span></span>  
 <span data-ttu-id="e9458-118">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="e9458-118">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e9458-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9458-119">See also</span></span>

- [<span data-ttu-id="e9458-120">ISymUnmanagedReader, interface</span><span class="sxs-lookup"><span data-stu-id="e9458-120">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
