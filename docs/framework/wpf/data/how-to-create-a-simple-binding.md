---
title: 'Procédure : Créer une liaison simple'
ms.date: 03/30/2017
helpviewer_keywords:
- simple binding [WPF], creating
- data binding [WPF], creating simple bindings
- binding data [WPF], creating
ms.assetid: 69b80f72-6259-44cb-8294-5bdcebca1e08
ms.openlocfilehash: d617c8b97aa679398ed2d061a652f5164f1e499b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61931562"
---
# <a name="how-to-create-a-simple-binding"></a><span data-ttu-id="73d0c-102">Procédure : Créer une liaison simple</span><span class="sxs-lookup"><span data-stu-id="73d0c-102">How to: Create a Simple Binding</span></span>
<span data-ttu-id="73d0c-103">Cet exemple vous montre comment créer un simple <xref:System.Windows.Data.Binding>.</span><span class="sxs-lookup"><span data-stu-id="73d0c-103">This example shows you how to create a simple <xref:System.Windows.Data.Binding>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="73d0c-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="73d0c-104">Example</span></span>  
 <span data-ttu-id="73d0c-105">Dans cet exemple, vous avez un `Person` objet avec une propriété de chaîne nommée `PersonName`.</span><span class="sxs-lookup"><span data-stu-id="73d0c-105">In this example, you have a `Person` object with a string property named `PersonName`.</span></span> <span data-ttu-id="73d0c-106">Le `Person` objet est défini dans l’espace de noms appelé `SDKSample`.</span><span class="sxs-lookup"><span data-stu-id="73d0c-106">The `Person` object is defined in the namespace called `SDKSample`.</span></span>  
  
 <span data-ttu-id="73d0c-107">La ligne en surbrillance qui contient le `<src>` élément dans l’exemple suivant instancie le `Person` de l’objet avec un `PersonName` valeur de propriété `Joe`.</span><span class="sxs-lookup"><span data-stu-id="73d0c-107">The highlighted line that contains the `<src>` element in the following example instantiates the `Person` object with a `PersonName` property value of `Joe`.</span></span> <span data-ttu-id="73d0c-108">Cette opération est effectuée le `Resources` section et affecté un `x:Key`.</span><span class="sxs-lookup"><span data-stu-id="73d0c-108">This is done in the `Resources` section and assigned an `x:Key`.</span></span>  
  
 [!code-xaml[SimpleBinding](~/samples/snippets/csharp/VS_Snippets_Wpf/SimpleBinding/CSharp/Page1.xaml?highlight=9,37)]  
  
 <span data-ttu-id="73d0c-109">La ligne en surbrillance qui contient le `<TextBlock>` élément lie ensuite le <xref:System.Windows.Controls.TextBlock> le contrôle à la `PersonName` propriété.</span><span class="sxs-lookup"><span data-stu-id="73d0c-109">The highlighted line that contains the `<TextBlock>` element then binds the <xref:System.Windows.Controls.TextBlock> control to the `PersonName` property.</span></span> <span data-ttu-id="73d0c-110">Par conséquent, le <xref:System.Windows.Controls.TextBlock> apparaît avec la valeur « Joe ».</span><span class="sxs-lookup"><span data-stu-id="73d0c-110">As a result, the <xref:System.Windows.Controls.TextBlock> appears with the value "Joe".</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="73d0c-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73d0c-111">See also</span></span>

- [<span data-ttu-id="73d0c-112">Vue d’ensemble de la liaison de données</span><span class="sxs-lookup"><span data-stu-id="73d0c-112">Data Binding Overview</span></span>](data-binding-overview.md)
- [<span data-ttu-id="73d0c-113">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="73d0c-113">How-to Topics</span></span>](data-binding-how-to-topics.md)
