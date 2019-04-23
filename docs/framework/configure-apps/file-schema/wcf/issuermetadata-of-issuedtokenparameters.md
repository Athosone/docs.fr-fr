---
title: <issuerMetadata> de <issuedTokenParameters>
ms.date: 03/30/2017
ms.assetid: 1a85ca37-496d-4fa3-8d44-d6c9383d735c
ms.openlocfilehash: e46e56c6285af24941a550b2c4f7dec3b441db69
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59214804"
---
# <a name="issuermetadata-of-issuedtokenparameters"></a><span data-ttu-id="5e643-102">\<issuerMetadata> of \<issuedTokenParameters></span><span class="sxs-lookup"><span data-stu-id="5e643-102">\<issuerMetadata> of \<issuedTokenParameters></span></span>
<span data-ttu-id="5e643-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="5e643-103">\<system.serviceModel></span></span>  
<span data-ttu-id="5e643-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="5e643-104">\<bindings></span></span>  
<span data-ttu-id="5e643-105">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="5e643-105">\<customBinding></span></span>  
<span data-ttu-id="5e643-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="5e643-106">\<binding></span></span>  
<span data-ttu-id="5e643-107">\<security></span><span class="sxs-lookup"><span data-stu-id="5e643-107">\<security></span></span>  
<span data-ttu-id="5e643-108">\<issuedTokenParameters></span><span class="sxs-lookup"><span data-stu-id="5e643-108">\<issuedTokenParameters></span></span>  
<span data-ttu-id="5e643-109">\<issuerMetadata></span><span class="sxs-lookup"><span data-stu-id="5e643-109">\<issuerMetadata></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5e643-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e643-110">Syntax</span></span>  
  
```xml  
<issuerMetaData address="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5e643-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="5e643-111">Attributes and Elements</span></span>  
 <span data-ttu-id="5e643-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="5e643-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5e643-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="5e643-113">Attributes</span></span>  
  
|<span data-ttu-id="5e643-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="5e643-114">Attribute</span></span>|<span data-ttu-id="5e643-115">Description</span><span class="sxs-lookup"><span data-stu-id="5e643-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5e643-116">adresse</span><span class="sxs-lookup"><span data-stu-id="5e643-116">address</span></span>|<span data-ttu-id="5e643-117">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="5e643-117">Required.</span></span> <span data-ttu-id="5e643-118">Chaîne qui spécifie l'adresse du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="5e643-118">A string that specifies the address of the endpoint.</span></span> <span data-ttu-id="5e643-119">L'adresse doit être un URI absolu.</span><span class="sxs-lookup"><span data-stu-id="5e643-119">The address must be an absolute URI.</span></span> <span data-ttu-id="5e643-120">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="5e643-120">The default value is an empty string.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5e643-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5e643-121">Child Elements</span></span>  
  
|<span data-ttu-id="5e643-122">Élément</span><span class="sxs-lookup"><span data-stu-id="5e643-122">Element</span></span>|<span data-ttu-id="5e643-123">Description</span><span class="sxs-lookup"><span data-stu-id="5e643-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5e643-124">\<headers></span><span class="sxs-lookup"><span data-stu-id="5e643-124">\<headers></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers-element.md)|<span data-ttu-id="5e643-125">Collection d'en-têtes d'adresses.</span><span class="sxs-lookup"><span data-stu-id="5e643-125">A collection of address headers.</span></span>|  
|[<span data-ttu-id="5e643-126">\<identity></span><span class="sxs-lookup"><span data-stu-id="5e643-126">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="5e643-127">Identité qui permet l'authentification d'un point de terminaison par les autres points de terminaison qui échangent des messages avec lui.</span><span class="sxs-lookup"><span data-stu-id="5e643-127">An identity that enables the authentication of an endpoint by other endpoints exchanging messages with it.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="5e643-128">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5e643-128">Parent Elements</span></span>  
  
|<span data-ttu-id="5e643-129">Élément</span><span class="sxs-lookup"><span data-stu-id="5e643-129">Element</span></span>|<span data-ttu-id="5e643-130">Description</span><span class="sxs-lookup"><span data-stu-id="5e643-130">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5e643-131">\<issuedTokenParameters></span><span class="sxs-lookup"><span data-stu-id="5e643-131">\<issuedTokenParameters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtokenparameters.md)|<span data-ttu-id="5e643-132">Indique les paramètres d'un jeton de sécurité émis dans un scénario de sécurité fédéré.</span><span class="sxs-lookup"><span data-stu-id="5e643-132">Specifies the parameters for an security token issued in a Federated security scenario.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="5e643-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e643-133">See also</span></span>

- <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenParameters>
- <xref:System.ServiceModel.Configuration.IssuedTokenParametersElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="5e643-134">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="5e643-134">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="5e643-135">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="5e643-135">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="5e643-136">Fonctionnalités de sécurité avec des liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="5e643-136">Security Capabilities with Custom Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md)
- [<span data-ttu-id="5e643-137">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="5e643-137">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="5e643-138">Liaisons</span><span class="sxs-lookup"><span data-stu-id="5e643-138">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="5e643-139">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="5e643-139">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="5e643-140">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="5e643-140">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="5e643-141">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="5e643-141">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
- [<span data-ttu-id="5e643-142">Guide pratique pour Créer une liaison personnalisée à l’aide de SecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="5e643-142">How to: Create a Custom Binding Using the SecurityBindingElement</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)
- [<span data-ttu-id="5e643-143">Sécurité de liaison personnalisée</span><span class="sxs-lookup"><span data-stu-id="5e643-143">Custom Binding Security</span></span>](../../../../../docs/framework/wcf/samples/custom-binding-security.md)
