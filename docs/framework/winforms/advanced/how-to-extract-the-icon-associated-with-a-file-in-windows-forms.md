---
title: 'Procédure : extraire l’icône associée à un fichier dans Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- displaying a file name and its file type icon in a ListView control [Windows Forms]
- file name extension icons [Windows Forms], displaying in a ListView
- extracting icons associated with a file type [Windows Forms]
ms.assetid: 88e2ad8b-c34f-415a-84f2-dad756b5c928
ms.openlocfilehash: d754dc5e8a57b3c4e2e5439bb2524a22d44813c6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59112552"
---
# <a name="how-to-extract-the-icon-associated-with-a-file-in-windows-forms"></a><span data-ttu-id="1a66e-102">Procédure : extraire l’icône associée à un fichier dans Windows Forms</span><span class="sxs-lookup"><span data-stu-id="1a66e-102">How to: Extract the Icon Associated with a File in Windows Forms</span></span>
<span data-ttu-id="1a66e-103">Grand nombre de fichiers ont des icônes incorporées qui fournissent une représentation visuelle du type de fichier associé.</span><span class="sxs-lookup"><span data-stu-id="1a66e-103">Many files have embedded icons that provide a visual representation of the associated file type.</span></span> <span data-ttu-id="1a66e-104">Par exemple, documents Microsoft Word contiennent une icône qui les identifie comme documents Word.</span><span class="sxs-lookup"><span data-stu-id="1a66e-104">For example, Microsoft Word documents contain an icon that identifies them as Word documents.</span></span> <span data-ttu-id="1a66e-105">Lors de l’affichage des fichiers dans un contrôle de table ou un contrôle de liste, vous souhaiterez afficher l’icône représentant le type de fichier en regard de chaque nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="1a66e-105">When displaying files in a list control or table control, you may want to display the icon representing the file type next to each file name.</span></span> <span data-ttu-id="1a66e-106">Faire cela facilement à l’aide de la <xref:System.Drawing.Icon.ExtractAssociatedIcon%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="1a66e-106">You can do this easily by using the <xref:System.Drawing.Icon.ExtractAssociatedIcon%2A> method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1a66e-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="1a66e-107">Example</span></span>  
 <span data-ttu-id="1a66e-108">L’exemple de code suivant montre comment extraire l’icône associée à un fichier et afficher le nom de fichier et son icône associée dans un <xref:System.Windows.Forms.ListView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="1a66e-108">The following code example demonstrates how to extract the icon associated with a file and display the file name and its associated icon in a <xref:System.Windows.Forms.ListView> control.</span></span>  
  
 [!code-csharp[System.Drawing.Icon.ExtractAssociatedIconEx#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.Icon.ExtractAssociatedIconEx/CS/Form1.cs#1)]
 [!code-vb[System.Drawing.Icon.ExtractAssociatedIconEx#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.Icon.ExtractAssociatedIconEx/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="1a66e-109">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="1a66e-109">Compiling the Code</span></span>  
 <span data-ttu-id="1a66e-110">Pour compiler l’exemple :</span><span class="sxs-lookup"><span data-stu-id="1a66e-110">To compile the example:</span></span>  
  
-   <span data-ttu-id="1a66e-111">Collez le code précédent dans un Windows Form et appelez le `ExtractAssociatedIconExample` méthode à partir du constructeur du formulaire ou <xref:System.Windows.Forms.Form.Load> méthode de gestion des événements.</span><span class="sxs-lookup"><span data-stu-id="1a66e-111">Paste the preceding code into a Windows Form, and call the `ExtractAssociatedIconExample` method from the form's constructor or <xref:System.Windows.Forms.Form.Load> event-handling method.</span></span>  
  
     <span data-ttu-id="1a66e-112">Vous devez vous assurer que votre formulaire importe le <xref:System.IO> espace de noms.</span><span class="sxs-lookup"><span data-stu-id="1a66e-112">You will need to make sure that your form imports the <xref:System.IO> namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1a66e-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a66e-113">See also</span></span>

- [<span data-ttu-id="1a66e-114">Images, bitmaps et métafichiers</span><span class="sxs-lookup"><span data-stu-id="1a66e-114">Images, Bitmaps, and Metafiles</span></span>](images-bitmaps-and-metafiles.md)
- [<span data-ttu-id="1a66e-115">Contrôle ListView</span><span class="sxs-lookup"><span data-stu-id="1a66e-115">ListView Control</span></span>](../controls/listview-control-windows-forms.md)
