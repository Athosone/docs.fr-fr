---
title: My.Response (objet) (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- My.MyWebExtension.Response
- My.Response
helpviewer_keywords:
- My.Response object
ms.assetid: 626359bc-3165-40b4-bfaf-2c610e26eb5b
ms.openlocfilehash: 2f72f493d99c1e0b0469150c041649486e5ed124
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58818993"
---
# <a name="myresponse-object"></a><span data-ttu-id="2e218-102">My.Response, objet</span><span class="sxs-lookup"><span data-stu-id="2e218-102">My.Response Object</span></span>
<span data-ttu-id="2e218-103">Obtient le <xref:System.Web.HttpResponse> objet associé à la <xref:System.Web.UI.Page>.</span><span class="sxs-lookup"><span data-stu-id="2e218-103">Gets the <xref:System.Web.HttpResponse> object associated with the <xref:System.Web.UI.Page>.</span></span> <span data-ttu-id="2e218-104">Cet objet vous permet d’envoyer des données de réponse HTTP à un client et contient des informations relatives à cette réponse.</span><span class="sxs-lookup"><span data-stu-id="2e218-104">This object allows you to send HTTP response data to a client and contains information about that response.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2e218-105">Notes</span><span class="sxs-lookup"><span data-stu-id="2e218-105">Remarks</span></span>  
 <span data-ttu-id="2e218-106">Le `My.Response` objet contient actuel <xref:System.Web.HttpResponse> objet associé à la page.</span><span class="sxs-lookup"><span data-stu-id="2e218-106">The `My.Response` object contains the current <xref:System.Web.HttpResponse> object associated with the page.</span></span>  
  
 <span data-ttu-id="2e218-107">Le `My.Response` objet est disponible uniquement pour [!INCLUDE[vstecasp](~/includes/vstecasp-md.md)] applications.</span><span class="sxs-lookup"><span data-stu-id="2e218-107">The `My.Response` object is only available for [!INCLUDE[vstecasp](~/includes/vstecasp-md.md)] applications.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2e218-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="2e218-108">Example</span></span>  
 <span data-ttu-id="2e218-109">L’exemple suivant obtient la collection d’en-têtes à partir de la `My.Request` objet et utilise le `My.Response` objet à écrire dans la page ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="2e218-109">The following example gets the header collection from the `My.Request` object and uses the `My.Response` object to write it to the ASP.NET page.</span></span>  
  
 [!code-vb[VbVbalrMyWeb#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyWeb/VB/Default.aspx#1)]  
  
## <a name="see-also"></a><span data-ttu-id="2e218-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e218-110">See also</span></span>

- <xref:System.Web.HttpResponse>
- [<span data-ttu-id="2e218-111">My.Request (objet)</span><span class="sxs-lookup"><span data-stu-id="2e218-111">My.Request Object</span></span>](../../../visual-basic/language-reference/objects/my-request-object.md)
