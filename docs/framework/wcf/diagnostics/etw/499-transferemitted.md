---
title: 499 - TransferEmitted
ms.date: 03/30/2017
ms.assetid: 07a26434-a7a0-40fc-b5d0-3520a04328ae
ms.openlocfilehash: b1ade828ee6519288165e272e7d9f36fd6aca9ff
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61774931"
---
# <a name="499---transferemitted"></a>499 - TransferEmitted
## <a name="properties"></a>Properties  
  
|||  
|-|-|  
|Id|499|  
|Mots clés|Dépannage, UserEvents, EndToEndMonitoring, ServiceModel, WFTracking, ServiceHost, WCFMessageLogging|  
|Niveau|LogAlways|  
|Canal|Microsoft-Windows-Application Server-Applications/Analyse|  
  
## <a name="description"></a>Description  
 Cet événement est émis lorsque l'événement de transfert se produit.  
  
## <a name="message"></a>Message  
 Événement Transfer émis.  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|HostReference|`xs:string`|Pour les services hébergés par le Web, ce champ identifie de manière unique le service dans la hiérarchie Web. Son format est défini en tant que « chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName'. Exemple : « Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService ».|  
|AppDomain|`xs:string`|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
