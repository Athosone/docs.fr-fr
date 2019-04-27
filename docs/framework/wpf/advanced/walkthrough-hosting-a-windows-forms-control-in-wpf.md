---
title: 'Procédure pas à pas : hébergement d’un contrôle Windows Forms dans WPF'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- hosting Windows Forms control in WPF [WPF]
ms.assetid: 9cb88415-39b0-4c46-80c4-ff325b674286
ms.openlocfilehash: 4e9b42738ff661425b05a63f2a5e5790c5cbd84b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61699458"
---
# <a name="walkthrough-hosting-a-windows-forms-control-in-wpf"></a><span data-ttu-id="3ba5d-102">Procédure pas à pas : hébergement d’un contrôle Windows Forms dans WPF</span><span class="sxs-lookup"><span data-stu-id="3ba5d-102">Walkthrough: Hosting a Windows Forms Control in WPF</span></span>

[!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <span data-ttu-id="3ba5d-103">fournit de nombreux contrôles avec un ensemble complet de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="3ba5d-103">provides many controls with a rich feature set.</span></span> <span data-ttu-id="3ba5d-104">Toutefois, vous souhaiterez parfois utiliser [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôle sur votre [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] pages.</span><span class="sxs-lookup"><span data-stu-id="3ba5d-104">However, you may sometimes want to use [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] controls on your [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] pages.</span></span> <span data-ttu-id="3ba5d-105">Par exemple, avoir un investissement substantiel dans existant [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôles, ou vous pouvez avoir un [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôle qui fournit des fonctionnalités uniques.</span><span class="sxs-lookup"><span data-stu-id="3ba5d-105">For example, you may have a substantial investment in existing [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] controls, or you may have a [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] control that provides unique functionality.</span></span>

<span data-ttu-id="3ba5d-106">Cette procédure pas à pas vous montre comment héberger un [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] <xref:System.Windows.Forms.MaskedTextBox?displayProperty=nameWithType> control sur un [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] page à l’aide de code.</span><span class="sxs-lookup"><span data-stu-id="3ba5d-106">This walkthrough shows you how to host a [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] <xref:System.Windows.Forms.MaskedTextBox?displayProperty=nameWithType> control on a [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] page by using code.</span></span>

<span data-ttu-id="3ba5d-107">Pour l’intégralité du code des tâches illustrées dans cette procédure pas à pas, consultez [hébergement d’un contrôle de formulaires Windows dans WPF, exemple](https://go.microsoft.com/fwlink/?LinkID=160057).</span><span class="sxs-lookup"><span data-stu-id="3ba5d-107">For a complete code listing of the tasks shown in this walkthrough, see [Hosting a Windows Forms Control in WPF Sample](https://go.microsoft.com/fwlink/?LinkID=160057).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3ba5d-108">Prérequis</span><span class="sxs-lookup"><span data-stu-id="3ba5d-108">Prerequisites</span></span>

<span data-ttu-id="3ba5d-109">Cette procédure pas à pas nécessite Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3ba5d-109">You need Visual Studio to complete this walkthrough.</span></span>

## <a name="hosting-the-windows-forms-control"></a><span data-ttu-id="3ba5d-110">Hébergement d’un contrôle Windows Forms</span><span class="sxs-lookup"><span data-stu-id="3ba5d-110">Hosting the Windows Forms Control</span></span>

### <a name="to-host-the-maskedtextbox-control"></a><span data-ttu-id="3ba5d-111">Pour héberger le contrôle MaskedTextBox</span><span class="sxs-lookup"><span data-stu-id="3ba5d-111">To host the MaskedTextBox control</span></span>

1. <span data-ttu-id="3ba5d-112">Créez un projet d’Application WPF nommé `HostingWfInWpf`.</span><span class="sxs-lookup"><span data-stu-id="3ba5d-112">Create a WPF Application project named `HostingWfInWpf`.</span></span>

2. <span data-ttu-id="3ba5d-113">Ajoutez les références aux assemblys suivants.</span><span class="sxs-lookup"><span data-stu-id="3ba5d-113">Add references to the following assemblies.</span></span>

    -   <span data-ttu-id="3ba5d-114">WindowsFormsIntegration</span><span class="sxs-lookup"><span data-stu-id="3ba5d-114">WindowsFormsIntegration</span></span>

    -   <span data-ttu-id="3ba5d-115">System.Windows.Forms</span><span class="sxs-lookup"><span data-stu-id="3ba5d-115">System.Windows.Forms</span></span>

3. <span data-ttu-id="3ba5d-116">Ouvrez MainWindow.xaml dans le [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)].</span><span class="sxs-lookup"><span data-stu-id="3ba5d-116">Open MainWindow.xaml in the [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)].</span></span>

4. <span data-ttu-id="3ba5d-117">Nom de la <xref:System.Windows.Controls.Grid> élément `grid1`.</span><span class="sxs-lookup"><span data-stu-id="3ba5d-117">Name the <xref:System.Windows.Controls.Grid> element `grid1`.</span></span>

     [!code-xaml[HostingWfInWPF#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HostingWfInWPF/CSharp/HostingWfInWPF/Window1.xaml#1)]

5. <span data-ttu-id="3ba5d-118">Dans le mode Création ou XAML, sélectionnez le <xref:System.Windows.Window> élément.</span><span class="sxs-lookup"><span data-stu-id="3ba5d-118">In Design view or XAML view, select the <xref:System.Windows.Window> element.</span></span>

6. <span data-ttu-id="3ba5d-119">Dans la fenêtre Propriétés, cliquez sur le **événements** onglet.</span><span class="sxs-lookup"><span data-stu-id="3ba5d-119">In the Properties window, click the **Events** tab.</span></span>

7. <span data-ttu-id="3ba5d-120">Double-cliquez sur le <xref:System.Windows.FrameworkElement.Loaded> événement.</span><span class="sxs-lookup"><span data-stu-id="3ba5d-120">Double-click the <xref:System.Windows.FrameworkElement.Loaded> event.</span></span>

8. <span data-ttu-id="3ba5d-121">Insérez le code suivant pour gérer les <xref:System.Windows.FrameworkElement.Loaded> événement.</span><span class="sxs-lookup"><span data-stu-id="3ba5d-121">Insert the following code to handle the <xref:System.Windows.FrameworkElement.Loaded> event.</span></span>

     [!code-csharp[HostingWfInWPF#10](~/samples/snippets/csharp/VS_Snippets_Wpf/HostingWfInWPF/CSharp/HostingWfInWPF/Window1.xaml.cs#10)]
     [!code-vb[HostingWfInWPF#10](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HostingWfInWPF/VisualBasic/HostingWfInWpf/Window1.xaml.vb#10)]

9. <span data-ttu-id="3ba5d-122">En haut du fichier, ajoutez le code suivant `Imports` ou `using` instruction.</span><span class="sxs-lookup"><span data-stu-id="3ba5d-122">At the top of the file, add the following `Imports` or `using` statement.</span></span>

     [!code-csharp[HostingWfInWPF#11](~/samples/snippets/csharp/VS_Snippets_Wpf/HostingWfInWPF/CSharp/HostingWfInWPF/Window1.xaml.cs#11)]
     [!code-vb[HostingWfInWPF#11](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HostingWfInWPF/VisualBasic/HostingWfInWpf/Window1.xaml.vb#11)]

10. <span data-ttu-id="3ba5d-123">Appuyez sur **F5** pour générer et exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="3ba5d-123">Press **F5** to build and run the application.</span></span>

## <a name="see-also"></a><span data-ttu-id="3ba5d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ba5d-124">See also</span></span>

- <xref:System.Windows.Forms.Integration.ElementHost>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [<span data-ttu-id="3ba5d-125">Concevoir en XAML dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3ba5d-125">Design XAML in Visual Studio</span></span>](/visualstudio/designers/designing-xaml-in-visual-studio)
- [<span data-ttu-id="3ba5d-126">Procédure pas à pas : Hébergement d’un contrôle de formulaires Windows dans WPF à l’aide de XAML</span><span class="sxs-lookup"><span data-stu-id="3ba5d-126">Walkthrough: Hosting a Windows Forms Control in WPF by Using XAML</span></span>](walkthrough-hosting-a-windows-forms-control-in-wpf-by-using-xaml.md)
- [<span data-ttu-id="3ba5d-127">Procédure pas à pas : Hébergement d’un contrôle Composite de formulaires Windows dans WPF</span><span class="sxs-lookup"><span data-stu-id="3ba5d-127">Walkthrough: Hosting a Windows Forms Composite Control in WPF</span></span>](walkthrough-hosting-a-windows-forms-composite-control-in-wpf.md)
- [<span data-ttu-id="3ba5d-128">Procédure pas à pas : Hébergement d’un contrôle Composite WPF dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="3ba5d-128">Walkthrough: Hosting a WPF Composite Control in Windows Forms</span></span>](walkthrough-hosting-a-wpf-composite-control-in-windows-forms.md)
- [<span data-ttu-id="3ba5d-129">Contrôles Windows Forms et contrôles WPF équivalents</span><span class="sxs-lookup"><span data-stu-id="3ba5d-129">Windows Forms Controls and Equivalent WPF Controls</span></span>](windows-forms-controls-and-equivalent-wpf-controls.md)
- [<span data-ttu-id="3ba5d-130">Hébergement d’un contrôle Windows Forms dans WPF, exemple</span><span class="sxs-lookup"><span data-stu-id="3ba5d-130">Hosting a Windows Forms Control in WPF Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=160057)
