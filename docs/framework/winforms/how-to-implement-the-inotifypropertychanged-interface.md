---
title: 'Procédure : implémenter l’interface INotifyPropertyChanged'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- INotifyPropertyChanged interface [Windows Forms], implementing
ms.assetid: eac428af-b43b-46ac-80d9-1a5f88658725
ms.openlocfilehash: cfdfb22fd854a8f630243e0f612761c71cb778d8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59225597"
---
# <a name="how-to-implement-the-inotifypropertychanged-interface"></a>Procédure : implémenter l’interface INotifyPropertyChanged
L’exemple de code suivant montre comment implémenter la <xref:System.ComponentModel.INotifyPropertyChanged> interface. Implémentez cette interface sur les objets métier qui sont utilisés dans la liaison de données Windows Forms. En cas d’implémentation, l’interface communique à un contrôle dépendant les modifications des propriétés sur un objet métier.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[System.ComponentModel.IPropertyChangeExample#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.IPropertyChangeExample/CS/Form1.cs#1)]
 [!code-vb[System.ComponentModel.IPropertyChangeExample#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.IPropertyChangeExample/VB/Form1.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- [Guide pratique pour Appliquer le modèle PropertyNameChanged](how-to-apply-the-propertynamechanged-pattern.md)
- [Liaison de données Windows Forms](windows-forms-data-binding.md)
- [Guide pratique pour Générer des Notifications de modification à l’aide d’un BindingSource et l’Interface INotifyPropertyChanged](./controls/raise-change-notifications--bindingsource.md)
- [Notification de modifications dans la liaison de données Windows Forms](change-notification-in-windows-forms-data-binding.md)
