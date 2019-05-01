---
title: IMetaDataAssemblyEmit::DefineAssembly, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyEmit.DefineAssembly
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyEmit::DefineAssembly
helpviewer_keywords:
- IMetaDataAssemblyEmit::DefineAssembly method [.NET Framework metadata]
- DefineAssembly method [.NET Framework metadata]
ms.assetid: a0637d66-74bf-4f2d-8137-9ff838bccece
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b95a583aec87e3ba3e247d1ef800302b62657837
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62044822"
---
# <a name="imetadataassemblyemitdefineassembly-method"></a>IMetaDataAssemblyEmit::DefineAssembly, méthode
Crée un `Assembly` de structure qui contient les métadonnées pour l’assembly spécifié et retourne le jeton de métadonnées associé.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT DefineAssembly (  
    [in]  void                 *pbPublicKey,  
    [in]  ULONG                cbPublicKey,  
    [in]  ULONG                uHashAlgId,  
    [in]  LPCWSTR              szName,   
    [in]  ASSEMBLYMETADATA     *pMetaData,  
    [in]  DWORD                dwAssemblyFlags,  
    [out] mdAssembly           *pmda  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pbPublicKey`  
 [in] La clé publique qui identifie l’éditeur de l’assembly, ou NULL si l’assembly n'est pas un nom fort.  
  
 `cbPublicKey`  
 [in] La taille en octets de `pbPublicKey`.  
  
 `uHashAlgId`  
 [in] Identificateur de l’algorithme de hachage à utiliser pour chiffrer les fichiers dans l’assembly, ou NULL pour spécifier l’algorithme SHA-1.  
  
 `szName`  
 [in] Le nom lisible de l’assembly. Cette valeur ne doit pas dépasser 1 024 caractères.  
  
 `pMetaData`  
 [in] Pointeur vers une instance ASSEMBLYMETADATA qui contient les informations de version, la plateforme et aux paramètres régionaux de l’assembly.  
  
 `dwAssemblyFlags`  
 [in] Une combinaison de [CorAssemblyFlags](../../../../docs/framework/unmanaged-api/metadata/corassemblyflags-enumeration.md) valeurs qui décrivent les fonctionnalités de l’assembly.  
  
 `pmda`  
 [out] Pointeur vers le jeton de métadonnées.  
  
## <a name="remarks"></a>Notes  
 Seul `Assembly` structure des métadonnées peut être défini dans un manifeste.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IMetaDataAssemblyEmit, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-interface.md)
