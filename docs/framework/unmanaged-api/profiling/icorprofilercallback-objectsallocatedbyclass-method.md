---
title: ICorProfilerCallback::ObjectsAllocatedByClass, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ObjectsAllocatedByClass
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ObjectsAllocatedByClass
helpviewer_keywords:
- ObjectsAllocatedByClass method [.NET Framework profiling]
- ICorProfilerCallback::ObjectsAllocatedByClass method [.NET Framework profiling]
ms.assetid: 91d688f3-a80e-419d-9755-ff94bc04188a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b9f5d2c08abbcab6bc1a6d0569b8e70d7c919def
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59195863"
---
# <a name="icorprofilercallbackobjectsallocatedbyclass-method"></a>ICorProfilerCallback::ObjectsAllocatedByClass, méthode
Informe le profileur sur le nombre d’instances de chaque classe spécifiée qui ont été créés depuis le dernier garbage collection.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT ObjectsAllocatedByClass(  
    [in] ULONG   cClassCount,  
    [in, size_is(cClassCount)] ClassID classIds[] ,  
    [in, size_is(cClassCount)] ULONG   cObjects[] );  
```  
  
## <a name="parameters"></a>Paramètres  
 `cClassCount`  
 [in] La taille de la `classIds` et `cObjects` tableaux.  
  
 `classIds`  
 [in] Tableau d’ID, où chaque ID spécifie une classe avec une ou plusieurs instances de classe.  
  
 `cObjects`  
 [in] Un tableau d’entiers, où chaque entier spécifie le nombre d’instances pour la classe correspondante dans le `classIds` tableau.  
  
## <a name="remarks"></a>Notes  
 Le `classIds` et `cObjects` tableaux sont des tableaux parallèles. Par exemple, `classIds[i]` et `cObjects[i]` référencent la même classe. Si aucune instance d’une classe n’a été créé depuis le dernier garbage collection, la classe est omise. Le `ObjectsAllocatedByClass` rappel ne signale pas les objets alloués dans le tas d’objets volumineux.  
  
 Les nombres signalés par `ObjectsAllocatedByClass` ne sont que des estimations. Pour des nombres exacts, utilisez [ICorProfilerCallback::ObjectAllocated](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-objectallocated-method.md).  
  
 Le `classIds` tableau peut contenir une ou plusieurs entrées null si le correspondant `cObjects` tableau possède des types qui sont le déchargement.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorProfilerCallback, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
