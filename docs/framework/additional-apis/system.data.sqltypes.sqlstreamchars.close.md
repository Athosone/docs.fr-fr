---
title: Méthode SqlStreamChars.Close (System.Data.SqlTypes)
author: stevestein
ms.author: sstein
ms.date: 12/20/2018
ms.technology: dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.Close
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: d0c29bbc5c6bea98cf36e3c2b6bf7825d6843ccc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61705868"
---
# <a name="sqlstreamcharsclose-method"></a><span data-ttu-id="70e33-102">SqlStreamChars.Close (méthode)</span><span class="sxs-lookup"><span data-stu-id="70e33-102">SqlStreamChars.Close Method</span></span>

<span data-ttu-id="70e33-103">Ferme le flux actuel et libère toutes les ressources système associées au flux.</span><span class="sxs-lookup"><span data-stu-id="70e33-103">Closes the current stream and releases any system resources associated with the stream.</span></span> <span data-ttu-id="70e33-104">L’assembly qui contient cette méthode a une relation de friend avec SQLAccess.dll.</span><span class="sxs-lookup"><span data-stu-id="70e33-104">The assembly that contains this method has a friend relationship with SQLAccess.dll.</span></span> <span data-ttu-id="70e33-105">Il est prévu pour une utilisation par SQL Server.</span><span class="sxs-lookup"><span data-stu-id="70e33-105">It's intended for use by SQL Server.</span></span><span data-ttu-id="70e33-106"> Pour les autres bases de données, utilisez le mécanisme d’hébergement fourni par cette base de données.</span><span class="sxs-lookup"><span data-stu-id="70e33-106"> For other databases, use the hosting mechanism provided by that database.</span></span>

```csharp
public virtual void Close ();
```

## <a name="remarks"></a><span data-ttu-id="70e33-107">Notes</span><span class="sxs-lookup"><span data-stu-id="70e33-107">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="70e33-108">Le `SqlStreamChars.Close` méthode est privée et qu’il n’est pas destiné à être utilisé directement dans votre code.</span><span class="sxs-lookup"><span data-stu-id="70e33-108">The `SqlStreamChars.Close` method is private and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="70e33-109">Microsoft ne prend pas en charge l’utilisation de ce champ dans une application de production en toute circonstance.</span><span class="sxs-lookup"><span data-stu-id="70e33-109">Microsoft does not support the use of this field in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="70e33-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70e33-110">Requirements</span></span>

<span data-ttu-id="70e33-111">**Espace de noms :** <xref:System.Data.SqlTypes></span><span class="sxs-lookup"><span data-stu-id="70e33-111">**Namespace:** <xref:System.Data.SqlTypes></span></span>

<span data-ttu-id="70e33-112">**Assembly :** System.Data (dans System.Data.dll)</span><span class="sxs-lookup"><span data-stu-id="70e33-112">**Assembly:** System.Data (in System.Data.dll)</span></span>

<span data-ttu-id="70e33-113">**Versions du .NET framework :** Disponible à partir de 2.0.</span><span class="sxs-lookup"><span data-stu-id="70e33-113">**.NET Framework versions:** Available since 2.0.</span></span>