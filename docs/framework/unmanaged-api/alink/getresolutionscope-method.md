---
title: GetResolutionScope, méthode
ms.date: 03/30/2017
api_name:
- IALink.GetResolutionScope
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetResolutionScope
helpviewer_keywords:
- GetResolutionScope method
ms.assetid: 5b48ca60-dacd-44b2-9979-4a5122f00812
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6c6d298c84b801b87832c56026b05f647cb5a9dd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59135170"
---
# <a name="getresolutionscope-method"></a><span data-ttu-id="1e482-102">GetResolutionScope, méthode</span><span class="sxs-lookup"><span data-stu-id="1e482-102">GetResolutionScope Method</span></span>
<span data-ttu-id="1e482-103">Récupère l’étendue d’un type donné.</span><span class="sxs-lookup"><span data-stu-id="1e482-103">Retrieves the scope of a given type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1e482-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e482-104">Syntax</span></span>  
  
```  
HRESULT GetResolutionScope(  
    mdAssembly  AssemblyID,  
    mdToken     FileToken,  
    mdToken     TargetFile,  
    mdToken*    pScope  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="1e482-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e482-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="1e482-106">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="1e482-106">ID of the assembly.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="1e482-107">Fichier qui a besoin d’une référence.</span><span class="sxs-lookup"><span data-stu-id="1e482-107">File that is in need of a reference.</span></span>  
  
 `TargetFile`  
 <span data-ttu-id="1e482-108">Jeton du fichier dans lequel le type est défini, généralement récupéré avec [ImportFile, méthode](../../../../docs/framework/unmanaged-api/alink/importfile-method.md).</span><span class="sxs-lookup"><span data-stu-id="1e482-108">Token of file that type is defined in, usually retrieved with [ImportFile Method](../../../../docs/framework/unmanaged-api/alink/importfile-method.md).</span></span>  
  
 `pScope`  
 <span data-ttu-id="1e482-109">Reçoit la référence d’assembly ou module.</span><span class="sxs-lookup"><span data-stu-id="1e482-109">Receives the assembly or module reference.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1e482-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="1e482-110">Return Value</span></span>  
 <span data-ttu-id="1e482-111">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="1e482-111">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1e482-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e482-112">Requirements</span></span>  
 <span data-ttu-id="1e482-113">Nécessite alink.h.</span><span class="sxs-lookup"><span data-stu-id="1e482-113">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1e482-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e482-114">See also</span></span>

- [<span data-ttu-id="1e482-115">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="1e482-115">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="1e482-116">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="1e482-116">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="1e482-117">API ALink</span><span class="sxs-lookup"><span data-stu-id="1e482-117">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
