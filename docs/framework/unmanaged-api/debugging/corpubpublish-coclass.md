---
title: CorpubPublish (coclasse)
ms.date: 03/30/2017
api_name:
- CorpubPublish Coclass
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorpubPublish
helpviewer_keywords:
- CorpubPublish coclass [.NET Framework debugging]
ms.assetid: 191015da-f54a-4bac-a28a-1de7ab3c3428
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 05d9eef36885aee05d88f7da994c8b168c3221b3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61996305"
---
# <a name="corpubpublish-coclass"></a>CorpubPublish (coclasse)
Fournit les interfaces pour la publication d'informations sur les domaines d'application et les processus.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
coclass CorpubPublish {  
    [default] interface ICorPublish;  
    interface           ICorPublishProcess;  
    interface           ICorPublishAppDomain;  
    interface           ICorPublishProcessEnum;  
    interface           ICorPublishAppDomainEnum;  
};  
```  
  
## <a name="interfaces"></a>Interfaces  
  
|Interface|Description|  
|---------------|-----------------|  
|[ICorPublish, interface](../../../../docs/framework/unmanaged-api/debugging/icorpublish-interface.md)|Fournit des méthodes pour la publication d’informations sur les processus et les domaines d’application dans ces processus.|  
|[ICorPublishAppDomain, interface](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomain-interface.md)|Représente et fournit des informations sur un domaine d’application dans un processus.|  
|[ICorPublishAppDomainEnum, interface](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomainenum-interface.md)|Fournit des méthodes qui parcourent une collection de domaines d’application qui existent actuellement dans un processus.|  
|[ICorPublishProcess, interface](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md)|Représente un processus qui s’exécute sur un ordinateur.|  
|[ICorPublishProcessEnum, interface](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocessenum-interface.md)|Fournit des méthodes qui parcourent une collection de processus qui s’exécutent sur un ordinateur.|  
  
## <a name="remarks"></a>Notes  
 Un scénario de publication classique implique un développeur qui souhaite déboguer du code managé qui s’exécute sur un ordinateur au sein d’un domaine d’application. L’environnement d’hébergement peut-être s’exécuter plus d’un domaine d’application dans un processus. Le développeur souhaite utiliser une interface utilisateur graphique ou autres moyens pour répertorier tous les processus qui sont exécutent sur l’ordinateur et choisir un processus spécifique. La liste doit inclure tous les domaines d’application dans les processus en cours d’exécution du code managé. Le développeur peut ensuite identifier le domaine d’application spécifique et attacher un débogueur à ce domaine.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorPub.idl  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :**  [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
