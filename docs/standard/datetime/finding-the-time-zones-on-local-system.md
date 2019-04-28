---
title: Recherche des fuseaux horaires définis sur un système local
ms.date: 04/10/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- time zones [.NET Framework], local
- time zones [.NET Framework], finding local system time zones
- time zone identifiers [.NET Framework]
- local time zone access
- time zones [.NET Framework], retrieving
- UTC times, finding local system time zones
- time zones [.NET Framework], UTC
ms.assetid: 3f63b1bc-9a4b-4bde-84ea-ab028a80d3e1
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a65798c46b01bb7a702559d685590ecf7a6f2793
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61819754"
---
# <a name="finding-the-time-zones-defined-on-a-local-system"></a>Recherche des fuseaux horaires définis sur un système local

La classe <xref:System.TimeZoneInfo> n'expose pas de constructeur public. En conséquence, le mot clé `new` ne peut pas être utilisé pour créer un objet <xref:System.TimeZoneInfo>. Pour instancier des objets <xref:System.TimeZoneInfo>, vous devez donc soit récupérer dans le Registre des informations sur les fuseaux horaires prédéfinis, soit créer un fuseau horaire personnalisé. Cette rubrique explique comment instancier un fuseau horaire à partir de données stockées dans le Registre. En outre, les propriétés `static` (`shared` en Visual Basic) de la classe <xref:System.TimeZoneInfo> permettent d'accéder au temps universel coordonné (UTC) et au fuseau horaire local.

> [!NOTE]
> Si les fuseaux horaires ne sont pas définis dans le Registre, vous pouvez créer des fuseaux horaires personnalisés en appelant les surcharges de la méthode <xref:System.TimeZoneInfo.CreateCustomTimeZone%2A>. Création d’un fuseau horaire personnalisé est décrite dans la [Comment : Créer des fuseaux horaires sans règles d’ajustement](../../../docs/standard/datetime/create-time-zones-without-adjustment-rules.md) et [Comment : Créer des fuseaux horaires avec des règles d’ajustement](../../../docs/standard/datetime/create-time-zones-with-adjustment-rules.md) rubriques. Vous pouvez également instancier un objet <xref:System.TimeZoneInfo> en le restaurant à partir d'une chaîne sérialisée à l'aide de la méthode <xref:System.TimeZoneInfo.FromSerializedString%2A>. Sérialiser et désérialiser un <xref:System.TimeZoneInfo> objet est abordé dans le [Comment : Enregistrer des fuseaux horaires dans une ressource incorporée](../../../docs/standard/datetime/save-time-zones-to-an-embedded-resource.md) et [Comment : Restaurer des fuseaux horaires dans une ressource incorporée](../../../docs/standard/datetime/restore-time-zones-from-an-embedded-resource.md) rubriques.

## <a name="accessing-individual-time-zones"></a>L’accès aux fuseaux horaires individuels

La classe <xref:System.TimeZoneInfo> fournit deux objets de fuseaux horaires prédéfinis qui représentent l'heure UTC et le fuseau horaire local. Ils sont disponibles dans les propriétés <xref:System.TimeZoneInfo.Utc%2A> et <xref:System.TimeZoneInfo.Local%2A>, respectivement. Pour obtenir des instructions sur l’accès à l’heure UTC ou les fuseaux horaires, consultez [Comment : Accéder aux objets de fuseau UTC et l’heure locale prédéfinis](../../../docs/standard/datetime/access-utc-and-local.md).

Vous pouvez également instancier un objet <xref:System.TimeZoneInfo> qui représente tout fuseau horaire défini dans le Registre. Pour obtenir des instructions sur l’instanciation d’un objet de fuseau horaire spécifique, consultez [Comment : Instancier un objet TimeZoneInfo](../../../docs/standard/datetime/instantiate-time-zone-info.md).

## <a name="time-zone-identifiers"></a>Identificateurs de fuseau horaire

L'identificateur de fuseau horaire est un champ clé qui identifie le fuseau horaire de manière unique. Alors que la plupart des clés sont relativement courtes, l'identificateur de fuseau horaire est long. Dans la plupart des cas, sa valeur correspond à la propriété <xref:System.TimeZoneInfo.StandardName%2A?displayProperty=nameWithType>, utilisée pour fournir le nom de l'heure standard du fuseau horaire. Toutefois, il existe des exceptions. Pour vous assurer que l'identificateur fourni est valide, la meilleure façon consiste à énumérer les fuseaux horaires disponibles sur votre système et à noter les identificateurs associés.

## <a name="see-also"></a>Voir aussi

- [Dates, heures et fuseaux horaires](../../../docs/standard/datetime/index.md)
- [Guide pratique pour Accéder aux objets de fuseau UTC et l’heure locale prédéfinis](../../../docs/standard/datetime/access-utc-and-local.md)
- [Guide pratique pour Instancier un objet TimeZoneInfo](../../../docs/standard/datetime/instantiate-time-zone-info.md)
- [Conversion d’heures entre fuseaux horaires](../../../docs/standard/datetime/converting-between-time-zones.md)
