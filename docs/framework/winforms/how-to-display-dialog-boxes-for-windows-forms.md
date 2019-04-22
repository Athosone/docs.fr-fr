---
title: 'Procédure : afficher des boîtes de dialogue pour Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Windows Forms, displaying
- Windows Forms dialog boxes [Windows Forms], displaying
- Windows Forms, calling one form from another
- dialog boxes [Windows Forms], displaying for Windows Forms
ms.assetid: aaac1b38-c651-495a-8d3d-5a9bfb32fee3
ms.openlocfilehash: b99f2273dae88faf86448da6e1d2986a83803abf
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59773816"
---
# <a name="how-to-display-dialog-boxes-for-windows-forms"></a><span data-ttu-id="95038-102">Procédure : afficher des boîtes de dialogue pour Windows Forms</span><span class="sxs-lookup"><span data-stu-id="95038-102">How to: Display Dialog Boxes for Windows Forms</span></span>
<span data-ttu-id="95038-103">Afficher une boîte de dialogue de la même façon que vous affichez toute autre forme dans une application.</span><span class="sxs-lookup"><span data-stu-id="95038-103">You display a dialog box in the same way you display any other form in an application.</span></span> <span data-ttu-id="95038-104">Le formulaire de démarrage est chargé automatiquement lors de l’application est exécutée.</span><span class="sxs-lookup"><span data-stu-id="95038-104">The startup form loads automatically when the application is run.</span></span> <span data-ttu-id="95038-105">Pour rendre un deuxième formulaire ou la boîte de dialogue s’affichent dans l’application, écrire du code pour charger et l’afficher.</span><span class="sxs-lookup"><span data-stu-id="95038-105">To make a second form or dialog box appear in the application, write code to load and display it.</span></span> <span data-ttu-id="95038-106">De même, pour rendre le formulaire ou la boîte de dialogue zone disparaissent, écrire du code pour décharger ou le masquer.</span><span class="sxs-lookup"><span data-stu-id="95038-106">Similarly, to make the form or dialog box disappear, write code to unload or hide it.</span></span>  
  
### <a name="to-display-a-dialog-box"></a><span data-ttu-id="95038-107">Pour afficher une boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="95038-107">To display a dialog box</span></span>  
  
1. <span data-ttu-id="95038-108">Accédez au gestionnaire d’événements avec lequel vous souhaitez ouvrir la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="95038-108">Navigate to the event handler with which you want to open the dialog box.</span></span> <span data-ttu-id="95038-109">Cela peut se produire lorsqu’une commande de menu est sélectionnée, lorsqu’un clic est effectué, ou tout autre événement se produit.</span><span class="sxs-lookup"><span data-stu-id="95038-109">This can happen when a menu command is selected, when a button is clicked, or when any other event occurs.</span></span>  
  
2. <span data-ttu-id="95038-110">Dans le Gestionnaire d’événements, ajoutez le code pour ouvrir la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="95038-110">In the event handler, add code to open the dialog box.</span></span> <span data-ttu-id="95038-111">Dans cet exemple, un événement de clic de bouton est utilisé pour afficher la boîte de dialogue :</span><span class="sxs-lookup"><span data-stu-id="95038-111">In this example, a button-click event is used to show the dialog box:</span></span>  
  
    ```vb  
    Private Sub Button1_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button1.Click  
       Dim dlg1 as new Form()  
       dlg1.ShowDialog()  
    End Sub  
    ```  
  
    ```csharp  
    private void button1_Click(object sender, System.EventArgs e)   
    {  
       Form dlg1 = new Form();  
       dlg1.ShowDialog();  
    }  
    ```  
  
    ```cpp  
    private:   
      void button1_Click(System::Object ^ sender,  
        System::EventArgs ^ e)  
      {  
        Form ^ dlg1 = gcnew Form();  
        dlg1->ShowDialog();  
      }  
    ```
