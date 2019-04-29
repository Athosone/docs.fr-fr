---
title: ICorDebugModule3::CreateReaderForInMemorySymbols, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugModule3.CreateReaderForInMemorySymbols
api_location:
- CorDebug.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule3::CreateReaderForInMemorySymbols
helpviewer_keywords:
- CreateReaderForInMemorySymbols method, ICorDebugModule3 interface [.NET Framework debugging]
- ICorDebugModule3::CreateReaderForInMemorySymbols method [.NET Framework debugging]
ms.assetid: af317171-d66d-4114-89eb-063554c74940
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ccfe83707b6354c42a4c3c81e911918b2ea79ec4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61942452"
---
# <a name="icordebugmodule3createreaderforinmemorysymbols-method"></a>ICorDebugModule3::CreateReaderForInMemorySymbols, méthode
Crée un lecteur de symboles de débogage pour un module dynamique.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT CreateReaderForInMemorySymbols (  
      [in] REFIID riid,  
      [out][iid_is(riid)] void **    ppObj  
```  
  
## <a name="parameters"></a>Paramètres  
 riid  
 [in] IID de l’interface COM à retourner. En règle générale, il s’agit d’un [ISymUnmanagedReader Interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md).  
  
 ppObj  
 [out] Pointeur vers un pointeur vers l’interface retournée.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK  
 Le lecteur a été créé avec succès.  
  
 CORDBG_E_MODULE_LOADED_FROM_DISK  
 Le module n’est pas un module en mémoire ou dynamique.  
  
 CORDBG_E_SYMBOLS_NOT_AVAILABLE  
 Symboles n’ont pas été fournis par l’application ou ne sont pas encore disponibles.  
  
 E_FAIL (ou autres codes de retour E_)  
 Impossible de créer le lecteur.  
  
## <a name="remarks"></a>Notes  
 Cette méthode peut également être utilisée pour créer un objet lecteur de symboles pour les modules en mémoire (non dynamique), mais uniquement une fois que les symboles sont tout d’abord disponibles (indiqué par le [UpdateModuleSymbols, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-updatemodulesymbols-method.md) rappel).  
  
 Cette méthode retourne une nouvelle instance de lecteur chaque fois qu’elle est appelée (comme [CComPtrBase::CoCreateInstance](/cpp/atl/reference/ccomptrbase-class#cocreateinstance)). Par conséquent, le débogueur doit mettre en cache le résultat et demander une nouvelle instance uniquement lorsque les données sous-jacentes peuvent avoir changé (autrement dit, quand un [LoadClass, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-loadclass-method.md) reçu de rappel).  
  
 Modules dynamiques n’ont pas de symboles disponibles jusqu'à ce que le premier type a été chargé (comme indiqué par le [LoadClass, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-loadclass-method.md) rappel).  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** 4.5, 4, 3.5 SP1  
  
## <a name="see-also"></a>Voir aussi

- [ICorDebugRemoteTarget, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugremotetarget-interface.md)
- [ICorDebug, interface](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)

- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
