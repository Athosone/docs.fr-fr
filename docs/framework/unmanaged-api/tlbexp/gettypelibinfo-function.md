---
title: Fonction GetTypeLibInfo
ms.date: 03/30/2017
api_name:
- GetTypeLibInfo
api_location:
- TlbRef.dll
api_type:
- DLLExport
f1_keywords:
- GetTypeLibInfo
helpviewer_keywords:
- GetTypeLibInfo function [.NET Framework]
ms.assetid: a1c4d165-9bdc-4ca8-940e-292d4ffcc338
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d12cbb66464baba4ee706ccb076764fbf025fc5f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61786176"
---
# <a name="gettypelibinfo-function"></a>Fonction GetTypeLibInfo
Retourne des informations sur la bibliothèque de types spécifiée en examinant sa [TLIBATTR](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/ns-oaidl-tagtlibattr) structure.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetTypeLibInfo(  
    [in]   LPWSTR     szFile,  
    [out]  GUID      *pTypeLibID,  
    [out]  LCID      *pTypeLibLCID,  
    [out]  SYSKIND   *pTypeLibPlatform,  
    [out]  USHORT    *pTypeLibMajorVer,  
    [out]  USHORT    *pTypeLibMinorVer  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `szFile`  
 [in] Le nom de fichier de la bibliothèque de types.  
  
 `pTypeLibID`  
 [out] Le GUID de la bibliothèque de types.  
  
 `pTypeLibLCID`  
 [out] ID de localisation de la bibliothèque de types.  
  
 `pTypeLibPlatform`  
 [out] Un [SYSKIND](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/ne-oaidl-tagsyskind) indicateur qui identifie le système d’exploitation cible pour la bibliothèque de types. Les valeurs courantes sont SYS_WIN32 et SYS_WIN64.  
  
 `pTypeLibMajorVer`  
 [out] Numéro de version principale de la bibliothèque de types. Par exemple, pour la version *x.y*, le numéro de version majeure est *x*.  
  
 `pTypeLibMinorVer`  
 [out] Numéro de version secondaire de la bibliothèque de types. Par exemple, pour la version *x.y*, le numéro de version mineure est *y*.  
  
## <a name="remarks"></a>Notes  
 Le `GetTypeLibInfo` fonction est appelée par le [Tlbexp.exe (exportateur)](../../../../docs/framework/tools/tlbexp-exe-type-library-exporter.md). Cet outil génère une bibliothèque de types décrivant les types dans un assembly du common language runtime (CLR).  
  
 Si un paramètre est null, la fonction retourne un `HRESULT` de `E_POINTER`. Sinon, il retourne `S_OK`.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** TlbRef.h  
  
 **Bibliothèque :** TlbRef.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Fonctions d’assistance Tlbexp](../../../../docs/framework/unmanaged-api/tlbexp/index.md)
- [LoadTypeLibEx de le dont (fonction)](https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-loadtypelibex)
