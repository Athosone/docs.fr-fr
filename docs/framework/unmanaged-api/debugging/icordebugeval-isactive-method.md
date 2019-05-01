---
title: ICorDebugEval::IsActive, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugEval.IsActive
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval::IsActive
helpviewer_keywords:
- IsActive method, ICorDebugEval interface [.NET Framework debugging]
- ICorDebugEval::IsActive method [.NET Framework debugging]
ms.assetid: bf2bba24-d278-43bd-b1c5-35680e748d3e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0d992ea86b3221af222bb01f1985fe277cea5a2c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61988983"
---
# <a name="icordebugevalisactive-method"></a>ICorDebugEval::IsActive, méthode
Obtient une valeur qui indique si cet objet ICorDebugEval est en cours d’exécution.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT IsActive (  
    [out] BOOL              *pbActive  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pbActive`  
 [out] Pointeur vers une valeur qui indique si cette version d’évaluation est active.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
