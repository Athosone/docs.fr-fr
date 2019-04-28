---
title: Sécurité de message avec certificats mutuels
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 99d7a528-7ae4-4d39-a0f9-3066ea237de0
ms.openlocfilehash: 8fc8d6d4a63b7a752fb8c26991d904761fdcebdd
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61923061"
---
# <a name="message-security-with-mutual-certificates"></a><span data-ttu-id="cfc02-102">Sécurité de message avec certificats mutuels</span><span class="sxs-lookup"><span data-stu-id="cfc02-102">Message Security with Mutual Certificates</span></span>
<span data-ttu-id="cfc02-103">Le scénario suivant illustre un service Windows Communication Foundation (WCF) et le client sécurisé à l’aide du mode de sécurité de message.</span><span class="sxs-lookup"><span data-stu-id="cfc02-103">The following scenario shows a Windows Communication Foundation (WCF) service and client secured using message security mode.</span></span> <span data-ttu-id="cfc02-104">Le client et le service sont authentifiés à l'aide de certificats.</span><span class="sxs-lookup"><span data-stu-id="cfc02-104">The client and the service are authenticated with certificates.</span></span>  
  
 <span data-ttu-id="cfc02-105">Ce scénario est interopérable car il utilise WS-Security avec le profil de jeton de certificat X.509.</span><span class="sxs-lookup"><span data-stu-id="cfc02-105">This scenario is interoperable because it uses WS-Security with the X.509 certificate token profile.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="cfc02-106">Ce scénario n'effectue pas la négociation du certificat de service.</span><span class="sxs-lookup"><span data-stu-id="cfc02-106">This scenario does not perform negotiation of the service certificate.</span></span> <span data-ttu-id="cfc02-107">Le certificat de service doit être fourni au client avant toute communication.</span><span class="sxs-lookup"><span data-stu-id="cfc02-107">The service certificate must be provided to the client in advance of any communication.</span></span> <span data-ttu-id="cfc02-108">Le certificat de serveur peut être distribué avec l'application ou fourni dans une communication hors plage.</span><span class="sxs-lookup"><span data-stu-id="cfc02-108">The server certificate can be distributed with the application or provided in an out-of-band communication.</span></span>  
  
 <span data-ttu-id="cfc02-109">![Message de sécurité avec certificats mutuels](../../../../docs/framework/wcf/feature-details/media/f4157312-b17c-416c-a5ee-fa7b54db211b.gif "f4157312-b17c-416c-a5ee-fa7b54db211b")</span><span class="sxs-lookup"><span data-stu-id="cfc02-109">![Message security with mutual certificates](../../../../docs/framework/wcf/feature-details/media/f4157312-b17c-416c-a5ee-fa7b54db211b.gif "f4157312-b17c-416c-a5ee-fa7b54db211b")</span></span>  
  
|<span data-ttu-id="cfc02-110">Caractéristique</span><span class="sxs-lookup"><span data-stu-id="cfc02-110">Characteristic</span></span>|<span data-ttu-id="cfc02-111">Description</span><span class="sxs-lookup"><span data-stu-id="cfc02-111">Description</span></span>|  
|--------------------|-----------------|  
|<span data-ttu-id="cfc02-112">Mode de sécurité</span><span class="sxs-lookup"><span data-stu-id="cfc02-112">Security Mode</span></span>|<span data-ttu-id="cfc02-113">Message</span><span class="sxs-lookup"><span data-stu-id="cfc02-113">Message</span></span>|  
|<span data-ttu-id="cfc02-114">Interopérabilité</span><span class="sxs-lookup"><span data-stu-id="cfc02-114">Interoperability</span></span>|<span data-ttu-id="cfc02-115">Oui, avec WS-Security et des clients et des services compatibles avec le profil de jeton de certificat X.509.</span><span class="sxs-lookup"><span data-stu-id="cfc02-115">Yes, with WS-Security and X.509 certificate token profile compatible clients and services.</span></span>|  
|<span data-ttu-id="cfc02-116">Authentification</span><span class="sxs-lookup"><span data-stu-id="cfc02-116">Authentication</span></span>|<span data-ttu-id="cfc02-117">Authentification mutuelle du serveur et du client.</span><span class="sxs-lookup"><span data-stu-id="cfc02-117">Mutual authentication of the server and client.</span></span>|  
|<span data-ttu-id="cfc02-118">Intégrité</span><span class="sxs-lookup"><span data-stu-id="cfc02-118">Integrity</span></span>|<span data-ttu-id="cfc02-119">Oui</span><span class="sxs-lookup"><span data-stu-id="cfc02-119">Yes</span></span>|  
|<span data-ttu-id="cfc02-120">Confidentialité</span><span class="sxs-lookup"><span data-stu-id="cfc02-120">Confidentiality</span></span>|<span data-ttu-id="cfc02-121">Oui</span><span class="sxs-lookup"><span data-stu-id="cfc02-121">Yes</span></span>|  
|<span data-ttu-id="cfc02-122">Transport</span><span class="sxs-lookup"><span data-stu-id="cfc02-122">Transport</span></span>|<span data-ttu-id="cfc02-123">HTTP</span><span class="sxs-lookup"><span data-stu-id="cfc02-123">HTTP</span></span>|  
|<span data-ttu-id="cfc02-124">Liaison</span><span class="sxs-lookup"><span data-stu-id="cfc02-124">Binding</span></span>|<xref:System.ServiceModel.WSHttpBinding>|  
  
## <a name="service"></a><span data-ttu-id="cfc02-125">Service</span><span class="sxs-lookup"><span data-stu-id="cfc02-125">Service</span></span>  
 <span data-ttu-id="cfc02-126">La configuration et le code ci-dessous sont conçus pour s'exécuter indépendamment.</span><span class="sxs-lookup"><span data-stu-id="cfc02-126">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="cfc02-127">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="cfc02-127">Do one of the following:</span></span>  
  
- <span data-ttu-id="cfc02-128">Créez un service autonome à l'aide du code sans configuration.</span><span class="sxs-lookup"><span data-stu-id="cfc02-128">Create a stand-alone service using the code with no configuration.</span></span>  
  
- <span data-ttu-id="cfc02-129">Créez un service à l'aide de la configuration fournie, mais ne définissez pas de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="cfc02-129">Create a service using the supplied configuration, but do not define any endpoints.</span></span>  
  
### <a name="code"></a><span data-ttu-id="cfc02-130">Code</span><span class="sxs-lookup"><span data-stu-id="cfc02-130">Code</span></span>  
 <span data-ttu-id="cfc02-131">Le code ci-dessous crée un point de terminaison de service qui utilise la sécurité de message.</span><span class="sxs-lookup"><span data-stu-id="cfc02-131">The following code shows creates a service endpoint that uses message security.</span></span> <span data-ttu-id="cfc02-132">Le service requiert un certificat pour s'authentifier.</span><span class="sxs-lookup"><span data-stu-id="cfc02-132">The service requires a certificate to authenticate itself.</span></span>  
  
 [!code-csharp[C_SecurityScenarios#13](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#13)]
 [!code-vb[C_SecurityScenarios#13](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#13)]  
  
### <a name="configuration"></a><span data-ttu-id="cfc02-133">Configuration</span><span class="sxs-lookup"><span data-stu-id="cfc02-133">Configuration</span></span>  
 <span data-ttu-id="cfc02-134">La configuration ci-dessous peut être utilisée à la place du code pour créer le même service.</span><span class="sxs-lookup"><span data-stu-id="cfc02-134">The following configuration can be used instead of the code to create the same service.</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
    <behaviors>  
      <serviceBehaviors>  
        <behavior name="serviceCredentialBehavior">  
          <serviceCredentials>  
            <serviceCertificate findValue="Contoso.com"   
                                storeLocation="LocalMachine"  
                                storeName="My"   
                                x509FindType="FindBySubjectName" />  
          </serviceCredentials>  
        </behavior>  
      </serviceBehaviors>  
    </behaviors>  
    <services>  
      <service behaviorConfiguration="serviceCredentialBehavior"   
               name="ServiceModel.Calculator">  
        <endpoint address="http://localhost/Calculator"   
                  binding="wsHttpBinding"  
                  bindingConfiguration="InteropCertificateBinding"  
                  name="WSHttpBinding_ICalculator"  
                  contract="ServiceModel.ICalculator" />  
      </service>  
    </services>  
    <bindings>  
      <wsHttpBinding>  
        <binding name="InteropCertificateBinding">  
          <security mode="Message">  
            <message clientCredentialType="Certificate"  
                     negotiateServiceCredential="false"  
                     establishSecurityContext="false" />  
          </security>  
        </binding>  
      </wsHttpBinding>  
    </bindings>  
    <client />  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="client"></a><span data-ttu-id="cfc02-135">Client</span><span class="sxs-lookup"><span data-stu-id="cfc02-135">Client</span></span>  
 <span data-ttu-id="cfc02-136">La configuration et le code ci-dessous sont conçus pour s'exécuter indépendamment.</span><span class="sxs-lookup"><span data-stu-id="cfc02-136">The following code and configuration are meant to run independently.</span></span> <span data-ttu-id="cfc02-137">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="cfc02-137">Do one of the following:</span></span>  
  
- <span data-ttu-id="cfc02-138">Créez un client autonome à l'aide du code (et du code client).</span><span class="sxs-lookup"><span data-stu-id="cfc02-138">Create a stand-alone client using the code (and client code).</span></span>  
  
- <span data-ttu-id="cfc02-139">Créez un client qui ne définit pas d'adresse de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="cfc02-139">Create a client that does not define any endpoint addresses.</span></span> <span data-ttu-id="cfc02-140">Au lieu de cela, utilisez le constructeur client qui accepte le nom de configuration comme argument.</span><span class="sxs-lookup"><span data-stu-id="cfc02-140">Instead, use the client constructor that takes the configuration name as an argument.</span></span> <span data-ttu-id="cfc02-141">Exemple :</span><span class="sxs-lookup"><span data-stu-id="cfc02-141">For example:</span></span>  
  
     [!code-csharp[C_SecurityScenarios#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#0)]
     [!code-vb[C_SecurityScenarios#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#0)]  
  
### <a name="code"></a><span data-ttu-id="cfc02-142">Code</span><span class="sxs-lookup"><span data-stu-id="cfc02-142">Code</span></span>  
 <span data-ttu-id="cfc02-143">Le code ci-dessous crée le client.</span><span class="sxs-lookup"><span data-stu-id="cfc02-143">The following code creates the client.</span></span> <span data-ttu-id="cfc02-144">Le mode de sécurité a la valeur Message et le type d'informations d'identification client a la valeur Certificat.</span><span class="sxs-lookup"><span data-stu-id="cfc02-144">The security mode is set to Message, and the client credential type is set to Certificate.</span></span>  
  
 [!code-csharp[C_SecurityScenarios#20](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#20)]
 [!code-vb[C_SecurityScenarios#20](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#20)]  
  
### <a name="configuration"></a><span data-ttu-id="cfc02-145">Configuration</span><span class="sxs-lookup"><span data-stu-id="cfc02-145">Configuration</span></span>  
 <span data-ttu-id="cfc02-146">Les éléments ci-dessous configurent le client.</span><span class="sxs-lookup"><span data-stu-id="cfc02-146">The following configures the client.</span></span> <span data-ttu-id="cfc02-147">Un certificat client doit être spécifié à l’aide de la [ \<clientCertificate >](../../../../docs/framework/configure-apps/file-schema/wcf/clientcertificate-of-clientcredentials-element.md).</span><span class="sxs-lookup"><span data-stu-id="cfc02-147">A client certificate must be specified using the [\<clientCertificate>](../../../../docs/framework/configure-apps/file-schema/wcf/clientcertificate-of-clientcredentials-element.md).</span></span> <span data-ttu-id="cfc02-148">En outre, le certificat de service est spécifié en utilisant le [ \<defaultCertificate >](../../../../docs/framework/configure-apps/file-schema/wcf/defaultcertificate-element.md).</span><span class="sxs-lookup"><span data-stu-id="cfc02-148">Also, the service certificate is specified using the [\<defaultCertificate>](../../../../docs/framework/configure-apps/file-schema/wcf/defaultcertificate-element.md).</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
    <behaviors>  
      <endpointBehaviors>  
        <behavior name="ClientCredentialsBehavior">  
          <clientCredentials>  
            <clientCertificate findValue="Cohowinery.com"   
                 storeLocation="CurrentUser"  
                 storeName="My"  
                 x509FindType="FindBySubjectName" />  
            <serviceCertificate>  
              <defaultCertificate findValue="Contoso.com"   
                                  storeLocation="CurrentUser"  
                                  storeName="TrustedPeople"  
                                  x509FindType="FindBySubjectName" />  
            </serviceCertificate>  
          </clientCredentials>  
        </behavior>  
      </endpointBehaviors>  
    </behaviors>  
    <bindings>  
      <wsHttpBinding>  
        <binding name="WSHttpBinding_ICalculator" >  
          <security mode="Message">  
            <message clientCredentialType="Certificate"   
                     negotiateServiceCredential="false"  
                     establishSecurityContext="false" />  
          </security>  
        </binding>  
      </wsHttpBinding>  
    </bindings>  
    <client>  
      <endpoint address="http://machineName/Calculator"   
                behaviorConfiguration="ClientCredentialsBehavior"  
                binding="wsHttpBinding"   
                bindingConfiguration="WSHttpBinding_ICalculator"  
                contract="ICalculator"  
                name="WSHttpBinding_ICalculator">  
        <identity>  
          <certificate encodedValue="Encoded_Value_Not_Shown" />  
        </identity>  
      </endpoint>  
    </client>  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="cfc02-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfc02-149">See also</span></span>

- [<span data-ttu-id="cfc02-150">Vue d’ensemble de la sécurité</span><span class="sxs-lookup"><span data-stu-id="cfc02-150">Security Overview</span></span>](../../../../docs/framework/wcf/feature-details/security-overview.md)
- [<span data-ttu-id="cfc02-151">Modèle de sécurité pour Windows Server AppFabric</span><span class="sxs-lookup"><span data-stu-id="cfc02-151">Security Model for Windows Server App Fabric</span></span>](https://go.microsoft.com/fwlink/?LinkID=201279&clcid=0x409)
- [<span data-ttu-id="cfc02-152">Guide pratique pour Créer et installer des certificats temporaires dans WCF pour la sécurité de Transport pendant le développement</span><span class="sxs-lookup"><span data-stu-id="cfc02-152">How to: Create and Install Temporary Certificates in WCF for Transport Security During Development</span></span>](https://go.microsoft.com/fwlink/?LinkId=244264)
