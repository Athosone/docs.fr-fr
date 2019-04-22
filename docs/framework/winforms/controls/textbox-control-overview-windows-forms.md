---
title: Vue d'ensemble du contrôle TextBox (Windows Forms)
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- TextBox
helpviewer_keywords:
- TextBox control [Windows Forms], about TextBox controls
- text boxes [Windows Forms], adding
ms.assetid: d1a9c7f5-fa53-480a-a75c-158f8649ea2f
ms.openlocfilehash: a91b67df1071c79707bb20a68efb4d5e6f083ae0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59162135"
---
# <a name="textbox-control-overview-windows-forms"></a>Vue d'ensemble du contrôle TextBox (Windows Forms)
Les zones de texte Windows Forms sont utilisés pour obtenir des données à partir de l’utilisateur ou pour afficher le texte. Le <xref:System.Windows.Forms.TextBox> contrôle est généralement utilisé pour le texte modifiable, bien qu’il peut également être en lecture seule. Zones de texte peuvent afficher plusieurs lignes, habiller le texte à la taille du contrôle et ajouter une mise en forme. Le <xref:System.Windows.Forms.TextBox> contrôle fournit un style de format unique pour le texte affiché ou entré dans le contrôle. Pour afficher plusieurs types de texte mis en forme, utilisez la <xref:System.Windows.Forms.RichTextBox> contrôle. Pour plus d’informations, consultez [vue d’ensemble du contrôle RichTextBox](richtextbox-control-overview-windows-forms.md).  
  
## <a name="working-with-the-textbox-control"></a>Utilisation du contrôle de zone de texte  
 Le texte affiché par le contrôle est contenu dans le <xref:System.Windows.Forms.TextBox.Text%2A> propriété. Par défaut, vous pouvez entrer jusqu'à 2 048 caractères dans une zone de texte. Si vous définissez la <xref:System.Windows.Forms.TextBox.Multiline%2A> propriété `true`, vous pouvez entrer jusqu'à 32 Ko de texte. Le <xref:System.Windows.Forms.TextBox.Text%2A> propriété peut être définie au moment du design avec la fenêtre Propriétés, au moment de l’exécution dans le code ou par l’utilisateur au moment de l’exécution. Le contenu actuel d’une zone de texte peut être récupéré au moment de l’exécution en lisant le <xref:System.Windows.Forms.TextBox.Text%2A> propriété.  
  
 L’exemple de code suivant définit le texte dans le contrôle au moment de l’exécution. Le `InitializeMyControl` procédure s’exécutera pas automatiquement ; il doit être appelé.  
  
```vb  
Private Sub InitializeMyControl()  
   ' Put some text into the control first.  
   TextBox1.Text = "This is a TextBox control."  
End Sub  
```  
  
```csharp  
private void InitializeMyControl() {  
   // Put some text into the control first.  
   textBox1.Text = "This is a TextBox control.";  
}  
```  
  
```cpp  
private:  
   void InitializeMyControl()  
   {  
      // Put some text into the control first.  
      textBox1->Text = "This is a TextBox control.";  
   }  
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.TextBox>
- [Guide pratique pour Contrôler le Point d’Insertion dans un contrôle de zone de texte Windows Forms](how-to-control-the-insertion-point-in-a-windows-forms-textbox-control.md)
- [Guide pratique pour Créer une zone de texte mot de passe avec le contrôle de zone de texte Windows Forms](how-to-create-a-password-text-box-with-the-windows-forms-textbox-control.md)
- [Guide pratique pour Créer une zone de texte en lecture seule](how-to-create-a-read-only-text-box-windows-forms.md)
- [Guide pratique pour Placez des guillemets doubles dans une chaîne](how-to-put-quotation-marks-in-a-string-windows-forms.md)
- [Guide pratique pour Sélectionner du texte dans le contrôle de zone de texte Windows Forms](how-to-select-text-in-the-windows-forms-textbox-control.md)
- [Guide pratique pour Afficher plusieurs lignes dans le contrôle de zone de texte Windows Forms](how-to-view-multiple-lines-in-the-windows-forms-textbox-control.md)
- [TextBox, contrôle](textbox-control-windows-forms.md)
