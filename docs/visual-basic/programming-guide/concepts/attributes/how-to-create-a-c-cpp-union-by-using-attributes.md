---
title: 'Procédure : Créer une Union C / C++ à l’aide d’attributs (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: 9352a7e4-c0da-4d07-aa14-55ed43736fcb
ms.openlocfilehash: 0c3ebf248f5d2f20e2fff25fb8326a294b51d153
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61789088"
---
# <a name="how-to-create-a-cc-union-by-using-attributes-visual-basic"></a><span data-ttu-id="ba58f-102">Procédure : Créer une Union C/C++ à l’aide d’attributs (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ba58f-102">How to: Create a C/C++ Union by Using Attributes (Visual Basic)</span></span>
<span data-ttu-id="ba58f-103">Vous pouvez personnaliser la disposition des structs en mémoire à l’aide d’attributs.</span><span class="sxs-lookup"><span data-stu-id="ba58f-103">By using attributes you can customize how structs are laid out in memory.</span></span> <span data-ttu-id="ba58f-104">Par exemple, vous pouvez créer ce qu’on appelle une union en C/C++ à l’aide des attributs `StructLayout(LayoutKind.Explicit)` et `FieldOffset`.</span><span class="sxs-lookup"><span data-stu-id="ba58f-104">For example, you can create what is known as a union in C/C++ by using the `StructLayout(LayoutKind.Explicit)` and `FieldOffset` attributes.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ba58f-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="ba58f-105">Example</span></span>  
 <span data-ttu-id="ba58f-106">Dans ce segment de code, tous les champs de `TestUnion` débutent au même emplacement en mémoire.</span><span class="sxs-lookup"><span data-stu-id="ba58f-106">In this code segment, all of the fields of `TestUnion` start at the same location in memory.</span></span>  
  
```vb  
' Add an Imports statement for System.Runtime.InteropServices.  
  
<System.Runtime.InteropServices.StructLayout(   
      System.Runtime.InteropServices.LayoutKind.Explicit)>   
Structure TestUnion  
    <System.Runtime.InteropServices.FieldOffset(0)>   
    Public i As Integer  
  
    <System.Runtime.InteropServices.FieldOffset(0)>   
    Public d As Double  
  
    <System.Runtime.InteropServices.FieldOffset(0)>   
    Public c As Char  
  
    <System.Runtime.InteropServices.FieldOffset(0)>   
    Public b As Byte  
End Structure  
```  
  
## <a name="example"></a><span data-ttu-id="ba58f-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="ba58f-107">Example</span></span>  
 <span data-ttu-id="ba58f-108">Voici un autre exemple où les champs débutent à différents emplacements définis explicitement.</span><span class="sxs-lookup"><span data-stu-id="ba58f-108">The following is another example where fields start at different explicitly set locations.</span></span>  
  
```vb  
' Add an Imports statement for System.Runtime.InteropServices.  
  
 <System.Runtime.InteropServices.StructLayout(  
      System.Runtime.InteropServices.LayoutKind.Explicit)>   
Structure TestExplicit  
     <System.Runtime.InteropServices.FieldOffset(0)>   
     Public lg As Long  
  
     <System.Runtime.InteropServices.FieldOffset(0)>   
     Public i1 As Integer  
  
     <System.Runtime.InteropServices.FieldOffset(4)>   
     Public i2 As Integer  
  
     <System.Runtime.InteropServices.FieldOffset(8)>   
     Public d As Double  
  
     <System.Runtime.InteropServices.FieldOffset(12)>   
     Public c As Char  
  
     <System.Runtime.InteropServices.FieldOffset(14)>   
     Public b As Byte  
 End Structure  
```  
  
 <span data-ttu-id="ba58f-109">Les deux champs entiers, `i1` et `i2`, partagent leurs emplacements de mémoire avec `lg`.</span><span class="sxs-lookup"><span data-stu-id="ba58f-109">The two integer fields, `i1` and `i2`, share the same memory locations as `lg`.</span></span> <span data-ttu-id="ba58f-110">Ce type de contrôle sur la disposition des structs est utile quand vous utilisez des appels de code non managé.</span><span class="sxs-lookup"><span data-stu-id="ba58f-110">This sort of control over struct layout is useful when using platform invocation.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ba58f-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba58f-111">See also</span></span>

- <xref:System.Reflection>
- <xref:System.Attribute>
- [<span data-ttu-id="ba58f-112">Guide de programmation Visual Basic</span><span class="sxs-lookup"><span data-stu-id="ba58f-112">Visual Basic Programming Guide</span></span>](../../../../visual-basic/programming-guide/index.md)
- [<span data-ttu-id="ba58f-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="ba58f-113">Attributes</span></span>](../../../../standard/attributes/index.md)
- [<span data-ttu-id="ba58f-114">Réflexion (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ba58f-114">Reflection (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/reflection.md)
- [<span data-ttu-id="ba58f-115">Attributs (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ba58f-115">Attributes (Visual Basic)</span></span>](../../../../visual-basic/language-reference/attributes.md)
- [<span data-ttu-id="ba58f-116">Créer des attributs personnalisés (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ba58f-116">Creating Custom Attributes (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/attributes/creating-custom-attributes.md)
- [<span data-ttu-id="ba58f-117">Accéder à des attributs à l’aide de la réflexion (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ba58f-117">Accessing Attributes by Using Reflection (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/attributes/accessing-attributes-by-using-reflection.md)
