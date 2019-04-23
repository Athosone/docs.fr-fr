---
title: ISymUnmanagedReader::GetNamespaces, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetNamespaces
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetNamespaces
helpviewer_keywords:
- ISymUnmanagedReader::GetNamespaces method [.NET Framework debugging]
- GetNamespaces method, ISymUnmanagedReader interface [.NET Framework debugging]
ms.assetid: 3feb4796-2fab-45ce-beca-6f5bc530b971
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 570532433483e9d0a08f4d685087c0736e135390
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59076729"
---
# <a name="isymunmanagedreadergetnamespaces-method"></a><span data-ttu-id="99907-102">ISymUnmanagedReader::GetNamespaces, méthode</span><span class="sxs-lookup"><span data-stu-id="99907-102">ISymUnmanagedReader::GetNamespaces Method</span></span>
<span data-ttu-id="99907-103">Obtient les espaces de noms définis dans une portée globale dans ce magasin de symboles.</span><span class="sxs-lookup"><span data-stu-id="99907-103">Gets the namespaces defined at global scope within this symbol store.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="99907-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99907-104">Syntax</span></span>  
  
```  
HRESULT GetNamespaces (  
    [in]  ULONG32  cNameSpaces,  
    [out] ULONG32  *pcNameSpaces,  
    [out, size_is (cNameSpaces),  
        length_is (*pcNameSpaces)]  
        ISymUnmanagedNamespace*  namespaces[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="99907-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99907-105">Parameters</span></span>  
 `cNameSpaces`  
 <span data-ttu-id="99907-106">[in] La taille du tableau d’espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="99907-106">[in] The size of the namespaces array.</span></span>  
  
 `pcNameSpaces`  
 <span data-ttu-id="99907-107">[out] Pointeur vers une variable qui reçoit la longueur de la liste de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="99907-107">[out] A pointer to a variable that receives the length of the namespace list.</span></span>  
  
 `namespaces`  
 <span data-ttu-id="99907-108">[out] Pointeur vers une variable qui reçoit la liste de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="99907-108">[out] A pointer to a variable that receives the namespace list.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="99907-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="99907-109">Return Value</span></span>  
 <span data-ttu-id="99907-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="99907-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="99907-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99907-111">Requirements</span></span>  
 <span data-ttu-id="99907-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="99907-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="99907-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99907-113">See also</span></span>

- [<span data-ttu-id="99907-114">ISymUnmanagedReader, interface</span><span class="sxs-lookup"><span data-stu-id="99907-114">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
