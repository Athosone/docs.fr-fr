---
title: API et bibliothèques de classes supplémentaires
ms.date: 01/29/2018
helpviewer_keywords:
- Additional class libraries
- Additional managed libraries
- .NET Framework out-of-band releases
- out-of-band releases
ms.assetid: cf2d9006-b631-4e5d-81cd-20aab78c60f1
author: mairaw
ms.author: mairaw
ms.topic: conceptual
ms.openlocfilehash: a48a145cd337a18c4ce63b281e1c82032d0532e7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61675362"
---
# <a name="additional-class-libraries-and-apis"></a>API et bibliothèques de classes supplémentaires

Le .NET Framework est en constante évolution. Pour améliorer le développement multiplateforme et introduire de nouvelles fonctionnalités très tôt, les nouvelles fonctionnalités sont publiées hors bande (OOB). Cette rubrique répertorie les projets OOB pour lesquels nous fournissons une documentation.  
  
En outre, certaines bibliothèques ciblent des plateformes ou des implémentations précises du .NET Framework. Par exemple, le <xref:System.Text.CodePagesEncodingProvider> classe rend les codages de page de code disponible pour les applications UWP développées à l’aide de .NET Framework. Cette rubrique liste également ces bibliothèques.  
  
## <a name="oob-projects"></a>Projets OOB
  
| Projet | Description |  
| ------- | ----------- |  
| <xref:System.Collections.Immutable> | Fournit des collections thread-safe dont le contenu est assuré de ne jamais changer. |
| <xref:System.Net.Http.WinHttpHandler> | Fournit un gestionnaire de messages pour <xref:System.Net.Http.HttpClient> basé sur l’interface WinHTTP de Windows. |
| <xref:System.Numerics> | Fournit une bibliothèque de types de vecteurs qui peuvent tirer parti de l’accélération matérielle SIMD.| 
| <xref:System.Threading.Tasks.Dataflow> | La bibliothèque de flux de données TPL fournit des composants de flux de données destinés à accroître la robustesse des applications prenant en charge l’accès concurrentiel. |  

## <a name="platform-specific-libraries"></a>Bibliothèques propres à une plateforme
  
| Projet | Description |  
| ------- | ----------- |  
| <xref:System.Text.CodePagesEncodingProvider> | Étend la <xref:System.Text.EncodingProvider> classe pour rendre les codages de page de code disponibles pour les applications qui ciblent la plateforme Windows universelle. |  
  
## <a name="private-apis"></a>API privées  

Ces API prennent en charge l'infrastructure du produit et ne sont ni utilisables ni destinées à être utilisées directement à partir du code.  
  
| Nom de l'API |
| -------- |
| [Classe de System.Net.Connection](../../../docs/framework/additional-apis/connection.md) |
| [System.Net.Connection.m\_WriteList champ](../../../docs/framework/additional-apis/m_writelist.md) |
| [Classe de System.Net.ConnectionGroup](../../../docs/framework/additional-apis/connectiongroup.md) |
| [System.Net.ConnectionGroup.m\_ConnectionList champ](../../../docs/framework/additional-apis/m_connectionlist.md) |
| [Classe de System.Net.CoreResponseData](../../../docs/framework/additional-apis/coreresponsedata.md) |
| [System.Net.CoreResponseData.m\_ResponseHeaders Field](../../../docs/framework/additional-apis/coreresponsedata_m_responseheaders.md) |
| [System.Net.CoreResponseData.m\_StatusCode Field](../../../docs/framework/additional-apis/coreresponsedata_m_statuscode.md) |
| [System.Net.HttpWebRequest.\_AutoRedirects Field](../../../docs/framework/additional-apis/_autoredirects.md) |
| [System.Net.HttpWebRequest. \_CoreResponse champ](../../../docs/framework/additional-apis/httpwebrequest__coreresponse.md) |
| [System.Net.HttpWebRequest. \_HttpResponse champ](../../../docs/framework/additional-apis/_httpresponse.md) |
| [System.Net.ServicePoint.m\_ConnectionGroupList Field](../../../docs/framework/additional-apis/m_connectiongrouplist.md) |
| [System.Net.ServicePointManager.s\_ServicePointTable champ](../../../docs/framework/additional-apis/s_servicepointtable.md) |
| [System.Windows.Diagnostics.VisualDiagnostics.s\_isDebuggerCheckDisabledForTestPurposes Field](../../../docs/framework/additional-apis/s-isdebuggercheckdisabledfortestpurposes-field.md) |
| [Classe de System.Windows.Forms.Design.DataMemberFieldEditor](../../../docs/framework/additional-apis/datamemberfieldeditor-class.md) |
| [Classe de System.Windows.Forms.Design.DataMemberListEditor](../../../docs/framework/additional-apis/datamemberlisteditor-class.md) |
  
## <a name="see-also"></a>Voir aussi

- [Versions finales hors plage de .NET Framework](../../../docs/framework/get-started/the-net-framework-and-out-of-band-releases.md)
