---
title: 'Procédure : définir le texte affiché par un contrôle Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Windows Forms, captions
- Button control [Windows Forms], button text
- StdFont object and CommandButton caption
- captions [Windows Forms], Windows Forms controls
- Text property [Windows Forms], Windows Forms control
- Button control [Windows Forms], text display
- labels [Windows Forms], adding to CommandButton control
- buttons [Windows Forms], text
- captions [Windows Forms], setting
- text
- examples [Windows Forms], controls
- text [Windows Forms], Windows Forms controls
- controls [Windows Forms], captions
- forms [Windows Forms], captions
ms.assetid: 36b95bff-8780-479d-b86a-f1a0673653aa
ms.openlocfilehash: 59570af89e6236e3c13866d45dc5361d52b84274
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59308521"
---
# <a name="how-to-set-the-text-displayed-by-a-windows-forms-control"></a><span data-ttu-id="01589-102">Procédure : définir le texte affiché par un contrôle Windows Forms</span><span class="sxs-lookup"><span data-stu-id="01589-102">How to: Set the Text Displayed by a Windows Forms Control</span></span>
<span data-ttu-id="01589-103">Généralement, les contrôles Windows Forms affichent du texte en rapport avec la fonction principale du contrôle.</span><span class="sxs-lookup"><span data-stu-id="01589-103">Windows Forms controls usually display some text that is related to the primary function of the control.</span></span> <span data-ttu-id="01589-104">Par exemple, un contrôle <xref:System.Windows.Forms.Button> affiche habituellement une légende indiquant l'action à exécuter quand le bouton est activé.</span><span class="sxs-lookup"><span data-stu-id="01589-104">For example, a <xref:System.Windows.Forms.Button> control usually displays a caption indicating what action will be performed when the button is clicked.</span></span> <span data-ttu-id="01589-105">Pour tous les contrôles, vous pouvez définir ou retourner le texte à l'aide de la propriété <xref:System.Windows.Forms.Control.Text%2A>.</span><span class="sxs-lookup"><span data-stu-id="01589-105">For all controls, you can set or return the text by using the <xref:System.Windows.Forms.Control.Text%2A> property.</span></span> <span data-ttu-id="01589-106">Vous pouvez modifier la police en utilisant la propriété <xref:System.Windows.Forms.Control.Font%2A>.</span><span class="sxs-lookup"><span data-stu-id="01589-106">You can change the font by using the <xref:System.Windows.Forms.Control.Font%2A> property.</span></span> <span data-ttu-id="01589-107">Vous pouvez également définir le texte à l'aide du concepteur.</span><span class="sxs-lookup"><span data-stu-id="01589-107">You can also set the text using the designer.</span></span>  <span data-ttu-id="01589-108">Voir également [Guide pratique pour Créer des touches d’accès rapide pour Windows Forms à l’aide du Concepteur de contrôles](how-to-create-access-keys-for-windows-forms-controls-using-the-designer.md), [Comment : Définir le texte affiché par un Windows Forms à l’aide du Concepteur de contrôle](how-to-set-the-text-displayed-by-a-windows-forms-control-using-the-designer.md), [Comment : Définir l’Image affichée par un Windows Forms à l’aide du Concepteur de contrôle](how-to-set-the-image-displayed-by-a-windows-forms-control-using-the-designer.md).</span><span class="sxs-lookup"><span data-stu-id="01589-108">Also see [How to: Create Access Keys for Windows Forms Controls Using the Designer](how-to-create-access-keys-for-windows-forms-controls-using-the-designer.md), [How to: Set the Text Displayed by a Windows Forms Control Using the Designer](how-to-set-the-text-displayed-by-a-windows-forms-control-using-the-designer.md), [How to: Set the Image Displayed by a Windows Forms Control Using the Designer](how-to-set-the-image-displayed-by-a-windows-forms-control-using-the-designer.md).</span></span>  
  
### <a name="to-set-the-text-displayed-by-a-control-programmatically"></a><span data-ttu-id="01589-109">Pour définir le texte affiché par un contrôle par programmation</span><span class="sxs-lookup"><span data-stu-id="01589-109">To set the text displayed by a control programmatically</span></span>  
  
1. <span data-ttu-id="01589-110">Affectez une chaîne comme valeur de la propriété <xref:System.Windows.Forms.Control.Text%2A>.</span><span class="sxs-lookup"><span data-stu-id="01589-110">Set the <xref:System.Windows.Forms.Control.Text%2A> property to a string.</span></span>  
  
     <span data-ttu-id="01589-111">Pour créer une clé d’accès soulignée, incluez une esperluette (&) avant la lettre qui sera la clé d’accès.</span><span class="sxs-lookup"><span data-stu-id="01589-111">To create an underlined access key, includes an ampersand (&) before the letter that will be the access key.</span></span>  
  
2. <span data-ttu-id="01589-112">Affectez un objet de type <xref:System.Drawing.Font> comme valeur de la propriété <xref:System.Windows.Forms.Control.Font%2A>.</span><span class="sxs-lookup"><span data-stu-id="01589-112">Set the <xref:System.Windows.Forms.Control.Font%2A> property to an object of type <xref:System.Drawing.Font>.</span></span>  
  
    ```vb  
    Button1.Text = "Click here to save changes"  
    Button1.Font = New Font("Arial", 10, FontStyle.Bold, GraphicsUnit.Point)  
    ```  
  
    ```csharp  
    button1.Text = "Click here to save changes";  
    button1.Font = new Font("Arial", 10, FontStyle.Bold,  
       GraphicsUnit.Point);  
    ```  
  
    ```cpp  
    button1->Text = "Click here to save changes";  
    button1->Font = new System::Drawing::Font("Arial",  
       10, FontStyle::Bold, GraphicsUnit::Point);  
    ```  
  
    > [!NOTE]
    >  <span data-ttu-id="01589-113">Vous pouvez utiliser un caractère d'échappement pour afficher un caractère spécial dans des éléments d'interface utilisateur qui l'interpréteraient normalement différemment, tels que des éléments de menu.</span><span class="sxs-lookup"><span data-stu-id="01589-113">You can use an escape character to display a special character in user-interface elements that would normally interpret them differently, such as menu items.</span></span> <span data-ttu-id="01589-114">Par exemple, la ligne de code suivante définit le texte de l’élément de menu à lire « & Now For Something complètement différent » :</span><span class="sxs-lookup"><span data-stu-id="01589-114">For example, the following line of code sets the menu item's text to read "& Now For Something Completely Different":</span></span>  
  
    ```vb  
    MPMenuItem.Text = "&& Now For Something Completely Different"  
    ```  
  
    ```csharp  
    mpMenuItem.Text = "&& Now For Something Completely Different";  
    ```  
  
    ```cpp  
    mpMenuItem->Text = "&& Now For Something Completely Different";  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="01589-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01589-115">See also</span></span>

- <xref:System.Windows.Forms.Control.Text%2A?displayProperty=nameWithType>
- [<span data-ttu-id="01589-116">Guide pratique pour Créer des clés d’accès pour les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="01589-116">How to: Create Access Keys for Windows Forms Controls</span></span>](how-to-create-access-keys-for-windows-forms-controls.md)
- [<span data-ttu-id="01589-117">Guide pratique pour Répondre aux clics de bouton Windows Forms</span><span class="sxs-lookup"><span data-stu-id="01589-117">How to: Respond to Windows Forms Button Clicks</span></span>](how-to-respond-to-windows-forms-button-clicks.md)
