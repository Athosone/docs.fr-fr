---
title: 'Procédure : Interroger des caractères dans une chaîne (LINQ) (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: 499ebbe0-746c-4235-9dba-ce722c12b50e
ms.openlocfilehash: 3f460f635c581eef5655c5707e3dd356e7986d74
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61644383"
---
# <a name="how-to-query-for-characters-in-a-string-linq-visual-basic"></a>Procédure : Interroger des caractères dans une chaîne (LINQ) (Visual Basic)
La classe <xref:System.String> implémente l’interface <xref:System.Collections.Generic.IEnumerable%601> générique. De ce fait, il est possible d’interroger n’importe quelle chaîne comme une séquence de caractères. Toutefois, ceci n’est pas une utilisation courante de LINQ. Pour les opérations de critères spéciaux complexes, utilisez la classe <xref:System.Text.RegularExpressions.Regex>.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant interroge une chaîne pour déterminer le nombre de chiffres qu’elle contient. Notez que la requête est « réutilisée » après sa première exécution. Ceci est possible car la requête proprement dite ne stocke pas de résultats réels.  
  
```vb  
Class QueryAString  
  
    Shared Sub Main()  
  
        ' A string is an IEnumerable data source.  
        Dim aString As String = "ABCDE99F-J74-12-89A"  
  
        ' Select only those characters that are numbers  
        Dim stringQuery = From ch In aString   
                          Where Char.IsDigit(ch)   
                          Select ch  
        ' Execute the query  
        For Each c As Char In stringQuery  
            Console.Write(c & " ")  
        Next  
  
        ' Call the Count method on the existing query.  
        Dim count As Integer = stringQuery.Count()  
        Console.WriteLine(System.Environment.NewLine & "Count = " & count)  
  
        ' Select all characters before the first '-'  
        Dim stringQuery2 = aString.TakeWhile(Function(c) c <> "-")  
  
        ' Execute the second query  
        For Each ch In stringQuery2  
            Console.Write(ch)  
        Next  
  
        Console.WriteLine(System.Environment.NewLine & "Press any key to exit")  
        Console.ReadKey()  
    End Sub  
End Class  
' Output:  
' 9 9 7 4 1 2 8 9   
' Count = 8  
' ABCDE99F  
```  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Créez un projet qui cible le .NET Framework version 3.5 ou ultérieure, avec une référence à System.Core.dll et une déclaration `Imports` pour l’espace de noms System.Linq.  
  
## <a name="see-also"></a>Voir aussi

- [LINQ et chaînes (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/linq-and-strings.md)
- [Guide pratique pour Combiner des requêtes LINQ avec des Expressions régulières (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/how-to-combine-linq-queries-with-regular-expressions.md)
