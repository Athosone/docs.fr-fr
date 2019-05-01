---
title: ICorProfilerCallback8::DynamicMethodJITCompilationFinished (méthode)
ms.date: 04/10/2018
api_name:
- ICorProfilerCallback8.DynamicMethodJITCompilationFinished
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9dbe8d4f7050b93ffb34280be6d63367ef294ae8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62049711"
---
# <a name="icorprofilercallback8dynamicmethodjitcompilationfinished-method"></a>ICorProfilerCallback8::DynamicMethodJITCompilationFinished (méthode)
[Pris en charge dans le .NET Framework 4.7 et versions ultérieures]  
  
Notifie le profileur chaque fois que la compilation JIT d’une méthode dynamique est terminée.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT DynamicMethodJITCompilationFinished(  
     [in]  FunctionID  functionId,   
     [in]  BOOL        hrStatus,   
     [in]  BOOL        fIsSafeToBlock   
);  
```  
  
## <a name="parameters"></a>Paramètres  
[in] `functionId`  
L’identificateur de la fonction en mémoire pour le JIT démarrage de la compilation.   

[in] `hrStatus`   
Une valeur qui indique si la compilation JIT a réussi.

[in] `fIsSafeToBlock`   
`true` pour indiquer que le blocage peut entraîner l’exécution pour attendre que le thread appelant retourner à partir de ce rappel ; `false` pour indiquer que le blocage n’affecte pas l’opération du runtime.  

## <a name="remarks"></a>Notes  

Ce rappel est déclenché chaque fois que la compilation JIT d’une méthode dynamique est terminée. Cela inclut diverses de stubs de langage intermédiaire et de méthodes LCG. Son objectif est de fournir les enregistreurs de profileur avec suffisamment d’informations pour identifier la méthode compilée pour les utilisateurs.

> [!NOTE]
> `functionId` les valeurs ne peut pas être permet de résoudre à leurs jetons de métadonnées, car les méthodes dynamiques ont pas de métadonnées.

## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  
  
## <a name="see-also"></a>Voir aussi

- [DynamicMethodJITCompilationStarted, méthode](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md)
- [ICorProfilerCallback8, interface](icorprofilercallback8-interface.md)
