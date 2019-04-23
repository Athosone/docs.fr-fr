---
title: 'Procédure : créer un gestionnaire d’autorisations personnalisé pour un service'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Windows Communication Foundation, extending
- OperationRequirement class
ms.assetid: 6214afde-44c1-4bf5-ba07-5ad6493620ea
ms.openlocfilehash: e3d0143cd68bc94c6ff07e65ca5a3c8971b45f23
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59337836"
---
# <a name="how-to-create-a-custom-authorization-manager-for-a-service"></a>Procédure : créer un gestionnaire d’autorisations personnalisé pour un service
L’infrastructure de modèle d’identité dans Windows Communication Foundation (WCF) prend en charge un modèle extensible d’autorisation basée sur les revendications. Les revendications sont extraites de jetons et sont éventuellement traitées par les stratégies d'autorisation personnalisées puis placées dans un <xref:System.IdentityModel.Policy.AuthorizationContext>. Un gestionnaire d'autorisations examine les revendications dans le <xref:System.IdentityModel.Policy.AuthorizationContext> pour prendre des décisions concernant les autorisations.  
  
 Par défaut, les décisions relatives aux autorisations sont prises par la classe <xref:System.ServiceModel.ServiceAuthorizationManager> ; cependant, ces décisions peuvent être substituées en créant un gestionnaire d'autorisations personnalisé. Pour créer un gestionnaire d'autorisations personnalisé, créez une classe qui dérive de <xref:System.ServiceModel.ServiceAuthorizationManager> et implémente la méthode <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccessCore%2A>. Les décisions relatives aux autorisations sont prises dans la méthode <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccessCore%2A>, qui retourne la valeur `true` lorsque l'accès est accordé et `false` lorsque l'accès est refusé.  
  
 Si la décision d'autorisation dépend du contenu du corps de message, utilisez la méthode <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccess%2A>.  
  
 En raison des problèmes de performances, essayez de reconcevoir si possible votre application afin que la décision d'autorisation ne nécessite pas l'accès au corps du message.  
  
 L'enregistrement du gestionnaire d'autorisations personnalisé pour un service peut être réalisé dans du code ou dans la configuration.  
  
### <a name="to-create-a-custom-authorization-manager"></a>Pour créer un gestionnaire d'autorisations personnalisé  
  
1. Dérivez une classe d'une classe de la classe <xref:System.ServiceModel.ServiceAuthorizationManager>.  
  
     [!code-csharp[c_CustomAuthMgr#5](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_customauthmgr/cs/c_customauthmgr.cs#5)]
     [!code-vb[c_CustomAuthMgr#5](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_customauthmgr/vb/c_customauthmgr.vb#5)]  
  
2. Remplacez la méthode <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccessCore%28System.ServiceModel.OperationContext%29> .  
  
     Utilisez le <xref:System.ServiceModel.OperationContext> passé à la méthode <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccessCore%28System.ServiceModel.OperationContext%29> pour prendre des décisions concernant les autorisations.  
  
     L'exemple de code suivant utilise la méthode <xref:System.IdentityModel.Claims.ClaimSet.FindClaims%28System.String%2CSystem.String%29> pour rechercher la revendication personnalisée `http://www.contoso.com/claims/allowedoperation` afin de prendre une décision relative à une autorisation.  
  
     [!code-csharp[c_CustomAuthMgr#6](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_customauthmgr/cs/c_customauthmgr.cs#6)]
     [!code-vb[c_CustomAuthMgr#6](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_customauthmgr/vb/c_customauthmgr.vb#6)]  
  
### <a name="to-register-a-custom-authorization-manager-using-code"></a>Pour enregistrer un gestionnaire d'autorisations personnalisé à l'aide de code  
  
1. Créez une instance du gestionnaire d'autorisations personnalisé et assignez-la à la propriété <xref:System.ServiceModel.Description.ServiceAuthorizationBehavior.ServiceAuthorizationManager%2A>.  
  
     <xref:System.ServiceModel.Description.ServiceAuthorizationBehavior> est accessible à l'aide de la propriété <xref:System.ServiceModel.ServiceHostBase.Authorization%2A>.  
  
     L'exemple de code suivant enregistre le gestionnaire d'autorisations personnalisé `MyServiceAuthorizationManager`.  
  
     [!code-csharp[c_CustomAuthMgr#4](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_customauthmgr/cs/c_customauthmgr.cs#4)]
     [!code-vb[c_CustomAuthMgr#4](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_customauthmgr/vb/c_customauthmgr.vb#4)]  
  
### <a name="to-register-a-custom-authorization-manager-using-configuration"></a>Pour enregistrer un gestionnaire d'autorisations personnalisé à l'aide d'une configuration  
  
1. Ouvrez le fichier de configuration pour le service.  
  
2. Ajouter un [ \<serviceAuthorization >](../../../../docs/framework/configure-apps/file-schema/wcf/serviceauthorization-element.md) à la [ \<comportements >](../../../../docs/framework/configure-apps/file-schema/wcf/behaviors.md).  
  
     Pour le [ \<serviceAuthorization >](../../../../docs/framework/configure-apps/file-schema/wcf/serviceauthorization-element.md), ajouter un `serviceAuthorizationManagerType` d’attribut et définissez sa valeur sur le type qui représente le Gestionnaire d’autorisations personnalisé.  
  
3. Ajoutez une liaison qui sécurise la communication entre le client et le service.  
  
     La liaison choisie pour cette communication détermine les revendications ajoutées au <xref:System.IdentityModel.Policy.AuthorizationContext>, que le gestionnaire d'autorisations personnalisé utilise pour prendre des décisions concernant les autorisations. Pour plus d’informations sur les liaisons fournies par le système, consultez [System-Provided Bindings](../../../../docs/framework/wcf/system-provided-bindings.md).  
  
4. Associez le comportement à un point de terminaison de service, en ajoutant un [ \<service >](../../../../docs/framework/configure-apps/file-schema/wcf/service.md) élément et définissez la valeur de la `behaviorConfiguration` avec la valeur de l’attribut de nom pour le [ \<comportement >](../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-servicebehaviors.md) élément.  
  
     Pour plus d’informations sur la configuration d’un point de terminaison de service, consultez [Comment : Créer un point de terminaison de Service dans la Configuration](../../../../docs/framework/wcf/feature-details/how-to-create-a-service-endpoint-in-configuration.md).  
  
     L'exemple de code suivant enregistre le gestionnaire d'autorisations personnalisé `Samples.MyServiceAuthorizationManager`.  
  
    ```xml  
    <configuration>  
      <system.serviceModel>  
        <services>  
          <service   
              name="Microsoft.ServiceModel.Samples.CalculatorService"  
              behaviorConfiguration="CalculatorServiceBehavior">  
            <host>  
              <baseAddresses>  
                <add baseAddress="http://localhost:8000/ServiceModelSamples/service"/>  
              </baseAddresses>  
            </host>  
            <endpoint address=""  
                      binding="wsHttpBinding_Calculator"  
                      contract="Microsoft.ServiceModel.Samples.ICalculator" />  
          </service>  
        </services>  
        <bindings>  
          <WSHttpBinding>  
           <binding name = "wsHttpBinding_Calculator">  
             <security mode="Message">  
               <message clientCredentialType="Windows"/>  
             </security>  
            </binding>  
          </WSHttpBinding>  
    </bindings>  
        <behaviors>  
          <serviceBehaviors>  
            <behavior name="CalculatorServiceBehavior">  
              <serviceAuthorization serviceAuthorizationManagerType="Samples.MyServiceAuthorizationManager,MyAssembly" />  
             </behavior>  
         </serviceBehaviors>  
       </behaviors>  
      </system.serviceModel>  
    </configuration>  
    ```  
  
    > [!WARNING]
    >  Notez que lorsque vous spécifiez serviceAuthorizationManagerType, la chaîne doit contenir le nom de type qualifié complet. une virgule, et le nom de l'assembly dans lequel le type est défini. Si vous omettez le nom de l'assembly, WCF tentera de charger le type à partir de System.ServiceModel.dll.  
  
## <a name="example"></a>Exemple  
 L'exemple de code suivant illustre une implémentation de base d'une classe <xref:System.ServiceModel.ServiceAuthorizationManager> qui inclut la substitution de la méthode <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccessCore%2A>. L'exemple de code recherche une revendication personnalisée dans le <xref:System.IdentityModel.Policy.AuthorizationContext> et retourne la valeur `true` lorsque la ressource pour cette revendication personnalisée correspond à la valeur d'action du <xref:System.ServiceModel.OperationContext>. Pour une implémentation plus complète d’un <xref:System.ServiceModel.ServiceAuthorizationManager> de classe, consultez [stratégie d’autorisation](../../../../docs/framework/wcf/samples/authorization-policy.md).  
  
 [!code-csharp[c_CustomAuthMgr#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_customauthmgr/cs/c_customauthmgr.cs#2)]
 [!code-vb[c_CustomAuthMgr#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_customauthmgr/vb/c_customauthmgr.vb#2)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.ServiceAuthorizationManager>
- [Stratégie d’autorisation](../../../../docs/framework/wcf/samples/authorization-policy.md)
