---
title: 'Procédure : désactiver des onglets'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- tab pages [Windows Forms], hiding in forms
- TabControl control [Windows Forms], disabling pages
ms.assetid: adcc6618-8a34-4ee1-bbe3-47e732de6a59
ms.openlocfilehash: 21592fdd74c43d40310e0fcbc96af6565a42e08b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62013450"
---
# <a name="how-to-disable-tab-pages"></a>Procédure : désactiver des onglets
Dans certains cas, vous souhaitez restreindre l’accès aux données qui sont disponibles dans votre application Windows Forms. Un exemple de ce pourrait être lorsque vous avez des données affichées dans les pages d’onglets d’un contrôle onglet. les administrateurs peut avoir plus d’informations sur une page d’onglets que vous souhaitez restreindre l’invité ou des utilisateurs de niveau inférieur.  
  
### <a name="to-disable-tab-pages-programmatically"></a>Pour désactiver les pages d’onglets par programmation  
  
1. Écrire du code pour gérer le contrôle onglet <xref:System.Windows.Forms.TabControl.SelectedIndexChanged> événement. Il s’agit de l’événement est déclenché lorsque l’utilisateur bascule d’un onglet à l’autre.  
  
2. Vérifiez les informations d’identification. Selon les informations présentées, vous voudrez vérifier l’utilisateur a ouvert une session avec le nom d’utilisateur ou une autre forme d’informations d’identification avant d’autoriser l’utilisateur d’afficher l’onglet.  
  
3. Si l’utilisateur dispose des informations d’identification appropriées, afficher l’onglet qui a été cliqué. Si l’utilisateur n’a pas d’informations d’identification appropriées, afficher une boîte de message ou certains autres interface utilisateur indiquant qu’ils ne pas avoir accès et revenir à l’onglet initial.  
  
    > [!NOTE]
    >  Lorsque vous implémentez cette fonctionnalité dans vos applications de production, vous pouvez effectuer cette vérification des informations d’identification au cours du formulaire <xref:System.Windows.Forms.Form.Load> événement. Cela vous permettra de masquer l’onglet avant l’affichage de n’importe quelle interface utilisateur, ce qui constitue une approche beaucoup plus propre de la programmation. La méthodologie utilisée ci-dessous (vérification des informations d’identification et la désactivation de l’onglet pendant la <xref:System.Windows.Forms.TabControl.SelectedIndexChanged> événement) est à titre d’illustration.  
  
4. Si vous le souhaitez, si vous avez plus de deux pages d’onglets, afficher une page différente de la version d’origine.  
  
     Dans l’exemple ci-dessous, un <xref:System.Windows.Forms.CheckBox> contrôle est utilisé à la place de la vérification les informations d’identification, comme critère pour l’accès à l’onglet varie par application. Lorsque le <xref:System.Windows.Forms.TabControl.SelectedIndexChanged> événement est déclenché si la vérification des informations d’identification a la valeur true (autrement dit, la case à cocher est activée) et l’onglet sélectionné est `TabPage2` (l’onglet avec les informations confidentielles, dans cet exemple), puis `TabPage2` s’affiche. Sinon, `TabPage3` s’affiche et une boîte de message est affichée à l’utilisateur, indiquant qu’ils ne disposait pas des privilèges d’accès appropriés. Le code ci-dessous illustre un formulaire avec un <xref:System.Windows.Forms.CheckBox> contrôle (`CredentialCheck`) et un <xref:System.Windows.Forms.TabControl> contrôle avec trois pages d’onglets.  
  
    ```vb  
    Private Sub TabControl1_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles TabControl1.SelectedIndexChanged  
       ' Check Credentials Here  
  
       If CredentialCheck.Checked = True And _   
       TabControl1.SelectedTab Is TabPage2 Then  
          TabControl1.SelectedTab = TabPage2  
       ElseIf CredentialCheck.Checked = False _   
       And TabControl1.SelectedTab Is TabPage2 Then  
          MessageBox.Show _   
         ("Unable to load tab. You have insufficient access privileges.")  
          TabControl1.SelectedTab = TabPage3  
       End If  
    End Sub  
    ```  
  
    ```csharp  
    private void tabControl1_SelectedIndexChanged(object sender, System.EventArgs e)  
    {  
        // Check Credentials Here  
  
        if ((CredentialCheck.Checked == true) && (tabControl1.SelectedTab == tabPage2))   
        {  
            tabControl1.SelectedTab = tabPage2;  
        }  
        else if ((CredentialCheck.Checked == false) && (tabControl1.SelectedTab == tabPage2))  
        {  
            MessageBox.Show("Unable to load tab. You have insufficient access privileges.");  
            tabControl1.SelectedTab = tabPage3;  
        }  
    }  
    ```  
  
    ```cpp  
    private:  
       System::Void tabControl1_SelectedIndexChanged(  
          System::Object ^ sender,  
          System::EventArgs ^  e)  
       {  
          // Check Credentials Here  
          if ((CredentialCheck->Checked == true) &&  
              (tabControl1->SelectedTab == tabPage2))  
          {  
             tabControl1->SelectedTab = tabPage2;  
          }  
          else if ((CredentialCheck->Checked == false) &&  
                   (tabControl1->SelectedTab == tabPage2))  
          {  
             MessageBox::Show(String::Concat("Unable to load tab. ",  
                "You have insufficient access privileges."));  
             tabControl1->SelectedTab = tabPage3;  
          }  
       }  
    ```  
  
     (Visual C#, Visual C++) Placez le code suivant dans le constructeur du formulaire pour inscrire le Gestionnaire d’événements.  
  
    ```csharp  
    this.tabControl1.SelectedIndexChanged +=   
       new System.EventHandler(this.tabControl1_SelectedIndexChanged);  
    ```  
  
    ```cpp  
    this->tabControl1->SelectedIndexChanged +=  
       gcnew System::EventHandler(this, &Form1::tabControl1_SelectedIndexChanged);  
    ```  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble du contrôle TabControl](tabcontrol-control-overview-windows-forms.md)
- [Guide pratique pour Ajouter un contrôle à une Page d’onglets](how-to-add-a-control-to-a-tab-page.md)
- [Guide pratique pour Ajouter et supprimer des onglets avec le contrôle TabControl de Windows Forms](how-to-add-and-remove-tabs-with-the-windows-forms-tabcontrol.md)
- [Guide pratique pour Modifier l’apparence du contrôle TabControl Windows Forms](how-to-change-the-appearance-of-the-windows-forms-tabcontrol.md)
