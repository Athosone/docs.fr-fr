---
title: ISymUnmanagedAsyncMethodPropertiesWriter::DefineCatchHandlerILOffset, méthode
ms.date: 03/30/2017
ms.assetid: 92af7896-2201-408d-8b1b-23e28001eeac
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 923c85a9dff11753a338fcfd3673d3590fca607a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59196747"
---
# <a name="isymunmanagedasyncmethodpropertieswriterdefinecatchhandleriloffset-method"></a><span data-ttu-id="57f9f-102">ISymUnmanagedAsyncMethodPropertiesWriter::DefineCatchHandlerILOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="57f9f-102">ISymUnmanagedAsyncMethodPropertiesWriter::DefineCatchHandlerILOffset Method</span></span>
<span data-ttu-id="57f9f-103">Définit le langage intermédiaire de décalage pour le gestionnaire catch généré par le compilateur qui encapsule une méthode async.</span><span class="sxs-lookup"><span data-stu-id="57f9f-103">Sets the IL offset for the compiler-generated catch handler that wraps an async method.</span></span>  
  
 <span data-ttu-id="57f9f-104">L’offset IL de la capture générée est utilisé par le débogueur pour gérer les captures comme s’il s’agissait d’un code non utilisateur même si elle peut se produire dans une méthode de code utilisateur.</span><span class="sxs-lookup"><span data-stu-id="57f9f-104">The IL offset of the generated catch is used by the debugger to handle the catch as if it were non-user code even though it might occur in a user code method.</span></span> <span data-ttu-id="57f9f-105">En particulier, il est utilisé en réponse à une **CatchHandlerFound** événement d’exception.</span><span class="sxs-lookup"><span data-stu-id="57f9f-105">In particular, it is used in response to a **CatchHandlerFound** exception event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="57f9f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57f9f-106">Syntax</span></span>  
  
```idl  
HRESULT DefineCatchHandlerILOffset(    [in] ULONG32 catchHandlerOffset);  
```  
  
## <a name="parameters"></a><span data-ttu-id="57f9f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57f9f-107">Parameters</span></span>  
  
|<span data-ttu-id="57f9f-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="57f9f-108">Parameter</span></span>|<span data-ttu-id="57f9f-109">Description</span><span class="sxs-lookup"><span data-stu-id="57f9f-109">Description</span></span>|  
|---------------|-----------------|  
|`catchHandlerOffset`||  
  
## <a name="return-value"></a><span data-ttu-id="57f9f-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="57f9f-110">Return Value</span></span>  
 <span data-ttu-id="57f9f-111">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="57f9f-111">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="57f9f-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57f9f-112">Requirements</span></span>  
 <span data-ttu-id="57f9f-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="57f9f-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="57f9f-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57f9f-114">See also</span></span>

- [<span data-ttu-id="57f9f-115">ISymUnmanagedAsyncMethodPropertiesWriter, interface</span><span class="sxs-lookup"><span data-stu-id="57f9f-115">ISymUnmanagedAsyncMethodPropertiesWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md)
