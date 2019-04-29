---
title: 'Procédure : échanger des messages au sein d’une session fiable'
ms.date: 03/30/2017
ms.assetid: 87cd0e75-dd2c-44c1-8da0-7b494bbdeaea
ms.openlocfilehash: aad4eae870e3ba603c56a28a620fe8bc0e31ceb6
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61778363"
---
# <a name="how-to-exchange-messages-within-a-reliable-session"></a><span data-ttu-id="324c0-102">Procédure : échanger des messages au sein d’une session fiable</span><span class="sxs-lookup"><span data-stu-id="324c0-102">How to: Exchange Messages Within a Reliable Session</span></span>

<span data-ttu-id="324c0-103">Cette rubrique décrit les étapes requises pour activer une session fiable utilisant l’une des liaisons fournies par le système qui prennent en charge une telle session, mais pas par défaut.</span><span class="sxs-lookup"><span data-stu-id="324c0-103">This topic outlines the steps required to enable a reliable session using one of the system-provided bindings that support such a session, but not by default.</span></span> <span data-ttu-id="324c0-104">Vous activez une session fiable de façon impérative à l’aide de code ou de façon déclarative dans votre fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="324c0-104">You enable a reliable session imperatively using code or declaratively in your configuration file.</span></span> <span data-ttu-id="324c0-105">Cette procédure utilise les fichiers de configuration client et le service pour activer la session fiable et pour stipuler que les messages arrivent dans le même ordre que celui dans lequel ils ont été envoyés.</span><span class="sxs-lookup"><span data-stu-id="324c0-105">This procedure uses the client and service configuration files to enable the reliable session and to stipulate that the messages arrive in the same order in which they were sent.</span></span>

<span data-ttu-id="324c0-106">La partie clé de cette procédure est que l’élément de configuration de point de terminaison contiennent un `bindingConfiguration` attribut qui fait référence à une configuration de liaison nommée `Binding1`.</span><span class="sxs-lookup"><span data-stu-id="324c0-106">The key part of this procedure is that the endpoint configuration element contain a `bindingConfiguration` attribute that references a binding configuration named `Binding1`.</span></span> <span data-ttu-id="324c0-107">Le [  **\<liaison >** ](../../../../docs/framework/misc/binding.md) élément de configuration fait référence à ce nom pour activer les sessions fiables en définissant le `enabled` attribut de la [  **\<reliableSession >** ](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/ms731302(v=vs.100)) élément à `true`.</span><span class="sxs-lookup"><span data-stu-id="324c0-107">The [**\<binding>**](../../../../docs/framework/misc/binding.md) configuration element references this name to enable reliable sessions by setting the `enabled` attribute of the [**\<reliableSession>**](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/ms731302(v=vs.100)) element to `true`.</span></span> <span data-ttu-id="324c0-108">Vous spécifiez les assurances de remise ordonnée pour la session fiable en affectant à l'attribut `ordered` la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="324c0-108">You specify the ordered delivery assurances for the reliable session by setting the `ordered` attribute to `true`.</span></span>

<span data-ttu-id="324c0-109">Pour la copie de la source de cet exemple, consultez [Session fiable WS](../../../../docs/framework/wcf/samples/ws-reliable-session.md).</span><span class="sxs-lookup"><span data-stu-id="324c0-109">For the source copy of this example, see [WS Reliable Session](../../../../docs/framework/wcf/samples/ws-reliable-session.md).</span></span>

### <a name="configure-the-service-with-a-wshttpbinding-to-use-a-reliable-session"></a><span data-ttu-id="324c0-110">Configurer le service avec une liaison WSHttpBinding afin d’utiliser une session fiable</span><span class="sxs-lookup"><span data-stu-id="324c0-110">Configure the service with a WSHttpBinding to use a reliable session</span></span>

1. <span data-ttu-id="324c0-111">Définissez un contrat de service pour le type de service.</span><span class="sxs-lookup"><span data-stu-id="324c0-111">Define a service contract for the type of service.</span></span>

   [!code-csharp[c_HowTo_UseReliableSession#1121](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_usereliablesession/cs/service.cs#1121)]

1. <span data-ttu-id="324c0-112">Implémentez le contrat de service dans une classe de service.</span><span class="sxs-lookup"><span data-stu-id="324c0-112">Implement the service contract in a service class.</span></span> <span data-ttu-id="324c0-113">Notez que les informations de liaison ou d’adresse n’est pas spécifiées dans l’implémentation du service.</span><span class="sxs-lookup"><span data-stu-id="324c0-113">Note that the address or binding information isn't specified inside the implementation of the service.</span></span> <span data-ttu-id="324c0-114">Vous n’êtes pas obligé d’écrire du code pour extraire les informations de liaison ou d’adresse à partir du fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="324c0-114">You aren't required to write code to retrieve the address or binding information from the configuration file.</span></span>

   [!code-csharp[c_HowTo_UseReliableSession#1122](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_usereliablesession/cs/service.cs#1122)]

1. <span data-ttu-id="324c0-115">Créer un *Web.config* fichier pour configurer un point de terminaison pour le `CalculatorService` qui utilise le <xref:System.ServiceModel.WSHttpBinding> avec une session fiable activée et la livraison chronologique des messages requis.</span><span class="sxs-lookup"><span data-stu-id="324c0-115">Create a *Web.config* file to configure an endpoint for the `CalculatorService` that uses the <xref:System.ServiceModel.WSHttpBinding> with reliable session enabled and ordered delivery of messages required.</span></span>

   [!code-xml[c_HowTo_UseReliableSession#2111](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_usereliablesession/common/web.config#2111)]

1. <span data-ttu-id="324c0-116">Créer un *Service.svc* fichier qui contient la ligne :</span><span class="sxs-lookup"><span data-stu-id="324c0-116">Create a *Service.svc* file that contains the line:</span></span>

   ```
   <%@ServiceHost language=c# Service="CalculatorService" %>
   ```

1. <span data-ttu-id="324c0-117">Place le *Service.svc* fichier dans votre répertoire virtuel Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="324c0-117">Place the *Service.svc* file in your Internet Information Services (IIS) virtual directory.</span></span>

### <a name="configure-the-client-with-a-wshttpbinding-to-use-a-reliable-session"></a><span data-ttu-id="324c0-118">Configurer le client avec une liaison WSHttpBinding afin d’utiliser une session fiable</span><span class="sxs-lookup"><span data-stu-id="324c0-118">Configure the client with a WSHttpBinding to use a reliable session</span></span>

1. <span data-ttu-id="324c0-119">Utilisez le [ServiceModel Metadata Utility Tool (*Svcutil.exe*)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) à partir de la ligne de commande pour générer le code à partir des métadonnées de service :</span><span class="sxs-lookup"><span data-stu-id="324c0-119">Use the [ServiceModel Metadata Utility Tool (*Svcutil.exe*)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) from the command line to generate code from service metadata:</span></span>

   ```console
   Svcutil.exe <service's Metadata Exchange (MEX) address or HTTP GET address>
   ```

1. <span data-ttu-id="324c0-120">Le client généré contient la `ICalculator` interface qui définit le contrat de service que l’implémentation du client doit satisfaire.</span><span class="sxs-lookup"><span data-stu-id="324c0-120">The generated client contains the `ICalculator` interface that defines the service contract that the client implementation must satisfy.</span></span>

   [!code-csharp[C_HowTo_UseReliableSession#1221](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_usereliablesession/cs/client.cs#1221)]

1. <span data-ttu-id="324c0-121">L'application cliente générée contient également l'implémentation de `ClientCalculator`.</span><span class="sxs-lookup"><span data-stu-id="324c0-121">The generated client application also contains the implementation of the `ClientCalculator`.</span></span> <span data-ttu-id="324c0-122">Notez que les informations d’adresse et la liaison n’est pas spécifiées de n’importe où à l’intérieur de l’implémentation du service.</span><span class="sxs-lookup"><span data-stu-id="324c0-122">Note that the address and binding information isn't specified anywhere inside the implementation of the service.</span></span> <span data-ttu-id="324c0-123">Vous n’êtes pas obligé d’écrire du code pour extraire les informations de liaison ou d’adresse à partir du fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="324c0-123">You aren't required to write code to retrieve the address or binding information from the configuration file.</span></span>

   [!code-csharp[C_HowTo_UseReliableSession#1222](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_usereliablesession/cs/client.cs#1222)]

1. <span data-ttu-id="324c0-124">*SvcUtil.exe* génère également la configuration pour le client qui utilise le <xref:System.ServiceModel.WSHttpBinding> classe.</span><span class="sxs-lookup"><span data-stu-id="324c0-124">*Svcutil.exe* also generates the configuration for the client that uses the <xref:System.ServiceModel.WSHttpBinding> class.</span></span> <span data-ttu-id="324c0-125">Nommez le fichier de configuration *App.config* lors de l’utilisation de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="324c0-125">Name the configuration file *App.config* when using Visual Studio.</span></span>

   [!code-xml[C_HowTo_UseReliableSession#2211](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_usereliablesession/common/app.config#2211)]

1. <span data-ttu-id="324c0-126">Créez une instance de la `ClientCalculator` dans une application et appeler les opérations de service.</span><span class="sxs-lookup"><span data-stu-id="324c0-126">Create an instance of the `ClientCalculator` in an application and call the service operations.</span></span>

   [!code-csharp[C_HowTo_UseReliableSession#1223](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_usereliablesession/cs/client.cs#1223)]

1. <span data-ttu-id="324c0-127">Compilez, puis exécutez le client.</span><span class="sxs-lookup"><span data-stu-id="324c0-127">Compile and run the client.</span></span>

## <a name="example"></a><span data-ttu-id="324c0-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="324c0-128">Example</span></span>

<span data-ttu-id="324c0-129">Plusieurs liaisons fournies par le système prennent en charge des sessions fiables par défaut.</span><span class="sxs-lookup"><span data-stu-id="324c0-129">Several of the system-provided bindings support reliable sessions by default.</span></span> <span data-ttu-id="324c0-130">Elles incluent notamment :</span><span class="sxs-lookup"><span data-stu-id="324c0-130">These include:</span></span>

- <xref:System.ServiceModel.WSDualHttpBinding>

- <xref:System.ServiceModel.NetNamedPipeBinding>

- <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationBinding>

<span data-ttu-id="324c0-131">Pour obtenir un exemple montrant comment créer une liaison personnalisée qui prend en charge des sessions fiables, consultez [Comment : Créer une liaison de Session fiable personnalisée avec le protocole HTTPS](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-reliable-session-binding-with-https.md).</span><span class="sxs-lookup"><span data-stu-id="324c0-131">For an example of how to create a custom binding that supports reliable sessions, see [How to: Create a Custom Reliable Session Binding with HTTPS](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-reliable-session-binding-with-https.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="324c0-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="324c0-132">See also</span></span>

- [<span data-ttu-id="324c0-133">Sessions fiables</span><span class="sxs-lookup"><span data-stu-id="324c0-133">Reliable Sessions</span></span>](../../../../docs/framework/wcf/feature-details/reliable-sessions.md)
