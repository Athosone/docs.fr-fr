---
title: ICorProfilerInfo::SetILFunctionBody, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.SetILFunctionBody
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::SetILFunctionBody
helpviewer_keywords:
- ICorProfilerInfo::SetILFunctionBody method [.NET Framework profiling]
- SetILFunctionBody method [.NET Framework profiling]
ms.assetid: b159c712-00f4-4fc7-a990-40bf9f642e8f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d10bb7033688efce9488078d2ef605e2a29382f6
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61792650"
---
# <a name="icorprofilerinfosetilfunctionbody-method"></a>ICorProfilerInfo::SetILFunctionBody, méthode
Remplace le corps de la fonction spécifiée dans le module spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT SetILFunctionBody(  
    [in] ModuleID    moduleId,  
    [in] mdMethodDef methodid,  
    [in] LPCBYTE     pbNewILMethodHeader);  
```  
  
## <a name="parameters"></a>Paramètres  
 `moduleId`  
 [in] L’ID du module dans lequel la fonction réside.  
  
 `methodid`  
 [in] Le jeton de la fonction pour laquelle remplacer le corps.  
  
 `pbNewILMethodHeader`  
 [in] Le nouvel en-tête pour la fonction.  
  
## <a name="remarks"></a>Notes  
 Le `SetILFunctionBody` méthode remplace l’adresse virtuelle relative de la fonction dans les métadonnées afin qu’il pointe vers le nouveau corps de fonction et ajuste les structures de données internes en fonction des besoins.  
  
 Le `SetILFunctionBody` méthode peut être appelée uniquement sur les fonctions qui n’ont jamais été compilées par un compilateur juste-à-temps (JIT).  
  
 Utilisez le [ICorProfilerInfo::GetILFunctionBodyAllocator](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-getilfunctionbodyallocator-method.md) méthode pour allouer de l’espace pour la nouvelle méthode pour vous assurer que la mémoire tampon est compatible.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorProfilerInfo, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
