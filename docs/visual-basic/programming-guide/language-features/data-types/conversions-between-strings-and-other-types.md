---
title: Conversion entre des chaînes et d'autres types (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- data type conversion [Visual Basic], string
- conversions [Visual Basic], type
- string conversion [Visual Basic]
- conversions [Visual Basic], data type
- type conversion [Visual Basic], string
- regional options
ms.assetid: c3a99596-f09a-44a5-81dd-1b89a094f1df
ms.openlocfilehash: 1e42fca7800a76cab10fd60058e34d31ae8b8830
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58821659"
---
# <a name="conversions-between-strings-and-other-types-visual-basic"></a>Conversion entre des chaînes et d'autres types (Visual Basic)
Vous pouvez convertir la valeur numérique, `Boolean`, ou date/heure de valeur à un `String`. Vous pouvez également convertir dans le sens inverse, à partir d’une valeur de chaîne en type numérique, `Boolean`, ou `Date` , fournie par le contenu de la chaîne peut être interprété comme une valeur valide du type de données de destination. Si cela est impossible, une erreur d’exécution se produit.  
  
 Les conversions de toutes ces affectations dans les deux directions, sont des conversions restrictives. Vous devez utiliser des mots clés de conversion de type (`CBool`, `CByte`, `CDate`, `CDbl`, `CDec`, `CInt`, `CLng`, `CSByte`, `CShort`, `CSng`, `CStr`, `CUInt`, `CULng`, `CUShort`, et `CType`). Le <xref:Microsoft.VisualBasic.Strings.Format%2A> et <xref:Microsoft.VisualBasic.Conversion.Val%2A> fonctions vous donnent un contrôle supplémentaire sur les conversions entre des chaînes et nombres.  
  
 Si vous avez défini une classe ou structure, vous pouvez définir des opérateurs de conversion de type entre `String` et le type de votre classe ou structure. Pour plus d'informations, voir [Procédure : Définir un opérateur de Conversion](../../../../visual-basic/programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md).  
  
## <a name="conversion-of-numbers-to-strings"></a>Conversion de nombres en chaînes  
 Vous pouvez utiliser la `Format` fonction pour convertir un nombre en une chaîne mise en forme, qui peut inclure non seulement les chiffres appropriés, mais aussi mettre en forme de symboles comme un symbole monétaire (tel que `$`), des milliers séparateurs ou *groupement des chiffres symboles* (tel que `,`) et un séparateur décimal (tel que `.`). `Format` utilise automatiquement les symboles appropriés en fonction de la **Options régionales** paramètres spécifiés dans le Windows **le panneau de configuration**.  
  
 Notez que la concaténation (`&`) opérateur peut convertir implicitement un nombre en une chaîne, comme le montre l’exemple suivant.  
  
```  
' The following statement converts count to a String value.  
Str = "The total count is " & count  
```  
  
## <a name="conversion-of-strings-to-numbers"></a>Conversion de chaînes en nombres  
 Vous pouvez utiliser le `Val` fonction pour convertir explicitement les chiffres d’une chaîne en nombre. `Val` lit la chaîne jusqu'à ce qu’il rencontre un caractère autre qu’un chiffre, une espace, un onglet, un saut de ligne ou une période. Les séquences « & O » et « & H » altèrent la base du système de numération et mettre fin à l’analyse. Jusqu'à ce qu’il s’arrête de lire, `Val` convertit tous les caractères appropriés en une valeur numérique. Par exemple, l’instruction suivante retourne la valeur `141.825`.  
  
 `Val("   14   1.825 miles")`  
  
 Lorsque Visual Basic convertit une chaîne en valeur numérique, il utilise le **Options régionales** paramètres spécifiés dans le Windows **le panneau de configuration** pour interpréter les milliers separator, séparateur décimal, et symbole de devise. Cela signifie qu’une conversion peut réussir avec certains paramètres, mais pas une autre. Par exemple, `"$14.20"` est acceptable dans les paramètres régionaux anglais (États-Unis), mais pas dans tous les paramètres régionaux Français.  
  
## <a name="see-also"></a>Voir aussi

- [Conversions de type en Visual Basic](../../../../visual-basic/programming-guide/language-features/data-types/type-conversions.md)
- [Conversions étendues et restrictives](../../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
- [Conversions implicites et explicites](../../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)
- [Guide pratique pour Convertir un objet en un autre Type dans Visual Basic](../../../../visual-basic/programming-guide/language-features/data-types/how-to-convert-an-object-to-another-type.md)
- [Conversions de tableau](../../../../visual-basic/programming-guide/language-features/data-types/array-conversions.md)
- [Types de données](../../../../visual-basic/language-reference/data-types/index.md)
- [Fonctions de conversion de types](../../../../visual-basic/language-reference/functions/type-conversion-functions.md)
- [Introduction aux applications internationales basées sur le .NET Framework](/visualstudio/ide/introduction-to-international-applications-based-on-the-dotnet-framework)
