---
title: <security> élément de <ws2007FederationHttpBinding>
ms.date: 03/30/2017
ms.assetid: 826219b4-3a16-45fc-832d-0cd7cbbd3b84
ms.openlocfilehash: 15740144b0aad7eb2798db4712e4769d08d893a6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59186860"
---
# <a name="security-element-of-ws2007federationhttpbinding"></a><span data-ttu-id="37db4-102">\<sécurité > élément de \<ws2007FederationHttpBinding ></span><span class="sxs-lookup"><span data-stu-id="37db4-102">\<security> element of \<ws2007FederationHttpBinding></span></span>
<span data-ttu-id="37db4-103">Définit les paramètres de sécurité de la [ \<ws2007FederationHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/ws2007federationhttpbinding.md) élément.</span><span class="sxs-lookup"><span data-stu-id="37db4-103">Defines the security settings of the [\<ws2007FederationHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/ws2007federationhttpbinding.md) element.</span></span>  
  
 <span data-ttu-id="37db4-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="37db4-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="37db4-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="37db4-105">\<bindings></span></span>  
<span data-ttu-id="37db4-106">\<ws2007FederationHttpBinding></span><span class="sxs-lookup"><span data-stu-id="37db4-106">\<ws2007FederationHttpBinding></span></span>  
<span data-ttu-id="37db4-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="37db4-107">\<binding></span></span>  
<span data-ttu-id="37db4-108">\<security></span><span class="sxs-lookup"><span data-stu-id="37db4-108">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="37db4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37db4-109">Syntax</span></span>  
  
```xml  
<ws2007FederationBinding>
  <binding>
    <security mode="None/Message/TransportWithMessageCredential">
      <message negotiateServiceCredential="Boolean"
               algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/  Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
               defaultProtectionLevel="none/sign/EncryptAndSign"
               issuedTokenType="string"
               issuedKeyType="SymmetricKey/PublicKey">
      </message>
    </security>
  </binding>
</ws2007FederationBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="37db4-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="37db4-110">Attributes and Elements</span></span>  
 <span data-ttu-id="37db4-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="37db4-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="37db4-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="37db4-112">Attributes</span></span>  
  
|<span data-ttu-id="37db4-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="37db4-113">Attribute</span></span>|<span data-ttu-id="37db4-114">Description</span><span class="sxs-lookup"><span data-stu-id="37db4-114">Description</span></span>|  
|---------------|-----------------|  
|`mode`|<span data-ttu-id="37db4-115">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="37db4-115">Optional.</span></span> <span data-ttu-id="37db4-116">Spécifie le type de sécurité appliqué.</span><span class="sxs-lookup"><span data-stu-id="37db4-116">Specifies the type of security that is applied.</span></span> <span data-ttu-id="37db4-117">La valeur par défaut est `Message`.</span><span class="sxs-lookup"><span data-stu-id="37db4-117">The default value is `Message`.</span></span> <span data-ttu-id="37db4-118">Cet attribut est de type <xref:System.ServiceModel.WSFederationHttpSecurityMode>.</span><span class="sxs-lookup"><span data-stu-id="37db4-118">This attribute is of type <xref:System.ServiceModel.WSFederationHttpSecurityMode>.</span></span>|  
  
## <a name="mode-attribute"></a><span data-ttu-id="37db4-119">Attribut Mode</span><span class="sxs-lookup"><span data-stu-id="37db4-119">mode Attribute</span></span>  
  
|<span data-ttu-id="37db4-120">Value</span><span class="sxs-lookup"><span data-stu-id="37db4-120">Value</span></span>|<span data-ttu-id="37db4-121">Description</span><span class="sxs-lookup"><span data-stu-id="37db4-121">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="37db4-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="37db4-122">None</span></span>|<span data-ttu-id="37db4-123">Le message SOAP n'est pas sécurisé pendant le transfert.</span><span class="sxs-lookup"><span data-stu-id="37db4-123">The SOAP message is not secure during transfer.</span></span>|  
|<span data-ttu-id="37db4-124">Message</span><span class="sxs-lookup"><span data-stu-id="37db4-124">Message</span></span>|<span data-ttu-id="37db4-125">L'intégrité, la confidentialité, l'authentification du serveur et l'authentification du client sont fournies à l'aide de la sécurité des messages SOAP.</span><span class="sxs-lookup"><span data-stu-id="37db4-125">Integrity, confidentiality, server authentication and client authentication are provided using SOAP message security.</span></span> <span data-ttu-id="37db4-126">Par défaut, le corps est chiffré et signé.</span><span class="sxs-lookup"><span data-stu-id="37db4-126">By default, the body is encrypted and signed.</span></span> <span data-ttu-id="37db4-127">Le service doit être configuré à l'aide d'un certificat.</span><span class="sxs-lookup"><span data-stu-id="37db4-127">The service must be configured with a certificate.</span></span> <span data-ttu-id="37db4-128">L'authentification du client est basée sur le jeton émis au client par un service d'émission de jeton de sécurité.</span><span class="sxs-lookup"><span data-stu-id="37db4-128">Client authentication is based on the token issued to the client by a security token service.</span></span>|  
|<span data-ttu-id="37db4-129">TransportWithMessageCredential</span><span class="sxs-lookup"><span data-stu-id="37db4-129">TransportWithMessageCredential</span></span>|<span data-ttu-id="37db4-130">L'intégrité, la confidentialité et l'authentification du serveur sont fournies par HTTPS.</span><span class="sxs-lookup"><span data-stu-id="37db4-130">Integrity, confidentiality and server authentication are provided by HTTPS.</span></span> <span data-ttu-id="37db4-131">Le service doit être configuré à l'aide d'un certificat.</span><span class="sxs-lookup"><span data-stu-id="37db4-131">The service must be configured with a certificate.</span></span> <span data-ttu-id="37db4-132">L'authentification du client est fournie au moyen de la sécurité des messages SOAP et est basée sur le jeton émis au client par un service d'émission de jeton de sécurité.</span><span class="sxs-lookup"><span data-stu-id="37db4-132">Client authentication is provided by means of SOAP message security and is based on the token issued to the client by a security token service.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="37db4-133">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="37db4-133">Child Elements</span></span>  
  
|<span data-ttu-id="37db4-134">Élément</span><span class="sxs-lookup"><span data-stu-id="37db4-134">Element</span></span>|<span data-ttu-id="37db4-135">Description</span><span class="sxs-lookup"><span data-stu-id="37db4-135">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="37db4-136">\<message></span><span class="sxs-lookup"><span data-stu-id="37db4-136">\<message></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-of-ws2007httpbinding.md)|<span data-ttu-id="37db4-137">Définit les paramètres de sécurité au niveau du message.</span><span class="sxs-lookup"><span data-stu-id="37db4-137">Defines the settings for the message-level security.</span></span> <span data-ttu-id="37db4-138">Cet élément est de type <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement>.</span><span class="sxs-lookup"><span data-stu-id="37db4-138">This element is of type <xref:System.ServiceModel.Configuration.FederatedMessageSecurityOverHttpElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="37db4-139">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="37db4-139">Parent Elements</span></span>  
  
|<span data-ttu-id="37db4-140">Élément</span><span class="sxs-lookup"><span data-stu-id="37db4-140">Element</span></span>|<span data-ttu-id="37db4-141">Description</span><span class="sxs-lookup"><span data-stu-id="37db4-141">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="37db4-142">\<binding></span><span class="sxs-lookup"><span data-stu-id="37db4-142">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="37db4-143">Définit toutes les fonctions de liaison de la [ \<wsDualHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wsdualhttpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="37db4-143">Defines all binding capabilities of the [\<wsDualHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsdualhttpbinding.md).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="37db4-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37db4-144">See also</span></span>

- <xref:System.ServiceModel.WSFederationHttpSecurity>
- <xref:System.ServiceModel.WSFederationHttpBinding.Security%2A>
- <xref:System.ServiceModel.Configuration.WSFederationHttpBindingElement.Security%2A>
- <xref:System.ServiceModel.Configuration.WSFederationHttpSecurityElement>
- [<span data-ttu-id="37db4-145">Guide pratique pour Créer une liaison WSFederationHttpBinding</span><span class="sxs-lookup"><span data-stu-id="37db4-145">How to: Create a WSFederationHttpBinding</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-wsfederationhttpbinding.md)
- [<span data-ttu-id="37db4-146">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="37db4-146">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="37db4-147">Sélection d’un type d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="37db4-147">Selecting a Credential Type</span></span>](../../../../../docs/framework/wcf/feature-details/selecting-a-credential-type.md)
- [<span data-ttu-id="37db4-148">Liaisons</span><span class="sxs-lookup"><span data-stu-id="37db4-148">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="37db4-149">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="37db4-149">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="37db4-150">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="37db4-150">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="37db4-151">\<binding></span><span class="sxs-lookup"><span data-stu-id="37db4-151">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
