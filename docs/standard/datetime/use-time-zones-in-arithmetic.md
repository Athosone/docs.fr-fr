---
title: 'Procédure : utiliser des fuseaux horaires en arithmétique de date et heure'
ms.date: 04/10/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- time zones [.NET Framework], arithmetic operations
- arithmetic operations [.NET Framework], dates and times
- dates [.NET Framework], adding and subtracting
ms.assetid: 83dd898d-1338-415d-8cd6-445377ab7871
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 053ca2d10deadf58d5bb8b4628fb5dee815d82c8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62026495"
---
# <a name="how-to-use-time-zones-in-date-and-time-arithmetic"></a>Procédure : utiliser des fuseaux horaires en arithmétique de date et heure

En règle générale, lorsque vous effectuer la date et l’heure à l’aide d’arithmétique <xref:System.DateTime> ou <xref:System.DateTimeOffset> valeurs, le résultat ne reflète pas les règles d’ajustement de fuseau horaire. Cela est vrai même lorsque le fuseau horaire de la valeur de date et d’heure est clairement identifiable (par exemple, lors de la <xref:System.DateTime.Kind%2A> propriété est définie sur <xref:System.DateTimeKind.Local>). Cette rubrique montre comment effectuer des opérations arithmétiques sur les valeurs de date et d’heure qui appartiennent à un fuseau horaire particulier. Les résultats de ces opérations arithmétiques reflètent les règles d’ajustement du fuseau horaire.

### <a name="to-apply-adjustment-rules-to-date-and-time-arithmetic"></a>Pour appliquer des règles d’ajustement dans les opérations arithmétiques de date et d’heure

1. Implémentez une méthode de couplage étroit d’une valeur de date et d’heure avec le fuseau horaire auquel elle appartient. Par exemple, déclarez une structure qui inclut à la fois la valeur de date et d’heure et son fuseau horaire. L’exemple suivant utilise cette approche pour lier un <xref:System.DateTime> valeur avec son fuseau horaire.

   [!code-csharp[System.DateTimeOffset.Conceptual#6](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.DateTimeOffset.Conceptual/cs/Conceptual6.cs#6)]
   [!code-vb[System.DateTimeOffset.Conceptual#6](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.DateTimeOffset.Conceptual/vb/Conceptual6.vb#6)]

2. Convertir une heure en temps universel coordonné (UTC) en appelant le <xref:System.TimeZoneInfo.ConvertTimeToUtc%2A> méthode ou le <xref:System.TimeZoneInfo.ConvertTime%2A> (méthode).

3. Effectuez l’opération arithmétique sur l’heure UTC.

4. Convertissez l’heure UTC au fuseau horaire associé de l’heure d’origine en appelant le <xref:System.TimeZoneInfo.ConvertTime%28System.DateTime%2CSystem.TimeZoneInfo%29?displayProperty=nameWithType> (méthode).

## <a name="example"></a>Exemple

L’exemple suivant ajoute deux heures et trente minutes à 9 mars 2008, à 1:30 A.M., heure du Centre des États-Unis. Le passage du fuseau horaire à l’heure d’été se produit trente minutes plus tard, à 2:00, le 9 mars 2008. Étant donné que cet exemple suit les quatre étapes répertoriées à la section précédente, il signale correctement l’heure obtenue, soit 5:00, le 9 mars 2008.

[!code-csharp[System.DateTimeOffset.Conceptual#8](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.DateTimeOffset.Conceptual/cs/Conceptual8.cs#8)]
[!code-vb[System.DateTimeOffset.Conceptual#8](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.DateTimeOffset.Conceptual/vb/Conceptual8.vb#8)]

Les deux <xref:System.DateTime> et <xref:System.DateTimeOffset> valeurs sont dissociées de tout fuseau horaire auquel elles peuvent appartenir. Pour effectuer des opérations arithmétiques de date et d’heure d’une manière qui applique automatiquement les règles d’ajustement d’un fuseau horaire, le fuseau horaire auquel toute valeur de date et d’heure appartient doit être identifiable immédiatement. Cela signifie qu’une date et une heure et leur fuseau horaire associé doivent être étroitement couplés. Il existe plusieurs manières de procéder, dont les suivantes :

* Supposez que toutes les heures utilisées dans une application appartiennent à un fuseau horaire particulier. Bien qu’appropriée dans certains cas, cette approche présente une souplesse limitée et une portabilité éventuellement limitée.

* Définissez un type qui couple étroitement une valeur de date et d’heure avec son fuseau horaire associé en incluant les deux comme champs. Cette approche est utilisée dans l’exemple de code qui définit une structure pour stocker la date et l’heure, et le fuseau horaire, dans deux champs membres.

L’exemple montre comment effectuer des opérations arithmétiques sur <xref:System.DateTime> valeurs afin que les règles d’ajustement de fuseau horaire sont appliquées au résultat. Toutefois, <xref:System.DateTimeOffset> valeurs peuvent être utilisées tout aussi facilement. L’exemple suivant illustre la façon dont le code dans l’exemple d’origine peut être adapté pour utiliser <xref:System.DateTimeOffset> au lieu de <xref:System.DateTime> valeurs.

[!code-csharp[System.DateTimeOffset.Conceptual#7](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.DateTimeOffset.Conceptual/cs/Conceptual6.cs#7)]
[!code-vb[System.DateTimeOffset.Conceptual#7](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.DateTimeOffset.Conceptual/vb/Conceptual6.vb#7)]

Notez que si cet ajout est effectué simplement sur le <xref:System.DateTimeOffset> valeur sans tout d’abord sa conversion en heure UTC, le résultat indique le point correct dans le temps, mais son décalage ne reflète pas celui du fuseau horaire désigné pour cette heure.

## <a name="compiling-the-code"></a>Compilation du code

Cet exemple nécessite :

* Qu’une référence à System.Core.dll soit ajoutée au projet.

* Que l'espace de noms <xref:System> soit importé avec l'instruction `using` (obligatoire en C#).

## <a name="see-also"></a>Voir aussi

- [Dates, heures et fuseaux horaires](../../../docs/standard/datetime/index.md)
- [Exécution d’opérations arithmétiques avec des dates et heures](../../../docs/standard/datetime/performing-arithmetic-operations.md)
