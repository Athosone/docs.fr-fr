---
title: IHostCrst, interface
ms.date: 03/30/2017
api_name:
- IHostCrst
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostCrst
helpviewer_keywords:
- IHostCrst interface [.NET Framework hosting]
ms.assetid: ac298ebd-0815-47e4-a823-30b31baab903
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 939f100e8ee386642a29c33827a8339caf0467b9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61967828"
---
# <a name="ihostcrst-interface"></a>IHostCrst, interface
Sert de représentation sous forme de l’hôte d’une section critique de thread.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[Enter, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostcrst-enter-method.md)|Passe à la section critique.|  
|[Leave, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostcrst-leave-method.md)|Quitte la section critique.|  
|[SetSpinCount, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostcrst-setspincount-method.md)|Définit le nombre de sélection numérique pour la section critique.|  
|[TryEnter, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostcrst-tryenter-method.md)|Tentatives de saisie de la section critique et signale la réussite ou l’échec immédiatement.|  
  
## <a name="remarks"></a>Notes  
 `IHostCrst` permet le common language runtime (CLR) de communiquer directement avec la représentation sous forme de l’hôte d’une section critique, au lieu d’utiliser les fonctions Win32 comme `EnterCriticalSection` ou `LeaveCriticalSection`.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICLRSyncManager, interface](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)
- [IHostSyncManager, interface](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)
- [Interfaces d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
