---
title: Types valeur - Référence C#
ms.custom: seodec18
ms.date: 11/26/2018
f1_keywords:
- cs.valuetypes
helpviewer_keywords:
- value types [C#]
- types [C#], value types
- C# language, value types
ms.assetid: 471eb994-2958-49d5-a6be-19b4313f80a3
ms.openlocfilehash: 77aed78e7822e06b3b1e6c48b07790d93e09559c
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53612723"
---
# <a name="value-types-c-reference"></a>Types valeur (référence C#)

Il existe deux sortes de types valeur :

- [Structs](struct.md)

- [Énumérations](enum.md)

## <a name="main-features-of-value-types"></a>Principales caractéristiques des types valeur

Une variable d’un type valeur contient une valeur du type. Par exemple, une variable du type `int` peut contenir la valeur `42`. Ce type s’oppose au type référence, qui contient une référence à une instance du type, également appelée objet. Lorsque vous affectez une nouvelle valeur à une variable d’un type valeur, cette valeur est copiée. Si vous affectez une nouvelle valeur à une variable d’un type référence, la référence est copiée, et non l’objet lui-même.

Tous les types valeur sont implicitement dérivés de <xref:System.ValueType?displayProperty=nameWithType>.

Contrairement aux types référence, vous ne pouvez pas faire dériver un nouveau type d’un type valeur. En revanche, comme les types référence, les structs peuvent implémenter des interfaces.

Les variables de type valeur ne peut pas être `null` par défaut. Toutefois, les variables des [types Nullable](../../../csharp/programming-guide/nullable-types/index.md) correspondants peuvent être `null`.

Chaque type valeur a un constructeur par défaut implicite qui initialise la valeur par défaut de ce type. Pour plus d’informations sur les valeurs par défaut des types valeur, voir [Tableau des valeurs par défaut](default-values-table.md).

## <a name="simple-types"></a>Types simples

Les *types simples* sont un ensemble de types struct prédéfinis fournis par C#, composé des types suivants :

- [Types intégraux](integral-types-table.md) : types numériques entiers et type [char](char.md)
- [Types virgule flottante](floating-point-types-table.md)
- [bool](bool.md)

Les types simples sont identifiés par des mots clés, qui sont simplement des alias de types struct prédéfinis dans l’espace de noms <xref:System>. Par exemple, [int](int.md) est un alias de <xref:System.Int32?displayProperty=nameWithType>. Pour connaître la liste complète des alias, voir [Tableau des types intégrés](built-in-types-table.md).

Les types simples diffèrent des autres types struct en ce qu’ils autorisent des opérations supplémentaires :

- Les types simples peuvent être initialisés à l’aide de littéraux. Par exemple, `'A'` est un littéral de type `char`, tandis que `2001` est un littéral de type `int`.

- Vous pouvez déclarer des constantes des types simples avec le mot clé [const](const.md). Il n’est pas possible d’avoir des constantes d’autres types struct.

- Les expressions constantes, dont les opérandes sont tous des constantes de type simple, sont évaluées au moment de la compilation.

Pour plus d’informations, voir la section [Types simples](~/_csharplang/spec/types.md#simple-types) de la [spécification du langage C#](../language-specification/index.md).

## <a name="initializing-value-types"></a>Initialiser des types valeur

En C#, les variables locales doivent être initialisées avant d’être utilisées. Par exemple, vous pouvez déclarer une variable locale sans l’initialiser comme dans l’exemple suivant :

```csharp
int myInt;
```

Vous ne pouvez pas l’utiliser avant de l’avoir initialisée. Vous pouvez l’initialiser à l’aide de l’instruction suivante :

```csharp
myInt = new int();  // Invoke default constructor for int type.
```

Cette instruction est équivalente à l’instruction suivante :

```csharp
myInt = 0;         // Assign an initial value, 0 in this example.
```

Bien entendu, vous pouvez intégrer la déclaration et l’initialisation dans une même instruction comme dans les exemples suivants :

```csharp
int myInt = new int();
```

– ou –

```csharp
int myInt = 0;
```

L’opérateur [new](new.md) permet d’appeler le constructeur par défaut du type spécifique et d’assigner la valeur par défaut à la variable. Dans l’exemple précédent, le constructeur par défaut a assigné la valeur `0` à `myInt`. Pour plus d’informations sur les valeurs affectées en appelant les constructeurs par défaut, voir [Tableau des valeurs par défaut](default-values-table.md).

Avec les types définis par l’utilisateur, l’opérateur [new](new.md) permet d’appeler le constructeur par défaut. Par exemple, l’instruction suivante appelle le constructeur par défaut du struct `Point` :

```csharp
Point p = new Point(); // Invoke default constructor for the struct.
```

Après cet appel, le struct est considéré comme définitivement assigné ; autrement dit, tous ses membres sont initialisés avec leurs valeurs par défaut.

Pour plus d'informations sur l'opérateur `new`, voir [new](new.md).

Pour plus d’informations sur la mise en forme de la sortie des types numériques, voir [Tableau des formats des résultats numériques](formatting-numeric-results-table.md).

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Mots clés C#](index.md)
- [Types](types.md)
- [Tableaux de référence des types](reference-tables-for-types.md)
- [Types référence](reference-types.md)
- [Types Nullable](../../programming-guide/nullable-types/index.md)