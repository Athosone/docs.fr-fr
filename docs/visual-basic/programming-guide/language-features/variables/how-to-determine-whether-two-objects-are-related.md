---
title: 'Procédure : Déterminer si deux objets sont liés (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- inheritance [Visual Basic], Visual Basic objects
- objects [Visual Basic], inheritance
- object variables [Visual Basic], determining relation
ms.assetid: da002e3f-6616-4bad-a229-f842d06652bb
ms.openlocfilehash: f59e00d80d28fc4bf24874d25b5c12643649c834
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59342098"
---
# <a name="how-to-determine-whether-two-objects-are-related-visual-basic"></a><span data-ttu-id="4daf5-102">Procédure : Déterminer si deux objets sont liés (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="4daf5-102">How to: Determine Whether Two Objects Are Related (Visual Basic)</span></span>
<span data-ttu-id="4daf5-103">Vous pouvez comparer deux objets pour déterminer la relation, le cas échéant, entre les classes à partir de laquelle ils sont créés.</span><span class="sxs-lookup"><span data-stu-id="4daf5-103">You can compare two objects to determine the relationship, if any, between the classes from which they are created.</span></span> <span data-ttu-id="4daf5-104">Le <xref:System.Type.IsInstanceOfType%2A> méthode de la <xref:System.Type?displayProperty=nameWithType> classe retourne `True` si la classe spécifiée hérite de la classe en cours, ou si le type actuel est une interface prise en charge par la classe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4daf5-104">The <xref:System.Type.IsInstanceOfType%2A> method of the <xref:System.Type?displayProperty=nameWithType> class returns `True` if the specified class inherits from the current class, or if the current type is an interface supported by the specified class.</span></span>  
  
### <a name="to-determine-if-one-object-inherits-from-another-objects-class-or-interface"></a><span data-ttu-id="4daf5-105">Pour déterminer si un objet hérite de la classe ou une interface d’un autre objet</span><span class="sxs-lookup"><span data-stu-id="4daf5-105">To determine if one object inherits from another object's class or interface</span></span>  
  
1. <span data-ttu-id="4daf5-106">Sur l’objet que vous pensez peut être du type de base, appellent le <xref:System.Object.GetType%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="4daf5-106">On the object you think might be of the base type, invoke the <xref:System.Object.GetType%2A> method.</span></span>  
  
2. <span data-ttu-id="4daf5-107">Sur le <xref:System.Type?displayProperty=nameWithType> objet retourné par <xref:System.Object.GetType%2A>, appeler le <xref:System.Type.IsInstanceOfType%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="4daf5-107">On the <xref:System.Type?displayProperty=nameWithType> object returned by <xref:System.Object.GetType%2A>, invoke the <xref:System.Type.IsInstanceOfType%2A> method.</span></span>  
  
3. <span data-ttu-id="4daf5-108">Dans la liste d’arguments pour <xref:System.Type.IsInstanceOfType%2A>, spécifiez l’objet que vous pensez être du type dérivé.</span><span class="sxs-lookup"><span data-stu-id="4daf5-108">In the argument list for <xref:System.Type.IsInstanceOfType%2A>, specify the object you think might be of the derived type.</span></span>  
  
     <span data-ttu-id="4daf5-109"><xref:System.Type.IsInstanceOfType%2A> Retourne `True` si son type d’argument hérite le <xref:System.Type?displayProperty=nameWithType> type d’objet.</span><span class="sxs-lookup"><span data-stu-id="4daf5-109"><xref:System.Type.IsInstanceOfType%2A> returns `True` if its argument type inherits from the <xref:System.Type?displayProperty=nameWithType> object type.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4daf5-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="4daf5-110">Example</span></span>  
 <span data-ttu-id="4daf5-111">L’exemple suivant détermine si un objet représente une classe dérivée à partir d’une autre classe de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4daf5-111">The following example determines whether one object represents a class derived from another object's class.</span></span>  
  
```  
Public Class baseClass  
End Class  
Public Class derivedClass : Inherits baseClass  
End Class  
Public Class testTheseClasses  
    Public Sub seeIfRelated()  
        Dim baseObj As Object = New baseClass()  
        Dim derivedObj As Object = New derivedClass()  
        Dim related As Boolean  
        related = baseObj.GetType().IsInstanceOfType(derivedObj)  
        MsgBox(CStr(related))  
    End Sub  
End Class  
```  
  
 <span data-ttu-id="4daf5-112">Notez l’emplacement inattendu des deux variables objets dans l’appel à <xref:System.Type.IsInstanceOfType%2A>.</span><span class="sxs-lookup"><span data-stu-id="4daf5-112">Note the unexpected placement of the two object variables in the call to <xref:System.Type.IsInstanceOfType%2A>.</span></span> <span data-ttu-id="4daf5-113">Le type de base supposé est utilisé pour générer le <xref:System.Type?displayProperty=nameWithType> classe et le type dérivé supposé est passée en tant qu’argument à la <xref:System.Type.IsInstanceOfType%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="4daf5-113">The supposed base type is used to generate the <xref:System.Type?displayProperty=nameWithType> class, and the supposed derived type is passed as an argument to the <xref:System.Type.IsInstanceOfType%2A> method.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4daf5-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4daf5-114">See also</span></span>

- <xref:System.Object.GetType%2A>
- <xref:System.Type?displayProperty=nameWithType>
- <xref:System.Type.IsInstanceOfType%2A>
- [<span data-ttu-id="4daf5-115">Object (type de données)</span><span class="sxs-lookup"><span data-stu-id="4daf5-115">Object Data Type</span></span>](../../../../visual-basic/language-reference/data-types/object-data-type.md)
- [<span data-ttu-id="4daf5-116">Variables objets</span><span class="sxs-lookup"><span data-stu-id="4daf5-116">Object Variables</span></span>](../../../../visual-basic/programming-guide/language-features/variables/object-variables.md)
- [<span data-ttu-id="4daf5-117">Valeurs des variables objets</span><span class="sxs-lookup"><span data-stu-id="4daf5-117">Object Variable Values</span></span>](../../../../visual-basic/programming-guide/language-features/variables/object-variable-values.md)
- [<span data-ttu-id="4daf5-118">Guide pratique pour Déterminer si deux objets sont identiques</span><span class="sxs-lookup"><span data-stu-id="4daf5-118">How to: Determine Whether Two Objects Are Identical</span></span>](../../../../visual-basic/programming-guide/language-features/variables/how-to-determine-whether-two-objects-are-identical.md)
