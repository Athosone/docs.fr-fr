---
title: Ajout d’éléments, attributs et nœuds à une arborescence XML (Visual Basic)
ms.date: 07/20/2015
ms.assetid: e243e694-c987-43aa-8b22-1e33dace582c
ms.openlocfilehash: 35d3bdb27342dd7a871778ad4749db4d6849bd60
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58814313"
---
# <a name="adding-elements-attributes-and-nodes-to-an-xml-tree-visual-basic"></a><span data-ttu-id="8c246-102">Ajout d’éléments, attributs et nœuds à une arborescence XML (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="8c246-102">Adding Elements, Attributes, and Nodes to an XML Tree (Visual Basic)</span></span>
<span data-ttu-id="8c246-103">Vous pouvez ajouter du contenu (éléments, attributs, commentaires, instructions de traitement, texte et CData) à une arborescence XML existante.</span><span class="sxs-lookup"><span data-stu-id="8c246-103">You can add content (elements, attributes, comments, processing instructions, text, and CDATA) to an existing XML tree.</span></span>  
  
## <a name="methods-for-adding-content"></a><span data-ttu-id="8c246-104">Méthodes pour ajouter du contenu</span><span class="sxs-lookup"><span data-stu-id="8c246-104">Methods for Adding Content</span></span>  
 <span data-ttu-id="8c246-105">Les méthodes suivantes ajoutent du contenu enfant à un objet <xref:System.Xml.Linq.XElement> ou <xref:System.Xml.Linq.XDocument> :</span><span class="sxs-lookup"><span data-stu-id="8c246-105">The following methods add child content to an <xref:System.Xml.Linq.XElement> or an <xref:System.Xml.Linq.XDocument>:</span></span>  
  
|<span data-ttu-id="8c246-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="8c246-106">Method</span></span>|<span data-ttu-id="8c246-107">Description</span><span class="sxs-lookup"><span data-stu-id="8c246-107">Description</span></span>|  
|------------|-----------------|  
|<xref:System.Xml.Linq.XContainer.Add%2A>|<span data-ttu-id="8c246-108">Ajoute du contenu à la fin du contenu enfant de l'objet <xref:System.Xml.Linq.XContainer>.</span><span class="sxs-lookup"><span data-stu-id="8c246-108">Adds content at the end of the child content of the <xref:System.Xml.Linq.XContainer>.</span></span>|  
|<xref:System.Xml.Linq.XContainer.AddFirst%2A>|<span data-ttu-id="8c246-109">Ajoute du contenu au début du contenu enfant de l'objet <xref:System.Xml.Linq.XContainer>.</span><span class="sxs-lookup"><span data-stu-id="8c246-109">Adds content at the beginning of the child content of the <xref:System.Xml.Linq.XContainer>.</span></span>|  
  
 <span data-ttu-id="8c246-110">Les méthodes suivantes ajoutent du contenu en tant que nœuds frères d'un objet <xref:System.Xml.Linq.XNode>.</span><span class="sxs-lookup"><span data-stu-id="8c246-110">The following methods add content as sibling nodes of an <xref:System.Xml.Linq.XNode>.</span></span> <span data-ttu-id="8c246-111">Le nœud le plus courant auquel vous ajoutez du contenu frère est <xref:System.Xml.Linq.XElement>, bien que vous puissiez ajouter du contenu frère valide à d'autres types de nœuds tels que <xref:System.Xml.Linq.XText> ou <xref:System.Xml.Linq.XComment>.</span><span class="sxs-lookup"><span data-stu-id="8c246-111">The most common node to which you add sibling content is <xref:System.Xml.Linq.XElement>, although you can add valid sibling content to other types of nodes such as <xref:System.Xml.Linq.XText> or <xref:System.Xml.Linq.XComment>.</span></span>  
  
|<span data-ttu-id="8c246-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="8c246-112">Method</span></span>|<span data-ttu-id="8c246-113">Description</span><span class="sxs-lookup"><span data-stu-id="8c246-113">Description</span></span>|  
|------------|-----------------|  
|<xref:System.Xml.Linq.XNode.AddAfterSelf%2A>|<span data-ttu-id="8c246-114">Ajoute du contenu après l'objet <xref:System.Xml.Linq.XNode>.</span><span class="sxs-lookup"><span data-stu-id="8c246-114">Adds content after the <xref:System.Xml.Linq.XNode>.</span></span>|  
|<xref:System.Xml.Linq.XNode.AddBeforeSelf%2A>|<span data-ttu-id="8c246-115">Ajoute du contenu avant l'objet <xref:System.Xml.Linq.XNode>.</span><span class="sxs-lookup"><span data-stu-id="8c246-115">Adds content before the <xref:System.Xml.Linq.XNode>.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="8c246-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="8c246-116">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="8c246-117">Description</span><span class="sxs-lookup"><span data-stu-id="8c246-117">Description</span></span>  
 <span data-ttu-id="8c246-118">L'exemple suivant crée deux arborescences XML, puis modifie l'une des arborescences.</span><span class="sxs-lookup"><span data-stu-id="8c246-118">The following example creates two XML trees, and then modifies one of the trees.</span></span>  
  
### <a name="code"></a><span data-ttu-id="8c246-119">Code</span><span class="sxs-lookup"><span data-stu-id="8c246-119">Code</span></span>  
  
```vb  
Dim srcTree As XElement = _  
    <Root>  
        <Element1>1</Element1>  
        <Element2>2</Element2>  
        <Element3>3</Element3>  
        <Element4>4</Element4>  
        <Element5>5</Element5>  
    </Root>  
Dim xmlTree As XElement = _  
    <Root>  
        <Child1>1</Child1>  
        <Child2>2</Child2>  
        <Child3>3</Child3>  
        <Child4>4</Child4>  
        <Child5>5</Child5>  
    </Root>  
  
xmlTree.Add(<NewChild>new content</NewChild>)  
xmlTree.Add( _  
    From el In srcTree.Elements() _  
    Where CInt(el) > 3 _  
    Select el)  
  
' Even though Child9 does not exist in srcTree, the following statement  
' will not throw an exception, and nothing will be added to xmlTree.  
xmlTree.Add(srcTree.Element("Child9"))  
Console.WriteLine(xmlTree)  
```  
  
### <a name="comments"></a><span data-ttu-id="8c246-120">Commentaires</span><span class="sxs-lookup"><span data-stu-id="8c246-120">Comments</span></span>  
 <span data-ttu-id="8c246-121">Ce code génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="8c246-121">This code produces the following output:</span></span>  
  
```xml  
<Root>  
  <Child1>1</Child1>  
  <Child2>2</Child2>  
  <Child3>3</Child3>  
  <Child4>4</Child4>  
  <Child5>5</Child5>  
  <NewChild>new content</NewChild>  
  <Element4>4</Element4>  
  <Element5>5</Element5>  
</Root>  
```  
  
## <a name="see-also"></a><span data-ttu-id="8c246-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c246-122">See also</span></span>

- [<span data-ttu-id="8c246-123">Modification d’arborescences XML (LINQ to XML) (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="8c246-123">Modifying XML Trees (LINQ to XML) (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/modifying-xml-trees-linq-to-xml.md)
