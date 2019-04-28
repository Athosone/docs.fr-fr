---
title: 'Procédure : positionner des contrôles dans des Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- Location
- Location.Y
- Location.X
helpviewer_keywords:
- controls [Windows Forms]
- controls [Windows Forms], moving
- snaplines
- controls [Windows Forms], positioning
ms.assetid: 4693977e-34a4-4f19-8221-68c3120c2b2b
ms.openlocfilehash: a0b97073b2f9363a64bfc4a4ede7ffa69e2bce42
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61913261"
---
# <a name="how-to-position-controls-on-windows-forms"></a><span data-ttu-id="6e155-102">Procédure : positionner des contrôles dans des Windows Forms</span><span class="sxs-lookup"><span data-stu-id="6e155-102">How to: Position Controls on Windows Forms</span></span>
<span data-ttu-id="6e155-103">Pour positionner des contrôles, utiliser le Concepteur de formulaires Windows ou spécifiez le <xref:System.Windows.Forms.Control.Location%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="6e155-103">To position controls, use the Windows Forms Designer, or specify the <xref:System.Windows.Forms.Control.Location%2A> property.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="6e155-104">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="6e155-104">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="6e155-105">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="6e155-105">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="6e155-106">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="6e155-106">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-position-a-control-on-the-design-surface-of-the-windows-forms-designer"></a><span data-ttu-id="6e155-107">Pour positionner un contrôle sur l’aire de conception du Concepteur Windows Forms</span><span class="sxs-lookup"><span data-stu-id="6e155-107">To position a control on the design surface of the Windows Forms Designer</span></span>  
  
- <span data-ttu-id="6e155-108">Faites glisser le contrôle vers l’emplacement approprié avec la souris.</span><span class="sxs-lookup"><span data-stu-id="6e155-108">Drag the control to the appropriate location with the mouse.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="6e155-109">Sélectionnez le contrôle et les déplacer avec la flèche touches pour positionner plus précisément.</span><span class="sxs-lookup"><span data-stu-id="6e155-109">Select the control and move it with the ARROW keys to position it more precisely.</span></span> <span data-ttu-id="6e155-110">En outre, *les lignes d’alignement* vous aident à placer les contrôles avec précision sur votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="6e155-110">Also, *snaplines* assist you in placing controls precisely on your form.</span></span> <span data-ttu-id="6e155-111">Pour plus d’informations, consultez [Procédure pas à pas : Organisation des contrôles dans les Windows Forms à l’aide des lignes d’alignement](walkthrough-arranging-controls-on-windows-forms-using-snaplines.md).</span><span class="sxs-lookup"><span data-stu-id="6e155-111">For more information, see [Walkthrough: Arranging Controls on Windows Forms Using Snaplines](walkthrough-arranging-controls-on-windows-forms-using-snaplines.md).</span></span>  
  
### <a name="to-position-a-control-using-the-properties-window"></a><span data-ttu-id="6e155-112">Pour positionner un contrôle à l’aide de la fenêtre Propriétés</span><span class="sxs-lookup"><span data-stu-id="6e155-112">To position a control using the Properties window</span></span>  
  
1. <span data-ttu-id="6e155-113">Cliquez sur le contrôle que vous souhaitez positionner.</span><span class="sxs-lookup"><span data-stu-id="6e155-113">Click the control you want to position.</span></span>  
  
2. <span data-ttu-id="6e155-114">Dans le **propriétés** fenêtre, les valeurs de type pour le <xref:System.Windows.Forms.Control.Location%2A> propriété séparés par une virgule, pour positionner le contrôle dans son conteneur.</span><span class="sxs-lookup"><span data-stu-id="6e155-114">In the **Properties** window, type values for the <xref:System.Windows.Forms.Control.Location%2A> property, separated by a comma, to position the control within its container.</span></span>  
  
     <span data-ttu-id="6e155-115">Le premier nombre (X) est la distance entre la bordure gauche du conteneur ; le deuxième nombre (Y) est la distance entre la bordure supérieure de la zone conteneur, en pixels.</span><span class="sxs-lookup"><span data-stu-id="6e155-115">The first number (X) is the distance from the left border of the container; the second number (Y) is the distance from the upper border of the container area, measured in pixels.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="6e155-116">Vous pouvez développer le <xref:System.Windows.Forms.Control.Location%2A> propriété permettant de taper le **X** et **Y** valeurs individuellement.</span><span class="sxs-lookup"><span data-stu-id="6e155-116">You can expand the <xref:System.Windows.Forms.Control.Location%2A> property to type the **X** and **Y** values individually.</span></span>  
  
### <a name="to-position-a-control-programmatically"></a><span data-ttu-id="6e155-117">Pour positionner un contrôle par programmation</span><span class="sxs-lookup"><span data-stu-id="6e155-117">To position a control programmatically</span></span>  
  
1. <span data-ttu-id="6e155-118">Définir le <xref:System.Windows.Forms.Control.Location%2A> propriété du contrôle à un <xref:System.Drawing.Point>.</span><span class="sxs-lookup"><span data-stu-id="6e155-118">Set the <xref:System.Windows.Forms.Control.Location%2A> property of the control to a <xref:System.Drawing.Point>.</span></span>  
  
    ```vb  
    Button1.Location = New Point(100, 100)  
    ```  
  
    ```csharp  
    button1.Location = new Point(100, 100);  
    ```  
  
    ```cpp  
    button1->Location = Point(100, 100);  
    ```  
  
2. <span data-ttu-id="6e155-119">Modifiez la coordonnée X de l’emplacement du contrôle à l’aide de la <xref:System.Windows.Forms.Control.Left%2A> sous-propriété.</span><span class="sxs-lookup"><span data-stu-id="6e155-119">Change the X coordinate of the control's location using the <xref:System.Windows.Forms.Control.Left%2A> subproperty.</span></span>  
  
    ```vb  
    Button1.Left = 300  
    ```  
  
    ```csharp  
    button1.Left = 300;  
    ```  
  
    ```cpp  
    button1->Left = 300;  
    ```  
  
### <a name="to-increment-a-controls-location-programmatically"></a><span data-ttu-id="6e155-120">Pour incrémenter l’emplacement d’un contrôle par programmation</span><span class="sxs-lookup"><span data-stu-id="6e155-120">To increment a control's location programmatically</span></span>  
  
1. <span data-ttu-id="6e155-121">Définir le <xref:System.Windows.Forms.Control.Left%2A> sous-propriété pour incrémenter la coordonnée X du contrôle.</span><span class="sxs-lookup"><span data-stu-id="6e155-121">Set the <xref:System.Windows.Forms.Control.Left%2A> subproperty to increment the X coordinate of the control.</span></span>  
  
    ```vb  
    Button1.Left += 200  
    ```  
  
    ```csharp  
    button1.Left += 200;  
    ```  
  
    ```cpp  
    button1->Left += 200;  
    ```  
  
    > [!NOTE]
    >  <span data-ttu-id="6e155-122">Utilisez le <xref:System.Windows.Forms.Control.Location%2A> propriété à définir d’un contrôle X et Y place simultanément.</span><span class="sxs-lookup"><span data-stu-id="6e155-122">Use the <xref:System.Windows.Forms.Control.Location%2A> property to set a control's X and Y positions simultaneously.</span></span> <span data-ttu-id="6e155-123">Pour définir une position individuellement, utilisez le contrôle <xref:System.Windows.Forms.Control.Left%2A> (**X**) ou <xref:System.Windows.Forms.Control.Top%2A> (**Y**) sous-propriété.</span><span class="sxs-lookup"><span data-stu-id="6e155-123">To set a position individually, use the control's <xref:System.Windows.Forms.Control.Left%2A> (**X**) or <xref:System.Windows.Forms.Control.Top%2A> (**Y**) subproperty.</span></span> <span data-ttu-id="6e155-124">N’essayez pas de définir implicitement les coordonnées X et Y de la <xref:System.Drawing.Point> structure qui représente la position du bouton, car cette structure contient une copie des coordonnées du bouton.</span><span class="sxs-lookup"><span data-stu-id="6e155-124">Do not try to implicitly set the X and Y coordinates of the <xref:System.Drawing.Point> structure that represents the button's location, because this structure contains a copy of the button's coordinates.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6e155-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e155-125">See also</span></span>

- [<span data-ttu-id="6e155-126">Contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="6e155-126">Windows Forms Controls</span></span>](index.md)
- [<span data-ttu-id="6e155-127">Procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide des lignes d’alignement</span><span class="sxs-lookup"><span data-stu-id="6e155-127">Walkthrough: Arranging Controls on Windows Forms Using Snaplines</span></span>](walkthrough-arranging-controls-on-windows-forms-using-snaplines.md)
- [<span data-ttu-id="6e155-128">Procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide d’un TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="6e155-128">Walkthrough: Arranging Controls on Windows Forms Using a TableLayoutPanel</span></span>](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md)
- [<span data-ttu-id="6e155-129">Procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide d’un FlowLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="6e155-129">Walkthrough: Arranging Controls on Windows Forms Using a FlowLayoutPanel</span></span>](walkthrough-arranging-controls-on-windows-forms-using-a-flowlayoutpanel.md)
- [<span data-ttu-id="6e155-130">Disposition des contrôles dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="6e155-130">Arranging Controls on Windows Forms</span></span>](arranging-controls-on-windows-forms.md)
- [<span data-ttu-id="6e155-131">Création d'étiquettes et de raccourcis pour les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="6e155-131">Labeling Individual Windows Forms Controls and Providing Shortcuts to Them</span></span>](labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
- [<span data-ttu-id="6e155-132">Contrôles à utiliser dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="6e155-132">Controls to Use on Windows Forms</span></span>](controls-to-use-on-windows-forms.md)
- [<span data-ttu-id="6e155-133">Classement par fonction des contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="6e155-133">Windows Forms Controls by Function</span></span>](windows-forms-controls-by-function.md)
- <span data-ttu-id="6e155-134">[Guide pratique pour Définir l’emplacement de l’écran des Windows Forms](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/52aha046(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="6e155-134">[How to: Set the Screen Location of Windows Forms](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/52aha046(v=vs.100))</span></span>
