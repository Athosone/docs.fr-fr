---
title: Variables de structure (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- structures [Visual Basic], variables
- structures [Visual Basic], structure variables
- variables [Visual Basic], structure variables
- structure variables [Visual Basic]
ms.assetid: 156872f8-aabc-4454-8e2d-f2253c3c13c9
ms.openlocfilehash: 9a6e542e297a17f44d929235530ae6058cf13a36
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58816328"
---
# <a name="structure-variables-visual-basic"></a>Variables de structure (Visual Basic)
Une fois que vous avez créé une structure, vous pouvez déclarer des variables de niveau de la procédure et au niveau du module en tant que type. Par exemple, vous pouvez créer une structure qui enregistre les informations concernant un système informatique. Cela est illustré par l'exemple suivant.  
  
```  
Public Structure systemInfo  
    Public cPU As String  
    Public memory As Long  
    Public purchaseDate As Date  
End Structure  
```  
  
 Vous pouvez désormais déclarer des variables de ce type. L’exemple suivant illustre cela.  
  
```  
Dim mySystem, yourSystem As systemInfo  
```  
  
> [!NOTE]
>  Dans les classes et les modules, les structures déclarées à l’aide de la [instruction Dim](../../../../visual-basic/language-reference/statements/dim-statement.md) par défaut d’un accès public. Si vous envisagez une structure soit privée, assurez-vous que vous déclarez à l’aide de la [privé](../../../../visual-basic/language-reference/modifiers/private.md) mot clé.  
  
## <a name="access-to-structure-values"></a>Accès aux valeurs de la Structure  
 Pour attribuer et récupérer des valeurs à partir des éléments d’une variable de structure, vous utilisez la même syntaxe que vous utilisez pour définir et obtenir des propriétés sur un objet. Vous placez l’opérateur d’accès au membre (`.`) entre le nom de variable de structure et le nom d’élément. L’exemple suivant accède aux éléments des variables déclarées précédemment en tant que type `systemInfo`.  
  
```  
mySystem.cPU = "486"  
Dim tooOld As Boolean  
If yourSystem.purchaseDate < #1/1/1992# Then tooOld = True  
```  
  
## <a name="assigning-structure-variables"></a>Affectation de Variables de Structure  
 Vous pouvez également affecter une variable à un autre si les deux sont du même type de structure. Cette opération copie tous les éléments d’une structure aux éléments correspondants dans l’autre. L’exemple suivant illustre cela.  
  
```  
yourSystem = mySystem  
```  
  
 Si un élément de structure est un type référence, comme un `String`, `Object`, ou tableau, le pointeur vers les données est copié. Dans l’exemple précédent, si `systemInfo` avait inclus une variable objet, puis l’exemple précédent aurait copié le pointeur à partir de `mySystem` à `yourSystem`, et une modification apportée aux données de l’objet via une structure serait en vigueur lors de l’accès par l’autre structure.  
  
## <a name="see-also"></a>Voir aussi

- [Types de données](../../../../visual-basic/programming-guide/language-features/data-types/index.md)
- [Types de données élémentaires](../../../../visual-basic/programming-guide/language-features/data-types/elementary-data-types.md)
- [Types de données composites](../../../../visual-basic/programming-guide/language-features/data-types/composite-data-types.md)
- [Value Types and Reference Types](../../../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md)
- [Structures](../../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [Dépannage des types de données](../../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md)
- [Guide pratique pour déclarer une structure](../../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)
- [Structures et autres éléments de programmation](../../../../visual-basic/programming-guide/language-features/data-types/structures-and-other-programming-elements.md)
- [Structures et classes](../../../../visual-basic/programming-guide/language-features/data-types/structures-and-classes.md)
- [Structure (instruction)](../../../../visual-basic/language-reference/statements/structure-statement.md)
