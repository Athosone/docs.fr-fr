---
title: ICorDebugProcess4, interface
ms.date: 02/07/2019
api_name:
- ICorDebugProcess4
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess4
helpviewer_keywords:
- ICorDebugProcess4 interface [.NET Framework debugging]
topic_type:
- apiref
author: hoyosjs
ms.author: juhoyosa
ms.openlocfilehash: 1bdc958f2516bcd7c2eb74312fbf478e6d49535a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61948800"
---
# <a name="icordebugprocess4-interface"></a>ICorDebugProcess4, interface

Prend en charge hors de contrôle de l’exécution de processus.

## <a name="methods"></a>Méthodes

| Méthode                                                                 | Description                                                                                             |
| ---------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| [ProcessStateChanged](icordebugprocess4-processstatechanged-method.md) | Notifie le pipeline ICorDebug que hors du débogueur de processus se poursuit l’exécution du programme débogué. |

## <a name="remarks"></a>Notes

Cette interface réside dans le runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque. Toutefois, il est une interface COM qui dérive de `IUnknown` avec le GUID `E930C679-78AF-4953-8AB7-B0AABF0F9F80` qui peuvent être obtenues via les mécanismes COM habituels.

## <a name="requirements"></a>Configuration requise

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).

**En-tête :** Aucun.

**Bibliothèque :** Aucun.

**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v20plus-md.md)]

## <a name="see-also"></a>Voir aussi

- [Interfaces de débogage](debugging-interfaces.md)
- [Débogage](index.md)
