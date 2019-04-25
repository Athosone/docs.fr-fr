---
title: Opérateurs surchargeables - Guide de programmation C#
ms.custom: seodec18
ms.date: 08/27/2018
helpviewer_keywords:
- C# language, operator overloading
- operator overloading [C#]
ms.assetid: 390d9d01-79fc-40ab-9ed3-0bf448da1b6a
ms.openlocfilehash: d0a5555bbe68aa82218c1dbe3d24705b26aff9c8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59296574"
---
# <a name="overloadable-operators-c-programming-guide"></a>Opérateurs surchargeables (Guide de programmation C#)

Dans C#, les types définis par l’utilisateur peuvent surcharger des opérateurs en définissant des fonctions membres statiques à l’aide du mot clé [operator](../../language-reference/keywords/operator.md). Toutefois, tous les opérateurs ne peuvent pas être surchargés et d'autres présentent des restrictions, comme indiqué dans ce tableau :

| Opérateurs | Possibilité de surcharge |
| --------- | --------------- |
|[+](../../language-reference/operators/addition-operator.md), [-](../../language-reference/operators/subtraction-operator.md), [!](../../language-reference/operators/boolean-logical-operators.md#logical-negation-operator-), [~](../../language-reference/operators/bitwise-complement-operator.md), [++](../../language-reference/operators/arithmetic-operators.md#increment-operator-), [--](../../language-reference/operators/arithmetic-operators.md#decrement-operator---), [true](../../language-reference/keywords/true-false-operators.md), [false](../../language-reference/keywords/true-false-operators.md)|Ces opérateurs unaires peuvent être surchargés.|
|[+](../../language-reference/operators/addition-operator.md), [-](../../language-reference/operators/subtraction-operator.md), [\*](../../language-reference/operators/arithmetic-operators.md#multiplication-operator-), [/](../../language-reference/operators/arithmetic-operators.md#division-operator-), [%](../../language-reference/operators/arithmetic-operators.md#remainder-operator-), [&](../../language-reference/operators/and-operator.md), [&#124;](../../language-reference/operators/or-operator.md), [^](../../language-reference/operators/xor-operator.md), [\<\<](../../language-reference/operators/left-shift-operator.md), [>>](../../language-reference/operators/right-shift-operator.md)|Ces opérateurs binaires peuvent être surchargés.|
|[==](../../language-reference/operators/equality-operators.md#equality-operator-), [!=](../../language-reference/operators/equality-operators.md#inequality-operator-), [\<](../../language-reference/operators/less-than-operator.md), [>](../../language-reference/operators/greater-than-operator.md), [\<=](../../language-reference/operators/less-than-equal-operator.md), [>=](../../language-reference/operators/greater-than-equal-operator.md)|Les opérateurs de comparaison peuvent être surchargés (mais consultez la remarque qui suit ce tableau).|
|[&&](../../language-reference/operators/boolean-logical-operators.md#conditional-logical-and-operator-), [&#124;&#124;](../../language-reference/operators/boolean-logical-operators.md#conditional-logical-or-operator-)|Les opérateurs logiques conditionnels ne peuvent pas être surchargés, mais ils sont évalués à l’aide des opérateurs surchargeables `&` et <code>&#124;</code>.|
|[&#91;&#93;](../../language-reference/operators/index-operator.md)|L’opérateur d’indexation de tableau ne peut pas être surchargé, mais vous pouvez définir des [indexeurs](../indexers/index.md).|
|[(T)x](../../language-reference/operators/invocation-operator.md)|L’opérateur de cast ne peut pas être surchargé, mais vous pouvez définir de nouveaux opérateurs de conversion (consultez [explicit](../../language-reference/keywords/explicit.md) et [implicit](../../language-reference/keywords/implicit.md)).|
|[+=](../../language-reference/operators/addition-assignment-operator.md), [-=](../../language-reference/operators/subtraction-assignment-operator.md), [\*=](../../language-reference/operators/arithmetic-operators.md#compound-assignment), [/=](../../language-reference/operators/arithmetic-operators.md#compound-assignment), [%=](../../language-reference/operators/arithmetic-operators.md#compound-assignment), [&=](../../language-reference/operators/and-assignment-operator.md), [&#124;=](../../language-reference/operators/or-assignment-operator.md), [^=](../../language-reference/operators/xor-assignment-operator.md), [\<\<=](../../language-reference/operators/left-shift-assignment-operator.md), [>>=](../../language-reference/operators/right-shift-assignment-operator.md)|Les opérateurs d’assignation ne peuvent pas être surchargés explicitement. Toutefois, quand vous surchargez un opérateur binaire, l’opérateur d’assignation correspondant, le cas échéant, est aussi implicitement surchargé. Par exemple, `+=` est évalué à l’aide de l’opérateur `+`, qui peut être surchargé.|
|[=](../../language-reference/operators/assignment-operator.md), [.](../../language-reference/operators/member-access-operator.md), [?:](../../language-reference/operators/conditional-operator.md), [??](../../language-reference/operators/null-coalescing-operator.md), [->](../../language-reference/operators/dereference-operator.md), [=>](../../language-reference/operators/lambda-operator.md), [f(x)](../../language-reference/operators/invocation-operator.md), [as](../../language-reference/keywords/as.md), [checked](../../language-reference/keywords/checked.md), [unchecked](../../language-reference/keywords/unchecked.md), [default](../../programming-guide/statements-expressions-operators/default-value-expressions.md), [delegate](../../programming-guide/statements-expressions-operators/anonymous-methods.md), [is](../../language-reference/keywords/is.md), [new](../../language-reference/keywords/new.md), [sizeof](../../language-reference/keywords/sizeof.md), [typeof](../../language-reference/keywords/typeof.md)|Ces opérateurs ne peuvent pas être surchargés.|

> [!NOTE]
> Les opérateurs de comparaison, s'ils sont surchargés, doivent l'être par paires ; autrement dit, si `==` est surchargé, `!=` doit également l'être. L’inverse est vrai aussi, quand la surcharge de `!=` nécessite une surcharge de `==`. Il en est de même pour les opérateurs de comparaison `<` et `>`, et pour `<=` et `>=`.

Pour savoir comment surcharger un opérateur, consultez l’article sur le mot clé [operator](../../language-reference/keywords/operator.md).

## <a name="see-also"></a>Voir aussi

- [Guide de programmation C#](../index.md)
- [Instructions, expressions et opérateurs](index.md)
- [Opérateurs](operators.md)
- [Opérateurs C#](../../language-reference/operators/index.md)
- Article [Why are overloaded operators always static in C#?](https://blogs.msdn.microsoft.com/ericlippert/2007/05/14/why-are-overloaded-operators-always-static-in-c/)
