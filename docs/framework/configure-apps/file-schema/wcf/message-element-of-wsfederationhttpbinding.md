---
title: <message> élément de <wsFederationHttpBinding>
ms.date: 03/30/2017
ms.assetid: 9d710389-d9d8-4454-9bf2-da4ccda31cec
ms.openlocfilehash: 79739dd715d7982555e5577c921cb65156af5923
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59223812"
---
# <a name="message-element-of-wsfederationhttpbinding"></a><span data-ttu-id="65380-102">\<message > élément de \<wsFederationHttpBinding ></span><span class="sxs-lookup"><span data-stu-id="65380-102">\<message> element of \<wsFederationHttpBinding></span></span>
<span data-ttu-id="65380-103">Définit les paramètres de la sécurité au niveau du message pour le [ \<wsFederationHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="65380-103">Defines the settings for the message-level security for the [\<wsFederationHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md).</span></span>  
  
 <span data-ttu-id="65380-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="65380-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="65380-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="65380-105">\<bindings></span></span>  
<span data-ttu-id="65380-106">\<wsFederatedBinding></span><span class="sxs-lookup"><span data-stu-id="65380-106">\<wsFederatedBinding></span></span>  
<span data-ttu-id="65380-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="65380-107">\<binding></span></span>  
<span data-ttu-id="65380-108">\<security></span><span class="sxs-lookup"><span data-stu-id="65380-108">\<security></span></span>  
<span data-ttu-id="65380-109">\<message></span><span class="sxs-lookup"><span data-stu-id="65380-109">\<message></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="65380-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65380-110">Syntax</span></span>  
  
```xml  
<wsFederationBinding>
  <binding>
    <security>
      <message algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
               issuedTokenType="string"
               issuedKeyType="SymmetricKey/PublicKey"
               negotiateServiceCredential="Boolean">
        <claimTypeRequirements>
          <add claimType="URI"
               isOptional="Boolean" />
        </claimTypeRequirements>
        <issuer address="Uri">
          <headers>
            <add name="String"
                 namespace="String" />
          </headers>
          <identity>
            <certificate encodedValue="String" />
            <certificateReference findValue="String"
                                  isChainIncluded="Boolean"
                                  storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"
                                  storeLocation="LocalMachine/CurrentUser"
                                  x509FindType="System.Security.Cryptography.X509certificates.X509findtype" />
            <dns value="String" />
            <rsa value="String" />
            <servicePrincipalName value="String" />
            <usePrincipalName value="String" />
          </identity>
        </issuer>
        <issuerMetadata address="String">
          <headers>
            <add name="String"
                 namespace="String" />
          </headers>
          <identity>
            <certificate encodedValue="String" />
            <certificateReference findValue="String"
                                  isChainIncluded="Boolean"
                                  storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"
                                  storeLocation="LocalMachine/CurrentUser"
                                  X509FindType="System.Security.Cryptography.X509certificates.X509findtype" />
            <dns value="String" />
            <rsa value="String" />
            <servicePrincipalName value="String" />
            <usePrincipalName value="String" />
          </identity>
        </issuerMetadata>
        <tokenRequestParameters>
          <xmlElement>
          </xmlElement>
        </tokenRequestParameters>
      </message>
    </security>
  </binding>
</wsFederationBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="65380-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="65380-111">Attributes and Elements</span></span>  
 <span data-ttu-id="65380-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="65380-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="65380-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="65380-113">Attributes</span></span>  
  
|<span data-ttu-id="65380-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="65380-114">Attribute</span></span>|<span data-ttu-id="65380-115">Description</span><span class="sxs-lookup"><span data-stu-id="65380-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="65380-116">algorithmSuite</span><span class="sxs-lookup"><span data-stu-id="65380-116">algorithmSuite</span></span>|<span data-ttu-id="65380-117">Définit les algorithmes de chiffrement de message et de clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="65380-117">Sets the message encryption and key-wrap algorithms.</span></span> <span data-ttu-id="65380-118">Consultez le tableau « attribut algorithmSuite » pour des valeurs valides de cet attribut.</span><span class="sxs-lookup"><span data-stu-id="65380-118">See the "algorithmSuite attribute" table for valid values of this attribute.</span></span> <span data-ttu-id="65380-119">La valeur par défaut est `Basic256`.</span><span class="sxs-lookup"><span data-stu-id="65380-119">The default value is `Basic256`.</span></span><br /><br /> <span data-ttu-id="65380-120">Cet attribut est de type <xref:System.ServiceModel.Security.SecurityAlgorithmSuite>.</span><span class="sxs-lookup"><span data-stu-id="65380-120">This attribute is of type <xref:System.ServiceModel.Security.SecurityAlgorithmSuite>.</span></span> <span data-ttu-id="65380-121">Ces algorithmes se mappent à ceux définis dans la spécification Security Policy Language (WS-SecurityPolicy).</span><span class="sxs-lookup"><span data-stu-id="65380-121">These algorithms map to those specified in the Security Policy Language (WS-SecurityPolicy) specification.</span></span>|  
|<span data-ttu-id="65380-122">issuedKeyType</span><span class="sxs-lookup"><span data-stu-id="65380-122">issuedKeyType</span></span>|<span data-ttu-id="65380-123">Spécifie le type de clé à émettre.</span><span class="sxs-lookup"><span data-stu-id="65380-123">Specifies the type of key to be issued.</span></span> <span data-ttu-id="65380-124">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="65380-124">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="65380-125">-   SymmetricKey</span><span class="sxs-lookup"><span data-stu-id="65380-125">-   SymmetricKey</span></span><br /><span data-ttu-id="65380-126">-   PublicKey</span><span class="sxs-lookup"><span data-stu-id="65380-126">-   PublicKey</span></span><br /><br /> <span data-ttu-id="65380-127">La valeur par défaut est `SymmetricKey`.</span><span class="sxs-lookup"><span data-stu-id="65380-127">The default is `SymmetricKey`.</span></span> <span data-ttu-id="65380-128">Cet attribut est de type <xref:System.IdentityModel.Tokens.SecurityKeyType>.</span><span class="sxs-lookup"><span data-stu-id="65380-128">This attribute is of type <xref:System.IdentityModel.Tokens.SecurityKeyType>.</span></span>|  
|<span data-ttu-id="65380-129">issuedTokenType</span><span class="sxs-lookup"><span data-stu-id="65380-129">issuedTokenType</span></span>|<span data-ttu-id="65380-130">Chaîne qui contient un URI qui spécifie le type de jeton à publier.</span><span class="sxs-lookup"><span data-stu-id="65380-130">A string that contains a URI that specifies the type of token to be issued.</span></span> <span data-ttu-id="65380-131">La valeur par défaut est `null`.</span><span class="sxs-lookup"><span data-stu-id="65380-131">The default is `null`.</span></span>|  
|<span data-ttu-id="65380-132">negotiateServiceCredential</span><span class="sxs-lookup"><span data-stu-id="65380-132">negotiateServiceCredential</span></span>|<span data-ttu-id="65380-133">Valeur booléenne qui spécifie si les informations d'identification du service doivent être échangées dans le cadre de la négociation ou si elles sont disponibles hors bande.</span><span class="sxs-lookup"><span data-stu-id="65380-133">A Boolean value that specifies whether the service credential should be exchanged as part of negotiation or is available out of band.</span></span> <span data-ttu-id="65380-134">La valeur par défaut est `true`, ce qui signifie que les informations d'identification du service sont négociées.</span><span class="sxs-lookup"><span data-stu-id="65380-134">The default is `true`, which means that the service credential is negotiated.</span></span>|  
  
## <a name="algorithmsuite-attribute"></a><span data-ttu-id="65380-135">Attribut algorithmSuite</span><span class="sxs-lookup"><span data-stu-id="65380-135">algorithmSuite Attribute</span></span>  
  
|<span data-ttu-id="65380-136">Value</span><span class="sxs-lookup"><span data-stu-id="65380-136">Value</span></span>|<span data-ttu-id="65380-137">Description</span><span class="sxs-lookup"><span data-stu-id="65380-137">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="65380-138">Basic128</span><span class="sxs-lookup"><span data-stu-id="65380-138">Basic128</span></span>|<span data-ttu-id="65380-139">Utilisez le chiffrement Basic128, Sha1 pour le condensat du message et Rsa-oaep-mgf1p pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="65380-139">Use Basic128 encryption, Sha1 for message digest, and Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="65380-140">Basic192</span><span class="sxs-lookup"><span data-stu-id="65380-140">Basic192</span></span>|<span data-ttu-id="65380-141">Utilisez le chiffrement Basic192, Sha1 pour le condensat du message et Rsa-oaep-mgf1p pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="65380-141">Use Basic192 encryption, Sha1 for message digest, Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="65380-142">Basic256</span><span class="sxs-lookup"><span data-stu-id="65380-142">Basic256</span></span>|<span data-ttu-id="65380-143">Utilisez le chiffrement Basic256, Sha1 pour le condensat du message et Rsa-oaep-mgf1p pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="65380-143">Use Basic256 encryption, Sha1 for message digest, Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="65380-144">Basic256Rsa15</span><span class="sxs-lookup"><span data-stu-id="65380-144">Basic256Rsa15</span></span>|<span data-ttu-id="65380-145">Utilisez Basic256 pour le chiffrement du message, Sha1 pour le condensat du message et Rsa15 pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="65380-145">Use Basic256 for message encryption, Sha1 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="65380-146">Basic192Rsa15</span><span class="sxs-lookup"><span data-stu-id="65380-146">Basic192Rsa15</span></span>|<span data-ttu-id="65380-147">Utilisez Basic192 pour le chiffrement du message, Sha1 pour le condensat du message et Rsa15 pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="65380-147">Use Basic192 for message encryption, Sha1 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="65380-148">TripleDes</span><span class="sxs-lookup"><span data-stu-id="65380-148">TripleDes</span></span>|<span data-ttu-id="65380-149">Utilisez le chiffrement TripleDes, Sha1 pour le condensat du message et Rsa-oaep-mgf1p pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="65380-149">Use TripleDes encryption, Sha1 for message digest, Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="65380-150">Basic128Rsa15</span><span class="sxs-lookup"><span data-stu-id="65380-150">Basic128Rsa15</span></span>|<span data-ttu-id="65380-151">Utilisez Basic128 pour le chiffrement du message, Sha1 pour le résumé du message et Rsa15 pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="65380-151">Use Basic128 for message encryption, Sha1 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="65380-152">TripleDesRsa15</span><span class="sxs-lookup"><span data-stu-id="65380-152">TripleDesRsa15</span></span>|<span data-ttu-id="65380-153">Utilisez le chiffrement TripleDes, Sha1 pour le condensat du message et Rsa15 pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="65380-153">Use TripleDes encryption, Sha1 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="65380-154">Basic128Sha256</span><span class="sxs-lookup"><span data-stu-id="65380-154">Basic128Sha256</span></span>|<span data-ttu-id="65380-155">Utilisez Basic128 pour le chiffrement du message, Sha256 pour le résumé du message et Rsa-oaep-mgf1p pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="65380-155">Use Basic128 for message encryption, Sha256 for message digest and Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="65380-156">Basic192Sha256</span><span class="sxs-lookup"><span data-stu-id="65380-156">Basic192Sha256</span></span>|<span data-ttu-id="65380-157">Utilisez Basic192 pour le chiffrement du message, Sha256 pour le résumé du message et Rsa-oaep-mgf1p pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="65380-157">Use Basic192 for message encryption, Sha256 for message digest and Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="65380-158">Basic256Sha256</span><span class="sxs-lookup"><span data-stu-id="65380-158">Basic256Sha256</span></span>|<span data-ttu-id="65380-159">Utilisez Basic256 pour le chiffrement du message, Sha256 pour le condensat du message et Rsa-oaep-mgf1p pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="65380-159">Use Basic256 for message encryption, Sha256 for message digest and Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="65380-160">TripleDesSha256</span><span class="sxs-lookup"><span data-stu-id="65380-160">TripleDesSha256</span></span>|<span data-ttu-id="65380-161">Utilisez TripleDes pour le chiffrement du message, Sha256 pour le résumé du message et Rsa-oaep-mgf1p pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="65380-161">Use TripleDes for message encryption, Sha256 for message digest and Rsa-oaep-mgf1p for key wrap.</span></span>|  
|<span data-ttu-id="65380-162">Basic128Sha256Rsa15</span><span class="sxs-lookup"><span data-stu-id="65380-162">Basic128Sha256Rsa15</span></span>|<span data-ttu-id="65380-163">Utilisez Basic128 pour le chiffrement du message, Sha256 pour le condensat du message et Rsa15 pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="65380-163">Use Basic128 for message encryption, Sha256 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="65380-164">Basic192Sha256Rsa15</span><span class="sxs-lookup"><span data-stu-id="65380-164">Basic192Sha256Rsa15</span></span>|<span data-ttu-id="65380-165">Utilisez Aes192 pour le chiffrement du message, Sha256 pour le condensat du message et Rsa15 pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="65380-165">Use Aes192 for message encryption, Sha256 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="65380-166">Basic256Sha256Rsa15</span><span class="sxs-lookup"><span data-stu-id="65380-166">Basic256Sha256Rsa15</span></span>|<span data-ttu-id="65380-167">Utilisez Basic256 pour le chiffrement du message, Sha256 pour le condensat du message et Rsa15 pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="65380-167">Use Basic256 for message encryption, Sha256 for message digest and Rsa15 for key wrap.</span></span>|  
|<span data-ttu-id="65380-168">TripleDesSha256Rsa15</span><span class="sxs-lookup"><span data-stu-id="65380-168">TripleDesSha256Rsa15</span></span>|<span data-ttu-id="65380-169">Utilisez TripleDes pour le chiffrement du message, Sha256 pour le condensat du message et Rsa15 pour la clé de type WRAP.</span><span class="sxs-lookup"><span data-stu-id="65380-169">Use TripleDes for message encryption, Sha256 for message digest and Rsa15 for key wrap.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="65380-170">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="65380-170">Child Elements</span></span>  
  
|<span data-ttu-id="65380-171">Élément</span><span class="sxs-lookup"><span data-stu-id="65380-171">Element</span></span>|<span data-ttu-id="65380-172">Description</span><span class="sxs-lookup"><span data-stu-id="65380-172">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="65380-173">\<claimTypeRequirements></span><span class="sxs-lookup"><span data-stu-id="65380-173">\<claimTypeRequirements></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/claimtyperequirements-element.md)|<span data-ttu-id="65380-174">Spécifie une collection de types de revendication pour cette liaison.</span><span class="sxs-lookup"><span data-stu-id="65380-174">Specifies a collection of claim types for this binding.</span></span> <span data-ttu-id="65380-175">Chaque élément est de type <xref:System.ServiceModel.Configuration.ClaimTypeElement>.</span><span class="sxs-lookup"><span data-stu-id="65380-175">Each element is of type <xref:System.ServiceModel.Configuration.ClaimTypeElement>.</span></span>|  
|<span data-ttu-id="65380-176">issuer</span><span class="sxs-lookup"><span data-stu-id="65380-176">issuer</span></span>|<span data-ttu-id="65380-177">Spécifie un point de terminaison qui publie un jeton de sécurité.</span><span class="sxs-lookup"><span data-stu-id="65380-177">Specifies an endpoint that issues a security token.</span></span> <span data-ttu-id="65380-178">Cet élément est de type <xref:System.ServiceModel.Configuration.IssuedTokenParametersEndpointAddressElement>.</span><span class="sxs-lookup"><span data-stu-id="65380-178">This element is of type <xref:System.ServiceModel.Configuration.IssuedTokenParametersEndpointAddressElement>.</span></span>|  
|<span data-ttu-id="65380-179">issuerMetadata</span><span class="sxs-lookup"><span data-stu-id="65380-179">issuerMetadata</span></span>|<span data-ttu-id="65380-180">Spécifie l'adresse de point de terminaison de l'émetteur.</span><span class="sxs-lookup"><span data-stu-id="65380-180">Specifies the endpoint address of the issuer.</span></span>|  
|[<span data-ttu-id="65380-181">\<tokenRequestParameters></span><span class="sxs-lookup"><span data-stu-id="65380-181">\<tokenRequestParameters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/tokenrequestparameters.md)|<span data-ttu-id="65380-182">Collection de paramètres de demande de jeton.</span><span class="sxs-lookup"><span data-stu-id="65380-182">A collection of token request parameters.</span></span> <span data-ttu-id="65380-183">Chaque paramètre est un élément XML.</span><span class="sxs-lookup"><span data-stu-id="65380-183">Each parameter is an XML element.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="65380-184">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="65380-184">Parent Elements</span></span>  
  
|<span data-ttu-id="65380-185">Élément</span><span class="sxs-lookup"><span data-stu-id="65380-185">Element</span></span>|<span data-ttu-id="65380-186">Description</span><span class="sxs-lookup"><span data-stu-id="65380-186">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="65380-187">\<security></span><span class="sxs-lookup"><span data-stu-id="65380-187">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-wsfederationhttpbinding.md)|<span data-ttu-id="65380-188">Définit les paramètres de sécurité d’une liaison.</span><span class="sxs-lookup"><span data-stu-id="65380-188">Defines the security settings for a binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="65380-189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65380-189">See also</span></span>

- <xref:System.ServiceModel.FederatedMessageSecurityOverHttp>
- <xref:System.ServiceModel.Configuration.WSFederationHttpSecurityElement.Message%2A>
- <xref:System.ServiceModel.WSFederationHttpSecurity.Message%2A>
- <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement>
- [<span data-ttu-id="65380-190">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="65380-190">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="65380-191">Liaisons</span><span class="sxs-lookup"><span data-stu-id="65380-191">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="65380-192">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="65380-192">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="65380-193">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="65380-193">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="65380-194">\<binding></span><span class="sxs-lookup"><span data-stu-id="65380-194">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
