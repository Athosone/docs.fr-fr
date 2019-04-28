---
title: 225 - TraceCorrelationKeys
ms.date: 03/30/2017
ms.assetid: d9083aaf-3816-4c1c-bae0-2d7f49628345
ms.openlocfilehash: 0bb54387dbd738a01225008edfc45ecb7297cd00
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61755660"
---
# <a name="225---tracecorrelationkeys"></a>225 - TraceCorrelationKeys
## <a name="properties"></a>Properties  
  
|||  
|-|-|  
|Id|225|  
|Mots clés|Dépannage, ServiceModel|  
|Niveau|Information|  
|Canal|Microsoft-Windows-Application Server-Applications/Analyse|  
  
## <a name="description"></a>Description  
 Cet événement est émis lorsque la corrélation basée sur le contenu est utilisée pour un service de workflow. Il contient les clés de corrélation appliquées pour mettre en corrélation un message avec une instance.  
  
## <a name="message"></a>Message  
 Clé de corrélation '%1' calculée à l'aide des valeurs '%2' dans l'étendue parente '%3'.  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|Clé d'instance|`xs:GUID`|Clé générée à partir des valeurs de corrélation.|  
|Valeurs|`xs:string`|Valeurs utilisées pour calculer la clé d'instance de corrélation.|  
|Étendue parente|`xs:string`||  
|HostReference|`xs:string`|Pour les services hébergés par le Web, ce champ identifie de manière unique le service dans la hiérarchie Web. Son format est défini en tant que « chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName'. Exemple : « Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService ».|  
|AppDomain|`xs:string`|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
