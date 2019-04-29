---
title: 'Procédure : Rechercher un élément avec un élément enfant spécifique (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: b0d0a463-6a85-46c3-8453-ad25b0ecf93c
ms.openlocfilehash: 1b226f009776f397f73ab9ee7826484eb8869f28
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61780599"
---
# <a name="how-to-find-an-element-with-a-specific-child-element-visual-basic"></a><span data-ttu-id="095ee-102">Procédure : Rechercher un élément avec un élément enfant spécifique (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="095ee-102">How to: Find an Element with a Specific Child Element (Visual Basic)</span></span>
<span data-ttu-id="095ee-103">Cette rubrique montre comment rechercher un élément particulier qui a un élément enfant avec une valeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="095ee-103">This topic shows how to find a particular element that has a child element with a specific value.</span></span>  
  
## <a name="example"></a><span data-ttu-id="095ee-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="095ee-104">Example</span></span>  
 <span data-ttu-id="095ee-105">L'exemple recherche l'élément `Test` qui a un élément enfant `CommandLine` avec la valeur « Examp2.EXE ».</span><span class="sxs-lookup"><span data-stu-id="095ee-105">The example finds the `Test` element that has a `CommandLine` child element with the value of "Examp2.EXE".</span></span>  
  
 <span data-ttu-id="095ee-106">Cet exemple utilise le document XML suivant : [Exemple de fichier XML : Configuration de test (LINQ to XML)](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-test-configuration-linq-to-xml.md).</span><span class="sxs-lookup"><span data-stu-id="095ee-106">This example uses the following XML document: [Sample XML File: Test Configuration (LINQ to XML)](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-test-configuration-linq-to-xml.md).</span></span>  
  
```vb  
Dim root As XElement = XElement.Load("TestConfig.xml")  
Dim tests As IEnumerable(Of XElement) = _  
    From el In root.<Test> _  
    Where el.<CommandLine>.Value = "Examp2.EXE" _  
    Select el  
For Each el as XElement In tests  
    Console.WriteLine(el.@TestId)  
Next  
```  
  
 <span data-ttu-id="095ee-107">Ce code génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="095ee-107">This code produces the following output:</span></span>  
  
```  
0002  
0006  
```  
  
 <span data-ttu-id="095ee-108">Notez que cet exemple utilise le [propriété d’axe enfant XML](../../../../visual-basic/language-reference/xml-axis/xml-child-axis-property.md), le [propriété d’axe d’attribut XML](../../../../visual-basic/language-reference/xml-axis/xml-attribute-axis-property.md)et le [propriété de valeur XML](../../../../visual-basic/language-reference/xml-axis/xml-value-property.md).</span><span class="sxs-lookup"><span data-stu-id="095ee-108">Note that this example uses the [XML Child axis property](../../../../visual-basic/language-reference/xml-axis/xml-child-axis-property.md), the [XML Attribute axis property](../../../../visual-basic/language-reference/xml-axis/xml-attribute-axis-property.md), and the [XML Value property](../../../../visual-basic/language-reference/xml-axis/xml-value-property.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="095ee-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="095ee-109">Example</span></span>  
 <span data-ttu-id="095ee-110">L'exemple suivant illustre la même requête pour du code XML qui est dans un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="095ee-110">The following example shows the same query for XML that is in a namespace.</span></span> <span data-ttu-id="095ee-111">Pour plus d’informations, consultez [utilisation des espaces de noms XML (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/working-with-xml-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="095ee-111">For more information, see [Working with XML Namespaces (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/working-with-xml-namespaces.md).</span></span>  
  
 <span data-ttu-id="095ee-112">Cet exemple utilise le document XML suivant : [Exemple de fichier XML : Configuration de test dans un espace de noms](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-test-configuration-in-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="095ee-112">This example uses the following XML document: [Sample XML File: Test Configuration in a Namespace](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-test-configuration-in-a-namespace.md).</span></span>  
  
```vb  
Imports <xmlns='http://www.adatum.com'>  
  
Module Module1  
    Sub Main()  
        Dim root As XElement = XElement.Load("TestConfigInNamespace.xml")  
        Dim tests As IEnumerable(Of XElement) = _  
            From el In root.<Test> _  
            Where el.<CommandLine>.Value = "Examp2.EXE" _  
            Select el  
        For Each el As XElement In tests  
            Console.WriteLine(el.@TestId)  
        Next  
    End Sub  
End Module  
```  
  
 <span data-ttu-id="095ee-113">Ce code génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="095ee-113">This code produces the following output:</span></span>  
  
```  
0002  
0006  
```  
  
## <a name="see-also"></a><span data-ttu-id="095ee-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="095ee-114">See also</span></span>

- <xref:System.Xml.Linq.XElement.Attribute%2A>
- <xref:System.Xml.Linq.XContainer.Elements%2A>
- [<span data-ttu-id="095ee-115">Requêtes de base (LINQ to XML) (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="095ee-115">Basic Queries (LINQ to XML) (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/basic-queries-linq-to-xml.md)
- [<span data-ttu-id="095ee-116">Vue d’ensemble des opérateurs de requête standard (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="095ee-116">Standard Query Operators Overview (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md)
- [<span data-ttu-id="095ee-117">Opérations de projection (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="095ee-117">Projection Operations (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/projection-operations.md)
