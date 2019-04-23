---
title: ISymUnmanagedWriter::GetDebugInfo, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.GetDebugInfo
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::GetDebugInfo
helpviewer_keywords:
- ISymUnmanagedWriter::GetDebugInfo method [.NET Framework debugging]
- GetDebugInfo method [.NET Framework debugging]
ms.assetid: dd31c210-6829-45eb-927e-cc53932638b7
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 41d96c6d2024dbc3cab669f2dba2f99faef89f4b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59074246"
---
# <a name="isymunmanagedwritergetdebuginfo-method"></a>ISymUnmanagedWriter::GetDebugInfo, méthode
Retourne les informations nécessaires pour un compilateur écrire l’entrée de répertoire de débogage dans l’en-tête du fichier exécutable portable (PE). Le writer de symbole remplit tous les champs à l’exception de `TimeDateStamp` et `PointerToRawData`. (Le compilateur est chargé de définir ces deux champs en conséquence).  
  
 Un compilateur doit appeler cette méthode, émettre le blob de données dans le fichier PE, définissez le `PointerToRawData` champ IMAGE_DEBUG_DIRECTORY pour pointer vers les données émises et écrire IMAGE_DEBUG_DIRECTORY dans le fichier PE. Le compilateur doit également définir le `TimeDateStamp` champ égal le `TimeDateStamp` du fichier PE qui est généré.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetDebugInfo(  
    [in, out] IMAGE_DEBUG_DIRECTORY *pIDD,  
    [in]  DWORD cData,  
    [out] DWORD *pcData,  
    [out, size_is(cData),  
        length_is(*pcData)] BYTE data[]);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pIDD`  
 [in, out] Pointeur vers un IMAGE_DEBUG_DIRECTORY que le writer de symbole remplira.  
  
 `cData`  
 [in] Un `DWORD` qui contient la taille des données de débogage.  
  
 `pcData`  
 [out] Un pointeur vers un `DWORD` qui reçoit la taille de la mémoire tampon requise pour contenir les données de débogage.  
  
 `data`  
 [out] Un pointeur vers une mémoire tampon qui est assez grand pour contenir les données de débogage pour le magasin de symboles.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.  
  
## <a name="requirements"></a>Configuration requise  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi

- [ISymUnmanagedWriter, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
