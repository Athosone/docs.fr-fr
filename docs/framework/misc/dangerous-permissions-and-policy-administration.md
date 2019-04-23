---
title: Autorisations dangereuses et administration de stratégie
ms.date: 03/30/2017
helpviewer_keywords:
- permissions [.NET Framework], policy administration
- security [.NET Framework], dangerous permissions
- code security, dangerous permissions
- secure coding, dangerous permissions
- permissions [.NET Framework], dangerous
ms.assetid: 1929e854-23a0-4bb1-94be-e8aa3b609e32
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ae24cdcb97e30da0bd4aec6569ef3dcda11488c6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59078940"
---
# <a name="dangerous-permissions-and-policy-administration"></a>Autorisations dangereuses et administration de stratégie
Plusieurs des opérations protégées pour lesquelles le .NET Framework fournit des autorisations risquent de permettre le contournement du système de sécurité. Ces autorisations dangereuses doivent être accordées uniquement à du code fiable, et seulement en cas de nécessité. Il n’existe généralement aucune défense contre du code malveillant, si ces autorisations sont accordées.  
  
> [!NOTE]
>  Dans le [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)], des modifications importantes ont été apportées à la terminologie et au modèle de sécurité du .NET Framework. Pour plus d’informations sur ces modifications, consultez [modifications de sécurité](../../../docs/framework/security/security-changes.md).  
  
 Les autorisations dangereuses sont expliquées dans le tableau suivant.  
  
|Autorisation|Risque potentiel|  
|----------------|--------------------|  
|<xref:System.Security.Permissions.SecurityPermission>||  
|<xref:System.Security.Permissions.SecurityPermissionFlag.UnmanagedCode>|Permet au code managé d’appeler du code non managé, ce qui est souvent dangereux.|  
|<xref:System.Security.Permissions.SecurityPermissionFlag.SkipVerification>|En l’absence de vérification, le code peut tout faire.|  
|<xref:System.Security.Permissions.SecurityPermissionFlag.ControlEvidence>|Les preuves invalidées peuvent tromper la stratégie de sécurité.|  
|<xref:System.Security.Permissions.SecurityPermissionFlag.ControlPolicy>|La modification de la stratégie de sécurité peut permettre de désactiver la sécurité.|  
|<xref:System.Security.Permissions.SecurityPermissionFlag.SerializationFormatter>|L’utilisation de la sérialisation peut constituer un moyen de contourner les mécanismes d’accessibilité. Pour plus d’informations, consultez [Sécurité et sérialisation](../../../docs/framework/misc/security-and-serialization.md).|  
|<xref:System.Security.Permissions.SecurityPermissionFlag.ControlPrincipal>|La capacité à définir le principal actuel peut permettre de tromper la sécurité basée sur les rôles.|  
|<xref:System.Security.Permissions.SecurityPermissionFlag.ControlThread>|La manipulation des threads est dangereuse en raison de l’état de sécurité associé aux threads.|  
|<xref:System.Security.Permissions.ReflectionPermission>||  
|<xref:System.MemberAccessException>|Permet d’utiliser des membres privés pour passer outre les mécanismes d’accessibilité.|  
  
## <a name="see-also"></a>Voir aussi

- [Instructions de codage sécurisé](../../../docs/standard/security/secure-coding-guidelines.md)
