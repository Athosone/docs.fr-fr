---
title: 'Procédure : Substituer la méthode OnRender de Panel'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
f1_keywords:
- overriding OnRender method
- Panel control, overriding OnRender method
- OnRender method
- controls, Panel, overriding OnRender method
helpviewer_keywords:
- overriding OnRender method of Panel control [WPF]
- OnRender method [WPF], overriding
- Panel control [WPF], overriding OnRender method
ms.assetid: 57397834-a085-4e36-90ab-416fad98f341
ms.openlocfilehash: c4539847368c1a5789e99ec92106d17077ed5943
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61770836"
---
# <a name="how-to-override-the-panel-onrender-method"></a><span data-ttu-id="63346-102">Procédure : Substituer la méthode OnRender de Panel</span><span class="sxs-lookup"><span data-stu-id="63346-102">How to: Override the Panel OnRender Method</span></span>
<span data-ttu-id="63346-103">Cet exemple montre comment substituer la <xref:System.Windows.Controls.Panel.OnRender%2A> méthode de <xref:System.Windows.Controls.Panel> afin d’ajouter des effets graphiques personnalisés à un élément de disposition.</span><span class="sxs-lookup"><span data-stu-id="63346-103">This example shows how to override the <xref:System.Windows.Controls.Panel.OnRender%2A> method of <xref:System.Windows.Controls.Panel> in order to add custom graphical effects to a layout element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="63346-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="63346-104">Example</span></span>  
 <span data-ttu-id="63346-105">Utilisez le <xref:System.Windows.Controls.Panel.OnRender%2A> méthode afin d’ajouter des effets graphiques à un élément de panneau rendu.</span><span class="sxs-lookup"><span data-stu-id="63346-105">Use the <xref:System.Windows.Controls.Panel.OnRender%2A> method in order to add graphical effects to a rendered panel element.</span></span> <span data-ttu-id="63346-106">Par exemple, vous pouvez utiliser cette méthode pour ajouter une bordure personnalisée ou des effets d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="63346-106">For example, you can use this method to add custom border or background effects.</span></span> <span data-ttu-id="63346-107">Un <xref:System.Windows.Media.DrawingContext> objet est passé en tant qu’argument, qui fournit des méthodes pour dessiner des formes, texte, images ou vidéos.</span><span class="sxs-lookup"><span data-stu-id="63346-107">A <xref:System.Windows.Media.DrawingContext> object is passed as an argument, which provides methods for drawing shapes, text, images, or videos.</span></span> <span data-ttu-id="63346-108">Par conséquent, cette méthode est utile pour la personnalisation d’un objet de panneau.</span><span class="sxs-lookup"><span data-stu-id="63346-108">As a result, this method is useful for customization of a panel object.</span></span>  
  
 [!code-csharp[LightWeightCustomPanel#1](~/samples/snippets/csharp/VS_Snippets_Wpf/LightWeightCustomPanel/CSharp/OffsetPanel.cs#1)]
 [!code-vb[LightWeightCustomPanel#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/LightWeightCustomPanel/visualbasic/offsetpanel.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="63346-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63346-109">See also</span></span>

- <xref:System.Windows.Controls.Panel>
- [<span data-ttu-id="63346-110">Vue d’ensemble de Panel</span><span class="sxs-lookup"><span data-stu-id="63346-110">Panels Overview</span></span>](panels-overview.md)
- [<span data-ttu-id="63346-111">Exemple de panneau Radial personnalisé</span><span class="sxs-lookup"><span data-stu-id="63346-111">Custom Radial Panel Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=159982)
- [<span data-ttu-id="63346-112">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="63346-112">How-to Topics</span></span>](panel-how-to-topics.md)
