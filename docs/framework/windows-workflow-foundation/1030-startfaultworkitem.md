---
title: 1030 - StartFaultWorkItem
ms.date: 03/30/2017
ms.assetid: e1601fb9-0bc6-4dbe-816f-f24914063d34
ms.openlocfilehash: 3848d644e77041a62a52eb2eae5eeef286dfe334
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61924317"
---
# <a name="1030---startfaultworkitem"></a>1030 - StartFaultWorkItem
## <a name="properties"></a>Properties  
  
|||  
|-|-|  
|Id|1030|  
|Mots clés|WFRuntime|  
|Niveau|Verbose|  
|Canal|Microsoft-Windows-Application Server-Applications/Débogage|  
  
## <a name="description"></a>Description  
 Indique qu'un FaultWorkItem démarre l'exécution.  
  
## <a name="message"></a>Message  
 Démarrage de l’exécution d’un FaultWorkItem pour l’activité « %1 », DisplayName : « %2 », InstanceId : '%3'.  L'exception a été propagée à partir de l'activité « %4 », DisplayName : « %5 », InstanceId : « %6 ».  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|FaultActivity|xs:string|Nom de type de l'activité d'erreur.|  
|FaultActivityDisplayName|xs:string|Nom complet de l'activité d'erreur.|  
|FaultActivityInstanceId|xs:string|ID d'instance de l'activité d'erreur.|  
|ExceptionActivity|xs:string|Nom de type de l'activité qui a levé l'exception.|  
|ExceptionActivityDisplayName|xs:string|Nom complet de l'activité qui a levé l'exception.|  
|ExceptionActivityInstanceId|xs:string|ID d'instance de l'activité ayant levé l'exception.|  
|Exception|xs:string|Détails de l'exception|  
|AppDomain|xs:string|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
