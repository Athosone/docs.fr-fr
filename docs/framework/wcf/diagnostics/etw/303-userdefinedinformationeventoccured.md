---
title: 303 - UserDefinedInformationEventOccured
ms.date: 03/30/2017
ms.assetid: 5ed5acaf-3755-4417-92c4-4ebc8e854ca1
ms.openlocfilehash: 0b782b5ac0527b5acb3ebf0bf11c117563042495
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61595775"
---
# <a name="303---userdefinedinformationeventoccured"></a>303 - UserDefinedInformationEventOccured
## <a name="properties"></a>Properties  
  
|||  
|-|-|  
|Id|303|  
|Mots clés|Dépannage, HealthMonitoring, UserEvents, ServiceModel, EndToEndMonitoring|  
|Niveau|Information|  
|Canal|Microsoft-Windows-Application Server-Applications/Analyse|  
  
## <a name="description"></a>Description  
 Cet événement est émis à partir du code utilisateur. Les développeurs peuvent émettre cet événement lorsqu'un événement d'informations personnalisé se produit dans leur service. Cela peut s'effectuer à l'aide des API <xref:System.Diagnostics.Eventing>. En outre, il existe un exemple WCF qui encapsule cette API et montre comment émettre correctement cet événement.  
  
## <a name="message"></a>Message  
 Nom : '%1', Référence : '%2', Charge : %3  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|Nom|`xs:string`|Nom de l'événement défini par l'utilisateur.|  
|HostReference|`xs:string`|Pour les services hébergés par le Web, ce champ identifie de manière unique le service dans la hiérarchie Web. Son format est défini en tant que « chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName'. Exemple : « Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService ».|  
|Charge utile|`xs:string`|Charge utile de l'événement définie par l'utilisateur.|
