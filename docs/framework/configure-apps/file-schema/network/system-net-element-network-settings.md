---
title: <system.Net>, élément (paramètres réseau)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#system.Net
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.Net
helpviewer_keywords:
- system.Net element
- <system.Net> element
ms.assetid: 52de4d6c-b24d-44aa-ba7d-6b5061f1357e
ms.openlocfilehash: febea73ddbc45276f97835eb4af7ee0d0d68dda5
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59095268"
---
# <a name="systemnet-element-network-settings"></a><span data-ttu-id="0f2f5-102">\<system.Net >, élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="0f2f5-102">\<system.Net> Element (Network Settings)</span></span>
<span data-ttu-id="0f2f5-103">Contient des paramètres qui spécifient la manière dont .NET Framework se connecte au réseau.</span><span class="sxs-lookup"><span data-stu-id="0f2f5-103">Contains settings that specify how the .NET Framework connects to the network.</span></span>  
  
 <span data-ttu-id="0f2f5-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="0f2f5-104">\<configuration></span></span>  
<span data-ttu-id="0f2f5-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="0f2f5-105">\<system.net></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0f2f5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f2f5-106">Syntax</span></span>  
  
```xml  
<system.net>   
</system.net>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0f2f5-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="0f2f5-107">Attributes and Elements</span></span>  
 <span data-ttu-id="0f2f5-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="0f2f5-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0f2f5-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="0f2f5-109">Attributes</span></span>  
 <span data-ttu-id="0f2f5-110">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0f2f5-110">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="0f2f5-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0f2f5-111">Child Elements</span></span>  
  
|<span data-ttu-id="0f2f5-112">**Élément**</span><span class="sxs-lookup"><span data-stu-id="0f2f5-112">**Element**</span></span>|<span data-ttu-id="0f2f5-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="0f2f5-113">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="0f2f5-114">authenticationModules</span><span class="sxs-lookup"><span data-stu-id="0f2f5-114">authenticationModules</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/authenticationmodules-element-network-settings.md)|<span data-ttu-id="0f2f5-115">Spécifie les modules utilisés pour authentifier les demandes Internet.</span><span class="sxs-lookup"><span data-stu-id="0f2f5-115">Specifies modules used to authenticate Internet requests.</span></span>|  
|[<span data-ttu-id="0f2f5-116">connectionManagement</span><span class="sxs-lookup"><span data-stu-id="0f2f5-116">connectionManagement</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/connectionmanagement-element-network-settings.md)|<span data-ttu-id="0f2f5-117">Spécifie le nombre maximal de connexions à un hôte Internet.</span><span class="sxs-lookup"><span data-stu-id="0f2f5-117">Specifies the maximum number of connections to an Internet host.</span></span>|  
|[<span data-ttu-id="0f2f5-118">defaultProxy</span><span class="sxs-lookup"><span data-stu-id="0f2f5-118">defaultProxy</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/defaultproxy-element-network-settings.md)|<span data-ttu-id="0f2f5-119">Configure le serveur proxy HTTP (Hypertext Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="0f2f5-119">Configures the Hypertext Transfer Protocol (HTTP) proxy server.</span></span>|  
|[<span data-ttu-id="0f2f5-120">mailSettings</span><span class="sxs-lookup"><span data-stu-id="0f2f5-120">mailSettings</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/mailsettings-element-network-settings.md)|<span data-ttu-id="0f2f5-121">Configure les options d’envoi du courrier SMTP Simple Mail Transport Protocol ().</span><span class="sxs-lookup"><span data-stu-id="0f2f5-121">Configures Simple Mail Transport Protocol (SMTP) mail sending options.</span></span>|  
|[<span data-ttu-id="0f2f5-122">requestCaching</span><span class="sxs-lookup"><span data-stu-id="0f2f5-122">requestCaching</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/requestcaching-element-network-settings.md)|<span data-ttu-id="0f2f5-123">Contrôle le mécanisme de mise en cache pour les demandes réseau.</span><span class="sxs-lookup"><span data-stu-id="0f2f5-123">Controls the caching mechanism for network requests.</span></span>|  
|[<span data-ttu-id="0f2f5-124">settings</span><span class="sxs-lookup"><span data-stu-id="0f2f5-124">settings</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/settings-element-network-settings.md)|<span data-ttu-id="0f2f5-125">Configure les options réseau de base pour les classes dans le <xref:System.Net> et les espaces de noms enfants.</span><span class="sxs-lookup"><span data-stu-id="0f2f5-125">Configures basic network options for classes in the <xref:System.Net> and related child namespaces.</span></span>|  
|[<span data-ttu-id="0f2f5-126">webRequestModules</span><span class="sxs-lookup"><span data-stu-id="0f2f5-126">webRequestModules</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/webrequestmodules-element-network-settings.md)|<span data-ttu-id="0f2f5-127">Spécifie les modules à utiliser pour demander des informations à partir d’hôtes Internet.</span><span class="sxs-lookup"><span data-stu-id="0f2f5-127">Specifies modules to use to request information from Internet hosts.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="0f2f5-128">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0f2f5-128">Parent Elements</span></span>  
  
|<span data-ttu-id="0f2f5-129">**Élément**</span><span class="sxs-lookup"><span data-stu-id="0f2f5-129">**Element**</span></span>|<span data-ttu-id="0f2f5-130">**Description**</span><span class="sxs-lookup"><span data-stu-id="0f2f5-130">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="0f2f5-131">configuration</span><span class="sxs-lookup"><span data-stu-id="0f2f5-131">configuration</span></span>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)|<span data-ttu-id="0f2f5-132">Contient des paramètres pour tous les espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="0f2f5-132">Contains settings for all namespaces.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0f2f5-133">Notes</span><span class="sxs-lookup"><span data-stu-id="0f2f5-133">Remarks</span></span>  
 <span data-ttu-id="0f2f5-134">Le [ \<system.net >](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md) élément contient des paramètres pour les classes dans le <xref:System.Net> et les espaces de noms enfants.</span><span class="sxs-lookup"><span data-stu-id="0f2f5-134">The [\<system.net>](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md) element contains settings for classes in the <xref:System.Net> and related child namespaces.</span></span> <span data-ttu-id="0f2f5-135">Les paramètres configurent les modules d’authentification, gestion des connexions, les paramètres de messagerie, le serveur proxy et les modules de demande Internet pour recevoir des informations à partir d’hôtes Internet.</span><span class="sxs-lookup"><span data-stu-id="0f2f5-135">The settings configure authentication modules, connection management, mail settings, the proxy server, and Internet request modules for receiving information from Internet hosts.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0f2f5-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="0f2f5-136">Example</span></span>  
 <span data-ttu-id="0f2f5-137">L’exemple suivant montre une configuration classique utilisée par <xref:System.Net> classes.</span><span class="sxs-lookup"><span data-stu-id="0f2f5-137">The following example shows a typical configuration used by <xref:System.Net> classes.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <authenticationModules>  
      <add type="System.Net.DigestClient" />  
      <add type="System.Net.NegotiateClient" />  
      <add type="System.Net.KerberosClient" />  
      <add type="System.Net.NtlmClient" />  
      <add type="System.Net.BasicClient" />  
    </authenticationModules>  
    <connectionManagement>  
      <add address="*" maxconnection="2" />  
    </connectionManagement>  
    <defaultProxy>  
      <proxy  
        usesystemdefault="true"  
        bypassonlocal="true"  
      />  
    </defaultProxy>  
    <webRequestModules>  
      <add prefix="http"  
           type="System.Net.HttpRequestCreator"  
      />  
      <add prefix="https"  
           type="System.Net.HttpRequestCreator"  
      />  
      <add prefix="file"  
           type="System.Net.FileWebRequestCreator"  
      />  
    </webRequestModules>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="0f2f5-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f2f5-138">See also</span></span>

- [<span data-ttu-id="0f2f5-139">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="0f2f5-139">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
