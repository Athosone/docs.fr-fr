---
title: 'Procédure : Orner les enfants d’un panneau'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- adorners [WPF], binding to children of Panels
- Panel control [WPF], binding adorners to children
ms.assetid: 4cc9b972-b472-4e5c-bdf3-3702d7fbb1f5
ms.openlocfilehash: 746f197a5132934f94a678dc3b5e2a1f65eb93bd
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62019020"
---
# <a name="how-to-adorn-the-children-of-a-panel"></a><span data-ttu-id="32a92-102">Procédure : Orner les enfants d’un panneau</span><span class="sxs-lookup"><span data-stu-id="32a92-102">How to: Adorn the Children of a Panel</span></span>
<span data-ttu-id="32a92-103">Cet exemple montre comment lier par programmation un ornement aux enfants d’une certaine <xref:System.Windows.Controls.Panel>.</span><span class="sxs-lookup"><span data-stu-id="32a92-103">This example shows how to programmatically bind an adorner to the children of a specified <xref:System.Windows.Controls.Panel>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="32a92-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="32a92-104">Example</span></span>  
 <span data-ttu-id="32a92-105">Pour lier un ornement aux enfants d’un <xref:System.Windows.Controls.Panel>, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="32a92-105">To bind an adorner to the children of a <xref:System.Windows.Controls.Panel>, follow these steps:</span></span>  
  
1. <span data-ttu-id="32a92-106">Déclarez un nouveau <xref:System.Windows.Documents.AdornerLayer> objet et appelez le `static` <xref:System.Windows.Documents.AdornerLayer.GetAdornerLayer%2A> méthode pour rechercher une couche d’ornement pour l’élément dont les enfants doivent être ornés.</span><span class="sxs-lookup"><span data-stu-id="32a92-106">Declare a new <xref:System.Windows.Documents.AdornerLayer> object and call the `static`<xref:System.Windows.Documents.AdornerLayer.GetAdornerLayer%2A> method to find an adorner layer for the element whose children are to be adorned.</span></span>  
  
2. <span data-ttu-id="32a92-107">Énumérez les enfants de l’élément parent et appelez le <xref:System.Windows.Documents.AdornerLayer.Add%2A> méthode pour lier un ornement à chaque élément enfant.</span><span class="sxs-lookup"><span data-stu-id="32a92-107">Enumerate through the children of the parent element and call the <xref:System.Windows.Documents.AdornerLayer.Add%2A> method to bind an adorner to each child element.</span></span>  
  
 <span data-ttu-id="32a92-108">L’exemple suivant lie un SimpleCircleAdorner (illustré ci-dessus) aux enfants d’un <xref:System.Windows.Controls.StackPanel> nommé *myStackPanel*.</span><span class="sxs-lookup"><span data-stu-id="32a92-108">The following example binds a SimpleCircleAdorner (shown above) to the children of a <xref:System.Windows.Controls.StackPanel> named *myStackPanel*.</span></span>  
  
 [!code-csharp[Adorners_SimpleCircleAdorner#_AdornChildren](~/samples/snippets/csharp/VS_Snippets_Wpf/Adorners_SimpleCircleAdorner/CSharp/Window1.xaml.cs#_adornchildren)]
 [!code-vb[Adorners_SimpleCircleAdorner#_AdornChildren](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Adorners_SimpleCircleAdorner/VisualBasic/Window1.xaml.vb#_adornchildren)]  
  
> [!NOTE]
>  <span data-ttu-id="32a92-109">L’utilisation du [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] pour lier un ornement à un autre élément n’est pas prise en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="32a92-109">Using [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] to bind an adorner to another element is currently not supported.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="32a92-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32a92-110">See also</span></span>

- [<span data-ttu-id="32a92-111">Vue d’ensemble des ornements</span><span class="sxs-lookup"><span data-stu-id="32a92-111">Adorners Overview</span></span>](adorners-overview.md)
