---
title: ICLRRuntimeHost::ExecuteApplication, méthode
ms.date: 03/30/2017
api_name:
- ICLRRuntimeHost.ExecuteApplication
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeHost::ExecuteApplication
helpviewer_keywords:
- ICLRRuntimeHost::ExecuteApplication method [.NET Framework hosting]
- ExecuteApplication method [.NET Framework hosting]
ms.assetid: 5f28cc4e-7176-4e00-aa1f-58ae6ee52fe4
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8ce7e9ff4041abd1e89330bd3a565b755875d3b2
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59194225"
---
# <a name="iclrruntimehostexecuteapplication-method"></a>ICLRRuntimeHost::ExecuteApplication, méthode
Utilisé dans les scénarios de déploiement ClickOnce basée sur un manifeste pour spécifier l’application à activer dans un nouveau domaine. Pour plus d’informations sur ces scénarios, consultez [ClickOnce Security and Deployment](/visualstudio/deployment/clickonce-security-and-deployment).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT ExecuteApplication(  
    [in] LPCWSTR   pwzAppFullName,  
    [in] DWORD     dwManifestPaths,  
    [in] LPCWSTR   *ppwzManifestPaths,  
    [in] DWORD     dwActivationData,  
    [in] LPCWSTR   *ppwzActivationData,  
    [out] int      *pReturnValue  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pwzAppFullName`  
 [in] Le nom complet de l’application, tel que défini pour <xref:System.ApplicationIdentity>.  
  
 `dwManifestPaths`  
 [in] Le nombre de chaînes contenues dans le `ppwzManifestPaths` tableau.  
  
 `ppwzManifestPaths`  
 [in] Facultatif. Tableau de chaînes qui contient les chemins d’accès de manifestes pour l’application.  
  
 `dwActivationData`  
 [in] Le nombre de chaînes contenues dans le `ppwzActivationData` tableau.  
  
 `ppwzActivationData`  
 [in] Facultatif. Un tableau de chaînes qui contient des données de l’activation de l’application, comme la partie de chaîne de requête de l’URL pour les applications déployées sur le Web.  
  
 `pReturnValue`  
 [out] La valeur retournée par le point d’entrée de l’application.  
  
## <a name="return-value"></a>Valeur de retour  
  
|HRESULT|Description|  
|-------------|-----------------|  
|S_OK|`ExecuteApplication` retourné avec succès.|  
|HOST_E_CLRNOTAVAILABLE|Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.|  
|HOST_E_TIMEOUT|L’appel a expiré.|  
|HOST_E_NOT_OWNER|L’appelant ne possède pas le verrou.|  
|HOST_E_ABANDONED|Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.|  
|E_FAIL|Une défaillance catastrophique inconnue s’est produite. Si une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus. Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.|  
  
## <a name="remarks"></a>Notes  
 `ExecuteApplication` est utilisé pour activer des applications ClickOnce dans un domaine d’application nouvellement créé.  
  
 Le `pReturnValue` paramètre de sortie est défini sur la valeur retournée par l’application. Si vous fournissez une valeur NULL pour `pReturnValue`, `ExecuteApplication` n’échoue pas, mais il ne retourne pas de valeur.  
  
> [!IMPORTANT]
>  N’appelez pas la [méthode Start](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-start-method.md) méthode avant d’appeler le `ExecuteApplication` méthode permettant d’activer une application basée sur un manifeste. Si le `Start` méthode est appelée en premier, le `ExecuteApplication` appel de méthode échoue.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ActivationContext>
- <xref:System.AppDomainManager>
- <xref:System.ApplicationIdentity>
- [ICLRRuntimeHost, interface](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md)
- [SetAppDomainManager, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-setappdomainmanager-method.md)
- [Procédure pas à pas : téléchargement d'assemblys à la demande avec l'API du déploiement ClickOnce à l'aide du concepteur](/visualstudio/deployment/walkthrough-downloading-assemblies-on-demand-with-the-clickonce-deployment-api-using-the-designer)
