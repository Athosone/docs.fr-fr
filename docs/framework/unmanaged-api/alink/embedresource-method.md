---
title: EmbedResource, méthode
ms.date: 03/30/2017
api_name:
- IALink.EmbedResource
- EmbedResource
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EmbedResource
helpviewer_keywords:
- EmbedResource method
ms.assetid: 667bd954-6dc6-4020-a3cb-0e8224179993
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ef7d6272c04c3edab8ef652bcb2759861ff2b982
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61790050"
---
# <a name="embedresource-method"></a><span data-ttu-id="a4b1a-102">EmbedResource, méthode</span><span class="sxs-lookup"><span data-stu-id="a4b1a-102">EmbedResource Method</span></span>
<span data-ttu-id="a4b1a-103">Déclare une ressource incorporée.</span><span class="sxs-lookup"><span data-stu-id="a4b1a-103">Declares an embedded resource.</span></span> <span data-ttu-id="a4b1a-104">Cette méthode n’incorpore pas réellement la ressource.</span><span class="sxs-lookup"><span data-stu-id="a4b1a-104">This method does not actually embed the resource.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a4b1a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4b1a-105">Syntax</span></span>  
  
```  
HRESULT EmbedResource(  
    mdAssembly  AssemblyID,  
    mdToken     FileToken,  
    LPCWSTR     pszResourceName,  
    DWORD       dwOffset,  
    DWORD       dwFlags  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="a4b1a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4b1a-106">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="a4b1a-107">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="a4b1a-107">ID of the assembly.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="a4b1a-108">ID de jeton ou l’assembly du fichier qui contient la ressource de fichier.</span><span class="sxs-lookup"><span data-stu-id="a4b1a-108">File token or assembly ID of file that contains the resource.</span></span>  
  
 `pszResourceName`  
 <span data-ttu-id="a4b1a-109">Nom de la ressource.</span><span class="sxs-lookup"><span data-stu-id="a4b1a-109">Name of the resource.</span></span>  
  
 `dwOffset`  
 <span data-ttu-id="a4b1a-110">Décalage de la ressource à partir de l’adresse RVA.</span><span class="sxs-lookup"><span data-stu-id="a4b1a-110">Offset of resource from RVA.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="a4b1a-111">Accessibilité indicateurs tels que `mrPublic` et `mrPrivate`.</span><span class="sxs-lookup"><span data-stu-id="a4b1a-111">Accessibility flags such as `mrPublic` and `mrPrivate`.</span></span> <span data-ttu-id="a4b1a-112">Ces indicateurs peuvent être passés à [DefineExportedType, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineexportedtype-method.md).</span><span class="sxs-lookup"><span data-stu-id="a4b1a-112">These flags may be passed to [DefineExportedType Method](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineexportedtype-method.md).</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a4b1a-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a4b1a-113">Return Value</span></span>  
 <span data-ttu-id="a4b1a-114">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="a4b1a-114">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a4b1a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4b1a-115">Requirements</span></span>  
 <span data-ttu-id="a4b1a-116">Nécessite alink.h.</span><span class="sxs-lookup"><span data-stu-id="a4b1a-116">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a4b1a-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4b1a-117">See also</span></span>

- [<span data-ttu-id="a4b1a-118">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="a4b1a-118">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="a4b1a-119">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="a4b1a-119">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="a4b1a-120">API ALink</span><span class="sxs-lookup"><span data-stu-id="a4b1a-120">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
