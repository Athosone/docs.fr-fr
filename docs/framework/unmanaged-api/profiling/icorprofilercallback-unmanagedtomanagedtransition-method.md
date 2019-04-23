---
title: ICorProfilerCallback::UnmanagedToManagedTransition, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.UnmanagedToManagedTransition
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::UnmanagedToManagedTransition
helpviewer_keywords:
- ICorProfilerCallback::UnmanagedToManagedTransition method [.NET Framework profiling]
- UnmanagedToManagedTransition method [.NET Framework profiling]
ms.assetid: ade2cc01-9b81-4e09-a5f9-b3b9dda27e96
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 312f133c263becfd815f1b4ad48dff4892963aaf
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59227845"
---
# <a name="icorprofilercallbackunmanagedtomanagedtransition-method"></a>ICorProfilerCallback::UnmanagedToManagedTransition, méthode
Notifie le profileur qu’une transition du code non managé au code managé s’est produite.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT UnmanagedToManagedTransition(  
    [in] FunctionID functionId,  
    [in] COR_PRF_TRANSITION_REASON reason);  
```  
  
## <a name="parameters"></a>Paramètres  
 `functionId`  
 [in] L’ID de la fonction est appelée.  
  
 `reason`  
 [in] Une valeur de la [COR_PRF_TRANSITION_REASON](../../../../docs/framework/unmanaged-api/profiling/cor-prf-transition-reason-enumeration.md) énumération qui indique si la transition s’est produite en raison d’un appel dans le code managé à partir de code non managé, ou en raison d’un retour à partir d’une fonction non managée appelée par un objet managé.  
  
## <a name="remarks"></a>Notes  
 Si la valeur de `reason` est COR_PRF_TRANSITION_RETURN et `functionId` n’est ne pas null, la fonction ID est celle de la fonction non managée et n’a jamais été compilé à l’aide du compilateur juste-à-temps (JIT). Fonctions non managées ont des informations de base qui s’y rapportent, comme un nom et des métadonnées.  
  
 Si la valeur de `reason` est COR_PRF_TRANSITION_CALL, il est possible que la fonction appelée (autrement dit, la fonction managée) n’a pas encore été compilé par JIT.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorProfilerCallback, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [ManagedToUnmanagedTransition, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-managedtounmanagedtransition-method.md)
- [Utilisation d’un PInvoke explicite en C++ (attribut DllImport)](/cpp/dotnet/using-explicit-pinvoke-in-cpp-dllimport-attribute)
- [Utilisation de l’interopérabilité C++ (PInvoke implicite)](/cpp/dotnet/using-cpp-interop-implicit-pinvoke)
