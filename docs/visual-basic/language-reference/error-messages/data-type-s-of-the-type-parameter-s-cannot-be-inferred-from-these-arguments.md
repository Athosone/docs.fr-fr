---
title: Impossible de déduire le ou les types de données du ou des paramètres de type à partir de ces arguments
ms.date: 07/20/2015
f1_keywords:
- bc36644
- bc36647
- vbc36647
- vbc36644
helpviewer_keywords:
- BC36644
- BC36647
ms.assetid: 0e0050f2-2039-4311-b260-f0ebfde84189
ms.openlocfilehash: 91ee4bf9242df822890b0a171061f375a3b24cbc
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58828002"
---
# <a name="data-types-of-the-type-parameters-cannot-be-inferred-from-these-arguments"></a>Impossible de déduire le ou les types de données du ou des paramètres de type à partir de ces arguments
Impossible de déduire l’ou les types de données des paramètres de type à partir de ces arguments. La spécification explicite du ou des types de données peut permettre de corriger cette erreur.  
  
 Cette erreur se produit quand la résolution de surcharge a échoué. Elle entraîne l’affichage d’un message subordonné qui indique pourquoi un candidat de surcharge particulier a été éliminé. Le message d’erreur explique que le compilateur ne peut pas utiliser l’inférence de type pour rechercher des types de données pour les paramètres de type.  
  
> [!NOTE]
>  Quand la spécification des arguments n’est pas une option (par exemple, pour les opérateurs de requête dans les expressions de requête), le message d’erreur apparaît sans la deuxième phrase.  
  
 Le code suivant illustre cette erreur.  
  
```vb  
Module Module1  
  
    Sub Main()  
  
        '' Not Valid.  
        'OverloadedGenericMethod("Hello", "World")  
  
    End Sub  
  
    Sub OverloadedGenericMethod(Of T)(ByVal x As String,   
                                      ByVal y As InterfaceExample(Of T))  
    End Sub  
  
    Sub OverloadedGenericMethod(Of T, R)(ByVal x As T,   
                                         ByVal y As InterfaceExample(Of R))  
    End Sub  
  
End Module  
  
Interface InterfaceExample(Of T)  
End Interface  
```  
  
 **ID d’erreur :** BC36647 and BC36644  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Vous pourrez peut-être spécifier un type de données pour le ou les paramètres de type au lieu de compter sur l’inférence de type.  
  
## <a name="see-also"></a>Voir aussi

- [Conversion simplifiée des délégués](../../../visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion.md)
- [Generic Procedures in Visual Basic](../../../visual-basic/programming-guide/language-features/data-types/generic-procedures.md)
- [Conversions de type en Visual Basic](../../../visual-basic/programming-guide/language-features/data-types/type-conversions.md)
