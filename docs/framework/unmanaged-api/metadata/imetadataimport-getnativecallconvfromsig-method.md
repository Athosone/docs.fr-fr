---
title: IMetaDataImport::GetNativeCallConvFromSig, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetNativeCallConvFromSig
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetNativeCallConvFromSig
helpviewer_keywords:
- GetNativeCallConvFromSig method [.NET Framework metadata]
- IMetaDataImport::GetNativeCallConvFromSig method [.NET Framework metadata]
ms.assetid: 50e04026-4d4a-47d9-96c1-f4677d6d938b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ef1ac83b383a9f6bbee7f55441d2abfcb081afa6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59122744"
---
# <a name="imetadataimportgetnativecallconvfromsig-method"></a>IMetaDataImport::GetNativeCallConvFromSig, méthode
Obtient la convention d’appel native pour la méthode représentée par le pointeur de signature spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetNativeCallConvFromSig (  
   [in]  void const  *pvSig,  
   [in]  ULONG       cbSig,  
   [out] ULONG       *pCallConv  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pvSig`  
 [in] Pointeur vers la signature de métadonnées de la méthode pour retourner la convention d’appel pour.  
  
 `cbSig`  
 [in] La taille en octets de `pvSig`.  
  
 `pCallConv`  
 [out] Pointeur vers la convention d’appel native.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Runtime.InteropServices.CallingConvention>
- [IMetaDataImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [IMetaDataImport2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
