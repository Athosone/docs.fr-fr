---
title: StrongNameErrorInfo, fonction
ms.date: 03/30/2017
api_name:
- StrongNameErrorInfo
api_location:
- mscoree.dll
- mscorsn.dll
- clr.dll
- mscorwks.dll
- mscoreei.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameErrorInfo
helpviewer_keywords:
- StrongNameErrorInfo function [.NET Framework strong naming]
ms.assetid: e91bf8c3-7c26-4732-938e-2e5b04abfc99
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 909c283b1355153ffe1aa02acfbe8acc25a7e215
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59124096"
---
# <a name="strongnameerrorinfo-function"></a>StrongNameErrorInfo, fonction
Obtient le dernier code d’erreur déclenché par l’une des fonctions de nom fort.  
  
 Cette fonction a été déconseillée.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT StrongNameErrorInfo ();   
```  
  
## <a name="return-value"></a>Valeur de retour  
 Code d’erreur COM dernier défini par une des fonctions à nom fort.  
  
## <a name="remarks"></a>Notes  
 La plupart des méthodes à nom fort retournent une simple `true` ou `false` indication de leur achèvement. Utilisez le `StrongNameErrorInfo` fonction pour récupérer un HRESULT qui spécifie la dernière erreur générée par les fonctions de nom fort.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** StrongName.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
