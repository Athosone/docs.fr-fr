---
title: Types de méthodes de manipulation de chaînes en Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], manipulating [Visual Basic]
- string manipulation
ms.assetid: 905055cd-7f50-48fb-9eed-b0995af1dc1f
ms.openlocfilehash: 44eb101ebdfeb316958a659107190ef1fc84df44
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61938266"
---
# <a name="types-of-string-manipulation-methods-in-visual-basic"></a><span data-ttu-id="1e68b-102">Types de méthodes de manipulation de chaînes en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="1e68b-102">Types of String Manipulation Methods in Visual Basic</span></span>
<span data-ttu-id="1e68b-103">Il existe différentes façons de les analyser et manipuler des chaînes.</span><span class="sxs-lookup"><span data-stu-id="1e68b-103">There are several different ways to analyze and manipulate your strings.</span></span> <span data-ttu-id="1e68b-104">Certaines des méthodes font partie du langage Visual Basic, et d’autres sont inhérentes à la `String` classe.</span><span class="sxs-lookup"><span data-stu-id="1e68b-104">Some of the methods are a part of the Visual Basic language, and others are inherent in the `String` class.</span></span>  
  
## <a name="visual-basic-language-and-the-net-framework"></a><span data-ttu-id="1e68b-105">Langage Visual Basic et .NET Framework</span><span class="sxs-lookup"><span data-stu-id="1e68b-105">Visual Basic Language and the .NET Framework</span></span>  
 <span data-ttu-id="1e68b-106">Méthodes de Visual Basic sont utilisées en tant que fonctions inhérentes du langage.</span><span class="sxs-lookup"><span data-stu-id="1e68b-106">Visual Basic methods are used as inherent functions of the language.</span></span> <span data-ttu-id="1e68b-107">Ils peuvent être utilisés sans qualification dans votre code.</span><span class="sxs-lookup"><span data-stu-id="1e68b-107">They may be used without qualification in your code.</span></span> <span data-ttu-id="1e68b-108">L’exemple suivant illustre une utilisation classique d’une commande de manipulation de chaînes Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="1e68b-108">The following example shows typical use of a Visual Basic string-manipulation command:</span></span>  
  
 [!code-vb[VbVbalrStrings#44](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#44)]  
  
 <span data-ttu-id="1e68b-109">Dans cet exemple, le `Mid` fonction effectue une opération directe sur `aString` et affecte la valeur à `bString`.</span><span class="sxs-lookup"><span data-stu-id="1e68b-109">In this example, the `Mid` function performs a direct operation on `aString` and assigns the value to `bString`.</span></span>  
  
 <span data-ttu-id="1e68b-110">Pour obtenir la liste des méthodes de manipulation de chaîne Visual Basic, consultez [liste des manipulations de chaîne](../../../../visual-basic/language-reference/keywords/string-manipulation-summary.md).</span><span class="sxs-lookup"><span data-stu-id="1e68b-110">For a list of Visual Basic string manipulation methods, see [String Manipulation Summary](../../../../visual-basic/language-reference/keywords/string-manipulation-summary.md).</span></span>  
  
### <a name="shared-methods-and-instance-methods"></a><span data-ttu-id="1e68b-111">Méthodes partagées et des méthodes d’Instance</span><span class="sxs-lookup"><span data-stu-id="1e68b-111">Shared Methods and Instance Methods</span></span>  
 <span data-ttu-id="1e68b-112">Vous pouvez également manipuler des chaînes avec les méthodes de la `String` classe.</span><span class="sxs-lookup"><span data-stu-id="1e68b-112">You can also manipulate strings with the methods of the `String` class.</span></span> <span data-ttu-id="1e68b-113">Il existe deux types de méthodes de `String`: *partagé* méthodes et *instance* méthodes.</span><span class="sxs-lookup"><span data-stu-id="1e68b-113">There are two types of methods in `String`: *shared* methods and *instance* methods.</span></span>  
  
#### <a name="shared-methods"></a><span data-ttu-id="1e68b-114">Méthodes partagées</span><span class="sxs-lookup"><span data-stu-id="1e68b-114">Shared Methods</span></span>  
 <span data-ttu-id="1e68b-115">Une méthode partagée est une méthode qui provient de la `String` classe lui-même et ne nécessite pas une instance de cette classe fonctionne.</span><span class="sxs-lookup"><span data-stu-id="1e68b-115">A shared method is a method that stems from the `String` class itself and does not require an instance of that class to work.</span></span> <span data-ttu-id="1e68b-116">Ces méthodes peuvent être qualifiés avec le nom de la classe (`String`) plutôt qu’avec une instance de la `String` classe.</span><span class="sxs-lookup"><span data-stu-id="1e68b-116">These methods can be qualified with the name of the class (`String`) rather than with an instance of the `String` class.</span></span> <span data-ttu-id="1e68b-117">Exemple :</span><span class="sxs-lookup"><span data-stu-id="1e68b-117">For example:</span></span>  
  
 [!code-vb[VbVbalrStrings#45](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#45)]  
  
 <span data-ttu-id="1e68b-118">Dans l’exemple précédent, le <xref:System.String.Copy%2A?displayProperty=nameWithType> méthode est une méthode statique, qui agit sur une expression qui lui est attribuée et affecte la valeur obtenue vers `bString`.</span><span class="sxs-lookup"><span data-stu-id="1e68b-118">In the preceding example, the <xref:System.String.Copy%2A?displayProperty=nameWithType> method is a static method, which acts upon an expression it is given and assigns the resulting value to `bString`.</span></span>  
  
#### <a name="instance-methods"></a><span data-ttu-id="1e68b-119">Méthodes d’instance</span><span class="sxs-lookup"><span data-stu-id="1e68b-119">Instance Methods</span></span>  
 <span data-ttu-id="1e68b-120">Méthodes d’instance, en revanche, proviennent d’une instance particulière de `String` et doivent être qualifiés avec le nom d’instance.</span><span class="sxs-lookup"><span data-stu-id="1e68b-120">Instance methods, by contrast, stem from a particular instance of `String` and must be qualified with the instance name.</span></span> <span data-ttu-id="1e68b-121">Exemple :</span><span class="sxs-lookup"><span data-stu-id="1e68b-121">For example:</span></span>  
  
 [!code-vb[VbVbalrStrings#46](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#46)]  
  
 <span data-ttu-id="1e68b-122">Dans cet exemple, le <xref:System.String.Substring%2A?displayProperty=nameWithType> méthode est une méthode de l’instance de `String` (autrement dit, `aString`).</span><span class="sxs-lookup"><span data-stu-id="1e68b-122">In this example, the <xref:System.String.Substring%2A?displayProperty=nameWithType> method is a method of the instance of `String` (that is, `aString`).</span></span> <span data-ttu-id="1e68b-123">Elle effectue une opération sur `aString` et assigne cette valeur à `bString`.</span><span class="sxs-lookup"><span data-stu-id="1e68b-123">It performs an operation on `aString` and assigns that value to `bString`.</span></span>  
  
 <span data-ttu-id="1e68b-124">Pour plus d’informations, consultez la documentation pour le <xref:System.String> classe.</span><span class="sxs-lookup"><span data-stu-id="1e68b-124">For more information, see the documentation for the <xref:System.String> class.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1e68b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e68b-125">See also</span></span>

- [<span data-ttu-id="1e68b-126">Introduction aux chaînes en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="1e68b-126">Introduction to Strings in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/strings/introduction-to-strings.md)
