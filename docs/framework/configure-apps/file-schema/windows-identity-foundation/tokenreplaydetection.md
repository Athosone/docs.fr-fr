---
title: <tokenReplayDetection>
ms.date: 03/30/2017
ms.assetid: ac3f588e-5f75-4275-b969-2d492ecc3b47
author: BrucePerlerMS
ms.openlocfilehash: 4deeb1d84f2621adb7ff1b649a505138b6856ec1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61790492"
---
# <a name="tokenreplaydetection"></a>\<tokenReplayDetection>
Active la détection de relecture de jetons et spécifie le délai d’expiration pour les jetons.  
  
 \<system.identityModel>  
\<identityConfiguration>  
\<tokenReplayDetection>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <tokenReplayDetection enabled=xs:boolean expirationPeriod=TimeSpan>  
    </tokenReplayDetection>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="type"></a>Type  
 <xref:System.IdentityModel.Configuration.TokenReplayDetectionElement>  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|enabled|Une valeur qui spécifie si la détection de relecture de jetons est activée ; détection de relecture « true » pour activer un jeton.|  
|expirationPeriod|Un <xref:System.TimeSpan> qui spécifie la quantité maximale de temps avant qu’un élément est considéré comme expiré et supprimé du cache.  Pour plus d’informations sur la spécification <xref:System.TimeSpan> valeurs, consultez [valeurs Timespan](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<identityConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|Spécifie les paramètres de l’identité de niveau de service.|  
|[\<securityTokenHandlerConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|Fournit une configuration pour une collection de sécurité gestionnaires de jetons.|  
  
## <a name="remarks"></a>Notes  
 Un `<tokenReplayDetection>` élément peut être spécifié au niveau du service sous le `<identityConfiguration>` élément ou sur le niveau de collection de gestionnaires de jetons de sécurité sous la `<securityTokenHandlerConfiguration>` élément. Les paramètres sur une collection de gestionnaires de jetons remplacent celles spécifiées sur le service.  
  
 Le type du cache de relecture de jetons est spécifié par le [ \<tokenReplayCache >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaycache.md) élément.
