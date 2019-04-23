---
title: ISymUnmanagedReader::GetSymbolStoreFileName, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetSymbolStoreFileName
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetSymbolStoreFileName
helpviewer_keywords:
- GetSymbolStoreFileName method [.NET Framework debugging]
- ISymUnmanagedReader::GetSymbolStoreFileName method [.NET Framework debugging]
ms.assetid: c84f4846-9bc8-44a4-9a76-e39106d6d8b2
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 147b33a3f49f9163daea776779ca26f62561a84e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59170376"
---
# <a name="isymunmanagedreadergetsymbolstorefilename-method"></a><span data-ttu-id="bf03e-102">ISymUnmanagedReader::GetSymbolStoreFileName, méthode</span><span class="sxs-lookup"><span data-stu-id="bf03e-102">ISymUnmanagedReader::GetSymbolStoreFileName Method</span></span>
<span data-ttu-id="bf03e-103">Fournit le nom de fichier sur disque du magasin de symboles.</span><span class="sxs-lookup"><span data-stu-id="bf03e-103">Provides the on-disk file name of the symbol store.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bf03e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf03e-104">Syntax</span></span>  
  
```  
HRESULT GetSymbolStoreFileName (  
    [in]  ULONG32 cchName,  
    [out] ULONG32 *pcchName,  
    [out, size_is (cchName),  
        length_is (*pcchName)] WCHAR szName[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bf03e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf03e-105">Parameters</span></span>  
 `cchName`  
 <span data-ttu-id="bf03e-106">[in] La taille de la `szName` mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="bf03e-106">[in] The size of the `szName` buffer.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="bf03e-107">[out] Un pointeur vers la variable qui reçoit la longueur du nom retourné dans `szName`, y compris le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="bf03e-107">[out] A pointer to the variable that receives the length of the name returned in `szName`, including the null termination.</span></span>  
  
 `szName`  
 <span data-ttu-id="bf03e-108">[out] Pointeur vers la variable qui reçoit le nom de fichier du magasin de symboles.</span><span class="sxs-lookup"><span data-stu-id="bf03e-108">[out] A pointer to the variable that receives the file name of the symbol store.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="bf03e-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="bf03e-109">Return Value</span></span>  
 <span data-ttu-id="bf03e-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="bf03e-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bf03e-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf03e-111">Requirements</span></span>  
 <span data-ttu-id="bf03e-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="bf03e-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bf03e-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf03e-113">See also</span></span>

- [<span data-ttu-id="bf03e-114">ISymUnmanagedReader, interface</span><span class="sxs-lookup"><span data-stu-id="bf03e-114">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
