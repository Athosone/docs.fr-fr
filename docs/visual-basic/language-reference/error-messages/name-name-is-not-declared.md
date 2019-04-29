---
title: Le nom '<name>' n'est pas déclaré
ms.date: 10/10/2018
f1_keywords:
- bc30451
- vbc30451
helpviewer_keywords:
- BC30451
ms.assetid: 765f099b-e21e-47c6-a906-a065444e56b3
ms.openlocfilehash: 3aadc49f91021409123550ba2712f1acf5b99d83
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61651023"
---
# <a name="name-name-is-not-declared"></a>Nom de «\<nom >' n’est pas déclaré
Une instruction fait référence à un élément de programmation, mais le compilateur ne peut pas trouver un élément portant ce nom exact.  
  
 **ID d’erreur :** BC30451  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Vérifiez l’orthographe du nom dans l’instruction de référence. Visual Basic respecte la casse, mais toute autre variation dans l’orthographe est considérée comme un nom complètement différent. Notez que le caractère de soulignement (`_`) fait partie du nom et donc de l’orthographe.  
  
2. Vérifiez que vous disposez de l’opérateur d’accès au membre (`.`) entre un objet et son membre. Par exemple, si vous disposez d’un contrôle <xref:System.Windows.Forms.TextBox> dont le nom est `TextBox1`, pour accéder à sa propriété <xref:System.Windows.Forms.TextBoxBase.Text%2A> , vous devez taper `TextBox1.Text`. Si, au lieu de cela, vous tapez `TextBox1Text`, vous créez un nom différent.  
  
3. Si l’orthographe est correcte et que la syntaxe n’importe quel objet d’accès de membre est correcte, vérifiez que l’élément a été déclaré. Pour plus d’informations, consultez [Declared Elements](../../programming-guide/language-features/declared-elements/index.md).  
  
4. Si l’élément de programmation a été déclaré, vérifiez qu’il est dans la portée. Si l’instruction de référence est en dehors de la région déclarant l’élément de programmation, vous devrez peut-être qualifier le nom d’élément. Pour plus d'informations, consultez [Scope in Visual Basic](../../programming-guide/language-features/declared-elements/scope.md).  

5. Si vous n’utilisez pas un type qualifié complet ou le nom de type et de membre (par exemple, votre code fait référence à une propriété en tant que `MethodInfo.Name` au lieu de `System.Reflection.MethodInfo.Name`), ajoutez un [Imports, instruction](../statements/imports-statement-net-namespace-and-type.md).

6. Si vous essayez de compiler un projet de SDK-style (un projet avec un \*fichier .vbproj qui commence par la ligne `<Project Sdk="Microsoft.NET.Sdk">`) et le message d’erreur fait référence à un type ou membre dans l’assembly Microsoft.VisualBasic.dll, configurez votre application Compilez avec une référence à la bibliothèque Runtime Visual Basic. Par défaut, un sous-ensemble de la bibliothèque est incorporé dans votre assembly dans un projet de style SDK.

   Par exemple, l’exemple suivant compilation échoue, car le <xref:Microsoft.VisualBasic.CompilerServices.Conversions.ToInteger%2A?displayProperty=fullName> méthode ne peut pas être trouvée. Il n’est pas incorporé dans le sous-ensemble du Runtime Visual Basic inclus avec votre application.  

   [!code-vb[BC30451](~/samples/snippets/visualbasic/language-reference/error-messages/bc30451/program1.vb)]

   Pour résoudre cette erreur, ajoutez le `<VBRuntime>Default</VBRuntime>` élément aux projets `<PropertyGroup>` section, comme le montre de fichier de projet Visual Basic suivant.

   [!code-vb[BC30451](~/samples/snippets/visualbasic/language-reference/error-messages/bc30451/vbruntime.vbproj?highlight=6)]

## <a name="see-also"></a>Voir aussi

- [Liste des déclarations et des constantes](../../../visual-basic/language-reference/keywords/declarations-and-constants-summary.md)
- [Conventions d’affectation de noms de Visual Basic](../../../visual-basic/programming-guide/program-structure/naming-conventions.md)
- [Noms d’éléments déclarés](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md)
- [Références aux éléments déclarés](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)
