---
title: 'Procédure : Créer une Collection utilisée par un initialiseur de Collection (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- collection initializers [Visual Basic]
ms.assetid: c858db10-424d-47e0-92cd-e08087cc5ebc
ms.openlocfilehash: 75c280b57df03bde173c740123cccda278536dc1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62053624"
---
# <a name="how-to-create-a-collection-used-by-a-collection-initializer-visual-basic"></a><span data-ttu-id="d8db8-102">Procédure : Créer une Collection utilisée par un initialiseur de Collection (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d8db8-102">How to: Create a Collection Used by a Collection Initializer (Visual Basic)</span></span>
<span data-ttu-id="d8db8-103">Lorsque vous utilisez un initialiseur de collection pour créer une collection, le compilateur Visual Basic cherche un `Add` méthode du type de collection pour laquelle les paramètres pour le `Add` méthode correspondent aux types des valeurs dans l’initialiseur de collection.</span><span class="sxs-lookup"><span data-stu-id="d8db8-103">When you use a collection initializer to create a collection, the Visual Basic compiler searches for an `Add` method of the collection type for which the parameters for the `Add` method match the types of the values in the collection initializer.</span></span> <span data-ttu-id="d8db8-104">Cela `Add` méthode est utilisée pour remplir la collection avec les valeurs à partir de l’initialiseur de collection.</span><span class="sxs-lookup"><span data-stu-id="d8db8-104">This `Add` method is used to populate the collection with the values from the collection initializer.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d8db8-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="d8db8-105">Example</span></span>  
 <span data-ttu-id="d8db8-106">L’exemple suivant montre un `OrderCollection` collection qui contient un public `Add` méthode un initialiseur de collection peut utiliser pour ajouter des objets de type `Order`.</span><span class="sxs-lookup"><span data-stu-id="d8db8-106">The following example shows an `OrderCollection` collection that contains a public `Add` method that a collection initializer can use to add objects of type `Order`.</span></span> <span data-ttu-id="d8db8-107">Le `Add` méthode vous permet d’utiliser la syntaxe d’initialiseur de collection abrégée.</span><span class="sxs-lookup"><span data-stu-id="d8db8-107">The `Add` method enables you to use the shortened collection initializer syntax.</span></span>  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo2#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCollectionInitializersHowTo2/VB/Module1.vb#4)]  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo2#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCollectionInitializersHowTo2/VB/Module1.vb#1)]  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo2#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCollectionInitializersHowTo2/VB/Module1.vb#2)]  
  
 [!code-vb[VbVbalrCollectionInitializersHowTo2#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCollectionInitializersHowTo2/VB/Module1.vb#3)]  
  
## <a name="see-also"></a><span data-ttu-id="d8db8-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8db8-108">See also</span></span>

- [<span data-ttu-id="d8db8-109">Initialiseurs de collection</span><span class="sxs-lookup"><span data-stu-id="d8db8-109">Collection Initializers</span></span>](../../../../visual-basic/programming-guide/language-features/collection-initializers/index.md)
- [<span data-ttu-id="d8db8-110">Guide pratique pour Créer une méthode d’Extension utilisée par un initialiseur de Collection Add</span><span class="sxs-lookup"><span data-stu-id="d8db8-110">How to: Create an Add Extension Method Used by a Collection Initializer</span></span>](../../../../visual-basic/programming-guide/language-features/collection-initializers/how-to-create-an-add-extension-method-used-by-a-collection-initializer.md)
