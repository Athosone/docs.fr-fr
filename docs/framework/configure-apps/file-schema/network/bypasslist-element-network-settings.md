---
title: <bypasslist>, élément (paramètres réseau)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#bypasslist
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/defaultProxy/bypasslist
helpviewer_keywords:
- bypasslist element
- <bypasslist> element
ms.assetid: 124446b7-abb1-4e5e-a492-b64398f268f1
ms.openlocfilehash: d3d986dae478f49504dae21b9f39574b7887b4d2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61674621"
---
# <a name="bypasslist-element-network-settings"></a><span data-ttu-id="3674e-102">\<BypassList >, élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="3674e-102">\<bypasslist> Element (Network Settings)</span></span>
<span data-ttu-id="3674e-103">Fournit un ensemble d’expressions régulières décrivant les adresses qui n’utilisent pas un proxy.</span><span class="sxs-lookup"><span data-stu-id="3674e-103">Provides a set of regular expressions that describe addresses that do not use a proxy.</span></span>  
  
 <span data-ttu-id="3674e-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="3674e-104">\<configuration></span></span>  
<span data-ttu-id="3674e-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="3674e-105">\<system.net></span></span>  
<span data-ttu-id="3674e-106">\<defaultProxy></span><span class="sxs-lookup"><span data-stu-id="3674e-106">\<defaultProxy></span></span>  
<span data-ttu-id="3674e-107">\<bypasslist></span><span class="sxs-lookup"><span data-stu-id="3674e-107">\<bypasslist></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3674e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3674e-108">Syntax</span></span>  
  
```xml  
<bypasslist>   
</bypasslist>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3674e-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="3674e-109">Attributes and Elements</span></span>  
 <span data-ttu-id="3674e-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="3674e-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3674e-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="3674e-111">Attributes</span></span>  
 <span data-ttu-id="3674e-112">Aucun.</span><span class="sxs-lookup"><span data-stu-id="3674e-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="3674e-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3674e-113">Child Elements</span></span>  
  
|<span data-ttu-id="3674e-114">**Élément**</span><span class="sxs-lookup"><span data-stu-id="3674e-114">**Element**</span></span>|<span data-ttu-id="3674e-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="3674e-115">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="3674e-116">add</span><span class="sxs-lookup"><span data-stu-id="3674e-116">add</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/add-element-for-bypasslist-network-settings.md)|<span data-ttu-id="3674e-117">Ajoute une adresse IP ou le nom DNS à la liste de contournement proxy.</span><span class="sxs-lookup"><span data-stu-id="3674e-117">Adds an IP address or DNS name to the proxy bypass list.</span></span>|  
|[<span data-ttu-id="3674e-118">clear</span><span class="sxs-lookup"><span data-stu-id="3674e-118">clear</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/clear-element-for-bypasslist-network-settings.md)|<span data-ttu-id="3674e-119">Efface la liste de contournement.</span><span class="sxs-lookup"><span data-stu-id="3674e-119">Clears the bypass list.</span></span>|  
|[<span data-ttu-id="3674e-120">remove</span><span class="sxs-lookup"><span data-stu-id="3674e-120">remove</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/remove-element-for-bypasslist-network-settings.md)|<span data-ttu-id="3674e-121">Supprime une adresse IP ou le nom DNS de la liste de contournement proxy.</span><span class="sxs-lookup"><span data-stu-id="3674e-121">Removes an IP address or DNS name from the proxy bypass list.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="3674e-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3674e-122">Parent Elements</span></span>  
  
|<span data-ttu-id="3674e-123">**Élément**</span><span class="sxs-lookup"><span data-stu-id="3674e-123">**Element**</span></span>|<span data-ttu-id="3674e-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="3674e-124">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="3674e-125">defaultProxy</span><span class="sxs-lookup"><span data-stu-id="3674e-125">defaultProxy</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/defaultproxy-element-network-settings.md)|<span data-ttu-id="3674e-126">Configure le serveur proxy HTTP (Hypertext Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="3674e-126">Configures the Hypertext Transfer Protocol (HTTP) proxy server.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3674e-127">Notes</span><span class="sxs-lookup"><span data-stu-id="3674e-127">Remarks</span></span>  
 <span data-ttu-id="3674e-128">La liste de contournement contient des expressions régulières qui décrivent les URI qui <xref:System.Net.WebRequest> instances accéder directement au lieu de via le serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="3674e-128">The bypass list contains regular expressions that describe URIs that <xref:System.Net.WebRequest> instances access directly instead of through the proxy server.</span></span>  
  
 <span data-ttu-id="3674e-129">Soyez prudent lorsque vous spécifiez une expression régulière pour cet élément.</span><span class="sxs-lookup"><span data-stu-id="3674e-129">You should use caution when specifying a regular expression for this element.</span></span> <span data-ttu-id="3674e-130">L’expression régulière « [a-z] +\\.contoso\\.com » correspond à tout hôte dans le domaine contoso.com, mais il correspond également à n’importe quel hôte dans le domaine contoso.com.cpandl.com.</span><span class="sxs-lookup"><span data-stu-id="3674e-130">The regular expression "[a-z]+\\.contoso\\.com" matches any host in the contoso.com domain, but it also matches any host in the contoso.com.cpandl.com domain.</span></span> <span data-ttu-id="3674e-131">Pour faire correspondre uniquement sur un ordinateur hôte dans le domaine contoso.com, utilisez une ancre (« $») : « [a-z] +\\.contoso\\.com$ ».</span><span class="sxs-lookup"><span data-stu-id="3674e-131">To match only a host in the contoso.com domain, use an anchor ("$"): "[a-z]+\\.contoso\\.com$".</span></span>  
  
 <span data-ttu-id="3674e-132">Pour plus d’informations sur les expressions régulières, consultez. [Expressions régulières .NET framework](../../../../../docs/standard/base-types/regular-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="3674e-132">For more information about regular expressions, see .[.NET Framework Regular Expressions](../../../../../docs/standard/base-types/regular-expressions.md).</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="3674e-133">Fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="3674e-133">Configuration Files</span></span>  
 <span data-ttu-id="3674e-134">Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="3674e-134">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="3674e-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="3674e-135">Example</span></span>  
 <span data-ttu-id="3674e-136">L’exemple suivant ajoute deux adresses à la liste de contournement.</span><span class="sxs-lookup"><span data-stu-id="3674e-136">The following example adds two addresses to the bypass list.</span></span> <span data-ttu-id="3674e-137">La première contourne le proxy pour tous les serveurs dans le domaine contoso.com ; la deuxième contourne le proxy pour tous les serveurs dont les adresses IP commencent par 192.168.</span><span class="sxs-lookup"><span data-stu-id="3674e-137">The first bypasses the proxy for all servers in the contoso.com domain; the second bypasses the proxy for all servers whose IP addresses begin with 192.168.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <defaultProxy>  
      <bypasslist>  
        <add address="[a-z]+\.contoso\.com$" />  
        <add address="192\.168\.\d{1,3}\.\d{1,3}" />  
      </bypasslist>  
    </defaultProxy>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="3674e-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3674e-138">See also</span></span>

- <xref:System.Net.WebProxy?displayProperty=nameWithType>
- [<span data-ttu-id="3674e-139">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="3674e-139">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
