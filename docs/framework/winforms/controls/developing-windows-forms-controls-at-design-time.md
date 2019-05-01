---
title: Développement de contrôles Windows Forms au moment du design
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms controls [Windows Forms]
- Windows Forms controls, creating
- controls [Windows Forms]
- controls [Windows Forms], creating
- user controls [Windows Forms]
- custom controls [Windows Forms]
ms.assetid: e5a8e088-7ec8-4fd9-bcb3-9078fd134829
ms.openlocfilehash: 641a6c1c99169c6836c33b3e84b2ae02aba298d2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61972235"
---
# <a name="developing-windows-forms-controls-at-design-time"></a><span data-ttu-id="05bdb-102">Développement de contrôles Windows Forms au moment du design</span><span class="sxs-lookup"><span data-stu-id="05bdb-102">Developing Windows Forms Controls at Design Time</span></span>
<span data-ttu-id="05bdb-103">Pour les auteurs de contrôles, le .NET Framework fournit une multitude de technologies de création de contrôles.</span><span class="sxs-lookup"><span data-stu-id="05bdb-103">For control authors, the .NET Framework provides a wealth of control authoring technology.</span></span> <span data-ttu-id="05bdb-104">Les auteurs ne sont plus contraints de concevoir des contrôles composites qui agissent en tant que collection de contrôles préexistants.</span><span class="sxs-lookup"><span data-stu-id="05bdb-104">Authors are no longer limited to designing composite controls that act as a collection of preexisting controls.</span></span> <span data-ttu-id="05bdb-105">À travers l’héritage, vous pouvez créer vos propres contrôles à partir de contrôles composites ou de contrôles Windows Forms préexistants.</span><span class="sxs-lookup"><span data-stu-id="05bdb-105">Through inheritance, you can create your own controls from preexisting composite controls or preexisting Windows Forms controls.</span></span> <span data-ttu-id="05bdb-106">Vous pouvez également concevoir vos propres contrôles qui implémentent un dessin personnalisé.</span><span class="sxs-lookup"><span data-stu-id="05bdb-106">You can also design your own controls that implement custom painting.</span></span> <span data-ttu-id="05bdb-107">Ces options permettent une grande souplesse dans la conception et les fonctionnalités de l’interface visuelle.</span><span class="sxs-lookup"><span data-stu-id="05bdb-107">These options enable a great deal of flexibility to the design and functionality of the visual interface.</span></span> <span data-ttu-id="05bdb-108">Pour tirer parti de ces fonctionnalités, vous devez bien connaître les concepts de la programmation orientée objet.</span><span class="sxs-lookup"><span data-stu-id="05bdb-108">To take advantage of these features, you should be familiar with object-based programming concepts.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="05bdb-109">Il n’est pas nécessaire d’avoir une connaissance approfondie de l’héritage, mais il peut s’avérer utile pour faire référence à [fondamentaux de l’héritage (Visual Basic)](~/docs/visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md).</span><span class="sxs-lookup"><span data-stu-id="05bdb-109">It is not necessary to have a thorough understanding of inheritance, but you may find it useful to refer to [Inheritance basics (Visual Basic)](~/docs/visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md).</span></span>  
  
 <span data-ttu-id="05bdb-110">Si vous voulez créer des contrôle personnalisés à utiliser sur des Web Forms, consultez [Développement de contrôles serveur ASP.NET personnalisés](https://docs.microsoft.com/previous-versions/aspnet/zt27tfhy(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="05bdb-110">If you want to create custom controls to use on Web Forms, see [Developing Custom ASP.NET Server Controls](https://docs.microsoft.com/previous-versions/aspnet/zt27tfhy(v=vs.100)).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="05bdb-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="05bdb-111">In This Section</span></span>  
 [<span data-ttu-id="05bdb-112">Procédure pas à pas : Création d’un contrôle Composite avec Visual Basic</span><span class="sxs-lookup"><span data-stu-id="05bdb-112">Walkthrough: Authoring a Composite Control with Visual Basic</span></span>](walkthrough-authoring-a-composite-control-with-visual-basic.md)  
 <span data-ttu-id="05bdb-113">Montre comment créer un contrôle composite simple dans Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="05bdb-113">Shows how to create a simple composite control in Visual Basic.</span></span>  
  
 [<span data-ttu-id="05bdb-114">Procédure pas à pas : Création d’un contrôle Composite avec VisualC#</span><span class="sxs-lookup"><span data-stu-id="05bdb-114">Walkthrough: Authoring a Composite Control with Visual C#</span></span>](walkthrough-authoring-a-composite-control-with-visual-csharp.md)  
 <span data-ttu-id="05bdb-115">Montre comment créer un contrôle composite simple dans C#.</span><span class="sxs-lookup"><span data-stu-id="05bdb-115">Shows how to create a simple composite control in C#.</span></span>  
  
 [<span data-ttu-id="05bdb-116">Procédure pas à pas : Héritage d’un contrôle de formulaire Windows avec Visual Basic</span><span class="sxs-lookup"><span data-stu-id="05bdb-116">Walkthrough: Inheriting from a Windows Forms Control with Visual Basic</span></span>](walkthrough-inheriting-from-a-windows-forms-control-with-visual-basic.md)  
 <span data-ttu-id="05bdb-117">Montre comment créer un contrôle Windows Forms simple à l’aide de l’héritage dans Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="05bdb-117">Shows how to create a simple Windows Forms control using inheritance in Visual Basic.</span></span>  
  
 [<span data-ttu-id="05bdb-118">Procédure pas à pas : Héritage d’un contrôle de formulaire Windows avec VisualC#</span><span class="sxs-lookup"><span data-stu-id="05bdb-118">Walkthrough: Inheriting from a Windows Forms Control with Visual C#</span></span>](walkthrough-inheriting-from-a-windows-forms-control-with-visual-csharp.md)  
 <span data-ttu-id="05bdb-119">Montre comment créer un contrôle Windows Forms simple à l’aide de l’héritage dans C#.</span><span class="sxs-lookup"><span data-stu-id="05bdb-119">Shows how to create a simple Windows Forms control using inheritance in C#.</span></span>  
  
 [<span data-ttu-id="05bdb-120">Procédure pas à pas : Effectuer des tâches courantes à l’aide d’intelligent des balises sur Windows Forms contrôles</span><span class="sxs-lookup"><span data-stu-id="05bdb-120">Walkthrough: Performing Common Tasks Using Smart Tags on Windows Forms Controls</span></span>](performing-common-tasks-using-smart-tags-on-wf-controls.md)  
 <span data-ttu-id="05bdb-121">Montre comment utiliser la fonctionnalité de balise active sur les contrôles Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="05bdb-121">Shows how to use the smart tag feature on Windows Forms controls.</span></span>  
  
 [<span data-ttu-id="05bdb-122">Procédure pas à pas : Sérialisation des Collections de Types Standard avec DesignerSerializationVisibilityAttribute</span><span class="sxs-lookup"><span data-stu-id="05bdb-122">Walkthrough: Serializing Collections of Standard Types with the DesignerSerializationVisibilityAttribute</span></span>](serializing-collections-designerserializationvisibilityattribute.md)  
 <span data-ttu-id="05bdb-123">Montre comment utiliser le <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute.Content?displayProperty=nameWithType> attribut pour sérialiser une collection.</span><span class="sxs-lookup"><span data-stu-id="05bdb-123">Shows how to use the <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute.Content?displayProperty=nameWithType> attribute to serialize a collection.</span></span>  
  
 [<span data-ttu-id="05bdb-124">Procédure pas à pas : Débogage des contrôles Windows Forms personnalisés au moment du design</span><span class="sxs-lookup"><span data-stu-id="05bdb-124">Walkthrough: Debugging Custom Windows Forms Controls at Design Time</span></span>](walkthrough-debugging-custom-windows-forms-controls-at-design-time.md)  
 <span data-ttu-id="05bdb-125">Montre comment déboguer le comportement au moment du design de votre contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="05bdb-125">Shows how to debug the design-time behavior of a Windows Forms control.</span></span>  
  
 [<span data-ttu-id="05bdb-126">Procédure pas à pas : Création d’un contrôle de formulaire Windows qui tire parti des fonctionnalités au moment du Design de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="05bdb-126">Walkthrough: Creating a Windows Forms Control That Takes Advantage of Visual Studio Design-Time Features</span></span>](creating-a-wf-control-design-time-features.md)  
 <span data-ttu-id="05bdb-127">Montre comment intégrer étroitement un contrôle composite dans l’environnement de conception.</span><span class="sxs-lookup"><span data-stu-id="05bdb-127">Shows how to tightly integrate a composite control into the design environment.</span></span>  
  
 [<span data-ttu-id="05bdb-128">Guide pratique pour Créer des contrôles pour les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="05bdb-128">How to: Author Controls for Windows Forms</span></span>](how-to-author-controls-for-windows-forms.md)  
 <span data-ttu-id="05bdb-129">Fournit une vue d’ensemble des considérations pour l’implémentation d’un contrôle Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="05bdb-129">Provides an overview of considerations for implementing a Windows Forms control.</span></span>  
  
 [<span data-ttu-id="05bdb-130">Guide pratique pour Créer des contrôles composites</span><span class="sxs-lookup"><span data-stu-id="05bdb-130">How to: Author Composite Controls</span></span>](how-to-author-composite-controls.md)  
 <span data-ttu-id="05bdb-131">Montre comment créer un contrôle en héritant d’un contrôle composite.</span><span class="sxs-lookup"><span data-stu-id="05bdb-131">Shows how to create a control by inheriting from a composite control.</span></span>  
  
 [<span data-ttu-id="05bdb-132">Guide pratique pour Hériter de la classe UserControl</span><span class="sxs-lookup"><span data-stu-id="05bdb-132">How to: Inherit from the UserControl Class</span></span>](how-to-inherit-from-the-usercontrol-class.md)  
 <span data-ttu-id="05bdb-133">Fournit une vue d’ensemble de la procédure de création d’un contrôle composite.</span><span class="sxs-lookup"><span data-stu-id="05bdb-133">Provides an overview of the procedure for creating a composite control.</span></span>  
  
 [<span data-ttu-id="05bdb-134">Guide pratique pour Windows existant hériter de contrôles de formulaires</span><span class="sxs-lookup"><span data-stu-id="05bdb-134">How to: Inherit from Existing Windows Forms Controls</span></span>](how-to-inherit-from-existing-windows-forms-controls.md)  
 <span data-ttu-id="05bdb-135">Montre comment créer un contrôle étendu en héritant de la <xref:System.Windows.Forms.Button> classe de contrôle.</span><span class="sxs-lookup"><span data-stu-id="05bdb-135">Shows how to create an extended control by inheriting from the <xref:System.Windows.Forms.Button> control class.</span></span>  
  
 [<span data-ttu-id="05bdb-136">Guide pratique pour Héritez de la classe de contrôle</span><span class="sxs-lookup"><span data-stu-id="05bdb-136">How to: Inherit from the Control Class</span></span>](how-to-inherit-from-the-control-class.md)  
 <span data-ttu-id="05bdb-137">Fournit une vue d’ensemble de la création d’un contrôle étendu.</span><span class="sxs-lookup"><span data-stu-id="05bdb-137">Provides an overview of creating an extended control.</span></span>  
  
 [<span data-ttu-id="05bdb-138">Guide pratique pour Aligner un contrôle sur les bords des formulaires au moment du Design</span><span class="sxs-lookup"><span data-stu-id="05bdb-138">How to: Align a Control to the Edges of Forms at Design Time</span></span>](how-to-align-a-control-to-the-edges-of-forms-at-design-time.md)  
 <span data-ttu-id="05bdb-139">Montre comment utiliser le <xref:System.Windows.Forms.Control.Dock%2A> propriété pour aligner votre contrôle sur le bord du formulaire qu’il occupe.</span><span class="sxs-lookup"><span data-stu-id="05bdb-139">Shows how to use the <xref:System.Windows.Forms.Control.Dock%2A> property to align your control to the edge of the form it occupies.</span></span>  
  
 [<span data-ttu-id="05bdb-140">Guide pratique pour Afficher un contrôle dans la boîte de dialogue de boîte à outils éléments choisir</span><span class="sxs-lookup"><span data-stu-id="05bdb-140">How to: Display a Control in the Choose Toolbox Items Dialog Box</span></span>](how-to-display-a-control-in-the-choose-toolbox-items-dialog-box.md)  
 <span data-ttu-id="05bdb-141">Montre la procédure d’installation de votre contrôle afin qu’il apparaisse dans la boîte de dialogue **Personnaliser la boîte à outils**.</span><span class="sxs-lookup"><span data-stu-id="05bdb-141">Shows the procedure for installing your control so that it appears in the **Customize Toolbox** dialog box.</span></span>  
  
 [<span data-ttu-id="05bdb-142">Guide pratique pour Fournir une Bitmap de boîte à outils pour un contrôle</span><span class="sxs-lookup"><span data-stu-id="05bdb-142">How to: Provide a Toolbox Bitmap for a Control</span></span>](how-to-provide-a-toolbox-bitmap-for-a-control.md)  
 <span data-ttu-id="05bdb-143">Montre comment utiliser le <xref:System.Drawing.ToolboxBitmapAttribute> pour afficher une icône en regard de votre contrôle personnalisé dans le **boîte à outils**.</span><span class="sxs-lookup"><span data-stu-id="05bdb-143">Shows how to use the <xref:System.Drawing.ToolboxBitmapAttribute> to display an icon next to your custom control in the **Toolbox**.</span></span>  
  
 [<span data-ttu-id="05bdb-144">Guide pratique pour Tester le comportement au moment de l’exécution d’un UserControl</span><span class="sxs-lookup"><span data-stu-id="05bdb-144">How to: Test the Run-Time Behavior of a UserControl</span></span>](how-to-test-the-run-time-behavior-of-a-usercontrol.md)  
 <span data-ttu-id="05bdb-145">Montre comment utiliser le **conteneur de test UserControl** pour tester le comportement d’un contrôle composite.</span><span class="sxs-lookup"><span data-stu-id="05bdb-145">Shows how to use the **UserControl Test Container** to test the behavior of a composite control.</span></span>  
  
 [<span data-ttu-id="05bdb-146">Erreurs au moment du design dans le Concepteur Windows Forms</span><span class="sxs-lookup"><span data-stu-id="05bdb-146">Design-Time Errors in the Windows Forms Designer</span></span>](design-time-errors-in-the-windows-forms-designer.md)  
 <span data-ttu-id="05bdb-147">Explique la signification et l’utilisation de la liste d’erreurs au moment du design qui apparaît dans Microsoft Visual Studio en cas d’échec du chargement du Concepteur Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="05bdb-147">Explains the meaning and use of the Design-Time Error List that appears in Microsoft Visual Studio when the Windows Forms designer fails to load.</span></span>  
  
 [<span data-ttu-id="05bdb-148">Dépannage de la création de contrôles et de composants</span><span class="sxs-lookup"><span data-stu-id="05bdb-148">Troubleshooting Control and Component Authoring</span></span>](troubleshooting-control-and-component-authoring.md)  
 <span data-ttu-id="05bdb-149">Montre comment diagnostiquer et résoudre les problèmes courants qui peuvent se produire quand vous créez un composant ou un contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="05bdb-149">Shows how to diagnose and fix common issues that can occur when you author a custom component or control.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="05bdb-150">Référence</span><span class="sxs-lookup"><span data-stu-id="05bdb-150">Reference</span></span>  
 <xref:System.Windows.Forms.Control?displayProperty=nameWithType>  
 <span data-ttu-id="05bdb-151">Décrit cette classe et propose des liens vers tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="05bdb-151">Describes this class and has links to all of its members.</span></span>  
  
 <xref:System.Windows.Forms.UserControl?displayProperty=nameWithType>  
 <span data-ttu-id="05bdb-152">Décrit cette classe et propose des liens vers tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="05bdb-152">Describes this class and has links to all of its members.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="05bdb-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="05bdb-153">Related Sections</span></span>  
 [<span data-ttu-id="05bdb-154">Développement de contrôles Windows Forms personnalisés avec le .NET Framework</span><span class="sxs-lookup"><span data-stu-id="05bdb-154">Developing Custom Windows Forms Controls with the .NET Framework</span></span>](developing-custom-windows-forms-controls.md)  
 <span data-ttu-id="05bdb-155">Explique comment créer vos propres contrôles personnalisés avec le .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="05bdb-155">Discusses how to create your own custom controls with the .NET Framework.</span></span>  
  
 [<span data-ttu-id="05bdb-156">Indépendance du langage et composants indépendants du langage</span><span class="sxs-lookup"><span data-stu-id="05bdb-156">Language Independence and Language-Independent Components</span></span>](../../../standard/language-independence-and-language-independent-components.md)  
 <span data-ttu-id="05bdb-157">Présente le common language runtime, qui est conçu pour simplifier la création et l’utilisation des composants.</span><span class="sxs-lookup"><span data-stu-id="05bdb-157">Introduces the common language runtime, which is designed to simplify the creation and use of components.</span></span> <span data-ttu-id="05bdb-158">Un aspect important de cette simplification est l’interopérabilité améliorée entre les composants écrits à l’aide de différents langages de programmation.</span><span class="sxs-lookup"><span data-stu-id="05bdb-158">An important aspect of this simplification is enhanced interoperability between components written using different programming languages.</span></span> <span data-ttu-id="05bdb-159">La Common Language Specification (CLS) permet de créer des outils et composants fonctionnant avec plusieurs langages de programmation.</span><span class="sxs-lookup"><span data-stu-id="05bdb-159">The Common Language Specification (CLS) makes it possible to create tools and components that work with multiple programming languages.</span></span>  
  
 [<span data-ttu-id="05bdb-160">Procédure pas à pas : Remplissage automatique de la boîte à outils avec des composants personnalisés</span><span class="sxs-lookup"><span data-stu-id="05bdb-160">Walkthrough: Automatically Populating the Toolbox with Custom Components</span></span>](walkthrough-automatically-populating-the-toolbox-with-custom-components.md)  
 <span data-ttu-id="05bdb-161">Décrit comment activer l’affichage de votre composant ou de votre contrôle dans la boîte de dialogue **Personnaliser la boîte à outils**.</span><span class="sxs-lookup"><span data-stu-id="05bdb-161">Describes how to enable your component or control to be displayed in the **Customize Toolbox** dialog box.</span></span>
