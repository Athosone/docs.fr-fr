---
title: 'Déclarations d’importation : Le mot clé open'
description: En savoir plus sur F# importer des déclarations et comment ils spécifient un module ou un espace de noms dont les éléments que vous pouvez référencer sans utiliser un nom qualifié complet.
ms.date: 04/04/2019
ms.openlocfilehash: ad64190c3243c57a185f3b864270fca80590f079
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61937499"
---
# <a name="import-declarations-the-open-keyword"></a>Déclarations d’importation : Le `open` mot clé

> [!NOTE]
> Les liens des informations de référence sur les API qui figurent dans cet article pointent vers MSDN.  Les informations de référence sur les API docs.microsoft.com ne sont pas terminées.

Un *déclaration d’importation* spécifie un module ou un espace de noms dont les éléments que vous pouvez référencer sans utiliser un nom qualifié complet.

## <a name="syntax"></a>Syntaxe

```fsharp
open module-or-namespace-name
```

## <a name="remarks"></a>Notes

Faisant référence à code en utilisant le chemin qualifié complet de l’espace de noms ou module chaque fois pouvez créer le code qui est difficile à écrire, lire et mettre à jour. Au lieu de cela, vous pouvez utiliser le `open` mot clé pour utilisé fréquemment des modules et les espaces de noms afin que lorsque vous référencez un membre de ce module ou un espace de noms, vous pouvez utiliser la forme abrégée du nom au lieu du nom qualifié complet. Ce mot clé est similaire à la `using` mot clé en c#, `using namespace` dans Visual C++, et `Imports` en Visual Basic.

Le module ou un espace de noms fourni doit être dans le même projet ou dans un projet ou assembly référencé. Si elle n’est pas le cas, vous pouvez ajouter une référence au projet, ou utiliser le `-reference` commande`-`option de ligne (ou son abréviation, `-r`). Pour plus d’informations, consultez l’article [Options du compilateur](compiler-options.md).

La déclaration d’importation rend les noms disponibles dans le code qui suit la déclaration, jusqu'à la fin de l’espace de noms, module ou fichier englobante.

Lorsque vous utilisez plusieurs déclarations d’importation, ils doivent apparaître sur des lignes distinctes.

Le code suivant illustre l’utilisation de la `open` mot clé pour simplifier le code.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet6801.fs)]

Le F# compilateur n’émet pas d’une erreur ou un avertissement lorsque des ambiguïtés se produisent lorsque le même nom se produit dans plus d’un module open ou espace de noms. Lorsque des ambiguïtés se produisent, F# privilégie le module ou un espace de noms plus récemment ouverts. Par exemple, dans le code suivant, `empty` signifie `Seq.empty`, même si `empty` se trouve à la fois dans le `List` et `Seq` modules.

```fsharp
open List
open Seq
printfn "%A" empty
```

Par conséquent, soyez prudent lorsque vous ouvrez des modules ou espaces de noms tels que `List` ou `Seq` qui contiennent des membres qui ont des noms identiques ; au lieu de cela, envisagez d’utiliser les noms qualifiés. Vous devez éviter toute situation dans laquelle le code dépend de l’ordre des déclarations d’importation.

## <a name="namespaces-that-are-open-by-default"></a>Espaces de noms qui sont ouverts par défaut

Certains espaces de noms sont utilisés si souvent dans F# code qu’ils sont ouverts implicitement sans avoir besoin d’une déclaration d’importation explicite. Le tableau suivant présente les espaces de noms qui sont ouverts par défaut.

|Espace de noms|Description|
|---------|-----------|
|`Microsoft.FSharp.Core`|Contient la base F# tels que des définitions pour les types intégrés de type `int` et `float`.|
|`Microsoft.FSharp.Core.Operators`|Contient des opérations arithmétiques de base telles que `+` et `*`.|
|`Microsoft.FSharp.Collections`|Contient des classes de collection immuable comme `List` et `Array`.|
|`Microsoft.FSharp.Control`|Contient des types pour les constructions de contrôle telles que l’évaluation paresseuse et flux de travail asynchrones.|
|`Microsoft.FSharp.Text`|Contient des fonctions pour les e/s mise en forme, telles que le `printf` (fonction).|

## <a name="autoopen-attribute"></a>AutoOpen (attribut)

Vous pouvez appliquer le `AutoOpen` d’attribut à un assembly si vous souhaitez ouvrir automatiquement un espace de noms ou un module à l’assembly est référencé. Vous pouvez également appliquer le `AutoOpen` d’attribut à un module pour ouvrir automatiquement ce module lorsque le module parent ou un espace de noms est ouvert. Pour plus d’informations, consultez [Core.AutoOpenAttribute, classe](https://msdn.microsoft.com/visualfsharpdocs/conceptual/core.autoopenattribute-class-%5bfsharp%5d).

## <a name="requirequalifiedaccess-attribute"></a>RequireQualifiedAccess (attribut)

Certains modules, des enregistrements ou les types d’union peuvent spécifier le `RequireQualifiedAccess` attribut. Lorsque vous référencez des éléments de ces modules, des enregistrements ou unions, vous devez utiliser un nom qualifié, quel que soit ou non d’une déclaration d’importation. Si vous utilisez cet attribut de façon stratégique sur les types qui définissent généralement utilisé des noms, vous aider à éviter les collisions de nom et code rendre plus résistante aux modifications dans les bibliothèques. Pour plus d’informations, consultez [Core.RequireQualifiedAccessAttribute, classe](https://msdn.microsoft.com/visualfsharpdocs/conceptual/core.requirequalifiedaccessattribute-class-%5Bfsharp%5D).

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](index.md)
- [Espaces de noms](namespaces.md)
- [Modules](modules.md)
