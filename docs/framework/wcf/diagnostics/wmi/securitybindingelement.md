---
title: SecurityBindingElement
ms.date: 03/30/2017
ms.assetid: ef93b6e6-3524-48a8-94d3-c8837f1872f9
ms.openlocfilehash: 1d367d0c5d14e6e75539dd2b20cdffcf2b34963d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59975557"
---
# <a name="securitybindingelement"></a>SecurityBindingElement
SecurityBindingElement  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class SecurityBindingElement : BindingElement  
{  
  string DefaultAlgorithmSuite;  
  boolean IncludeTimestamp;  
  string KeyEntropyMode;  
  LocalServiceSecuritySettings LocalServiceSecuritySettings;  
  string MessageSecurityVersion;  
  string SecurityHeaderLayout;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe SecurityBindingElement ne définit pas de méthode.  
  
## <a name="properties"></a>Properties  
 La classe SecurityBindingElement a les propriétés suivantes :  
  
### <a name="defaultalgorithmsuite"></a>DefaultAlgorithmSuite  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Spécifie les algorithmes à utiliser avec la liaison.  
  
### <a name="includetimestamp"></a>IncludeTimestamp  
 Type de données : booléen  
  
 Type d’accès : Propriétés en lecture seule  
  
 Valeur booléenne qui spécifie si chaque message contient un horodatage.  
  
### <a name="keyentropymode"></a>KeyEntropyMode  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Source d'entropie utilisée pour créer des clés.  
  
### <a name="localservicesecuritysettings"></a>LocalServiceSecuritySettings  
 Type de données : LocalServiceSecuritySettings  
  
 Type d’accès : Propriétés en lecture seule  
  
 Propriétés de sécurité spécifiques d’une liaison pour le service local.  
  
### <a name="messagesecurityversion"></a>MessageSecurityVersion  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Version utilisée pour la sécurité de message.  
  
### <a name="securityheaderlayout"></a>SecurityHeaderLayout  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Ordre des éléments dans l'en-tête de sécurité pour cette liaison.  
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Channels.SecurityBindingElement>
