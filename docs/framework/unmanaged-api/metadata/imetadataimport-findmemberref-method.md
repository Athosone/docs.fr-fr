---
title: IMetaDataImport::FindMemberRef, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.FindMemberRef
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::FindMemberRef
helpviewer_keywords:
- IMetaDataImport::FindMemberRef method [.NET Framework metadata]
- FindMemberRef method [.NET Framework metadata]
ms.assetid: 1ccda329-d752-4d89-abe8-511af3c3f4c9
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: abbd35fe390cc09951b762a5fd671d2d34a57c6c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61777882"
---
# <a name="imetadataimportfindmemberref-method"></a>IMetaDataImport::FindMemberRef, méthode
Obtient un pointeur vers le jeton MemberRef pour le membre de référence qui est délimitée par spécifié <xref:System.Type> et qui a la signature de nom et de métadonnées spécifiée.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT FindMemberRef (  
   [in]  mdTypeRef          td,  
   [in]  LPCWSTR            szName,   
   [in]  PCCOR_SIGNATURE    pvSigBlob,   
   [in]  ULONG              cbSigBlob,   
   [out] mdMemberRef        *pmr  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `td`  
 [in] Le jeton TypeRef pour la classe ou interface qui englobe la référence de membre à rechercher. Si cette valeur est `mdTokenNil`, la recherche est effectuée pour une variable globale ou une référence de fonction globale.  
  
 `szName`  
 [in] Le nom de la référence de membre à rechercher.  
  
 `pvSigBlob`  
 [in] Pointeur vers la signature de métadonnées binaires de la référence de membre.  
  
 `cbSigBlob`  
 [in] La taille en octets de `pvSigBlob`.  
  
 `pmr`  
 [out] Pointeur vers le jeton MemberRef correspondant.  
  
## <a name="remarks"></a>Notes  
 Vous spécifiez le membre à l’aide de son interface ou la classe englobante (`td`), son nom (`szName`) et éventuellement sa signature (`pvSigBlob`).  
  
 La signature est passé à `FindMemberRef` doit avoir été générée dans la portée actuelle, car les signatures sont liées à une étendue spécifique. Une signature peut incorporer un jeton qui identifie le type de valeur ou de la classe englobant. Le jeton est un index dans la table TypeDef local. Vous ne pouvez pas générer une signature d’exécution en dehors du contexte de la portée actuelle et utiliser cette signature comme entrée dans `FindMemberRef`.  
  
 `FindMemberRef` recherche uniquement les références de membre ont été définis directement dans la classe ou interface ; Il ne trouve pas de références de membre hérité.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IMetaDataImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [IMetaDataImport2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
