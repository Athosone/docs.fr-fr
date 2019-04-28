---
title: 3551 - BufferOutOfOrderMessageNoBookmark
ms.date: 03/30/2017
ms.assetid: 7930d6c4-c843-4a83-933a-cecd71b80d1e
ms.openlocfilehash: 89643edde5856688c762b0cf0d188bd4e7ba8a24
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61755530"
---
# <a name="3551---bufferoutofordermessagenobookmark"></a>3551 - BufferOutOfOrderMessageNoBookmark
## <a name="properties"></a>Properties  
  
|||  
|-|-|  
|Id|3551|  
|Mots clés|WFServices|  
|Niveau|Information|  
|Canal|Microsoft-Windows-Application Server-Applications/Analyse|  
  
## <a name="description"></a>Description  
 Indique qu'une reprise de signet a échoué. Une autre tentative d'opération de réception en mémoire tampon sera faite lorsque l'instance de service sera prête à traiter cette opération.  
  
## <a name="message"></a>Message  
 Impossible d'effectuer actuellement l'opération « %2 » sur l'instance de service « %1 ». Une autre tentative sera faite lorsque l'instance de service sera prête à traiter cette opération.  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|OperationName|xs:string|Nom de l'opération.|  
|ServiceInstanceId|xs:string|ID de l'instance du service.|  
|AppDomain|xs:string|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
