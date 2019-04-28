---
title: 'Procédure : réattribuer des contrôles existants à un autre parent'
ms.date: 03/30/2017
helpviewer_keywords:
- container controls [Windows Forms], Windows Forms
- layout [Windows Forms], resizing
- layout [Windows Forms], child controls
ms.assetid: 5a5723ff-34e0-4b6f-a57b-be4ebe35cb34
ms.openlocfilehash: 2639322707c1c7e378f6d389a1dec80fd619841c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61913170"
---
# <a name="how-to-reassign-existing-controls-to-a-different-parent"></a><span data-ttu-id="789fe-102">Procédure : réattribuer des contrôles existants à un autre parent</span><span class="sxs-lookup"><span data-stu-id="789fe-102">How to: Reassign Existing Controls to a Different Parent</span></span>
<span data-ttu-id="789fe-103">Vous pouvez affecter des contrôles qui existent sur votre formulaire à un nouveau contrôle de conteneur.</span><span class="sxs-lookup"><span data-stu-id="789fe-103">You can assign controls that exist on your form to a new container control.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="789fe-104">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="789fe-104">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="789fe-105">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="789fe-105">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="789fe-106">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="789fe-106">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-reassign-existing-controls-to-a-different-parent"></a><span data-ttu-id="789fe-107">Pour réaffecter des contrôles existants à un autre parent</span><span class="sxs-lookup"><span data-stu-id="789fe-107">To reassign existing controls to a different parent</span></span>  
  
1. <span data-ttu-id="789fe-108">Faites glisser trois contrôles <xref:System.Windows.Forms.Button> de la **Boîte à outils** vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="789fe-108">Drag three <xref:System.Windows.Forms.Button> controls from the **Toolbox** onto the form.</span></span>  
  
     <span data-ttu-id="789fe-109">Disposez-les près les uns des autres en les laissant non alignés.</span><span class="sxs-lookup"><span data-stu-id="789fe-109">Position them near to each other, but leave them unaligned.</span></span>  
  
2. <span data-ttu-id="789fe-110">Dans la **Boîte à outils**, cliquez sur l’icône de contrôle <xref:System.Windows.Forms.FlowLayoutPanel> .</span><span class="sxs-lookup"><span data-stu-id="789fe-110">In the **Toolbox**, click the <xref:System.Windows.Forms.FlowLayoutPanel> control icon.</span></span>  
  
     <span data-ttu-id="789fe-111">Ne faites pas glisser l’icône vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="789fe-111">Do not drag the icon onto the form.</span></span>  
  
3. <span data-ttu-id="789fe-112">Déplacez le pointeur de la souris près des trois contrôles <xref:System.Windows.Forms.Button> .</span><span class="sxs-lookup"><span data-stu-id="789fe-112">Move the mouse pointer close to the three <xref:System.Windows.Forms.Button> controls.</span></span>  
  
     <span data-ttu-id="789fe-113">Le pointeur devient une croix à laquelle est attachée l’icône de contrôle <xref:System.Windows.Forms.FlowLayoutPanel> .</span><span class="sxs-lookup"><span data-stu-id="789fe-113">The pointer changes to a crosshair with the <xref:System.Windows.Forms.FlowLayoutPanel> control icon attached.</span></span>  
  
4. <span data-ttu-id="789fe-114">Cliquez et maintenez le bouton de la souris enfoncé.</span><span class="sxs-lookup"><span data-stu-id="789fe-114">Click and hold the mouse button.</span></span>  
  
5. <span data-ttu-id="789fe-115">Faites glisser le pointeur de la souris pour tracer le contour du contrôle <xref:System.Windows.Forms.FlowLayoutPanel> .</span><span class="sxs-lookup"><span data-stu-id="789fe-115">Drag the mouse pointer to draw the outline of the <xref:System.Windows.Forms.FlowLayoutPanel> control.</span></span>  
  
6. <span data-ttu-id="789fe-116">Tracez le contour des trois contrôles <xref:System.Windows.Forms.Button> .</span><span class="sxs-lookup"><span data-stu-id="789fe-116">Draw the outline around the three <xref:System.Windows.Forms.Button> controls.</span></span>  
  
7. <span data-ttu-id="789fe-117">Relâchez le bouton de la souris.</span><span class="sxs-lookup"><span data-stu-id="789fe-117">Release the mouse button.</span></span>  
  
     <span data-ttu-id="789fe-118">Les trois contrôles <xref:System.Windows.Forms.Button> sont maintenant insérés dans le contrôle <xref:System.Windows.Forms.FlowLayoutPanel> .</span><span class="sxs-lookup"><span data-stu-id="789fe-118">The three <xref:System.Windows.Forms.Button> controls are now inserted into the <xref:System.Windows.Forms.FlowLayoutPanel> control.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="789fe-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="789fe-119">See also</span></span>

- <xref:System.Windows.Forms.FlowLayoutPanel>
- <xref:System.Windows.Forms.TableLayoutPanel>
- [<span data-ttu-id="789fe-120">Disposition des contrôles dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="789fe-120">Arranging Controls on Windows Forms</span></span>](arranging-controls-on-windows-forms.md)
- [<span data-ttu-id="789fe-121">Procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide d’un TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="789fe-121">Walkthrough: Arranging Controls on Windows Forms Using a TableLayoutPanel</span></span>](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md)
- [<span data-ttu-id="789fe-122">Procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide des lignes d’alignement</span><span class="sxs-lookup"><span data-stu-id="789fe-122">Walkthrough: Arranging Controls on Windows Forms Using Snaplines</span></span>](walkthrough-arranging-controls-on-windows-forms-using-snaplines.md)
