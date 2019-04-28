---
title: 'Procédure : accéder à la source HTML dans le modèle objet de document HTML managé'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- managed HTML DOM
- HTML [Windows Forms], accessing in Windows Forms
ms.assetid: 53db79fa-8a5e-448e-88c2-f54ace3860b6
ms.openlocfilehash: f2306e3405aa0ff37060d987bdc82b58fbaa7784
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62011266"
---
# <a name="how-to-access-the-html-source-in-the-managed-html-document-object-model"></a><span data-ttu-id="3d9dc-102">Procédure : accéder à la source HTML dans le modèle objet de document HTML managé</span><span class="sxs-lookup"><span data-stu-id="3d9dc-102">How to: Access the HTML Source in the Managed HTML Document Object Model</span></span>
<span data-ttu-id="3d9dc-103">Les propriétés <xref:System.Windows.Forms.WebBrowser.DocumentStream%2A> et <xref:System.Windows.Forms.WebBrowser.DocumentText%2A> sur le contrôle <xref:System.Windows.Forms.WebBrowser> renvoient le code HTML du document actif comme il était quand il a été affiché pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="3d9dc-103">The <xref:System.Windows.Forms.WebBrowser.DocumentStream%2A> and <xref:System.Windows.Forms.WebBrowser.DocumentText%2A> properties on the <xref:System.Windows.Forms.WebBrowser> control return the HTML of the current document as it existed when it was first displayed.</span></span> <span data-ttu-id="3d9dc-104">Toutefois, si vous modifiez la page à l'aide des appels de méthode et de propriété tels que <xref:System.Windows.Forms.HtmlElement.AppendChild%2A> et <xref:System.Windows.Forms.HtmlElement.InnerHtml%2A>, ces modifications n'apparaissent pas quand vous appelez <xref:System.Windows.Forms.WebBrowser.DocumentStream%2A> et <xref:System.Windows.Forms.WebBrowser.DocumentText%2A>.</span><span class="sxs-lookup"><span data-stu-id="3d9dc-104">However, if you modify the page using method and property calls such as <xref:System.Windows.Forms.HtmlElement.AppendChild%2A> and <xref:System.Windows.Forms.HtmlElement.InnerHtml%2A>, these changes will not appear when you call <xref:System.Windows.Forms.WebBrowser.DocumentStream%2A> and <xref:System.Windows.Forms.WebBrowser.DocumentText%2A>.</span></span> <span data-ttu-id="3d9dc-105">Pour obtenir le code source HTML le plus à jour pour le modèle DOM, vous devez appeler la propriété <xref:System.Windows.Forms.HtmlElement.OuterHtml%2A> sur l'élément HTML.</span><span class="sxs-lookup"><span data-stu-id="3d9dc-105">To obtain the most up-to-date HTML source for the DOM, you must call the <xref:System.Windows.Forms.HtmlElement.OuterHtml%2A> property on the HTML element.</span></span>  
  
 <span data-ttu-id="3d9dc-106">La procédure suivante illustre comment récupérer la source dynamique et l'afficher dans un menu contextuel distinct.</span><span class="sxs-lookup"><span data-stu-id="3d9dc-106">The following procedure shows how to retrieve the dynamic source and display it in a separate shortcut menu.</span></span>  
  
### <a name="retrieving-the-dynamic-source-with-the-outerhtml-property"></a><span data-ttu-id="3d9dc-107">Récupération de la source dynamique avec la propriété OuterHtml</span><span class="sxs-lookup"><span data-stu-id="3d9dc-107">Retrieving the dynamic source with the OuterHtml property</span></span>  
  
1. <span data-ttu-id="3d9dc-108">Créez une application Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="3d9dc-108">Create a new Windows Forms application.</span></span> <span data-ttu-id="3d9dc-109">Démarrer avec un seul <xref:System.Windows.Forms.Form>et appelez-le `Form1`.</span><span class="sxs-lookup"><span data-stu-id="3d9dc-109">Start with a single <xref:System.Windows.Forms.Form>, and call it `Form1`.</span></span>  
  
2. <span data-ttu-id="3d9dc-110">Hôte du <xref:System.Windows.Forms.WebBrowser> contrôler dans votre application Windows Forms et nommez-le `WebBrowser1`.</span><span class="sxs-lookup"><span data-stu-id="3d9dc-110">Host the <xref:System.Windows.Forms.WebBrowser> control in your Windows Forms application, and name it `WebBrowser1`.</span></span> <span data-ttu-id="3d9dc-111">Pour plus d'informations, voir [Procédure : Ajouter des fonctionnalités de navigateur Web à une Application de formulaires Windows](how-to-add-web-browser-capabilities-to-a-windows-forms-application.md).</span><span class="sxs-lookup"><span data-stu-id="3d9dc-111">For more information, see [How to: Add Web Browser Capabilities to a Windows Forms Application](how-to-add-web-browser-capabilities-to-a-windows-forms-application.md).</span></span>  
  
3. <span data-ttu-id="3d9dc-112">Créez une deuxième <xref:System.Windows.Forms.Form> dans votre application appelé `CodeForm`.</span><span class="sxs-lookup"><span data-stu-id="3d9dc-112">Create a second <xref:System.Windows.Forms.Form> in your application called `CodeForm`.</span></span>  
  
4. <span data-ttu-id="3d9dc-113">Ajouter un <xref:System.Windows.Forms.RichTextBox> le contrôle à `CodeForm` et définissez son <xref:System.Windows.Forms.Control.Dock%2A> propriété `Fill`.</span><span class="sxs-lookup"><span data-stu-id="3d9dc-113">Add a <xref:System.Windows.Forms.RichTextBox> control to `CodeForm` and set its <xref:System.Windows.Forms.Control.Dock%2A> property to `Fill`.</span></span>  
  
5. <span data-ttu-id="3d9dc-114">Créez une propriété publique sur `CodeForm` appelée `Code`.</span><span class="sxs-lookup"><span data-stu-id="3d9dc-114">Create a public property on `CodeForm` called `Code`.</span></span>  
  
     [!code-csharp[DisplayWebBrowserCode#1](~/samples/snippets/csharp/VS_Snippets_Winforms/DisplayWebBrowserCode/CS/CodeForm.cs#1)]
     [!code-vb[DisplayWebBrowserCode#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/DisplayWebBrowserCode/VB/CodeForm.vb#1)]  
  
6. <span data-ttu-id="3d9dc-115">Ajouter un <xref:System.Windows.Forms.Button> contrôle nommé `Button1` à votre <xref:System.Windows.Forms.Form>et surveillez le <xref:System.Windows.Forms.Control.Click> événement.</span><span class="sxs-lookup"><span data-stu-id="3d9dc-115">Add a <xref:System.Windows.Forms.Button> control named `Button1` to your <xref:System.Windows.Forms.Form>, and monitor for the <xref:System.Windows.Forms.Control.Click> event.</span></span> <span data-ttu-id="3d9dc-116">Pour plus d’informations sur la surveillance des événements, consultez [événements](../../../standard/events/index.md).</span><span class="sxs-lookup"><span data-stu-id="3d9dc-116">For details on monitoring events, see [Events](../../../standard/events/index.md).</span></span>  
  
7. <span data-ttu-id="3d9dc-117">Ajoutez le code ci-après au gestionnaire d'événements <xref:System.Windows.Forms.Control.Click>.</span><span class="sxs-lookup"><span data-stu-id="3d9dc-117">Add the following code to the <xref:System.Windows.Forms.Control.Click> event handler.</span></span>  
  
     [!code-csharp[DisplayWebBrowserCode#2](~/samples/snippets/csharp/VS_Snippets_Winforms/DisplayWebBrowserCode/CS/Form1.cs#2)]
     [!code-vb[DisplayWebBrowserCode#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/DisplayWebBrowserCode/VB/Form1.vb#2)]  
  
## <a name="robust-programming"></a><span data-ttu-id="3d9dc-118">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="3d9dc-118">Robust Programming</span></span>  
 <span data-ttu-id="3d9dc-119">Testez systématiquement la valeur de <xref:System.Windows.Forms.WebBrowser.Document%2A> avant d'essayer de le récupérer.</span><span class="sxs-lookup"><span data-stu-id="3d9dc-119">Always test the value of <xref:System.Windows.Forms.WebBrowser.Document%2A> before attempting to retrieve it.</span></span> <span data-ttu-id="3d9dc-120">Si le chargement de la page active n'est pas terminé, l'initialisation de <xref:System.Windows.Forms.WebBrowser.Document%2A> ou de ses objets enfants peut éventuellement ne pas se produire.</span><span class="sxs-lookup"><span data-stu-id="3d9dc-120">If the current page is not finished loading, <xref:System.Windows.Forms.WebBrowser.Document%2A> or one or more of its child objects may not be initialized.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3d9dc-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d9dc-121">See also</span></span>

- [<span data-ttu-id="3d9dc-122">Utilisation du modèle DOM HTML managé</span><span class="sxs-lookup"><span data-stu-id="3d9dc-122">Using the Managed HTML Document Object Model</span></span>](using-the-managed-html-document-object-model.md)
- [<span data-ttu-id="3d9dc-123">Vue d’ensemble du contrôle WebBrowser</span><span class="sxs-lookup"><span data-stu-id="3d9dc-123">WebBrowser Control Overview</span></span>](webbrowser-control-overview.md)
