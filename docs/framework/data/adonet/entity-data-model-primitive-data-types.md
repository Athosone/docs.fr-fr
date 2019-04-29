---
title: 'Entity Data Model : types de données primitifs'
ms.date: 03/30/2017
ms.assetid: 7635168e-0566-4fdd-8391-7941b0d9f787
ms.openlocfilehash: 044a0ed981bb9cda3550fb3a3a9f1cb9bff96f25
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61667130"
---
# <a name="entity-data-model-primitive-data-types"></a>Entity Data Model : types de données primitifs
Le modèle EDM (Entity Data Model) prend en charge un ensemble de types de données primitif abstrait (par exemple, chaîne, booléen, Int32 et ainsi de suite) qui servent à définir [propriétés](../../../../docs/framework/data/adonet/property.md) dans un modèle conceptuel. Ces types de données primitifs sont des proxys pour les types de données primitifs réels qui sont pris en charge dans l'environnement de stockage ou d'hébergement, comme une base de données SQL Server ou le Common Language Runtime (CLR). Le modèle EDM ne définit pas la sémantique des opérations ou des conversions sur les types de données primitifs ; cette sémantique est définie par l'environnement de stockage ou d'hébergement. En général, les types de données primitifs dans le modèle EDM sont mappés aux types de données primitifs correspondants dans l'environnement de stockage ou d'hébergement. Pour plus d’informations sur la façon dont Entity Framework mappe les types primitifs dans le modèle EDM aux types de données SQL Server, consultez [SqlClient pour Entity FrameworkTypes](../../../../docs/framework/data/adonet/ef/sqlclient-for-ef-types.md).  
  
> [!NOTE]
>  Le modèle EDM ne prend pas en charge les collections de types de données primitifs.  
  
 Pour plus d’informations sur les types de données structurées dans le modèle EDM, consultez [type d’entité](../../../../docs/framework/data/adonet/entity-type.md) et [type complexe](../../../../docs/framework/data/adonet/complex-type.md).  
  
## <a name="primitive-data-types-supported-in-the-entity-data-model"></a>Types de données primitifs pris en charge dans le modèle EDM  
 Le tableau suivant répertorie les types de données primitifs pris en charge par le modèle EDM. Le tableau répertorie également les [facettes](../../../../docs/framework/data/adonet/facet.md) qui peut être appliqué à chaque type de données primitif.  
  
|Type de données primitif|Description|Facettes applicables|  
|-------------------------|-----------------|-----------------------|  
|Binaire|Contient des données binaires.|MaxLength, FixedLength, Nullable, Default|  
|Booléen|Contient la valeur `true` ou `false`.|Nullable, Default|  
|Byte|Contient une valeur d'entier 8 bits non signé.|Precision, Nullable, Default|  
|DateTime|Représente une date et une heure.|Precision, Nullable, Default|  
|DateTimeOffset|Contient une date et une heure en tant que décalage en minutes par rapport à l'heure GMT.|Precision, Nullable, Default|  
|Decimal|Contient une valeur numérique avec une précision et une échelle fixes.|Precision, Nullable, Default|  
|Double|Contient un nombre à virgule flottante avec une précision de 15 chiffres.|Precision, Nullable, Default|  
|Float|Contient un nombre à virgule flottante avec une précision de sept chiffres.|Precision, Nullable, Default|  
|GUID|Contient un identificateur unique de 16 octets.|Precision, Nullable, Default|  
|Int16|Contient une valeur d'entier 16 bits signé.|Precision, Nullable, Default|  
|Int32|Contient une valeur d'entier 32 bits signé.|Precision, Nullable, Default|  
|Int64|Contient une valeur d'entier 64 bits signé.|Precision, Nullable, Default|  
|SByte|Contient une valeur d'entier 8 bits signé.|Precision, Nullable, Default|  
|Chaîne|Contient des données caractères.|Unicode, FixedLength, MaxLength, Collation, Precision, Nullable, Default|  
|réflexion|Contient une heure.|Precision, Nullable, Default|  
  
## <a name="see-also"></a>Voir aussi

- [Concepts clés d’Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)
- [Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model.md)
