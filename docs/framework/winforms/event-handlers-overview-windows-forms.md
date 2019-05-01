---
title: Vue d'ensemble des gestionnaires d'événements (Windows Forms)
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Windows Forms, event handling
- event handling [Windows Forms], Windows Forms
- event handlers [Windows Forms], about event handlers
ms.assetid: 228112e1-1711-42ee-8ffa-ff3555bffe66
ms.openlocfilehash: 05acbfaf427060d015c2445360a7d73ebe97d070
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61966827"
---
# <a name="event-handlers-overview-windows-forms"></a><span data-ttu-id="05fee-102">Vue d'ensemble des gestionnaires d'événements (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="05fee-102">Event Handlers Overview (Windows Forms)</span></span>
<span data-ttu-id="05fee-103">Un gestionnaire d’événements est une méthode qui est liée à un événement.</span><span class="sxs-lookup"><span data-stu-id="05fee-103">An event handler is a method that is bound to an event.</span></span> <span data-ttu-id="05fee-104">Lorsque l’événement est déclenché, le code dans le Gestionnaire d’événements est exécuté.</span><span class="sxs-lookup"><span data-stu-id="05fee-104">When the event is raised, the code within the event handler is executed.</span></span> <span data-ttu-id="05fee-105">Chaque gestionnaire d’événements fournit deux paramètres qui vous permettent de gérer l’événement correctement.</span><span class="sxs-lookup"><span data-stu-id="05fee-105">Each event handler provides two parameters that allow you to handle the event properly.</span></span> <span data-ttu-id="05fee-106">L’exemple suivant montre un gestionnaire d’événements pour un <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Click> événement.</span><span class="sxs-lookup"><span data-stu-id="05fee-106">The following example shows an event handler for a <xref:System.Windows.Forms.Button> control's <xref:System.Windows.Forms.Control.Click> event.</span></span>  
  
```vb  
Private Sub button1_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles button1.Click  
  
End Sub  
```  
  
```csharp  
private void button1_Click(object sender, System.EventArgs e)   
{  
  
}  
```  
  
```cpp  
private:  
  void button1_Click(System::Object ^ sender,  
    System::EventArgs ^ e)  
  {  
  
  }  
```  
  
 <span data-ttu-id="05fee-107">Le premier paramètre,`sender`, fournit une référence à l’objet qui a déclenché l’événement.</span><span class="sxs-lookup"><span data-stu-id="05fee-107">The first parameter,`sender`, provides a reference to the object that raised the event.</span></span> <span data-ttu-id="05fee-108">Le deuxième paramètre, `e`, dans l’exemple ci-dessus, passe un objet spécifique à l’événement qui est géré.</span><span class="sxs-lookup"><span data-stu-id="05fee-108">The second parameter, `e`, in the example above, passes an object specific to the event that is being handled.</span></span> <span data-ttu-id="05fee-109">En référençant les propriétés de l’objet (et, parfois, ses méthodes), vous pouvez obtenir des informations telles que l’emplacement de la souris pour les événements de souris ou les données transférées dans les événements de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="05fee-109">By referencing the object's properties (and, sometimes, its methods), you can obtain information such as the location of the mouse for mouse events or data being transferred in drag-and-drop events.</span></span>  
  
 <span data-ttu-id="05fee-110">En général, chaque événement produit un gestionnaire d’événements avec un type d’objet d’événement différentes pour le deuxième paramètre.</span><span class="sxs-lookup"><span data-stu-id="05fee-110">Typically each event produces an event handler with a different event-object type for the second parameter.</span></span> <span data-ttu-id="05fee-111">Certains gestionnaires d’événements, telles que celles pour le <xref:System.Windows.Forms.Control.MouseDown> et <xref:System.Windows.Forms.Control.MouseUp> événements, ont le même type d’objet pour le second paramètre.</span><span class="sxs-lookup"><span data-stu-id="05fee-111">Some event handlers, such as those for the <xref:System.Windows.Forms.Control.MouseDown> and <xref:System.Windows.Forms.Control.MouseUp> events, have the same object type for their second parameter.</span></span> <span data-ttu-id="05fee-112">Pour ces types d’événements, vous pouvez utiliser le même gestionnaire d’événements pour gérer les deux événements.</span><span class="sxs-lookup"><span data-stu-id="05fee-112">For these types of events, you can use the same event handler to handle both events.</span></span>  
  
 <span data-ttu-id="05fee-113">Vous pouvez également utiliser le même gestionnaire d’événements pour gérer l’événement de même pour les différents contrôles.</span><span class="sxs-lookup"><span data-stu-id="05fee-113">You can also use the same event handler to handle the same event for different controls.</span></span> <span data-ttu-id="05fee-114">Par exemple, si vous disposez d’un groupe de <xref:System.Windows.Forms.RadioButton> contrôles sur un formulaire, vous pouvez créer un gestionnaire d’événements unique pour le <xref:System.Windows.Forms.Control.Click> événement et avoir de chaque contrôle <xref:System.Windows.Forms.Control.Click> événement lié au gestionnaire d’événements unique.</span><span class="sxs-lookup"><span data-stu-id="05fee-114">For example, if you have a group of <xref:System.Windows.Forms.RadioButton> controls on a form, you could create a single event handler for the <xref:System.Windows.Forms.Control.Click> event and have each control's <xref:System.Windows.Forms.Control.Click> event bound to the single event handler.</span></span> <span data-ttu-id="05fee-115">Pour plus d'informations, voir [Procédure : Connecter plusieurs événements à un seul gestionnaire d’événements dans les Windows Forms](how-to-connect-multiple-events-to-a-single-event-handler-in-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="05fee-115">For more information, see [How to: Connect Multiple Events to a Single Event Handler in Windows Forms](how-to-connect-multiple-events-to-a-single-event-handler-in-windows-forms.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="05fee-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05fee-116">See also</span></span>

- [<span data-ttu-id="05fee-117">Création de gestionnaires d’événements dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="05fee-117">Creating Event Handlers in Windows Forms</span></span>](creating-event-handlers-in-windows-forms.md)
- [<span data-ttu-id="05fee-118">Vue d'ensemble des événements</span><span class="sxs-lookup"><span data-stu-id="05fee-118">Events Overview</span></span>](events-overview-windows-forms.md)
