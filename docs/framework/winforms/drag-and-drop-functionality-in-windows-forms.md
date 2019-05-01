---
title: Fonctionnalité de glisser-déplacer dans les Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- drag and drop [Windows Forms], Windows Forms
- Windows Forms, drag and drop
ms.assetid: 65cd2c03-8782-474e-b958-cbe43eeb902c
ms.openlocfilehash: 437b632706b27cd487d60c2ad23db3f9a3c96c09
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61966855"
---
# <a name="drag-and-drop-functionality-in-windows-forms"></a>Fonctionnalité de glisser-déplacer dans les Windows Forms
Windows Forms comprend un ensemble de méthodes, événements et classes qui implémentent le comportement de glisser-déposer. Cette rubrique offre une vue d’ensemble de la prise en charge du glisser-déposer dans Windows Forms.  Consultez également [les opérations de glisser-déplacer et prise en charge du Presse-papiers](./advanced/drag-and-drop-operations-and-clipboard-support.md).  
  
## <a name="performing-drag-and-drop-operations"></a>Exécution d’opérations de glisser-déposer  
 Pour effectuer une opération de glisser-déposer, utilisez la méthode <xref:System.Windows.Forms.Control.DoDragDrop%2A> de la classe <xref:System.Windows.Forms.Control>. Pour plus d'informations sur la façon d'exécuter une opération de glisser-déplacer, consultez <xref:System.Windows.Forms.Control.DoDragDrop%2A>. Pour obtenir le rectangle sur lequel le pointeur de la souris doit être déplacé pour qu'une opération de glisser-déplacer commence, utilisez la propriété <xref:System.Windows.Forms.SystemInformation.DragSize%2A> de la classe <xref:System.Windows.Forms.SystemInformation>.  
  
## <a name="events-related-to-drag-and-drop-operations"></a>Événements liés aux opérations de glisser-déposer  
 Il existe deux catégories d'événements dans une opération de glisser-déplacer : les événements qui se produisent sur la cible actuelle de l'opération de glisser-déplacer et ceux qui se produisent sur la source de l'opération de glisser-déplacer.  
  
### <a name="events-on-the-current-target"></a>Événements sur la cible actuelle  
 Le tableau suivant présente les événements qui se produisent sur la cible actuelle d'une opération de glisser-déplacer.  
  
|Événement de souris|Description|  
|-----------------|-----------------|  
|<xref:System.Windows.Forms.Control.DragEnter>|Cet événement se produit quand un objet est déplacé dans les limites d'un contrôle. Le gestionnaire pour cet événement reçoit un argument de type <xref:System.Windows.Forms.DragEventArgs>.|  
|<xref:System.Windows.Forms.Control.DragOver>|Cet événement se produit quand un objet est déplacé alors que le pointeur de la souris se trouve dans les limites du contrôle. Le gestionnaire pour cet événement reçoit un argument de type <xref:System.Windows.Forms.DragEventArgs>.|  
|<xref:System.Windows.Forms.Control.DragDrop>|Cet événement se produit quand une opération de glisser-déplacer est terminée. Le gestionnaire pour cet événement reçoit un argument de type <xref:System.Windows.Forms.DragEventArgs>.|  
|<xref:System.Windows.Forms.Control.DragLeave>|Cet événement se produit quand un objet est déplacé hors des limites d'un contrôle. Le gestionnaire pour cet événement reçoit un argument de type <xref:System.EventArgs>.|  
  
 La classe <xref:System.Windows.Forms.DragEventArgs> fournit l'emplacement du pointeur de la souris, l'état actuel des boutons de la souris et des touches de modification du clavier, les données déplacées et des valeurs <xref:System.Windows.Forms.DragDropEffects> qui spécifient les opérations autorisées par la source de l'événement de glisser et l'effet de déplacement cible pour cette opération.  
  
### <a name="events-on-the-source"></a>Événements sur la source  
 Le tableau suivant présente les événements qui se produisent sur la source de l’opération de glisser-déposer.  
  
|Événement de souris|Description|  
|-----------------|-----------------|  
|<xref:System.Windows.Forms.Control.GiveFeedback>|Cet événement se produit pendant une opération glisser. Il permet de fournir une aide visuelle à l’utilisateur (par exemple la modification du pointeur de souris) pour signaler que l’opération de glisser-déplacer est en cours. Le gestionnaire pour cet événement reçoit un argument de type <xref:System.Windows.Forms.GiveFeedbackEventArgs>.|  
|<xref:System.Windows.Forms.Control.QueryContinueDrag>|Cet événement se produit pendant une opération de glisser-déposer et permet à la source de cette opération de déterminer si l’opération doit être annulée. Le gestionnaire pour cet événement reçoit un argument de type <xref:System.Windows.Forms.QueryContinueDragEventArgs>.|  
  
 La classe <xref:System.Windows.Forms.QueryContinueDragEventArgs> fournit l'état actuel des boutons de la souris et des touches de modification du clavier, une valeur indiquant si la touche Échappement a été enfoncée et une valeur <xref:System.Windows.Forms.DragAction> qui peut être définie pour spécifier si l'opération de glisser-déplacer doit continuer.  
  
## <a name="see-also"></a>Voir aussi

- [Entrée de la souris dans une application Windows Forms](mouse-input-in-a-windows-forms-application.md)
