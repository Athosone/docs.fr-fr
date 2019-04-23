---
title: Service Auditing Behavior
ms.date: 03/30/2017
ms.assetid: 59bf0cda-e496-4418-a3a1-2f0f6e85f8ce
ms.openlocfilehash: 1719db9749336d584627280aba3412557b164356
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59310393"
---
# <a name="service-auditing-behavior"></a>Service Auditing Behavior
Cet exemple montre comment utiliser <xref:System.ServiceModel.Description.ServiceSecurityAuditBehavior> pour activer l'audit des événements de sécurité pendant des opérations de service. Cet exemple est basé sur le [mise en route](../../../../docs/framework/wcf/samples/getting-started-sample.md). Le service et le client ont été configurés à l’aide de la [ \<wsHttpBinding >](../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md). Le `mode` attribut de la [ \<sécurité >](../../../../docs/framework/configure-apps/file-schema/wcf/security-of-custombinding.md) a été défini sur `Message` et `clientCredentialType` a été défini sur `Windows`. Dans cet exemple, le client est une application console (.exe) et le service est hébergé par les services IIS (Internet Information Services).  
  
> [!NOTE]
>  La procédure d'installation ainsi que les instructions de génération relatives à cet exemple figurent à la fin de cette rubrique.  
  
 Le fichier de configuration de service utilise l'élément `serviceSecurityAudit` pour configurer l'audit.  
  
```xml  
<behaviors>  
  <serviceBehaviors>  
    <behavior name="CalculatorServiceBehavior">  
      ...  
<!-- serviceSecurityAudit allows specification of audit location   
     and whether to audit success, failure or both. This service   
     logs success and failure of messageAuthentication   
     to the default location -->  
     <serviceSecurityAudit auditLogLocation ="Default" messageAuthenticationAuditLevel = "SuccessOrFailure" />  
    </behavior>  
  </serviceBehaviors>  
</behaviors>  
```  
  
 Lorsque vous exécutez l'exemple, les demandes et réponses d'opération s'affichent dans la fenêtre de console du client. Appuyez sur ENTER dans la fenêtre de console pour arrêter le client.  
  
 Les journaux d'audit résultants peuvent être consultés en exécutant l'Observateur d'événements. Par défaut, les événements d’audit peuvent être consultés sur Windows XP dans le journal d’application, tandis que sur Windows Server 2003 et Windows Vista, ils peuvent être consultés dans le journal de sécurité. Les événements d'audit peuvent être consultés sur Windows Server 2008 et Windows 7 dans les journaux d'application et de services. L’emplacement des événements d’audit peut être spécifié en définissant le `auditLogLocation` l’attribut « Application » ou « Sécurité ». Pour plus d'informations, voir [Procédure : Auditer les événements de sécurité](../../../../docs/framework/wcf/feature-details/how-to-audit-wcf-security-events.md). Si les événements sont écrits dans le journal de sécurité LocalSecurityPolicy -> Qu'enable Object Access doit être définie pour « Success » et « Failure ».  
  
 Lors de la consultation du journal des événements, la source des événements d'audit est « ServiceModel Audit 3.0.0.0 ». Enregistrements d’audit authentification du message portent la catégorie « MessageAuthentication » tandis que les enregistrements d’audit d’autorisation du service portent la catégorie « ServiceAuthorization ».  
  
 Les événements de l'audit d'authentification du message permettent de savoir si le message a été falsifié, s'il a expiré et si le client peut s'authentifier auprès du service. Ils fournissent des informations sur la réussite ou l'échec de l'authentification, l'identité du client, le point de terminaison auquel le message a été envoyé et l'action associée au message.  
  
 Les événements de l'audit d'autorisation du service permettent de connaître la décision d'autorisation prise par un gestionnaire d'autorisation du service. Ils fournissent des informations sur la réussite ou l'échec de l'autorisation, ainsi que l'identité du client, le point de terminaison auquel le message a été envoyé, l'action associée au message, l'identificateur du contexte d'autorisation généré à partir du message entrant et le type du gestionnaire d'autorisations qui a pris la décision d'accès.  
  
### <a name="to-set-up-build-and-run-the-sample"></a>Pour configurer, générer et exécuter l'exemple  
  
1. Vérifiez que vous avez effectué la [procédure d’installation unique pour les exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).  
  
2. Pour générer l’édition C# ou Visual Basic .NET de la solution, conformez-vous aux instructions figurant dans [Building the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/building-the-samples.md).  
  
3. Pour exécuter l’exemple dans une configuration unique ou plusieurs ordinateurs, suivez les instructions de [en cours d’exécution les exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/running-the-samples.md).  
  
## <a name="see-also"></a>Voir aussi

- [Audit](../../../../docs/framework/wcf/feature-details/auditing-security-events.md)
- [Guide pratique pour Auditer les événements de sécurité](../../../../docs/framework/wcf/feature-details/how-to-audit-wcf-security-events.md)
