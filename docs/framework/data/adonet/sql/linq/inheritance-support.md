---
title: Prise en charge de l'héritage
ms.date: 03/30/2017
ms.assetid: 19bb2794-b4e7-402e-8307-1d1517381a08
ms.openlocfilehash: 668f4f1dd284550e644ce6b8a4491ca47105575e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59230913"
---
# <a name="inheritance-support"></a><span data-ttu-id="9e507-102">Prise en charge de l'héritage</span><span class="sxs-lookup"><span data-stu-id="9e507-102">Inheritance Support</span></span>
[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="9e507-103">prend en charge *mappage de table unique*.</span><span class="sxs-lookup"><span data-stu-id="9e507-103">supports *single-table mapping*.</span></span> <span data-ttu-id="9e507-104">En d'autres termes, une hiérarchie d'héritage complète est stockée dans une seule table de base de données.</span><span class="sxs-lookup"><span data-stu-id="9e507-104">In other words, a complete inheritance hierarchy is stored in a single database table.</span></span> <span data-ttu-id="9e507-105">La table contient l'union au format à plat de toutes les colonnes de données possibles pour l'ensemble de la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="9e507-105">The table contains the flattened union of all possible data columns for the whole hierarchy.</span></span> <span data-ttu-id="9e507-106">Une union est le résultat de la combinaison de deux tables en une table contenant les lignes de l'une ou l'autre des tables d'origine. Chaque ligne comporte des valeurs null dans les colonnes qui ne s'appliquent pas au type de l'instance représenté par la ligne.</span><span class="sxs-lookup"><span data-stu-id="9e507-106">(A union is the result of combining two tables into one table that has the rows that were present in either of the original tables.) Each row has nulls in the columns that do not apply to the type of the instance represented by the row.</span></span>  
  
 <span data-ttu-id="9e507-107">La stratégie de mappage de table unique est la représentation la plus simple de l'héritage. Elle fournit des caractéristiques de performances satisfaisantes pour de nombreuses catégories de requêtes.</span><span class="sxs-lookup"><span data-stu-id="9e507-107">The single-table mapping strategy is the simplest representation of inheritance and provides good performance characteristics for many different categories of queries.</span></span>  
  
 <span data-ttu-id="9e507-108">Pour implémenter ce mappage dans [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], vous devez spécifier les attributs et les propriétés d'attribut sur la classe racine de la hiérarchie d'héritage.</span><span class="sxs-lookup"><span data-stu-id="9e507-108">To implement this mapping in [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], you must specify the attributes and attribute properties on the root class of the inheritance hierarchy.</span></span> <span data-ttu-id="9e507-109">Pour plus d'informations, voir [Procédure : Mapper des hiérarchies d’héritage](../../../../../../docs/framework/data/adonet/sql/linq/how-to-map-inheritance-hierarchies.md).</span><span class="sxs-lookup"><span data-stu-id="9e507-109">For more information, see [How to: Map Inheritance Hierarchies](../../../../../../docs/framework/data/adonet/sql/linq/how-to-map-inheritance-hierarchies.md).</span></span>  
  
 <span data-ttu-id="9e507-110">Les développeurs à l’aide de Visual Studio peuvent également utiliser le [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] pour mapper des hiérarchies d’héritage.</span><span class="sxs-lookup"><span data-stu-id="9e507-110">Developers using Visual Studio can also use the [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] to map inheritance hierarchies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9e507-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e507-111">See also</span></span>

- [<span data-ttu-id="9e507-112">Informations générales</span><span class="sxs-lookup"><span data-stu-id="9e507-112">Background Information</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/background-information.md)
