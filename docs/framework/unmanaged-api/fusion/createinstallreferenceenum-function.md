---
title: Fonction CreateInstallReferenceEnum
ms.date: 03/30/2017
api_name:
- CreateInstallReferenceEnum
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- DLLExport
f1_keywords:
- CreateInstallReference
helpviewer_keywords:
- CreateInstallReference function [.NET Framework fusion]
ms.assetid: 80dbbbf8-54fc-4894-b74a-0179d3201083
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d7820b33dcfacae5ede5235607e40d95940fc474
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61771902"
---
# <a name="createinstallreferenceenum-function"></a>Fonction CreateInstallReferenceEnum
Obtient un pointeur vers un [IInstallReferenceEnum](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceenum-interface.md) instance qui représente une liste de références d’une application à l’assembly spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT CreateInstallReferenceEnum (  
    [out] IInstallReferenceEnum **ppRefEnum,  
    [in]  IAssemblyName         *pName,  
    [in]  DWORD                 dwFlags,  
    [in]  LPVOID                pvReserved  
 );  
```  
  
## <a name="parameters"></a>Paramètres  
 `ppRefEnum`  
 [out] Retourné `IInstallReferenceEnum` pointeur.  
  
 `pName`  
 [in] Le [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) qui identifie l’assembly pour lequel énumérer des références.  
  
 `dwFlags`  
 [in] Indicateurs qui influencent le comportement de l’énumérateur.  
  
 `pvReserved`  
 [in] Réservé pour une extensibilité future. `pvReserved` doit être une référence null.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Fusion.h  
  
 **Bibliothèque :** Le fichier fusion.dll et Mscorwks.dll. Utilisez le fichier Fusion.dll plutôt que Mscorwks.dll pour vous assurer que vous ciblez la version correcte du .NET Framework.  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IInstallReferenceEnum, interface](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceenum-interface.md)
- [IAssemblyName, interface](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)
- [Fonctions statiques globales de fusion](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
