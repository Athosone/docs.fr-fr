---
title: 'Procédure : utiliser la sécurité du transport et des informations d’identification de message'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- TransportWithMessageCredentials
ms.assetid: 6cc35346-c37a-4859-b82b-946c0ba6e68f
ms.openlocfilehash: f9c90ac93a27f90479ee7225f62afb98a5000fe9
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59321474"
---
# <a name="how-to-use-transport-security-and-message-credentials"></a><span data-ttu-id="e9ce0-102">Procédure : utiliser la sécurité du transport et des informations d’identification de message</span><span class="sxs-lookup"><span data-stu-id="e9ce0-102">How to: Use Transport Security and Message Credentials</span></span>
<span data-ttu-id="e9ce0-103">Sécurisation d’un service avec les informations d’identification de transport et message utilise le meilleur des modes de sécurité de Transport et Message dans Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="e9ce0-103">Securing a service with both transport and message credentials uses the best of both Transport and Message security modes in Windows Communication Foundation (WCF).</span></span> <span data-ttu-id="e9ce0-104">En résumé, la sécurité de la couche de transport assure l'intégrité et la confidentialité des informations tandis que la sécurité de la couche de message offre diverses informations d'identification, lesquelles ne sont pas disponibles lorsque seule la sécurité de niveau transport est utilisée.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-104">In sum, transport-layer security provides integrity and confidentiality, while message-layer security provides a variety of credentials that are not possible with strict transport security mechanisms.</span></span> <span data-ttu-id="e9ce0-105">Cette rubrique contient la procédure par étape permettant d’implémenter la sécurité de transport avec les informations d’identification de message à l’aide des liaisons <xref:System.ServiceModel.WSHttpBinding> et <xref:System.ServiceModel.NetTcpBinding>.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-105">This topic shows the basic steps for implementing transport with message credentials using the <xref:System.ServiceModel.WSHttpBinding> and <xref:System.ServiceModel.NetTcpBinding> bindings.</span></span> <span data-ttu-id="e9ce0-106">Pour plus d’informations sur la définition du mode de sécurité, consultez [Comment : Définir le Mode de sécurité](../../../../docs/framework/wcf/how-to-set-the-security-mode.md).</span><span class="sxs-lookup"><span data-stu-id="e9ce0-106">For more information about setting the security mode, see [How to: Set the Security Mode](../../../../docs/framework/wcf/how-to-set-the-security-mode.md).</span></span>  
  
 <span data-ttu-id="e9ce0-107">Lorsque vous affectez au mode de sécurité la valeur `TransportWithMessageCredential`, le mécanisme chargé d'offrir la sécurité de niveau transport dépend du transport utilisé.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-107">When setting the security mode to `TransportWithMessageCredential`, the transport determines the actual mechanism that provides the transport-level security.</span></span> <span data-ttu-id="e9ce0-108">Pour le transport HTTP, le mécanisme utilisé est Secure Sockets Layer (SSL) sur HTTP, c'est-à-dire HTTPS, pour le transport TCP, il s'agit de SSL sur TCP ou de Windows.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-108">For HTTP, the mechanism is Secure Sockets Layer (SSL) over HTTP (HTTPS); for TCP, it is SSL over TCP or Windows.</span></span>  
  
 <span data-ttu-id="e9ce0-109">Si le transport correspond à HTTP (à l'aide de la liaison <xref:System.ServiceModel.WSHttpBinding>), la sécurité de niveau transport est assurée par SSL sur HTTP.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-109">If the transport is HTTP (using the <xref:System.ServiceModel.WSHttpBinding>), SSL over HTTP provides the transport-level security.</span></span> <span data-ttu-id="e9ce0-110">Dans ce cas, vous devez configurer l’ordinateur hébergeant le service en attribuant un certificat SSL à l’un de ses ports, comme indiqué ci-après dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-110">In that case, you must configure the computer hosting the service with an SSL certificate bound to a port, as shown later in this topic.</span></span>  
  
 <span data-ttu-id="e9ce0-111">Si le transport correspond à TCP (à l'aide de la liaison <xref:System.ServiceModel.NetTcpBinding>), la sécurité de niveau transport est assurée par la sécurité Windows ou par SSL sur TCP.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-111">If the transport is TCP (using the <xref:System.ServiceModel.NetTcpBinding>), by default the transport-level security provided is Windows security, or SSL over TCP.</span></span> <span data-ttu-id="e9ce0-112">Lorsque vous utilisez la sécurité SSL sur TCP, vous devez spécifier le certificat à l'aide de la méthode <xref:System.ServiceModel.Security.X509CertificateRecipientServiceCredential.SetCertificate%2A>, comme indiqué ci-après dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-112">When using SSL over TCP, you must specify the certificate using the <xref:System.ServiceModel.Security.X509CertificateRecipientServiceCredential.SetCertificate%2A> method, as shown later in this topic.</span></span>  
  
### <a name="to-use-the-wshttpbinding-with-a-certificate-for-transport-security-in-code"></a><span data-ttu-id="e9ce0-113">Pour utiliser la liaison WSHttpBinding avec un certificat pour la sécurité de niveau transport (dans le code)</span><span class="sxs-lookup"><span data-stu-id="e9ce0-113">To use the WSHttpBinding with a certificate for transport security (in code)</span></span>  
  
1. <span data-ttu-id="e9ce0-114">Utilisez l’outil HttpCfg.exe pour attribuer un certificat SSL à l’un des ports de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-114">Use the HttpCfg.exe tool to bind an SSL certificate to a port on the machine.</span></span> <span data-ttu-id="e9ce0-115">Pour plus d'informations, voir [Procédure : Configurer un Port avec un certificat SSL](../../../../docs/framework/wcf/feature-details/how-to-configure-a-port-with-an-ssl-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="e9ce0-115">For more information, see [How to: Configure a Port with an SSL Certificate](../../../../docs/framework/wcf/feature-details/how-to-configure-a-port-with-an-ssl-certificate.md).</span></span>  
  
2. <span data-ttu-id="e9ce0-116">Créez une instance de la classe <xref:System.ServiceModel.WSHttpBinding>, puis affectez à la propriété <xref:System.ServiceModel.WSHttpSecurity.Mode%2A> la valeur <xref:System.ServiceModel.SecurityMode.TransportWithMessageCredential>.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-116">Create an instance of the <xref:System.ServiceModel.WSHttpBinding> class and set the <xref:System.ServiceModel.WSHttpSecurity.Mode%2A> property to <xref:System.ServiceModel.SecurityMode.TransportWithMessageCredential>.</span></span>  
  
3. <span data-ttu-id="e9ce0-117">Affectez à la propriété <xref:System.ServiceModel.HttpTransportSecurity.ClientCredentialType%2A> une valeur appropriée.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-117">Set the <xref:System.ServiceModel.HttpTransportSecurity.ClientCredentialType%2A> property to an appropriate value.</span></span> <span data-ttu-id="e9ce0-118">(Pour plus d’informations, consultez [sélection d’un Type d’informations d’identification](../../../../docs/framework/wcf/feature-details/selecting-a-credential-type.md).) Dans l'exemple de code suivant, la valeur <xref:System.ServiceModel.MessageCredentialType.Certificate> est utilisée.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-118">(For more information, see [Selecting a Credential Type](../../../../docs/framework/wcf/feature-details/selecting-a-credential-type.md).) The following code uses the <xref:System.ServiceModel.MessageCredentialType.Certificate> value.</span></span>  
  
4. <span data-ttu-id="e9ce0-119">Créez une instance de la classe <xref:System.Uri> en utilisant une adresse de base appropriée.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-119">Create an instance of the <xref:System.Uri> class with an appropriate base address.</span></span> <span data-ttu-id="e9ce0-120">Remarque : cette adresse doit utiliser le schéma HTTPS et contenir le véritable nom de l’ordinateur ainsi que le numéro de port auquel le certificat SSL a été attribué.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-120">Note that the address must use the "HTTPS" scheme and must contain the actual name of the machine and the port number that the SSL certificate is bound to.</span></span> <span data-ttu-id="e9ce0-121">Vous pouvez également définir l'adresse de base dans la configuration.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-121">(Alternatively, you can set the base address in configuration.)</span></span>  
  
5. <span data-ttu-id="e9ce0-122">Ajoutez un point de terminaison de service à l'aide de la méthode <xref:System.ServiceModel.ServiceHost.AddServiceEndpoint%2A>.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-122">Add a service endpoint using the <xref:System.ServiceModel.ServiceHost.AddServiceEndpoint%2A> method.</span></span>  
  
6. <span data-ttu-id="e9ce0-123">Créez une instance de <xref:System.ServiceModel.ServiceHost>, puis appelez la méthode <xref:System.ServiceModel.ICommunicationObject.Open%2A>, comme illustré dans l'exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-123">Create the instance of the <xref:System.ServiceModel.ServiceHost> and call the <xref:System.ServiceModel.ICommunicationObject.Open%2A> method, as shown in the following code.</span></span>  
  
     [!code-csharp[c_SettingSecurityMode#7](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_settingsecuritymode/cs/source.cs#7)]
     [!code-vb[c_SettingSecurityMode#7](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_settingsecuritymode/vb/source.vb#7)]  
  
### <a name="to-use-the-nettcpbinding-with-a-certificate-for-transport-security-in-code"></a><span data-ttu-id="e9ce0-124">Pour utiliser la liaison NetTcpBinding avec un certificat pour la sécurité de niveau transport (dans le code)</span><span class="sxs-lookup"><span data-stu-id="e9ce0-124">To use the NetTcpBinding with a certificate for transport security (in code)</span></span>  
  
1. <span data-ttu-id="e9ce0-125">Créez une instance de la classe <xref:System.ServiceModel.NetTcpBinding>, puis affectez à la propriété <xref:System.ServiceModel.NetTcpSecurity.Mode%2A> la valeur <xref:System.ServiceModel.SecurityMode.TransportWithMessageCredential>.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-125">Create an instance of the <xref:System.ServiceModel.NetTcpBinding> class and set the <xref:System.ServiceModel.NetTcpSecurity.Mode%2A> property to <xref:System.ServiceModel.SecurityMode.TransportWithMessageCredential>.</span></span>  
  
2. <span data-ttu-id="e9ce0-126">Affectez à la propriété <xref:System.ServiceModel.MessageSecurityOverTcp.ClientCredentialType%2A> une valeur appropriée.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-126">Set the <xref:System.ServiceModel.MessageSecurityOverTcp.ClientCredentialType%2A> to an appropriate value.</span></span> <span data-ttu-id="e9ce0-127">Dans l'exemple de code suivant, la valeur <xref:System.ServiceModel.MessageCredentialType.Certificate> est utilisée.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-127">The following code uses the <xref:System.ServiceModel.MessageCredentialType.Certificate> value.</span></span>  
  
3. <span data-ttu-id="e9ce0-128">Créez une instance de la classe <xref:System.Uri> en utilisant une adresse de base appropriée.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-128">Create an instance of the <xref:System.Uri> class with an appropriate base address.</span></span> <span data-ttu-id="e9ce0-129">Remarque : cette adresse doit utiliser le schéma « net.tcp ».</span><span class="sxs-lookup"><span data-stu-id="e9ce0-129">Note that the address must use the "net.tcp" scheme.</span></span> <span data-ttu-id="e9ce0-130">Vous pouvez également définir l'adresse de base dans la configuration.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-130">(Alternatively, you can set the base address in configuration.)</span></span>  
  
4. <span data-ttu-id="e9ce0-131">Créez une instance de la classe <xref:System.ServiceModel.ServiceHost>.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-131">Create the instance of the <xref:System.ServiceModel.ServiceHost> class.</span></span>  
  
5. <span data-ttu-id="e9ce0-132">Utilisez la méthode <xref:System.ServiceModel.Security.X509CertificateRecipientServiceCredential.SetCertificate%2A> de la classe <xref:System.ServiceModel.Security.X509CertificateRecipientServiceCredential> pour définir de manière explicite le certificat X.509 de ce service.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-132">Use the <xref:System.ServiceModel.Security.X509CertificateRecipientServiceCredential.SetCertificate%2A> method of the <xref:System.ServiceModel.Security.X509CertificateRecipientServiceCredential> class to explicitly set the X.509 certificate for the service.</span></span>  
  
6. <span data-ttu-id="e9ce0-133">Ajoutez un point de terminaison de service à l'aide de la méthode <xref:System.ServiceModel.ServiceHost.AddServiceEndpoint%2A>.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-133">Add a service endpoint using the <xref:System.ServiceModel.ServiceHost.AddServiceEndpoint%2A> method.</span></span>  
  
7. <span data-ttu-id="e9ce0-134">Appelez la méthode <xref:System.ServiceModel.ICommunicationObject.Open%2A>, comme illustré dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="e9ce0-134">Call the <xref:System.ServiceModel.ICommunicationObject.Open%2A> method, as shown in the following code.</span></span>  
  
     [!code-csharp[c_SettingSecurityMode#8](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_settingsecuritymode/cs/source.cs#8)]
     [!code-vb[c_SettingSecurityMode#8](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_settingsecuritymode/vb/source.vb#8)]  
  
### <a name="to-use-the-nettcpbinding-with-windows-for-transport-security-in-code"></a><span data-ttu-id="e9ce0-135">Pour utiliser la liaison NetTcpBinding avec Windows comme sécurité de transport (dans le code)</span><span class="sxs-lookup"><span data-stu-id="e9ce0-135">To use the NetTcpBinding with Windows for transport security (in code)</span></span>  
  
1. <span data-ttu-id="e9ce0-136">Créez une instance de la classe <xref:System.ServiceModel.NetTcpBinding>, puis affectez à la propriété <xref:System.ServiceModel.NetTcpSecurity.Mode%2A> la valeur <xref:System.ServiceModel.SecurityMode.TransportWithMessageCredential>.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-136">Create an instance of the <xref:System.ServiceModel.NetTcpBinding> class and set the <xref:System.ServiceModel.NetTcpSecurity.Mode%2A> property to <xref:System.ServiceModel.SecurityMode.TransportWithMessageCredential>.</span></span>  
  
2. <span data-ttu-id="e9ce0-137">Configurez la sécurité de transport sur Windows en affectant à la propriété <xref:System.ServiceModel.TcpTransportSecurity.ClientCredentialType%2A> la valeur <xref:System.ServiceModel.TcpClientCredentialType.Windows>.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-137">Set the transport security to use Windows by setting the <xref:System.ServiceModel.TcpTransportSecurity.ClientCredentialType%2A> to <xref:System.ServiceModel.TcpClientCredentialType.Windows>.</span></span> <span data-ttu-id="e9ce0-138">Remarque : il s'agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-138">(Note that this is the default.)</span></span>  
  
3. <span data-ttu-id="e9ce0-139">Affectez à la propriété <xref:System.ServiceModel.MessageSecurityOverTcp.ClientCredentialType%2A> une valeur appropriée.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-139">Set the <xref:System.ServiceModel.MessageSecurityOverTcp.ClientCredentialType%2A> to an appropriate value.</span></span> <span data-ttu-id="e9ce0-140">Dans l'exemple de code suivant, la valeur <xref:System.ServiceModel.MessageCredentialType.Certificate> est utilisée.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-140">The following code uses the <xref:System.ServiceModel.MessageCredentialType.Certificate> value.</span></span>  
  
4. <span data-ttu-id="e9ce0-141">Créez une instance de la classe <xref:System.Uri> en utilisant une adresse de base appropriée.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-141">Create an instance of the <xref:System.Uri> class with an appropriate base address.</span></span> <span data-ttu-id="e9ce0-142">Remarque : cette adresse doit utiliser le schéma « net.tcp ».</span><span class="sxs-lookup"><span data-stu-id="e9ce0-142">Note that the address must use the "net.tcp" scheme.</span></span> <span data-ttu-id="e9ce0-143">Vous pouvez également définir l'adresse de base dans la configuration.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-143">(Alternatively, you can set the base address in configuration.)</span></span>  
  
5. <span data-ttu-id="e9ce0-144">Créez une instance de la classe <xref:System.ServiceModel.ServiceHost>.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-144">Create the instance of the <xref:System.ServiceModel.ServiceHost> class.</span></span>  
  
6. <span data-ttu-id="e9ce0-145">Utilisez la méthode <xref:System.ServiceModel.Security.X509CertificateRecipientServiceCredential.SetCertificate%2A> de la classe <xref:System.ServiceModel.Security.X509CertificateRecipientServiceCredential> pour définir de manière explicite le certificat X.509 de ce service.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-145">Use the <xref:System.ServiceModel.Security.X509CertificateRecipientServiceCredential.SetCertificate%2A> method of the <xref:System.ServiceModel.Security.X509CertificateRecipientServiceCredential> class to explicitly set the X.509 certificate for the service.</span></span>  
  
7. <span data-ttu-id="e9ce0-146">Ajoutez un point de terminaison de service à l'aide de la méthode <xref:System.ServiceModel.ServiceHost.AddServiceEndpoint%2A>.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-146">Add a service endpoint using the <xref:System.ServiceModel.ServiceHost.AddServiceEndpoint%2A> method.</span></span>  
  
8. <span data-ttu-id="e9ce0-147">Appelez la méthode <xref:System.ServiceModel.ICommunicationObject.Open%2A>, comme illustré dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="e9ce0-147">Call the <xref:System.ServiceModel.ICommunicationObject.Open%2A> method, as shown in the following code.</span></span>  
  
     [!code-csharp[c_SettingSecurityMode#9](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_settingsecuritymode/cs/source.cs#9)]
     [!code-vb[c_SettingSecurityMode#9](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_settingsecuritymode/vb/source.vb#9)]  
  
## <a name="using-configuration"></a><span data-ttu-id="e9ce0-148">Utilisation de la configuration</span><span class="sxs-lookup"><span data-stu-id="e9ce0-148">Using Configuration</span></span>  
  
#### <a name="to-use-the-wshttpbinding"></a><span data-ttu-id="e9ce0-149">Pour utiliser la liaison WSHttpBinding</span><span class="sxs-lookup"><span data-stu-id="e9ce0-149">To use the WSHttpBinding</span></span>  
  
1. <span data-ttu-id="e9ce0-150">Configurez l’ordinateur en attribuant un certificat SSL à l’un de ses ports.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-150">Configure the computer with an SSL certificate bound to a port.</span></span> <span data-ttu-id="e9ce0-151">(Pour plus d’informations, consultez [Comment : Configurer un Port avec un certificat SSL](../../../../docs/framework/wcf/feature-details/how-to-configure-a-port-with-an-ssl-certificate.md)).</span><span class="sxs-lookup"><span data-stu-id="e9ce0-151">(For more information, see [How to: Configure a Port with an SSL Certificate](../../../../docs/framework/wcf/feature-details/how-to-configure-a-port-with-an-ssl-certificate.md)).</span></span> <span data-ttu-id="e9ce0-152">Vous n’avez pas besoin de définir un <`transport`> valeur de l’élément avec cette configuration.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-152">You do not need to set a <`transport`> element value with this configuration.</span></span>  
  
2. <span data-ttu-id="e9ce0-153">Spécifiez le type d'informations d'identification pour la sécurité de niveau message.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-153">Specify the client credential type for the message-level security.</span></span> <span data-ttu-id="e9ce0-154">L’exemple suivant définit la `clientCredentialType` attribut de la <`message`> élément à `UserName`.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-154">The following example sets the `clientCredentialType` attribute of the <`message`> element to `UserName`.</span></span>  
  
    ```xml  
    <wsHttpBinding>  
    <binding name="WsHttpBinding_ICalculator">  
            <security mode="TransportWithMessageCredential" >  
               <message clientCredentialType="UserName" />  
            </security>  
    </binding>  
    </wsHttpBinding>  
    ```  
  
#### <a name="to-use-the-nettcpbinding-with-a-certificate-for-transport-security"></a><span data-ttu-id="e9ce0-155">Pour utiliser la liaison NetTcpBinding avec un certificat pour la sécurité de transport</span><span class="sxs-lookup"><span data-stu-id="e9ce0-155">To use the NetTcpBinding with a certificate for transport security</span></span>  
  
1. <span data-ttu-id="e9ce0-156">Pour la sécurité SSL sur TCP, vous devez spécifier de manière explicite le certificat dans l'élément `<behaviors>`.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-156">For SSL over TCP, you must explicitly specify the certificate in the `<behaviors>` element.</span></span> <span data-ttu-id="e9ce0-157">Dans l'exemple suivant, le certificat spécifié est publié par un émetteur figurant dans l'emplacement de magasin par défaut (ordinateur local et magasins personnels).</span><span class="sxs-lookup"><span data-stu-id="e9ce0-157">The following example specifies a certificate by its issuer in the default store location (local machine and personal stores).</span></span>  
  
    ```xml  
    <behaviors>  
     <serviceBehaviors>  
       <behavior name="mySvcBehavior">  
           <serviceCredentials>  
             <serviceCertificate findValue="contoso.com"  
                                 x509FindType="FindByIssuerName" />  
           </serviceCredentials>  
       </behavior>  
     </serviceBehaviors>  
    </behaviors>  
    ```  
  
2. <span data-ttu-id="e9ce0-158">Ajouter un [ \<netTcpBinding >](../../../../docs/framework/configure-apps/file-schema/wcf/nettcpbinding.md) à la section des liaisons</span><span class="sxs-lookup"><span data-stu-id="e9ce0-158">Add a [\<netTcpBinding>](../../../../docs/framework/configure-apps/file-schema/wcf/nettcpbinding.md) to the bindings section</span></span>  
  
3. <span data-ttu-id="e9ce0-159">Ajoutez un élément de liaison, puis affectez à l’attribut `name` une valeur adéquate.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-159">Add a binding element, and set the `name` attribute to an appropriate value.</span></span>  
  
4. <span data-ttu-id="e9ce0-160">Ajouter un <`security`> élément et définissez la `mode` attribut `TransportWithMessageCredential`.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-160">Add a <`security`> element, and set the `mode` attribute to `TransportWithMessageCredential`.</span></span>  
  
5. <span data-ttu-id="e9ce0-161">Ajouter un <`message>` élément et définissez la `clientCredentialType` attribut une valeur appropriée.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-161">Add a <`message>` element, and set the `clientCredentialType` attribute to an appropriate value.</span></span>  
  
    ```xml  
    <bindings>  
    <netTcpBinding>  
      <binding name="myTcpBinding">  
        <security mode="TransportWithMessageCredential" >  
           <message clientCredentialType="Windows" />  
        </security>  
      </binding>  
    </netTcpBinding>  
    </bindings>  
    ```  
  
#### <a name="to-use-the-nettcpbinding-with-windows-for-transport-security"></a><span data-ttu-id="e9ce0-162">Pour utiliser la liaison NetTcpBinding avec Windows comme sécurité de transport</span><span class="sxs-lookup"><span data-stu-id="e9ce0-162">To use the NetTcpBinding with Windows for transport security</span></span>  
  
1. <span data-ttu-id="e9ce0-163">Ajouter un [ \<netTcpBinding >](../../../../docs/framework/configure-apps/file-schema/wcf/nettcpbinding.md) à la section des liaisons</span><span class="sxs-lookup"><span data-stu-id="e9ce0-163">Add a [\<netTcpBinding>](../../../../docs/framework/configure-apps/file-schema/wcf/nettcpbinding.md) to the bindings section,</span></span>  
  
2. <span data-ttu-id="e9ce0-164">Ajouter un <`binding`> et affectez le `name` attribut une valeur appropriée.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-164">Add a <`binding`> element and set the `name` attribute to an appropriate value.</span></span>  
  
3. <span data-ttu-id="e9ce0-165">Ajouter un <`security`> élément et définissez la `mode` attribut `TransportWithMessageCredential`.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-165">Add a <`security`> element, and set the `mode` attribute to `TransportWithMessageCredential`.</span></span>  
  
4. <span data-ttu-id="e9ce0-166">Ajouter un <`transport`> et affectez le `clientCredentialType` attribut `Windows`.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-166">Add a <`transport`> element and set the `clientCredentialType` attribute to `Windows`.</span></span>  
  
5. <span data-ttu-id="e9ce0-167">Ajouter un <`message`> et affectez le `clientCredentialType` attribut une valeur appropriée.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-167">Add a <`message`> element and set the `clientCredentialType` attribute to an appropriate value.</span></span> <span data-ttu-id="e9ce0-168">Dans l'exemple de code suivant, un certificat est affecté à la valeur.</span><span class="sxs-lookup"><span data-stu-id="e9ce0-168">The following code sets the value to a certificate.</span></span>  
  
    ```xml  
    <bindings>  
    <netTcpBinding>  
      <binding name="myTcpBinding">  
        <security mode="TransportWithMessageCredential" >  
           <transport clientCredentialType="Windows" />  
           <message clientCredentialType="Certificate" />  
        </security>  
      </binding>  
    </netTcpBinding>  
    </bindings>  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="e9ce0-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9ce0-169">See also</span></span>

- [<span data-ttu-id="e9ce0-170">Guide pratique pour Définir le Mode de sécurité</span><span class="sxs-lookup"><span data-stu-id="e9ce0-170">How to: Set the Security Mode</span></span>](../../../../docs/framework/wcf/how-to-set-the-security-mode.md)
- [<span data-ttu-id="e9ce0-171">Sécurisation de services</span><span class="sxs-lookup"><span data-stu-id="e9ce0-171">Securing Services</span></span>](../../../../docs/framework/wcf/securing-services.md)
- [<span data-ttu-id="e9ce0-172">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="e9ce0-172">Securing Services and Clients</span></span>](../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
