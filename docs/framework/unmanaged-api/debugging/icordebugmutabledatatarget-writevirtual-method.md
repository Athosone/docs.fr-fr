---
title: ICorDebugMutableDataTarget::WriteVirtual, méthode
ms.date: 03/30/2017
ms.assetid: 80833648-58a7-491a-8dc8-9a48e9bb3adc
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2fba970de6e5882d3cbe9be17b5b49be5a3e81aa
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59171650"
---
# <a name="icordebugmutabledatatargetwritevirtual-method"></a>ICorDebugMutableDataTarget::WriteVirtual, méthode
Écrit la mémoire dans l'espace d'adressage du processus cible.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT WriteVirtual(  
   [in] CORDB_ADDRESS address,  
   [in, size_is(bytesRequested)] const BYTE * pBuffer,  
   [in] ULONG32 bytesRequested);  
```  
  
## <a name="parameters"></a>Paramètres  
 `address`  
 [in] Adresse à laquelle le contenu de `pBuffer` doit être écrit.  
  
 `pBuffer`  
 [in] Pointeur vers un tableau d'octets contenant les octets à écrire.  
  
 `address`  
 [in] Nombre d'octets dans `pBuffer`.  
  
## <a name="return-value"></a>Valeur de retour  
 `S_OK` en cas de réussite ou tout autre `HRESULT` en cas d'échec.  
  
## <a name="remarks"></a>Notes  
 Si des octets ne peuvent pas être écrits, l'appel de méthode échoue sans aucune modification des octets dans l'espace d'adressage cible. (Sinon, la cible se retrouve dans un état incohérent qui rend toute opération de débogage supplémentaire peu fiable.)  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorDebugMutableDataTarget, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugmutabledatatarget-interface.md)
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
