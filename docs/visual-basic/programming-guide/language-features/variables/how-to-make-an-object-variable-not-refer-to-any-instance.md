---
title: 'Procédure : Crée un objet de Variable ne fait pas référence à n’importe quelle Instance (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- Nothing keyword [Visual Basic], variable assignment
- object variables [Visual Basic], null reference
ms.assetid: e6d30578-bdae-4142-a3ac-a10697bf696a
ms.openlocfilehash: 373d4ae84c44b212ad02b0b4266af75921e40423
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61769055"
---
# <a name="how-to-make-an-object-variable-not-refer-to-any-instance-visual-basic"></a>Procédure : Crée un objet de Variable ne fait pas référence à n’importe quelle Instance (Visual Basic)
Vous pouvez dissocier une variable objet à partir de n’importe quelle instance d’objet en lui affectant [rien](../../../../visual-basic/language-reference/nothing.md).  
  
### <a name="to-disassociate-an-object-variable-from-any-object-instance"></a>Pour dissocier une variable objet à partir de n’importe quelle instance d’objet  
  
- Affectez à la variable `Nothing` dans une instruction d’assignation.  
  
    ```  
    ' Assume account is a defined class  
    Dim currentAccount As account  
    currentAccount = Nothing  
    ```  
  
## <a name="robust-programming"></a>Programmation fiable  
 Si votre code tente d’accéder à un membre d’une variable objet qui a été défini sur `Nothing`, un <xref:System.NullReferenceException> se produit. Si vous définissez une variable objet `Nothing` fréquemment, ou s’il est possible de la variable n’est pas initialisée, il est judicieux de placer les accès aux membres dans un `Try...Catch...Finally` bloc.  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 Si vous utilisez une variable d’objet pour les objets qui contiennent des données confidentielles ou sensibles, vous pouvez définir la variable `Nothing` lorsque vous N'utilisez pas activement un de ces objets. Cela réduit le risque de code malveillant accède aux données.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.NullReferenceException>
- [Variables objets](../../../../visual-basic/programming-guide/language-features/variables/object-variables.md)
- [Assignation des variables objets](../../../../visual-basic/programming-guide/language-features/variables/object-variable-assignment.md)
- [Nothing](../../../../visual-basic/language-reference/nothing.md)
- [Try...Catch...Finally (instruction)](../../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
