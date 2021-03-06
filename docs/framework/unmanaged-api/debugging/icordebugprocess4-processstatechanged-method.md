---
title: ICorDebugProcess4::ProcessStateChanged (méthode)
ms.date: 02/07/2019
api_name:
- ICorDebugProcess4::ProcessStateChanged
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess4::ProcessStateChanged
helpviewer_keywords:
- ICorDebugProcess4::ProcessStateChanged method [.NET Framework debugging]
topic_type:
- apiref
author: hoyosjs
ms.author: juhoyosa
ms.openlocfilehash: b77dd1277e7d23729f30d9d495c5417055a22759
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61948801"
---
# <a name="icordebugprocess4processstatechanged-method"></a>ICorDebugProcess4::ProcessStateChanged (méthode)

Notifie le pipeline ICorDebug que hors du débogueur de processus se poursuit l’exécution du programme débogué.

## <a name="syntax"></a>Syntaxe

```
HRESULT ProcessStateChanged(
    [in] CorDebugStateChange change
);
```

## <a name="parameters"></a>Paramètres

 `eChange`\
[in] Un membre de la [cordebugstatechange, énumération](cordebugstatechange-enumeration.md) décrivant une modification dans l’état d’exécution du processus.

## <a name="remarks"></a>Notes

La méthode fournie fait partie de la `ICorDebugProcess4` interface et correspond à l’emplacement de quatrième de la table de la méthode virtuelle.

## <a name="requirements"></a>Configuration requise

 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).

 **En-tête :** Aucun.

 **Bibliothèque :** Aucun.
 
 **Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v20plus-md.md)]

## <a name="see-also"></a>Voir aussi

- [ICorDebugProcess4 Interface](icordebugprocess4-interface.md)
- [Interfaces de débogage](debugging-interfaces.md)
- [Débogage](index.md)