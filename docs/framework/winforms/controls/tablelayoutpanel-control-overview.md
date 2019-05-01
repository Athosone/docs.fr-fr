---
title: Vue d'ensemble du contrôle TableLayoutPanel
ms.date: 03/30/2017
f1_keywords:
- TableLayoutPanel
helpviewer_keywords:
- controls [Windows Forms], resizing
- resizable controls [Windows Forms]
- Windows Forms controls, proportional resizing
- Windows Forms, proportional resizing of controls
- layout [Windows Forms], TableLayoutPanel control
- TableLayoutPanel control [Windows Forms], about TableLayoutPanel control
ms.assetid: 337661c8-61cb-44ee-93e0-3662bddec327
ms.openlocfilehash: 65daba0ce1a6f1c37fb257c1029396577821aad9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62009628"
---
# <a name="tablelayoutpanel-control-overview"></a><span data-ttu-id="09345-102">Vue d'ensemble du contrôle TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="09345-102">TableLayoutPanel Control Overview</span></span>
<span data-ttu-id="09345-103">Le contrôle <xref:System.Windows.Forms.TableLayoutPanel> réorganise son contenu dans une grille.</span><span class="sxs-lookup"><span data-stu-id="09345-103">The <xref:System.Windows.Forms.TableLayoutPanel> control arranges its contents in a grid.</span></span> <span data-ttu-id="09345-104">La disposition étant effectuée au moment du design et au moment de l'exécution, elle peut changer dynamiquement quand l'environnement d'application change.</span><span class="sxs-lookup"><span data-stu-id="09345-104">Because the layout is performed both at design time and run time, it can change dynamically as the application environment changes.</span></span> <span data-ttu-id="09345-105">Cela permet de redimensionner proportionnellement les contrôles du panneau, pour pouvoir répondre à des modifications telles que le redimensionnement du contrôle parent ou le changement de longueur de texte en raison de la localisation.</span><span class="sxs-lookup"><span data-stu-id="09345-105">This gives the controls in the panel the ability to proportionally resize, so they can respond to changes such as the parent control resizing or text length changing due to localization.</span></span>  
  
 <span data-ttu-id="09345-106">Tout contrôle Windows Forms peut être un enfant du contrôle <xref:System.Windows.Forms.TableLayoutPanel>, y compris d'autres instances de <xref:System.Windows.Forms.TableLayoutPanel>.</span><span class="sxs-lookup"><span data-stu-id="09345-106">Any Windows Forms control can be a child of the <xref:System.Windows.Forms.TableLayoutPanel> control, including other instances of <xref:System.Windows.Forms.TableLayoutPanel>.</span></span> <span data-ttu-id="09345-107">Cela vous permet de construire des dispositions sophistiquées qui s'adaptent aux modifications au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="09345-107">This allows you to construct sophisticated layouts that adapt to changes at run time.</span></span>  
  
 <span data-ttu-id="09345-108">Le contrôle <xref:System.Windows.Forms.TableLayoutPanel> peut s'étendre pour accepter de nouveaux contrôles quand ils sont ajoutés, en fonction de la valeur des propriétés <xref:System.Windows.Forms.TableLayoutPanel.RowCount%2A>, <xref:System.Windows.Forms.TableLayoutPanel.ColumnCount%2A>, et <xref:System.Windows.Forms.TableLayoutPanel.GrowStyle%2A>.</span><span class="sxs-lookup"><span data-stu-id="09345-108">The <xref:System.Windows.Forms.TableLayoutPanel> control can expand to accommodate new controls when they are added, depending on the value of the <xref:System.Windows.Forms.TableLayoutPanel.RowCount%2A>, <xref:System.Windows.Forms.TableLayoutPanel.ColumnCount%2A>, and <xref:System.Windows.Forms.TableLayoutPanel.GrowStyle%2A> properties.</span></span> <span data-ttu-id="09345-109">L'affectation de la valeur 0 à la propriété <xref:System.Windows.Forms.TableLayoutPanel.RowCount%2A> ou <xref:System.Windows.Forms.TableLayoutPanel.ColumnCount%2A> indique que le <xref:System.Windows.Forms.TableLayoutPanel> sera indépendant dans la direction correspondante.</span><span class="sxs-lookup"><span data-stu-id="09345-109">Setting either the <xref:System.Windows.Forms.TableLayoutPanel.RowCount%2A> or <xref:System.Windows.Forms.TableLayoutPanel.ColumnCount%2A> property to a value of 0 specifies that the <xref:System.Windows.Forms.TableLayoutPanel> will be unbound in the corresponding direction.</span></span>  
  
 <span data-ttu-id="09345-110">Vous pouvez également contrôler la direction d'expansion (horizontale ou verticale) une fois que le contrôle <xref:System.Windows.Forms.TableLayoutPanel> est rempli de contrôles enfants.</span><span class="sxs-lookup"><span data-stu-id="09345-110">You can also control the direction of expansion (horizontal or vertical) after the <xref:System.Windows.Forms.TableLayoutPanel> control is full of child controls.</span></span> <span data-ttu-id="09345-111">Par défaut, le contrôle <xref:System.Windows.Forms.TableLayoutPanel> s'étend vers le bas en ajoutant des lignes.</span><span class="sxs-lookup"><span data-stu-id="09345-111">By default, the <xref:System.Windows.Forms.TableLayoutPanel> control expands downward by adding rows.</span></span>  
  
 <span data-ttu-id="09345-112">Si vous souhaitez que les lignes et les colonnes se comportent différemment du comportement par défaut, vous pouvez contrôler leurs propriétés à l'aide des propriétés <xref:System.Windows.Forms.TableLayoutPanel.RowStyles%2A> et <xref:System.Windows.Forms.TableLayoutPanel.ColumnStyles%2A>.</span><span class="sxs-lookup"><span data-stu-id="09345-112">If you want rows and columns that behave differently from the default behavior, you can control the properties of rows and columns by using the <xref:System.Windows.Forms.TableLayoutPanel.RowStyles%2A> and <xref:System.Windows.Forms.TableLayoutPanel.ColumnStyles%2A> properties.</span></span> <span data-ttu-id="09345-113">Vous pouvez définir les propriétés des lignes ou des colonnes individuellement.</span><span class="sxs-lookup"><span data-stu-id="09345-113">You can set the properties of rows or columns individually.</span></span>  
  
 <span data-ttu-id="09345-114">Le contrôle <xref:System.Windows.Forms.TableLayoutPanel> ajoute les propriétés suivantes à ses contrôles enfants : `Cell`, `Column`, `Row`, `ColumnSpan`, et `RowSpan`.</span><span class="sxs-lookup"><span data-stu-id="09345-114">The <xref:System.Windows.Forms.TableLayoutPanel> control adds the following properties to its child controls: `Cell`, `Column`, `Row`, `ColumnSpan`, and `RowSpan`.</span></span>  
  
 <span data-ttu-id="09345-115">Vous pouvez fusionner des cellules dans le contrôle <xref:System.Windows.Forms.TableLayoutPanel> en définissant les propriétés `ColumnSpan` ou `RowSpan` sur un contrôle enfant.</span><span class="sxs-lookup"><span data-stu-id="09345-115">You can merge cells in the <xref:System.Windows.Forms.TableLayoutPanel> control by setting the `ColumnSpan` or `RowSpan` properties on a child control.</span></span>  
  
1. [<span data-ttu-id="09345-116">Guide pratique pour Aligner et étirer un contrôle dans un contrôle TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="09345-116">How to: Align and Stretch a Control in a TableLayoutPanel Control</span></span>](how-to-align-and-stretch-a-control-in-a-tablelayoutpanel-control.md)  
  
2. [<span data-ttu-id="09345-117">Guide pratique pour Étendre des lignes et colonnes dans un contrôle TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="09345-117">How to: Span Rows and Columns in a TableLayoutPanel Control</span></span>](how-to-span-rows-and-columns-in-a-tablelayoutpanel-control.md)  
  
3. [<span data-ttu-id="09345-118">Guide pratique pour Modifier des colonnes et lignes dans un contrôle TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="09345-118">How to: Edit Columns and Rows in a TableLayoutPanel Control</span></span>](how-to-edit-columns-and-rows-in-a-tablelayoutpanel-control.md)  
  
4. [<span data-ttu-id="09345-119">Procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide d’un TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="09345-119">Walkthrough: Arranging Controls on Windows Forms Using a TableLayoutPanel</span></span>](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md)  
  
## <a name="see-also"></a><span data-ttu-id="09345-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09345-120">See also</span></span>

- <xref:System.Windows.Forms.FlowLayoutPanel>
- <xref:System.Windows.Forms.TableLayoutSettings>
- [<span data-ttu-id="09345-121">Guide pratique pour Créer qu'un Windows Forms de disposition qui répond bien à la localisation</span><span class="sxs-lookup"><span data-stu-id="09345-121">How to: Design a Windows Forms Layout that Responds Well to Localization</span></span>](how-to-design-a-windows-forms-layout-that-responds-well-to-localization.md)
- [<span data-ttu-id="09345-122">Guide pratique pour Créer un formulaire Windows redimensionnable pour l’entrée de données</span><span class="sxs-lookup"><span data-stu-id="09345-122">How to: Create a Resizable Windows Form for Data Entry</span></span>](how-to-create-a-resizable-windows-form-for-data-entry.md)
- [<span data-ttu-id="09345-123">Meilleures pratiques pour le contrôle TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="09345-123">Best Practices for the TableLayoutPanel Control</span></span>](best-practices-for-the-tablelayoutpanel-control.md)
