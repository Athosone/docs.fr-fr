---
title: <transport> de <webHttpBinding>
ms.date: 03/30/2017
ms.assetid: f150fb19-7de1-44af-81f4-86cad881cd05
ms.openlocfilehash: 8dcd51cd248dbba3ccf60295cb1712167684328e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59116280"
---
# <a name="transport-of-webhttpbinding"></a><span data-ttu-id="fba7a-102">\<transport > de \<webHttpBinding ></span><span class="sxs-lookup"><span data-stu-id="fba7a-102">\<transport> of \<webHttpBinding></span></span>
<span data-ttu-id="fba7a-103">Définit les paramètres de sécurité au niveau du transport pour un point de terminaison de service configuré pour recevoir des demandes HTTP.</span><span class="sxs-lookup"><span data-stu-id="fba7a-103">Defines the transport-level security settings for a service endpoint configured to receive HTTP requests.</span></span>  
  
 <span data-ttu-id="fba7a-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="fba7a-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="fba7a-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="fba7a-105">\<bindings></span></span>  
<span data-ttu-id="fba7a-106">\<webHttpBinding></span><span class="sxs-lookup"><span data-stu-id="fba7a-106">\<webHttpBinding></span></span>  
<span data-ttu-id="fba7a-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="fba7a-107">\<binding></span></span>  
<span data-ttu-id="fba7a-108">\<security></span><span class="sxs-lookup"><span data-stu-id="fba7a-108">\<security></span></span>  
<span data-ttu-id="fba7a-109">\<transport></span><span class="sxs-lookup"><span data-stu-id="fba7a-109">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fba7a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fba7a-110">Syntax</span></span>  
  
```xml  
<webHttpBinding>
  <binding>
    <security mode="None|Transport|Message|TransportWithMessageCredential|TransportCredentialOnly">
      <transport clientCredentialType="None|Basic|Digest|Ntlm|Windows"
                 proxyCredentialType="None|Basic|Digest|Ntlm|Windows"
                 realm="string">
        <extendedProtectionPolicy policyEnforcement="Never|WhenSupported|Always"
                                  protectionScenario="TransportSelected|TrustedProxy">
          <customServiceNames>
          </customServiceNames>
        </extendedProtectionPolicy>
      </transport>
    </security>
  </binding>
</webHttpBinding>
```  
  
## <a name="type"></a><span data-ttu-id="fba7a-111">Type</span><span class="sxs-lookup"><span data-stu-id="fba7a-111">Type</span></span>  
 <xref:System.ServiceModel.HttpTransportSecurity>  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="fba7a-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="fba7a-112">Attributes and Elements</span></span>  
 <span data-ttu-id="fba7a-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="fba7a-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="fba7a-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="fba7a-114">Attributes</span></span>  
  
|<span data-ttu-id="fba7a-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="fba7a-115">Attribute</span></span>|<span data-ttu-id="fba7a-116">Description</span><span class="sxs-lookup"><span data-stu-id="fba7a-116">Description</span></span>|  
|---------------|-----------------|  
|`clientCredentialType`|<span data-ttu-id="fba7a-117">Spécifie les informations d'identification utilisées pour authentifier le client auprès du service.</span><span class="sxs-lookup"><span data-stu-id="fba7a-117">Specifies the credential used to authenticate the client to the service.</span></span> <span data-ttu-id="fba7a-118">Cet attribut est de type <xref:System.ServiceModel.HttpClientCredentialType>.</span><span class="sxs-lookup"><span data-stu-id="fba7a-118">This attribute is of type <xref:System.ServiceModel.HttpClientCredentialType>.</span></span>|  
|`proxyCredentialType`|<span data-ttu-id="fba7a-119">Spécifie les informations d'identification utilisées pour authentifier le client auprès d'un proxy de domaine.</span><span class="sxs-lookup"><span data-stu-id="fba7a-119">Specifies the credential used to authenticate the client to a domain proxy.</span></span> <span data-ttu-id="fba7a-120">Cet attribut est de type <xref:System.ServiceModel.HttpProxyCredentialType>.</span><span class="sxs-lookup"><span data-stu-id="fba7a-120">This attribute is of type <xref:System.ServiceModel.HttpProxyCredentialType>.</span></span>|  
|`realm`|<span data-ttu-id="fba7a-121">Chaîne indiquant le domaine de l’authentification de base ou Digest.</span><span class="sxs-lookup"><span data-stu-id="fba7a-121">A string that specifies the authentication realm for digest or basic authentication.</span></span> <span data-ttu-id="fba7a-122">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="fba7a-122">The default is an empty string.</span></span><br /><br /> <span data-ttu-id="fba7a-123">Un domaine d'authentification spécifie au moins le nom de l'hôte qui exécute l'authentification.</span><span class="sxs-lookup"><span data-stu-id="fba7a-123">An authentication realm specifies at least the name of the host that performs the authentication.</span></span> <span data-ttu-id="fba7a-124">Il peut également spécifier une collection d’utilisateurs disposant d’un accès.</span><span class="sxs-lookup"><span data-stu-id="fba7a-124">It can also specify a collection of users that has access.</span></span> <span data-ttu-id="fba7a-125">Un utilisateur peut interroger le domaine d'authentification pour vérifier quels noms d'utilisateurs et mots de passe peuvent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="fba7a-125">A user can query the authentication realm to ascertain which one of the several possible usernames and passwords can be used.</span></span>|  
|`policyEnforcement`|<span data-ttu-id="fba7a-126">Cette énumération spécifie à quel moment <xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy> doit être appliqué.</span><span class="sxs-lookup"><span data-stu-id="fba7a-126">This enumeration specifies when the <xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy> should be enforced.</span></span><br /><br /> <span data-ttu-id="fba7a-127">1.  Never : la stratégie n'est jamais appliquée (la protection étendue est désactivée).</span><span class="sxs-lookup"><span data-stu-id="fba7a-127">1.  Never – The policy is never enforced (Extended Protection is disabled).</span></span><br /><span data-ttu-id="fba7a-128">2.  WhenSupported : la stratégie est appliquée uniquement si le client prend en charge la protection étendue.</span><span class="sxs-lookup"><span data-stu-id="fba7a-128">2.  WhenSupported – The policy is enforced only if the client supports Extended Protection.</span></span><br /><span data-ttu-id="fba7a-129">3.  Always : la stratégie est toujours appliquée.</span><span class="sxs-lookup"><span data-stu-id="fba7a-129">3.  Always – The policy is always enforced.</span></span> <span data-ttu-id="fba7a-130">Les clients qui ne prennent pas en charge la protection étendue ne pourront pas être authentifiés.</span><span class="sxs-lookup"><span data-stu-id="fba7a-130">Clients which don’t support Extended Protection will fail to authenticate.</span></span>|  
  
## <a name="clientcredentialtype-attribute"></a><span data-ttu-id="fba7a-131">Attribut clientCredentialType</span><span class="sxs-lookup"><span data-stu-id="fba7a-131">clientCredentialType Attribute</span></span>  
  
|<span data-ttu-id="fba7a-132">Value</span><span class="sxs-lookup"><span data-stu-id="fba7a-132">Value</span></span>|<span data-ttu-id="fba7a-133">Description</span><span class="sxs-lookup"><span data-stu-id="fba7a-133">Description</span></span>|  
|-----------|-----------------|  
|`None`|<span data-ttu-id="fba7a-134">La sécurité est désactivée.</span><span class="sxs-lookup"><span data-stu-id="fba7a-134">Security is disabled.</span></span>|  
|`Basic`|<span data-ttu-id="fba7a-135">Utilise l'authentification de base.</span><span class="sxs-lookup"><span data-stu-id="fba7a-135">Uses basic authentication.</span></span>|  
|`Certificate`|<span data-ttu-id="fba7a-136">Utilise des certificats X.509 pour authentifier le client.</span><span class="sxs-lookup"><span data-stu-id="fba7a-136">Uses X.509 certificates to authenticate the client.</span></span>|  
|`Digest`|<span data-ttu-id="fba7a-137">Utilise l’authentification Digest.</span><span class="sxs-lookup"><span data-stu-id="fba7a-137">Uses digest authentication.</span></span>|  
|`Ntlm`|<span data-ttu-id="fba7a-138">Utilise l'authentification NTLM comme solution de secours dans un domaine Windows.</span><span class="sxs-lookup"><span data-stu-id="fba7a-138">Uses NTLM authentication as a fallback with a Windows domain.</span></span>|  
|`Windows`|<span data-ttu-id="fba7a-139">Utilise l'authentification intégrée Windows.</span><span class="sxs-lookup"><span data-stu-id="fba7a-139">Uses integrated Windows authentication.</span></span>|  
  
## <a name="proxycredentialtype-attribute"></a><span data-ttu-id="fba7a-140">Attribut proxyCredentialType</span><span class="sxs-lookup"><span data-stu-id="fba7a-140">proxyCredentialType Attribute</span></span>  
  
|<span data-ttu-id="fba7a-141">Value</span><span class="sxs-lookup"><span data-stu-id="fba7a-141">Value</span></span>|<span data-ttu-id="fba7a-142">Description</span><span class="sxs-lookup"><span data-stu-id="fba7a-142">Description</span></span>|  
|-----------|-----------------|  
|`None`|<span data-ttu-id="fba7a-143">La sécurité est désactivée.</span><span class="sxs-lookup"><span data-stu-id="fba7a-143">Security is disabled.</span></span>|  
|`Basic`|<span data-ttu-id="fba7a-144">Utilise l'authentification de base.</span><span class="sxs-lookup"><span data-stu-id="fba7a-144">Uses basic authentication.</span></span>|  
|`Digest`|<span data-ttu-id="fba7a-145">Utilise l’authentification Digest.</span><span class="sxs-lookup"><span data-stu-id="fba7a-145">Uses digest authentication.</span></span>|  
|`Ntlm`|<span data-ttu-id="fba7a-146">Utilise l'authentification NTLM comme solution de secours dans un domaine Windows.</span><span class="sxs-lookup"><span data-stu-id="fba7a-146">Uses NTLM as a fallback with a Windows domain.</span></span>|  
|`Windows`|<span data-ttu-id="fba7a-147">Utilise l'authentification intégrée Windows.</span><span class="sxs-lookup"><span data-stu-id="fba7a-147">Uses integrated Windows authentication.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="fba7a-148">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fba7a-148">Child Elements</span></span>  
 <span data-ttu-id="fba7a-149">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fba7a-149">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="fba7a-150">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fba7a-150">Parent Elements</span></span>  
  
|<span data-ttu-id="fba7a-151">Élément</span><span class="sxs-lookup"><span data-stu-id="fba7a-151">Element</span></span>|<span data-ttu-id="fba7a-152">Description</span><span class="sxs-lookup"><span data-stu-id="fba7a-152">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="fba7a-153">\<security></span><span class="sxs-lookup"><span data-stu-id="fba7a-153">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-webhttpbinding.md)|<span data-ttu-id="fba7a-154">Représente les fonctionnalités de sécurité de la [ \<wsHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md) élément.</span><span class="sxs-lookup"><span data-stu-id="fba7a-154">Represents the security capabilities of the [\<wsHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md) element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="fba7a-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fba7a-155">See also</span></span>

- <xref:System.ServiceModel.HttpTransportSecurity>
- <xref:System.ServiceModel.Configuration.WebHttpSecurityElement.Transport%2A>
- <xref:System.ServiceModel.WebHttpSecurity.Transport%2A>
- <xref:System.ServiceModel.Configuration.HttpTransportSecurityElement>
- [<span data-ttu-id="fba7a-156">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="fba7a-156">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="fba7a-157">Liaisons</span><span class="sxs-lookup"><span data-stu-id="fba7a-157">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="fba7a-158">Configuration des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="fba7a-158">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="fba7a-159">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="fba7a-159">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="fba7a-160">\<binding></span><span class="sxs-lookup"><span data-stu-id="fba7a-160">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
- [<span data-ttu-id="fba7a-161">Modèle de programmation HTTP web WCF</span><span class="sxs-lookup"><span data-stu-id="fba7a-161">WCF Web HTTP Programming Model</span></span>](../../../../../docs/framework/wcf/feature-details/wcf-web-http-programming-model.md)
