---
title: ICorProfilerInfo::GetAssemblyInfo, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetAssemblyInfo
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- GetAssemblyInfo Method
helpviewer_keywords:
- GetAssemblyInfo method [.NET Framework profiling]
- ICorProfilerInfo::GetAssemblyInfo method [.NET Framework profiling]
ms.assetid: 7a3c97c3-1e31-47b1-bf23-386785c509c4
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ad4ebe4e1255ce13974063eef3d0a4feeb5dd92b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62049620"
---
# <a name="icorprofilerinfogetassemblyinfo-method"></a>ICorProfilerInfo::GetAssemblyInfo, méthode
Accepte un ID d'assembly et retourne le nom de l'assembly et l'ID de son module de manifeste.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetAssemblyInfo(  
    [in]  AssemblyID  assemblyId,  
    [in]  ULONG       cchName,  
    [out] ULONG       *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]  
          WCHAR       szName[] ,  
    [out] AppDomainID *pAppDomainId,  
    [out] ModuleID    *pModuleId);  
```  
  
## <a name="parameters"></a>Paramètres  
 `assemblyId`  
 [in] Identificateur de l'assembly.  
  
 `cchName`  
 [in] Longueur, en caractères, de `szName`.  
  
 `pcchName`  
 [out] Pointeur vers la longueur totale en caractères du nom de l'assembly.  
  
 `szName`  
 [out] Mémoire tampon de caractères larges fournie par l'appelant. Suite au retour de la méthode, celle-ci contient le nom de l'assembly.  
  
 `pAppDomainId`  
 [out] Pointeur vers l'ID du domaine d'application qui contient l'assembly.  
  
 `pModuleId`  
 [out] Pointeur vers l'ID du module du manifeste de l'assembly.  
  
## <a name="remarks"></a>Notes  
 Suite au retour de cette méthode, vous devez vérifier que la mémoire tampon `szName` est suffisamment grande pour contenir le nom complet de l'assembly. Pour ce faire, comparez la valeur vers laquelle `pcchName` pointe à celle du paramètre `cchName`. Si `pcchName` pointe vers une valeur supérieure à `cchName`, allouez une mémoire tampon `szName` plus grande, mettez à jour `cchName` pour refléter la nouvelle taille et rappelez `GetAssemblyInfo`.  
  
 Vous pouvez également commencer par appeler `GetAssemblyInfo` avec un tampon `szName` de longueur nulle pour obtenir la taille correcte du tampon. Vous pouvez ensuite ajuster la taille de la mémoire tampon en fonction de la valeur retournée dans `pcchName` et rappeler `GetAssemblyInfo`.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorProfilerInfo, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
- [Interfaces de profilage](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [Profilage](../../../../docs/framework/unmanaged-api/profiling/index.md)
