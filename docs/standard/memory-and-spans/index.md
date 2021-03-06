---
title: Mémoire et étendues
ms.date: 10/03/2018
ms.technology: dotnet-standard
helpviewer_keywords:
- Memory<T>
- Span<T>
- buffers"
- pipeline processing
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1a61f56eca242db65bd555553132450c3f8af7f6
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61909439"
---
# <a name="memory--and-span-related-types"></a>Types liés à la mémoire et l’étendue

À partir de .NET Core 2.1, .NET inclut plusieurs types reliés entre eux qui représentent une région contiguë et fortement typée de mémoire arbitraire. Elles incluent notamment :

- <xref:System.Span%601?displayProperty=nameWithType>, un type utilisé pour accéder à une zone contiguë de mémoire. Une instance <xref:System.Span%601> peut être sauvegardée par un tableau de type `T`, un objet <xref:System.String>, une mémoire tampon allouée avec [stackalloc](~/docs/csharp/language-reference/keywords/stackalloc.md), ou un pointeur vers une mémoire non managée. Comme elle doit être allouée sur la pile, elle comporte plusieurs restrictions. Par exemple, un champ dans une classe ne peut pas être de type <xref:System.Span%601>, et l’étendue ne peut pas être utilisée dans des opérations asynchrones.

- <xref:System.ReadOnlySpan%601?displayProperty=nameWithType>, une version immuable de la structure <xref:System.Span%601>.

- <xref:System.Memory%601?displayProperty=nameWithType>, une zone contiguë de mémoire qui est allouée sur le segment managé plutôt que sur la pile. Une instance <xref:System.Memory%601> peut être sauvegardée par un tableau de type `T` ou un <xref:System.String>. Comme elle peut être stockée sur le tas managé, <xref:System.Memory%601> ne présente aucune limite pour <xref:System.Span%601>.

- <xref:System.ReadOnlyMemory%601?displayProperty=nameWithType>, une version immuable de la structure <xref:System.Memory%601>.

- <xref:System.Buffers.MemoryPool%601?displayProperty=nameWithType>, qui alloue des blocs de mémoire très typés d’un pool de mémoire à un propriétaire. Les instances <xref:System.Buffers.IMemoryOwner%601> peuvent être louées à partir du pool en appelant <xref:System.Buffers.MemoryPool%601.Rent%2A?displayProperty=nameWithType> puis replacées dans le pool en appelant <xref:System.Buffers.MemoryPool%601.Dispose?displayProperty=nameWithType>.

- <xref:System.Buffers.IMemoryOwner%601?displayProperty=nameWithType>, qui représente le propriétaire d’un bloc de mémoire et gère la durée de vie.

- <xref:System.Buffers.MemoryManager%601>, une classe de base abstraite qui peut être utilisée pour remplacer l’implémentation de <xref:System.Memory%601> afin de sauvegarder <xref:System.Memory%601> par des types supplémentaires, par exemple des descripteurs sécurisés. <xref:System.Buffers.MemoryManager%601> s’applique à des scénarios avancés.

- <xref:System.ArraySegment%601>, un wrapper pour un certain nombre d’éléments de tableau commençant à un index particulier.

- <xref:System.MemoryExtensions?displayProperty=nameWithType>, une collection de méthodes d’extension pour la conversion de chaînes, de tableaux et de segments de tableau en blocs <xref:System.Memory%601>.

> [!NOTE]
> Pour les frameworks antérieurs, <xref:System.Span%601> et <xref:System.Memory%601> sont disponibles dans le [package System.Memory NuGet](https://www.nuget.org/packages/System.Memory/).

Pour plus d'informations, consultez l'espace de noms <xref:System.Buffers?displayProperty=nameWithType>.

## <a name="working-with-memory-and-span"></a>Utilisation de la mémoire et de l’étendue

Étant donné que les types liés à la mémoire et à l’étendue servent généralement à stocker les données dans un pipeline de traitement, il est important que les développeurs suivent un ensemble de meilleures pratiques lorsqu’ils utilisent <xref:System.Span%601>, <xref:System.Memory%601> et des types connexes. Ces meilleures pratiques sont documentées dans les [instructions d’utilisation de la mémoire\< et de l’étendue\<](memory-t-usage-guidelines.md).

## <a name="see-also"></a>Voir aussi

- <xref:System.Memory%601?displayProperty=nameWithType>
- <xref:System.ReadOnlyMemory%601?displayProperty=nameWithType>
- <xref:System.Span%601?displayProperty=nameWithType>
- <xref:System.ReadOnlySpan%601?displayProperty=nameWithType>
- <xref:System.Buffers?displayProperty=nameWithType>