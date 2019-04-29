---
title: Méthode ICLRStrongName::StrongNameSignatureGeneration
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameSignatureGeneration
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameSignatureGeneration
helpviewer_keywords:
- StrongNameSignatureGeneration method, ICLRStrongName interface [.NET Framework hosting]
- ICLRStrongName::StrongNameSignatureGeneration method [.NET Framework hosting]
ms.assetid: 4cdb1284-947a-4ed4-94c1-c5ff5cdfce56
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 679afd7b1053043a7cc43304a544a516024a4696
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61663793"
---
# <a name="iclrstrongnamestrongnamesignaturegeneration-method"></a>Méthode ICLRStrongName::StrongNameSignatureGeneration
Génère une signature de nom fort pour l’assembly spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT StrongNameSignatureGeneration (   
    [in]  LPCWSTR   wszFilePath,  
    [in]  LPCWSTR   wszKeyContainer,  
    [in]  BYTE      *pbKeyBlob,  
    [in]  ULONG     cbKeyBlob,  
    [out] BYTE      **ppbSignatureBlob,  
    [out] ULONG     *pcbSignatureBlob  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `wszFilePath`  
 [in] Le chemin d’accès au fichier qui contient le manifeste de l’assembly pour lequel la signature de nom fort est générée.  
  
 `wszKeyContainer`  
 [in] Le nom du conteneur de clé qui contient la paire de clés publique/privée.  
  
 Si `pbKeyBlob` a la valeur null, `wszKeyContainer` doit spécifier un conteneur valid dans le fournisseur de services de chiffrement (CSP). Dans ce cas, la paire de clés stockée dans le conteneur est utilisée pour signer le fichier.  
  
 Si `pbKeyBlob` n’est pas null, la paire de clés est supposée être contenue dans l’objet binaire volumineux (BLOB) de clé.  
  
 Les clés doivent être Rivest-Shamir-Adleman (RSA 1024 bits) clés de signature. Aucun autre type de clés n’est pris en charge pour l’instant.  
  
 `pbKeyBlob`  
 [in] Pointeur vers la paire de clés publique/privée. Cette paire est au format créé par Win32 `CryptExportKey` (fonction). Si `pbKeyBlob` est null, le conteneur de clé spécifié par `wszKeyContainer` est supposée pour contenir la paire de clés.  
  
 `cbKeyBlob`  
 [in] La taille, en octets, de `pbKeyBlob`.  
  
 `ppbSignatureBlob`  
 [out] Pointeur vers l’emplacement auquel le common language runtime retourne la signature. Si `ppbSignatureBlob` est null, le runtime stocke la signature dans le fichier spécifié par `wszFilePath`.  
  
 Si `ppbSignatureBlob` est non null, le common language runtime alloue de l’espace dans lequel retourner la signature. L’appelant doit libérer cet espace à l’aide de la [ICLRStrongName::StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamefreebuffer-method.md) (méthode).  
  
 `pcbSignatureBlob`  
 [out] La taille, en octets, de la signature retournée.  
  
## <a name="return-value"></a>Valeur de retour  
 `S_OK` Si la méthode a réussi ; Sinon, une valeur HRESULT qui indique un échec (consultez [valeurs HRESULT courantes](https://go.microsoft.com/fwlink/?LinkId=213878) pour obtenir la liste).  
  
## <a name="remarks"></a>Notes  
 Spécifiez null pour `wszFilePath` pour calculer la taille de la signature sans créer la signature.  
  
 La signature peut être enregistrés directement dans le fichier, ou retourné à l’appelant.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MetaHost.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [StrongNameSignatureGenerationEx, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignaturegenerationex-method.md)
- [ICLRStrongName, interface](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
