---
title: HOST_TYPE, énumération
ms.date: 03/30/2017
api_name:
- HOST_TYPE
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- HOST_TYPE
helpviewer_keywords:
- HOST_TYPE enumeration [.NET Framework hosting]
ms.assetid: 51f848be-84c5-4036-9839-c762c576bbf5
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: dfb1cff3e95c5ff86d22913745b7d14982766b48
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61968599"
---
# <a name="hosttype-enumeration"></a>HOST_TYPE, énumération
Contient des valeurs qui spécifient le type d’hôte qui lance une application.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum {  
    HOST_TYPE_DEFAULT     = 0x0,  
    HOST_TYPE_APPLAUNCH   = 0x1,  
    HOST_TYPE_CORFLAG     = 0x2  
} HOST_TYPE;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`HOST_TYPE_APPLAUNCH`|Lancez l’application à partir de AppLaunch.exe.<br /><br /> Utilisez cette valeur pour les applications de confiance partielle.|  
|`HOST_TYPE_CORFLAG`|Lancez l’application directement. Autrement dit, lancez l’application à partir de son propre fichier .exe.<br /><br /> Utilisez cette valeur pour les applications de confiance.|  
|`HOST_TYPE_DEFAULT`|Identique à HOST_TYPE_APPLAUNCH.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Énumérations d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
