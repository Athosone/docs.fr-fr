---
title: IAssemblyCacheItem::CreateStream, méthode
ms.date: 03/30/2017
api_name:
- IAssemblyCacheItem.CreateStream
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyCacheItem::CreateStream
helpviewer_keywords:
- CreateStream method [.NET Framework fusion]
- IAssemblyCacheItem::CreateStream method [.NET Framework fusion]
ms.assetid: 697ab0f4-470c-4baa-a415-4a975c42d0d5
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 380e248c8c4e3407fff868cdd9a5c63b63e50c69
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61697511"
---
# <a name="iassemblycacheitemcreatestream-method"></a><span data-ttu-id="6e7eb-102">IAssemblyCacheItem::CreateStream, méthode</span><span class="sxs-lookup"><span data-stu-id="6e7eb-102">IAssemblyCacheItem::CreateStream Method</span></span>

<span data-ttu-id="6e7eb-103">Crée un flux avec le format et le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="6e7eb-103">Creates a stream with the specified name and format.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e7eb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e7eb-104">Syntax</span></span>

```cpp
HRESULT CreateStream (
    [in]  DWORD dwFlags,
    [in]  LPCWSTR pszStreamName,
    [in]  DWORD dwFormat,
    [in]  DWORD dwFormatFlags,
    [out] IStream **ppIStream,
    [in, optional] ULARGE_INTEGER *puliMaxSize
);
```

## <a name="parameters"></a><span data-ttu-id="6e7eb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e7eb-105">Parameters</span></span>

`dwFlags`\
<span data-ttu-id="6e7eb-106">[in] Indicateurs définis dans Fusion.idl.</span><span class="sxs-lookup"><span data-stu-id="6e7eb-106">[in] Flags defined in Fusion.idl.</span></span>

`pszStreamName`\
<span data-ttu-id="6e7eb-107">[in] Le nom du flux doit être créé.</span><span class="sxs-lookup"><span data-stu-id="6e7eb-107">[in] The name of the stream to be created.</span></span>

`dwFormat`\
<span data-ttu-id="6e7eb-108">[in] Le format du fichier à être diffusé en continu.</span><span class="sxs-lookup"><span data-stu-id="6e7eb-108">[in] The format of the file to be streamed.</span></span>

`dwFormatFlags`\
<span data-ttu-id="6e7eb-109">[in] Indicateurs spécifiques au format définis dans Fusion.idl.</span><span class="sxs-lookup"><span data-stu-id="6e7eb-109">[in] Format-specific flags defined in Fusion.idl.</span></span>

`ppIStream`\
<span data-ttu-id="6e7eb-110">[out] Un pointeur vers l’adresse de retourné [IStream](/windows/desktop/api/objidl/nn-objidl-istream) instance.</span><span class="sxs-lookup"><span data-stu-id="6e7eb-110">[out] A pointer to the address of the returned [IStream](/windows/desktop/api/objidl/nn-objidl-istream) instance.</span></span>

`puliMaxSize`\
<span data-ttu-id="6e7eb-111">[in, optional] La taille maximale du flux référencé par `ppIStream`.</span><span class="sxs-lookup"><span data-stu-id="6e7eb-111">[in, optional] The maximum size of the stream referenced by `ppIStream`.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e7eb-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e7eb-112">Requirements</span></span>

<span data-ttu-id="6e7eb-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6e7eb-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>

<span data-ttu-id="6e7eb-114">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="6e7eb-114">**Header:** Fusion.h</span></span>

<span data-ttu-id="6e7eb-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6e7eb-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="6e7eb-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e7eb-116">See also</span></span>

- [<span data-ttu-id="6e7eb-117">IAssemblyCacheItem, interface</span><span class="sxs-lookup"><span data-stu-id="6e7eb-117">IAssemblyCacheItem Interface</span></span>](iassemblycacheitem-interface.md)