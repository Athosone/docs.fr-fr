---
title: 'Procédure : spécifier des informations d’identification de client'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 82293d7f-471a-4549-8f19-0be890e7b074
ms.openlocfilehash: ecb8f7ef74f1f0625454eb2d6cebf9d282a5ece3
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59327098"
---
# <a name="how-to-specify-client-credential-values"></a><span data-ttu-id="57dd5-102">Procédure : spécifier des informations d’identification de client</span><span class="sxs-lookup"><span data-stu-id="57dd5-102">How to: Specify Client Credential Values</span></span>
<span data-ttu-id="57dd5-103">À l’aide de Windows Communication Foundation (WCF), le service peut spécifier comment un client est authentifié auprès du service.</span><span class="sxs-lookup"><span data-stu-id="57dd5-103">Using Windows Communication Foundation (WCF), the service can specify how a client is authenticated to the service.</span></span> <span data-ttu-id="57dd5-104">Par exemple, un service peut stipuler que le client soit authentifié avec un certificat.</span><span class="sxs-lookup"><span data-stu-id="57dd5-104">For example, a service can stipulate that the client be authenticated with a certificate.</span></span>  
  
### <a name="to-determine-the-client-credential-type"></a><span data-ttu-id="57dd5-105">Pour déterminer le type d'informations d'identification du client</span><span class="sxs-lookup"><span data-stu-id="57dd5-105">To determine the client credential type</span></span>  
  
1. <span data-ttu-id="57dd5-106">Récupérez les métadonnées à partir du point de terminaison des métadonnées du service.</span><span class="sxs-lookup"><span data-stu-id="57dd5-106">Retrieve metadata from the service's metadata endpoint.</span></span> <span data-ttu-id="57dd5-107">Les métadonnées se composent généralement de deux fichiers : le code client dans le langage de programmation de votre choix (la valeur par défaut est Visual C#) et un fichier de configuration XML.</span><span class="sxs-lookup"><span data-stu-id="57dd5-107">The metadata typically consists of two files: the client code in the programming language of your choice (the default is Visual C#), and an XML configuration file.</span></span> <span data-ttu-id="57dd5-108">L'une des manières permettant de récupérer des métadonnées consiste à utiliser l'outil Svcutil.exe pour retourner le code client et la configuration cliente.</span><span class="sxs-lookup"><span data-stu-id="57dd5-108">One way to retrieve metadata is to use the Svcutil.exe tool to return the client code and client configuration.</span></span> <span data-ttu-id="57dd5-109">Pour plus d’informations, consultez [récupérer des métadonnées](../../../docs/framework/wcf/feature-details/retrieving-metadata.md) et [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md).</span><span class="sxs-lookup"><span data-stu-id="57dd5-109">For more information, see [Retrieving Metadata](../../../docs/framework/wcf/feature-details/retrieving-metadata.md) and [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md).</span></span>  
  
2. <span data-ttu-id="57dd5-110">Ouvrez le fichier de configuration XML.</span><span class="sxs-lookup"><span data-stu-id="57dd5-110">Open the XML configuration file.</span></span> <span data-ttu-id="57dd5-111">Si vous utilisez l'outil Svcutil.exe, le nom par défaut du fichier est Output.config.</span><span class="sxs-lookup"><span data-stu-id="57dd5-111">If you use the Svcutil.exe tool, the default name of the file is Output.config.</span></span>  
  
3. <span data-ttu-id="57dd5-112">Rechercher la  **\<sécurité >** élément avec la **mode** attribut (**< mode de sécurité =** `MessageOrTransport` **>** où `MessageOrTransport` est défini sur l’un des modes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="57dd5-112">Find the **\<security>** element with the **mode** attribute (**<security mode =**`MessageOrTransport`**>** where `MessageOrTransport` is set to one of the security modes.</span></span>  
  
4. <span data-ttu-id="57dd5-113">Recherchez l'élément enfant qui correspond à la valeur de mode.</span><span class="sxs-lookup"><span data-stu-id="57dd5-113">Find the child element that matches the mode value.</span></span> <span data-ttu-id="57dd5-114">Par exemple, si le mode est défini sur **Message**, recherchez le  **\<message >** élément contenu dans le  **\<sécurité >** élément.</span><span class="sxs-lookup"><span data-stu-id="57dd5-114">For example, if the mode is set to **Message**, find the **\<message>** element contained in the **\<security>** element.</span></span>  
  
5. <span data-ttu-id="57dd5-115">Notez la valeur affectée à la **clientCredentialType** attribut.</span><span class="sxs-lookup"><span data-stu-id="57dd5-115">Note the value assigned to the **clientCredentialType** attribute.</span></span> <span data-ttu-id="57dd5-116">La valeur réelle dépend du mode utilisé, du transport ou du message.</span><span class="sxs-lookup"><span data-stu-id="57dd5-116">The actual value depends on which mode is used, transport or message.</span></span>  
  
 <span data-ttu-id="57dd5-117">Le code XML suivant montre la configuration pour un client utilisant la sécurité du message et nécessitant un certificat pour authentifier le client.</span><span class="sxs-lookup"><span data-stu-id="57dd5-117">The following XML code shows configuration for a client using message security and requiring a certificate to authenticate the client.</span></span>  
  
```xml  
<security mode="Message">  
    <transport clientCredentialType="Windows" proxyCredentialType="None"  
        realm="" />  
     <message clientCredentialType="Certificate" negotiateServiceCredential="true"  
    algorithmSuite="Default" establishSecurityContext="true" />  
</security>  
```  
  
## <a name="example-tcp-transport-mode-with-certificate-as-client-credential"></a><span data-ttu-id="57dd5-118">Exemple : Mode de Transport TCP avec certificat comme informations d’identification du Client</span><span class="sxs-lookup"><span data-stu-id="57dd5-118">Example: TCP Transport Mode with Certificate as Client Credential</span></span>  
 <span data-ttu-id="57dd5-119">Cet exemple définit le mode de sécurité sur le mode Transport et définit la valeur d'informations d'identification du client sur un certificat X.509.</span><span class="sxs-lookup"><span data-stu-id="57dd5-119">This example sets the security mode to Transport mode and sets the client credential value to an X.509 certificate.</span></span> <span data-ttu-id="57dd5-120">Les procédures suivantes montrent comment définir la valeur d'information d'identification du client sur le client dans le code et dans la configuration.</span><span class="sxs-lookup"><span data-stu-id="57dd5-120">The following procedures demonstrate how to set the client credential value on the client in code and configuration.</span></span> <span data-ttu-id="57dd5-121">Cela suppose que vous avez utilisé le [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) pour retourner les métadonnées (code et configuration) à partir du service.</span><span class="sxs-lookup"><span data-stu-id="57dd5-121">This assumes that you have used the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) to return the metadata (code and configuration) from the service.</span></span> <span data-ttu-id="57dd5-122">Pour plus d'informations, voir [Procédure : Créer un Client](../../../docs/framework/wcf/how-to-create-a-wcf-client.md).</span><span class="sxs-lookup"><span data-stu-id="57dd5-122">For more information, see [How to: Create a Client](../../../docs/framework/wcf/how-to-create-a-wcf-client.md).</span></span>  
  
#### <a name="to-specify-the-client-credential-value-on-the-client-in-code"></a><span data-ttu-id="57dd5-123">Pour spécifier la valeur d'information d'identification du client sur le client dans le code</span><span class="sxs-lookup"><span data-stu-id="57dd5-123">To specify the client credential value on the client in code</span></span>  
  
1. <span data-ttu-id="57dd5-124">Utilisez le [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) pour générer le code et la configuration à partir du service.</span><span class="sxs-lookup"><span data-stu-id="57dd5-124">Use the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) to generate code and configuration from the service.</span></span>  
  
2. <span data-ttu-id="57dd5-125">Créez une instance du client WCF à l’aide du code généré.</span><span class="sxs-lookup"><span data-stu-id="57dd5-125">Create an instance of the WCF client using the generated code.</span></span>  
  
3. <span data-ttu-id="57dd5-126">Sur la classe de client, affectez à la propriété <xref:System.ServiceModel.ClientBase%601.ClientCredentials%2A> de la classe <xref:System.ServiceModel.ClientBase%601> une valeur appropriée.</span><span class="sxs-lookup"><span data-stu-id="57dd5-126">On the client class, set the <xref:System.ServiceModel.ClientBase%601.ClientCredentials%2A> property of the <xref:System.ServiceModel.ClientBase%601> class to an appropriate value.</span></span> <span data-ttu-id="57dd5-127">Cet exemple affecte à la propriété un certificat X.509 à l'aide de la méthode <xref:System.ServiceModel.Security.X509CertificateInitiatorClientCredential.SetCertificate%2A> de la classe <xref:System.ServiceModel.Security.X509CertificateInitiatorClientCredential>.</span><span class="sxs-lookup"><span data-stu-id="57dd5-127">This example sets the property to an X.509 certificate using the <xref:System.ServiceModel.Security.X509CertificateInitiatorClientCredential.SetCertificate%2A> method of the <xref:System.ServiceModel.Security.X509CertificateInitiatorClientCredential> class.</span></span>  
  
     [!code-csharp[c_TcpService#4](../../../samples/snippets/csharp/VS_Snippets_CFX/c_tcpservice/cs/source.cs#4)]
     [!code-vb[c_TcpService#4](../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_tcpservice/vb/source.vb#4)]  
  
     <span data-ttu-id="57dd5-128">Vous pouvez utiliser n'importe lesquelles des énumérations de la classe <xref:System.Security.Cryptography.X509Certificates.X509FindType>.</span><span class="sxs-lookup"><span data-stu-id="57dd5-128">You can use any of the enumerations of the <xref:System.Security.Cryptography.X509Certificates.X509FindType> class.</span></span> <span data-ttu-id="57dd5-129">Le nom du sujet est utilisé ici au cas où le certificat serait modifié (en raison d'une date d'expiration).</span><span class="sxs-lookup"><span data-stu-id="57dd5-129">The subject name is used here in case the certificate is changed (due to an expiration date).</span></span> <span data-ttu-id="57dd5-130">L'utilisation du nom du sujet permet à l'infrastructure de retrouver le certificat.</span><span class="sxs-lookup"><span data-stu-id="57dd5-130">Using the subject name enables the infrastructure to find the certificate again.</span></span>  
  
#### <a name="to-specify-the-client-credential-value-on-the-client-in-configuration"></a><span data-ttu-id="57dd5-131">Pour spécifier la valeur d'information d'identification du client sur le client dans la configuration</span><span class="sxs-lookup"><span data-stu-id="57dd5-131">To specify the client credential value on the client in configuration</span></span>  
  
1. <span data-ttu-id="57dd5-132">Ajouter un [ \<comportement >](../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md) élément à la [ \<comportements >](../../../docs/framework/configure-apps/file-schema/wcf/behaviors.md) élément.</span><span class="sxs-lookup"><span data-stu-id="57dd5-132">Add a [\<behavior>](../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md) element to the [\<behaviors>](../../../docs/framework/configure-apps/file-schema/wcf/behaviors.md) element.</span></span>  
  
2. <span data-ttu-id="57dd5-133">Ajouter un [ \<clientCredentials >](../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md) élément à la [ \<comportements >](../../../docs/framework/configure-apps/file-schema/wcf/behaviors.md) élément.</span><span class="sxs-lookup"><span data-stu-id="57dd5-133">Add a [\<clientCredentials>](../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md) element to the [\<behaviors>](../../../docs/framework/configure-apps/file-schema/wcf/behaviors.md) element.</span></span> <span data-ttu-id="57dd5-134">Assurez-vous d'affecter à l'attribut `name` requis une valeur appropriée.</span><span class="sxs-lookup"><span data-stu-id="57dd5-134">Be sure to set the required `name` attribute to an appropriate value.</span></span>  
  
3. <span data-ttu-id="57dd5-135">Ajouter un [ \<clientCertificate >](../../../docs/framework/configure-apps/file-schema/wcf/clientcertificate-of-servicecredentials.md) élément à la [ \<clientCredentials >](../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md) élément.</span><span class="sxs-lookup"><span data-stu-id="57dd5-135">Add a [\<clientCertificate>](../../../docs/framework/configure-apps/file-schema/wcf/clientcertificate-of-servicecredentials.md) element to the [\<clientCredentials>](../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md) element.</span></span>  
  
4. <span data-ttu-id="57dd5-136">Affectez aux attributs suivants des valeurs appropriées : `storeLocation`, `storeName`, `x509FindType` et `findValue`, comme illustré dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="57dd5-136">Set the following attributes to appropriate values: `storeLocation`, `storeName`, `x509FindType`, and `findValue`, as shown in the following code.</span></span> <span data-ttu-id="57dd5-137">Pour plus d’informations sur les certificats, consultez [Utilisation de certificats](../../../docs/framework/wcf/feature-details/working-with-certificates.md).</span><span class="sxs-lookup"><span data-stu-id="57dd5-137">For more information about certificates, see [Working with Certificates](../../../docs/framework/wcf/feature-details/working-with-certificates.md).</span></span>  
  
    ```xml  
    <behaviors>  
       <endpointBehaviors>  
          <behavior name="endpointCredentialBehavior">  
            <clientCredentials>  
              <clientCertificate findValue="Contoso.com"   
                                 storeLocation="LocalMachine"  
                                 storeName="TrustedPeople"  
                                 x509FindType="FindBySubjectName" />  
            </clientCredentials>  
          </behavior>  
       </endpointBehaviors>  
    </behaviors>  
    ```  
  
5. <span data-ttu-id="57dd5-138">Lorsque vous configurez le client, spécifiez le comportement en définissant l'attribut `behaviorConfiguration` de l'élément `<endpoint>`, comme illustré dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="57dd5-138">When configuring the client, specify the behavior by setting the `behaviorConfiguration` attribute of the `<endpoint>` element, as shown in the following code.</span></span> <span data-ttu-id="57dd5-139">L’élément de point de terminaison est un enfant de la [ \<client >](../../../docs/framework/configure-apps/file-schema/wcf/client.md) élément.</span><span class="sxs-lookup"><span data-stu-id="57dd5-139">The endpoint element is a child of the [\<client>](../../../docs/framework/configure-apps/file-schema/wcf/client.md) element.</span></span> <span data-ttu-id="57dd5-140">Spécifiez également le nom de la configuration de liaison en affectant à l’attribut `bindingConfiguration` la liaison pour le client.</span><span class="sxs-lookup"><span data-stu-id="57dd5-140">Also, specify the name of the binding configuration by setting the `bindingConfiguration` attribute to the binding for the client.</span></span> <span data-ttu-id="57dd5-141">Si vous utilisez un fichier de configuration généré, le nom de la liaison est généré automatiquement.</span><span class="sxs-lookup"><span data-stu-id="57dd5-141">If you are using a generated configuration file, the binding's name is automatically generated.</span></span> <span data-ttu-id="57dd5-142">Dans cet exemple, le nom est `"tcpBindingWithCredential"`.</span><span class="sxs-lookup"><span data-stu-id="57dd5-142">In this example, the name is `"tcpBindingWithCredential"`.</span></span>  
  
    ```xml  
    <client>  
      <endpoint name =""  
                address="net.tcp://contoso.com:8036/aloha"  
                binding="netTcpBinding"  
                bindingConfiguration="tcpBindingWithCredential"  
                behaviorConfiguration="endpointCredentialBehavior" />  
    </client>  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="57dd5-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57dd5-143">See also</span></span>

- <xref:System.ServiceModel.NetTcpBinding>
- <xref:System.ServiceModel.Security.X509CertificateRecipientServiceCredential.SetCertificate%2A>
- <xref:System.ServiceModel.Security.X509CertificateRecipientServiceCredential>
- <xref:System.ServiceModel.ClientBase%601>
- <xref:System.ServiceModel.Security.X509CertificateInitiatorClientCredential>
- [<span data-ttu-id="57dd5-144">Programmation de la sécurité dans WCF</span><span class="sxs-lookup"><span data-stu-id="57dd5-144">Programming WCF Security</span></span>](../../../docs/framework/wcf/feature-details/programming-wcf-security.md)
- [<span data-ttu-id="57dd5-145">Sélection d’un type d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="57dd5-145">Selecting a Credential Type</span></span>](../../../docs/framework/wcf/feature-details/selecting-a-credential-type.md)
- [<span data-ttu-id="57dd5-146">Outil ServiceModel Metadata Utility (Svcutil.exe)</span><span class="sxs-lookup"><span data-stu-id="57dd5-146">ServiceModel Metadata Utility Tool (Svcutil.exe)</span></span>](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)
- [<span data-ttu-id="57dd5-147">Utilisation des certificats</span><span class="sxs-lookup"><span data-stu-id="57dd5-147">Working with Certificates</span></span>](../../../docs/framework/wcf/feature-details/working-with-certificates.md)
- [<span data-ttu-id="57dd5-148">Guide pratique pour Créer un Client</span><span class="sxs-lookup"><span data-stu-id="57dd5-148">How to: Create a Client</span></span>](../../../docs/framework/wcf/how-to-create-a-wcf-client.md)
- [<span data-ttu-id="57dd5-149">\<netTcpBinding></span><span class="sxs-lookup"><span data-stu-id="57dd5-149">\<netTcpBinding></span></span>](../../../docs/framework/configure-apps/file-schema/wcf/nettcpbinding.md)
- [<span data-ttu-id="57dd5-150">\<security></span><span class="sxs-lookup"><span data-stu-id="57dd5-150">\<security></span></span>](../../../docs/framework/configure-apps/file-schema/wcf/security-of-nettcpbinding.md)
- [<span data-ttu-id="57dd5-151">\<message></span><span class="sxs-lookup"><span data-stu-id="57dd5-151">\<message></span></span>](../../../docs/framework/configure-apps/file-schema/wcf/message-element-of-nettcpbinding.md)
- [<span data-ttu-id="57dd5-152">\<behavior></span><span class="sxs-lookup"><span data-stu-id="57dd5-152">\<behavior></span></span>](../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)
- [<span data-ttu-id="57dd5-153">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="57dd5-153">\<behaviors></span></span>](../../../docs/framework/configure-apps/file-schema/wcf/behaviors.md)
- [<span data-ttu-id="57dd5-154">\<clientCertificate></span><span class="sxs-lookup"><span data-stu-id="57dd5-154">\<clientCertificate></span></span>](../../../docs/framework/configure-apps/file-schema/wcf/clientcertificate-of-servicecredentials.md)
- [<span data-ttu-id="57dd5-155">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="57dd5-155">\<clientCredentials></span></span>](../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md)
