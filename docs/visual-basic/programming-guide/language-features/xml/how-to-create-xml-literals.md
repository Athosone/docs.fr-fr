---
title: 'Procédure : Créer des littéraux XML (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- XML literals [Visual Basic], creating
ms.assetid: 573a6db5-b14d-4e42-b356-8cc7e2d77745
ms.openlocfilehash: 836ec4390e7675effe57c75c79768272d66925a3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61775906"
---
# <a name="how-to-create-xml-literals-visual-basic"></a>Procédure : Créer des littéraux XML (Visual Basic)
Vous pouvez créer un document, un fragment ou un élément XML directement dans le code à l’aide d’un littéral XML. Les exemples de cette rubrique montrent comment créer un élément XML qui comporte trois éléments enfants et comment créer un document XML.  
  
 Vous pouvez également utiliser le [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] API pour créer [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] objets. Pour plus d'informations, consultez <xref:System.Xml.Linq.XElement>.  
  
### <a name="to-create-an-xml-element"></a>Pour créer un élément XML  
  
- Créer le code XML inline à l’aide de la syntaxe des littéraux XML, qui est identique à la syntaxe XML réelle.  
  
     [!code-vb[VbXMLSamples#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples2.vb#5)]  
  
     Exécutez le code. La sortie de ce code est :  
  
     `<contact>`  
  
     `<name>Patrick Hines</name>`  
  
     `<phone type="home">206-555-0144</phone>`  
  
     `<phone type="work">425-555-0145</phone>`  
  
     `</contact>`  
  
### <a name="to-create-an-xml-document"></a>Pour créer un document XML  
  
- Créer le document XML inline. Le code suivant crée un document XML qui a la syntaxe littérale, une déclaration XML, une instruction de traitement, un commentaire et un élément qui contient un autre élément.  
  
     [!code-vb[VbXMLSamples#30](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples13.vb#30)]  
  
     Exécutez le code. La sortie de ce code est :  
  
     `<?xml-stylesheet type="text/xsl" href="show_book.xsl"?>`  
  
     `<!-- Tests that the application works. -->`  
  
     `<books>`  
  
     `<book/>`  
  
     `</books>`  
  
## <a name="see-also"></a>Voir aussi

- [XML](../../../../visual-basic/programming-guide/language-features/xml/index.md)
- [Création de code XML dans Visual Basic](../../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)
- [Littéral d’élément XML](../../../../visual-basic/language-reference/xml-literals/xml-element-literal.md)
- [Littéral de document XML](../../../../visual-basic/language-reference/xml-literals/xml-document-literal.md)
