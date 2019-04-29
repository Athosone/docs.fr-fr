---
title: COR_IL_MAP, structure
ms.date: 03/30/2017
api_name:
- COR_IL_MAP
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_IL_MAP
helpviewer_keywords:
- COR_IL_MAP structure [.NET Framework debugging]
ms.assetid: 534ebc17-963d-4b26-8375-8cd940281db3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e6d8023c7ac6d917c9df40fb18316ddc12df5ec1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61609422"
---
# <a name="corilmap-structure"></a>COR_IL_MAP, structure
Spécifie des modifications dans le décalage relatif d'une fonction.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef struct _COR_IL_MAP {  
    ULONG32 oldOffset;   
    ULONG32 newOffset;   
    BOOL    fAccurate;  
} COR_IL_MAP;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`oldOffset`|L’ancien intermediate langage MSIL (Microsoft) décalage par rapport au début de la fonction.|  
|`newOffset`|Le nouveau décalage MSIL par rapport au début de la fonction.|  
|`fAccurate`|`true` Si le mappage est connu pour être précis ; Sinon, `false`.|  
  
## <a name="remarks"></a>Notes  
 Le format de la carte est comme suit : Le débogueur suppose que `oldOffset` fait référence à un offset MSIL dans le code MSIL non modifié d’origine. Le `newOffset` paramètre fait référence à l’offset MSIL correspondant dans le nouveau code instrumenté.  
  
 Pour l’exécution pas à pas pour fonctionner correctement, les conditions suivantes doivent être remplies :  
  
- Le mappage doit être trié dans l’ordre croissant.  
  
- Code MSIL instrumenté ne doit pas être réorganisé.  
  
- Code MSIL d’origine ne doit pas être supprimé.  
  
- Le mappage doit inclure des entrées pour tous les points de séquence fichier de programme (PDB) de la base de données de la carte.  
  
 Le mappage n’interpole pas les entrées manquantes. L’exemple suivant montre un mappage et ses résultats.  
  
 Carte :  
  
- ancien offset 0, 0 nouveau décalage  
  
- ancien offset 5, 10 nouveau décalage  
  
- ancien offset 9, 20 nouveau décalage  
  
 Résultats :  
  
- Un ancien offset de 0, 1, 2, 3 ou 4 sera mappé à un nouveau décalage de 0.  
  
- Un ancien offset de 5, 6, 7 ou 8 sera mappé à nouveau décalage de 10.  
  
- Un ancien offset de 9 ou version ultérieure sera mappé à nouveau décalage de 20.  
  
- Un nouveau décalage de 0, 1, 2, 3, 4, 5, 6, 7, 8 ou 9 sera mappé à l’ancien offset 0.  
  
- Un nouveau décalage de 10, 11, 12, 13, 14, 15, 16, 17, 18 ou 19 sera mappé à l’ancien offset 5.  
  
- Un nouveau décalage supérieur ou égal à 20 sera mappé à l’ancien offset 9.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorProf.idl  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Structures de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
- [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
