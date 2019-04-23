---
title: <add> de <protocolMapping>
ms.date: 03/30/2017
ms.assetid: 08e62249-1641-41d1-91b1-66d7b46244e4
ms.openlocfilehash: 85d09c920de2ca1ab4971551ff98ea58c4492f44
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59109263"
---
# <a name="add-of-protocolmapping"></a><span data-ttu-id="606e3-102">\<add> of \<protocolMapping></span><span class="sxs-lookup"><span data-stu-id="606e3-102">\<add> of \<protocolMapping></span></span>
<span data-ttu-id="606e3-103">Représente un mappage de protocole par défaut entre un schéma de protocole de transport (par exemple, http, net.tcp, net.pipe, etc.) et une liaison Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="606e3-103">Represents a default protocol mapping between a transport protocol scheme (e.g., http, net.tcp, net.pipe, etc.) and a Windows Communication Foundation (WCF) binding.</span></span> <span data-ttu-id="606e3-104">Lorsque vous créez des points de terminaison par défaut lors de l’exécution, WCF examine les mappages configurés et décide de liaison à utiliser en tant qu’adresse de base.</span><span class="sxs-lookup"><span data-stu-id="606e3-104">When creating default endpoints at runtime, WCF looks at the configured mappings and decides on which binding to use for a particular based address.</span></span>  
  
 <span data-ttu-id="606e3-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="606e3-105">\<system.serviceModel></span></span>  
<span data-ttu-id="606e3-106">\<protocolMapping></span><span class="sxs-lookup"><span data-stu-id="606e3-106">\<protocolMapping></span></span>  
<span data-ttu-id="606e3-107">\<add></span><span class="sxs-lookup"><span data-stu-id="606e3-107">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="606e3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="606e3-108">Syntax</span></span>  
  
```xml  
<protocolMapping>
  <add binding="String"
       bindingConfiguration="String"
       scheme="http/net.msmq/net.pipe/net.tcp" />
</protocolMapping>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="606e3-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="606e3-109">Attributes and Elements</span></span>  
 <span data-ttu-id="606e3-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="606e3-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="606e3-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="606e3-111">Attributes</span></span>  
  
|<span data-ttu-id="606e3-112">Élément</span><span class="sxs-lookup"><span data-stu-id="606e3-112">Element</span></span>|<span data-ttu-id="606e3-113">Description</span><span class="sxs-lookup"><span data-stu-id="606e3-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="606e3-114">liaison</span><span class="sxs-lookup"><span data-stu-id="606e3-114">binding</span></span>|<span data-ttu-id="606e3-115">Chaîne qui spécifie le type de liaison à utiliser pour un point de terminaison pendant la création de points de terminaison par défaut.</span><span class="sxs-lookup"><span data-stu-id="606e3-115">A string that specifies the type of binding to be used for an endpoint during default endpoint creation.</span></span>|  
|<span data-ttu-id="606e3-116">bindingConfiguration</span><span class="sxs-lookup"><span data-stu-id="606e3-116">bindingConfiguration</span></span>|<span data-ttu-id="606e3-117">Chaîne qui spécifie le nom de la section de configuration de liaison à référencer.</span><span class="sxs-lookup"><span data-stu-id="606e3-117">A string that specifies the name of the binding configuration section to be referenced.</span></span>|  
|<span data-ttu-id="606e3-118">scheme</span><span class="sxs-lookup"><span data-stu-id="606e3-118">scheme</span></span>|<span data-ttu-id="606e3-119">Schéma de protocole de transport à utiliser pour le point de terminaison par défaut.</span><span class="sxs-lookup"><span data-stu-id="606e3-119">The transport protocol scheme to be used for the default endpoint.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="606e3-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="606e3-120">Child Elements</span></span>  
 <span data-ttu-id="606e3-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="606e3-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="606e3-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="606e3-122">Parent Elements</span></span>  
  
|<span data-ttu-id="606e3-123">Élément</span><span class="sxs-lookup"><span data-stu-id="606e3-123">Element</span></span>|<span data-ttu-id="606e3-124">Description</span><span class="sxs-lookup"><span data-stu-id="606e3-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="606e3-125">\<protocolMapping></span><span class="sxs-lookup"><span data-stu-id="606e3-125">\<protocolMapping></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/protocolmapping.md)|<span data-ttu-id="606e3-126">Représente une section de configuration pour la définition des mappages de protocole par défaut entre les schémas de protocole de transport (par exemple, http, net.tcp, net.pipe, etc.) et des liaisons Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="606e3-126">Represents a configuration section for defining default protocol mappings between transport protocol schemes (e.g., http, net.tcp, net.pipe, etc.) and Windows Communication Foundation (WCF) bindings.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="606e3-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="606e3-127">Example</span></span>  
 <span data-ttu-id="606e3-128">L'exemple de configuration suivant montre le mappage de protocole par défaut dans le fichier machine.config.</span><span class="sxs-lookup"><span data-stu-id="606e3-128">The following configuration example shows the default protocol mapping in the machine.config file.</span></span> <span data-ttu-id="606e3-129">Vous pouvez remplacer ce mappage par défaut au niveau de l'ordinateur en modifiant le fichier machine.config.</span><span class="sxs-lookup"><span data-stu-id="606e3-129">You can override this default mapping at the machine level by modifying the machine.config file.</span></span> <span data-ttu-id="606e3-130">Ou, si vous souhaitez uniquement le remplacer dans la portée d'une application, vous pouvez remplacer cette section dans le fichier de configuration de votre application et modifier le mappage pour les schémas de protocole individuels.</span><span class="sxs-lookup"><span data-stu-id="606e3-130">Or if you would only like to override it within the scope of an application, you can override this section within your application configuration file and change the mapping for individual protocol schemes.</span></span>  
  
```xml  
<protocolMapping>
  <add scheme="http"
       binding="basicHttpBinding" />
  <add scheme="net.tcp"
       binding="netTcpBinding" />
  <add scheme="net.pipe"
       binding="netNamedPipeBinding" />
  <add scheme="net.msmq"
       binding="netMsmqBinding" />
</protocolMapping>
```  
  
## <a name="see-also"></a><span data-ttu-id="606e3-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="606e3-131">See also</span></span>

- <xref:System.ServiceModel.Configuration.ProtocolMappingSection?displayProperty=nameWithType>
- <xref:System.ServiceModel.Configuration.ProtocolMappingElement?displayProperty=nameWithType>
