---
title: 'Procédure : imprimer un formulaire Windows'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Windows Forms, printing
- printing [Windows Forms]
- printing a form
- printing [Windows Forms], printing a form
ms.assetid: c8dff5f8-f56a-4c07-ae31-64643b31f8fc
ms.openlocfilehash: 85fb12028687578b76e0f16061deb9b9a4de70e3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62003975"
---
# <a name="how-to-print-a-windows-form"></a><span data-ttu-id="0e43b-102">Procédure : imprimer un formulaire Windows</span><span class="sxs-lookup"><span data-stu-id="0e43b-102">How to: Print a Windows Form</span></span>
<span data-ttu-id="0e43b-103">Dans le cadre du processus de développement, vous généralement intérêt à imprimer une copie de votre formulaire Windows.</span><span class="sxs-lookup"><span data-stu-id="0e43b-103">As part of the development process, you typically will want to print a copy of your Windows Form.</span></span> <span data-ttu-id="0e43b-104">L’exemple de code suivant montre comment imprimer une copie de l’écran actuel à l’aide de la <xref:System.Drawing.Graphics.CopyFromScreen%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="0e43b-104">The following code example shows how to print a copy of the current form by using the <xref:System.Drawing.Graphics.CopyFromScreen%2A> method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0e43b-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="0e43b-105">Example</span></span>  
 [!code-csharp[System.Drawing.Graphics.CopyFromScreen#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.Graphics.CopyFromScreen/CS/Form1.cs#1)]
 [!code-vb[System.Drawing.Graphics.CopyFromScreen#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.Graphics.CopyFromScreen/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="0e43b-106">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="0e43b-106">Compiling the Code</span></span>  
 <span data-ttu-id="0e43b-107">Il s’agit d’un exemple de code complet qui contient un `Main` (méthode).</span><span class="sxs-lookup"><span data-stu-id="0e43b-107">This is a complete code example that contains a `Main` method.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="0e43b-108">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="0e43b-108">Robust Programming</span></span>  
 <span data-ttu-id="0e43b-109">Les conditions ci-dessous peuvent générer une exception.</span><span class="sxs-lookup"><span data-stu-id="0e43b-109">The following conditions may cause an exception:</span></span>  
  
- <span data-ttu-id="0e43b-110">Vous n’êtes pas autorisé à accéder à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="0e43b-110">You do not have permission to access the printer.</span></span>  
  
- <span data-ttu-id="0e43b-111">Aucune imprimante n’est installée.</span><span class="sxs-lookup"><span data-stu-id="0e43b-111">There is no printer installed.</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="0e43b-112">Sécurité .NET Framework</span><span class="sxs-lookup"><span data-stu-id="0e43b-112">.NET Framework Security</span></span>  
 <span data-ttu-id="0e43b-113">Pour exécuter cet exemple de code, vous devez être autorisé à accéder à l’imprimante que vous utilisez avec votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0e43b-113">In order to run this code example, you must have permission to access the printer you use with your computer.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0e43b-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e43b-114">See also</span></span>

- <xref:System.Drawing.Printing.PrintDocument>
- [<span data-ttu-id="0e43b-115">Guide pratique pour Rendre des Images avec GDI +</span><span class="sxs-lookup"><span data-stu-id="0e43b-115">How to: Render Images with GDI+</span></span>](how-to-render-images-with-gdi.md)
- [<span data-ttu-id="0e43b-116">Guide pratique pour Imprimer des graphiques dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="0e43b-116">How to: Print Graphics in Windows Forms</span></span>](how-to-print-graphics-in-windows-forms.md)
