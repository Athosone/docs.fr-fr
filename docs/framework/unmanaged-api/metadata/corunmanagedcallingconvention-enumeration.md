---
title: CorUnmanagedCallingConvention, énumération
ms.date: 03/30/2017
api_name:
- CorUnmanagedCallingConvention
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorUnmanagedCallingConvention
helpviewer_keywords:
- CorUnmanagedCallingConvention enumeration [.NET Framework metadata]
ms.assetid: 83058790-160b-4703-a5eb-74b66acbdfa9
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ff308a81282a1cc14c35583daf9cbb057149e556
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59178449"
---
# <a name="corunmanagedcallingconvention-enumeration"></a>CorUnmanagedCallingConvention, énumération
Spécifie les conventions d’appel du code non managé.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum CorUnmanagedCallingConvention {  
  
    IMAGE_CEE_UNMANAGED_CALLCONV_C         = 0x1,  
    IMAGE_CEE_UNMANAGED_CALLCONV_STDCALL   = 0x2,  
    IMAGE_CEE_UNMANAGED_CALLCONV_THISCALL  = 0x3,  
    IMAGE_CEE_UNMANAGED_CALLCONV_FASTCALL  = 0x4,  
  
    IMAGE_CEE_CS_CALLCONV_C                = 0x1,  
    IMAGE_CEE_CS_CALLCONV_STDCALL          = 0x2,  
    IMAGE_CEE_CS_CALLCONV_THISCALL         = 0x3,  
    IMAGE_CEE_CS_CALLCONV_FASTCALL         = 0x4  
  
} CorUnmanagedCallingConvention;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`IMAGE_CEE_UNMANAGED_CALLCONV_C`|La convention d’appel langage C.|  
|`IMAGE_CEE_UNMANAGED_CALLCONV_STDCALL`|La convention d’appel standard.|  
|`IMAGE_CEE_UNMANAGED_CALLCONV_THISCALL`|« Thie » convention d’appel.|  
|`IMAGE_CEE_UNMANAGED_CALLCONV_FASTCALL`|La convention d’appel « rapide ».|  
|`IMAGE_CEE_CS_CALLCONV_C`|Non utilisé.|  
|`IMAGE_CEE_CS_CALLCONV_STDCALL`|Non utilisé.|  
|`IMAGE_CEE_CS_CALLCONV_THISCALL`|Non utilisé.|  
|`IMAGE_CEE_CS_CALLCONV_FASTCALL`|Non utilisé.|  
  
## <a name="remarks"></a>Notes  
 Le CLR ne prend pas en charge la convention d’appel « rapide » dans le .NET Framework version 1.0.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorHdr.h  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Énumérations de métadonnées](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
