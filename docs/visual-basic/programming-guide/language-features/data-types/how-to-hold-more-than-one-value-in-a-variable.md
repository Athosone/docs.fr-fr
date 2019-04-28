---
title: 'Procédure : Stocker plusieurs valeurs dans une Variable (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- classes [Visual Basic], composite data types
- composite types [Visual Basic]
- composite data types [Visual Basic]
- data types [Visual Basic], composite
- arrays [Visual Basic], composite data types
- structures [Visual Basic], composite data types
- arrays [Visual Basic], compilation errors
- types [Visual Basic], composite
ms.assetid: 5fe0e558-aac2-4a40-b7f2-7cfea7336917
ms.openlocfilehash: e2e1648ea508ecdd744adb8d2a4f7fdbc1e586c4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61906488"
---
# <a name="how-to-hold-more-than-one-value-in-a-variable-visual-basic"></a><span data-ttu-id="b37ea-102">Procédure : Stocker plusieurs valeurs dans une Variable (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b37ea-102">How to: Hold More Than One Value in a Variable (Visual Basic)</span></span>
<span data-ttu-id="b37ea-103">Une variable contient plusieurs valeurs si vous déclarez comme étant d’un *type de données composite*.</span><span class="sxs-lookup"><span data-stu-id="b37ea-103">A variable holds more than one value if you declare it to be of a *composite data type*.</span></span>  
  
 <span data-ttu-id="b37ea-104">[Les Types de données composites](../../../../visual-basic/programming-guide/language-features/data-types/composite-data-types.md) incluent des structures, des tableaux et des classes.</span><span class="sxs-lookup"><span data-stu-id="b37ea-104">[Composite Data Types](../../../../visual-basic/programming-guide/language-features/data-types/composite-data-types.md) include structures, arrays, and classes.</span></span> <span data-ttu-id="b37ea-105">Une variable de type de données composite peut contenir une combinaison de types de données élémentaires et d’autres types composites.</span><span class="sxs-lookup"><span data-stu-id="b37ea-105">A variable of a composite data type can hold a combination of elementary data types and other composite types.</span></span> <span data-ttu-id="b37ea-106">Structures et classes peuvent contenir du code ainsi que les données.</span><span class="sxs-lookup"><span data-stu-id="b37ea-106">Structures and classes can hold code as well as data.</span></span>  
  
### <a name="to-hold-more-than-one-value-in-a-variable"></a><span data-ttu-id="b37ea-107">Pour stocker plusieurs valeurs dans une variable</span><span class="sxs-lookup"><span data-stu-id="b37ea-107">To hold more than one value in a variable</span></span>  
  
1. <span data-ttu-id="b37ea-108">Déterminer le type de données composites que vous souhaitez utiliser pour votre variable.</span><span class="sxs-lookup"><span data-stu-id="b37ea-108">Determine what composite data type you want to use for your variable.</span></span>  
  
2. <span data-ttu-id="b37ea-109">Si le type de données composite n’est pas déjà défini, définissez-le afin que votre variable puisse l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="b37ea-109">If the composite data type is not already defined, define it so that your variable can use it.</span></span>  
  
    - <span data-ttu-id="b37ea-110">Définir une structure avec un [instruction Structure](../../../../visual-basic/language-reference/statements/structure-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b37ea-110">Define a structure with a [Structure Statement](../../../../visual-basic/language-reference/statements/structure-statement.md).</span></span>  
  
    - <span data-ttu-id="b37ea-111">Définir un tableau avec un [instruction Dim](../../../../visual-basic/language-reference/statements/dim-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b37ea-111">Define an array with a [Dim Statement](../../../../visual-basic/language-reference/statements/dim-statement.md).</span></span>  
  
    - <span data-ttu-id="b37ea-112">Définir une classe avec un [Class, instruction](../../../../visual-basic/language-reference/statements/class-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b37ea-112">Define a class with a [Class Statement](../../../../visual-basic/language-reference/statements/class-statement.md).</span></span>  
  
3. <span data-ttu-id="b37ea-113">Déclarez votre variable avec un `Dim` instruction.</span><span class="sxs-lookup"><span data-stu-id="b37ea-113">Declare your variable with a `Dim` statement.</span></span>  
  
4. <span data-ttu-id="b37ea-114">Suivez le nom de variable avec une `As` clause.</span><span class="sxs-lookup"><span data-stu-id="b37ea-114">Follow the variable name with an `As` clause.</span></span>  
  
5. <span data-ttu-id="b37ea-115">Suivez le `As` mot clé par le nom du type de données composite approprié.</span><span class="sxs-lookup"><span data-stu-id="b37ea-115">Follow the `As` keyword with the name of the appropriate composite data type.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b37ea-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b37ea-116">See also</span></span>

- [<span data-ttu-id="b37ea-117">Types de données</span><span class="sxs-lookup"><span data-stu-id="b37ea-117">Data Types</span></span>](../../../../visual-basic/language-reference/data-types/index.md)
- [<span data-ttu-id="b37ea-118">Caractères de type</span><span class="sxs-lookup"><span data-stu-id="b37ea-118">Type Characters</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/type-characters.md)
- [<span data-ttu-id="b37ea-119">Types de données composites</span><span class="sxs-lookup"><span data-stu-id="b37ea-119">Composite Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/composite-data-types.md)
- [<span data-ttu-id="b37ea-120">Structures</span><span class="sxs-lookup"><span data-stu-id="b37ea-120">Structures</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [<span data-ttu-id="b37ea-121">Tableaux</span><span class="sxs-lookup"><span data-stu-id="b37ea-121">Arrays</span></span>](../../../../visual-basic/programming-guide/language-features/arrays/index.md)
- [<span data-ttu-id="b37ea-122">Objets et classes</span><span class="sxs-lookup"><span data-stu-id="b37ea-122">Objects and Classes</span></span>](../../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
- [<span data-ttu-id="b37ea-123">Value Types and Reference Types</span><span class="sxs-lookup"><span data-stu-id="b37ea-123">Value Types and Reference Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md)
