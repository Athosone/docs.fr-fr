---
title: ICorProfilerCallback::RootReferences, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RootReferences
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RootReferences
helpviewer_keywords:
- RootReferences method [.NET Framework profiling]
- ICorProfilerCallback::RootReferences method [.NET Framework profiling]
ms.assetid: dbdf853b-d1a4-4828-8ef7-53d121d8e6ae
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b616017745d7cc33d57b1626b6c27c59a0a60a32
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59091170"
---
# <a name="icorprofilercallbackrootreferences-method"></a>ICorProfilerCallback::RootReferences, méthode
Notifie le profileur avec les informations concernant les références racine après le garbage collection.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT RootReferences(  
    [in] ULONG    cRootRefs,  
    [in, size_is(cRootRefs)] ObjectID rootRefIds[] );  
```  
  
## <a name="parameters"></a>Paramètres  
 `cRootRefs`  
 [in] Le nombre de références dans le `rootRefIds` tableau.  
  
 `rootRefIds`  
 [in] Tableau d’ID d’objet qui font référence à un objet statique ou un objet sur la pile.  
  
## <a name="remarks"></a>Notes  
 Les deux `RootReferences` et [ICorProfilerCallback2::RootReferences2](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-rootreferences2-method.md) sont appelées pour notifier le profileur. Les profileurs implémenteront normalement une ou l’autre, mais pas les deux, car les informations passées dans `RootReferences2` est un sur-ensemble de celles passées dans `RootReferences`.  
  
 Il est possible pour le `rootRefIds` tableau destiné à contenir un objet null. Par exemple, toutes les références d’objet déclarées sur la pile sont traités comme des racines par le garbage collector et seront toujours signalées.  
  
 Les ID d’objet retourné par `RootReferences` ne sont pas valides pendant le rappel lui-même, car le garbage collection peut être occupé à déplacer les objets des anciennes adresses vers de nouvelles adresses. Par conséquent, les profileurs ne doivent pas essayer d’inspecter les objets pendant un `RootReferences` appeler. Lorsque [ICorProfilerCallback2::GarbageCollectionFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionfinished-method.md) est appelée, tous les objets ont été déplacés vers leurs nouveaux emplacements et peuvent être inspectés sans risque.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorProfilerCallback, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
