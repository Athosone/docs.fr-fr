---
title: Les arguments de type ne peuvent pas être déduits à partir du délégué
ms.date: 07/20/2015
f1_keywords:
- bc36564
- vbc36564
helpviewer_keywords:
- BC36564
ms.assetid: 21312807-e1cd-4ac1-ae1c-c28a9c25164d
ms.openlocfilehash: 1024cf6f2c1fa112db29cb710eef190a5022d3af
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58838597"
---
# <a name="type-arguments-could-not-be-inferred-from-the-delegate"></a>Les arguments de type ne peuvent pas être déduits à partir du délégué
Une instruction d’assignation utilise `AddressOf` pour assigner l’adresse d’une procédure générique à un délégué, mais elle ne fournit aucun argument de type à la procédure générique.  
  
 En général, lorsque vous appelez un type générique, vous fournissez un argument de type pour chaque paramètre de type défini par le type générique. Si vous ne fournissez pas d’arguments de type, le compilateur tente de déduire les types à passer aux paramètres de type. Si le contexte ne fournit pas au compilateur des informations suffisantes pour déduire les types, une erreur est générée.  
  
 **ID d’erreur :** BC36564  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Spécifiez les arguments de type pour la procédure générique dans l’expression `AddressOf` .  
  
## <a name="see-also"></a>Voir aussi

- [Generic Types in Visual Basic](../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)
- [AddressOf (opérateur)](../../../visual-basic/language-reference/operators/addressof-operator.md)
- [Generic Procedures in Visual Basic](../../../visual-basic/programming-guide/language-features/data-types/generic-procedures.md)
- [Liste de types](../../../visual-basic/language-reference/statements/type-list.md)
- [Méthodes d’extension](../../../visual-basic/programming-guide/language-features/procedures/extension-methods.md)
