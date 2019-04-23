---
title: Fonctions de date et d'heure
ms.date: 03/30/2017
ms.assetid: 971762d0-663b-4b64-8c61-352a8e6d3949
ms.openlocfilehash: 8d5bbb9577e8016d6d5f2d0bef1932f6321a1e02
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59181920"
---
# <a name="date-and-time-functions"></a>Fonctions de date et d'heure
Le fournisseur de données .NET Framework pour SQL Server (SqlClient) propose des fonctions de date et d'heure qui effectuent des opérations sur une valeur d'entrée `System.DateTime` et retournent une valeur `string`, numérique ou `System.DateTime` comme résultat. Ces fonctions se trouvent dans l'espace de noms SqlServer, lequel est disponible lorsque vous utilisez SqlClient. La propriété d’espace de noms d’un fournisseur permet à Entity Framework de découvrir le préfixe attribué par ce fournisseur à des constructions spécifiques, telles que des types et des fonctions. Le tableau suivant montre les fonctions de date et d’heure SqlClient.  
  
|Fonction|Description|  
|--------------|-----------------|  
|`DATEADD(datepart, number, date)`|Retourne une nouvelle valeur `DateTime` qui est basée sur l'ajout d'un intervalle à la date spécifiée.<br /><br /> **Arguments**<br /><br /> `datepart`: `String` qui représente la partie de la date sur laquelle retourner une nouvelle valeur.<br /><br /> `number`: Valeur `Int32`, `Int64`, `Decimal` ou `Double` utilisée pour incrémenter `datepart`.<br /><br /> `date:` Une expression qui retourne un `DateTime`, ou `DateTimeOffset`, ou `Time` avec une précision = [0-7], ou une chaîne de caractères dans un format de date.<br /><br /> **Valeur de retour**<br /><br /> Une nouvelle valeur `DateTime`, `DateTimeOffset` ou `Time` avec une précision comprise entre 0-7.<br /><br /> **Exemple**<br /><br /> `SqlServer.DATEADD('day', 22, cast('6/9/2006' as DateTime))`|  
|`DATEDIFF(datepart,startdate,enddate)`|Retourne le nombre de limites de date et d'heure comprises entre deux dates spécifiées.<br /><br /> **Arguments**<br /><br /> `datepart`: `String` qui représente la partie de la date sur laquelle doit être calculée la différence.<br /><br /> `startdate`: Une date de début pour le calcul est une expression qui retourne une valeur `DateTime`, `DateTimeOffset` ou `Time` avec une précision comprise entre 0-7, ou une chaîne de caractères dans un format de date.<br /><br /> `enddate:` Date de fin pour le calcul est une expression qui retourne un `DateTime`, ou `DateTimeOffset`, ou `Time` valeur avec une précision = [0-7], ou une chaîne de caractères dans un format de date.<br /><br /> **Valeur de retour**<br /><br /> Élément `Int32`.<br /><br /> **Exemple**<br /><br /> `SqlServer.DATEDIFF('day', cast('6/9/2006' as DateTime),`<br /><br /> `cast('6/20/2006' as DateTime))`|  
|`DATENAME(datepart, date)`|Retourne une chaîne de caractères représentant la composante date spécifiée de la date spécifiée.<br /><br /> **Arguments**<br /><br /> `datepart`: `String` qui représente la partie de la date sur laquelle retourner une nouvelle valeur.<br /><br /> `date`: Expression qui retourne une valeur `DateTime,``DateTimeOffset` ou `Time` avec une précision comprise entre 0-7, ou une chaîne de caractères dans un format de date.<br /><br /> **Valeur de retour**<br /><br /> Chaîne de caractères représentant la partie de date spécifiée de la date donnée.<br /><br /> **Exemple**<br /><br /> `SqlServer.DATENAME('year', cast('6/9/2006' as DateTime))`|  
|`DATEPART(datepart, date)`|Retourne un entier qui représente l'élément de date spécifié de la date donnée.<br /><br /> **Arguments**<br /><br /> `datepart`: `String` qui représente la partie de la date sur laquelle retourner une nouvelle valeur.<br /><br /> `date`: Expression qui retourne une valeur `DateTime,``DateTimeOffset,` ou `Time` avec une précision comprise entre 0-7, ou une chaîne de caractères dans un format de date.<br /><br /> **Valeur de retour**<br /><br /> Partie de date spécifiée de la date donnée, sous la forme d'une valeur `Int32`.<br /><br /> **Exemple**<br /><br /> `SqlServer.DATEPART('year', cast('6/9/2006' as DateTime))`|  
|`DAY(date)`|Retourne le jour de la date spécifiée sous forme d’entier.<br /><br /> **Arguments**<br /><br /> `date`: Une expression de type `DateTime` ou `DateTimeOffset` avec une précision comprise entre 0-7.<br /><br /> **Valeur de retour**<br /><br /> Jour de la date spécifiée, sous la forme d'une valeur `Int32`.<br /><br /> **Exemple**<br /><br /> `SqlServer.DAY(cast('6/9/2006' as DateTime))`|  
|`GETDATE()`|Fournit la date et l'heure actuelles sous la forme employée de manière interne par SQL Server pour stocker les valeurs datetime.<br /><br /> **Valeur de retour**<br /><br /> Date et heure système actuelles sous forme de valeur `DateTime` avec une précision de 3.<br /><br /> **Exemple**<br /><br /> `SqlServer.GETDATE()`|  
|`GETUTCDATE()`|Produit la valeur datetime au format UTC (Universal Time Coordinate ou GMT (heure de Greenwich)).<br /><br /> **Valeur de retour**<br /><br /> Valeur `DateTime` avec une précision de 3 au format UTC.<br /><br /> **Exemple**<br /><br /> `SqlServer.GETUTCDATE()`|  
|`MONTH(date)`|Retourne la partie mois de la date spécifiée sous la forme d'un entier.<br /><br /> **Arguments**<br /><br /> `date`: Une expression de type `DateTime` ou `DateTimeOffset` avec une précision comprise entre 0-7.<br /><br /> **Valeur de retour**<br /><br /> Partie mois de la date spécifiée sous la forme d'une valeur `Int32`.<br /><br /> **Exemple**<br /><br /> `SqlServer.MONTH(cast('6/9/2006' as DateTime))`|  
|`YEAR(date)`|Retourne l'année de la date spécifiée sous la forme d'un entier.<br /><br /> **Arguments**<br /><br /> `date`: Une expression de type `DateTime` ou `DateTimeOffset` avec une précision comprise entre 0-7.<br /><br /> **Valeur de retour**<br /><br /> Année de la date spécifiée, sous la forme d'une valeur `Int32`.<br /><br /> **Exemple**<br /><br /> `SqlServer.YEAR(cast('6/9/2006' as DateTime))`|  
|`SYSDATETIME()`|Retourne une valeur `DateTime` avec une précision de 7.<br /><br /> **Valeur de retour**<br /><br /> Valeur `DateTime` avec une précision de 7.<br /><br /> **Exemple**<br /><br /> `SqlServer.SYSDATETIME()`|  
|`SYSUTCDATE()`|Produit la valeur datetime au format UTC (Universal Time Coordinate ou GMT (heure de Greenwich)).<br /><br /> **Valeur de retour**<br /><br /> Valeur `DateTime` avec une précision de 7 au format UTC.<br /><br /> **Exemple**<br /><br /> `SqlServer.SYSUTCDATE()`|  
|`SYSDATETIMEOFFSET()`|Retourne une valeur `DateTimeOffset` avec une précision de 7.<br /><br /> **Valeur de retour**<br /><br /> Valeur `DateTimeOffset` avec une précision de 7 au format UTC.<br /><br /> **Exemple**<br /><br /> `SqlServer.SYSDATETIMEOFFSET()`|  
  
 Pour plus d'informations sur les fonctions de date et d'heure prises en charge par SqlClient, voir la documentation correspondant à la version de SQL Server que vous avez spécifiée dans le manifeste du fournisseur SqlClient :  
  
|SQL Server 2000|SQL Server 2005|SQL Server 2008|  
|---------------------|---------------------|---------------------|  
|[Fonctions de date et heure (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=115908)|[Fonctions de date et heure (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=115909)|[Fonctions de date et heure (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=98360)|  
  
## <a name="see-also"></a>Voir aussi

- [Fonctions SqlClient pour Entity Framework](../../../../../docs/framework/data/adonet/ef/sqlclient-for-ef-functions.md)
