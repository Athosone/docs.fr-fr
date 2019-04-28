---
title: Services duplex
ms.date: 05/09/2018
dev_langs:
- csharp
- vb
ms.assetid: 396b875a-d203-4ebe-a3a1-6a330d962e95
ms.openlocfilehash: 33cfcb765b93309d365a85e679107405a55a91f9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61858037"
---
# <a name="duplex-services"></a><span data-ttu-id="5ad7c-102">Services duplex</span><span class="sxs-lookup"><span data-stu-id="5ad7c-102">Duplex Services</span></span>

<span data-ttu-id="5ad7c-103">Un contrat de service duplex est un modèle d'échange de messages dans lequel les deux points de terminaison peuvent envoyer indépendamment des messages à l'autre.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-103">A duplex service contract is a message exchange pattern in which both endpoints can send messages to the other independently.</span></span> <span data-ttu-id="5ad7c-104">Un service duplex peut, par conséquent, renvoyer des messages au point de terminaison client, en fournissant un comportement de type événement.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-104">A duplex service, therefore, can send messages back to the client endpoint, providing event-like behavior.</span></span> <span data-ttu-id="5ad7c-105">La communication duplex se produit lorsqu'un client se connecte à un service et lui fournit un canal sur lequel il peut lui renvoyer des messages.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-105">Duplex communication occurs when a client connects to a service and provides the service with a channel on which the service can send messages back to the client.</span></span> <span data-ttu-id="5ad7c-106">Notez que le comportement de type événement des services duplex ne fonctionne que dans une session.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-106">Note that the event-like behavior of duplex services only works within a session.</span></span>

<span data-ttu-id="5ad7c-107">Pour créer un contrat duplex, créez une paire d'interfaces.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-107">To create a duplex contract you create a pair of interfaces.</span></span> <span data-ttu-id="5ad7c-108">La première est l'interface de contrat de service qui décrit les opérations qu'un client peut appeler.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-108">The first is the service contract interface that describes the operations that a client can invoke.</span></span> <span data-ttu-id="5ad7c-109">Ce contrat de service doit spécifier un *contrat de rappel* dans le <xref:System.ServiceModel.ServiceContractAttribute.CallbackContract%2A?displayProperty=nameWithType> propriété.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-109">That service contract must specify a *callback contract* in the <xref:System.ServiceModel.ServiceContractAttribute.CallbackContract%2A?displayProperty=nameWithType> property.</span></span> <span data-ttu-id="5ad7c-110">Le contrat de rappel est l'interface qui définit les opérations que le service peut appeler sur le point de terminaison client.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-110">The callback contract is the interface that defines the operations that the service can call on the client endpoint.</span></span> <span data-ttu-id="5ad7c-111">Un contrat duplex ne requiert pas de session, bien que les liaisons duplex fournies par le système en utilisent.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-111">A duplex contract does not require a session, although the system-provided duplex bindings make use of them.</span></span>

<span data-ttu-id="5ad7c-112">Voici un exemple de contrat duplex :</span><span class="sxs-lookup"><span data-stu-id="5ad7c-112">The following is an example of a duplex contract.</span></span>

[!code-csharp[c_DuplexServices#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_duplexservices/cs/service.cs#0)]
[!code-vb[c_DuplexServices#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_duplexservices/vb/service.vb#0)]

<span data-ttu-id="5ad7c-113">La classe `CalculatorService` implémente l'interface `ICalculatorDuplex` principale.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-113">The `CalculatorService` class implements the primary `ICalculatorDuplex` interface.</span></span> <span data-ttu-id="5ad7c-114">Le service utilise le mode d'instance <xref:System.ServiceModel.InstanceContextMode.PerSession> pour conserver le résultat de chaque session.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-114">The service uses the <xref:System.ServiceModel.InstanceContextMode.PerSession> instance mode to maintain the result for each session.</span></span> <span data-ttu-id="5ad7c-115">Une propriété privée appelée `Callback` accède au canal de rappel au client.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-115">A private property named `Callback` accesses the callback channel to the client.</span></span> <span data-ttu-id="5ad7c-116">Le service utilise le rappel pour renvoyer des messages au client via l'interface de rappel, comme le montre l'exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-116">The service uses the callback for sending messages back to the client through the callback interface, as shown in the following sample code.</span></span>

[!code-csharp[c_DuplexServices#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_duplexservices/cs/service.cs#1)]
[!code-vb[c_DuplexServices#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_duplexservices/vb/service.vb#1)]

<span data-ttu-id="5ad7c-117">Le client doit fournir une classe qui implémente l'interface de rappel du contrat duplex pour permettre la réception des messages envoyés par le service.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-117">The client must provide a class that implements the callback interface of the duplex contract, for receiving messages from the service.</span></span> <span data-ttu-id="5ad7c-118">L'exemple de code suivant présente une classe `CallbackHandler` qui implémente l'interface `ICalculatorDuplexCallback`.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-118">The following sample code shows a `CallbackHandler` class that implements the `ICalculatorDuplexCallback` interface.</span></span>

[!code-csharp[c_DuplexServices#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_duplexservices/cs/client.cs#2)]
[!code-vb[c_DuplexServices#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_duplexservices/vb/client.vb#2)]

<span data-ttu-id="5ad7c-119">Le client WCF généré pour un contrat duplex requiert une <xref:System.ServiceModel.InstanceContext> classe doit être fourni lors de sa création.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-119">The WCF client that is generated for a duplex contract requires a <xref:System.ServiceModel.InstanceContext> class to be provided upon construction.</span></span> <span data-ttu-id="5ad7c-120">Cette classe <xref:System.ServiceModel.InstanceContext> est utilisée comme site pour un objet qui implémente l'interface de rappel et gère les messages renvoyés à partir du service.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-120">This <xref:System.ServiceModel.InstanceContext> class is used as the site for an object that implements the callback interface and handles messages that are sent back from the service.</span></span> <span data-ttu-id="5ad7c-121">Une classe <xref:System.ServiceModel.InstanceContext> est construite avec une instance de la classe `CallbackHandler`.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-121">An <xref:System.ServiceModel.InstanceContext> class is constructed with an instance of the `CallbackHandler` class.</span></span> <span data-ttu-id="5ad7c-122">Cet objet gère les messages envoyés par le service au client sur l'interface de rappel.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-122">This object handles messages sent from the service to the client on the callback interface.</span></span>

[!code-csharp[c_DuplexServices#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_duplexservices/cs/client.cs#3)]
[!code-vb[c_DuplexServices#3](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_duplexservices/vb/client.vb#3)]

<span data-ttu-id="5ad7c-123">La configuration pour le service doit être installée pour fournir une liaison prenant à la fois en charge la communication de session et la communication duplex.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-123">The configuration for the service must be set up to provide a binding that supports both session communication and duplex communication.</span></span> <span data-ttu-id="5ad7c-124">L'élément `wsDualHttpBinding` prend en charge la communication de session et permet la communication duplex en fournissant des connexions HTTP doubles, à raison d'une pour chaque direction.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-124">The `wsDualHttpBinding` element supports session communication and allows duplex communication by providing dual HTTP connections, one for each direction.</span></span>

<span data-ttu-id="5ad7c-125">Sur le client, vous devez configurer une adresse que le serveur peut utiliser afin de s'y connecter, tel qu'indiqué dans l'exemple de configuration suivant.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-125">On the client, you must configure an address that the server can use to connect to the client, as shown in the following sample configuration.</span></span>

> [!NOTE]
> <span data-ttu-id="5ad7c-126">Les clients non duplex qui ne parviennent pas à s'authentifier à l'aide d'une conversation sécurisée lèvent en général une exception <xref:System.ServiceModel.Security.MessageSecurityException>.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-126">Non-duplex clients that fail to authenticate using a secure conversation typically throw a <xref:System.ServiceModel.Security.MessageSecurityException>.</span></span> <span data-ttu-id="5ad7c-127">Toutefois, si un client duplex qui utilise une conversation sécurisée ne parvient pas à s'authentifier, il reçoit à la place une exception <xref:System.TimeoutException>.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-127">However, if a duplex client that uses a secure conversation fails to authenticate, the client receives a <xref:System.TimeoutException> instead.</span></span>

<span data-ttu-id="5ad7c-128">Si vous créez un client/service à l'aide de l'élément `WSHttpBinding` et que vous n'incluez pas le point de terminaison de rappel client, vous recevrez l'erreur suivante.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-128">If you create a client/service using the `WSHttpBinding` element and you do not include the client callback endpoint, you will receive the following error.</span></span>

```
HTTP could not register URL
htp://+:80/Temporary_Listen_Addresses/<guid> because TCP port 80 is being used by another application.
```

<span data-ttu-id="5ad7c-129">L’exemple de code suivant montre comment spécifier le client adresse de point de terminaison par programme.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-129">The following sample code shows how to specify the client endpoint address programmatically.</span></span>

```csharp
WSDualHttpBinding binding = new WSDualHttpBinding();
EndpointAddress endptadr = new EndpointAddress("http://localhost:12000/DuplexTestUsingCode/Server");
binding.ClientBaseAddress = new Uri("http://localhost:8000/DuplexTestUsingCode/Client/");
```

```vb
Dim binding As New WSDualHttpBinding()
Dim endptadr As New EndpointAddress("http://localhost:12000/DuplexTestUsingCode/Server")
binding.ClientBaseAddress = New Uri("http://localhost:8000/DuplexTestUsingCode/Client/")
```

<span data-ttu-id="5ad7c-130">L'exemple de code suivant indique comment spécifier l'adresse de point de terminaison client dans la configuration.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-130">The following sample code shows how to specify the client endpoint address in configuration.</span></span>

```xml
<client>
    <endpoint name ="ServerEndpoint"
          address="http://localhost:12000/DuplexTestUsingConfig/Server"
          bindingConfiguration="WSDualHttpBinding_IDuplexTest"
            binding="wsDualHttpBinding"
           contract="IDuplexTest" />
</client>
<bindings>
    <wsDualHttpBinding>
        <binding name="WSDualHttpBinding_IDuplexTest"
          clientBaseAddress="http://localhost:8000/myClient/" >
            <security mode="None"/>
         </binding>
    </wsDualHttpBinding>
</bindings>
```

> [!WARNING]
> <span data-ttu-id="5ad7c-131">Le model duplex ne détecte pas automatiquement si un service ou un client ferme son canal.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-131">The duplex model does not automatically detect when a service or client closes its channel.</span></span> <span data-ttu-id="5ad7c-132">Par conséquent, si un client se ferme de façon inattendue, par défaut le service n'est pas notifié ; il en est de même pour un client qui se ferme de façon inattendue.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-132">So if a client unexpectedly terminates, by default the service will not be notified, or if a client unexpectedly terminates, the service will not be notified.</span></span> <span data-ttu-id="5ad7c-133">Les clients et les services peuvent implémenter leur propre protocole pour se notifier mutuellement s'ils le souhaitent.</span><span class="sxs-lookup"><span data-stu-id="5ad7c-133">Clients and services can implement their own protocol to notify each other if they so choose.</span></span>

## <a name="see-also"></a><span data-ttu-id="5ad7c-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ad7c-134">See also</span></span>

- [<span data-ttu-id="5ad7c-135">Duplex</span><span class="sxs-lookup"><span data-stu-id="5ad7c-135">Duplex</span></span>](../../../../docs/framework/wcf/samples/duplex.md)
- [<span data-ttu-id="5ad7c-136">Spécification du comportement du client au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="5ad7c-136">Specifying Client Run-Time Behavior</span></span>](../../../../docs/framework/wcf/specifying-client-run-time-behavior.md)
- [<span data-ttu-id="5ad7c-137">Guide pratique pour Créer une fabrique de canal et l’utiliser pour créer et gérer des canaux</span><span class="sxs-lookup"><span data-stu-id="5ad7c-137">How to: Create a Channel Factory and Use it to Create and Manage Channels</span></span>](../../../../docs/framework/wcf/feature-details/how-to-create-a-channel-factory-and-use-it-to-create-and-manage-channels.md)
