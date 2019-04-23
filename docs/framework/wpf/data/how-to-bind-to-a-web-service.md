---
title: 'Procédure : Effectuer une liaison à un service Web'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- binding data [WPF], Web service
- Web service binding [WPF]
- data binding [WPF], Web service
ms.assetid: 77e2d373-69ba-4cbd-b6f5-2c83c38fc98b
ms.openlocfilehash: 2c3bc1f2142f07aba3df2da6c46117d3907443a5
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59304985"
---
# <a name="how-to-bind-to-a-web-service"></a><span data-ttu-id="07aa7-102">Procédure : Effectuer une liaison à un service Web</span><span class="sxs-lookup"><span data-stu-id="07aa7-102">How to: Bind to a Web Service</span></span>
<span data-ttu-id="07aa7-103">Cet exemple montre comment lier des objets retournés par les appels de méthode de service Web.</span><span class="sxs-lookup"><span data-stu-id="07aa7-103">This example shows how to bind to objects returned by Web service method calls.</span></span>  
  
## <a name="example"></a><span data-ttu-id="07aa7-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="07aa7-104">Example</span></span>  
 <span data-ttu-id="07aa7-105">Cet exemple utilise le [MSDN/TechNet Publishing System (MTPS) Content Service](https://go.microsoft.com/fwlink/?LinkId=95677) pour récupérer la liste des langues prises en charge par un document spécifié.</span><span class="sxs-lookup"><span data-stu-id="07aa7-105">This example uses the [MSDN/TechNet Publishing System (MTPS) Content Service](https://go.microsoft.com/fwlink/?LinkId=95677) to retrieve the list of languages supported by a specified document.</span></span>  
  
 <span data-ttu-id="07aa7-106">Avant d’appeler un service Web, vous devez créer une référence à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="07aa7-106">Before you call a Web service, you need to create a reference to it.</span></span> <span data-ttu-id="07aa7-107">Pour créer une référence Web au service MTPS en utilisant [!INCLUDE[TLA#tla_visualstu](../../../../includes/tlasharptla-visualstu-md.md)], suivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="07aa7-107">To create a Web reference to the MTPS service using [!INCLUDE[TLA#tla_visualstu](../../../../includes/tlasharptla-visualstu-md.md)], follow the following steps:</span></span>  
  
1. <span data-ttu-id="07aa7-108">Ouvrez votre projet dans [!INCLUDE[TLA2#tla_visualstu](../../../../includes/tla2sharptla-visualstu-md.md)].</span><span class="sxs-lookup"><span data-stu-id="07aa7-108">Open your project in [!INCLUDE[TLA2#tla_visualstu](../../../../includes/tla2sharptla-visualstu-md.md)].</span></span>  
  
2. <span data-ttu-id="07aa7-109">À partir de la **projet** menu, cliquez sur **ajouter une référence Web**.</span><span class="sxs-lookup"><span data-stu-id="07aa7-109">From the **Project** menu, click **Add Web Reference**.</span></span>  
  
3. <span data-ttu-id="07aa7-110">Dans la boîte de dialogue, définissez la **URL** à [ http://services.msdn.microsoft.com/contentservices/contentservice.asmx?wsdl ](https://services.msdn.microsoft.com/contentservices/contentservice.asmx?wsdl).</span><span class="sxs-lookup"><span data-stu-id="07aa7-110">In the dialog box, set the **URL** to [http://services.msdn.microsoft.com/contentservices/contentservice.asmx?wsdl](https://services.msdn.microsoft.com/contentservices/contentservice.asmx?wsdl).</span></span>  
  
4. <span data-ttu-id="07aa7-111">Appuyez sur **accédez** , puis **ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="07aa7-111">Press **Go** and then **Add Reference**.</span></span>  
  
 <span data-ttu-id="07aa7-112">Ensuite, vous appelez la méthode de service Web et définir le <xref:System.Windows.FrameworkElement.DataContext%2A> de la fenêtre à l’objet retourné ou le contrôle approprié.</span><span class="sxs-lookup"><span data-stu-id="07aa7-112">Next, you call the Web service method and set the <xref:System.Windows.FrameworkElement.DataContext%2A> of the appropriate control or window to the returned object.</span></span> <span data-ttu-id="07aa7-113">Le **GetContent** méthode du service MTPS accepte une référence à la **getContentRequest** objet.</span><span class="sxs-lookup"><span data-stu-id="07aa7-113">The **GetContent** method of the MTPS service takes a reference to the **getContentRequest** object.</span></span> <span data-ttu-id="07aa7-114">Par conséquent, l’exemple suivant définit tout d’abord un objet de demande :</span><span class="sxs-lookup"><span data-stu-id="07aa7-114">Therefore, the following example first sets up a request object:</span></span>  
  
 [!code-csharp[BindToWebService#Namespace](~/samples/snippets/csharp/VS_Snippets_Wpf/BindToWebService/CSharp/Window1.xaml.cs#namespace)]
 [!code-vb[BindToWebService#Namespace](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BindToWebService/VisualBasic/Window1.xaml.vb#namespace)]  
[!code-csharp[BindToWebService#WebServiceCall](~/samples/snippets/csharp/VS_Snippets_Wpf/BindToWebService/CSharp/Window1.xaml.cs#webservicecall)]
[!code-vb[BindToWebService#WebServiceCall](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BindToWebService/VisualBasic/Window1.xaml.vb#webservicecall)]  
  
 <span data-ttu-id="07aa7-115">Après le <xref:System.Windows.FrameworkElement.DataContext%2A> a été défini, vous pouvez créer des liaisons pour les propriétés de l’objet qui le <xref:System.Windows.FrameworkElement.DataContext%2A> a été défini sur.</span><span class="sxs-lookup"><span data-stu-id="07aa7-115">After the <xref:System.Windows.FrameworkElement.DataContext%2A> has been set, you can create bindings to the properties of the object that the <xref:System.Windows.FrameworkElement.DataContext%2A> has been set to.</span></span> <span data-ttu-id="07aa7-116">Dans cet exemple, le <xref:System.Windows.FrameworkElement.DataContext%2A> est défini sur le **getContentResponse** objet retourné par la **GetContent** (méthode).</span><span class="sxs-lookup"><span data-stu-id="07aa7-116">In this example, the <xref:System.Windows.FrameworkElement.DataContext%2A> is set to the **getContentResponse** object returned by the **GetContent** method.</span></span> <span data-ttu-id="07aa7-117">Dans l’exemple suivant, le <xref:System.Windows.Controls.ItemsControl> et les affiche le **paramètres régionaux** les valeurs de **availableVersionsAndLocales** de **getContentResponse**.</span><span class="sxs-lookup"><span data-stu-id="07aa7-117">In the following example, the <xref:System.Windows.Controls.ItemsControl> binds to and displays the **locale** values of **availableVersionsAndLocales** of **getContentResponse**.</span></span>  
  
 [!code-xaml[BindToWebService#Binding](~/samples/snippets/csharp/VS_Snippets_Wpf/BindToWebService/CSharp/Window1.xaml#binding)]  
  
 <span data-ttu-id="07aa7-118">Pour plus d’informations sur la structure des **getContentResponse**, consultez [Content Service documentation](https://services.msdn.microsoft.com/ContentServices/ContentService.asmx).</span><span class="sxs-lookup"><span data-stu-id="07aa7-118">For information about the structure of **getContentResponse**, see [Content Service documentation](https://services.msdn.microsoft.com/ContentServices/ContentService.asmx).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="07aa7-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07aa7-119">See also</span></span>

- [<span data-ttu-id="07aa7-120">Vue d’ensemble de la liaison de données</span><span class="sxs-lookup"><span data-stu-id="07aa7-120">Data Binding Overview</span></span>](data-binding-overview.md)
- [<span data-ttu-id="07aa7-121">Vue d'ensemble des sources de liaison</span><span class="sxs-lookup"><span data-stu-id="07aa7-121">Binding Sources Overview</span></span>](binding-sources-overview.md)
- [<span data-ttu-id="07aa7-122">Rendre des données disponibles pour la liaison en XAML</span><span class="sxs-lookup"><span data-stu-id="07aa7-122">Make Data Available for Binding in XAML</span></span>](how-to-make-data-available-for-binding-in-xaml.md)
