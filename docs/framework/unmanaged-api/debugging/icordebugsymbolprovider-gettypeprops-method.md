---
title: Icordebugsymbolprovider::gettypeprops, méthode
ms.date: 03/30/2017
ms.assetid: 35ac4140-91ea-4c77-b1c4-1daf41986ca5
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a5f9867dbdc244ed22948dbe9a07a7ea06292d6a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61994095"
---
# <a name="icordebugsymbolprovidergettypeprops-method"></a>Icordebugsymbolprovider::gettypeprops, méthode
Retourne des informations sur les propriétés d'un type, comme le nombre de signature de ses paramètres génériques, en fonction d'une adresse virtuelle relative (RVA) dans une vtable.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetTypeProps(  
   [in]  ULONG32 vtableRva,  
   [in]  ULONG32 cbSignature,  
   [out] ULONG32 *pcbSignature,  
   [out, size_is(cbSignature), length_is(*pcbSignature)] BYTE signature[]  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `tableRva`  
 [in] Adresse virtuelle relative (RVA) dans une vtable.  
  
 `cbSignature`  
 [in] Taille du tableau `signature`. Consultez la section Notes.  
  
 `pcbSignature`  
 [out] Pointeur vers la taille du tableau `signature` retourné.  
  
 `signature`  
 [out] Mémoire tampon qui conserve les signatures typespec de tous les paramètres génériques.  
  
## <a name="remarks"></a>Notes  
 Pour obtenir la taille requise du type `signature` de tableau, définissez la `cbSignature` argument à 0 et `signature` à **null**. Suite au retour de la méthode, `pcbSignature` contient le nombre d'octets requis pour le tableau `signature`.  
  
> [!NOTE]
>  Cette méthode est uniquement disponible avec .NET Native.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [GetMethodProps, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-getmethodprops-method.md)
- [ICorDebugSymbolProvider, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md)
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
