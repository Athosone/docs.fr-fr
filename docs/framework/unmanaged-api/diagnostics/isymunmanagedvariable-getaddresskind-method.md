---
title: ISymUnmanagedVariable::GetAddressKind, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedVariable.GetAddressKind
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedVariable::GetAddressKind
helpviewer_keywords:
- GetAddressKind method [.NET Framework debugging]
- ISymUnmanagedVariable::GetAddressKind method [.NET Framework debugging]
ms.assetid: a71563c0-62f2-4eb4-970c-825d61827613
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: eae5b21af3bcdca911ec13067a61bb957d4ae6ab
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59092940"
---
# <a name="isymunmanagedvariablegetaddresskind-method"></a><span data-ttu-id="c5d66-102">ISymUnmanagedVariable::GetAddressKind, méthode</span><span class="sxs-lookup"><span data-stu-id="c5d66-102">ISymUnmanagedVariable::GetAddressKind Method</span></span>
<span data-ttu-id="c5d66-103">Obtient le type d’adresse de cette variable.</span><span class="sxs-lookup"><span data-stu-id="c5d66-103">Gets the kind of address of this variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c5d66-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5d66-104">Syntax</span></span>  
  
```  
HRESULT GetAddressKind(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c5d66-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5d66-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="c5d66-106">[out] Un pointeur vers un `ULONG32` qui reçoit la valeur.</span><span class="sxs-lookup"><span data-stu-id="c5d66-106">[out] A pointer to a `ULONG32` that receives the value.</span></span> <span data-ttu-id="c5d66-107">Les valeurs possibles sont définies dans le [CorSymAddrKind](../../../../docs/framework/unmanaged-api/diagnostics/corsymaddrkind-enumeration.md) énumération.</span><span class="sxs-lookup"><span data-stu-id="c5d66-107">The possible values are defined in the [CorSymAddrKind](../../../../docs/framework/unmanaged-api/diagnostics/corsymaddrkind-enumeration.md) enumeration.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c5d66-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c5d66-108">Return Value</span></span>  
 <span data-ttu-id="c5d66-109">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="c5d66-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c5d66-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5d66-110">Requirements</span></span>  
 <span data-ttu-id="c5d66-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="c5d66-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c5d66-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5d66-112">See also</span></span>

- [<span data-ttu-id="c5d66-113">ISymUnmanagedVariable, interface</span><span class="sxs-lookup"><span data-stu-id="c5d66-113">ISymUnmanagedVariable Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-interface.md)
