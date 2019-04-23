---
title: 'Procédure : Supprimer une ressource système (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- Using statement [Visual Basic], disposing of system resources
- Visual Basic code, control flow
- system resources, disposing of
- resources [Visual Basic], disposing of system
- system resources
- Using statement [Visual Basic], Using...End Using
- Using block
ms.assetid: 8be2b239-8090-419b-8e7e-bcaa75b0ecc8
ms.openlocfilehash: e3594db036edc3a6288b0373737c1ee26a691a57
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59341905"
---
# <a name="how-to-dispose-of-a-system-resource-visual-basic"></a>Procédure : Supprimer une ressource système (Visual Basic)
Vous pouvez utiliser un `Using` bloc pour garantir que le système supprime une ressource lorsque votre code quitte le bloc. Cela est utile si vous utilisez une ressource système qui consomme une grande quantité de mémoire ou d’autres composants également vouloir utiliser.  
  
### <a name="to-dispose-of-a-database-connection-when-your-code-is-finished-with-it"></a>Pour supprimer une connexion de base de données lorsque votre code est terminé avec lui  
  
1. Veillez à inclure le texte approprié [instruction Imports (.NET Namespace et Type)](../../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md) pour la connexion de base de données au début de votre fichier source (dans ce cas, <xref:System.Data.SqlClient>).  
  
2. Créer un `Using` bloc avec le `Using` et `End Using` instructions. Dans le bloc, placez le code qui traite de la connexion de base de données.  
  
3. Déclarez la connexion et de créer une instance de celui-ci dans le cadre de la `Using` instruction.  
  
    ```  
    ' Insert the following line at the beginning of your source file.  
    Imports System.Data.SqlClient  
    Public Sub AccessSql(ByVal s As String)  
        Using sqc As New System.Data.SqlClient.SqlConnection(s)  
            MsgBox("Connected with string """ & sqc.ConnectionString & """")  
        End Using  
    End Sub  
    ```  
  
     Le système supprime la ressource, quel que soit la manière dont vous quittez le bloc, y compris le cas d’une exception non gérée.  
  
     Notez que vous ne pouvez pas accéder à `sqc` à partir d’en dehors de la `Using` bloquer, car sa portée est limitée au bloc.  
  
     Vous pouvez utiliser cette même technique sur une ressource système comme un descripteur de fichier ou un wrapper COM. Vous utilisez un `Using` bloquer quand vous voulez être certain de laisser la ressource est disponible pour d’autres composants après avoir quitté le `Using` bloc.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Data.SqlClient.SqlConnection>
- [Flux de contrôle](../../../../visual-basic/programming-guide/language-features/control-flow/index.md)
- [Structures de décision](../../../../visual-basic/programming-guide/language-features/control-flow/decision-structures.md)
- [Structures de boucle](../../../../visual-basic/programming-guide/language-features/control-flow/loop-structures.md)
- [Autres structures de contrôle](../../../../visual-basic/programming-guide/language-features/control-flow/other-control-structures.md)
- [Structures de contrôle imbriquées](../../../../visual-basic/programming-guide/language-features/control-flow/nested-control-structures.md)
- [Using (instruction)](../../../../visual-basic/language-reference/statements/using-statement.md)
