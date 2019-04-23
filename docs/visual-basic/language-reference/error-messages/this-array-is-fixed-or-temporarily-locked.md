---
title: Ce tableau est prédéfini ou est temporairement verrouillé (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vbrID10
ms.assetid: de6713a6-51d7-4edb-8515-d5fb544e2091
ms.openlocfilehash: c74d9524ff64101ba6002e133b93c9b80e8f50a9
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59337966"
---
# <a name="this-array-is-fixed-or-temporarily-locked-visual-basic"></a>Ce tableau est prédéfini ou est temporairement verrouillé (Visual Basic)
Cette erreur a les causes possibles suivantes :  
  
-   À l’aide de `ReDim` pour modifier le nombre d’éléments d’un tableau de taille fixe.  
  
-   Redimensionnement d’un tableau dynamique au niveau du module, dans lequel un élément a été passé en tant qu’argument à une procédure. Si un élément est passé, le tableau est verrouillé pour empêcher la désallocation de mémoire pour le paramètre de référence dans la procédure.  
  
-   Tentative d’assigner une valeur à un `Variant` variable contenant un tableau, mais la `Variant` est actuellement verrouillé.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Rendre le tableau d’origine dynamique non fixe en le déclarant avec `ReDim` (si le tableau est déclaré dans une procédure), ou en le déclarant sans spécifier le nombre d’éléments (si le tableau est déclaré au niveau du module.  
  
2. Déterminer s’il faut vraiment transmettre l’élément, dans la mesure où il est visible dans toutes les procédures dans le module.  
  
3. Déterminez ce qui verrouille le `Variant` et y remédier.  
  
## <a name="see-also"></a>Voir aussi

- [Tableaux](../../../visual-basic/programming-guide/language-features/arrays/index.md)
