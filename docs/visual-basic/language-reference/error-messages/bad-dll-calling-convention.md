---
title: Convention d’appel de DLL incorrecte
ms.date: 07/20/2015
f1_keywords:
- vbrID49
ms.assetid: 7c7def45-b0ab-450f-ad3f-4383dfd9aed7
ms.openlocfilehash: f7b0c3a6edbe0b950195306fa66287ff9b209bfe
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61935276"
---
# <a name="bad-dll-calling-convention"></a><span data-ttu-id="9c75a-102">Convention d’appel de DLL incorrecte</span><span class="sxs-lookup"><span data-stu-id="9c75a-102">Bad DLL calling convention</span></span>
<span data-ttu-id="9c75a-103">Arguments passés à une bibliothèque de liens dynamiques (DLL) doivent correspondre exactement à ceux attendus par la routine.</span><span class="sxs-lookup"><span data-stu-id="9c75a-103">Arguments passed to a dynamic-link library (DLL) must exactly match those expected by the routine.</span></span> <span data-ttu-id="9c75a-104">Conventions d’appel traitent nombre, type et ordre des arguments.</span><span class="sxs-lookup"><span data-stu-id="9c75a-104">Calling conventions deal with number, type, and order of arguments.</span></span> <span data-ttu-id="9c75a-105">Votre programme peut appeler une routine dans une DLL qui lui est passée le type incorrect ou le nombre d’arguments.</span><span class="sxs-lookup"><span data-stu-id="9c75a-105">Your program may be calling a routine in a DLL that is being passed the wrong type or number of arguments.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="9c75a-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="9c75a-106">To correct this error</span></span>  
  
1. <span data-ttu-id="9c75a-107">Assurez-vous que tous les types d’argument correspondent à ceux spécifiés dans la déclaration de la routine que vous appelez.</span><span class="sxs-lookup"><span data-stu-id="9c75a-107">Make sure all argument types agree with those specified in the declaration of the routine that you are calling.</span></span>  
  
2. <span data-ttu-id="9c75a-108">Vérifiez que vous passez le même nombre d’arguments indiqué dans la déclaration de la routine que vous appelez.</span><span class="sxs-lookup"><span data-stu-id="9c75a-108">Make sure you are passing the same number of arguments indicated in the declaration of the routine that you are calling.</span></span>  
  
3. <span data-ttu-id="9c75a-109">Si la routine DLL attend des arguments par valeur, assurez-vous que `ByVal` est spécifié pour ces arguments dans la déclaration de la routine.</span><span class="sxs-lookup"><span data-stu-id="9c75a-109">If the DLL routine expects arguments by value, make sure `ByVal` is specified for those arguments in the declaration for the routine.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9c75a-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c75a-110">See also</span></span>

- [<span data-ttu-id="9c75a-111">Types d’erreurs</span><span class="sxs-lookup"><span data-stu-id="9c75a-111">Error Types</span></span>](../../../visual-basic/programming-guide/language-features/error-types.md)
- [<span data-ttu-id="9c75a-112">Call (instruction)</span><span class="sxs-lookup"><span data-stu-id="9c75a-112">Call Statement</span></span>](../../../visual-basic/language-reference/statements/call-statement.md)
- [<span data-ttu-id="9c75a-113">Declare (instruction)</span><span class="sxs-lookup"><span data-stu-id="9c75a-113">Declare Statement</span></span>](../../../visual-basic/language-reference/statements/declare-statement.md)
