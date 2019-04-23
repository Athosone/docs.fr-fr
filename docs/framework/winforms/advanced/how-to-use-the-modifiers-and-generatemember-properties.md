---
title: 'Procédure : utiliser les modificateurs et les propriétés GenerateMember'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
f1_keywords:
- Designer_GenerateMember
- Designer_Modifiers
helpviewer_keywords:
- base forms
- inheritance [Windows Forms], forms
- inherited forms [Windows Forms], Windows Forms
- inherited forms
- form inheritance
- Windows Forms, inheritance
ms.assetid: 3381a5e4-e1a3-44e2-a765-a0b758937b85
ms.openlocfilehash: 6194ef288bd43267c2b00fa6d7c6250e90b37c75
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59322639"
---
# <a name="how-to-use-the-modifiers-and-generatemember-properties"></a><span data-ttu-id="7320c-102">Procédure : utiliser les modificateurs et les propriétés GenerateMember</span><span class="sxs-lookup"><span data-stu-id="7320c-102">How to: Use the Modifiers and GenerateMember Properties</span></span>
<span data-ttu-id="7320c-103">Lorsque vous placez un composant sur un formulaire Windows, les deux propriétés sont fournies par l’environnement de conception : `GenerateMember` et `Modifiers`.</span><span class="sxs-lookup"><span data-stu-id="7320c-103">When you place a component on a Windows Form, two properties are provided by the design environment: `GenerateMember` and `Modifiers`.</span></span> <span data-ttu-id="7320c-104">Le `GenerateMember` propriété spécifie quand le Concepteur de formulaires Windows génère une variable membre pour un composant.</span><span class="sxs-lookup"><span data-stu-id="7320c-104">The `GenerateMember` property specifies when the Windows Forms Designer generates a member variable for a component.</span></span> <span data-ttu-id="7320c-105">Le `Modifiers` propriété est le modificateur d’accès assigné à cette variable de membre.</span><span class="sxs-lookup"><span data-stu-id="7320c-105">The `Modifiers` property is the access modifier assigned to that member variable.</span></span> <span data-ttu-id="7320c-106">Si la valeur de la `GenerateMember` propriété est `false`, la valeur de la `Modifiers` propriété n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="7320c-106">If the value of the `GenerateMember` property is `false`, the value of the `Modifiers` property has no effect.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="7320c-107">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="7320c-107">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="7320c-108">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="7320c-108">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="7320c-109">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="7320c-109">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-specify-whether-a-component-is-a-member-of-the-form"></a><span data-ttu-id="7320c-110">Pour spécifier si un composant est un membre du formulaire</span><span class="sxs-lookup"><span data-stu-id="7320c-110">To specify whether a component is a member of the form</span></span>  
  
1. <span data-ttu-id="7320c-111">Dans le Concepteur de formulaires Windows, ouvrez votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="7320c-111">In the Windows Forms Designer, open your form.</span></span>  
  
2. <span data-ttu-id="7320c-112">Ouvrez le **boîte à outils**et sur le formulaire, placez trois <xref:System.Windows.Forms.Button> contrôles.</span><span class="sxs-lookup"><span data-stu-id="7320c-112">Open the **Toolbox**, and on the form, place three <xref:System.Windows.Forms.Button> controls.</span></span>  
  
3. <span data-ttu-id="7320c-113">Définir le `GenerateMember` et `Modifiers` propriétés pour chaque <xref:System.Windows.Forms.Button> contrôle conformément au tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7320c-113">Set the `GenerateMember` and `Modifiers` properties for each <xref:System.Windows.Forms.Button> control according to the following table.</span></span>  
  
    |<span data-ttu-id="7320c-114">Nom du bouton</span><span class="sxs-lookup"><span data-stu-id="7320c-114">Button name</span></span>|<span data-ttu-id="7320c-115">Valeur de GenerateMember</span><span class="sxs-lookup"><span data-stu-id="7320c-115">GenerateMember value</span></span>|<span data-ttu-id="7320c-116">Valeur de modificateurs</span><span class="sxs-lookup"><span data-stu-id="7320c-116">Modifiers value</span></span>|  
    |-----------------|--------------------------|---------------------|  
    |`button1`|`true`|`private`|  
    |`button2`|`true`|`protected`|  
    |`button3`|`false`|<span data-ttu-id="7320c-117">Aucune modification</span><span class="sxs-lookup"><span data-stu-id="7320c-117">No change</span></span>|  
  
4. <span data-ttu-id="7320c-118">Générez la solution.</span><span class="sxs-lookup"><span data-stu-id="7320c-118">Build the solution.</span></span>  
  
5. <span data-ttu-id="7320c-119">Dans l’**Explorateur de solutions**, cliquez sur le bouton **Afficher tous les fichiers**.</span><span class="sxs-lookup"><span data-stu-id="7320c-119">In **Solution Explorer**, click the **Show All Files** button.</span></span>  
  
6. <span data-ttu-id="7320c-120">Ouvrez le **Form1** nœud, puis, dans le **éditeur de Code**, ouvrez le **Form1.Designer.vb** ou **Form1.Designer.cs** fichier.</span><span class="sxs-lookup"><span data-stu-id="7320c-120">Open the **Form1** node, and in the **Code Editor**,open the **Form1.Designer.vb** or **Form1.Designer.cs** file.</span></span> <span data-ttu-id="7320c-121">Ce fichier contient le code émis par le Concepteur de formulaires Windows.</span><span class="sxs-lookup"><span data-stu-id="7320c-121">This file contains the code emitted by the Windows Forms Designer.</span></span>  
  
7. <span data-ttu-id="7320c-122">Trouver les déclarations pour les trois boutons.</span><span class="sxs-lookup"><span data-stu-id="7320c-122">Find the declarations for the three buttons.</span></span> <span data-ttu-id="7320c-123">L’exemple de code suivant montre les différences spécifiées par le `GenerateMember` et `Modifiers` propriétés.</span><span class="sxs-lookup"><span data-stu-id="7320c-123">The following code example shows the differences specified by the `GenerateMember` and `Modifiers` properties.</span></span>  
  
     [!code-csharp[System.Windows.Forms.GenerateMember#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.GenerateMember/CS/Form1.cs#3)]
     [!code-vb[System.Windows.Forms.GenerateMember#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.GenerateMember/VB/Form1.vb#3)]  
  
     [!code-csharp[System.Windows.Forms.GenerateMember#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.GenerateMember/CS/Form1.cs#2)]
     [!code-vb[System.Windows.Forms.GenerateMember#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.GenerateMember/VB/Form1.vb#2)]  
  
> [!NOTE]
>  <span data-ttu-id="7320c-124">Par défaut, le Concepteur de formulaires Windows attribue le `private` (`Friend` en Visual Basic) modificateur aux contrôles conteneur comme <xref:System.Windows.Forms.Panel>.</span><span class="sxs-lookup"><span data-stu-id="7320c-124">By default, the Windows Forms Designer assigns the `private` (`Friend` in Visual Basic) modifier to container controls like <xref:System.Windows.Forms.Panel>.</span></span> <span data-ttu-id="7320c-125">Si votre base de <xref:System.Windows.Forms.UserControl> ou <xref:System.Windows.Forms.Form> a un contrôle conteneur, il n’acceptera pas de nouveaux enfants dans les formulaires et contrôles hérités.</span><span class="sxs-lookup"><span data-stu-id="7320c-125">If your base <xref:System.Windows.Forms.UserControl> or <xref:System.Windows.Forms.Form> has a container control, it will not accept new children in inherited controls and forms.</span></span> <span data-ttu-id="7320c-126">La solution consiste à modifier le modificateur du contrôle conteneur de base à `protected` ou `public`.</span><span class="sxs-lookup"><span data-stu-id="7320c-126">The solution is to change the modifier of the base container control to `protected` or `public`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7320c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7320c-127">See also</span></span>

- <xref:System.Windows.Forms.Button>
- [<span data-ttu-id="7320c-128">Héritage visuel des Windows Forms</span><span class="sxs-lookup"><span data-stu-id="7320c-128">Windows Forms Visual Inheritance</span></span>](windows-forms-visual-inheritance.md)
- [<span data-ttu-id="7320c-129">Procédure pas à pas : Démonstration de l’héritage visuel</span><span class="sxs-lookup"><span data-stu-id="7320c-129">Walkthrough: Demonstrating Visual Inheritance</span></span>](walkthrough-demonstrating-visual-inheritance.md)
- [<span data-ttu-id="7320c-130">Guide pratique pour Hériter des Windows Forms</span><span class="sxs-lookup"><span data-stu-id="7320c-130">How to: Inherit Windows Forms</span></span>](how-to-inherit-windows-forms.md)
