---
title: 'Procédure : Transformer du XML à l’aide de LINQ (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- XML [Visual Basic], transforming
- LINQ to XML [Visual Basic], transforming XML
ms.assetid: 815687f4-0bc2-4c0b-adc6-d78744aa356f
ms.openlocfilehash: c34d3988c89e0ce07676e9181200fc039010b50a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59324981"
---
# <a name="how-to-transform-xml-by-using-linq-visual-basic"></a>Procédure : Transformer du XML à l’aide de LINQ (Visual Basic)
[Littéraux XML](../../../../visual-basic/language-reference/xml-literals/index.md) rendent facile à lire les données XML à partir d’une source et le transforme en un nouveau format XML. Vous pouvez tirer parti des requêtes LINQ pour récupérer le contenu à transformer, ou modifier le contenu d’un document existant dans un nouveau format XML.  
  
 L’exemple de cette rubrique transforme le contenu d’un document source XML au format HTML à afficher dans un navigateur.  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-transform-an-xml-document"></a>Pour transformer un document XML  
  
1. Dans Visual Studio, créez un nouveau projet Visual Basic dans le **Application Console** modèle de projet.  
  
2. Double-cliquez sur le fichier Module1.vb créé dans le projet pour modifier le code Visual Basic. Ajoutez le code suivant à la `Sub Main` de la `Module1` module. Ce code crée le document XML source comme un <xref:System.Xml.Linq.XDocument> objet.  
  
    ```vb  
    Dim catalog =   
      <?xml version="1.0"?>  
        <Catalog>  
          <Book id="bk101">  
            <Author>Garghentini, Davide</Author>  
            <Title>XML Developer's Guide</Title>  
            <Price>44.95</Price>  
            <Description>  
              An in-depth look at creating applications  
              with <technology>XML</technology>. For   
              <audience>beginners</audience> or   
              <audience>advanced</audience> developers.  
            </Description>  
          </Book>  
          <Book id="bk331">  
            <Author>Spencer, Phil</Author>  
            <Title>Developing Applications with Visual Basic .NET</Title>  
            <Price>45.95</Price>  
            <Description>  
              Get the expert insights, practical code samples,   
              and best practices you need   
              to advance your expertise with <technology>Visual   
              Basic .NET</technology>.   
              Learn how to create faster, more reliable applications  
              based on professional,   
              pragmatic guidance by today's top <audience>developers</audience>.  
            </Description>  
          </Book>  
        </Catalog>  
    ```  
  
     [Guide pratique pour Charger XML à partir d’un fichier, une chaîne ou un Stream](../../../../visual-basic/programming-guide/language-features/xml/how-to-load-xml-from-a-file-string-or-stream.md).  
  
3. Après le code pour créer le document XML source, ajoutez le code suivant pour extraire tous les \<livre > éléments à partir de l’objet et les transformer en un document HTML. La liste des \<livre > éléments est créé à l’aide d’une requête LINQ qui retourne une collection de <xref:System.Xml.Linq.XElement> objets qui contiennent le code HTML transformé. Vous pouvez utiliser des expressions incorporées pour placer les valeurs à partir du document source dans le nouveau format XML.  
  
     Le document HTML résultant est écrit dans un fichier à l’aide de la <xref:System.Xml.Linq.XElement.Save%2A> (méthode).  
  
    ```vb  
    Dim htmlOutput =   
      <html>  
        <body>  
          <%= From book In catalog.<Catalog>.<Book>   
              Select <div>  
                       <h1><%= book.<Title>.Value %></h1>  
                       <h3><%= "By " & book.<Author>.Value %></h3>  
                        <h3><%= "Price = " & book.<Price>.Value %></h3>  
                        <h2>Description</h2>  
                        <%= TransformDescription(book.<Description>(0)) %>  
                        <hr/>  
                      </div> %>  
        </body>  
      </html>  
  
    htmlOutput.Save("BookDescription.html")  
    ```  
  
4. Après avoir `Sub Main` de `Module1`, ajoutez une nouvelle méthode (`Sub`) pour transformer un \<Description > nœud dans le format HTML spécifié. Cette méthode est appelée par le code à l’étape précédente et est utilisée pour conserver le format de la \<Description > éléments.  
  
     Cette méthode remplace les sous-éléments de le \<Description > élément HTML. Le `ReplaceWith` méthode est utilisée pour conserver l’emplacement des sous-éléments. Le contenu transformé de la \<Description > élément est inclus dans un paragraphe HTML (\<p >) élément. Le <xref:System.Xml.Linq.XContainer.Nodes%2A> propriété est utilisée pour récupérer le contenu transformé de la \<Description > élément. Cela garantit que les sous-éléments sont inclus dans le contenu transformé.  
  
     Ajoutez le code suivant après `Sub Main` de `Module1`.  
  
    ```vb  
    Public Function TransformDescription(ByVal desc As XElement) As XElement  
  
      ' Replace <technology> elements with <b>.  
      Dim content = (From element In desc...<technology>).ToList()  
  
      If content.Count > 0 Then  
        For i = 0 To content.Count - 1  
          content(i).ReplaceWith(<b><%= content(i).Value %></b>)  
        Next  
      End If  
  
      ' Replace <audience> elements with <i>.  
      content = (From element In desc...<audience>).ToList()  
  
      If content.Count > 0 Then  
        For i = 0 To content.Count - 1  
          content(i).ReplaceWith(<i><%= content(i).Value %></i>)  
        Next  
      End If  
  
      ' Return the updated contents of the <Description> element.  
      Return <p><%= desc.Nodes %></p>  
    End Function  
    ```  
  
5. Enregistrez les modifications apportées.  
  
6. Appuyez sur F5 pour exécuter le code. Enregistré le document résultant ressemblera à ce qui suit :  
  
    ```  
    <?xml version="1.0"?>  
    <html>  
      <body>  
        <div>  
          <h1>XML Developer's Guide</h1>  
          <h3>By Garghentini, Davide</h3>  
          <h3>Price = 44.95</h3>  
          <h2>Description</h2>  
          <p>  
            An in-depth look at creating applications  
            with <b>XML</b>. For   
            <i>beginners</i> or   
            <i>advanced</i> developers.  
          </p>  
          <hr />  
        </div>  
        <div>  
          <h1>Developing Applications with Visual Basic .NET</h1>  
          <h3>By Spencer, Phil</h3>  
          <h3>Price = 45.95</h3>  
          <h2>Description</h2>  
          <p>  
            Get the expert insights, practical code   
            samples, and best practices you need   
            to advance your expertise with <b>Visual   
            Basic .NET</b>. Learn how to create faster,  
            more reliable applications based on  
            professional, pragmatic guidance by today's   
            top <i>developers</i>.  
          </p>  
          <hr />  
        </div>  
      </body>  
    </html>  
    ```  
  
## <a name="see-also"></a>Voir aussi

- [Littéraux XML](../../../../visual-basic/language-reference/xml-literals/index.md)
- [Manipulation de code XML dans Visual Basic](../../../../visual-basic/programming-guide/language-features/xml/manipulating-xml.md)
- [XML](../../../../visual-basic/programming-guide/language-features/xml/index.md)
- [Guide pratique pour Charger XML à partir d’un fichier, une chaîne ou un Stream](../../../../visual-basic/programming-guide/language-features/xml/how-to-load-xml-from-a-file-string-or-stream.md)
- [LINQ](../../../../visual-basic/programming-guide/language-features/linq/index.md)
- [Introduction à LINQ en Visual Basic](../../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
