---
title: StrongNameGetBlobFromImage, fonction
ms.date: 03/30/2017
api_name:
- StrongNameGetBlobFromImage
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameGetBlobFromImage
helpviewer_keywords:
- StrongNameGetBlobFromImage function [.NET Framework strong naming]
ms.assetid: 1de658e6-da32-4d01-9097-6f43c92222e1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b136e1fa480e53bcacfd9ea832d1dc4d1bd69f74
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62000296"
---
# <a name="strongnamegetblobfromimage-function"></a>StrongNameGetBlobFromImage, fonction
Obtient une représentation binaire de l’image de l’assembly à l’adresse mémoire spécifiée.  
  
 Cette fonction a été déconseillée. Utilisez le [ICLRStrongName::StrongNameGetBlobFromImage](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetblobfromimage-method.md) méthode à la place.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
BOOLEAN StrongNameGetBlobFromImage (  
    [in]  BYTE        *pbBase,  
    [in]  DWORD       dwLength,  
    [in]  BYTE        *pbBlob,  
    [in, out] DWORD   *pcbBlob  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pbBase`  
 [in] L’adresse mémoire du manifeste d’assembly mappé.  
  
 `dwLength`  
 [in] La taille, en octets, de l’image à `pbBase`.  
  
 `pbBlob`  
 [in] Une mémoire tampon pour contenir la représentation binaire de l’image.  
  
 `pcbBlob`  
 [in, out] La taille maximale en octets, demandée de `pbBlob`. Au retour, la taille réelle, en octets, de `pbBlob`.  
  
## <a name="return-value"></a>Valeur de retour  
 `true` de réussite ; Sinon, `false`.  
  
## <a name="remarks"></a>Notes  
 Si le `StrongNameGetBlobFromImage` (fonction) ne pas aboutir, appelez le [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) fonction pour récupérer la dernière erreur générée.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** StrongName.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [StrongNameGetBlobFromImage, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetblobfromimage-method.md)
- [StrongNameGetBlob, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetblob-method.md)
- [ICLRStrongName, interface](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
