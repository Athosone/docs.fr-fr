---
title: 'Procédure : créer un flux Atom de base'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 6e0cacc1-9b11-4665-adb7-577a62626fd6
ms.openlocfilehash: 11aa71f82af5a1bd764a4cc9e3514a795d559fc2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62000855"
---
# <a name="how-to-create-a-basic-atom-feed"></a><span data-ttu-id="910a9-102">Procédure : créer un flux Atom de base</span><span class="sxs-lookup"><span data-stu-id="910a9-102">How to: Create a Basic Atom Feed</span></span>
<span data-ttu-id="910a9-103">Windows Communication Foundation (WCF) vous permet de créer un service qui expose un flux de syndication.</span><span class="sxs-lookup"><span data-stu-id="910a9-103">Windows Communication Foundation (WCF) allows you to create a service that exposes a syndication feed.</span></span> <span data-ttu-id="910a9-104">Cette rubrique explique comment créer un service de syndication qui expose un flux de syndication Atom.</span><span class="sxs-lookup"><span data-stu-id="910a9-104">This topic discusses how to create a syndication service that exposes an Atom syndication feed.</span></span>  
  
### <a name="to-create-a-basic-syndication-service"></a><span data-ttu-id="910a9-105">Pour créer un service de syndication de base</span><span class="sxs-lookup"><span data-stu-id="910a9-105">To create a basic syndication service</span></span>  
  
1. <span data-ttu-id="910a9-106">Définissez un contrat de service utilisant une interface marquée avec l'attribut <xref:System.ServiceModel.Web.WebGetAttribute>.</span><span class="sxs-lookup"><span data-stu-id="910a9-106">Define a service contract using an interface marked with the <xref:System.ServiceModel.Web.WebGetAttribute> attribute.</span></span> <span data-ttu-id="910a9-107">Chaque opération exposée comme un flux de syndication doit retourner un objet <xref:System.ServiceModel.Syndication.Atom10FeedFormatter>.</span><span class="sxs-lookup"><span data-stu-id="910a9-107">Each operation that is exposed as a syndication feed should return a <xref:System.ServiceModel.Syndication.Atom10FeedFormatter> object.</span></span>  
  
     [!code-csharp[htAtomBasic#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/htatombasic/cs/program.cs#0)]
     [!code-vb[htAtomBasic#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htatombasic/vb/program.vb#0)]  
  
    > [!NOTE]
    >  <span data-ttu-id="910a9-108">Toutes les opérations du service qui appliquent <xref:System.ServiceModel.Web.WebGetAttribute> sont mappées aux demandes HTTP GET.</span><span class="sxs-lookup"><span data-stu-id="910a9-108">All service operations that apply the <xref:System.ServiceModel.Web.WebGetAttribute> are mapped to HTTP GET requests.</span></span> <span data-ttu-id="910a9-109">Pour mapper votre opération à une méthode HTTP différente, utilisez <xref:System.ServiceModel.Web.WebInvokeAttribute> à la place.</span><span class="sxs-lookup"><span data-stu-id="910a9-109">To map your operation to a different HTTP method, use the <xref:System.ServiceModel.Web.WebInvokeAttribute> instead.</span></span> <span data-ttu-id="910a9-110">Pour plus d'informations, voir [Procédure : Créer un Service Web HTTP de WCF de base](../../../../docs/framework/wcf/feature-details/how-to-create-a-basic-wcf-web-http-service.md).</span><span class="sxs-lookup"><span data-stu-id="910a9-110">For more information, see [How to: Create a Basic WCF Web HTTP Service](../../../../docs/framework/wcf/feature-details/how-to-create-a-basic-wcf-web-http-service.md).</span></span>  
  
2. <span data-ttu-id="910a9-111">Implémentez le contrat de service.</span><span class="sxs-lookup"><span data-stu-id="910a9-111">Implement the service contract.</span></span>  
  
     [!code-csharp[htAtomBasic#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/htatombasic/cs/program.cs#1)]
     [!code-vb[htAtomBasic#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htatombasic/vb/program.vb#1)]  
  
3. <span data-ttu-id="910a9-112">Créez un objet <xref:System.ServiceModel.Syndication.SyndicationFeed> et ajoutez un auteur, une catégorie et une description.</span><span class="sxs-lookup"><span data-stu-id="910a9-112">Create a <xref:System.ServiceModel.Syndication.SyndicationFeed> object and add an author, category, and description.</span></span>  
  
     [!code-csharp[htAtomBasic#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/htatombasic/cs/program.cs#2)]
     [!code-vb[htAtomBasic#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htatombasic/vb/program.vb#2)]  
  
4. <span data-ttu-id="910a9-113">Créez plusieurs objets <xref:System.ServiceModel.Syndication.SyndicationItem>.</span><span class="sxs-lookup"><span data-stu-id="910a9-113">Create several <xref:System.ServiceModel.Syndication.SyndicationItem> objects.</span></span>  
  
     [!code-csharp[htAtomBasic#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/htatombasic/cs/program.cs#3)]
     [!code-vb[htAtomBasic#3](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htatombasic/vb/program.vb#3)]  
  
5. <span data-ttu-id="910a9-114">Ajoutez les objets <xref:System.ServiceModel.Syndication.SyndicationItem> au flux.</span><span class="sxs-lookup"><span data-stu-id="910a9-114">Add the <xref:System.ServiceModel.Syndication.SyndicationItem> objects to the feed.</span></span>  
  
     [!code-csharp[htAtomBasic#4](../../../../samples/snippets/csharp/VS_Snippets_CFX/htatombasic/cs/program.cs#4)]
     [!code-vb[htAtomBasic#4](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htatombasic/vb/program.vb#4)]  
  
6. <span data-ttu-id="910a9-115">Retournez le flux.</span><span class="sxs-lookup"><span data-stu-id="910a9-115">Return the feed.</span></span>  
  
     [!code-csharp[htAtomBasic#5](../../../../samples/snippets/csharp/VS_Snippets_CFX/htatombasic/cs/program.cs#5)]
     [!code-vb[htAtomBasic#5](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htatombasic/vb/program.vb#5)]  
  
### <a name="to-host-the-service"></a><span data-ttu-id="910a9-116">Pour héberger le service</span><span class="sxs-lookup"><span data-stu-id="910a9-116">To host the service</span></span>  
  
1. <span data-ttu-id="910a9-117">Créez un objet <xref:System.ServiceModel.Web.WebServiceHost>.</span><span class="sxs-lookup"><span data-stu-id="910a9-117">Create a <xref:System.ServiceModel.Web.WebServiceHost> object.</span></span>  
  
     [!code-csharp[htAtomBasic#6](../../../../samples/snippets/csharp/VS_Snippets_CFX/htatombasic/cs/program.cs#6)]
     [!code-vb[htAtomBasic#6](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htatombasic/vb/program.vb#6)]  
  
2. <span data-ttu-id="910a9-118">Ouvrez l'hôte de service, chargez le flux à partir du service, affichez le flux et attendez que l'utilisateur appuie sur ENTRÉE.</span><span class="sxs-lookup"><span data-stu-id="910a9-118">Open the service host, load the feed from the service, display the feed, and wait for the user to press ENTER.</span></span>  
  
     [!code-csharp[htAtomBasic#8](../../../../samples/snippets/csharp/VS_Snippets_CFX/htatombasic/cs/program.cs#8)]
     [!code-vb[htAtomBasic#8](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htatombasic/vb/program.vb#8)]  
  
### <a name="to-call-getblog-with-an-http-get"></a><span data-ttu-id="910a9-119">Pour appeler GetBlog() avec un HTTP GET</span><span class="sxs-lookup"><span data-stu-id="910a9-119">To call GetBlog() with an HTTP GET</span></span>  
  
1. <span data-ttu-id="910a9-120">Ouvrez Internet Explorer, tapez l’URL suivante et appuyez sur ENTRÉE : `http://localhost:8000/BlogService/GetBlog`</span><span class="sxs-lookup"><span data-stu-id="910a9-120">Open Internet Explorer, type the following URL, and press ENTER: `http://localhost:8000/BlogService/GetBlog`</span></span>  
  
     <span data-ttu-id="910a9-121">L’URL contient l’adresse de base du service (`http://localhost:8000/BlogService`), l’adresse relative du point de terminaison et l’opération de service à appeler.</span><span class="sxs-lookup"><span data-stu-id="910a9-121">The URL contains the base address of the service (`http://localhost:8000/BlogService`), the relative address of the endpoint, and the service operation to call.</span></span>  
  
### <a name="to-call-getblog-from-code"></a><span data-ttu-id="910a9-122">Pour appeler GetBlog() à partir d'un code</span><span class="sxs-lookup"><span data-stu-id="910a9-122">To call GetBlog() from code</span></span>  
  
1. <span data-ttu-id="910a9-123">Créez un <xref:System.Xml.XmlReader> avec l'adresse de base et la méthode que vous appelez.</span><span class="sxs-lookup"><span data-stu-id="910a9-123">Create a <xref:System.Xml.XmlReader> with the base address and the method you are calling.</span></span>  
  
     [!code-csharp[htAtomBasic#9](../../../../samples/snippets/csharp/VS_Snippets_CFX/htatombasic/cs/snippets.cs#9)]
     [!code-vb[htAtomBasic#9](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htatombasic/vb/snippets.vb#9)]  
  
2. <span data-ttu-id="910a9-124">Appelez la méthode <xref:System.ServiceModel.Syndication.SyndicationFeed.Load%28System.Xml.XmlReader%29> statique, en passant dans le <xref:System.Xml.XmlReader> que vous venez de créer.</span><span class="sxs-lookup"><span data-stu-id="910a9-124">Call the static <xref:System.ServiceModel.Syndication.SyndicationFeed.Load%28System.Xml.XmlReader%29> method, passing in the <xref:System.Xml.XmlReader> you just created.</span></span>  
  
     [!code-csharp[htAtomBasic#10](../../../../samples/snippets/csharp/VS_Snippets_CFX/htatombasic/cs/snippets.cs#10)]
     [!code-vb[htAtomBasic#10](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htatombasic/vb/snippets.vb#10)]  
  
     <span data-ttu-id="910a9-125">Cela appelle l'opération de service et remplit un nouvel objet <xref:System.ServiceModel.Syndication.SyndicationFeed> avec le module de formatage retourné à partir de l'opération de service.</span><span class="sxs-lookup"><span data-stu-id="910a9-125">This invokes the service operation and populates a new <xref:System.ServiceModel.Syndication.SyndicationFeed> with the formatter returned from the service operation.</span></span>  
  
3. <span data-ttu-id="910a9-126">Accédez à l'objet de flux.</span><span class="sxs-lookup"><span data-stu-id="910a9-126">Access the feed object.</span></span>  
  
     [!code-csharp[htAtomBasic#11](../../../../samples/snippets/csharp/VS_Snippets_CFX/htatombasic/cs/snippets.cs#11)]
     [!code-vb[htAtomBasic#11](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htatombasic/vb/snippets.vb#11)]  
  
## <a name="example"></a><span data-ttu-id="910a9-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="910a9-127">Example</span></span>  
 <span data-ttu-id="910a9-128">Les éléments suivants représentent l'intégralité du code pour cet exemple.</span><span class="sxs-lookup"><span data-stu-id="910a9-128">The following is the full code listing for this example.</span></span>  
  
 [!code-csharp[htAtomBasic#12](../../../../samples/snippets/csharp/VS_Snippets_CFX/htatombasic/cs/program.cs#12)]
 [!code-vb[htAtomBasic#12](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htatombasic/vb/program.vb#12)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="910a9-129">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="910a9-129">Compiling the Code</span></span>  
 <span data-ttu-id="910a9-130">Lors de la compilation du code précédent, référencez System.ServiceModel.dll et System.ServiceModel.Web.dll.</span><span class="sxs-lookup"><span data-stu-id="910a9-130">When compiling the preceding code, reference System.ServiceModel.dll and System.ServiceModel.Web.dll.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="910a9-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="910a9-131">See also</span></span>

- <xref:System.ServiceModel.WebHttpBinding>
- <xref:System.ServiceModel.Web.WebGetAttribute>
