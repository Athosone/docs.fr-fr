---
title: Impossible d’obtenir le nom complet du système d’exploitation en raison d’une erreur interne
ms.date: 07/20/2015
f1_keywords:
- vbrDiagnosticInfo_FullOSName
ms.assetid: f69da02b-eb9a-4284-bb9e-3025517ae6c1
ms.openlocfilehash: ecbed5b59d36b1984c0b0ae161821ea99d28e090
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59334638"
---
# <a name="could-not-obtain-full-operation-system-name-due-to-internal-error"></a><span data-ttu-id="8cf8a-102">Impossible d’obtenir le nom complet du système d’exploitation en raison d’une erreur interne</span><span class="sxs-lookup"><span data-stu-id="8cf8a-102">Could not obtain full operation system name due to internal error</span></span>
<span data-ttu-id="8cf8a-103">Impossible d’obtenir le nom complet du système d’exploitation en raison d’une erreur interne.</span><span class="sxs-lookup"><span data-stu-id="8cf8a-103">Could not obtain full operation system name due to internal error.</span></span> <span data-ttu-id="8cf8a-104">Ceci peut être dû au fait que WMI est absent de l’ordinateur actuel.</span><span class="sxs-lookup"><span data-stu-id="8cf8a-104">This might be caused by WMI not existing on the current machine.</span></span>  
  
 <span data-ttu-id="8cf8a-105">Un appel à la propriété `My.Computer.Info.OSFullName` a échoué.</span><span class="sxs-lookup"><span data-stu-id="8cf8a-105">A call to the `My.Computer.Info.OSFullName` property failed.</span></span> <span data-ttu-id="8cf8a-106">WMI (Windows Management Instrumentation) n’est peut-être pas installé sur l’ordinateur actuel.</span><span class="sxs-lookup"><span data-stu-id="8cf8a-106">A possible cause for this failure is if Windows Management Instrumentation (WMI) is not installed on the current computer.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="8cf8a-107">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="8cf8a-107">To correct this error</span></span>  
  
1. <span data-ttu-id="8cf8a-108">Ajoutez un bloc `Try...Catch` autour de l’appel à la propriété `My.Computer.Info.OSFullName` .</span><span class="sxs-lookup"><span data-stu-id="8cf8a-108">Add a `Try...Catch` block around the call to the `My.Computer.Info.OSFullName` property.</span></span>  
  
2. <span data-ttu-id="8cf8a-109">Pour plus d’informations sur WMI et comment l’installer, accédez à et recherchez « Windows Management Instrumentation Core ».</span><span class="sxs-lookup"><span data-stu-id="8cf8a-109">For more information about WMI and how to install it, go to  and search for "Windows Management Instrumentation Core".</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8cf8a-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8cf8a-110">See also</span></span>

- [<span data-ttu-id="8cf8a-111">My.Computer.Info.OSFullName</span><span class="sxs-lookup"><span data-stu-id="8cf8a-111">My.Computer.Info.OSFullName</span></span>](xref:Microsoft.VisualBasic.Devices.ComputerInfo.OSFullName)
- [<span data-ttu-id="8cf8a-112">Gestion et levée d’exceptions dans .NET</span><span class="sxs-lookup"><span data-stu-id="8cf8a-112">Handling and throwing exceptions in .NET</span></span>](../../standard/exceptions/index.md)
- [<span data-ttu-id="8cf8a-113">Try...Catch...Finally (instruction)</span><span class="sxs-lookup"><span data-stu-id="8cf8a-113">Try...Catch...Finally Statement</span></span>](../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
