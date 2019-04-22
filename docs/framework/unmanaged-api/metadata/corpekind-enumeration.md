---
title: CorPEKind, énumération
ms.date: 03/30/2017
api_name:
- CorPEKind
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorPEKind
helpviewer_keywords:
- CorPEKind enumeration [.NET Framework metadata]
ms.assetid: 22dc6dea-b1b9-4982-a730-a022d586b117
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d8f830ca7e273b65dc9ec77566a02df6c32cd464
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59202389"
---
# <a name="corpekind-enumeration"></a><span data-ttu-id="f18fd-102">CorPEKind, énumération</span><span class="sxs-lookup"><span data-stu-id="f18fd-102">CorPEKind Enumeration</span></span>
<span data-ttu-id="f18fd-103">Contient des valeurs qui décrivent un fichier exécutable portable (PE), tel que retourné par un appel à [IMetaDataImport2::GetPEKind](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-getpekind-method.md).</span><span class="sxs-lookup"><span data-stu-id="f18fd-103">Contains values that describe a portable executable (PE) file, as returned from a call to [IMetaDataImport2::GetPEKind](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-getpekind-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f18fd-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f18fd-104">Syntax</span></span>  
  
```  
typedef enum CorPEKind {  
  
    peNot           = 0x00000000,  
    peILonly        = 0x00000001,  
    pe32BitRequired = 0x00000002,  
    pe32Plus        = 0x00000004,  
    pe32Unmanaged   = 0x00000008,  
    pe32BitPreferred= 0x00000010  
  
} CorPEKind;  
```  
  
## <a name="members"></a><span data-ttu-id="f18fd-105">Membres</span><span class="sxs-lookup"><span data-stu-id="f18fd-105">Members</span></span>  
  
|<span data-ttu-id="f18fd-106">Membre</span><span class="sxs-lookup"><span data-stu-id="f18fd-106">Member</span></span>|<span data-ttu-id="f18fd-107">Description</span><span class="sxs-lookup"><span data-stu-id="f18fd-107">Description</span></span>|  
|------------|-----------------|  
|`peNot`|<span data-ttu-id="f18fd-108">Indique qu’il ne s’agit pas d’un fichier PE.</span><span class="sxs-lookup"><span data-stu-id="f18fd-108">Indicates that this is not a PE file.</span></span>|  
|`peILOnly`|<span data-ttu-id="f18fd-109">Indique que ce fichier PE contient uniquement du code managé.</span><span class="sxs-lookup"><span data-stu-id="f18fd-109">Indicates that this PE file contains only managed code.</span></span>|  
|`pe32BitRequired`|<span data-ttu-id="f18fd-110">Indique que ce fichier PE effectue des appels de Win32.</span><span class="sxs-lookup"><span data-stu-id="f18fd-110">Indicates that this PE file makes Win32 calls.</span></span>|  
|`pe32Plus`|<span data-ttu-id="f18fd-111">Indique que ce fichier PE s’exécute sur une plateforme 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f18fd-111">Indicates that this PE file runs on a 64-bit platform.</span></span>|  
|`pe32Unmanaged`|<span data-ttu-id="f18fd-112">Indique que ce fichier exécutable portable est du code natif.</span><span class="sxs-lookup"><span data-stu-id="f18fd-112">Indicates that this PE file is native code.</span></span>|  
|<span data-ttu-id="f18fd-113">pe32BitPreferred</span><span class="sxs-lookup"><span data-stu-id="f18fd-113">pe32BitPreferred</span></span>|<span data-ttu-id="f18fd-114">Indique que ce fichier PE est indépendant de la plateforme et qu’il préfère être chargé dans un environnement 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f18fd-114">Indicates that this PE file is platform-neutral and prefers to be loaded in a 32-bit environment.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f18fd-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f18fd-115">Remarks</span></span>  
 <span data-ttu-id="f18fd-116">Ces valeurs peuvent être utilisées dans des combinaisons au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="f18fd-116">These values can be used in bitwise combinations.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f18fd-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f18fd-117">Requirements</span></span>  
 <span data-ttu-id="f18fd-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f18fd-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f18fd-119">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="f18fd-119">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="f18fd-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f18fd-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f18fd-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f18fd-121">See also</span></span>

- [<span data-ttu-id="f18fd-122">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="f18fd-122">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
