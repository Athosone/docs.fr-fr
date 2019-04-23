---
title: 'Procédure : Représenter des colonnes calculées'
ms.date: 03/30/2017
ms.assetid: 4025f1fd-9dfa-46c0-b04f-34e8bc7957a2
ms.openlocfilehash: df72562b303e5b9a7c31334df06926f157b59b05
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59324736"
---
# <a name="how-to-represent-computed-columns"></a><span data-ttu-id="48a5f-102">Procédure : Représenter des colonnes calculées</span><span class="sxs-lookup"><span data-stu-id="48a5f-102">How to: Represent Computed Columns</span></span>
<span data-ttu-id="48a5f-103">Utilisez le [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.Expression%2A> propriété sur un <xref:System.Data.Linq.Mapping.ColumnAttribute> attribut pour représenter une colonne dont le contenu est le résultat du calcul.</span><span class="sxs-lookup"><span data-stu-id="48a5f-103">Use the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.Expression%2A> property on a <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute to represent a column whose contents are the result of calculation.</span></span>  
  
 <span data-ttu-id="48a5f-104">Pour obtenir des exemples de code, consultez <xref:System.Data.Linq.Mapping.ColumnAttribute.Expression%2A>.</span><span class="sxs-lookup"><span data-stu-id="48a5f-104">For code examples, see <xref:System.Data.Linq.Mapping.ColumnAttribute.Expression%2A>.</span></span>  
  
> [!NOTE]
>  [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="48a5f-105">ne prend pas en charge les colonnes calculées en tant que clés primaires.</span><span class="sxs-lookup"><span data-stu-id="48a5f-105">does not support computed columns as primary keys.</span></span>  
  
### <a name="to-represent-a-computed-column"></a><span data-ttu-id="48a5f-106">Pour représenter une colonne calculée</span><span class="sxs-lookup"><span data-stu-id="48a5f-106">To represent a computed column</span></span>  
  
1. <span data-ttu-id="48a5f-107">Ajoutez la propriété <xref:System.Data.Linq.Mapping.ColumnAttribute.Expression%2A> à l'attribut <xref:System.Data.Linq.Mapping.ColumnAttribute>.</span><span class="sxs-lookup"><span data-stu-id="48a5f-107">Add the <xref:System.Data.Linq.Mapping.ColumnAttribute.Expression%2A> property to the <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute.</span></span>  
  
2. <span data-ttu-id="48a5f-108">Assignez une représentation sous forme de chaîne de la formule à la propriété <xref:System.Data.Linq.Mapping.ColumnAttribute.Expression%2A>.</span><span class="sxs-lookup"><span data-stu-id="48a5f-108">Assign a string representation of the formula to the <xref:System.Data.Linq.Mapping.ColumnAttribute.Expression%2A> property.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="48a5f-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48a5f-109">See also</span></span>

- [<span data-ttu-id="48a5f-110">Modèle objet LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="48a5f-110">The LINQ to SQL Object Model</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md)
- [<span data-ttu-id="48a5f-111">Guide pratique pour Personnaliser des Classes d’entité à l’aide de l’éditeur de Code</span><span class="sxs-lookup"><span data-stu-id="48a5f-111">How to: Customize Entity Classes by Using the Code Editor</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-customize-entity-classes-by-using-the-code-editor.md)
