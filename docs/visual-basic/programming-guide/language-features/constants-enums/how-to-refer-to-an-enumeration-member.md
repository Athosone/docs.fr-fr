---
title: 'Procédure : Faire référence à un membre d’énumération (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- enumerations [Visual Basic], referring to
- values [Visual Basic], associating constant values with names
- enumeration members
- constants [Visual Basic], enumerated
ms.assetid: bbb5c3cc-7cdb-4814-8d6a-a6d91546ed1e
ms.openlocfilehash: e9ea359d58dfa11f7bba7fec3d31955e18d24953
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61907593"
---
# <a name="how-to-refer-to-an-enumeration-member-visual-basic"></a>Procédure : Faire référence à un membre d’énumération (Visual Basic)
Les énumérations offrent un moyen pratique d’utiliser des ensembles de constantes connexes et d’associer des valeurs constantes avec des noms. Par exemple, vous pouvez déclarer une énumération pour un ensemble de constantes entières associées aux jours de la semaine puis utiliser les noms des jours au lieu de leur valeur entière dans votre code.  
  
 Vous pouvez éviter d’utiliser des noms qualifiés complets avec la `Imports` instruction. Pour plus d’informations, consultez [énumérations et Qualification de noms](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md).  
  
### <a name="to-refer-to-an-enumeration-member"></a>Pour faire référence à un membre d’énumération  
  
- Qualifier le nom du membre de l’énumération. Par exemple, l’exemple suivant affecte la `Saturday` membre de la `FirstDayOfWeek` énumération à la variable `DayValue`.  
  
     [!code-vb[VbEnumsTask#19](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#19)]  
  
## <a name="see-also"></a>Voir aussi

- [Guide pratique pour Déclarer une énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-enumerations.md)
- [Énumérations et qualification de noms](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md)
- [Guide pratique pour Parcourir une énumération dans Visual Basic](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-iterate-through-an-enumeration.md)
- [Guide pratique pour Déterminer la chaîne associée à une valeur d’énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-determine-the-string-associated-with-an-enumeration-value.md)
- [Quand utiliser une énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/when-to-use-an-enumeration.md)
