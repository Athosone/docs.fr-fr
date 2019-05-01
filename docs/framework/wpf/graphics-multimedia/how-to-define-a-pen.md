---
title: 'Procédure : Définir un stylet'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- pens [WPF], defining
- creating [WPF], pens
ms.assetid: 7a4f2900-cdf9-49de-84e0-ba5d0ded4d33
ms.openlocfilehash: 1d69a40604dbf2f7a73c17279ae946faeb6c634a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61965403"
---
# <a name="how-to-define-a-pen"></a><span data-ttu-id="5a6d5-102">Procédure : Définir un stylet</span><span class="sxs-lookup"><span data-stu-id="5a6d5-102">How to: Define a Pen</span></span>
<span data-ttu-id="5a6d5-103">Cet exemple montre comment utiliser un <xref:System.Windows.Media.Pen> pour esquisser une forme.</span><span class="sxs-lookup"><span data-stu-id="5a6d5-103">This example shows how use a <xref:System.Windows.Media.Pen> to outline a shape.</span></span> <span data-ttu-id="5a6d5-104">Pour créer une simple <xref:System.Windows.Media.Pen>, vous devez uniquement spécifier son <xref:System.Windows.Media.Pen.Thickness%2A> et <xref:System.Windows.Media.Pen.Brush%2A>.</span><span class="sxs-lookup"><span data-stu-id="5a6d5-104">To create a simple <xref:System.Windows.Media.Pen>, you need only specify its <xref:System.Windows.Media.Pen.Thickness%2A> and <xref:System.Windows.Media.Pen.Brush%2A>.</span></span> <span data-ttu-id="5a6d5-105">Vous pouvez créer un stylet plus complexe en spécifiant un <xref:System.Windows.Media.Pen.DashStyle%2A>, <xref:System.Windows.Media.Pen.DashCap%2A>, <xref:System.Windows.Media.Pen.LineJoin%2A>, <xref:System.Windows.Media.Pen.StartLineCap%2A>, et <xref:System.Windows.Media.Pen.EndLineCap%2A>.</span><span class="sxs-lookup"><span data-stu-id="5a6d5-105">You can create more complex pen's by specifying a <xref:System.Windows.Media.Pen.DashStyle%2A>, <xref:System.Windows.Media.Pen.DashCap%2A>, <xref:System.Windows.Media.Pen.LineJoin%2A>, <xref:System.Windows.Media.Pen.StartLineCap%2A>, and <xref:System.Windows.Media.Pen.EndLineCap%2A>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5a6d5-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="5a6d5-106">Example</span></span>  
 <span data-ttu-id="5a6d5-107">L’exemple suivant utilise un <xref:System.Windows.Media.Pen> pour esquisser une forme définie par un <xref:System.Windows.Media.GeometryDrawing>.</span><span class="sxs-lookup"><span data-stu-id="5a6d5-107">The following example uses a <xref:System.Windows.Media.Pen> to outline a shape defined by a <xref:System.Windows.Media.GeometryDrawing>.</span></span>  
  
 [!code-csharp[PenExamples_snip#PenExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PenExamples_snip/CSharp/PenExample.cs#penexamplewholepage)]
 [!code-vb[PenExamples_snip#PenExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PenExamples_snip/VisualBasic/PenExample.vb#penexamplewholepage)]  
  
 <span data-ttu-id="5a6d5-108">![Contours produits par un stylet](./media/graphicsmm-simple-pen.jpg "graphicsmm_simple_pen")</span><span class="sxs-lookup"><span data-stu-id="5a6d5-108">![Outlines produces by a Pen](./media/graphicsmm-simple-pen.jpg "graphicsmm_simple_pen")</span></span>  
<span data-ttu-id="5a6d5-109">GeometryDrawing</span><span class="sxs-lookup"><span data-stu-id="5a6d5-109">A GeometryDrawing</span></span>
