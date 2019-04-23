---
title: 'Procédure : afficher l’heure avec le contrôle DateTimePicker'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- time [Windows Forms], displaying in DateTimePicker control
- examples [Windows Forms], DateTimePicker control
- DateTimePicker control [Windows Forms], displaying time
ms.assetid: 0c1c8b40-1b50-4301-a90c-39516775ccb1
ms.openlocfilehash: 7906811d5a324ba3f2bd73cc057298e007ac311b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59329854"
---
# <a name="how-to-display-time-with-the-datetimepicker-control"></a><span data-ttu-id="a2712-102">Procédure : afficher l’heure avec le contrôle DateTimePicker</span><span class="sxs-lookup"><span data-stu-id="a2712-102">How to: Display Time with the DateTimePicker Control</span></span>
<span data-ttu-id="a2712-103">Si vous souhaitez que votre application permette aux utilisateurs de sélectionner une date et une heure et qu'elle affiche la date et l'heure au format spécifié, utilisez le contrôle <xref:System.Windows.Forms.DateTimePicker>.</span><span class="sxs-lookup"><span data-stu-id="a2712-103">If you want your application to enable users to select a date and time, and to display that date and time in the specified format, use the <xref:System.Windows.Forms.DateTimePicker> control.</span></span> <span data-ttu-id="a2712-104">La procédure suivante montre comment utiliser le contrôle <xref:System.Windows.Forms.DateTimePicker> pour afficher l'heure.</span><span class="sxs-lookup"><span data-stu-id="a2712-104">The following procedure shows how to use the <xref:System.Windows.Forms.DateTimePicker> control to display the time.</span></span>  
  
### <a name="to-display-the-time-with-the-datetimepicker-control"></a><span data-ttu-id="a2712-105">Pour afficher l'heure avec le contrôle DateTimePicker</span><span class="sxs-lookup"><span data-stu-id="a2712-105">To display the time with the DateTimePicker control</span></span>  
  
1. <span data-ttu-id="a2712-106">Affectez à la propriété <xref:System.Windows.Forms.DateTimePicker.Format%2A> la valeur <xref:System.Windows.Forms.DateTimePickerFormat.Time></span><span class="sxs-lookup"><span data-stu-id="a2712-106">Set the <xref:System.Windows.Forms.DateTimePicker.Format%2A> property to <xref:System.Windows.Forms.DateTimePickerFormat.Time></span></span>  
  
     [!code-csharp[System.Windows.Forms.DateTimePickerTimeOnly#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DateTimePickerTimeOnly/CS/Form1.cs#2)]
     [!code-vb[System.Windows.Forms.DateTimePickerTimeOnly#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DateTimePickerTimeOnly/VB/Form1.vb#2)]  
  
2. <span data-ttu-id="a2712-107">Affectez à la propriété <xref:System.Windows.Forms.DateTimePicker.ShowUpDown%2A> de <xref:System.Windows.Forms.DateTimePicker> la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="a2712-107">Set the <xref:System.Windows.Forms.DateTimePicker.ShowUpDown%2A> property for the <xref:System.Windows.Forms.DateTimePicker> to `true`.</span></span>  
  
     [!code-csharp[System.Windows.Forms.DateTimePickerTimeOnly#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DateTimePickerTimeOnly/CS/Form1.cs#3)]
     [!code-vb[System.Windows.Forms.DateTimePickerTimeOnly#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DateTimePickerTimeOnly/VB/Form1.vb#3)]  
  
## <a name="example"></a><span data-ttu-id="a2712-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="a2712-108">Example</span></span>  
 <span data-ttu-id="a2712-109">L'exemple de code suivant montre comment créer un <xref:System.Windows.Forms.DateTimePicker> qui permet aux utilisateurs de choisir uniquement une heure.</span><span class="sxs-lookup"><span data-stu-id="a2712-109">The following code sample shows how to create a <xref:System.Windows.Forms.DateTimePicker> that enables users to choose a time only.</span></span>  
  
 [!code-csharp[System.Windows.Forms.DateTimePickerTimeOnly#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DateTimePickerTimeOnly/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.DateTimePickerTimeOnly#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DateTimePickerTimeOnly/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="a2712-110">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="a2712-110">Compiling the Code</span></span>  
 <span data-ttu-id="a2712-111">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="a2712-111">This example requires:</span></span>  
  
-   <span data-ttu-id="a2712-112">Références aux assemblys System, System.Data, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="a2712-112">References to the System, System.Data, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="a2712-113">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="a2712-113">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="a2712-114">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="a2712-114">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a2712-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2712-115">See also</span></span>

- [<span data-ttu-id="a2712-116">DateTimePicker, contrôle</span><span class="sxs-lookup"><span data-stu-id="a2712-116">DateTimePicker Control</span></span>](datetimepicker-control-windows-forms.md)
