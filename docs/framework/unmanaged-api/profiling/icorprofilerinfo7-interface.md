---
title: ICorProfilerInfo7, interface
ms.date: 03/30/2017
ms.assetid: cf37c462-73c5-412a-a7f8-bb26ca746313
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6d8586031c5bcb0303a64b67ee601fe41b81ee3f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59134847"
---
# <a name="icorprofilerinfo7-interface"></a>ICorProfilerInfo7, interface
[Prise en charge dans [!INCLUDE[net_v461](../../../../includes/net-v461-md.md)] et versions ultérieures]  
  
 Une sous-classe de [ICorProfilerInfo6](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo6-interface.md) qui fournit une méthode pour appliquer qui vient d’être défini des métadonnées à un module et qui fournit l’accès à un flux de symbole d’en mémoire.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[ApplyMetaData, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-applymetadata-method.md)|Applique les métadonnées qui vient d’être définie par le `IMetadataEmit::Define*` méthodes à un module spécifié.|  
|[GetInMemorySymbolsLength, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-getinmemorysymbolslength-method.md)|Retourne la longueur d’un flux de symbole d’en mémoire.|  
|[ReadInMemorySymbols](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-readinmemorysymbols.md)|Lit les octets à partir d’un flux de symbole d’en mémoire.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de profilage](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
