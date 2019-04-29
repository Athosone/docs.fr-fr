---
title: IEnumRAWINPUTDEVICE
ms.date: 03/30/2017
helpviewer_keywords:
- IEnumRAWINPUTDEVICE interface [WPF]
ms.assetid: 88c8b389-a48b-46b9-b895-8ed7b1e26fea
ms.openlocfilehash: 04caca0c580d26fde7fc9a3e3a11b7a8fed26d65
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61949563"
---
# <a name="ienumrawinputdevice"></a><span data-ttu-id="79b8f-102">IEnumRAWINPUTDEVICE</span><span class="sxs-lookup"><span data-stu-id="79b8f-102">IEnumRAWINPUTDEVICE</span></span>
<span data-ttu-id="79b8f-103">Cette interface énumère les périphériques d'entrée brute ; elle est uniquement utilisée par PresentationHost.exe.</span><span class="sxs-lookup"><span data-stu-id="79b8f-103">This interface enumerates the raw input devices, and is only used by PresentationHost.exe.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="79b8f-104">Cette API est conçue et pris en charge uniquement sur l'ordinateur client local</span><span class="sxs-lookup"><span data-stu-id="79b8f-104">This API is only intended and supported for use on the local client machine</span></span>  
  
## <a name="members"></a><span data-ttu-id="79b8f-105">Membres</span><span class="sxs-lookup"><span data-stu-id="79b8f-105">Members</span></span>  
  
|<span data-ttu-id="79b8f-106">Membre</span><span class="sxs-lookup"><span data-stu-id="79b8f-106">Member</span></span>|<span data-ttu-id="79b8f-107">Description</span><span class="sxs-lookup"><span data-stu-id="79b8f-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="79b8f-108">IEnumRAWINPUTDEVIC:Next</span><span class="sxs-lookup"><span data-stu-id="79b8f-108">IEnumRAWINPUTDEVIC:Next</span></span>](ienumrawinputdevic-next.md)|<span data-ttu-id="79b8f-109">Énumère les éléments `celt` suivants (c'est-à-dire les structures RAWINPUTDEVICE) dans la liste de l'énumérateur, en les retournant dans `rgelt` avec le nombre réel d'éléments énumérés dans `pceltFetched`.</span><span class="sxs-lookup"><span data-stu-id="79b8f-109">Enumerates the next `celt` elements (that is, RAWINPUTDEVICE structures) in the enumerator's list, returning them in `rgelt` along with the actual number of enumerated elements in `pceltFetched`.</span></span>|  
|[<span data-ttu-id="79b8f-110">IEnumRAWINPUTDEVIC:Skip</span><span class="sxs-lookup"><span data-stu-id="79b8f-110">IEnumRAWINPUTDEVIC:Skip</span></span>](ienumrawinputdevic-skip.md)|<span data-ttu-id="79b8f-111">Demande à l’énumérateur d’ignorer les `celt` éléments dans l’énumération afin que l’appel suivant à [IEnumRAWINPUTDEVIC:Next](ienumrawinputdevic-next.md) ne retourne pas ces éléments.</span><span class="sxs-lookup"><span data-stu-id="79b8f-111">Instructs the enumerator to skip the next `celt` elements in the enumeration so that the next call to [IEnumRAWINPUTDEVIC:Next](ienumrawinputdevic-next.md) will not return those elements.</span></span>|  
|[<span data-ttu-id="79b8f-112">IEnumRAWINPUTDEVIC:Reset</span><span class="sxs-lookup"><span data-stu-id="79b8f-112">IEnumRAWINPUTDEVIC:Reset</span></span>](ienumrawinputdevic-reset.md)|<span data-ttu-id="79b8f-113">Réinitialise la séquence d'énumération au début.</span><span class="sxs-lookup"><span data-stu-id="79b8f-113">Resets the enumeration sequence to the beginning.</span></span>|  
|[<span data-ttu-id="79b8f-114">IEnumRAWINPUTDEVIC:Clone</span><span class="sxs-lookup"><span data-stu-id="79b8f-114">IEnumRAWINPUTDEVIC:Clone</span></span>](ienumrawinputdevic-clone.md)|<span data-ttu-id="79b8f-115">Crée un autre énumérateur de périphériques d'entrée brute avec le même état que l'énumérateur actif pour itérer au sein de la même liste.</span><span class="sxs-lookup"><span data-stu-id="79b8f-115">Creates another raw input device enumerator with the same state as the current enumerator to iterate over the same list.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="79b8f-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79b8f-116">See also</span></span>

- [<span data-ttu-id="79b8f-117">À propos des entrées brutes</span><span class="sxs-lookup"><span data-stu-id="79b8f-117">About Raw Input</span></span>](/windows/desktop/inputdev/about-raw-input)
