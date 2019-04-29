---
title: Await, opérateur (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Await
helpviewer_keywords:
- Await operator [Visual Basic]
- Await [Visual Basic]
ms.assetid: 6b1ce283-e92b-4ba7-b081-7be7b3d37af9
ms.openlocfilehash: d9d50433e3bc24df7cda137a145ab3f0f0302a1f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61608662"
---
# <a name="await-operator-visual-basic"></a>Await, opérateur (Visual Basic)
Vous appliquez le `Await` opérateur à un opérande dans une expression lambda ou de méthode asynchrone pour interrompre l’exécution de la méthode jusqu'à ce que la tâche attendue se termine. La tâche représente un travail en cours.  
  
 La méthode dans laquelle `Await` est utilisée doit avoir un [Async](../../../visual-basic/language-reference/modifiers/async.md) modificateur. Cette méthode, définie à l’aide du modificateur `Async` et contenant généralement une ou plusieurs expressions `Await`, est appelée *méthode async*.  
  
> [!NOTE]
>  Les mots clés `Async` et `Await` ont été introduits dans Visual Studio 2012. Pour une introduction à la programmation asynchrone, consultez [programmation asynchrone avec Async et Await](../../../visual-basic/programming-guide/concepts/async/index.md).  
  
 En règle générale, la tâche à laquelle vous appliquez le `Await` opérateur est la valeur de retour d’un appel à une méthode qui implémente le [Task-Based Asynchronous Pattern](https://go.microsoft.com/fwlink/?LinkId=204847), autrement dit, un <xref:System.Threading.Tasks.Task> ou un <xref:System.Threading.Tasks.Task%601>.  
  
 Dans le code suivant, le <xref:System.Net.Http.HttpClient> méthode <xref:System.Net.Http.HttpClient.GetByteArrayAsync%2A> retourne `getContentsTask`, un `Task(Of Byte())`. La tâche est une promesse de produire le tableau d’octets réel quand l’opération est terminée. L'opérateur `Await` est appliqué à `getContentsTask` pour suspendre l'exécution dans `SumPageSizesAsync` jusqu'à ce que `getContentsTask` soit terminé. Entre-temps, le contrôle revient à l'appelant de `SumPageSizesAsync`. Quand `getContentsTask` est terminé, l'expression `Await` s'évalue en tableau d'octets.  
  
```vb  
Private Async Function SumPageSizesAsync() As Task  
  
    ' To use the HttpClient type in desktop apps, you must include a using directive and add a   
    ' reference for the System.Net.Http namespace.  
    Dim client As HttpClient = New HttpClient()   
    ' . . .   
    Dim getContentsTask As Task(Of Byte()) = client.GetByteArrayAsync(url)  
    Dim urlContents As Byte() = Await getContentsTask  
  
    ' Equivalently, now that you see how it works, you can write the same thing in a single line.  
    'Dim urlContents As Byte() = Await client.GetByteArrayAsync(url)  
    ' . . .  
End Function  
```  
  
> [!IMPORTANT]
>  Pour un exemple complet, consultez [Procédure pas à pas : Accès au web avec Async et Await](../../../visual-basic/programming-guide/concepts/async/walkthrough-accessing-the-web-by-using-async-and-await.md). Vous pouvez télécharger l’exemple à partir des [exemples de code pour les développeurs](https://code.msdn.microsoft.com/Async-Sample-Accessing-the-9c10497f) sur le site web de Microsoft. L'exemple est dans le projet AsyncWalkthrough_HttpClient.  
  
 Si `Await` est appliqué au résultat d’un appel de méthode qui retourne un `Task(Of TResult)`, le type de la `Await` expression est TResult. Si `Await` est appliqué au résultat d’un appel de méthode qui retourne un `Task`, le `Await` expression ne retourne aucune valeur. L'exemple suivant illustre la différence.  
  
```vb  
' Await used with a method that returns a Task(Of TResult).  
Dim result As TResult = Await AsyncMethodThatReturnsTaskTResult()  
  
' Await used with a method that returns a Task.  
Await AsyncMethodThatReturnsTask()  
```  
  
 Un `Await` expression ou instruction ne bloque pas le thread sur lequel elle s’exécute. Au lieu de cela, il indique au compilateur de signer le reste de la méthode async, après le `Await` expression, comme une continuation sur la tâche attendue. Le contrôle revient alors à l'appelant de la méthode async. Quand la tâche est terminée, elle appelle sa continuation et l'exécution de la méthode async reprend là où elle s'était arrêtée.  
  
 Un `Await` expression peut se produire uniquement dans le corps d’une expression lambda ou de méthode immédiatement englobante qui est marquée par un `Async` modificateur. Le terme *Await* sert de mot clé uniquement dans ce contexte. Partout ailleurs, il est interprété en tant qu'identificateur. Dans l’expression lambda ou de la méthode async, un `Await` expression ne peut pas se produire dans une expression de requête, dans le `catch` ou `finally` de blocs à un [essayez... Catch... Enfin](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md) instruction, dans l’expression de variable de contrôle de boucle d’un `For` ou `For Each` boucle, ou dans le corps d’un [SyncLock](../../../visual-basic/language-reference/statements/synclock-statement.md) instruction.  
  
## <a name="exceptions"></a>Exceptions  
 La plupart des méthodes async retournent un <xref:System.Threading.Tasks.Task> ou <xref:System.Threading.Tasks.Task%601>. Les propriétés de la tâche retournée comportent des informations sur son état et son historique. Celles-ci indiquent notamment si la tâche est terminée ou non, si la méthode async a levé une exception ou a été annulée et quel est le résultat final. L'opérateur `Await` accède à ces propriétés.  
  
 Si vous attendez une méthode async retournant des tâches qui lève une exception, l'opérateur `Await` lève de nouveau l'exception.  
  
 Si vous attendez une méthode async retournant des tâches qui est annulée, le `Await` opérateur lève à nouveau une <xref:System.OperationCanceledException>.  
  
 Une tâche qui se trouve dans un état d’erreur peut refléter plusieurs exceptions.  Par exemple, la tâche peut être le résultat d'un appel à <xref:System.Threading.Tasks.Task.WhenAll%2A?displayProperty=nameWithType>. Quand vous attendez une telle tâche, l’opération await lève à nouveau une seule des exceptions. Toutefois, vous ne pouvez pas prédire laquelle de ces exceptions est de nouveau levée.  
  
 Pour obtenir des exemples de gestion des erreurs dans les méthodes async, consultez [essayez... Catch... Instruction finally](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md).  
  
## <a name="example"></a>Exemple  
 L'exemple Windows Forms suivant illustre l'utilisation de `Await` dans une méthode async, `WaitAsynchronouslyAsync`. Comparez le comportement de cette méthode avec celui de `WaitSynchronously`. Sans un `Await` opérateur, `WaitSynchronously` s’exécute de façon synchrone en dépit de l’utilisation de la `Async` modificateur dans sa définition et un appel à <xref:System.Threading.Thread.Sleep%2A?displayProperty=nameWithType> dans son corps.  
  
```vb  
Private Async Sub Button1_Click(sender As Object, e As EventArgs) Handles Button1.Click  
    ' Call the method that runs asynchronously.  
    Dim result As String = Await WaitAsynchronouslyAsync()  
  
    ' Call the method that runs synchronously.  
    'Dim result As String = Await WaitSynchronously()  
  
    ' Display the result.  
    TextBox1.Text &= result  
End Sub  
  
' The following method runs asynchronously. The UI thread is not  
' blocked during the delay. You can move or resize the Form1 window   
' while Task.Delay is running.  
Public Async Function WaitAsynchronouslyAsync() As Task(Of String)  
    Await Task.Delay(10000)  
    Return "Finished"  
End Function  
  
' The following method runs synchronously, despite the use of Async.  
' You cannot move or resize the Form1 window while Thread.Sleep  
' is running because the UI thread is blocked.  
Public Async Function WaitSynchronously() As Task(Of String)  
    ' Import System.Threading for the Sleep method.  
    Thread.Sleep(10000)  
    Return "Finished"  
End Function  
```  
  
## <a name="see-also"></a>Voir aussi

- [Programmation asynchrone avec Async et Await](../../../visual-basic/programming-guide/concepts/async/index.md)
- [Procédure pas à pas : Accès au web avec Async et Await](../../../visual-basic/programming-guide/concepts/async/walkthrough-accessing-the-web-by-using-async-and-await.md)
- [Async](../../../visual-basic/language-reference/modifiers/async.md)
