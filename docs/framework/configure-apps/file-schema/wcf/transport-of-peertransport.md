---
title: <transport> de <peerTransport>
ms.date: 03/30/2017
ms.assetid: d7116240-845c-4b6f-b203-262de6b597ef
ms.openlocfilehash: 9b6f548515afbba5068659bd5c6f7f2b33f80cda
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59076001"
---
# <a name="transport-of-peertransport"></a><span data-ttu-id="12b00-102">\<transport > de \<peerTransport ></span><span class="sxs-lookup"><span data-stu-id="12b00-102">\<transport> of \<peerTransport></span></span>
<span data-ttu-id="12b00-103">Indique le type de transport correspondant aux messages sécurisés envoyés par des homologues configurés avec cette liaison.</span><span class="sxs-lookup"><span data-stu-id="12b00-103">Specifies the transport type for secured messages sent by peers configured with this binding.</span></span>  
  
 <span data-ttu-id="12b00-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="12b00-104">\<system.serviceModel></span></span>  
<span data-ttu-id="12b00-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="12b00-105">\<bindings></span></span>  
<span data-ttu-id="12b00-106">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="12b00-106">\<customBinding></span></span>  
<span data-ttu-id="12b00-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="12b00-107">\<binding></span></span>  
<span data-ttu-id="12b00-108">\<peerTransport></span><span class="sxs-lookup"><span data-stu-id="12b00-108">\<peerTransport></span></span>  
<span data-ttu-id="12b00-109">\<security></span><span class="sxs-lookup"><span data-stu-id="12b00-109">\<security></span></span>  
<span data-ttu-id="12b00-110">\<transport></span><span class="sxs-lookup"><span data-stu-id="12b00-110">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="12b00-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12b00-111">Syntax</span></span>  
  
```xml  
<security>
  <transport credentialType="Certificate/Password" />
</security>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="12b00-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="12b00-112">Attributes and Elements</span></span>  
 <span data-ttu-id="12b00-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="12b00-113">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="12b00-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="12b00-114">Attributes</span></span>  
  
|<span data-ttu-id="12b00-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="12b00-115">Attribute</span></span>|<span data-ttu-id="12b00-116">Description</span><span class="sxs-lookup"><span data-stu-id="12b00-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="12b00-117">credentialType</span><span class="sxs-lookup"><span data-stu-id="12b00-117">credentialType</span></span>|<span data-ttu-id="12b00-118">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="12b00-118">Optional.</span></span> <span data-ttu-id="12b00-119">Spécifie le type d'informations d'identification utilisé pour vérifier les messages envoyés avec le transport d'homologues.</span><span class="sxs-lookup"><span data-stu-id="12b00-119">Specifies the type of credentials used to verify messages sent with the peer transport.</span></span> <span data-ttu-id="12b00-120">Cet attribut est de type <xref:System.ServiceModel.PeerTransportCredentialType>.</span><span class="sxs-lookup"><span data-stu-id="12b00-120">This attribute is of type <xref:System.ServiceModel.PeerTransportCredentialType>.</span></span>|  
  
## <a name="credentialtype-attribute"></a><span data-ttu-id="12b00-121">Attribut credentialType</span><span class="sxs-lookup"><span data-stu-id="12b00-121">credentialType Attribute</span></span>  
  
|<span data-ttu-id="12b00-122">Value</span><span class="sxs-lookup"><span data-stu-id="12b00-122">Value</span></span>|<span data-ttu-id="12b00-123">Description</span><span class="sxs-lookup"><span data-stu-id="12b00-123">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="12b00-124">Certificat</span><span class="sxs-lookup"><span data-stu-id="12b00-124">Certificate</span></span>|<span data-ttu-id="12b00-125">L'authentification du transport de canal homologue requiert un certificat X509.</span><span class="sxs-lookup"><span data-stu-id="12b00-125">Authentication of the peer channel transport requires an X509 certificate.</span></span>|  
|<span data-ttu-id="12b00-126">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="12b00-126">Password</span></span>|<span data-ttu-id="12b00-127">L'authentification du transport de canal homologue requiert un mot de passe correct.</span><span class="sxs-lookup"><span data-stu-id="12b00-127">Authentication of the peer channel transport requires a correct password.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="12b00-128">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="12b00-128">Child Elements</span></span>  
 <span data-ttu-id="12b00-129">Aucun.</span><span class="sxs-lookup"><span data-stu-id="12b00-129">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="12b00-130">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="12b00-130">Parent Elements</span></span>  
  
|<span data-ttu-id="12b00-131">Élément</span><span class="sxs-lookup"><span data-stu-id="12b00-131">Element</span></span>|<span data-ttu-id="12b00-132">Description</span><span class="sxs-lookup"><span data-stu-id="12b00-132">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="12b00-133">\<security></span><span class="sxs-lookup"><span data-stu-id="12b00-133">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-peertransport.md)|<span data-ttu-id="12b00-134">Définit les paramètres de sécurité pour un transport d'homologue.</span><span class="sxs-lookup"><span data-stu-id="12b00-134">Defines the security settings for a peer transport.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="12b00-135">Notes</span><span class="sxs-lookup"><span data-stu-id="12b00-135">Remarks</span></span>  
 <span data-ttu-id="12b00-136">Cet élément est défini uniquement si l’attribut de mode de [ \<sécurité >](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-peertransport.md) a la valeur `Transport` ou `TransportWithMessageCredential`.</span><span class="sxs-lookup"><span data-stu-id="12b00-136">This element is set only if the mode attribute of [\<security>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-peertransport.md) is set to `Transport` or `TransportWithMessageCredential`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="12b00-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12b00-137">See also</span></span>

- <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement>
- <xref:System.ServiceModel.PeerSecuritySettings.Transport%2A>
- <xref:System.ServiceModel.PeerTransportSecuritySettings>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="12b00-138">Sécurité de transport</span><span class="sxs-lookup"><span data-stu-id="12b00-138">Transport Security</span></span>](../../../../../docs/framework/wcf/feature-details/transport-security.md)
- [<span data-ttu-id="12b00-139">Transports</span><span class="sxs-lookup"><span data-stu-id="12b00-139">Transports</span></span>](../../../../../docs/framework/wcf/feature-details/transports.md)
- [<span data-ttu-id="12b00-140">Choix d’un transport</span><span class="sxs-lookup"><span data-stu-id="12b00-140">Choosing a Transport</span></span>](../../../../../docs/framework/wcf/feature-details/choosing-a-transport.md)
- [<span data-ttu-id="12b00-141">Liaisons</span><span class="sxs-lookup"><span data-stu-id="12b00-141">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="12b00-142">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="12b00-142">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="12b00-143">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="12b00-143">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="12b00-144">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="12b00-144">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
