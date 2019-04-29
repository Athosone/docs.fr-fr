---
title: LINQ to XML Annotations2
ms.date: 07/20/2015
ms.assetid: c3e8b3ff-fceb-4428-b0ca-1ed6f128aac8
ms.openlocfilehash: edf8e0126c632deae6b6d4c235c4880d7b8687e8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61663425"
---
# <a name="linq-to-xml-annotations"></a><span data-ttu-id="5f771-102">Annotations LINQ to XML</span><span class="sxs-lookup"><span data-stu-id="5f771-102">LINQ to XML Annotations</span></span>
<span data-ttu-id="5f771-103">Les annotations dans [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] vous permettent d’associer n’importe quel objet arbitraire de n’importe quel type arbitraire à n’importe quel composant XML dans une arborescence XML.</span><span class="sxs-lookup"><span data-stu-id="5f771-103">Annotations in [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] enable you to associate any arbitrary object of any arbitrary type with any XML component in an XML tree.</span></span>  
  
 <span data-ttu-id="5f771-104">Pour ajouter une annotation à un composant XML, tel qu'un objet <xref:System.Xml.Linq.XElement> ou <xref:System.Xml.Linq.XAttribute>, vous appelez la méthode <xref:System.Xml.Linq.XObject.AddAnnotation%2A>.</span><span class="sxs-lookup"><span data-stu-id="5f771-104">To add an annotation to an XML component, such as an <xref:System.Xml.Linq.XElement> or <xref:System.Xml.Linq.XAttribute>, you call the <xref:System.Xml.Linq.XObject.AddAnnotation%2A> method.</span></span> <span data-ttu-id="5f771-105">Vous pouvez récupérer des annotations par type.</span><span class="sxs-lookup"><span data-stu-id="5f771-105">You retrieve annotations by type.</span></span>  
  
 <span data-ttu-id="5f771-106">Notez que les annotations ne font pas partie du jeu d'informations XML ; elles ne sont pas sérialisées ou désérialisées.</span><span class="sxs-lookup"><span data-stu-id="5f771-106">Note that annotations are not part of the XML infoset; they are not serialized or deserialized.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="5f771-107">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5f771-107">Methods</span></span>  
 <span data-ttu-id="5f771-108">Vous pouvez utiliser les méthodes suivantes lorsque vous travaillez avec des annotations :</span><span class="sxs-lookup"><span data-stu-id="5f771-108">You can use the following methods when working with annotations:</span></span>  
  
|<span data-ttu-id="5f771-109">Méthode</span><span class="sxs-lookup"><span data-stu-id="5f771-109">Method</span></span>|<span data-ttu-id="5f771-110">Description</span><span class="sxs-lookup"><span data-stu-id="5f771-110">Description</span></span>|  
|------------|-----------------|  
|<xref:System.Xml.Linq.XObject.AddAnnotation%2A>|<span data-ttu-id="5f771-111">Ajoute un objet à la liste d'annotation de <xref:System.Xml.Linq.XObject>.</span><span class="sxs-lookup"><span data-stu-id="5f771-111">Adds an object to the annotation list of an <xref:System.Xml.Linq.XObject>.</span></span>|  
|<xref:System.Xml.Linq.XObject.Annotation%2A>|<span data-ttu-id="5f771-112">Obtient le premier objet annotation du type spécifié de <xref:System.Xml.Linq.XObject>.</span><span class="sxs-lookup"><span data-stu-id="5f771-112">Gets the first annotation object of the specified type from an <xref:System.Xml.Linq.XObject>.</span></span>|  
|<xref:System.Xml.Linq.XObject.Annotations%2A>|<span data-ttu-id="5f771-113">Obtient une collection d’annotations du type spécifié pour un objet <xref:System.Xml.Linq.XObject>.</span><span class="sxs-lookup"><span data-stu-id="5f771-113">Gets a collection of annotations of the specified type for an <xref:System.Xml.Linq.XObject>.</span></span>|  
|<xref:System.Xml.Linq.XObject.RemoveAnnotations%2A>|<span data-ttu-id="5f771-114">Supprime les annotations du type spécifié d’un objet <xref:System.Xml.Linq.XObject>.</span><span class="sxs-lookup"><span data-stu-id="5f771-114">Removes the annotations of the specified type from an <xref:System.Xml.Linq.XObject>.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="5f771-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f771-115">See also</span></span>

- [<span data-ttu-id="5f771-116">Avancées programmation LINQ to XML (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="5f771-116">Advanced LINQ to XML Programming (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/advanced-linq-to-xml-programming.md)
