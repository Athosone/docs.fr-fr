---
title: ServiceAuthorizationBehavior
ms.date: 03/30/2017
ms.assetid: 77dad8e8-fea4-4d1c-b366-2f01a2a87f78
ms.openlocfilehash: 51555e3357b8c33a53261c4894d97798b0a05656
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61957053"
---
# <a name="serviceauthorizationbehavior"></a>ServiceAuthorizationBehavior
ServiceAuthorizationBehavior  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class ServiceAuthorizationBehavior : Behavior  
{  
  boolean ImpersonateCallerForAllOperations;  
  string PrincipalPermissionMode;  
  string RoleProvider;  
  string ServiceAuthorizationManager;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe ServiceAuthorizationBehavior ne définit pas de méthode.  
  
## <a name="properties"></a>Properties  
 La classe ServiceAuthorizationBehavior a les propriétés suivantes :  
  
### <a name="impersonatecallerforalloperations"></a>ImpersonateCallerForAllOperations  
 Type de données : booléen  
  
 Type d’accès : Propriétés en lecture seule  
  
 Valeur qui contrôle si le service essaie d'emprunter l'identité à l'aide des informations d'identification fournies par le message entrant.  
  
### <a name="principalpermissionmode"></a>PrincipalPermissionMode  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Principal de sécurité utilisée pour effectuer les opérations sur le serveur.  
  
### <a name="roleprovider"></a>RoleProvider  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Nom du fournisseur de rôles ASP.NET.  
  
### <a name="serviceauthorizationmanager"></a>ServiceAuthorizationManager  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Gestionnaire d'autorisations utilisé pour l'autorisation personnalisée.  
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Description.ServiceAuthorizationBehavior>
