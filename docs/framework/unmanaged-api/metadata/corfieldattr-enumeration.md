---
title: CorFieldAttr, énumération
ms.date: 03/30/2017
api_name:
- CorFieldAttr
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorFieldAttr
helpviewer_keywords:
- CorFieldAttr enumeration [.NET Framework metadata]
ms.assetid: 6ae2c4be-212c-4e74-9288-40a11dc26522
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 432e202eb8db105e8d56d3d36cdc8001bac5320c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59182375"
---
# <a name="corfieldattr-enumeration"></a><span data-ttu-id="364de-102">CorFieldAttr, énumération</span><span class="sxs-lookup"><span data-stu-id="364de-102">CorFieldAttr Enumeration</span></span>
<span data-ttu-id="364de-103">Contient des valeurs qui décrivent les métadonnées concernant un champ.</span><span class="sxs-lookup"><span data-stu-id="364de-103">Contains values that describe metadata about a field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="364de-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="364de-104">Syntax</span></span>  
  
```  
typedef enum CorFieldAttr {  
  
    fdFieldAccessMask           =   0x0007,  
    fdPrivateScope              =   0x0000,  
    fdPrivate                   =   0x0001,  
    fdFamANDAssem               =   0x0002,  
    fdAssembly                  =   0x0003,  
    fdFamily                    =   0x0004,  
    fdFamORAssem                =   0x0005,  
    fdPublic                    =   0x0006,  
  
    fdStatic                    =   0x0010,  
    fdInitOnly                  =   0x0020,  
    fdLiteral                   =   0x0040,  
    fdNotSerialized             =   0x0080,  
  
    fdSpecialName               =   0x0200,  
  
    fdPinvokeImpl               =   0x2000,  
  
    fdReservedMask              =   0x9500,  
    fdRTSpecialName             =   0x0400,  
    fdHasFieldMarshal           =   0x1000,  
    fdHasDefault                =   0x8000,  
    fdHasFieldRVA               =   0x0100  
  
} CorFieldAttr;  
```  
  
## <a name="members"></a><span data-ttu-id="364de-105">Membres</span><span class="sxs-lookup"><span data-stu-id="364de-105">Members</span></span>  
  
|<span data-ttu-id="364de-106">Membre</span><span class="sxs-lookup"><span data-stu-id="364de-106">Member</span></span>|<span data-ttu-id="364de-107">Description</span><span class="sxs-lookup"><span data-stu-id="364de-107">Description</span></span>|  
|------------|-----------------|  
|`fdFieldAccessMask`|<span data-ttu-id="364de-108">Spécifie les informations d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="364de-108">Specifies accessibility information.</span></span>|  
|`fdPrivateScope`|<span data-ttu-id="364de-109">Spécifie que le champ ne peut pas être référencé.</span><span class="sxs-lookup"><span data-stu-id="364de-109">Specifies that the field cannot be referenced.</span></span>|  
|`fdPrivate`|<span data-ttu-id="364de-110">Spécifie que le champ est accessible uniquement par son type parent.</span><span class="sxs-lookup"><span data-stu-id="364de-110">Specifies that the field is accessible only by its parent type.</span></span>|  
|`fdFamANDAssem`|<span data-ttu-id="364de-111">Spécifie que le champ est accessible par les classes dérivées dans son assembly.</span><span class="sxs-lookup"><span data-stu-id="364de-111">Specifies that the field is accessible by derived classes in its assembly.</span></span>|  
|`fdAssembly`|<span data-ttu-id="364de-112">Spécifie que le champ est accessible par tous les types dans son assembly.</span><span class="sxs-lookup"><span data-stu-id="364de-112">Specifies that the field is accessible by all types in its assembly.</span></span>|  
|`fdFamily`|<span data-ttu-id="364de-113">Spécifie que le champ est accessible uniquement par son type et classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="364de-113">Specifies that the field is accessible only by its type and derived classes.</span></span>|  
|`fdFamORAssem`|<span data-ttu-id="364de-114">Spécifie que le champ est accessible par les classes dérivées et par tous les types dans son assembly.</span><span class="sxs-lookup"><span data-stu-id="364de-114">Specifies that the field is accessible by derived classes and by all types in its assembly.</span></span>|  
|`fdPublic`|<span data-ttu-id="364de-115">Spécifie que le champ est accessible par tous les types avec une visibilité de cette étendue.</span><span class="sxs-lookup"><span data-stu-id="364de-115">Specifies that the field is accessible by all types with visibility of this scope.</span></span>|  
|`fdStatic`|<span data-ttu-id="364de-116">Spécifie que le champ est un membre de son type plutôt qu’un membre d’instance.</span><span class="sxs-lookup"><span data-stu-id="364de-116">Specifies that the field is a member of its type rather than an instance member.</span></span>|  
|`fdInitOnly`|<span data-ttu-id="364de-117">Spécifie que le champ ne peut pas être modifié après son initialisation.</span><span class="sxs-lookup"><span data-stu-id="364de-117">Specifies that the field cannot be changed after it is initialized.</span></span>|  
|`fdLiteral`|<span data-ttu-id="364de-118">Spécifie que la valeur du champ est une constante de compilation.</span><span class="sxs-lookup"><span data-stu-id="364de-118">Specifies that the field value is a compile-time constant.</span></span>|  
|`fdNotSerialized`|<span data-ttu-id="364de-119">Spécifie que le champ n’est pas sérialisé lorsque son type est exécutée à distant.</span><span class="sxs-lookup"><span data-stu-id="364de-119">Specifies that the field is not serialized when its type is remoted.</span></span>|  
|`fdSpecialName`|<span data-ttu-id="364de-120">Spécifie que le champ est spécial et que son nom décrit comment.</span><span class="sxs-lookup"><span data-stu-id="364de-120">Specifies that the field is special, and that its name describes how.</span></span>|  
|`fdPinvokeImpl`|<span data-ttu-id="364de-121">Spécifie que l’implémentation du champ est transmise via PInvoke.</span><span class="sxs-lookup"><span data-stu-id="364de-121">Specifies that the field implementation is forwarded through PInvoke.</span></span>|  
|`fdReservedMask`|<span data-ttu-id="364de-122">Réservé à un usage interne par le common language runtime.</span><span class="sxs-lookup"><span data-stu-id="364de-122">Reserved for internal use by the common language runtime.</span></span>|  
|`fdRTSpecialName`|<span data-ttu-id="364de-123">Spécifie que les métadonnées du common language runtime API internes doivent vérifier l’encodage du nom.</span><span class="sxs-lookup"><span data-stu-id="364de-123">Specifies that the common language runtime metadata internal APIs should check the encoding of the name.</span></span>|  
|`fdHasFieldMarshal`|<span data-ttu-id="364de-124">Spécifie que le champ contienne des informations de marshaling.</span><span class="sxs-lookup"><span data-stu-id="364de-124">Specifies that the field contains marshaling information.</span></span>|  
|`fdHasDefault`|<span data-ttu-id="364de-125">Spécifie que le champ a une valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="364de-125">Specifies that the field has a default value.</span></span>|  
|`fdHasFieldRVA`|<span data-ttu-id="364de-126">Spécifie que le champ a une adresse virtuelle relative.</span><span class="sxs-lookup"><span data-stu-id="364de-126">Specifies that the field has a relative virtual address.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="364de-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="364de-127">Requirements</span></span>  
 <span data-ttu-id="364de-128">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="364de-128">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="364de-129">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="364de-129">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="364de-130">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="364de-130">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="364de-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="364de-131">See also</span></span>

- [<span data-ttu-id="364de-132">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="364de-132">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
