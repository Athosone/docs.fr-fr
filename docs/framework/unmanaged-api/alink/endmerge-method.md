---
title: EndMerge, méthode
ms.date: 03/30/2017
api_name:
- IALink.EndMerge
- EndMerge
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EndMerge
helpviewer_keywords:
- EndMerge method
ms.assetid: 1d03bb15-a2c8-4a04-8fc6-b126c89c3778
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 020cc56126249b27a52387e6efa3aa10c83d9126
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61789985"
---
# <a name="endmerge-method"></a><span data-ttu-id="4f91a-102">EndMerge, méthode</span><span class="sxs-lookup"><span data-stu-id="4f91a-102">EndMerge Method</span></span>
<span data-ttu-id="4f91a-103">Indique que tous les attributs personnalisés ont été fusionnés dans la portée d’émission.</span><span class="sxs-lookup"><span data-stu-id="4f91a-103">Indicates that all custom attributes have been merged into the emit scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4f91a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f91a-104">Syntax</span></span>  
  
```  
HRESULT EndMerge(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="4f91a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f91a-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="4f91a-106">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="4f91a-106">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4f91a-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4f91a-107">Return Value</span></span>  
 <span data-ttu-id="4f91a-108">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="4f91a-108">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4f91a-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f91a-109">Requirements</span></span>  
 <span data-ttu-id="4f91a-110">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="4f91a-110">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4f91a-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f91a-111">See also</span></span>

- [<span data-ttu-id="4f91a-112">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="4f91a-112">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="4f91a-113">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="4f91a-113">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="4f91a-114">API ALink</span><span class="sxs-lookup"><span data-stu-id="4f91a-114">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
