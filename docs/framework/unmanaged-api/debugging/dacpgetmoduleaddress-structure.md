---
title: DacpGetModuleAddress Structure
ms.date: 01/16/2019
api.name:
- DacpGetModuleAddress Structure
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- DacpGetModuleAddress Structure
helpviewer.keywords:
- DacpGetModuleAddress Structure [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: cbea6c0562c68ae5d18247dc97bc53eb9dfbfd7e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61965932"
---
# <a name="dacpgetmoduleaddress-structure"></a>DacpGetModuleAddress Structure

Définit le conteneur pour une demande d’adresse de module.

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>Syntaxe

```
struct DacpGetModuleAddress
{
    CLRDATA_ADDRESS ModulePtr;
};
```

## <a name="members"></a>Membres

| Membre      | Description                |
| ----------- | -------------------------- |
| `ModulePtr` | Pointeur vers le module. |

## <a name="methods"></a>Méthodes

| Méthode                                                                                               | Description                                                                    |
| ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| [Requête](../../../../docs/framework/unmanaged-api/debugging/dacpgetmoduleaddress-request-method.md) | Exécute une requête pour remplir la structure à partir de la structure de runtime donné. |

## <a name="remarks"></a>Notes

Cette structure se trouve au sein du runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque. Pour l’utiliser, définir la structure comme indiqué ci-dessus, où `CLRDATA_ADDRESS` est un entier non signé 64 bits.

## <a name="requirements"></a>Configuration requise
**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
**En-tête :** Aucun.  
**Bibliothèque :** Aucun.  
**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a>Voir aussi

- [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [Structures de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
