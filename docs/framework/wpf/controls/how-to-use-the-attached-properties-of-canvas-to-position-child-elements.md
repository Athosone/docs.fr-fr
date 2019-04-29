---
title: 'Procédure : Utiliser les propriétés jointes d’un canevas pour positionner des éléments enfants'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- attached properties [WPF Designer]
- Canvas control [WPF], attached properties
ms.assetid: 48f1d25d-3820-4107-a4cc-d6c1e5664a44
ms.openlocfilehash: 347c8502bd4c5fafcde7a142327f85bfb75b9954
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61699069"
---
# <a name="how-to-use-the-attached-properties-of-canvas-to-position-child-elements"></a><span data-ttu-id="d272d-102">Procédure : Utiliser les propriétés jointes d’un canevas pour positionner des éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d272d-102">How to: Use the Attached Properties of Canvas to Position Child Elements</span></span>
<span data-ttu-id="d272d-103">Cet exemple montre comment utiliser les propriétés jointes de <xref:System.Windows.Controls.Canvas> pour positionner des éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="d272d-103">This example shows how to use the attached properties of <xref:System.Windows.Controls.Canvas> to position child elements.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d272d-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="d272d-104">Example</span></span>  
 <span data-ttu-id="d272d-105">L’exemple suivant ajoute quatre <xref:System.Windows.Controls.Button> éléments en tant qu’éléments enfants d’un parent <xref:System.Windows.Controls.Canvas>.</span><span class="sxs-lookup"><span data-stu-id="d272d-105">The following example adds four <xref:System.Windows.Controls.Button> elements as child elements of a parent <xref:System.Windows.Controls.Canvas>.</span></span> <span data-ttu-id="d272d-106">Chaque élément est représenté par un <xref:System.Windows.Controls.Canvas.Bottom%2A>, <xref:System.Windows.Controls.Canvas.Left%2A>, <xref:System.Windows.Controls.Canvas.Right%2A>, et <xref:System.Windows.Controls.Canvas.Top%2A>.</span><span class="sxs-lookup"><span data-stu-id="d272d-106">Each element is represented by a <xref:System.Windows.Controls.Canvas.Bottom%2A>, <xref:System.Windows.Controls.Canvas.Left%2A>, <xref:System.Windows.Controls.Canvas.Right%2A>, and <xref:System.Windows.Controls.Canvas.Top%2A>.</span></span>
<span data-ttu-id="d272d-107">Chaque <xref:System.Windows.Controls.Button> est positionné par rapport au parent <xref:System.Windows.Controls.Canvas> , en fonction de sa valeur de propriété assignée.</span><span class="sxs-lookup"><span data-stu-id="d272d-107">Each <xref:System.Windows.Controls.Button> is positioned relative to the parent <xref:System.Windows.Controls.Canvas> and according to its assigned property value.</span></span>  
  
 [!code-cpp[CanvasAttachedProperties#1](~/samples/snippets/cpp/VS_Snippets_Wpf/CanvasAttachedProperties/CPP/CanvasAttachedProps.cpp#1)]
 [!code-csharp[CanvasAttachedProperties#1](~/samples/snippets/csharp/VS_Snippets_Wpf/CanvasAttachedProperties/CSharp/CanvasAttachedProps.cs#1)]
 [!code-vb[CanvasAttachedProperties#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CanvasAttachedProperties/VisualBasic/CanvasAttachedProps.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="d272d-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d272d-108">See also</span></span>

- <xref:System.Windows.Controls.Canvas>
- <xref:System.Windows.Controls.Canvas.Bottom%2A>
- <xref:System.Windows.Controls.Canvas.Left%2A>
- <xref:System.Windows.Controls.Canvas.Right%2A>
- <xref:System.Windows.Controls.Canvas.Top%2A>
- <xref:System.Windows.Controls.Button>
- [<span data-ttu-id="d272d-109">Vue d’ensemble de Panel</span><span class="sxs-lookup"><span data-stu-id="d272d-109">Panels Overview</span></span>](panels-overview.md)
- [<span data-ttu-id="d272d-110">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="d272d-110">How-to Topics</span></span>](canvas-how-to-topics.md)
- [<span data-ttu-id="d272d-111">Vue d'ensemble des propriétés jointes</span><span class="sxs-lookup"><span data-stu-id="d272d-111">Attached Properties Overview</span></span>](../advanced/attached-properties-overview.md)
