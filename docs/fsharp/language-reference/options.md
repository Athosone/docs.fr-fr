---
title: Options
description: Découvrez comment utiliser F# option types lorsqu’une valeur réelle n’existerait pas pour une valeur nommée ou une variable.
ms.date: 05/16/2016
ms.openlocfilehash: 6d32693bccc74c2cab642e4f626c9463092e8a39
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61666480"
---
# <a name="options"></a>Options

Le type d’option dans F# est utilisé lorsqu’une valeur réelle n’existerait pas pour une valeur nommée ou une variable. Une option a un type sous-jacent et peut contenir une valeur de ce type, ou il ne peut pas avoir une valeur.

## <a name="remarks"></a>Notes

Le code suivant illustre une fonction qui génère un type d’option.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1404.fs)]

Comme vous pouvez le voir, si l’entrée `a` est supérieur à 0, `Some(a)` est généré.  Sinon, `None` est généré.

La valeur `None` est utilisée lorsqu’une option n’a pas une valeur réelle. Sinon, l’expression `Some( ... )` donne la possibilité de valeur. Les valeurs `Some` et `None` sont utiles dans les critères spéciaux, comme dans la fonction suivante `exists`, qui retourne `true` si l’option a la valeur et `false` si elle n’est pas le cas.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1401.fs)]

## <a name="using-options"></a>À l’aide des Options

Options sont couramment utilisées lors d’une recherche ne retourne pas de résultat correspondant, comme indiqué dans le code suivant.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1403.fs)]

Dans le code précédent, une liste est effectuée de manière récursive. La fonction `tryFindMatch` prend une fonction de prédicat `pred` qui retourne une valeur booléenne et une liste à rechercher. Si un élément qui répond au prédicat est trouvé, la récursivité se termine et la fonction retourne la valeur en tant qu’option dans l’expression `Some(head)`. La récursivité se termine lorsque la liste vide est mis en correspondance. À ce stade, la valeur `head` n’a pas été trouvé, et `None` est retourné.

Nombreux F# des fonctions de bibliothèque qui recherchent une collection pour une valeur qui peut existe ou non retourner la `option` type. Par convention, ces fonctions commencent par le `try` de préfixe, par exemple, [ `Seq.tryFindIndex` ](https://msdn.microsoft.com/library/c357b221-edf6-4f68-bf40-82a3156d945a).

Options peuvent également être utiles lorsqu’une valeur ne peut pas exister, par exemple s’il est possible qu’une exception est levée lorsque vous tentez de construire une valeur. L'exemple de code suivant illustre ceci.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1402.fs)]

Le `openFile` fonction dans l’exemple précédent a un type `string -> File option` , car elle retourne un `File` objet si le fichier s’ouvre avec succès et `None` si une exception se produit. Selon la situation, il ne peut pas être un choix de conception approprié pour intercepter une exception plutôt que d’autoriser à se propager.

En outre, il est toujours possible de passer `null` ou une valeur qui a la valeur null pour le `Some` cas d’une option. Il s’agit généralement d’éviter et est généralement dans la routine F# de programmation, mais est possible en raison de la nature des types de référence dans .NET.

## <a name="option-properties-and-methods"></a>Méthodes et propriétés d’option

Le type d’option prend en charge les propriétés et méthodes suivantes.

|Propriété ou méthode|Type|Description|
|------------------|----|-----------|
|[Aucun](https://msdn.microsoft.com/library/83ef260a-aa33-4e6f-aee6-b9bf0a461476)|`'T option`|Une propriété statique qui vous permet de créer une valeur d’option qui a le `None` valeur.|
|[IsNone](https://msdn.microsoft.com/library/f08532ca-1716-4f60-ae59-8ef6256df234)|`bool`|Retourne `true` si l’option a la `None` valeur.|
|[IsSome](https://msdn.microsoft.com/library/c5088d51-c5d7-425f-a77f-12c379bb356f)|`bool`|Retourne `true` si l’option a une valeur qui n’est pas `None`.|
|[Certains](https://msdn.microsoft.com/library/12f048d2-e293-4596-accb-de036ecd63fc)|`'T option`|Un membre statique qui crée une option qui a une valeur qui n’est pas `None`.|
|[Valeur](https://msdn.microsoft.com/library/c79f68e8-11fd-45b1-a053-e8fc38b56df7)|`'T`|Retourne la valeur sous-jacente, ou lève une `System.NullReferenceException` si la valeur est `None`.|

## <a name="option-module"></a>Module d’option

Il existe un module, [Option](https://msdn.microsoft.com/library/e615e4d3-bbbb-49ba-addc-6061ea2e2f4c), qui contient des fonctions utiles qui effectuent des opérations sur les options. Certaines fonctions répètent les fonctionnalités des propriétés, mais sont utiles dans les contextes où une fonction est nécessaire. [Option.isSome](https://msdn.microsoft.com/library/41ad0857-5672-4326-84b5-c33dc43dcf79) et [Option.isNone](https://msdn.microsoft.com/library/73db6a53-15e7-40a6-94f9-a0049e5f4819) sont les deux fonctions de module qui testent si une option contient une valeur. [Option.Get](https://msdn.microsoft.com/library/803e9fcb-6edd-4910-808c-25f08cbc55ea) Obtient la valeur, le cas échéant. S’il n’existe aucune valeur, elle lève `System.ArgumentException`.

Le [Option.bind](https://msdn.microsoft.com/library/c3406192-24ac-49b5-bc3b-8f805187f1c0) fonction exécute une fonction sur la valeur, s’il existe une valeur. La fonction doit accepter exactement un argument, et son type de paramètre doit être le type d’option. La valeur de retour de la fonction est un autre type d’option.

Le module option inclut également des fonctions qui correspondent aux fonctions qui sont disponibles pour les listes, des tableaux, des séquences et d’autres types de collection. Ces fonctions incluent [ `Option.map` ](https://msdn.microsoft.com/library/91a20385-7e73-40c2-9adc-635e86d6a622), [ `Option.iter` ](https://msdn.microsoft.com/library/83389eef-3dff-4074-b4cc-f69581c25191), [ `Option.forall` ](https://msdn.microsoft.com/library/ba884586-5eae-49c5-9e36-05481c1c3428), [ `Option.exists` ](https://msdn.microsoft.com/library/a606d2d4-fddc-4eab-ab37-c6138fb7ad99), [ `Option.foldBack` ](https://msdn.microsoft.com/library/a882fbaf-c019-46f0-b4f5-b8c2b8b90ffb), [ `Option.fold` ](https://msdn.microsoft.com/library/af896794-3d53-406c-9411-316cd5c33ad8), et [ `Option.count` ](https://msdn.microsoft.com/library/2dac83a9-684e-4d0f-b50e-ff722a8bb876). Ces fonctions permettent d’options à utiliser comme une collection de zéro ou un élément. Pour plus d’informations et des exemples, consultez la discussion des fonctions de collection dans [répertorie](lists.md).

## <a name="converting-to-other-types"></a>Conversion à d’autres Types

Options peuvent être converties en listes ou tableaux. Lorsqu’une option est convertie dans un de ces structures de données, la structure de données qui en résulte a zéro ou un élément. Pour convertir une option dans un tableau, utilisez [ `Option.toArray` ](https://msdn.microsoft.com/library/c8044873-ba17-4b52-8231-eb1a28318c64). Pour convertir une option à une liste, utilisez [ `Option.toList` ](https://msdn.microsoft.com/library/5f1af295-9fa9-40ad-b4a1-3578d94d44e1).

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](index.md)
- [Types F#](fsharp-types.md)
