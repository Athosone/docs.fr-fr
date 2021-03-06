---
title: 'Procédure : accéder à des collections à clé dans Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- keyed collections [Windows Forms]
- collections [Windows Forms], accessing with keys
ms.assetid: b9b79b8b-d9bf-4f8c-b9d6-9578bc3219d3
ms.openlocfilehash: fdd3a56ab9a267990bb0e832c0d4cc2af9334034
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61801827"
---
# <a name="how-to-access-keyed-collections-in-windows-forms"></a>Procédure : accéder à des collections à clé dans Windows Forms
- Vous pouvez accéder à des éléments de collection individuels par clé. Cette fonctionnalité a été ajoutée à de nombreuses classes de collection sont généralement utilisées par les applications Windows Forms. La liste suivante présente certaines des classes de collection qui ont des collections à clé accessibles :  
  
- <xref:System.Windows.Forms.ListView.ListViewItemCollection>  
  
- <xref:System.Windows.Forms.ListViewItem.ListViewSubItemCollection>  
  
- <xref:System.Windows.Forms.Control.ControlCollection>  
  
- <xref:System.Windows.Forms.TabControl.TabPageCollection>  
  
- <xref:System.Windows.Forms.TreeNodeCollection>  
  
 La clé associée à un élément dans une collection est généralement le nom de l’élément. Les procédures suivantes vous montrent comment utiliser les classes de collection pour effectuer des tâches courantes.  
  
### <a name="to-find-and-give-focus-to-a-nested-control-in-a-control-collection"></a>Pour rechercher et de donner le focus à un contrôle imbriqué dans un regroupement de contrôle  
  
- Utilisez le <xref:System.Windows.Forms.Control.ControlCollection.Find%2A> et <xref:System.Windows.Forms.Control.Focus%2A> méthodes pour spécifier le nom du contrôle à rechercher et de donner le focus à.  
  
     [!code-csharp[System.Windows.Forms.KeyedCollectionsEx#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.KeyedCollectionsEx/CS/Form1.cs#1)]
     [!code-vb[System.Windows.Forms.KeyedCollectionsEx#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.KeyedCollectionsEx/VB/Form1.vb#1)]  
  
### <a name="to-access-an-image-in-an-image-collection"></a>Pour accéder à une image dans une collection d’images  
  
- Utilisez le <xref:System.Windows.Forms.ImageList.ImageCollection.Item%2A> propriété pour spécifier le nom de l’image que vous souhaitez accéder.  
  
     [!code-csharp[System.Windows.Forms.KeyedCollectionsEx#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.KeyedCollectionsEx/CS/Form1.cs#2)]
     [!code-vb[System.Windows.Forms.KeyedCollectionsEx#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.KeyedCollectionsEx/VB/Form1.vb#2)]  
  
### <a name="to-set-a-tab-page-as-the-selected-tab"></a>Pour définir une page d’onglets en tant que l’onglet sélectionné  
  
- Utilisez le <xref:System.Windows.Forms.TabControl.SelectedTab%2A> propriété avec le <xref:System.Windows.Forms.TabControl.TabPageCollection.Item%2A> propriété pour spécifier le nom de la page d’onglets à définir comme onglet sélectionné.  
  
     [!code-csharp[System.Windows.Forms.KeyedCollectionsEx#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.KeyedCollectionsEx/CS/Form1.cs#3)]
     [!code-vb[System.Windows.Forms.KeyedCollectionsEx#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.KeyedCollectionsEx/VB/Form1.vb#3)]  
  
## <a name="see-also"></a>Voir aussi

- [Bien démarrer avec Windows Forms](getting-started-with-windows-forms.md)
- [Guide pratique pour Ajouter ou supprimer des Images avec le composant ImageList Windows Forms](./controls/how-to-add-or-remove-images-with-the-windows-forms-imagelist-component.md)
