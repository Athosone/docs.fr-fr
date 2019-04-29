---
title: 57398 - MaxInstancesExceeded
ms.date: 03/30/2017
ms.assetid: f943d209-dfeb-43e5-b572-c9a06217936e
ms.openlocfilehash: d644c25ec2dee06eea4a5fb66c30792bb650f252
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61945962"
---
# <a name="57398---maxinstancesexceeded"></a>57398 - MaxInstancesExceeded
## <a name="properties"></a>Properties  
  
|||  
|-|-|  
|Id|57398|  
|Mots clés|WFServices|  
|Niveau|Warning|  
|Canal|Microsoft-Windows-Application Server-Applications/Analyse|  
  
## <a name="description"></a>Description  
 Indique que le système a atteint la limite définie pour la limitation des « MaxConcurrentInstances ».  
  
## <a name="message"></a>Message  
 Le système a atteint la limite définie pour la limitation des 'MaxConcurrentInstances'. La limite a été définie sur %1. La valeur de limitation peut être modifiée en modifiant l'attribut « maxConcurrentInstances » de l'élément serviceThrottle ou en modifiant la propriété « MaxConcurrentInstances » à l'aide du comportement ServiceThrottlingBehavior.  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|Nom|xs:string|Nom de l'élément.|  
|AppDomain|xs:string|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
