---
title: <security> de <wsDualHttpBinding>
ms.date: 03/30/2017
ms.assetid: 869c05e7-4ebe-467d-95ab-c8f8de4e6b9e
ms.openlocfilehash: c6f9e34724ccc3a0d05da3e1886b4f0bcbaae064
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59171507"
---
# <a name="security-of-wsdualhttpbinding"></a><span data-ttu-id="f3520-102">\<sécurité > de \<wsDualHttpBinding ></span><span class="sxs-lookup"><span data-stu-id="f3520-102">\<security> of \<wsDualHttpBinding></span></span>
<span data-ttu-id="f3520-103">Définit les fonctionnalités de sécurité de la [ \<wsDualHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wsdualhttpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="f3520-103">Defines the security capabilities of the [\<wsDualHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsdualhttpbinding.md).</span></span>  
  
 <span data-ttu-id="f3520-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="f3520-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="f3520-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="f3520-105">\<bindings></span></span>  
<span data-ttu-id="f3520-106">\<wsDualHttpBinding></span><span class="sxs-lookup"><span data-stu-id="f3520-106">\<wsDualHttpBinding></span></span>  
<span data-ttu-id="f3520-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="f3520-107">\<binding></span></span>  
<span data-ttu-id="f3520-108">\<security></span><span class="sxs-lookup"><span data-stu-id="f3520-108">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f3520-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3520-109">Syntax</span></span>  
  
```xml  
<security mode="Message/None">
  <message algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
           clientCredentialType="Certificate/IssuedToken/None/UserName/Windows"
           negotiateServiceCredential="Boolean"/>
</security>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f3520-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="f3520-110">Attributes and Elements</span></span>  
 <span data-ttu-id="f3520-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="f3520-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f3520-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="f3520-112">Attributes</span></span>  
  
|<span data-ttu-id="f3520-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="f3520-113">Attribute</span></span>|<span data-ttu-id="f3520-114">Description</span><span class="sxs-lookup"><span data-stu-id="f3520-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f3520-115">mode</span><span class="sxs-lookup"><span data-stu-id="f3520-115">mode</span></span>|<span data-ttu-id="f3520-116">-Facultatif.</span><span class="sxs-lookup"><span data-stu-id="f3520-116">-   Optional.</span></span> <span data-ttu-id="f3520-117">Spécifie le type de sécurité appliqué.</span><span class="sxs-lookup"><span data-stu-id="f3520-117">Specifies the type of security that is applied.</span></span> <span data-ttu-id="f3520-118">La valeur par défaut est `Message`.</span><span class="sxs-lookup"><span data-stu-id="f3520-118">The default value is `Message`.</span></span> <span data-ttu-id="f3520-119">Cet attribut est de type <xref:System.ServiceModel.WSDualHttpSecurityMode>.</span><span class="sxs-lookup"><span data-stu-id="f3520-119">This attribute is of type <xref:System.ServiceModel.WSDualHttpSecurityMode>.</span></span>|  
  
## <a name="mode-attribute"></a><span data-ttu-id="f3520-120">Mode, attribut</span><span class="sxs-lookup"><span data-stu-id="f3520-120">Mode Attribute</span></span>  
  
|<span data-ttu-id="f3520-121">Value</span><span class="sxs-lookup"><span data-stu-id="f3520-121">Value</span></span>|<span data-ttu-id="f3520-122">Description</span><span class="sxs-lookup"><span data-stu-id="f3520-122">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="f3520-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f3520-123">None</span></span>|<span data-ttu-id="f3520-124">La sécurité est désactivée.</span><span class="sxs-lookup"><span data-stu-id="f3520-124">Security is disabled.</span></span>|  
|<span data-ttu-id="f3520-125">Message</span><span class="sxs-lookup"><span data-stu-id="f3520-125">Message</span></span>|<span data-ttu-id="f3520-126">La sécurité est fournie à l'aide de la sécurité des messages SOAP.</span><span class="sxs-lookup"><span data-stu-id="f3520-126">Security is provided using SOAP message security.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f3520-127">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f3520-127">Child Elements</span></span>  
  
|<span data-ttu-id="f3520-128">Élément</span><span class="sxs-lookup"><span data-stu-id="f3520-128">Element</span></span>|<span data-ttu-id="f3520-129">Description</span><span class="sxs-lookup"><span data-stu-id="f3520-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f3520-130">\<message></span><span class="sxs-lookup"><span data-stu-id="f3520-130">\<message></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-of-wsdualhttpbinding.md)|<span data-ttu-id="f3520-131">Définit les paramètres de sécurité au niveau du message.</span><span class="sxs-lookup"><span data-stu-id="f3520-131">Defines the settings for the message-level security.</span></span> <span data-ttu-id="f3520-132">Cet élément est de type <xref:System.ServiceModel.MessageSecurityOverHttp>.</span><span class="sxs-lookup"><span data-stu-id="f3520-132">This element is of type <xref:System.ServiceModel.MessageSecurityOverHttp>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="f3520-133">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f3520-133">Parent Elements</span></span>  
  
|<span data-ttu-id="f3520-134">Élément</span><span class="sxs-lookup"><span data-stu-id="f3520-134">Element</span></span>|<span data-ttu-id="f3520-135">Description</span><span class="sxs-lookup"><span data-stu-id="f3520-135">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f3520-136">\<binding></span><span class="sxs-lookup"><span data-stu-id="f3520-136">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="f3520-137">Définit toutes les fonctions de liaison de la [ \<wsDualHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wsdualhttpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="f3520-137">Defines all binding capabilities of the [\<wsDualHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsdualhttpbinding.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f3520-138">Notes</span><span class="sxs-lookup"><span data-stu-id="f3520-138">Remarks</span></span>  
 <span data-ttu-id="f3520-139">Une liaison double expose l'adresse IP du client au service.</span><span class="sxs-lookup"><span data-stu-id="f3520-139">A dual binding exposes the IP address of the client to the service.</span></span> <span data-ttu-id="f3520-140">Ce client doit utiliser un mode de sécurité qui vérifiera qu'il se connecte uniquement à des services de confiance.</span><span class="sxs-lookup"><span data-stu-id="f3520-140">The client should use security to ensure that it only connects to services it trusts.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f3520-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3520-141">See also</span></span>

- <xref:System.ServiceModel.WSDualHttpSecurity>
- <xref:System.ServiceModel.BasicHttpSecurity>
- [<span data-ttu-id="f3520-142">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="f3520-142">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="f3520-143">Liaisons</span><span class="sxs-lookup"><span data-stu-id="f3520-143">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="f3520-144">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="f3520-144">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="f3520-145">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="f3520-145">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="f3520-146">\<binding></span><span class="sxs-lookup"><span data-stu-id="f3520-146">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
