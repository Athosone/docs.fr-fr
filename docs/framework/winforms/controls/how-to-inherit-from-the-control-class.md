---
title: 'Procédure : hériter de la classe Control'
ms.date: 03/30/2017
helpviewer_keywords:
- inheritance [Windows Forms], Windows Forms custom controls
- Control class [Windows Forms], inheriting from
- custom controls [Windows Forms], inheritance
- OnPaint method [Windows Forms]
- custom controls [Windows Forms], creating
ms.assetid: 46ba0df3-5cf7-443c-a3b4-a72660172476
ms.openlocfilehash: 14f225f5587379b3efa7b6dc2475f1b697ebb281
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61941139"
---
# <a name="how-to-inherit-from-the-control-class"></a><span data-ttu-id="39de4-102">Procédure : hériter de la classe Control</span><span class="sxs-lookup"><span data-stu-id="39de4-102">How to: Inherit from the Control Class</span></span>
<span data-ttu-id="39de4-103">Si vous souhaitez créer un contrôle entièrement personnalisé à utiliser sur un formulaire Windows, vous devez hériter de la <xref:System.Windows.Forms.Control> classe.</span><span class="sxs-lookup"><span data-stu-id="39de4-103">If you want to create a completely custom control to use on a Windows Form, you should inherit from the <xref:System.Windows.Forms.Control> class.</span></span> <span data-ttu-id="39de4-104">Tout en héritant de la <xref:System.Windows.Forms.Control> classe nécessite que vous effectuer davantage de planification et de l’implémentation, il vous fournit également la plus grande plage d’options.</span><span class="sxs-lookup"><span data-stu-id="39de4-104">While inheriting from the <xref:System.Windows.Forms.Control> class requires that you perform more planning and implementation, it also provides you with the largest range of options.</span></span> <span data-ttu-id="39de4-105">Lorsque vous héritez de <xref:System.Windows.Forms.Control>, vous héritez des fonctionnalités très basique qui facilite le travail de contrôles.</span><span class="sxs-lookup"><span data-stu-id="39de4-105">When inheriting from <xref:System.Windows.Forms.Control>, you inherit the very basic functionality that makes controls work.</span></span> <span data-ttu-id="39de4-106">Les fonctionnalités inhérentes à la <xref:System.Windows.Forms.Control> classe gère l’entrée utilisateur via le clavier et de la souris, définissent les limites et la taille du contrôle, fournit un handle windows et fournit la gestion des messages et la sécurité.</span><span class="sxs-lookup"><span data-stu-id="39de4-106">The functionality inherent in the <xref:System.Windows.Forms.Control> class handles user input through the keyboard and mouse, defines the bounds and size of the control, provides a windows handle, and provides message handling and security.</span></span> <span data-ttu-id="39de4-107">Elles n’intègrent pas la peinture, qui désigne ici le rendu réel de l’interface graphique du contrôle, ni les fonctionnalités d’interaction utilisateur spécifiques.</span><span class="sxs-lookup"><span data-stu-id="39de4-107">It does not incorporate any painting, which in this case is the actual rendering of the graphical interface of the control, nor does it incorporate any specific user interaction functionality.</span></span> <span data-ttu-id="39de4-108">Vous devez fournir tous ces aspects par le biais de code personnalisé.</span><span class="sxs-lookup"><span data-stu-id="39de4-108">You must provide all of these aspects through custom code.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="39de4-109">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="39de4-109">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="39de4-110">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="39de4-110">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="39de4-111">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="39de4-111">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-create-a-custom-control"></a><span data-ttu-id="39de4-112">Pour créer un contrôle personnalisé</span><span class="sxs-lookup"><span data-stu-id="39de4-112">To create a custom control</span></span>  
  
1. <span data-ttu-id="39de4-113">Créez un projet d’**application Windows** ou de **bibliothèque de contrôles Windows**.</span><span class="sxs-lookup"><span data-stu-id="39de4-113">Create a new **Windows Application** or **Windows Control Library** project.</span></span>  
  
2. <span data-ttu-id="39de4-114">Dans le menu **Projet** , choisissez **Ajouter une classe**.</span><span class="sxs-lookup"><span data-stu-id="39de4-114">From the **Project** menu, choose **Add Class**.</span></span>  
  
3. <span data-ttu-id="39de4-115">Dans la boîte de dialogue **Ajouter un nouvel élément**, cliquez sur **Contrôle personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="39de4-115">In the **Add New Item** dialog box, click **Custom Control**.</span></span>  
  
     <span data-ttu-id="39de4-116">Un nouveau contrôle personnalisé est ajouté à votre projet.</span><span class="sxs-lookup"><span data-stu-id="39de4-116">A new custom control is added to your project.</span></span>  
  
4. <span data-ttu-id="39de4-117">Appuyez sur F7 pour ouvrir l’**éditeur de code** de votre contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="39de4-117">Press F7 to open the **Code Editor** for your custom control.</span></span>  
  
5. <span data-ttu-id="39de4-118">Recherchez le <xref:System.Windows.Forms.Control.OnPaint%2A> (méthode), qui doit être vide à l’exception d’un appel à la <xref:System.Windows.Forms.Control.OnPaint%2A> méthode de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="39de4-118">Locate the <xref:System.Windows.Forms.Control.OnPaint%2A> method, which will be empty except for a call to the <xref:System.Windows.Forms.Control.OnPaint%2A> method of the base class.</span></span>  
  
6. <span data-ttu-id="39de4-119">Modifiez le code afin d’incorporer la peinture personnalisée pour votre contrôle.</span><span class="sxs-lookup"><span data-stu-id="39de4-119">Modify the code to incorporate any custom painting you want for your control.</span></span>  
  
     <span data-ttu-id="39de4-120">Pour plus d’informations sur l’écriture de code permettant d’afficher des graphiques concernant les contrôles, consultez [Peinture et rendu personnalisés des contrôles](custom-control-painting-and-rendering.md).</span><span class="sxs-lookup"><span data-stu-id="39de4-120">For information about writing code to render graphics for controls, see [Custom Control Painting and Rendering](custom-control-painting-and-rendering.md).</span></span>  
  
7. <span data-ttu-id="39de4-121">Implémentez les méthodes, les propriétés ou les événements personnalisés que votre contrôle intégrera.</span><span class="sxs-lookup"><span data-stu-id="39de4-121">Implement any custom methods, properties, or events that your control will incorporate.</span></span>  
  
8. <span data-ttu-id="39de4-122">Enregistrez et testez votre contrôle.</span><span class="sxs-lookup"><span data-stu-id="39de4-122">Save and test your control.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="39de4-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39de4-123">See also</span></span>

- [<span data-ttu-id="39de4-124">Variétés de contrôles personnalisés</span><span class="sxs-lookup"><span data-stu-id="39de4-124">Varieties of Custom Controls</span></span>](varieties-of-custom-controls.md)
- [<span data-ttu-id="39de4-125">Guide pratique pour Hériter de la classe UserControl</span><span class="sxs-lookup"><span data-stu-id="39de4-125">How to: Inherit from the UserControl Class</span></span>](how-to-inherit-from-the-usercontrol-class.md)
- [<span data-ttu-id="39de4-126">Guide pratique pour Windows existant hériter de contrôles de formulaires</span><span class="sxs-lookup"><span data-stu-id="39de4-126">How to: Inherit from Existing Windows Forms Controls</span></span>](how-to-inherit-from-existing-windows-forms-controls.md)
- [<span data-ttu-id="39de4-127">Guide pratique pour Créer des contrôles pour les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="39de4-127">How to: Author Controls for Windows Forms</span></span>](how-to-author-controls-for-windows-forms.md)
- [<span data-ttu-id="39de4-128">Dépannage des gestionnaires d’événements hérités en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="39de4-128">Troubleshooting Inherited Event Handlers in Visual Basic</span></span>](~/docs/visual-basic/programming-guide/language-features/events/troubleshooting-inherited-event-handlers.md)
- [<span data-ttu-id="39de4-129">Développement de contrôles Windows Forms au moment du design</span><span class="sxs-lookup"><span data-stu-id="39de4-129">Developing Windows Forms Controls at Design Time</span></span>](developing-windows-forms-controls-at-design-time.md)
