---
title: Les paramètres de type ne peuvent pas être utilisés comme qualificateurs
ms.date: 07/20/2015
f1_keywords:
- vbc32098
- bc32098
helpviewer_keywords:
- BC32098
ms.assetid: bab05325-dde8-4621-a5f6-368b5b7b2d76
ms.openlocfilehash: ba7348ae50965ffcf2719b20934451916c8fa95a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59296353"
---
# <a name="type-parameters-cannot-be-used-as-qualifiers"></a>Les paramètres de type ne peuvent pas être utilisés comme qualificateurs
Un élément de programmation est qualifié avec une chaîne de qualification qui inclut un paramètre de type.  
  
 Un paramètre de type représente une exigence pour un type qui doit être fourni lorsque le type générique est construit. Il ne représente pas un type défini spécifique. Une chaîne de qualification doit inclure uniquement les éléments qui sont définis au moment de la compilation.  
  
 Les instructions suivantes peuvent générer cette erreur.  
  
```  
Public Function checkText(Of c As System.Windows.Forms.Control)(  
    ByVal badText As String) As Boolean  
  
    Dim saveText As c.Text  
    ' Insert code to look for badText within saveText.  
End Function  
```  
  
 **ID d’erreur :** BC32098  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Supprimez le paramètre de type de la chaîne de qualification ou remplacez-le par un type défini.  
  
2. Si vous devez utiliser un type construit pour rechercher l’élément de programmation ne soient pas qualifiée, vous devez utiliser la logique de programme supplémentaire.  
  
## <a name="see-also"></a>Voir aussi

- [Références aux éléments déclarés](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)
- [Generic Types in Visual Basic](../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)
- [Liste de types](../../../visual-basic/language-reference/statements/type-list.md)
