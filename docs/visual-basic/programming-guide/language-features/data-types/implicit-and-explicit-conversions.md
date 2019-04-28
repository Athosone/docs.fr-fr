---
title: Conversions implicites et explicites (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- conversions [Visual Basic], type
- variables [Visual Basic], changing data type
- casting
- conversions [Visual Basic], data type
- type conversion [Visual Basic], implicit conversions
- CType function [Visual Basic], conversions
- casting, data types
- data type conversion [Visual Basic], explicit
- type conversion [Visual Basic], explicit conversions
- data types [Visual Basic], casting
- conversions [Visual Basic], implicit
- explicit data type conversions [Visual Basic]
- conversions [Visual Basic]
- changing data types [Visual Basic]
- conversions [Visual Basic], explicit
- data type conversion [Visual Basic], implicit
- implicit data type conversions [Visual Basic]
ms.assetid: 77de1659-af8a-492c-967e-e7ef60ccce66
ms.openlocfilehash: 82ff710629089cd14c7e982b4afa4301d0790811
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62008252"
---
# <a name="implicit-and-explicit-conversions-visual-basic"></a>Conversions implicites et explicites (Visual Basic)
Un *conversion implicite* ne nécessite pas une syntaxe spéciale dans le code source. Dans l’exemple suivant, Visual Basic convertit implicitement la valeur de `k` à une valeur à virgule flottante simple précision avant de l’assigner à `q`.  
  
```  
Dim k As Integer  
Dim q As Double  
' Integer widens to Double, so you can do this with Option Strict On.  
k = 432  
q = k  
```  
  
 Un *conversion explicite* utilise une conversion de type mot clé. Visual Basic fournit plusieurs de ces mots clés, qui forcent une expression entre parenthèses au type de données souhaité. Ces mots clés agissent comme des fonctions, mais le compilateur génère le code inline, par conséquent, l’exécution est légèrement plus rapide qu’avec un appel de fonction.  
  
 Dans l’extension suivante de l’exemple précédent, le `CInt` mot clé convertit la valeur de `q` en un entier avant de l’assigner à `k`.  
  
```  
' q had been assigned the value 432 from k.  
q = Math.Sqrt(q)  
k = CInt(q)  
' k now has the value 21 (rounded square root of 432).  
```  
  
## <a name="conversion-keywords"></a>Mots clés de conversion  
 Le tableau suivant présente les mots clés de conversion disponibles.  
  
|Mot clé de conversion de type|Convertit une expression en type de données|Types de données autorisés d’expression à convertir|  
|---|---|---|  
|`CBool`|[Booléen (type de données)](../../../../visual-basic/language-reference/data-types/boolean-data-type.md)|Tout type numérique (y compris `Byte`, `SByte`et les types énumérés), `String`, `Object`|  
|`CByte`|[Byte (type de données)](../../../../visual-basic/language-reference/data-types/byte-data-type.md)|Tout type numérique (y compris `SByte` et les types énumérés), `Boolean`, `String`, `Object`|  
|`CChar`|[Char (type de données)](../../../../visual-basic/language-reference/data-types/char-data-type.md)|`String`, `Object`|  
|`CDate`|[Date (type de données)](../../../../visual-basic/language-reference/data-types/date-data-type.md)|`String`, `Object`|  
|`CDbl`|[Double (type de données)](../../../../visual-basic/language-reference/data-types/double-data-type.md)|Tout type numérique (y compris `Byte`, `SByte`et les types énumérés), `Boolean`, `String`, `Object`|  
|`CDec`|[Decimal (type de données)](../../../../visual-basic/language-reference/data-types/decimal-data-type.md)|Tout type numérique (y compris `Byte`, `SByte`et les types énumérés), `Boolean`, `String`, `Object`|  
|`CInt`|[Integer (type de données)](../../../../visual-basic/language-reference/data-types/integer-data-type.md)|Tout type numérique (y compris `Byte`, `SByte`et les types énumérés), `Boolean`, `String`, `Object`|  
|`CLng`|[Long (type de données)](../../../../visual-basic/language-reference/data-types/long-data-type.md)|Tout type numérique (y compris `Byte`, `SByte`et les types énumérés), `Boolean`, `String`, `Object`|  
|`CObj`|[Object (type de données)](../../../../visual-basic/language-reference/data-types/object-data-type.md)|Tout type|  
|`CSByte`|[SByte (type de données)](../../../../visual-basic/language-reference/data-types/sbyte-data-type.md)|Tout type numérique (y compris `Byte` et les types énumérés), `Boolean`, `String`, `Object`|  
|`CShort`|[Short (type de données)](../../../../visual-basic/language-reference/data-types/short-data-type.md)|Tout type numérique (y compris `Byte`, `SByte`et les types énumérés), `Boolean`, `String`, `Object`|  
|`CSng`|[Single (type de données)](../../../../visual-basic/language-reference/data-types/single-data-type.md)|Tout type numérique (y compris `Byte`, `SByte`et les types énumérés), `Boolean`, `String`, `Object`|  
|`CStr`|[String (type de données)](../../../../visual-basic/language-reference/data-types/string-data-type.md)|Tout type numérique (y compris `Byte`, `SByte`et les types énumérés), `Boolean`, `Char`, `Char` tableau, `Date`, `Object`|  
|`CType`|Type spécifié après la virgule (`,`)|Lors de la conversion vers un *type de données élémentaire* (y compris un tableau d’un type élémentaire), les mêmes types que le mot clé de conversion correspondant<br /><br /> Lors de la conversion vers un *type de données composite*, les interfaces qu’il implémente et les classes dont il hérite<br /><br /> Durant la conversion d’une classe ou une structure sur laquelle vous avez surchargé `CType`, cette classe ou structure|  
|`CUInt`|[UInteger (type de données)](../../../../visual-basic/language-reference/data-types/uinteger-data-type.md)|Tout type numérique (y compris `Byte`, `SByte`et les types énumérés), `Boolean`, `String`, `Object`|  
|`CULng`|[ULong (type de données)](../../../../visual-basic/language-reference/data-types/ulong-data-type.md)|Tout type numérique (y compris `Byte`, `SByte`et les types énumérés), `Boolean`, `String`, `Object`|  
|`CUShort`|[UShort (type de données)](../../../../visual-basic/language-reference/data-types/ushort-data-type.md)|Tout type numérique (y compris `Byte`, `SByte`et les types énumérés), `Boolean`, `String`, `Object`|  
  
## <a name="the-ctype-function"></a>La fonction CType  
 Le [CType Function](../../../../visual-basic/language-reference/functions/ctype-function.md) opère sur deux arguments. Le premier est l’expression à convertir, et la seconde est la classe de type ou l’objet de données de destination. Notez que le premier argument doit être une expression, pas un type.  
  
 `CType` est un *fonction inline*, ce qui signifie que le code compilé effectue la conversion, souvent sans générer une fonction appeler. Cela améliore les performances.  
  
 Pour obtenir une comparaison de `CType` avec les autres mots-clés de conversion de type, consultez [opérateur DirectCast](../../../../visual-basic/language-reference/operators/directcast-operator.md) et [opérateur TryCast](../../../../visual-basic/language-reference/operators/trycast-operator.md).  
  
### <a name="elementary-types"></a>Types élémentaires  
 L'exemple suivant montre l'utilisation de `CType`.  
  
```  
k = CType(q, Integer)  
' The following statement coerces w to the specific object class Label.  
f = CType(w, Label)  
```  
  
### <a name="composite-types"></a>Types composites  
 Vous pouvez utiliser `CType` pour convertir des valeurs pour les types de données composites ou élémentaires. Vous pouvez également l’utiliser pour forcer une classe d’objet pour le type d’un de ses interfaces, comme dans l’exemple suivant.  
  
```  
' Assume class cZone implements interface iZone.  
Dim h As Object  
' The first argument to CType must be an expression, not a type.  
Dim cZ As cZone  
' The following statement coerces a cZone object to its interface iZone.  
h = CType(cZ, iZone)  
```  
  
### <a name="array-types"></a>Types de tableau  
 `CType` peut également convertir les types de données de tableau, comme dans l’exemple suivant.  
  
```  
Dim v() As classV  
Dim obArray() As Object  
' Assume some object array has been assigned to obArray.  
' Check for run-time type compatibility.  
If TypeOf obArray Is classV()  
    ' obArray can be converted to classV.  
    v = CType(obArray, classV())  
End If  
```  
  
 Pour plus d’informations et un exemple, consultez [Conversions de tableau](../../../../visual-basic/programming-guide/language-features/data-types/array-conversions.md).  
  
### <a name="types-defining-ctype"></a>Types définissant CType  
 Vous pouvez définir `CType` sur une classe ou structure que vous avez défini. Cela vous permet de convertir des valeurs vers et depuis le type de votre classe ou structure. Pour plus d’informations et un exemple, consultez [Comment : Définir un opérateur de Conversion](../../../../visual-basic/programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md).  
  
> [!NOTE]
>  Valeurs utilisées avec un mot clé de conversion doivent être valides pour le type de données de destination, ou une erreur se produit. Par exemple, si vous tentez de convertir un `Long` à un `Integer`, la valeur de la `Long` doivent se trouver dans la plage valide pour le `Integer` type de données.  
  
> [!CAUTION]
>  Spécification `CType` à convertir à partir d’un type de classe vers un autre échoue au moment de l’exécution si le type de source ne dérive pas du type de destination. Un tel échec lève une <xref:System.InvalidCastException> exception.  
  
 Toutefois, si un des types est une structure ou classe que vous avez défini et si vous avez défini `CType` sur cette classe ou structure, une conversion peut réussir si elle satisfait aux exigences de votre `CType`. Voir [Guide pratique pour Définir un opérateur de Conversion](../../../../visual-basic/programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md).  
  
 Effectuez une conversion explicite est également appelé *cast* une expression à une classe de type ou l’objet de données donné.  
  
## <a name="see-also"></a>Voir aussi

- [Conversions de type en Visual Basic](../../../../visual-basic/programming-guide/language-features/data-types/type-conversions.md)
- [Conversion entre des chaînes et d’autres types](../../../../visual-basic/programming-guide/language-features/data-types/conversions-between-strings-and-other-types.md)
- [Guide pratique pour Convertir un objet en un autre Type dans Visual Basic](../../../../visual-basic/programming-guide/language-features/data-types/how-to-convert-an-object-to-another-type.md)
- [Structures](../../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [Types de données](../../../../visual-basic/language-reference/data-types/index.md)
- [Fonctions de conversion de types](../../../../visual-basic/language-reference/functions/type-conversion-functions.md)
- [Dépannage des types de données](../../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md)
