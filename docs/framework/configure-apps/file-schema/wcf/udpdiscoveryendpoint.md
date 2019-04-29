---
title: <udpDiscoveryEndpoint>
ms.date: 03/30/2017
ms.assetid: 1f485329-2771-43bc-88de-df8f2faa3bb7
ms.openlocfilehash: 180763404ee9070e9ed6e5476d4568a0a018dcb3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61788152"
---
# <a name="udpdiscoveryendpoint"></a><span data-ttu-id="51590-101">\<udpDiscoveryEndpoint></span><span class="sxs-lookup"><span data-stu-id="51590-101">\<udpDiscoveryEndpoint></span></span>
<span data-ttu-id="51590-102">Cet élément de configuration définit un point de terminaison standard préconfiguré pour les opérations de découverte sur une liaison de multidiffusion UDP.</span><span class="sxs-lookup"><span data-stu-id="51590-102">This configuration element defines a standard endpoint that is pre-configured for discovery operations over a UDP multicast binding.</span></span> <span data-ttu-id="51590-103">Ce point de terminaison a un contrat fixe et prend en charge deux versions de protocole WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="51590-103">This endpoint has a fixed contract and supports two WS-Discovery protocol versions.</span></span> <span data-ttu-id="51590-104">De plus, il a une liaison UDP fixe et une valeur d’adresse par défaut indiquée dans les spécifications WS-Discovery (WS-Discovery Avril 2005 ou WS-Discovery V1.1).</span><span class="sxs-lookup"><span data-stu-id="51590-104">In addition, it has a fixed UDP binding and a default address as specified in the WS-Discovery specifications (WS-Discovery April 2005 or WS-Discovery V1.1).</span></span>  
  
 <span data-ttu-id="51590-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="51590-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="51590-106">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="51590-106">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="51590-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51590-107">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <discoveryEndpoint>
      <standardEndpoint discoveryMode="Adhoc/Managed"
                        discoveryVersion="WSDiscovery11/WSDiscoveryApril2005"
                        maxResponseDelay="Timespan"
                        multicastAddress="Uri"
                        name="String" />
    </discoveryEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="51590-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="51590-108">Attributes and Elements</span></span>  
 <span data-ttu-id="51590-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="51590-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="51590-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="51590-110">Attributes</span></span>  
  
|<span data-ttu-id="51590-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="51590-111">Attribute</span></span>|<span data-ttu-id="51590-112">Description</span><span class="sxs-lookup"><span data-stu-id="51590-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="51590-113">discoveryMode</span><span class="sxs-lookup"><span data-stu-id="51590-113">discoveryMode</span></span>|<span data-ttu-id="51590-114">Chaîne qui spécifie le mode de protocole de découverte.</span><span class="sxs-lookup"><span data-stu-id="51590-114">A string that specifies the mode of discovery protocol.</span></span> <span data-ttu-id="51590-115">Les valeurs valides sont « Ad hoc » et « Géré ».</span><span class="sxs-lookup"><span data-stu-id="51590-115">Valid values are "Adhoc" and "Managed".</span></span> <span data-ttu-id="51590-116">En mode managé, le protocole repose sur un proxy de découverte, qui fait office de référentiel des services détectables.</span><span class="sxs-lookup"><span data-stu-id="51590-116">In managed mode the protocol relies on a Discovery Proxy, which acts as a repository of Discoverable services.</span></span> <span data-ttu-id="51590-117">Le mode ad hoc nécessite que le protocole utilise le mécanisme de multidiffusion UDP pour rechercher les services disponibles.</span><span class="sxs-lookup"><span data-stu-id="51590-117">Adhoc mode requires the protocol to use UDP multicast mechanism to find available services.</span></span> <span data-ttu-id="51590-118">Cette valeur est de type <xref:System.ServiceModel.Discovery.ServiceDiscoveryMode>.</span><span class="sxs-lookup"><span data-stu-id="51590-118">This value is of type <xref:System.ServiceModel.Discovery.ServiceDiscoveryMode>.</span></span>|  
|<span data-ttu-id="51590-119">discoveryVersion</span><span class="sxs-lookup"><span data-stu-id="51590-119">discoveryVersion</span></span>|<span data-ttu-id="51590-120">Chaîne qui spécifie l'une des deux versions du protocole WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="51590-120">A string that specifies one of the two versions of WS-Discovery protocol.</span></span> <span data-ttu-id="51590-121">Les valeurs valides sont WSDiscovery11 et WSDiscoveryApril2005.</span><span class="sxs-lookup"><span data-stu-id="51590-121">Valid values are WSDiscovery11 and WSDiscoveryApril2005.</span></span> <span data-ttu-id="51590-122">Cette valeur est de type <xref:System.ServiceModel.Discovery.DiscoveryVersion>.</span><span class="sxs-lookup"><span data-stu-id="51590-122">This value is of type <xref:System.ServiceModel.Discovery.DiscoveryVersion>.</span></span>|  
|<span data-ttu-id="51590-123">maxResponseDelay</span><span class="sxs-lookup"><span data-stu-id="51590-123">maxResponseDelay</span></span>|<span data-ttu-id="51590-124">Valeur Timespan qui indique la valeur maximale du délai d'attente du protocole de découverte avant l'envoi de certains messages, tels que ceux de type Probe Match ou Resolve Match.</span><span class="sxs-lookup"><span data-stu-id="51590-124">A Timespan value that specifies the maximum value for the delay the Discovery protocol will wait before sending certain messages such as Probe Match or Resolve Match.</span></span><br /><br /> <span data-ttu-id="51590-125">Si tous les messages ProbeMatches sont envoyés en même temps, une tempête de réseau peut en résulter.</span><span class="sxs-lookup"><span data-stu-id="51590-125">If all ProbeMatches are sent at the same time, a network storm may result.</span></span> <span data-ttu-id="51590-126">Pour empêcher cet effet, les messages ProbeMatches sont envoyés avec un délai aléatoire entre chaque message ProbeMatch.</span><span class="sxs-lookup"><span data-stu-id="51590-126">To prevent this from occurring, ProbeMatches are sent with a random delay between each ProbeMatch.</span></span> <span data-ttu-id="51590-127">Le délai aléatoire est compris entre 0 et la valeur définie par cet attribut.</span><span class="sxs-lookup"><span data-stu-id="51590-127">The random delay is in the range of 0 to the value set by this attribute.</span></span> <span data-ttu-id="51590-128">Si l'attribut a la valeur 0, les messages ProbeMatches sont envoyés dans une boucle serrée sans délai.</span><span class="sxs-lookup"><span data-stu-id="51590-128">If this attribute is set to 0, then the ProbeMatches messages are sent in a tight loop without any delay.</span></span> <span data-ttu-id="51590-129">Sinon, les messages ProbeMatches sont envoyés avec un délai aléatoire de sorte que la durée totale nécessaire à l'envoi de tous les messages ProbeMatches ne dépasse pas le maxResponseDelay.</span><span class="sxs-lookup"><span data-stu-id="51590-129">Otherwise, the ProbeMatches messages are sent with some random delay such that the total time taken to send all ProbeMatches messages does not exceed the maxResponseDelay.</span></span> <span data-ttu-id="51590-130">Cette valeur est uniquement pertinente pour les services, elle n'est pas utilisée par les clients.</span><span class="sxs-lookup"><span data-stu-id="51590-130">This value is only relevant for services, it is not used by clients.</span></span>|  
|<span data-ttu-id="51590-131">multicastAddress</span><span class="sxs-lookup"><span data-stu-id="51590-131">multicastAddress</span></span>|<span data-ttu-id="51590-132">URI qui spécifie une adresse de multidiffusion à utiliser pour l'envoi et la réception des messages de découverte.</span><span class="sxs-lookup"><span data-stu-id="51590-132">A Uri that specifies a multicast address to use for sending and receiving the discovery messages.</span></span> <span data-ttu-id="51590-133">La valeur par défaut est représentée par l'adresse de multidiffusion conforme à la spécification du protocole.</span><span class="sxs-lookup"><span data-stu-id="51590-133">The default value is the multicast address as conformant to the protocol specification.</span></span>|  
|`name`|<span data-ttu-id="51590-134">Chaîne qui spécifie le nom de la configuration du point de terminaison standard.</span><span class="sxs-lookup"><span data-stu-id="51590-134">A String that specifies the name of the configuration of the standard endpoint.</span></span> <span data-ttu-id="51590-135">Le nom est utilisé dans l'attribut `endpointConfiguration` du point de terminaison de service pour lier un point de terminaison standard à sa configuration.</span><span class="sxs-lookup"><span data-stu-id="51590-135">The name is used in the `endpointConfiguration` attribute of the service endpoint to link a standard endpoint to its configuration.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="51590-136">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="51590-136">Child Elements</span></span>  
  
|<span data-ttu-id="51590-137">Élément</span><span class="sxs-lookup"><span data-stu-id="51590-137">Element</span></span>|<span data-ttu-id="51590-138">Description</span><span class="sxs-lookup"><span data-stu-id="51590-138">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="51590-139">\<udpTransportSettings></span><span class="sxs-lookup"><span data-stu-id="51590-139">\<udpTransportSettings></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/udptransportsettings.md)|<span data-ttu-id="51590-140">Collection de paramètres qui vous permettent de configurer le transport UDP pour le point de terminaison UDP.</span><span class="sxs-lookup"><span data-stu-id="51590-140">A collection of settings that allow you to configure UDP transport for the UDP endpoint.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="51590-141">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="51590-141">Parent Elements</span></span>  
  
|<span data-ttu-id="51590-142">Élément</span><span class="sxs-lookup"><span data-stu-id="51590-142">Element</span></span>|<span data-ttu-id="51590-143">Description</span><span class="sxs-lookup"><span data-stu-id="51590-143">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="51590-144">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="51590-144">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="51590-145">Collection de points de terminaison standard qui sont des points de terminaison prédéfinis dont une ou plusieurs propriétés (adresse, liaison, contrat) sont fixes.</span><span class="sxs-lookup"><span data-stu-id="51590-145">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="51590-146">Exemple</span><span class="sxs-lookup"><span data-stu-id="51590-146">Example</span></span>  
 <span data-ttu-id="51590-147">L'exemple suivant montre un service qui écoute des messages de découverte sur un transport de multidiffusion UDP.</span><span class="sxs-lookup"><span data-stu-id="51590-147">The following example demonstrates a service listening for discovery messages over a UDP multicast transport.</span></span>  
  
```xml  
<services>
  <service name="CalculatorService"
           behaviorConfiguration="CalculatorServiceBehavior">
    <endpoint binding="basicHttpBinding"
              address="calculator"
              contract="ICalculatorService" />
    <endpoint name="DiscoveryEndpoint"
              kind="udpDiscoveryEndpoint" />
  </service>
  <standardEndpoints>
    <udpDiscoveryEndpoint>
      <standardEndpoint name="DiscoveryEndpoint"
                        version="WSDiscoveryApril2005" />
    </udpDiscoveryEndpoint>
  </standardEndpoints>
</services>
```  
  
## <a name="see-also"></a><span data-ttu-id="51590-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51590-148">See also</span></span>

- <xref:System.ServiceModel.Discovery.DiscoveryEndpoint>
