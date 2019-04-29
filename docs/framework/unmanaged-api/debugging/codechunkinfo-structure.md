---
title: CodeChunkInfo, structure
ms.date: 03/30/2017
api_name:
- CodeChunkInfo
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CodeChunkInfo
helpviewer_keywords:
- CodeChunkInfo structure [.NET Framework debugging]
ms.assetid: 0f482454-8517-48de-ba7a-d7aedab13bb5
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 58c9d4c66af0bb9f4e66d17b18ac78ef8271bc31
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61609605"
---
# <a name="codechunkinfo-structure"></a><span data-ttu-id="a13ab-102">CodeChunkInfo, structure</span><span class="sxs-lookup"><span data-stu-id="a13ab-102">CodeChunkInfo Structure</span></span>

<span data-ttu-id="a13ab-103">Représente un bloc de code unique en mémoire.</span><span class="sxs-lookup"><span data-stu-id="a13ab-103">Represents a single chunk of code in memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a13ab-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a13ab-104">Syntax</span></span>  
  
```  
typedef struct _CodeChunkInfo {  
    CORDB_ADDRESS startAddr;  
    ULONG32       length;  
} CodeChunkInfo;  
```  
  
## <a name="members"></a><span data-ttu-id="a13ab-105">Membres</span><span class="sxs-lookup"><span data-stu-id="a13ab-105">Members</span></span>  
  
|<span data-ttu-id="a13ab-106">Membre</span><span class="sxs-lookup"><span data-stu-id="a13ab-106">Member</span></span>|<span data-ttu-id="a13ab-107">Description</span><span class="sxs-lookup"><span data-stu-id="a13ab-107">Description</span></span>|  
|------------|-----------------|  
|`startAddr`|<span data-ttu-id="a13ab-108">Un `CORDB_ADDRESS` valeur qui spécifie l’adresse de départ du segment.</span><span class="sxs-lookup"><span data-stu-id="a13ab-108">A `CORDB_ADDRESS` value that specifies the starting address of the chunk.</span></span>|  
|`length`|<span data-ttu-id="a13ab-109">La taille, en octets, du bloc.</span><span class="sxs-lookup"><span data-stu-id="a13ab-109">The size, in bytes, of the chunk.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a13ab-110">Notes</span><span class="sxs-lookup"><span data-stu-id="a13ab-110">Remarks</span></span>  
 <span data-ttu-id="a13ab-111">Le bloc de code unique est une région de code natif qui fait partie d’un objet de code comme une fonction.</span><span class="sxs-lookup"><span data-stu-id="a13ab-111">The single chunk of code is a region of native code that is part of a code object such as a function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a13ab-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a13ab-112">Requirements</span></span>  
 <span data-ttu-id="a13ab-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a13ab-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a13ab-114">**En-tête :** CorDebug.idl</span><span class="sxs-lookup"><span data-stu-id="a13ab-114">**Header:** CorDebug.idl</span></span>  
  
 <span data-ttu-id="a13ab-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a13ab-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a13ab-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a13ab-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a13ab-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a13ab-117">See also</span></span>

- [<span data-ttu-id="a13ab-118">GetCodeChunks, méthode</span><span class="sxs-lookup"><span data-stu-id="a13ab-118">GetCodeChunks Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcode2-getcodechunks-method.md)
- [<span data-ttu-id="a13ab-119">Structures de débogage</span><span class="sxs-lookup"><span data-stu-id="a13ab-119">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
- [<span data-ttu-id="a13ab-120">Débogage</span><span class="sxs-lookup"><span data-stu-id="a13ab-120">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
