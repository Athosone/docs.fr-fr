---
title: 111 - CustomTrackingRecordError
ms.date: 03/30/2017
ms.assetid: d469fb12-e094-4d6c-9b4d-abd7ce0d17da
ms.openlocfilehash: 737d48714020e20fc7b864de4e650ae234a8580e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62009758"
---
# <a name="111---customtrackingrecorderror"></a>111 - CustomTrackingRecordError
## <a name="properties"></a>Properties  
  
|||  
|-|-|  
|Id|111|  
|Mots clés|UserEvents, EndToEndMonitoring, Dépannage, HealthMonitoring, WFTracking|  
|Niveau|Error|  
|Canal|Microsoft-Windows-Application Server-Applications/Analyse|  
  
## <a name="description"></a>Description  
 Cet événement est émis par le participant de suivi ETW lorsqu'une activité dans une instance de workflow émet un événement CustomTrackingRecord avec erreur de niveau.  
  
## <a name="message"></a>Message  
 TrackRecord = CustomTrackingRecord, InstanceID = %1, RecordNumber=%2, EventTime=%3, Name=%4, ActivityName=%5, ActivityId=%6, ActivityInstanceId=%7, ActivityTypeName=%8, Data=%9, Annotations=%10, ProfileName = %11  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|InstanceId|xs:GUID|ID d'instance pour le workflow|  
|RecordNumber|xs:long|Numéro de séquence de l'enregistrement émis.|  
|EventTime|xs:dateTime|Heure au format UTC à laquelle l'événement a été émis|  
|Nom|xs:string|Nom de l'événement CustomTrackingRecord|  
|ActivityName|xs:string|Nom de l'activité qui a émis l'événement CustomTrackingRecord|  
|ActivityId|xs:string|ID de l'activité qui a émis l'événement CustomTrackingRecord|  
|ActivityInstanceId|xs:string|ID d'instance de l'activité qui a émis l'événement CustomTrackingRecord|  
|ActivityTypeName|xs:string|Nom de l'activité qui a émis l'événement CustomTrackingRecord|  
|Données|xs:string|Données suivies avec cet événement.  Les valeurs sont stockées dans un élément xml au format \<éléments >\< nom de l’élément = « dataName » type = "> dataValue\</élément > \< /éléments >.  Si aucune donnée n’a été suivie, la chaîne contient \<éléments / >. La taille d'événement ETW est limitée par la taille de la mémoire tampon ETW ou par la charge utile maximale pour un événement ETW. Si la taille de l’événement dépasse les limites ETW, l’événement est tronqué en supprimant les annotations et en remplaçant la valeur de données avec \<éléments >... \</Items >.  Les types suivants sont stockés en tant que valeur telle que retournée par ToString(); string,char,bool,int,short,long,uint,ushort,ulong,System.Single,float,double,System.Guid,System.DateTimeOffset,System.DateTime.  Tous les autres types sont sérialisés à l'aide de System.Runtime.Serialization.NetDataContractSerializer.|  
|Annotations|xs:string|Annotations ayant été ajoutées à cet événement.  Les valeurs sont stockées dans un élément xml au format \<éléments >\< nom de l’élément = « annotationName » type = "> annotationValue\</élément > \< /éléments >.  Si aucune annotation n’est spécifiée, la chaîne contient \<éléments / >. La taille d'événement ETW est limitée par la taille de la mémoire tampon ETW ou par la charge utile maximale pour un événement ETW. Si la taille de l’événement dépasse les limites ETW, l’événement est tronqué en supprimant les annotations et en remplaçant la valeur de l’annotation avec \<éléments >... \</Items >.|  
|ProfileName|xs:string|Nom ou modèle de suivi qui a provoqué l'émission de cet événement|  
|HostReference|xs:string|Pour les services hébergés sur le Web, ce champ identifie de manière unique le service dans la hiérarchie Web.  Son format est défini en tant que « chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName' exemple : « Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService »|  
|AppDomain|xs:string|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
