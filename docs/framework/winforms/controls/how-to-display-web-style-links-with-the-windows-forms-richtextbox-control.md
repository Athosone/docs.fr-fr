---
title: 'Procédure : afficher des liens de style web avec le contrôle RichTextBox Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- text boxes [Windows Forms], displaying Web links
- examples [Windows Forms], text boxes
- RichTextBox control [Windows Forms], linking to Web pages
ms.assetid: 95089a37-a202-4f7a-94ee-6ee312908851
ms.openlocfilehash: faaa48051c80b6dfd330f15f72a38297ff2d1b9f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61941581"
---
# <a name="how-to-display-web-style-links-with-the-windows-forms-richtextbox-control"></a>Procédure : afficher des liens de style web avec le contrôle RichTextBox Windows Forms
Les formulaires Windows <xref:System.Windows.Forms.RichTextBox> contrôle peut afficher des liens Web en couleur et souligné. Vous pouvez écrire du code qui ouvre une fenêtre de navigateur affichant le site Web spécifié dans le texte du lien lorsque l’utilisateur clique sur le lien.  
  
### <a name="to-link-to-a-web-page-with-the-richtextbox-control"></a>Pour lier à une page Web avec le contrôle RichTextBox  
  
1. Définir le <xref:System.Windows.Forms.RichTextBox.Text%2A> en une chaîne qui inclut une URL valide (par exemple, « http://www.microsoft.com/»).  
  
2. Assurez-vous que le <xref:System.Windows.Forms.RichTextBox.DetectUrls%2A> propriété est définie sur `true` (la valeur par défaut).  
  
3. Créer une nouvelle instance globale de la <xref:System.Diagnostics.Process> objet.  
  
4. Écrire un gestionnaire d’événements pour le <xref:System.Windows.Forms.RichTextBox.LinkClicked> événement qui envoie le navigateur le texte souhaité.  
  
     Dans l’exemple ci-dessous, le <xref:System.Windows.Forms.RichTextBox.LinkClicked> événement ouvre une instance d’Internet Explorer à l’URL spécifiée dans le <xref:System.Windows.Forms.RichTextBox.Text%2A> propriété de la <xref:System.Windows.Forms.RichTextBox> contrôle. Cet exemple suppose un formulaire avec un <xref:System.Windows.Forms.RichTextBox> contrôle.  
  
    > [!IMPORTANT]
    >  Dans l’appel la <xref:System.Diagnostics.Process.Start%2A?displayProperty=nameWithType> (méthode), vous rencontrerez un <xref:System.Security.SecurityException> exception si vous exécutez le code dans un contexte de confiance partielle en raison de privilèges insuffisants. Pour plus d’informations, consultez [Notions fondamentales de la sécurité d’accès du code](../../misc/code-access-security-basics.md).  
  
    ```vb  
    Public p As New System.Diagnostics.Process  
    Private Sub RichTextBox1_LinkClicked _  
       (ByVal sender As Object, ByVal e As _  
       System.Windows.Forms.LinkClickedEventArgs) _  
       Handles RichTextBox1.LinkClicked  
          ' Call Process.Start method to open a browser  
          ' with link text as URL.  
          p = System.Diagnostics.Process.Start("IExplore.exe", e.LinkText)  
    End Sub  
    ```  
  
    ```csharp  
    public System.Diagnostics.Process p = new System.Diagnostics.Process();  
  
    private void richTextBox1_LinkClicked(object sender,   
    System.Windows.Forms.LinkClickedEventArgs e)  
    {  
       // Call Process.Start method to open a browser  
       // with link text as URL.  
       p = System.Diagnostics.Process.Start("IExplore.exe", e.LinkText);  
    }  
    ```  
  
    ```cpp  
    public:  
       System::Diagnostics::Process ^ p;  
  
    private:  
       void richTextBox1_LinkClicked(System::Object ^  sender,  
          System::Windows::Forms::LinkClickedEventArgs ^  e)  
       {  
          // Call Process.Start method to open a browser  
          // with link text as URL.  
          p = System::Diagnostics::Process::Start("IExplore.exe",  
             e->LinkText);  
       }  
    ```  
  
     ([!INCLUDE[vcprvc](../../../../includes/vcprvc-md.md)]) Vous devez initialiser le processus `p`, ce que vous pouvez faire en incluant l’instruction suivante dans le constructeur de votre formulaire :  
  
    ```cpp  
    p = gcnew System::Diagnostics::Process();  
    ```  
  
     (Visual c#, [!INCLUDE[vcprvc](../../../../includes/vcprvc-md.md)]) placez le code suivant dans le constructeur du formulaire pour inscrire le Gestionnaire d’événements.  
  
    ```csharp  
    this.richTextBox1.LinkClicked += new   
       System.Windows.Forms.LinkClickedEventHandler  
       (this.richTextBox1_LinkClicked);  
    ```  
  
    ```cpp  
    this->richTextBox1->LinkClicked += gcnew  
       System::Windows::Forms::LinkClickedEventHandler  
       (this, &Form1::richTextBox1_LinkClicked);  
    ```  
  
     Il est important d’arrêter immédiatement le processus que vous avez créé une fois que vous avez fini de travailler avec lui. Qui fait référence au code présenté ci-dessus, votre code pour arrêter le processus peut ressembler à ceci :  
  
    ```vb  
    Public Sub StopWebProcess()  
       p.Kill()  
    End Sub  
    ```  
  
    ```csharp  
    public void StopWebProcess()  
    {  
       p.Kill();  
    }  
    ```  
  
    ```cpp  
    public: void StopWebProcess()  
    {  
       p->Kill();  
    }  
    ```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.RichTextBox.DetectUrls%2A>
- <xref:System.Windows.Forms.RichTextBox.LinkClicked>
- <xref:System.Windows.Forms.RichTextBox>
- [RichTextBox, contrôle](richtextbox-control-windows-forms.md)
- [Contrôles à utiliser dans les Windows Forms](controls-to-use-on-windows-forms.md)
