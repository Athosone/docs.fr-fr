---
title: 'Procédure : Déclarer et appeler une propriété par défaut en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- defaults [Visual Basic], properties
- properties [Visual Basic], default
- procedures [Visual Basic], defining
- default properties [Visual Basic], in Visual Basic
- Visual Basic code, procedures
- Visual Basic code, properties
- default properties
ms.assetid: 68b4026e-09ef-4613-808e-f6287494ff63
ms.openlocfilehash: 9ca9a0ccdac3ac13429928233a0c09d58427ce74
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61665765"
---
# <a name="how-to-declare-and-call-a-default-property-in-visual-basic"></a>Procédure : Déclarer et appeler une propriété par défaut en Visual Basic
Un *propriété par défaut* est une propriété de classe ou structure auquel votre code peut accéder sans la spécifier. Lors de l’appel des noms de code, une classe ou structure, mais pas une propriété et le contexte autorise l’accès à une propriété, Visual Basic résout l’accès à cette classe ou propriété par défaut de la structure s’il en existe.  
  
 Une classe ou structure peut avoir au plus une propriété par défaut. Toutefois, vous pouvez surcharger une propriété par défaut et avoir plusieurs versions de celui-ci.  
  
 Pour plus d’informations, consultez [par défaut](../../../../visual-basic/language-reference/modifiers/default.md).  
  
### <a name="to-declare-a-default-property"></a>Pour déclarer une propriété par défaut  
  
1. Déclarez la propriété de façon normale. Ne spécifiez pas le `Shared` ou `Private` mot clé.  
  
2. Inclure le `Default` mot clé dans la déclaration de propriété.  
  
3. Spécifiez au moins un paramètre pour la propriété. Vous ne pouvez pas définir une propriété par défaut qui n’accepte pas d’au moins un argument.  
  
     [!code-vb[VbVbcnProcedures#17](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#17)]  
  
### <a name="to-call-a-default-property"></a>Pour appeler une propriété par défaut  
  
1. Déclarez une variable du type de classe ou la structure conteneur.  
  
     [!code-vb[VbVbcnProcedures#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#16)]  
  
2. Utilisez le nom de variable seul dans une expression où vous inclurez normalement le nom de propriété.  
  
     [!code-vb[VbVbcnProcedures#21](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#21)]  
  
3. Suivez le nom de variable avec une liste d’arguments entre parenthèses. Une propriété par défaut doit prendre au moins un argument.  
  
     [!code-vb[VbVbcnProcedures#20](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#20)]  
  
4. Pour récupérer la valeur de propriété par défaut, utilisez le nom de variable avec une liste d’arguments dans une expression ou après l’égal (`=`) connectez-vous à une instruction d’assignation.  
  
     [!code-vb[VbVbcnProcedures#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#15)]  
  
5. Pour définir la valeur de propriété par défaut, utilisez le nom de variable avec une liste d’arguments, sur le côté gauche d’une instruction d’assignation.  
  
     [!code-vb[VbVbcnProcedures#14](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#14)]  
  
6. Vous pouvez toujours spécifier le nom de propriété par défaut avec le nom de variable, comme vous le feriez pour accéder à n’importe quelle autre propriété.  
  
     [!code-vb[VbVbcnProcedures#19](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#19)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant déclare une propriété par défaut sur une classe.  
  
 [!code-vb[VbVbcnProcedures#12](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#12)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment appeler la propriété par défaut `myProperty` sur la classe `class1`. Stockent des valeurs dans les trois instructions d’assignation `myProperty`et le <xref:Microsoft.VisualBasic.Interaction.MsgBox%2A> appel lit les valeurs.  
  
 [!code-vb[VbVbcnProcedures#13](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#13)]  
  
 L’utilisation la plus courante d’une propriété par défaut est le <xref:Microsoft.VisualBasic.Collection.Item%2A> propriété sur différentes classes de collection.  
  
## <a name="robust-programming"></a>Programmation fiable  
 Propriétés par défaut peuvent entraîner une légère réduction dans les caractères de code source, mais ils peuvent rendre votre code plus difficile à lire. Si le code appelant n’est pas familiarisé avec votre classe ou structure, lorsqu’il fait référence au nom de classe ou structure il ne peut pas être certains que cette référence accède à la classe ou structure lui-même ou une propriété par défaut. Cela peut entraîner des erreurs du compilateur ou des erreurs de logique d’exécution subtiles.  
  
 Vous pouvez légèrement réduire les risques d’erreurs de propriété par défaut en utilisant toujours la [Option Strict, instruction](../../../../visual-basic/language-reference/statements/option-strict-statement.md) pour définir le contrôle de type du compilateur `On`.  
  
 Si vous envisagez d’utiliser une classe prédéfinie ou une structure dans votre code, vous devez déterminer s’il possède une propriété par défaut et si c’est le cas, ce que son nom est.  
  
 En raison de ces inconvénients, vous devez envisager de ne pas définir les propriétés par défaut. Pour la lisibilité du code, vous devez également envisager de toujours faire explicitement référence à toutes les propriétés, même les propriétés par défaut.  
  
## <a name="see-also"></a>Voir aussi

- [Procédures de propriété](./property-procedures.md)
- [Paramètres et arguments d’une procédure](./procedure-parameters-and-arguments.md)
- [Property (instruction)](../../../../visual-basic/language-reference/statements/property-statement.md)
- [Default](../../../../visual-basic/language-reference/modifiers/default.md)
- [Différences entre les propriétés et les Variables en Visual Basic](./differences-between-properties-and-variables.md)
- [Guide pratique pour Créer une propriété](./how-to-create-a-property.md)
- [Guide pratique pour Déclarer une propriété avec des niveaux d’accès mixtes](./how-to-declare-a-property-with-mixed-access-levels.md)
- [Guide pratique pour Appeler une procédure de propriété](./how-to-call-a-property-procedure.md)
- [Guide pratique pour Placer une valeur dans une propriété](./how-to-put-a-value-in-a-property.md)
- [Guide pratique pour Obtenir une valeur d’une propriété](./how-to-get-a-value-from-a-property.md)
