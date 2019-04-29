---
title: IManagedObject::GetObjectIdentity, méthode
ms.date: 03/30/2017
api_name:
- IManagedObject.GetObjectIdentity
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- GetObjectIdentity
helpviewer_keywords:
- GetObjectIdentity method [.NET Framework hosting]
- IManagedObject::GetObjectIdentity method [.NET Framework hosting]
ms.assetid: b862ff3e-e480-4cdf-84e2-e1013334a467
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6d014d2900ea790f84331ed933143513ae9e63f7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61943511"
---
# <a name="imanagedobjectgetobjectidentity-method"></a>IManagedObject::GetObjectIdentity, méthode
Obtient l’identité de cet objet managé.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetObjectIdentity (  
    [out] BSTR*   pBSTRGUID,  
    [out] int*    AppDomainID,  
    [out] CCW_PTR pCCW  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pBSTRGUID`  
 [out] Un pointeur vers le GUID du processus dans lequel réside l’objet.  
  
 `AppDomainID`  
 [out] Pointeur vers l’ID de l’objet domaine d’application.  
  
 `pCCW`  
 [out] Pointeur vers l’index de l’objet dans la v-table classique COM.  
  
## <a name="remarks"></a>Notes  
 L’identité d’un objet managé inclut les GUID du processus, les ID de domaine d’application et les index de l’objet dans la v-table classique COM.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IManagedObject, interface](../../../../docs/framework/unmanaged-api/hosting/imanagedobject-interface.md)
