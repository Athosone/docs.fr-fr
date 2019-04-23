---
title: ISymUnmanagedAsyncMethod::GetKickoffMethod, méthode
ms.date: 03/30/2017
ms.assetid: ba084444-9e68-4cde-9388-54b950670987
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4599d41336778db8ce8dcf3ac567e4e2cc8833e6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59174939"
---
# <a name="isymunmanagedasyncmethodgetkickoffmethod-method"></a><span data-ttu-id="05226-102">ISymUnmanagedAsyncMethod::GetKickoffMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="05226-102">ISymUnmanagedAsyncMethod::GetKickoffMethod Method</span></span>
<span data-ttu-id="05226-103">Consultez [definekickoffmethod, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definekickoffmethod-method.md).</span><span class="sxs-lookup"><span data-stu-id="05226-103">See [DefineKickoffMethod Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definekickoffmethod-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="05226-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05226-104">Syntax</span></span>  
  
```idl  
HRESULT GetKickoffMethod(    [out, retval] mdToken* kickoffMethod);  
```  
  
## <a name="parameters"></a><span data-ttu-id="05226-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05226-105">Parameters</span></span>  
  
|<span data-ttu-id="05226-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="05226-106">Parameter</span></span>|<span data-ttu-id="05226-107">Description</span><span class="sxs-lookup"><span data-stu-id="05226-107">Description</span></span>|  
|---------------|-----------------|  
|`kickoffMethod`||  
  
## <a name="return-value"></a><span data-ttu-id="05226-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="05226-108">Return Value</span></span>  
 <span data-ttu-id="05226-109">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="05226-109">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="05226-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05226-110">Requirements</span></span>  
 <span data-ttu-id="05226-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="05226-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="05226-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05226-112">See also</span></span>

- [<span data-ttu-id="05226-113">ISymUnmanagedAsyncMethod, interface</span><span class="sxs-lookup"><span data-stu-id="05226-113">ISymUnmanagedAsyncMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-interface.md)
