---
title: RaiseEvent, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.RaiseEventMethod
- vb.RaiseEvent
- RaiseEvent
helpviewer_keywords:
- raising events [Visual Basic], RaiseEvent statement
- RaiseEvent statement [Visual Basic]
- event handlers, connecting events to
ms.assetid: f82e380a-1e6b-4047-bea8-c853f4d2c742
ms.openlocfilehash: 5d8fd6adf33c992341324e07bcd2ad12986bbdf2
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58821008"
---
# <a name="raiseevent-statement"></a>RaiseEvent, instruction
Déclenche un événement déclaré au niveau du module dans une classe, un formulaire ou un document.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
RaiseEvent eventname[( argumentlist )]  
```  
  
## <a name="parts"></a>Composants  
 `eventname`  
 Obligatoire. Nom de l’événement à déclencher.  
  
 `argumentlist`  
 Optionnel. Liste délimitée par des virgules de variables, des tableaux ou des expressions. Le `argumentlist` argument doit être mis entre parenthèses. S’il n’y a pas d’arguments, les parenthèses doivent être omis.  
  
## <a name="remarks"></a>Notes  
 Requis `eventname` est le nom d’un événement déclaré dans le module. Il suit les conventions d’affectation de noms variable Visual Basic.  
  
 Si l’événement n’a pas été déclaré dans le module dans lequel il est déclenché, une erreur se produit. Le fragment de code suivant illustre une déclaration d’événement et d’une procédure dans laquelle l’événement est déclenché.  
  
 [!code-vb[VbVbalrEvents#37](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrEvents/VB/Class1.vb#37)]  
  
 Vous ne pouvez pas utiliser `RaiseEvent` pour déclencher des événements qui ne sont pas explicitement déclarés dans le module. Par exemple, tous les formulaires héritent un <xref:System.Windows.Forms.Control.Click> événement à partir de <xref:System.Windows.Forms.Form?displayProperty=nameWithType>, il ne peut pas être déclenché à l’aide de `RaiseEvent` dans un formulaire dérivé. Si vous déclarez un `Click` événement dans le module du formulaire, elle occulte du formulaire propre <xref:System.Windows.Forms.Control.Click> événement. Vous pouvez toujours appeler le formulaire <xref:System.Windows.Forms.Control.Click> événement en appelant le <xref:System.Windows.Forms.Control.OnClick%2A> (méthode).  
  
 Par défaut, un événement défini dans Visual Basic déclenche ses gestionnaires d’événements dans l’ordre que les connexions sont établies. Étant donné que les événements peuvent disposer de `ByRef` paramètres, un processus qui se connecte ultérieurement peut recevoir des paramètres qui ont été modifiés par un gestionnaire d’événements précédent. Une fois que les gestionnaires d’événements est exécuté, le contrôle est retourné à la sous-routine qui a déclenché l’événement.  
  
> [!NOTE]
>  Les événements non partagés ne doivent pas être déclenchés dans le constructeur de la classe dans laquelle ils sont déclarés. Bien que ces événements ne provoquent pas d’erreurs d’exécution, ceux-ci peuvent ne pas être interceptée par les gestionnaires d’événements associés. Utilisez le `Shared` modificateur pour créer un événement partagé Si vous avez besoin de déclencher un événement à partir d’un constructeur.  
  
> [!NOTE]
>  Vous pouvez modifier le comportement par défaut des événements en définissant un événement personnalisé. Pour les événements personnalisés, le `RaiseEvent` instruction appelle de l’événement `RaiseEvent` accesseur. Pour plus d’informations sur les événements personnalisés, consultez [Event, instruction](../../../visual-basic/language-reference/statements/event-statement.md).  
  
## <a name="example"></a>Exemple  
 L'exemple suivant utilise des événements pour décompter les secondes de 10 à 0. Le code illustre plusieurs méthodes liées aux événements, des propriétés et des instructions, y compris la `RaiseEvent` instruction.  
  
 La classe qui déclenche un événement est la source de l'événement, et les méthodes qui traitent l'événement sont les gestionnaires d'événements. Une source d'événement peut avoir plusieurs gestionnaires pour les événements qu'elle génère. Quand la classe déclenche l'événement, celui-ci se produit pour chaque classe ayant choisi de gérer les événements pour cette instance de l'objet.  
  
 L'exemple utilise également un formulaire (`Form1`) avec un bouton (`Button1`) et une zone de texte (`TextBox1`). Quand vous cliquez sur le bouton, la première zone de texte affiche un compte à rebours de 10 à 0 secondes. Quand la durée totale (10 secondes) s'est écoulée, la première zone de texte affiche « Terminé ».  
  
 Le code correspondant à `Form1` indique les états de début et de fin du formulaire. Il contient également le code exécuté lors du déclenchement des événements.  
  
 Pour utiliser cet exemple, ouvrez un nouveau projet d’Application de Windows, ajoutez un bouton nommé `Button1` et une zone de texte nommée `TextBox1` au formulaire principal, nommé `Form1`. Avec le bouton droit de la forme, puis cliquez sur **afficher le Code** pour ouvrir l’éditeur de Code.  
  
 Ajouter un `WithEvents` à la section des déclarations de variable le `Form1` classe.  
  
 [!code-vb[VbVbalrEvents#14](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrEvents/VB/Class1.vb#14)]  
  
## <a name="example"></a>Exemple  
 Ajoutez le code suivant au code pour `Form1`. Remplacez toute procédure en double qui peut-être exister, telles que `Form_Load`, ou `Button_Click`.  
  
 [!code-vb[VbVbalrEvents#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrEvents/VB/Class1.vb#15)]  
  
 Appuyez sur F5 pour exécuter l’exemple précédent, puis cliquez sur le bouton intitulé **Démarrer**. La première zone de texte commence à décompter les secondes. Quand la durée totale (10 secondes) s'est écoulée, la première zone de texte affiche « Terminé ».  
  
> [!NOTE]
>  Le `My.Application.DoEvents` méthode ne traite pas les événements de la même façon que le formulaire. Pour permettre au formulaire gérer les événements directement, vous pouvez utiliser le multithreading. Pour plus d’informations, consultez [Managed Threading](../../../standard/threading/index.md).  
  
## <a name="see-also"></a>Voir aussi

- [Événements](../../../visual-basic/programming-guide/language-features/events/index.md)
- [Event (instruction)](../../../visual-basic/language-reference/statements/event-statement.md)
- [AddHandler (instruction)](../../../visual-basic/language-reference/statements/addhandler-statement.md)
- [RemoveHandler (instruction)](../../../visual-basic/language-reference/statements/removehandler-statement.md)
- [Handles](../../../visual-basic/language-reference/statements/handles-clause.md)
