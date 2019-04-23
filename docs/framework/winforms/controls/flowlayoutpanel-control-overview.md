---
title: Vue d'ensemble du contrôle FlowLayoutPanel
ms.date: 03/30/2017
f1_keywords:
- FlowLayoutPanel
helpviewer_keywords:
- forms [Windows Forms], dynamic layout
- layout [Windows Forms], dynamic
- Windows Forms, dynamic layout
- FlowLayoutPanel control [Windows Forms], about FlowLayoutPanel control
ms.assetid: 3883e024-f5a0-456d-9c27-b4dfa1cc9045
ms.openlocfilehash: 260146cd901fe2b80a73c01060ccd55958cd169e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59203039"
---
# <a name="flowlayoutpanel-control-overview"></a><span data-ttu-id="59c16-102">Vue d'ensemble du contrôle FlowLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="59c16-102">FlowLayoutPanel Control Overview</span></span>
<span data-ttu-id="59c16-103">Le contrôle <xref:System.Windows.Forms.FlowLayoutPanel> réorganise son contenu dans un sens de flux horizontal ou vertical.</span><span class="sxs-lookup"><span data-stu-id="59c16-103">The <xref:System.Windows.Forms.FlowLayoutPanel> control arranges its contents in a horizontal or vertical flow direction.</span></span> <span data-ttu-id="59c16-104">Vous pouvez encapsuler le contenu du contrôle d'une ligne à la suivante ou d'une colonne à la suivante.</span><span class="sxs-lookup"><span data-stu-id="59c16-104">You can wrap the control's contents from one row to the next, or from one column to the next.</span></span> <span data-ttu-id="59c16-105">Vous pouvez également ajuster plutôt qu'encapsuler son contenu.</span><span class="sxs-lookup"><span data-stu-id="59c16-105">Alternately, you can clip instead of wrap its contents.</span></span>  
  
 <span data-ttu-id="59c16-106">Vous pouvez spécifier le sens du flux en définissant la valeur de la propriété <xref:System.Windows.Forms.FlowLayoutPanel.FlowDirection%2A>.</span><span class="sxs-lookup"><span data-stu-id="59c16-106">You can specify the flow direction by setting the value of the <xref:System.Windows.Forms.FlowLayoutPanel.FlowDirection%2A> property.</span></span> <span data-ttu-id="59c16-107">Le contrôle <xref:System.Windows.Forms.FlowLayoutPanel> inverse correctement son sens du flux dans les dispositions de droite à gauche (RTL, Right-to-Left).</span><span class="sxs-lookup"><span data-stu-id="59c16-107">The <xref:System.Windows.Forms.FlowLayoutPanel> control correctly reverses its flow direction in Right-to-Left (RTL) layouts.</span></span> <span data-ttu-id="59c16-108">Vous pouvez également spécifier si le contenu du contrôle <xref:System.Windows.Forms.FlowLayoutPanel> est encapsulé ou coupé en définissant la valeur de la propriété <xref:System.Windows.Forms.FlowLayoutPanel.WrapContents%2A>.</span><span class="sxs-lookup"><span data-stu-id="59c16-108">You can also specify whether the <xref:System.Windows.Forms.FlowLayoutPanel> control's contents are wrapped or clipped by setting the value of the <xref:System.Windows.Forms.FlowLayoutPanel.WrapContents%2A> property.</span></span>  
  
 <span data-ttu-id="59c16-109">Le contrôle <xref:System.Windows.Forms.FlowLayoutPanel> prend automatiquement une dimension adaptée à son contenu quand vous affectez la valeur `true` à la propriété <xref:System.Windows.Forms.Control.AutoSize%2A>.</span><span class="sxs-lookup"><span data-stu-id="59c16-109">The <xref:System.Windows.Forms.FlowLayoutPanel> control automatically sizes to its contents when you set the <xref:System.Windows.Forms.Control.AutoSize%2A> property to `true`.</span></span> <span data-ttu-id="59c16-110">Il fournit également un **FlowBreak** propriété à ses contrôles enfants.</span><span class="sxs-lookup"><span data-stu-id="59c16-110">It also provides a **FlowBreak** property to its child controls.</span></span> <span data-ttu-id="59c16-111">L'affectation de la valeur `true` à la propriété FlowBreak fait en sorte que le contrôle <xref:System.Windows.Forms.FlowLayoutPanel> cesse de disposer les contrôles dans le sens du flux actuel et qu'il encapsule à la ligne ou la colonne suivante.</span><span class="sxs-lookup"><span data-stu-id="59c16-111">Setting the value of the FlowBreak property to `true` causes the <xref:System.Windows.Forms.FlowLayoutPanel> control to stop laying out controls in the current flow direction and wrap to the next row or column.</span></span>  
  
 <span data-ttu-id="59c16-112">Tout contrôle Windows Forms peut être un enfant du contrôle <xref:System.Windows.Forms.FlowLayoutPanel>, y compris d'autres instances de <xref:System.Windows.Forms.FlowLayoutPanel>.</span><span class="sxs-lookup"><span data-stu-id="59c16-112">Any Windows Forms control can be a child of the <xref:System.Windows.Forms.FlowLayoutPanel> control, including other instances of <xref:System.Windows.Forms.FlowLayoutPanel>.</span></span> <span data-ttu-id="59c16-113">Avec cette fonctionnalité, vous pouvez construire des dispositions sophistiquées qui s'adaptent aux dimensions de votre formulaire au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="59c16-113">With this capability, you can construct sophisticated layouts that adapt to your form's dimensions at run time.</span></span>  
  
 <span data-ttu-id="59c16-114">Consultez également [procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide d’un FlowLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-flowlayoutpanel.md).</span><span class="sxs-lookup"><span data-stu-id="59c16-114">Also see [Walkthrough: Arranging Controls on Windows Forms Using a FlowLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-flowlayoutpanel.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="59c16-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59c16-115">See also</span></span>

- <xref:System.Windows.Forms.FlowLayoutPanel.FlowDirection%2A>
- <xref:System.Windows.Forms.TableLayoutPanel>
- [<span data-ttu-id="59c16-116">FlowLayoutPanel, contrôle</span><span class="sxs-lookup"><span data-stu-id="59c16-116">FlowLayoutPanel Control</span></span>](flowlayoutpanel-control-windows-forms.md)
