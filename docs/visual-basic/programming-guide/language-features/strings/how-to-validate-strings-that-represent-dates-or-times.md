---
title: 'Procédure : Valider des chaînes qui représentent des Dates ou des heures (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], validating
- String data type [Visual Basic], validation
ms.assetid: ae7d4b29-3436-4032-bdbf-4650eb1c8e19
ms.openlocfilehash: f24ff05e48327c21c02eb92b07db17266f743a80
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58815228"
---
# <a name="how-to-validate-strings-that-represent-dates-or-times-visual-basic"></a>Procédure : Valider des chaînes qui représentent des Dates ou des heures (Visual Basic)
Le code suivant exemple définit un `Boolean` valeur qui indique si une chaîne représente une date ou heure valide.  
  
## <a name="example"></a>Exemple  
 [!code-vb[VbVbcnRegEx#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnRegEx/VB/Class1.vb#2)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Remplacez `("01/01/03")` et `"9:30 PM"` avec la date et l’heure que vous souhaitez valider. Vous pouvez remplacer la chaîne par une autre chaîne codée en dur, avec un `String` variable, ou avec une méthode qui retourne une chaîne, tel que `InputBox`.  
  
## <a name="robust-programming"></a>Programmation fiable  
 Utilisez cette méthode pour valider la chaîne avant d’essayer de convertir le `String` à un `DateTime` variable. En vérifiant la date ou heure tout d’abord, vous pouvez éviter de générer une exception au moment de l’exécution.  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.Information.IsDate%2A>
- <xref:Microsoft.VisualBasic.Interaction.InputBox%2A>
- [Validation de chaînes en Visual Basic](../../../../visual-basic/programming-guide/language-features/strings/validating-strings.md)
