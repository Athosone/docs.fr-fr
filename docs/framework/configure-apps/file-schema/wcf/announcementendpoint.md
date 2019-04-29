---
title: <announcementEndpoint>
ms.date: 03/30/2017
ms.assetid: 034b7c69-a770-4502-8cef-38007bbcd025
ms.openlocfilehash: 4f3cf2748acc75b0ec83732664c5f97114f3663a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61701253"
---
# <a name="announcementendpoint"></a><span data-ttu-id="25d76-101">\<announcementEndpoint></span><span class="sxs-lookup"><span data-stu-id="25d76-101">\<announcementEndpoint></span></span>
<span data-ttu-id="25d76-102">Cet élément de configuration définit un point de terminaison standard avec un contrat d'annonce fixe.</span><span class="sxs-lookup"><span data-stu-id="25d76-102">This configuration element defines a standard endpoint with a fixed announcement contract.</span></span> <span data-ttu-id="25d76-103">Un service peut éventuellement annoncer sa disponibilité en envoyant un message d'annonce en ligne ou hors connexion selon qu'il est respectivement ouvert ou fermé.</span><span class="sxs-lookup"><span data-stu-id="25d76-103">A service can optionally announce its availability by sending an online and offline announcement message when it is opened or closed respectively.</span></span> <span data-ttu-id="25d76-104">Un service Windows Communication Foundation (WCF) spécifie les points de terminaison d’annonce dans le [ \<serviceDiscovery >](../../../../../docs/framework/configure-apps/file-schema/wcf/servicediscovery.md) élément et utilise AnnouncementClient pour effectuer les annonces.</span><span class="sxs-lookup"><span data-stu-id="25d76-104">A Windows Communication Foundation (WCF) service specifies the announcement endpoints in the [\<serviceDiscovery>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicediscovery.md) element and uses the AnnouncementClient to perform the announcements.</span></span> <span data-ttu-id="25d76-105">Un client souhaite écouter pour l’annonce provenant d’un autre service joue en fait un service WCF ; Par conséquent, vous devez configurer les points de terminaison d’annonce pour ce client dans le [ \<services >](../../../../../docs/framework/configure-apps/file-schema/wcf/services.md) section.</span><span class="sxs-lookup"><span data-stu-id="25d76-105">A client wishing to listen for the announcement from other service is actually acting as a WCF service; thus you have to configure the announcement endpoints for that client in the [\<services>](../../../../../docs/framework/configure-apps/file-schema/wcf/services.md) section.</span></span>  
  
<span data-ttu-id="25d76-106">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="25d76-106">\<system.ServiceModel></span></span>  
<span data-ttu-id="25d76-107">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="25d76-107">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="25d76-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25d76-108">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <announcementEndpoint>
      <standardEndpoint discoveryVersion="WSDiscovery11/WSDiscoveryApril2005"
                        maxAnnouncementDelay="Timespan"
                        name="String" />
    </announcementEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="25d76-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="25d76-109">Attributes and Elements</span></span>  
 <span data-ttu-id="25d76-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="25d76-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="25d76-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="25d76-111">Attributes</span></span>  
  
|<span data-ttu-id="25d76-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="25d76-112">Attribute</span></span>|<span data-ttu-id="25d76-113">Description</span><span class="sxs-lookup"><span data-stu-id="25d76-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="25d76-114">discoveryVersion</span><span class="sxs-lookup"><span data-stu-id="25d76-114">discoveryVersion</span></span>|<span data-ttu-id="25d76-115">Chaîne qui spécifie l'une des deux versions du protocole WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="25d76-115">A string that specifies one of the two versions of WS-Discovery protocol.</span></span> <span data-ttu-id="25d76-116">Les valeurs valides sont WSDiscovery11 et WSDiscoveryApril2005.</span><span class="sxs-lookup"><span data-stu-id="25d76-116">Valid values are WSDiscovery11 and WSDiscoveryApril2005.</span></span> <span data-ttu-id="25d76-117">Cette valeur est de type <xref:System.ServiceModel.Discovery.Configuration.AnnouncementEndpointElement.DiscoveryVersion>.</span><span class="sxs-lookup"><span data-stu-id="25d76-117">This value is of type <xref:System.ServiceModel.Discovery.Configuration.AnnouncementEndpointElement.DiscoveryVersion>.</span></span>|  
|<span data-ttu-id="25d76-118">maxAnnouncementDelay</span><span class="sxs-lookup"><span data-stu-id="25d76-118">maxAnnouncementDelay</span></span>|<span data-ttu-id="25d76-119">Valeur Timespan qui spécifie le délai d'attente maximal du protocole de découverte avant l'envoi d'un message de type Hello.</span><span class="sxs-lookup"><span data-stu-id="25d76-119">A Timespan value that specifies the maximum value for the delay the Discovery protocol will wait before sending a Hello message.</span></span> <span data-ttu-id="25d76-120">Les messages attendent pendant un délai aléatoire compris entre 0 et la valeur de cet attribut avant d'être envoyés.</span><span class="sxs-lookup"><span data-stu-id="25d76-120">The messages will wait for a random time value between 0 and the value of this attribute before being sent.</span></span> <span data-ttu-id="25d76-121">Cet attribut permet de définir un délai court et aléatoire pour empêcher toute tempête de réseau lorsqu'un réseau est en panne et que tous les services reviennent en ligne en même temps.</span><span class="sxs-lookup"><span data-stu-id="25d76-121">This attribute is used to set a small, random delay to prevent network storms when a network goes out and all services come back online at the same time.</span></span>|  
|<span data-ttu-id="25d76-122">name</span><span class="sxs-lookup"><span data-stu-id="25d76-122">name</span></span>|<span data-ttu-id="25d76-123">Chaîne qui spécifie le nom de la configuration du point de terminaison standard.</span><span class="sxs-lookup"><span data-stu-id="25d76-123">A String that specifies the name of the configuration of the standard endpoint.</span></span> <span data-ttu-id="25d76-124">Le nom est utilisé dans l'attribut `endpointConfiguration` du point de terminaison de service pour lier un point de terminaison standard à sa configuration.</span><span class="sxs-lookup"><span data-stu-id="25d76-124">The name is used in the `endpointConfiguration` attribute of the service endpoint to link a standard endpoint to its configuration.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="25d76-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="25d76-125">Child Elements</span></span>  
 <span data-ttu-id="25d76-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="25d76-126">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="25d76-127">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="25d76-127">Parent Elements</span></span>  
  
|<span data-ttu-id="25d76-128">Élément</span><span class="sxs-lookup"><span data-stu-id="25d76-128">Element</span></span>|<span data-ttu-id="25d76-129">Description</span><span class="sxs-lookup"><span data-stu-id="25d76-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="25d76-130">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="25d76-130">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="25d76-131">Collection de points de terminaison standard qui sont des points de terminaison prédéfinis dont une ou plusieurs propriétés (adresse, liaison, contrat) sont fixes.</span><span class="sxs-lookup"><span data-stu-id="25d76-131">A collection of standard endpoints that are pre-defined endpoints with one or more of their properties (address, binding, contract) fixed.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="25d76-132">Exemple</span><span class="sxs-lookup"><span data-stu-id="25d76-132">Example</span></span>  
 <span data-ttu-id="25d76-133">L'exemple suivant montre un client qui écoute des messages d'annonce sur HTTP et Peernet.</span><span class="sxs-lookup"><span data-stu-id="25d76-133">The following example demonstrates a client listening for announcements messages over http and peernet.</span></span>  
  
```xml  
<services>
  <service name="ServiceAnnouncementListener">
    <endpoint name="httpAnnouncementEndpoint"
              kind="announcementEndpoint"
              binding="basicHttpBinding"
              address="announcements" />
    <endpoint name="peerNetAnnouncementEndpoint"
              kind="announcementEndpoint"
              binding="peerTcpBinding"
              address="net.p2p://discoveryMesh/multicast"
              bindingConfiguration="discoveryPeerTcpBindingConfig" />
  ...
  </service>
</services>

<standardEndpoints>
  <announcementEndpoint>
    <standardEndpoint name="httpAnnouncementEndpoint"
                      version="WSDiscoveryApril2005" />
    <standardEndpoint name="peerNetAnnouncementEndpoint"
                      version="WSDiscoveryApril2005" />
  </announcementEndpoint>
</standardEndpoints>
```  
  
## <a name="see-also"></a><span data-ttu-id="25d76-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25d76-134">See also</span></span>

- <xref:System.ServiceModel.Discovery.AnnouncementEndpoint>
