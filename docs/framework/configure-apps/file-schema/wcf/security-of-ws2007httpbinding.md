---
title: <security> de <ws2007HttpBinding>
ms.date: 03/30/2017
ms.assetid: fdda0ff7-b462-4e26-af52-e87ddab71945
ms.openlocfilehash: bac8b9c4af812e924296008fa81227d181b30c0d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61670428"
---
# <a name="security-of-ws2007httpbinding"></a><span data-ttu-id="31fe4-102">\<sécurité > de \<ws2007HttpBinding ></span><span class="sxs-lookup"><span data-stu-id="31fe4-102">\<security> of \<ws2007HttpBinding></span></span>
<span data-ttu-id="31fe4-103">Représente les paramètres de sécurité utilisés avec la [ \<ws2007HttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/ws2007httpbinding.md) élément.</span><span class="sxs-lookup"><span data-stu-id="31fe4-103">Represents the security settings used with the [\<ws2007HttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/ws2007httpbinding.md) element.</span></span>  
  
 <span data-ttu-id="31fe4-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="31fe4-104">\<system.serviceModel></span></span>  
<span data-ttu-id="31fe4-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="31fe4-105">\<bindings></span></span>  
<span data-ttu-id="31fe4-106">\<ws2007HttpBinding></span><span class="sxs-lookup"><span data-stu-id="31fe4-106">\<ws2007HttpBinding></span></span>  
<span data-ttu-id="31fe4-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="31fe4-107">\<binding></span></span>  
<span data-ttu-id="31fe4-108">\<security></span><span class="sxs-lookup"><span data-stu-id="31fe4-108">\<security></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="31fe4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31fe4-109">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <bindings>
    <ws2007HttpBinding>
      <binding name = "String">
        <security mode="None/Message/Transport/TransportWithMessageCredential">
          <transport>
          </transport>
          <message>
          </message>
        </security>
      </binding>
    </ws2007HttpBinding>
  </bindings>
</system.ServiceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="31fe4-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="31fe4-110">Attributes and Elements</span></span>  
 <span data-ttu-id="31fe4-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="31fe4-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="31fe4-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="31fe4-112">Attributes</span></span>  
  
|<span data-ttu-id="31fe4-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="31fe4-113">Attribute</span></span>|<span data-ttu-id="31fe4-114">Description</span><span class="sxs-lookup"><span data-stu-id="31fe4-114">Description</span></span>|  
|---------------|-----------------|  
|`mode`|<span data-ttu-id="31fe4-115">-Facultatif.</span><span class="sxs-lookup"><span data-stu-id="31fe4-115">-   Optional.</span></span> <span data-ttu-id="31fe4-116">Spécifie le type de sécurité appliqué.</span><span class="sxs-lookup"><span data-stu-id="31fe4-116">Specifies the type of security that is applied.</span></span> <span data-ttu-id="31fe4-117">La valeur par défaut est `Message`.</span><span class="sxs-lookup"><span data-stu-id="31fe4-117">The default is `Message`.</span></span><br /><br /> <span data-ttu-id="31fe4-118">Cet attribut est de type <xref:System.ServiceModel.SecurityMode>.</span><span class="sxs-lookup"><span data-stu-id="31fe4-118">This attribute is of type <xref:System.ServiceModel.SecurityMode>.</span></span>|  
  
## <a name="mode-attribute"></a><span data-ttu-id="31fe4-119">Mode, attribut</span><span class="sxs-lookup"><span data-stu-id="31fe4-119">Mode Attribute</span></span>  
  
|<span data-ttu-id="31fe4-120">Value</span><span class="sxs-lookup"><span data-stu-id="31fe4-120">Value</span></span>|<span data-ttu-id="31fe4-121">Description</span><span class="sxs-lookup"><span data-stu-id="31fe4-121">Description</span></span>|  
|-----------|-----------------|  
|`None`|<span data-ttu-id="31fe4-122">La sécurité est désactivée.</span><span class="sxs-lookup"><span data-stu-id="31fe4-122">Security is disabled.</span></span>|  
|`Transport`|<span data-ttu-id="31fe4-123">La sécurité est fournie à l'aide de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="31fe4-123">Security is provided using HTTPS.</span></span> <span data-ttu-id="31fe4-124">Le service doit être configuré avec les certificats SSL.</span><span class="sxs-lookup"><span data-stu-id="31fe4-124">The service must be configured with Secure Sockets Layer (SSL) certificates.</span></span> <span data-ttu-id="31fe4-125">Le message est entièrement sécurisé à l’aide du protocole HTTPS et le service est authentifié par le client à l’aide du certificat SSL du service.</span><span class="sxs-lookup"><span data-stu-id="31fe4-125">The message is entirely secured using HTTPS and the service is authenticated by the client using the service’s SSL certificate.</span></span> <span data-ttu-id="31fe4-126">L’authentification du client est contrôlée par le `ClientCredentials` attribut de la [ \<transport >](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-ws2007httpbinding.md) élément.</span><span class="sxs-lookup"><span data-stu-id="31fe4-126">The client authentication is controlled through the `ClientCredentials` attribute of the [\<transport>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-ws2007httpbinding.md) element.</span></span>|  
|`Message`|<span data-ttu-id="31fe4-127">La sécurité est fournie à l'aide de la sécurité des messages SOAP.</span><span class="sxs-lookup"><span data-stu-id="31fe4-127">Security is provided using SOAP message security.</span></span> <span data-ttu-id="31fe4-128">Par défaut, le corps SOAP est chiffré et signé.</span><span class="sxs-lookup"><span data-stu-id="31fe4-128">By default, the SOAP body is encrypted and signed.</span></span> <span data-ttu-id="31fe4-129">Ce mode offre diverses fonctionnalités : déterminer si les informations d'identification du service sont disponibles pour le client hors bande, quelle est la suite algorithmique à utiliser et quel niveau de protection est à appliquer au corps du message via le <xref:System.ServiceModel.Security.SecurityMessageProperty>, entre autres.</span><span class="sxs-lookup"><span data-stu-id="31fe4-129">This mode offers a variety of features, such as whether the service credentials are available at the client out of band, the algorithm suite to use, and what level of protection to apply to the message body through the <xref:System.ServiceModel.Security.SecurityMessageProperty>.</span></span> <span data-ttu-id="31fe4-130">L'authentification du client est exécutée une fois par session et les résultats d'authentification sont mis en cache pour la durée de la session.</span><span class="sxs-lookup"><span data-stu-id="31fe4-130">Client authentication is performed once for each session and the results of authentication are cached for the duration of the session.</span></span>|  
|`TransportWithMessageCredential`|<span data-ttu-id="31fe4-131">Dans ce mode, le protocole HTTPS garantit l'intégrité, la confidentialité et l'authentification du serveur, et la sécurité des messages SOAP garantit l'authentification du client.</span><span class="sxs-lookup"><span data-stu-id="31fe4-131">In this mode, HTTPS provides integrity, confidentiality, and server authentication, and SOAP message security provides client authentication.</span></span> <span data-ttu-id="31fe4-132">Par défaut, l'authentification du client est exécutée une fois par session et les résultats d'authentification sont mis en cache pour la durée de la session.</span><span class="sxs-lookup"><span data-stu-id="31fe4-132">By default, client authentication is performed once for each session and the results of authentication are cached for the duration of the session.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="31fe4-133">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="31fe4-133">Child Elements</span></span>  
  
|<span data-ttu-id="31fe4-134">Élément</span><span class="sxs-lookup"><span data-stu-id="31fe4-134">Element</span></span>|<span data-ttu-id="31fe4-135">Description</span><span class="sxs-lookup"><span data-stu-id="31fe4-135">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="31fe4-136">\<transport></span><span class="sxs-lookup"><span data-stu-id="31fe4-136">\<transport></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-ws2007httpbinding.md)|<span data-ttu-id="31fe4-137">Définit les paramètres de sécurité de transport.</span><span class="sxs-lookup"><span data-stu-id="31fe4-137">Defines the transport security settings.</span></span> <span data-ttu-id="31fe4-138">Cet élément correspond au type <xref:System.ServiceModel.Configuration.HttpTransportSecurityElement>.</span><span class="sxs-lookup"><span data-stu-id="31fe4-138">This element corresponds to the <xref:System.ServiceModel.Configuration.HttpTransportSecurityElement> type.</span></span> <span data-ttu-id="31fe4-139">Ces paramètres sont appliqués uniquement lorsque le mode a la valeur Transport.</span><span class="sxs-lookup"><span data-stu-id="31fe4-139">These settings are applied only when the mode is set to Transport.</span></span>|  
|[<span data-ttu-id="31fe4-140">\<message></span><span class="sxs-lookup"><span data-stu-id="31fe4-140">\<message></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-of-ws2007httpbinding.md)|<span data-ttu-id="31fe4-141">Définit les paramètres de sécurité pour le message.</span><span class="sxs-lookup"><span data-stu-id="31fe4-141">Defines the security settings for the message.</span></span> <span data-ttu-id="31fe4-142">Cet élément correspond au type <xref:System.ServiceModel.Configuration.MessageSecurityOverHttpElement>.</span><span class="sxs-lookup"><span data-stu-id="31fe4-142">This element corresponds to the <xref:System.ServiceModel.Configuration.MessageSecurityOverHttpElement> type.</span></span> <span data-ttu-id="31fe4-143">Ces paramètres ne sont pas appliqués lorsque le mode a la valeur Transport.</span><span class="sxs-lookup"><span data-stu-id="31fe4-143">These settings are not applied when the mode is set to Transport.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="31fe4-144">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="31fe4-144">Parent Elements</span></span>  
  
|<span data-ttu-id="31fe4-145">Élément</span><span class="sxs-lookup"><span data-stu-id="31fe4-145">Element</span></span>|<span data-ttu-id="31fe4-146">Description</span><span class="sxs-lookup"><span data-stu-id="31fe4-146">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="31fe4-147">\<ws2007HttpBinding></span><span class="sxs-lookup"><span data-stu-id="31fe4-147">\<ws2007HttpBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/ws2007httpbinding.md)|<span data-ttu-id="31fe4-148">Liaison sécurisée pour les applications de transport HTTP.</span><span class="sxs-lookup"><span data-stu-id="31fe4-148">A secure binding for HTTP transport applications.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="31fe4-149">Notes</span><span class="sxs-lookup"><span data-stu-id="31fe4-149">Remarks</span></span>  
 <span data-ttu-id="31fe4-150">Cet élément est conçu pour interagir avec les services qui implémentent les spécifications WS-\*.</span><span class="sxs-lookup"><span data-stu-id="31fe4-150">This element is designed for interoperation with services that implement WS-\* specifications.</span></span> <span data-ttu-id="31fe4-151">La sécurité de transport de cette liaison correspond à Secure Sockets Layer (SSL) sur HTTP, c'est-à-dire à HTTPS.</span><span class="sxs-lookup"><span data-stu-id="31fe4-151">The transport security for this binding is Secure Sockets Layer (SSL) over HTTP, or HTTPS.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="31fe4-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31fe4-152">See also</span></span>

- <xref:System.ServiceModel.WSHttpSecurity>
- <xref:System.ServiceModel.WSHttpBinding.Security%2A>
- <xref:System.ServiceModel.Configuration.WSHttpBindingElement.Security%2A>
- <xref:System.ServiceModel.Configuration.WSHttpSecurityElement>
- <xref:System.ServiceModel.BasicHttpSecurity>
- [<span data-ttu-id="31fe4-153">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="31fe4-153">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="31fe4-154">Liaisons</span><span class="sxs-lookup"><span data-stu-id="31fe4-154">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="31fe4-155">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="31fe4-155">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="31fe4-156">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="31fe4-156">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="31fe4-157">\<binding></span><span class="sxs-lookup"><span data-stu-id="31fe4-157">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
