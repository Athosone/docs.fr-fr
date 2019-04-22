---
title: Procédures génériques dans Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- generic methods [Visual Basic], type inference
- generics [Visual Basic], type inference
- procedures [Visual Basic], generic
- generic procedures
- type inference, generics
- generic methods [Visual Basic]
- type inference
- generics [Visual Basic], procedures
- generic procedures [Visual Basic], type inference
ms.assetid: 95577b28-137f-4d5c-a149-919c828600e5
ms.openlocfilehash: 4aed16ce9eb59da54156a0cd5f1594819788521b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58818915"
---
# <a name="generic-procedures-in-visual-basic"></a>Procédures génériques dans Visual Basic
Un *procédure générique*, également appelé un *méthode générique*, est une procédure définie au moins un paramètre de type. Cela permet au code appelant d’adapter les types de données à ses exigences chaque fois qu’il appelle la procédure.  
  
 Une procédure n’est pas générique simplement en vertu d’en cours de définition à l’intérieur d’une classe générique ou une structure générique. Pour être générique, la procédure doit prendre au moins un paramètre de type, en plus de tous les paramètres normaux que peut prendre. Une classe générique ou une structure peut contenir des procédures non génériques et une classe non générique, structure, ou le module peut contenir des procédures génériques.  
  
 Une procédure générique peut utiliser ses paramètres de type dans sa liste de paramètres normale, dans son type de retour s’il a un et dans sa procédure de code.  
  
## <a name="type-inference"></a>Inférence de type  
 Vous pouvez appeler une procédure générique sans fournir d’arguments de type du tout. Si vous l’appelez de cette façon, le compilateur tente de déterminer les types de données appropriées à passer des arguments de type de la procédure. Il s’agit *l’inférence de type*. Le code suivant montre un appel dans lequel le compilateur déduit qu’il doit passer le type `String` au paramètre de type `t`.  
  
 [!code-vb[VbVbalrDataTypes#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDataTypes/VB/Class1.vb#15)]  
  
 Si le compilateur ne peut pas déduire les arguments de type à partir du contexte de votre appel, il signale une erreur. Une des causes possibles de cette erreur est une incompatibilité de rang de tableau. Par exemple, supposons que vous définissez un paramètre normal comme un tableau d’un paramètre de type. Si vous appelez la procédure générique en fournissant un tableau d’un rang différent (nombre de dimensions), la différence provoque l’inférence de type échec. Le code suivant montre un appel dans lequel un tableau à deux dimensions est passé à une procédure qui attend un tableau unidimensionnel.  
  
```vb  
Public Sub demoSub(Of t)(ByVal arg() As t)
End Sub

Public Sub callDemoSub()
    Dim twoDimensions(,) As Integer
    demoSub(twoDimensions)
End Sub
```
  
 Vous pouvez appeler l’inférence de type uniquement en omettant tous les arguments de type. Si vous fournissez un argument de type, vous devez fournir toutes les.  
  
 Inférence de type est pris en charge uniquement pour les procédures génériques. Vous ne pouvez pas appeler l’inférence de type sur les classes génériques, des structures, des interfaces ou des délégués.  
  
## <a name="example"></a>Exemple  
  
### <a name="description"></a>Description  
 L’exemple suivant définit un générique `Function` procédure pour rechercher un élément particulier dans un tableau. Il définit un paramètre de type et l’utilise pour construire les deux paramètres dans la liste de paramètres.  
  
### <a name="code"></a>Code  
 [!code-vb[VbVbalrDataTypes#14](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDataTypes/VB/Class1.vb#14)]  
  
### <a name="comments"></a>Commentaires  
 L’exemple précédent doit avoir la possibilité de comparer `searchValue` sur chaque élément de `searchArray`. Pour garantir cette capacité, il contraint le paramètre de type `T` pour implémenter le <xref:System.IComparable%601> interface. Le code utilise le <xref:System.IComparable%601.CompareTo%2A> méthode au lieu du `=` opérateur, car il n’existe aucune garantie qu’un argument de type fourni pour `T` prend en charge la `=` opérateur.  
  
 Vous pouvez tester le `findElement` procédure avec le code suivant.  
  
 [!code-vb[VbVbalrDataTypes#13](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDataTypes/VB/Class1.vb#13)]  
  
 L’exemple précédent appelle à `MsgBox` afficher « 0 », « 1 » et « -1 » respectivement.  
  
## <a name="see-also"></a>Voir aussi

- [Generic Types in Visual Basic](../../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)
- [Guide pratique pour définir une classe qui fournisse des fonctionnalités identiques pour différents types de données](../../../../visual-basic/programming-guide/language-features/data-types/how-to-define-a-class-that-can-provide-identical-functionality.md)
- [Guide pratique pour utiliser une classe générique](../../../../visual-basic/programming-guide/language-features/data-types/how-to-use-a-generic-class.md)
- [Procédures](../../../../visual-basic/programming-guide/language-features/procedures/index.md)
- [Paramètres et arguments d’une procédure](../../../../visual-basic/programming-guide/language-features/procedures/procedure-parameters-and-arguments.md)
- [Liste de types](../../../../visual-basic/language-reference/statements/type-list.md)
- [Liste de paramètres](../../../../visual-basic/language-reference/statements/parameter-list.md)
