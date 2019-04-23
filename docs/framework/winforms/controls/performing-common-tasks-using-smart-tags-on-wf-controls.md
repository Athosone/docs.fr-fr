---
title: 'Procédure pas à pas : exécution de tâches courantes à l’aide de balises actives dans les contrôles Windows Forms'
ms.date: 03/30/2017
helpviewer_keywords:
- DesignerAction object model
- smart tags
- designer actions
ms.assetid: cac337e6-00f6-4584-80f4-75728f5ea113
ms.openlocfilehash: a93402be30cb461ac6a0ed9daa4a684598a85da1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59318245"
---
# <a name="walkthrough-performing-common-tasks-using-smart-tags-on-windows-forms-controls"></a><span data-ttu-id="e179b-102">Procédure pas à pas : exécution de tâches courantes à l’aide de balises actives dans les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e179b-102">Walkthrough: Performing Common Tasks Using Smart Tags on Windows Forms Controls</span></span>
<span data-ttu-id="e179b-103">Lorsque vous construisez des formulaires et contrôles pour votre application Windows Forms, il existe de nombreuses tâches que vous allez effectuer à plusieurs reprises.</span><span class="sxs-lookup"><span data-stu-id="e179b-103">As you construct forms and controls for your Windows Forms application, there are many tasks you will perform repeatedly.</span></span> <span data-ttu-id="e179b-104">Il existe quelques tâches courantes que vous rencontrerez :</span><span class="sxs-lookup"><span data-stu-id="e179b-104">These are some of the commonly performed tasks you will encounter:</span></span>  
  
-   <span data-ttu-id="e179b-105">Ajout ou suppression d’un onglet sur un <xref:System.Windows.Forms.TabControl>.</span><span class="sxs-lookup"><span data-stu-id="e179b-105">Adding or removing a tab on a <xref:System.Windows.Forms.TabControl>.</span></span>  
  
-   <span data-ttu-id="e179b-106">Ancrage d’un contrôle à son parent.</span><span class="sxs-lookup"><span data-stu-id="e179b-106">Docking a control to its parent.</span></span>  
  
-   <span data-ttu-id="e179b-107">Modification de l’orientation d’un <xref:System.Windows.Forms.SplitContainer> contrôle.</span><span class="sxs-lookup"><span data-stu-id="e179b-107">Changing the orientation of a <xref:System.Windows.Forms.SplitContainer> control.</span></span>  
  
 <span data-ttu-id="e179b-108">Pour accélérer le développement, de nombreux contrôles offrent des balises actives, qui sont des menus contextuels qui vous permettent d’effectuer des tâches courantes comme celles-ci en un seul geste au moment du design.</span><span class="sxs-lookup"><span data-stu-id="e179b-108">To speed development, many controls offer smart tags, which are context-sensitive menus that allow you to perform common tasks like these in a single gesture at design time.</span></span> <span data-ttu-id="e179b-109">Ces tâches sont appelées *verbes de balise active*.</span><span class="sxs-lookup"><span data-stu-id="e179b-109">These tasks are called *smart-tag verbs*.</span></span>  
  
 <span data-ttu-id="e179b-110">Balises actives restent attachées à une instance de contrôle pour sa durée de vie dans le concepteur et sont toujours disponibles.</span><span class="sxs-lookup"><span data-stu-id="e179b-110">Smart tags remain attached to a control instance for its lifetime in the designer and are always available.</span></span>  
  
 <span data-ttu-id="e179b-111">Cette procédure pas à pas décrit notamment les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="e179b-111">Tasks illustrated in this walkthrough include:</span></span>  
  
-   <span data-ttu-id="e179b-112">Création d’un projet Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e179b-112">Creating a Windows Forms project</span></span>  
  
-   <span data-ttu-id="e179b-113">À l’aide de balises actives</span><span class="sxs-lookup"><span data-stu-id="e179b-113">Using smart tags</span></span>  
  
-   <span data-ttu-id="e179b-114">Activation et désactivation des balises actives</span><span class="sxs-lookup"><span data-stu-id="e179b-114">Enabling and Disabling Smart Tags</span></span>  
  
 <span data-ttu-id="e179b-115">À l’issue de cette procédure, vous comprendrez le rôle joué par ces fonctionnalités de disposition importantes.</span><span class="sxs-lookup"><span data-stu-id="e179b-115">When you are finished, you will have an understanding of the role played by these important layout features.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e179b-116">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="e179b-116">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="e179b-117">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="e179b-117">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="e179b-118">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="e179b-118">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
## <a name="creating-the-project"></a><span data-ttu-id="e179b-119">Création du projet</span><span class="sxs-lookup"><span data-stu-id="e179b-119">Creating the Project</span></span>  
 <span data-ttu-id="e179b-120">La première étape consiste à créer le projet et à configurer le formulaire.</span><span class="sxs-lookup"><span data-stu-id="e179b-120">The first step is to create the project and set up the form.</span></span>  
  
#### <a name="to-create-the-project"></a><span data-ttu-id="e179b-121">Pour créer le projet</span><span class="sxs-lookup"><span data-stu-id="e179b-121">To create the project</span></span>  
  
1. <span data-ttu-id="e179b-122">Créer un projet d’application Windows appelé « SmartTagsExample » (**fichier** > **New** > **projet**  >   **Visual C#** ou **Visual Basic** > **bureau classique** > **Windows Forms Application**).</span><span class="sxs-lookup"><span data-stu-id="e179b-122">Create a Windows-based application project called "SmartTagsExample" (**File** > **New** > **Project** > **Visual C#** or **Visual Basic** > **Classic Desktop** > **Windows Forms Application**).</span></span>  
  
2. <span data-ttu-id="e179b-123">Sélectionnez le formulaire dans le **Windows Forms Designer**.</span><span class="sxs-lookup"><span data-stu-id="e179b-123">Select the form in the **Windows Forms Designer**.</span></span>  
  
## <a name="using-smart-tags"></a><span data-ttu-id="e179b-124">À l’aide de balises actives</span><span class="sxs-lookup"><span data-stu-id="e179b-124">Using Smart Tags</span></span>  
 <span data-ttu-id="e179b-125">Balises actives sont toujours disponibles au moment du design sur les contrôles qui les proposent.</span><span class="sxs-lookup"><span data-stu-id="e179b-125">Smart tags are always available at design time on controls that offer them.</span></span>  
  
#### <a name="to-use-smart-tags"></a><span data-ttu-id="e179b-126">Pour utiliser des balises actives</span><span class="sxs-lookup"><span data-stu-id="e179b-126">To use smart tags</span></span>  
  
1. <span data-ttu-id="e179b-127">Faites glisser un <xref:System.Windows.Forms.TabControl> à partir de la **boîte à outils** vers votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="e179b-127">Drag a <xref:System.Windows.Forms.TabControl> from the **Toolbox** onto your form.</span></span> <span data-ttu-id="e179b-128">Notez le glyphe de balise active (![glyphe de balise active](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) qui apparaît sur le côté du <xref:System.Windows.Forms.TabControl>.</span><span class="sxs-lookup"><span data-stu-id="e179b-128">Note the smart-tag glyph (![Smart Tag Glyph](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) that appears on the side of the <xref:System.Windows.Forms.TabControl>.</span></span>  
  
2. <span data-ttu-id="e179b-129">Cliquez sur le glyphe de balise active.</span><span class="sxs-lookup"><span data-stu-id="e179b-129">Click the smart-tag glyph.</span></span> <span data-ttu-id="e179b-130">Dans le menu contextuel qui s’affiche en regard du glyphe, sélectionnez le **ajouter un onglet** élément.</span><span class="sxs-lookup"><span data-stu-id="e179b-130">In the shortcut menu that appears next to the glyph, select the **Add Tab** item.</span></span> <span data-ttu-id="e179b-131">Observez qu’une nouvelle page d’onglets est ajoutée à la <xref:System.Windows.Forms.TabControl>.</span><span class="sxs-lookup"><span data-stu-id="e179b-131">Observe that a new tab page is added to the <xref:System.Windows.Forms.TabControl>.</span></span>  
  
3. <span data-ttu-id="e179b-132">Faites glisser un contrôle <xref:System.Windows.Forms.TableLayoutPanel> de la **boîte à outils** vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="e179b-132">Drag a <xref:System.Windows.Forms.TableLayoutPanel> control from the **Toolbox** onto your form.</span></span>  
  
4. <span data-ttu-id="e179b-133">Cliquez sur le glyphe de balise active.</span><span class="sxs-lookup"><span data-stu-id="e179b-133">Click the smart-tag glyph.</span></span> <span data-ttu-id="e179b-134">Dans le menu contextuel qui s’affiche en regard du glyphe, sélectionnez le **ajouter une colonne** élément.</span><span class="sxs-lookup"><span data-stu-id="e179b-134">In the shortcut menu that appears next to the glyph, select the **Add Column** item.</span></span> <span data-ttu-id="e179b-135">Observez qu’une nouvelle colonne est ajoutée à la <xref:System.Windows.Forms.TableLayoutPanel> contrôle.</span><span class="sxs-lookup"><span data-stu-id="e179b-135">Observe that a new column is added to the <xref:System.Windows.Forms.TableLayoutPanel> control.</span></span>  
  
5. <span data-ttu-id="e179b-136">Faites glisser un contrôle <xref:System.Windows.Forms.SplitContainer> de la **boîte à outils** vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="e179b-136">Drag a <xref:System.Windows.Forms.SplitContainer> control from the **Toolbox** onto your form.</span></span>  
  
6. <span data-ttu-id="e179b-137">Cliquez sur le glyphe de balise active.</span><span class="sxs-lookup"><span data-stu-id="e179b-137">Click the smart-tag glyph.</span></span> <span data-ttu-id="e179b-138">Dans le menu contextuel qui s’affiche en regard du glyphe, sélectionnez le **l’orientation du fractionnement Horizontal** élément.</span><span class="sxs-lookup"><span data-stu-id="e179b-138">In the shortcut menu that appears next to the glyph, select the **Horizontal splitter orientation** item.</span></span> <span data-ttu-id="e179b-139">Observez que le <xref:System.Windows.Forms.SplitContainer> barre de fractionnement du contrôle est maintenant orientée horizontalement.</span><span class="sxs-lookup"><span data-stu-id="e179b-139">Observe that the <xref:System.Windows.Forms.SplitContainer> control's splitter bar is now oriented horizontally.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e179b-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e179b-140">See also</span></span>

- <xref:System.Windows.Forms.TextBox>
- <xref:System.Windows.Forms.TabControl>
- <xref:System.Windows.Forms.SplitContainer>
- <xref:System.ComponentModel.Design.DesignerActionList>
- <span data-ttu-id="e179b-141">[Procédure pas à pas : Ajout de balises actives à un composant de formulaires Windows](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/ms171829(v=vs.120))</span><span class="sxs-lookup"><span data-stu-id="e179b-141">[Walkthrough: Adding Smart Tags to a Windows Forms Component](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/ms171829(v=vs.120))</span></span>
