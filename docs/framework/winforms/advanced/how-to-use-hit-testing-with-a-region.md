---
title: 'Procédure : utiliser le test de positionnement avec une région'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- hit tests [Windows Forms], using regions
- regions [Windows Forms], hit testing
ms.assetid: 3a4c07cb-a40a-4d14-ad35-008f531910a8
ms.openlocfilehash: 136f15f1364fb2aed791b4a61d0f11411b055967
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59150499"
---
# <a name="how-to-use-hit-testing-with-a-region"></a><span data-ttu-id="9a7ff-102">Procédure : utiliser le test de positionnement avec une région</span><span class="sxs-lookup"><span data-stu-id="9a7ff-102">How to: Use Hit Testing with a Region</span></span>
<span data-ttu-id="9a7ff-103">L’objectif du test de positionnement consiste à déterminer si le curseur se trouve sur un objet donné, tel qu’une icône ou un bouton.</span><span class="sxs-lookup"><span data-stu-id="9a7ff-103">The purpose of hit testing is to determine whether the cursor is over a given object, such as an icon or a button.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9a7ff-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="9a7ff-104">Example</span></span>  
 <span data-ttu-id="9a7ff-105">L’exemple suivant crée une région en forme de plus par l’union de deux régions rectangulaires.</span><span class="sxs-lookup"><span data-stu-id="9a7ff-105">The following example creates a plus-shaped region by forming the union of two rectangular regions.</span></span> <span data-ttu-id="9a7ff-106">Supposons que la variable `point` contient l’emplacement du clic plus récent.</span><span class="sxs-lookup"><span data-stu-id="9a7ff-106">Assume that the variable `point` holds the location of the most recent click.</span></span> <span data-ttu-id="9a7ff-107">Le code vérifie si `point` se trouve dans la région en forme de plus.</span><span class="sxs-lookup"><span data-stu-id="9a7ff-107">The code checks to see whether `point` is in the plus-shaped region.</span></span> <span data-ttu-id="9a7ff-108">Si le point se trouve dans la région (une atteinte), la région est remplie avec un pinceau rouge opaque.</span><span class="sxs-lookup"><span data-stu-id="9a7ff-108">If the point is in the region (a hit), the region is filled with an opaque red brush.</span></span> <span data-ttu-id="9a7ff-109">Sinon, la région est remplie avec un pinceau rouge translucide.</span><span class="sxs-lookup"><span data-stu-id="9a7ff-109">Otherwise, the region is filled with a semitransparent red brush.</span></span>  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.MiscLegacyTopics#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="9a7ff-110">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="9a7ff-110">Compiling the Code</span></span>  
 <span data-ttu-id="9a7ff-111">L’exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de <xref:System.Windows.Forms.PaintEventHandler>.</span><span class="sxs-lookup"><span data-stu-id="9a7ff-111">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9a7ff-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a7ff-112">See also</span></span>

- <xref:System.Drawing.Region>
- [<span data-ttu-id="9a7ff-113">Régions dans GDI+</span><span class="sxs-lookup"><span data-stu-id="9a7ff-113">Regions in GDI+</span></span>](regions-in-gdi.md)
- [<span data-ttu-id="9a7ff-114">Guide pratique pour Utiliser le découpage avec une région</span><span class="sxs-lookup"><span data-stu-id="9a7ff-114">How to: Use Clipping with a Region</span></span>](how-to-use-clipping-with-a-region.md)
