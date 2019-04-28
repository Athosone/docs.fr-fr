---
title: Déduction du texte d'un élément
ms.date: 03/30/2017
ms.assetid: 789799e5-716f-459f-a168-76c5cf22178b
ms.openlocfilehash: 6ffe8f2fbf01fbe8dfa9d78f3dfb9e39b6e80b16
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61879630"
---
# <a name="inferring-element-text"></a><span data-ttu-id="d21d6-102">Déduction du texte d'un élément</span><span class="sxs-lookup"><span data-stu-id="d21d6-102">Inferring Element Text</span></span>
<span data-ttu-id="d21d6-103">Si un élément contient du texte et ne contient aucun élément enfant à déduire en tant que tables telles que (éléments avec attributs) ou des éléments répétés, une nouvelle colonne portant le nom **TableName_Text** sera ajouté à la table qui est déduite pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="d21d6-103">If an element contains text and has no child elements to be inferred as tables (such as elements with attributes or repeated elements), a new column with the name **TableName_Text** will be added to the table that is inferred for the element.</span></span> <span data-ttu-id="d21d6-104">Le texte contenu dans l'élément sera ajouté à une ligne de la table et stocké dans la nouvelle colonne.</span><span class="sxs-lookup"><span data-stu-id="d21d6-104">The text contained in the element will be added to a row in the table and stored in the new column.</span></span> <span data-ttu-id="d21d6-105">Le **ColumnMapping** propriété de la nouvelle colonne est définie **MappingType.SimpleContent**.</span><span class="sxs-lookup"><span data-stu-id="d21d6-105">The **ColumnMapping** property of the new column will be set to **MappingType.SimpleContent**.</span></span>  
  
 <span data-ttu-id="d21d6-106">Examinons, par exemple, le code XML suivant.</span><span class="sxs-lookup"><span data-stu-id="d21d6-106">For example, consider the following XML.</span></span>  
  
```xml  
<DocumentElement>  
  <Element1 attr1="value1">Text1</Element1>  
</DocumentElement>  
```  
  
 <span data-ttu-id="d21d6-107">Le processus d’inférence produira une table nommée **Element1** avec deux colonnes : **attr1** et **Element1_Text**.</span><span class="sxs-lookup"><span data-stu-id="d21d6-107">The inference process will produce a table named **Element1** with two columns: **attr1** and **Element1_Text**.</span></span> <span data-ttu-id="d21d6-108">Le **ColumnMapping** propriété de la **attr1** jeu de colonnes **MappingType.Attribute**.</span><span class="sxs-lookup"><span data-stu-id="d21d6-108">The **ColumnMapping** property of the **attr1** column will be set to **MappingType.Attribute**.</span></span> <span data-ttu-id="d21d6-109">Le **ColumnMapping** propriété de la **Element1_Text** jeu de colonnes **MappingType.SimpleContent**.</span><span class="sxs-lookup"><span data-stu-id="d21d6-109">The **ColumnMapping** property of the **Element1_Text** column will be set to **MappingType.SimpleContent**.</span></span>  
  
 <span data-ttu-id="d21d6-110">**Jeu de données :** DocumentElement</span><span class="sxs-lookup"><span data-stu-id="d21d6-110">**DataSet:** DocumentElement</span></span>  
  
 <span data-ttu-id="d21d6-111">**Table :** Element1</span><span class="sxs-lookup"><span data-stu-id="d21d6-111">**Table:** Element1</span></span>  
  
|<span data-ttu-id="d21d6-112">attr1</span><span class="sxs-lookup"><span data-stu-id="d21d6-112">attr1</span></span>|<span data-ttu-id="d21d6-113">Element1_Text</span><span class="sxs-lookup"><span data-stu-id="d21d6-113">Element1_Text</span></span>|  
|-----------|--------------------|  
|<span data-ttu-id="d21d6-114">valeur1</span><span class="sxs-lookup"><span data-stu-id="d21d6-114">value1</span></span>|<span data-ttu-id="d21d6-115">Text1</span><span class="sxs-lookup"><span data-stu-id="d21d6-115">Text1</span></span>|  
  
 <span data-ttu-id="d21d6-116">Si un élément contient du texte, mais possède également des éléments enfants contenant du texte, une colonne ne sera pas ajoutée à la table pour stocker le texte contenu dans l'élément.</span><span class="sxs-lookup"><span data-stu-id="d21d6-116">If an element contains text, but also has child elements that contain text, a column will not be added to the table to store the text contained in the element.</span></span> <span data-ttu-id="d21d6-117">Ce texte sera ignoré, alors que le texte des éléments enfants sera inclus dans une ligne de la table.</span><span class="sxs-lookup"><span data-stu-id="d21d6-117">The text contained in the element will be ignored, while the text in the child elements is included in a row in the table.</span></span> <span data-ttu-id="d21d6-118">Examinons, par exemple, le code XML suivant.</span><span class="sxs-lookup"><span data-stu-id="d21d6-118">For example, consider the following XML.</span></span>  
  
```xml  
<Element1>  
  Text1  
  <ChildElement1>Text2</ChildElement1>  
  Text3  
</Element1>  
```  
  
 <span data-ttu-id="d21d6-119">Le processus d’inférence produira une table nommée **Element1** avec une colonne nommée **ChildElement1**.</span><span class="sxs-lookup"><span data-stu-id="d21d6-119">The inference process will produce a table named **Element1** with one column named **ChildElement1**.</span></span> <span data-ttu-id="d21d6-120">Le texte pour le **ChildElement1** élément figureront dans une ligne dans la table.</span><span class="sxs-lookup"><span data-stu-id="d21d6-120">The text for the **ChildElement1** element will be included in a row in the table.</span></span> <span data-ttu-id="d21d6-121">L'autre texte sera ignoré.</span><span class="sxs-lookup"><span data-stu-id="d21d6-121">The other text will be ignored.</span></span> <span data-ttu-id="d21d6-122">Le **ColumnMapping** propriété de la **ChildElement1** jeu de colonnes **MappingType.Element**.</span><span class="sxs-lookup"><span data-stu-id="d21d6-122">The **ColumnMapping** property of the **ChildElement1** column will be set to **MappingType.Element**.</span></span>  
  
 <span data-ttu-id="d21d6-123">**Jeu de données :** DocumentElement</span><span class="sxs-lookup"><span data-stu-id="d21d6-123">**DataSet:** DocumentElement</span></span>  
  
 <span data-ttu-id="d21d6-124">**Table :** Element1</span><span class="sxs-lookup"><span data-stu-id="d21d6-124">**Table:** Element1</span></span>  
  
|<span data-ttu-id="d21d6-125">ChildElement1</span><span class="sxs-lookup"><span data-stu-id="d21d6-125">ChildElement1</span></span>|  
|-------------------|  
|<span data-ttu-id="d21d6-126">Text2</span><span class="sxs-lookup"><span data-stu-id="d21d6-126">Text2</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d21d6-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d21d6-127">See also</span></span>

- [<span data-ttu-id="d21d6-128">Inférence de la structure relationnelle d’un DataSet à partir de XML</span><span class="sxs-lookup"><span data-stu-id="d21d6-128">Inferring DataSet Relational Structure from XML</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/inferring-dataset-relational-structure-from-xml.md)
- [<span data-ttu-id="d21d6-129">Chargement d’un DataSet à partir de XML</span><span class="sxs-lookup"><span data-stu-id="d21d6-129">Loading a DataSet from XML</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-a-dataset-from-xml.md)
- [<span data-ttu-id="d21d6-130">Chargement des informations de schéma de DataSet à partir de XML</span><span class="sxs-lookup"><span data-stu-id="d21d6-130">Loading DataSet Schema Information from XML</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-dataset-schema-information-from-xml.md)
- [<span data-ttu-id="d21d6-131">Utilisation de XML dans un DataSet</span><span class="sxs-lookup"><span data-stu-id="d21d6-131">Using XML in a DataSet</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/using-xml-in-a-dataset.md)
- [<span data-ttu-id="d21d6-132">DataSets, DataTables et DataViews</span><span class="sxs-lookup"><span data-stu-id="d21d6-132">DataSets, DataTables, and DataViews</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)
- [<span data-ttu-id="d21d6-133">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="d21d6-133">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
