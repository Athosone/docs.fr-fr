---
title: Structures et autres éléments de programmation (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- structures [Visual Basic], arrays
- procedures [Visual Basic], structures as arguments to
- objects [Visual Basic], structure elements
- arrays [Visual Basic], structure elements
- nested structures [Visual Basic]
ms.assetid: 0f849313-ccd2-4c9a-acb9-69de6751c088
ms.openlocfilehash: a943bbdec617ba6c95685df3a4fcdb36b52def22
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61906449"
---
# <a name="structures-and-other-programming-elements-visual-basic"></a><span data-ttu-id="c2615-102">Structures et autres éléments de programmation (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c2615-102">Structures and Other Programming Elements (Visual Basic)</span></span>
<span data-ttu-id="c2615-103">Vous pouvez utiliser des structures en conjonction avec les tableaux, les objets et les procédures, ainsi qu’entre eux.</span><span class="sxs-lookup"><span data-stu-id="c2615-103">You can use structures in conjunction with arrays, objects, and procedures, as well as with each other.</span></span> <span data-ttu-id="c2615-104">Les interactions utilisent la même syntaxe que ces éléments individuellement.</span><span class="sxs-lookup"><span data-stu-id="c2615-104">The interactions use the same syntax as these elements use individually.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c2615-105">Vous ne peut pas initialiser un des éléments de structure dans la déclaration de structure.</span><span class="sxs-lookup"><span data-stu-id="c2615-105">You cannot initialize any of the structure elements in the structure declaration.</span></span> <span data-ttu-id="c2615-106">Vous pouvez assigner des valeurs uniquement aux éléments d’une variable qui a été déclarée comme étant d’un type structure.</span><span class="sxs-lookup"><span data-stu-id="c2615-106">You can assign values only to elements of a variable that has been declared to be of a structure type.</span></span>  
  
## <a name="structures-and-arrays"></a><span data-ttu-id="c2615-107">Structures et les tableaux</span><span class="sxs-lookup"><span data-stu-id="c2615-107">Structures and Arrays</span></span>  
 <span data-ttu-id="c2615-108">Une structure peut contenir un tableau comme un ou plusieurs de ses éléments.</span><span class="sxs-lookup"><span data-stu-id="c2615-108">A structure can contain an array as one or more of its elements.</span></span> <span data-ttu-id="c2615-109">L'exemple suivant illustre ce comportement.</span><span class="sxs-lookup"><span data-stu-id="c2615-109">The following example illustrates this.</span></span>  
  
```vb  
Public Structure systemInfo  
    Public cPU As String  
    Public memory As Long  
    Public diskDrives() As String  
    Public purchaseDate As Date  
End Structure   
```  
  
 <span data-ttu-id="c2615-110">Vous accéder aux valeurs d’un tableau dans une structure de la même façon que vous accédez à une propriété sur un objet.</span><span class="sxs-lookup"><span data-stu-id="c2615-110">You access the values of an array within a structure the same way you access a property on an object.</span></span> <span data-ttu-id="c2615-111">L'exemple suivant illustre ce comportement.</span><span class="sxs-lookup"><span data-stu-id="c2615-111">The following example illustrates this.</span></span>  
  
```vb  
Dim mySystem As systemInfo  
ReDim mySystem.diskDrives(3)  
mySystem.diskDrives(0) = "1.44 MB"  
```  
  
 <span data-ttu-id="c2615-112">Vous pouvez également déclarer un tableau de structures.</span><span class="sxs-lookup"><span data-stu-id="c2615-112">You can also declare an array of structures.</span></span> <span data-ttu-id="c2615-113">L'exemple suivant illustre ce comportement.</span><span class="sxs-lookup"><span data-stu-id="c2615-113">The following example illustrates this.</span></span>  
  
```vb  
Dim allSystems(100) As systemInfo  
```  
  
 <span data-ttu-id="c2615-114">Vous suivez les mêmes règles pour accéder aux composants de cette architecture de données.</span><span class="sxs-lookup"><span data-stu-id="c2615-114">You follow the same rules to access the components of this data architecture.</span></span> <span data-ttu-id="c2615-115">L'exemple suivant illustre ce comportement.</span><span class="sxs-lookup"><span data-stu-id="c2615-115">The following example illustrates this.</span></span>  
  
```vb  
ReDim allSystems(5).diskDrives(3)  
allSystems(5).CPU = "386SX"  
allSystems(5).diskDrives(2) = "100M SCSI"  
```  
  
## <a name="structures-and-objects"></a><span data-ttu-id="c2615-116">Structures et les objets</span><span class="sxs-lookup"><span data-stu-id="c2615-116">Structures and Objects</span></span>  
 <span data-ttu-id="c2615-117">Une structure peut contenir un objet comme un ou plusieurs de ses éléments.</span><span class="sxs-lookup"><span data-stu-id="c2615-117">A structure can contain an object as one or more of its elements.</span></span> <span data-ttu-id="c2615-118">L'exemple suivant illustre ce comportement.</span><span class="sxs-lookup"><span data-stu-id="c2615-118">The following example illustrates this.</span></span>  
  
```vb  
Protected Structure userInput  
    Public userName As String  
    Public inputForm As System.Windows.Forms.Form  
    Public userFileNumber As Integer  
End Structure  
```  
  
 <span data-ttu-id="c2615-119">Vous devez utiliser une classe d’objet spécifique dans une déclaration, plutôt que `Object`.</span><span class="sxs-lookup"><span data-stu-id="c2615-119">You should use a specific object class in such a declaration, rather than `Object`.</span></span>  
  
## <a name="structures-and-procedures"></a><span data-ttu-id="c2615-120">Structures et procédures</span><span class="sxs-lookup"><span data-stu-id="c2615-120">Structures and Procedures</span></span>  
 <span data-ttu-id="c2615-121">Vous pouvez passer une structure comme un argument de procédure.</span><span class="sxs-lookup"><span data-stu-id="c2615-121">You can pass a structure as a procedure argument.</span></span> <span data-ttu-id="c2615-122">L'exemple suivant illustre ce comportement.</span><span class="sxs-lookup"><span data-stu-id="c2615-122">The following example illustrates this.</span></span>  
  
```vb  
Public currentCPUName As String = "700MHz Pentium compatible"  
Public currentMemorySize As Long = 256  
Public Sub fillSystem(ByRef someSystem As systemInfo)  
    someSystem.cPU = currentCPUName  
    someSystem.memory = currentMemorySize  
    someSystem.purchaseDate = Now  
End Sub  
```  
  
 <span data-ttu-id="c2615-123">L’exemple précédent passe la structure *par référence*, ce qui permet à la procédure modifier ses éléments afin que les modifications prennent effet dans le code appelant.</span><span class="sxs-lookup"><span data-stu-id="c2615-123">The preceding example passes the structure *by reference*, which allows the procedure to modify its elements so that the changes take effect in the calling code.</span></span> <span data-ttu-id="c2615-124">Si vous souhaitez protéger une structure contre de telles modifications, passez par valeur.</span><span class="sxs-lookup"><span data-stu-id="c2615-124">If you want to protect a structure against such modification, pass it by value.</span></span>  
  
 <span data-ttu-id="c2615-125">Vous pouvez également retourner une structure à partir d’un `Function` procédure.</span><span class="sxs-lookup"><span data-stu-id="c2615-125">You can also return a structure from a `Function` procedure.</span></span> <span data-ttu-id="c2615-126">L'exemple suivant illustre ce comportement.</span><span class="sxs-lookup"><span data-stu-id="c2615-126">The following example illustrates this.</span></span>  
  
```vb  
Dim allSystems(100) As systemInfo  
Function findByDate(ByVal searchDate As Date) As systemInfo  
    Dim i As Integer  
    For i = 1 To 100  
        If allSystems(i).purchaseDate = searchDate Then Return allSystems(i)  
    Next i  
   ' Process error: system with desired purchase date not found.  
End Function  
```  
  
## <a name="structures-within-structures"></a><span data-ttu-id="c2615-127">Structures au sein de Structures</span><span class="sxs-lookup"><span data-stu-id="c2615-127">Structures Within Structures</span></span>  
 <span data-ttu-id="c2615-128">Les structures peuvent contenir d’autres structures.</span><span class="sxs-lookup"><span data-stu-id="c2615-128">Structures can contain other structures.</span></span> <span data-ttu-id="c2615-129">L'exemple suivant illustre ce comportement.</span><span class="sxs-lookup"><span data-stu-id="c2615-129">The following example illustrates this.</span></span>  
  
```vb  
Public Structure driveInfo  
    Public type As String  
    Public size As Long  
End Structure  
Public Structure systemInfo  
    Public cPU As String  
    Public memory As Long  
    Public diskDrives() As driveInfo  
    Public purchaseDate As Date  
End Structure  
```  
  
```vb  
Dim allSystems(100) As systemInfo  
ReDim allSystems(1).diskDrives(3)  
allSystems(1).diskDrives(0).type = "Floppy"  
```  
  
 <span data-ttu-id="c2615-130">Vous pouvez également utiliser cette technique pour encapsuler une structure définie dans un module au sein d’une structure définie dans un autre module.</span><span class="sxs-lookup"><span data-stu-id="c2615-130">You can also use this technique to encapsulate a structure defined in one module within a structure defined in a different module.</span></span>  
  
 <span data-ttu-id="c2615-131">Les structures peuvent contenir d’autres structures à une profondeur arbitraire.</span><span class="sxs-lookup"><span data-stu-id="c2615-131">Structures can contain other structures to an arbitrary depth.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c2615-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2615-132">See also</span></span>

- [<span data-ttu-id="c2615-133">Types de données</span><span class="sxs-lookup"><span data-stu-id="c2615-133">Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/index.md)
- [<span data-ttu-id="c2615-134">Types de données élémentaires</span><span class="sxs-lookup"><span data-stu-id="c2615-134">Elementary Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/elementary-data-types.md)
- [<span data-ttu-id="c2615-135">Types de données composites</span><span class="sxs-lookup"><span data-stu-id="c2615-135">Composite Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/composite-data-types.md)
- [<span data-ttu-id="c2615-136">Value Types and Reference Types</span><span class="sxs-lookup"><span data-stu-id="c2615-136">Value Types and Reference Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md)
- [<span data-ttu-id="c2615-137">Structures</span><span class="sxs-lookup"><span data-stu-id="c2615-137">Structures</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [<span data-ttu-id="c2615-138">Dépannage des types de données</span><span class="sxs-lookup"><span data-stu-id="c2615-138">Troubleshooting Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md)
- [<span data-ttu-id="c2615-139">Guide pratique pour déclarer une structure</span><span class="sxs-lookup"><span data-stu-id="c2615-139">How to: Declare a Structure</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)
- [<span data-ttu-id="c2615-140">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="c2615-140">Structure Variables</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/structure-variables.md)
- [<span data-ttu-id="c2615-141">Structures et classes</span><span class="sxs-lookup"><span data-stu-id="c2615-141">Structures and Classes</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/structures-and-classes.md)
- [<span data-ttu-id="c2615-142">Structure (instruction)</span><span class="sxs-lookup"><span data-stu-id="c2615-142">Structure Statement</span></span>](../../../../visual-basic/language-reference/statements/structure-statement.md)
