---
title: Implements, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Implements
- Implements
helpviewer_keywords:
- Implements statement [Visual Basic], syntax
- Implements statement [Visual Basic]
- interface implementation [Visual Basic], Implements statement
ms.assetid: 1fafb83f-f55a-4215-8ea9-681e8622613d
ms.openlocfilehash: 1f0c6b052ead303e0b43465dac2067422abc4ef8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58818867"
---
# <a name="implements-statement"></a>Implements, instruction
Spécifie une ou plusieurs interfaces, ou les membres d’interface, qui doivent être implémentées dans la classe ou sur définition de la structure dans laquelle elle apparaît.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Implements interfacename [, ...]  
-or-  
Implements interfacename.interfacemember [, ...]  
```  
  
## <a name="parts"></a>Composants  
 `interfacename`  
 Obligatoire. Une interface dont les propriétés, procédures et les événements doivent être implémentées par des membres correspondants dans la classe ou structure.  
  
 `interfacemember`  
 Obligatoire. Le membre d’une interface est implémentée.  
  
## <a name="remarks"></a>Notes  
 Une interface est une collection de prototypes représentant les membres (propriétés, procédures et événements) encapsule l’interface. Interfaces contiennent uniquement les déclarations des membres ; classes et structures implémentent ces membres. Pour plus d’informations, consultez [Interfaces](../../../visual-basic/programming-guide/language-features/interfaces/index.md).  
  
 Le `Implements` instruction doit suivre immédiatement le `Class` ou `Structure` instruction.  
  
 Lorsque vous implémentez une interface, vous devez implémenter tous les membres déclarés dans l’interface. L’omission de n’importe quel membre est considérée comme une erreur de syntaxe. Pour implémenter un membre, vous spécifiez le [implémente](../../../visual-basic/language-reference/statements/implements-clause.md) mot clé (qui est distinct de la `Implements` instruction) lorsque vous déclarez le membre dans la classe ou structure. Pour plus d’informations, consultez [Interfaces](../../../visual-basic/programming-guide/language-features/interfaces/index.md).  
  
 Les classes peuvent utiliser [privé](../../../visual-basic/language-reference/modifiers/private.md) implémentations des propriétés et procédures, mais ces membres sont accessibles uniquement par la conversion d’une instance de la classe d’implémentation dans une variable déclarée comme étant du type de l’interface.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment utiliser le `Implements` instruction pour implémenter des membres d’une interface. Il définit une interface nommée `ICustomerInfo` avec un événement, une propriété et une procédure. La classe `customerInfo` implémente tous les membres définis dans l’interface.  
  
 [!code-vb[VbVbalrStatements#33](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#33)]  
  
 Notez que la classe `customerInfo` utilise le `Implements` instruction sur une ligne de code source distinct pour indiquer que la classe implémente tous les membres de la `ICustomerInfo` interface. Ensuite, chaque membre dans la classe utilise le `Implements` mot clé dans le cadre de sa déclaration de membre pour indiquer qu’il implémente ce membre d’interface.  
  
## <a name="example"></a>Exemple  
 Les deux procédures suivantes montrent comment vous pouvez utiliser l’interface implémentée dans l’exemple précédent. Pour tester l’implémentation, ajoutez ces procédures à votre projet et l’appel de la `testImplements` procédure.  
  
 [!code-vb[VbVbalrStatements#34](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#34)]  
  
## <a name="see-also"></a>Voir aussi

- [Implements](../../../visual-basic/language-reference/statements/implements-clause.md)
- [Interface (instruction)](../../../visual-basic/language-reference/statements/interface-statement.md)
- [Interfaces](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
