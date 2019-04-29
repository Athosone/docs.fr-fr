---
title: 'Procédure : Lier des données à un InkCanvas'
ms.date: 03/30/2017
helpviewer_keywords:
- InkCanvas [WPF], binding data to
- binding data [WPF], to InkCanvas
ms.assetid: 8d6b4d9e-ea7f-4412-ba83-3feccec5a515
ms.openlocfilehash: 5d3fc0ed7b6176d7bc68bf20af42c311b5563908
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61776465"
---
# <a name="how-to-data-bind-to-an-inkcanvas"></a><span data-ttu-id="ee3ec-102">Procédure : Lier des données à un InkCanvas</span><span class="sxs-lookup"><span data-stu-id="ee3ec-102">How to: Data Bind to an InkCanvas</span></span>
## <a name="example"></a><span data-ttu-id="ee3ec-103">Exemple</span><span class="sxs-lookup"><span data-stu-id="ee3ec-103">Example</span></span>  
 <span data-ttu-id="ee3ec-104">L’exemple suivant montre comment lier le <xref:System.Windows.Controls.InkCanvas.Strokes%2A> propriété d’un <xref:System.Windows.Controls.InkCanvas> vers un autre <xref:System.Windows.Controls.InkCanvas>.</span><span class="sxs-lookup"><span data-stu-id="ee3ec-104">The following example demonstrates how to bind the <xref:System.Windows.Controls.InkCanvas.Strokes%2A> property of an <xref:System.Windows.Controls.InkCanvas> to another <xref:System.Windows.Controls.InkCanvas>.</span></span>  
  
 [!code-xaml[InkCanvasBindingSnippet#2](~/samples/snippets/csharp/VS_Snippets_Wpf/InkCanvasBindingSnippet/CS/Window2.xaml#2)]  
  
 <span data-ttu-id="ee3ec-105">L’exemple suivant montre comment lier le <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A> propriété à une source de données.</span><span class="sxs-lookup"><span data-stu-id="ee3ec-105">The following example demonstrates how to bind the <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A> property to a data source.</span></span>  
  
 [!code-xaml[InkCanvasBindingSnippet#3](~/samples/snippets/csharp/VS_Snippets_Wpf/InkCanvasBindingSnippet/CS/Window2.xaml#3)]  
[!code-xaml[InkCanvasBindingSnippet#4](~/samples/snippets/csharp/VS_Snippets_Wpf/InkCanvasBindingSnippet/CS/Window2.xaml#4)]  
  
 <span data-ttu-id="ee3ec-106">L’exemple suivant déclare deux <xref:System.Windows.Controls.InkCanvas> objets dans XAML et établit la liaison de données entre eux et d’autres sources de données.</span><span class="sxs-lookup"><span data-stu-id="ee3ec-106">The following example declares two <xref:System.Windows.Controls.InkCanvas> objects in XAML and establishes data binding between them and other data sources.</span></span>  <span data-ttu-id="ee3ec-107">La première <xref:System.Windows.Controls.InkCanvas>, appelé `ic`, est lié à deux sources de données.</span><span class="sxs-lookup"><span data-stu-id="ee3ec-107">The first <xref:System.Windows.Controls.InkCanvas>, called `ic`, is bound to two data sources.</span></span>  <span data-ttu-id="ee3ec-108">Le <xref:System.Windows.Controls.InkCanvas.EditingMode%2A> et <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A> propriétés sur `ic` sont liés aux <xref:System.Windows.Controls.ListBox> objets, qui sont liés à son tour à des tableaux définis dans le XAML.</span><span class="sxs-lookup"><span data-stu-id="ee3ec-108">The <xref:System.Windows.Controls.InkCanvas.EditingMode%2A> and <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A> properties on `ic` are bound to <xref:System.Windows.Controls.ListBox> objects, which are in turn bound to arrays defined in the XAML.</span></span>  <span data-ttu-id="ee3ec-109">Le <xref:System.Windows.Controls.InkCanvas.EditingMode%2A>, <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A>, et <xref:System.Windows.Controls.InkCanvas.Strokes%2A> propriétés de la seconde <xref:System.Windows.Controls.InkCanvas> sont liés à la première <xref:System.Windows.Controls.InkCanvas>, `ic`.</span><span class="sxs-lookup"><span data-stu-id="ee3ec-109">The <xref:System.Windows.Controls.InkCanvas.EditingMode%2A>, <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A>, and <xref:System.Windows.Controls.InkCanvas.Strokes%2A> properties of the second <xref:System.Windows.Controls.InkCanvas> are bound to the first <xref:System.Windows.Controls.InkCanvas>, `ic`.</span></span>  
  
 [!code-xaml[InkCanvasBindingSnippet#1](~/samples/snippets/csharp/VS_Snippets_Wpf/InkCanvasBindingSnippet/CS/Window1.xaml#1)]
