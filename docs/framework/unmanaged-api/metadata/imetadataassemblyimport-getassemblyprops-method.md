---
title: IMetaDataAssemblyImport::GetAssemblyProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.GetAssemblyProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::GetAssemblyProps
helpviewer_keywords:
- GetAssemblyProps method [.NET Framework metadata]
- IMetaDataAssemblyImport::GetAssemblyProps method [.NET Framework metadata]
ms.assetid: 0eaa4aa9-9441-444a-920c-e4b2a2db899e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4817a62d276bfdb50bfcbf658f40f5568673bea0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59163213"
---
# <a name="imetadataassemblyimportgetassemblyprops-method"></a>IMetaDataAssemblyImport::GetAssemblyProps, méthode
Obtient le jeu de propriétés pour l’assembly avec la signature de métadonnées spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetAssemblyProps (  
    [in]  mdAssembly          mda,  
    [out] const void          **ppbPublicKey,   
    [out] ULONG               *pcbPublicKey,  
    [out] ULONG               *pulHashAlgId,  
    [out] LPWSTR              szName,  
    [in] ULONG                cchName,  
    [out] ULONG               *pchName,  
    [out] ASSEMBLYMETADATA    *pMetaData,  
    [out] DWORD               *pdwAssemblyFlags  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `mda`  
 [in]. Le `mdAssembly` jeton de métadonnées qui représente l’assembly pour lequel obtenir les propriétés.  
  
 `ppbPublicKey`  
 [out] Pointeur vers la clé publique ou le jeton de métadonnées.  
  
 `pcbPublicKey`  
 [out] Le nombre d’octets dans la clé publique retournée.  
  
 `pulHashAlgId`  
 [out] Pointeur vers l’algorithme utilisé pour hacher les fichiers dans l’assembly.  
  
 `szName`  
 [out] Le nom simple de l’assembly.  
  
 `cchName`  
 [in] La taille, en caractères étendus de `szName`.  
  
 `pchName`  
 [out] Le nombre de caractères étendus réellement retournés dans `szName`.  
  
 `pMetaData`  
 [out] Pointeur vers une structure ASSEMBLYMETADATA qui contient les métadonnées de l’assembly.  
  
 `pdwAssemblyFlags`  
 [out] Indicateurs qui décrivent les métadonnées appliquées à un assembly. Cette valeur est une combinaison d’une ou plusieurs [CorAssemblyFlags](../../../../docs/framework/unmanaged-api/metadata/corassemblyflags-enumeration.md) valeurs.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IMetaDataAssemblyImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)
