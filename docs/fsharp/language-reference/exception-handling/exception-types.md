---
title: Types d'exceptions
description: Découvrez comment définir et utiliser F# types d’exception.
ms.date: 05/16/2016
ms.openlocfilehash: ed721dd0dc46a486fafeac2fa4c096800995ccb7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61772721"
---
# <a name="exception-types"></a>Types d'exceptions

Il existe deux catégories d’exceptions dans F#: types d’exceptions .NET et F# types d’exception. Cette rubrique décrit comment définir et utiliser F# types d’exception.

## <a name="syntax"></a>Syntaxe

```fsharp
exception exception-type of argument-type
```

## <a name="remarks"></a>Notes

Dans la syntaxe précédente, *type d’exception* est le nom d’un nouveau F# type d’exception, et *type d’argument* représente le type d’un argument qui peut être fourni lorsque vous déclenchez une exception de ce type. Vous pouvez spécifier plusieurs arguments à l’aide d’un type de tuple pour *type d’argument*.

Une définition classique pour un F# exception ressemble à ceci.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet5501.fs)]

Vous pouvez générer une exception de ce type à l’aide de la `raise` de fonction, comme suit.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet5502.fs)]

Vous pouvez utiliser un F# type d’exception directement dans les filtres dans un `try...with` expression, comme illustré dans l’exemple suivant.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet5503.fs)]

Le type d’exception que vous définissez avec le `exception` mot clé dans F# est un nouveau type qui hérite de `System.Exception`.

## <a name="see-also"></a>Voir aussi

- [Gestion des exceptions](index.md)
- [Exceptions : fonction `raise`](the-raise-function.md)
- [Hiérarchie des exceptions](https://msdn.microsoft.com/library/z4c5tckx.aspx)