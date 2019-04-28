---
title: Occultation dans Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- inheritance [Visual Basic], shadowing
- overriding, and shadowing
- shadowing
- duplicate names [Visual Basic]
- shadowing, by inheritance
- declared elements [Visual Basic], referencing
- shadowing, by scope
- declared elements [Visual Basic], hiding
- naming conflicts, shadowing
- declared elements [Visual Basic], shadowing
- shadowing, and overriding
- scope [Visual Basic], shadowing
- Shadows keyword [Visual Basic], about
- objects [Visual Basic], names
- names [Visual Basic], shadowing
ms.assetid: 54bb4c25-12c4-4181-b4a0-93546053964e
ms.openlocfilehash: 9ad992a53618fa2f410e0b0fb23886c30136384f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61917899"
---
# <a name="shadowing-in-visual-basic"></a>Occultation dans Visual Basic
Lorsque deux éléments de programmation partagent le même nom, un d’eux peut masquer, ou *ombre*, autre. Dans ce cas, l’élément occulté n’est pas disponible pour référence ; au lieu de cela, lorsque votre code utilise le nom d’élément, le compilateur Visual Basic les résout à l’élément d’occultation.  
  
## <a name="purpose"></a>Objectif  
 L’objectif principal d’une occultation est de protéger la définition de vos membres de classe. La classe de base peut subir un changement qui crée un élément avec le même nom qu’un que vous avez déjà défini. Si cela se produit, le `Shadows` modificateur force références de votre classe à être résolues vers le membre que vous avez défini, et non vers le nouvel élément de classe de base.  
  
## <a name="types-of-shadowing"></a>Types d’occultation  
 Un élément peut occulter un autre élément de deux manières différentes. L’élément d’occultation peut être déclaré dans une sous-région de la région contenant l’élément occulté, dans laquelle s’effectue l’occultation de cas *via étendue*. Une classe dérivée peut redéfinir un membre de classe de base, dans lequel cas l’occultation est effectuée *via l’héritage*.  
  
### <a name="shadowing-through-scope"></a>Occultation par portée  
 Il est possible pour la programmation des éléments dans le même module, classe ou structure peuvent avoir le même nom mais une portée différente. Lorsque deux éléments sont déclarés de cette manière, et le code fait référence au nom qu’ils partagent, l’élément avec la portée plus restreinte occulte l’autre élément (la portée de bloc est la plus restreinte).  
  
 Par exemple, un module peut définir un `Public` variable nommée `temp`, et une procédure dans le module peut déclarer une variable locale nommée également `temp`. Références à `temp` depuis la procédure, accéder à la variable locale, tandis que les références à `temp` à partir d’en dehors de la procédure accèdent le `Public` variable. Dans ce cas, la variable de procédure `temp` occulte la variable de module `temp`.  
  
 L’illustration suivante montre deux variables, toutes deux nommées `temp`. La variable locale `temp` occulte la variable membre `temp` lors de l’accès à partir de sa propre procédure `p`. Toutefois, le `MyClass` mot clé contourne l’occultation et accède à la variable de membre.  
  
 ![Graphique montrant occultation par portée.](./media/shadowing/shadow-scope-diagram.gif)
  
 Pour obtenir un exemple d’une occultation par portée, consultez [Comment : Masquer une Variable portant le même nom que votre Variable](../../../../visual-basic/programming-guide/language-features/declared-elements/how-to-hide-a-variable-with-the-same-name-as-your-variable.md).  
  
### <a name="shadowing-through-inheritance"></a>Occultation par héritage  
 Si une classe dérivée redéfinit un élément de programmation hérité d’une classe de base, l’élément qui redéfinit occulte l’élément d’origine. Vous pouvez occulter tout type d’élément déclaré, ou ensemble d’éléments surchargés, avec un autre type. Par exemple, un `Integer` variable peut occulter un `Function` procédure. Si vous masquez une procédure avec une autre procédure, vous pouvez utiliser une autre liste de paramètres et un type de retour différent.  
  
 L’illustration suivante montre une classe de base `b` et une classe dérivée `d` qui hérite de `b`. La classe de base définit une procédure nommée `proc`, et la classe dérivée l’occulte avec une autre procédure du même nom. La première `Call` instruction accède à l’occultation `proc` dans la classe dérivée. Toutefois, le `MyBase` mot clé contourne l’occultation et accède à la procédure occultée dans la classe de base.  
  
 ![Diagramme graphique d'une occultation par héritage](./media/shadowing/shadowing-inherit-diagram.gif)  
  
 Pour obtenir un exemple d’une occultation par héritage, consultez [Comment : Masquer une Variable portant le même nom que votre Variable](../../../../visual-basic/programming-guide/language-features/declared-elements/how-to-hide-a-variable-with-the-same-name-as-your-variable.md) et [Comment : Masquer une Variable héritée](../../../../visual-basic/programming-guide/language-features/declared-elements/how-to-hide-an-inherited-variable.md).  
  
#### <a name="shadowing-and-access-level"></a>Occultation et niveau d’accès  
 L’élément d’occultation n’est pas toujours accessible à partir du code à l’aide de la classe dérivée. Par exemple, il peut être déclaré `Private`. Dans ce cas, l’occultation échoue et le compilateur résout toute référence au même élément que vous avez si aucun occultation. Cet élément est l’élément accessible la qui moins d’étapes vers l’arrière à partir de la classe d’occultation. Si l’élément occulté est une procédure, la résolution consiste à la version la plus proche accessible avec le même nom, la liste des paramètres et le type de retour.  
  
 L’exemple suivant montre une hiérarchie d’héritage de trois classes. Chaque classe définit un `Sub` procédure `display`, et chaque classe dérivée occulte le `display` procédure dans sa classe de base.  
  
```  
Public Class firstClass  
    Public Sub display()  
        MsgBox("This is firstClass")  
    End Sub  
End Class  
Public Class secondClass  
    Inherits firstClass  
    Private Shadows Sub display()  
        MsgBox("This is secondClass")  
    End Sub  
End Class  
Public Class thirdClass  
    Inherits secondClass  
    Public Shadows Sub display()  
        MsgBox("This is thirdClass")  
    End Sub  
End Class  
Module callDisplay  
    Dim first As New firstClass  
    Dim second As New secondClass  
    Dim third As New thirdClass  
    Public Sub callDisplayProcedures()  
        ' The following statement displays "This is firstClass".  
        first.display()  
        ' The following statement displays "This is firstClass".  
        second.display()  
        ' The following statement displays "This is thirdClass".  
        third.display()  
    End Sub  
End Module  
```  
  
 Dans l’exemple précédent, la classe dérivée `secondClass` shadows `display` avec un `Private` procédure. Lorsque module `callDisplay` appels `display` dans `secondClass`, le code appelant est en dehors de `secondClass` , il ne peut pas accéder privé `display` procédure. L’occultation est invalidée et le compilateur résout la référence à la classe de base `display` procédure.  
  
 Toutefois, la classe dérivée supplémentaire `thirdClass` déclare `display` comme `Public`, de sorte que le code dans `callDisplay` peuvent y accéder.  
  
## <a name="shadowing-and-overriding"></a>Occultation et substitution  
 Ne confondez pas l’occultation et substitution. Les deux sont utilisés lorsqu’une classe dérivée hérite d’une classe de base et redéfinissent un élément déclaré par un autre. Mais il existe des différences importantes entre les deux. Pour obtenir une comparaison, consultez [différences entre l’occultation et substitution](../../../../visual-basic/programming-guide/language-features/declared-elements/differences-between-shadowing-and-overriding.md).  
  
## <a name="shadowing-and-overloading"></a>Occultation et surcharge  
 Si vous masquez le même élément de classe de base avec plusieurs éléments dans votre classe dérivée, les éléments occultants deviennent des versions surchargées de cet élément. Pour plus d'informations, consultez [Procedure Overloading](../../../../visual-basic/programming-guide/language-features/procedures/procedure-overloading.md).  
  
## <a name="accessing-a-shadowed-element"></a>Accès à un élément occulté  
 Lorsque vous accédez à un élément à partir d’une classe dérivée, vous le faites normalement par l’instance actuelle de cette classe dérivée, en qualifiant le nom de l’élément avec la `Me` mot clé. Si votre classe dérivée occulte l’élément dans la classe de base, vous pouvez accéder à l’élément de la classe de base en qualifiant avec le `MyBase` mot clé.  
  
 Pour obtenir un exemple d’accès à un élément occulté, consultez [Comment : Accéder à une Variable masquée par une classe dérivée](../../../../visual-basic/programming-guide/language-features/declared-elements/how-to-access-a-variable-hidden-by-a-derived-class.md).  
  
### <a name="declaration-of-the-object-variable"></a>Déclaration de la Variable objet  
 Création de la variable objet peut également déterminer si la classe dérivée accède à un élément d’occultation ou l’élément occulté. L’exemple suivant crée deux objets à partir d’une classe dérivée, mais un seul objet est déclaré en tant que classe de base et l’autre en tant que la classe dérivée.  
  
```  
Public Class baseCls  
    ' The following statement declares the element that is to be shadowed.  
    Public z As Integer = 100  
End Class  
Public Class dervCls  
    Inherits baseCls  
    ' The following statement declares the shadowing element.  
    Public Shadows z As String = "*"  
End Class  
Public Class useClasses  
    ' The following statement creates the object declared as the base class.  
    Dim basObj As baseCls = New dervCls()  
    ' Note that dervCls widens to its base class baseCls.  
    ' The following statement creates the object declared as the derived class.  
    Dim derObj As dervCls = New dervCls()  
    Public Sub showZ()   
    ' The following statement outputs 100 (the shadowed element).  
        MsgBox("Accessed through base class: " & basObj.z)  
    ' The following statement outputs "*" (the shadowing element).  
        MsgBox("Accessed through derived class: " & derObj.z)  
    End Sub  
End Class  
```  
  
 Dans l’exemple précédent, la variable `basObj` est déclaré comme classe de base. Affectation d’un `dervCls` objet constitue une conversion étendue et est donc valide. Toutefois, la classe de base ne peut pas accéder à la version de masquage de la variable `z` dans la classe dérivée, le compilateur résout `basObj.z` à la valeur d’origine de la classe de base.  
  
## <a name="see-also"></a>Voir aussi

- [Références aux éléments déclarés](../../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)
- [Portée dans Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/scope.md)
- [Conversions étendues et restrictives](../../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
- [Shadows](../../../../visual-basic/language-reference/modifiers/shadows.md)
- [Overrides](../../../../visual-basic/language-reference/modifiers/overrides.md)
- [Me, My, MyBase et MyClass](../../../../visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass.md)
- [Éléments fondamentaux de l’héritage](../../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md)
