---
title: Propriété de valeur XML (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.XmlPropertyExtensionValue
helpviewer_keywords:
- Value property [Visual Basic]
- Visual Basic code, accessing XML
- XML axis [Visual Basic], Value
- XML Value property [Visual Basic]
ms.assetid: 7ddd057a-a195-4e9b-ad8b-2ee0e615a20f
ms.openlocfilehash: 1c7aa1cc32bc1c5ef637f7a606db7e695f1dfaee
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61799162"
---
# <a name="xml-value-property-visual-basic"></a>Propriété de valeur XML (Visual Basic)
Fournit l’accès à la valeur du premier élément d’une collection de <xref:System.Xml.Linq.XElement> objets.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
object.Value  
```  
  
## <a name="parts"></a>Composants  
  
|Terme|Définition|  
|---|---|  
|`object`|Obligatoire. Collection d'objets <xref:System.Xml.Linq.XElement>.|  
  
## <a name="return-value"></a>Valeur de retour  
 Un `String` qui contient la valeur du premier élément de la collection, ou `Nothing` si la collection est vide.  
  
## <a name="remarks"></a>Notes  
 Le <xref:System.Xml.Linq.XElement.Value%2A> propriété permet de facilement accéder à la valeur du premier élément dans une collection de <xref:System.Xml.Linq.XElement> objets. Cette propriété vérifie d’abord si la collection contient au moins un objet. Si la collection est vide, cette propriété retourne `Nothing`. Sinon, cette propriété retourne la valeur de la <xref:System.Xml.Linq.XElement.Value%2A> propriété du premier élément dans la collection.  
  
> [!NOTE]
>  Quand vous accédez à la valeur d’un attribut XML à l’aide du '\@' identificateur, la valeur d’attribut est retournée en tant qu’un `String` et vous n’avez pas besoin de spécifier explicitement le <xref:System.Xml.Linq.XAttribute.Value%2A> propriété.  
  
 Pour accéder aux autres éléments dans une collection, vous pouvez utiliser la propriété indexeur d’extension XML. Pour plus d’informations, consultez [propriété d’indexeur d’Extension](../../../visual-basic/language-reference/xml-axis/extension-indexer-property.md).  
  
## <a name="inheritance"></a>Héritage  
 La plupart des utilisateurs ne devrez pas mettre en œuvre <xref:System.Collections.Generic.IEnumerable%601>et peuvent donc ignorer cette section.  
  
 Le <xref:System.Xml.Linq.XElement.Value%2A> propriété est une propriété d’extension pour les types qui implémentent `IEnumerable(Of XElement)`. La liaison de cette propriété d’extension est similaire à la liaison de méthodes d’extension : si un type implémente une des interfaces et définit une propriété qui porte le nom « Valeur », cette propriété est prioritaire sur la propriété d’extension. En d’autres termes, cela <xref:System.Xml.Linq.XElement.Value%2A> propriété peut être substituée en définissant une nouvelle propriété dans une classe qui implémente `IEnumerable(Of XElement)`.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment utiliser le <xref:System.Xml.Linq.XElement.Value%2A> propriété pour accéder au premier nœud dans une collection de <xref:System.Xml.Linq.XElement> objets. L’exemple utilise la propriété d’axe enfant pour obtenir la collection de tous les nœuds enfants nommés `phone` qui se trouvent dans le `contact` objet.  
  
 [!code-vb[VbXMLSamples#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples7.vb#15)]  
  
 Ce code affiche le texte suivant :  
  
 `Phone number: 206-555-0144`  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment obtenir la valeur d’un attribut XML à partir d’une collection de <xref:System.Xml.Linq.XAttribute> objets. L’exemple utilise la propriété de l’axe d’attribut pour afficher la valeur de la `type` attribut pour tous les `phone` éléments.  
  
 [!code-vb[VbXMLSamples#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples7.vb#16)]  
  
 Ce code affiche le texte suivant :  
  
 `home`  
  
 `work`  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Xml.Linq.XElement>
- <xref:System.Collections.Generic.IEnumerable%601>
- [Propriétés d’axe XML](../../../visual-basic/language-reference/xml-axis/index.md)
- [Littéraux XML](../../../visual-basic/language-reference/xml-literals/index.md)
- [Création de code XML dans Visual Basic](../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)
- [Méthodes d’extension](../../../visual-basic/programming-guide/language-features/procedures/extension-methods.md)
- [Propriété d’indexeur d’extension](../../../visual-basic/language-reference/xml-axis/extension-indexer-property.md)
- [Propriété d’axe enfant XML](../../../visual-basic/language-reference/xml-axis/xml-child-axis-property.md)
- [Propriété d’axe d’attribut XML](../../../visual-basic/language-reference/xml-axis/xml-attribute-axis-property.md)
