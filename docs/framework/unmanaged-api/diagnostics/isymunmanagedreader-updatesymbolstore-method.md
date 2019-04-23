---
title: ISymUnmanagedReader::UpdateSymbolStore, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.UpdateSymbolStore
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::UpdateSymbolStore
helpviewer_keywords:
- UpdateSymbolStore method [.NET Framework debugging]
- ISymUnmanagedReader::UpdateSymbolStore method [.NET Framework debugging]
ms.assetid: 4a17d723-86b9-4f27-bd0d-b70c3259011c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f62c954bf9d73ab564eba388e742794a330362d4
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59080499"
---
# <a name="isymunmanagedreaderupdatesymbolstore-method"></a><span data-ttu-id="e29c6-102">ISymUnmanagedReader::UpdateSymbolStore, méthode</span><span class="sxs-lookup"><span data-stu-id="e29c6-102">ISymUnmanagedReader::UpdateSymbolStore Method</span></span>
<span data-ttu-id="e29c6-103">Met à jour le magasin de symboles existant avec un magasin de symboles delta.</span><span class="sxs-lookup"><span data-stu-id="e29c6-103">Updates the existing symbol store with a delta symbol store.</span></span> <span data-ttu-id="e29c6-104">Cette méthode est utilisée dans les scénarios modifier et continuer pour mettre à jour le magasin de symboles pour correspondre aux deltas avec le fichier exécutable portable d’origine (PE).</span><span class="sxs-lookup"><span data-stu-id="e29c6-104">This method is used in edit-and-continue scenarios to update the symbol store to match deltas to the original portable executable (PE) file.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e29c6-105">Vous devez spécifier un seul de le `filename` ou `pIStream` paramètres, pas les deux.</span><span class="sxs-lookup"><span data-stu-id="e29c6-105">You need specify only one of the `filename` or `pIStream` parameters, not both.</span></span> <span data-ttu-id="e29c6-106">Si `filename` est spécifié, le magasin de symboles sera actualisée avec les symboles dans ce fichier.</span><span class="sxs-lookup"><span data-stu-id="e29c6-106">If `filename` is specified, the symbol store will be updated with the symbols in that file.</span></span> <span data-ttu-id="e29c6-107">Si `pIStream` est spécifié, le magasin sera actualisé avec les données à partir de la <xref:System.Runtime.InteropServices.ComTypes.IStream>.</span><span class="sxs-lookup"><span data-stu-id="e29c6-107">If `pIStream` is specified, the store will be updated with the data from the <xref:System.Runtime.InteropServices.ComTypes.IStream>.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e29c6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e29c6-108">Syntax</span></span>  
  
```  
HRESULT UpdateSymbolStore (  
    [in] const WCHAR *filename,  
    [in] IStream *pIStream);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e29c6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e29c6-109">Parameters</span></span>  
 `filename`  
 <span data-ttu-id="e29c6-110">[in] Le nom du fichier qui contient le magasin de symboles.</span><span class="sxs-lookup"><span data-stu-id="e29c6-110">[in] The name of the file that contains the symbol store.</span></span>  
  
 `pIStream`  
 <span data-ttu-id="e29c6-111">[in] Le flux de fichier, utilisé comme alternative à le `filename` paramètre.</span><span class="sxs-lookup"><span data-stu-id="e29c6-111">[in] The file stream, used as an alternative to the `filename` parameter.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e29c6-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e29c6-112">Return Value</span></span>  
 <span data-ttu-id="e29c6-113">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e29c6-113">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e29c6-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e29c6-114">Requirements</span></span>  
 <span data-ttu-id="e29c6-115">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="e29c6-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e29c6-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e29c6-116">See also</span></span>

- [<span data-ttu-id="e29c6-117">ISymUnmanagedReader, interface</span><span class="sxs-lookup"><span data-stu-id="e29c6-117">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
