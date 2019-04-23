---
title: IAssemblyEnum::GetNextAssembly, méthode
ms.date: 03/30/2017
api_name:
- IAssemblyEnum.GetNextAssembly
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyEnum::GetNextAssembly
helpviewer_keywords:
- GetNextAssembly method [.NET Framework fusion]
- IAssemblyEnum::GetNextAssembly method [.NET Framework fusion]
ms.assetid: 5d7a4ca2-5f46-4ef1-a9a2-257884e9dc11
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9a77e468363b59e76e55aa24d97d064189ad297e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59117740"
---
# <a name="iassemblyenumgetnextassembly-method"></a>IAssemblyEnum::GetNextAssembly, méthode
Obtient un pointeur vers la prochaine [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) contenues dans cette [IAssemblyEnum](../../../../docs/framework/unmanaged-api/fusion/iassemblyenum-interface.md) objet.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetNextAssembly (  
    [in]  LPVOID          pvReserved,  
    [out] IAssemblyName   **ppName,  
    [in]  DWORD           dwFlags  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pvReserved`  
 [in] Réservé pour une extensibilité future. `pvReserved` doit être une référence null.  
  
 `ppName`  
 [out] Retourné `IAssemblyName` pointeur.  
  
 `dwFlags`  
 [in] Réservé pour une extensibilité future. `dwFlags` doit être 0 (zéro).  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Fusion.h  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IAssemblyName, interface](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)
- [IAssemblyEnum, interface](../../../../docs/framework/unmanaged-api/fusion/iassemblyenum-interface.md)
