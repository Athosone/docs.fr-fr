---
title: 'Procédure : déterminer les propriétés de la page à l’aide du composant PageSetupDialog'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- page properties
- page setup
- PageSetupDialog component
ms.assetid: 6dae05bc-c0fd-4357-bb93-841a1631d98f
ms.openlocfilehash: 7c65eb54bb95b9a20cd1e43f0d491af47985f2e0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59329204"
---
# <a name="how-to-determine-page-properties-using-the-pagesetupdialog-component"></a><span data-ttu-id="403ab-102">Procédure : déterminer les propriétés de la page à l’aide du composant PageSetupDialog</span><span class="sxs-lookup"><span data-stu-id="403ab-102">How to: Determine Page Properties Using the PageSetupDialog Component</span></span>
<span data-ttu-id="403ab-103">Le composant [PageSetupDialog](pagesetupdialog-component-windows-forms.md) présente des options de disposition, de format du papier et d’autres choix de mise en page à l’utilisateur pour un document.</span><span class="sxs-lookup"><span data-stu-id="403ab-103">The [PageSetupDialog](pagesetupdialog-component-windows-forms.md) component presents layout, paper size, and other page layout choices to the user for a document.</span></span>  
  
 <span data-ttu-id="403ab-104">Vous devez spécifier une instance de la classe <xref:System.Drawing.Printing.PrintDocument> ; il s’agit du document à imprimer.</span><span class="sxs-lookup"><span data-stu-id="403ab-104">You need to specify an instance of the <xref:System.Drawing.Printing.PrintDocument> class—this is the document to be printed.</span></span> <span data-ttu-id="403ab-105">De plus, les utilisateurs doivent avoir une imprimante installée sur leur ordinateur, localement ou sur un réseau, car c’est en partie comme cela que le composant <xref:System.Windows.Forms.PageSetupDialog> détermine les choix de mise en page présentés à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="403ab-105">Additionally, users must have a printer installed on their computer, either locally or through a network, as this is partly how the <xref:System.Windows.Forms.PageSetupDialog> component determines the page formatting choices presented to the user.</span></span>  
  
 <span data-ttu-id="403ab-106">L’interaction entre le composant <xref:System.Windows.Forms.PageSetupDialog> et la classe <xref:System.Drawing.Printing.PageSettings> constitue l’un des aspects importants de son utilisation.</span><span class="sxs-lookup"><span data-stu-id="403ab-106">An important aspect of working with the <xref:System.Windows.Forms.PageSetupDialog> component is how it interacts with the <xref:System.Drawing.Printing.PageSettings> class.</span></span> <span data-ttu-id="403ab-107">La classe <xref:System.Drawing.Printing.PageSettings> sert à spécifier des paramètres qui modifient la façon dont une page est imprimée, comme l’orientation du papier, le format de la page et les marges.</span><span class="sxs-lookup"><span data-stu-id="403ab-107">The <xref:System.Drawing.Printing.PageSettings> class is used to specify settings that modify the way a page will be printed, such as paper orientation, the size of the page, and the margins.</span></span> <span data-ttu-id="403ab-108">Chacun de ces paramètres est représenté en tant que propriété de la classe <xref:System.Drawing.Printing.PageSettings> .</span><span class="sxs-lookup"><span data-stu-id="403ab-108">Each of these settings is represented as a property of the <xref:System.Drawing.Printing.PageSettings> class.</span></span> <span data-ttu-id="403ab-109">La classe <xref:System.Windows.Forms.PageSetupDialog> modifie ces valeurs de propriétés pour une instance donnée de la classe <xref:System.Drawing.Printing.PageSettings> associée au document (et représentée en tant que propriété <xref:System.Drawing.Printing.PrintDocument.DefaultPageSettings%2A> ).</span><span class="sxs-lookup"><span data-stu-id="403ab-109">The <xref:System.Windows.Forms.PageSetupDialog> class modifies these property values for a given instance of the <xref:System.Drawing.Printing.PageSettings> class that is associated with the document (and is represented as a <xref:System.Drawing.Printing.PrintDocument.DefaultPageSettings%2A> property).</span></span>  
  
### <a name="to-set-page-properties-using-the-pagesetupdialog-component"></a><span data-ttu-id="403ab-110">Pour définir les propriétés de la page à l’aide du composant PageSetupDialog</span><span class="sxs-lookup"><span data-stu-id="403ab-110">To set page properties using the PageSetupDialog component</span></span>  
  
1. <span data-ttu-id="403ab-111">Utilisez la méthode <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> pour afficher la boîte de dialogue, en spécifiant le <xref:System.Drawing.Printing.PrintDocument> à utiliser.</span><span class="sxs-lookup"><span data-stu-id="403ab-111">Use the <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> method to display the dialog box, specifying the <xref:System.Drawing.Printing.PrintDocument> to use.</span></span>  
  
     <span data-ttu-id="403ab-112">Dans l’exemple ci-dessous, le gestionnaire d’événements <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Click> ouvre une instance du composant <xref:System.Windows.Forms.PageSetupDialog> .</span><span class="sxs-lookup"><span data-stu-id="403ab-112">In the example below, the <xref:System.Windows.Forms.Button> control's <xref:System.Windows.Forms.Control.Click> event handler opens an instance of the <xref:System.Windows.Forms.PageSetupDialog> component.</span></span> <span data-ttu-id="403ab-113">Un document existant est spécifié dans la propriété <xref:System.Windows.Forms.PageSetupDialog.Document%2A> , et sa propriété <xref:System.Drawing.Printing.PageSettings.Color%2A?displayProperty=nameWithType> prend la valeur `false`.</span><span class="sxs-lookup"><span data-stu-id="403ab-113">An existing document is specified in the <xref:System.Windows.Forms.PageSetupDialog.Document%2A> property, and its <xref:System.Drawing.Printing.PageSettings.Color%2A?displayProperty=nameWithType> property is set to `false`.</span></span>  
  
     <span data-ttu-id="403ab-114">L’exemple suppose que votre formulaire contient un <xref:System.Windows.Forms.Button> contrôle, un <xref:System.Drawing.Printing.PrintDocument> composant nommé `myDocument`et un <xref:System.Windows.Forms.PageSetupDialog> composant.</span><span class="sxs-lookup"><span data-stu-id="403ab-114">The example assumes your form has a <xref:System.Windows.Forms.Button> control, a <xref:System.Drawing.Printing.PrintDocument> component named `myDocument`, and a <xref:System.Windows.Forms.PageSetupDialog> component.</span></span>  
  
    ```vb  
    Private Sub Button1_Click(ByVal sender As System.Object, _  
    ByVal e As System.EventArgs) Handles Button1.Click  
       ' The print document 'myDocument' used below  
       ' is merely for an example.  
       'You will have to specify your own print document.  
       PageSetupDialog1.Document = myDocument  
       ' Sets the print document's color setting to false,  
       ' so that the page will not be printed in color.  
       PageSetupDialog1.Document.DefaultPageSettings.Color = False  
       PageSetupDialog1.ShowDialog()  
    End Sub  
    ```  
  
    ```csharp  
    private void button1_Click(object sender, System.EventArgs e)  
    {  
       // The print document 'myDocument' used below  
       // is merely for an example.  
       // You will have to specify your own print document.  
       pageSetupDialog1.Document = myDocument;  
       // Sets the print document's color setting to false,  
       // so that the page will not be printed in color.  
       pageSetupDialog1.Document.DefaultPageSettings.Color = false;  
       pageSetupDialog1.ShowDialog();  
    }  
    ```  
  
    ```cpp  
    private:  
       System::Void button1_Click(System::Object ^  sender,  
          System::EventArgs ^  e)  
       {  
          // The print document 'myDocument' used below  
          // is merely for an example.  
          // You will have to specify your own print document.  
          pageSetupDialog1->Document = myDocument;  
          // Sets the print document's color setting to false,  
          // so that the page will not be printed in color.  
          pageSetupDialog1->Document->DefaultPageSettings->Color = false;  
          pageSetupDialog1->ShowDialog();  
       }  
    ```  
  
     <span data-ttu-id="403ab-115">(Visual c# et [!INCLUDE[vcprvc](../../../../includes/vcprvc-md.md)]) placez le code suivant dans le constructeur du formulaire pour inscrire le Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="403ab-115">(Visual C# and [!INCLUDE[vcprvc](../../../../includes/vcprvc-md.md)]) Place the following code in the form's constructor to register the event handler.</span></span>  
  
    ```csharp  
    this.button1.Click += new System.EventHandler(this.button1_Click);  
    ```  
  
    ```cpp  
    this->button1->Click += gcnew   
       System::EventHandler(this, &Form1::button1_Click);  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="403ab-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="403ab-116">See also</span></span>

- <xref:System.Windows.Forms.PageSetupDialog>
- [<span data-ttu-id="403ab-117">Guide pratique pour Créer des travaux d’impression Standard de Windows Forms</span><span class="sxs-lookup"><span data-stu-id="403ab-117">How to: Create Standard Windows Forms Print Jobs</span></span>](../advanced/how-to-create-standard-windows-forms-print-jobs.md)
- [<span data-ttu-id="403ab-118">PageSetupDialog, composant</span><span class="sxs-lookup"><span data-stu-id="403ab-118">PageSetupDialog Component</span></span>](pagesetupdialog-component-windows-forms.md)
