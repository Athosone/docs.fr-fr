---
title: IMetaDataAssemblyImport::GetManifestResourceProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.GetManifestResourceProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::GetManifestResourceProps
helpviewer_keywords:
- GetManifestResourceProps method [.NET Framework metadata]
- IMetaDataAssemblyImport::GetManifestResourceProps method [.NET Framework metadata]
ms.assetid: 00be4789-ac63-4397-b2ec-1629a5c5a585
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ba99d84686974b425bcdee0bbf4770e4843e1351
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59081656"
---
# <a name="imetadataassemblyimportgetmanifestresourceprops-method"></a>IMetaDataAssemblyImport::GetManifestResourceProps, méthode
Obtient le jeu de propriétés de la ressource de manifeste avec la signature de métadonnées spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetManifestResourceProps (  
    [in]  mdManifestResource   mdmr,   
    [out] LPWSTR               szName,   
    [in]  ULONG                cchName,   
    [out] ULONG                *pchName,   
    [out] mdToken              *ptkImplementation,   
    [out] DWORD                *pdwOffset,   
    [out] DWORD                *pdwResourceFlags  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `mdmr`  
 [in] Un `mdManifestResource` jeton qui représente la ressource pour laquelle obtenir les propriétés.  
  
 `szName`  
 [out] Le nom de la ressource.  
  
 `cchName`  
 [in] La taille, en caractères étendus de `szName`.  
  
 `pchName`  
 [out] Un pointeur vers le nombre de caractères étendus réellement retournés dans `szName`.  
  
 `ptkImplementation`  
 [out] Un pointeur vers un `mdFile` jeton ou un `mdAssemblyRef` jeton qui représente le fichier ou l’assembly, respectivement, qui contient la ressource.  
  
 `pdwOffset`  
 [out] Pointeur vers une valeur qui spécifie l’offset de début de la ressource dans le fichier.  
  
 `pdwResourceFlags`  
 [out] Un pointeur vers les indicateurs qui décrivent les métadonnées appliquées à une ressource. La valeur des indicateurs est une combinaison d’une ou plusieurs [CorManifestResourceFlags](../../../../docs/framework/unmanaged-api/metadata/cormanifestresourceflags-enumeration.md) valeurs.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IMetaDataAssemblyImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)
