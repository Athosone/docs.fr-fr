---
title: Élément <peerAuthentication>
ms.date: 03/30/2017
ms.assetid: 09a8a9ff-e395-42f6-8ceb-9d44bdc1cbe1
ms.openlocfilehash: 1e99f6d117604f9ba2672972a4b09e7fe9f96792
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59092966"
---
# <a name="peerauthentication-element"></a><span data-ttu-id="0ee15-102">\<peerAuthentication > élément</span><span class="sxs-lookup"><span data-stu-id="0ee15-102">\<peerAuthentication> Element</span></span>
<span data-ttu-id="0ee15-103">Spécifie les options d'authentification pour les clients du réseau pair à pair.</span><span class="sxs-lookup"><span data-stu-id="0ee15-103">Specifies authentication options for peer-to-peer clients.</span></span>  
  
 <span data-ttu-id="0ee15-104">Pour plus d’informations sur la programmation de peer-to-peer, consultez [mise en réseau Peer-to-Peer](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md).</span><span class="sxs-lookup"><span data-stu-id="0ee15-104">For more information about peer-to-peer programming, see [Peer-to-Peer Networking](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md).</span></span>  
  
 <span data-ttu-id="0ee15-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="0ee15-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="0ee15-106">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="0ee15-106">\<behaviors></span></span>  
<span data-ttu-id="0ee15-107">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="0ee15-107">\<endpointBehaviors></span></span>  
<span data-ttu-id="0ee15-108">\<behavior></span><span class="sxs-lookup"><span data-stu-id="0ee15-108">\<behavior></span></span>  
<span data-ttu-id="0ee15-109">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="0ee15-109">\<clientCredentials></span></span>  
<span data-ttu-id="0ee15-110">\<peer></span><span class="sxs-lookup"><span data-stu-id="0ee15-110">\<peer></span></span>  
<span data-ttu-id="0ee15-111">\<PeerAuthentication></span><span class="sxs-lookup"><span data-stu-id="0ee15-111">\<PeerAuthentication></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0ee15-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ee15-112">Syntax</span></span>  
  
```xml  
<peerAuthentication customCertificateValidatorType="namespace.typeName, [,AssemblyName] [,Version=version number] [,Culture=culture] [,PublicKeyToken=token]"
                    certificateValidationMode="ChainTrust/None/PeerTrust/PeerOrChainTrust/Custom"
                    revocationMode="NoCheck/Online/Offline"
                    trustedStoreLocation="CurrentUser/LocalMachine" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0ee15-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="0ee15-113">Attributes and Elements</span></span>  
 <span data-ttu-id="0ee15-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="0ee15-114">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0ee15-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="0ee15-115">Attributes</span></span>  
  
|<span data-ttu-id="0ee15-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="0ee15-116">Attribute</span></span>|<span data-ttu-id="0ee15-117">Description</span><span class="sxs-lookup"><span data-stu-id="0ee15-117">Description</span></span>|  
|---------------|-----------------|  
|`customCertificateValidatorType`|<span data-ttu-id="0ee15-118">Chaîne facultative.</span><span class="sxs-lookup"><span data-stu-id="0ee15-118">Optional string.</span></span> <span data-ttu-id="0ee15-119">Type et assembly utilisés pour valider un type personnalisé.</span><span class="sxs-lookup"><span data-stu-id="0ee15-119">A type and assembly used to validate a custom type.</span></span> <span data-ttu-id="0ee15-120">Cet attribut doit être défini lorsque `certificateValidationMode` a la valeur `Custom`.</span><span class="sxs-lookup"><span data-stu-id="0ee15-120">This attribute must be set when `certificateValidationMode` is set to `Custom`.</span></span>|  
|`certifcateValidationMode`|<span data-ttu-id="0ee15-121">Énumération facultative.</span><span class="sxs-lookup"><span data-stu-id="0ee15-121">Optional enumeration.</span></span> <span data-ttu-id="0ee15-122">Spécifie l'un de trois modes utilisés pour valider des informations d'identification.</span><span class="sxs-lookup"><span data-stu-id="0ee15-122">Specifies one of three modes used to validate credentials.</span></span> <span data-ttu-id="0ee15-123">S'il est défini à `Custom`, un `customCertificateValidator` doit également être fourni.</span><span class="sxs-lookup"><span data-stu-id="0ee15-123">If set to `Custom`, then a `customCertificateValidator` must also be supplied.</span></span> <span data-ttu-id="0ee15-124">La valeur par défaut est `ChainTrust`.</span><span class="sxs-lookup"><span data-stu-id="0ee15-124">The default is `ChainTrust`.</span></span>|  
|`revocationMode`|<span data-ttu-id="0ee15-125">Énumération facultative.</span><span class="sxs-lookup"><span data-stu-id="0ee15-125">Optional enumeration.</span></span> <span data-ttu-id="0ee15-126">Un des modes utilisés pour vérifier des listes de certificat révoqués (CRL).</span><span class="sxs-lookup"><span data-stu-id="0ee15-126">One of the modes used to check for a revoked certificate lists (CRL).</span></span> <span data-ttu-id="0ee15-127">La valeur par défaut est `Online`.</span><span class="sxs-lookup"><span data-stu-id="0ee15-127">The default is `Online`.</span></span>|  
|`trustedStoreLocation`|<span data-ttu-id="0ee15-128">Énumération facultative.</span><span class="sxs-lookup"><span data-stu-id="0ee15-128">Optional enumeration.</span></span> <span data-ttu-id="0ee15-129">L'un des deux emplacements du magasin du système : `LocalMachine` ou `CurrentUser`.</span><span class="sxs-lookup"><span data-stu-id="0ee15-129">One of the two system store locations: `LocalMachine` or `CurrentUser`.</span></span> <span data-ttu-id="0ee15-130">Cette valeur est utilisée lorsqu'un certificat de service est négocié au client.</span><span class="sxs-lookup"><span data-stu-id="0ee15-130">This value is used when a service certificate is negotiated to the client.</span></span> <span data-ttu-id="0ee15-131">La validation est effectuée sur le **personnes** stocker dans l’emplacement de magasin spécifié.</span><span class="sxs-lookup"><span data-stu-id="0ee15-131">Validation is performed against the **Trusted People** store in the specified store location.</span></span> <span data-ttu-id="0ee15-132">La valeur par défaut est `CurrentUser`.</span><span class="sxs-lookup"><span data-stu-id="0ee15-132">The default is `CurrentUser`.</span></span>|  
  
## <a name="customcertificatevalidatortype-attribute"></a><span data-ttu-id="0ee15-133">customCertificateValidatorType, attribut</span><span class="sxs-lookup"><span data-stu-id="0ee15-133">customCertificateValidatorType Attribute</span></span>  
  
|<span data-ttu-id="0ee15-134">Value</span><span class="sxs-lookup"><span data-stu-id="0ee15-134">Value</span></span>|<span data-ttu-id="0ee15-135">Description</span><span class="sxs-lookup"><span data-stu-id="0ee15-135">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="0ee15-136">Chaîne</span><span class="sxs-lookup"><span data-stu-id="0ee15-136">String</span></span>|<span data-ttu-id="0ee15-137">Spécifie le nom de type, l'assembly et d'autres données utilisées pour rechercher le type.</span><span class="sxs-lookup"><span data-stu-id="0ee15-137">Specifies the type name and assembly and other data used to find the type.</span></span> <span data-ttu-id="0ee15-138">Au minimum, un espace de noms et un nom de type sont requis.</span><span class="sxs-lookup"><span data-stu-id="0ee15-138">At minimum, a namespace and type name are required.</span></span> <span data-ttu-id="0ee15-139">Les informations facultatives incluent : le nom de l'assembly, le numéro de version, la culture et le jeton de clé publique.</span><span class="sxs-lookup"><span data-stu-id="0ee15-139">Optional information includes: assembly name, version number, culture, and public key token.</span></span>|  
  
## <a name="certificatevalidationmode-attribute"></a><span data-ttu-id="0ee15-140">certificateValidationMode, attribut</span><span class="sxs-lookup"><span data-stu-id="0ee15-140">certificateValidationMode Attribute</span></span>  
  
|<span data-ttu-id="0ee15-141">Value</span><span class="sxs-lookup"><span data-stu-id="0ee15-141">Value</span></span>|<span data-ttu-id="0ee15-142">Description</span><span class="sxs-lookup"><span data-stu-id="0ee15-142">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="0ee15-143">Énumération</span><span class="sxs-lookup"><span data-stu-id="0ee15-143">Enumeration</span></span>|<span data-ttu-id="0ee15-144">Une des valeurs suivantes : `None`, `PeerTrust`, `ChainTrust`, `PeerOrChainTrust` et `Custom`.</span><span class="sxs-lookup"><span data-stu-id="0ee15-144">One of the following values: `None`, `PeerTrust`, `ChainTrust`, `PeerOrChainTrust`, `Custom`.</span></span> <span data-ttu-id="0ee15-145">La valeur par défaut est `ChainTrust`.</span><span class="sxs-lookup"><span data-stu-id="0ee15-145">The default is `ChainTrust`.</span></span><br /><br /> <span data-ttu-id="0ee15-146">Pour plus d’informations, consultez [utilisation des certificats](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md).</span><span class="sxs-lookup"><span data-stu-id="0ee15-146">For more information, see [Working with Certificates](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md).</span></span>|  
  
## <a name="revocationmode-attribute"></a><span data-ttu-id="0ee15-147">revocationMode, attribut</span><span class="sxs-lookup"><span data-stu-id="0ee15-147">revocationMode Attribute</span></span>  
  
|<span data-ttu-id="0ee15-148">Value</span><span class="sxs-lookup"><span data-stu-id="0ee15-148">Value</span></span>|<span data-ttu-id="0ee15-149">Description</span><span class="sxs-lookup"><span data-stu-id="0ee15-149">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="0ee15-150">Énumération</span><span class="sxs-lookup"><span data-stu-id="0ee15-150">Enumeration</span></span>|<span data-ttu-id="0ee15-151">Une des valeurs suivantes : `NoCheck`, `Online` et `Offline`.</span><span class="sxs-lookup"><span data-stu-id="0ee15-151">One of the following values: `NoCheck`, `Online`, `Offline`.</span></span> <span data-ttu-id="0ee15-152">La valeur par défaut est `Online`.</span><span class="sxs-lookup"><span data-stu-id="0ee15-152">The default is `Online`.</span></span><br /><br /> <span data-ttu-id="0ee15-153">Pour plus d’informations, consultez [utilisation des certificats](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md).</span><span class="sxs-lookup"><span data-stu-id="0ee15-153">For more information, see [Working with Certificates](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md).</span></span>|  
  
## <a name="trustedstorelocation-attribute"></a><span data-ttu-id="0ee15-154">trustedStoreLocation, attribut</span><span class="sxs-lookup"><span data-stu-id="0ee15-154">trustedStoreLocation Attribute</span></span>  
  
|<span data-ttu-id="0ee15-155">Value</span><span class="sxs-lookup"><span data-stu-id="0ee15-155">Value</span></span>|<span data-ttu-id="0ee15-156">Description</span><span class="sxs-lookup"><span data-stu-id="0ee15-156">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="0ee15-157">Énumération</span><span class="sxs-lookup"><span data-stu-id="0ee15-157">Enumeration</span></span>|<span data-ttu-id="0ee15-158">Une des valeurs suivantes : `LocalMachine` ou `CurrentUser`.</span><span class="sxs-lookup"><span data-stu-id="0ee15-158">One of the following values: `LocalMachine` or `CurrentUser`.</span></span> <span data-ttu-id="0ee15-159">La valeur par défaut est `CurrentUser`.</span><span class="sxs-lookup"><span data-stu-id="0ee15-159">The default is `CurrentUser`.</span></span> <span data-ttu-id="0ee15-160">Si l'application cliente s'exécute sous un compte système, le certificat se trouve généralement dans `LocalMachine`.</span><span class="sxs-lookup"><span data-stu-id="0ee15-160">If the client application is running under a system account then the certificate is typically under `LocalMachine`.</span></span> <span data-ttu-id="0ee15-161">Si l'application cliente s'exécute sous un compte d'utilisateur, le certificat se trouve généralement dans `CurrentUser`.</span><span class="sxs-lookup"><span data-stu-id="0ee15-161">If the client application is running under a user account then the certificate is typically in `CurrentUser`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0ee15-162">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0ee15-162">Child Elements</span></span>  
 <span data-ttu-id="0ee15-163">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0ee15-163">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="0ee15-164">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0ee15-164">Parent Elements</span></span>  
  
|<span data-ttu-id="0ee15-165">Élément</span><span class="sxs-lookup"><span data-stu-id="0ee15-165">Element</span></span>|<span data-ttu-id="0ee15-166">Description</span><span class="sxs-lookup"><span data-stu-id="0ee15-166">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0ee15-167">\<peer></span><span class="sxs-lookup"><span data-stu-id="0ee15-167">\<peer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/peer-of-clientcredentials-element.md)|<span data-ttu-id="0ee15-168">Spécifie une information d'identification utilisée pour authentifier le client auprès d'un service homologue.</span><span class="sxs-lookup"><span data-stu-id="0ee15-168">Specifies a credential used for authenticating the client to a peer service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0ee15-169">Notes</span><span class="sxs-lookup"><span data-stu-id="0ee15-169">Remarks</span></span>  
 <span data-ttu-id="0ee15-170">L'élément `<authentication>` correspond à la classe <xref:System.ServiceModel.Security.X509PeerCertificateAuthentication>.</span><span class="sxs-lookup"><span data-stu-id="0ee15-170">The `<authentication>` element corresponds to the <xref:System.ServiceModel.Security.X509PeerCertificateAuthentication> class.</span></span> <span data-ttu-id="0ee15-171">Cet élément spécifie un validateur, appelé pendant l'authentification de voisins dans la maille.</span><span class="sxs-lookup"><span data-stu-id="0ee15-171">This element specifies a validator, which is invoked during neighbor-to-neighbor authentication in the mesh.</span></span> <span data-ttu-id="0ee15-172">Lorsqu'un nouvel homologue essaie d'établir une connexion avec un voisin, il transmet ses propres informations d'identification à l'homologue répondant.</span><span class="sxs-lookup"><span data-stu-id="0ee15-172">When a new peer tries to establish a neighbor connection, it passes its own credential to the responding peer.</span></span> <span data-ttu-id="0ee15-173">Le validateur du répondeur est appelé pour vérifier les informations d'identification du tiers distant.</span><span class="sxs-lookup"><span data-stu-id="0ee15-173">The validator of the responder is invoked to verify the credential of the remote party.</span></span> <span data-ttu-id="0ee15-174">Chaque fois qu'une connexion est établie avec un homologue de la maille, les deux homologues sont authentifiés mutuellement, ce qui signifie que des validateurs sont appelés à chaque extrémité.</span><span class="sxs-lookup"><span data-stu-id="0ee15-174">Whenever a peer connection is established in the mesh, both peers are mutually authenticated, meaning validators on both ends are invoked.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0ee15-175">Exemple</span><span class="sxs-lookup"><span data-stu-id="0ee15-175">Example</span></span>  
 <span data-ttu-id="0ee15-176">Le code suivant affecte la valeur `PeerOrChainTrust` au mode de validation du certificat.</span><span class="sxs-lookup"><span data-stu-id="0ee15-176">The following code sets the certificate validation mode to `PeerOrChainTrust`.</span></span>  
  
```xml  
<behaviors>
  <endpointBehaviors>
    <behavior name="MyEndpointBehavior">
      <clientCredentials>
        <peer>
          <certificate findValue="www.contoso.com"
                       storeLocation="LocalMachine"
                       x509FindType="FindByIssuerName" />
          <peerAuthentication certificateValidationMode="PeerOrChainTrust" />
          <messageSenderAuthentication certificateValidationMode="None" />
        </peer>
      </clientCredentials>
    </behavior>
  </endpointBehaviors>
</behaviors>
```  
  
## <a name="see-also"></a><span data-ttu-id="0ee15-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ee15-177">See also</span></span>

- <xref:System.ServiceModel.Configuration.PeerCredentialElement>
- <xref:System.ServiceModel.Security.X509PeerCertificateAuthentication>
- <xref:System.ServiceModel.Security.PeerCredential.PeerAuthentication%2A>
- <xref:System.ServiceModel.Configuration.PeerCredentialElement.PeerAuthentication%2A>
- <xref:System.ServiceModel.Configuration.X509PeerCertificateAuthenticationElement>
- [<span data-ttu-id="0ee15-178">Utilisation des certificats</span><span class="sxs-lookup"><span data-stu-id="0ee15-178">Working with Certificates</span></span>](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)
- [<span data-ttu-id="0ee15-179">Réseaux homologues</span><span class="sxs-lookup"><span data-stu-id="0ee15-179">Peer-to-Peer Networking</span></span>](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md)
- <span data-ttu-id="0ee15-180">[Authentification de Message de canal homologue](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="0ee15-180">[Peer Channel Message Authentication](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/aa967730(v=vs.90))</span></span>
- <span data-ttu-id="0ee15-181">[Authentification personnalisée de canal homologue](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms751447(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="0ee15-181">[Peer Channel Custom Authentication](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms751447(v=vs.90))</span></span>
- [<span data-ttu-id="0ee15-182">Sécurisation des applications de canal homologue</span><span class="sxs-lookup"><span data-stu-id="0ee15-182">Securing Peer Channel Applications</span></span>](../../../../../docs/framework/wcf/feature-details/securing-peer-channel-applications.md)
