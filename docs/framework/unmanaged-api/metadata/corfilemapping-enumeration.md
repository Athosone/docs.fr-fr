---
title: CorFileMapping, énumération
ms.date: 03/30/2017
api_name:
- CorFileMapping
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorFileMapping
helpviewer_keywords:
- CorFileMapping enumeration [.NET Framework metadata]
ms.assetid: 3ca41592-b8da-475a-8032-a15627730003
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a3056836d289383161f9fa538c3c6349f88b6ba6
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61905734"
---
# <a name="corfilemapping-enumeration"></a>CorFileMapping, énumération
Contient des valeurs qui décrivent le type de mappage de fichier est retourné à partir d’un appel à la [IMetaDataInfo::GetFileMapping](../../../../docs/framework/unmanaged-api/metadata/imetadatainfo-getfilemapping-method.md) (méthode).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum CorFileMapping {  
  
    fmFlat                  =   0x0000,  
    fmExecutableImage       =   0x0001  
  
} CorFileMapping;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`fmFlat`|Le fichier est mappé comme un fichier de données. Autrement dit, le `SEC_IMAGE` indicateur n’a pas été transmis à Microsoft Win32 `CreateFileMapping` (fonction).|  
|`fmExecutableImage`|Le fichier est mappé pour l’exécution, en utilisant le `LoadLibrary` (fonction) ou le `CreateFileMapping` fonctionne avec le `SEC_IMAGE` indicateur.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorHdr.h  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Énumérations de métadonnées](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
- [GetFileMapping, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatainfo-getfilemapping-method.md)
