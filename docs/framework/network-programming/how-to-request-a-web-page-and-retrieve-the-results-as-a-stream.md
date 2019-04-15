---
title: 'Procédure : demander une page web et récupérer les résultats sous forme de flux'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d32b7f35-29d8-4fb7-ad71-d219edc5e359
ms.openlocfilehash: 23c094f0a3f528750c9589dbc99a0ada86236967
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59097198"
---
# <a name="how-to-request-a-web-page-and-retrieve-the-results-as-a-stream"></a><span data-ttu-id="c9104-102">Procédure : demander une page web et récupérer les résultats sous forme de flux</span><span class="sxs-lookup"><span data-stu-id="c9104-102">How to: Request a Web Page and Retrieve the Results as a Stream</span></span>
<span data-ttu-id="c9104-103">Cet exemple montre comment demander une page web et récupérer les résultats sous forme de flux.</span><span class="sxs-lookup"><span data-stu-id="c9104-103">This example shows how to request a Web page and retrieve the results in a stream.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c9104-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="c9104-104">Example</span></span>  
  
```csharp  
WebClient myClient = new WebClient();  
Stream response = myClient.OpenRead("http://www.contoso.com/index.htm");  
// The stream data is used here.  
response.Close();  
```  
  
```vb  
Dim myClient As WebClient = New WebClient()  
Dim response As Stream = myClient.OpenRead("http://www.contoso.com/index.htm")  
' The stream data is used here.  
response.Close()  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="c9104-105">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="c9104-105">Compiling the Code</span></span>  
 <span data-ttu-id="c9104-106">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="c9104-106">This example requires:</span></span>  
  
-   <span data-ttu-id="c9104-107">Références aux espaces de noms <xref:System.IO> et <xref:System.Net>.</span><span class="sxs-lookup"><span data-stu-id="c9104-107">References to the <xref:System.IO> and <xref:System.Net> namespaces.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c9104-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9104-108">See also</span></span>

- [<span data-ttu-id="c9104-109">Demande de données</span><span class="sxs-lookup"><span data-stu-id="c9104-109">Requesting Data</span></span>](../../../docs/framework/network-programming/requesting-data.md)
