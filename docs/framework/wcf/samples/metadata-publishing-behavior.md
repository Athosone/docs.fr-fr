---
title: Metadata Publishing Behavior
ms.date: 03/30/2017
helpviewer_keywords:
- service behaviors, metadata publishing sample
- Metadata Publishing Behaviors Sample [Windows Communication Foundation]
ms.assetid: 78c13633-d026-4814-910e-1c801cffdac7
ms.openlocfilehash: 20922636f140e0ac9faff55bf94c0b2633a8070d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59773920"
---
# <a name="metadata-publishing-behavior"></a>Metadata Publishing Behavior
Cet exemple montre comment contrôler les fonctionnalités de publication des métadonnées d’un service. Pour empêcher toute divulgation non intentionnelle de métadonnées de service potentiellement sensibles, la configuration par défaut pour les services Windows Communication Foundation (WCF) désactive la publication des métadonnées. Ce comportement est sécurisé par défaut, mais il signifie également que vous ne pouvez pas utiliser d'outil d'importation de métadonnées (tel que Svcutil.exe) pour générer le code client requis pour appeler le service, à moins que le comportement de publication des métadonnées du service soit activé explicitement dans la configuration.  
  
> [!IMPORTANT]
>  Pour plus de clarté, cet exemple montre comment créer un point de terminaison de publication de métadonnées non sécurisé. De tels points de terminaison sont potentiellement disponibles aux consommateurs non authentifiés anonymes et il est nécessaire de se montrer vigilant et de s'assurer que la divulgation publique des métadonnées d'un service est appropriée avant de déployer de tels points de terminaison. Consultez le [personnalisé sécuriser les métadonnées de point de terminaison](../../../../docs/framework/wcf/samples/custom-secure-metadata-endpoint.md) exemple pour obtenir un exemple qui sécurise un point de terminaison de métadonnées.  
  
 L’exemple est basé sur le [mise en route](../../../../docs/framework/wcf/samples/getting-started-sample.md), qui implémente le `ICalculator` contrat de service. Dans cet exemple, le client est une application console (.exe) et le service est hébergé par les services IIS (Internet Information Services).  
  
> [!NOTE]
>  La procédure d'installation ainsi que les instructions de génération relatives à cet exemple figurent à la fin de cette rubrique.  
  
 Pour qu'un service expose des métadonnées, <xref:System.ServiceModel.Description.ServiceMetadataBehavior> doit être configuré sur le service. Lorsque ce comportement est présent, vous pouvez publier des métadonnées en configurant un point de terminaison afin qu'il exposer le contrat <xref:System.ServiceModel.Description.IMetadataExchange> en tant qu'implémentation d'un protocole MEX (WS-MetadataExchange). Par commodité, le nom de configuration abrégé « IMetadataExchange » a été donné à ce contrat. Cet exemple utilise `mexHttpBinding`, qui est une liaison standard équivalente à `wsHttpBinding` dont le mode de sécurité a la valeur `None`. Une adresse relative de « mex » est utilisée dans le point de terminaison, lorsqu’elle est résolue par rapport aux base des services adresse les résultats dans une adresse de point de terminaison de `http://localhost/servicemodelsamples/service.svc/mex`. La configuration de comportement se présente comme suit :  
  
```xml  
<behaviors>  
  <serviceBehaviors>  
    <behavior name="CalculatorServiceBehavior">  
      <!-- The serviceMetadata behavior publishes metadata through   
           the IMetadataExchange contract. When this behavior is   
           present, you can expose this contract through an endpoint   
           as shown below. Setting httpGetEnabled to true publishes   
           the service's WSDL at the <baseaddress>?wsdl, for example,  
           http://localhost/servicemodelsamples/service.svc?wsdl -->  
      <serviceMetadata httpGetEnabled="True"/>  
      <serviceDebug includeExceptionDetailInFaults="False" />  
    </behavior>  
  </serviceBehaviors>  
</behaviors>  
```  
  
 Le point de terminaison MEX se présente comme suit :  
  
```xml  
<!-- the MEX endpoint is exposed at   
     http://localhost/servicemodelsamples/service.svc/mex   
     To expose the IMetadataExchange contract, you   
     must enable the serviceMetadata behavior as demonstrated                           
     previously. -->  
<endpoint address="mex"  
          binding="mexHttpBinding"  
          contract="IMetadataExchange" />  
```  
  
 Cet exemple affecte <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpGetEnabled%2A> à la propriété `true` qui expose également les métadonnées du service à l'aide de HTTP GET. Pour activer un point de terminaison de métadonnées HTTP GET, le service doit avoir une adresse de base HTTP. La chaîne de requête `?wsdl` est utilisée sur l'adresse de base du service pour accéder aux métadonnées. Par exemple, pour voir le WSDL pour le service dans un navigateur Web vous utiliseriez l’adresse `http://localhost/servicemodelsamples/service.svc?wsdl`. Vous pouvez également utiliser ce comportement pour exposer des métadonnées sur HTTPS en affectant <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpsGetEnabled%2A> à `true`. Cela requiert une adresse de base HTTPS.  
  
 Pour accéder à utiliser de point de terminaison MEX du service le [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md).  
  
 `svcutil.exe /n:"http://Microsoft.ServiceModel.Samples,Microsoft.ServiceModel.Samples" http://localhost/servicemodelsamples/service.svc/mex /out:generatedClient.cs`  
  
 Cette opération génère un client basé sur les métadonnées du service.  
  
 Pour accéder aux métadonnées du service à l’aide de HTTP GET, dirigez votre navigateur vers `http://localhost/servicemodelsamples/service.svc?wsdl`.  
  
 Si vous supprimez ce comportement et tentez d'ouvrir le service, vous obtenez une exception. Cette erreur se produit car sans le comportement, le point de terminaison configuré avec le contrat `IMetadataExchange` n'a aucune implémentation.  
  
 Si vous affectez `HttpGetEnabled` à `false`, la page d'aide CalculatorService s'affiche à la place des métadonnées du service.  
  
### <a name="to-set-up-build-and-run-the-sample"></a>Pour configurer, générer et exécuter l'exemple  
  
1. Vérifiez que vous avez effectué la [procédure d’installation unique pour les exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).  
  
2. Pour générer l’édition C# ou Visual Basic .NET de la solution, conformez-vous aux instructions figurant dans [Building the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/building-the-samples.md).  
  
3. Pour exécuter l’exemple dans une configuration unique ou plusieurs ordinateurs, suivez les instructions de [en cours d’exécution les exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/running-the-samples.md).  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Services\Behaviors\Metadata`  
