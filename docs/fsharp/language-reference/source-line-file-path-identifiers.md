---
title: Identificateurs de ligne, de fichier et de chemin d’accès source
description: Découvrez comment utiliser intégrée F# valeurs d’identificateur qui vous permettent d’accéder à la source de ligne numéro, directory et nom de fichier dans votre code.
ms.date: 05/16/2016
ms.openlocfilehash: 4b145fe1fe20e3d7f868558e33bab26204fb0125
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61663620"
---
# <a name="source-line-file-and-path-identifiers"></a>Identificateurs de ligne, de fichier et de chemin d’accès source

Les identificateurs `__LINE__`, `__SOURCE_DIRECTORY__` et `__SOURCE_FILE__` sont des valeurs intégrées qui vous permettent d’accéder à la ligne numéro, répertoire et fichier nom source dans votre code.

## <a name="syntax"></a>Syntaxe

```fsharp
__LINE__
__SOURCE_DIRECTORY__
__SOURCE_FILE__
```

## <a name="remarks"></a>Notes

Chacune de ces valeurs a le type `string`.

Le tableau suivant récapitule les identificateurs de ligne, de fichier et chemin d’accès source qui sont disponibles dans F#. Ces identificateurs ne sont pas des macros de préprocesseur ; ils sont des valeurs intégrées qui sont reconnus par le compilateur.

|Identificateur prédéfini|Description|
|---------------------|-----------|
|`__LINE__`|Prend la valeur de numéro de ligne en cours, vous envisagez `#line` directives.|
|`__SOURCE_DIRECTORY__`|Prend la valeur actuelle chemin d’accès complet du répertoire source, envisagez `#line` directives.|
|`__SOURCE_FILE__`|A pour valeur le nom de fichier source actuel et son chemin d’accès, vous envisagez `#line` directives.|

Pour plus d’informations sur la `#line` directive, consultez [Directives de compilateur](compiler-directives.md).

## <a name="example"></a>Exemple

L’exemple de code suivant illustre l’utilisation de ces valeurs.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet7401.fs)]

Sortie :

```
Line: 4
Source Directory: C:\Users\username\Documents\Visual Studio 2017\Projects\SourceInfo\SourceInfo
Source File: C:\Users\username\Documents\Visual Studio 2017\Projects\SourceInfo\SourceInfo\Program.fs
```

## <a name="see-also"></a>Voir aussi

- [Directives de compilateur](compiler-directives.md)
- [Informations de référence du langage F#](index.md)
