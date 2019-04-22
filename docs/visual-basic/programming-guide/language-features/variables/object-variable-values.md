---
title: Valeurs des variables objets (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- object variables [Visual Basic], values
- values [Visual Basic], of object variables
- data types [Visual Basic], object variable
- variables [Visual Basic], object
ms.assetid: 31555704-58a3-49f1-9a0a-6421f605664f
ms.openlocfilehash: c17c5f85952596f0a080ca473e8f792740e66b8f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58840391"
---
# <a name="object-variable-values-visual-basic"></a>Valeurs des variables objets (Visual Basic)
Une variable de la [Object Data Type](../../../../visual-basic/language-reference/data-types/object-data-type.md) peuvent faire référence à des données de n’importe quel type. La valeur que vous stockez dans un `Object` variable est conservée ailleurs en mémoire, tandis que la variable contient un pointeur vers les données.  
  
## <a name="object-classifier-functions"></a>Fonctions classifieur d’objets  
 Visual Basic fournit des fonctions qui retournent des informations sur ce qu’un `Object` variable fait référence, comme indiqué dans le tableau suivant.  
  
|Fonction|Retourne la valeur True si la variable objet fait référence à|  
|--------------|---------------------------------------------------|  
|<xref:Microsoft.VisualBasic.Information.IsArray%2A>|Un tableau de valeurs, plutôt qu’une seule valeur|  
|<xref:Microsoft.VisualBasic.Information.IsDate%2A>|Un [Type de données Date](../../../../visual-basic/language-reference/data-types/date-data-type.md) valeur, ou une chaîne qui peut être interprétée comme une valeur de date et d’heure|  
|<xref:Microsoft.VisualBasic.Information.IsDBNull%2A>|Un objet de type <xref:System.DBNull>, qui représente les données manquantes ou inexistantes|  
|<xref:Microsoft.VisualBasic.Information.IsError%2A>|Un objet d’exception qui dérive de <xref:System.Exception>|  
|<xref:Microsoft.VisualBasic.Information.IsNothing%2A>|[Nothing](../../../../visual-basic/language-reference/nothing.md), autrement dit, aucun objet n’est actuellement assigné à la variable|  
|<xref:Microsoft.VisualBasic.Information.IsNumeric%2A>|Un nombre ou une chaîne qui peut être interprétée comme un nombre|  
|<xref:Microsoft.VisualBasic.Information.IsReference%2A>|Un type référence (par exemple, une chaîne, un tableau, un délégué ou un type de classe)|  
  
 Vous pouvez utiliser ces fonctions pour éviter de soumettre une valeur non valide à une opération ou une procédure.  
  
## <a name="typeof-operator"></a>TypeOf, opérateur  
 Vous pouvez également utiliser le [TypeOf, opérateur](../../../../visual-basic/language-reference/operators/typeof-operator.md) pour déterminer si une variable objet fait actuellement référence à un type de données spécifique. Le `TypeOf`... `Is` expression prend la valeur `True` si le type au moment de l’exécution de l’opérande est dérivé ou implémente le type spécifié.  
  
 L’exemple suivant utilise `TypeOf` variables objets faisant référence à des types valeur et référence.  
  
```  
' The following statement puts a value type (Integer) in an Object variable.  
Dim num As Object = 10  
' The following statement puts a reference type (Form) in an Object variable.  
Dim frm As Object = New Form()  
If TypeOf num Is Long Then Debug.WriteLine("num is Long")  
If TypeOf num Is Integer Then Debug.WriteLine("num is Integer")  
If TypeOf num Is Short Then Debug.WriteLine("num is Short")  
If TypeOf num Is Object Then Debug.WriteLine("num is Object")  
If TypeOf frm Is Form Then Debug.WriteLine("frm is Form")  
If TypeOf frm Is Label Then Debug.WriteLine("frm is Label")  
If TypeOf frm Is Object Then Debug.WriteLine("frm is Object")  
```  
  
 L’exemple précédent écrit les lignes suivantes à la **déboguer** fenêtre :  
  
 `num is Integer`  
  
 `num is Object`  
  
 `frm is Form`  
  
 `frm is Object`  
  
 La variable objet `num` fait référence aux données de type `Integer`, et `frm` fait référence à un objet de classe <xref:System.Windows.Forms.Form>.  
  
## <a name="object-arrays"></a>Tableaux d’objets  
 Vous pouvez déclarer et utiliser un tableau de `Object` variables. Cela est utile lorsque vous avez besoin gérer une variété de types de données et des classes d’objets. Tous les éléments dans un tableau doivent avoir les mêmes données déclarées de type. Déclaration de ce type de données en tant que `Object` vous permet de stocker des objets et instances en même temps que d’autres types de données dans le tableau de la classe.  
  
## <a name="see-also"></a>Voir aussi

- [Variables objets](../../../../visual-basic/programming-guide/language-features/variables/object-variables.md)
- [Déclaration des variables objets](../../../../visual-basic/programming-guide/language-features/variables/object-variable-declaration.md)
- [Assignation des variables objets](../../../../visual-basic/programming-guide/language-features/variables/object-variable-assignment.md)
- [Guide pratique pour Reportez-vous à l’Instance actuelle d’un objet](../../../../visual-basic/programming-guide/language-features/variables/how-to-refer-to-the-current-instance-of-an-object.md)
- [Guide pratique pour Déterminer le Type désigné par une Variable objet](../../../../visual-basic/programming-guide/language-features/variables/how-to-determine-what-type-an-object-variable-refers-to.md)
- [Guide pratique pour Déterminer si deux objets sont liés](../../../../visual-basic/programming-guide/language-features/variables/how-to-determine-whether-two-objects-are-related.md)
- [Guide pratique pour Déterminer si deux objets sont identiques](../../../../visual-basic/programming-guide/language-features/variables/how-to-determine-whether-two-objects-are-identical.md)
- [Types de données](../../../../visual-basic/programming-guide/language-features/data-types/index.md)
