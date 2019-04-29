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
# <a name="types-of-string-manipulation-methods-in-visual-basic"></a>Types de méthodes de manipulation de chaînes en Visual Basic
Il existe différentes façons de les analyser et manipuler des chaînes. Certaines des méthodes font partie du langage Visual Basic, et d’autres sont inhérentes à la `String` classe.  
  
## <a name="visual-basic-language-and-the-net-framework"></a>Langage Visual Basic et .NET Framework  
 Méthodes de Visual Basic sont utilisées en tant que fonctions inhérentes du langage. Ils peuvent être utilisés sans qualification dans votre code. L’exemple suivant illustre une utilisation classique d’une commande de manipulation de chaînes Visual Basic :  
  
 [!code-vb[VbVbalrStrings#44](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#44)]  
  
 Dans cet exemple, le `Mid` fonction effectue une opération directe sur `aString` et affecte la valeur à `bString`.  
  
 Pour obtenir la liste des méthodes de manipulation de chaîne Visual Basic, consultez [liste des manipulations de chaîne](../../../../visual-basic/language-reference/keywords/string-manipulation-summary.md).  
  
### <a name="shared-methods-and-instance-methods"></a>Méthodes partagées et des méthodes d’Instance  
 Vous pouvez également manipuler des chaînes avec les méthodes de la `String` classe. Il existe deux types de méthodes de `String`: *partagé* méthodes et *instance* méthodes.  
  
#### <a name="shared-methods"></a>Méthodes partagées  
 Une méthode partagée est une méthode qui provient de la `String` classe lui-même et ne nécessite pas une instance de cette classe fonctionne. Ces méthodes peuvent être qualifiés avec le nom de la classe (`String`) plutôt qu’avec une instance de la `String` classe. Exemple :  
  
 [!code-vb[VbVbalrStrings#45](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#45)]  
  
 Dans l’exemple précédent, le <xref:System.String.Copy%2A?displayProperty=nameWithType> méthode est une méthode statique, qui agit sur une expression qui lui est attribuée et affecte la valeur obtenue vers `bString`.  
  
#### <a name="instance-methods"></a>Méthodes d’instance  
 Méthodes d’instance, en revanche, proviennent d’une instance particulière de `String` et doivent être qualifiés avec le nom d’instance. Exemple :  
  
 [!code-vb[VbVbalrStrings#46](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#46)]  
  
 Dans cet exemple, le <xref:System.String.Substring%2A?displayProperty=nameWithType> méthode est une méthode de l’instance de `String` (autrement dit, `aString`). Elle effectue une opération sur `aString` et assigne cette valeur à `bString`.  
  
 Pour plus d’informations, consultez la documentation pour le <xref:System.String> classe.  
  
## <a name="see-also"></a>Voir aussi

- [Introduction aux chaînes en Visual Basic](../../../../visual-basic/programming-guide/language-features/strings/introduction-to-strings.md)
