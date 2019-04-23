---
title: Déduction des relations
ms.date: 03/30/2017
ms.assetid: 8fa86a9d-6545-4a9d-b1f5-58d9742179c7
ms.openlocfilehash: f8a9aba493dfe82466608ea60932ddfec5ef64f1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59127879"
---
# <a name="inferring-relationships"></a><span data-ttu-id="a4e95-102">Déduction des relations</span><span class="sxs-lookup"><span data-stu-id="a4e95-102">Inferring Relationships</span></span>
<span data-ttu-id="a4e95-103">Si un élément déduit en tant que table comporte un élément enfant également déduit en tant que table, un objet <xref:System.Data.DataRelation> sera créé entre les deux tables.</span><span class="sxs-lookup"><span data-stu-id="a4e95-103">If an element that is inferred as a table has a child element that is also inferred as a table, a <xref:System.Data.DataRelation> will be created between the two tables.</span></span> <span data-ttu-id="a4e95-104">Une nouvelle colonne avec un nom de **ParentTableName_Id** sera ajouté à la table créée par l’élément parent et à la table créée pour l’élément enfant.</span><span class="sxs-lookup"><span data-stu-id="a4e95-104">A new column with a name of **ParentTableName_Id** will be added to both the table created for the parent element, and the table created for the child element.</span></span> <span data-ttu-id="a4e95-105">Le **ColumnMapping** propriété de cette colonne d’identité est définie **MappingType.Hidden**.</span><span class="sxs-lookup"><span data-stu-id="a4e95-105">The **ColumnMapping** property of this identity column will be set to **MappingType.Hidden**.</span></span> <span data-ttu-id="a4e95-106">La colonne sera une clé primaire auto-incrémentée pour la table parente et sera utilisée pour le **DataRelation** entre les deux tables.</span><span class="sxs-lookup"><span data-stu-id="a4e95-106">The column will be an auto-incrementing primary key for the parent table, and will be used for the **DataRelation** between the two tables.</span></span> <span data-ttu-id="a4e95-107">Le type de données de la colonne d’identité ajoutée sera **System.Int32**, contrairement au type de données de toutes les autres colonnes déduites, qui est **System.String**.</span><span class="sxs-lookup"><span data-stu-id="a4e95-107">The data type of the added identity column will be **System.Int32**, unlike the data type of all other inferred columns, which is **System.String**.</span></span> <span data-ttu-id="a4e95-108">Un <xref:System.Data.ForeignKeyConstraint> avec **DeleteRule** = **Cascade** sera également créé à l’aide de la nouvelle colonne dans les tables parent et enfant.</span><span class="sxs-lookup"><span data-stu-id="a4e95-108">A <xref:System.Data.ForeignKeyConstraint> with **DeleteRule** = **Cascade** will also be created using the new column in both the parent and child tables.</span></span>  
  
 <span data-ttu-id="a4e95-109">Examinons, par exemple, le code XML suivant :</span><span class="sxs-lookup"><span data-stu-id="a4e95-109">For example, consider the following XML:</span></span>  
  
```xml  
<DocumentElement>  
  <Element1>  
    <ChildElement1 attr1="value1" attr2="value2"/>  
    <ChildElement2>Text2</ChildElement2>  
  </Element1>  
</DocumentElement>  
```  
  
 <span data-ttu-id="a4e95-110">Le processus d'inférence produira deux tables :  **Element1** et **ChildElement1**.</span><span class="sxs-lookup"><span data-stu-id="a4e95-110">The inference process will produce two tables: **Element1** and **ChildElement1**.</span></span>  
  
 <span data-ttu-id="a4e95-111">Le **Element1** table aura deux colonnes : **Element1_Id** et **ChildElement2**.</span><span class="sxs-lookup"><span data-stu-id="a4e95-111">The **Element1** table will have two columns: **Element1_Id** and **ChildElement2**.</span></span> <span data-ttu-id="a4e95-112">Le **ColumnMapping** propriété de la **Element1_Id** jeu de colonnes **MappingType.Hidden**.</span><span class="sxs-lookup"><span data-stu-id="a4e95-112">The **ColumnMapping** property of the **Element1_Id** column will be set to **MappingType.Hidden**.</span></span> <span data-ttu-id="a4e95-113">Le **ColumnMapping** propriété de la **ChildElement2** jeu de colonnes **MappingType.Element**.</span><span class="sxs-lookup"><span data-stu-id="a4e95-113">The **ColumnMapping** property of the **ChildElement2** column will be set to **MappingType.Element**.</span></span> <span data-ttu-id="a4e95-114">Le **Element1_Id** colonne sera définie en tant que la clé primaire de la **Element1** table.</span><span class="sxs-lookup"><span data-stu-id="a4e95-114">The **Element1_Id** column will be set as the primary key of the **Element1** table.</span></span>  
  
 <span data-ttu-id="a4e95-115">Le **ChildElement1** table aura trois colonnes : **attr1**, **attr2** et **Element1_Id**.</span><span class="sxs-lookup"><span data-stu-id="a4e95-115">The **ChildElement1** table will have three columns: **attr1**, **attr2** and **Element1_Id**.</span></span> <span data-ttu-id="a4e95-116">Le **ColumnMapping** propriété pour le **attr1** et **attr2** colonnes seront définies sur **MappingType.Attribute**.</span><span class="sxs-lookup"><span data-stu-id="a4e95-116">The **ColumnMapping** property for the **attr1** and **attr2** columns will be set to **MappingType.Attribute**.</span></span> <span data-ttu-id="a4e95-117">Le **ColumnMapping** propriété de la **Element1_Id** jeu de colonnes **MappingType.Hidden**.</span><span class="sxs-lookup"><span data-stu-id="a4e95-117">The **ColumnMapping** property of the **Element1_Id** column will be set to **MappingType.Hidden**.</span></span>  
  
 <span data-ttu-id="a4e95-118">Un **DataRelation** et **ForeignKeyConstraint** sera créé à l’aide de la **Element1_Id** colonnes des deux tables.</span><span class="sxs-lookup"><span data-stu-id="a4e95-118">A **DataRelation** and **ForeignKeyConstraint** will be created using the **Element1_Id** columns from both tables.</span></span>  
  
 <span data-ttu-id="a4e95-119">**Jeu de données :** DocumentElement</span><span class="sxs-lookup"><span data-stu-id="a4e95-119">**DataSet:** DocumentElement</span></span>  
  
 <span data-ttu-id="a4e95-120">**Table :** Element1</span><span class="sxs-lookup"><span data-stu-id="a4e95-120">**Table:** Element1</span></span>  
  
|<span data-ttu-id="a4e95-121">Element1_Id</span><span class="sxs-lookup"><span data-stu-id="a4e95-121">Element1_Id</span></span>|<span data-ttu-id="a4e95-122">ChildElement2</span><span class="sxs-lookup"><span data-stu-id="a4e95-122">ChildElement2</span></span>|  
|------------------|-------------------|  
|<span data-ttu-id="a4e95-123">0</span><span class="sxs-lookup"><span data-stu-id="a4e95-123">0</span></span>|<span data-ttu-id="a4e95-124">Text2</span><span class="sxs-lookup"><span data-stu-id="a4e95-124">Text2</span></span>|  
  
 <span data-ttu-id="a4e95-125">**Table :** ChildElement1</span><span class="sxs-lookup"><span data-stu-id="a4e95-125">**Table:** ChildElement1</span></span>  
  
|<span data-ttu-id="a4e95-126">attr1</span><span class="sxs-lookup"><span data-stu-id="a4e95-126">attr1</span></span>|<span data-ttu-id="a4e95-127">attr2</span><span class="sxs-lookup"><span data-stu-id="a4e95-127">attr2</span></span>|<span data-ttu-id="a4e95-128">Element1_Id</span><span class="sxs-lookup"><span data-stu-id="a4e95-128">Element1_Id</span></span>|  
|-----------|-----------|------------------|  
|<span data-ttu-id="a4e95-129">valeur1</span><span class="sxs-lookup"><span data-stu-id="a4e95-129">value1</span></span>|<span data-ttu-id="a4e95-130">valeur2</span><span class="sxs-lookup"><span data-stu-id="a4e95-130">value2</span></span>|<span data-ttu-id="a4e95-131">0</span><span class="sxs-lookup"><span data-stu-id="a4e95-131">0</span></span>|  
  
 <span data-ttu-id="a4e95-132">**DataRelation :** Element1_ChildElement1</span><span class="sxs-lookup"><span data-stu-id="a4e95-132">**DataRelation:** Element1_ChildElement1</span></span>  
  
 <span data-ttu-id="a4e95-133">**ParentTable :** Element1</span><span class="sxs-lookup"><span data-stu-id="a4e95-133">**ParentTable:** Element1</span></span>  
  
 <span data-ttu-id="a4e95-134">**ParentColumn :** Element1_Id</span><span class="sxs-lookup"><span data-stu-id="a4e95-134">**ParentColumn:** Element1_Id</span></span>  
  
 <span data-ttu-id="a4e95-135">**ChildTable :** ChildElement1</span><span class="sxs-lookup"><span data-stu-id="a4e95-135">**ChildTable:** ChildElement1</span></span>  
  
 <span data-ttu-id="a4e95-136">**ChildColumn :** Element1_Id</span><span class="sxs-lookup"><span data-stu-id="a4e95-136">**ChildColumn:** Element1_Id</span></span>  
  
 <span data-ttu-id="a4e95-137">**Imbriqué :** True</span><span class="sxs-lookup"><span data-stu-id="a4e95-137">**Nested:** True</span></span>  
  
 <span data-ttu-id="a4e95-138">**ForeignKeyConstraint :** Element1_ChildElement1</span><span class="sxs-lookup"><span data-stu-id="a4e95-138">**ForeignKeyConstraint:** Element1_ChildElement1</span></span>  
  
 <span data-ttu-id="a4e95-139">**Colonne :** Element1_Id</span><span class="sxs-lookup"><span data-stu-id="a4e95-139">**Column:** Element1_Id</span></span>  
  
 <span data-ttu-id="a4e95-140">**ParentTable :** Element1</span><span class="sxs-lookup"><span data-stu-id="a4e95-140">**ParentTable:** Element1</span></span>  
  
 <span data-ttu-id="a4e95-141">**ChildTable :** ChildElement1</span><span class="sxs-lookup"><span data-stu-id="a4e95-141">**ChildTable:** ChildElement1</span></span>  
  
 <span data-ttu-id="a4e95-142">**DeleteRule :** Cascade</span><span class="sxs-lookup"><span data-stu-id="a4e95-142">**DeleteRule:** Cascade</span></span>  
  
 <span data-ttu-id="a4e95-143">**AcceptRejectRule :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="a4e95-143">**AcceptRejectRule:** None</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a4e95-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4e95-144">See also</span></span>

- [<span data-ttu-id="a4e95-145">Inférence de la structure relationnelle d’un DataSet à partir de XML</span><span class="sxs-lookup"><span data-stu-id="a4e95-145">Inferring DataSet Relational Structure from XML</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/inferring-dataset-relational-structure-from-xml.md)
- [<span data-ttu-id="a4e95-146">Chargement d’un DataSet à partir de XML</span><span class="sxs-lookup"><span data-stu-id="a4e95-146">Loading a DataSet from XML</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-a-dataset-from-xml.md)
- [<span data-ttu-id="a4e95-147">Chargement des informations de schéma de DataSet à partir de XML</span><span class="sxs-lookup"><span data-stu-id="a4e95-147">Loading DataSet Schema Information from XML</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-dataset-schema-information-from-xml.md)
- [<span data-ttu-id="a4e95-148">Imbrication de DataRelations</span><span class="sxs-lookup"><span data-stu-id="a4e95-148">Nesting DataRelations</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/nesting-datarelations.md)
- [<span data-ttu-id="a4e95-149">Utilisation de XML dans un DataSet</span><span class="sxs-lookup"><span data-stu-id="a4e95-149">Using XML in a DataSet</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/using-xml-in-a-dataset.md)
- [<span data-ttu-id="a4e95-150">DataSets, DataTables et DataViews</span><span class="sxs-lookup"><span data-stu-id="a4e95-150">DataSets, DataTables, and DataViews</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)
- [<span data-ttu-id="a4e95-151">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="a4e95-151">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
